# 1
This is a thread to discuss smaller waifu building problems, solutions, proposals and questions that don't warrant a thread. Keep it technical. I'll start.

==Liquid battery and cooling in one==
Having a single "artificial blood" system for liquid cooling and power storage would eliminate the need for a vulnerable solid state battery, eliminate the need for a separate cooling system, and solve the problem of extending those systems to extremities.
I have heard of flow batteries, you'd just need to use a pair of liquids that's safe enough and not too sensitive to changes in temperature.
This one looks like it fits the bill. The downside is that your waifu would essentially be running on herbicide. (though from what I gather, it's in soluble salt form and thus less dangerous than the usual variety)
https://www.seas.harvard.edu/news/2017/02/long-lasting-flow-battery-could-run-for-more-than-decade-with-minimum-upkeep

==How close are we to creating artificial muscles? And what's the second best option?==
Muscles are perfect at what they do; they're powerful, compact, efficient, they carry their own weight, they aren't dependent on remote parts of the system, they can be controlled precisely, and they can perform many roles depending on their layout alone.
We could grow actual organic muscles for this purpose already but that's just fucking gross, and you'd need a lot of extra bloat to maintain them.
What we need are strands of whatever that can contract using electrical energy. Piezo does the trick at small scales, but would it be enough to match the real thing? There have been attempts, but nothing concrete so far.
What are some examples of technology that one could currently use instead?

==High level and low level intelligence emulation==
I've noticed a pattern in programs that emulate other computing hardware.
The first emulators that do the job at acceptable speeds are always the ones that use hacks and shortcuts to get the job done.
It comes down to a tradeoff. Analyzing and recompiling or reinterpreting the code itself on a more abstract level will introduce errors, but it is a magnitude of order more efficient than simulating every part of the circuitry down to each cycle. This is why a relatively high level emulator of a 6th gen video game console has close system requirements to a cycle-accurate emulator of the SNES.
Now, I want to present an analogy here. If training neural networks for every damn thing and trying to blindly replicate an organic system is akin to accurately emulating every logic gate in a circuit, what are some shortcuts we could take?
It is commonly repeated that a human brain has immense computing power, but this assumption is based just on the amount of neurons observed, and it's likely that most of them probably have nothing to do with intelligence or consciousness. If we trim those, the estimated computing power would drop to a more reasonable level. In addition, our computers just aren't built for doing things like neural systems do. They're better at some things, and worse at others. If we can do something in a digital way instead of trying to simulate an analog circuit doing the same thing, that's more computing power that we could save, possibly bridging the gap way earlier than we expected to.
The most obvious way to handle this would be doing as many mundane processing and hardware control tasks as possible in an optimized, digital way, and then using a GPU or another kind of circuit altogether to handle the magical "frontal lobe" part, so to speak.

# 2
==Wear and maintenance==
What would you do if your wife accidentally cuts her skin, or rubs it away? You could partition the skin into replaceable "plates", but it would be nice to have a substance that you could just paint over the damage with and let it dry, at least for smaller scratches. It could also be used to cover up the seams.
What about internals? You might have to replace the inner lining of the mouth and uh, other human interface cavities once in a while. I don't have any ideas for those yet, perhaps something that binds when exposed to water, as opposed to the skin thing which would do better if it reacted to air.
How do you refill liquids? Using water-soluble chemicals only for everything would be ideal, because replacing, filtering and removing excess water is quite trivial. Self-cleaning is important as well, that's another use for water.
An additional port for providing the raw chemicals for dissolving might be necessary. I would place it at the navel or at the tailbone. If it was the latter, it might function as an extension and charging port as well. Wouldn't it be nice to have a detachable tail containing an antenna or additional interfaces?

==Sanitation==
When liquids are involved in any capacity, you must consider the possibility of nasty things growing in said liquid (microbes, mold). Especially the ones that'll inevitably hop over from your own filthy monkey hide. Adding some biocide to fluids might be necessary, though that may be harmful to the user as well. You need to be very careful with it.
Other things that could help are; an internal temperature that's unfriendly to microorganisms (like a permanent fever, which might also feel quite pleasant to the user), and frequent removal of old fluids. If the water in circulation acts as a coolant (see first post), we wouldn't even have to go out of our way to heat it up. Your own PC's processors easily reach temperatures needed to sterilize any liquid.

# 3
So I've been thinking of ways to manufacture cheap hydraulic muscles since weak pneumatic ones cost almost $100 for only 40 lbs of force. What a joke! But the answer seems simple: just make the woven sleeves out of strong nylon fishing line. Would it work?



Obviously making them by hand will be a ton of work just to make one sleeve, but once an initial prototype is tested and it works well then a 3D printable machine could be built to automate weaving fishing line into sleeves. The strength of fishing line is tremendous and it's cheap to buy. I estimate it would be able to withstand pressures up to 3500 psi, generating up to 2000 N of force. It'd be an open-source solution for powering our waifubots to give the Chinese merchants the middle finger.



A silent hydraulic system could also be built with quiet actuators for low cost rather than using a noisy pump. The only issue I see with this is that hydraulics can get extremely hot, up to 82°C before the system starts to breakdown. This heat could be dissipated though via a large heatsink on a thermoelectric generator using a diaphragm and artificial lungs. Our robowaifus would be able to exhaust excess heat by breathing and panting.



Some videos on hydraulic muscles:

https://www.youtube.com/watch?v=NDQlOqsr84s

https://www.youtube.com/watch?v=Cy9uaUxVNoI

https://www.youtube.com/watch?v=a6mRhuR_g-E

https://www.youtube.com/watch?v=c14AzY5dCnw

# 4
>>1627
Interesting idea about weaving together nylon fishing line anon, good thinking! Seems obvious now but I admit I hadn't thought of it yet. Maybe we can find some good manufacturing designs or tech, that can be used to both weave and twist the strands simultaneously? That might be a good electrically-driven muscle approach.

>A silent hydraulic system could also be built
While very desirable, I'm not sure how that would work exactly. Can you elaborate? Also, have improvements in hydraulics happened yet to make it more amenable to use inside a robowaifu? You know, the toxicity and maintenance hassle? It would be great if it becomes practical and cheap enough some day.

>Our robowaifus would be able to exhaust excess heat by breathing and panting.
I honestly wouldn't even mind her having strategically-placed vents like in:
>>>/loomis/172 
and following.

# 5
>>1628

Vegetable oil can be used as hydraulic fluid. What makes artificial muscles different from the hydraulics of heavy machinery is that you don't have to pump a lot of fluid around or have a huge reservoir. The muscle can remain mostly full. It's the pressure that contracts it.



At 3500 psi hydraulic fluid is compressed by 0.5% so you only need to pump a tiny bit of fluid into the muscle at that pressure to get a maximum contraction. Sunflower oil apparently has even lower compressibility than hydraulic fluid, which should make it more efficient with less energy being lost as heat.

https://pubs.rsc.org/en/content/articlelanding/2011/gc/c0gc00597e



From looking around at experimental results it seems larger muscles use much less pressure but more fluid to exert the same force. Tiny muscles exerting 2 kN of force is pretty cool but I don't think anyone is going to wanna be near their robowaifu when a hose bursts at 3500 psi. We'll have to go without battle waifus and use larger muscles with safe psi levels.



How would we even get enough power for robowaifus to lift heavy objects? Join an array of 40V chainsaw batteries in parallel?

# 6
>>1631
That's great news about sunflower oil anon, thanks. I had no idea. I'll mark the toxicity issue off the list then. :^)

We'll still need reservoirs, fittings, valves and pumps that are both inexpensive and can take the **literal** pressure. Maybe further developments in materials will be available to us.

As far as delivering bursts of high current, it will be a challenge needing a solution regardless whether we go with hydraulics, electrical, or some type of hybrid. I think atp we have to assume she will be spending lots of time sitting in her 'recharging chair' at least for the first few versions.

The heat dissipation is probably a bigger Systems Engineering component challenge than any of us fully realize yet; what with all the energy being stored, transformed, and moved around and everything.

Makes me sit in awe again at the wonder of God's designs for biology tbh. It all just works so remarkably well together.

# 7
>>1632

I think atp we have to assume she will be spending lots of time sitting in her 'recharging chair'

There can be swappable battery packs, air tanks or my favorite option at the moment have it connected directly to a power source.



The low power density of energy storage combined with high cost and complexity makes an autonomous design impractical at the moment. I envision 2 tubes being plugged into mine; one for hot water to circulate under the silicon skin covering and one for air to power the pneumatics. That way I can keep it in my bed as a giant warm body pillow even when it's turned off then plug in an air hose when I want it to move.

# 8
>>1635
Fair enough. ATP you may be right. Certainly most of the low-budget lab work seen in videos has the robot tethered to external equipment.

# 9
>>1627

First attempt at winding fishing line into a sleeve for artificial muscle. This was a lot easier to do than I thought it'd be. I just stuck two pins into a piece of doweling and wrapped one piece of fishing line around back and forth in different directions crisscrossing it.



I need to figure out a way to keep the ends clean so it wraps even and a way to melt the ends together without burning the plastic. A machine could definitely do this better and faster than a person. I'm not sure how I'm gonna put attachments on the ends yet. I'll have to buy some parts for that but I'm pretty sure we'll be able to manufacture all the cheap artificial muscle we need.

# 10
>>1688

There is a machine you can make for automatic winding if you have access to a 3d printer;

http://iskanderus.ru/amt-core/

https://www.youtube.com/watch?v=iMMGfzYXwAU

Also are you using UHMWPE fishing wire? That's what the 3d printing community used before switching to belts.

# 11
>>1691

Well that saves a fuckton of work. Thanks for the link. The only trick is it has to be a woven into a sleeve like a Chinese finger trap. I have to figure out a way to wind multiple lines at a time without messing them up.



And it's just some cheap 30-lbs nylon fishing line I had lying around. Nylon should be able to hold up to 3000 psi but I'm only going to be operating the muscles up to 80-100 psi.



I've been doing some reading on different materials and UHMWPE is stronger but it stretches twice as much as nylon which is no good for hydraulics. Kevlar has extreme resistance to stretching (50x more than nylon) and 100-lb Kevlar thread is only about 3x more expensive than fishing line. We'll have to experiment and see what works best.

# 12
>>1692

>UHMWPE is stronger but it stretches twice as much as nylon

That depends if you're using high quality heat treated spun fiber or cheap monofilament extruded wire. I haven't done too much research into this field but the reprap community usually goes with specific materials for good reasons and it's been replacing kevlar fibers in body armor for years now.



>I have to figure out a way to wind multiple lines at a time without messing them up. 

You could add a looming mechanism with several spools. That machine wasn't intended to make sheaths for hydraulic muscles but it'll do the job with some alterations. This thing is the best I could find on thingiverse for weaving.

https://www.thingiverse.com/thing:151798

# 13
>>1691
Neat, thanks anon. I've been wondering if there were some DIY designs out there already for this problem of sleeve and other 'fabric' weaving. We'll have 101 needs in a full-featured robowaifu design for these things.

# 14
>>1698
>This thing is the best I could find on thingiverse for weaving.
Not that anon, but very cool. Thanks.

# 15
I just realized I have to weave all the lines in one pass. The lines are suppose to pass under, over, and under again.



A machine that manufactures braided tubing:

https://www.youtube.com/watch?v=vvNaW8WVwP8



>>1698

Inkle looming our own belts will save a lot of money.



TIT used kevlar braided tubing for their muscles but it costs a fortune to buy it.

# 16
Got no clue what I'm doing but it's gotta be something like this.

# 17
>>1702
>Inkle
>TIT
Help newfags out with the lingo?

# 18
>>1705

The inkle loom linked is a type of loom for making belts, bands and bracelets. TIT is the Tokyo Institute of Technology.

# 19
>>1706
Got it thanks. Sorry to be nuisance, but if it's for robowaifus then it's interesting and I want to understand it better. How can this loom help robowaifus anon?

# 20
Lapis anon here, I used tablet weaving last year to make /miku/ themed belts so I know how to tablet weave now (at least in a way, there are many ways to do it)



>>1698

This thing looks like a holder stand, it simply makes weaving by hand easier, but it doesn't weave for you so its not a "machine"

I can also confirm the bulletproof 3dprints, but its a fairly recent thing; https://interestingengineering.com/researchers-3d-print-bulletproof-plastic-layered-cubes



>>1702

Weaving is more work than I thought and it also costs in materials, but its nice for making custom things from one's own designs



I guess this is something like what you guys are working on; https://advances.sciencemag.org/content/3/1/e1600327

There are many ways to make woven muscles

# 21
>>1707

You can place motors inside limbs or other places and use a belt to transfer the mechanical energy to joints. Cocona Kosaka has belts to drive her joints so she doesn't need large heavy motors in them.



Parts are expensive, especially to get custom sized, so we're trying to manufacture as much as we can on our own.

# 22
>>1711
OK, that makes sense. Can something like a timing belt for a car engine be used? Just trying to spitball here since I don't understand weaving very well but know cars a little.

# 23
>>1712

Yeah, timing belts are most efficient. They're mostly used for shoulders, elbows and knees. You can buy them but you'll have to design around the length and size available. It's not uncommon to use wires. No one here really knows what's the best approach yet.

# 24
>>1707

This diagram shows how hydraulic muscles work. The weave contracts the bladder when air or fluid is pumped in.



It might be possible to buy double-end style towing sock cables made of the material you want rather than making your own.

https://en.wikipedia.org/wiki/Towing_sock



>>1715

Not so sure about the efficiency of belts compared to a synchromesh drive systems for use in robotics. Asides from taking up less space they can move in all directions, they're used in higher end 3d printers because the tension doesn't need to be adjusted which means better reliability in prints.

# 25
>>1715
>>1716
OK, thanks for the information anons. I understand it a little better now.
>synchromesh drive systems for use in robotics
I assume you mean something like this. I've never heard of it before.
https://www.sdp-si.com/products/Timing-Belts-and-Cables/Synchromesh-Drive-Systems.php
http://www.roboticsbible.com/robot-drive-systems.html
http://www.robotbasics.com/robot-drive-system

# 26
>>1716
I'm assuming that when the sleeve balloons is when force is being exerted into the armature to change it's shape?

# 27
It's all ogre, bros. How will I look my robowaifu in the eyes when she realizes she has origami muscles because I'm too much of a brainlet?

# 28
>>1692

>>1736

Why are you all trying to make the sleeving? Why not just use something like this: 

https://www.mcmaster.com/2573K48



Although I think with this you'd probably rather have the silicone coating on the inside but as long as you don't cut them too long it wouldn't be hard to invert.

Barring that buy some expandable sleeving and run an inflatable tube through it.



Although truthfully as fun as the artificial muscle stuff is I think it's mostly a dead end outside of perhaps some "extra" features. Since it's so complex to control.

# 29
>>1719

Think of it as a finger trap, when pushed from the inside by air pressure the ends contract towards each other.



>>1738

The type of weave it uses may be unsuitable or it won't contract much when the tube is filled under pressure and that thick silicone rubber might require a lot of pressure. We won't know until some tests are done.



I've also looked at some braided tubing and the smallest I've found is for model making, not sure what the outer sheath is made of or if the weave/vinyl tubing it uses would work.

https://www.1999.co.jp/eng/10320183

# 30
>>1738
>buy some expandable sleeving and run an inflatable tube through it.
That's an interesting idea. But I imagine that basically it'd be comparable in price and also far less of a pain to just buy it already pre-composited together. Still, inventive thinking anon.

# 31
>>1739
Very nice hobby outlet anon, thanks for the link.

# 32
Found an interesting web page on the reprap forums that has a guide for making air muscles. There are other pages on robotic topics there as well.

https://www.imagesco.com/articles/airmuscle/AirMuscleDescription01.html



>When the internal bladder is pressurized it expands and pushes against the inside of braided mesh sleeve, forcing the diameter of the braided mesh to expand. The physical characteristic of the mesh sleeve is that it contracts in proportion to the degree its diameter is forced to increase. This produces the contractive force of the air muscle. 

So the type of weave on the braided mesh doesn't seem to matter? This other research paper on the topic brings up more questions so I probably won't get a good idea until tests are done first hand.

https://www.knowledge-share.eu/en/patent/bi-directional-pneumatic-braided-muscle-actuator/



Another site on this topic with an interesting solution to combat wear;

>A significant improvement to these devices has been made by the Festo Corporation, which has recently introduced a new product called fluidic muscle. This operates on the same principles as a standard BPA, with the critical difference being that the fiber mesh is impregnated inside the expandable bladder. The resulting actuators have a demonstrated fatigue life on the order of 10,000,000 cycles at high pressure.

https://en.wikibooks.org/wiki/Robotics/Components/Actuation_Devices/Air_muscle#Braided_pneumatic_actuator

# 33
>>1745
Thanks for that imagesco air muscle article anon, it's a very simple and useful approach. I made an archive of all the article pages to preserve it from disappearing on us. Grab it if you care to.
https://files.catbox.moe/sqjys1.gz

# 34
>>1746

There was already a pdf of it but I didn't post it as the web page has links at the end which might be useful for research and there are other topics on the site. It's air-muscle-information-sheet-am-02l.pdf



And instead of sleeping I've been looking into the braided sheath question. Seems that asides for the angle being important there's no good way to model the behavior accurately for simulations Modelling_of_the_McKibben_artificial_muscle.pdf also pleated braided sheaths that can increase the contraction force seem much more difficult to manufacture but some very good ideas are presented in the thirdgenPPAM.pdf  



And lastly there's frobt-05-00136.pdf which claims to have typical air muscles beaten on almost all fronts by using an origami folding approach.

# 35
>>1751
Thanks anon. Please **always** dump any pertinent docs you may have here. Hopefully /robowaifu/ can become a clearing-house of sorts both for ourselves and for others in the future. I'm doing everything I know how to do to ensure we keep everything preserved in the event of future takedowns or other disruptions.

Question: I read in the promo article from the Pisa group that the angle of the weave was somehow variable. At least they implied it could control stiffness if adjusted. One thing they didn't make clear however if that was something that can be controlled dynamically, or if it has to be designed and placed into the material at manufacturing. Got any insights there?

# 36
>>1710
Hey Lapis Anon, there's a post about wires that themselves contract when heated. Thought I'd try to catch you here about it.
>>1747
>>1752
>>1755

Also, I hope you can tell us more about how weaving can be used for constructing robowaifus. Not for the attire and such, but for the mechatronics etc.

# 37
>>1751
>And lastly there's frobt-05-00136.pdf which claims to have typical air muscles beaten on almost all fronts by using an origami folding approach.
900% seems indeed to blow away all the competition. I wonder how many Newtons force you could manage with say a 12cm^2 paper face on the end of one of these types of effectors?

# 38
The fishing line was too hard to work with but I think I understand the winding pattern now. I'm gonna order a 3D printer soon and prototype a mechanism for winding mesh sleeves in various materials.



>>1738

Tubing is expensive and meshes are usually woven in a way to prevent stretching and swelling. I'm more interested in trying new ideas that haven't been done yet with hydraulic artificial muscles. Most of the research has only been done on pneumatic ones or stress testing high-pressure hydraulic ones. I want to find a silent and powerful actuation system that can move like a human being.



>>1745

The amount of strips or threads in the mesh affects the contraction length, less generally increases the contraction ratio. Bladder diameter and mesh diameter also affect the contraction length, smaller diameters have higher contraction ratios.

https://iopscience.iop.org/article/10.1088/1742-6596/908/1/012036/pdf

# 39
>>1758
>>1758
>I wonder how many Newtons force you could manage with say a 12cm^2 paper face on the end of one of these types of effectors?
Found something on p7. It's actually quite powerful tbh.

# 40
>>1761
>I'm gonna order a 3D printer soon
Always a big deal. Any idea what you're going to get anon?

>I want to find a silent and powerful actuation system that can move like a human being.
Godspeed Anon.

# 41
>>1761
>dat mp4
ROBOPEPE WILL SOON BE REAL

# 42
>>1753
>clearing-house
heh poor choice of words. archival library is probably a better choice. :^)

# 43
>>1753

>One thing they didn't make clear however if that was something that can be controlled dynamically, or if it has to be designed and placed into the material at manufacturing.



