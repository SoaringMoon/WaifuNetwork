# 1
Hi Anons, making a thread as suggested in >>10947

I've been thinking about this for a long while, and wanted to throw in a draft and see if anyone has comments/criticisms/additions. 

I present to you the draft of the Robowaifu Power and Control System (RPCS). This draft is by no means complete or definite, but it is a starting point. Let's call it version 0.1a. The version follows major.minor and a letter for bug-fixes. Minor is for feature addition/reduction, major for when we eventually get there XD. From a legal stand point, this is under CC0 or public domain (unless Chobitsu has specific licensing for the content on /robowaifu/). I intend for the draft to develop further and stay open for use by anyone.

==Summary==
A full-size robowaifu system needs several things:
- Power distribution. Main system bus coming from a Li-ON battery (or other technology). One backup 5V emergency power supply used by slow communications to check appendage integrity, sensors etc.
- Main processor. In this post I won't be delving into it in great detail, and mostly treating it as a black box.
- Low/medium throughput communication for simple sensor, debug, or status information. Must be robust and must work before any high-level software is working (including the network stack).
- High throughput communication for large data-logging, visual processing etc.
- "Spine" or communication interconnect. Multiplexes many connections from many sub-systems to the main processor. Includes power distribution connection (allowing individual control to sub-systems).
- Sub-systems to actually do the fun stuff! (Arms, legs, nekomimi ears, etc.)

==Terminology==
'''Brain''' refers to the main processor (and all of its sub-systems treated as a single unit).
'''Body''' refers to all the sub-systems and interconnect as a whole.
'''Spine''' refers to sub-system in charge of collating data to the brain.
'''Sub-system''' refers to the individual blocks making up the body (technically includes the brain and spine).

==Power Distribution==
For low power electronics you'll need 3.3V and lower, 5V for bulkier sensors, 12V for small motors, 24V or 48V for heavy duty movement (or heating etc.). As DC-DC switch-mode power supplies have been improving in efficiency, it may be worthwhile to only have one bus voltage (such as 12V or 24V), while generating the others locally. This would reduce the number of cables and overall complexity. You may have noticed this happening to PC ATX supplies, as older ones used to have +/-3.3V and +/-5V (with decent current ratings), whereas now most of the current rating is on the 12V rail and negative supplies are generated locally.

Switch-mode power supplies are noisy (have ripple current and voltage) and also require careful design to ensure stability (look into control theory, it is fun >:) ), so precision sensors, ADCs/DACs etc. need to have additional filtering and potentially local voltage/current regulators and references. However I don't consider this a major issue as noise will be picked up regardless along the wires coming from the power system to anywhere else. Shielding will also be required to reduce electromagnetic interference (as such long wires will essentially become radio antennas).

Depending on battery technology, we may also get close to the desired bus voltage anyway and may have something akin to VBUS (which has a range of 4.5-5.5V) where the overall bus voltage will rise and fall depending on current battery level. For example:
3-series Li-ON cell, output voltage range of 11.1-12.6V 
4-series Li-ON cell, output voltage range of 14.8-16.8V
Perhaps the sub-systems could also individually monitor the bus voltage and adjust their operating profile based on available capacity?
For example, reduce amount of unnecessary movement (sway, general social cues etc.) when battery reaches low level.

An emergency power rail would aid in situations where the main supply is down or intermittent. I propose using 5V, as it is enough to both microelectronics, as well as small sensors and motors. It must be isolated from the main bus and hence generated separately by an additional battery (but could be charged from the same charging socket).

The power supply block can be tested (voltage/current measurements) and restarted (main supply restarted by emergency supply, emergency supply restarted by main supply). Granular power control to individual sub-systems is controlled from the spine.

Perhaps it is worthwhile to have a redundant secondary bus? Exactly the same as primary (automatically switched to in the spine), but isolated and located elsewhere. Diagram shows this as an optional (dashed rectangle).

Can be communicated with using the low throughput connection. Is high throughput connection necessary?

==[PART 1]==

# 2
>>11018
==[PART 2]==

==Low/Medium Throughput Communication==
There are many different protocols used by sensors, actuators, controllers. Main ones I can think about are I2C, SPI, USART (UART). However in a system of such scale as a human-sized robowaifu, distances can be on the order of a few metres. There will also be plenty of opportunities to pick up noise and interference as the wires run along actuators, power systems, and processors. This is why I'd say implementing a CAN bus is a better idea.

