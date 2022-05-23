# 1
Considering where we want to go, a robowaifu with brittle and fragile PCBs, soldering contacts and delicate wires is something which can and should be improved upon. 

Closed CPU architecture is key as well as the possibility to port the waifu to a new body if necessary. 

Several supplements and 6 shots of espresso later, I've sketched this (somewhat humorous but also somewhat serious) concept. 

This is only a processor and not a memory module, but there are a few things I wanted to bring up via this illustration

1. The idea of discarding the PCB model for something suspending in heat dissipating resin, mostly rigid, waterproof and shock resistant, those chips aren't going anywhere, plus it looks black/translucent and cool and we want our waifus aesthetic without clunky square innards. This gives it the mega-man memory crystal aesthetic

2. CPUs dedicated to specific types of processing. Do one job and do it well. 

a)Since our human brains are split into left-right, logical vs. abstract, I think it would be an advantage to have separate processors to say recall facts and perform calculations vs say, paint a picture or appreciate nature. The "creative" CPU may very well work like Google AI or something of that sort via self seeding feedback-recursion. (therefore our waifus can imagine and dream too).

b)mirror neurons and environmental modeling: important for our waifu to understand that we are like her, and not simply another object like a chair or a tree. Gives her the ability to understand how to interact with others and the world via empathy by constantly comparing her own similar experiences with what she sees or experiences. This also requires an internal 3d spacial model of her environment which would be continually updates from sensory input, and like us, fuzzy logic assumption could fill in the gaps where necessary. I figure something like a GPU core array would do the trick here.

c) Impetus motivational chip - basically the reward/dopamine system 

d) Safety or Hazard prevention Chip - would interface directly with the Environmental Simulation chip, any potential hazard or danger to herself or her owner (or even another, if she is the cause) would cause her to freeze or back up a step before assessing further. Would also be useful for necessary danger/pain avoidant reflexes and self preservation. I figure industrial (BUS for example) systems such as in factories or that manage car braking, steering, etc. would already be on the cutting edge of this and we might be able to borrow something from them.



Ports would basically be for power and charging a small internal lithium battery and another strictly for I/O



Use this thread for any elaboration on this concept, or feedback (or your own ideas if you think you have something better but along the same lines)



-M.Ronin

# 2
>>10965
These are some interesting notions Anon. I think it's not unlikely we'll need some actual hardware breakthroughs to achieve an AGI. (Cf. ''Commander Data'' on ''Star Trek: TNG''). My instinct is that software alone won't be sufficient, given the typical ''John von Neumann'' hardware architectures commonly available to us. Not to in any way denigrate the great work of this man, and the other men who followed in his footsteps. But the human brain manages the wonders it accomplishes on ''~12 __Watts__'' of power. Obviously there's quite a huge disconnect going on with our own efforts, as opposed to God's.

BTW, we actually have one CE here working on his own CPU design. Maybe he would be interested in your suggestions as well?

# 3
>>10981

wait I like this

can we still have the cores inside a resin instead of PCB tho ; )>>10981

# 4
>>10965

Really good ideas anon, thanks!



>>10970

I'm looking into CPU design (not sure if I am the one that 10970 mentioned) and from your concept I see a pretty serious bottleneck: interconnect. This has been, and still is a major challenge for IC production. Although depending on bandwidth required, we may be able to get away with it.



These CPUs need to talk to each other as well as share memory, which means having some sort of common bus that can multiplex requests (or have multi-port memories).



Modern System-on-Chips (SoCs) have a similar issue and a lot of work goes into making access control policy to prevent certain areas of memory from being accessible by particular subsystems. As you can imagine, this is also where the vulnerabilities arise >:).



A compromise might be to have separate memory regions.

- Dedicated memory for each CPU, which is inaccessible to anyone other than that CPU (and the debug interface ;) ). Secure.

- Shared memory accessible to some CPUs (such as visual memory for the environment processing and safety CPU). Somewhat secure.

- Shared memory accessible to ALL CPUs. Insecure, essentially scratchpad area.



The insecure area could be using for inter-CPU communication. Perhaps even encryption could be employed for less time-sensitive messages to improve privacy.

>The idea of discarding the PCB model for something suspending in heat dissipating resin

I like your idea for moving away from PCBs, as electronics in general needs to become easier to produce locally to enable repair and reduce reliance on big corpos.

