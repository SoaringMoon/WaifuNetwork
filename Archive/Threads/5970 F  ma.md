# 1
Alright mathematicians/physicians report in. Us Plebeians need your honest help to create robowaifus in beginner's terms. How do we make our robowaifus properly dance with us at the Royal Ball?

>tl;dr
Surely in the end it will be the laws of physic and not mere hyperbole that brings us all real robowaifus in the end. Moar maths kthx.

# 2
>>7777
Not a mathematician (electronics engineer), but would certainly like a ballroom dancing bot.
Used to do ballroom dancing at uni and must say, having a perfect follower be the best. To dance Viennese waltz with my robo-waifu.... <3
The best thing is probably to start with a simple self-balancing robot, look at some existing projects, analyse the inverse pendulum problem.

# 3
>>7777
>>7786
Same anon.
Did a quick search and saw this interesting article:
https://ctms.engin.umich.edu/CTMS/index.php?example=InvertedPendulum&section=SystemModeling

For control systems you need calculus, linear algebra, complex numbers knowledge. By analysing your problem (in the article's case, a kart with an inverse pnedulum), you can find if the system is stable. Unstable systems will experience a large change in position, speed etc. with a small input (imagine nudging an upright domino for example).

# 4
>>7786
>analyse the inverse pendulum problem.
This. Specifically, we need a both forward- and inverse-kinematics solver system that will work on the multi-jointed bipedal complex of hips/knees/ankles/feet. This solver should at the least be able to address a steady-state mass affixed directly centered above the pelvis (the so called center of gravity in a typical humanoid) and allow for walking.

This central mass is the 'inverse pendulum' and the solver must address successfully the complex just mentioned.

# 5
>>7786
>Ballroom dancing robot
Does it have to have legs or can it just roll about on wheels? Because I reckon a robot skidding about the ballroom will be much easier. Just call it a new style!

(P.S. can ya tell I know nothing about ballroom dancing? :D)

# 6
>>7786
>but would certainly like a ballroom dancing bot.
Seconded. What if /robowaifu/ were to focus explicitly and specifically on solving that single problem alone Anon? Wouldn't we in many practical ways be advancing the much bigger set of general motion solutions for robowaifus across the entire spectrum? 

Surely ballroom dancing represents a domain that really pushes the envelope of sophisticated, discriminating humanoid bodily motion, yet without going to real extremes like robowaifu gymnasts or qt3.14 robowaifu enforcers. Seems like a relatively balanced goal for us that is a real achievement in itself, but not too unreachable conceptually overall.

# 7
related xpost, I think.
>>7825

# 8
>>7802
>...about on wheels? Because I reckon a robot skidding...
That could be a good solution to start with.

One of the requirements for dancing Viennese Waltz without getting too tired, is to maintain close contact and move past each other instead of trying to rotate. The cool thing is that the motion looks like continuous spinning when really you're stepping forward through your partner and doing a 180 degree turn and then repeat the action this time moving backwards. Do this cleanly enough and fast enough (6/8 timing music is FAST xD), then it will look like quite beautiful, the couple moving around on the floor.
In practice, I rarely had a gal that I clicked well enough well enough with (and who cared as much about the dance as I did) to actually make Viennese waltz work. Basic form of this dance has the simplest steps, but one of the most difficult techniques.

So mechanical legs are still probably necessary for such a fit (though may be wheels could be used where the feet would be?)

>can ya tell I know nothing about ballroom dancing? :D
I'll be honest, quite a niche hobby indeed XD

>>7811
I like you thinking. I'm in a similar boat in that, I want a robo-waifu to entertain me (by communication and dancing). Other features are not necessary to me. So as you point out, developments should happen in parallel and in different areas. Perhaps much further down the line functionality could be combined (though I would not sacrifice ballroom abilihy for much else :P) Perhaps if we agreed on a common "personality core", which could be attached to different robo-waifu models, depending on the required task. Still get to have *your* waifu, just the outer hardware changes.


>>7830
Thanks, I'll give it a read later.

# 9
I'm using the videos of StatQuest (Josh Starmer) to learn about statistics and more: https://youtube.com/c/joshstarmer
Here the basics: https://youtube.com/playlist?list=PLblh5JKOoLUK0FLuzwntyYI10UQFUhsY9

# 10
>>9065
I also want to recommend "Nudge Algebra" app for repeating some basic math skills, to prevent forgetting them, or for relearning if that already happened.

# 11
I'm going to look into this problem. I'll start by trying to understand how to model physical controls in a scalable way. If anyone wants to join me, I'm starting off by reading through the two books below. I plan to post regular updates and explanations as I make my way through the first book. If you have questions about anything I post, feel free to ask.

Human-like Biomechanics
https://link.springer.com/book/10.1007/978-1-4020-4116-4
This book provides an approach for modeling physical action and perception in a way that supposedly scales to human-level complexity.

Referent control of action and perception
https://link.springer.com/book/10.1007/978-1-4939-2736-4
This book is very grounded, it points out a lot of practical problems with common approaches, and it offers solutions that seem reasonable. In particular, >>7788, it argues against inverse dynamics models because they introduce a lot of complexity when feedback gets involved, and so they don't scale well. This book looks good for grounding and philosophy, but I believe the first book is necessary to turn the ideas here into something that can actually be implemented.

# 12
>>14784
If the formatting doesn't work here, paste this post into a markdown editor like https://stackedit.io/app#. If you have VS Code installed, that has a built-in markdown editor.
If you want to understand this but have trouble following, let me know what the difficulty is. I assume some familiarity with calculus and linear algebra, at least enough to do basic neural network stuff.

The introductory section is on modeling forces. There are some prerequisites:
- Differential forms. These represent infinitesimal spaces. A 1-form is an infinitesimal length, a 2-form is an infinitesimal area, a 3-form is an infinitesimal volume. One of the first things the book does is draw a distinction between absolute derivatives, vectors, and differential 1-forms.
- Einstein summation notation. As far I can tell, this notation is NOT precise, meaning one equation in Einstein notation can mean multiple things. I think it's supposed to be shorthand, not mathematically rigorous. The terms involved are usually not abelian (meaning A*B is not always the same as B*A), but the author seems to swap them freely for notation's sake. Maybe this is a problem with the author rather than the notation.

I guess the first step is to model forces. This is done with the Hamiltonian equation of motion.
$H(q,p) = \frac{1}{2m}||p||^2 + V(q)$
- H(q,p) is "total energy". q is position, p is momentum. From this form, the important part is that there are two sources of energy: one that is fully determined by the position, and one that is fully determined by the momentum.
- Total energy should be constant for a given system, so energy can transfer between V(q) (potential energy) and p^2/2m (kinetic energy). Every change in one of these terms comes from a change in the arguments.

That's the motivation for the next two equations:
$\dot{q} = \frac{\partial H}{\partial p} = \partial_p H$
$\dot{p} = -\frac{\partial H}{\partial q} = \partial_q H$

Where the dot over a symbol refers to the time derivative. These two equations show that changes in position and momentum fully determine one another, which is an hint that complex numbers are going to get involved. If changes in position in momentum *didn't* fully determine one another, we would be using normal vectors to represent these quantities since they would need to be modeled independently. Since they do determine one another, we can treat them as the x and y variables of the Cauchy-Riemann equations (https://en.wikipedia.org/wiki/Cauchy%E2%80%93Riemann_equations). The constraints of those equations can be represented implicitly by saying that the position and momentum are the real and imaginaries parts of complex numbers, and that the Hamiltonian is *complex differentiable* (as opposed to the normal kind of differentiable).

The author decides to just use bigger matrices instead of complex numbers though.
$\xi = (q,p)$
$J = \binom{0 \quad I}{-I \quad 0}$
$\dot \xi = J \cdot grad_\xi(H)$

$\xi$ now represents the combined position and momentum. J is the stand-in for the square-root of negative 1 (but in matrix form. Now the change in position-momentum is given by the gradient of H. If you're familiar with neural networks, you can now figure out how the system evolves by doing something like gradient descent on H. The only difference is that instead of following -1 times the gradient, you follow J times the gradient.

The $\dot{q}$ equation is the velocity equation (since velocity is change in position with respect to time). The $\dot{p}$ equation is the force equation (since force is change in momentum with respect to time). These equations in total show how the two relate to one another, like in the Hill's muscle model https://en.wikipedia.org/wiki/Hill%27s_muscle_model. As a general principle, any non-conservative forces (like the relationship between a neuron and a muscle) should be added to the force side of the equation to represent translational (meaning non-rotational) biomechanics. I think the same principle should apply to rotational biomechanics, but I'll find out as I read more.

# 13
>>7777
Holy get

Protip: There is already a calculator or formula for almost any physics problem you can imagine. Here is a really good calculator to determine speed and power requirements for wheeled robots. Walking will always require more power. Self balancing will also require more power and always use power just to stand up.
https://www.robotshop.com/community/blog/show/drive-motor-sizing-tool
I personally like using Google Sheets as a calculator as it is feature rich and inherently accessible to almost any machine with a web browser. This link can help you get started with making custom formulas.
https://edu.gcfglobal.org/en/googlespreadsheets/creating-simple-formulas/1/

# 14
>>14785
The next section introduces *metric tensors*. A metric tensor tells you how to measure vectors and relationships between vectors. In practice, that means lengths and angles. I think this is important because different components of a system can measure lengths and angles differently, and sometimes a single component might change how it measures these things based on some state. These situations can be modeled as changes to metric tensors.

A metric tensor is a linear, symmetric function that takes two vectors as input and produces a scalar as output. This means you can think of it as a symmetric matrix that takes a vector on the left and a vector on the right, then returns the result of multiplying everything together.

$g(v,w) = v^\dagger gw$

(I'm being a little sloppy here by treating g as both a function and a matrix. It should be unambiguous though.)

I'm using $\dagger$ to mean "transpose". For any AI people here, I'll try to be consistent about treating a vector $k$ as a column vector and $k^\dagger$ as a row vector / linear operator.

It's symmetric because metric tensors represent degree-2 polynomials (same as a normal dot product, which not-coincidentally is also used to measure lengths and angles), and in a polynomial, the coefficient for $a b$ is the same as the coefficient for $b a$.

As I mentioned, dot products can be used to measure lengths and angles. When a metric tensor is involved, it is implicit in all dot products. That means $v \cdot w = g(v, w) = v^\dagger g w$. For lengths, $v \cdot v = g(v, v) = v^\dagger g v = |v|^2$. In a euclidean space, g is an identity matrix.

The next part is on configuration spaces, which are used to represent the state of a system. There are two main points here:
- A configuration may be represented by more variables than it has degrees of freedom, meaning some variable settings impose constraints on other variable settings.
- The exact same configuration subspace might be represented by two different sets of variables. This would happen when, for example, two components jointly affect a configuration variable but when they measure that variable in different ways.

The implication is that configuration subspaces are related to one another, and that's something we need to model. These relationships can be represented by functions. For example, if $q'^k$ is determined by $q^j$

$q'^k = q'^k(q^j)$

(The book and I are both being sloppy here by treating $q'^k$ as both a point-or-vector-or-metric-tensor and as function that maps things from the $q^j$ subspace into the $q'^k$ subspace. It's assumed here that there is only one correct way to do this.)

One important thing here is that the function $q'^k$ "knows" how to convert points, vectors, and metric tensors. In other words, it can map *enough* stuff that anyone looking at $q^j$ from the lens of $q'^k$ can make sense of all the quantities necessary to understand how the $q'^k$ slice of the system is affected by $q^j$.

After that is a section on inertia, which I'm having a very hard time following. See the pic. I'm putting down my best guess for what it means, but I'm not confident in my explanation. If someone here can understand it better, please do explain.

There are two relevant quantities here: the (scalar) moment of inertia and the (non-scalar) inertia tensor. The (scalar) moment of inertia gives the conversion from *angular velocity* to *angular momentum* through the following equation:

$L = I(\lambda) \omega$

Where L is the angular momentum, I is moment of inertia, $\lambda$ is the axis of rotation, and $\omega$ is the angular velocity. The *inertia tensor* (the second relevant quantity) makes the dependence onf $\lambda$ linear.

$I_m(\lambda) = \lambda^\dagger I_t \lambda$

Where $I_m$ is the (scalar) moment of inertia, $\lambda^\dagger$ is the transpose of $\lambda$ (the axis of rotation), and $I_t$ is the inertia tensor. (For AI people, I'll try to be consistent about treating a vector $k$ as a column vector, and $k^\dagger$ is a row vector.) Keep in mind that all dot products on the right-hand side are done with respect to the metric tensor. With the dot products expanded out (and keeping in mind that $g = g^\dagger$ since g is symmetric), it would look like:

$I_m(\lambda) = \lambda^\dagger g I_t g \lambda$

The actual value of the inertia tensor is given by:

$\sum mass_p \cdot (g x_p) (x_p^\dagger g)$

With x representing the position of a particle relative to some origin and g representing the metric tensor as usual. This says that the inertia tensor depends linearly on mass and quadratically on each coordinate relative to some origin. Fully expanded, the relationship between the moment of inertia and the inertia tensor looks like this:

$I_m(\lambda) = (\lambda^\dagger g x_p) (x_p^\dagger g \lambda)$

Skipping ahead a bit, the author points out that joints are by nature rotational. The whole point of modeling muscle forces is to figure out how they get transformed to create torque 1-forms, which do all the actual work in a body. For joints, this makes sense. Maybe for dancing, this would be sufficient. In the more general case, we'll need more than torque to model motions that aren't based on joints, like face movements.

# 15
>>14790
>See the pic
It might be easier to see if I actually upload it.

# 16
>>14790
>>14791
>$I_m(\lambda) = \lambda^\dagger g I_t g \lambda$
>Fully expanded, the relationship between the moment of inertia and the inertia tensor looks like this:
>$I_m(\lambda) = (\lambda^\dagger g x_p) (x_p^\dagger g \lambda)$
I got this wrong. Here's the actual relationship between the moment of inertia and the metric tensor:
$I_m(\lambda) = \lambda^\dagger (g x_p^\dagger x_p g - x_p g g x_p^\dagger) \lambda$

With implicit metric tensors:
$I_m(\lambda) = \lambda^\dagger (x_p^\dagger x_p - x_p x_p^\dagger) \lambda$

I don't have a great intuition for that middle term. It's measuring a failure to commute (i.e., the extent to which ab is not equal to ba). Since:
- All matrices can be written as a product of scaling, mirroring, and rotation matrices,
- Scaling matrices commute, and
- Mirroring matrices are disallowed by the fact that g is positive definite,

It intuitively makes sense that the middle term would measure rotation, but the exact details aren't clear to me. I'm going to move on for now.

# 17
>>14784
>>14785
>>14790
>>14804
I find this extremely gratifying to know you are researching this area for us Anon. This will surely prove to be a vital area for all of us to solve. I wish I could follow along with you, but I simply don't have the maths experience yet. At some point perhaps there might be some collaborations on creating the actual software to perform these calculations for our robowaifus in a fast, efficient way on modest hardware? 

Hopefully so. But regardless, please press forward with your research efforts! We'll be watching your progress attentively here.

# 18
>>14943
I want to make these posts more accessible to people with less math experience. The goal for a lot of this is to build intuition for how to construct more complex interactions. The new intuition isn't that useful if it's given to only a few people.

I guess as a general note for anyone reading: if you want to understand this but have trouble doing so, let me know what your math & physics background is, and let me know the first point where you felt like you were in over your head. I've assumed familiarity with calculus and linear algebra. I won't be able to give an overview of those topics, but I can at least point you in the right direction if you haven't studied these things, and I can answer questions about these topics to help you understand them more intuitively. Note that calculus and linear algebra are the same prerequisites for creating deep neural networks, so if you want to work on algorithms for AI or robotics, it's good to study those two topics.

>>14804
Sorry for the long lag between posts. I'll have a bit more time for these posts in a few weeks.
See pic for my translation of the next chunk. If you're having trouble with the markdown in the previous posts, I can convert those to images like this one.

# 19
>>15002

Ah, physics. I am familiar with calculus and remember some physics forumlas. Those classes had put these equations into more readable forms and often used derivatives of these and explained why. Linear algebra is something I’ve never heard of.

# 20
>>15003
>Those classes had put these equations into more readable forms and often used derivatives of these and explained why.
You were doing classical mechanics, right? Velocity is the time-derivative of position, acceleration is the time-derivative of velocity. Force is the time-derivative of momentum, and energy is the space-integral of force. These equations are simple as long as you're not doing anything too complicated with angular momentum. I think this is one of the main reason why the equations that people study in, e.g., high school, are so much simpler than the ones used later on.
The problem with angular momentum is that it involves a lot of interaction between spatial dimensions. That's something linear algebra is great at modeling, but, in linear algebra, a*b is not always the same thing as b*a. This same phenomenon shows up in physics. You might remember that with a cross product, which is one form of multiplication covered by linear algebra, a cross b is equal to the negative of b cross a. That's one of the "nice" cases. In more general cases, a*b can be related to b*a in more complicated ways.
When things like the order of operations matters, it becomes much more pressing to model your dynamics using a single equation. If you don't, it becomes very difficult to keep track of how you're supposed to merge equations to get the actual dynamics, especially as your system gets larger. With simpler systems, you can usually intuit how to account for changes in perspective manually. With more complex systems, you need to model the relationships between perspectives explicitly, otherwise there's no hope of being able to put them into a single equation.

So that's what the more abstract versions of these equations do. They let you model angular momentum better, and they let you merge equations more systematically. Lagrangian Mechanics tells you how you can create one giant equation to model everything, and it does so in a way that makes it easy to figure out the parts of the dynamics you actually care about. That's basically what we're doing. Hamiltonian Mechanics is just some slick way to simplify the equations further and to understand some of the variables involved better.

Most of the complexity comes from the fact that the order of operations matters, which is why I need to say things like:
Kinetic energy = 1/2 v'Gv
Instead of:
Kinetic energy = 1/2 mv^2
The second equation works when an object is moving in a straight line and when your sensors are calibrated so velocity is measured the same way in all directions. It doesn't work when you have angular velocity. The first equation always works.

>Linear algebra is something I’ve never heard of.
You might have heard of vectors and matrices. Linear algebra is all about vectors and transformations of vectors. (A matrix is how you represent a transformation of vectors.) Vectors are important because it's how we represent changes in coordinates, and more generally any direction with a magnitude. For example, a velocity has a direction and magnitude, so it can be represented by a vector. The same is true for acceleration, force, and momentum. A matrix is a way of transforming vectors through rotating, streching, shrinking, flipping (like through a mirror), and any combination of these things.
If you want an intro to linear algebra, I would highly recommend 3blue1brown's video series on the topic:
https://www.youtube.com/watch?v=fNk_zzaMoSs&list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab

# 21
>>15011



>When things like the order of operations matters, it becomes much more pressing to model your dynamics using a single equation.



Though in some cases, mostly comparisons, its important to be able to clearly model the relationships between different functions. 



>So that's what the more abstract versions of these equations do. They let you model angular momentum better, and they let you merge equations more systematically. 



>Most of the complexity comes from the fact that the order of operations matters, which is why I need to say things like:



Thank you for reminding me of some of the formulas I had forgotten about. Derivatives are a vital concept and can't tell if you meant 1/2(v*Gv) or if you meant it to be another ^ sign.



>You might have heard of vectors and matrices.

Yes I have.  Though they were not really featured all that heavily at all. Its more helpful when programming a robowaifu's spatial recognition than anything.

# 22
>>15016
>Though in some cases, mostly comparisons, its important to be able to clearly model the relationships between different functions. 
Exactly, but the specifics should be encapsulated in a way that the rest of the system can just pull the information it needs without needing to worry about how each module models its relationships. If something does need to be explicitly exposed to the rest of the system, like which volume that can be quickly grasped by a hand, it should be exposed as an optional value for other system modules to consume. Special functions and variables should never be required to predict common things, like the trajectory of a module.
For this particular book, the Hamiltonian is the "one equation" that each module needs to expose. It takes in a momentum, position, and potential field as input, and it returns total energy. Assuming something is keeping track of positions and momenta, this is enough to calculate how any module will change over time, and what candidate changes need to be applied to get a module to change in a particular way.
One unintuitive aspect of this is that it's not quite appropriate to try to control a system using forces directly. The problem with using forces directly is that every time something doesn't go exactly as expected, you need to recalculate how much force to apply. The "right" way to control a system seems to be through a potential field. A potential field tells you how much force to apply for every position that an object can be in. This lets you control things more smoothly, and as long as you don't end up creating some really chaotic dynamics, it should get you to the end state you want without requiring you to recalculate your trajectory every time something goes slightly wrong. The amount of force to apply should be calculated from the Hamiltonian: it's the partial derivative of the Hamiltonian with respect to position. So if you want to move the hand to a particular location, you should create some function that with a minimum at that location. From that function, you can caculate what for the apply no matter what position the hand is in, and that function can remain unchanged until the objective changes.
There are a plenty of frameworks that do automatic differentiation, some numerically and some symbolically, and implementing it should be relatively easy on the small chance that we need to do it ourselves.
I still need to spend more time thinking about how to make this more concrete and how to support all of the sorts of flexibility we would want in a dancing robowife, but the big picture that this book paints seems compelling.

>Derivatives are a vital concept and can't tell if you meant 1/2(v*Gv) or if you meant it to be another ^ sign.
You got it right. Sorry, I forgot that ' (apostraphe) usually means "derivative" and * (asterisk) usually means "transpose". The meaning of the symbols changes across fields, and it's hard to keep track of sometimes. The dot-over-the-variable-for-derivative in >>15002 comes from the book, and it seems common in physics. The cross-(dagger)-for-transpose comes from a particular branch of math. I think the apostrophe-for-derivative and asterisk-for-transpose notation was much more common when I studied physics and calculus in school. If that makes my summaries easier to read, I can switch my notation to that.

>You might have heard of vectors and matrices.
>Yes I have.  Though they were not really featured all that heavily at all. Its more helpful when programming a robowaifu's spatial recognition than anything.
I think the first time I used them in practice was for game development. Matrices and vectors show up there because it's much easier to model parts of an object from their own relative positions and have the parent object keep track of their reference frames. To render a parent object, the parent "switches" to the reference frame of each child object in turn and has the child render itself. This is possible because the game engine keeps track of a matrix that's used to automatically transform every vector the child uses. When any object multiplies the game engine's matrix with its own matrix, it's effectively changing the perspective used for rendering. So for a parent to switch to the child's perspective, it only needs to change the matrix that the game engine uses while rendering the child.
The same thing is going on here. The g and G matrices in >>15002 play a very similar role to the game engine's matrix.

# 23
>>15002
Please pardon the methodical multi-responses. I personally find it conducive to disconnected, async communications (often separated by days in my case) with Anons when I want to be thorough.
>I want to make these posts more accessible to people with less math experience.
Thank you! That's the only real hope I might have for following along.
>The goal for a lot of this is to build intuition for how to construct more complex interactions. 
I kind of already have some of that. Both from my basic intellectual abilities, and from my programming experiences.
>The new intuition isn't that useful if it's given to only a few people.
So true. One of our goals here on /robowaifu/ is to make it reasonable and feasible for ''every-man'' to construct their own robot wives, as they see fit. Simplification of necessary complexity is a given.

>I guess as a general note for anyone reading: if you want to understand this but have trouble doing so, let me know what your math & physics background is, and let me know the first point where you felt like you were in over your head.
< and let me know the first point where you felt like you were in over your head.
Lol, but there are so many! Primarily it's to do with unfamiliarity with math notations. I dropped out of school very early, and never got much by way of maths notation. My programming experience is entirely self-taught.
>I've assumed familiarity with calculus and linear algebra.
I understand the basic concepts behind integration and derivatives, but that's it. Just the basics. As for LinAlg, I grasp the basic ideas of Matrix and Vector operations, but again, very basic. I did however manage to piece together a few test case programs that would properly do matrix multiplications, etc.

>I won't be able to give an overview of those topics, but I can at least point you in the right direction if you haven't studied these things, and I can answer questions about these topics to help you understand them more intuitively. 
Again, thank you.
>Note that calculus and linear algebra are the same prerequisites for creating deep neural networks, so if you want to work on algorithms for AI or robotics, it's good to study those two topics.
Of that I'm quite sure. Further, I want us to actually '''__implement__''' the code algorithms for doing so! :^)

BTW, I could follow the topics slightly better with the image you provided here for this post, so yes I personally would welcome you do so for others.

# 24
>>15011
>Velocity is the time-derivative of position, acceleration is the time-derivative of velocity. Force is the time-derivative of momentum, and energy is the space-integral of force.
Let me try to restate these as questions in my own words, and please evaluate my understanding, Maths-Anon.

''Velocity'' is an expression of the instantaneous 'change' in position from one time point to another?

''Acceleration'' is an expression of the instantaneous 'change' in Velocity from one time point to another?

''Force'' is an expression of the instantaneous 'change' in Momentum **Lol, w/e ''that'' is** from one time point to another?

''Energy'' is an expression of the total Force 's acting across a given volume?

# 25
>>15018
>so yes I personally would welcome you do so for others.
BTW I'd like ''both'' the image + the written text, if reasonable.

# 26
>>15020

It's hard to find a medium that will support everything. Colab seems like the best option right now since it supports markdown with embedded mathjax, and it will show both the rendered text and, when double-clicking a cell, the source text. If it ends up being useful, I can also add code examples in the script to make things more concrete.



I updated my previous posts to use the new notation:

- https://colab.research.google.com/drive/1kxQDLDL--WyFsTHEyXCdY1xOOrv1vEG1?usp=sharing



I plan to keep that "script" up-to-date with future posts here.

# 27
>>15167
Thanks for your response and for your efforts in this area Anon. It's much appreciated!

# 28
>>15019

That's correct. Note that the "volume" for energy should be 1-dimensional, like a path. I added an explanation to the script in >>15167, same as the attached image. Here's the text description.

---



Objects move around and rotate in space. Every object has a position in that space, a mass, and a velocity.

- The velocity describes the instantaneous change ($d/dt$) in position.

- These quantities also define a momentum, which is $mass * velocity$. Momentum is a representation of how much an object resists slowing down to zero velocity. Momentum increases with mass and with velocity.

- Instantaneous change ($d/dt$) in velocity is called acceleration.



Changes to object positions are done indirectly. To change an object position, you need to apply a force, which provides an instantaneous change ($d/dt$) to momentum.

- For the physics we're dealing with, forces don't change the mass of an object. Since changes in momentum can come from either changes in mass or changes in velocity and since forces don't change mass, all forces will result in some change in velocity (acceleration).



The common approach is to represent forces through a potential field. A potential field is represented by some energy value at every point in the space. (If the space is flat, the potential field would be visualized by something like imaginary hills and valleys placed throughout the space.) You can calculate a force at any given point in the potential field by measuring the downward slope (negative $d/dx$).



You can get a measure of "total force" as an object moves through a potential field by calculating $\int_{x_0}^{x_t} force(x) dx$. The result has units of type "force times distance", which is the same as energy. Since $force(x) = - \frac{d}{dx} potential(x)$, the integral is the same as $potential(x_0) - potential(x_t)$, which has units of the same type as the potential field. This means that the potential field assigns an energy value to each point $x$. Because of this, the potential field is also called potential energy.



A lot of interesting equations result from the fact that force can be represented as either a negative slope ($-d/dx$) in an energy field or an instantaneous change ($d/dt$) in momentum.

# 29
>>15186
Excellent post Anon, thanks. Please give me some time to chew this over and I'll respond better. Just wanted to let you know it's been seen.

# 30
>>15186
AUUUUUUUUGH! **:^)**
I still haven't made time yet Anon. I haven't forgotten.

# 31
Some stuff for dance generation: https://expressivemachinery.gatech.edu/projects/luminai/

It looks like this is based on Viewpoint theory, which is a theory of improvisation. There's a book about it called "The Viewpoints Book".

# 32
>>15459
Sounds interesting Anon. Unfortunately, they are blocking access across Tor so I'm unable to see it. But there has been some good things come out of GA Tech in our area so yep, I can believe it. Thanks!