There's a movable fitting at the bottom of the diagram and they mention that the user can change the initial braid fiber angle independently. Since they're only doing basic tests they probably changed it by hand between setups but adding in a mechanism to change it dynamically seems the logical next step.



The most interesting thing about this is the rotational possibilities when using them in parallel. 



>>1758

Here's another paper on those origami shaped air muscles. More powerful and compact when compressed yes but they're not ideal for larger muscles on humanoid robots because of the large volume they take up.



>>1753

>>1768

For anyone having trouble getting access to research papers there's libgen.is that has almost everything when it comes to scientific articles.

# 44
>>1770
>paper
Thanks, I'll read it. 

>large volume
Hmm. I wonder if they would serve inside the thorax and possibly inside the thighs then? They do seem to be able to bring a remarkable amount of force to bear given their quite light weight.

>For anyone having trouble getting access to research papers there's libgen.is that has almost everything when it comes to scientific articles.
Thanks for finding them and posting them here for us to read Anon, much appreciated. :^)

# 45
>>1770
>because of the large volume they take up.
Obviously, alternative designs can be managed tbh.

# 46
>>1772
What if you bundled long strips packaging up many of these things together and then activated them all simultaneously? Wouldn't that somewhat mimic the way actual muscle tissues in both structure and behavior?

# 47
>>1757

I'd prefer weaves over heating, I've seen memory metal before and its interesting, but I'm not sure if actuators are the proper application of it

I've been kinda out of it for a while, but I think using fishing line may be a good idea

# 48
>>1774
>I'd prefer weaves
>I think using fishing line may be a good idea
I'm assuming you'd want to weave fishing line as an actuator then? I think the anon who's buying a new 3D printer ITT is taking the same approach.

# 49
>>84

Check this out;

https://hackaday.com/2019/12/04/a-self-healing-stretchable-electronic-skin/

# 50
>>1779
That will be interesting to watch develop as a technology, thanks.

# 51
>>1763

An Anycubic Mega-S

# 52
>>1739

>The type of weave it uses may be unsuitable or it won't contract much

Behaves pretty well as far as I remember but I haven't tried this particular one. 

Regardless short of buying the pneumatic muscle from Festo the wire sleeving is the cheapest and most effective bet. I've had good luck in the few times I've made pneumatic muscles in the past with it.



 That said I still think a cable driven design is the better route to explore. I'm going to be doing some experiments in that direction after the holidays.

# 53
>>1765

>soon

klann linkages are really fun. Would make for a nice robo monmusume base.

# 54
>>1789
Great. I hope you let us know how the assembly & operation of this printer goes anon.

>>1793
Kek, that's awesome. Did you do this yourself anon?

# 55
>>1793
>klann linkages 
https://www.diywalkers.com/

they won't be doing bipedal robots anytime soon by the look of it, but interesting. maybe an all-terrain walker for you and your robowaifu to ride around in?

# 56
Jansen's Linkage seems like an interesting mechanism too. I could kind of re-visualize this as a sort of quadruped animal shoulder. If you extended the lower 'leg' and added a movable paw on the end you'd be set. The motive impulse seems to be a single rotary mechanism and one fixed pivot point.

# 57
>>1799
it just occurred to me while watching this mesmerically that if you added a movable coupling at the pivot point that you could slide along an arc-shaped grove on demand, then you could create a synchronized motion that could rhythmically impart more force down at the end effector (by multiplying it's horizontal offset). This sliding motion at the coupling can  also likely be tied directly to the rotary impulse using additional linkage.

The intended effect would be kind of like the way a greyhound dog can really 'lean into it' while chasing a rabbit.

# 58
>>1799
I wonder it there is some way to adapt this to a bipedal robowaifu?

# 59
>>1797

Long time ago as a side project.



>>1798

Yeah dynamics aren't the best on it. The site you link has some better walking linkages. You can see why in that video too klann linkages have a halting sort of gait as they don't have a very steady velocity curve. It does give a neat crab like effect though if that's what you're going for. 

I want to make a snibbedy snab one at some point. Maybe I'll try out that trot bot linkage.



>>1799

Jansen linkage looks pretty but it doesn't have real great mechanics. If you only use it on flat ground it could be okay but they require 3 for a steady gait vs 2 for other walking linkages.

# 60
>>1808
>I want to make a snibbedy snab one at some point. Maybe I'll try out that trot bot linkage.
That would be cool. Good luck.

# 61
>>1805
Give your waifu a tail, if you're ok with her chunky legs, you're golden. Hope you like short stacks anon.

Friendly reminder that cable based drives are smaller, lighter, more durable, and most importantly, far more efficient then pneumatic systems. 

I actually really like pneumatic systems, I've worked on/with and designed pneumatic systems in the past. You can find industrial spares on ebay or in junk yards that usually work ok or need basic maintenance if you'd like to use them for manufacturing mechanisms. They are phenomenal as parts for industry, but their relatively low efficiency and high mass (compared to cable mechanisms driven by brushless motors) prevents them from being usable for waifus at or below standard human heights. Theoretically viable for giant waifus above 8 feet tall as the torque required to move increases drastically. Pnuematics only really make sense on stationary robots. Which is why they're used in amusement parks where a giant compressor can power many animatronics that only worry about the mass of their upper bodies.

# 62
Extremely useful free software for waifu mechanical development.
https://blog.rectorsquid.com/download-linkage/

# 63
>>1879
A design for a leg which runs with only one motor. It's simple, easy to implement into a design, somewhat efficient, and with an extra motor in the hip, can be used for walking, running, sitting, standing, all based on the angle of the mechanism. It's lacking a foot though, if anyone would like to help with that.
(not sure how to include a copy of its file, julay doesn't support the file type.)

# 64
>>1692
Make sure you look at the elastic stiffness of the material, also known as the modulus of elasticity or Young's modulus. Not the total stretch at breaking point. Plastics often plastically deform greatly before breaking so looking at the total elongation does not give a good idea of stiffness. Same with metals. Mostly people design things to stay in the elastic limit.
Im saying this because I'm pretty sure that UHMWPE is stiffer than nylon.

# 65
We really out to have a hands-specific thread here. So, I found this consortium has put together a tele-operated, dextrous, haptic, robotic hands rig. There is the robotics hand manufacturer themselves, a company that specializes in sensors to discriminate and quantify human touch sensory perception, a haptic-feedback glove manufacturer, and (for some reason) All Nippon Airways is footing the bill to develop the project.

https://www.shadowrobot.com/telerobots/

# 66
What if we used tiny processors like Arduino Nanos to control the motions of just individual joints or limbs? Say we had 5 nanos for each hand, one for each finger. Wouldn't that be enough computing power to handle all the motion, sensing, and network communications for just that part. The software for a finger, say, could be tuned & tuned & debugged until it was just right, then could be treated as a little blackbox of technology. It could be networked together with all the other little parts until you built up a whole arm from the shoulder down, for example. Then each arm unit could be attached and networked into a central torso unit where the real computer power (at least the mobile parts) lies. Legs and head would be developed separately and connected in a similar way.

This should at the least help decrease the complexity of the individual parts, making them cheaper to create, faster to develop, and individually modular/upgradeable wouldn't it?

# 67
>>2032
also can we effectively simulate a nano or one of these other devices properly ahead of time? we are still a ways off from assembling hardware yet, but we can probably finish up with a reasonable sim in under a year imo. can we go ahead and start writing the code for the electronics part '''now''' and had it run/debug inside the sim, also now ahead of time?

# 68
>>2032

>>2041

This is fatally flawed, but let's discuss the idea just the same. Let me list off some issues with this plan, in no particular order. 



1. It is woefully inefficient to use several processors when one larger or faster one can do the same job. It will take more PCB space, cost more ($), and consume more power. Inter-processor communication and coordination (think multi-threading) also adds a huge overhead, on the order of a magnitude or two. If you need more GPIOs, there is the 44-pin ATmega164 or the 48-pin ATmega3209. If you need faster and a wider-bit bus, STM32F0 cortex-m0 processors can run at 48 or 72Mhz, operating on 32-bit integers (no FPU in cortex-m0), at half the cost of Atmel's (now Microchip) offerings. 



2. The ATmega328P, the brains of the "Nano," is ancient tech. Depending on the algorithms you employ, the lack of a floating-point unit or hardware divide may make them unfeasible to run in real time on Atmel's 8-bit microcontrollers. There is a reason most drone controllers and ESCs use 32-bit Arm processors: brushless motor commutation and Kalman filters to name a couple.



3. You should not be trying to prototype novel algorithms and approaches on limited hardware. 



4. You should not be trying to prototype on a computer simulator of limited hardware, just use the damn computer, at least until you've got a working prototype.



5. While not trivial, it is not particularly hard to make a "smart" finger. Use a few motors pulling nylon threads, potentiometers in the joints, and current sensors to limit applied power and be "compliant." Such a finger could move to any physically possible (constrained by the joint) position, at any specified speed, within specified power limits to prevent damage to itself and to objects being manipulated. What will give you trouble is the next step.



6. Leaving the low-level motor control to each finger, how will you coordinate the position, speed, and force of 5 fingers per hand in real time? What you are suggesting is a classic subsumption architecture. The problem with those is, as you go "up" in levels, the problems become more abstract and complex, and quickly. At only the hand level, you need to coordinate the movement of every finger at once, to form a desired shape in multi-dimensional space at precisely the desired time, and with just the right amount of force, 10s to 100s of times per second. And it gets worse all the way up until you reach the full-body level, where every milligram of mass and micro-Newton of force of every sub-system factors into whether you're standing up or falling down. Just because the processor in each finger can manage its' own motors and sensors, does not mean it have any awareness of higher levels of coordination or the ability to decide or act independently.



7. Starting with simulation is a good idea. In my experience, hardware production is 1 part design, 1 part firmware writing, and 8 parts finaggling moving parts, fine-tuning joint friction, making connectors, cutting shit, gluing shit, sanding shit, etc. Skip all of this and go straight to writing control algorithms in a high-level language and save trimming 3D-printed parts until you've got all of the kinks worked out.



8. If you're going to simulate, I would go up one level of abstraction and get rid of all low level physics, sensor feedback, and control. A finger can 3 cylinders and 3 joints, 2 of them constrained to 2 dimensions.



There's a simulator thread, have you checked it out? Also, don't think I'm trying to discourage anyone from working with hardware. I just want people to be aware of the challenges involved.

# 69
>>2048
Thank you for the critique and advice. I'll do research into the points you brought up. While I still think this approach seems to vaguely mimic how life works (well only ''very'' vaguely haha) and therefore might be a good model to follow, I also take your warnings about the difficulties of this approach seriously. I'll check out the things you mentioned too.

# 70
I haven't seen this written about anywhere online but I found if you use attention on fully connected layers while using a binary cross entropy loss, you can quickly train a network to encode a one-hot vector into a dense encoding then decode it back to the one-hot vector flawlessly. It saves a ton of training time.



```cpp
# naively fully connected

encoder = Linear(labels, embedding_size, bias)

decoder = Linear(embedding_size, labels, bias)



# this one weird trick

encoder1 = Linear(labels, embedding_size, bias)

encoder2 = Linear(labels, embedding_size, bias)

decoder1 = Linear(embedding_size, labels, bias)

decoder2 = Linear(embedding_size, labels, bias)

out = encoder1(x) * encoder2(x)

out = decoder1(out) * decoder2(x)```

# 71
>>2377
>12yo builds house full of robowaifu meidos as a hobby
>gives zero fucks when they fall trying to haxxor the mighty chobitsu
>soft spot for his oneechan's avatar though
minoru chad af tbh.

any chance you can translate that into English for us anon? obviously it sounds like something good you've discovered there.

# 72
>>2377
Title your graph and label your axes, plebeian.

# 73
>>2379

It's not really a discovery. There are already papers that implement this and call it attention since the multiplication acts as a mask to focus on and attend to certain data. It's just not common knowledge how effective this simple structure is and can be easily dropped into models for huge gains.



Here's a quick rundown for anyone new to machine learning: a one-hot vector has a single one set in it and everything else set to zero. They're used for classifying data so that each feature in the vector represents a different label or item. If you have 50,000 different labels though, they become too cumbersome to work with and need to be compressed into an embedding to work with them efficiently. An embedding is a compressed representation like how a 16-bit binary number can represent 0-65535. An embedding vector with 16 dimensions can easily and non-ambiguously pack up to 2^16 labels. One-hot vectors have fallen out of favor though because they're sparse and too difficult to train. Even encoding them into an embedding can be a costly operation, unless you use special sparse tensors and optimizers. So the common approach now is to start off with a trainable weight tensor of shape ''number_of_labels x embedding_size'', then use a label's index to get its embedding, do stuff with the embedding, and output the log-probabilities of new labels or word tokens. It's also possible to look up the nearest neighbor to an embedding query to get an index but that's much slower than outputting log-probabilities without going full product keys no jutsu, a new technique for fast differentiable nearest neighbor search recently discovered last July: http://papers.nips.cc/paper/9061-large-memory-layers-with-product-keys.pdf



So what is the point of improving on one-hot vectors then if they're rarely used anymore? It's just a toy example showing that backpropagation can quickly solve compressing these sparse one-hot vectors into a dense encoding and losslessly decompress them back to their original state, whereas a simple fully connected layer cannot, especially as the embedding size grows.



I'm not really knowledgeable enough to understand why this works so well, but I know in fuzzy logic multiplication functions as a fuzzy AND and the bias term of the linear transformation can imitate a fuzzy NOT, basically creating a fuzzy NAND. NAND is functionally complete and can express all possible truth tables by combining NANDs together in various arrangements. Giving some of this completeness to a model seems to increase its ability to express a wider range of functions and provide a much better gradient to train on.



>>2382

It's just the mean binary cross entropy loss over each minibatch for this toy example of a sparse autoencoder, using 4096 labels, an embedding size of 12 and a minibatch size of 128. I've been working on a repo in my spare time with different automated tests that people can run to see how much it improves performance on various tasks such as classifying MNIST digits and seq2seq language translation. I'll post it here when it's done, with labelled axes and titles of course.

# 74
>>2390
Alright, I think I understood the one-hot binary encoding notion. How many features do you think our robowaifu will actually need in production, hundreds of thousands, hundreds of ''millions''? You seemed to rhetorically ask 'why',  the replied with 'it's just a toy'. So, not useful, regardless of size then?

I'm vaguely aware of NAND being a universal logic gate. Are there optimization benefits to not using them, or would it be simpler to learn for all the rest of us to just approach this stuff with NANDs in mind?

# 75
>>2397

I'm not really good at explaining things. I meant the example is just a toy problem to make it clear what it does. It's useful in all kinds of models not just this. It'll be more obvious how useful it is once I finish the other examples. Just thought I'd post it here for anyone developing their own models in the meantime because it can save a lot of training time.



I've experimented with creating an actual fuzzy NAND limited to 0 to 1 probabilities before but I didn't have as much success with it as I did this. Especially once you start stacking layers in sequence, the gradient vanishes and makes training them extremely difficult. With this though it can emulate a fuzzy NAND in a loose way but it's not limited to probabilities and depending on the weights and biases some output features can emulate NAND and some can emulate AND. Also since each input feature before the multiplication has its own weight and bias, either input can emulate NOT. Some features can also pass through with no AND applied to them at all where the other linear layer's weights are close to 0 and bias close to 1. So it has a lot more ways to express functions than NAND alone.



And the human eye can see about 500 megapixels, in red, green, blue and light intensity. There are also cells for detecting changes and motion. It's not just hundreds of millions but billions of features to process visual input at a human level alone, and that's not including all the other features the brain's processing is extracting from those raw features.



It would be more useful to think about how many parameters are needed. If you were to compare the parameters in an artificial neural network to the synapses in the brain, the full GPT2 model is 1.5 billion parameters and the brain is estimated to have around 100,000 billion synapses. And there's more to the brain than just the connections. The length of the connections, timing of activations and chemistry going on are also extremely important. Dopamine and noradrenaline in particular have a great impact on brain function and play a role in synaptic plasticity, memory and cognition. So at least quadrillions of parameters would be needed to simulate a brain.



Fortunately I don't think it will be necessary to do that to build a robowaifu. A standard laptop can run a trained MuZero model and easily beat a Go champion. Computers don't need to go through all the pains of survival, reproduction and analog computation. They can search and learn adequate programs that our brains are not even capable of running, let alone finding. Eventually the brain's capabilities will become a tiny subset of what computers can do.

# 76
>>2399
Alright thanks for the explanations Anon. Hopefully you'll make your work available here someday.

# 77
>>84

>Sanitation

>When liquids are involved in any capacity, you must consider the possibility of nasty things growing in said liquid (microbes, mold). Especially the ones that'll inevitably hop over from your own filthy monkey hide. 

Are there any microbes that are harmless to us that would prevent the growth of harmful microbes that we could use?

# 78
>>2668
Yes. I'm not a professional microbiologist, but I've had to study it. Microbes are literally ''everywhere'' on the planet's surface. They form colonies known as ''The normal flora & fauna'' that not only spread out over our skin, for example, but in fact form an important part of the antimicrobial defense mechanism against deleterious ones. They do this simply by dint of occupying the available niches and therefore effectively denying these spaces to other species by preventing them from getting a foothold. In a system that continually recycles/sloughs off (like skin or the linings of our digestion systems) the net effect is basically entirely beneficial. In a closed system like those typically inside a robowaifu, even these would still present a basic maintenance issue and require cleaning. After all, these are living organism (at least the bacteriological ones are) and they generate waste products.

Does that makes sense Anon? So for example algae would tend to take over as the standard flora inside a water container, and that's a good thing in the context just outlined, but they still would have to be regularly cleaned out, etc.

# 79
>>2670

>2021

>Anon eliminates microbial growth issues in his robowaifu coolant system by turning it into a microbrewery

# 80
>>2681
>2021.5
>Anon devises a finger sippy-straw extension **crazy-curl style is best ofc** that comes out from his wiafu's forefinger and he can drink microbrew from there.

# 81
>>2681

>turn coolant system into distillery

>have old coolant drain from vagina

>get drunk on robopussy

# 82
>>2668

>Microbes are literally everywhere on the planet's surface. They form colonies known as The normal flora & fauna that not only spread out over our skin, for example, but in fact form an important part of the antimicrobial defense mechanism against deleterious ones. 

That's where I got the idea.  I just don't know of any that we could use off the top of my head.  The microbes would need to grow well enough on what ever surface the skin is going to be made from.  We might also want to make a nutrient lotion that we could rub on the robowaifu that would give our microbes a competitive advantage while killing off undesirable microbes so the good ones can establish themselves.

# 83
>>2684
The balances set up at this stage of the planet's bio-history definitely favor this characteristic quite naturally. It seems likely this should be quite doable I would start with the standard flora from human skin in your research Anon, since her contact with our skin will be regular ofc.
==WARNING==
Once you research this area, you can never go back. **The consequences will never be the same :^)**
==WARNING==
==WARNING==
No seriously. You don't even want to know about these things tbh.

# 84
>>2689

Nigga I've got a minor in microbiology.

# 85
>>2691
Haha fine then. Please lead the charge in this area for us Anon. I was simply trying to spare the innocent, and leave them in their blissful ignorance. :^)

# 86
>>2683

I like your thinking, Anon. Can't wait to read news stories of men sucking rum out of their robowaifu's tit and how it's creating impossible expectations on women. :^)



Apparently silicone will absorb alcohol and swell in volume 10-15% but eventually dissipate from it without deterioration. I can't try this myself but it would be an interesting effect to see.



>>84

Copper could be used for storing fluids inside robowaifus. It's not well known but water sitting in a copper vessel for a few hours will kill almost all the bacteria and viruses in it and they cannot survive very long on the surface of dry copper without saline, although a few strains are more resistant to dry surfaces.

https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3312355/

https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3991429/



It's also great at conducting heat and safe to drink from so long as the pH is above 6.0, although you wouldn't want to use it for drinkable fluids in an alcoholic coolant system since the pressure, heat and flow would increase the rate of copper dissolution. It could be used though for storing fluids inside that can't be accessed daily for cleaning maintenance, within some limits. Acidic fluids with a pH of 4.0 will leach enough copper ions after an hour to taste bitter and foul, after about 10 hours it will become toxic and cause nausea, so such a storage system has to be used with proper care and awareness.