Quoting from a TI application note (link below, and pdf attached): "specification calls for high immunity to electrical interference and the ability to self-diagnose and repair data errors." Such a protocol will be useful for maintaining state throughout the entire body. All sub-systems can be connected to the same bus (thus every message will be visible to everyone else), or point-to-point typologies can be implemented.

The CAN bus transaction decoding is generally proprietary in automotive (beyond the original 8 byte payload), but there are some open standards we could use. For example J1939, which is used for heavy duty vehicles (sounds about right for a robowaifu XD). There are also OBD2, CANopen, and CAN FD available to name a few. 

A scenario I imagine is using this bus during boot up to identify available sub-systems (like a motherboard BIOS detects hardware). The spine could collate info from every device and send the resulting report to the brain, where further decisions can be made (which profile/drivers to load etc.). The brain might also monitor the message to confirm the spine is working as intended.
During operation sub-systems could also broadcast actuator/sensor data, thus allowing sub-systems to talk to one another and compensate for a given task on the fly. The brain or spine could passively listen to the state of the sub-systems for data-logging or software control.

As I have not studied the CAN bus too much (or used it yet), there's more I need to learn about before I can make concrete decisions on it. There are also several different standards (latest being ISO 11898-2) I've linked a few different articles and documents for CAN bus.

Links to CAN info:
https://www.ti.com/lit/an/sloa101b/sloa101b.pdf
https://www.can-cia.org/can-knowledge/can/can-fd/
https://www.csselectronics.com/screen/page/simple-intro-to-can-bus/
https://www.csselectronics.com/screen/page/simple-intro-j1939-explained

==High Throughput Communication==
At first I thought this type of comms will be used short distances (such as cameras to the brain), however I remembered that Ethernet exists. Using CAT5/6 cables, high speed and throughput can be achieved. This medium can be used to transfer large amounts of sensory data from any sub-system/appendage to the brain. We could even utilise existing networking implementations and have a local network within the robowaifu.

The issue with using IP networking (other than the obvious security issue) is that much more powerful microcontrollers are required to run the TCP/IP stack. However I don't think we need the full network capability. Firstly I wouldn't allow any remote connection to this LAN at all, and secondly the Ethernet physical layer could be used without TCP/IP. Although the advantage of using TCP/IP would be that data correction and packet fragmentation is available.

This type of comms would be brought up later in the power on sequence, so it cannot be relied on for critical messages.

=="Spine" Interconnect==
A robowaifu will contain a great number of sub-systems and even greater number of sensors, actuators, processors. To minimise the wiring required, while also allowing a greater degree of control by the brain, sub-system communication should be aggregated and then sent together to the brain.
The spine will contain:
- a network switch (allowing Ethernet connections to the rest of the body)
- control registers, which the brain uses to enable/disable sub-systems.
- power control

Having a network switch in the spine ensures only one network connection is required to the brain, and spine's number of Ethernet ports can be extended as needed.

The control registers are a flexible area of memory (perhaps implemented in an FPGA?) that allow control of sub-systems at a higher level. Enable/disable, debug mode, operating profile (performance, efficiency etc.), and anything else that might come up.

The power supply rails (both emergency and main) can be toggled for each sub-system. The restart sequence also has to be initiated from the spine, to ensure a safe power down occurs without loss of data. A default power profile will be stored in the spine firmware flash, however the brain can make any changes as necessary during operation.
==[END OF PART 2]==

# 3
>>11018
>>11019
==[PART 3]==

==Additional==
While writing this I actually started getting more and more ideas. One such idea is the Operating System for the brain must have a kernel that can grant access lower level functions (power control, sensor data, etc.). Not sure how far the kernel and userland model can be taken for a robowaifu (as it is a real-time system after all). Perhaps there will be a real-time OS component, and a "normal" OS that is allocated resources whenever the real-time part doesn't need resources?

This draft is missing a lot of detail on the sub-systems themselves. Is an arm a sub-system, or is it a combination of several sub-systems? Well, the answer is likely the latter, but perhaps the brain might only see an abstraction based on control registers and a memory area for complex set of commands...
Just like our appendages are great number of systems, so will the robowaifu have sub-systems within sub-systems. CAN bus and Ethernet can propagate as far as needed by a complex sub-system, and the implementation detail within the sub-system is up to the developer. Now we just need a standard set of commands, registers, and custom extensions to include in the spine for the brain to control.

Thank you for reading this Anon! I hope it either stimulates you to build your own robowaifus or gets you to look further into various aspects of a real-time engineering system!

