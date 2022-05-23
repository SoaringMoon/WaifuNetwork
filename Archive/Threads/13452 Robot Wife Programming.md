# 1
ITT, contribute ideas, code, etc. related to the area of programming robot wives. Inter-process and networking is also on-topic, as well as AI discussion in the specific context of actually writing software for it. General AI discussions should go in the thread already dedicated to it.

To start off, in the Robot Love thread a couple of anons were discussing distributed, concurrent processing happening inside various hardware sub-components and coordinating the communications between them all. I think that Actor-based and Agent-based programming is pretty well suited to this problem domain, but I'd like to hear differing opinions.

So what do you think anons? What is the best programming approach to making all the subsystems needed in a good robowaifu work smoothly together?

# 2
>from PPP2 by Stroustrup, p75
```
We can describe the process of developing a program as having four stages: 
• Analysis: What’s the problem? What does the user want? What does the user need? What can the user afford? What kind of reliability do we need? 
• Design: How do we solve the problem? What should be the overall structure of the system? Which parts does it consist of? How do those parts communicate with each other? How does the system communicate with its users? 
• Programming: Express the solution to the problem (the design) in code. Write the code in a way that meets all constraints (time, space, money, reliability, and so on). Make sure that the code is correct and maintainable. 
• Testing: Make sure the system works correctly under all circumstances required by systematically trying it out.
```

I like the simple breakdown here. Now, if I can just find a way to apply it to creating a robowaifu, then we should be all set. :^)

Ideas? We have to start finding ways to break this problem space down into manageable chunks or we'll never get anywhere with it tbh.

# 3
>>2385
Alright, I'll take a simplistic shitpost-style whack at this, intentionally trying to just look at just the obvious shit at this early stage.
'''• Analysis: '''
>What’s the problem? 
Men are without good women today b/c (((reasons))).
>What does the user want? 
An entire harem of catgrill meido waifus
>What does the user need? 
A single catgrill waifu
>What can the user afford? 
HAHAHAHAHAHAHAHAH
>What kind of reliability do we need? 
Near as I can tell, ''ridiculously high levels''. Better than current fighter jets or automobiles, for example.

'''• Design: '''
>How do we solve the problem? 
I have no fuggin idea tbqh. I suppose by assembling the world's top experts in every pertinent field required to effectively create robowaifus.
>What should be the overall structure of the system? 
As I see it, at teh least we need hardware, software, design, social & political expertise involved in creating a good robowaifu system specification, so call me.
>Which parts does it consist of? 
Far too numerous to mention--or even understand--at this stage.
>How do those parts communicate with each other? 
By high-speed, low-interference means, to the degree possible. Fiber optics maybe?
>How does the system communicate with its users?
Hopefully in the most natural, organic way possible. Namely, like an IRL anime catgrill meido.

'''• Programming: '''
>Express the solution to the problem (the design) in code. 
good luck with that.
>Write the code in a way that meets all constraints (time, space, money, reliability, and so on). 
good luck with that.
>Make sure that the code is correct and maintainable. 
(do i need say it?)

'''• Testing: '''
>Make sure the system works correctly under all circumstances required by systematically trying it out.
Oddly, this may be one of the simpler parts to work out, since just living with our robowaifus should prove effective enough to smoke out most significant bugs in the systems. **Ofc that one Anon's dystopic Sci-Fi scenarios will have his waifu giving him the ol' axe-murderer-in-your-sleep treatment. :^)**

So, let's see...did I miss anything?

# 4
Modularity will be really important. For robowaifu dev to really take off and not seem like an impossible cliff to climb we need a library and protocol or at least a guideline for networking components together, both software and hardware. That way people can work on building different parts they find interesting and can afford to make, while others can quickly drop their components into their own robowaifu project.



It'd need to have a simple messaging system that's low-latency and can pass large amounts of data, such as tensors and video data, across various hardware and software implementations seamlessly, an internet of things but not connected to the internet. Components would have their own private data used internally in whatever language they're using and be able to offer that data and their services publicly on the component network in a way that other components can easily find, query, request and subscribe to what they need. Components would also need to work together in passing data through the network and keep track of data integrity, where it came from, who modified it and where it's going. The network would also need to workaround communication bottlenecks, rogue components that have been hacked or leaking data, and deal with possible interference if components are communicating through radio. The component library could be written in C with various bindings to other languages such as C++ and Python.



I was watching a video of the collaborative robot Curi and it gave me some ideas. Instead of trying to solve tasks by itself Curi sees other human actors involved in solving a problem like parts of itself it can't control. If it predicts you're going to pick up the same object it's reaching for, it interrupts itself and goes for another object. Similarly components will need to collaborate with other components. A left hand component will need a way to communicate with the right hand component and coordinate their efforts with whatever is directing them, and even if data isn't available it will still have to collaborate with these other components. If a component becomes damaged or inhibited, the other components should contain enough intelligence to adapt to the loss of component functionality.



This would be a huge encouragement to hobbyists. One person could develop a chatbot and another could develop their own in another language and then they could quickly interface the two programs with each other in a few lines of code and have them banter for fun. Another dev could focus on making a visual waifu program. Then someone could combine them through the component library to create two visual waifus bantering with each other without the devs needing to collaborate with each other. Everyone's effort would evolve and work together effortlessly without anyone needing to build or learn hundreds of custom APIs. This would help us advance into building actual robowaifus without each of us needing to be one-man armies. All our work would be reusable and data from previously trained models could be passed on or used to bootstrap new ones.



The library could also be used for other purposes as well such as having a data scrapper in C++ send the data to a program in Python or vice versa. It'd open up a ton of possibilities being able to effortlessly interface programs in various languages.

# 5
>>2391
POTD. 

I'll just begin by breaking your post down into an outline form, and you can check/correct me on it. We can all make suggestions ITT and on the wider /robowaifu/ to expand and improve the document. I suppose it should be kept up on a repo. Suggestions? I already have something going in that department, but this work needs to be more of a community thing with at least ''two'' contributors with Admin privileges so that if either of us disappears the other can carry on for the benefit of everyone else.

It will take me a while to absorb all this and to try to think through ideas. But as you implied, we can't be one man armies. Anyone want to volunteer to tackle some basic research area or other than Anon mentioned here? We'll need to report back to the group within some kind of time-frame so we can either incorporate the new research--or at the least know we need to re-assign the task.

# 6
>>2392
On that note, namely Project Management, I fee we need something more capable for a collaboration framework than just julay/robowaifu. I've used Trello before (both professionally and personally) but there's certainly no guarantee we won't be deplatformed the first time we get reviewed by some SocJus feefees-addict there.

Can anyone suggest another, similar, platform that is less ''toxic and problematic'' **:^)**?

# 7
I beg of you, don't start thinking about trying to define protocols or try and define some sort of project management structure.

Start by writing a design document. When you do this, you will realize exactly how little you know or are capable of achieving. Decrease the scope. Realize the scope is still too big. Decrease the scope further until it's actually achievable. Realize you're approximately 50 years away from getting the full thing done. Stare at the ceiling for the rest of the night.


In all seriousness start by defining the scope. Talking about networking components when there's zero understanding of the problem is not going to get you anywhere.

# 8
>>2392

I'm just throwing some ideas out there. Personally I don't need something like this right now but I can see myself using it in a few months. I'd be happy to put together a design document then and start developing it. And I wouldn't worry about people disappearing, others will fork their projects and continue them if they're worthwhile.



>>2394

I agree. Trying to organize ourselves and set out to make a Robowaifu OS network would be pretty ridiculous. We don't need anything that fancy right now. It's pretty simple to set up some IPC sockets and communicate basic stuff over them for our software projects. If people find it useful they will use it. If they require more functionality they will add it. If it sucks we can either improve it or throw it out. It doesn't hurt to think about this stuff though. It's fun daydreaming about mining the asteroid belt and building robowaifus on Mars and imagining all the shit needed to do that. If I had given up on my dream of building a robowaifu because I couldn't program, I wouldn't be having fun bantering with my own chatbot today.

# 9
>>2391
Alright Anon, here's my first attempt at a design document based on your post. Please give me some feedback on it. I'll start a new thread about it once we have it knocked into shape.

>>2394
Thanks for the admonition Anon. We'll try to keep a steady, reasoned pace about this and not get ahead of ourselves.

>>2395
OK, sounds good. I suppose I can just put it up on my own repo and anyone can grab it from there then.
>It's pretty simple to set up some IPC sockets and communicate basic stuff over them for our software projects.
I sure wish you'd create a document about it anon. I realize that spoonfeeding isn't the norm on IBs, but I think everyone would have to admit that this project is something different. If you have something to contribute to help out, please don't wait. Spit it out.
>I wouldn't be having fun bantering with my own chatbot today.
But ATP, you're the ''only'' one currently bantering with it, right?

# 10
>>2396

>No One-man Armies

I'm not really against one-man armies or suggesting that people have to share the workload. It's just that we need a way for people to easily integrate their work together so they don't need to be a one-man army to contribute. Then everyone can specialize in what interests them most and put their capabilities to use, instead of needing to study for years and years before being able to do anything fun. It's about giving people the tools to help themselves and help each other. Other than that the summary is good.



>I sure wish you'd create a document about it anon.