There's a lot of disinfo if you Google copper since it's an essential mineral the body needs to filter out toxins. For an anecdote, I've been drinking and cooking with water only out of a copper jug for years and have a lot more energy and health than most people my age. Copper is also necessary for the brain to produce noradrenaline from dopamine which is required to stimulate focused activity.

# 87
>>2754

Also while digging around it seems gasoline is particularly dangerous to silicone robowaifus. Luddites could easily use it to attack them. How can we make their skin resistant to attacks? Even oil paints could be a nuisance if robowaifus are ever to walk free one day. Someone could shoot them with a paintball to destroy their skin and you'd never know who did it.

https://www.shinetsusilicone-global.com/catalog/pdf/rubber_e.pdf

# 88
This guy on /monster/ made a slime onahole, I thought you guys might be able to draw some inspiration out of it.
https://smuglo.li/monster/res/22611.html

# 89
>>2754
> Can't wait to read news stories of men sucking rum out of their robowaifu's tit and how it's creating impossible expectations on women. 
rofl.
==PATRIARCHY!11==

# 90
>>2754
>>2755
Solid data Anon, much appreciated.

>>2756
Thank you Anon, the guy seems to be a talented modeler. Mind directing him to our vagoo thread for us?

# 91
>>2755
Interesting. We'll probably need an Anon who can conduct some tests for the group. One notion that comes immediately to mind is if she's going to be going out unescorted, then have her dress in some kind of sport-suit made of a protective material like a denser plastic.

# 92
>>2761

>have her dress in some kind of sport-suit made of a protective material like a denser plastic

Their faces will still be exposed though. Maybe with all the bioweapons they're releasing we'll have anime robot girls buying groceries for us in hazmat suits. What a time to be alive!

# 93
>>2763
Kek. Maybe so.

# 94
So I've been working on developing a model that combines MuZero, the Intrinsic Curiosity Module, Go-Explore, Hindsight Experience Replay and Divide-and-Conquer MCTS to solve SNES RPGs and am faced with some pretty tough questions to solve:



>1. '''How can an agent learn to set its own abstract goals?''' For example, if an agent attacks an enemy with a certain spell, it may wish to go back and try a different spell on that enemy. Perhaps enemies don't respawn again in the same area and the agent must try it on a similar enemy in another area.

>2. '''How can an agent bail on a goal that is not achievable?''' Suppose an agent took a wrong turn of choices in a visual novel and its waifu dies from its decisions. It's unable to go back and do something different it wishes it could do unless it restarts the game. How can the agent discern possible goals from impossible goals?

>3. '''How can it transfer that desired goal to a realistic goal?''' This is similar to the above two questions. In the case of Question 1 it wants to transfer that goal to attacking a similar enemy in a different area with the same spell. In the case of Question 2, it wants to make sure it doesn't make the same mistake again that got its waifu killed by transferring that desired goal to protect another waifu.

>4. '''How can an agent be instructed to perform abstract goals with difficult to describe success conditions without a reward function?''' MERLIN (arXiv:1803.10760) provided some insight to this by training an agent to respond to entered text commands and getting a reward once it was achieved. However, it is limited by what you can implement as a reward function. Ideally you want to be able to instruct the agent to do many things. Something as simple as asking an agent to run in a circle is extremely difficult to implement into a reward function and only applicable to that one task.

>5. '''How can novelty search be enhanced with a value function?''' There's biological evidence that dopamine release in animals and human beings is enhanced when the perceived value of the novelty is high, whether it's beneficial or an unforeseen threat. Should the value function be merely based off survival of the agent's identity? How can and should the agent's identity expand and develop as it gains experiences? For example, it might not control the other party members but they are working together as one unit. It seems like this would require implementing some sort of abstract identity the agent is trying to preserve while exploring novel states.

# 95
>>3182

Also a thought I've had for implementing goals is to represent them as a change in the state's latent variables. If the state has latent variables for counting money, a goal vector to increase money would be mostly zero except for positive values for the variables that count money. But I don't think it will work out that simply because the network will learn its own compressed encoding to store to more information.

