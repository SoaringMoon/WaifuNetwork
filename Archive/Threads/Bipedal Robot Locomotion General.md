# 1
We need to talk about bipedal locomotion. It's a complicated topic but one that has to be solved if we are ever to have satisfyingly believable robowaifus. There has surely already been a lot of research done on this topic, and we need to start digging and find the info that's out there. There are some projects that have at least partial robolegs solutions working, but none that I know of that look very realistic yet. We likely won't come up with some master-stroke of genius and solve everyone's problems here on /robowaifu/, but we should at least take a whack at it who knows? We certainly can't accomplish anything if we don't try.

I personally believe we should be keeping the weight out of the extremities – including the legs – while other anons think that we should add weight to the feet for balance. What's you're ideas anon? How do we control the gait? How do we adjust for different conditions? What if our robowaifu is carrying things? **What about the legs during sex?** Should we focus on the maths behind MIP (Mobile Inverted Pendulum), or is there a different approach that would be more straightforward? A mixture? Maybe we can even do weird stuff like reverse-knee legs that so many animals have. Robofaun waifu anyone? What about having something like heelys or bigger wheels in the feet as well?

I'm pretty sure if we just put our heads together and don't stop trying, we'll eventually arrive at least one good general solution to the problem of creating bipedal robot legs.

>tl;dr
ITT post good robowaifu legs

>tech diagrams sauce
www.youtube.com/watch?v=pgaEE27nsQw
www.goatstream.com/research/papers/SA2013/SA2013.pdf

# 2
Neuromechanical simulation of human locomotion (SimGait + HBP)

https://biorob.epfl.ch/research/research-dynamical/simgait/

# 3
>>1601
Multi-Modal Locomotion
By the same lab. Includes executable simulation software links (Win, Mac).

https://biorob.epfl.ch/research/research-humanoid/research-humanoid-walkman/

# 4
>>1602
Related papers:

Walking controller
>Imprecise dynamic walking with time-projection control

Human-like animations
>Scalable closed-form trajectories for periodic and non-periodic
human-like walking

sauce:
github.com/salmanfaraji/Walking3LP

# 5
Neural Control of Balance During Walking
>Neural control of standing balance has been extensively studied. However, most falls occur during walking rather than standing, and findings from standing balance research do not necessarily carry over to walking. This is primarily due to the constraints of the gait cycle: Body configuration changes dramatically over the gait cycle, necessitating different responses as this configuration changes. Notably, certain responses can only be initiated at specific points in the gait cycle, leading to onset times ranging from 350 to 600 ms, much longer than what is observed during standing (50–200 ms). Here, we investigated the neural control of upright balance during walking. Specifically, how the brain transforms sensory information related to upright balance into corrective motor responses. We used visual disturbances of 20 healthy young subjects walking in a virtual reality cave to induce the perception of a fall to the side and analyzed the muscular responses, changes in ground reaction forces and body kinematics. Our results showed changes in swing leg foot placement and stance leg ankle roll that accelerate the body in the direction opposite of the visually induced fall stimulus, consistent with previous results. Surprisingly, ankle musculature activity changed rapidly in response to the stimulus, suggesting the presence of a direct reflexive pathway from the visual system to the spinal cord, similar to the vestibulospinal pathway. We also observed systematic modulation of the ankle push-off, indicating the discovery of a previously unobserved balance mechanism. Such modulation has implications not only for balance but plays a role in modulation of step width and length as well as cadence. These results indicated a temporally-coordinated series of balance responses over the gait cycle that insures flexible control of upright balance during walking.

<Keywords: balance, walking, neural feedback, vision, virtual reality, sensorimotor control

www.ncbi.nlm.nih.gov/pmc/articles/PMC6146212/

# 6
Dynamic Principles of Gait and Their Clinical Implications
>A healthy gait pattern depends on an array of biomechanical features, orchestrated by the central nervous system for economy and stability. Injuries and other pathologies can alter these features and result in substantial gait deficits, often with detrimental consequences for energy expenditure and balance. An understanding of the role of biomechanics in the generation of healthy gait, therefore, can provide insight into these deficits. This article examines the basic principles of gait from the standpoint of dynamic walking, an approach that combines an inverted pendulum model of the stance leg with a pendulum model of the swing leg and its impact with the ground. The heel-strike at the end of each step has dynamic effects that can contribute to a periodic gait and its passive stability. Biomechanics, therefore, can account for much of the gait pattern, with additional motor inputs that are important for improving economy and stability. The dynamic walking approach can predict the consequences of disruptions to normal biomechanics, and the associated observations can help explain some aspects of impaired gait. This article reviews the basic principles of dynamic walking and the associated experimental evidence for healthy gait and then considers how the principles may be applied to clinical gait pathologies.

www.ncbi.nlm.nih.gov/pmc/articles/PMC2816028/

# 7
Modeling robot geometries like molecules, application to fast multi-contact posture planning for humanoids
>Traditional joint-space models used to describe equations of motion for humanoid robots offer nice properties linked directly to the way these robots are built. However, from a computational point of view and convergence properties, these models are not the fastest when used in planning optimizations. In this paper, inspired by Cartesian coordinates used to model molecular structures, we propose a new modeling technique for humanoid robots. We represent robot segments by vectors and derive equations of motion for the full body. Using this methodology in a complex task of multi-contact posture planning with minimal joint torques, we set up optimization problems and analyze the performance. We demonstrate that compared to joint-space models that get trapped in local minima, the proposed vector-based model offers much faster computational speed and a suboptimal but unique final solution. The underlying principle lies in reducing the nonlinearity and exploiting the sparsity in the problem structure. Apart from the specific case study of posture optimization, these principles can make the proposed technique a promising candidate for many other optimization-based complex tasks in robotics.