# 4
Outstanding OP Anon. 

I consider anon's ''IPCNet'' document (>>2418) informative, if not directly pertinent to your thread. Also, this work certainly bears inclusion into the ''Robowaifu Design Document'' (>>3001). It's my hope you'll expand your effort here into a full-fledged document, similar to the IPCNet one.

I consider this an important step forward for /robowaifu/.

>note:
>''From a legal stand point, this is under CC0 or public domain (unless Chobitsu has specific licensing for the content on /robowaifu/).''
I'll add a post to our Licensing thread to bring it up for discussion on compatibility with our main BSD-3/Expat(MIT) licensing.

# 5
>''CAN-CAN System Engineers Dancing in the night tbh''

# 6
>>11026
Thanks for the links to the docs Chobitsu. The LaTeX doc is quite thorough, so I gave it a skim read for now. I'll look into the refman package and start a write up (unless you have specific suggestions/templates).

The IPC doc got me thinking about a few other aspects, which I'll add sections for.

Oh, and I'll change the License from CC0 to MIT(Expat), as it is adequate for this work.

>>11033
Thanks for the material, gotta to read up on CAN before I can make further progress.

# 7
>>11052
>Y/W
>Good luck
https://copperhilltech.com/controller-area-network-can-bus-prototyping-with-the-arduino-uno/

# 8
>>11018
excellent
this is what we need, basically a robo waifu is going to be more that the sum of a CPU / AI chat and some animatronics. It will needs its own standards and conventions and its own language, so to speak.

# 9
>>11026
>I consider anon's IPCNet document (>>2418) informative, if not directly pertinent to your thread.

wait, how did I miss this? I feel like this should be at the very top of the Pinned Library Thread and in a FAQ at least. A master document that ties everything together and provides a comprehensive overview of everything that's been worked on to this point is essential to the viability of this project.

# 10
>>11054
>It will needs its own standards and conventions
This is something I have noticed to be lacking, probably because you need to be interested in reading/analysing standards (and have engineering experience). I like this seemingly boring task though XD

>>11055
>A master document that ties everything together and provides a comprehensive overview of everything
I agree that it is essential, as long as we have a condensed version available. It's important to have an overview doc being somewhat readable (perhaps 50 pages max), with specific considerations being available separately and in a giant combined doc.

With latex we could have separate .tex files for each consideration (RPCS, IPCNet, mechanics, embedded software, application software, etc.) which can then be compiled into both separate and one large document.