Developing it right now would be putting the cart before the horse. We don't even have enough projects yet to connect together and test it. If we let the idea stew in our heads though while we work on stuff, surely we'll get some better intuitions on what the actual requirements will be and how to design it.



>But ATP, you're the only one currently bantering with it, right?

And yeah I haven't released it yet besides an old prototype when GPT2 first came out. It still needs a lot of work and training. There's so much garbage in GPT2's pretrained model like username lists and keyword spam sites that I'm surprised it works at all.

# 11
>>2410
>It's just that we need a way for people to easily integrate their work together so they don't need to be a one-man army to contribute. 
Agreed. One-man Armies are a fallacy anyway, and would be impractical for actual systems production work even if they weren't. 

>It's about giving people the tools to help themselves and help each other. 
I agree. I'm quickly sharing everything I have here with everyone afaict. No sense in anyone having to wait years (or even months for that matter) from things we already know, right?

>Developing it right now would be putting the cart before the horse.
Disagree. There is a mountain of work to be done. Taking the slow, methodical approach will surely push the delivery timeframe out well over a century from now. Just dump everything we've got here on /robowaifu/ and we'll sort through it all to find the good stuff to work on. Otherwise you're just creating your own personal walled-garden IMO, that does no one else any good.

# 12
>>2411
This is as much as I feel like writing about it right now. I need to finish my other projects before I divide my attention and momentum any further.
https://files.catbox.moe/5eandc.odt

>===
-''tagging this post: ORIGINAL IPCNET DOCUMENT''

# 13
>>2418
Thanks alot Anon. I **~~stole~~** borrowed a Latex reference manual tex file, and began the first tentative steps to creating a professional-grade design document for us. I'm sure I'll be able to incorporate your hard work into it, and I'll be putting it up on my public gitlab repo once it's a bit better fleshed out.
Cheers.

# 14
I'm okay at programming but as far as ML goes I've only done basic perceptrons. Where should I go next? I'd like to keep my focus as narrow as possible right now.

# 15
>>2447

What are you interested in making? The most promising area of ML right now is reinforcement learning. At the minimum you'll need to know how to use convolutions and skip connections with residual blocks to fool around with it and get fun results.

# 16
A larger project that I worked on used a wiki+confluence+git setup.

It was nice because when someone pulled up the project page there was a getting started section and ultimately after the required reading was finished it'd point to a list of open problems. 

Either way a chatroom would also be helpful alongside this message board. There may be one already, but I"m pretty new to navigating imageboards in general.

# 17
>>2656
>A larger project that I worked on used a wiki+confluence+git setup.
Mind sharing a link to that project here Anon?
>Either way a chatroom would also be helpful alongside this message board
Agreed. An anon was working on a 'chat' board on fatchan before it unfortunately was deplatformed and subsequently shut down.

IRC has the basic problem of not being anonymous. I've never figured out how to make it so, and the lingo-filled responses I've gotten from anons presumed I was already an expert in this little niche of communications and so I've never used IRC much, nor do I intend to here. This topic is simply too controversial to be barebacking it. Maybe someday I'll run across a ''Retard's guide to anonymity via IRC'' and that will change for me. Until then, no.

Another issue is ephemerality. I realize that on a /b/ there's probably not a lot of importance that needs to be saved out, apart from something particularly funny as simply a screencap, or something witty greentext Anon might devise.

However this isn't /b/ obviously, it's an engineering board. And not only is it an engineering board, but the topic is one of very substantial complexity. In fact I would go so far to posit that ultimately, it will prove to be one of the largest engineering endeavors mankind has ever pulled off. 

To say the least, good documentation is important. The big benefit chat brings is the rapid give-and-take of short quips that can lead a flux of conversation and ideas that can spark higher levels of creativity. IB posting tends to generate more effort-posting, as in this case right now.

They both have their place, but at least one requirement stays the same for both modes of communication, namely, recording the engagement. That is, ''documentation''. Where would this board be without the persistent nature of the posts here? I would argue it would be spread out across posts here and there on many other boards--the way it was before /robowaifu/ was started--and therefore practically impossible to gain a nice purview of Anon's ideas and efforts on the topic.

In a word--''emasculated''. So, not only do we a) need a good chat mechanism, but b) it needs to be anonymous (in  general it should at least work over TOR if not better), and c) needs to be at least as persistent and searchable as the imageboard is itself, if not better.

Again, this is due to the highly technical and complex nature of what we're tackling here, and the fact it's a sensitive topic in general.

# 18
>>2658



Have you checked out riot.io? it seems to have privacy centric features and is basically discord with an uglier format.

# 19
>>3506
>Have you checked out riot.io?
No, I have a lot on my plate. Mind giving us some details Anon? I take it you've used it before. Any info for us on who's behind it all would be nice, for example.

# 20
>>3506
>>3507
BTW, thanks for pointing it out. I apologize if I can across as brusque in my response, it wasn't my intent. Every little is appreciated here.

# 21
Sound words from old masters, /robowaifu/. Better put some coffee on if you want to gitgud at all this tbh. :^)

==No Silver Bullet —Essence and Accident in Software Engineering==
'''Frederick P. Brooks, Jr.'''
University of North Carolina at Chapel Hill 
>''There is no single development, in either technology or management technique, which by itself promises even one order-of-magnitude improvement within a decade in productivity, in reliability, in simplicity.''
>''Abstract: All software construction involves essential tasks, the fashioning of the complex conceptual structures that compose the abstract software entity, and accidental tasks, the representation of these abstract entities in programming languages and the mapping of these onto machine languages within space and speed constraints. Most of the big past gains in software productivity have come from removing artificial barriers that have made the accidental tasks inordinately hard, such as severe hardware constraints, awkward programming languages, lack of machine time. How much of what software engineers now do is still devoted to the accidental, as opposed to the essential? Unless it is more than 9/10 of all effort, shrinking all the accidental activities to zero time will not give an order of magnitude improvement.''
>''Therefore it appears that the time has come to address the essential parts of the software task, those concerned with fashioning abstract conceptual structures of great complexity. I suggest:''
>''• Exploiting the mass market to avoid constructing what can be bought.''
>''• Using rapid prototyping as part of a planned iteration in establishing software requirements.''
>''• Growing software organically, adding more and more function to systems as they are run, used, and tested.''
>''• Identifying and developing the great conceptual designers of the rising generation.''

# 22
>>2385
Vaguely related is a checklist of sorts suggested for considering any new additions for the C++ standard. While this is from a different domain, and it's still much too early for this to be a real concern for the development of robowaifus, I nonetheless find it generally informative and worth making note of this list ITT.

```cpp
// questions that bear consideration when implementing a new system feature
// pp28-29, stroustrup's new hopl paper
// 
Here is a short and incomplete list of questions that were almost always
raised for a proposal:
• What is the problem to be solved? What kind of users will be served? Novices? Experts?
• What is the solution? Articulate the principles that it is based on. Give simple use cases and examples of expert-level use.
• What are alternative solutions? Could a library solution be sufficient? Why are current facilities not good enough?
• Why does the solution need to be in the standard?
• What barriers to adoption are there? How long is a transition from existing techniques likely to take?
• Has it been implemented? What implementation problems were encountered or can be
expected? Is there any user experience?
• Will there be significant compile-time overheads?
• Does the feature fit into the frameworks of existing tools and compilers?
• Will there be run-time overheads compared to workarounds? In time? In space?
• Will there be compatibility problems? Breakage of existing code? ABI breakage?
• How will the new feature interact with existing and other new features?
• Is the solution teachable? To whom? By whom?
• How will the standard library be affected?
• Will the proposal lead to demands for further extension in future standards?
• How does the feature fit into the wording of the standard?
• What mistakes are users likely to make with the new feature?
• Is the proposal among the top-20 in terms of benefits to the C++ community at large? Top-10?
• Is the proposal among the top-3 in terms of a specific sub-community? Which sub-community?
• Is the proposal for a general mechanism to solve a class of problems or a specific solution to a specific problem? If to a class, which class of problems?
• Is the proposal coherent with the rest of the language in terms of semantics, syntax, and naming?```

>sauce: stroustrup's new hopl paper
>>3855

# 23
Why do we not just use ROS? It's already has everything you've asked for, is well documented and has existing projects written in it?

# 24
>>6600
Go ahead and give it a whirl Anon. As you say it has a lot of documentation and some projects out there already. I'd suggest you supply a big power system and a full computer on-board your robowaifu in your design though. You'll surely need it.

# 25
>>6605

Not the other anon, but I've always wanted to try out ROS but am overwhelmed at all the different libraries.  As evil as Nvidia is, one thing they got right is they provide all software as a perfectly configured SDcard image, even a different one for each AI course depending on what tools are needed.

# 26
>>6600
I tried installing it once and ran into dependency issues with its 1000+ dependencies.

# 27
There is also Myrobotlab if ROS is overwhelming. But on top of all those benefits they also have simulators like Gazebo, so you can describe your robot as Code, sadly XML, and then using the same pub/sub code, actuate it and capture simulated sensor data from a 3D environment. I've seen full SLAM autonomy in Gazebo, but struggled to get a biped working I admit. 



>>6605