<Terms: Humanoid Robots, Kinematics, Biologically-Inspired Robots, Task Planning, Gesture, Posture and Facial Expressions, Optimization and Optimal Control

https://infoscience.epfl.ch/record/230040/

# 8
>>237
I think the most fundamental thing for walking is balance. It could be optimized for as the minimum amount of energy to maintain a pose or state. It's really important we acknowledge robowaifus will have different bodies and parts than us and what they find balanced to walk with will be something else entirely unless we pay close attention to engineer their bodies with similar weight, range of motion and forces as us.

The second most important thing is experience. Robowaifus will need to practice to improve their world model's prediction function to judge the weight of objects, their weight distribution, slipperiness of surfaces and such to understand what the minimum energy state will be. There are things robots don't have sensors for like feeling a cylinder sliding through their grip, but there are visual cues and other things that can be detected such as slipping objects feeling lighter. Robots can also have completely different sensors in their body parts such as accelerometers and gyroscopes.

Objects in general need to be approached with caution and gentleness, using only the minimum amount of force needed to achieve tasks. Overexertion requires corrections and can be identified within the system as shaking. In disaster situations rubble and debris may also move when walked upon. Motion planning will need to navigate uncertain environments and avoid potential motor stalls and falls by taking the safest understood route, unless there is no other way to go or it's too dangerous and should stop. Collisions with other people, stairs and moving vehicles must be also factored in but I think finding the minimum energy required will naturally solve this because walking into a bus going 50 kph is gonna be a lot of energy to overcome.

I wish I had some experience with 3D programming. If someone could put together a simple mechanical simulation or find one, I could rig up some AI to first master using its limbs and then optimize it to walk towards a goal with minimum energy. It would help us study how limb weight, weight distribution, joint placement, actuator power and range of motion will affect gait and we can come up with better designs that can balance more like a human being or something else entirely that's beautiful and practical in its own way.

# 9
>>1608
>If someone could put together a simple mechanical simulation 
<or find one,
would this one do?
>>1602

# 10
>>1610
Not sure, I'm on Linux and would have to see if it can run in Octave. I do most of my AI in PyTorch and it seems Octave has a Python interface.

I think this will be helpful but I was thinking more of a simulation where weights can be attached to body parts for more realistic torque calculations. That way we can test, design and evolve parts to be more functional in the real world.

# 11
>>1611
Well, I'm setting up Octave myself for the very first time right at this moment to try and test the program, so you're ahead of me heh.

Yes, that diagram helps. I'm think about building a 3D model for robowaifus starting with a graph description of the bones for rigging using boost.graph. Once that's workable to the degree where mesh data can be bound to the bones and rendered, do you think you could work with it?

# 12
Here's the error I'm getting trying to run the m script w/ Octave:
[code]johnny@mactoshub:~/_msc/rw/repos/Walking3LP$ octave Walking3LP.m
error: 'gui_mainfcn' undefined near line 62 column 5
error: called from
    Walking3LP at line 62 column 5[/code]

# 13
>>1611
BTW, if you examine the GUI image, you see that mass can be added/removed from limbs for the sim runs. Looks very flexible to me tbh.

# 14
>>1614
Here's the code section in question. The error line mentioned is the one inside the else clause. Apparently 'gui_manfcn()' is a Matlab API which Octave must have a different name for. Any matlab guys here?
[code]% Begin initialization code - DO NOT EDIT
gui_Singleton = 1;
gui_State = struct('gui_Name',       mfilename, ...
                   'gui_Singleton',  gui_Singleton, ...
                   'gui_OpeningFcn', @Walking3LP_OpeningFcn, ...
                   'gui_OutputFcn',  @Walking3LP_OutputFcn, ...
                   'gui_LayoutFcn',  [] , ...
                   'gui_Callback',   []);
if nargin && ischar(varargin{1})
    gui_State.gui_Callback = str2func(varargin{1});
end

if nargout
    [varargout{1:nargout}] = gui_mainfcn(gui_State, varargin{:});
else
    gui_mainfcn(gui_State, varargin{:});
end
% End initialization code - DO NOT EDIT[/code]

# 15
>>1615
>gui_mainfcn() *

# 16
There's a simple but inelegant short term solution; add an extra limb with omnidirectional wheels to the bipedal robot. It can be an armature that's detachable at the hip with the wheels behind the body. Or it can retract by folding inside the lower or upper legs depending on the kinematics.

This would allow for decent mobility at a slightly faster than shuffling pace as 3 points of contact on the ground at all times creates static rather than dynamic locomotion. It also lets you add a lot more weight to the robot without worrying about stability.

This is the only robot I've seen that tries a hybrid folding limb approach and is pretty innovative. As for a simple mechanical simulation program I'm also trying to find something that does this. playdynamo.itch.io/dynamo looked promising but it performs terribly in Wine and keeps trying to connect to the internet when blocked. I might give FreeCAD or Blender another try but both of those are very time consuming to get used to.

# 17
>>1617
clever idea bout the wrap-around wheels heh. we've had numerous discussions on the alternatives to bipedalism for our robowaifus here over the years. i think the general consensus for those of us not willing to give up on a human-like form for our waifus **like myself :^)** the nearest workable alternative seems to be to give her a motorized wheelchair to move around with until we can perfect bipedal locomotion.

