# 1
Creating a functional Robowaifu is a yuge Systems Engineering problem. It is arguably the single most complex technical engineering project in history bar none, IMO. But don't be daunted by he scale of the problem anon **(and you will be if you actually think deeply about it for long, hehe)**, nor discouraged. Like every other major technical advance, it's a progressive process. A little here, a little there. In the words of Sir Isaac Newton, "If I have seen further it is by standing on the shoulders of Giants." Progress in things like this happen not primarily by leaps of genius--though ofc that also occurs--but rather chiefly comes by incremental steps towards the objective. If there's anything I'm beginning to recognize in life it's that the key to success lies mainly in one unwavering agenda for your goals: '''Just don't quit'''.

>tl;dr
Post SE and Integration resources ITT.

www.nasa.gov/sites/default/files/atoms/files/nasa_systems_engineering_handbook.pdf

# 2
>>98
From  §1.1:
>"This handbook should be used as a companion for implementing NPR 7123.1, Systems Engineering Processes and Requirements,…"
''Version 1B, Effective Date: April 18, 2013'', is here:
snebulos.mit.edu/projects/reference/NASA-Generic/NPR_7123_1B.pdf

>pic sauce
linuxgizmos.com/linux-based-robonaut-2-preps-for-active-iss-duty/

# 3
>Systems Engineering
The kikepedia article is a pretty good intro to why SE is it's own discipline.
en.wikipedia.org/wiki/Systems_engineering

# 4
One of the goals we need to be striving for is effective modeling and behavioral analysis of the complex & interdependent systems within robowaifus. There is already a large body of literature on this topic. After a little research I've settled on ''mCRL2'' as a good place to start, as well as the Actor-based approach to behavior. I'll be spending some time over the summer seeing about modeling some behavior like a robowaifu arm/hand/ipcnet subsystem as a test case.

Pics related is the book & site available for the tool designed to facilitate creating and simulating Communicating Processes Algebra.
https://www.mcrl2.org/web/user_manual/index.html
https://github.com/mCRL2org/mCRL2

I built the tool successfully on Manjaro Linux from the repo, and there are some pre-builts available in different package managers like Ubuntu's.

https://en.wikipedia.org/wiki/Algebra_of_Communicating_Processes
https://en.wikipedia.org/wiki/Process_calculus
https://en.wikipedia.org/wiki/Calculus_of_communicating_systems
https://en.wikipedia.org/wiki/Calculus_of_broadcasting_systems
https://en.wikipedia.org/wiki/Actor_model

# 5
>>3720
Book related contains a paper outlining both the mCRL2 Toolset language and the workflow, starting on p21.

# 6
Interesting ideas about using ML to automate optimizations of various systems resources, primarily related to compute cores.

>Abstract—Efficient sharing of system resources is critical to obtaining high utilization and enforcing system-level performance objectives on chip multiprocessors (CMPs). Although several proposals that address the management of a single microarchitectural resource have been published in the literature, coordinated management of multiple interacting resources on CMPs remains an open problem.
>We propose a framework that manages multiple shared CMP resources in a coordinated fashion to enforce higher-level performance objectives. We formulate global resource allocation as a machine learning problem. At runtime, our resource management scheme monitors the execution of each application, and learns a predictive model of system performance as a function of allocation decisions. By learning each application’s performance response to different resource distributions, our approach makes it possible to anticipate the system-level performance impact of allocation decisions at runtime with little runtime overhead. As a result, it becomes possible to make reliable comparisons among different points in a vast and dynamically changing allocation space, allowing us to adapt our allocation decisions as applications undergo phase changes.
>Our evaluation concludes that a coordinated approach to managing multiple interacting resources is key to delivering high performance in multiprogrammed workloads, but this is possible only if accompanied by efficient search mechanisms. We also show that it is possible to build a single mechanism that consistently delivers high performance under various important performance metrics.

# 7
Not an engineering book, rather more like a Tedpill-ish rant against complex tech, but it probably has something important to say about how we as engineers should approach the complex interdependencies inside our robowaifu's system.

>''...and big accidents almost always have very small beginnings.[3] Such events appear trivial to begin with before unpredictably cascading through the system to create a large event with severe consequences.''