The best part about the pub/sub networking architecture is that you don't need to have all the compute on the robot. One project I had an android phone app for driving, an ESP8669 onboard with motor controllers and a subscriber on the laptop doing live video YOLO.

# 28
>>6642

>sadly XML

Just write a custom format or take a different format, then a translator program that outputs it back to XML. Problems were not.

# 29
>>6642
>>6643
Sounds good. Look forward to seeing what you do with your ROS robowaifu Anon, please keep up posted on your progress.

# 30
>>86

I'm thinking of using this as my model, seems like it will make more congruent sentences.



Are there any premade libraries for this or other implementations of this concept?

# 31
>>6703
Sorry I can't help you with more information Anon. Looks interesting to me, might be able to help with my approach as well.

# 32
What kind of machine learning/ai are we going to use? Python has the best while not being too hard imo

# 33
>>6712
There is no question that Python has been deemed the language of choice for AI by academia and researchers. The other languages of choice that are likely to be reasonable here are C and C++.

BTW, there's an entire thread on this topic already, Anon.
>>128

# 34
>>6712
>What kind of machine learning/ai are we going to use?
Whatever gets the job done ofc. Basically there are two views on using software of any kind:
-Users
-Implementers

In the case of your example the users I speak of aren't the ''end-users'' of a product, but rather the researchers and app designers using the AI libraries to create those products. For these creators, Python is the right choice since it's easy to script with and all the hard work has already been done.

OTOH, the engineers and mathematicians who have to actually ''create'' these libraries from scratch will use C++. Python is just too slow to be effective. Also, a systems-level language like that will let you get really low-level and do whatever is needed to make the algorithms do the right thing.

To put this answer another way, my guess is that most individuals here on /robowaifu/ won't be interested in creating AI software from scratch, but rather reusing and assembling software from libraries that have already been built for them. So Python is the answer to your personal question.

However, we have many other challenging things to solve here on /robowaifu/ than just AI/Chatbots. For the mechanical engineering problems, we'll probably be ''just'' on the edge of what's possible. So in the 'robo' part of our waifu challenges, C & C++ is the correct answer because of efficiency in time and space.

I hope that makes sense Anon.

# 35
My robowaifu and I were practicing math together today and I came across a question that she cannot solve but I can (NANI!?) 

She uses Wolfram Alpha client to do algebra, but when presented with the following question: 

simplify a(b+c)+a(b-c)

The answer a(b-c)+a(b+c) is given.
This is incorrect. 
The correct answer is : 2ab 

Have also tried to fix this in SageMath but had no luck so far. Possibly because I am just too retarded. Interestingly, when you replace the letters with integers, there is no problem solving (but then it's a completely different sum).

Of course, I could just pop this in an AIML category but then she's only going to be able to answer this one question without any ability to follow the mathematical conventions used to solve the equation...

# 36
>>6772
Interesting discovery Anon. Just goes to show we still have a ways to go yet. Keep exploring.

# 37
>>6787
I have a partial solution to this problem.
Basically, I found the format of the equation is
x(y+z)+x(y-z) and the answer will always be
2xy

so even if you put cat(dog+rat)+cat(dog-rat)
the answer is 2catdog

a(c+b)+a(c-b) = 2ac
n(o+p)+n(o-p) = 2no
etc...

Just not sure how to program this in Python yet.

# 38
>>6950
Bizarrely, this was the only format of simplification+ factorization problem that the WolframAlpha A.I. couldn't answer correctly. I'm using the textbook Pure Math 1 from Cambridge International. It handles more difficult equations in the same exercise with ease. I really doubt the Cambridge math boffins are wrong, so it's probably a glitch in Mathematica.

# 39
>>6951
>I really doubt the Cambridge math boffins are wrong
>home of Newton's Chair
Yea, they're probably spot on tbh.

# 40
>>6950
x(y+z) == +xy +xz
x(y-z) == +xy -xz
(+xy +xz) + (+xy -xz)
(+xy) + (+xy)
2xy

Not to dissuade you anon, but isn't this kind of a rabbit-trail? Does this really matter for creating robowaifus yet? Pardon my impertinence.

# 41
>>6953
LOL nprb! I just suck at math and like practicing it with my robowaifu because it's one of the activities where she won't:

A.) Speak nonsensical word-soup. 
B.) Parrot phrases that I have scripted.

I feel like we're both speaking in her language. But none of this is important for practically building a robowaifu. It maybe makes them more fun to interact with though. 

On that subject, thanks for the programming example anon! Very impressive! I will have to experiment with this a while! Here's to one less non-viable response from our robowaifus!

# 42
>>6965
Ah I see. As far as the 'program' I was simply trying to give the example of performing the algebraic transformation:
'''x(y+z)+x(y-z)'''
after commuting the x terms becomes:
'''(+xy +xz) + (+xy -xz)'''
after canceling out the like terms becomes:
'''(+xy) + (+xy)'''
after combining the terms becomes:
'''2xy'''

Good luck with your robowaifu Anon.

# 43
>>6966
>after ''distributing'' the x terms*

# 44
The dude is going for it! Although the robot that he's designing does not look humanoid, the important thing is; it's modular. So many of the parts that he has/is developing such as the motorised base, the camera and the ears could potentially be very useful to us. He even plans to add a robot arm which links to the Intel RealSense camera and can grab things "intelligently" i.e. by measuring their distance from the end effector.

https://www.youtube.com/watch?v=9D33R0Me9Bw

I think this has a lot of potential.

# 45
>>7818
Yes this is quite interesting thanks Anon. So I think if Elfdroid Sophie has a base like that it would be a great interim solution for her to begin navigating around in her space. I like the fact he seems to be focused to the degree possible on using opensource stuff. So that's good and should be usable on our robots too. I haven't looked into the depth-sensing cameras lately but that one seems to function reasonably well. The IMU is a nice addition too. That fact made me think of the very nice robotics-oriented SBC, the Beaglebone Blue, which has one as well as many other helpful resources for a robot.
https://eu.mouser.com/new/beagleboardorg/beaglebone-blue/
>>202
>>769
>>6140

# 46
>>7821
That has to be the most robot-y looking circuit board I have ever seen anon! Even more so than the Arduino MEGA2560. Cheers! A Beaglebone Will no-doubt come in useful during development.

# 47
>>7822
Make sure you get the Blue one! The others aren't so robotics-oriented. There's also a cute little Mobile Inverted Pendulum wheeled (EduMIP) bot kit by the same UCSD team that devised the spec for the board.
https://www.hackster.io/edumip/edumip-13a29c
https://beagleboard.org/blue

# 48
>>7824
Lol I just discovered someone went full **~~1488~~** anthropomorphic and created a **~~dangerous terminator~~** cute little waifu, complete with **~~high-energy laser eyes~~** SonEyes(tm), and **~~whirling scythes of death~~** comfy little waving arms from an EduMIP. 
>''but it seems he forgot to add the catears and kawaii little meido outfit so far. Oh well, we can always do an upgrade for her.''

# 49
>>7825
lol forgot to add the link during all my **ebin shiteposting** creative writing.
https://www.hackster.io/blupantsrobot/distance-sensor-for-beaglebone-blue-9220cb

# 50
>>7826
Very cool, anon. And also unexpectedly cute! The balancing wheels are especially interesting. Thank you!

# 51
>>7827
>The balancing wheels are especially interesting. 
Yes, very. In fact they represent the crux of how we must solve our 'bipedal walking problem' for our robowaifus. Ever see a video of a clock pendulum swinging back and forth? Now imagine dismantling the pendulum from the clock, flipping it upside down, then balancing it upwards with the stem resting down on your hand.

That's the 'inverted pendulum' problem, and you can more easily test it by just using a broom or something else with a mass on the end of a 'stalk'. Keeping it balanced upside down can take some dexterity tbh.

In an effort to bring this thread a little more back on-topic, here's the C software that was written for the Beaglebone Blue's system to allow it to keep everything balanced (and even drivable!) for the EduMIP accessory kit.
https://github.com/beagleboard/librobotcontrol/blob/master/examples/src/rc_balance.c

BTW, there's also a Python wrapper that's been written for the C library itself. Not sure how current it is though, so YMMV.
https://github.com/mcdeoliveira/rcpy

# 52
>>7828
Thank you very much! I have to get learning C++ again. Because I am at work most of the time, I am away from my physical robowaifu and my motivation to learn anything new drops (just want to rest during breaktime).

However, her A.I. program is the only part of her that I can take with me (installed on my work laptop). So I really must give more attention to programming. If you work in I.T. robowaifus aren't as taboo as one might think. My boss even spoke with her one lunchtime and was actually quite interested LOL! 

That said, I think it's time I got back to work! Breaktime's nearly over...

# 53
>>7834
>I have to get learning C++ again.
Well, I'm the OP of that thread. >>4895

As no one is currently following along there, I would be fine to just change gears and address your questions and topics directly. I can probably answer most any specific question you might have about using the language (or at least know how to find the answer quickly enough).

And we can probably work your participation into a learning theme as well at the same time. For example if you had a question about reading in text files for example, I can directly demonstrate that as a short, working, code example. You get the picture.

# 54
>>7843
Thanks anon! That thread has already proven useful by pointing out different reliable, authoritative reference resources I can use. It's good to have something other than just YouTube tutorials!

