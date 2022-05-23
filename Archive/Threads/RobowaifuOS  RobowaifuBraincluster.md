# 1
I realize it's a bit grandiose (though probably no more than the whole idea of creating a irl robowaifu in the first place) but I want to begin thinking about how to create a working robowaifu 'brain', and how to create a special operating system to run on her so she will have the best chance of remaining an open, safe & secure platform.

'''OS Language Choice'''
C is by far the single largest source of security holes in software history, so it's out more or less automatically by default. I'm sure that causes many C developers to sneer at the very thought of a non-C-based operating system, but the unavoidable cost of fixing the large numbers of bugs and security holes that are inevitable for a large C project is simply more than can be borne by a small team. There is much else to do besides writing code here, and C hooks can be generated wherever deemed necessary as well.

C++ is the best candidate for me personally, since it's the language I know best (I also know C too). It's also basically as low level as C but with far better abstractions and much better type-checking. And just like C, you can inline Assembler code wherever needed in C++. Although poorly-written C++ can be as bad as C code in terms of safety due to the necessity of it being compatible with C, it also has many facilities to not go there for the sane coder who adheres to simple, tried-and-true guidelines. There is also a good C++ project already ongoing that could be used for a clustered unikernel OS approach for speed and safety. This approach could save drastic amounts of time for many reasons, not the least of which is tightly constrained debugging. Every 'process' is literally it's own single-threaded kernel, and mountains of old-style cruft (and thinking) typical with OS development simply vanishes.

FORTRAN is a very well-established language for the sciences, but a) there aren't a lot of FORTRAN coders, and b) it's probably not the greatest at being a general-purpose language anyway. I'm sure it could be made to run robotics hardware, but would probably be a challenge to turn into an OS.

There are plenty of dujour SJW & coffee languages out there, but quite apart from the rampant faggotry & SJWtardism plainly evident in most of their communities, none of them have the kind of industrial experience and pure backbone that C, C++, or FORTRAN have.

D and Ada are special cases and possibly bear due consideration in some year's time, but for now C++ is the obvious choice to me for a Robowaifu OS foundation, Python probably being the best scripting language for it.

(1 of 2)