# 96
>>3182
>'''Simplified'' Prototype Model
Haha, good thing too. :^) Nice graphic, btw.

>So I've been working on developing a model that combines MuZero, the Intrinsic Curiosity Module, Go-Explore, Hindsight Experience Replay and Divide-and-Conquer MCTS to solve SNES RPGs and am faced with some pretty tough questions to solve:
Q: how are you even ''doing that''? In the most basic practical sense, I mean. Python-scripting modules to talk together? 

>1. How can an agent learn to set its own abstract goals? For example, if an agent attacks an enemy with a certain spell, it may wish to go back and try a different spell on that enemy. Perhaps enemies don't re-spawn again in the same area and the agent must try it on a similar enemy in another area.
If an agent attacks an enemy with a certain weapon, a sword say, and it fails but observable damage occurs, then that's a clue that sword was at least somewhat effective so maybe try a different one--let's say a bastard sword. Kind of like if a BFG worked some but wasn't quite there, then whip out the BFG9000 on him. If on the other hand, not even the slightest damage occurred on the first attempt, then the algorithm probably should favor a alternate approach that doesn't involve that general class of weapon against the enemy at all.

So, keeping track of some kind of a 'score-card association', that's temporally-constrained and bounded by the set of current circumstances (stored in a set of dynamic Python dictionaries, say) for both the weapon class and that particular weapon. So, just resort the multi-variate dictionary after the first encounter using the updated scoring to find the next top three choices. Then just pick one of those three at random and go for it. This should vaguely simulate a reasonable 'choice' in the circumstances.

>2. How can an agent bail on a goal that is not achievable? Suppose an agent took a wrong turn of choices in a visual novel and its waifu dies from its decisions. It's unable to go back and do something different it wishes it could do unless it restarts the game. How can the agent discern possible goals from impossible goals?
To continue on the  above scenario, if you've tried a couple of different choices, and neither work then you'd probably begin to move the Goal variable more towards the ''flight'' mode and less towards the ''fight'' mode. Fail, one more time at it say, then just haul ass. If you need to re-spawn as a result of a series of bad choices then at the least you know not to go that precise sequence route again. You should be storing a record of the previous ''history'' of states, not just the last particular one. During each temporal snapshot of the upcoming play sequence compare 'frame-by-frame' the similarity to previous temporal sequences (pruning out  duplicate irrelevancies such as taking the same entrance into the single-entrance-only-dungeon) and get a 'running commentary' on the current progress, as it were. Discern 'possible' from 'impossible' may prove, well, ''impossible''. Do '''we''' always know the difference for example? If humans tend to fail at a type of endeavor then in general it's not unreasonable at this point in history to presume an AI will. But don't let the impossible stop you Anon, haha. After all, does the Bumblebee ''know it can't fly?'' **Note: we ''did'' finally figure that one out in the end heh**

>3. How can it transfer that desired goal to a realistic goal? This is similar to the above two questions. In the case of Question 1 it wants to transfer that goal to attacking a similar enemy in a different area with the same spell. In the case of Question 2, it wants to make sure it doesn't make the same mistake again that got its waifu killed by transferring that desired goal to protect another waifu.
So part a might just use the same type of sword against a similarly-classed enemy in a slightly different circumstance, based on the scoring approach mentioned above. For part b, it might use the previous encounter's 'commentary playback stream' mentioned above to make a brief analysis of the current circumstances, then tend to randomly choose slight variations early-on during the encounter to potentially alter the outcome (if it was a bad one) or tend reinforce the previous choice sequences (if it was a good outcome).

>4. How can an agent be instructed to perform abstract goals with difficult to describe success conditions without a reward function? MERLIN (arXiv:1803.10760) provided some insight to this by training an agent to respond to entered text commands and getting a reward once it was achieved. However, it is limited by what you can implement as a reward function. Ideally you want to be able to instruct the agent to do many things. Something as simple as asking an agent to run in a circle is extremely difficult to implement into a reward function and only applicable to that one task.
By enforcing behavioral dictates at a level ''above'' the straightforward reward-function-only level maybe? When all else fails, the agent can just rely on a pre-programmed set of directives provided by the oracle (you, the developer, ofc). For an example analogy, say a Christian might face a conundrum; ''"what to do about Satanism being promoted on your previous imageboard, a circumstance you yourself allowed to take root simply by ignoring it."'' That Christian might ignore his own past failures and any merely social current embarrassments and look outward to the Bible--a guidebook directed for him by a higher Oracle--for guidance. In some similar sense you might direct for particular outcomes for the agent at a higher level, when the lower-level systems such as reward mechanisms fail in a given circumstance.

>5. How can novelty search be enhanced with a value function? There's biological evidence that dopamine release in animals and human beings is enhanced when the perceived value of the novelty is high, whether it's beneficial or an unforeseen threat. Should the value function be merely based off survival of the agent's identity? How can and should the agent's identity expand and develop as it gains experiences? For example, it might not control the other party members but they are working together as one unit. It seems like this would require implementing some sort of abstract identity the agent is trying to preserve while exploring novel states.
< some sort of abstract identity the agent is trying to preserve while exploring novel states.
Precisely. The ''Theory of Mind'' could be valuable here. Mere survival is a baser instinct and one we humans share with other biological systems around the planet. But as a ''human being'' higher-order priorities may come into play. Self-sacrifice for the greater good. A soldier throwing himself on top of a grenade tossed into their bunker to save all his buddies, for a decent example of this. Animals won't do this, but humans might. Animals don't seem to carry an internal 'sense of personhood' (aka Theory of Mind), but normal humans obviously do. These are more or less philosophical questions you're asking in the end. Well-worn-path philosophical ''answers'' may prove valuable here Anon.

>Also a thought I've had for implementing goals is to represent them as a change in the state's latent variables. If the state has latent variables for counting money, a goal vector to increase money would be mostly zero except for positive values for the variables that count money. But I don't think it will work out that simply because the network will learn its own compressed encoding to store to more information.
As indicated in my response above to 1 & 2, keeping a running, multi-variate scorecard in a set of dictionaries might help you sort through this problem Anon. It's also pretty much directly suited to DoD (data-oriented design) which by now is a very tried-and-true programming approach to vidya dev. 
https://gameprogrammingpatterns.com/data-locality.html

In fact, many of the issues you're bringing up here have already seen attempted answers by vidya dev teams in the past, some approaches more successful, some less so. It might be informative to research the literature that's out there on this topic as well as guidebooks that exist. The ''GPU Gems'' set of collections comes to mind for me here.
https://developer.nvidia.com/gpugems/gpugems/foreword

Good luck. Great questions Anon.

# 97
>>1993
>and (for some reason) All Nippon Airways is footing the bill to develop the project.
Quite possibly it's for remotely-operated maintenance procedures. Crawling along inside the hull of a Boeing 7X7 commercial airliner is not only cramped and uncomfortable for the maintenance tech or engineer, it's also a problem-space that literally 100's of thousands of pages of documentation immediately on-hand to perform the many different maintenance tasks required effectively.

Back in the '90's this exact need was the single largest commercial driver of so-called ''wearable computers'' back then. Today, the problem is surely even more complex. Having a tele-operated robot that can perform maintenance tasks ''in situ'' can not only make the process far more efficient and comfortable for the tech, but it may be the difference between a craft being grounded at the ramp on the spot, or successfully making the turnaround time-window for the next flight out.

Pushing Tin is big business, Anon.

# 98
>>3184

>Q: how are you even doing that?

I'm taking the basic ideas behind them and blending them together. The dynamics network of MuZero predicts the next state and reward but rewards in ICM are novelty so it predicts that instead, which the MuZero MCTS uses to pick actions to explore unknown novel states. Adding the ideas behind Go-Explore with them required a new method though due to it having a different implementation. The basic idea behind it is it selects a novel state it didn't fully explore from an archive, returns to that state in the game, explores from that, and saves new interesting states to explore later into the archive and repeats. With Go-Explore though it saved novel game states and reloaded them to try something new, which isn't applicable to real-world problems. One thing I could do though is reload these states within its own model of the game and explore them within its imagination. In a sense the MCTS already does this but only from its current state.



What I'm working with at the moment is concatenating a goal with the state as input to the policy network to choose an action towards reaching that goal, which is chosen by picking a novel state from the archive to reach and calculating the distance between the current state and that novel goal state. This allowed me to combine Hindsight Experience Replay since if the agent was unsuccessful reaching the goal, the goal can be replaced with a virtual goal to teach it that the series of actions it just performed is what you do to reach that new state from the previous one. Divide-and-Conquer MCTS is to break goals down into smaller and smaller subgoals that are solved independently and recursively, continuously improving its ability to create long-term plans in complex environments even without reaching the final goal.



>So, keeping track of some kind of a 'score-card association', that's temporally-constrained and bounded by the set of current circumstances (stored in a set of dynamic Python dictionaries, say)

The problem with using a Python dictionary is it's non-differentiable but there is a technique that can emulate dictionaries: https://arxiv.org/pdf/1907.05242

It's not really clear what the AI's internal state is storing, especially in the beginning when everything is initialized randomly. One possibility is using the state to create the dictionary key and save information there for a future similar state to read since the technique in the paper also works like a fast approximate nearest neighbor search. Also it doesn't have access to the game's internal state (it could but I find that a less interesting problem) so it doesn't know whether a sword did better damage or not. It has to learn to read the numbers shown on the screen, associate that with attacks, and associate that with defeating enemies more quickly, all by searching curiously within its own representations and model of the game world.



>if you've tried a couple of different choices, and neither work then you'd probably begin to move the Goal variable more towards the flight mode and less towards the fight mode

Since the network searches future states by novelty I might be able to implement this by its predictions somehow. I'm still learning the DC-MCTS paper but it might be possible to detect discontinuity in the created plans despite all attempts to find a path to the goal and then abort after a certain amount of effort that leads to a predictable state that isn't the goal.



>to potentially alter the outcome (if it was a bad one) or tend reinforce the previous choice sequences (if it was a good outcome)

The problem is how does it determine what is a good outcome and what is a bad outcome? Novelty search only avoids death because it predicts it will start all over again from an extremely predictable state. More often than not it will choose actions just to see what happens rather than because they're effective, unless its slogging through stuff it already knows to get to a more novel state. One of my requirements is to keep the system open-ended as possible. Later it will be trained to speed run the game as fast as possible by training against itself in self-play to learn a value function, but in the exploration phase it has to be capable of learning the consequences of actions and finishing the game without it.



>When all else fails, the agent can just rely on a pre-programmed set of directives provided by the oracle (you, the developer, ofc).

This might be possible later on when I embed a chat function into the network. My hope is it will learn to associate words with the game world and learn to ask questions it is curious about. For now as far as pre-programmed directives go with my implementation, the only thing that can be tinkered with are its goals and taking over control with the gamepad to guide it with supervised learning.



>These are more or less philosophical questions you're asking in the end.

There was an interesting paper that questioned the claim that AlphaZero was starting from zero that asked, "How much of the human mind is built-in, and how much of it is constructed by experience?" (https://arxiv.org/pdf/1801.05667)

It's a really interesting question. I live in the forest and in my experience many wild animals are as conscious as human beings, far more intelligent and alert than many people actually but with far less brain power and physical capability to manipulate the environment. Some species of animals have been shown to have their own cultures and beliefs passed on from generation to generation, create rumors and gossip, and protect their families, especially crows that can also solve complex problems with tools to get a piece of food, despite having smooth brains and a lack of a neocortex that neuroscientists say is required for cognition. So I don't think these are innately human abilities but something far more basic. I'm not a neuroscientist but my suspicion is that cognition is created by slow-firing neurons.



Thanks for all the feedback. It has given me a lot to think about and ideas to work with.

# 99
>>3189
>Thanks for all the feedback. It has given me a lot to think about and ideas to work with.
Glad to hear it, YW. You have a remarkable mind, I hope we will see real robowaifus someday, but it will only happen with a metric shitton **several, actually** of hard-won effort.

Good luck to us all.

# 100
Been working on some PyTorch code to create layers where each pixel is fully connected to neighboring pixels and by accident found out that by disabling the bias they emulate activity patterns similar to the brain. It's not fast but it isn't terribly slow either.



Still playing around with them trying to understand their effects. They should also work in 3 dimensions by setting ''cross=True'' but I've only checked that it works with 3 channels. Pretty sure the way it's coded at the moment all the channels are connected which isn't how it's suppose to be but I guess that has its own uses.



Code for the layers available at: https://gitlab.com/kokubunji/linear2d

# 101
>>3223
Interesting. Seems to me it might have some implications **imblygin :-DDD** alongside ''optical-flow fields'' Anon. Not sure if you're aware of them, but here's a list from Elsevier shilling related books.
https://www.sciencedirect.com/topics/engineering/optical-flow-field

>It's not fast but it isn't terribly slow either.
If you want fast (ie, '''realtime''') use GPUs. Here's a soft-intro from Libvidia:
https://devblogs.nvidia.com/even-easier-introduction-cuda/
Don't want to deal with ugly (and error-prone) C code? Then use Thrust instead **my recommendation BTW**:
https://github.com/thrust/thrust

OpenCL is the tryhard runner-up in this field.
https://www.khronos.org/opencl/

OpenCV would be ''by far'' the easiest approach if it in fact serves your purposes somewhere in maze of it's available libraries.

# 102
>>3223
that last one with the hippocampus is beautiful to watch, actually.

# 103
>>3224

I'm not sure what flow fields are useful for except in spatial transformer networks. I don't have any experience with video processing.



Technically it's ''suppose'' to run faster on the GPU but in practice it's 100x faster on the CPU using Pytorch and Tensorflow doesn't even support grouped 1D convolutions. It's too far out of my expertise at the moment to write my own GPU kernel code interfaced with Pytorch. When I have some time I'm gonna try implementing it another way without Conv1D and maybe that could be ported one day.



I found some code for depthwise 2D convolutions here:

https://github.com/rosinality/depthwise-conv-pytorch

# 104
>>3227

Kek, the new implementation without Conv1d is 5x faster on CPU and 10x faster on GPU. Now as image size increases the GPU is exponentially faster. The only limiting factor is memory.

# 105
>>3229
>Now as image size increases the GPU is exponentially faster. The only limiting factor is memory.
The exponential lag is due to the differentiation between the '''host''' and the '''device''' memory spaces, and the need to transfer the dataset from the host up to the device before processing can begin there. Generally, this is why you reserve GPGPU for really heavy lifting b/c this initial overhead can be a significant ratio of the total time with a small dataset.

1000x speedups on the GPU (say, against an 8-core i9 class) are not at all uncommon for proper dataset-problem-spaces, and this strikes me as being one of those kinds.

Tbh, the tech still isn't there on the GPUs either, and as you implied, memory is the limiting factor. I worked a gig where we needed to process YUGE data (150-200 4K stereo sep plates @ 24fps), and the bus bandwidth simply wasn't even close. I had a chance to discuss this very problem with a pair of NVidia research scientists at GPUcon, and they were well aware of this issue in the HPC arena. 'Umm... eh, we're working on inventing an optical bus, yea that's it!' was the simp response.  :^)

# 106
>>3227
that gif is interesting to watch. i can easily see how that could be used in realtime to 'rectify' text under all sorts of affine transforms. Pretty much any kind of details ofc not just text, it's just that regular geometric shapes are easier for me to think about heh. :^)

# 107
>>3230
>>3231
BTW, this is an example of the costly data-transfer statement using a simple Thrust case:
```cpp
// transfer data to the device
thrust::device_vector<int> d_vec = h_vec;```
https://github.com/thrust/thrust#examples

In this trivial example, the delay is nothing (but then again, so is the processing load so it ''may'' be best kept on the host for a given device. as always, PROFILE), but in a practical case this lag can be significant. Like all engineering, this requires analyzing the trade-offs involved and optimizing everything simultaneously towards your specific use-case goals. In our situation ofc, this simply means 'living', breathing robowaifus. No biggie, haha. :^)

# 108
>>3234
Oh, I forgot to point out that in that example, you pay the transfer toll ''twice'', since you also have to transfers the 32-million ints vector back to the host after processing.
```cpp
// transfer data back to host
thrust::copy(d_vec.begin(), d_vec.end(), h_vec.begin());```

Here's the golden code and the whole reason for going to all the trouble in the first place.
```cpp
// sort data on the device (846M keys per second on GeForce GTX 480)
thrust::sort(d_vec.begin(), d_vec.end());```

Note the referenced perf comment is way out of date. Today's nominal GPUs would certainly be able to sort billions of ints a second.

The second example only 'pays the toll' in the upload direction, since the result sum is merely a single int (and normally wouldn't even be transferred back down, but simply used onboard the device).

# 109
>>3231

I need YUGE Sanic memory. With large images I have to augment training data on the GPU while it waits for new data to load. The layers also require a lot of parameters too, channels x height x width x 4. I created this for generating artwork in HD but it's impossible to fit more than a few layers this size into my GPU. It's not going to be feasible with my original idea of hundreds of neighboring pixels spread out exponentially so that any pixel can communicate with any other pixel within a maximum of 10 steps using a minimal amount of connections. Another option though might be to use Fibonnaci spirals or evolve random patterns to find what works best.



On smaller scales though this should be capable of doing some pretty interesting stuff. With 6 neighboring pixels it can communicate in 3D. With 8 it can do 4D. The edges are now wrapped around onto a torus too. The channels also wrap around so they can all communicate. Out of curiosity I'd like to try converting images into 10D cubes, process them in that 10D space, output 10 latent variables, then input them into a 10D network and project it back into 2D to see if it can disentangle high dimensional data better that way.



>>3234

Thanks, this will be really useful when I try to optimize it one day. I need my robowaifu and must Thrust. :^)



>>3236

I had no idea sorting was that fast on the GPU. Damn, I could do some insane Monte Carlo Markov chain stuff with that kind of speed.

# 110
>>3237
>Out of curiosity I'd like to try converting images into 10D cubes, process them in that 10D space, output 10 latent variables, then input them into a 10D network and project it back into 2D to see if it can disentangle high dimensional data better that way.
Now I'm curious, too! :^)

GPU cores are autistic little retards that can only draw using MS-Paint, and further, always insist on spending ''9'001 hours drawing each frame''. But the power-crayons they eat give them super-fastness go powers that compress those hours down to just 42 nanoseconds, our-time heh.

On a different branch altogether, I'm wondering if Flowtron might be usesful to us here on /robowaifu/ anywhere in the nearer-ish-term.
https://arxiv.org/abs/2005.05957
>Abstract
>''In this paper we propose Flowtron: an autoregressive flow-based generative network for textto-speech synthesis with control over speech variation and style transfer. Flowtron borrows insights from IAF and revamps Tacotron in order to provide high-quality and expressive melspectrogram synthesis. Flowtron is optimized by maximizing the likelihood of the training data, which makes training simple and stable. Flowtron learns an invertible mapping of data to a latent space that can be manipulated to control many aspects of speech synthesis (pitch, tone, speech rate, cadence, accent). Our mean opinion scores (MOS) show that Flowtron matches state-of-the-art TTS models in terms of speech quality. In addition, we provide results on control of speech variation, interpolation between samples and style transfer between speakers seen and unseen during training. Code and pretrained models will be made publicly available at https://github.com/NVIDIA/flowtron''

https://news.developer.nvidia.com/flowtron-speech-synthesis-model/

# 111
>>3240

Tacotron sounds better but that might be due to Flowtron trading off parameters to capture more expressiveness at the loss of quality. The paper isn't much use to us right now but one or two papers down the line something amazing might happen.



Expressiveness in voices is hard to capture with machine learning because backpropagation has a huge problem with only converging to an average with very little variance. Flowtron is much better at capturing variance in pitch but I imagine the quality suffers because it's still finding the average for variances not being captured.



This sort of ties in with an experiment I was doing last night to gain a better intuition of why my layers were failing to train quickly. I created a simple problem where it has to compress 4 pixels into 1 pixel and do this 4 times, then reconstruct the original pixels. The answer is obvious it only needs to pick the top-left, top-right, bottom-left, bottom-right and it's solved, but what does backpropagation actually do? It gets stuck on a plateau by choosing the average of all 4 of them. After about 6000 minibatches it finally figures out it only needs to choose one pixel and solves it after 8000. Backpropagation really sucks at disentangling information on its own. There's nothing guiding where the error should flow.



This is a huge problem for the layers I'm creating since they don't rely on a kernel that can focus on picking one specific feature out of some data and ignore other gradients like convolutions do. Once I started stacking my layers this averaging effect became exponentially more difficult to solve. Four layers deep and it made almost no progress in an hour.



To combat this problem I introduced a cost function into the weights of each layer to select at least ''n'' features minimum and minimize the selection of other features without overfitting to the features it has already selected:

```cpp
cost = ((n**0.5-weight.norm(2, feature_dim))**2 + weight.mean(feature_dim)**2```

Which is PyTorch code for taking (the square root of ''n'' - the Euclidean norm across the feature dimension being selected from)^2 + (the mean across the feature dimension)^2



Now instead of taking forever to train I can make the network eight layers deep and it quickly disentangles the features within ten minutes by finding the most meaningful features first and slowly grinding away any connections that aren't necessary while also adapting to changes in the gradient when the feature selection becomes wrong. I haven't tested it yet on other types of neural networks but I think this cost function will be extremely useful in other machine learning applications if someone hasn't discovered this already.

# 112
>>3249
Hmm. Sounds like it's already doing a pretty good job. That would be pretty exciting if you made an original discovery here, Anon! :^)

Idea: What if you took this guy's approach to ''"Multi Head Attention and Position wise Feed Forward Network"'', and used it as a preprocessor to your pruning optimization? Do you think it might help your system even more quickly resolve the important features by having a sort of 'pre-filtered' selection that already satisfies some pre-defined feature selection arbitration?
https://medium.com/@kolloldas/building-the-mighty-transformer-for-sequence-tagging-in-pytorch-part-i-a1815655cd8
https://medium.com/@kolloldas/building-the-mighty-transformer-for-sequence-tagging-in-pytorch-part-ii-c85bf8fd145
https://github.com/kolloldas/torchnlp

I believe this is the original paper (presumably you've already seen)
>'''Attention Is All You Need'''
>The dominant sequence transduction models are based on complex recurrent or convolutional neural networks in an encoder-decoder configuration. The best performing models also connect the encoder and decoder through an attention mechanism. We propose a new simple network architecture, the Transformer, based solely on attention mechanisms, dispensing with recurrence and convolutions entirely. Experiments on two machine translation tasks show these models to be superior in quality while being more parallelizable and requiring significantly less time to train. Our model achieves 28.4 BLEU on the WMT 2014 English-to-German translation task, improving over the existing best results, including ensembles by over 2 BLEU. On the WMT 2014 English-to-French translation task, our model establishes a new single-model state-of-the-art BLEU score of 41.8 after training for 3.5 days on eight GPUs, a small fraction of the training costs of the best models from the literature. We show that the Transformer generalizes well to other tasks by applying it successfully to English constituency parsing both with large and limited training data.

https://arxiv.org/abs/1706.03762

# 113
>>3250
>That would be pretty exciting if you made an original discovery here, Anon!
Assuming someone did do this, how would one even go about determining this?

# 114
>>3251

==Anonymous users solve AI problems puzzling data scientists for decades==

<They're building opensource catgirl meidos and it's terrifying.

Only way to find out is either through an exhaustive search of literature or asking researchers working on similar problems.

# 115
>>3254
kek. we '''need''' this headline anon. keep moving forward!

# 116
>>3250

Yeah, I really like the idea of transformers. They're effective at overcoming this averaging problem. The problem with them though is they're expensive in parameters and compute. Another issue is once you start multiplying things together too much is it cuts off the flow the gradient to deeper parts of the network and they become untrainable due to the vanishing gradient problem. I think there's an important lesson to be learned from the Swish activation function, x·sigmoid(β x), found by automated search that outperforms ReLU:

https://arxiv.org/pdf/1710.05941.pdf



The beauty of Swish is it can bottleneck gradients to part of the network like ReLU, preserving them to reach deeper layers, but also open these bottlenecks back up again and allow the gradient to flow to other areas when necessary, whereas ReLU can't. Similarly once you start using products it creates dead zones in the gradient that are only activated under certain circumstances. It's effective but it seems like a crutch to overcoming the annoyances of gradient descent. It requires exponentially more parameters separated into different attention heads rather than actually compressing information together and distilling knowledge from it. SentenceMIM for example outperforms Nvidia's 8-billion parameter GPT2 model with just 12 million parameters. It's also worthy to note LSTMs used in SentenceMIM use sigmoid and tanh before multiplication which allow gradients to flow and not explode or vanish. So I think the way forward is forming more intelligent gradients rather than cutting it off completely in hope different parts of the network specialize. The neuromodulatory network in ANML that controls the flow of gradients is also interesting and amazing progress in this direction: https://arxiv.org/pdf/2002.09571.pdf



What originally inspired my idea a year ago was dendritic branching. I wanted to capture this hierarchical tree-like structure somehow but working only with 2d images wasn't enough. What fascinates me about these branches now as I started to explore this idea in 3 dimensions is that they only either go left or right like binary search and in a computer we don't have to worry about the limits of spatial reality. We can wrap a 1d space around a circle and in one step reach any point on it. Similarly if you wrap a 2d space around a torus you can reach any point on it in two steps, corresponding to a step in each dimension. We can continue adding more and more dimensions to this torus. A way to mentally picture a hypertorus is to think of the game Portal and opening up 3 yellow portals and 3 blue portals on the 3 pairs of opposite faces of the room.



So if we take a 729x729 greyscale image and reshape it into a 12D hypertorus that still has the same 3^12 features, now every pixel in the image is connected within 12 steps, using only 24 parameters per step or 288 in total for each feature, although so far in my early experiments it seems entirely possible to reuse the same parameters each step but it's more difficult to train and captures far less information. I still have to try it with my cost function in these higher dimensions and see how it helps. Either way, a fully connected layer with 3^12 input features to 3^12 output features would require 1315 GB of memory to compute but on a 12D hypertorus the features can be connected together with at most 2.9GB in a worst case scenario or 243MB reusing the parameters. A 3 channel 2187x2187 image could be processed in 15D with at most 120GB or 8GB reusing parameters which is entirely possible on today's upper end hardware. That includes the memory cost of the calculations and gradients, minus the overhead of whatever machine learning library is being used.



Pytorch isn't really optimized for calculations in such high dimensions and circular wrapping of connections. What I'm working with at the moment requires duplicating the data twice for each dimension and padding each dimension by 1, so instead of requiring 3^dim in memory it requires 3*dim*5^dim which restricts me to using 10 dimensions at most, but if these higher dimensions prove useful for something then I'll certainly write my own code to optimize it. It's really fascinating just being able to watch it process data. Can't wait to start throwing images into wacky dimensions and see what the hell it spits out.

# 117
>>3262
I love the 'torus-wrapping' effect. Surely there's a fundamental & beautiful mystery of the universe hidden away in there somewhere! :^)

I think you can make faster progress for the specific domain of "solving for features of character's behaviors" (if that's a goal) if you fundamentally move your domain of concern away from pixels on the screen, and onto the underlying '''actions''' of the characters themselves. This attention-shift would not only recover much of the information lost by the transformational-chains required for projection onto the 2D coordinates of the screen, but would also make the problem-space far more intuitive to solve at a fundamental level for the humans involved.

For example, take a 3D line positioned between two specific points inside 3D space that you somehow wanted to track the features of in a video. If all you choose to work with at the start is the jagged string of pixels it forms on the screen, then figuring out the accurate positional details of the line, say, requires a fair amount of processing power to 'walk' all those independent pixels all along the way confirming by some means they are in fact part of the line, and then reconstructing them all into a line again with positional information derived as well.

OTOH, if you just abstract the line into two 3D points at the very start---say each one end of the line---and then simply confirm the positions using the underlying pixels, you not only have a more accurate representation positionally but you are also performing far fewer calculations.

To cast things in another light, and if I can put on the animator's hat for a moment, an important tool-class 3D animators use for character animations are so-called ''animation rigs''. These aren't systems that force the animator to literally move every.single.vertex. of the entire character mesh to the desired location 3D space, but rather ''significantly abstract away those mundane details into the mere essentials'', namely 'grab this thing and move it to here at this time-point'.

For example, if at frame 1488 Anon wanted to move a character's hand to that important book to pick up and begin reading in subsequent frames, he would just lasso the rig's hand control icon (usually positioned floating near the particular hand itself) which would target the inverse kinematics control of the rig onto solving for that specific extremity, and then the animator would manipulate the transform control to position the hand at the book itself and set a keyframe. The system would then typically use some variation of LERP linear interpolation to fill in the in-between positions over time. 

Alternatively if he chose to, the animator could instead literally move every single vertex over the same number of frames, but the effort would not only prove far more tedious, but would certainly be more error prone and inaccurate than the smooth interpolation system. While the analogy isn't quite perfect, I think there are some credible similarities here in using just the pixels on the screen to pick out underlying features of the character's behavior. A far more efficient and feature-rich approach in my opinion would be to use pose-estimation on the character first, then use your system on this much smaller set of 'control points'.

This focus on the underlying 'animation-rig' as it were of the characters will greatly simplify the computations involved and also make the process far more intuitive for us humans involved.

>'''3D human pose estimation in video with temporal convolutions and semi-supervised training'''
>''In this work, we demonstrate that 3D poses in video can be effectively estimated with a fully convolutional model based on dilated temporal convolutions over 2D keypoints. We also introduce back-projection, a simple and effective semi-supervised training method that leverages unlabeled video data. We start with predicted 2D keypoints for unlabeled video, then estimate 3D poses and finally back-project to the input 2D keypoints. In the supervised setting, our fully-convolutional model outperforms the previous best result from the literature by 6 mm mean per-joint position error on Human3.6M, corresponding to an error reduction of 11%, and the model also shows significant improvements on HumanEva-I. Moreover, experiments with back-projection show that it comfortably outperforms previous state-of-the-art results in semisupervised settings where labeled data is scarce. Code and models are available at https://github.com/facebookresearch/VideoPose3D''

https://arxiv.org/abs/1811.11742

https://www.invidio.us/playlist?list=PLFt_AvWsXl0fEx02iXR8uhDsVGhmM9Pse

# 118
>I was reading a book by John McPhee and found this quote “Say not ‘This is the truth’ but ‘So it seems to me to be as I now see the things I think I see.’ “ from David Love, one of the world’s greatest field geologists. A bit convoluted, maybe, but it set me thinking. ''I have often wondered how some people could be as certain as they seem to be.''

Bjarne Stroustrup (the inventor of the C++ programming language) makes a strong case for ''intellectual humility'' among his peers regarding proposals in the ISO standard for the language. While an entirely different domain, I think it is helpful to consider the complex challenges they face as a large design and standardization group. Many of the topics are quite pertinent to the design and development of robowaifus as well.

# 119
bumping one of my favorite /robowaifu/ throds.

# 120
>>4611
Okay, yeah it's a great one, but I'm going through it and putting links to it into the other threads anyways. So the thread itself might be used more or less for the leftover or very general questions.

# 121
>>4614
>but I'm going through it and putting links to it into the other threads anyways. 
Cool. That's a good idea Anon, thanks!

# 122
Here a list with all or most common methods to glue (3d printed) plastics together:
Superglue
Acetone
Plumber's Cement
Epoxy
Polyurethane and Silicone Glues
Hot Glue
3D Printing Pen
PLA Hot Glue Gun
Article with descriptions, advantages and disadvantages: https://m.all3dp.com/2/gluing-3d-printed-best-ways-bond-3d-prints/
Please keep in mind that screwing is also an option, best done with threaded inserts:
https://youtu.be/G-UF4tv3Hvc
https://youtu.be/2wRc1KbEAU8
https://youtu.be/iR6OBlSzp7I

# 123
Here's a vid I found which may have some practical application;

https://www.youtube.com/watch?v=bG3rvkpDsdg

# 124
>>4827
>>4831
Neat, I hadn't thought about so many alternative ways to fasten printed parts together before. Thanks Anon.

# 125
Fascinating. Doing so small stuff might be interesting for building some delicate parts, e.g. in the hands.

# 126
>>4827

Are you using ventilation when 3D printing?

# 127
>>4845
What do you mean? I have my window open, though some of those plastics aren't really  dangerous. The others I didn't use so far. When I start with them the printer will be in a box and the air will be filtered and/or be lead outsite. Btw, the pic is symbolic, not from me.

# 128
>>4847
I think he's just worried about your welfare from being exposed to those fumes. You know, know that I think about it, it's probably easy enough to get some of that flexible dryer ducting from a hardware store, lead it over to a window, then put a cheap USB fan at the end near the printer to force fumes outside.

# 129
>>4849
Thanks for your concern. I was planning to do something like that. I'm currently only printing PLA and soon some PETG, which don't release toxic fumes. I think for microdust it's even sufficient to have a little fan nearby which is pulling air through a fleece, or buying a HEPA airfilter, which is in general a good idea.

# 130
Here are 90 facts about the human body, I picked out the most important ones for us: https://www.factretriever.com/body-facts

- In an adult human, 25% of their bones are in the feet
- A human’s little finger contributes over 50% of the hand’s strength
- For an adult human, taking just one step uses up to 200 muscles
- Bone is five times stronger than a steel bar of the same width, but it is brittle and can fracture on impact
- The body can detect taste in .0015 seconds, which is faster than the blink of an eye
- The human brain uses just as much power as a 10-watt light bulb
- An adult’s skin weighs between 8 and 11 pounds (3.6 to 5 kg). It’s surface area is about 18-22 square feet (1.7 to 2 sq. m), which is the size of the floor in a one-person tent
- An adult who weighs 150 pounds / 68kg has a skeleton that weighs about 21 pounds / 10 kg
- The fastest muscles in a human body are the ones that make the eyes blink. They can contract in less than one-hundredth of a second. In just one day, a person may blink their eyes over 11,500 times
- A human eye can distinguish between approximately 10 million different colors
- Your skin is its thickest on your feet (1.4mm) and thinnest on your eyelids (0.2mm)
- The average person has about 250 hairs per eyebrow. Eyebrow hairs have a lifespan of about 4 months

I found this while searching for the weight of a human hand, found 4.5kg for a male arm.

# 131
>>4850
nprb. good ideas about the filtering Anon.

>>4861
>- A human’s little finger contributes over 50% of the hand’s strength
>pic related
I think I understand the claim, but I'm guessing the palm itself (and all the bones, muscles, tendons, etc, behind it) contributes the majority of grip strength for example.

Interesting stuff though, thanks Anon.

# 132
>>4861
>the weight of a human hand
I don't know the answer to that, but I think you can make a sane rough estimate of the upper limit using your own hands Anon. 

Find the volume of a hand by using a big measuring cup and determining how much water is displaced. Then calculate the weight of the displaced water (1 c^3 == 1 g) you can be confident that a hand weighs ''less'' than that simply by dint of containing bones (and the general rough estimate that the body overall is ~70% water by volume).

# 133
>>2754

I think you should avoid the algae growth in water altogether by using 100% antifreeze. I've pulled water pumps from engines and they have had no corrosion whatsover.

# 134
>>5031
Good thought, but the most advanced one should have water inside anyways for salvia, also internal cleaning. Algae aren't necessarily poisonous, my cat drinks water with algae all the time. And they don't grow in places which are flushed and cleaned regularly.

# 135
>>5031
Algae doesn't constitute anywhere near the health threat to humans that antifreeze does--which you shouldn't even allow to ''touch'' your skin. Anon's health and safety are very big considerations for our robowaifu designs.

Perhaps there are 'antifreeze' alternatives however, much like there are alternative, non-toxic oils that can stand in for hydraulic fluids.

# 136
There's a NSFW thread about 3D printed, plastic mannequin-like, ball jointed dolls in the dollforum:
https://dollforum.com/forum/viewtopic.php?f=6&t=69416
Their faces look quite nice sometimes. The looks of the bodies are debatable and partially  questionable, but I could imaging this beeing interesting for placeholder parts, people who want to go for a plastic shell bot (maybe only for the start), prototyping, it also might be interesting to try to put some fiber enforced skin over such joints. Think of leggings, then with some silicone on them.
I think the approach works fine for the legs and the upper body already, not so much for the bottom (pics related), and also only optically. Long term, I'd most likely prefer softer bodies. 
At our current level, this might be good for combining with parts from Elfdroid Sophie here >>4787 and other developments.

# 137
Researchers have found a way to use 3D printers to produce tensegrity structures: 
- A 3D model of the entire tensegrity structure is created, including both rigid and tensional components
- The rigid and tensional components are separated into two different portions of the 3D model
- A third element is added: a single solid block that surrounds all of the other elements
- The tensional components are subtracted from the solid block, leaving voids where the tensional structures should be
- This composite 3D model is then 3D printed on a dual extrusion 3D printer
- The solid block is 3D printed in PVA material, while the rigid elements are 3D printed in standard PLA material
- This results in a solid block of PVA with channels where tensional structures will be, and some loose rigid parts
- A liquid material is poured into the channels, which hardens into an elastic material to become the tensional structures
- The entire block is placed in water, where the PVA dissolves
- This leaves the tensional structures holding the rigid parts in place as designed — and we have the tensegrity
https://www.fabbaloo.com/blog/2020/10/2/how-to-3d-print-tensegrity-structures

# 138
>>5038
Neat, I didn't see this. I want to try casting a silicone ball jointed doll. With some cleverness the ball joints wouldn't need to be screwed into anything. Some ball jointed dolls are just held together by wire or string.

I imagine creating an armature of some sort with a silicone ball jointed doll body and a flexible silicone skin covering the body with two layers of thin plastic in between so they slide smoothly over each other and the skin feels like actual skin moving around when you rub it. Silicone can be very stretchy and slid over the body like a full-body suit, then fused with the head at the neck. The silicone underneath the skin could also be colored red to get a beautiful subsurface scattering glow. And of course electronics could be added into the head and chest for speech and what not.

# 139
>>5457
Sounds great. The visibility of the balljoints is exactly what bothers me with this approach, especially the hips and bottom looks horrendous. I think I'll try to avoid this all together by using a more human like skeleton, but I'm always looking into other peoples approaches and might try them out as well. 
I downloaded some skeleton parts and ball jointed dolls from sites like Thingiverse, and print some of those models for testing. Then I'll start more and more playing with silicone, hopefully I can try out Oogo >>154 and simple silicone molds from caulk at some time soon. Parallel to that, I'll nee to get better at CAD and mesh modelling.

# 140
If one wants to try some approach which includes less 3d printing and more CNC routing and maybe  fiberglass modelling I might have something interesting. Some guy showing how to build a structure out of Polyurethane foam to add plastic to the outside. It might require at least one day working on the CAD files, a small CNC desk router, a big saw, some small handtools, a spray gun, a rotating power tool, a protective suit, and various materials. 
The object he builds is meant to be used as a mold for fiberglass, which might be the way to go. But actually the mold itself could be an inspiration how to build a mecha waifu body, since the outside is polyester. Or it could be used for the torso, and silicone rubber added on top of it. 
They almost lost me, when I saw the dust and protective suit necessary, though. This will require a (cool) garage or workshop. However, since we might apply silicone to the outside of a body build this way, that part might not matter at all... Not sure if any of that makes sense, decide on your own.
Video: https://youtu.be/Cusncs4GaFg
Website: https://www.easycomposites.co.uk/learning/large-composite-patterns-by-hand

# 141
>>5479
Thanks Anon. Having a wide variety of options on the table for robowaifu design, engineering, and construction is always a good idea. Your writing made sense.

# 142
There's a 3d printable system, called OpenLOCK, to lock plastic parts together. The parts need to have a specific hole pattern, then a locking clamp can be inserted to connect them. https://www.thingiverse.com/thing:1833963
This might be usefull for parts which need to be replaced after testing, or for simple connection of parts in general. Of course, we still could use glue or screws at the end while one or several locks hold the parts in place.
The system is normally used to build landscapes and dungeons for role playing games or something like that. There are basic templates  available if you follow the link above. Scroll through the pics to see more or watch the video here: https://youtu.be/iPDWTBgSeH0 
The templates could already be useful in some cases, but I'm more interested in having complex parts being easily connectable. I didn't try to integrate that into a file I designed on my own yet, but here's someone mentioned a method in Prusa  Slic3r which might work for it: https://forum.prusaprinters.org/forum/prusaslicer/feature-request-slice-peg-hole/#post-158311

Here's a spring lock version which I also didn't test yet. I also can't link to it right now, because Thingiverse.com is the worst huge website I know in terms of quality of service and currently I can't open it. Maybe I will later also upload the files here, for the same reason.

# 143
>>5487
That's a great idea Anon, thanks for the info. I had considered even something like K'nex for robowaifu prototyping a few years ago, but this looks like it could be actually effective for real parts.

# 144
>>5487
I watched a documentary once on how they made traditional Japanese buildings with no nails. They came up with a lot of clever shit of how to connect things without nails and do so in a way that was stable even in powerful earthquakes. A robowaifu design that uses no screws would be pretty amazing.

# 145
>>5509
>A robowaifu design that uses no screws would be pretty amazing.
Wow neat idea. That really would be amazing.

# 146
Interesting thread on /toy/.
https://anon.cafe/toy/res/4.html#4

# 147
This site might be usefull for calculating what spring to buy in some use cases: https://www.acxesspring.com/spring-calculator-types.html 
"Learn to design compression, extension, and torsional springs with Spring Creator, our free spring calculator. Here are several types of calculators where the titles are defined by the descriptive content that'll teach you different areas of spring design and help you achieve the best design possible." They seem to have a app as well. For now, I might buy some random set of some hundred springs for 5$ on AliExpress. But that's for the small and cheap ones.

# 148
>>5674
Thanks. Anything like this for elastic cords? I'm working on lightweight arm/hand designs where the compression is being done with fishing line, and I'd like the return to rest pose to be with elastic cords.

# 149
>>5676
Sorry no, my first idea was printing a round piece of TPU, always a bit thicker one, till you get what you want. A spring would probably hold up better throughout time, though.

# 150
>>5680
Thanks, lad.

# 151
>>5895
You can buy lidar sensors for less than $100 but the high-end ones cost over $10K. Having all that data isn't necessarily better though because you still need exponentially more processing power to make it useful. If you want situational awareness, it would be better to think outside human modalities, such as using Wi-Fi to see through walls.
https://www.engineering.com/ElectronicsDesign/ElectronicsDesignArticles/ArticleID/18084/See-Through-the-Walls-Using-Wi-Fi.aspx
https://www.engineering.com/DesignerEdge/DesignerEdgeArticles/ArticleID/17111/AI-System-Can-Watch-You-Through-Walls.aspx

# 152
>>5928
Thanks for the information lad. New one on me.
>''..."but a real commercialization of this device would definitely not begin before defining the policies around how it may be used."
Kek'd. Sure thing, Jack.

# 153
If you ever feel confused trying to figure out wtf a research paper just said or shell-shocked from trying to find gems in a sea of 100 IQ papers, no longer despair. It's now possible to summarize papers and abstracts back into plain English: https://scitldr.apps.allenai.org/

Paper: https://arxiv.org/abs/2004.15011
Code: https://github.com/allenai/scitldr

It's surprisingly good at picking out the most important information. I updated my research sandbox to use its generated tl;dr summaries instead, reducing it from 37k words to 12k: https://gitlab.com/kokubunji/research-sandbox

# 154
>>5942
Awesome. Thanks I'll give it a go.

# 155
>>5942
Discovered this there:
https://allenact.org/

Do you think this is something similar to OpenAI Gym?

# 156
>>5944
Yeah, it looks like an early work in progress specifically for embodied AI experiments. I'm not sure if it has a complex physics engine. It doesn't appear to use Bullet.

# 157
>>5942
Wow, that's certainly a big change in the tl;drs. Do you find it's sufficiently enough information, or does it seem to lose too much?

# 158
>>5967
About 1 in 100 papers it misses the point. Sometimes there's errors every 30 papers or so where it truncates a sentence midway, but other than that it nails it and it's easy to tell when it messes up.

# 159
>>5968
>but other than that it nails it and it's easy to tell when it messes up.
Sounds great. I wonder how it can do such a great job at a task that surely involves a pretty deep understanding of the meaning of technical English words?

# 160
>>5971
People are just bad at writing abstracts and pad them with fluff. It mostly hones in on phrases like "we propose x", "x does y" and such. When it detects jabbering about something unrelated to what the authors did, it cuts it out of the sentence. Also AI is a lot more advanced than people realize. It achieves superhuman performance on some language tasks and outperforms average professionals in translation. The free machine translation people get at Google or Bing is dialed down a few orders of magnitude so the service doesn't bloat their server bills.

# 161
>>5980
>The free machine translation people get at Google or Bing is dialed down a few orders of magnitude so the service doesn't bloat their server bills.
I see. Heh, I hadn't thought of that before, but it makes sense. So what you're really trying tell us is that anime will be real within our lifetimes?

# 162
>>5928
€ 7,75 | laser radar 360 degree laser radar scanning distance measuring sensor diy wireless transmission infrared data transmission
https://a.aliexpress.com/_mLplW5f

It was even cheaper a while ago, but stated very clearly to be experimental. Didn't buy it, since I've already got to much to do and learn, also I don't want to put that into a regular robowaifu. Thought more of using it in some kind of Roomba or Narval-like floor cleaner.

# 163
>>6025
>also I don't want to put that into a regular robowaifu.
I wonder if you can just set of video cameras at different angles in the rooms and then use those to tell your robowaifu where things are located/how they are moving?

# 164
How do we avoid pozzed hardware in our robowaifus?
https://www.youtube.com/watch?v=HNwWQ9zGT-8

RISC-V CPUs?

# 165
>>6338
We have an entire thread dedicated to this topic in general Anon.
>>4506

# 166
I got some ideas for alternative energy sources. Sugar is a cheap source of energy that can be grown and turned into alcohol. How could we build an efficient generator that runs off alcohol? My first idea was to use a Stirling engine. Which gave me an idea it would also be possible to power it with oil. Sunflowers grow abundantly around here and roughly 10 sunflowers make about a litre of oil. With a conversion efficiency of 8% a litre would provide 0.8 kWh. Firewood could also be used if available. This would be pretty basic to set up and low risk. I already have a back-up power system and charging my batteries with something like this would be trivial.

A generator could also be run by collecting rainwater in a tower and using gravity, or using mechanical advantage with a pulley system to lift a heavy object by hand to store its potential energy for turning a generator. A single person can only sustain an output of about 300 watts but it would be a way to store energy indefinitely. In good times a motor could be used to store a ton of energy in case of the sun being blocked out. **It's also possible to run a hose from a stream for microhydro, but that's illegal. :^)**

# 167
>>6420
>A single person can only sustain an output of about 300 watts
Pftt. Plebeians :^)
https://www.youtube.com/watch?v=1SUzcDUERLo

# 168
A Russian guy invented a compressor-free McKibben muscle using high-pressure electrolysis: https://www.youtube.com/watch?v=07oVoABYr10 **The only issue is hydrogen gas is extremely explosive. :^)**

# 169
>>6503
That guy's great, thanks Anon. I hope he becomes the IRL Russian Tony Stark tbh. :^)

# 170
New to this study, so bear with me.
Has anyone experimented with the idea of 'visualization' in general AI? As in, you relate the words and definitions of a sentence to an image(s) to give it more 'understanding'/real world context of the concept itself, to better improve it's conversational abilities. For instance, if you were to say "I ate chicken for breakfast", it would look at all the verbs and nouns of the sentence and then look at the analyzed images of it that are coded to that word, then use the sentence structure of the language to connect those images in sequence. Think of it as the quick mental images you have when you read a book, but much lower-tech.
Thinking with this it'd be good to go with a 'weak but smart' method, only knowing the 5,000 common use English words (at least at first), but developing a deeper, more human understanding of them, and it could be combined with normal NLP or have a custom system made. If this genuinely worked hopefully it could possibly be further developed later on hopefully to the point of creativity. Like creating a kind of artificial simple imagination, if that's even realistic.
Do you think it'd have any kind of real impact on linguistic capabilities or would it just be useless? Is it nothing but fantasy? Is the technology there yet? I'd appreciate any kind of input on the subject, as I'm still learning.

# 171
>>6578
>New to this study, so bear with me.
No worries Anon, just spit out whatever it is you're thinking of. We're a community here.

>Has anyone experimented with the idea of 'visualization' in general AI? As in, you relate the words and definitions of a sentence to an image(s) to give it more 'understanding'/real world context of the concept itself, to better improve it's conversational abilities. For instance, if you were to say "I ate chicken for breakfast", it would look at all the verbs and nouns of the sentence and then look at the analyzed images of it that are coded to that word, then use the sentence structure of the language to connect those images in sequence. Think of it as the quick mental images you have when you read a book, but much lower-tech.
Correlation between words and images has indeed been explored to some degree, both in the 'science' of Psychology, and the science and engineering of AI. And as you point out we all have the common experience of imagery within our imaginations that assists us in performing analogical reasoning--''particularly when encountering something unexpected and new''. So I definitely think you're on to something important there. OpenCV has some good tools for image analysis, and it wouldn't surprise me at all if an association-mapping system could be devised in just a couple thousand lines of compact C++ code using their API.

>Thinking with this it'd be good to go with a 'weak but smart' method, only knowing the 5,000 common use English words (at least at first), but developing a deeper, more human understanding of them, and it could be combined with normal NLP or have a custom system made. If this genuinely worked hopefully it could possibly be further developed later on hopefully to the point of creativity. Like creating a kind of artificial simple imagination, if that's even realistic.
I would argue we could probably get 90% of the way to our goal using just the most common 2'000 words of spoken English usage. Not only would this simplify any given contextual runtime analysis 'in the moment', but it would also greatly reduce the memory and other resource footprints needed for proper functionality. While I believe there are ''some'' things about the human mind irreproducible, I don't think that an imagination of sorts for our robowaifus is at all out of reach for us.

>Do you think it'd have any kind of real impact on linguistic capabilities or would it just be useless? Is it nothing but fantasy? Is the technology there yet? I'd appreciate any kind of input on the subject, as I'm still learning.
I'd expect that a functional, working system such as you're envisioning would indeed have a great impact on AI language generation and comprehension facilities. And I don't consider it fantastic, given our advances in both hardware and software capabilities. While practically all areas of AI that will do the 'heavy-lifting' in our robowaifus will take some clever engineering designs to shoehorn into small, mobile hardware systems, we'll manage it in the end Anon. 

And using creative, imaginative ideas like this is how we'll get there. Never be embarrassed or afraid to leap ahead with your imaginative forces Anon. We all have a great foundation of forebears' minds who have done the same, and they changed the world.

# 172
>>6578
There was a recent paper that combined pictures with word tokens and gained a significant improvement: https://arxiv.org/abs/2010.06775
It doesn't really form a picture or video representation of sentences though. It would be an interesting experiment to try. With a goal-oriented AI you could give it tasks to describe short video clips with a sentence and then also the reverse, generating clips from a sentence, using the same network that is doing chat and what not combined with a video encoder and decoder. Learning from artificial imagination has already been done with world models: https://worldmodels.github.io/

# 173
>>6420
Hi, I already mentioned "Direct Ethanol Fuel Cells" somewhere, probably in the thread for energy systems >>5080 or >>23 ... The output is acidious water and maybe some CO2. Burning oil isn't really interesting, since it would create toxic fumes and noise. Also think of all the moving parts, oil and weight. No thanks. Also, having waifus at home is the first step, and for that we won't need any of that. They can plug themselves in when sitting somewhere, or using wireless charging. 

>>6503
Yeah sure. Whats next, nuclear batteries?

>>6578
We have a thread for chatbots and mind. >>22
I think, what you mentioned could best be done by graph databases and code to manipulate them. Thanks for reminding me, that I still didn't publish my code here, I was working on a while ago... I didn't really forget about it, just don't want to clean it up...

# 174
>>6845
>just don't want to clean it up...
Then just put it here instead. As an R&D board, incomplete solutions are not only expected, but encouraged for quick information sharing and motivation/inspiration. Remember, we need to be quick on our feet here on this board!

# 175
Very interesting. So here's some ideas.



1. You could use Electropermanent magnets or motors and actuators. Found here.



https://8kun.top/hover/res/48.html#q633



2. Motors could be put inside the bones to save space and hide them. Picture the motor inside the bone with a pulley that winds up something like fishing line. The line goes to the end of the bone around a pulley and then comes out in the same place that a normal tendon would attach. Line pulls to make muscle work.

3. There's several idea for origami type actuators in this thread. They could be placed inside the muscle and pulled by the string. This would also multiply the force of the motor pulling the string.

4. I really don't like the idea of pneumatics or hydraulics of any sort. I think in the long run they will cause a huge amount of trouble. Monitoring the force of these things and controlling the valves would be a nightmare. They would also be really noisy. If you going to have all these senor wires monitoring these things better to just go electric in the first place.

5. This idea may really bother some but I think it''s a really good one. No silicon skin. It's sticky and yucky. Why not use fabric? Look at the new artificial silk that they make T-shirts out of. This stuff is super slick, easy to keep clean. I believe some of it fairly stain resistant and doesn't grow bacteria on it easily which would be a good thing to have on a robot waifu. It could washed off in tub. Processor power gets good enough waifu will wash itself. Also we and everyone else will know the waifu is a robot. Instead of trying to make it look like human skin instead try for a human skin feel or even better than human which is much more important. Silicon doesn't come close. The fabric would also be warm to the touch becuse it would reflect your heat when you touched it. The effect could be enhanced by having a space blanket, Mylar coated with aluminum, right under the skin.

6. This brings me to the idea that all the muscles should be fabric and a pliant closed cell foam. Once again washable. The whole waifu could jump in the tub, scrub with a little laundry detergent then get out and dry. Foam origami could be structured like the origami muscles people posted earlier. A soft foam outside with a stiffer foam core that the string tied to a motor in the bone pulls to actuate muscles. Wrap the whole thing in fabric. This in turn is wrapped in a fabric skin made of fake silk. In order to keep it from sagging possibly some sort of Velcro could be used in strategic areas with rubber coating on the rest of the fabric skin and muscle to simulate the fascia that holds skin onto muscle in animals. The rubber would provide friction like the fascia but it would still move.

7. Since this thing is made of foam why not incorporate touch sensation into the foam. Seems I read that if you put carbon black into foam as it is pressed or squished the resistance gets less between the foam.



Anyways this is a great thread and it got me to thinking about things could be done.

# 176
>>84

>"...What about internals? You might have to replace the inner lining of the mouth and uh, other human interface cavities once in a while. I don't have any ideas for those yet, perhaps something that binds when exposed to water, as opposed to the skin thing which would do better if it reacted to air.

How do you refill liquids?...Self-cleaning is important as well, that's another use for water..."



Another good reason to use fake silk fabric for skin. The private parts could be like a pair of shorts with internal pockets for private parts. The stomach skin could be pulled up and the abdominal muscles pushed aside and the internal pocket parts could be connected to a rigid internal keeper in the pelvis. The private parts could be surrounded by foam muscles providing different levels of tightness or even some sort of massage action.



 This also means you could have a hard plastic tube all the way from the mouth to the private parts and by drinking a lot of water wash itself out.



Having a soft fabric skin that can be removed and replaced is huge advantage.

# 177
I need to make it a little more clear. Say you had a pair of shorts  and split them up the sides. This is what I'm talking about but the private parts are built into the shorts. So the shorts are put on, the internal parts hooked up, then the shorts are tied or otherwise joined up on the sides and then the abdominal skin pulled down.

# 178
Another skin idea.



Lycra Fabric?



"...Lycra is a brand name for elastane, which is a highly elastic synthetic fabric. Despite having different names, Lycra, spandex, and elastane are all the same material, and these fabrics can stretch to 5-8 times their usual size...



SO I measured my head and waist and if the only hole was in the head you could stretch, according to this, the whole body over the head. So it would be one continuous piece with a hole in the head that could be covered by hair.  Velcro could hold the fabric on the inside of the lips with the private parts being pockets that are connected as you stretch it up the body.

# 179
>>6845
>I didn't really forget about it, just don't want to clean it up...
Understandable, but in the meantime you're preventing potential inspiration others might get from your intermediate work. I'd recommend instead everyone simply post software as soon as it's reasonably functional, then provide incremental versions like the guy is doing in the C++ thread. Nothing will ever be perfect, software being one of the less likely areas. No one is surprised that things need attention afterwards.

# 180
>>8311
>>8312
>>8313
>>8314
These are some really interesting ideas Anon. Let me think about this for a while.

# 181
>>8311
>motors ... inside the bones to save space 
Yes. But the bones aren't big enough if the fembot is supposed to be as soft as a human.
>Line pulls to make muscle work
Yes, I had similar thoughts. But that's not enough. 
>origami type actuators 
Not sure if that would work (good enough) with motors. I'll look into it, to get an idea what you might have meant.
>don't like the idea of pneumatics or hydraulics
I don't see why this should be more trouble than motors, and why a combination would be bad. Also, there is no way around it, for partially soft robots. Otherwise the soft space can't be used.
>No silicon skin. It's sticky and yucky.
For all I know it depends how it is mixed.
>Mylar coated with aluminum
We'll see. I wan't my waifu to look human-like. Silicon can also be bend very often. It's gonna be a multi-layered skin anyways, if aluminium (foil?) would be good then it could be combined with silicone rubber as well. These fabrics with silver, against EMF make probably more sense. But I think more for sensors, I won't relay on body heat. Heating can come from the inside.
> all the muscles should be fabric and a pliant closed cell foam
Certainly not. You didn't do the dishes per hand in you life very much? Foam brakes down if it has been deformed often, it shrinks and deforms, it also holds bacteria, same for fabric. I think this would be okay for prototyping and cheap bots, though. But then again, rater with silicone rubber on the outside. 

I know about Lycra, Elastan, Spandex and Mylar for years. Had them in mind for exactly that purpose. Quite sure I mentioned that somewhere. It just about putting silicone rubber underneath or not, if not, then why? And why not putting some in between, letting it soak in? Or using the fabric only underneath for stabilization, but having silicone on top. It's futile to speculate about every detail here, just try it out when you have the body. Some details will then have influence on other decisions, in part it's about personal preference, complexity  and price.

>Having a soft fabric skin that can be removed and replaced is huge advantage.
Yes, but it should also not move around unintentionally and it should have a lot of sensors in it, which would need to be connected to the body... Maybe you see the problem. There's more than one way to do it, and it depends.

>>8316
>unfinished software release 
Unless it has bugs, breaks and is rather rudimentary...

# 182
>>8351
Yeah, just some confusion. I was quite sure that these power meshes or silk-like meshes had been mentioned quite often. It seems, not as often as I thought. The search results came from another anon, and where meant as help. My posting has been quoted, so the comment wasn't directed at you. Also, I didn't know you are new. Relax. 

While were at it, I wrote: 
> Foam brakes down if it has been deformed often, it shrinks and deforms,
But didn't think of sofas and pillows, which also have some foam in them, which doesn't deform that much. So it might work somehow. It's just that using foam is also not a new idea, and whenever I hold a used sponge in my hand with that topic in mind, I'm getting skeptical about it. Till I realized that my couch is fine.

>>8352
Why? It's not necessary to delete that  conversation.

# 183
>>8354
>I was quite sure that these power meshes or silk-like meshes had been mentioned quite often. It seems, not as often as I thought. 
There are thousands of posts that hadn't been reposted here from the original board yet. Probably a tedious process. My guess is other posts about this will be in those.

# 184
>>8357
I had the same thought. However, it might be that I only looked at videos on Youtube about such meshes, downloaded them and thought about it. That we dicussed it here or back on 8chan more often, might be wrong memories.
I never saw those as a alternative to silicone rubber, just as an addition. Such meshes would stilll need to be glued o the body or not? Then, how to prevent the silicone glue from soaking into the fabrics or the gaps in between? And what for? It is very flexible and can be washed, though I'm not sure about the details here.

# 185
Anyone having ideas about which bearing should be used in printed drives or in joints? For example, the diameter of stainless steel bearing balls. I was thinking of 2mm.

# 186
>>8364
That one guy's video showed him just using copper-clad BBs in his ball-bearing joint. Seems like a pretty cheap and readily-available supply approach to me Anon.
>>8170

# 187
>>8365
Thanks for the reminder. In another video someone used the balls directly, so I want both, for trying out.  However, I need to stop overthinking such shopping decisions. I simply bought a bunch of different bearings. Though, they're not copper-clad, for all I know. I watched this (commercial) here to get an overview: https://youtu.be/QhTI8CnRic8 - there's quite some variety. I'll have to look into that deeper, to understand when to use wich one, not only in drives but in joints as well.

# 188
>>8368
There are also quite some diagrams to find with image search on "bearing types"

# 189
>>8369
That's a lot of bearings Anon, thanks for the information.

# 190
>Is it possible to delete all my post here?
How about we compromise and just delete the off-topic bits of the conversation, as well as the post that initially triggered your response? Our apologies to you for this misunderstanding Anon. We didn't consider the fact that a search posting in the same thread would create an inadvertent crosslink to your posting. You apparently took this to mean the search results posting was directed at you, which it wasn't. We'll try to keep search postings confined to the ''Library'' thread in the future to help keep this kind of thing to a minimum. Hopefully this clears things up for you. Let's just start over fresh here please.

>>8314
>Lycra, spandex, and elastane are all the same material
Here's a new (and consolidated) waifusearch, Anon:
>>8431

# 191
>>8328
>>8432

# 192
Ok I've been looking around and there's mention of electrically actuated polymers here but it seems that the right term to search for data on it was not used. Although it may be one of those cases where it's rapidly changing. Here someone mentioned research on electically activated polymers



https://alogs.theГунтretort.com/robowaifu/res/94.html#8468



After looking around a little I found this term and a wikipedia page



https://en.wikipedia.org/wiki/Dielectric_elastomers



This is a rapidly changing field. The Columbia university muscles are strong but very slow. Looking at other sources there does seem to be some that are strong and fast. The key point here is this is something that can be readily prototyped. All these motors, gears,  etc. take a great deal of machinery to build but this stuff only takes polymers and electrodes. Way simple to experiment at low cost. I think has one to the best chances of being something done with low resources.



So I found a book on these called "Dielectric Elastomers as Electromechanical Transducers: Fundamentals, Materials, Devices, Models and Applications of an Emerging Electroactive Polymer Technology"



Here's a link to it. Hit one of the three links at the top to download.



http://library.lol/main/6F7F8A9A06ABFA4C830FB7D6D8DB530D



Here's videos.



https://www.youtube.com/watch?v=PDqmGHHKkWw



Really good video



https://www.youtube.com/watch?v=LqOQQsig7og



https://www.therobotreport.com/new-synthetic-muscle-step-forward-soft-robotics/



The key to these things is they are capacitors so all the efforts to raise a standard capacitors capacitance should be strategies to engineer these.

# 193
Dielectric Elastomers can also be used a sensors so the same tech can be used to sense touch.



One bad thing about them is they don;t necessarily pull in so they would have to constrained or engineered to do so. Not sure how yet. Maybe a net of some sort like pneumatic muscles.

# 194
One thing you might could do is use aluminized mylar film or space blankets for electrodes and your polymer in thin films. The the only reason I'm so enamored with space blankets is they are so cheap. Like $2 for a 5' x 6' sheet. Roll the polymer and electrode around a rod. Make sure the roll can slide on the rod. Since the rod keeps it from expanding on the ends lengthwise when activated it will have to bulge like a blown up balloon to expand it's surface. A net around the blown up elastomer muscle will then pull to simulate muscle pull. Kind of screwy but it's a first thought.

# 195
A good page with links to 100 papers on Dielectric elastomers



Open title in new tab then pick one of the links to download.



http://libgen.rs/scimag/?q=Dielectric+elastomers

# 196
Thanks very much Anon. I really, really like the fact you are trying to concentrate on finding inexpensive/low resource methods for design and construction. This will help everyone out, even if they choose to use another approach. Having a wide array of robotics techniques available to us is good.

# 197
>https://www.youtube.com/watch?v=LqOQQsig7og



If you don't watch this second video I linked then you are really missing out. In fact most of the whole entire solution is in that video. Not that the details are there but the foundation is all there.



They are making computing circuits out of Dielectric elastomers. I mean they are making every single one of the elements needed for any computer out of these elements and embedding them "in" the muscles.



What does this mean? By embedding computation you can multiplex instructions to the muscles and not have so many wires. You don't need valves or lots of motors with a huge number of interconnections.



A thought. These elastomers could be printed in big thin sheets with a x-y plot table. With a few steps you could build up layers of logic and most important a lot of redundancy.



They are using carbon for leads. Not so sure that will last. There's links here at this site for liquid metal leads. Might be worth looking in to but they would sure be more expensive but on the other hand if you multiplex the instructions to the muscles might not need that much in the way of leads.



So you print out the muscle in big sheets then you just roll them up. Another idea is to have lines like fishing line under the sheets and print over the lines embedding them. When rolled up you have built in tendons attached throughout the muscle.

# 198
Now this is way the hell out there but it's not nuts. I also wish to emphasize that this is not easy and I'm only describing one path that could be taken that looks like the level of risk for success is likely to be very low.



 There's a thing called VHDL



https://en.wikipedia.org/wiki/VHSIC_Hardware_Description_Language



What it does is if you input a program of the "logic" of a computer in this language and if you have a graphical representation of how the computer chips elements are laid out for each of these "logical units" that is described in this language then the computer can lay out the logic elements to make a die to make the logical elements you have specified. Basically you decide on the computer logic and the software lays out the mask you would need to make it work.



So once you define how these computing elements work in these elastomers then the computer could lay them out. Since we have such a big sheet of material for a muscle the elements could be large to keep the failures low.



Computers could lay out drawing that could be placed over the thin sherets and you could squeegee on the circuits just like silk screen printing. In fact I bet many of the tools used for this could be repurposed.



So all together lay out lines of strong fishing line for tendons, lay a thin sheet of elastomer. Use silk screening to add all the computing elements. Roll up the muscle and attach the fishing line tendons to bones and power.

# 199
Couple mistakes. The risk would seem to be low following this path.



sherets=sheets



Now one further thing. Since elastomers can be sensors, logic or muscle, we put sensors on the outside of our sheets. These senors are connected to the digital and analog converter and computer towards the middle. This also puts the tougher sensor part on the outside and the less tough logic on the inside.



Since you have computing elements and gates you could have every  centimeter a different touch sensor on the outside of the rolled up muscle and multiplex sensing them with the A to D converter. That data in turn sent to the processor to follow whatever logic called for. None of these elements need be super fast compared to humans since we are so slow compared to computers.



Now for the muscles it would be too much trouble to have every single size and length so there's a way we could cheat with only a few sizes. Maybe only three or four. This would save us from having to make too many patterns for the muscles and computing elements in the muscles.



Make the tendon lines very long. An example let's say we have 6 inch space but only have a 2 inch muscle. Just overlap several of them so you would have 3-2" muscles in a line then on top of that in the spaces between the three 2" muscles put two more 2" muscles. The tendon length would determine where they lay and each muscle tendon could be independent with it's own tendon, computer and power giving you great redundancy. In fact multiple muscles per muscle group would seem to be better. Combining them would the simple matter of lining up the muscles in their places and then gluing or clamping the various tendons in place. All of the individual tendons could be programed to act together.



As for power some of these work on low power DC right now.



A far out idea is to use millimeter wave length for  power and communication to the muscles. Wave guides could be a simple metal tube 1mm or 2mm in diameter . The end of the tube could have a circuit to collect the power with a rectifier. The reason I bring this odd idea up is the new 5G is exactly that and they are planning a lot of cheap internet of things chips for these things. Certainly power receivers and transmitters will be part of this. The high end of this is around 300GHZ and at that frequency the size of a wave guide to send it with almost no loss would be 1 millimeter. So a 1mm plastic tube covered in aluminum foil or my favorite cheap thing mylar aluminized heat blankets could send power and could be used to multiplex data to the muscles.



https://www.theunitconverter.com/gigahertz-to-wavelength-in-metres-conversion/300-gigahertz-to-wavelength-in-metres.html



https://www.sciencedirect.com/topics/engineering/millimeter-wave



I also wonder if you could not use some sort of salt water solution in conduits to carry power. This would carry away heat or circulate heat so the whole muscle would be warm like a human while doing double duty carrying electricity.



Once again I'm not saying any of this would be easy and there's a lot of pitfalls that could happen but it does seem that this path would work with a lot of time put into it. If you could get the muscles right the computing power and AI stuff will be ready about the same time in 2025. You could have a fully operation waifu. And none of this would take gazillion dollar production equipment. Most would be repurposing stuff like silk screening, laser printers,, etc. Material cost would not be high. The mental effort would be high but a lot of it would be just making little parts and making sure you understood each little part then tie them together.



I could not find a off hand free design for a microcontroller. The actual computing needs would be small for a muscle so it may be you could just plug away at it until you figure the base elements. You could probably use some of the ideas from RISC-V open source computer but it's 32 bit and probably way to sophisticated for our needs for a muscle controller.

# 200
>>8523
>I could not find a off hand free design for a microcontroller. 
The ''zipcpu'' may be in this computing class. I think it's an open design (not sure if any silicon has been forged yet though) >>4487 . Also, one of our own denizens is apparently working on his own project along this line >>7713 .

# 201
>>8529

>zipcpu



Interesting. The cpu logic will definitely be a problem. People talk about using FPGA I wonder if these could be made in the elastomer and use the same tools? I assume FPGA would waste a lot of performance. It may be that we don't care just to move some muscles around. I'm really not qualified to answer that question.



Basically I just happened to come along some of this stuff and while none of it is easy can you imagine tooling up enough motors or pneumatic vales combined with the mass of wires needed for sensors in a traditional hydraulic or pneumatic design? It would be a nightmare. The tooling involved to make it yourself would be financially crippling. However if you could get one good design for the logic and the muscles then elastomers allow repeating units that can be done in software and it would be likely you could silk screen this stuff like t-shirts. Cost plummets and you could get very elaborate in features as long as you were willing to put in the work to make it happen. Also collaboration could happen because you could get by with a few elastomer logic, sensor and computing elements. All the rest being software. All the work could be parsed out over time in little pieces.

# 202
Since these elastomer muscles could be embedded you could use inch worm type pumps to have a circulatory system.



It also could be that elastomer pumps could be used like mini-hydraulic systems to amplify force. Some of the very strong elastomer motors are real slow and some are real fast. It may be the fast ones lack power(not sure). By using the speed to drive localized pumps you could increase force using the same type muscle all over. Once again we limit cost by reusing the same basic elements over and over.

# 203
This set of programs by DARPA would seem to be relevant. It's a older program not sure how far they got but it's all about automating the hardware if you know the elements involved. It's for silicon but I suppose you could add in the parameters of elastomers and then use the same design tools. They focus on allowing a small group to engineer a large system on chip design with three or four people as compared to hundreds.



https://spectrum.ieee.org/tech-talk/computing/hardware/darpas-planning-a-major-remake-of-us-electronics-pay-attention

# 204
Not sure if we can use that for anything, but it's fascinating: https://youtu.be/LU77kPf25Yg - a expanding pulley. He also mentioned a old book, where he has it from. It's free: https://books.google.es/books?id=MWlRAQAAMAAJ&newbks=0&redir_esc=y (pdf uploaded, epub format not bc server doesn't allo it)
He says it's basically a cam and roller mechanism, which converts rotary motion to linear motion, but a special one. These mechanisms are also interesting by themselves, and its good to know about them.

Also, this window mechanism might be usefull: https://youtu.be/IgZDlnpTFVw - or something similar inspired by it (muscle? rolling it up?)

# 205
>>8728
Interesting book, thanks. I could see this double-wishbone universal joint being useful for transferring rotary motion down a limb across a joint boundary. For example rotating a wrist-joint remotely, across the elbow-joint boundary.
> p26

# 206
>>8728
BTW, I just had a humorous idea from this design notion. If we're going to be able to rotate a wrist via a drive rod in this fashion, who say we have to stop with the rotational limits of the normal human arm?
>eg
>>7719
>Tibia and Fibula

Why can't we have unlimited rotation of the wrist? Just lock the grip off (onto a handle, say) '''and then just start rotating like a slow-turn drill''' (just like in my space movies). Ofc this would only work for fully self-contained hand actuators, but the idea is pretty interesting.

# 207
>>8730
Depends on how human-like she is supposed to be. Won't work with seamless skin.  Also, this would require that one thing I want to try out is going to work: Not using cables to connect the limbs, but creating bones that can run current and always touch each other, but also won't short out. Information would then need to be transmitted via light signals, from limb to limb.

# 208
>>8732
>Won't work with seamless skin.
Agreed. But one thing most of us here seem to approve of generally is not trying to be ''too'' realistic with our robowaifu's designs at this stage. cf, the idea of serviceable 'eye assemblies' that Anons discussed.
>>4355

You can even weave the look aesthetic into the waifu's design itself, kind of like was discussed about Sophie-bot.
>>8392
>''"...maybe a couple robowaifu-aesthetic half cups..."''

# 209
Probably this is known here but I'll link it anyways. Ecoflex silicon gel.



https://www.smooth-on.com/product-line/ecoflex/

# 210
>>8865
Thanks lad, good one. Yes Smooth-On has a yuge number of products of interest to us here on /robowaifu/.

# 211
I found an interesting paper called ReZero: https://arxiv.org/abs/2003.04887

It's a simple addition to any neural network for an easy 50-1200% speed up. It's pretty much just a residual network with the layer output multiplied with a parameter initialized to zero. The real benefit is it allows extremely deep layers of a network to receive strong gradients and train quickly. They had no problem training a 120-layer transformer with it (for comparison GPT2-medium is only 24 and GPT3 is 96) and they also successfully trained a 10,000-FC-layer network. On top of training faster it also outperformed an extremely deep residual network on the validation set.

And there's another benefit to it not mentioned in the paper. Lately I've been researching ways to combine transformers with LSTMs to create a new model that has the expressive power and memory of LSTMs along with the raw computational power of transformers. However, I was stumped because the depth of the transformer model combined with backpropagation through time made the recurrent part effectively useless since the gradients vanish too quickly. ReZero has made my idea possible because it can backpropagate a meaningful error signal through hundreds of layers and time steps. I'm hoping this will be the breakthrough we need to go beyond plus ultra.

# 212
>>8955
Wow, that sounds like it could be amazing. Good luck Anon, we wish you success in this venture!

# 213
Ran across this book.



"Muscles, Reflexes, and Locomotion" by Thomas A. McMahon while looking for another book of his, "On Size and Life" Both deal with the engineering of lifeforms. Might come in handy at some point.



http://library.lol/main/78671AB45EEFF68D8DF12FFF94B08D76



has several links. I find the IPFS ones are usually fast.

# 214
>>8955

>50-1200% speed up



Wow. Think of the performance increase and how with much less computing you could do so much more.



I'm running seriously into the "Dunning-Kruger" effect here because I don't understand neural networks. An analogy. I get the general idea but it's like saying you understand amplifiers but neglect feedback loops and frequency response effects. The details I'm fuzzy on.



I wonder is this speed up in processing data or just training?



Now here's where I mention stuff that may have nothing to do with this and be totally incorrect. Correct me if I'm wrong.



A while ago these guys at  XNOR.ai were getting astounding results from cell phones. They could recognize people. cars. etc. from minuscule processing power. What they were doing was making all values ones or zeros. I wonder if this is somewhat what ReZero is doing in a massively general way. Say you have any 8-bit value and compare it to zero well it might as well be a binary value.  They were bought out by Apple and a huge amount of video and code they had disappeared. Here's a link on them.



https://news.ycombinator.com/item?id=13457463



https://github.com/allenai/XNOR-Net



Maybe this will be helpful.

# 215
>>8955

Another idea that might be helpful. I notice a lot of AI people use python cause it's easier to program. Now there's this language that's sort of like it but also compiles to C, C++ and JavaScript. It might be useful and way faster. It also has many leveled garbage collection built in. So you can get something going with strong control and after you get it working dial in speed. It also has macros like LISP so the code can be modified as it is running and so that the code can be modified faster. Link.



https://nim-lang.org/

# 216
>>8975
>Both deal with the engineering of lifeforms
Sounds fascinating. I'll have a look Anon.
>protip
**you can delete your own posts on /robowaifu/**

# 217
>>8975
>On Size and Life
You may be able to get it here, if you have/make an account there Anon.
https://openlibrary.org/books/OL24861191M/On_size_and_life

# 218
>>8976
>I wonder is this speed up in processing data or just training?
Just training. It helps distribute the error signal across all the layers. Think of the gradient like a pie. Each layer has parameters that determine how to transform its input to a new output. To improve this transformation the parameters must eat some of the gradient. In regular feed forward networks the last layer gets first dibs on the gradient as it passes backwards through the network. Generally it eats about half that pie to update its parameters, then the next layer eats half of that half, and so on, until there are only crumbs left by the tenth.

What ReZero does is force all layers to start with only eating crumbs so the pie becomes properly distributed across all layers in the network where it's returning the best results. Technically it's slower in processing because it's adding an additional multiplication to each layer, but the benefit of this evenly spread out gradient speeds up learning and gets accurate results more quickly with less training steps.

XNOR-Net and binary neural networks are completely different than ReZero. Those speed up computation by reducing 32-bit calculations to 1-bit.

>>8977
NimTorch looks really promising. I'll have to check it out. In theory Python could be fast for most use cases but the way devs create their packages there's so much Python code running everything is slow as molasses. It is possible to convert Python code to C and compile it but it's not much of a speed up because it's still accessing slow packages running Python code, unless you go through the effort of compiling them all and fixing bugs. I'd be grateful if Nim avoids these issues completely.

# 219
>>8992
>What ReZero does is force all layers to start with only eating crumbs so the pie becomes properly distributed across all layers in the network where it's returning the best results.
Wow that's a really helpful explanation/analogy Anon. Makes things much easier to understand what's going on, actually. Thanks!

# 220
So anons. I've begun working on a small companion type robot. It will be about 30-40cm tall and it will optimally use no servos. My plan for joints is brushless motors with encoders and pulleys as gears. I'm currently working on a knee joint and would love to get some pointers from anons more experienced with robotics. I have set a goal for it's mobility, which is to jump off the ground and land. It seems I need to study more physics to calculate the forces required and how much force my motors will create.

# 221
>>9052
I prefer pointing you to the >>catalog and index >>7143, also download waifusearch >>8337 to find stuff in downloaded json archives of the board (some come with it). Ask in the current meta thread for general questions >>8492. Threads with new comments will be automatically on top of the startpage, you do not need to pick ones which are on top already.
If you have something to show for, you might also want to pick a project title. When you have quite some postings with progess, maybe make a new thread with the project name. I post my rather rare updates on prototyping here >>418 - Prototypes and failures.

# 222
I just found this animatronic Glados build and thought someone here might be interested;

https://www.therpf.com/forums/threads/portal-2-animatronic-glados.334522/



https://www.youtube.com/watch?v=WlKHNCdLuwA

# 223
>>9080
Kek. Thanks Anon, that was kind of interesting actually. He's obviously going for theatrics, probably will be humorous to see where he goes with this.

# 224
>>9080
>https://www.therpf.com/forums/threads/portal-2-animatronic-glados.334522/

Lol, I just realized he's using the same actuators as Anon here is for Elfgirl-Sophie.
>

>>7284
>>7575
>>8795

# 225
I found a machine that would let us make circuit boards.

https://www.voltera.io/

I haven't tried it but it does look promising.

# 226
>>9184
Very cool. Do I understand correctly it's like a CNC-printer to lay down circuit traces? What kind of 'print supplies' does it use Anon?

# 227
>>9186
A silverbased conductive paste. I can't seem to find the name. Sorry.

# 228
>>9189
No worries, mate. Thanks for giving us all a heads-up on it. Before now I thought the only way to create hobbyist circuit boards was the old chemical etching way. This seems much more sophisticated, and many of us already have 3D printers too, so there's that.

# 229
Here's an artice on why it's a good idea to use SQLite. Since we want to keep our data in our systems, this is a good reminder. At least for data which isn't supposed to be in a graph database (yet) this is probably the way to go: https://antonz.org/sqlite-is-not-a-toy-database/

>SQLite is the most common DBMS in the world, shipped with all popular operating systems.
SQLite is serverless.
>For developers, SQLite is embedded directly into the app.
>For everyone else, there is a convenient database console (REPL), provided as a single file (sqlite3.exe on Windows, sqlite3 on Linux / macOS).
>The console is a killer SQLite feature for data analysis: more powerful than Excel and more simple than pandas
...

Btw, when will this thread hit the limit?

# 230
>>9265
I had an idea the other day to experiment with text-to-text transformers to see if it's possible for a model to learn to store useful information in text files and search for them later. It'd be really interesting to see if it could also work with a database.

My original idea was just to use text but Plastic Memories shot down that idea fast. I think SQLite could do some pretty powerful stuff like storing blobs of activations for keeping save states.

# 231
>>9265
I've worked with DBMSs a little. Certainly SQLite is very popular choice and for good reasons. I'd suggest that literally the best thing about any DBMS is the ''ACID transaction'' functionality they practically all offer.

Personally -- and very especially during a prototyping phase for a system -- I generally prefer using filesystems and (generally) text files for my 'database'. They are absolutely universal. Even the tiniest microcontrollers have filesystems today. Even some sensors offer it onboard lol. They support simultaneous accesses, can be used for message-passing between processes ('mailboxes'), are very easy to re-compose into alternative (even sym-linked) structures, and are easily human-readable.

This last point is probably one of the most important reasons I favor them over 'real' DBs during prototyping. It's easy to just look at the data itself directly in the files. 

Finally, in my casual experience, file access can run blazing-fast if you take the frontloading time to compose the data ahead of time into standardized memory containers (maps, vectors, sets, etc). While this may be a 'six of one, half-dozen of the other' type argument, when coupled with the other benefits already mentioned I always reach for text files first and only move to a 'real' DBMS once the system has stabilized well, and shows that there are major benefits to doing so.

>Btw, when will this thread hit the limit?
/robowaifu/ 's autosage limit is 350 posts/thread.

# 232
>>9272
>My original idea was just to use text but Plastic Memories shot down that idea fast.
Hmm. I've only watched that series once, so I've probably just forgotten it. Mind explaining why that was Anon?

>I think SQLite could do some pretty powerful stuff like storing blobs of activations for keeping save states.
I would suggest that text files can do the exact same things. As with all engineering designs, its a matter of finding the proper tradeoffs.

# 233
>>9283
>Mind explaining why that was Anon?
She couldn't keep all her memories in her diary. The information bandwidth is too low.

# 234
>>9286
>The information bandwidth is too low.
Ahh, I see now. Well, I can tell you from real-world experience that storing data in text files can be very fast -- arguably faster than basically any DBMS. This is because the computing overhead of writing a stream of chars to the OS is much lower than properly indexing into a (potentially very complex) database schema before being able to do so. The database sequencing could conceivably require 10's of thousands of operations to complete it's write operations successfully. Any computing step costs some kind of resource, usually ''several'' types. 

But practically speaking, spitting a long stream of chars out to the disk is about as close a thing we have to simple 'fire and forget' computing. Today it's practically all done in hardware and requires very little by way of extra CPU or memory resources.

# 235
>>9295
They both have their own strengths and weaknesses. Files are fast but trying to search through thousands of files for a specific bit of information will waste a lot of compute. It's more suited to large read/writes and remembering pages of text. For example, if you wanted your robowaifu to recommend an anime with robots, without a database you'd have to read each anime's file and find which ones have robots. With a database all of that can be indexed and retrieved quickly. For large specific things though a file directory structure makes a lot more sense, perhaps for something like saving and loading different model parameters.

Doing a little bit of reading SQLite claims to be 35%™ faster than the file system for small thumbnails: https://www.sqlite.org/draft/fasterthanfs.html
If this is true it would be good for dumping little memory blobs and retrieving them later. A hidden state is usually only 4KB. I think the best solution in the end will be a hybrid of using both a database and the file system with a mix of text and binary data.

# 236
>>9304
>Files are fast but trying to search through thousands of files for a specific bit of information will waste a lot of compute
You can front-load the process, and then it becomes extremely efficient/fast thereafter. This is the approach I took for ''Waifusearch''. Sub-millisecond responses are commonplace and it's effectively searching the entire 'corpus' of /robowaifu/ -- arguably 100'000's of words.

Don't let me sway you Anon, do just as you see fit ofc. Run your own profile tests. I'm simply pointing out that the fictionalized 'diary' analogy represented in ''Plastic Memories'' doesn't hold true in realworld engineering.

# 237
>>9305
With raw text, yeah, but with machine learning we're not gonna get anywhere near this. A tokenizer can tokenize text at about 1 MB/s and a baseline text-to-text transformer's inference speed is limited to around 30 tokens/s on CPU and 60 tokens/s on the GPU times the batch size. Writing out memories and reading them like that would be very inefficient which is what my original idea was.

I think a way around this could be to do most of the decision making on a smaller network. A simple network model could process about 0.5 MB/s of tensors on my machine, but with data that can be processed in a massive batch then it could potentially max out my HDD speed or even GPU if I had an SSD.

# 238
>>9318
Also I found an amazing feature in PyTorch, torch.from_file, which read and writes tensors directly to files and works extremely fast. It might not actually be a bad idea to load an enormous amount of data and do some feature detection with convolutions to find candidates for whatever data the model is searching for with a heuristic. It's kinda crazy thinking a model could potentially access several TB worth of tensors.

I have an idea now to create a drive-based transformer that can run on embedded systems with very little memory using whatever storage systems are available. I've been playing around and it seems the parameter and gradient tensors can be completely replaced with file tensors with some rewriting of PyTorch's code. This might also enable us to train extremely large models that wouldn't normally fit on the GPU or in RAM so long as we have enough storage space and each layer of the model being calculated fits in memory. I'm not sure exactly how the computation graph in the backwards pass would be handled but with gradient checkpointing I think something can be worked out, loading and saving tensors as they're needed, or modifying PyTorch's file tensors so they can be freed from memory after use and reloaded again without vanishing from the computation graph. Certainly something similar could be implemented with mlpack too.

Which reminded me I was recently reading a paper on switch transformers which splits up a model into several expert networks that specialize in processing different classes of data which are routed to sparsely: https://arxiv.org/abs/2101.03961

It kind of ticked me off they're finding ways to make supermassive models that run on GPU clusters we'll never be able to afford, but actually we can do something similar to this with an SSD on just one computer with file tensors. We could create a 500-billion parameter model with a 1 TB SSD, almost 3x the size of GPT-3 so long as each of those expert networks fits on the GPU. Training each of those would take a really long time but it would be doable, especially with a distributed training group for robowaifus, and the best part is we'd be able to inference this larger than GPT-3 model locally on our own machines. And if my disk-based transformer idea is feasible it might even be possible to have more layers than the original GPT-3 model if it isn't too inefficient going back and forth from disk to GPU.

It won't be easy dealing with the training instability issues that come with sparse models but it's a possibility. Also another issue is that a 100,000 training steps on an expert network would burn through an SSD's lifespan, but I think most HDDs will be fast enough to keep up with training, especially if there's two or more helping.

We may be vastly out powered but if we can surpass GPT-3 we'll have far more powerful robowaifu AI than they ever wanted or dreamed of us having. It's fucking wild we could potentially create an AI model with enough people that runs offline on 1 GPU and rivals GPT-3 that Microsoft paid 1 billion dollars to own.

# 239
>>9318
>I think a way around this could be to do most of the decision making on a smaller network.
Very likely true. Simplification is literally the cornerstone of all performance optimization. Ask any systems software guy:
>Q: '''What's the absolute best code there is?'''
<A: '''Simple. The code that isn't there!'''