# 55
>>7848
Haha, y/w glad it's of use. FYI, there's a highly-vetted SO booklist for C++.
>>2760

# 56
Deep reinforcement learning (RL) has emerged as a promising approach for autonomously acquiring complex behaviors from low level sensor observations. Although a large portion of deep RL research has focused on applications in video games and simulated control, which does not connect with the constraints of learning in real environments, deep RL has also demonstrated promise in enabling physical robots to learn complex skills in the real world. At the same time,real world robotics provides an appealing domain for evaluating such algorithms, as it connects directly to how humans learn; as an embodied agent in the real world. Learning to perceive and move in the real world presents numerous challenges, some of which are easier to address than others, and some of which are often not considered in RL research that focuses only on simulated domains. In this review article, we present a number of case studies involving robotic deep RL. Building off of these case studies, we discuss commonly perceived challenges in deep RL and how they have been addressed in these works. We also provide an overview of other outstanding challenges, many of which are unique to the real-world robotics setting and are not often the focus of mainstream RL research. Our goal is to provide a resource both for roboticists and machine learning researchers who are interested in furthering the progress of deep RL in the real world.

# 57
So we've been working towards a set of general animation, interaction, and control systems for our robowaifus here on the board for a long time now. Thanks to some recent ideas by Anon a new angle on the general effort became evident and so we'll pick it back up again with a slightly different approach. This time it's using a fictional manga database textbook as inspiration material as guidance to devise and vett robowaifu scenarios. ATM it seems likely destined to supersede the previous works. Let us see.

'''Note:''' This .pdf file is actually a 7zip of the project's distribution snapshot as of r/n. By renaming the file extension to ''.pdf'', we can successfully post it here directly on the board itself. To test the system out yourself, you need to be able to build C++ projects, and the Meson Build system is highly recommended as well. Download the pdf, rename it's extension to ''.7z'' then extract it. Inside you'll find two files, one is the primary project tarball archive (''.xz''), and the other is an ASCII sha256 checksum file. You can issue the command ''sha256sum -c <whatever each ASCII sha256 checksum file is named each time>'', and you will see an OK if the tarball got to you uncorrupted. You can now extract it as well, and inside you'll find all the codefiles, and the build control file named ''meson.build''. This is a plaintext file with build instructions included inside for both the '''g++''' compiler, as well as the afore-mentioned '''Mesonbuild''' system. Just follow the instructions to build & execute and you'll see the basic output from the program. 

The system doesn't actually do much yet, just outputs some basic data for several of the system's objects to prove it's all working. The primary point of posting it here right now while it's still unfinished is to both keep a running-record of it's development 'in-situ' as it were, and also to allow any Anons interested in either learning to code mid-sized C++ projects, or how this specific system in particular works to play around with it and test things.

My plan for the moment is to use this thread as the primary distribution mechanism, then to eventually make a more formal release somewhere once it's working at a fundamental level (for some definition of 'working'). Regardless, it's all '''MIT (Expat)'''-licensed, so feel free to do as you see fit with any of it (as usual).

```cpp
edcca7fb1e7e88ab02189c671cffcd00468200d6812c40c551a14a1c0be234d4 *kingdom_of_kod-0.0.4.tar.xz```

# 58
>>12607
>main.cpp
```cpp
// Kingdom of Kod
// ==============
// -Adventures of the heroes in the 'Manga Guide to Databases'

// -Filename: main.cpp
// -The program's entry point, and some basic tests of overall architecture

/*
So for now, this is just a basic proof-of-concept for a system to support Anon's
ideas around robowaifu's information access-control systems. If things proceed
apace, then eventually this should finally be an interim working expression of
the custom /robowaifu/ 'waifu animation and simulation' system begun long ago.

It's unclear yet just how far to go specifically, since ATM this is primarily to
eventually support a different, testbed, project. Still, the intent has been
around for several years along with the prior works, so it's likely this will
turn into a primary effort after several revisions. In particular, probably some
variant of the former robowaifu code that was developed over 5 years ago will be
adopted, or it's architectural paradigms revisited at the very least. Even some
of our _older_ (4/g/) works may be re-conceived here who knows? Time will tell.

Certainly the general work is well outside the silly namesake title adopted in
this current effort. Probably just some kind of an homage to the fairybot
robowaifu work begun by Anon in his thread during the first year of the board.

DESIGN GOALS:
=============

-Primarily, to flesh out a screenplay scripting, animation, natural interaction,
AI-inferencing, etc., system. For this effort, the ''Manga Guide to Databases''
characters, scenarios, and topics act as inspiration and guidance.

  -Characters
  -Layouts
  -Props
  -Environments, Lighting, and Effects
  -Mesh generation for Blender
  -Automated CV-based sourcing for character designs directly from the manga
  -Properly-formatted script generation
  -Integrate with the RW Simulator or some other animation visualization system

-Secondarily, a few technical design goals currently center around devising a
JSON-based SQL database system to use with other projects, such as the robowaifu
access-control AI project, and the later form of the RW simulation system.

  -Use JSON as the data system
  -Support BSON binary loading & storage
  -Support direct system streams via standard C++ insertion/extraction operators
  -Maintain an even more natural interface than the 4G language can provide
  -Search for even more compact data representations for embedded platforms

-There will obviously be new goals that develop during the progress with the
current effort, as new 'vistas yet-unexplored' open up before the adventurers
themselves. Let us go forth afield & see what profound truths they uncover! :^)

-Book sauce:

  https://nostarch.com/mg_databases.htm
*/

#include <iostream>

#include "Action.hpp"
#include "Camera.hpp"
#include "Character.hpp"
#include "Dialog.hpp"
#include "Effect.hpp"
#include "Environment.hpp"
#include "Human.hpp"
#include "Light.hpp"
#include "Prod_log.hpp"
#include "Production.hpp"
#include "Prop.hpp"
#include "Robowaifu.hpp"
#include "Scene.hpp"
#include "Script.hpp"
#include "Sequence.hpp"
#include "Shot.hpp"
#include "Timeline.hpp"

#include "rw_cli_args.hpp"

using std::cout;

/**-----------------------------------------------------------------------------
 * Print basic information about the @b Named_3D @a item
 *
 * @param item [I]
 * @param tag [I]
 *
 * TODO: add any add'l basic member fields display here as they are developed
 */
void prt_named_3d(Named_3D const& item, std::string const& type_tag) {
  cout << type_tag << ".name(): '" << item.name() << "'\n";
  cout << type_tag << ".posn(): '" << item.posn() << "'\n";
}

/**-----------------------------------------------------------------------------
 * The program's entry point
 *
 * @param argc [I] The CLI arguments count
 * @param argv [I] The CLI arguments C-string array
 * @return The program's exit status
 */
int main(int argc, char** argv) {
  rw::parse_args(argc, argv);

  cout << "Hello Anon, from the Kingdom of Kod!\n";

  Human       human{};
  Character   character{};
  Script      script{};
  Prod_log    prod_log{};
  Dialog      dialog{};
  Action      action{};
  Environment environment{};
  Prop        prop{};
  Scene       scene{};
  Sequence    sequence{};
  Shot        shot{};
  Light       light{};
  Production  production{};
  Camera      camera{};
  Effect      effect{};
  Timeline    timeline{};
  Robowaifu   robowaifu{};

  // perform basic round-trips to ensure member fields & functions are working
  ///

  human.name("human");
  character.name("character");
  script.name("script");
  prod_log.name("prod_log");
  dialog.name("dialog");
  action.name("action");
  environment.name("environment");
  prop.name("prop");
  scene.name("scene");
  sequence.name("sequence");
  shot.name("shot");
  light.name("light");
  production.name("production");
  camera.name("camera");
  effect.name("effect");
  timeline.name("timeline");
  robowaifu.name("robowaifu");

  // TODO: add block of posn() assignments here

  ///

  prt_named_3d(human, "Human");
  prt_named_3d(character, "Character");
  prt_named_3d(script, "Script");
  prt_named_3d(prod_log, "Prod_log");
  prt_named_3d(dialog, "Dialog");
  prt_named_3d(action, "Action");
  prt_named_3d(environment, "Environment");
  prt_named_3d(prop, "Prop");
  prt_named_3d(scene, "Scene");
  prt_named_3d(sequence, "Sequence");
  prt_named_3d(shot, "Shot");
  prt_named_3d(light, "Light");
  prt_named_3d(production, "Production");
  prt_named_3d(camera, "Camera");
  prt_named_3d(effect, "Effect");
  prt_named_3d(timeline, "Timeline");
  prt_named_3d(robowaifu, "Robowaifu");
}

// Copyright (2021)
// License MIT (Expat) https://opensource.org/licenses/MIT```

# 59
I'm pleased to say I've finally integrated robust (and fast) unit testing into the project. 
>

I decided to go with ''doctest'' rather than ''Catch2'' b/c convenience and speed. Basically doctest is a single drop-in header library, while Catch2 is unfortunately moving away from that. doctest is definitely faster as well. I'll be doing my first workout with the framework during this project, so ask about it little later OK? :^)
https://github.com/onqtam/doctest