We should look into old methods of mounting hardware such as Point-to-point construction, or using a modular system based on connectors and ports. I'd rather have easier repair-ability than ultra-sleek design.



In regards to my CPU design, it is simple enough that one could produce many cores in a single system, and thus different cores could be allocated to specific robowaifu functions. My arch will be an extension of a system that is explained here (I'm not the author):

http://users.atw.hu/gerigeri/DawnOS/index.html

Being somewhat vague as I still have kinks to iron out before I will publish the documentation, assembler, examples.

# 5
>>11004
Very interesting post Anon. Though not exactly on topic with it, here's a somewhat related item about asynchrony in analog circuitry (>>10381).

# 6
>>11004

>and from your concept I see a pretty serious bottleneck: interconnect

I meant to imply that they chips would have a way to either snap into one another directly (risky, but innovative), or into some sort of semi-flexible standin for a motherboard/bus. I hadn't gotten as far as specifics, and if we're going to get into memory, now we're back to the standard PC internals paradigm (except with a miniaturized and streamlined formfactor)

However I like the idea of partitioning memory in separate "onboard" caches.

Personally, aesthetically speaking I'd like the innards to resemble small organs rather than say, legos. Chips contained inside a resin or even some time of insulating thermal "goo". Anything that micronized would be impossible to repair by hand anyhow and could be mass produced and replaceable, anything unique to your waifu could be backed up as data and restored to new duplicate hardware. However, yes, actuators, joints, power supply, sensors, all of that would ideally be self-serviceable. No Apple waifus!

# 7
>>11069
>and if we're going to get into memory, now we're back to the standard PC internals paradigm (except with a miniaturized and streamlined formfactor)
Which would be a nice step forward from where we all are ATM, technology-wise. For example (not that I'm super happy about it) the goyphone revolution wouldn't have ever happened (and least not anytime soon) without, well, ''goyphones''. No one would lug around a clunky old desktop x86 for what a goyphone provides them.

>Chips contained inside a resin or even some time of insulating thermal "goo".
Actually you'd want the 'thermal' goo to be heat-''conductive''. As in 'please dear goo, conduct all the heat I'm making inside my innards away from me as fast as possible!!' Even if you find innovative approaches to technology, you'll still have to make it work in the real world, with real physics. Heat is always going to be an enemy for our tech, and needs to be dumped efficiently.

>all of that would ideally be self-serviceable. No Apple waifus!
What? No murderous ''iDolly-bots'' Anon? :^)
Heh, yes we definitely need to keep user-serviceability for our robowaifus firmly in mind for our designs here.

# 8
>>11072

lol i meant Electrically Insulative while being Thermally Conductive, yes



>goyphones

>What? No murderous iDolly-bots Anon? :^)

 lel

# 9
>>11074
Not too surprisingly (all good engineering work is basically calculating the physical and economic tradeoffs of a system), silver is both a __great__ ''heat'' conductor, and a good ''electrical'' conductor. It's a conundrum we've been dealing with for at least 100 years.

If you come up with or located a great compromise choice, please let us know Anon! We certainly need a solution for this. :^)

https://forums.tomshardware.com/threads/how-is-thermal-paste-made-of-silver.2887885/

# 10
>>11075

>Thermal paste is mostly a grease carrier with some powdered solids in it. For AS5 the powder is ground up silver and it is considered very unlikely that the silver particles will ever perfectly line up to cause a short because of the very large amount of grease and tiny amount of solids.



admittedly that's tricky, I imagine anything that surrounds the silver will impede its heat conductivity. This will require thinking outside the box, maybe metamaterials of a certain property could solve this one

# 11
>>11076
>This will require thinking outside the box, maybe metamaterials
Sounds great. I'm sure you can think of something interesting for it. Please keep us updated here on it ITT. My guess is some form of liquid carrier for the heat -- something that is also electrically insulative -- will be the proper course for us in keeping our high-heat (eg, hip actuators, etc.) robowaifu components nice and cooled off.

# 12
>>11072
>>11074
>>11075
>>11076
>>11079
Simply crosslinking this post here, since we already have an entire thread dedicated to this topic. (>>11080)

# 13
>>11081

thanks!

that led me to this as a possible solution

https://en.wikipedia.org/wiki/Silicone_oil

# 14
>>11075

here we go, I posted in the other crosslinked thread. This is certainly doable.

>>11106