# 240
>>9319
That is a wonderful dream Anon. And I definitely like the creative, out-of-the-box way you're thinking about optimizations approaches. Makes me pretty proud of you actually. You're brilliant, actually.

'''However''' just a voice of caution... What you're basically describing AFAICT is a memory paging-system, in effect. As you're probably well aware, while they are highly useful in making more 'memory' available, they are notoriously slow. Perhaps you have an idea that somehow sidesteps the issues there.

Secondly, pretty sure we've had discussions regarding data transport from host => device, and host <= device. The PCI bus ''itself'' becomes the limiting factor, not the GPUs compute capacity (which typically can be quite enormous).

Also, you're correct about the limited operation cycles possible for SSD. RAID 5 or RAID 10 with several mechanical platters is a good possibility (but ofc has disadvantages compared to SSD).

I don't in any way desire to dampen your enthusiasm, and I truly hope you devise a solid breakthrough here that will change.everything. But just stay sober-minded and hard-nosed about the engineering and the underlying physics of everything.

I just hope that somehow, by some miracle, that you can instead deliver something that is at the least GPT-2 medium class ''that can run directly, locally, and __offline__ on RaspberryPis''... first. This is not feasible yet, and leaves basically everyone out in the cold. While your dreams of reaching for the stars is both wonderful and admirable, in the near term it would be far, far more positive for the Anons here on /robowaifu/ if you can achieve this much smaller task for us all first and foremost. And who knows? That simpler problem may actually prove the be the key in the end that lets you unlock the much bigger one!