Still, good ideas anon keep them coming.

# 18
>>1617
BTW, I think the Pepper robot uses a tri-wheel scheme for it's base?

# 19
>>1618
I see my approach more as an assisted form of bipedalism building up to the real thing. This quick sketch might give a better idea of what I'm talking about. It would still have the appearance of walking so it's not comparable to sitting in a wheelchair or being carted around vertically on a hand truck.

By using two mechanum wheels you get to spin around by running each wheel in opposite directions. Omnidirectional wheels have their own advantages and disadvantages.

# 20
>>237
70.000 USD for a fucking prosthetic leg, jfc.

# 21
>>1621
I see. Yes that diagram does make it clear. In effect, you are providing her with an irl cartoonishly oversized 'foot' with which to get around on, but one that would shrink back to normal size when not needed.

>>1622
Ever price even the most basic of medical supplies in a hospital context anon? No surprises tbh.

# 22
>>1624
>Ever price even the most basic of medical supplies in a hospital context anon? No surprises tbh.

Yep, but 70k is still a lot for a device that's not even worth a fraction of the price in materials or manufacturing. I mean what's to be expected when every megalomaniac cocksucker and their granny is allowed to milk people's health for all it's worth and call it a day.

# 23
>>1625
Look I'm not promoting their (((approach))) I'm simply encouraging you to be realistic. Let's continue this off-topic discussion in the Lounge if you'd like.

# 24
>>1621
Looking into humanoid bipedal robots that have a single wheel on its feet this EMIEW2 is the closest one. Other robots typically have several wheels per foot(Zephyr) have the wheel as part of a normal robot foot to add wheeled locomotion(GoRoBot) or more than a pair of legs. The other decent design is the WL-16 leg platform using WS-2 feet but that has a caster alongside a powered wheel.

I've gone through at least 50 research papers on robot walking methods(and have another 50 to go through) and have seen some interesting designs and solutions but none of them use the approach I'm proposing where the wheel is only used to shift the center of gravity during the stride while keeping the robot stable with 3 points of contact on the ground at all times.

One thing that hit me when browsing another forum are those minisegways cost less than $200 now. Rather than trying to do bipedal locomotion I'm going to have my first model balance properly on top of that until a cheap solution is found.

# 25
>>1776
>I've gone through at least 50 research papers on robot walking methods(and have another 50 to go through)
Mind posting a few of them here for the rest of us anon?

# 26
>>1776
>hoverboards
Yep, we've had this conversation before now. The posts haven't been restored here yet but I came down in favor of the idea myself.

# 27
>>1776
Why is that robot in the middle wearing a diaper?

# 28
>>1777
Eh most of them aren't worth reading otherwise I'd have uploaded a pack of them here. These two are probably the best I've found on the topic for a general overview.

>>1778
The segway mini isn't really a hoverboard since you use your knees rather than your feet to control it. The center of gravity is much lower to the ground and there's no having to keep the robot upright on it.

>>1794
It looks even more like a diaper from the back. The reason for the protrusion around the abdomen is it's designed to sit in the seiza position with giant feet.

# 29
>>1806
>Eh most of them aren't worth reading otherwise I'd have uploaded a pack of them here. These two are probably the best I've found on the topic for a general overview.
Fair enough thanks, thanks for filtering the mediocre for us Anon.
>segway mini 
https://www.invidio.us/watch?v=h8GUkc6mzzI
They seem a little more expensive than 'less than $200'. Am I missing something? They do look like a good choice. The robowaifu would still need basic bipedal locomotion to be able to use it effectively (climbing on/off, steering) but nothing particularly good. Good idea.

# 30
A lot of good thinking going on here anons, but much of this discussion is fundamentally flawed. We want our waifu to be:
-Inexpensive
-Easily Reproducible
-Low Power

From these tenets, having any active stabilization beyond the minimum isn't advisable. She should have legs that naturally conform to walking on various terrains. For this reason, having a tail or some other method of passive balance (a dress that hides balancing struts, big feet with a low center of gravity, or have her hold something like a walker in front of her.) these examples will all work for a robowaifu that is inexpensive and low power as she doesn't waste energy on balance.

Roll is a great example of low center of mass with big feet

# 31
>>1873
I don't think balance is a concern for complexity or power consumption. Returning to balance from outside forces is easily accomplished.

Getting a dynamic gait is the big problem. Maybe we could cheat it with a neural network. Really if you're not just making a sex robot you're going to be using neural networks or something close.

A simple solution for movement is to go completely on rails. Not rails literally but railings countertops and other waist-height edges. The waifu would be restricted to the home but would have plenty of well defined static supports to use and only flat surfaces to traverse.
She'd just never cross a wide open room or maybe you could throw a pool table in the middle of it.

Some Anon have entertained the idea of using a tether for power and could equip their home with a literal overhead rail system that would be far more discrete than the other stabilization ideas mentioned.

# 32
>>1882
If you're using rails and tethers, why walk? Also, self balancing is easy for humans but, hard for computers. Neural networks should be used for her personality and communication, it's better to make her walking something that relies on good mechanics rather then complex software. 
We must keep costs and complexity both in hardware and software, to a minimum.

# 33
I'd like to throw another idea in. For very human-like waifus: Wheels are the way to go, but if she should have normal looking feet, then let's build her some kind of rolling boots. Like those for skiing, but less tight and with wheels on the bottom. Batteries included. She would only need to keep balance, but   knowing how the contraption behaves is going to help with that. Also her ankle would be hold by the boot and she wouldn't need to move her arms or legs.