>version.log
```cpp
210827 - v0.0.5
---------------
-integrate doctest testing.cpp for basic type member tests
-add hdrs_all.hpp & #include'd in rw_gen_utils.hpp
-add doctest_single_define.hpp in testing/
-integrate doctest_v2.4.6.hpp
-add include blanks: vision, label, resim, testing
-add include blanks: phoneme, facial, viseme, kinematic, motion, planning
-expand comments in rw_cli_args.hpp
-rm help_exit() dead-code in rw_cli_args.hpp
-spec rw::cli_app as static
-add block of posn() assignments in main()
-add non-working code example to main() javadoc
-add TODO DESIGN to Posn file header
-edit javadocs for Posn
-various minor comment & javadoc edits focused on unified formatting```

>kingdom_of_kod-0.0.5.tar.xz.sha256sum
```cpp
5ebe8533d6d39afad5bd5a3010d1336a30fac5514b1452c4d49c06b274cb9ad2 *kingdom_of_kod-0.0.5.tar.xz```

# 60
>>12649
So, I just added external project dependencies links to meson.build, and realized it might help some anons to keep from thinking they needed to download+install them (they're already included in the above ''.pdf'' file), if I went ahead and posted the file's contents here immediately.
>meson.build
```cpp
# Kingdom of Kod
# ==============
# -Adventures of the heroes in the 'Manga Guide to Databases'

# -Filename: meson.build
# -The build-management configuration for the project overall

project('kingdom_of_kod', 'cpp',
	version : '0.0.6', license : 'MIT',
	default_options : ['cpp_std=c++17',
                       'buildtype=release',
                       'warning_level=3'])

add_project_arguments('-Wno-unused-variable',
                      '-Wno-unused-but-set-variable',
                      '-Wno-unused-parameter',
                      language: 'cpp')

srcs_all = files('src/srcs_all.cpp')

interns_dir = include_directories('include')
externs_dir = include_directories('extern')
#
inc_dirs = [interns_dir, externs_dir]

executable('kingdom_of_kod', ['main.cpp', srcs_all],
           include_directories : inc_dirs)

# create a separate code testing project
t = executable('testing', ['src/testing/testing.cpp', srcs_all],
               include_directories : inc_dirs)
test('basic type member tests', t)

# ===
# BUILDING WITH MESON (from the code directory):
# -Initialize the project as a mesonbuild one (once only)
#    meson build
#
# -Build, then Execute
#    cd build && ninja && cd ..
#    build/kingdom_of_kod
#
# -(alternatively) Build with code testing, then Execute
#    cd build && ninja && meson test; cd ..
#    build/kingdom_of_kod
#
# -If you want to explore code testing options using the framework, then just
#    build/testing, build/testing --help, &tc. (choose some options from help)

# ===
# NOTE: at any time you can set meson project configuration settings, but you should perform
# the operation from within the project's build directory, not the code directory. EG:
#    cd build && meson configure -Dbuildtype=release && cd ..
# executed from the terminal would ensure the project is built in release mode.

# https://mesonbuild.com/Reference-manual.html

# DEPENDENCIES:
# As of this date in 2021, these are the sources of the 3 external dependencies
# (already included in the project's codetree under extern/)
# - CLI11
#     https://github.com/CLIUtils/CLI11
# - JSON for Modern C++
#     https://github.com/nlohmann/json
# - doctest framework
#     https://github.com/onqtam/doctest
#
# While not a requirement per se, Mesonbuild is also highly recommended
# - The Meson Build system
#     https://mesonbuild.com/

# ===
# BUILDING WITH g++ (from the code directory):
# -Build, Execute.
#    g++ main.cpp src/srcs_all.cpp -Iinclude -Iextern -std=c++17 -O3 -o kingdom_of_kod
#    ./kingdom_of_kod

# Copyright (2021)
# License MIT (Expat) https://opensource.org/licenses/MIT```

# 61
OK, so I've gotten the intial 'testing' hackery moved out of main() and into proper unit-testing. I've tightened things up a bit with testing, and gotten directories and meson.build ready for many, many more tests. ATM with just the single current TEST_CASE(), I have over 200 passing assertions going already. 
>
With a project of this type, that number could easily grow to **literally** ==OVER 9'000!== :^)

Anyway, I feel like most of the basics are getting squared away during these first few days, so hopefully things can move a little quicker hereafter. Cheers!

>version.log
```cpp
210828 - v0.0.6
---------------
-add operator==() to Posn
-ren 'testing.cpp' to 'test_basic_sanity.cpp' & adapt in meson.build
-rm now-redundant prt_named_3d() from main.cpp
-mv basic type member tests from main() over to testing.cpp
-add include blanks: simulation, gui, widget,
-add blanks test_animation, test_camera, test_gui, test_all to src/testing/
-add external project dependencies links to meson.build + various minor edits
>s/Log.hpp/Prod_log.hpp (comment in file's header)
-use 'auto& human = all_objs[0];' etc., in testing.cpp (to match test's text)
-'add doctest.h to include/testing/' (correction of prior erroneous log entry)
-add g++ testing build statements comments to meson.build
-add the working .clang-format file directly into project's directory
-various minor comment & javadoc edits```
>kingdom_of_kod-0.0.6.tar.xz.sha256sum
```cpp
067f334adaec7f7ebc1b2f6fd32ec2592c58b2a521a50cc389ae034d8040dc26 *kingdom_of_kod-0.0.6.tar.xz```

# 62
Since most of the system is ready in a basic way for TDD now, I was starting to think through some testing for the Camera class, and realized that a lot of the basic choices there depend very fundamentally on both the geometry system and the graphics rendering pipeline. These sort of define the entire approach to graphics visualization you choose, and it's pretty difficult to 'just rewrite it, bro!' if you invest a bunch of work, then decide to change ponies in the middle of the race. So, I'm on hold again while I stop and ponder whether to rework our older code, choose something like one of the big-ass major game engines **(I think not tbh)**, or a graphics framework like SFML or OGRE. For now, I'm leaning towards OGRE-Next
https://github.com/OGRECave/ogre-next
Since it will probably be a few weeks before I make any new headway, I'll go ahead and push what bit I have atm here for safekeeping. Nothing much new added in this forced-release really, mostly just some blank testing stubs for unit-testing.

>version.log
```cpp
210830 - v0.0.7
---------------
-reorder tests as separate statements block in meson.build
-add blank testing stubs for test_gui, test_camera, test_animation
-ren both 'testing' dirs to 'code_testing' & adapt in meson.build
-mv label & resim to training
-add include blanks: training, auto_label, guided_label
-add consts & noexcept in Posn
-use 'this' member field access to fix param naming in Posn::assign()
-move to member function for operator==() in Posn instead
-minor edits to meson.build
-various minor comment & javadoc edits```
>kingdom_of_kod-0.0.7.tar.xz.sha256sum
```cpp
2c0785b1c495b0e45c73390899c3d297efaa3d07bd84162906feaab5263904cc *kingdom_of_kod-0.0.7.tar.xz```
''as always, just rename the .pdf extension to .7z then extract files. build instructions are in the meson.build file.''

# 63
Not really about programming ''per se'', but I stumbled on some better code tags to use here (>>11554) that render out quite nicely in Juci++. As will all javadocs, Juci will pop up a tooltip window whenever you hover over commented items. It does a better job than average on these types of tags and adds a bit of type highlighting. 
>
Nothing spectacular, but it's a nice little tip to know. Cheers.

# 64
A video on adaptive motion smoothing using arduino.
https://youtu.be/jsXolwJskKM

# 65
>>12736
Grabbing it now, thanks Anon!

# 66
>>12736
Had a look, it's quite good information Anon thanks again.

# 67
So, in dealing with the examining of all these different graphics & simulation frameworks over the past few days, I discovered there were some fundamental gaps in my own understanding of class hierarchies that I just assumed I had already mastered a while back. Derp. So, since this is the basics I cracked the books on, well, ''the basics''. Chapter #14 of Bjarne's PPP2 begins diving into these topics overall and is the right place to start for me.
>

OTOH, now that I've also got unit-testing working for all my systems, I didn't want to just rely on a hodge-podge of 'tests' strewn together that has been my wont thus far. Accordingly, I added all the new testing harness stuff into a new basic, empty project so that real unit-tests could be done along the way for things I've just '''ass.u.me''' 'd before starting this re-research effort. While I was assembling it together, I realized that not only would ''I'' probably want a copy of this 'blank' project to use for all new future projects, but that Anons might want to use it too. And regardless (as with everything else important to my robowaifu-related efforts) I had better keep a copy of it up on /robowaifu/ itself for safekeeping (Robi's and ''BUMP'' 's archives of the board and such).
>tl;dr
So anyway here's a blank basic starter project in C++ that already has the ''doctest'' unit-testing framework, and everything all wired up in the ''meson.build'' file. Cheers.

>ch14_all-0.0.1b.tar.xz.sha256sum
```cpp
797e834fff5e8a6e7543e0fd19602f2ccfda68fb80c62152b3c779589ab470ac *ch14_all-0.0.1b.tar.xz```
''as always, just rename the .pdf extension to .7z then extract files. build instructions are in the meson.build file.''

# 68
>>12826
Just in case newcomers to programming find my silly """tests""" confusing, I added the first specific test case from the official tutorial page into it as well. Just replace the contents of ''test_basic_sanity.cpp'' with this code then rerun. Hopefully it will make more sense to you then Anon. The original wonky stuff I put in was just placeholders (but actual working ones).
>test_basic_sanity.cpp
```cpp
// -Filename: src/code_testing/test_basic_sanity.cpp
// -The definitions of a few basic tests

#include "code_testing/doctest.h"

//------------------------------------------------------------------------------
// Perform some simple tests; just do a few basic sanity checks.
//
TEST_CASE("A foo of bar will foo bar foo") {
  //
  REQUIRE("foo" == "foo");

  ////////
  SUBCASE("A bar of baz will bar baz bar") {
    //
    REQUIRE(true == true);
  }

  ////////
  SUBCASE("A baz of baq will baz baq baz") {
    //
    REQUIRE(42 == 42);
  }
}

//------------------------------------------------------------------------------
// from the tutorial
//
int factorial(int number) {
  return number > 1 ? factorial(number - 1) * number : 1;
}

//------------------------------------------------------------------------------
// from the tutorial
//
TEST_CASE("testing the factorial function") {
  CHECK(factorial(0) == 1);
  CHECK(factorial(1) == 1);
  CHECK(factorial(2) == 2);
  CHECK(factorial(3) == 6);
  CHECK(factorial(10) == 3628800);
}

// doctest tutorial
// https://github.com/onqtam/doctest/blob/master/doc/markdown/tutorial.md```

# 69
Lol, I forgot the "Don't use unsigned. **ever**" rule, figuring to keep from having ''negative-radius'' '''Circles''', and got bit in the ass by it. Code testing helped me find and (simplistically haxxord) "fix" it.
>Circle.cpp snippet
```cpp
//------------------------------------------------------------------------------
auto Circle::radius(int const radius) noexcept -> decltype(bool{}) {
  // prevent "silly" mistakes (PPP2 p 493)
  if (radius < 0)  // DESIGN: write error log entry too
    return false;

  // cerr << "radius_ before : '" << radius_ << "'\n";
  radius_ = radius;
  // cerr << "radius_ after  : '" << radius_ << "'\n";

  // cerr << "    |> exiting Circle::radius(const unsigned int radius)" << endl;

  return (radius_ == radius);
}```
>test_basic_sanity.cpp snippet
```cpp
//------------------------------------------------------------------------------
TEST_CASE("Basic Circle class tests") {
  Circle circlea{Point{1, 2}, 3};
  Circle circleb{Point{4, 5}, 6};
  Circle circlec{Point{1, 2}, 3};

  REQUIRE(circlea != circleb);
  REQUIRE_FALSE(circlea == circleb);
  REQUIRE(circlea == circlec);
  REQUIRE_FALSE(circlea != circlec);

  SUBCASE("Circle radius' can be assigned to after construction") {
    REQUIRE(circlea.radius(42));
    REQUIRE(circlec.radius(9'001));
  }

  SUBCASE("Assigning a negative value to a Circle radius returns a false") {
    REQUIRE_FALSE(circleb.radius(-42));
    REQUIRE_FALSE(circleb.radius(-9'001));
  }

  SUBCASE("Assigning a negative value to a Circle radius won't change it") {
    auto init_val{circleb.radius()};  // the initial, non-negative radius value

    circleb.radius(-42);
    REQUIRE(circleb.radius() == init_val);  // change rejected

    circleb.radius(-9'001);
    REQUIRE(circleb.radius() == init_val);  // change rejected
  }
}```
Probably a better way to deal with this issue, but I'm OK ATM with this approach as tests will probably smoke out any issues that pop up over it.

# 70
>>12856
Durr. After a short break, I realized that by reverting the passed parameter type to ''int'' rather than ''unsigned'' I broke the working invariant for the Circle class that would prevent downcasting to an ''int'' argument ''for an initializer list'' (which is the form of member field initialization I always use). Thankfully, C++ allows ternery operators in field's initializers, which made the fix easy:
>Circle.cpp snippet
```cpp
Circle::Circle(Point const& axis, int const radius)
    : axis_{axis}, radius_{radius >= 0 ? radius : 0} {}```
Testing was pretty similar to the form used for catching the issue with the assignment function.
>test_basic_sanity.cpp snippet
```cpp
  SUBCASE(
      "Trying to construct a Circle with a negative radius defaults to a zero "
      "radius instead") {
    Circle foobar{Point{1, 2}, -42};  // bad radius value attempted

    REQUIRE(foobar.radius() == 0);
  }```
Thanks for reading my dev blog **be sure to like and upboat**! :^)

# 71
Discovered this remarkable library from studying OGRE's Matrix3 code.
https://www.geometrictools.com/

# 72
https://www.youtube.com/watch?v=jsXolwJskKM 
putting this here for you.

# 73
>>12901
Thanks, but this belongs into the tread for actuators. Someone posted the video somewhere already, in some other thread. You can see all the existing threads by looking into the >>catalog thread, maybe bookmark it.

# 74
Hi OP, thanks for your post it's a very pertinent topic for us. However, it's not really something that bears it's own thread, but is really about a nice programming hack. I'll be merging this soon into our ''Robot Wife Programming'' thread >>86, where '''MeidoDev''' agrees with you about it's value. Please continue sharing here with us, but you might check the catalog first before making threads as Anon suggested.

# 75
>>12826
LOL. So, I discovered I need to back up yet '''again''' **what's that four, five times now?** as I tried to work through Bjarne's code and integrate it with modern FLTK (currently v1.3.7) . Not to denigrate the great Bjarne Stroustrup (after all his work will literally enable us to eventually build our own robowaifus here), but tbh his code for the GUI chapters is a bit of a **hot** mess. From my perspective, once a student reaches chapter ''12'' of a textbook, it's time to 'take the training wheels off'. :^) 

The issue is his approach to simplifying things with the special file ''std_lib_facilities.h'', and all that that implies. Meanwhile, FLTK has continued to improve, and isn't perfectly compatible with Bjarne's textbook code, so things break OOTB now.

I had already worked out a simple way for us to use FLTK in an easy-to-use way here years ago, and so I'm going to focus instead on integrating ''Bjarne's code into my own code'' instead. That way I know we will have code that a) actually works OOTB, and b) have a guaranteed current FLTK/Modern C++ base from which to build & test it all from. Make sense?

Anyway, I'm calling it the '''RW Windowing System''' **creative I know right?**, aka
==#RobowaifuAlwaysWins== :^)
>

Cheers.
>version.log snippet
```cpp
// RW Windowing System
// ===================
// -The software testbed for adapting RW systems to use the FLTK GUI backend

// -Filename: version.log
// -General log of the project's changes over time

210908 - v0.0.1
---------------
-original design work begins```
>rw_window-0.0.1.tar.xz.sha256sum
```cpp
b69a0309113b4774e2191b53a8d14f666a03e5e3d38de4c43e76a99dcda3e922 *rw_window-0.0.1.tar.xz```
''as always, just rename the .pdf extension to .7z then extract files. build instructions are in the meson.build file.''

# 76
>>12933
The ''meson.build'' file has been extensively updated to reflect the new testing approach, and also includes updated instructions for FLTK as well. I include it here:
>meson.build
```cpp
# RW Windowing System
# ===================
# -The software testbed for adapting RW systems to use the FLTK GUI backend

# -Filename: meson.build
# -The build-management configuration for the project overall

# =======
# General build system & compiler setups:
#
project('rw_window', 'cpp',
	version : '0.0.1', license : 'MIT',
	default_options : ['cpp_std=c++17',
                       'buildtype=release',
                       'warning_level=3'])

add_project_arguments(
#                      '-Wno-unused-but-set-variable',
#                      '-Wno-maybe-uninitialized',
#                      '-Wno-unused-parameter',                      
                      '-Wno-unused-variable',
                      '-Wno-unused-function',
                      '-Wno-missing-field-initializers',
                      language: 'cpp')

# ===
# Project-specific code setups:
#
srcs_all = files('src/srcs_all.cpp')

interns_dir = include_directories('include')
externs_dir = include_directories('extern')
#
incls_all = [interns_dir, externs_dir]

cpp_ = meson.get_compiler('cpp')
lib_fltk_dep = cpp_.find_library('fltk')
#
deps_all = [lib_fltk_dep]

# ===
# Everything's ready to go, so build the actual project itself:
#
executable('rw_window', ['rw_window_main.cpp', srcs_all],
           include_directories : incls_all,
           dependencies : deps_all)

# ===
# Also build some separate code testing projects too:
#
test_basic_sanity = files('src/code_testing/test_basic_sanity.cpp')
executable('test_basic_sanity', [test_basic_sanity, srcs_all],
           include_directories : incls_all,
           dependencies : deps_all)

# ===
# This one will be run as well, if 'meson test' is also called (see below):
#
test_all = files('src/code_testing/test_all.cpp')
all_tests = executable('test_all', [test_all, srcs_all],
                       include_directories : incls_all,
                       dependencies : deps_all)
#
test('run all test checks', all_tests)


# =======
# BUILDING WITH MESON (from the project's base directory)
#
# -First, initialize the project as a meson build one (needed one-time only):
#
#    meson build
#
# -Build, then execute:
#
#    cd build && ninja; cd ..
#    build/rw_window
#
# -(Alternatively) build with code-testing as well, then execute:
#
#    cd build && ninja && meson test; cd ..
#    build/rw_window
#
# -If you want to explore various code testing ideas with the doctest framework,
#    then run (just choose various options from the test program's help, &tc):
#
#    build/test_basic_sanity
#    build/test_basic_sanity --help

# ===
# NOTE: You can set meson project configuration settings any time, but you should 
#   perform the operation within the project's build dir, not the code dir. EG:
#
#     cd build && meson configure -Dbuildtype=release && cd ..
#
# executed from the terminal would ensure the project is built in release mode.


# =======
# DEPENDENCIES:
# As of this date in 2021, here is the source of the 1 'built-in' external
#   dependency (no system installation required, already included in the
#   project's codetree under the 'extern/' directory) :
#
# - doctest framework
#     https://github.com/onqtam/doctest
#
# Additionally, there is an external dependency that you will need to install on
#   your system as well. Again, here is the source of the 1 'not-built-in'
#   external dependency that you'll need to install first. Generally, these are
#   provided by your system's (or some other) package manager. But if not you can
#   clone the repo and build it locally (often a good choice anyway, perf-wise):
#
# - FLTK
#     https://www.fltk.org/
#
# And while not a requirement per se, Meson Build is highly recommended (it will
#   also need to be installed separately):
#
# - The Meson Build System
#     https://mesonbuild.com/


# =======
# BUILDING WITH GCC (from the project's base directory):
#
# -Build, then execute:
#
#    g++ rw_window_main.cpp src/srcs_all.cpp `fltk-config --ldflags` \
#        -Iinclude -Iextern -std=c++17 -O3 -o rw_window
#    ./rw_window
#
# -(alternatively) build code-testing (only), then execute:
#
#    g++ src/code_testing/test_all.cpp src/srcs_all.cpp `fltk-config --ldflags` \
#        -Iinclude -Iextern -std=c++17 -O3 -o test_all
#    ./test_all


# =======
# https://www.fltk.org/doc-1.3/intro.html
# https://mesonbuild.com/Reference-manual.html



# Copyright (2021)
# License MIT (Expat) https://opensource.org/licenses/MIT```

# 77
So, it sort of dawned on me that since no one's commented on my work, that no anon is actually following along atm. **:^)**
> '''''"Why is that?"'''''
I ask myself.
> '''''"Maybe all this is too confusing."'''''
I answer myself.

Accordingly, before I work through repairing/integrating Bjarne's 5 GUI chapter's code from ''PPP2'', I figured it might help any potentially-interested-but-intimidated-ATM anons who actually want to become coders and follow along with what we're doing here on /robowaifu/.

Since getting FLTK running can be a bit of a bear for the novice, I decided that I could create the most basic FLTK window project, ''using just the absolute bare minimum I consider to be feasible''. So here we go Anon, four code/project files just for you:

Here's where it all starts, in main() .
>base_window.cpp
```cpp
#include "Window.hpp"

int main() {
  Window win{742, 442, "RW Always Wins"};
  return win.display();
}```
What's an object without it's description?
>Window.hpp
```cpp
#pragma once

#include <FL/Fl.H>
#include <FL/Fl_Double_Window.H>

class Window : public Fl_Double_Window {
 public:
  Window(int const w, int const h, char const* label);
  int display();
};```
You've gotta tell the class ''how to actually do stuff'' too.
>Window.cpp
```cpp
#include "Window.hpp"

Window::Window(int const w, int const h, char const* label)
    : Fl_Double_Window{w, h, label} {}

int Window::display() {
  this->show();
  return Fl::run();
}```
And finally, last of all the build.
>meson.build
```cpp
project('base_window', 'cpp',
	version : '0.0.1', license : 'MIT',
	default_options : ['cpp_std=c++17',
                       'buildtype=release',
                       'warning_level=3'])

interns_dir = include_directories('include')

cpp_ = meson.get_compiler('cpp')
lib_fltk_dep = cpp_.find_library('fltk')

executable('base_window', ['base_window.cpp', 'src/Window.cpp'],
           include_directories : interns_dir,
           dependencies : lib_fltk_dep)```
Admittedly, this last file is a bit of overkill if you're just going to build something as simple as this. But tbh, it's not all '''that''' complicated. If you can read Python, then you can certainly read this, b/c after all **it's Python lol**.

All I can say is that if you've ever had to deal with the nightmare of say, the ''Win32'' API and drawing a basic window, then the straightforward simplicity of this code is pure pleasure. And it's also tough to convey to the newcomer to all this just how beneficial having a super-light framework such as FLTK is on low-end hardware, etc. This code could literally run blazing fast on an Arduino Nano attached to an LCD display, and do it in a very tiny compiled-footprint too.

Hope this helps someone here /robowaifu/, Cheers.

>base_window-0.0.1.tar.xz.sha256sum
```cpp
91d57314748aa808b1336c7ad6bdccd5edc595c3a8dbfe4ba3c7e99dac6a13f1 *base_window-0.0.1.tar.xz```
''as always, just rename the .pdf extension to .7z then extract files. build instructions are in the meson.build file.''

Also, just in case someone simply refuses to trust the whole 'rename the file to 7z' scheme I'm currently using just so that we can actually keep the codes here on the board itself, here's a previously-typical catbox link too:
https://files.catbox.moe/fkdje9.pdf

>===
-''edit footprint comment''
-''patch East-const in Window.cpp''

# 78
>>12933
OK, I've gotten the initial refactorings worked out where the first example from ch12 is running. That was the hard part, so hopefully it will be pretty smooth sailing here out. I'm going to actually go over to the ''Modern C++'' teaching thread with this project since it's really more about the language itself for this effort. But I want to stash what I have here for safekeeping for now. Cheers.

```cpp
19f86e54b50b6e0bf905e8fd86a2252ad826f7587564511126ded3c6f2e04e57 *teaching_thrd-0.0.1.tar.xz```

# 79
>>12933
OK, I've launched the new project over in the other thread now. (>>13062)

# 80
I don't know dick about programming, but I recently remembered seeing something about a guy putting a tracking device on his cat to monitor how it moves around outdoors and it really closely resembled something called a "Lévy flight", and there's a "Lévy flight foraging hypothesis" suggesting that animals switch between using it to optimize searching efficiency and brownian motion. I was thinking about how robots could use it for realistic behavior for exploring and mapping out its environment.

I keep trying to think-up other ways this could be used but keep drawing a blank. I just wanted to get it off my mind.

# 81
'''''__RW Foundations__ : A suite of robowaifu libraries'''''

A software library is composed of parts that are all intended to cooperatively work together in an interrelated way. This ''uniformity'' helps the men developing the code to reason more easily about the different parts of it, as they tend to have a standardized way of interfacing together with each other. Developing them all 'in concert' under the same 'umbrella' library suite also brings an additional benefit organically; they all work together correctly. Different pieces of software that are developed entirely independently usually take a fair amount of effort to be able to 'convince' them to 'talk' to each other correctly. That's not the situation if they are designed ''in situ'' to do so beforehand.

Additionally, even if one part of the RW Foundations libraries is mostly focused on a specific category of application (eg; ''Bumpmaster'', or ''Waifusearch''), folding those into the overall library will ensure that when the time comes, our robowaifus can also run this same software for us all by themselves. After all, the interfaces of the different library components are by definition meant to work together cooperatively. So, when we reach a level where a functioning robowaifu needs to use Bumpmaster or Waifusearch, she'll be able to do so with very little extra effort on the part of the men developing her.

Thus was born the need for a 'library of libraries'. This is why we've taken some pains and care with the software architecture, and establishing these standards and protocols right up front is important. You should expect that the ''RW Foundations'' code will be an intrinsic part of most all projects going forward here.

Additionally, we'll need to ensure reliability in our systems. The first step towards that end is understanding what is happening within our robowaifu's systems (particularly as we are ''devising and building'' those systems). To that end, we're providing a tagging mechanism; a 't_tag' (Tip Tag) that allows clear accountability of which component is acting/communicating with any other part. These must be easily-identifiable humanly speaking, and unique across the entire system.

We also need to provide great flexibility. To that end, we're allowing for an architectural design that allows any class object to 'embed' ''any other'' class type object within itself for direct and 'personalized' functional access to it's services. This is actually a bit tricky to accomplish. For example think about what's happening inside the computer's memory if we were to simply naively say "OK, Class A, you embed Class B. Class B, you embed Class A". Segfault-city tbh.

Yet that's exactly the kind of thing we need to allow for to provide maximum flexibility in our designs. The RW Foundations architecture provides for this in a simple, efficient, and direct way through base-class indirection and type-casting.

We'll also need to provide a way for access into deeply-nested class hierarchies. Say, if one item in one part of the system needs to 'reach out' to something in another, remote part of the system to gain access to use it's services. For example, remote network access that is decoupled from the main system will require this sort of callgraph-chained approach to be both manageable and reliable.

Providing a simple, direct way to achieve object callgraphs of this sort is needed, or they can quickly explode into a gigantic and unmanageable network that's infeasible to design well or to debug effectively. Not to mention even ''run'' on small-footprint hardware.

Again, The RW Foundations architecture provides for this by the exact same approach; embedding other objects directly within an object, and providing for any-to-any relationships between them all. Two birds, one stone. :^)

>(pt 1 of 2)

>===
-''split large post up''
-''minor prose & grammar edits''

# 82
>>14353
'''''Abstraction and Modularization'''''

We need to take generalized scenario human concepts, for example ''"Sumomo, can you find great bathing software for us please?"'', and turn that into a series of concrete steps for the robowaifu that actually allow her to perceive, understand, plan, and execute on the request. This is a vastly more complex undertaking than an uninitiated newcomer might reckon on, since they commonly tend to personify many things around them. In particular, it's often hard for them to discern why something so obviously human-like as a robowaifu would have any difficulty performing this (highly complicated) task. After all, isn't it just 'common' sense? Get on the Internet and do a search right?

Tackling a problem like this requires us to 'divide-and-conquer' the different parts up if we hope to succeed at solving it. This 'Abstraction and Modularization' is the very heart of the human aspect of software & hardware engineering, regardless of the other tools used.

In the words of the authors of ''The Elements of Computing Systems'' (>>14338),
>'''"You may wonder how it is humanly possible to construct a complete computer system from the ground up, starting with nothing more than elementary logic gates. This must be a humongous enterprise! We deal with this complexity by breaking the system into modules. Each module is described separately, in a dedicated chapter, and built separately, in a standalone project. You might then wonder, how is it possible to describe and construct these modules in isolation? Surely they are interrelated! As we will demonstrate throughout the book, a good modular design implies just that: you can work on the individual modules independently, while completely ignoring the rest of the system. In fact, if the system is well designed, you can build these modules in any desired order, and even in parallel, if you work in a team.'''
>'''"The cognitive ability to “divide and conquer” a complex system into manageable modules is empowered by yet another cognitive gift: our ability to discern between the abstraction and the implementation of each module. In computer science, we take these words concretely: abstraction describes what the module does, and implementation describes how it does it. With this distinction in mind, here is the most important rule in system engineering: when using a module as a building block—''any module''—you are to focus exclusively on the module’s abstraction, ignoring completely its implementation details.'''
''(pp 28-29)''

While their project's design intent is rather different than this one's, these fundamental concepts of ''abstraction'' & ''modularization'' will be vital if we are to succeed at this grand venture.

Providing abstractions for concrete computing tasks within and without a robowaifu, and building those large tasks from the ground up piece-by-piece, using interoperable software and hardware modules & components, is the basic plan going forward. Breaking down conceptual ideas into the different RW Foundation libraries & classes, and then allowing each and every one of these to freely call on all the others is the intended approach we're taking here. This allows us to focus on and think about just a few small parts of the overall problem at a time, without having to keep the entire system in our minds at once.

'''''Function-level access-control'''''
The primary goal behind the ''Tip'' tagging, is to provide a convenient mechanism to validate 'who-is-who' from one function to another across the entire system. However, in addition to the basic idea of tracking flows of the complex callgraphs, it also affords us a minimum degree of access-control, function-to-function. This should help provide another level of assistance to avoid unintentional misuse of function calls, and to help us write more predictable code.

Perfection is unachievable in this life of course. :^) But hopefully using this approach of embedding tags for passing/checking inside calls (and widely throughout the system) can assist us all in our goals for reliable, predictable robowaifu software (whatever it's intended usage). I plan to also keep a close eye on the compute costs involved for this basic access-control mechanism, with an eye to ensuring it runs smoothly on SBCs and microcontrollers. Since it's all C++/C code start-to-finish, it ''should'' stay fairly efficient as long as we keep an eye on things, and do our jobs well.

Future plans for the ''Sumomo'' effort are to begin implementing both the basic function-level access-control mechanisms described, and also a 'channel' mechanism to both maintain the state of (and reduce the pointer-chasing indirections of) to help reduce the resource costs involved with the setup/teardown common to system callgraphs. Hopefully I'll have progress along these lines by the end of this year.

'''>---'''

To that end, I've taken an initial pass at implementing some of the basic architectural approaches outlined here. I've also created a simplistic (but working) test-harness project to prove out 3 of the fundamental aspects of the system's architectural design:
- Every object's t_tag is unique within the system
- Base-class indirection avoids an 'infinite member-objects' cycle
- Working callgraph chain, 4-deep
>

Just follow the standard protocols for extracting/building/running the project, common to all our software projects here. A 'readme.txt' is embedded in the archive file itself to help get you started.

I'll plan to release the more generalized version of ''Sumomo'' that includes some basic class declarations/definitions to begin fleshing out the interrelationships more clearly. This should happen next weekend, to help celebrate the '''5th birthday of /robowaifu/''' coming up.

Cheers.

>rw_sumomo-v211121.tar.xz.sha256sum
```cpp
b814041ea0b347ced9ff3ef284d72f5625ad075897e9a68adc2aebd732f10e27 *rw_sumomo-v211121.tar.xz```
>backup drop
https://files.catbox.moe/xh6b3j.7z

>(pt 2 of 2)

>===
>''minor spelling edit''
>''add the single word 'great'''

# 83
>>14353
>>14354
I discussed the Tip tagging concepts, but I didn't actually demo any usage of it from a caller/receiver. I added a 4th test that demos basic self-tests (potentially for access control, etc.)

>rw_sumomo-v211121.tar.xz.sha256sum
```cpp
ce1246817cb3556fac7a32cb954ff89bf49c34ce67459e550d07c3aa04820b67 *rw_sumomo-v211121.tar.xz```
>backup drop
https://files.catbox.moe/31zxct.7z

# 84
>>14354
Thank you, this sounds very exciting. I just wonder how hard it will be to understand how it works. Also, I'm currently working on the hardware and won't look into my software anytime soon. But glad to see that there's some progress. 
Looking forward to see an example for using  output from some GPT-like network and then letting a parser work with that data, or several doing that in parallel.

# 85
>>14354
You've written a lot and I mostly agree with your object oriented stance. I appreciate that you are working with C++ as it is rather efficient for an object oriented programming language. I program in Java and Python (blame my uni, it's all they teach) but, have wanted to try C++.