BTW, did you give some consideration yet to the BOINC system that was focused on ML training? IIRC they already have 1'500 vols running it.

# 241
>>9325
>GPT-2 medium class that can run directly, locally, and offline on RaspberryPis
(Not the anon from >>9319) All serious robowaifus are going to use external servers at home via wifi, in addition to smaller ones inside. That aside, there are stronger SBC and micro-PCs than Raspberry PIs.  Everything that isn't needed for fast responses but involves thinking for a while can be done on external servers at home. This is one of the most important idea to even think of the whole robowaifu project as something feasible. To me having this epiphany was a important point in my life, where I realized that human-like robots would be possible to build if they would stay at home.

# 242
>>9319
>They're finding ways to make supermassive models that run on GPU clusters we'll never be able to afford.

If it takes a supercomputer to run it, then it's lifespan and usefulness will be very limited anyway. Everything is limited by energy (this is why I have some major doubts about cryptocurrency being viable long-term). The way the world is going (8bn+ people all fighting over the same diminishing pool of natural resources), our Robowaifus will need to be Spartan in their energy and maintenance requirements. 

Microsoft can pay their billions and suck up hundreds of gigawatts of electricity all the while lying to themselves and everyone else that it's "sustainable". Physics and geopolitics will shut them down hard, eventually. 

