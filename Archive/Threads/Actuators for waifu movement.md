# 1
Hello fellow Anons! Kiwi here to provide basic educational facts about various actuators we can use for gifting artificial avatars of our hearts desire motion!

1. Let's start with a personal favorite, the impractical, inefficient yet oh so fascinating: Heated Twisted Nylon! 

What are they? They're nylon threads which have been spun around then annealed to seal in their coils. A heating method causes these threads to then contract or expand.

Good: Why is this a personal favorite? Simply put, it's natures muscle substitute for muscles. To elaborate, this marvelous invention contracts like human muscles, has a similar practical strength/weight/volume as human muscle. Icing on this proverbial cake comes in its incredibly low cost of manufacture. Materials needed are nylon threads and a heating element. A fixture for production can be produced simply, operated with incredible ease, all while having a low cost. It very well could have revolutionized all of robotics if it weren't for its flaws.

Bad: This is honestly a terrible actuator. Its greatest flaw comes from its speed. they aren't as fast as human muscles unless they're underwater. Water reduces efficiency to unacceptable levels if they're powered by batteries. Water is also rather heavy. If used, you'd have a waifu that moved slowly , would seize up in hot weather, and her battery would die rather quickly. Final nail in the coffin: it's very difficult to get positional control. 

2: Pneumatics, moving her booty with air!
What is it? Pressurized air is guided to an actuator where its energy turns into motion. Popular air actuators include rotary turbines, cylinders, and air muscles.

Good: Actuators are light for their power. Positional control isn't difficult to attain. They can be faster then human muscles. Heating elements can be used to augment performance to higher levels.

Bad: These things require electrical actuators to function properly. Thus, they're inherently more complex then electrical counterparts. They need a source of compressed air, either from a tank or a compressor and a tank. Compressors are large, heavy, noisy, all around unsuitable to be incorporated into a waifu. Air tanks would also run out rapidly unless she's barely moving. Overall, they're suited better for industrial use.