>Perrow identifies three conditions that make a system likely to be susceptible to Normal Accidents. These are:
>''The system is complex''
>''The system is tightly coupled''
>''The system has catastrophic potential''

https://en.wikipedia.org/wiki/Normal_Accidents

# 8
>>98
>>4631
Now having a year's experience as an electronics engineer, can confirm that integration is now of the hardest jobs/skills. Currently working between hardware and software, and I now put so little trust in our designers. Documentation is meh, to properly understand the current chip being designed, you need to know the mistakes made (and carried over) from at least 3-4 years ago. And I'm honestly amazed our chips are popular, given how buggy they are XD Changed my view on the industry all together. This is for commercial, large volume chips, and it might be different for smaller batch, industrial chips (hahahahahaha).

# 9
>>4632
That's interesting Anon. So, I'm curious how these design flaws manifest themselves in the chip's observable behavior, and what approaches are used to ameliorate the issues that come up (preferably in laymen's language hehe).

# 10
>>4637
Sure I'll just make sure we're on the same page here, I'll briefly cover what a chip is usually composed of.

Like a mechanical system which consists of components (or even a computer), so too does the integrated circuit (IC) consist of smaller blocks with specific functions. These blocks would be designed by individual designers and then combined together into progressively bigger units, until eventually you reach the top level, where you can see the main functions of the chip. This hierarchy allows to split the work and allow many people to work on the design at the same time.

You might already notice a glaring issue, having too many people work on blocks, especially if they are in different sites across the world, means ensuring everyone understands the overall functionality is difficult. This means in practice, designers might not consider how their block might affect something else further down the line.

Our team runs an emulator of the chip that works in real time, allowing to test functionality on minute/hour/daily scales, which would be too much for simulations. However we also usually see the integration issues. The way we test also doesn't use firmware (bare metal) which means we need a good understanding of how to drive certain blocks once they have been integrated into the chip. Rarely the case due to sheer complexity, shitty docs, important tidbits being engineers' heads requiring regular meetings and email conversations. Though it's really cool to work on the boundary between hardware and software.

For example, there's a comms block that talks to the outside world using a few serial protocols (like SPI) which is old and hasn't been given the chance to be fixed and completely verified. When it was designed initially, the plan was to use it for a short while, but it continues to exist today in new chips (nothing more permanent than temporary eh?). It has such a long list of bugs that the firmware teams constantly has to make workarounds, or just not use the certain modes of operation altogether. And one of my first red pills of tech business: no matter how shit a block, no matter how many workarounds, no matter if even the client is affected because the datasheet limits how features can be used, if you have the firmware, leave it alone. Digital designer can make small blocks in days, writing firmware would take weeks/months. And when consumer grade chips are taped-out (released for production) on a yearly basis, your prioritise the time on new, faster, better features. If you don't, the company falls through.

It's retarded, we have a family of chips with the SAME problems year after year. Let's just say I would NEVER use them in any critical application. Though they are not designed for such areas really.

As an engineer who studied advanced subjects for a while, it feels like a waste to spend months tracking an issue that could likely be figured out by someone who saw it years ago. But fuck am I staying here for 5 years just to get better at figuring out their shitty design.

Given my age I can't waste time if I want to make great developments (like robo waifu sub systems ;) ). This experience has been great for how NOT to design and test chips, so I'll be sure to make better use of my time in my own projects. 

Oh and please allocate time in your projects to document aspects of your designs that are **not** obvious. I know it's hard to do so, designing is usually more fun, but you might just save some poor sod a few days XD

# 11
>>4638

>''...of how to drive certain blocks once they have been integrated into the chip.''
Mind expanding on this a little? What does 'drive' specify in this context? Does this have something to do with the electrical signals, levels, and timings in the boundary interfaces between system blocks (or maybe across busses)?