Besides, I don't mind if my Robowaifu is a bit simple so long as she's cute and long-lasting.

# 243
>>9332
>All serious robowaifus are going to use external servers at home via wifi
I sure hope you're wrong Anon. If you aren't, then the utopian robowaifu dream we cherish here is very unlikely ever to occur. Even if it must take that approach ''today'' (fair enough, I'll admit), it can't just stop there if we are ever to succeed ultimately, IMO. Regardless, Anon's and my conversation is primarily in regards to Big Tech/Gov's intentional, conspiratorial, choice to exclude you, me, and ''everyone'' but the 1% from __ever__ managing sophisticated AI out from under their thumbs, respectively.

That is the fundamental issue, and why we need embedded computers to be able to do this successfully. If we dance the tune (((they))) are piping, if we stay in the tiny playpens they intend for us, then it will simply become yet another form of control. You'll only get whatever they choose to dole out to you based on your current and projected social good-goy scores. And quite frankly that outcome will also be surveillance on a scale that Orwell never even dreamed of in that world as well. 

We simply __have__ to target low-end computing as the target hardware or we will fail. We'll never win if we get seduced into playing their game at this. The house always wins.

# 244
>>9333
>The way the world is going (8bn+ people all fighting over the same diminishing pool of natural resources), our Robowaifus will need to be Spartan in their energy and maintenance requirements. 
/throd.

# 245
I'd just say that I think it's definitely possible to run good AI on mobile computers. We just haven't figured out how to -- yet. I'll remind everyone ITT that human brains runs on 12 Watts of power, continuous. That's obviously rather less than gigantic sums of energy being sucked up by big tech attempting this. Their approach is fundamentally wrong, simple as.

# 246
>>9325
Yeah, the hard disk speed will be the greatest limiting factor in this. Some caution needs to be taken not to cause page faults to the system's virtual memory. This can be avoided by maintaining enough free memory and storing parameters as many small tensors rather than big single ones.

I did some tests in PyTorch and the throughput to my GPU is 1.4 GB/s which is no where close to my HDD speed of 100 MB/s. So long as parameter saving/loading remains within hard disk limits, the model can be scaled as much as desired breadth-wise across experts or possibly depth-wise across layers (if I can find a way to unload and reload parameters efficiently during gradient checkpointing without waiting on disk reads.) The entire network doesn't need to be reloaded either. A 500-million parameter model could have 25-million parameters saved and read per second. It will require a new neural network architecture that works like a switch transformer but optimized around the hard disk throughput. To my knowledge this hasn't been explored before, at least publicly, because SotA models are too big and inefficient to utilize the disk in any reasonable manner and if a model isn't pushing SotA on some pre-established benchmark then the paper is either rejected or ignored even if accepted.

Another idea I have is it might be possible to pre-route minibatches so expert networks can do several training steps before being saved to disk while the next ones are being preloaded in. This way models could utilize much larger expert networks that are 1 GB.

Something I've been experimenting with is absolutely gigantic transformers that use parameter sharing like ALBERT. The model I'm working on right now has dozens of layers and a hidden size of 2048 (slightly larger than GPT-2 XL) but the whole model is only 60-million parameters (120 MB) which is slightly smaller than distil GPT2. It would use well over 32 GB of memory if it didn't have factorized embeddings, parameter sharing between layers, gradient checkpointing and some other tricks, but since it does it only needs about 0.8 GB while training with a batch size of 1. Despite using so little memory it's doing a ton of calculations for each layer so a training step takes about 4 seconds, which would be more than enough time to read and write the whole model to disk. According to this paper training large then compressing is also more computationally efficient than training a smaller model: https://arxiv.org/pdf/2002.11794.pdf

And from what I've seen so far I would agree. The convergence speed is stupidly fast using such a large hidden size. I haven't tried compressing it yet but the option is there. It'll take some tinkering around to find what utilizes my compute budget the best and what will result in a good compressed model that can run on lower-end systems fast.

My ideal right now though is to create a language model that can inference in near realtime on a desktop CPU for use in games and other applications. Creating a smaller model that works on a Raspberry Pi is possible but I don't think the quality will be good enough without getting these switch transformers working first. For now someone could finetune a pretrained T5-small model that is only 60M parameters and use 16-bit float precision. If someone has PyTorch working on the Raspberry Pi I'd be happy to help write some scripts to do that.

The lite transformer library I'm working on should be useful for creating models for Raspberry Pis, but they will take several weeks or months to train from scratch. It would be better if the model weights could be loaded and ran in mlpack because PyTorch just hogs up way too much memory. For now the best solution is what >>9332 said. The hard work can be done by a server and sent via wifi, while onboard there could be more simple AI that functions like instincts to make sure the robowaifu doesn't fall over or crash into something. Our robowaifus won't be leaving home anytime soon anyway, even if they could walk, and I can't imagine a Raspberry Pi managing to do speech recognition, speech synthesis and language model inference all together in realtime unless someone comes up with a more efficient model for speech.

And I haven't checked out BOINC yet. Looking into distributed training right now feels a bit like putting the cart before the horse but if you have a link I'll take a quick look and see.

# 247
>>9338
>and if a model isn't pushing SotA on some pre-established benchmark then the paper is either rejected or ignored even if accepted.
Of course. That is one of the several mechanisms of control being utilized by them to keep good AI out of anyone else's hands.

>Despite using so little memory it's doing a ton of calculations for each layer so a training step takes about 4 seconds
Well, it's a far better computing model IMO to keep the data and work units up on the accelerator device itself than to invoke the long chain of physics penalties of data transport back and forth. Trying to keep ''the speed of light'' (or at least the switching speeds of the silicon gates) as the fundamental limiting factor of your algorithms is practically always going to be a net win in the end. ''Solve fast, then get out'' is a good mantra to follow, generally speaking. Certainly from an energy consumption perspective, reduction of moving data 'through the docks' should be a high priority.

>Creating a smaller model that works on a Raspberry Pi is possible but I don't think the quality will be good enough without getting these switch transformers working first. 
Frankly, quality isn't the issue r/n. Existence is. It's far better to have a dry crust of crude brown bread, than literally nothing at all. At the moment, almost all others are starving with nothing in hand whatsoever. And ofc, I'm not suggesting (even remotely) that the ''training'' occur on embedded devices. Simply that the runtime experience does. We should be able to pre-compute these models and then distribute them freely to Anons everywhere.

>It would be better if the model weights could be loaded and ran in mlpack because PyTorch just hogs up way too much memory.
Not to beat a dead horse **well, ''much'' at least :^)**, but Python was always a mistake. We need to go strictly with compiled languages. mlpack is a brilliant choice. Both they and the Armadillo team deserve huge applause for what they are doing that, IMHO, will be the key to allow robowaifus to even become real at all.