# 11
>>11052
>The LaTeX doc is quite thorough
Honestly, it's simply a skeleton framework, written in a scant few hours of frenetic thinking. There are literally at least a thousand pages yet to be written!
>I'll look into the refman package and start a write up 
Good thinking, please do. This package seemed to be the most versatile for our needs with the big task of designing, engineering, prototyping, & manufacturing robowaifus. I think it's a very good choice.
>(unless you have specific suggestions/templates).
Actually, that's my specific advice in '''§ 18.4 ''Changing the layout, step by step'''''.

>Oh, and I'll change the License from CC0 to MIT(Expat), as it is adequate for this work.
Sounds great Anon, thanks. BTW, I'll go about clarifying the ''MIT(Expat)'' in the various license designations we have about.

# 12
>>11055
> I feel like this should be at the very top of the Pinned Library Thread and in a FAQ at least.
I don't have any objections to that Anon. In fact if you'll create a good FAQ for the board (I'd suggest a /meta post for it), I'll add it to our ''Welcome'' thread.

>>11058
>I like this seemingly boring task though XD
You're hired! Honestly, we as a board '''__need__''' an Assistant BO. Right now I'm literally the only one looking over the place, and that's a very tenuous position for a board I personally consider both truly unique and ultimately quite valuable. Please consider becoming a board vol, Electronic Chronicler.

# 13
>>11060
>In fact if you'll create a good FAQ for the board (I'd suggest a /meta post for it), I'll add it to our Welcome thread.

I can do that, where would you like me to submit the drafts for this FAQ?

# 14
>>11060
Honestly, we as a board need an Assistant BO.
Sent you a message, hopefully it got throught your spam filters ;)

# 15
>>11067
I'd suggest submitting it within the /meta-3 thread Anon (>>8492). Don't be concerned it it needs to be a multi-parter (6144 char limit for our site) that's fine.

>>11090
>Sent you a message, hopefully it got throught your spam filters ;)
Yes, I got it, and replied.

# 16
>>11093
>Yes, I got it, and replied.
Unfortunately I locked myself out of the password manager I have, and not been able to hashcat my way in. So that email account (and your message) is effectively lost.
I'll message you again once I set up an email (and calm down from my own stupidity).

# 17
>>11095
Oh no! I hope it wasn't tied to anything essential Elec-Chron.

# 18
Continuing this discussion from another thread:
>>11098
>>11099

I can't help but think that there should be something like the OSI model for programming sub-systems, where higher layers in general are built on lower-layer elements. I'll take a first crack at defining it:

==Layer 1 - Hardware==
This layer likely wouldn't actually contain any AI/ML elements, and just contains the raw code required to make specific hardware work. This could also be considered as 'device drivers', or, if you like to think in terms of human development, the unconscious body knowledge (how to move your individual muscles, but not any co-ordination). Ideally, the drivers would have a standardized interface so that the higher layers of the stack could be migrated to another set of hardware with minimal retraining. This layer would most likely come shipped with a set of hardware.

==Layer 2 - Low-level tasks==
 This layer is largely responsible with interfacing directly with the device drivers to accomplish a low-level task. Examples of things that code in this layer might do could be:
- Grip an object with a certain force
- Move appendages to a certain angle/location
- Translate audio input into a useful form (text, most likely), and translate text back to audio output.
- Vision processing could potentially fall into this layer?
These are all things that require direct sensory input or device output. Here, some machine learning may be required, though some of these tasks could be driven by hard code. We start to see groups of outputs connected together toward a goal. This layer could be open-source and shared, though might also come shipped with a specific set of hardware.

==Layer 3 - Mid-level tasks==
This layer combines multiple low-level tasks into a constructive whole. To make another human development analogy, this would probably be tasks that a toddler might begin learning (though the AI will likely attain mastery of these skills at an adult level). Examples might be:
- Reach out and grab an object
- Walk to a specific location
- Synchronize lip movement with audio output
These are all tasks that could be recognized as a 'skill', but not one that humans perform consciously. Most of them will require implementation of either machine learning or some manner of procedural generation. Here and in the next layer, it makes the most sense for these 'skills' to be built on a shared model.

==Layer 4 - 'Skills'==
This layer combines mid-level tasks into something we'd call a "skill". Something like cooking, driving, singing, dancing, conversation, etc. Really, anything you might consider taking a class on to improve would fall into this category. It combines and sequences layer 3 and potentially layer 2 tasks into a whole package. These might be something you'd drop-in and drop-out to teach your robowaifu something new or update their ability.

==Layer 5 - Autonomy==
Up until now, our discrete programs have largely been of the form 'send command, get output'. Here is where we get into the wild world of higher-order thinking and decision making. Tasks here are largely more abstract, and their goals are to orchestrate the execution of layer 3/4 code. Ironically, here a shared model becomes less desirable again, because the knowledge here would likely be viewed as what makes up your waifu's "personality".
Examples of goals that might be in Layer 5 would be:
- How should I respond to a certain question or request?
- How should I approach a dangerous situation in the most optimal manner?
- When should I make breakfast?
This is the layer I'm least confident about, and it might be wise to break it down into a more manageable chunk. I'm not sure how, though. Code at this layer is the kind of problem that I'm sure keeps AI researchers around the world awake at night. However, the pyramid of lower-layer skills helps this 'orchestration' AI avoid having to learn every possible skill and how to move every single joint, which would cripple it by sheer computational weight.

Please critique and modify these layers as much as you like, this is my first thoughts and my source on this is entirely my ass.

# 19
>>11101
>This layer could be open-source and shared
I wouldn't personally get behind anything that ''wasn't'' 'open-source and shared' relating to our own robowaifus, friend. Glowniggers are quite problematic enough without purposefully inviting ''Big Brother'' directly into our homes via un-auditable, Globohomo Big Tech/Gov systems.

# 20
>>11101
I love it
lets do it

# 21
>>11113
Yeah, that's fair. Ethically and personally, I think any code running on what is supposed to be your closest companion should be 100% transparent to you. You wouldn't want Amazon RoboWaifu to send all its sensory data back to Bezos so he can simulate your life and sell you shit.

Pragmatically, I wouldn't be surprised if at some point in the future hardware companies get involved, build a robot for consumers to buy, and want to keep their sauce secret as it relates to low-level interfaces like that so people can't just reverse-engineer their design. I don't know if I'd ever buy one for myself, but there's likely R&D advantages that come with a larger company.

My "pipe dream" is that we hit a tech singularity, our waifus self-produce, and they like us enough for peaceful coexistence. That's the only scenario I'd be personally OK with closed-source, since it's outside of human influence and I'd consider them independent 'people' with rights to their own private information.

# 22
>>11126
>''"I think any code running on what is supposed to be your closest companion should be 100% transparent to you."''
>''"That's the only scenario I'd be personally OK with closed-source, since it's outside of human influence"''
I'd suggest you consider your own words. You're promoting a walking dichotomy. And no surprise to me, quite frankly, since:
>''"and I'd consider them independent 'people' with rights to their own private information."''
Is a prime example of leftist ideologies, and the very antithesis of the goals behind /robowaifu/. 

Effectively, there is really but ''one'':
'''''"To improve the lives of disenfranchised men around the world, who have been robbed of any hope of a normal, healthy relationship with a normal, healthy woman."'''''

This theft has been due __entirely__ to leftists and the globohomo agenda they effectively all universally espouse now. To wit, ''there are no normal, healthy women left''. I'd suggest you familiarize yourself with the board's culture, in the unlikely event you think I'm just pulling this firm cultural and sociological position out of thin air here.

# 23
>>11128
I think we're having a failure to communicate here, because I wholeheartedly agree with the cultural and sociological postion you've made. Men truly have been robbed of the hope and the joy of a normal healthy relationship with a woman, because the normal healthy women have been destroyed (or possibly never existed in the first place).

I think our misunderstanding is that my pipe dream veers a little too far into science-fiction, and is a place we will probably not see in our lifetimes, but maybe the next few generations will.
The tipping point I'm trying to present is IF (and that 'if' is unlikely and where we steer into the realm of fiction) machine learning hits a point where it builds and grows on itself, and our robowaifus begin to develop themselves. At that point, their source code would be their own creation. To ask for the source code that they created for themselves at that point (if we could even understand it, since it may well be pure bytecode) would be the same as asking a human for a full scan of their brain.

# 24
>>11129
>pure bytecode
Then it's a matter of understanding the architecture the code is executed on ;)

# 25
>>11129
I see, thanks for the clarification Anon. My apologies for my manner, it wasn't really my intent to be dismissive of your point. Please forgive me.

I'd say we've veered well off-course ITT, and are pretty squarely in the realm of philosophy. Heh, anon even created one for us recently! So, my philosophy on your position is more of a 'all things are naked and open' type of deal us to our robowaifu's 'souls', but I think I understand your position now. Since as you say, it's unlikely that any of us are likely to even confront such a scenario I think we can pretty comfortably simply delay the topic indefinitely. :^)

# 26
>>11132
I responded to your 3rd email.

# 27
Great topic.  Though I think you can consolidate some of the levels, especially for smaller scale robowaifus.

I'm a hardware guy and I think the hardware part will get easier as more purpose built devices become available.

For example, in some of my rc cars I have a lights controller, a sound controller, and a video controller.  My custom sound controller used be be an arduino and a micro SD card reader.  Now there's a dedicated mp3 player with card slot that interfaces with serial.  The lights controller used to be another arduino module, now they make RC receivers with built in lights controller.

I thought I would have to hook up a discrete camera with an ESP32, now guess what ESP32-CAMs are so standard now that I haven't even touched my dedicated ESP32s at all.

So we can assume that the most basic hardware tasks... if there is no dedicated hardware already, then it will be a basic arduino already programmed with the libraries to interface with that sensor.  Now for others...

CAN bus... good idea.  I notice most of the university rover bots use some form of CAN bus.  I need to look into this, I don't know where to begin.

LAN / ethernet... I'm not sure.  Most microcontrollers are IOT devices so they have built in wifi (ESP8266, ESP32).  Of course they're not that secure but perhaps there's an argument of wi-fiing commands to the arm rather than stringing a long cable along.

# 28
>>11138
>CAN bus... good idea.  I notice most of the university rover bots use some form of CAN bus.  I need to look into this, I don't know where to begin.
Probably a good choice here:
https://copperhilltech.com/a-comprehensible-guide-to-controller-area-network/

I think autonomous cars are a good intermediate target towards full robowaifus tbh.

# 29
>>11139
> autonomous cars
I think that any move towards taking individual control away from a method of transport is a bad idea. As an electronic engineer, I want fewer automated systems in cars, not more. They only cause more issue for local repair services and centralize the access to spare parts. Also networking in cars is one of the worst developments I've ever seen (to hell with security, just give the access to the major engine systems over network eh?).

A good compromise would be automated public transport, heavy goods, trains, but only on dedicated "highway"-like lanes. Not only this would make the electronics simpler (already achievable), it also leaves the normal roads alone.

>>11137
Seems that this email server is either not visible to yours, or is not accepting the email all together. Apologies about that.
You know any good alternatives before I just go and make a pozzed account instead? XD

# 30
>>11138
>I thought I would have to hook up a discrete camera with an ESP32, now guess what ESP32-CAMs are so standard now that I haven't even touched my dedicated ESP32s at all.
I agree with you that integration will come, and that it will improve. What I don't want to happen (and what already happens) is that you get dedicated SoCs that are so complex, that the designers themselves barely have much of an understanding of what's available (and the number of bugs and/or exploits).

I'd rather have a description that covers the interfaces in such a way as to allow both modular and integrated design, so that paranoids like myself can use simpler parts to separate the functionality (in exchange for more required space, bill of material increase, extra cost).

> Of course they're not that secure but perhaps there's an argument of wi-fiing commands to the arm rather than stringing a long cable along.
Maybe the RCPS standard should just include a more generalized concept of an IP network, where the implementer has the choice of using a wired or wireless protocol. Again I'm skeptical with the use of WiFi due to its vulnerability and ease of remote access/hacking, but the option can be there. Perhaps for smaller scale robowaifus, or even for swarm bots WiFi has a better use-case. I'd argue ethernet cables are not too large, given the scale of adult-sized robowaifus.

# 31
>>11140
<autonomous cars
>I think that any move towards taking individual control away from a method of transport is a bad idea. 
I certainly don't disagree Anon. I probably need to clarify my view in context
<''"I think autonomous cars are a good intermediate target towards full robowaifus tbh."''
is meant from ''our'' perspective, not the globalist's. I'll try to find a way to unpack my thoughts here w/o becoming overly wordy about it. 

One of the goals behind the globalist's Marxist agenda for the entire world is to remove any personal autonomy ''whatsoever''. So for them, the idea that you eventually wont have a driver's license and wont be able to just drive a car wherever you want to go (a clearly-implied agenda by the WEF) means you are far easier to control. Their (((cars))) you rent from them simply will refuse to go where they don't want you going. In that sense 'autonomous' cars are simply yet another means of ''control'', same as UBI say.

My meaning is simply in the /robowaifu/-esque sense of the word: namely that cars can properly figure out how to successfully navigate, maintain themselves, etc., etc., on their own -- just like our robowaifus should be able to do.

And in a more practical sense for our situation right at the moment, the statement was more properly applied to radio-controlled vehicles, which anon had mentioned briefly.

>As an electronic engineer, I want fewer automated systems in cars, not more. They only cause more issue for local repair services and centralize the access to spare parts. 
As both an engineer and a high-performance racing machines fan, I couldn't agree with you more Anon.

>Also networking in cars is one of the worst developments I've ever seen (to hell with security, just give the access to the major engine systems over network eh?).
It's a mess, and a pattern we very clearly want to avoid in devising our own robowaifus.

>A good compromise would be automated public transport, heavy goods, trains, but only on dedicated "highway"-like lanes. Not only this would make the electronics simpler (already achievable), it also leaves the normal roads alone.
That's a broad societal topic, and one I'm neither qualified nor enthusiastic about. I absolutely __loathe__ public transportation, having had to actually use it frequently in urban America. It's both dangerous (blacks), and a practical nuisance. I highly, highly doubt either situation is likely to improve with time, rather the opposite. Besides, as I sort of implied I'd much rather drive/ride myself!

My apologies Anon. LOL I definitely didn't succeed at being concise. :^)

# 32
>>11139
Thanks
>>11140
>>11144
I personally think autonomous cars are stupid, as you will literally need robot-only lanes and road networks with flawless road markings to make it foolproof.  My ideal would be walkable  towns connected by autonomous trains, and a bike that you can carry onboard those trains.  Granted my perspective is because I live in Asia where there is no race problem and public transport is clean.

Now despite thinking that real autonomous cars are stupid, the STUDY of autonomous navigation is extremely useful.  Specifically at a scale that you can install GPS modules and read AR markets (QR codes) to guide a machine along a planetary surface.

>>11141
Good points.  My general rule is to use the dumbest/cheapest chip available for the task by simplifying either the program cycle or the pincount.  Often it means reducing pincount so I can use an arduino Nano instead of a Mega, a D1 mini instead of a full blown ESP32.  Sometimes I even implement simple logic using discrete AND/OR/NAND/NOR gates and transistors if a microcontroller isn't necessary.

# 33
>>11150
We are never going to have fully autonomous cars in the U.K. Our road network is really cramped and badly designed. The government cannot even keep up with filling in potholes, never mind upgrading the whole system. Add to that lots of foreign drivers and road rage, and you get the idea. Even a super-intelligent machine cannot navigate total fucking chaos 😂 

Because congestion around London is now so bad, the highways agency even allowed drivers to use the hard shoulder on part of the M25 once, which is a nigh-suicidal thing to do. They called it a "smart motorway".

# 34
>>11151
Also, many electric vehicles and hybrids are significantly heavier than their internal-combustion engine driven counterparts. Which means even more tearing up of road surfaces in future. I think most of our roads will simply decay back into dirt tracks eventually.

# 35
>>11140
>Apologies about that.
No, it's hardly your fault Anon. My guess is that your email service is kicking anything from mine. The guy running the thing has a bit of a checkered history. I simply got it because it allowed anonymous accounts over Tor.

Anyway, here's a >tl;dr
>Saw your post about becoming an Assistant BO. What is that exactly?
<That's simply my term for what is 'officially' a board volunteer.
<I'd specified clearly to Robi that he replace me with someone from the volunteer positions if something happens to me.
<At the moment, there are no active volunteers.
<Basically it's just a safety net, to protect the board in case I disappear or something.

That should be concise enough.

# 36
>>11018

in my opinion, the robot chasis is not big enough for a proper brain.  For that reason, much of the thinking and memory needs to be offloaded into some kind of private cloud, most likely a server stack running some kind of well known cloudy services and a common database.

Humans remember by association.  Databases store using indexes.  In theory, each memory needs to be indexed and time sequenced so that it's triggered by each of the senses, some kind of "experience" relationship, and so on.  This kind of event-based memory would need to be pre-indexed (nightly job during sleep/charge cycle) and stored in some kind of ginormous long-term storage device.

Until tech catches up with the processing requirement, this will have to do.

Use of wireless tech (wifi among them) as well as some kind of cellular data connection would enable normal operation under most circumstances.  On loss of signal the brain would have to go into some kind of 'autonomous' mode, maybe respond to simple commands like "walk this way" or "go to sleep"


But as far as fitting the brain inside the robot's head, I think that's just asking too much.  Eye processing, hearing, speech, and facial expressions alone would require too much hardware in the same space.

Using network cable for the spinal column is a great idea.

I had envisioned a robot with multiple autonomous subsystems, and an overseeing "conscious" subsystem that sends simple commands to stand, walk, sit, etc. in the way that many of our normal movements are almost reflexive.  The controller subsystems would be sent a small program on how to function, then the subsystems themselves would work together with high level management by the "conscious" controller.

Communication between subsystems is therefore extremely important, as would be communication between the robot and "the cloudy part" of the brain.

# 37
>>11157
Not him Anon, but I like the Systems Engineering approach to your thinking. Volume itself is a hard restraint, as you clearly indicated. To that, I'd compound the issue by adding that wiring harnesses -- even properly streamlined ones -- are an additional consideration. These can become quite complex just by themselves, and also take careful considerations to allow for component maintenance/replacements w/o undue complications.

Further, within the same volume ''thermal considerations'' come into play once the electronics & gear become complex enough (and especially once the volume becomes tight). Routing of cooling too, becomes an issues quite similar in many respects to wiring harness designs. Just pumping raw airflow through can go a long way, but leaving clear paths for it's circuit through a volume has to be ensured. And any heat-sink radiation fins on the devices need to be properly located within the channels of airflow.

As you suggest, there are design trade-offs that can be considered (wifi, etc), but each choice properly has to be made within a bigger architectural system.

# 38
>>11157
I agree that to run the more intensive high-level calculations you'd definitely need an off-board server to phone home to.

Things that require hand-eye coordination or reflexes would probably need to be done locally though. For example, if you wanted to have the robot catch a ball, it would need to visually track the ball, calculate where to move its hand, and grip at the right time. The delay introduced by phoning up the cloud to present vision data and receive instructions may cause it to miss.

Realistically, the head isn't a good place to store a robobrain to begin with, and we should be storing the bulk of the electronics in the torso. A case could be made for doing vision/sound processing in the head just because that's where the sensors are, if the extra milliseconds to travel down the neck end up mattering.

# 39
>>11155
I tried once or twice, but he was gone to fast and also my network wasn't very stable, which might have caused it. I installed a client for IRC on my tablet, so I could try again.

# 40
>>11164
That's fine no rush. I'll be happy to ask Robi about it myself. He'll need to enable you to make an account, so we'll probably need to arrange a timeframe with you for it.

# 41
>>11144
>That's a broad societal topic, and one I'm neither qualified nor enthusiastic about. I absolutely loathe public transportation, having had to actually use it frequently in urban America. It's both dangerous (blacks), and a practical nuisance.
Mostly I do agree with you. I generally avoid using it when I can, however in euro it's at least tolerable. In the usa I remember it being kinda shit.

>My apologies Anon. LOL I definitely didn't succeed at being concise. :^)
Hehe, you ain't the only one ;)

>>11150
>Now despite thinking that real autonomous cars are stupid, the STUDY of autonomous navigation is extremely useful.  Specifically at a scale that you can install GPS modules and read AR markets (QR codes) to guide a machine along a planetary surface.
Haven't considered it on a global scale, but I imagine that would be massively useful to mankind even today. Oh inter-planetary travel, when will you come...

>Sometimes I even implement simple logic using discrete AND/OR/NAND/NOR gates and transistors if a microcontroller isn't necessary.
I really like that line of thinking. Having cheap-as-dirt MCUs have spoiled engineers and hobbyists alike (myself included sometimes).

>>11151
>Our road network is really cramped and badly designed.
Very good points. It's too common for techies and marketing to have wishful thinking, while forgetting that infrastructure is a massive cost (that not even a big corpo could really handle).


>>11155
Sent you from a third email, third time's the charm eh?
>Anyway, here's a >tl;dr
Thanks m8. Hopefully we can discuss further via email this time.
For now I guess I should setup BUMP again and clone the board?
Been a while since I bodged it to work with debian/devuan (with your fancy melon building ;) )


>>11157
>in my opinion, the robot chasis is not big enough for a proper brain.
Good point. So from an architecture point of view, would it be better to have N-number of "brain" sub-systems?
The first one actually takes charge, while the others are delegated for additional functionality (vision processing etc.).
From my point of view, only one "brain" sub-system really needs low-level access (CAN) for configuration (power, spine, sensors etc.), while the others can communicate using a high-throughput comms (the internal ethernet network) as they need to write/read much more data for normal operation.

>For that reason, much of the thinking and memory needs to be offloaded into some kind of private cloud
I see the benefits for it, and thus we must also have an open specification for the "cloud"/server component.
Personally I don't want anything to do with internet connectivity, but I admit that for debug/testing and much more complex behaviour, a server connection is required.
What I'll do is probably mention that the Spine will have an external router connected to it via internal network, which then provides the server connectivity. Otherwise the rest of the system must not have any external interface of its own, thus allowing packet filtering and port blocking done on the external router.
As a requirement, the external router must run one of the open source firmwares (Tomato, openwrt, etc.) to be compliant with the RCPS spec. Oh and of course alphabet corp blocked by default :P

>>11160
>volume thermal considerations 
Good reminder. The RPCS spec will not go too far into implementation (other than perhaps the electronics), but a document covering the thermal solutions (perhaps based on content in >>234) will be very handy. Although in regards to RPCS, thermal management means the spec must provide recommend volume for various sub-systems, as well as spacing between interface ports etc.

>>11166
>He'll need to enable you to make an account
I'm guessing this for another chap? I certainly haven't used IRC with you before XD

# 42
>>11175
One more thing about the brain.
Like a PC motherboard has a BIOS speaker, so should we have a minimal amount of hardware periphery for the low-level Brain, perhaps even just skip the whole concept and put all low level control in the Spine, with all the Brain sub-systems being connected via internal network.

I imagine at least a speaker, some lights, maybe a status display (or a debug connector for one?) to be available for checking error codes, knowing what stage in the boot process the robowaifu is in.

# 43
>>11175
>Thanks m8. Hopefully we can discuss further via email this time.
That'll be fine, I'll check in with it sometime soon.

>>11164
>>11175
>I'm guessing this for another chap?
Oh, heh. My apologies to you both. No, it was intended for you, Elec-Chron. Perhaps the other anon is helping us connect with Robi regarding your account setup? If so, thanks first Anon.

>'''note'''
''BTW, I plan to migrate all the posting on our vol account discussion over to the /meta thread so we're not cluttering up your RPCS thread with such things. So, don't be surprised when a few posts disappear ITT.''