>When it was designed initially, the plan was to use it for a short while, but it continues to exist today in new chips
Kek. Software engineering experiences this exact same issue.
>''Hey Ted! We need that FoobarMatic routine by Friday, how's the progress coming?''
>*spews coffee* ''Umm, well Bill, I was just testing a couple of little features, but we'll be ready''
>*36 hours of cruchmode-style effort later...*
>''Hey Bill, here's that code you wanted''
>''Ted, you look like shit. You feeling OK Bro?''
>''I'm good. Umm, I have a uhh, doctor's appointment this morning Bill. I should be back this afternoon''
>''See you later then Ted''
>*5 minutes later*
>''TED! What is this dogshit!? Well, I guess I'll merge it, we have to have '''something''' by noon. FUUUUUU.''
>*3 years pass*
>''Ted, you know that shitty FoobarMatic code you wrote? Well we need to extend it a little this week.''
>''Bill, about that stuff, I never meant it to stay around more than a week...''
>''Forget it. So, we need to enhance it. Just a few more features.''
>''How many new features, Bill?''
>''About 200 or so. By Friday, Ted.''
>*spews coffee*

>As an engineer who studied advanced subjects for a while, it feels like a waste to spend months tracking an issue that could likely be figured out by someone who saw it years ago. But fuck am I staying here for 5 years just to get better at figuring out their shitty design.
>Given my age I can't waste time if I want to make great developments (like robo waifu sub systems ;) ). This experience has been great for how NOT to design and test chips, so I'll be sure to make better use of my time in my own projects. 
Well, I hope your experience can help everyone here Anon. Gambatte, you can do it! :^)

>Oh and please allocate time in your projects to document aspects of your designs that are not obvious. 
Thanks for the advice. I try to figure out good function names in my code, and use basic comments when needed (though comments can easily get out of sync with a lazy coder. Invalid comments can be worse than no comments heh). Right now I'm going through some studies to figure out how various types of refactoring work best, and also writing tests for units (even tried dabbling with Test-Driven Development (TDD) as well).

We'll get there in due time Anon. BTW, thanks for the effort-post Anon.

# 12
>>4639
>Mind expanding on this a little? What does 'drive' specify in this context?
Apologies, I often use terminology interchangeably with not too much regard for ambiguity. In this case I meant "driving" as controlling the behaviour (like a horse driver). When you hear the term "drivers" in an OS, that's actually code that configures how a given peripheral can be used and provides a common set of functions for the OS to use. We essentially work at that level or lower (direct hardware).

When accessing a microcontroller or sensors with a communication interface (like SPI etc.), you have registers which you can write to in order to turn on certain features. A register is volatile memory (usually 8-32 bits in length) that can store data and allows software to control hardware.

For example, in a microcontroller you have registers for configuring the state of General Purpose Input/Output (GPIO) pins. Settings might involve whether the pin is an input, output, has a pull-up resistor, set for special function like an ADC, PWM, etc.

So what I meant in the context of my company's chips, is that it's difficult to know exactly which registers need to be set to enable one feature or another. The software team works separately from us and usually already have pre-written code (drivers) for configuring, say, the SPI comms. Whereas I often have to read a doc, realise info is missing, and then ask someone else.

>...I try to figure out good function names in my code, and use basic comments when needed...
Currently the assembler I'm coding in C (my processor project) and it's really hard to write function names that are not too long and still make sense XD.
Also hard to make "switch" and "if" statements not look like shit. I'm aiming for no more than 80 chars per line, to improve readability when viewed with another doc. Splitting bigger functions and using global library-scope variables helps.

>We'll get there in due time Anon.
Indeed, the more I live the more I realise that only unwavering passion can make real progress, and no matter how big a corporation, without the individual passion, will eventually crumble. I'll build my dancing waifu soon enough, just to do Viennese Waltz again :D

>BTW, thanks for the effort-post Anon.
Hey, it's fun to discuss these topics with my you lads ;)

# 13
>>4640
>Hey, it's fun to discuss these topics with my ~~you~~ lads ;)
Damn it grammar...

# 14
>>4640
Thanks for the explanation Anon, that definitely clears things up for me.

>it's really hard to write function names that are not too long and still make sense XD.
I too deal with this issue (what conscientious developer doesn't heh). I think there are at least 2 or 3 solid engineering principles that help out in general, if you can figure out a way to adopt them:
>1. limit the visible scope of named elements. then they can then be reasonably shorter and still 'make sense'.
>2. take advantage of language features to help reduce any ambiguity.
>3. don't name items ''at all'' if possible. eg, use anonymous functions, objects, etc. when reasonable.

I'm writing in C++ not C at the moment, and I'm well aware they are different worlds. One aspect of our software that we both must strive for is clarity of code, as well as robustness of code. I'll try to throw out a straightforward example of what I mean for you. I'm going to use a simple window display via the ''FLTK cross-platform C++ GUI toolkit'' (I'd personally consider it primarily a set of C libraries myself, but that's their official description https://www.fltk.org/ ). It's remarkably lightweight for a GUI system, just about the best there is for the full feature-set it offers. It goes back quite a ways to the NeXT & SGI and is still under active development today, so it's a good example of a well wrung-out graphics system by this point in time.

So, the FLTK has the notion of a window, whose signature is this (I'll use the double-buffered version as the example here):

[code]Fl_Double_Window(int X, int Y, int W, int H, const char *l = 0)[/code]
In practice, constructing one of these windows looks basically like this in C++:

[code]Fl_Double_Window foo_win{100, 100, 600, 400,"foo"};[/code]
Not too uncommon, but if you are a newb unfamiliar it's possible you'd mix up your X for your W, or your Y for your H. Heck, even an experienced dev might do this. Since these four ambiguous ints are all about a single '''idea''' namely, a ''rectangle'', a more solid approach would be to encapsulate them together as such. Further, since the X & Y are really the ''origin point'' for the rectangle shape, they present a second good opportunity for encapsulation together into a point.

Now the window constructor can just talk about it's rectangle and the window title. C++ makes such a thing very simple via inheritance and delegating constructors. If I create a Point and Rect class first, then I can inherit from the base FLTK class into my own Window class like this:

[code]class Window : public Fl_Double_Window
{
public:
  Window(const Rect& rect, const char* title)
      : Fl_Double_Window{rect.origin.x, rect.origin.y, rect.w, rect.h, title} {}
};[/code]
Now when creating a window, what I need to pass as args is a ''Rect'' and a title string. I unpack the Rectangle in the delegating constructor, passing that information on to the base Fl_Double_Window class. While this requires some extra groundwork (three new classes), I think it's clearer in it's meaning at the caller than having 4 unnamed & ambiguous ints as arguments (even if it increases the actual text length at the caller).

Further, ambiguity can be significantly reduced at the calling site by using ''designated initializers'' which specify precisely what values belong to what parameters. And robustness can be enhanced by using inline construction for the statement, which effectively guarantees limiting the scope of the variables to just the construction. Combining these ideas, the resulting call now looks like this:

[code]Window window{
      .rect  = Rect{.origin = Point{.x = 100, .y = 100}, .w = 600, .h = 400},
      .title = "Rect designated inits ctor"};[/code]      
Definitely wordier, but dramatically improved in terms of maintenance and overall reliability IMO.      

Here's the entire working example that puts it all together Anon:
[code]#include <FL/Fl.H>
#include <FL/Fl_Double_Window.H>

struct Point
{
  Point(const int x, const int y)
      : x{x}
      , y{y} {}

  int x, y;
};

struct Rect
{
  Rect(const Point origin, const int w, const int h)
      : origin{origin}
      , w{w}
      , h{h} {}

  Point origin;
  int   w, h;
};

class Window : public Fl_Double_Window
{
public:
  Window(const Rect& rect, const char* title)
      : Fl_Double_Window{rect.origin.x, rect.origin.y, rect.w, rect.h, title} {}
};

int main() {
  Window window{
      .rect  = Rect{.origin = Point{.x = 100, .y = 100}, .w = 600, .h = 400},
      .title = "Rect designated inits ctor"};
  window.color(FL_BLACK);
  window.show();

  return Fl::run();
}[/code]

# 15
>>4645
One other thing I neglected to specifically point out, notice how using nested encapsulation makes the the delegating constructor arguments entirely self-documenting--no comments needed whatsoever.

[code]Fl_Double_Window{rect.origin.x, rect.origin.y, rect.w, rect.h, title}[/code]

# 16
>>4646
Indeed, that is a lot cleaner Anon.
The issue I hear about a lot is the overuse of objects (having too many object hierarchies which just make understanding the code worse. In your case this is nice and simple though.
Currently I'm passing structs in in order to increase clarity.

How do I post code btw? The julay page doesn't show how.

# 17
>>4647
>In your case this is nice and simple though.
Thanks! Inheritance should be used, not abused. If it doesn't increase clarity at the caller, or bring some other needed improvement then don't use it is my advice.

>How do I post code btw?
[code][code] ... [/code][/code]

You put the code between to bracket tags with 'code' in them, one opening (just the brackets), and one closing (with a leading slash).

# 18
>>4648
https://julay.world/.static/pages/posting.html
(down in the tags section)

# 19
Not sure if this belongs in that thread, but here's a vid about control of robots: https://youtu.be/A22Ej6kb2wo
Here is his channel: https://www.youtube.com/channel/UChfUOAhz7ynELF-s_1LPpWg
The guy is involved with Drake, some alternative to ROS? https://drake.mit.edu/

# 20
>>4741
Thanks for those links Anon. Looks like MIT has moved forward with these efforts quite nicely over time.

# 21
>related crosspost (>>11160)

# 22
While this is nominally a database book ''per se'', it's largely focused on optimizations for data throughput. As such, it certainly qualifies as a valuable reference for robowaifu systems engineering. In particular, chapter 11 ''Stream Processing'', is a very important topic in the realms that the '''RPCS''' would seek to address.
>

www.oreilly.com/library/view/designing-data-intensive-applications/9781491903063/
https://github.com/ept/ddia-references

# 23
While this metaphor was explicitly developed for the software industry, it has many corollaries in other industries. For example, SophieDev Anon is trying his hand at 3D modeling. As a TD in the industry, I have seen literally dozens of examples of people -- artists in particular -- piling up technical debt rushing work with excessive shortcuts to try and meet some intermediate asset checkpoint and just get it out the door. But during that effort, they were not considering the later costs to fix their hot messes ''before'' being able to continue the overall project itself. That's technical debt in the creative industry, and it has direct implications for our robowaifu designs.

Another more apparent technical debt for some of us might be the choice to use the Python programming language as a means to 'quickly' get various AI projects up and going. Just like incurring real-world debts, this can speed up the prototyping stage measurably. But let's imagine that it turns out that multi-gigabyte libraries might have a hard time even fitting inside a small compute hardware platform within our early robowaifus -- much less running well on them. Further, suppose that robowaifus need to be able to respond in realtime/neartime for most AI-related tasks, and we find out that literally the only way to make these processes work properly is by using embedded C code on the microcontrollers instead. Now, the original ideas will need to be recast into this more efficiency-oriented approach ''first'' before it will actually work IRL. That's technical debt in software industry (with a close corollary in the electronics industry), and it must be repaid quickly if the project isn't to stall out.

We could discuss mechanics, power, materials, and so on. Technical debt is a potential phenomenon for all of these arenas. This is an important and fairly deep topic actually, and I'd like to begin a discussion with robowaifuists  about how we can both take advantage of technical debt, and also remediate it ('pay it back') in our works too.

If we don't account properly for this phenomenon early, we almost certainly as a group will fall literally years behind in our ability to deliver robowaifus (hopefully well before the globohomo ruins everything).

For any anons unaware of the concept, here's where the idea got started:
http://wiki.c2.com/?WardExplainsDebtMetaphor
https://www.agilealliance.org/introduction-to-the-technical-debt-concept

# 24
>>11904
>technical debt
>sculpting
I tried to do everything in CAD, but it has limits. I never thought sculpting parts should be avoided completely, only minimized as much as possible. Either way, there aren't many users here which are trying out stuff and posting it in the first place. The more parts we have we can work with, the better.
>Python bashing, once again
Code can be replaced piece by piece and called by the rest of the codebase. We won't have gigabytes of Python code anyways, I think. That aside, we will need to integrate as many programs from other people as possible, in all kinds of languages. Trying to write everything from the scratch in C or C++ would be some delusional attempt, so frustrating that the few people which are even trying now, would drop out,  since there would be no hope of ever archiving anything in some reasonable amount of time.

# 25
>>11917
You seem quite antagonistic to my basic claims, so I'll put them all aside for the moment (my real-world experiences notwithstanding).

In a more general sense then, can you offer any advice on my specific desired outcome through this conversation then, Anon? Namely;
>'''''how we can both take advantage of technical debt, and also remediate it ('pay it back') in our works too.'''''