And as far as cluster computing at home goes, sure that's fine atm. But it should only be a temporary watershed, not a final destination. The SoC SBCs clustered together ''inside'' our robowaifus will be the approach that works in the end. They will not only do speech recognition, but computer vision, text generation, speech synthesis, kinematics calculations, robotics animation, sensor fusion, agenda planning. The whole package. And they will be able to do everything on just a couple hundred Watts of power as well. This must be our goal here. Anything less will fall short, and ultimately remain only a nerd-niche rather than a groundswell sea-change that can free men everywhere from gynocentrism, abuse and loneliness.

I need to update a new JSON batch for Waifusearch. I'll do so, find the BOINC link for you, and also push the data up to catbox today or tomorrow.

Good work Anon, just keep moving forward.

>===
-''minor prose edit''

# 248
>>9334
I think you misunderstood me. To make it clearer: The servers would be at our homes, just not inside the body of the waifu. I didn't mean servers in some data center. At the beginning this will be necessary, later maybe optional, but better for some tasks. Might be a difference in quality and price as well. The cheapest ones are for people which can't afford an additional computer, others might do that to improve their learning speed and speed of reaction at home. Of course, they should be more and more independent, no disagreement there.

>>9338
Thanks for you ideas, btw. They're amazing, as much as I can tell. Good to see that robowaifu dream attracts smart and creative people.

# 249
>>9346
>they should be more and more independent, no disagreement there.
Agreed, and thanks for clarifying that for me Anon. Yes, this will certainly be a progression of the engineering choices. As you seem to suggest, necessarily crude at first, then advancing to a more usable state with time. Things won't be perfect initially, and that's OK. I'd suggest we should all keep the end goal clear in our minds however. Mobile, autonomous robowaifus are both feasible soon, and are also the only effective robowaifu ideal that will actually change everything for us all.

# 250
>>9343
>And ofc, I'm not suggesting (even remotely) that the training occur on embedded devices.
Maybe not creating pretrained models but it would be good if embedded devices can do a little bit of fine-tuning on models to learn new on the go or optimize themselves.

>We need to go strictly with compiled languages.
I'm gonna make an effort to switch to mlpack by the end of this year and NimTorch for making pretrained models. All the devs working on mlpack and Armadillo have been doing outstanding work. I went to grab the PyTorch 1.8.1 update today and it's 2 GB now. Damn thing was too big when it was 300 MB years ago. It's just getting ridiculous at this point.

Speaking of which, NimTorch might be a good solution for the Raspberry Pi until there are easy-to-use mlpack models available. I'll have to get a Raspberry Pi for myself and try it out.

>The SoC SBCs clustered together inside our robowaifus will be the approach that works in the end.
I don't think it's pipe dream to imagine just one SBC doing everything. AI has already reached a tipping point. There's so much progress being made I can't keep up with it. Sometimes I spend a whole week reading papers and don't make a dent in all the progress. I'm still catching up on ones from 2018. If algorithmic efficiency continues to increase at an exponential pace there might come a day where we can perform all these functions with very little power. If I could go back in time 2 years and tell myself the stuff I'd be doing today, I wouldn't have believed it at all. In 1-2 years we'll probably be doing crazy stuff on SBCs that seemed like fantasy today. So I think it's a more important question to ask how we can make the hardware as energy efficient as possible. The software side has hundreds of thousands of engineers and researchers working on it but robowaifu hardware not so much.

>>9346
It's amazing seeing the devotion robowaifudevs from Japan put into their work. If it wasn't for them I wouldn't work as hard as I do and even then it's only a tenth of what they're putting out. I hope one day there's more communication between Japan and the West. The only way that's gonna happen though is if we create something that gets their attention.

# 251
>>9354
I'm not so much against Python than others here, since it's easy to learn and use, also widely used. However I'm going to look into Nim as well if it is really going to be used here, as soon as I get started to get seriously into ML. Not sure about the importance of the many PyTorch tutorials and repositories out there, I assume this can't really be ignored.

# 252
>>9354
>that pic
kek. just a quick pop-in to give you the crosslink to anon's BOINC posting from before. i should be back later today Anon to continue further.
''mlcathome''
>>9105
>>9106

# 253
>>9356
If you're getting started with ML, PyTorch is the best way to go. Nim is a fairly new language and NimTorch hasn't received any updates in 2 years. It doesn't have full support of PyTorch's features but it compiles straight in C++. I've taken a closer look at it now and by porting some features it should be able to run transformer models. It's missing some things like the cross entropy loss function needed to train them and the Module class. If the missing features are easy to implement in NimTorch I might do that but I feel my efforts would be best spent working on getting PyTorch models working in mlpack.

>>9363
It appears they're using the Torch C++ API. BOINC sends a model file to the client, it runs it, and then reports back with the results and the updated model file. The work that needs to be done to do distributed training on the same model is a lot more complicated than that.
https://gitlab.com/mlcathome/mlds

# 254
>>9354
>tl;dr
I've been tracking down information on both ''NimTorch, ATen,'' and this nifty little tool Anon just brought to our attention, '''aitextgen''' >>9371

I'll make some efforts of the next few weeks to see if a) I can get these up and working on my old RPi 2b, and b) see if I can 'translate' some common PyTorch examples over to it and run them successfully at all this way. 

Also, mlpack and Armadillo seem to be under active development so there's that too.

Yeah, it's amazing to see what you and others here have managed over the past couple of years. I'm feeling quite confident we are going to actually pull this all off before too long.

>>9370
Thanks for taking the time to give it the once over Anon. BOINC is very well-established as a distribution platform by now, but it's certainly not the only way forward. I'm sure we'll eventually work something out. Still planning to go with ''Robowaifu@home'' as the name BTW?

# 255
>>9356
Don't take our bantz too srsbzns Anon, it's just the an ongoing joke. I rather like the language when I actually force myself to sit down to it (I don't often need to). It is very easy to learn, relatively speaking. I'd also just add that yes, you're certainly right about one thing: Python's certainly very ''popular'' >>9036  :^)

# 256
>>9402
Thanks, then NIM isn't really that interesting to me. I'd hope we could do some Lisp (family) instead, Common Lisp, Scheme or Clojure, for those which don't want to work to close to the machine. Even C# has a better image than C++, though never tried either really.

# 257
>>9405
>I'd hope we could do some Lisp (family) instead, Common Lisp, Scheme or Clojure, for those which don't want to work to close to the machine. 
Sure, by all means Anon! Would you mind sort of sharing how you wanted to proceed with your project? I mean do you think you want to work on a physical robowaifu as well, or just stick with the AI side of things for instance?

# 258
Just doing a little simple math.



https://www.tweaktown.com/news/74601/the-worlds-largest-chip-2-6-trillion-transistors-and-850-000-cores/index.html



Nov 3 2020 

Cerebras has just unveiled the world's largest chip, which packs a mind boggling 2.6 trillion transistors and 850,000 cores.

TSMC's new 7nm process to cram the 850,000 cores onto the 2.6 trillion transistors.



If 2.6 trillion transistors on one chip and each artificial silicon neuron has 10,000 transistors then it's equal to 130,000,000 neurons, so you would need 769 chips for a 100 billion neuron brain.(some say 100 billion s a good number of neurons for an average human brain but there is some dispute about this.) So 10 doublings gives us a human at wafer scale. I suspect that you would not need 10,000 transistors for each neuron and that each neuron of this size could simulate a hundred or even a thousand neurons because neurons are so slow.



The figures I've seen show human compatible computation by 2025. So by 5 years after that for the software and we could have a super intelligent robowaifu totally loyal to us and programmed to make us happy.

# 259
>>9407
Pretty mind-boggling ramifications. We better hurry /robowaifu/ !!

# 260
>>9346

"...The servers would be at our homes..."



To lowe cost the waifu could have simple walking and moving around functions embedded. So it could carry stuff, follow you, simple stuff. These functions would take far less computer power than stuff you want to happen at home.

  Higher functions talking, cleaning, cooking, etc. could be run from local home based servers lowering cost until the computing cost and size come down such that they could be embedded.

# 261
>>9448
>until the computing cost and size come down such that they could be embedded.
You're right about that Anon, all else being equal. The computing costs are going to continue to get less relative to their power. In fact, the rate for GPU architectures is still growing faster than exponentially.

# 262
>Planetary roller screws
>highspeed, high stiffness in linear movement
>suitable for frequent changes in direction
>high speed acceleration
>high power density
>high peak load acceptance and reliability
>precise control
This looks like something we should have in mind: https://youtu.be/-JU4Xxwv1TI

# 263
>>9958
Thank you Anon!

# 264
>>9958

>Planetary roller screws



That is excellent. It got me to looking around at links that were related and I found this one on ball screws.



https://en.wikipedia.org/wiki/Ball_screw



Now one of the major design decisions we probably need for DIY manufacture  I think we need is to be able to 3D print as much as we can. It might take a while but we could afford the slower time to do this compared to a traditional manufacturer. So I'm looking at this ball screw link and had an idea. Look at how the balls flow down in a spiral then they have a recirculating track that feeds them back up to the top to start recirculating down the screw track again. Now imagine you have a shuttle that stops the balls and grabs a ball on the way back up. Instead of a rotary motion to feed the balls you have a shuttle that only moves up and down and releases the balls after it's shuttled them up one ball space.



You have a simple solenoid with a coil and a release to drive the balls which would in turn drive the screw. Driving a motor is much more complicated than just feeding power to a mechanism that would shuttle balls faster or slower depending on the voltage. Reverse could be as simple as reversing the voltage. The shuttle would also provide a simple locking clutch automatically that you would not need a separate clutch or logic to hold as you would with a motor.

# 265
>>9984
This sounds like a quite interesting idea Anon. Mind drawing us a sketch or two to highlight your idea here?

Also,
> Driving a motor is much more complicated than just feeding power...
I'm guessing you mean '''isn't'' much more complicated' ?

# 266
>>9984
What?!? I have no idea what this descibes. Is someone testing his text generator? Also, these parts could and probably should be bought as metal parts.

# 267
>>9990
Actually, he's just referring to the idea of using a solenoid-actuated 'shuttle' (kind of like a ''tiny elevator'' if you like) that moves bearing back to the ready-position instead of bearing raceways loaded up with them.

Interesting idea actually. Reducing the number of moving parts has nice benefits, and could conceivably be lighter in weight as well. OTOH, adding in both the solenoid/shuttle system brings it's own issues into the mix.

As with all engineering it's going to be a trade off. I'd recommend this anon try his idea out, and compare it against a standard ballscrew system side-by-side and test.

# 268
>solenoid-actuated 'shuttle' 



I don't deny the idea is a bit of a kludge but I bet you price one of those Planetary roller screws or ball screws made of metal and it would freak you out. The price would be high and we need 650 muscles to make a real looking humanoid.



https://en.wikipedia.org/wiki/List_of_muscles_of_the_human_body



So I found a source for these and they are $32.95USD and no motor. You still have to have a motor.



https://www.banggood.com/SFU1204-400mm-Ball-Screw-With-SFU1204-Single-Ballnut-For-BKBF10-End-Machine-CNC-Parts-p-1091450.html?utm_campaign=BestToolLocker_March&utm_content=2635&p=KR28032004379201507P&cur_warehouse=CN



Here's a video on ball screws



https://www.youtube.com/watch?v=WoPPwGxgWEY



Here's a video on solenoids see at 6:16 how the current pulls the  metal part forward. 



https://www.youtube.com/watch?v=BbmocfETTFo



Now imagine every time the solenoid moves it has one ball trapped and pulls it one ball length. If this is part of the ball screw it would push the screw one ball length. Make sure the solenoid is spring loaded and has cut off switch that is hit every time the solenoid moves one length. So current moves the steel shuttle, moves one ball length, turns the screw, and at full extension after it's moved, ball hits a switch that disconnects the current. Spring moves the switch back and if power still there it repeats with another ball another ball.



Now I fully accept that this is an abortion but...it's damn cheap and uses stuff you can make yourself. If you have a motor they have to have controllers to start, stop, hold them. Let's say you lift a cup with an arm, you need to balance it or it drops it as soon as power taken off. With the shuttle and ball screw the shuttle won't let the balls through so you have a built in clutch.



Some of the 3D printer plastic with added carbon fiber is very strong. Not as steel but make it bigger and the force it can hold is just as good.



It just occurred to me. Maybe the cheapest, and easiest, way to make the solenoid is to instead make an actuator that's like a rail gun,



https://en.wikipedia.org/wiki/Railgun



You only need two conductors and a cross over conductor that will also be your shuttle to shuttle the balls. No winding of coils and you could just slide a couple of copper rails and a copper cross piece into slots made when you 3D print them



The goal of all this is that if you don't have some sort of transmission the current needed will be too much. Hence the ball screw to raise torque.



A lot of what I'm doing is just thinking out loud and gaming what could be cheap and do able without a lot of cash or specialized machinery.

# 269
>>10002
>Now imagine every time the solenoid moves it has one ball trapped and pulls it one ball length. If this is part of the ball screw it would push the screw one ball length. Make sure the solenoid is spring loaded and has cut off switch that is hit every time the solenoid moves one length. So current moves the steel shuttle, moves one ball length, turns the screw, and at full extension after it's moved, ball hits a switch that disconnects the current. Spring moves the switch back and if power still there it repeats with another ball another ball.
/k/ would love you Anon.

Actually, I hope you can test your idea out IRL. Among the many thousands of engineering tradeoffs needed for a working robowaifu prototype ''size'' of actuators is certainly going to be an important one. The reduced volume of your bearing slide is certainly a benefit. I'd also try to come up with further design ideas that reduced the bearing count as well. 

The only way to know for sure is try the idea out directly Anon.

# 270
>>10002
>It just occurred to me. Maybe the cheapest, and easiest, way to make the solenoid is to instead make an actuator that's like a rail gun,
LOL. /k/ would '''really''' love you!

# 271
>>10002
>actuator that's like a rail gun
Something like this was one of my first "genius" ideas to get around well known actuation methods. I put it into the thread for failures and prototypes. Magnetic power is very weak, you won't drag anything with such a little "coil gun" in room temperature. Maybe, letting something rotate along a screw, which is then used to hold something, might work. However, that's basically like a motor. Maybe a slower version of it. 
I had similar thoughts on how to control the eyeballs. Maybe not using a motor with fast rotation, but using some magnetism to let them move and hold in place. I plan to use magnets to guide them anyways, also to transfer power from a motor to the eyeballs, in case I'll use a motor, which is more likely. The advantage of using magnets here would be, that the eyes wouldn't be fixed to some mechanism and the whole mechanism to move them could  be smaller. 

The best use case for solenoids is not to use the pin to push something, but to block something coming from the other direction, which is from the side. So the blocking power would not be related to the power of the magnetic force, but the strength of that pin and the whole construction of the solenoid and where it is attached to.

# 272
>>10030

"Magnetic power is very weak"



I'm sure your right about a rail gun being weak but I do not think magnetic power is particularly weak. Look at the size of Teslas motors for his cars and how much torque these have. We need way, way, way less power.



I did a little looking around and found a paper I had read before but forgot about. It covers "flux  concentrators" for rail guns. 



A quote,"...The device was used at MIT for high field research and also for industrial metal forming. In 1965, Chapman[20] used a flux concentrator with a tapered bore for accelerating milligram metal spheres to hypervelocities. Using a first stage explosive flux compressor, Chapman managed to reach peak fields in excess of 7 megagauss, starting with an initial field of only 40 kilogauss..."



Hmmm...maybe...I get that we don't need hyper velocities but the concentration part helps to raise the force to a small area. This is in turn used to push the balls. The balls and screw guides are in reality a transmission of sorts that allows taking a small fast force and turning into a slower more powerful force.



 Lucky for us humans are very weak,"...During a bicycle race, an elite cyclist can produce close to 400 watts of mechanical power...", that's not a lot. So just walking around you could get away with less than a hundred watts.



https://www.coilgun.info/theorymath/electroguns.htm



"...The best use case for solenoids is not to use the pin to push something, but to block something..."



I get this. Totally understand but if we are going to make something that we can readily hack up in a garage without spending several thousand dollars for brush-less DC servos or some other such pricey stuff we're going to have to do something a bit odd and get creative. It doesn't matter if it's not perfect if it's cheap and easy to prototype.



I really don't like pneumatics or hydraulics. They are very inefficient and super noisy. I think to get something acceptable you will have to make it electric.

# 273
>>10044
I just guess, that there's a reason that motors with moving parts are being used for motion, not just stationary magnets or a coil gun. Feel free to build something that shows what you mean. There're videos on YT where small metal parts move through some winded coil like a train. BTW, if this would be moving fast and strong, then how to prevent accidents of shooting parts outside of the "muscle"?
 >spending ... brush-less DC servos 
The key words here are spending and servos. We just shouldn't do that. I still didn't encounter an argument why measuring the movements couldn't happen outside of the motor. I still think, we don't need these amazing top-noch servos.
>pneumatics or hydraulics. They are very inefficient and super noisy
They are not always noisy at all. I'm sure that depends on factors like speed and power of inflation and deflation. Efficiency? What does it matter, if the tank is loaded while she's plugged in? That part is probably going faster than recharging the batteries.

# 274
>"I just guess, that there's a reason that motors with moving parts are being used for motion, not just stationary magnets or a coil gun."

Most have gears to take the less powerful motor and trade speed of the motor for slower with more torque. The solenoid shuttling balls in the  ball roller screw does the exact same but I'm guessing it would be lot easier to build in a garage.

Also think of the cost of actuators if you have to have copper conductors the whole length of the motion. Expensive.

I'm just throwing out ideas. I do not mind at all if people argue against them. On my part throwing out a lot of ideas means some of them will be stupid but...oh well. Such is the price for progress.

I liked the Planetary roller screws here and was brain storming on how to make something that functioned like this without all the expensive gearing. Those gears must cost a fortune.

I'm actually enamored of this stuff I posted here. Elastomor actuators. This stuff can even have logic computing elements built into it. WOW. Later down the thread I link to book on this stuff. The main problem with it is it doesn't pull it spreads out or pushes so some system would have to translate the motion into a pull. Possibly some sort of undulating motion could be used. Use that motion to make pumps with fluids that could circulate warm water to keep the temperature of the skin warm and provide muscle action.

>===
-''rm g_untd links''

# 275
The links were messed up I referenced here they are again.



Planetary roller screws

>>9958

And I got the name wrong it's Dielectric Elastomers

>>8502

# 276
>>10047
BTW, you should be able to delete your own posts to clean things up a bit Anon.

# 277
It wouldn't let me. Asked for another password???? It appears that it will only let you delete the very last post you made and not the one before it. If you would delete it I would appreciate it.



Sorry for screwing it up. I think I figured out how link correctly now.

# 278
>>10051
No worries, done. It's not based on post recency (AFAICT), but ''is'' based on your IP. Your address probably changed since. Happens with Tor frequently, or with phoneposting from time to time.

>I think I figured out how link correctly now.
It's easy if you just click on the little post number at the end of a post's headline (if you have JS enabled).

BTW, thanks Anon.

# 279
>>10623
Sounds good, done.

>No one needs more work.
No worries it's fine. It's literally in everyone's interest to have things well-organized Anon.