That aside, if they have good sensors in their feet we should be able to solve bipedal walking at some point anyways. Though, it hasn't the highest priority of course.

# 34
>>4331
That's a pretty good idea Anon. Some sort of fore/aft-extendable Heelys might be sufficient to allow her to both skate around and to remain fairly stable.

>That aside, if they have good sensors in their feet we should be able to solve bipedal walking at some point anyways. 
TBH, it will take far more than just good sensors in the feet to solve this but I believe we will in time.

# 35
>>1885
>We must keep costs and complexity both in hardware and software, to a minimum.
Well said, Anon. Even for non-profit, garage-lab, labors-of-love projects, complexity & costs will always be an issue. And for the entrepreneurs among us, they already know keeping them low is a critical factor to success.

# 36
>>4369
I look at at this way: Those who work on more expensive waifus might need simpler prototypes which would be using tech from lower cost bots.  So, this doesn't harm the enthusiasts with less money. Also, the richer guys might pick up some other approaches as a side project. The scope here is from virtual, paper waifus to quite human-like with a lot of sensors.

# 37
>>4375
>The scope here is from virtual, paper waifus to quite human-like with a lot of sensors.
Alright fair enough Anon. My primary ambition with all this is to help literally millions of disenfranchised men build their own robowaifus at home. That means structural drinking straws, 3D-printed parts, cheap paper and plastic shells, cheap electrical motors, batteries, and electronics. The software I'm giving away entirely free at my own expense.

For the guys who want to build the US$120K deluxe robowaifus ready to go onto a SciFy set for a long day of shooting latest series, I say more power to them. 

As you say, there is a wide-scope of interests here at /robowaifu/ and that's a good thing ofc.

# 38
Has anyone printed Poppy and tried it with cheaper motors? Anyone ever looked for other people who tried that?
Some ideas in the comments: https://hackaday.com/2014/03/25/open-source-humanoid-robot-is-awesom-o/
Files, software, tutorials: https://github.com/poppy-project/poppy-humanoid
Their Youtube: https://www.youtube.com/c/PoppyprojectOrgVideos

# 39
>>4436
Yeah, you really hit the nail on the head with ''that'' question Anon. Poppy is a great little project, but those Dynamixel servos are waaaay too expensive for the torques you get. Granted they are good quality, but unless you're wealthy they are simply too expensive in my opinion.

I'm trying to puzzle out a solid approach to having a 'central power unit' in the torso, that uses simple (and cheap) regular DC motors to generate the force, and then distribute that around the body via clever transmission/transduction schemes.

# 40
>>4438
Cool. Did you print out Poppy and you're working on that? I don't know much about this stuff, yet. It seems to be important to measure where everything is, then adapt the body or the next move.
Did you consider using a neuronal network for that?

# 41
>>4440
>Cool. Did you print out Poppy and you're working on that?
No. Once I looked at  the overall cost of the project, I knew it would be fruitless to start printing parts out yet. Again, the power delivery is simply too cost-constrained r/n. Thus why I'm interested in solving it with regular DC motor which are out there in practically every capacity imaginable and far cheaper for each Newton delivered than high-tech servos are. The servos are for accuracy ofc, but I hope that some clever mechanical/software solutions can address that.

>Did you consider using a neuronal network for that?
Sure ofc that's the intent with whatever project we do here I think. As I've said for a while now, the AI for our robowaifus will be much, much harder to solve than the physical shell for her. It's going to take a long time, IMO.

# 42
>>4441
Oh, so you're saying it only makes sense to print it out and try it, when one knows about the size of the replacement dc motors? 

When I mentioned NN here I didn't mean some AI to create a whole waifu mind, but specifically to putting all the states of the motors and joints in, then learning from falling or not falling. Maybe looking not only into the last state, but the ones before which lead to failing or success.

# 43
Does anyone know a website with a search function to compare as many electric motors as possible. Didn't find anything and don't have the nerves for it today. I didn't mean AliExpress. Need to filter them for weight and other values.
It not only for finding motors for >>4436 (Poppy),  but yeah, this would a good example.

# 44
>>4473
Based on what this Skyentific guy on Youtube is using for his arms I endet up to find out that drone or RC motors will probably be what's needed to have the same power and then implement the sensors and controls in another way. I found them with "brushless multirotor motor". More I don't need for now.
When I have my printer I might play around with it, first only thinking about sensors.

>>1602 Link broken, new one: https://www.epfl.ch/labs/biorob/research/humanoid/walkman/