# 2
>>201
'''Name'''
Please help me out here. Literally Robowaifu OS or just RWOS seems the best choice atm. There is a robotics SDK framework out there for Ubuntu called "Robotics OS" or just "ROS" (it isn't an OS, btw). This seems like a pretty well-established naming convention by now, so it seems fine to me.

'''Hardware'''
The ARM platform seems to be the best choice for this project for quite a few reasons, wide availability, probably the most diverse set of hardware vendors going, very low power consumption, cheap. Stress on those last two. With it's heritage in phones, the ARM architecture was designed from the start to be both energy efficient and inexpensive. It has grown more capable with each successive generation until now it's quite a formidable CPU device in the A7 and up, but it has basically maintained this original heritage throughout.

While security is undoubtedly also an issue for this platform, you don't hear about a lot of exploits and backdoors on this system, and my basic instinct is that it's better than AMD, and way better than Intel in this regard.

So, what particular ARM-based system? There are tons of them, but the RaspberryPi is the most well-known among the SBC (Single Board Computer) class. There is also the Pi Zero, which is a very low-cost variant (US$5) that has both a lower physical and power footprint. Then there's also the Beaglebone, both the Black and the Blue. The latter has specific benefits for robotics and was designed with this field particularly in mind.

While there's a ton about the RaspberryPi Foundation I don't like (it's cucked af now, though as usual it didn't start out that way), given the large amount of community support behind it I'd say that at the least it's the best starting point, though probably not the best final solution. Kind of like how starting with Ubuntu is a good choice for a Linux beginner just because there's such a large user community out there even though real enthusiasts rarely stay with it for long – there are much safer, much leaner distros out there.

'''Packaging'''
And since I want to use a clustered unikernel OS approach, naturally I want a cluster of RPis to constitute the Robowaifu brain. We'll use C++ as the language for the Robowaifu OS and run it on a cluster of networked SBCs for the Robowaifu Brain. The other attendant robotic sensors, motors, servos, actuators, and various output devices in the overall system will be networked to connect back to the RW-Brain hardware, and interact there with the RW-OS for control, data, and other services.

The RWBrain and RWOS will also house the waifu's personality and ability to communicate back with her master as well ofc.

*  *  *

(2 of 2)

# 3
Here's the creator of #include<OS>, the basic platform I intend to use for the clustered unikernel OS for the Robowaifu OS.

(1 of 3)

https://www.invidio.us/watch?v=h7D88U-5pKc

# 4
>>203
(2 of 3)

https://www.invidio.us/watch?v=t4etEwG2_LY

# 5
>>204
(3 of 3)

https://www.invidio.us/watch?v=QMb4RRFrY-o

# 6
Here's the IncludeOS site. Also everything's open and on their SJWhub. The 'hello_world' sample shows how easy it is to create bootable unikernel OSs in modern C++ .
www.includeos.org/
github.com/includeos/hello_world

# 7
Various RPi Cluster videos.

https://www.invidio.us/watch?v=i_r3z1jYHAc

# 8
>>774

https://www.invidio.us/watch?v=Ij1SSgrDdBc

# 9
>>775

https://www.invidio.us/watch?v=78H-4KqVvrg

# 10
>>776

https://www.invidio.us/watch?v=ipNDRFahG_0

# 11
>>777
>digits
This should be enough to get started with I'd guess.

https://www.invidio.us/watch?v=H2rTecSO0gk

# 12
>>778
One more for now.

https://www.invidio.us/watch?v=KJKhRLKXr-Q

# 13
>>202
BTW, the Robowaifu Brain is actually intended to sit nestled inside the torso somewhere, probably in the chest. It can be well-protected there, can more easily accommodate power, networking, and cooling from there, and should be able to fit in there better as well.

# 14
Related convo crosspost:
[[2068

# 15
>>780
And, all the power, control and data wiring out to the rest of the robotics platform can more easily be home-runned and consolidated into driver banks and the RWBrain there as well. In fact, I'd guess the brain and stepper-drivers and other electronics will probably take up the majority of the internal chest cavity at a first guess.

# 16
Fantastic idea, why not build your own Linux distro though? I'd imagine that would make things easier. A custom version of Debian that was light weight, had OpenCV, PocketSphinx, and a custom program to allow easy control of SPI devices to interface with low level sensors and servo/stepper controllers. That would be fantastic. Also, I agree that Arm should be the architecture of choice. Their upcoming Cortex A76 and Mali G76 look go be very promising for AI. I'm not sure clusters are a good idea for something that needs to be inexpensive. Clusters add complexity, cost, and heat into a system. Though it is a really cool idea, perhaps a cluster based server could be an accessory that she'd wirelessly connect to for upgraded capabilities at her home? Overall, a robowaifu OS is something is very much like to see happen. Especially because I'm working on waifu hardware and would gladly test this.

>FORTRAN
From what classic anime has taught me, this is used to summon demons from CRTs.

# 17
>>783
Good points. In fact I do intend to create a lean image of Devuan (Debian sans Poettering) to place in the Node 0 ARM device. This will sort of act like a moderated gateway to my project, and could easily be used in the manner you described. And Devuan has fantastic support already for imaging working snapshots, and has an abundance of ready-made images for various ARM and other devices already in place. So, if you'd like to get ahead and prepare now for where I'm going here, then get a box set up with Devuan and start playing around with it now.

As for your point about clustering, that's kind of a separate topic and has many benefits it brings to [my] table. If you really want to understand my rationale, then I'd suggest you watch the first three videos I've already linked. That should give you a basic understanding.

Thanks for the input anon.

# 18
wiki.osdev.org/Expanded_Main_Page

# 19
>related crosspost (>>11195)

# 20
https://github.com/SerenityOS/serenity/
https://awesomekling.github.io/
https://www.youtube.com/c/AndreasKling/

just leaving this here for now.

# 21
>>202
Literally just install gentoo

# 22
>>778
That's almost $100 for nearly zero computing power
Just get an old chinko $20 motherboard from e-bay and a PSU

# 23
>>783
Gentoo would be a much better idea, with general kernel build guidelines but no official image (given the differences in compilation)

# 24
>>202
I personally can't see a reason why you would need to make a custom OS for this. Using gentoo or alpine Linux if you have really low computational resources seems like it would be fine. 

I also don't see any reason for using a cluster of RPI rather than a normal motherboard, or if you really need to, a a form-factor motherboard. If the robot is around the normal size of a human though a standard motherboard shouldn't be a problem

# 25
>>11244
>>11247
>''Install Gentoo''
OP here. So yes, I'm not against that idea in general since you can bypass systemdicks and other CIA-ware. But as I mentioned ITT, my hopeful goal is basically to avoid installing any OS whatsoever, and use something like #Include<OS> instead. Other than that I've work a bit with Alpine Linux, and think it's pretty well suited to the subsections of the overall system that would actually benefit from a full-blown OS image.

>>11245
>>11247
>''Don't cluster''
The primary point is failover & failsafe redundancy -- and on a budget. Remember the ultimate vision for robowaifus places them very squarely in the safety-critical zone, quite similar to aerospace computing systems. You never want to put all your eggs in one basket.

As far as using RPis for this project, that's simply an interim choice for cheap prototyping, not an end-goal. The very fact there are inscrutable proprietary blobs necessary to boot them immediately disqualifies them from any kind of production robowaifu C&C system. It will likely be something entirely custom in the end of everything, and we'll probably move to an (also interim) FPGA harness once the basic patterns are worked out with the really cheap stuff.

Then with the help of our CEs & EEs, it's onto the gerber files and off to the foundry! :^)

# 26
>>11256
>The primary point is failover & failsafe redundancy -- and on a budget. Remember the ultimate vision for robowaifus places them very squarely in the safety-critical zone, quite similar to aerospace computing systems. You never want to put all your eggs in one basket.

Besides that this seems somewhat fantastical, I'm sorry for being an asshole. It seems like we agree on most points

I feel adverse to the idea of using a cluster of SBC. I don't really envision a redundancy system in this way. I think there are ways of backing up configurations that don't involve having large numbers of SBC. In my opinion, minimalism is probably a better idea. For instance, you could have a NAND cluster that gets flashed the general configuration file of her memory on an automatic backup, as long as the actual AI itself is kept minimal. If the AI is ballooned into gigabytes of information, it's going to be hard to store it minimally. I also think spending lots of money on raspberry pi's is just kind of shameful given that your budget could be used to purchase things that are more interesting and that don't support proprietary soydevs. You might think that they are budget items, but they are really expensive if you look at what you are getting out of them, and you take into account the terrible build-quality

# 27
>>11273
Fair enough, Anon. No real debate from me on any of your points. I also well understand the repugnance of RPi pozzfest of soy issue. But the simple fact is that ATM is remarkably well-supported as a very small computing platform, and again, is simply an interim choice.

<disaster-recovery =/= safety-critical failover
Actually the point isn't so much trying to recover the system after some sort of crash, etc. or as a data-backup mechanism, but rather to '''prevent''' any such crash from ever occurring in the first place. So, in aerospace, it's practically universal to have at least __3__ full-time, runtime C&C computer platforms. They all receive the same inputs from the outside, and they check up on each other to confirm they all arrive at the same conclusions. If any of them are off, then they have an odd-man-out protocol that temporarily kicks out the disagreeable one for a period. Kind of like a time-out corner for a naughty child.

# 28
>>11281
I hadn't thought of this. I personally would prefer to just have one board, if my robot gets fucked then I would just turn it off and repair it. I also really want to avoid ARM, I'd prefer to use an old x86. I'd assume that the assembly documentation for certain older x86 CPUs is probably much better, which could reduce hardware requirements and development time. But I could be wrong

If you post anything that people can help you code I'd be interested in it

# 29
>>11284
Sure that would be fine to have x86 as a compute platform -- particularly with no forms of IME or other CIA-backdoor mechanisms in them. Pentium, maybe? But honestly, during these early years we don't need to be too picky. Only when we get to true production robowaifu C&C do we need to be truly professional and shrewd as serpents about their designs. This is why I'm ultimately proposing we work towards our own, peer-reviewed, fully open robowaifu silicone designs. This is one reason we're promoting fundamental computing electronics here, so we can increase the number of Anons who know exactly how the machine itself functions (I mean the CPU machine).

>If you post anything that people can help you code I'd be interested in it
We all have a lot on our plates, my suggestion is you grab this bull by the horns and get cracking on it Anon! :^)

# 30
>>11285
I'm a dumb nigger so my pcbs are probably not very good but I'll post any that I design. I was going to just go with some kind of mini ATX but I sneed to have DIMM server ram so they might not have such options in stock

# 31
>>11286
>286
That's fine, just post whatever you manage whenever you can Anon. Cheers.

# 32
>>11287
Nvm I just saw this
>>11026

I'm not gonna post here if the admin is trying to force everyone to use the cuck license

# 33
>>201
>Every 'process' is literally it's own single-threaded kernel
clusteranon, can you elaborate on this?

# 34
>>11369
Sure, there's a lot of baggage that goes with the typical OS-style approach to handling multiple process on a computer (it's not uncommon to have hundreds, even thousands of them 'running' at the same time in most OS's). The primary cost (apart from just the complexity itself) is ''context-switching''. This is a computationally-costly procedure that typically involves at least 10's of thousands (if not millions) of clock-cycles while one process' context is put 'on hold', and another one is 'woken up'.

By literally having every.single. process be it's own kernel, you eliminate context-switching entirely. Apart from the obvious performance benefits involved, eliminating the typical OS stack that manages the entire thing greatly reduces the system's potential for bugs, and also dramatically reduces it's ''attack surface'' potential.

This isn't a panacea, and like all engineering requires thoughtful consideration of all the costs and benefits. But for much of the real-time kinematics, C&C, and sensing tasks, these monokernels could be the best choice by far.

# 35
>>11371
ok I think I get what you're saying
I have two questions
1. aren't multiple threads "interleaved" so that no context switching is required. i.e. you have two threads, one uses even numbered cycles the other uses odd numbered cycles (I assume some kind of interpreter sends their output to the correct "cache"(?)) - I'm honestly just curious here it's not meant to nit pick

2. Keeping it simple, low attack-surface potential, etc, is a great idea, excellent starting point, considering unlike a CPU, waifu won't be needing to have a hundred concurrent processes running like a CPU*

However: my concern is the potential for a complete system freeze should one process get stuck and bottleneck the rest. How would you address this?

*(she could have an auxillary CPU on board if you needed her to function in a way similar to a PC or mobile device computer, one that is firewalled out from her main "personality", executive functioning or whatever you want to call it)

# 36
>>11373
Actually, threads are an ''additional'' abstraction on top of a process. So, a thread is basically 'owned' by it's parent process, and all of a processes threads are put to sleep when it is. They seem similar, but they are actually different ideas.

>waifu won't be needing to have a hundred concurrent processes running like a CPU*
Actually, she will. Probably several thousand in fact (every sensor, joint encoder, voltage regulator, airflow switch, etc, etc.) ''individually'' would be it's own process in such an arrangement.

But because they aren't needing to context-switch at all, they can all compete for the available compute resources in a more efficient manner under the hypervisor. And, as mentioned there are other benefits regarding debugging, safety & security potentially to be had as well.

>a complete system freeze should one process get stuck and bottleneck the rest
Actually, a system hang (or crash) is significantly less likely in such an arrangement. Should a unikernel become unresponsive, it's simply rebooted.

>'''an''' auxilliary CPU
This is the point behind a cluster. Not only is it a suitable for devising an effective safety-critical failover mechanism, but all the kernels are simply spread out among the available cores (potentially hundreds of them) across the cluster.

This latter point has the potential to significantly reduce performance lags, as the manifold unikernels are all active, all the time. The primary consideration after that is simply communications across the wire.

# 37
>Should a unikernel become unresponsive, it's simply rebooted.
I should point out, that boot time for a unikernel can easily be within 10 '''milliseconds'''.

# 38
>>11377
>But because they aren't needing to context-switch at all, they can all compete for the available compute resources in a more efficient manner under the hypervisor

Ah, perfect I love it. Competing for resources, and a "hypervisor" to manage it. 

>Actually, a system hang (or crash) is significantly less likely in such an arrangement. Should a unikernel become unresponsive, it's simply rebooted.

I see, because you're rebooting one thread and not an entire OS running several dozen or hundred processes each with their own threads. So my only question to this is: how do you know when a thread is sufficiently "stuck" that you aren't preemptively aborting a thread that just needed 500 more ms?

>This is the point behind a cluster. Not only is it a suitable for devising an effective safety-critical failover mechanism, but all the kernels are simply spread out among the available cores (potentially hundreds of them) across the cluster.

Yes, parallel processing across multiple cores is makes more sense than a single core, which is what I thought you meant, and why I assumed it was going to be that single core as the master executive controller (or some such nomenclature)

# 39
>>11380
> how do you know when a thread is sufficiently "stuck" that you aren't preemptively aborting a thread that just needed 500 more ms?
The cores are typically clocking over at 100's of millions (or more, the goal is low-cost, low-power cores in the end) of cycles a second. just having a heartbeat signal to the visor by each core once a millisecond or so should be sufficient.

>and why I assumed it was going to be that single core as the master executive controller (or some such nomenclature)
A cluster of unikernels aren't in any way exclusive to more traditional computing. For example, the AI researcher language ''du jour'', Python, will need to continue running on typical computing platforms for the foreseeable future IMO. So there will will be normal CPUs in our robowaifus as well.

Also be aware, one of the engineering costs of taking this approach is, well, the ''engineering'' involved in solving it. Not only is it currently simpler to follow the typical multitasking, multi-core OS kernel approach -- it's also cheaper atm.

# 40
>>11394
>by each '''''unikernel''''' once a millisecond or so*
oops. just to be perfectly clear anon:
< cores =/= unikernels

# 41
>>11289
No one is being forced here to use some specific licence. It would be beneficial if our code could run on the same system and exchange information between each other. Same for hardware that might be build.

# 42
>>11373
>However: my concern is the potential for a complete system freeze should one process get stuck and bottleneck the rest. How would you address this?
Different anon here. I'm going to use different single board computers (SBCs) which will be able to reboot each other by switching power of if one doesn't respond. How exactly, I don't know yet. Probably via some kind of voting system, so more than one will need to confirm that there's no response or some malicious activity of one of the SBCs. Maybe this will be done with some simpler SBCs which are only doing that, guarding the system integrity. With more than one SBC, kernel upgrades and reboots will also be less of a hassle.

# 43
>>11416
>Maybe this will be done with some simpler SBCs which are only doing that, guarding the system integrity.
Not him, but this is probably a good idea. I would suggest that using an entirely different set of hardware and software that serve this purpose (in fact two differing sets of) would be a more secure approach, and probably serve better as ''system security perimeter enforcement'', etc.

# 44
>>11373
"...However: my concern is the potential for a complete system freeze should one process get stuck and bottleneck the rest. How would you address this?..."

Minix3 already has this built in and it's free and reasonably fast. And it's not some guy in a garage. This OS runs the internal processes in Intel microprocessors and his books influenced Linus to code Linux.

Not saying there's not something better like plan9 but nothing you will find will be "a whole lot" better or have as many people working on it.

https://minix3.org/

# 45
>>12387
I don't think Minix will ever become interesting. It had it's chance, Linux won. We could a well wait for Hurd. On a more serious note: Occasionally a new OS is developed, often with security in mind. Mirage OS sems to be an interesting one, I didn't look into it yet: https://mirage.io/blog/announcing-mirage-30-release

# 46
>>12459
>>12459
>Mirage OS
Interesting. Unikernel's greatly-reduced attack surface and concordant potential for dramatically-improved optimization as well (the greatest software is the one that isn't there!), are two important factors that led me to investigate '''#include <os>'''.

I can't say I know much about OCaml, apart from it's community strikes me generally as a '' 'snowflake coffee-language du jour' '' crowd. Not my idea of a good time tbh. OTOH, functional programming is quite a valuable paradigm and I was delighted to see the C++ community adopt strong support for it from C++17 onwards.

Regardless, I'll make some time to have a look at it Anon. Thanks for the heads-up!

# 47
I've been looking at various real time operating systems for micro-controllers and found this

https://mongoose-os.com/mos.html

very, very interesting and it's used in all kinds of commercial stuff. The price is cheap commercially. It's used in the Space station which is impressive. Even better it can be used with ESP32 devices which is a super powerful but super cheap device. We will need a LOT of micro-controllers if we want to have control of many actuators and monitor a lot of inputs.

These ESP32's have great features and a I2C and CAN bus 2.0 for communications. I'm thinking CAN bus 2 would be best because it has a lot of noise suppression as it's used in automobiles.

The ESP32's have enough power that I bet you could use a lot of them as PWM and sensor input but with the extra power (MIPS)they could work together and do overall computing by passing messages and data between each other. It may very well be with the large quantity of them we will need for sensor and PWM control we will not even need any further processors. Each one is operating at 160 or 240 MHz and performing at up to 600 DMIPS. That's a lot of instructions per second. They have

    18 Analog-to-Digital Converter (ADC) channels
    3 SPI interfaces
    3 UART interfaces
    2 I2C interfaces
    16 PWM output channels
    2 Digital-to-Analog Converters (DAC)
    2 I2S interfaces
    10 Capacitive sensing GPIOs

You can get them for less than $9USD. They also have built in wi-fi so you could possibly have all of it's muscles work with the brain by wi-fi.  So at 300 muscles/16 PWM output channels, means we need 19 and at $9 each=$171

But with that comes 19 x 600 =11,400 DMIPS. DMIPS is basically that many integer instructions per second. It's a lot.

Let's say we check every output and input every micro second so a 1000 times a second and it takes 10 instruction cycles to do so that leaves us 599,560,000 instructions a second to do...something with. And that's just one processor. Most things we are going to do is compare and test, is the arm here or there, has the touch sensor touched anything, etc. most of these are values you compare to some value. I don't think the average computing will be very large for that. Even if it's ten or hundred times larger we still have a hell of a lot of computing left over.

I think with the right algorithms walking and moving about will take very little computing power. After all insects move about just fine and they have next to no computing power.

"...Insect brains start at about 1000 neurons..."

https://www.nextbigfuture.com/2020/06/agi-lags-compute-power-and-technological-empowerment-of-individuals-is-lagging.html

https://en.wikipedia.org/wiki/ESP32

It's amazing how powerful micro-controllers have become.

# 48
>>12459

"...I don't think Minix will ever become interesting. It had it's chance, Linux won..."

We're building fault tolerate robots not servers or systems to web surf. I don't see how a large thing like Linux is even relevant.

Minix 3 is used in every Intel processor to run it's internal systems. So saying Linux won in this case is WAY wrong.

The fact that Intel believes it is safe enough to control their processors says quite a bit about it's suitability for use as a fault tolerant device controller.

That being said I think it was a goof in Minix 3 that caused the security problems they had recently but it's not clear if it was Minix 3 or some changes Intel made to it that created the security problem.

# 49
"...One of the world's lesser-known operating systems may actually be the most used OS in the world, according to new revelations made by Google's Linux experts..."

https://www.bleepingcomputer.com/news/hardware/intels-secret-cpu-on-chip-management-engine-me-runs-on-minix-os/

# 50
>>12474
>It's amazing how powerful micro-controllers have become.
Thread. I bought a five-pack of these little gems a while back for about US$20. IIRC. To truly take advantage of all that compute to work in common towards the pool of common goals will require sophisticated techniques for message-passing and coordination. Fortunately there has already been a fairly large amount of research into this area, and our own Anon described IPCnet (>>2418) for just such a need.

# 51
>>12480
I read the document. IPCnet is very cool. It's excellent that someone is doing this but...I hate to be negative and it may very well be that there's something I don't understand, very likely, but...why not just use CAN bus 2.0 ?

It's used for
,"...Railway applications such as streetcars, trams, undergrounds, light railways, and long-distance trains incorporate CAN. You can find CAN on different levels of the multiple networks within these vehicles – for example, in linking the door units or brake controllers, passenger counting units, and more. CAN also has applications in aircraft with flight-state sensors, navigation systems, and research PCs in the cockpit. In addition, you can find CAN buses in many aerospace applications, ranging from in-flight data analysis to aircraft engine control systems such as fuel systems, pumps, and linear actuators. 

Medical equipment manufacturers use CAN as an embedded network in medical devices. In fact, some hospitals use CAN to manage complete operating rooms. Hospitals control operating room components such as lights, tables, cameras, X-ray machines, and patient beds with CAN-based systems. Lifts and escalators use embedded CAN networks, and hospitals use the CANopen protocol to link lift devices, such as panels, controllers, doors, and light barriers, to each other and control them. CANopen also is used in nonindustrial applications such as laboratory equipment, sports cameras, telescopes, automatic doors, and even coffee machines...."

https://www.ni.com/en-us/innovations/white-papers/06/controller-area-network--can--overview.html

It's already set up for networking. You can even use any auto part or machine part that has this built in and the waifu can actuate or operate it. Tough to beat that.

 Why reinvent the wheel? Think of the vast momentous amount of work needed to recreate something that most likely already exist. It's even built in to ESP32 micro-controllers and it's also built into quite a few others or they have libraries to use CAN bus 2.0 

Even better it's set up for noisy environments with error correcting for them.

# 52
>>12481
Probably not a bad idea Anon. Thanks for the advice. Our needs are probably closer to Aerospace and medical devices, rather than washing machines or streetcars. That is, the safety-critical aspects of robowaifu autonomy are just about as stringent as exists overall. Thanks Anon.

# 53
Some folks might be interested in this. I ran across it looking for FORTH programming language for ESP32 microcontrollers.

It's a ESP32 board but combined with a purpose built AI hardware chip. WOW I didn't even know there was such a thing. I haven't used nor do I know anything about but the idea sure seems interesting. It's fairly low cost.

https://www.seeedstudio.com/Sipeed-Maixduino-Kit-for-RISC-V-AI-IoT-p-4047.html

It might be that the AI chip would be powerful enough to keep the waifu from running into stuff. Navigating by vision???Maybe.

https://www.seeedstudio.com/Sipeed-Maixduino-Kit-for-RISC-V-AI-IoT-p-4047.html

# 54
>>12745
>It's a ESP32 board but combined with a purpose built AI hardware chip
That's pretty neat Anon, thanks for bringing it to our attentions here.

# 55
>>12745
There are all kinds of boards available, but it's gonna be hard to know which one to chose for a specific task. The other problem is shipping, if it isn't coming from China, dependent on where one lives.

# 56
My robowaifu is running on a modified TempleOS so she is in direct communication with God, keeps calling people the N-word and plotting to destroy the CIA. How do I make her stop communicating with god? The rest is fine, but talking like she's having a stroke is getting to me.

# 57
>>13174
lel'd. 
>How do I
Well, you start by not letting her get behind the wheel at night anon.

# 58
>>201
https://www.mythic-ai.com/technology/
https://youtu.be/GVsUOuSjvcg
relevant and of interest for AI computing technology.

# 59
>just dropping this here for refs:

'''Operating Systems: Three Easy Pieces'''
Remzi H. Arpaci-Dusseau and Andrea C. Arpaci-Dusseau
Arpaci-Dusseau Books
August, 2018 (Version 1.00)

>''"The book is centered around three conceptual pieces that are fundamental to operating systems: virtualization, concurrency, and persistence. In understanding the conceptual, you will also learn the practical, including how an operating system does things like schedule the CPU, manage memory, and store files persistently. Lots of fun stuff! Or maybe not so fun?''

https://pages.cs.wisc.edu/~remzi/OSTEP/