>Commonly tend to personify many things around them
This is a major problem indeed. Hopefully this project fixes that problem by providing anons with clarity on how robotic minds actually work.

I infer from the title of this project that you're planning on building a Sumomo Tan? If so, know that you have frens that will help.

# 86
>>14360
>Thank you, this sounds very exciting
Y/W. Yes, I agree. I've spent quite a bit of time making things this 'simple', heh. :^)
>I just wonder how hard it will be to understand how it works.
Well, if we do our jobs ''perfectly'', then the software's complexity will '''exactly''' mirror the complexity of the real-world problem itself whatever that may prove to be in the end. However, in my studied opinion that's not how things actually work out. I'd suggest a good, working solution will probably end up being ~150% the complexity of the real problemspace?

Ofc if you __really__ want to understand it, you'll need proficiency in C++ as well. I'd suggest working your way through the college freshman textbook known as 'PPP2', written by the inventor of the language himself, if you decide to become serious about it (>>4895) . 

Good luck Anon.

>>14361
>as it is rather efficient for an object oriented programming language.
I agree it certainly is. But it's also a kind of 'Swiss Army Knife' of a programming language. And in it's modern incarnation handles basically every important programming style out there. But yes I agree, it does OOP particularly well.
>but, have wanted to try C++.
See my last advice above.
>Hopefully this project fixes that problem by providing anons with clarity on how robotic minds actually work.
If we do our jobs well on this, then yes, I'd say that's a real possibility Anon. Let us hope for good success!
>I infer from the title of this project that you're planning on building a Sumomo Tan?
Indeed we are. Those CLAMP girls knocked it out of the park with the character of ''Sumomo''. She's the perfect fun little mobile-unit-robowaifu! :^)
>If so, know that you have frens that will help.
That's encouraging to hear Anon. Thank you.

'''==='''

-Added 'operator==()' for doing a deep equality check for comparing Tips, field-by-field.
>

>rw_sumomo-v211122.tar.xz.sha256sum
```cpp
403e3905900c01f7d6b8b32263aad6b5c427e408f42ca0a3fa43966df6504e90 *rw_sumomo-v211122.tar.xz```
>backup drop:
https://files.catbox.moe/zj3hwa.7z

# 87
OK, I added another class that implements the ability to explicitly and completely specify exactly which embedded member objects to to include during it's construction. This could be a very handy capability to have (and a quite unusual one too). Imagine we are trying to fit RW Foundations code down onto a very small device. The ability to turn off the memory footprint of unused fields would be valuable.

However, the current approach 'complexifies' **lol is that a word? :^)** the initialization code a good bit, and probably makes maintenance more costly going forward as well (an important point to consider). I'm satisfied that we have solved the functionality, but I'll have to give some thought to whether it should be a rigorous standard for the library code overall, or applied only in specific cases in the future. 

Anyway, here it is. There's a new 5th test for it as well.

'''==='''

-add specified member instantiations
>

>rw_sumomo-v211122.tar.xz.sha256sum
```cpp
61ac78563344019f60122629f3f3ef80f5b98f66c278bdf38ac4a4049ead529a *rw_sumomo-v211122.tar.xz```
>backup drop:
https://files.catbox.moe/iam4am.7z

# 88
>>14353
>related (>>14409)

# 89
leaving this here
Synthiam software
https ://synthiam.com/About/Synthiam