# 45
>>4504
One thing you have to be able to accommodate is extremely high RPMs with these motors, especially the tiny little ones for whoop-type micro drones (~50'000 RPM!). They drain energy rather quickly as you might imagine. But, they can impart a remarkable amount of lbs-ft in short order. Think of them kinda like F1 engines for fairybots heh.

Example:
Apex RC Products 7x20mm Fast 17,900kv / 66,000rpm CW CCW Brushed Motor Set

# 46
>>4505
Yes, some gearbox for reducing will be necessary. But, you really picked a extreme one, and also I meant rather the flat motors. In the video https://youtu.be/WKRLlthr9kY he is using something like on the pic. I have no data for it, since it seems to be out of production, similar looking ones have a RPM of 1200-5000 which would need to be reduced with a factor of about 150 or 200, I guess. Maybe that not the right approach anyways, the second picture is how the Dynamixel looks like (with ~200 reduction included).
I'll look into it on occasion, don't know yet if it will be possible to get a gearbox separately. It's far from urgent anyways.

# 47
>>4510
>But, you really picked a extreme one
Hehe. That's because I bought a few of these for use in robowaifu arms **and to have an 'excuse' to shell out some readies for a whoop drone :^)**. 

These little babys are so lightweight, that you could embed 5 of them into the end of each forearm just below the wrist w/o paying to high a lever-moment kinematic penalty. And, given their ability to wind up basically instantly, their ability to impart a remarkably high amount of (accumulated) force in short order makes them a unique possibility for driving strong, lightweight robowaifu hands. Inexpensive too!

As with all engineering, everything is a tradeoff. These scalding little bitches put out the heat force of a thousand suns. In their drone use, the motor's shells are both open to air and located directly under their equally high-speed rotating blades, which cools them off. We'd have no such luxury with them inside of our robowaifu's wrists, and I still haven't managed to puzzle out a reasonable cooling system for a 5-set yet.

If we can somehow manage that together, then it would be an ideal use-case for these great little motors.

# 48
>>4513
I rather wonder how much torque they have, and how you want to add a gearbox or other reduction? 
However this might fits better into >>406 for actuators in general. We still don't have a thread for hands and forearms or arms in general. I wonder if there has been one in the old forum and will it be imported?

# 49
Reminder: This was possible 6 years ago: https://youtu.be/8uiPHL-xey4 and this is from recently: https://youtu.be/aVJs_x2a9z4
I don't think people should focus on walking, but for example if one doesn't need a human-like form like a doll, without making a lot of noise while walking, then developing something might be much easier. Same goes for something rolling with feet like little tanks: https://www.thingiverse.com/thing:972768 (okay, that's a bit OT in a thread about bipedal walking)
Gymnastics and dancing: https://youtu.be/BhYUjSAwNB4

# 50
>>5223
>okay, that's a bit OT in a thread about bipedal walking
ehh, it's not too bad. we ''do'' have a wheelchair waifus thread >>2983, so it might be there, but this is probably the best place imo.

# 51
This here >>5358 is about walking, James Bruton released his example of a walking bot 2018.

# 52
Walking? Meh! Balance bot wheels for feet. "Rollergirl never takes off her skates".

# 53
>>5634
you must into pix plox

# 54
>>5635
Some things I have been looking at:
#1 Hovershoes. Off the shelf solution for locomotion with many open DIY solutions available.

Balance control becomes an issue for weight above hip line. Might suggest thinking about internal gyroscopic stabilization. Give it its own gravity well it its chest. #2 the Cubli robot uses 2 motorized disks to spin up manipulating balance.

Legs can act as dynamic shocks instead of primary locomotion and balance. Air muscles are viable for this job since the legs need to loosely hold positions instead of supplying quick motion.

What used to be a complex circuit for understanding balance and motor control can be done with an opensource RC flight controller with tweaked PIDs.   

$.02

# 55
>>5645
Thanks. Yes I think both hovershoes or some other form of motorized system could serve well as motive 'footwear' in the interim. And gyro-stabilization is also generally a good idea, if power-hungry. Ultimately, typical human bipedal locomotion is the goal, but in the meantime we'll settle for alternative approaches as needs be.
>PIDs. 
So, for the uninitiate, ''PID'' is some sort of feedback control mechanism then?

# 56
'''P'''roportional
'''I'''ntegral
'''D'''erivative

https://www.mathworks.com/videos/series/understanding-pid-control.html

>part 1
https://www.youtube.com/watch?v=wkfEZmsQqiA

# 57
>>5667
Apologies, that page seems to be account-walled.

Here's a playlist
https://invidious.snopyta.org/playlist?list=PLn8PRpmsu08pQBgjxYFXSsODEF3Jqmm-y

# 58
>>5667
Turns out this guy Brian Douglas has his own independent YT channel.
https://www.youtube.com/channel/UCq0imsn84ShAe9PBOFnoIrg

# 59
>>5671
Apologies, don't mean to bang on about it, but I'm finding more good resources as I dig along. 
https://engineeringmedia.com/resources

# 60
here we have an interesting mechanism https://www.youtube.com/watch?v=uv-Qp8p8Jqg

# 61
>>5930
That is interesting thanks. Is there a paper or anything more available on it Anon?

# 62
>>5931
nah this was random video in my youtube feed. I am wondering if this mechanism will be enough to achieve balance

# 63
>>5933
Here's his channel, seems like he's done a few of these. Amateur designer?

https://www.youtube.com/channel/UC7hw6ztc_mnFh630R0MS5uQ

# 64
>>5936
https://www.youtube.com/watch?v=vlBgMg9WFfA
men god.
Luckily  my family is heavy into machinery and maybe I will be able to build this. only the mechanism not the propulsion

# 65
>>5982
I think if you used 4 of those ''MIT Mini Cheetah'' clone thin disc actuators talked about here 
>>4890
in the hips, then you could probably pull this off. Apparently they run ~$350-400 ea. so plan on about $1500 for the actuators. But if you can get this working it would be both relatively inexpensive and remarkably efficient afaict. 

That anon's exact design would need some modification. The support frame for the hips would have to separate out the two pairs far enough apart to work well for **the onahole cartridge inside** robowaifus.

https://biomimetics.mit.edu/

# 66
>related xpost
>>8704

# 67
Feet development, related to DARA project >>8704

# 68
Are we not making this harder than it needs to be?
For example there are reasons humans have a higher center of mass and it takes more power and effort (and years of practice) to walk: our need to be 5 or 6' tall fluid filled bags for one
Lets take advantage of the clean slate we have with robo waifus. Several stacking advantages could make mobility a non-issue
1. Unfixed center of mass in design: as in "megaman" robots (and the Roll example), center of mass is drawn to the Boots, which themselves could be weighted further. (for "intimate" times the boots could be taken off to reveal more human-like feet, when sitting comfortably or lying down, etc). The rest of the structure doesn't need much, we don't need steel I beams for a skeleton, and the power battery and heavier parts could be set lower on the frame for the purpose of lowering the center of mass.
2. Gyroscopes: as in the Cube example above, gyros provide stability via angular momentum which could even be used to "push" against to maintain balance. Not sure how power consumptive gyros are but I imagine once they are set spinning it doesn't take a whole lot more to maintain the momentum with decent bearings and lubrication.
3. AI assisted learning. Same as how we learned to walk. Trial and error until a way to tackle moving from any point A to B across any slope or terrain is simply reflex. (I'd like to talk more about assigning movements to "reflex" CPUs, this is key since obviously we dont go thinking about every specific movement we need to make, we just think "go down stairs" or "open the door" and our habit and reflex handles the rest, correct?)

Probably more to add to this list, but I see no reason these three advantages would not stack in a way to solve the problem of mobility simply and elegantly.

# 69
>>9053
The idea has been bounced around here of a Roll-like waifu, and certainly keeping track of center-of-gravity is vital for bipedal locomotion.

As to your third point, particularly
> (I'd like to talk more about assigning movements to "reflex" CPUs, this is key since obviously we dont go thinking about every specific movement we need to make, we just think "go down stairs" or "open the door" and our habit and reflex handles the rest, correct?)
This seems to be pretty closely related to the idea of 'Neuromorphic Computing'. (You can find a paper in the ''Library'' thread). I'm inclined to agree with your ideas on this, and it's certainly good biomimetics, nervous system-wise. It entails it's own complexities too ofc, but I imagine the tradeoffs will be well worth it.

Good ideas, thanks! It would be nice if you'd sketch some ideas out for us so we can see clearly what you mean about 'stacking advantages'?

# 70
>>9053
Some of this is food for thought. However, we're going to see different approaches, because people have different priorities. For example: I wouldn't want her legs to feel to light when I lift them, also her not needing to wear boots all the time. For outside, it would be okay though. Also, I don't get the problem until I tried it out myself. Humans do it, so it should be solvable. 
Another thing is, bipedal walking without help or guidance (walls etc) should be towards the end of any priority list, imho. For a domestic girlfriend it isn't very important. She could walk with help, using walls, being driven or drive herself with some device, walk on all fours, dancing while gripping something (e.g. a pole), standing up after grabbing something, then pose or do the dishes while keeping balance,...

# 71
>>9054
>Good ideas, thanks! It would be nice if you'd sketch some ideas out for us so we can see clearly what you mean about 'stacking advantages'?
stacking as in multiplying, not merely Adding, each advantage
Gyroscope + Low Center of Mass is an order more advantageous than Gyroscope alone or Low Center of Mass alone
Because each is a different "vector" and not merely adding to the same vector
Does that clarify things?

# 72
>>9055

noted, but also consider than a powerful enough internal gyro or set of gyros could effectively be an "internal" balance pole of sorts

# 73
>>9057
>Does that clarify things?
Yes, it does thanks.

# 74
Some on topic videos about LOLA:
https://youtu.be/Vzqm94bxjKI
https://youtu.be/pmtKv8VEItY
https://youtu.be/twfDcsQvNBY (Predictive Kinematics, Kinematic Optimization)
https://youtu.be/piQm_oTYXIc
https://github.com/am-lola

# 75
>>9672
Thanks kindly for the links, Anon.

# 76
>>9058
Agreed. IMO, any practical robowaifu walking system today -- given our current rudimentary state of kinematics sensing, planning, and animation -- will necessarily  have some kind of gyroscopic stabilization to succeed. 

Here's an example of what good gyro systems can do >>5645
> the Cubli robot 

https://robohub.org/swiss-robots-cubli-a-cube-that-can-jump-up-balance-and-walk-across-your-desk/

# 77
Finally someone did a study on minimizing energy consumption in gaits.
>We focus on the problem of developing efficient controllers for quadrupedal robots. Animals can actively switch gaits at different speeds to lower their energy consumption.
>In this paper, we devise a hierarchical learning framework, in which distinctive locomotion gaits and natural gait transitions emerge automatically with a simple reward of energy minimization.
>We use reinforcement learning to train a high-level gait policy that specifies the contact schedules of each foot, while the low-level Model Predictive Controller (MPC) optimizes the motor torques so that the robot can walk at a desired velocity using that gait pattern.
>We test our learning framework on a quadruped robot and demonstrate automatic gait transitions, from walking to trotting and to fly-trotting, as the robot increases its speed up to 2.5m/s (5 body lengths/s). We show that the learned hierarchical controller consumes much less energy across a wide range of locomotion speed than baseline controllers.
https://arxiv.org/pdf/2104.04644.pdf

This could be adapted to bipedal walking by creating different expert policies for not only different speeds but also carrying items, moving hands and arms around, wearing a backpack, different size weights on the chest, cat girl tails and so on.

# 78
'''Adversarial Motion Priors for Stylized Physics-Based Character Control'''
>Synthesizing graceful and life-like behaviors for physically simulated characters has been a fundamental challenge in computer animation. Data-driven methods that leverage motion tracking are a prominent class of techniques for producing high fidelity motions for a wide range of behaviors. However, the effectiveness of these tracking-based methods often hinges on carefully designed objective functions, and when applied to large and diverse motion datasets, these methods require significant additional machinery to select the appropriate motion for the character to track in a given scenario.

>In this work, we propose to obviate the need to manually design imitation objectives and mechanisms for motion selection by utilizing a fully automated approach based on adversarial imitation learning. High-level task objectives that the character should perform can be specified by relatively simple reward functions, while the low-level style of the character's behaviors can be specified by a dataset of unstructured motion clips, without any explicit clip selection or sequencing. These motion clips are used to train an adversarial motion prior, which specifies style-rewards for training the character through reinforcement learning (RL). The adversarial RL procedure automatically selects which motion to perform, dynamically interpolating and generalizing from the dataset.

>Our system produces high-quality motions that are comparable to those achieved by state-of-the-art tracking-based techniques, while also being able to easily accommodate large datasets of unstructured motion clips. Composition of disparate skills emerges automatically from the motion prior, without requiring a high-level motion planner or other task-specific annotations of the motion clips. We demonstrate the effectiveness of our framework on a diverse cast of complex simulated characters and a challenging suite of motor control tasks.
https://xbpeng.github.io/projects/AMP/
Basically a way to use adversarial learning to imitate reference motions while seeking to solve a goal.

# 79
>>10160
>Finally someone did a study on minimizing energy consumption in gaits.
Excellent. I consider that topic to be essential for finally achieving the idealized goal of a human-like robowaifu without having a state-sponsored R&D budget available. This will only just be on the very edge of what's even technically feasible at the moment.. If it's achieved at all, it will be due to everything on board the robowaifu being designed to be as efficient and economic as possible. 

Macro physical behaviors like walking will consume significant energy resources. So, not only will efficient gaiting be needed to even work in a natural lifelike way, but it should also make it possible to have our robowaifus walk around for more than 2-3 minutes without immediately needing to do a full 8-hour deep recharge before she can move for another 2-3 minutes, etc., etc. Ever wonder why a humanoid robot that's as well-funded as even Honda's ''ASIMO'' is never shown walking for more than just a few steps in any promotional? Because it's gait is just about as inefficient as it could be, power-consumption wise.

And even significant steps forward in this arena such as Boston Dynamics parkour bot aren't shown going on long walks, in their case it's more a question of not keeping weights to a minimum, even though the gaiting algorithms are much better in that case.

Every.thing. on board must be optimized for robowaifus to succeed and become the reality we all dream of. __Everything__.

# 80
>>10164
I think in real use robowaifus will be more like laptops, plugged in most of the time but able to disconnect and go at any time. My robowaifu would most likely be sitting 95% of the time and my place is so small she could get around while still being connected to power. It'll be an interesting problem navigating small spaces without knocking anything over and not burning excessive amounts of power to avoid stuff.

# 81
>>10181
>It'll be an interesting problem navigating small spaces without knocking anything over
Yes, that definitely is going to require us to have an effective solution for at least two needs Anon:
1. Body-awareness. Distinct from ''Theory of Mind'', this needs to encompass not only a detailed knowledge of her own physical volume & shape, but also a predictive methodology that can ''plan for'' her own kinematic/physics dynamics upcoming, based on her own short-term planned movements.
2. Excellent situational-awareness. She needs to have a detailed map of her environment at all times -- and one that can more or less ''instantly'' adapt to changes in it. Your own motions in the space for example, or your cat's.

On a related point, until and unless we can actually give her a Theory of Mind, she'll have to rely on situational awareness (and possibly some types of crude heuristics) to be able figure out where you are/shortly will be. Thus (just one of the many) need(s) for a near-instantaneous observation capability.

# 82
>>10183
It would make sense to do this in a physics simulation. These were not only meant to train them, but to have one all the time for having awareness. Of course not simulating everything all the time, but when necessary. Also with simplified objects.

# 83
>>10186
Yes, that might be a good approach Anon, and for both of the enumerated needs too.

# 84
DrGuero made a new short video https://youtu.be/wxH3vQOz3JA, where he mentioned that his code is opensource now. His website http://ai2001.ifdef.jp is a bit slow right now, mb to much load after releasing the video. Also it's in Japanese, so some translation software will be necessary.

# 85
>>10343
Thanks Anon! Here's teh code page, I'm DLing now.
http://ai2001.ifdef.jp/uvc/code.html

>update
OK, I've had a quick look at the code. It's old-style 'C with classes' (c.1985 C++) code. It seems to have only one major external dependency, ''Open Dynamics Engine''.
https://ode.org/

It's also W*ndows software. I'll try to sort out getting it to build on a modern C++ compiler on Linux sometime shortly, probably this coming week. Thanks Anon, he may be able to help our Bipedal Locomotion progress along.

# 86
>>10343
>>10344
'''update:'''
OK, I've assembled the 4 code files into a workable project. I haven't set about trying to build it yet b/c dependencies. 
https://files.catbox.moe/wn95n1.7z

However, if anyone would care to work on translating the embedded comments in the codefiles, then that would be a big help to me later on getting the code to run for us. TIA.

# 87
>>10344
>https://ode.org/
'''update'''
By all appearances, the original ODE project has been abandoned. However, it's apparently continued under a new team. The project is now located at:
https://bitbucket.org/odedevs/ode/src/master/
[code]pamac info ode
Name                  : ode
Version               : 0.16.1-1
Description           : High performance library for simulating rigid body dynamics
URL                   : https://bitbucket.org/odedevs/ode/
Licenses              : BSD LGPL
Repository            : community
Installed Size        : 1.7 MB
Packager              : Antonio Rojas <arojas@archlinux.org>
Build Date            : 19/03/20
Install Date          : 10/05/21
Install Reason        : Explicitly installed
Signatures            : Yes[/code]

I've gotten all the demos to build on Linux, so that's a good sign. I'll have to sort out all the dependency issues in the build file, but I'd think this project should be doable on Linux in the end.

**As is commonplace for me, I overestimated my abilities and it will be longer than I planned on.**
I'll post here when I have it all working. Probably be a week or two hopefully.

# 88
>>10409
Thanks, I would have helped already, but I have problems with my browser. Also there are a lot of comments, so I'll need to use sed or something like it.
Great if you want to work on it, but bipedal walking isn't something very pressing. So don't worry about how long it takes.

# 89
>>10410
Thanks Anon, appreciated. I think r/n it's more of a thing to get working early, so that the AI geniuses here will have a readily-extensible tool they can use to work on connecting their AIs into, and coordinating a robowaifu's body movements, etc., via an early simulator environment.

My personal goal for the software is to be able to continue refining it into an actual robowaifu runtime software, and for it to work onboard with small SBCs inside her. 

In my early tests thus far with ODE, it's looking pretty encouraging (~ sub-millisecond collision responses, etc.)

# 90
>related xpost (>>10601, pdf embed)

# 91
>>5409
Here the whole history of James Brutons bipedal walking robots, back to 2004 to around 2018. Robot X, shown in >>5409, was the end result.
https://youtu.be/JWvH5PHKK74

# 92
>>10815
The real challenge isnt locomotion itself, its keeping the robot from falling over while moving. 

Though Boston Dynamics seems to have solved this issue. 

https://www.youtube.com/watch?v=fn3KWM1kuAw

# 93
>>11911
Everyone knows that they've solved it. Doesn't mean that we know how exactly or that we could replicate the same technique. You're missing the point. Bruton showed, what we can do as smaller developers or hobbyists. He didn't even study robotics. Also, he didn't overthink it, like some here tend to do. He just went on by try and error.

# 94
>>11911
>The real challenge isnt locomotion itself, its keeping the robot from falling over while moving. 
There's the rub, isn't it?

>Though Boston Dynamics seems to have solved this issue. 
Now if only they'd just release their code open-source we'd all be good to go! :^)

In the meantime, a '''M'''obile '''I'''nverted '''P'''endulum approach from UCSD has managed some verifiably-functional basic results (and we have direct access to the C code itself). Much more work needs to be done to mold it into human-like bipedal locomotion system suitable for a household robowaifu (>>7824).

https://www.ucsdrobotics.org/mips
https://github.com/beagleboard/librobotcontrol/blob/master/examples/src/rc_balance.c
https://en.wikipedia.org/wiki/Inverted_pendulum

# 95
OK, so anon's OSRM project has gotten me back to thinking about light+strong robowaifu skeletons again. On the topic of bipedal locomotion a thought occurred to me I want to put out here: Since extra-dense, high-mass items like batteries are proportionally a higher percent of the total mass for a strawgirl or osrm robowaifu, wouldn't it stand to reason that mass could be articulated into a useful counterweight system within the lower torso/pelvis volume to swing back and forth as a type of counter-balance for the overall system during natural-gait walking/running/etc. ?

The fact the mass is a higher percentage means it should be a particularly effective approach for either of these two types of robowaifus, but I imagine that it would be helpful even in a heavier robowaifu too. The basic idea is that you fix the batteries into an encasement attached to a short, inverted pendulum (inverted = batteries higher than pivot point). As the robowaifu's hips swing in one direction during her gait, the counterbalance pivots in the opposite direction.

Animals already do this kind of thing instinctively during locomotion, and humans do as well. Our neuronal-musculo-skeletal complex all get wired up for complex kinematic motions such as these as we grow. By the time we're 5 or 6 yo, normally we pretty much have the 'force/counter-force' coordination down pat.

Some of you may be aware that basically all skyscrapers constructed in any modern city have very massive 'floating' counterweights right at the top of the building that move this way and that depending on wind forces (and even earthquakes). A counterforce mass in our robowaifu's belly can serve a similar function and keep her center of gravity centered even when she's walking around.

That is all.

# 96
>>12562
>Another Anon that actually understands physics and the importance of mass. 
Based and mass-shift pilled 
Check out Dr.Guero's work in this field. (Picrel) http://ai2001.ifdef.jp/mr1/mr1.html
Femisapien also used this property. You can see her mass shifting point, it's the rotary encoder on her crotch. She shifts the mass of her body and electronics onto one leg, then moves the other leg forward as her weighted leg moves back. All you need is a parallel mechanism to keep her feet level and an added steering servo to twist her thighs for turning. Please do post any work you make even failures, I have a thread filled with my failures.

# 97
>>12582
Will do anon, thanks for link.

# 98
how soon we will have a bipedal robot that can imitate humans

# 99
>>13439
when the geniuses stop focusing on just the legs and finally figure out you cant have bipedal motion without fucking ears and start using gyroscopes

# 100
>>13447
How would you implement them?

# 101
>>13451
same way the human body does
a feedback loop making continuous micro adjustments
autopilots already do this with stabilizers, but thats easy for something with a plane perpendicular to gravity, parallel planes are in a league of their so dont bother until synthetic musclefibers become a thing