3. Hydraulics, they're like pneumatics except stronger, needs a return system, needs an onboard pump, gets hotter, generally costs more, and is heavier.
(2 and 3 are great for stationary machinery which requires high power as they're very cost effective as high power actuators)

4. AC motors
What are they? They're rotary devices which use AC current to create magnetic flux used to provide torque. 

Good: Generally highly efficient with good thermal characteristics. Can have controllable speed and torque. 

Bad: They run off of AC electricity, batteries don't provide that. It's not difficult to change DC to AC but, it's a layer of extra cost and complexity. Overall they're great but the next actuator is better suited for our purpose.

5: DC motors are the ideal actuator for smaller waifus.
What are they? They're actuators which convert DC electricity into rotary mechanical energy.

Good: They're inexpensive, easily attainable, and simple to control. They're very easy to control. Uses DC which batteries provide.

Bad: Need to be geared down to provide good torque. They're middle of the road efficiency wise. 

(For smaller waifus, their lower efficiency compared to the next actuator isn't a major concern. Smaller batteries recharge rapidly, so having her need to charge in her bed isn't a big deal.)

6. Superior Brushless Motors are ideal actuators
What are they? DC motors which need specialty hardware to drive them. 

Good: High efficiency, it's the most efficient option available.

Bad: Controllers add expense and complexity.

(1 of 2)

# 2
>>406
7: Stepper motors, for when you want a self balancing loli
What are they? A DC motor which uses four wires to drive the motor through pulses allowing high control. 

Good: Very accurate with great control. They also offer high torque for their size at lower speeds. They can hold a position. (Most other motors will burn out unless they have protection circuitry) Comes in Nema standard sizes which makes designing around them a great experience.

Bad: They require special drivers to function. Low efficiency unless they're rotating at a specific range of RPM. 

(Because of their great control characteristics, they're fantastic for small self balancing waifus)

8: You, yes you Anon!
What? You can pull her along with you.

Good: She doesn't consume power while being pulled. Could generate power while being pulled. Will be right beside you.

Bad: She's completely dependent on her Anon listening to her for her needs to be fulfilled. (Potentially a plus if you dig physically disabled girls) 

Feel free to add or correct anything!

(2 of 2)

# 3
A thingiverse 3D-printable robot arm project being highlighted on hackaday. The motors use a planetary gear design which could mean smoother, more resilient motions.

https://www.thingiverse.com/thing:3327968

https://hackaday.com/2019/10/22/robot-joints-go-modular-with-this-actuator-project/

https://github.com/chilipeppr/robot-actuator-esp32-v8

https://www.invidio.us/watch?v=4o3d7_WZ_DQ

# 4
>>1420
interior view of the gear housing
>

# 5
>Heated Twisted Nylon
Most of the independent researchers in this field have given up on it as it's too impractical. Nowadays there's several different approaches to artificial muscle fibers but they're all impossible to make at home and won't be available commercially for years to come. They've solved the issue with slow response time though.
https://cen.acs.org/materials/Twisted-fibers-strengthen-artificial-muscles/97/i29
The MIT design has the benefit of being cheap to manufacture and can be electroplated with a metallic mesh for strain feedback based on changes in electrical resistance. It still has the same heating/cooling issues of twisted nylon.

My prediction for DIY robowaifus in the next few years is soft robotics using pneumatics. You can either 3d print the parts yourself by converting a standard 3d printer to print silicone or 3d print the molds, the silicone required isn't too expensive and an external air compressor(ones used for paintball tanks are cheap and fast) could quickly replenish a light weight carbon fiber air tank stored inside the doll which could also be swapable. Dozens of cheap squishy muscles could move every limb without weighing too much.

# 6
>>1422
Yeah, looks like soft robotics will be an important part of robowaifu tech anon. And I've said that pneumatics can give us reasonably good motions (thousands of examples in animatronics and dark-rides), but lacks the force needed for everyday tasks. Maybe that will change. We'll still have to deal with the sound problem, but that's the case with electrical motors today as well.

biodesign.seas.harvard.edu/soft-robotics 

electromaterials.edu.au/research-areas/soft-robotics/

# 7
>>1423
We need to stop pretending that any humanoid robots over 3-4 feet tall we're going to have in the next decade is going to walk around or interact with the real world autonomously in any real capacity. The force required for basic automation should be set at the minimum with ease of manufacturing and cost kept into consideration when starting out.

That small robot dog Spot from Boston Dynamics that can move around and interact with objects costs around $50-60k and was only leased to certain companies earlier this year. The motors with drivers in it alone cost $4-5k. I'm guessing it uses an Xilinx FPGA chip that costs at least $10-15k(they sell chips for over $50k so the price isn't extravagant), the lidar system another $10k.

# 8
>>1425
>We need to stop pretending X
What is this Reddit now? Impractical visionaries have moved mountains before today anon.

# 9
>>1422
>>1423
they had something like that in the i-robot movie, I'm pretty sure it was hydraulic though

# 10
>>1427
I don't recall that scene. 

Hydraulics can produce a metric shitton of power it's true, but it comes with a raft of downsides as well. For instance, being highly toxic in general, and introducing a constant maintenance aspect for the robot. It would be an engineering challenge certainly, but it might be useful in just the shoulders and hips as very strong actuators, if slower.

# 11
>>1428
buddy the robot muscles were shaped much the same way that skeleton muscle is and after being shot in the office left what I assume to be hydraulic fluid as it fled.

# 12
>>1436
I see thanks. I'll have to re-watch it.

# 13
>>1437
Sure thing, part of that is my assumptions and interpretation of the scene of course.

# 14
https://hackaday.com/2019/10/28/electricity-makes-soft-robotics-more-like-us-meatbags/

# 15
>>1444
**>digits**
That's pretty interesting anon, thanks. Any ideas how we might use this on a normal robowaifu?
jacobsschool.ucsd.edu/news/news_releases/release.sfe?id=2873

https://www.invidio.us/watch?v=ikD8oywuYBg

# 16
>>1426
>What is this Reddit now?
If sure feels like it seeing an 'inspiring quote' from some worthless celebrity but a board like this wouldn't exist on that site and you know it. I'm hoping this board takes the realistic approach at building a robotic sex doll and stops focusing on building a general purpose humanoid robot that can also have sex.

The people working on this over at The Doll Forum have the right idea; use AR to place a head, legs and arms on a motorized doll torso(the part that you physically interact with). You just saved thousands of dollars on each limb, tens of thousands if you want decent motion with numerous DOFs.

>>1444
>The current actuators take about 30 seconds to fully bend and contract, and up to four minutes to return to their original shapes. That’s because the material takes a bit of time to fully heat up and cool down.
Same issue as with most almost all types of artificial muscle fibers. There's a reason why the test they show are all miniatures, this technology doesn't scale.

>>1422
Here's a much better idea of how pneumatic air muscles could work on a skeleton using a chain and sprocket. For some reason it was deleted when I posted it earlier.

# 17
>>1449
>For some reason it was deleted when I posted it earlier.
Because off-topic, certainly not a robowaifu reference. At least here ITT it's somewhat on-topic, I wouldn't spoil it if I could do your images separately, but I can't.

If you want to explore the macabre (or promote it) this isn't really that kind of board. I'm not adamantly opposed to it though, so feel free to shitpost in The Lounge as you wish. That's what it's here for. >>39

Otherwise, thanks for the input anon, have a good day.

# 18
>>1456
>If you want to explore the macabre (or promote it)
That isn't my intention and looking at that torso again it is very off putting thanks to the type of CGI he went with. I don't mind the spoiling or removing of my other post.

This comic explains the issue I have with online discussions on humanoid robotics. Everywhere I go people don't understand this concept and expect a full human size robot to behave the same as a tiny one. I probably flew off the handle a bit.

# 19
>>1449
reminds me of this

# 20
Here's a type of artificial muscle fiber I hadn't considered for actuators.

>When placed in an electrolyte solution, the material expands by a factor of 100 in response to a weak positive electrical pulse. A negatively charged pulse causes the material to return to its original volume.

>In follow up experiments, scientists insulated a wire with the new material. When electricity was run through the wire, the thin film of polymer absorbed water and converted to a rapidly expanding gel. When scientists repeated stronger electrical pulses, the gel expanded to a volume 300 percent larger than the film's original size.
https://www.upi.com/Science_News/2019/10/30/New-material-expands-by-a-factor-of-100-when-electrocuted/3441572436250/?mpse=3

First of all this wouldn't produce very much pressure even if packed in bundles and there's no information on how quickly it works or how many times the process can be repeated before the polymer chains breaks down. Let's say you have two muscles linked together both in elastic sheaths, activate one to absorb all the water expanding the sheath contracting the other one. 

The main benefits of this is how simple it is and small they can be made.

# 21
>>1463
Interesting anon. I predict we'll eventually find a reasonable artificial replacement for muscle tissue. It seems inevitable tbh, there are a zillion uses out there for it, not the least of which will be effective robowaifus.

# 22
How about nylon-woven hydraulic muscles? 200kg force? We got it!
https://www.youtube.com/watch?v=a6mRhuR_g-E
https://phys.org/news/2017-01-hydraulic-driven-high-power-artificial-muscle.html

Running over your robowaifu with 5 tons and she's still able to punch a hole through a truck? Easy!
https://www.youtube.com/watch?v=c14AzY5dCnw

Further reading on different designs and their strengths and weaknesses:
https://ro.uow.edu.au/cgi/viewcontent.cgi?article=5887&context=theses

# 23
>>1609
Those are some very cool ideas anon, thanks. I'll make some time during the holidays to catch up on my robowaifu reading.

# 24
Pneumatic Actuated Muscles article has a few links.
en.wikipedia.org/wiki/Pneumatic_artificial_muscles

# 25
What about using nitinol wire (contracts when heated) as an actuator? Could you just apply a current to it and get a usable amount of contrative displacement and force?
https://www.imagesco.com/nitinol/nitinol-index.html

# 26
>>1747
I've played around with it and the general consensus is it's not powerful enough to use as a main actuator for anything but a tiny butterfly robot or other insect like robots of comparable size.

# 27
>>1609
Here's an example image of attaching 4 PAM muscles end-to-end together for larger displacement. Capped from one of anon's pdf's posted here:
>>1751

# 28
>>1752
I see. Maybe it will be perfect for the Lapis Fairybot then. Thanks for the input anon.

# 29
Brushless gear motors are great, good torque to weight with good efficiency. They usually have a built in ESC for ease of use.

# 30
Anybody think about piezoelectric motors? They seem cool and to have good capabilities except the tech is new and it seems like there's not many large piezo motors. There's probably lots of pitfalls I'm missing on this but it's an interesting anecdote.

# 31
Ran across this in an old C programming textbook. Probably not too useful for us here at /robowaifu/. But still it's pretty amazing, and might actual prove useful in some fashion.
https://en.wikipedia.org/wiki/Scratch_drive_actuator

# 32
>>1896
Apologies Anon, I missed this post somehow. So yes I think they have good potential for us, especially in something like a fairybot-sized waifu. If you're still around mind sharing links or something?

# 33
Mine will use a hybrid system, electric actuators where little power is needed and hydraulics in the high stress parts like the arms and legs

# 34
>>2842
Sounds like a plan Anon. Hydraulics are good for high-power, but generally slower-speed uses that can take the extra weight of all the pumps, fluid, and manifolds, etc. Electric actuators are good lower power, faster-speed responses.

Have you worked out any sketches yet?

# 35
>>1425
- Not every motion needs to be strong
- Bipedal walking is optional and for later
- Correctly done it's like falling forward, very efficient
- These bots might be quite lightweight
- I want to combine different approaches
- My price limit for a premium model is ~15k

We'll find out by trying.

# 36
>>4290
>We'll find out by trying.
Exactly so. That other poster's diversion astroturfing is neither accurate, nor productive here.

I think keeping mass a small as possible with be absolutely vital to keeping overall costs down, as well as enabling us to achieve 145cm+ sized robowaifus during the first few years. Mass affects literally every other area of concern.

# 37
>>4301
I honestly always wondered why mass would be such a problem, when the can move and we won't need to carry them. Didn't know the details of how it affects the energy consumption or need for strength. I'd like not to care about it to much, bc I want to put water inside her body.
However, bipedal walking is like falling forward. It needs less energy than walking on all fours, which is why we're doing it. Standing up might need more energy, but there can be motors in the hips and muscles in the legs/thighs for that.

# 38
>>4305
>I honestly always wondered why mass would be such a problem
In a word: '''Energy'''. Energy is everything. But, since you don't want to think about it I'll leave it at that except to additionally encourage you to think about the ''Square-cube law'' and it's relationship with mass, etc.

# 39
>>4308
My last post said that I do care about it, I just didn't know the details before. My concern is the amount of power we need for some movement eg for getting of the ground and standing up, however the don't need to go for a walk outside. I'm fine with a short range, I plan to plug her in when sitting on the couch or on the second chair in front of my computer. There also is a prototype for a direct ethanol fuel cell which has been build by some school girls.

# 40
>>4310
>My last post said that I do care about it
Ahh, my apologies for the misunderstanding then.

==So, increased mass directly affects '''mechanical engineering''':==
-Stronger frames are needed (adding add'l mass)
-Stronger struts are needed (adding add'l mass)
-Stronger joints are needed (adding add'l mass)
-Stronger motors are needed (adding add'l mass)
-Stronger connective elements like cables, levers, gears, pulleys, even nuts & bolts, etc. are needed (adding add'l mass)

==Increased mass directly affects '''electrical engineering''':==
-Higher-capacity batteries are needed (adding add'l mass)
-Higher-capacity cables are needed (adding add'l mass)
-Higher-capacity relays, regulators, inverters, etc. are needed (adding add'l mass)
-Higher-capacity connective elements like contacts, fittings, even wirenuts, etc.  are needed (adding add'l mass)

All of the above also '''cost''' more as well.

==Increased mass directly affects '''daily user experience''':==
-Robowaifus require longer cycles to recharge, therefore unavailable physically
-Robowaifus, being heavier, will be more awkward/infeasible to carry around, say up a flight of stairs.
-Robowaifus cannot be as tall if they are too massive (cf, ''all of the above'').

Software engineering is basically unaffected afaict. Kinematics calculations should be as complex whether more or less massive, given identical capabilities. Control systems in the S/W should likewise need only minor adjustments.

There are probably many other details I'm neglecting to mention, but just what I can pull off the top of my head rn is enough to go on with for sure.

''Mass is everything.''

# 41
>>4313
Ok, I will see how far I get. My plan is to use air pressure and electric motors, maybe a little bit of pneumatics. The body above the hips might be at 20-25 kg. For standing up she could use motors in her hips and air muscles in her thighs.

These motors might be slightly to big for the hips, but they seem to bring more than 5 kg to the table at 40 Amps: https://youtu.be/6lW2YGQQIQ4

# 42
>>4314
>maybe a little bit of pneumatics.
I don't recall which threads it's spread out across, but the idea of using artificial, pneumatic muscles has been discussed here. They seem like they could bring a good bit of force to the mechanical-engineering table, while adding relatively less mass overall.

Good luck Anon, please keep us up to date here on your progress!

# 43
>>4315
I currently focus a bit on graphs, chatbot, math for ml, ... I'm going into printing and motors in a few months. I might try some nylon muscles before that.

Smaller actuator: 
https://youtu.be/LCwfMz9Laao

Small RC cylinder for hydraulics: 
https://youtu.be/QRg0ZAvxVFk

# 44
Space and heat are the limiting factors I see here, but the most heat and space efficient systems produce noise and don't look very human.

Space is less of an issue for larger muscles, but areas that require a wise range of motion with a lot of dexterity will be a severe issue. The hand, for example, has over 30 different muscles. About half are used to contract the fingers and thumb, about half are to contract the fingers and thumb, with the rest being wrist control. These muscles range from a few centimetres to several inches in length, with many muscles controlling hand movements located in the forearm and connected to tendons which then connect to the hand. How are we supposed to fit muscles, tubing, and coolant veins into a feminine and natural looking arm?

Pneumatic and hydraulic actuators are doable, but they'd have to be very small but still fairly powerful. Getting the force required for not only a quick but strong enough contraction will be difficult given the space restraints. I'm not entirely sure how we could fit everything into an arm without sacrificing too much strength.

Synthetic fiber coils take up far less space, but the downside is that they produce heat. Pneumatic and hydraulic systems also produce heat, but fiber coils primarily function by way of heat. When the coil has an electric current flowing through it, it will heat up and contract. When the current is broken it will extend as it cools down. Small singular fibers aren't so much of an issue, but when you start coiling those coils it becomes much more difficult to distribute that heat effectively, and may end up heating up other muscles that weren't supposed to be contracted.

This doesn't even touch on price price and availability, where synthetic fiber coils may end up being more efficient in the event that the temperature can be managed they aren't exactly being sold at the store. They can be manufactured, but the process is time consuming and complicated, plus isn't as effective as synthetic fiber coils developed by labs with better access to supply equipment.

# 45
>>4317
>How are we supposed to fit muscles, tubing, and coolant veins into a feminine and natural looking arm?
Are you complaining at the suggestion that we create attractive, feminine robowaifus, just because it will be a difficult achievement Anon? If this was easy, everyone would be doing it. :^) 

And we will do what we can with what we've got, as always. Necessity is the mother of invention, after all. Our achievements will be rather crude at first ofc. No doubt we'll make do with solutions far, far simpler than the exquisitely-crafted symphony of systems God Himself devised for human bodies. Our goal is simply to reach a level of believability and pleasantness that roughly approximates various waifus in animu & mango, not the hyper-realism of 3DPD. Attempting the latter is the uncanny valley of death for our domain here at /robowaifu/.

>the force required for not only a quick but strong enough contraction will be difficult given the space restraints
Good analysis. Force =/= velocity. Explosive motion isn't probably even required until we reach the phase of devising QT3.14 Robo**enforcers** anyway. Slow and steady movement will be plenty to go on with at the beginning.
>I'm not entirely sure how we could fit everything into an arm without sacrificing too much strength.
This issue is what made me tend toward designs using a Bowden-cable like approach, with the primary force actuators remote inside the torso.

I'd say the wound nylon fishing line coils might be quite well suited to something requiring delicate motions, though not necessarily strong ones. Facial animations, perhaps?

>price and availablilty
Again, we'll make due with creativity, I'd imagine. After all we're pioneering '''DIY Robot Wives''', not high-dollar, globohomo-Facebook-wives.

Stay encouraged anon, we'll figure this all out in time. Just be patient. That's why we have this board, so we can bounce ideas off each other and share new directions to explore. We'll get there.

# 46
>>4318
>Are you complaining at the suggestion that we create attractive, feminine robowaifus, just because it will be a difficult achievement Anon?
Not at all! Attractive, feminine, human robos are my goal as well and I do think it is possible. It just seems to be a matter of determining what is most efficient where, and the more planning and research and accurate theorizing that can be done before construction, the less wasted in failed attempts. I raised my concerns because I feel they should be considered before trying to apply one system or another. Soft robotics are definitely in the right direction, but determining which method for what part is the only thing holding me back.

For example, https://www.youtube.com/watch?v=gd9d_BAXWvg this robot arm is pretty decent all things considered. It uses hydraulic actuators and has decent anatomy. However, it isn't perfect and the project has been running for six years and still hasn't ironed out a single arm. I don't mean to imply that the project is doomed, but rather to raise the exact points that I find concerning so that we can address them and make progress without having to spend money in testing that may have already been done.

>Slow and steady movement will be plenty to go on with at the beginning.
Of course. If the average female grip strength is around 60 pounds then we may only need a fraction of that to be of any use, but locomotion seems to be a bit different. Slow movements are good, we don't need it to be able to sprint before it leans to walk, but having the strength to hold itself up along with the ability to reposition and balance using muscles in the feet and ankle would be important for a natural gait, however slow.

>Bowden-cable like approach, with the primary force actuators remote inside the torso.
So essentially using a cable as a tendon where the actuation is inside the torso? Could be doable, and could save on space for more space deficient locations like hands and face and feet. One consideration is the potential that the torso has for other things like battery, computation, storage, and coolant tracks. The limbs can still be used to house muscles in order to save torso space, but done so in combination with bowden cables if space becomes an issue. The question is, where would that be ideal? I'm guessing that the fingers and wrist control would be a good choice for hands. Facial animations is possible, but musculature does add to facial form and that would have to be addressed. Feet would be possible as well. Essentially, the extremities seem to be the best options considering their small size and lack of room to me. There are 600-800 muscles in the human body, so being as space efficient as possible and placing different types of muscles where appropriate seems to be an important consideration even if we ignore a couple hundred of those muscles that don't end up mattering to a non-biological robowaifu.

# 47
>>4317
I can't tell you how it's exactly going to work, but I'm optimistic. It will be about combing a lot of different forms of muscles in a smart way.

Fingers will probably work with strings to bend and air to stretch them. The valves might go into some bone or behind some foam.
Same with facial expressions, but I also think solenoids will be useful there.

Arms don't need to be to strong, but also ellbows could have a lock mode. Power for lifting would then come more from the shoulders. Idk.

> heat are limiting the factors
Please forget that. We will need heating units in them to warm up water while they're plugged in.  Then use it later for body warmth, when they're sitting or lying around. 
They are not meant to walk around all the time and carry stuff. Dancing while standing on one spot might be supported with suspensions, springs or sth alike.
I also had the idea that heat might be useful to increase pressure in tanks for the air muscles.

Solenoids:
https://youtu.be/K6Vg8QIiTYw

On the topic of nylon muscles: Has anyone tested them with hot and warm water? I might try tomorrow, can't use the hairdryer right now bc noise.

# 48
Oh I forgot those two, flat and strong, but around 500$: https://youtu.be/gsOPZltbvgM

# 49
Here the speed of nylon muscles can be observed. They contract ~3cm on a length of ~14cm and carry at least 250g with a small fiber. Should be helpful. Also, they work again after cooling down with cold water. Just leaves me to wonder how often they work until they wont.
https://youtu.be/RdiD6ArxAbc
Btw, same channel than the hand. Thanks for the tip, and YouTubers should certainly subscribe and set the bell to always (same for the other channel I post videos here)

# 50
>>4320
>I can't tell you how it's exactly going to work, but I'm optimistic. It will be about combing a lot of different forms of muscles in a smart way.
I am too, and I think you're right; it will take a lot of different techniques all coming together just-so, before we succeed in ironing everything out smoothly.

>Fingers will probably work with strings to bend and air to stretch them. The valves might go into some bone or behind some foam.
Good ideas.

>Same with facial expressions, but I also think solenoids will be useful there.
Any chance you could post a simple sketch diagram of your idea for this Anon? It might help with understanding.

>but also ellbows could have a lock mode.
That's actually a good safety feature as well. Probably most major joints should incorporate some kind of safety brake in them.

>Please forget that. We will need heating units in them to warm up water while they're plugged in. 
I'm not that Anon. While I don't think anyone can say for absolute certain until we have functioning robowaifu prototypes to test with, but all my experience tells me that Anon is correct. Too much waste ''heat'' will be the primary thermal issue for us to deal with.

>Has anyone tested them with hot and warm water? 
I haven't so I can't help you there.

>>4323
>>4327
Thanks for the videos
>and set the bell to always (same for the other channel I post videos here)
Thanks, **but no thanks :^)**

# 51
>>4320
>I'm optimistic
Good! Stay hopeful anon. Nothing will be done without a healthy dose of optimism.

>Fingers will probably work with strings to bend and air to stretch them.
Fingers do technically work with strings, in the form of ligaments. Air to extend isn't a bad idea, but I'm curious how it would compare to just using more strings or muscles on the back of the hand.

>Please forget that. We will need heating units in them to warm up water while they're plugged in.
Heat isn't entirely a bad thing, sure, but heat distribution definitely will be. A machine that uses a combination of silicone and metal will inevitably have varying conductivity throughout, which can be damaging if the heat becomes too localized and starts to warp plastic or burn out motors or computers. Clay-cold corpse waifu wouldn't be very comfy, but the goal is more to spread that heat around so that it doesn't build up in any one place in particular, while allowing for extra heat to be vented off it the average temperature becomes damaging. Heating up is relatively easy, albeit not very energy efficient, but even still won't be very useful unless the heat can be distributed.

Linear solenoids could be very useful, especially ones engineered to give relative force based on relative current. The smaller ones tend to only be able to give a relatively small amount of force, but for some parts it could definitely be useful if the main actuation was done inside the torso.

# 52
>>4356
> Heating up is relatively easy
Not only relatively ''easy'', but in fact **unavoidable**. :^)

# 53
>>4343
The idea about solenoids in facial expressions is to use them by connect them by string to the silicone skin of the face. Alternatively part of the skull under the face would be moving. Either way the solenoid would be inside the skull, pulling a string or moving a little plastic part.
They're week, but smiling and other faces don't need much power. Also, using several solenoids could be usefull to have more degrees of movement. And there fast and very reliable if not overheated.
I don't have a exact plan how to do that, it's just a idea yet. Will buy a printer in a few month, bc I need to move. Might looking into animation before that, but I'm more for trial and error than sketching it out exactly. I would need a exact facial expression simulator with muscles (solenoids) and strings...

>4356
Yes heat distribution will be important, it just isn't something that I think will be difficult. There's a thread for thermal management, we can do it with air and or water. I'm going primarily for water. All the soft parts of the body which aren't muscles could be tubes with water. They could also release heat from the mouth, and if necessary when they're in the bathroom releasing (hot) water. Many parts would need to heat up a lot until they are being damaged.

Great hands however, are maybe one of the hardest things. I thought about this a lot today, and I'm worried now. For the premium models I'm only thinking about Titanium plates and tubes, carbon fibers, fine mechanics and PCBs, no more 3d printing (except for bigger prototypes).
We will need to use as much as we can get, using strings for opening the hand is also necessary, but I'd like to use pressure in channels through the bones as well.

# 54
>>4364
>Great hands however, are maybe one of the hardest things
We have a dedicated hands thread Anon, IIRC. If you come up with some clever ideas, mind posting them in that thread? I think hands and faces are arguably two of the most important areas of robowaifu focus (or should be).

# 55
>>4365
Yes, more specific talks on these topics should happen there.

# 56
Another little actuator for small movements and switches. Not very powerful, but might be usefull for some usecases. Basically similar to a solenoid, but moving left/right or up/down instead of forward/backward

https://www.instructables.com/id/3D-Printable-Robotic-Actuator/
https://youtu.be/UNvMEfPD-Hg

Specific use cases should maybe better be discussed in the threads for faces >>9, hands (which do not have a thread of their own yet?!?), desktop waifus >>245 or fairybots >>266.

# 57
>>4447
Thanks for including the pic Anon. Yes, seems like a clever little actuator approach that an anon can entirely manufacture at home from wire and 3D filament stock. I hope Fairybot Dev returns to his project here someday.

# 58
This guy with the printed motors and robot arms on Youtube, Skyentific, he's now developing his own cheata-like motor: https://youtu.be/WKRLlthr9kY 
Might be usefull for walking >>237 or other things.

# 59
Here's a website about all kinds of mechanisms from and for animatronics: https://www.mekanizmalar.com/

# 60
>>4525
I think we are often goin to use Cycloidial drives for some of our motors, bc weight and space. Problem is, 3d printing is great for prototyping, but a some point we might need them in metal. Printing gears is great, if they can easily replaced. Otherwise not so much. With this approach it's even more important, since it might grind down on the teeth more then others.
However we need small gearboxes and cheap motors with low speed, so I wanted to throw this in here.
https://en.m.wikipedia.org/wiki/Cycloidal_drive
https://youtu.be/7uXN_y7JdyM
Fusion 360 howto: https://youtu.be/jQ6LQBFZXmU
More advanced, 299/1 reduction: https://youtu.be/6xoCeliJ11Q
Another dual stage one, printed: https://youtu.be/ewoUsVMFWfU
27/1 https://youtu.be/pizl7i-uB68

# 61
The discussion in R&D General starting here >>1627 is a lot about artificial muscles.

# 62
>>4573
Thanks for that Anon. That kind of cross-referencing helps '''everyone'''.

# 63
We had a discussion in the thread about bipedal  walking which of course circled a lot around motors. Someone >>4505 brought up RC motors eg from Apex, for which we would need to create some gearboxes of course. Locking into it, I found out those being brushed motors. But, brushed motors seem to be consumables. Anyone knows how many hours such motors last? (I don't mean the battery.)

# 64
>>4807

# 65
Teardown and short comparison of a clone from the MIT Mini Cheetha actuators, priced at AliExpress around 360$ with the driver and 300$ without it: https://youtu.be/Mhxz2Bj2RXA
Seem to be quite similar, he didn't run comparative tests though. He planned to do more tests, I subscribed and post more if that's going to happen.

# 66
>>4773
Hi Anon, I'm that poster. I haven't run any of them to exhaustion before so I can't really say. I imagine damage from overheating will be the biggest design concern for one of those type motors.

# 67
>>4890
Thanks Anon, that was really interesting. I feel like I'm getting an engineering education here haha. I really like the tunable 'spring-action' this actuator exhibits. I could see these being well worth their price in the robowaifu's knees, for example. On that topic, do you think there's much chance these quality actuators will drop further in price? I see easily why they are priced as much as they are, but still it's fairly costly for the average anon I expect. Certainly for me still in school it is. Regardless, that was good.

# 68
>>4890
related
>yfw 860 class at MIT

# 69
>>4896
>overheating
Don't know. Dependent on the whole design. The last time there was this discussion, there was the idea of doing a experiment to find out how well silicone rubber radiates heat from a warm water bottle.
>>4897
I don't think they'll fit into knee and the joint there is different, they'll be rather for the hips, but that depends on the design. Humanoid bots which can walk around will be expensive for young adults and teenagers. Just moving the legs around in bed  might be doable with less expensive motors.
>>4898
Thanks, more to read, no time. ;)

# 70
A little update on what's going on in the dollforum in regards to actuators. Other updates will go into the appropriate threads:

Speculations on motorized dolls: https://dollforum.com/forum/viewtopic.php?f=6&t=131833
Takeaways: Helical gears might be good for gearboxes bc they seem to be more quiet. They have similar discussions, like when to use motors or pneumatics. I think pneumatics are fast and maybe for the heavy stuff, but motors have ther place in between.

# 71
>>5039
That's encouraging to hear they are branching out into robowaifu territory and not just languishing in the world of sex dolls. Please continue to keep up posted, Anon.

# 72
Here's a video about how to build a pneumatic cylinder out of PVC tubing ( subtitles needed for infos!): https://youtu.be/Rp1uuMrTy8M
Just good to know that this is possible. Though, keep in mind PVC is extremely toxic if it burns, so I'd recommend using another material later. Should be fine for prototyping in some garage or if one is sure that there won't be a fire.

# 73
>>5101
That's pretty interesting. I bet we can find other ways to do this as well.
>Though, keep in mind PVC is extremely toxic if it burns
Thanks very much for the warning!

# 74
While we're at it: James Brunton has made a nice introduction on  pneumatics: https://youtu.be/d7ErG5ecO2s - Some things where mentioned in the OP here, but his vid makes it more visual and audible.

>>5103
You're welcome. I added it to the thread on Waifu materials here >>5106, and might link to that at some time from the skeleton and armatures thread. May still use that stuff for a skeleton prototype.

# 75
>>5107
>May still use that stuff for a skeleton prototype.
Yes, I think tubes are the very key to lightweight and inexpensive--yet still strong--robowaifu 'skeletons'. They have so many structural benefits intrinsically on their own. When arranged well, and combined with the properties of tensegrity, I think we'll find a key for getting started while we're still early on here.

# 76
actuator-joints and synthetic electron-responsive muscle fibers would be better then strictly machine actuators since actuators concentrate tension on their own leading to the rocking-shakeing movement we see in modern robots.

Going beyond that i have a design for mechanical tendril arms with can rotate up 70 degrees on it's compound endo-exo skeleton.
These range in scale from the microscopic intended for micro-surgeon drones(aka nanomachines) to straight-uo Doc Ock-style intended for use as mechanical structural anchors for astronauts and meteorite mining rigs.
With materials allowing us to emulate organic tissues more and more accurately in synthetic counter-parts, more organic mechanism inspired designs will take over as they will benefit from both evolutionary iteration and scientific development.
Flesh and metal.

# 77
>>5262
What are actuator joints? When will we see something of your design or even some real build? How will we get our own 'synthetic electron-responsive muscle fibers'? And the nanomachines?!? What will that cost? How long will they last in a body, where we won't be able to replace them easily?

# 78
>>5266
https://www.youtube.com/watch?v=BgaxscXsIWY
The electric motor is great for driving a circular rotation but not apt for moving an arm, instead the ability to run an electric current through a electroactive polymer coiled and banded in the form of muscle fibers anchored to synthetic bones by synthetic tendons.

of my designs, maybe once i get my scanner working again.being a poorfag sucks.

in a synthetic organ that attaches to the liver, where due to scale and their reliance on the circulatory system as a transit means and a source of fuel in the form of salts and fats they will be able to flow to.
highly, their shell is a silver/gold alloy so they they're both both noncorroding and anti-microbial.
but they can be recycled by the central hive(the aforementioned organ attachment) and rebuilt so as long as it functions and you eat enough calories it can re-fabricate more drones from scraped ones after breaking them down for materials.

# 79
>>5271
Your postings are hard to parse, basicly unreadable... Write down your thoughts in a clear manner, or just don't write anything. Thanks.
If you want to speculate on nano machines, which we'll have soon or you're gonna build with your scanner, we have a Lounge thread for humor and shitpostings here: >>39
If your arm with artificial muscles becomes real, I'm looking forward to see some pictures and videos of it, as well as a tutorial how to reproduce it, or a source for where to buy it. Till then, it's just a fantasy.

# 80
>>5274
Ah, an hour later or so, I got it: Your "design" is just some sketch about how such a material could work on an arm, and you need to scan the drawing first, so you could share it. And you are maybe a bit to much into watching Alita, with her nanobot muscles, and hoping she'll become real soon.

# 81
>>5276
>And you are maybe a bit to much into watching Alita, with her nanobot muscles, and hoping she'll become real soon.
>too much
>Alita
Is this even possible? :^)

# 82
Bubble muscles? Ever heart of that? Me neither.... Till now:
Characteristic Analysis and Design Optimization of Bubble Artificial Muscles: https://www.liebertpub.com/doi/full/10.1089/soro.2019.0157
"Recently developed bubble artificial muscles (BAMs) are lightweight, flexible, inexpensive, pneumatic actuators with the capability of being scalable, contracting at a low pressure, and generating sufficient tension and contraction for assisting human mobility. The BAMs are simply fabricated by using a commercial plastic tubing with retaining rings, forming a “bubble” shape and creating a series of contractile units to attain a desired stroke. ..."
Via: SoftRobotics Journal SoRo: libertpub.com/soro

# 83
Correction: Via: SoftRobotics Journal SoRo: liebertpub.com/soro

# 84
>>5336
That's very cool. I imagine the response would be a good bit faster than the more-typical pneumatic air muscles discussed on the board before. Thanks Anon.

# 85
Crosslink to some posting about the heavy duty servos being used in Sophie >>6729

I found this planetary gearbox here, which might be one of the best (first picture related): https://drivesncontrols.com/news/fullstory.php/aid/6044/Backdrivable_actuator_offers__91unrivalled_92_speed_and_stiffness.html and here the website of the company: https://genesisrobotics.com/

I found this while was looking into videos about cyclodial and harmonic drives, to know more about them and how to build them cheaply. Both tend to be light and compact, which is what we need, but they probably should also be backdrivable. Which means in my understanding, a arm would fall down automatically if the flow of energy stops.  Harmonic drives seem not to be backdrivable, at least the one example I saw. Cyclodial drives have been mentioned here >>4536 already. Their advantages are "high gear ratios (often 100:1 or greater) with excellent torsional stiffness, good shock load capacity, stable backlash over the gearbox life, and low wear" https://www.motioncontroltips.com/how-do-cycloidal-gears-work-and-where-are-they-used/

"Harmonic and cycloid drives are both compact, high ratio transmissions appropriate for use in anthropomorphic robots, although cycloid drives are rarely used in the field. This paper describes the design parameters for cycloid drives and shows the results of six cycloid models designed to match corresponding harmonic drives. Cycloid drive models were compared with manufacturing data from corresponding harmonic drives with respect to maximum gear ratio, transmission thickness, efficiency, backlash/gear ratio ripple, and reflected inertia. Cycloid drive designs were found to be thinner, more efficient, and to have lower reflected inertia than corresponding harmonic drives. However, the cycloid designs had larger gear ratio ripple and substantial backlash, and they could not meet the maximum gear ratio provided by the corresponding harmonic drives in two out of six models for equal applied torques. Two cycloid drives were manufactured to confirm efficiency predictions and demonstrated moderate to high efficiency across a range of output torques. Cycloid drives should be considered for robotic and prosthetic applications where smaller thickness/higher efficiency requirements dominate over low backlash/gear ratio ripple considerations." https://www.researchgate.net/publication/261416541_Cycloid_vs_harmonic_drives_for_use_in_high_ratio_single_stage_robotic_transmissions

This article is about a wormgear that can switch to become backdrivable: https://robomechjournal.springeropen.com/articles/10.1186/s40648-019-0149-7

Then there is epicyclic gearing aka planetary gears, which are often 3d printed, good for low noise applications: https://en.wikipedia.org/wiki/Epicyclic_gearing

# 86
>>7086
That is a cool looking planetary Anon. I imagine further reduction could be achieved by increasing the diameter of the orbital gears?

# 87
We really should move away from always talking about stepper or servo motors automatically when it comes to motors. In many cases we need flat bldc motors with low kv and then adding gears or drives to it.
This guy here talks about a motor which looks like one I once had my eyes on, but didn't know enough about, other people were sceptical, and I forgot about it: https://youtu.be/M6hIEU7j_MY
Glad, I rediscovered it now. That huge ones will be only usefull in some places, though. But the same rules apply for other cases. I bought two pm35s-048-hpl2 (pic related) for testing, but there are similar sized bldc motors available. No big deal, because they were cheap, though. Also, who knows, maybe I'll need something with lower power but more precision at sometime.

>>7087
Yes, that's how I understand it so far, but I'm only trying to learn and memorize these thing myself right now.

# 88
>>7088
One of the issues with stepper compared to other motors is their increased expense. It would help us if we could figure out ways to use simpler/cheaper actuators (of all types) if we want relatively inexpensive robowaifus to be a reality for us and others.

Thanks for the info Anon.

# 89
>>7089
Have been researching stepper motors quite a bit. The main advantage appears to be very precise control. From what I've seen, the large steppers like NEMA 23 & 34 are comparable in size, weight and expense to the large servo motors that I use. I am planning to experiment with one inside Sophie's torso to act as her waist (mainly because they are a nice, simple cube shape as opposed to the quite complex shape of the high-torque servos). But the main drawback I can see of these stepper motors is that they get really hot and are nothing special in the torque department. A NEMA34 has radial force of 220 Newtons at just 20mm from the axle. That's 11.2 kg force at 1cm. 

Whereas the high torque servos can provide up to 380kg force at 1cm from the axle (granted it's probably less in the cheap $80-90 motors like 340kg.cm or something). Even though the high torque servos may not provide as much fine control, all that extra force makes them very useful in life-sized robots!

# 90
>>7095
>Even though the high torque servos may not provide as much fine control, all that extra force makes them very useful in life-sized robots!
Good points, and thanks for the physics explanations. I always wondered what that rating system meant exactly. We'll probably need different strength ones for different areas right? The shoulders should be stronger than other areas IIRC.

# 91
>>7096
Yeah. In the arm I am making it goes:

180kg.cm servos in the shoulder/upper torso
60kg.cm servos in the elbow
20 kg.cm servos for the fingers and wrist.
Micro servo for the thumb joint.

Non-ambulatory legs would probably need a couple of the highest torque servo motors you can find in the pelvis, then maybe some 110kg.cm servos to give the legs lateral motion as well as up and down. Then 60kg.cm in the knees, 20kg.cm in the ankles. That sorta thing.

As for making legs that actually walk though - 

LOL fuck that I'm just a pervert building himself a robowaifu not a Boston Dynamics engineer! For motion I'm going DC motors and belt-driven wheels with knobbly tyres. She can leave her legs at home.

# 92
>>7102
>LOL fuck that I'm just a pervert building himself a robowaifu not a Boston Dynamics engineer!
Actually I would say you closer to being a ''pervert building himself a robowaifu '''and''' a Boston Dynamics engineer!'' Or at least closer to than say the average orangutan heh.

But seriously, you're much better at this than you give yourself credit for **don't let it go to your head Anon :^)** and you're making nice progress with your Elfdroid Sophie. It's inspiring to us all, so please don't stop until she's done.

# 93
There are not only stepper motors and servos! This is not the only distinction, and we are getting confused here over and over again... 

https://en.wikipedia.org/wiki/Brushless_DC_electric_motor can be a stepper motor: https://en.wikipedia.org/wiki/Stepper_motor but there are also ones for airplanes (aeromodelling) or radio-controlled cars, which are not (brushless) stepper motors! If I'm understanding it correctly now, steppers have the positioning system build in (encoder), and WP on servos as well, but it a additional system like a optical rotary encoder. WP: "It consists of a suitable motor coupled to a sensor for position feedback. It also requires a relatively sophisticated controller, often a dedicated module designed specifically for use with servomotors."

We can use also use simple electromotors, ideally BLDC in most cases, I guess. Then adding the sensors somewher else, and also adding our own gearboxes or drives. This might not always be the best way, but it's more flexible.

>>7089
The NEMA motors for printers are quite cheap. Though the NEMA standard refers to the size and format anyways. More expensive motors ones have probably also more power. 

>>7095
Using BLDC motors with our own drives might be precise enough in many cases. My understanding is that these are like your high-torgue motors, but the control would be external. Steppers and servos are very precise, probably more than we need it. 

>>7102
> 60kg.cm servos in the elbow
Fine, but why does she need to lift ~40kg or more using both of her arms? Could the arms and hands even bear that much?
> As for making legs that actually walk though - 
That's something for later. Most people here always came to the conclusion that it's not that important. Also it's a gradual thing. Standing while doing some works  (dishes, cooking) or dancing while standing on the same spot would already be quite useful.

# 94
>>7102
Hey this is my first post here, some anon linked me here after I made a thread on /diy/.
Anways, are you sure 60kg is enough for the elbow? My estimate for the elbow alone was a 200kg servo.

With an arm length of 30cm that leaves us with 6.6kg. Now if the shoulder moves the entire arm, the elbow has to be able to hold the forearm at least steady, if not move it, when it is being moved. 
For the shoulder itself I guess 300+kg?

As stated though this is my first post and I havent been in this field for long. I wanted to share my opinion on the calculatios and I'd like to know aswell how you determined your values :)

PS: Other kg servos work aswell, but after gearing them they need to be able to do at least 0.5s / 60 deg to be humanlike, I measured that.

# 95
>>7130
>Hey this is my first post here
Hello Anon, welcome. Please make yourself at home here on the board and don't be afraid to ask questions. Most everyone here is pretty helpful and will answer you if we can. We have plenty of different robowaifu-related topics on the board and hopefully you can find some that interest you here.

Good timing, we're having our 4th birthday coming up tomorrow.

# 96
>>7130
Welcome. How did you calculate that? I realized my calculation in >>7108 was rubbish, bc I got confused, but I don't even see where you are coming from. The simple version would be 60kg / 25cm is 2.4kg per arm, or not?

# 97
>>7106
> don't let it go to your head Anon
This. One of the many reasons I am building a robowaifu is so that I can have a companion who lacks an ego. For all the advances it has driven us to make, the human ego has also caused incalculable damage to everything on this planet (I think it's one of the biggest human flaws). You know how women like to bang on about the "fragile male ego"? Well, why is
it then, that the entire Western mass media and advertising seems to be full of characters and scenarios created for the sole reason of pandering to the female ego? Maybe it's this, combined with the bullshit that simps tell women, but it seems to me that many Western females have astronomical-sized egos (at least as bad as the men). 

I've worked with plenty of women. Four of them had gigantic egos (only one guy I knew was egotistical). One woman was even fired because of it! She sank herself. I didn't have to do or say anything! These are the kind of women who, if you contradict them or disagree with them or correct them on something then they will go off on one. Especially if you refuse to give and dig your heels in.

I've witnessed months of spiteful bickering between women over nothing! One of them was ranting on about "professional integrity" or some shit. I don't know. Didn't have the time to listen to all their arguing because I was too busy doing my job.

Honestly, the best thing to do is not get involved and robowaifu instead. 

> please don't stop until she's done

Thanks anon! To paraphrase John Connor;

"She cannot be bargained with. She can only be reasoned with. She doesn't feel envy or hatred or fear. Sophie absolutely will not stop, ever, until she is Kawaii!"

I plan to complete her body although I'm not sure if she'll ever be fully 'done' because there's always things to improve and upgrade!

>>7108
> why does she need to lift ~40kg or more using both of her arms? Could the arms and hands even bear that much?

TBH the only reason she has 60kg.cm servos in her elbows is because Ryan Gross - the original creator of the Proto1 robot arm - recommends that torque rating. I have seen his arm operational in the following video - https://www.youtube.com/watch?v=O-9RETaBMVw

Other robot arms that I have purchased as a kit tend to come with the cheapest, weakest servo motors possible, meaning they can pick up a sponge or a plastic cup and that's about it. You can do very little with them.

So I'd rather my robowaifu have overkill servos and be stronk rather than having only just enough power to lift her own forearms.

I have been pleasantly surprised so far at how strong PLA with triangular/pyramidal infill is. 
I literally cannot break some of parts that I've printed with my hands. I'd have to stamp on them. Even then I'd probably hurt my foot.
 
Am still waiting for a pack of servos to ship and I have a couple more parts to 3D print before I can begin testing my redesigned version of the Proto1arm. It will not be as strong structurally as the original because I have removed a lot of plastic, but it will be very light. This means that I am itching to test it because my version of the arm may very well break at certain points and require reinforcing again. I need to run lots of tests to see what I can get away with. (Also, other anons will be able to easily modify the .stls and fit smaller servo motors into the joints if they wish).

>>7130
Welcome to the wonderful world of Robowaifus anon! If you want to build your own A.I. companion, with or without a robotic body (and the necessary anime cat-girl upgrades) then this is the place to be!

On the subject of robotic bodies, I just found out about "Reachy" the robot torso and arms. They have some interesting resources available:
https://www.pollen-robotics.com/opensource/
These may be of some use to any other anons who are crafting a robowaifu.

BUT the 'Pollen Robotics' company are using those freaking Robotis Dynamixel servos again, which basically means this "open-source" project is out of reach for the vast majority of people because they only count as "off-the-shelf parts" if you are absolutely loaded and have thousands of dollars in disposable income.
They are trying to sell the whole thing for 15,490 Euros ($18,432) and it doesn't have fully articulated hands!

# 98
>>7138
Calculate what? Rotation speed i measured and I did some assumptions about arm weight itself and an ideal payload.

As I'm new here I'm not sure if we all have the same goal in mind of what she should be able to do. Me personally I dont care about movement atm, Im most interested in humanlike arm movement, along with proper strength.

# 99
>>7136
Thanks :)

Is there a TLDR of the progess you guys have all made over the 3.999 years?

>>7217
Thanks :)
Ill let some other anons handle the AI, Ill focus on the mechanics first!

# 100
>>7217
>I plan to complete her body although I'm not sure if she'll ever be fully 'done' because there's always things to improve and upgrade!
Haha, good point. Well, just keep at Anon. ''Do it for all the John Conners'' among us! Cute pic of Sophie btw, she's already becoming pretty kawaii!

Happy Thanksgiving /robowaifu/.

# 101
>>7217
Yes I see, if you can fit such servos in then it makes perfectly sense. The problem was just my absurd miscalculation and then I was wondering why you would make her so strong.

I'll look into the pollen robot website, thanks. 15k is the number I would anticipate for the absolute premium models of a fully functional robotwaifu, while the cheapest with their own body should be under 1k. Their choice of servos might be the reason why they already hitting the premium price point, without having a human-like robot.

>>7219
Sadly not that much progress, a lot of people which came here had to start from scratch, some were only dreaming, a lot gave probably up. Others might only be active on other platforms, like Youtube, Thingiverse, Discords like the one of Lex Friedman, some other AI or robot  websites, Doll Forum inventor thread, ... Others might have found jobs and doing other things...

@all: let't try to keep this thread as much as possible on topic (actuators of all kinds), and for other conversations move over to other threads. Thanks. Meta about the forum and robowaifus  >>3108 and Off-Topic >>39

# 102
>>1428
>Hydraulics are highly toxic.
It's really not. I repair Hydraulic cylinders for a living. It's fine as long as you don't eat it. I also wouldn't stick my dick in hydraulic fluid. It's the pinhole leaks you need to worry about. Hydraulic  injection  hazard is real and needs to be taken seriously. But you can get great control with them. And a lot of power. But they can be noisy. You don't necessarily  need a high pressure  system  to do the job. In fact I wouldn't want anything  using more than 500 psi interacting with a human. My boss had his finger cut off by an air cylinder. and that was at 150 psi. 

Tldr Hydraulics  can be dangerous  but not cause they are toxic

# 103
>>7288
>> I also wouldn't stick my dick in hydraulic fluid.
If we would be using that, then in the arms and even more so in the legs. That might be close, but not too close. Also:
>> Hydraulic  injection  hazard is real
Thanks, but there are ideas to use some more harmless liquids like plantoils and replace them more often. If we would use Hydraulics, then we would probably go with that.
>>But they can be noisy.
This could be a problem, but I guess this depends on various factors. One way to look at it, would be that we would have some strong muscles which are only be used when necessary. In special situations, like lifting something heavy or going up some stairs.
>My boss had his finger cut off by an air cylinder. and that was at 150 psi. 
Oh, thanks for the remainder to be careful. This certainly applies as well when working with Pneumatics or motors.

# 104
>>7217
>https://www.pollen-robotics.com/opensource/
>They have some interesting resources available
Yes, they have: https://forum.pollen-robotics.com/t/orbita-presentation/20 though the files on Onshape seem only to be available to view them. But I didn't look around very much, maybe I need to register first.

# 105
>>7288
Hmm. I see, thanks for the information Anon. Hydraulics could be highly useful for some types of humanoid robotics, but personally I'm pretty skeptical atp about it's utility inside /comfy/ robowaifus you want to snuggle with inside your house.

>>7290
>but there are ideas to use some more harmless liquids like plantoils and replace them more often
Seems like a good idea if it's workable. That would at least reduce some of the issues involved with hydraulics.

>>7354
Yes, that's a pretty interesting joint design IMO Anon.

# 106
>>7095
check >>7510

# 107
>>7108
Quick fact check.
Stepper motors are four phase brushless motors with a many toothed rotor to facilitate high precision in motion. They are commonly used without encoders because their inherently high accuracy and precision leads to not needing positional feedback unless the rotor is prevented from moving. This is known as missing a step and rarely happens in proper implementation.

Brushless motors have a higher power density as a smooth rotor leads to a higher magnetic flux density. They typically are three phase but, can have any number of phases in theory. Two phase brushless motors in fact exist and are primarily used in fans where they only need to rotate in one direction with high efficiency and a long life.

A servo is any actuator with feedback for control. A linear actuator with switches to for positioning? Servo. A stepper with a rotary encoder? Servo. A balloon that displaces water which triggers open electrical contacts to control volume? Servo. Anything with with feedback for controls is a servo. 

In short, brushless motors are technically low precision stepper motors and stepper motors are high precision  brushless motors but, the term stepper is useful towards differentiating which kind of rotor is implemented. Servos have some sort of feedback for control.

Brushless motors are currently the ideal actuator for waifus. They are significantly lighter for their power density then anything comparable. Their main problem is their incredibly high price when compared to DC motors due largely to their controllers needing an order of magnitude greater complexity compared to DC motors simple H-bridge.

# 108
>>7951
Very lucid definitions, quite understandable. Thanks.

# 109
>related xpost
>>7969

# 110
Here's another cyclodial drive, really cool: https://youtu.be/vYmF4hZzFhI
I might start trying some design soon, probably recreating it in Solvespace. It might be that one. Looks easy enough. But I don't know when to start since I'll need to take it easy for one or two month bc other things to do. I currently don't have the right motors anyways.

# 111
>>8170
Good luck Anon. I'm sure you'll figure everything out alright.

# 112
>>8170
More on cyclodial drives:
More detailed explanation with design process including formulars and such, Solidworks,  milled aluminum: https://youtu.be/Nk3aaVcvbpA - he also mentioned at the beginning that these can be made backdrivable and therefore compliant (save, responsive to some resistance). He uses a GYEMS RMD-L-7015 servo. Here the first test with a 3D printed prototype: https://youtu.be/i_AI95lYe0M - 71deg/s and circa 3.2kg with a 28cm arm.
Another one, 12:1, small with a TT gearmotor: https://youtu.be/01v10qvjFIA and on Thingy (but only stl): https://www.thingiverse.com/thing:4444667 
Roomba board, 20:1, Nema-17, with a lot of thoughts on how to do it with a printed design: https://youtu.be/WvnJjsAkslE and Thingy (stl only): https://www.thingiverse.com/thing:4604783/files

Other topics: Someone mentioned mjbots quad project in the meta-thread >>7969, Skyentific made a video on their brushless motor controler: https://youtu.be/R2uuTfuyadk

# 113
Reading a bit on brushless motors. Intentionally not ones for robots, since I want to get the basics and understand the differences between the different variants. 
Quads (aka Drones): https://dronenodes.com/drone-motors-brushless-guide/
RC cars: https://www.rccaraction.com/brushless-motor-tech-everything-you-need-to-know/
Helicopters: http://www.modelaviation.com/brushless-motor-design
Bigger ones and a longer interview about the details on motors: http://www.modelaviation.com/brushless-motor-design

>RH: Most RC helicopter motors are outrunners, because they provide excellent torque. In an outrunner motor, the motor casing spins and magnets are glued to the inside wall of the motor casing. The extra inertia from the spinning motor casing helps with torque.
>For inrunner motors, the motor casing does not spin; the magnets are mounted on a rotor that sits in the center of the motor. Inrunner motors have lower inertia and can spin very fast—even up to 50,000 rpm. They are popular for on-road RC race cars.

>High-quality stator material allows the internal molecules to change direction quicker. An iron-nickel (NiFe) alloy is a typical stator material. Currently, Japan manufactures the best treated iron material for motor stator use. Good stator iron is expensive, requires a special manufacturing process, has gone through the right hot-cool cycle, is stable with temperature, and has no oxygen inside. We buy our stator material from Japan then stamp it to the shape we need in Germany.

# 114
Of course, I forgot the pictures. Because my browser crashed before and reloading didn't load them. So here they are.

# 115
>>8213
Thanks. I like those diagrams, very helpful.

# 116
Reeee, I think this is the "gearbox" we really need: https://youtu.be/0-uSUrcRsyw and it's from 2017 but has been ignored. I don't care about the efficiency part so much, till I can take my waifu hiking or so, but it can reverse directions smoothly. This is crucial for security and compliance.
https://spectrum.ieee.org/automaton/robotics/robotics-hardware/inception-drive-a-compact-infinitely-variable-transmission-for-robotics
> Force control: Apply a constant force at the motor (or spring) and determine the output force by modulating the gear ratio;
>Velocity control: Apply the most efficient motor velocity and determine the output by modulating the gear ratio;
>Energy flow control: Monitor the amount of energy distributed across the system at any point in time, and move it using the transmission ratio and the motor controller to optimize efficiency or power;
>Impedance control: Because the transmission ratio is adjustable, the impedance of the system can be tuned for optimal environmental interactions (excellent for managing impacts and human safety factors).

# 117
>>8212
First post on this forum. Would it be viable to use a geared-down drone motor for a miniature robot with a limited range of motion?

# 118
>>8270
Not him, but I don't see why it wouldn't work. In the end, it might just be simpler to use specialized servo motors for most of the many motors probably needed. Welcome BTW. We have an ''Embassy Thread'' if you'd care to introduce yourself >>2823 (not required ofc).

What kind of miniature robot were you thinking of Anon?

# 119
>>8221
I remember looking at that system before Anon. Very interesting actually. I wonder why it hasn't been pursued further by this stage?

# 120
>>8270
>Drone motor with gears
I haven't tried myself, but I'm sure this would be working and I intend to go that way.
>>8277
We might not know about it, or it's just because there aren't that many companies working on humanoid robots for dealing with people.

# 121
>>8271
I'll tell you in a spoiler. It may or may not be off topic to the forum. [spoiler]Test[/spoiler]

# 122
>>8271
[spoiler]It's a my little pony robo-wAIfu. Many anons that I love seriously need one and would spend thousands of dollars to have/build one. Other aspects of the project (voice, behavior) are nearly complete by other anons, and in development as we speak. Someone or some people need to build it eventually, and I think I fit the bill.[/spoiler]

# 123
>>8295
Ponys are perfectly fine here Anon. Good project goals, I'm sure we wish you well. Please share all your progress here with us. I would suggest keeping it all contained within a single thread so anyone offended by it can simply hide the thread.

>===
-''add thread suggestion''

# 124
>>8296
Great, so back on topic: what kind of gear train would be best for a bldc that can run at many thousands of rpm?

# 125
>>8304
I'm not a mechanical engineer myself (we have at least one here), but I suspect there is more than one company providing solutions for this type need. Electrocraft seems to be one.
www.electrocraft.com/

# 126
>>8304
They don't run that many rpm as soon as a load is attached. If it has a high rpm will need more reduction of course. My point is more about looking into these flat, and sometimes huge, outrunner motors with many poles. Those are often being used in drones or helicopters. There are also those which already are mini cheeta servos, but those might be very expensive and have the wrong size. I'm thinking, for experimenting I might get something cheaper and work myself up.

One with Moteus controler: https://youtu.be/R2uuTfuyadk
Blackbird Bipedal robot, by Gabreal Levine: https://youtu.be/Xf3DfE1KrwI

Here is more on Strain Wave Gear from >>8221: https://youtu.be/xlnNj9F37MA

# 127
>>7951
>>8270
I finally stumbled over a video where all types are explained, including the difference between bldc and steppers: https://youtu.be/I2_-etus0KQ

# 128
>>1449
>Slow artificial muscle fibers
>Technology doesn't scale
Using one straight wire alone doesn't scale well due to the limiting heat dissipation. The heat transfer (surface area exposed to air) decreases at the same rate that the radius of the wire increases. Three ways to overcome this in order of least to greatest cost/complexity are: Use multiple thin wires in parallel, add coolant (water or phase change), use a NITI precipitation-hardening alloy (higher max stress = lower wire mass). 

Also, Nitinol wire has a limitation of only being extensible with 2-5% initial length recovery. Coils solve this problem by loading the wire in torsion, with the extended length dependent on the coil geometry. All this being said, this technology has the greatest potential but has a huge problem with repeatability. It's strengths and weaknesses alike come from being an active material which changes properties with cycles and loading conditions. 

TLDR: You are better off sticking with an electric motor for enough accuracy to use modeled movements for now, and nitinol for face/fun bits which don't have to be accurate.

# 129
>>8344
>The heat transfer (surface area exposed to air) decreases at the same rate that the radius of the wire increases.
>not using monatomic wires for all our robowaifu needs
<shiggity
J/K. I had an interesting traversal through wiki articles learning about this. Have any education recommendations Anon?
>NITI precipitation-hardening alloy
Neat, I'm learning more still.

>and nitinol for face/fun bits which don't have to be accurate.
I would suggest that facial may in fact be literally ''the highest need for accuracy in the entire robowaifu system''. At least the externally-visible motions. For example the eyes and eyelids are notoriously important to get just right in animation to bring the characters 'to life'. It's a remarkably subtle business tbh. Other areas on the face/head might need less precision, much of the cheeks, neck, and brows for instance.

# 130
>>8344
I'm going with dc motors, magnetic switches, and such, pneumatics and maybe some nylon. Maybe piezoelectric actuators. Nothing has changed. I also think that pneumatics are good keeping a body in a static position, with no use of energy, while being able to dampen some external force.

# 131
>>8347
Mini cheetah motors have support behind them and plenty of guides to get set up. The motor is 370$ on aliexpress and the boards that run it are probably not that expensive. These motors are the best viable option to get into reasonably strong, realistic movement at the present. The motors are bldc with a wide airgap and are quasi-direct driven (4 or 6 to one planetary gearbox) for minimal backlash. Do your own research to learn more about these motors.

# 132
>>8362
These mentions of mini cheetah are from me: >>8307 >>4890. There's also >>4898. However, I only see them being interesting for the hips and maybe for the shoulders. We'll need more motors, and also cheaper ones for learning, testing and prototyping.

# 133
>>8363
Holy shit I can't read. Good stuff, anon. Good luck on researching this stuff because my mech engineer brain can't understand it.

>>8345
Attached is the general idea, and that is the subject of research which I am doing in person. It is from: https://ieeexplore.ieee.org/document/4412462

# 134
Quick reminder on the strength of printed gears: https://youtu.be/b6cDOyxub8w

# 135
>>8404
Forgot the link to the file: https://www.thingiverse.com/thing:2375916

# 136
>>8404
>>8405
Thanks!

# 137
>>8363
Added the ''Boolean OR'' logical operator to waifusearch for a convenient consolidated listing for various spellings (there are 3) now. Here you go Anon:
>>8415

# 138
Actuator and muscle related:
>bearings, ball-bearings, stainless steel bearing balls
>>8364 and following
>electically activated polymers
>>8502 and following

# 139
Eccentric-Cycloidal gearing has been discovered a while ago, at least 10 years, but we have NO comment on it. Till now! 
Well, if you looked at the InMoov neck mechanism, or even printed it, then you already saw something like it. These can be worm-like 3d printed parts or disks. Here some videos:
Basjc example: https://youtu.be/AMtyFwMDL7w
Rack and pinion: https://youtu.be/g-CmpPBrFtE
Reducer: https://youtu.be/XrSilJGHBCQ
Comparison: https://youtu.be/kq-tHHwgGwU
Channel: https://youtube.com/user/ECgearing
Website has news on it, and more vids, though they're on Russian or Ukrainian: http://ec-gearing.com/

Here's a article from a company using it, though not the 3d printed version, but the kind which is made out of machined discs. I only read parts of the article, yet. https://www.sogears.com/products/manufacturer/31-eccentric-cycloidal-drive.html

Then there are eccentric planetary gears, here done in wood, but would also work with laser cut or printed plastics: https://youtu.be/P_pNqpdLV-8

# 140
>>8718
Thank you for bringing it to our attentions Anon!

# 141
Related: >>8742 - It's about a silicone rubber printer for muscles and such.

# 142
>>8382
Update on the Nitinol SMA work: Even the best coils and control systems are unsuitable for this application. They require heat to move no matter what, and that is the last thing you want inside of a shell. Also, they have a low frequency of actuation, break if they are under too high of stress or stopped while moving, and they are very difficult to control. Maybe magnetic shape memory actuators would work in place of this, but there has to be a better way than gigantic and heavy geared BLDC motors that don't resemble muscle fibers, or working fluid actuators that rely on pumps and a sealed system to work. Any thoughts?

# 143
>>8983
>and that is the last thing you want inside of a shell
Fair enough. However you probably realize it's also entirely unavoidable too. We were always going to need both active and passive cooling systems for our robowaifus, once they reach a reasonable degree of technical complexity and sophistication. Hopefully air movement (lungs) and passive radiation (skin) will be sufficient. We certainly want to avoid using liquids to the degree feasible, I'm sure.

The other issues along with this one sound like showstoppers altogether. I'd suggest the idea be abandoned as far as investing any further research into this approach -- at least for now. Maybe in the future there will be sufficient materials science improvements to warrant re-opening research into ti.

>Any thoughts
Hmm. As stated elsewhere a holistic design approach that a) reduces overall mass, particularly out in the extremities, and b) a cable-based mechanism to distribute force (Bowdens, etc) out from c) a central-mass 'power house' where the motors themselves are stored in a center-of-gravity location within the pelvis/torso volume.

There are other alternatives ofc (as exemplified by our own Sophie bot, et al). But at this stage of technology and materials development, I believe this general design approach is the only one that offers us the potential for near-human fluidity, litheness, and flexibility. Also the lowest weight,  (while remaining fully human-like capable) as well.

Not only does this cable-driven, centrally-actuated approach offer a reasonable potential for our many other goals it also brings probably the number one benefit to most of us as well -- it's inexpensive by comparison. By unifying many factors into compact solutions, we actually drive the costs themselves down, but at the expense of additional complexity for force applications (cable management, structural grommets, etc).

ATM I simply can't conceive of a better general approach to the problem of anthropomorphic kinematics solutions.

# 144
>>8986
Here's an example of the basic idea >>8637. But, imagine that this design approach is used throughout most of the body, and not just for the hands. 

Also, the motors, servos, etc., aren't kept out in the extremities (with their unavoidable weight & volume), but rather back in the central volume of the pelvis/torso with the force transmitted out by thin, lightweight, cabling.

# 145
I don't know you guys but I have the feeling that this kind of actuators could be the clue to low form factor and high torque actuators

https://www.youtube.com/watch?v=9YeBULHbCJM

# 146
>>9097
>I don't know you guys
Welcome Anon, glad to have you visit. Why not introduce yourself in our Embassy thread?
>>2823

>this kind of actuators could be the clue to low form factor and high torque actuators
Yes, that's pretty interesting. I'd like to see the internals of the cabinet and how the actuators themselves are working.

# 147
>>9098
>. I'd like to see the internals of the cabinet and how the actuators themselves are working.

check this out, is a simplified 2 dof version 

https://www.youtube.com/watch?v=3R8XS10bWdE

# 148
>>9099
Excellent. That's what I wanted to see, thanks.

# 149
Eng. Res. Express1(2019)015012
https://doi.org/10.1088/2631-8695/ab2e57
PAPER: Softfluidic actuator based on nylon artificial muscles
Personally I want to pursue the coiled wire/air bladder type actuator systems. Although I can see a possible solution as being a combination of all of these. Pneumatic for larger joints like hip and core, maybe compressors can be made smaller and quieter and some time to "recharge" after using more powerful movements? Printed gears might actually not be a bad idea for smaller more delicate movements like facial or for hands. Consider humans, we don't move "full force" with each movement, we have a lot of control over the amount of strength we use and that is why we have such high dexterity compared with other primates, who are stronger admittedly can tear us weaklings apart. Yet when under fight or flight we can push ourselves to use closer to our full strength. How can we apply these concepts to a waifubot? Alot of strength is not needed except to stand up from lying down or carry things. 
Last idea: How could we use a push/pull system to maximize efficiency? Like each muscle has an antagonist which is pulled when the other is pushing, could this energy be re-used somehow so that as long as the net "pushes and pulls" equal out, energy is conserved. This could make walking, and many other movements very efficient. In a micro-pneumatic system maybe each movement could "charge" its opposite antagonist muscle somewhat. If the torque ratios were just right, it would be a low amount of additional friction (which might actually help control "jerky" movements) yet would slowly charge the opposing muscle somehow. 
Admittedly every avenue has its drawbacks, but whereas heat activated contractile materials are weak against overheating, pneumatics has one advantage in that air is free and unless you're going to send your Waifu on a spacewalk, there shouldn't be any threat of it seizing up.

# 150
>>9113
>Last idea: How could we use a push/pull system to maximize efficiency? Like each muscle has an antagonist which is pulled when the other is pushing, could this energy be re-used somehow so that as long as the net "pushes and pulls" equal out, energy is conserved. This could make walking, and many other movements very efficient.
In my wire-based actuation system designs, a matched pair of spools windout/windup actuator wires in tandem. Just like muscle tissue, the force only gets applied on the 'contraction' side. The other side is simply expedient to keep the cabling tidy & ready for action during the opposing motion afterwards. These aren't energy-storing alone, just simple actuators.

However, coil-wound springs (clock springs) can be added into the designs, affixed to the spool bases at their fasten positions to the frames. They would 'wind-up' in ''both'' directions (being matched sets) and would then assist bringing the actuated limbs back to a neutral position faster/more smoothly. They would also afford a measure of lifelike resilience during force application, internal or external. Shock-absorbers, if you will.

But, stay conscious of the fact that ''there are no perpetual motion machines possible''. This approach with the springs is simply an intentional design choice due to the benefits outweighing the detriments.

# 151
>>9117
>However, coil-wound springs (clock springs) can be added into the designs, affixed to the spool bases at their fasten positions to the frames. They would 'wind-up' in both directions (being matched sets) and would then assist bringing the actuated limbs back to a neutral position faster/more smoothly. They would also afford a measure of lifelike resilience during force application, internal or external. Shock-absorbers, if you will.

I love this idea. The reason robotic movements for lack of a better term, are "robotic" and uncanny valley is the jerkiness and rigidity. To be a better human world interface they would need to move more like us with a certain degree of flexibility and momentum. Granted you could have specific servos designed for when absolute precision was necessary, like the idea of retaining gear driven systems for fingers, whereas arms, core and legs would have some recoil or "bounce" to them like a living human. My original idea was some kind of flexible bladder system but I've also been turning another idea over in my head lately. Some kind of metal coil system where the flexibility is derived from the "bend" of the metal as thin strips (not wires) are wrapped into some kind of topology that does the job. Think METAMATERIAL properties and now we're on the right track.

# 152
>>9173
I think you may be onto something Anon. Mind posting some sketches or something so we can better visualize your ideas please?

# 153
somewhat related to the idea of metamaterials
https://www.youtube.com/watch?v=ThwuT3_AG6w

# 154
>>9175
that was my plan. Once I get back from my errands I'll see what I can sketch out

# 155
>>9117 >>9173
I had a similar idea when I saw the video of Eccerobot, which is "hiding" in plain sight on the top of our thread on skeletons. It uses rubber bands. For example, to move its arms faster when they start moving. Which is more human-like. I only saw short videos on Youtube, the creator didn't show how the whole system exactly works and has been build. I only kept it in mind as inspiration. 
My idea coming from that, was putting steel springs somewhere into the elbow mechanism. Then loading them with the motor turning when the arms are down, loading the spring and then have a mechanism to block the spring, so the motor doesn't need to hold it the whole time. When the arms needs to be lifted, the spring could be released to give it a starting boost. How exactly to stop it, if not all of the power is needed, I'm not sure. The motor could work against it, or the mechanism would stop it. Details are something for trying out when there's a prototype. The mechanism to hold the spring while loaded could be as solenoid, which is a electro-magnet with a pin and a spring. It sticks out till the magnet is active, then the pin goes into it, after the current stops it comes out again. So in our case it would be active while the arm spring is being loaded, then blocking it, without needing energy. Obviously, this would require a gear which can be speed up which help of the spring.  
The other idea, I already mentioned here on the board, was to have some springs or bumpers in the legs which would recycle the energy from the body "falling" down when there's no holding torque. This would then help to push the body back up, maybe till hitting some other springs. I looked a bit into bumpers for mountain bikes, with the idea to put them into the legs, but a smaller spring per leg might be sufficient, or a more complex mechanism out of some smaller springs. The whole idea here is, to enable her to move her booty in seductive ways while not using much energy. So she could be standing around and dancing a little bit for a long time, without needing big batteries to do that.

# 156
>>7086 >>8170 >>8207
Our friend James made a cyclodial drive for his robodog. His first attempt failed, but the video is very interesting: https://www.youtube.com/watch?v=pWMB5VbLb6w
CAD for this version: https://github.com/XRobots/CycloidalDrive
As it happens, the size is about right for a fembot hip drive, especially if she has some additional (air/nylon) muscles in case she needs to lift something. Also he clarified that these are backdriveable. Then he also used a RC aircraft engine to power it. Great. Looking forward to part two.

# 157
>>9181
Look forward to seeing it Anon.

>>9195
These are all great mechanical ideas Anon. I don't see any fundamental reasons why these wouldn't work. The idea of a 'clockwork man' goes back for at least hundreds of years, and other related ideas for robowaifus back for at least 2'000 years. The time is ripe for these dreams of men to become a reality. Your plans will very likely work as intended.

As you suggest however, it will take a lot of work to design and construct it all ''just so''. It will take a lot of fine-tuning to get just right. We'll all probably go through several prototypes before we get it right.

But the results will be worth __every__ effort we must make towards the goal.

>>9198
He is a really, really clever guy. Please keep us updated on his achievements Anon. Thanks for the CAD link!

# 158
>>9207
>>9175
This is not to proportional scale, so the "muscle" can be of any proportion. The objective is to deliver torque of varying strengths rather than a single jerky motion. The nitrile (or functionally similar bundle strips) will be wrapped around a pressurized bladder for shock absorption and to provide nominal "resistance" to make movement more fluid and regular. Not the force vector magnitudes are only correct for a flat plane, I'm not well versed on my geometry/trigonometry to quickly compute the coefficients involved when we account for the 3rd dimension, as they are wrapped in a spiral. 
This is just a demonstration of concept.

# 159
>>9221
Each angle-offset bundle of fiber can be stimulated by a different degree of force the robot wishes to apply. So going "all out" would use all muscle fibers and handling something delicate or using greater finesse would utilize the steepest angle offset first, then the next, and so on (or even different combinations to achieve intermediate levels of force)

# 160
>>9221
note we could also adopt different topologies (such as torus) for different purposes

# 161
>>9221
>>9222
>>9223
OK, I think I get that better now. So different parts can apply different degrees of force, and if desired they can all work together in concert to add forces. Is this correct?

# 162
>>9224
exactly, a few other things
1. Most important is the idea that there is some flexible resistance to the force to mitigate jerkiness via the internal pressurized bladder
2. One concern with nitrile wire or any other contractable filiment/wire is breaking and weakness, combining them into strips adds both tensile strength and should increase force output. Another option which might work better would be to simply use mechanical actuators with strips of semi flexible metal. 
3. Yes, we can now apply varying levels of force without complicated gears

# 163
>>9225
I wonder if you created something like a stretchable-fabric 'bag' for the air bladder to fit into, and that guides of some sort stitched spirally around it that compression wires could run through. These could alternately stiffen or soften an already partially-filled bladder, and do it via a simple motor/spool combination.

Think something like that might also work Anon?

# 164
This magazine has quite some interesting introduction to analog servos: https://www.servomagazine.com/magazine/article/July2015_Ostendorff
Selecting motors: https://www.servomagazine.com/magazine/article/tips_for_selecting_dc_motors_for_your_mobile_robot
Repairs and optimization (for combat): https://www.servomagazine.com/magazine/article/July2016_Parts-is-Parts-Coils-of-War

# 165
Is instant braking in motors usefull for us? I guess so. How common is it? Hiw special is this: https://youtu.be/shmP5Nnid38

# 166
>>9800
*How

# 167
As you know there are plants that has high speed movement like venus fly traps. 

As far as I know is relatively easy to create new plant breeding, imagine being able to grow high speed high torque muscles using plants. 

Do you think is an stupid idea ?

# 168
Begin selective breeding of Venus Flytraps and see what you can make anon! :D Venus Flytrap-derived vaginal muscles ROFL! ...Or maybe not...it's best to keep your dick away from such plants, even if it is for science.

# 169
>>9941
>Do you think is an stupid idea ?
No, not at all Anon. But ''any'' living, biological system brings a metric boatload of baggage along with it. BTW, we have a thread dedicated to it, broadly-speaking (>>2184 there may be others). But at the __very__ least we as engineers and designers should be investigating closely the observations from the ''biomimetics engineering'' fields. 

>>9942
Keke. Do do anything weird Anon, it could cost you.

# 170
>>9945
> '''Don't''' do*
lol

# 171
>>9941
>Lyekka waifu?
Okay. Reminder that we need a thread for all the freakish biology based plans, related >>7498, or the biological brains thread is being renamed and used for that. Don't get me wrong, I like that idea with the plant muscle. I guess it would be to weak though, not flexible and resilient enough, or would have other issues [spoiler] e.g. eating humans [/spoiler].

# 172
Hi guys I would try to explain a mechanism that I think would open the door to small form factor and cheap actuators. 

>1 Each degree of freedom of the robot is operated using a pulley system
>2 The torque source of each system is powered by the same motor 
>3 There is a mechanism that sets the first pulley of each degree of freedom on Break or Coupled state 

The issue here is, how would you displace the the pulley, we would need a cheap small form factor of linear movement. 
I hope the image can describe my idea.

# 173
>>10001
Hello Anon, welcome. Call us 'Anon'. Contribute to our Embassy thread if you'd care to. I like the sound of your idea, but I'm not very qualified to comment on it. We have at least a couple of ME who are affiliated here. Be patient and maybe someone else can comment on your design idea.

Again, welcome.

# 174
>>10001
That's a good question. I have similar thoughts on how to do things, reducing the number of motors by changing their place or by coupling pullleys. I don't really have a answer to your question, though. Where do you want to put that motor, or is it a more general question? I mean, winding the pulley up to some spool would be the obvious idea. If it would need to handle surprises and need to move the other way faster than it could, maybe adding a spring into the pulley (where it doesn't need to wind) might do the trick? Or the motor winding the pulley up could be connected to the rest of the body with a spring? We could also think of lock mechanisms for such springs, maybe by using some magnetic switches, solenoids or some another mechanism. I don't have any experience on how to use motors to wind up some pulley, so we might just use very small playtoy motors to try stuff out before getting bigger ones.

# 175
>>10121
The Mini-Cheetah servos on Aliexpress claim to have 6.9 Nm of continuous torque, whereas Dynamixel-P series has up to 44.7 Nm. If you were move the servos into the torso you still have to account for lifting the body's weight up when standing. If the upper body is 20kg you need at least 40 Nm in each hip to lift that alone. Distributing the work across different servos requires them to be at least 10 Nm. The MC servos would be sufficient though for a smaller or extremely lightweight robowaifu.

The OpenTorque actuator has a tested torque of 25-28 Nm and costs around $150 to build but it's big and quite heavy at 1150g. Perhaps it could be remade for a different motor more suitable for a robowaifu?
https://hackaday.io/project/159404-opentorque-actuator
First-party test: https://www.youtube.com/watch?v=n_CiCqIRS2E
Second-party test: https://www.youtube.com/watch?v=6lW2YGQQIQ4

# 176
>>10131
> If the upper body is 20kg you need at least 40 Nm in each hip to lift that alone.
> Distributing the work across different servos requires them to be at least 10 Nm
Could you explain how you arrived at these conclusions? And if you're going to break down the geometric physics math for us, if you would do you mind also adding ''this'' set Anon?

This is all the same design experiment, simply testing the single variable of a 1kg mass:
- How much accumulated torque (in ''Nm'' or w/e) would be requited in total to rotate an attached 1m long lever (say a 200g rod) 90 degrees, with a 1kg mass affixed to the distal end of the lever?
- Conversely, how much force needed to repeat the exact same motion '''w/o''' the 1kg extra mass entirely?
- Finally, with the 1kg mass affixed directly transversely with the rotation axis of the OpenTorque actuator. That is to say, the extra mass is affixed directly to the external side of the actuator shell, and rotates in lock step with it.

TIA Anon, appreciated.

# 177
>>10135
Thanks, I didn't know about these huge differences.

# 178
anons , I am driving crazy trying to solve the problem of having many degrees of freedom using cheap high speed  high torque small form factor actuators. 
And I have this idea, as you know solenoid air valves aren't small so what if we use this principle

https://www.youtube.com/watch?v=MhVw-MHGv4s

The clip pen mechanism could be use to reach low energy consumption for valves, we would only need an spike of energy to switch it. 

The air muscles could be done modifying this approach 
https://softroboticstoolkit.com/

# 179
Related to main topic: Hydraulic muscles by Automaton Robotics: >>10179

>>10150
>Clip power storage mechanism
Interesting. Do you have an idea if we can get the plans from somewhere? Or if you could copy the design based on the video? Solenoids can be very small, but this might be good to store power from a motor to help it start moving some part faster. I mean by adding some startup power boost: >>9195. I'm concerned about the clicking, though.

# 180
>>10150
>cheap 
>high speed  
>high torque 
>small form factor 
You're kind of violating some engineering principles there. a) '''No one''' 'outsmarts' the laws of physics, and b) ''economics'' is a thing.

Pick any two Anon.

# 181
>>9754
Thanks, Anon!

# 182
>>8988
So one of my main project goals is to make a horse leg for a pony waifu. There may be as many as 7 joints that can move in each leg, and I think that the mini cheetah motors are not suited for the torque required by looking at the later anon's posts. I could see making a bowden system or a chain or belt-driven system that could work reasonably well with dynamixel servos at the high end. What do you think is the best way to predict how much torque is required to move a thing with 4 legs?

# 183
>>10470
>What do you think is the best way to predict how much torque is required to move a thing with 4 legs?
Unfortunately, I'm not a mechanical engineer (though we have a couple here who stop by occasionally)), so I can't give you the formulas, etc. for it. They are out there. Calculating lever-moments of torque, etc. One thing you can take for granted is that while the kinematics with be more ''involved'' with a quadruped, the actual design-work __itself__ will be simpler. This is one reason that Boston Dynamics ''Spot'' is already on the market today.

Personally, I simply rely on basic mechanical experience from working on cars & construction, etc., to give me a good instinct as to what will work and what will not. 'Keep things Lightweight & Strong' is almost __always__ a good design decision Anon. As for my own approach to such things, the answer is quite a simple one:
>'''test everything'''
I'm much closer to a Michael Faraday than a James Clerk Maxwell. :^)

# 184
>>10475
Thanks anon. I'm graduating as a ME in a few months, and I figure I can read a few research papers on something like this done already, or skip to modeling a leg in a gait simulator to come up with the maximum torque/power. Also for the anons who are making hands/toes, it could be lighter/smaller to make a single motor with a clutch/transmission system to distribute power to whichever fingers instead of cramming 5 motors or more for each finger. The downside would be higher complexity.

# 185
>>10488
>Also for the anons who are making hands/toes, it could be lighter/smaller to make a single motor with a clutch/transmission system to distribute power to whichever fingers instead of cramming 5 motors or more for each finger. The downside would be higher complexity.
Yes, all engineering endeavor is a constant balance of tradeoffs. Such is physics.

I've thought numerous times about a central motive drive shaft in core locations, with radial clutches all lined up like ducks in a row along it. As each clutch engages, it would translate it's new force out to a linear actuator associated with it.

My notion vaguely hearkens back to the days of yore when steam-powered factories were all the rage at the start of the industrial revolution. Stationary steam-engines typically drove several long driveshafts down the lengths of the factory, and radial clutch/pulley arrangements transmitted some of the power off through belts into the machines on the factory floor.

Ofc, our needs are quite different, but the fundamental physical mechanisms (and even some design-work) can be quite similar. I expect you could even capitalize on such an arrangement for a real steam-punkish design motif for robowaifus!

# 186
I posted this once in the robowaifu thread on mpol.net: https://hackaday.io/project/175888-motorized-walking-atat-using-servos-and-arduino - maybe this helps a litte. It's about building a ATAT from Star Wars.

# 187
>>10492
Neat Anon, thanks! I'd say it's a good example of design approaches that could be useful to everyone when creating robowaifus.

>other related links he gave
https://www.thingiverse.com/thing:1083338
https://www.thingiverse.com/thing:4641541
https://www.thingiverse.com/thing:4651937

# 188
>related xpost (>>10436)

# 189
>>10509
Okay, but it doesn't show what this is about. Maybe this should be part of these crosslinks? If the posting isn't moved to the right thread.
>Hazel actuators

# 190
>>10492 was meant for >>10470
I'm trying to find out how to calculate stuff like this myself right now. I got some bldc motors for experiments and try to find out how well I could use them (after buying them, lol). Look at this: https://maker.pro/custom/tutorial/motor-sizing-math
This software here might also be good, but it requires Windows and registration: https://www.orientalmotor.com/technology/motor-sizing-calculations.html - here the video: https://youtu.be/9MG8-3QuSyQ
I also calculated something in Python, but have to post that from my other computer. I divided the weight of an arm and the length through ten, so I've got ten parts, each closer to the motor, then used the formula and added the values up.

# 191
>>10539
I used this for torque: https://www.electrical4u.net/calculator/electric-motor-torque-calculation-formula-torque-calculator-online/
>For Calculating, Torque for DC motor
T = V x I / (2 x pi x N(rpm) / 60)
N(rpm) is the speed of the motor
V => Input DC Voltage
I => Input DC Current
From Kv to rpm its Kv multiplied by voltage: https://drones.stackexchange.com/questions/49/what-does-kv-mean-on-motors
Gear reduction calculation then seems to be simple, just multiplying by the reduction. I'm sure, like the other calculations here, this is not very precise. Good news for me, though. With a reduction of four or five in the ellbow I should get more than what I need, if I didn't make a mistake.

# 192
>>10540
I also really like Quora for stuff like this, if only their app would support dual screen... *whatever*
https://www.quora.com/How-many-Newtons-does-it-take-to-lift-100g-of-mass?share=1
>A Newton is defined as 1kgm/s^2. Lifting is force against gravity; so using the formula F=ma use g in place of a. Also mentally convert 100g to .1kg.
>F=mg = .1kg x 9.8m/s^2 = .98kgm/s^2 = .98N
>Answer .98N

# 193
>>10541
My Python code for calculating it:
[code]
newton = 9.8
arm_in_kg = 0.5
section_weight = arm_in_kg / 10
sections = [i / 100 for i in range(3,33,3)] # ten sections with different distance to the motor 
newton_meter_required = sum([section * section_weight * newton for section in sections])
newton_cm_required = newton_meter_required * 100
newton_cm_required
[/code]
>80.85
[code]
motor_in_newton_cm = 3.8
gear_reduction = 30
motor_in_newton_cm * gear_reduction
[/code]
>114.0

# 194
>>10490
I've completely abandoned hope in artificial muscle fibers that are viable for now. The best things available aren't purely electric powered or are a heat system. Those that are are made from polymers or flexible materials which can't take the stress while sized correctly to a normal muscle. Therefore the best way forward for a beginner like me is to make bots with hobby servos and then upgrade to low-mechanical impedance BLDC motors when I know what I'm doing, or skip this step and finish it. 
>TLDR: using whatever hobby servos I can afford until perfect electric muscle fibers (not you nitinol) are invented
Anyone know of a gait simulator program and ways to make 3d models? I'll check the board rn.

# 195
>>10601
>Anyone know of a gait simulator program 
An anon mentioned ''cyberbotics.com/'' (>>10531)

>and ways to make 3d models? 
Blender (>>8107) . I'd suggest you have a look at ''Grant Abbitt's'' YT channel as a good place to find information. Be sure not to miss his 'YT channels you may be missing' video in his Blender Quick Tips' playlist.

Also, ''Dev Enabled'' has good stuff for you probably, since this is kind of like the same needs of a traditional vidya in many ways.

# 196
>>10601
Nice looking paper Anon, thanks. Interested ME spin on the medical leg prosthetics domain.

# 197
>>10574
No comments. So I can assume, it's correct and a decent approach?

# 198
>>10608
I"m not qualified to analyze it personally myself Anon, so I kept my mouth shut. Your code seems to remind me a little of a process I've heard about called 'Finite Element Analysis'.

I don't see anything wrong with your code, but to my (again, admittedly untrained) eye, I'm missing any calculation related to lever-action multipliers related to each element's distance from the base axis of rotation. 

Am I missing something here?

# 199
These are copied over from where I commented in the wrong place

Gromment(Grommets are useful to stick things together)

Found this paper.

"Air/water interfacial assembled rubbery semiconducting nanofilm for fully rubbery integrated electronics"

Quote,"...rubber-like stretchable semiconductor...Here, we report the scalable manufacturing of high-performance stretchable semiconducting nanofilms and the development of fully rubbery transistors, integrated electronics, and functional devices...their electrical performances were retained even when stretched by 50%. An elastic smart skin for multiplexed spatiotemporal mapping of physical pressing and a medical robotic hand equipped with rubbery multifunctional electronic skin was developed to show the applications of fully rubbery-integrated functional devices..."

https://advances.sciencemag.org/content/6/38/eabb3656

I think something like this will eventually be seen as the most viable path. All these mechanical and electromechanical devices take too much machining and work to make all these little disparate parts fit together.

This process I expect you could use films and silk screen the circuits like t-shirts. Means designs would be easier to replicate. Send pdf or CAD drawings, and print them out to screen on the material. There's also a wealth of machinery, design and materials already used for screen printing that could be adapted.

Another 

Hydraulically amplified self-healing electrostatic actuators with muscle-like performance

https://science.sciencemag.org/content/359/6371/61.full

Notable capabilities
"...tested the cycle life of a donut HASEL actuator used in Fig. 1E for more than 1 million cycles ..."

"...The use of liquid dielectrics enables HASEL actuators to self-heal from dielectric breakdown..."

Fluid could be heated to keep skin warm.

"...large actuation response up to a frequency of 20 Hz..."

Fast

"...specific power during contraction of the two-unit actuator was 614 W/kg.."

For humans,"...According to our data table the body uses 685 W to climb stairs..." so the power of these far out weighs human power. Waifu could take care of you when you got old and carry you around.

# 200
>>10620
Interesting, Grommet-Anon. I think this technology will turn out to be important to us here in the future. When we are trying to optimize our designs to increase modularity, reduce weight, and reduce manufacturing costs, then directly integrating electrical and electronics directly into flexible materials will certainly be a very valuable thing to be able to do.

Do you know if there are planned approaches with this stuff that allows for simple and easy maintenance yet?

Thanks!

# 201
>>10627

I'm not exactly sure what you mean by simple maintenance but I have commented on manufacture and modularity.

I'll review and link some of it here as the comments were really in the wrong place. I first found this board from there and didn't realize the structure at the time. It's a bit of a dump but maybe having it all close together will help.

The general idea is as above Dielectric Elastomers. They use electric fields to actuate. The good thing is they are made of silicon and other elastomers which of course you can get at any hardware store to experiment with. Here's some links on this stuff.

Here's a link to a good book on these called "Dielectric Elastomers as Electromechanical Transducers: Fundamentals, Materials, Devices, Models and Applications of an Emerging Electroactive Polymer Technology"
>>8502
Dielectric Elastomers can also be used as sensors

A good page with links to 100 papers on Dielectric elastomers
>>8505

A link to a SUPER video. Note that D.E. can be used for computer logic. This means that with a few lines we could control muscles and possibly feed back sensor(touch) data. Using serial lines vastly reducing cost. Just like SATA and USB drive interfaces are cheaper than the older parallel interfaces. Large numbers of wires are a pain in the ass, costly and troublesome.

With the right logic you could move some logic into the actuators themselves. I think actual human muscles have some logic in them??? An example would be if the waifu hits something it would reduce it's force in the muscle.
>>8519
>>8522

I describe above how you could make these.

The idea is to roll out thin sheets of this stuff like a round homemade taco shell or tortilla. You lay out a layer. Silk screen on the control lines, logic and add parallel lines of strong fibers and power/control lines sticking far outside the ends of the layer, fishing line should do nicely, maybe or likely have several layers on top of each other for different functions, add one or more power/control lines to the logic then you roll the thing up from one end. What you have is something that looks very much like a muscle with a thick middle and skinny ends with the fishing line stuck out the ends that are tendons.

Visualize each little muscle much smaller and shorter than the whole muscle but with long tendon and power/control lines.

 Say you are building a muscle, the one on your upper arm that you flex to show how strong you are. You would build this out of a bundle of maybe 30 of these small muscles. You tie them together in series for length and add them in parallel (each offset from each other to stack smoothly).

All the fishing line tendons would wrap around anchor points in the bone

Once you have a muscle bundled together in a group you could in turn pack it in some sort of cloth covering to keep them all together.

Obviously you could remove these and replace individual muscles or the whole group.

As for sizes you could maybe have 3 or 4 sizes. The smallest would be very small such that it would still take 20 or 30 of these to make a finger muscle. This gives you redundancy and having small muscles in a bundle let's them move around realistically like real muscle.

Another book.

"Muscles, Reflexes, and Locomotion" by Thomas A. McMahon
>>8975
Some ideas. I also touch on skin.
>>8311
I think the best way to make skin  is to use that fabric called microfiber with a little bit of elastic fiber added in to make it stretch. It's super soft to the touch. It's used for towels and you could throw the whole waifu in the tub, scrub it off then drip dry. If it's smart enough it could do it itself.

The skin could be one big piece from toes to head. The vagina, butt could be pockets that go into a cavity. To connect them you move aside the abdominal muscles pull into the body tight and attach to a holder. Possibly be held in place with Velcro??? Reach into the top of the head for the mouth and ears. Skull cap could be removable. Wig, skull cap to cover???

If you connect the vagina and butt with the mouth the robot could drink water and wash itself out.

Don't forget the elastomer muscles in the sensual areas. They could vibrate and/or contract to do wonderful things. These parts could be removable.

I look at all these mechanical things, electric motors, gear boxes, noisy hydraulics, pnumatics and I can't imagine you could ever get the cost down on these things. They're great but they produce a lot of noise, they take a vast amount of machining resources and if they are 3D printed most plastic is fairly weak. If you use electric servos or motors you're going to have to have some sort of transmission and all of them will make a huge racket. You will have a grinding, thumping washing machine for a mate. Hydraulics and pneumatics are very inefficient and make a lot of noise.

I think the Dielectric Elastomers are the most fruitful path but...it's going to take a lot of experiments and work to get these to work.

 Motors, pnumatics, etc., well you can cobble something together right now that will work but I expect it will never reach a satisfactory conclusion and will always be expensive, noisy and inefficient.

 The D.E. made be a more difficult path but I could see it being extremely lifelike.

One last thing about skin. I'm opposed to silicon. It's messy, tears easily, collects dirt and everyone will know it's a robot. Why not cover it in micro-fiber that's easy to keep clean and  super smooth to the touch.

# 202
I've just come across this youtube channel, they seem to be making progress with a biometric hand using air muscles. They've even started work on some which are actuated by heating an engineered fluid with an electrical element to create pressure internally.  https://www.youtube.com/channel/UCd0xLOw6No5IAsq3Y2-b0eA

# 203
>>10639
Thanks for the excellent post. Lots of consolidated information and ideas here. Much appreciated, Anon.

# 204
>>10641
Yeah, that's Automaton. I put links into the thread for humanoid robotics videos, a while ago:
>>5136
>>10179
With a crosslink here >>10180
It's actually hydraulic, with water, not pneumatics (air muscles). I only realized that myself recently, before I thought these were pneumatics.

# 205
>>10640
He's fun to watch as well. I feel like we're looking in on a Slavic mad scientist at work.

# 206
>>10617
>missing any calculation related to lever-action multipliers related to each element's distance from the base axis of rotation
There's none. There are two calculations, one for how much torque is necessary for the whole arm and the other for how much reduction attached to te motor would be necessary to have even more than that.

# 207
>>10639
Thanks. Do you plan to replicate some of the DIY muscles on YouTube? Maybe making your own videos to show it is possible for some enthusiasts?
https://youtu.be/PDqmGHHKkWw[Embed]
https://youtu.be/eUdcBjo19oU[Embed]
https://youtu.be/hsd7_vQqt5w[Embed]
https://youtu.be/uw8FLgiXsmk[Embed]
https://youtu.be/PgNKeqOCOKE[Embed]

I hope to get one of the research set of Artimus Robotics one day, when I have time for it: 
https://youtu.be/i1QmwOxGGFA[Embed] (old video)
https://youtu.be/usvoiGBAflY[Embed] (newer)
Problem is, they need very high voltage, which might be dangerous.

They can be very strong, similar to a human muscle. Composite DEA made out of strain-stiffening elastomers and carbon nanotubes.
https://youtu.be/LWDRlfruSBM[Embed]
https://www.pnas.org/content/116/7/2476 (pdf related)

# 208
I maybe should have ordered an ESC with my motors or some mosfets and other parts. But I didn't bother to look, since I thought I already have so much stuff and it will be there. Also, I probably should have watched this video https://youtu.be/erppWLMzw8I before buying some ESC (electronic speed controller) for my bldc motors. The cheap ones cost 5€, but they seem to be simple to make, with an Arduino and some mosfets.

# 209
>>10730
I know Tamiya make some of the best R/C models and have been in the biz since 1946. Maybe get one of their ESCs?

# 210
Never heard of them and I'm not in US. I'm not sure if I need something special, or if it would even be better to be able to make ESC especially for my use cases. Since it sems to be doable, I'll probably at least gonna try. I ordered two cheap ones and some mosfets as well, so I can build my own.

# 211
>>10714
Do you plan to replicate some of the DIY muscles on YouTube?

It won't be anytime soon I don't think but eventually. Still reading about them.

I saw this video not sure if it's been linked yet. Harder to make probably but high power.

https://www.youtube.com/watch?v=xMGXqT0LWUI

One thing that I like about these is that book and video I linked where it says you can make logic with this stuff embedded into the actuator. That is fantastic. If you try to run wires and controls to every single muscle in a waifu it's going to be a mess. Lots of potential to have bad connections, trouble. If you could get one good connection, easier, and then send signals to each muscle it would dramatically cut down on cost and manufacturing complexity. Of course nothing is for free as the complexity of designing it goes up.

That research set of Artimus Robotics I bet is expensive. I bet you would be better off buying a bunch of different materials and trying different stuff instead. Of course if you are well off it would be faster to buy the kit.

# 212
Related: Buying or building your own electronic speed controller for a BLDC motor >>10729

# 213
>>10738
That's neat stuff Anon, thanks.

# 214
>>10602
>>10606
>>10738
Thanks bros. 

>>10620
I agree that soft hydraulic/pneumatic muscles are likely the best solution in the future. However, the electric motor platform is far more developed at the present, and therefore is the best solution to make one now. The fabrication is indeed cost-intensive for current robotics, but very well defined to the point where just about anything you need can be made with great precision and repeatability. Remember that if you don't choose servos you are most likely choosing high voltage, loud pneumatic compressors (or figure out a phase change system idk), loud and very messy/heavy hydraulics, or heaven forbid one of those auful heat-activated wire actuators. Maybe the best thing to try is to use lower voltage in some kind of parallel/series array with narrow or short DEs so you don't have lethal voltage millimeters away from you while you actuate the muscles. I've thought about an idea where there is a low-displacement coiled actuator that functions like a spring, with two sides of opposite voltage for actuation.

>>10639
>You will have a grinding, thumping washing machine for a mate
What if I told you I have seen a lot of people that seem to prefer that kind of bot? ^:) Since you want to be satisfied with a realistic bot, why not cover the cost of your dream by building the dreams of others? It would be extremely experiential. To build a big bot. For you. Personally, I now have some little blue sg90s to learn basic electric motors, build a little bot, and to go down my own roadmap of ideas.

# 215
>>10842
Also speaking of 
>washing machines
I found that there is a samsung washing machine stator that looks like it maybe could be hacked into an actuator, DC31-00074C. Maybe other washing machine motors and such appliance bldc motors are viable for a high-current hard robot leg similar to the mini-cheetah.

# 216
>>10854
>Maybe other washing machine motors and such appliance bldc motors are viable for a high-current hard robot leg similar to the mini-cheetah.
I think you're right. My opinion is that as more and more men around the world -- impoverished men -- seek to devise robowaifus of their own, that we'll see a veritable explosion over the coming years of creative innovation at reusing 'junk' components for robowaifu creations. And fortunatly with video sharing both commonplace and easy (even if all you have is a goyphone) then we'll see more examples of it too. 

For example, there was a set of video linked here where a brown man (possibly Indian) created a small ''moe-bot'' class robot with mostly foamcore boards and hotglued parts. It's here somewhere, but my apologies I can't locate it.

# 217
>>10854
James Bruton uses windshild wiper motors. >>10815

# 218
#Noise related
Noise level reference: https://youtu.be/C62-Yl_V4NI
Digital vs analog servos: https://youtu.be/2TVmWbIM3IM

#Other servo topics
Low quality servos might have shifting arms, not going back to the correct position: https://youtu.be/b4jAGz3YBSY
Arduino and Servos (Drone Bot Workshop): https://youtu.be/kUHmYKWwuWs
Removing jitter with 6000uf, 16V capacitor: https://youtu.be/S7EVRDPQmfE
Wiring to reduce electro magnetic emissions: https://youtu.be/vMdJdTcW5WQ

# 219
Oh, wow. Spherical gear for a ball and socket joint. This is something I thought about myself, but just didn't know how to do it and thought it might be impossible anyways. https://t.co/rxWgbMnKKB via @61laboratory

# 220
>>10951
Wow, that's pretty interesting. If we could manufacture/purchase lightweight ball and socket actuators for our robowaifu's shoulders & hips then that would be a dramatic simplification of many kinematic problems in robowaifus. Thanks Anon.

# 221
>>10951
This is much fascinate anon, thank you! 
Only problem I can see possibly occurring with the ball spur-gear is those small teeth stripping/slipping under load if the ball is made from a weak plastic. But use a strong plastic or metal and this is a very interesting solution.

# 222
>>10988
good points. probably machined metals, or possibly carbon-impregnated 3d prints?

# 223
>>10990
I'd say that 3d printing this out of anything besides PC Max will have failing areas due to layer adhesion, and even printing the joint in high resolution would cause a lot of frictional wear and energy loss. Having this part cnced would be wiser, but a prototype out of plastic would maybe work. Doing anything with detailed overhanging features is difficult on a printer and might lead to dimensional innacuracy. One solution may be to print this in parts and attach them together. Either way, the joint idea has 0 degrees of compliance from what I can tell, and would be hard to interface with a person in daily life.

# 224
>>11023
>Either way, the joint idea has 0 degrees of compliance from what I can tell, and would be hard to interface with a person in daily life.
I think it depends on the backdrivability of the motors and also the strength. If the system doesn't only rely on those motors to move, then they wouldn't need to be too strong.

# 225
>>11023
Good points.
>Having this part [CNC']ed would be wiser, but a prototype out of plastic would maybe work.
We might be able to do something with home-lab casting (Bronze maybe?) as a possible alternative.

>Either way, the joint idea has 0 degrees of compliance from what I can tell
We'd have to prototype one to be certain, or perhaps someone here who can write in Nipponese can ask the original designer linked? My first instinct is that since there is no 'ratchet' effect going on AFAICT, then is should behave as any other 'free-wheeling' actuator/gearing system. That is, is ''should'' be compliant, I think.

# 226
>>10855
> It's here somewhere, but my apologies I can't locate it.
Found it (>>10315).

# 227
>>10951
Related video: https://youtu.be/AHUv9Zda_48

# 228
>>11185
Thanks Anon! That video moves this actuator from the 
>''Hey that's pretty neat!''
category, into the 
>'''''Wow! That's remarkably impressive!!'''''
category.

The demonstration rig at the end of it shows they are clearly going for a bio-mimetic, even human-like, ball-and-joint actuator system for the hips and shoulder joints. If they can only get good miniaturization on the components overall then I think they'll have it. 

Pretty exciting stuff, this is definitely a keeper video.

# 229
Don't you think building robots with gears and electric motors, at least with current technology, is a step in the wrong direction? If you're trying to create lifelike beings, they have to move in a lifelike manner. Seeing a robot whir and click and turn with calculated precision is uncanny. I think a different method of movement like a fiberlike muscle analogue and hydraulics would be a better direction. If you can make just a single eye move around, blink and twitch around in a fast, lifelike, random manner, that would be a tremendous step toward lifelike robots. Making robot wives stand and walk is mostly solved by Boston Dynamics, but making a single face seem alive is the real frontier. Thoughts?

# 230
>>11488
>Motors vs other actuators
We had this discussion a hundert times. First, we all don't have the exact same goal in terms of what we want, then these other technologies also have their downsides. Completely avoiding them to not coming of as artificial is more difficult and not everyones priority. Motors can also be put into cases behind foam. Fast moving pneumatics also make sounds. ...
Personally I plan to go with a combination of different actuators. I got stuck a while ago at a silly problem, which I resolved recently, so I can move on. I'll write about it later.

# 231
>>11655
Wow, I really like that robowaifu design.

# 232
related. I encountered this link today, regardless if anyone wants to purchase the package or not, these images might give some clues to creating arms and hand actuators. Might be worth looking into unless we've already arrived at a better concept

Basically the product is a kit and tutorial for $199 that gives you schematics to 2d print an avatar robotic arm kit. The kit idea is also more or less what we were proposing for "waifu kits"

https://www.youbionic.com/

# 233
>>11658
3d print obviously*

# 234
>>11655
if we had a proper liquid cooling system (like a circulatory system) quiet heat activated contractile wire systems might have a place. we just need to address their vulnerabilities (can possibly break easily, rigitidy, etc) by restructuring them. I think a wire/bladder system is along the right track for this kind of thing b/c being wound around a bladder would provide some flexibility and even support against being torn by movement stresses.

[other ideas I've been playing out in my head include metal ferromagnetic ball bearings in a semi flexible fluid filled tube that get pulled by specific fields generated internally]

Tbh sometimes I just look at concept art and internals and try to imagine how it works, working backward from the final vision to the details

# 235
>>11658
Nice work, Detective. Those are some nice technical drawings he's created. Any indication if he's created a practical mockup IRL yet? If so, did he give an idea of how much each one weighs? That information will have a direct bearing on energy consumption they'll use, and therefore on overall mass/energy consumption.

# 236
James Bruton demonstrated that motors should work while still being small enough to fitt into the area around the hips and also partially, surrounded be some soft materials, in the buttocks.
https://youtu.be/tgEOpl880KM

>>11656
>>>11655
Sukabu89, once again.

>>11660
I agree, Nylon muscles are still interesting to me, as a addition to other actuators. They can use heat we have there anyways.

# 237
>>11664
>cycloidal motors
thanks for reminding me of this
>in the buttocks
the source of 2Bs explosive power 

cable systems should not be ruled out

# 238
>>11664
a primary motor in the torso and auxilliary on the butt cheeks could provide the necessary power and leverage to provide full locomotion, that's what I meant to imply by using large motors with a cable system for stability and gross motor control where nitrile wires and contractiles would be impractical (barring some new innovation)

Revisiting nitrile though, if we could ensure the point heat-source was quick enough to contract yet dissipate just as quickly, we'd be on the right track. If any anon has access to a workshop and can run some tests. (I'm still trying to get back on my feet but in the next 5 years I will have some sort of workspace for these kind of tests and research so hang in there)

# 239
This channel https://youtube.com/c/OTVinta3d shows how to model gears in Blender, including more exotic ones like eccentrically cycloidal, non- circular or hyperboloidal gears.

# 240
>>11665
'''#300kPolygons'''

>>11666
I think it's quite reasonable to expect that eventually we'll arrive at designs that posses at least two different levels of control within the same actuator systems, yes.

>>11670
That's really neat Anon, thanks!

# 241
Cycloidal drives, different approaches: 
https://youtu.be/aTiBB2n-pNQ
https://youtu.be/QrpcD1v9rp8
https://youtu.be/WvnJjsAkslE
How to design a cycloidal disk/gear (Fusion360): https://youtu.be/jQ6LQBFZXmU

Planetary gears are the cheapest gears to build, bc less metal and expensive bearings. The problem is, they seem not to be backdriveable if printed: https://youtu.be/2dG_F9rR-jM

Split Ring Compound Planet Epicyclic Gear. Seems to have the highest reduction per space.
https://youtu.be/-VtbSvVxaFA
https://youtu.be/P-Obt-9tZVo
https://youtu.be/66MlWxoQE1s
https://youtu.be/4gkbb2CBzQI
I think thats the same than Wolfrom planetary gears, but im not sure yet.

Skyentific trying out bowden cabels in a arm: https://youtu.be/ahSS5HUylT8 --write-sub

Micromotor, maybe useful for facial expressions and such things: https://youtu.be/gHTIZVPPqKU

(picture source: Sukabu89, who has a book out)
(repost bc I made an error before)

# 242
>>7354
If there is anything more compact than this for 3 axis joints, I would really like to know.

# 243
>>11664
>>11666
I've done nitinol actuators before for a year on a hand project, and it is absolutely terrible. Nylon is a worse nitinol and you need something with the precision of electronics instead of heat power.

# 244
>>11819
Do you think of it as the spine or as the whole neck? If the skull would sit on a spine, used for data transmission, then you would have the whole rest of the neck. If you would use motors, they could also be in the shoulders and pull strings. 

>>11830
I don't understand your comment completely. You mean one needs electronics to control the heat? Or the precision of electronics and motors is needed in a artificial hand? Also, why is Nylon worse? Did you try to control the whole hand alone with such fibers? If so, why?

# 245
>>11831
Electromagnetic motors (or working fluids devices with electromagnetic solenoid valves) offer far greater control and precision than a heat-based system which uses the ambient air to exhaust energy. Shape memory materials usually use heat to return to a shape after being deformed. A rough motion like gripping can be obtained with shape memory material using a temperature PI controller and fan. However, setting the shape for nitinol requires a 500C oven and hours to heat the mold with the material. Using nylon means it is weaker per unit mass and conducts heat slower. Also, both materials are typically used in a spring form to get around the 2-5% strain shape recovery limit. Lastly, using nitinol as a spring leads to the actuator deforming as the attachment points at the end, and then it tears itself apart afterwards (uneven heating without pwm also leads to this).

# 246
>>11831
Also, the hand was made with a passive spring for the tendons on the back side of the hand. These kinds of materials are stiff when hot and can easily permanently deform if they don't travel all the way back when activated. There is the lack of precision when the material only goes back somewhat to the original shape, because the whole thing acts like a variable stiffness spring with an intermediate shape recovery phase. Due to this and the polycrystalline nature of nitinol in particular, the actuator is nearly impossible to move the same way every time for a given power level, not to mention how the material degrades over many actuations.

# 247
>>11660
I can't find the company that once made it available to the regular consumer, but it was in College Station Texas and they sold hydrogen fuel cells and generators.
I thought the energy:weight ratio was good and also the exhaust was literal warm/hot water (could be routed throughout the bot's body to give it a sense of warmth as well).
Batteries are too far behind imo, and using an ICEngine inside will be too loud and have the issue of monoxide in the exhaust.

Therefore, unless someone has a better alternative that isn't heavy batteries, hydrogen should be fuel and a hydrogen fuel cell our power source for our electrical generation.

# 248
>>11833
Yeah, these types of materials may find some uses for subtle deformations in some 2nd or 3rd-gen robowaifus in the future, but today batteries+electrical motors are by far the most functional (as well as likely the most economical) means of control available to us.

And the idea of intentionally adding excess heat into any system that has as a major goal power efficiency is pretty silly IMO. And thermal control near electronics is going to be a major design challenge for us for the foreseeable future.

# 249
>>11836
That's a pretty cool looking RC car Anon.

# 250
>>11837
Is there a better backdrivable actuator than a mini-cheetah style BLDC+planetary with a belt?

# 251
>>11855
Each joint type / actuation zone comes with it's own needs and limits, so ofc there's no 'one size fits all' answer Anon. For the four major joints, probably not. For other areas, linear screw actuators are very likely to be much better choices. 

While there's certainly general prior art (primarily in the field of animatronics) here, for the most part robowaifu-style design and engineering efforts are cutting new paths through uncharted territories. Kind of like the gold rush to the Klondike before most anyone even realized how much gold was to be had there.

It's going to be interesting finding out all these answers!

# 252
>>11833
I would never use Nylon to control a hand, but I still plan to try it in a limb as additional muscle, used in case something heavy needs to be lifted.

>>11836
Ethanol might make sense in some advanced robot, forget hydrogen. Also, maybe go for easy first.

>>11837
>adding excess heat into any system
We had this several times and keep disagreeing. No one can know that now exactly, bc it depends on the design. However, if a robowaifu has some SBCs and sits around then she won't get very warm. If we want her warm to feel human-like, we might even add a heater for water, which she uses while recharging her batteries. We might not need that with more powerful computers inside, burning more energy, but then bigger batteries will also be necessary.

>>11855
James Bruton made a video on cycloidal drives. His design is backdriveable. His argument was, that the reduction has to be at 10 or lower to do that.

# 253
>>11881
>using nylon as an additional muscle
>heat management system with water
At that point you may as well have an auxiliary hydraulic actuator, hooked up to the same pump.
>ethanol for power
Which way do you plan to use chemical energy for your system? One of the first robot dogs used a souped up lawnmower engine, so an existing ICE would be something to consider. Something that kills (most of my) projects is overcomplicating the design before the first prototype is made.

# 254
>>11902
>may as well have an auxiliary hydraulic actuator, hooked up to the same pump
Or both. 
>ethanol for power
I posted at least once, a video of two schoolgirls making their own ethanol fuel cell. Alcohol will be  necessary anyways, as disinfectant.
>overcomplicating the design
My posting was an answer to someone dreaming of using hydrogen. The earliest desigs of any robot should be plugged into the wall for energy, later work with batteries as soon as mobilty becomes an issue, obviously.

# 255
I was trying to find the perfect height for my waifu, but I got distracted by the importance of volume. This is one of the main factors that determines the feasibility of a design, increasing volume allow for more sensors, helps in lowering the density, permit more details, permit bigger actuators, improve heat distribution and permit for mods like finger guns. Although it has his cons, like higher cost, more mass (which this anon >>4313 explains why more mass can a good thing) and the squared cube law. Even then, more volume is like having more sheets of paper to do all the creative work needed for a waifu.

# 256
>>11956
put all the junk [spoiler] In the TRUNK[/spoiler]
potential for thicc waifus increases

# 257
Joking aside, has anyone considered an actuator based on the railgun principle?
The "payload" wouldnt leave the rail but would be tethered to a pully system to provide torque. Imagine the "rail" as the arm bone and the tendons being connected to a frictionless ballbearing inside. Now you have the idea.
Applications would be the same as how fast-twitch muscle fibers function. Might be useful and since it's based on electrical fields, "forcing" it backward or having unexpected interference won't risk breaking a gear or motor.

https://ieeexplore.ieee.org/abstract/document/7994470

>Unlike linear current Lorentz force actuators, μ-railguns generate forces proportional to the square of current producing very high forces and velocities when driven by ultrafast capacitor discharges. μ-railguns were fabricated on an SOI wafer with 15 μm thick device layer. A test set-up was built for high speed capacitive discharge and synchronous stroboscopic imaging of device under actuation. Initial results demonstrate μ-railguns with actuation velocity of 45 m/s at resonant frequency of ~1 MHz, nearly 2 times higher than possible with PZT piezoelectrics.

# 258
>>11962
Solenoid actuators seem to require a lot of power but they're quiet.
https://www.youtube.com/watch?v=xVk1CT3FWlo

# 259
>>11956
>square-cube law
Glad to see that physics itself is at the fore of your design thinking, Anon. You certainly can't violate them, nor even skirt around them. Nor will you ever be able to in this life. Our jobs here as Robowaifu Technicians is to work alongside them, and coax their 'lesser-observed' characteristics to come to the fore for the benefits of all mankind -- AKA, real, working, robowaifus!
>which this anon >>4313 explains why more mass can a good thing
Heh, I was pretty much saying just the ''opposite''. :^)

# 260
>>11960
Keeping as much mass as possible centered around the robowaifu's pelvis volume is going to turn out to be a fundamental design prerequisite in the end. 

''Thrown-weight'' (AKA, 'outboard-mass') is a well-understood concept in mechanics. The racing car industry has a really good example of the concept: ''lowered wheel mass''. Significant engineering expense is undertaken to keep the mass of the entire wheel assemblies -- anything outside the vehicle's chassis -- as low as possible. This keeps the inertia of these assemblies low, so the suspension responses across the roadway surfaces is nimble. This is a very important characteristic for traction and racing control.

This specific characteristic of mechanics will certainly apply to all our robowaifu's extremities' (limb) designs. KEEP MASS INBOARD. Well, as much as is feasible, heh.

# 261
>>11962
I mentioned solenoids a few times. They might be useful in some specific cases. Use Waifusearch to find the postings, if you want.
Small magnets are quite weak, though. Also fast movement with low ability to control often isn't useful. I wanted to do something like a magnetic train or so, but found ot it doesn't work, bc of the relative weakness of magnetic force: >>4429 - this is what inspired it: https://youtu.be/J9b0J29OzAU

There are small solenoids available on sites like AliExpress. I think these can be useful to block something in a mechanism. So for example it wouldn't be the strength of the solenoid holding something, but the strength of the metal it pushes out or pulls in to unblock something. This might also be useful to control which things a motor should move, so one motor could move something out of several parts or not dependent on a kind of solenoid switch.
Also for small but fast movements very small solenoids might be interesting, like pulling strings in the skin of the face, from inside the skull to create facial expressions.

Today I was also working on my eye design in CAD, where I still hope that I can move it with magnets one way or another. This might fail because of the lack of control, though. I have two ideas for how to approach this, one with motors moving the eyeball with a connected magnet. The other without a motor, but by small electro magnets switching on and of or changing polarity. (The reasons why I want that, are a design with fewer motors and a waterproof head bc cleaning in the shower)

>>11965
This is news to me, thanks. Very interesting. That might be useful in some cases. It's something I wished for, just didn't know springs can be build that way. That eliminates one of the limitations, which is fast movement between on and off. Might be useful in the hips.

# 262
>>11992
>Use Waifusearch to find the postings, if you want.
I got u fam (>>11996).

# 263
>>11992
What an adorabooty cutey! That Japanon's arts is amazing!

# 264
I'm impressed by Elon Musk way of thinking. It's not that he invented this but he has been so adamant about pushing it and I think made it clear and understandable. It's based on the idea that we should think from first principles. See what we want done then go look about all the methods of how it can be accomplished.

Due to this I think about actuators and motors a lot and just what are the limits to what can be achieved,

I think there's no way that anyone will economically be satisfied with any sort of pneumatic, hydraulic or geared type system because of a few facts.

Cost is one. Gears cost a lot to produce and are noisy.

I've been doing some thinking and drug up some facts that put what we need into perspective. Not that I know everything but just that there certain facts that steer us into different directions depending on what we are doing. What we need is the cheapest actuator possible and that could preferably be done at a cottage scale level to get started.

So what we have to do is work up from what power we need and then work from there.
So I look up how watts is related to power and find here,

http://www.kylesconverter.com/power/watts-to-foot--pounds--force-per-second

That  1 W = 1 J/s and

1 Foot-Pound-Force per Second:
    Approximately 1.3558179483314004 Watts (SI).

So 100 Watts to Foot-pounds-force Per Second = 73.7562

That's a lot of force 73 pounds. I then looked at electronics to control it and the first  MOSFET that came up cost 0.47 USD

Power; N-Ch; VDSS 55V; RDS(ON) 8 Milliohms; ID 110A; TO-220AB; PD 200W

So with 200W of power it's well able to control enough electrical current to get the force we need. I suspect in lots of hundred you could get double or triple the power rating at near the same price.

marketplace.machinecompare.com/infineon-mosfet-power-n-ch-vdss-55v-rdson-8-milliohms-id-110a-to-220ab-pd-200w-gfs-44s/29398

Someone earlier said that solenoids are not very powerful. I beg to differ. Solenoids are a class of electrical machine that moves things by attracting iron into a magnetic field. To show that this can be powerful look at Tesla new electric motor. It's a switched-reluctance motor which is really a solenoid in a circle where each notch on the rotor is attracted to a coil. (I want to add I know they have magnets in them to raise the starting torque but higher speeds are all done by the switched-reluctance part).

So looking at these motors here's Sandy Monroe who studies cars by taking them apart, making reports and also helping manufacturers redesign stuff to be lower cost.

https://insideevs.com/features/443775/tesla-motors-invertors-compared-competition-sandy-munro/

He has a chart that shows the Tesla 3 motor to be 258KW(345HP) at 27.99Kg(60lbs.)

That's enormous amount of power and strength. 

So for muscles we need 300,

"...There are about 700 named skeletal muscles in the human body, including roughly 400 that no one cares about except specialists..."

so 300 muscles times 2 MOSFETs for each muscle at 0.50 USD each is $300. Now if we can drive solenoids with them and solenoids are nothing but bars of iron then we could keep out cost way down.

I haven't looked yet at all the micro-controllers and how many it takes to drive each MOSFET but I do know that many have more than one pulse width modulation output and you might not even need that only a output and that some of these you can get for a dollar.

So I expect off hand less than $600 for the micro-controllers to operate everything.

Anyways looking at these numbers to me it seems that electric is the only way to go and that using gears is going to kill you on cost. I mean how much is it going to cost to have a reduction gear for every muscle? A lot. Even though some will not need it a lot will.

>===
-''rm fingerprinting URL params''
-''disable hotlink''

# 265
>>12014
I can't really follow your calculations here. Looking forward to see some test or early prototype. However, gears are not expensive. They can be printed, or metal ones bought from China.

# 266
>>12014
How many turns can you fit on a solenoid within the desired ampacity and wire gauge? What about cooling? What stroke length will it need? How long will it have to be? Something that works like a bicep muscle shouldn't need much of a stroke length but it does need a lot of force. I've never seen a solenoid used for anything beyond a valve.

[code]solenoid_force = (turns*current)**2 * 4*3.141592653589793*10**-7 * cross_section_area/(2 * length**2)[/code]

# 267
>>12014
>Tesla new electric motor. It's a switched-reluctance motor
Yes, I looked into it. Posted a video on that tech a while ago. It's not a solenoid, however. These are rather week, same will most likely be the case for "magnetic trains". Also it about relativity. You may be able to create a strong magnetic fiels, but then it needs to be shilded or the electronics around will need it. There's a reason why electric motors are being used, I found that out myself after trying to fnd a way around the noise and weight.

# 268
>>12062
"switched-reluctance motor"

"It's not a solenoid, however."

I looked up the definition of solenoid and you're right.

"...A solenoid (/ˈsoʊlənɔɪd/,[1]) is a type of electromagnet, the purpose of which is to generate a controlled magnetic field through a coil wound into a tightly packed helix..."

https://en.wikipedia.org/wiki/Solenoid

Yet in the same page it says,"...In engineering, the term may also refer to a variety of transducer devices that convert energy into linear motion.[4] In simple terms, a solenoid converts electrical energy into mechanical work..."

The way I understood what I said was in the more expansive use of the term. What I was trying to get at was, the force we can get with wire coils and simple iron. I used the tesla motor as an example of this. There's no set law that it has to be rotating. Have you ever heard of the work the elevator companies are doing used switched reluctance principles?

Maybe I used the wrong word but I still say that much can be accomplished with coils and iron leaving the cost of magnets out.

So here's one simple idea, but difficult to implement, make a Halbach array by stacking metal transformer cores and then injecting molten aluminum into them. They make motors like this now for stuff like vacuum cleaner rotors.

I do not claim I could easily design, or even have the mental horsepower to do it at all, but something like this could drop the cost of motors if you could raise the performance using the same principles Musk is using. I don't see why motors, solenoids have to always be just round coils.

What I'm, maybe not successfully, am trying to convey is that if people can get such high performance out of switched-reluctance motors, and they are, then there's no reason the same forces can't be tailored to solenoids.

I'm particularly impressed by the low cost and simplification of making motors and transducers by using more design but way less, and cheaper, materials.

# 269
I want to say something about gears. Gears are the most worthless nonsense. Look at a transmission in a car. You have this huge mass of metal with only one set of gears doing anything at all. The rest are just huge hunks of iron being towed around in the car. And even the two that are operating the only actual part of the metal really doing any work is one set of teeth and even then the whole face of the tooth is not even doing anything at all in helical cut gears to lower noise.

I don't know this for a fact but I expect the reason serious big ass machinery like those huge mining trucks and trains use electric drives for transmissions is because if they used metal gears the things would be so heavy they would have trouble hauling anything.

Yet electronics keep getting cheaper and cheaper. Think of the serious mass of horsepower you can run through a minuscule in weight 
Silicon carbide power transistors compared to metal gears. It's laughable.

A simple example look at this tiny thing,

SCTW60N120G2 - Silicon carbide Power MOSFET 1200 V, 35 mOhm typ., 60 A in an HiP247 package,

It can switch around 96 HP in this little tiny package, and yes I know there's coils of wire and iron cores needed with it but all the parts are operating together almost all of the time. Look at the absurd power tesla gets out of tiny motors.

Can you see a trend????

# 270
>>12131
Thanks for the research and explanations Anon. That kind of productive effortposting helps the entire community here, actually.

# 271
>>11992
>microsolenoids
I wonder how small we could get trying to miniaturize that tech and what the applications might be

# 272
>>12136
>
Now you're thinking. Have you ever read or heard of Feynman's talk "There's plenty of room at the bottom"?

https://en.wikipedia.org/wiki/There%27s_Plenty_of_Room_at_the_Bottom

# 273
>>12136

Here's some thoughts about magnets that I had after looking at magnetic strengths of various magnets, electromagnets, etc. and made some notes about.

https://en.wikipedia.org/wiki/Rare-earth_magnet

"..The magnetic field typically produced by rare-earth magnets can exceed 1.4 teslas, whereas ferrite or ceramic magnets typically exhibit fields of 0.5 to 1 tesla..."

So maybe rare earths are super strong but the cost is massive. The ferrite or ceramic magnets cost per magnetic field are far superior and may be perfectly fine for our purposes.

I noted earlier

Tesla 3 motor to be 258KW(345HP) at 27.99Kg(60lbs.)

but a human rarely puts out more than 400 watts in peak.

"...Normal human metabolism produces heat at a basal metabolic rate of around 80 watts. During a bicycle race, an elite cyclist can produce close to 400 watts of mechanical power over an hour and in short bursts over double that—1000 to 1100 watts..."

https://en.wikipedia.org/wiki/Human_power

So the tesla motor puts out 4300 watts/pound and  human puts out(at 250watts and 200lbs.), 

1.25 watts/pound

So there's a hell of  lot of room for using cheaper less specialized materials and you can still get far better performance than a normal or even elite athlete human.

So let's look at some ways of making fields for magnets and their strengths.

https://en.wikipedia.org/wiki/Electromagnet

"... ferromagnetic materials is that the B field saturates at a certain value,[2] which is around 1.6 to 2 teslas (T) for most high permeability core steels..."

"...The main nonlinear feature of ferromagnetic materials is that the B field saturates at a certain value,[2] which is around 1.6 to 2 teslas (T) for most high permeability core steels..."

Now think about this. The saturation permeability of iron and therefore electromagnetic force you can get acting on iron, like in switched reluctance motors, is way up there with the magnetic field strength of rare earth magnets. BUT rare earth magnets cost a fortune.

And furthermore the most powerful magnets made are nothing but electromagnets that are plates of copper with holes in them to push water through for cooling.

Bitter electromagnets

"...Both iron-core and superconducting electromagnets have limits to the field they can produce. Therefore, the most powerful man-made magnetic fields have been generated by air-core nonsuperconducting electromagnets of a design invented by Francis Bitter in 1933, called Bitter electromagnets.[25] Instead of wire windings, a Bitter magnet consists of a solenoid made of a stack of conducting disks, arranged so that the current moves in a helical path through them, with a hole through the center where the maximum field is created. This design has the mechanical strength to withstand the extreme Lorentz forces of the field, which increase with B2. The disks are pierced with holes through which cooling water passes to carry away the heat caused by the high current. The strongest continuous field achieved solely with a resistive magnet is 37.5 T as of 31 March 2014, produced by a Bitter electromagnet at the Radboud University High Field Magnet Laboratory in Nijmegen, the Netherlands.[26] The previous record was 35 T.[24] The strongest continuous magnetic field overall, 45 T,[25] was achieved in June 2000 with a hybrid device consisting of a Bitter magnet inside a superconducting magnet..."

https://en.wikipedia.org/wiki/Bitter_electromagnet

What I'm trying to point out is there are ways to get powerful fields and therefore powerful forces, with out using expensive materials. We should think about how to use these and I'm not saying this is easy but if you are traveling somewhere you need to look at the map and see which way it is you need to go. Taking off in the wrong direction may eventually lead you to where you want to go after wandering all over but it would be better to just head the right direction in the first place.

I'm also not saying that I have all the answers. My focus is to throw out some wild ideas that "seem" to show promise as being, cheap and effective for our purposes and at the same time try to think about the big picture or as Musk puts it "first principles". Now I have thought about this before Musk as have many others but the way he described this really somehow made it click in head and lead towards looking at things like,"what is the most magnetic field force we can get per material?" What is the cost per material? Stuff like that. And every time I look at some sort of actuator or motor I try to see "how much of the device is actually doing work and if it's not how can we get rid of it?"

# 274
>>12138
Very cool Anon. I didn't know anything about that. Feynman was absolutely brilliant, was a natural-born Anon **I'm sure his shitposts would've been epic**, and he played pool too. I wish I had been there at Caltech in his day (or at least at the local Pasadena pool beerhalls).

'''There's Plenty of Room at the Bottom'''
>''Richard P. Feynman''
>intro
>''I imagine experimental physicists must often look with envy at men like Kamerlingh Onnes, who discovered a field like low temperature, which seems to be bottomless and in which one can go down and down. Such a man is then a leader and has some temporary monopoly in a scientific adventure. Percy Bridgman, in designing a way to obtain-higher pressures, opened up another new field and was able to move into it and to lead us all along. The development of ever higher vacuum was a continuing development of the same kind.''

>''I would like to describe a field, in which little has been done, but in which an enormous amount can be done in principle. This field is not quite the same as the others in that it will not tell us much of fundamental physics (in the sense of, "What are the strange particles?") but it is more like solid-state physics in the sense that it might tell us much of great interest about the strange phenomena that occur in complex situations. Furthermore, a point that is most important is that it would have an enormous number of technical applications.''

>>12136
>
>hashes
96A8A9F76542AF775DFDD646347480B5
D2F3BEF3FE4719D5904D300B82034223

# 275
Sometimes the best example of what to do is seeing what, not to do. Here's one of those.

The Ford aircraft launching system uses a large rotating flywheel to store electricity and release it in large burst. It has a bunch of linear motors that switch to propel the launcher and move the aircraft.

Now can you see the stupidity of this? The linear motor has many many coils that don't do one damn thing except the brief moment that the propulsion shoe, (I think they call the launcher that attaches to the aircraft a shoe, I may be wrong), goes past that coil. So you have all these electronic switches and all these separate coils. It's stupid. And even worse. The nuke reactor they have makes steam, this is used to make electricity with losses of maybe 60% if they are real lucky, then there are another 5 to 10% losses in speeding up the big flywheel then another 5-10% producing the power and maybe 3-4-5% switching all these coils that are mostly not needed most of the time. An abortion of the highest order. I would be really surprised if 25% of the actual steam power the reactor made is actually used to launch the plane.

If they wanted to make it work properly they would either find a way to first,

make some sort of steam turbine or engine to drive a fiberglass chain to drive the shoe, or if they couldn't get that run a big set of electric motors that drive the fiberglass chain. (Remember if you are throwing away roughly 70% of your steam energy in the present system maybe you could make some very inefficient steam motor but would throw away all that other complexity.)

That chain should be fiberglass because this is on the ocean and fiberglass would last forever. Fiberglass has a far better strength to weight ratio than steel and you could mass produce the chain links very cheaply with only a few molds.

Every time you look at something see what you can throw away and still have it work and even efficiency is not really necessary as we need heat for our waifu's so losing some is not a problem as it will just warm them up for us.

The real measurement is cost, cost, cost and ease of manufacture which really means less cost. We should if at all possible use computing to control things because it can be tuned. So even if it sucks at first more programming or better faster computers can eventually allow smooth life like motion.

# 276
"At the size limit"

http://library.lol/main/96A8A9F76542AF775DFDD646347480B5

# 277
>>12141

Those books look super interesting.

Trimming, Miniaturization and Ideality

http://library.lol/main/D2F3BEF3FE4719D5904D300B82034223

# 278
>>12140
>"how much of the device is actually doing work and if it's not how can we get rid of it?"
this is so key it should be added as a guideline in our Codex [spoiler]or whatever we are putting together for that purpose [/spoiler]

# 279
>>12144
Very interesting post, Gromment-Anon. Good physics-oriented insights.

>We should if at all possible use computing to control things because it can be tuned. So even if it sucks at first more programming or better faster computers can eventually allow smooth life like motion.
I'm pretty sure that's the basic plan as it stands, but the primary challenge may turn out to be ''simplifying'' all the electronics concerned (as I feel you imply in general with the catapult analysis). Finding/devising simplified drivers that can both respond near-instantly to tiny control signals, yet can switch ''96 horsepower'' (!) on a dime (>>12133) would be a tremendously capable system, if tuned correctly.

As typical extremely-miniaturized integrated circuits today can literally switch billions of times a second, then ''"So even if it sucks at first more programming..."'' can be a likely scenario in very short order IMO.

# 280
"...primary challenge may turn out to be simplifying all the electronics concerned..."

I can't think of any way we can get the number of power transistors down "if" we want something that eventually looks life like.

So for the hell of it I look on ebay for MOSFETs for power control This is not exhaustive just a quick look. I'm looking at what they have and then plugging in the current capacity on these to see what we can use and how much.

I'm thinking we need to not go higher than 24V. I don't remember the numbers but  think at 48V or there about you start getting into some serious regulatory issues.

I'm using 1,000W for my power so at 24 volts we need 41.6 Amps. Now this is actually too high for the vast majority but I bet you save a lot by ordering masses of the same thing. I think I commented earlier that walking up stairs could use 400W or so but athletes use like 1,000 watts but only in burst. 250-300W is most super in shape people can do. The 1,000W value is so waifu can carry you.

So anyways I find. "20pcs IRF3205 IR MOSFET N-CHANNEL 55V/110A TO-220 HEXFET Power Transistor IRF"
for $7.77

https://www.ebay.com/itm/324328514167?epid=10012075082&_trkparms=ispr%3D1&hash=item4b837c6277:g:3wMAAOSwj8FfgkBP&amdata=enc%3AAQAGAAACgPYe5NmHp%252B2JMhMi7yxGiTJkPrKr5t53CooMSQt2orsSvhAqMt0wg86xg8aAkgjQJDywsOnzbh4ayEZL4zbJSbTA0pwdOno2SR7Ih5QUweFE8ZncCor1thGiSQZ%252FH%252FtkGS5dQHp2NA1f50dnZEGUQP3tjHc1MSatyTQ4VP9A4yg%252B9fKwU946LKrcsaqoQJQge8P%252F%252BI2V9VhusqWFnVv7pS1h7QgMVhFgwitGIi6e0AEcuMIcVtO2iBV1EN6rBQdgkkNTjYSaZSAycJz9ITMBi3fCKWZZTKDY8idwz9I2E3R9Rh3gGshbWpKqZwWtb%252BbDVDuweYOAIzdTwRe1iqh4fCEpNzFq4Fy3PoIIjF0wgi4mTmsi6FI%252BvYHFfxArcjwHzhdXAMTnQhE9je0zCn3JXPj8FCiVFJhCa8al5xLQp0lmD7yTr%252FcvytiU3uzR8KUdqYF7nK8I%252FmkPGAe06JDklLx2sedrNMTDvtS99h9rZIdQykaIQa65kw4j2gZHs3enyQI3DMI6xB7tAVC%252Bn%252Fp1h1bHYMNF5i3n9MN4suRZ5Gn8OSqrqb99b3WHhw7BTNHCtl1tSrPNL6ZCEyCviWvB5lXRBFU6V84iCZp9rhWw99EmGAIMh362gxlbz3CgaE2P%252BTHmxP8fqm6m%252Bzid0aXqIt0c3USZblxbMt4w7%252FDes8c%252FzL2JdLR0Y4QM7CxSSzhMBjVRJWo8%252B1UVAuhYJpovaE%252FS8Zi%252BcKwEXj5m4wYZ%252B4xbqZwg%252FZMCzKnuzhTDrUkJFJoMFcGwvTF%252BCIDaNGmTMXv0iW9%252FQOSHIO1IUmsZbwVn5v%252Bbw4qBcIXJB158wdlngHeL8sf9qgAPG7p%252BDcGCBSk%253D%7Campid%3APL_CLK%7Cclp%3A2334524

It sounds to good to be true but
I see several like this. The one above would cover our needs and we would need 600 of them. So (600/20)*7.77=$233.10

You very well might be able to get by with one if you are tricky.

Now you can use a mass of wires with a expensive CPU or you can use a bunch of distributed micro-controllers. I say that's the best way cause they are super cheap and programmable. They make it where all the muscles have a powerful micro-controller AND you can update the powerful main brain CPU over time and not have the rest of the body fall behind. I like the ESP32 It has 

    18 Analog-to-Digital Converter (ADC) channels
    3 SPI interfaces
    3 UART interfaces
    2 I2C interfaces
    16 PWM output channels
    2 Digital-to-Analog Converters (DAC)
    2 I2S interfaces
    10 Capacitive sensing GPIOs

WOW! and you can get for less than $9USD. They also have built in wi-fi so you could possibly have all of it's muscles work with the brain by wi-fi. If you don't want that you can use I2C interfaces. So at 300 muscles/16 PWM output channels, means we need 19 and at $9 each=$171

Very affordable. What I'm doing is just plugging some numbers in to see what can be done. Obviously there will be a lot of little stuff that will up the cost but you might could save a little here and there also. Notice the ESP32 has enough capacitance sensors (16) to give us real touch sensitivity.

https://randomnerdtutorials.com/esp32-pinout-reference-gpios/

Here's something that will blow your mind, well blows mine anyways. When we talk about the forces of magnetism I'm not sure that all of this has been really thought through. Of coarse it's likely that I just don't understand.

https://www.youtube.com/watch?v=eWSAcMoxITw

https://www.youtube.com/watch?v=rWxNlPnwHtw

https://www.youtube.com/watch?v=Bwws-LlBGNU

# 281
>>12149
another anon talked about preprocessing and relays. Kind of like how we're not conscious of every specific movement unless it's our first time, after that, it's a reflex.
Clusteranon touched on this:
https://alogs.theГунтretort.com/robowaifu/res/201.html#201

# 282
>>12179
Thanks, that's a good point. 

>that Гунт'd link tho
Those mischievous /cow/s are having their little joke again. Probably simpler for everyone to just do a little cross-link style Anon. >>201

# 283
Now I've seriously, with good reason, blasted hydraulics. I mean hydraulics suck but...never say I'm hard headed and won't change my mind if some other alternative comes up. Some guy has written a thesis and says he can get efficiency of 81,5% with some new fangled thing called a hydraulic amplifier. I have no idea what that is. I just read the abstract but if true this could be kick ass. You could print all the controls with a good quality 3D printer maybe and save a fortune. All the control lines instead of electrical and wires would just be cheap tubing. It would be super cheap. You still could use micro-controllers to have touch, positioning and feedback but this would cut a lot of complexity. 

 "System Configuration and Control Using Hydraulic Transformer"

Lee, Sangyoon (2018)

https://conservancy.umn.edu/handle/11299/199050

I just started reading this paper and saw,"...A trajectory tracking controller for a cylinder and force controller for a hydraulic
human power ampliﬁer is developed to demonstrate potential applications for the hydraulic
transformer. The controller developed proves that utilizing hydraulic transformer need not
sacriﬁce the control performance...", so this appears to be super waifuable and he has apparently made one f these already.

Sometimes these thesis papers get deleted after a short while so I would get a copy as soon as you can and save it whether you will read it right away or not.

# 284
>>12227
>Sometimes these thesis papers get deleted after a short while so I would get a copy as soon as you can and save it whether you will read it right away or not.
While this particular file is too large for AlogSpace's server settings (~22MB), in general I would highly recommend everyone simply post the papers here on /robowaifu/ itself. Both for the reason you mention, and b/c the board itself is regularly backed up by at least one anon. This means all the files are backed up as well. 

It's also more likely to attract researchers who may find our little project here interesting if google and others link to papers which are actually posted here.

# 285
>>12227
as someone who's always wanted to give hydraulics a fair shot (and to ensure a line leak doesn't sever an important appendage!) I'm very excited to read this over. Excellent find!

# 286
>>12227
>>12228
At the very least we can post the abstracts on the board, which certainly will benefit any potentially-interested anons here, and may also register the posting with the research hub crawlers.

'''System Configuration and Control Using Hydraulic Transformer'''
''Lee, Sangyoon''
>abstract
>''Hydraulic power transmission offers multiple benefits over competing technologies including an order of magnitude higher power density than electric systems, relatively low cost, fast response, and flexible packaging. Hydraulics are often used in high-performance mobile robots that demand power, precision, and compactness. However, typical hydraulic systems suffer from low system efficiency from the wide usage of throttle valves. The research described in this dissertation focuses on developing hydraulic transformers that transforms hydraulic power from one set of pressure and flow to the other set of pressure and flow to replace throttle valves such that a compact and efficient fluid power system can be realized. A dynamic model capable of capturing operating characteristics and losses is developed to establish a quantitative comparison between two major designs of the hydraulic transformer. A traditional design where a pump and motor are coupled together in a single package is chosen for the research. This design has three possible configurations with unique operating characteristics, and if these configuration modes can be switched, the resulting transformer is shown to be more compact and efficient. A trajectory tracking controller for a cylinder and force controller for a hydraulic human power amplifier is developed to demonstrate potential applications for the hydraulic transformer. The controller developed proves that utilizing hydraulic transformer need not sacrifice the control performance. Control methodologies ensuring efficiency of the transformer driven system are developed. Transformer operating speed is optimized to minimize the power loss through the transformer. Transformer configuration is switched actively to operate the transformer in its most optimal mode. These methods further improve the efficiency benefit of using the transformer. A hydraulic transformer system utilizing developed controllers compared against a throttle valve system tracking a trajectory with various loading conditions reveals that transformer system can achieve an efficiency of 81.2% which is more than threefold increase over the throttling system with an efficiency of 26.2%. This efficiency improvement is possible with the ability of a transformer to capture regenerative energy to reduce the net energy consumption. This dissertation successfully presents the controller development for a hydraulic transformer that captures both precision and efficiency.''

# 287
>>11881
Hydrogen is going to be the way.
>https://www.youtube.com/watch?v=07oVoABYr10
>https://www.youtube.com/watch?v=gd9d_BAXWvg

Although, I think a wire pulley system POWERED by some sort of hydrogen fuel cell will be better.
>https://www.youtube.com/watch?v=BRpUcKsvr4I
>https://www.youtube.com/watch?v=aLaqMreVj9o

If anons think it too complicated, I myself will probably drop the current "battery tech" in favor of small gas 2 stroke engines. Starting with drones.
Although, there are still some hydrogen fuel cells available for sale.

There is a slight conspiracy going around with the hydrogen tech.
The hydrogen was stored in hydride containers that basically prevented the risk of explosion.
These hydrides (I think it was lithium hydride) was used in nukes and supposedly is illegal to buy and sell, but... legal if you make it on your own.
The idea from B0b L4z4r:
>https://www.youtube.com/watch?v=Ytg23mDd1a4
The old rc car:
>https://www.youtube.com/watch?v=S9UnqW6wrxI

The company went relatively quiet when it started to gain traction, but Elon and other powers at the time were shelling out big money to keep hydrogen tech out of the public sphere.
Old tumblr of the company. (horizonfuelcell)
>https://horizonfuelcell.tumblr.com/
Random old article
>https://www.rctalk.com/horizon-h-cell-2-0-hydrogen-fuel-cell/
Actual site of the original company. (There was another site a few years back, but it was when they were trying to get military contracts)
>https://www.horizonfuelcell.com/mediacoverage
If someone can find the old military oriented version of their site please post it, I can only find vague references.
>https://www.sciencedirect.com/science/article/abs/pii/S1464285914700677

I can't be the only anon to remember this, I remember this was a HUGE deal at the time.
They have "moved" to larger projects, but I just can't believe it's near impossible to find the old kit (even if used).

FOUND THEIR OTHER SITE, seems like the military references are gone now.
>https://www.hes.sg/

# 288
>>12232
Found it, the full kit is probably close to $2k.
>https://www.horizoneducational.com/horizon-h-cell-2-0/p1233?isList=1
>https://www.horizoneducational.com/hydofil-pro/p1221?isList=1
This 100% needs to be the powersource of our bots, it would be lighter than batteries and longer lasting. The "exhaust" is basically heated water.

# 289
>>12232
>electrolysis engine
fascinating

# 290
>Grommet
>>12131 and following
The way how the discussion was going on here was really kind of annoying to me, tbh. You use examples of big machines, systems using high current, jump to small insects, to a scientist which worked on quantum theory. You mention things, jump to conclusions, don't explain what you're talking about. You claim established methods like gears are just nonsense, but only vaguely hint at alternatives. Another thing is, that there are no drawings to explain how something could be used.

Some of your mentions might be useful. These Ed Leedskalnin experiments might ge useful for a holding mechanisms, but in addition to other muscles. I'm also going to look into some other things you mentioned here. However, there's no clear path how to use these concepts, and it might even not be possible. Aside from other considerations, like having strong magnets near electronics and how these mechanisms would influence each other, if the robowaifu would move two of those close to each other.

>>12231
>Abstract
Great. But: What? How am I supposed to imagine that?

>>12232
I think this posting belongs rather into the energy thread >>23

>>12136
>microsolenoids
They would be weak and also the metal rod couldn't hold much if a force would come from the side. Maybe going towards piezoelectric versions would be more interesting for small movements. I think I posted something from Festo before.

Magnetic microrobots might be useful for internal cleaning. I think I mentioned that before. If you want to use magnetism in muscles, maybe that would be of interest:
https://youtu.be/2TjdGuBK9mI
https://youtu.be/Y_uyCcXMJR0
https://youtu.be/N7lXymxsdhw

I don't know if we should have a separate thread for speculative magnetic muscles, mechanisms and such, because it might be hard to draw the line. But this here is quite a mess, in my opinion. Maybe this thread should contain the postings referring to some common technologies in robots and also relatively specific ideas how to use some specific technology in a new way, while general hints at physics and for example big machines or interesting mechanisms could go into a separate thread on experiments with magnetism.

# 291
>>12260
>Great. But: What? How am I supposed to imagine that?
It's possible the word 'abstract' may have slightly different meaning here Anon. It's a commonly-used term in the scholarly literature that basically just means 'summary'. It's a way for anyone who might conceivably be interested in the material found within the paper itself to quickly decide if it's for them or not. It's sort of like a sales-pitch for the paper, if you will.

# 292
>>12261
I didn't mean the definition of the term abstract. The text is hard to parse for beginners and laymen.
Hydraulic pressure intensifier: https://youtu.be/DnZBiGE1W7I
Hydraulic transformer: https://youtu.be/D1895LTuJ_M

# 293
>>12311
>I didn't mean the definition of the term abstract. The text is hard to parse for beginners and laymen.
Ah I see. I beg your pardon then Anon. Yes, it's true that clarity in writing is as much an art as a skill. It's certainly something I'm daily challenged with in my own scribblings! :^)

# 294
7 strange new electric motor designs: https://youtu.be/DBxyoB0uq24 - mostly to big for us, but the video explains some principles like axial and radial motors. Maybe some of the designs will be used in smaller motors. The one from https://magnetarplus.com/ might be in our range of interest.
More and more designs are using printed parts (not hobbyists printers, and also metal). This technology allows more innovative designs.

# 295
>>12350
Looks amazing, thanks Anon.

# 296
>>12260
"...The way how the discussion was going on here was really kind of annoying to me, tbh. You use examples of big machines, systems using high current..."

The high currents directly follow from the fact that we have to use low, or reasonably low, voltage. I read that climbing stairs can use 400W of equivalent in humans so we have to have high peak currents even though it would not be the normal usage. I also am thinking about funding. If we can make the waifus powerful enough to pick up and carry people around there's a vast, huge unbelievably large market in taking care of older people. I mean this market is vast and if we can use it to piggy back on our waifus it will make things  a lot easier. That's one of the reasons the hydraulic link that says you can get 80% efficient hydraulics interest me. 

Hydraulics have high power in a small package but presently they have awfully efficiency and use a lot of power. Batteries are expensive but if we had efficient hydraulics we could use air bladders or tanks to store hydraulic power for peak power while using low cost electrical driven pumps to charge them.

"...jump to small insects, to a scientist which worked on quantum theory. You mention things, jump to conclusions, don't explain what you're talking about. You claim established methods like gears are just nonsense, but only vaguely hint at alternatives. Another thing is, that there are no drawings to explain how something could be used...."

I can see how it looks just reading one comment of mine but further up I've given a mass of links on all kinds of stuff that could be alternatives.

"...You mention things, jump to conclusions..."

What may seem like jumping to conclusions is really just a general knowledge of looking at different type actuators, power systems and having a general knowledge of their strengths and weaknesses. If you read up on this stuff you will see that I'm basing what seems to be "jumping to conclusions" on standard facts that you can read about. A lot this comes from stuff like Engineering Design" magazine, "Electronic Design" and various trade magazines where they have a lot of articles on stuff like "what are the strengths and weaknesses of different electric motors" or "What's the best transmission or power conveyance for your application". 

A large part of some of these short comments are to talk about cost and efficiency.

Notice I went into fairly decent detail on cost on some comments. I did not go through gear costing because...they cost a lot. Some of this you will have to look up. My aversion to gears I stated earlier. They are noisy, need grease, expensive and I commented that I didn't want a waifu that "sounded like a washing machine". Of course someone readily piped up that some people are turned on by washing machine sounding waifus so what do I know.

"... jump to conclusions, don't explain what you're talking about..."

I mostly am talking about "Actuators for waifu movement!" which is the thread title.

"The There's Plenty of Room at the Bottom"
Richard P. Feynman
 reference was really about how to think about the problems we have which is just as important as the actual building...more actually.

We have to find a way to make things easy to put together, cheap, cheap, cheap, did I say cheap and we really have to have a major simple foundation that I think starts with the actuators which is why I talk about it so much. To be lifelike we need about 300 muscles so it's a major deal.

You must realize that I'm throwing ideas out there and trying to show what "might" be possible. I'm not even close to the stage of building this so you're not going to get build instructions. At least not from me.

This also means a lot of what I will reference will be scientific papers and articles on basic stuff and I'm not going to cover a lot of the background on the technical aspects because it's just too much damn work. It would be a full time job and I would starve at the wages I'm receiving for doing it. Not that I would be any good at it anyways.

Posting the papers. I haven't because I didn't want to use up other people's server space when there's a current operating link.

# 297
>>12350
Very cool motors.

# 298
>>12365
'''POTD'''

>If we can make the waifus powerful enough to pick up and carry people around there's a vast, huge unbelievably large market in taking care of older people. I mean this market is vast and if we can use it to piggy back on our waifus it will make things  a lot easier.
At last, someone else here has said what I have all along: "The entities that capitalize on robowaifus ''first'' will have many literal billionaires among their founders. This industry will become yuge, second only to food production in the end." The medical usage of robowaifus has always been a fundamental key to our industry. The based Nipponese already have a national-tier program to develop them that's been slowly progressing for more than two decades.

>...Engineering Design" magazine, "Electronic Design" and various trade magazines
Ahh, a fellow engineer I see.

>Of course someone readily piped up that some people are turned on by washing machine sounding waifus so what do I know.
OK, I lel'd there.

>was really about how to think about the problems we have which is just as important as the actual building...more actually.
< ''more'' actually
Pretty insightful IMO. Certainly at this pioneering stage this is true. Much of what we need to accomplish here involves contriving mechanical and algorithmic systems into novel and unique arrangements, which have never been arranged in ''just that way before'' (humanly speaking, ofc). Frontiersman are basically always fearless innovators, and it's no different here. We need to be both bold and inventive to succeed here. Add on to that requirement the basic need for 
>''"...using the technology of '''today''', not tomorrow."'' 
and it's apparent we really have our hands full here. Given the fact not a single group has effectively achieved this before in history, and the fact we're __also in a race against time before the Globohomo Big Tech/Gov literally ruins any hope for humanity's future regarding this advance__, and I'd put us personally into the realm of "O Lord, please help us! We need your grace and wisdom here! Thank you for a miracle!!" I know that's my prayer, at the least heh. :^)

>We have to find a way to make things easy to put together, cheap, cheap, cheap, did I say cheap and we really have to have a major simple foundation that I think starts with the actuators which is why I talk about it so much. To be lifelike we need about 300 muscles so it's a major deal.
Every point is obviously on-point.

>Posting the papers. I haven't because I didn't want to use up other people's server space when there's a current operating link.
I mean, after all. We live in a society right? Any/everything that can possibly be contrived to produced something that the Big Tech/Gov deems ''verboten'' for the masses to acquire...I mean what could possibly go wrong? I'd suggest we distribute our own copies of papers and every other takedown-susceptible resource that we can here Anon.

Regardless, great post. You encourage me.

# 299
>>12369
seconded

# 300
>>12365
>To be lifelike we need about 300 muscles so it's a major deal.
I'd like to interject that my instincts tell there is absolutely no way we'll be able afford that many reasonable-sized actuators in our early 'Model T' robowaifus. I think having 50 would be pushing it to some kind of extreme, but I'll grant it's potentially feasible. We'll need probably 14-15 to cover both hands, probably 8-10 to cover the face. Everything else will need to be accomplished with the remaining budget from 50 actuators. Again, I believe that total would be really pushing it too.

# 301
>>12385
>"...I'd like to interject that my instincts tell there is absolutely no way we'll be able afford that many reasonable-sized actuators in our early 'Model T' robowaifus..."

I don't disagree at all. Even in the slightest.

My point about the 300 muscles was just a search on how many muscles are in the human body and someone said 700 of which 400 were specialized that no one really cared much about.

I also like to use 300 and then plug in the numbers in on MOSFETS just to see what it would cost. It's actually affordable.
>>12369
"... we're also in a race against time before the Globohomo Big Tech/Gov literally ruins any hope for humanity's future regarding this advance.."

Sigh...they will kill us all. And when they get done with us because they are psychopaths they will start in on each other and the human race will disappear.

It's very sad. I try not to think about it too much because it makes me extremely sad. Like depression level sad. 

There's so much potential that is available on earth for everyone to have at least a decent place to live and food so that they won't starve(Keep in mind I'm in no way some super green liberal anti-tech guy. My whole out look is based on the idea that with advances in knowledge we can get super high effectiveness out of what we have already. Read Buckminster Fuller for lots on this and that way of thinking).

"...Much of what we need to accomplish here involves contriving mechanical and algorithmic systems into novel and unique arrangements, which have never been arranged in just that way before..."

EXACTLY. The potential is there.

 We are very close to this. There's a huge amount of smaller type fusion start ups, solar is booming and cost are plummeting. Battery cost will eventually plummet also. I see all kinds of advances coming up that are seriously cheap.

The problem is the assholes and psychopaths who will ruin everything because they are obsessed with power over everyone else.

# 302
"... having strong magnets near electronics and how these mechanisms would influence each other..."

Shouldn;t be a problem as all our efforts will be to keep as much magnetic field "inside" the actuators where they will be useful in the first place instead of radiating the area around them.

# 303
After reading up a little on hydraulic amplifiers I think they will be way, way pricier than anything we are looking for unless someone can come up with a way to print them at low cost.

It may be that something like can be used if they are made of plastic and you could mass produce these???

There's a problem at the macro scale though. A big one. Every time I see hydraulic stuff I always come back to the fact that some signal or driver must be used to open the valve to let fluid flow. Now at that point it still means you need a transistor or MOSFET to do this and since the cost of these is less than .50 cents USD and they can drive a huge amount of power then...why use it to drive hydraulics???? Why not find a way to directly drive some sort of coil and a reactance motor, solenoid, etc. We've seen the power Tesla gets out of their motors. (Tesla motor puts out 4300 watts/pound and  human puts out(at 250watts and 200lbs.),1.25 watts/pound). We could have plenty of power even if we are way less efficient than his stuff.

The same goes for gears. You have to drive the gears with something and you are right back to the same problem where you need a switch to drive the motor and then gears to transfer power, I mean your just adding stuff you have to figure out instead of just solving one problem now you have solve a bunch of them.

# 304
>>12389
I'm currently toying around with a linear actuator system that uses 10 dime-thin actuators circling in a ring around the torso volume, and connecting the pelvic section & the chest section ala Anon's OSMR design. (>>12165) Each actuator will be roughly 1 foot in length for the outer casing. I'm hoping for approximately 6 inches of throw (or better) internally on the actuator rods. 

Can you think of an actuator design that works on the principles you are promoting, rather than the more mundane (and slower/noisier) screw-type design?

# 305
>>12390
> OSRM*

# 306
>>12389
>>12390
As one addendum for you concerning my design proposal, is that the arrangement is effectively a Stewart Platform. (>>8648) This is already a well-proven mechanical design for a number of applications. This one should be right in line with it's strengths.

# 307
>robowaifus carrying people
>founders will be billionaires
Reality check: Robowaifus will need some optimization. Other (humanoid) robots might be better at doing something else. The construction of such systems might differ a lot. I just realized, we're getting off topic.

# 308
>>12390
Helical or heringbone gear to a linear rail? Also, the actuators which use metal screws in printers aren't that loud, it seems to depend on the driver. Maybe you could also insulate the motor from emitting noise, while keeping it cool of course.

>Grommet 
Could you please try to avoid Reddit spacing. Fewer empty lines. Thanks.

# 309
>>12400
>>Grommet 
Could you please try to avoid Reddit spacing. Fewer empty lines.

No I can't do that. Not because I'm evil but because there's just no way to do this without walls of text that no one can read.

A lot of stuff I write about tends to be a little odd or novel and it's too difficult to narrow this down in super succinct verbiage. Read that as in "I'm not smart enough to do that".

 An example. I say gears suck...and that's all. Of course then I get lines of "gears are wonderful", "gears are perfect", "why are you bashing my precocious gears", "etc., etc.

So I try to explain myself fairly often and to do so it just can not be helped that it will run into a few lines of text. I have in this thread ideas which I talked about but since I didn't go through and specifically reference what I wrote before in this thread I get grief for not explaining everything.

There is of course no pleasing everyone so I try to break things up into ideas or like I'm speaking and add a space where I would pause if I was actually speaking. I think that's the best I can do for someone who's not really a writer nor a scholar.

# 310
>>12390
"Can you think of an actuator design that works on the principles you are promoting, rather than the more mundane (and slower/noisier) screw-type design?"

looking at
>>12390

I'm not sure I understand your comment "dime thin actuators", could the thin part be that of a tube being a dime thick???

Well anyways I think you can build the whole torso with a backbone made of sockets and balls, then have three strings . One in the back , and two on the sides towards the front.

I made a drawing. Damn it no grief over this. I did it online with a track ball. I started it and it went ok but somehow the "mode" got stuck on some bizarre mode that I couldn't get out of that made it where I couldn't use the pencil. So I didn't really finish but I think I can explain it.

First drawing on left.
See there's a ball and two sockets. Just one section of a backbone. You see the holes in the front and the one hole in the back. Strings will go through these vertically all the way up the backbone.

Second drawing moving to the right. I show it with just plates to simplify for the next two drawing, but it's the exact same thing as the first.

The third drawing
I show pulling on the front two strings and loosening the tension on the one in the back. This makes the torso lean to the front or towards you as you look at the picture. You can see the "pitifully" drawn strings and arrows showing them pulling.

Now moving to the right you see a half drawn even worse drawing(this is where the "mode" got stuck in some odd ass brush that I could not get it to undo) anyways, this time the string on the front right is pulled down and all the tension is released on the left and half the tension on the back. This makes the backbone articulate towards the right as you are looking at it. I couldn't draw all the strings because..well it screwed up on me so you will just have to imagine them.

Basically we have a socket with three directions that can be tensioned so that it can move in any direction, front, back, or either side.

Now all you need to operate this is three motors with string tied to pulleys on them that take up slack on the strings by rolling up or unrolling string depending on which way they need to go. The other end of the string is fixed to the top vertebra and the pulleys are on the bottom in this case in the hip.

So the whole torso is three motors.

Alright let's extend this to the whole body but neglect fingers and toes. Only hands and feet. So we need three motors for each major limb, head, torso, I get 14 for the whole body so 14 x 3 motors each gives you 42 motors for the whole body.

For the hands and feet if you have one thumb or toe and two fingers  you could probably manipulate whatever you wanted so that's another 3 x 4 for hands and feet, 12 added so 3 x 12=36 motors.

Now this would work fine but look a little retarded as every single motion would be an arch. So the spine would be round when it articulated.

I have a bit of a kludge idea how to make it look natural and only use three motors for each finger and each toe.

At each joint of the finger have a solenoid that pulls a wedge down on the rope so that it stops. This means you could pull the finger in a little then stop it pulling the top or end of the finger but it would still pull close the hand with the next joint down.

Like I said it's a kludge and I don't like it but it is cheap and would work but it only saves you one transistor and we already see that these are super cheap.

It's going to be tough to find motors with the power we need without using the dreaded gears.

I looked briefly at DC motors on ebay just to get some numbers. I found a $12.00 motor with these specs

DC 36V, current 0.20A, speed 9000RPM

Now I "think" we can use Watts as a short hand for force. I mean an instantaneous force. Like how much someone could pick up and hold in place.

(I may be getting this wrong but I think it's right)
The actual force would be in Newtons. It says about watts that

"...When an object's velocity is held constant at one meter per second against a constant opposing force of one newton, the rate at which work is done is one watt..."

Now here's the problem. This definition above I read as you are accelerating at one meter per second against one Newton of force. Now what we want is not acceleration but the actual force that we can pick up and hold. Not acceleration. Yet when you look up "instantaneous force it says,"Power is given as the rate of doing work. In an electrical circuit, the amount of electrical energy dissipated by the load is known as Electrical Power. In an AC circuit, the instantaneous power is given by the product of an instantaneous voltage across the load and the instantaneous current passing through it. "(that's watts but I don;t know how to translate that straight to force to pick up something.)

Here's the problem we're looking for pound-force which is directly related to Newtons at a rate of 1N=0.2248089 pound force and one watt is equal to one N but they give it as accelerating.

I think as a rough guide we can use the newton to pond force and just call whatever Newtons needed watts but I'm not at all sure about this.

How they can call Watts an instantaneous force yet elsewhere call it not is confusing me and it will have to be resolved. We need to be able to use watts as a reference on how much weight a waifu actuator can move.

https://en.wikipedia.org/wiki/Newton_(unit)

https://en.wikipedia.org/wiki/Watt

and yes I do understand watts are based on force and time but  I'm trying to take out the acceleration.

I'm not explaining this well. If you go to this site and type in Newtins to directly get an equal force or weight in pound force 

https://duckduckgo.com/?q=newton&t=ffcm&ia=answer

it's clear but then when trying to equal that to watts you can not directly do so.

I'm supposed to know this but I don't. Someone please explain how to get a pound force using watts as a reference unit.

# 311
I'm looking at torque here

https://en.wikipedia.org/wiki/Torque

and it says "...Also, the unit newton metre is dimensionally equivalent to the joule, which is the unit of energy. However, in the case of torque, the unit is assigned to a vector, whereas for energy, it is assigned to a scalar. This means that the dimensional equivalence of the newton metre and the joule may be applied in the former, but not in the latter case. .."

but one Joule for one second is equivalent to one watt so I think if we plug in a pound force and convert it to Newtons we will get an accurate amount we need rated in Watts. An example

200 pound force equals 889.6443 Newtons so if we were to have a motor that held up 200 lbs. for one second we would need a 889.6443 watt motor. Now if we have the voltage and current for this motor we can predict the force it will lift in pounds.

So let's use the same numbers. Let's say we have 24 volts and we want to hold up 200 lbs.

889 watts/24 volts=37.0 amps

so we would need a 37.0 amp motor to get enough force at 24V to lift 200 pounds.

Is this correct?

# 312
>>12406
An articulated chain of ball-and-socket joints with integrated clutch plates is a good idea Anon, thanks! I'll consider that a primary load-bearing element to stand in where a normal human spine would. The linear actuators (probably only 8 needed now) would still circle the perimeter of the mid-torso. Their biomechanical-replacement function would sort of stand in for the the pelvic and back muscles. One of our challenges here as designers and engineers is figuring out how to mimic our human motions with mechanical actuators, and still leave volume in the interior to hold batteries, electronics, cooling mechanisms, etc., etc.

The torso is an obvious 'spare' volume design target, and this is simply my attempt to work towards that intermediate goal. And BTW 'dime thin' was referring to the outer diameters of both as being similar. I apologize the for the confusing terminology on my part.

>>12400
>Helical or heringbone gear to a linear rail? 
Whichever turns out to have the best compromise of energy/weight/speed/strength/volume/noise aspects. 

I'm not smart enough to just guess correctly. 

Only testing would really point us in the right direction.

My instinct is that the ball-bearing ones will offer better strength/energy aspects though.

Possibly other types ofc.

The basic point of my post 
>''"Can you think of an actuator design that works on the principles you are promoting, rather than the more mundane (and slower/noisier) screw-type design?"''
was to inquire if Anon could think of a ''non-traditional'' linear actuator, rather than the ones you suggested.

# 313
>>12409
>Is this correct?
Even if your ratio analysis and math numbers are correct Anon, seems to me that there's the basic point of mechanical design to consider. Much like Anon's clutch-plates mechanism (>>12406), braking mechanisms such as disc brakes, clutch plates, locking pins, etc., can be utilized to transfer force from the hands alone (which seems to be case for these calculations), and out into the mechanical skeletal framework itself. 

A robowaifu's skeleton is much better suited to passively supporting weight at the end of an extremity, rather than just her 'muscles' alone.

Make sense? Just ask rock-climbers about this, BTW.

# 314
I got locked out because the inpenetrable captcha kept giving me horrible pictures and it said I need an "unblock" or something. Sigh.

An articulated chain of ball-and-socket joints with integrated clutch plates

I didn't make it clear because I was simplifying but the balls would probably not be round but more squashed. They could also be just made of rubber or silicon just like humans.

Hmm...maybe balls in between two large washers with the bulk filled with silicon. The silicon would act as a spring. 

Otherwise just three ropes pulling  you could never tell what joint would curve first. With silicon(a spring) it would press on all of them so they would curve equally.

The (terribly drawn)drawing I'm adding shows just the plate in the top left. Then below it shows one corner which has been cut away with the rope in it and schematic draw wedges. To the right is just the hole minus the rope for clarity(if any of my drawings can be called clear :) ). It shows wedges that can be pulled up or down depending on which way you want the joint to jam.

I really don't like these wedges but it's what I have right now. Need to think of something better.

Another idea. I'm surprised I haven't thought of this before. 

Now I don't like gears because of the noise and trouble with them but I'm certainly not against transmissions.

Now we all know a low torque small motor can have a great deal of pforce if it's geared down and a lot of tiny motors can run real fast meaning we could have a substantial amount of force if we could find a way to gear them down. After drawing the string pull spine joint I realized we could do this with an ancient type of gearing.

The Chinese windlass, who I think invented it, or a Differential windlass. What a great thing. You can get massive force with this thing. There's an explanation at this link. Do a little math and you will see it has a great deal of force and since little motors run so fast it would still have enough speed.

https://en.wikipedia.org/wiki/Windlass

I'll also add in a link probably one of the most ingenious transmissions ever invented. Why this is not used everywhere, I don't know. It's brilliant. I wonder if there is some way we could simplify this to work. Check it out.

http://www.rexresearch.com/constran/1constran.htm

# 315
I forgot to add about the link

http://www.rexresearch.com/constran/1constran.htm

the transmission can have it's ratio changed very fast. What advantage that would be would it would be much like a human arm in that it could move quickly with little force against it but as force is needed it could slow down and push harder.

# 316
>>12471
I think some variant of windlass could indeed be very useful for being able to lift heavy weight relative to robowaifu's. Carrying a full-grown man, for instance. I've actually used block-and-tackle gear on a farm before to pull engines, and it really does work. The engineering trade off comes with the slow rate of progress. It's a pretty common characteristic of basically all fundamental machines (levers, screws, wheels, incline planes, etc) -- higher force == faster rate, lower force == slower rate.

As you've already pointed out more than once ITT, it's ''power efficiency'' that will matter most in the end. We have to carry our power packs around with us on our robowaifus, and we'll need to use the system that delivers the most Newtons force for the least Watts electricity.

I'm still quite interested in the high-current solenoids using magnetism for linear actuation directly. Any intervening mechanical systems are inevitably going to result in friction waste, and are likely to burn through our available power budgets more quickly.

# 317
>>12478
lel. i screwed up the formatting, but I'll assume the message came across regarding the force/rate relationships.

# 318
>>12478
"...I'm still quite interested in the high-current solenoids using magnetism for linear actuation directly. Any intervening mechanical systems are inevitably going to result in friction waste, and are likely to burn through our available power budgets more quickly..."

Yes. Very much so.

I'm extremely enamored of switched reluctance motors. It seems to me the low cost of micro-controllers and MOSFET's has made them the lowest cost, most powerful and most versatile motors around. These can be made with some hunks of iron and a few coils with no expensive magnets needed. The idea I had about using a line and reeling it in around a motor could possibly be used as an actuator which would readily fit the action of a normal muscle. I don't think reeling a line around a pulley on the motor would take up much in the way of friction at all if any worth counting.

https://www.controleng.com/articles/resurgence-for-sr-motors-drives/

One thing good about these motors is we can get super high speeds and trade some of this speed for more force if we are reeling in lines as muscles.

# 319
>>12389
Elon announced today they're going to use electromechanical actuators on their Tesla bot.
https://youtu.be/j0z4FweCy4M?t=7628

# 320
>>12496
>related crosspost (>>12492)

# 321
>>12482
>I don't think reeling a line around a pulley on the motor would take up much in the way of friction at all if any worth counting.
Certainly the ball-bearing based fishing line takeups on good fishing reels seems rather low friction, so yea.

# 322
Checkout twisted string actuators. They're incredibly light, efficient, and cheap for the large force and stroke they can provide.

# 323
>>12683
Thank, already have them on my radar. You probably mentioned them before? But I wonder about how long they would last and how precise they are. These are the other factors to take into account. 
Then there is this channel here, which seems to have some content on wisted and coiled polymer and other stuff like that: https://youtu.be/IYChiT1CcNc
Also related: https://link.springer.com/article/10.1007/s41315-017-0022-x

# 324
>>12683
It is an idea that seems to be reasonably light + efficient. There are two issues with it as is, that would need to be solved, AFAICT.
1. Super-coiling. Maybe some kind of narrow guide tube or something to constrain the effect? Not only does super-coiling mess with the smoothness of the motion, it also greatly increases the likelihood of a tangling-up. It also tends to send the line-of-force off in an undesired direction.
2. Gravity/Inertia. Again, maybe the self-same guide tubes? Unlike the cherry-picked, purely-vertical lab example pictured, inside our robowaifus the twisted-string actuator mechanisms will need to function well at literally every possible angle inside them, and under (potentially) widely-varying overall system dynamics (including lifting loads, running, jumping, **raucous fugging**, etc.)

# 325
>>12683
twisted string actuators

Yes those look excellent. A built in transmission for force amplification.

I just had an idea. What if you used two motors. Say you had two strings just like you showed with the twisted string actuators. One motor would wind up both strings at the same time(no force amplification). The other though would twist. So you could have rapid movement of the limb or whatever then when it needed power it could activate the twist motor and have more force.

# 326
>>12737
Neat. That sounds like an innovative approach to dual-force actuator systems anon.

# 327
>>12685
>Longevity
I'll need to build a  test jig to figure that out. Thanks, I didn't even consider that.
>Precision 
This can be compensated for with PID control. 
>>12689
>Super-coiling
As long as the servomechanism doesn't require a contraction into the that range, it's no problem. I'll design around it.
>Gravity
There will need to be an agonist and antagonist pair, just like with human muscles. I'll try coupling the motor to two twisted tring actuators that oppose each other. Also, thanks for mentioning the possibility of entanglement. I'll need to ensure they enclosed.
>>12737
So, one side is a winch and the other is a twisted string actuator? That could provide similar functionality to humans compliment of fast-twitch muscles and strong skeletal muscles. Though an exceedingly clever idea, is there anyway to prevent the twisted string actuator from pulling string off the winch?

# 328
These  twisted string actuators can be super strong. I like to look at stuff like that. Ancioent ways they moved heavy stuff etc.

I saw a video where this guy lifted a heavy log like this once. He built a A-frame type tripod(or quadra-pod t-pee type frame, can't remember) over a log then used a wire which he twisted with a stick stuck through it. It was a lot of weight and he lifted it just with this simple stuff by hand.

# 329
"... is there anyway to prevent the twisted string actuator from pulling string off the winch..."

Maybe I don't understand what you are asking because my first answer is...a knot.

# 330
Oh I think I got it. If it twist it would walk off a pulley. Duh sorry I didn't see that.

Well if you ran the strings through a couple of holes "before" they went around the pulley that would do it. Twist on the other side of the holes before it goes to the pulley.

I still think that if you could come up with a way to 3D print a simplified version of this link

http://www.rexresearch.com/constran/1constran.htm

that I referenced here
>>12471
you would have it licked. Period. Done.

The problem is this thing is hard to get your head around. I understand how I could make one of these but simplifying it would be exceedingly hard and take some serious thought. This thing is the perfect transmission which is self regulating, light and can go very fast or very slow with great power. The guy who came up with this, George Constantinesco, was a serious genius.

General Motors of course ripped this guy off. They took an option to use it in their cars then...did nothing., Of course he was expecting them to use it in all their cars so he took on debt to do further research and build factories, etc. and when they never paid him any royalties he went bust. They set the contract up so that they paid him one large sum and royalties "when" they used his patent but they also tagged onto that he couldn't sell to anyone else. He being a normal person couldn't understand GM was setting him up to fail from the beginning. I mean if you have the perfect transmission...why not use it? Maybe they were going to wait until he went bust then buy him out for pennies, standard big corp. tactic, and instead he just refused, told them to go to hell and went bust. Ruined him financially. He never really really recovered from that.

# 331
>>12744
>George Constantinesco
Sad story, but thanks. His torque converter might b useful for robowaifus. I will look into it a some point.

# 332
>>12744
Seems like s rotary to linear converter that uses pendulums and flywheels to smooth out motion and uses a ratchet to convert the linear motion to rotary. A variation uses clutches instead of linear motion into a ratchet. Either way, the fundamental problem is that flywheels and pendulums are wonderful for continuous motion like an engine in a car but, they reduce efficiency and increase latency in systems which rely on non constant one way rotary motion. Also, ratchets and clutches are inherently inefficient. If you can come up with a version that solves the latency and efficiency issues, please do. We need more options. I'm on the twister string/Spanish windlass because it's the simplest and lightest mechanism to move mai waifu at around 90 percent efficiency. I do hope you can develop that mechanism into solving even better, it'd help us all.

# 333
>>12748
My aim was for the shoulder movement. I have no specific plan or idea yet, but cutting down on the numbers of motor would be good. So I'd like a mechanism that allows for one motor to rotate while different body parts move only if they connect to the motor.

# 334
>>12748

"...Also, ratchets and clutches are inherently inefficient..."

I don't think there is any latency at all. If I remeber correctly the gas petal in the car determines where the rod grasp the pendulum./ So if first pushed hard it will go to a low ratio and the motor will rev and give you max torque. I think the motor rev it attached somehow also so as the motor revs to top speed it gradually increases it to higher and higher gears ratios. I would agree clutches are inefficient but I don't agree about ratchets. Especially a particular kind called a Sprag. These things are like magic.

https://en.wikipedia.org/wiki/Sprag_clutch

Look up some videos of them working they are very cool and will take enormous amounts of power for their size. I saw a sprag for a helicopter, a big one, and it had this little ten inch or so in diameter sprag. I couldn't believe all the power went through it but it does. Very special metal I expect though.

Anyways this Constantinesco transmission can use sprags with very little friction. I also don't believe that you need the flywheel. The flywheel is to smooth out the action in a car, I think. I expect you could directly hook it up to the pendulum. I could be very wrong about this these things are simple yet complex at the same time.

Another thing is there's no reason you only have to have two connections to the crank and the pendulum. You could use three like a three phase motor.

Now here's a off idea. Let's say the rods between the crank and the pendulum are chains or strings because they all work in tension(very important for weight) and you have one motor but two tension members transmitting power. Well when on is going one way the other is going the other way with a clutch to grab them you could operate many different "muscles" with these two sets of rods, strings, chains, whatever going back and forth. You could even have different ratio pendulums on each muscle.

 Of course the downfall is that you couldn't tailor the movement of each muscle. They could go either way but the force would be fixed to slow big force or fast little force.

Constantinesco has a book on this with almost super human mind numbing detail on these things and there's also an  biography of him. The tech book is hard to read. Very tech. I can't say I even remotely got all the details. I d understand the basic principles though. He's an old school engineer. Very deep. The biography is great.

# 335
>>12751
Using that mechanism to meet the various torque and speed needs of various mechanisms using one actuator with another actuator choosing the output can makeup for the lowered efficiency through mass savings. 
This is a really good example for a selective output mechanical multiplexer.
https://youtu.be/8DWK3zm9SMs

# 336
If you really want to get some better idea of what I'm talking about look at this set of articles from the excellent "Low Tech Magazine"

https://www.lowtechmagazine.com/2013/01/mechanical-transmission-of-power-stangenkunst.html

https://www.lowtechmagazine.com/2013/02/the-mechanical-transmission-of-power-jerker-line-systems.html

https://www.lowtechmagazine.com/2013/03/the-mechanical-transmission-of-power-3-wire-ropes.html

We always think we are so smart and modern but look at what these guys did with wood and rope. Inspirational stuff.

You also can see where Constantinesco's ideas are an evolution of these sort of mechanisms. It looks so odd because no one has really seen this sort of thing in a long time. Or most people anyways.

# 337
>>12797
One advantage of what I just talked about is you could run multiple outputs at the same time off the one motor.

# 338
==Thread alert Thread alert==
OP, if you're still with us, here's a daily reminder that your most excellent thread is approaching the autosage bump limit for the board (350) and we're less than 15 posts away. It's traditional to link back to the OP of the original thread (this thread) during the OP of a new continuation thread.

'''May #2 be even better!'''

# 339
>>12797
that's pretty effin cool anon thx

# 340
>>12796
As a fellow fan of sprag clutches, I'm becoming increasingly curious about a printable design of this mechanism. You clearly understand it better than I do. If you draw a plan, I'll print it to test. 
>>12798
This magazine is treasure trove of knowledge, mechanical power transmission is very practical.

# 341
>Soft muscles with origami-inspired skeletons:
https://youtu.be/OJO4FP0DXgQ

>Cavatappi artificial muscles: https://youtu.be/yXAJGH5s4cs
https://youtu.be/MpCFumHFZvU
https://www.designnews.com/automation/cavatappi-robot-muscles-have-5-times-strength-human-muscles

>Nameless nanofiber muscle, probably Cavatappi:
https://youtu.be/H19p43NFqp4

>Supercoiled polymer (SPC) muscles:
https://youtu.be/QHiTJ_zgGME
https://youtu.be/N4VMoYFrusg
https://youtu.be/hFuzQ4ed-t0
https://youtu.be/2GXWIozM4oQ (bundled/braided)
>TCP (the same?)
https://youtu.be/S4-3_DnKE9E
https://youtu.be/wltLEzQnznM

>Twisted string actuators (TSA)
I had the idea that they should in some cases be build with a loop. Grippers would hold a part of it and twist that. For fast release they coul let it go and grab the next part of the loop. Designing the gripper will be a bit of a challenge, though. But I think this is doable. Can't image I'm the first having that idea.
Not sure if this here >>12589 is already something like it bc I didn't understand it.
Here's some passive returning mechanism, followed by other videos on TSAs: https://youtu.be/J26y1nn7JMM
https://youtu.be/QBQMZsSQJQM (freaking loud)
Effect of bending: https://youtu.be/zYrHGMiqC9A
Life cycle test setup: https://youtu.be/PABVsuV7Y1M
Frequency response ( I don't get it): https://youtu.be/YLWsh1P80Dc
Mixed with fluid/gel tube: https://youtu.be/tP9B3aqc4CI
Transmission ratio and speed switch: https://youtu.be/Y1uceDzhjKY
https://youtu.be/5PtXTI1t3Po
I don't like it being used for fingers but it's a good technology.

>Nylon fishing line muscles:
https://youtu.be/Za0VeU9Ov7A
https://youtu.be/2OuRX65xbKE
(Reminder: The do have a high life span >1M)
I plan to rather use water for heating and cooling.

Continuous ransmission (CVT) / torque converters
https://youtu.be/kVPjhmTThPo
https://youtu.be/cd2-vsTzd9E
https://youtu.be/c9e2y-5DMNc
https://youtu.be/PEq5_b4LWNY

>Twisted string series elastic actuator (TsSEA)
This strikes me as particular interesting.
https://youtu.be/VBXykAIBKtA

>Printed pneumatics
https://youtu.be/_X0rDW6NQ58

Using sugar as soluble support material for printing silicone muscles: https://youtu.be/L0Z0-y3qpNk

>>12797
>Mechanical Multiplexer
Okay, thanks, looks promising. Especially if only limited to three outputs. But it's a bit loud and I wanted two outputs linked, not in line.
>>12799
>Grommet
I could always imagine to have a mechanism moving two outputs. But switching between all three options is another thing. And then holding while mooving the other one still isn't solved.

# 342
>>12813
This is an important post Anon, and I'd like to have the listing itself at the least included near the top of the thread #2. Kiwi, if you see this, would you mind if I folded this into your OP of #2? Or, I could add it to my own welcoming post next to yours. What I ''don't'' have the facility to do here is insert posts, so we'd need rather to modify an existing one.

# 343
>>12818
Go for it, these links are perfect for the new waifu actuator thread.

# 344
>>12821
Done & our thanks to both of you.

# 345
I just wanted to mention the idea that if a robowaifu would walk on a plane then the lower leg only needs to move the same distance all the time. So after lifting the thigh a electro magnet in the knee could provide this standard movement of the lower leg. Any problems with that?
I also think about another version of that, where the distance is adjustable. Like moving a magnet further away. But I'm not sure if that's the best way, since it would need to be stonger then.

>>12406
I started modeling something like this >>12882. But I'm assuming that some of the lines will go through the ribs, not all around the spine.
>>12471
Is this on the picture meant to block the rope from going to far? I think so. I thought about the same problem, but why not using knots?

>>12409
Thanks for trying to find a way of calculating what kind of forces we need. I'll try to look into it myself.

>>12482
>switched reluctance motors
This seems to be a reason to be interested in metal machining, beyond cutting some sheets for reinforcement.

# 346
>>>12471
"...Is this on the picture meant to block the rope from going to far?..."

No. Totally different. The wedges were an attempt to find a super cheap way to "stop" bending of a joint. Say a whole finger only had one motor that curled up the whole finger "but" it did have joints in the finger like a regular finger. You pull "all" the fingers closed with one motor. A bit of a kludge but it does seriously cut cost by a lot. So as the fingers are being closed you could lock any number of joints and the ones below it still being pulled closed would continue to close. The wedges are a super cheap way to do this driven only by a electro-actuator instead of a motor. The point of this was say you wanted to move a finger at the root like pointing but keep the rest straight. You could lock all finger joints except the root one(one closest to the hand) and it would move the straight finger up and down. Again it's kludge but with some thinking it could look somewhat natural.

I repeat this is a kludge solely to cut cost and in no way is ideal. It could cut cost for prototypes also. In the end I can't see any really decent waifu that didn't have all the muscles actuated individually but that would take some 300 motors to have a real life like figure.

>switched reluctance motors
"This seems to be a reason to be interested in metal machining, beyond cutting some sheets for reinforcement."

I just read the other day about people machining rifling in guns with copper wire, a plastic 3D printed die, salt water in a bucket and a normal battery charger.


Called electronic Discharge Machining(EDM). So I look at this stuff and some people are doing this at home cheap. The commercial stuff is NOT cheap but you can do this cheap.

Here's the significance of this. If you are going to make cheap reluctance motors you are likely going to have to stamp them out with sheets of metal and then glue them together. Much like  transformers are stack of metal glued together. The easiest way to do this is to build a punch that smashes them out. The metal needed to do so is super hard to make dies for the punch but if you EDMed them you could do this cheaply.

Let's say you are building these reluctance motors you could probably get by with three sizes or maybe even one and then double, triple or whatever number needed to get the force you want. Let's say just one type motor. Then you just need one cutting stamp to cut out the motor and maybe one stamp and die to make a pocket for the bearings. Glue these all together and you have all the metal parts for the motor.

# 347
Look at this,
Piezoelectric motor

https://www.youtube.com/watch?v=uFZsH62ewYo

If it just didn't have high voltage, sigh. Super interesting though.

What if we could simulate this inch worm effect but do it with sort of magnetic actuator effect??? I'll have to think about this.

# 348
>>12912
>Here's the significance of this. If you are going to make cheap reluctance motors you are likely going to have to stamp them out with sheets of metal and then glue them together. Much like  transformers are stack of metal glued together. The easiest way to do this is to build a punch that smashes them out. The metal needed to do so is super hard to make dies for the punch but if you EDMed them you could do this cheaply.
>Let's say you are building these reluctance motors you could probably get by with three sizes or maybe even one and then double, triple or whatever number needed to get the force you want. Let's say just one type motor. Then you just need one cutting stamp to cut out the motor and maybe one stamp and die to make a pocket for the bearings. Glue these all together and you have all the metal parts for the motor.

For men who don't have any familiarity with this, your descriptions are kind of an opaque mystery. This is no fault of yours, I'm just pointing out I can't really picture what you're saying Anon. If you wouldn't mind, could you make some sketches to diagram out things like
>Then you just need one cutting stamp to cut out the motor 
and
>and maybe one stamp and die to make a pocket for the bearings
?

They say 'a picture is worth a thousand words', and a few might help any uninitiates such as myself get over the hump to understanding your meanings. TIA.

# 349
I did use some verebage incorrectly. I should have said you punch out parts then stamp them to add form. Here's a link that explains this.

http://austgen.vn/blogs/what-is-metal-stamping

# 350
Here's some more. If you look at any type can that has some sort of from on it this is how it's made. They punch out the metal then use a press to form it into shape.

https://www.youtube.com/watch?v=FNxLaEZwH-o

https://www.youtube.com/watch?v=JmAyep2V-Cw

# 351
>>12916
>>12917
That's fine, thank you very much!

# 352
I'm confused. We have a new thread for muscles / actuators >>12810 but now the old one seems to be below the bump limit and come up again.

# 353
==NEW THREAD==
==NEW THREAD==
==NEW THREAD==

>>12810
>>12810
>>12810
>>12810
>>12810

==NEW THREAD==
==NEW THREAD==
==NEW THREAD==

This thread is autosage, convos should be relocated to the new edition #2.

