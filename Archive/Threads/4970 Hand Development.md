# 1
Since we have no thread for hands, I'm now opening one. Aside the AI, it might be the most difficult thing to archive. For now, we could at least collect and discuss some ideas about it. 

There's Will Cogleys channel: https://www.youtube.com/c/WillCogley - he's on his way to build a motor driven biomimetic hand. It's for humans eventually, so not much space for sensors right now, which can't be wired to humans anyways. He knows a lot about hands and we might be able to learn from it, and build something (even much smaller) for our waifus. 
Redesign: https://youtu.be/-zqZ-izx-7w
More: https://youtu.be/3pmj-ESVuoU
Finger prototype: https://youtu.be/MxbX9iKGd6w
CMC joint: https://youtu.be/DqGq5mnd_n4

I think the thread about sensoric skin >>242 is closely related to this topic, because it will be difficult to build a hand which also has good sensory input. We'll have to come up with some very small GelSight-like sensors.

F3 hand (pneumatic)
https://youtu.be/JPTnVLJH4SY
https://youtu.be/j_8Pvzj-HdQ
Festo hand (pneumatic)
https://youtu.be/5e0F14IRxVc

Thread >>417 is about Prosthetics, especially Open Prosthetics. This can be relevant to some degree. However, the constraints are different. We might have more space in the forearms, but we want marvelous sensors in the hands and have to connect them to the body.

The thread about actuators is related: >>406 and the  discussion in R&D General starting here >>1627 is a lot about artificial muscles.

My own concept in my mind for the most ambitious models so far is the following:  We have no space to waste. We might try to use light canals and LEDs inside to indicate bending. We'll probably need to use PCBs for transport of current incl data while acting as part of the bone. We'll probably need connectors between the parts which transport current without bending cables, eg cylinders with layers out of different materials where some of them are conductive. We should try to use Will Cogleys files as foundation, but since we might want to only build the bones out of hard material we might need to do it in metal to go smaller. This metal might be something expensive, like Titanium. We'll need tools for fine mechanics and such skills. I also think air pressure might be usefull to help open the hands fast, of course in combo with strings. I haven't thought about the actuators in the forearms a lot, by now.
That's it for now, I'm really curious about the ideas for the premium models, but even more so for the cheap and then maybe even smaller waifus.

# 2
>>4577
Thank you OP, I was starting to wonder when this thread would pop up.

I would add that there is another interesting hand with fingertip sensors:
Hand in action
https://vimeo.com/154571244
Fingertip sensor example
https://vimeo.com/155743044
Paper
https://homes.cs.washington.edu/~todorov/papers/XuICRA16.pdf

This paper has some good information about more human design of an artificial hand and the robot is, in my opinion, one of the best. what I dislike about this model is the bulky actuators it requires, but in reality most of the muscles controlling the hand are in the upper forearm connected to the fingers themselves with tendons. This can be made to look more natural with different actuators, like a hydraulic or pneumatic actuator, but the muscles in the hand which are anchored to the wrist or to other finger bones could prove challenging.

Another pretty decent design is this one:
https://www.youtube.com/watch?v=gd9d_BAXWvg
which follows a similar idea but is completely hydraulic.

A shame that neither of them made their designs public, but there is still a fair amount to be learned from observation.

# 3
Here a example of mistakes to avoid: https://youtu.be/s0LA48Sw62k

# 4
>>4577
Thanks for creating this thread OP. Hands are an important and complex topic actually.

# 5
New Will Cogley video on hands. I had the plan to look up some joints for different part of the Waifu, how they work, differences, ... Didn't know where to start and delayed it. Now he comes along with his new vid and gives me the right direction: https://youtu.be/dWUSH6DR4G8

Search for Condyloid joint, lead me to more, not all related to hands though:
https://youtu.be/zHYEhDMV5Bg
https://youtu.be/S7nUC__PRFU
https://youtu.be/0cYal_hitz4
https://youtu.be/2H10SZHGdvE

# 6
'''The Making of a 3D-Printed, Cable-Driven, Single-Model, Lightweight Humanoid Robotic Hand'''
>''Dexterity robotic hands can (Cummings, 1996) greatly enhance the functionality of humanoid robots, but the making of such hands with not only human-like appearance but also the capability of performing the natural movement of social robots is a challenging problem. The first challenge is to create the hand’s articulated structure and the second challenge is to actuate it to move like a human hand. A robotic hand for humanoid robot should look and behave human like. At the same time, it also needs to be light and cheap for widely used purposes. We start with studying the biomechanical features of a human hand and propose a simplified mechanical model of robotic hands, which can achieve the important local motions of the hand. Then, we use 3D modeling techniques to create a single interlocked hand model that integrates pin and ball joints to our hand model. Compared to other robotic hands, our design saves the time required for assembling and adjusting, which makes our robotic hand ready-to-use right after the 3D printing is completed. Finally, the actuation of the hand is realized by cables and motors. Based on this approach, we have designed a cost-effective, 3D printable, compact, and lightweight robotic hand. Our robotic hand weighs 150 g, has 15 joints, which are similar to a real human hand, and 6 Degree of Freedom (DOFs). It is actuated by only six small size actuators. The wrist connecting part is also integrated into the hand model and could be customized for different robots such as Nadine robot (Magnenat Thalmann et al., 2017). The compact servo bed can be hidden inside the Nadine robot’s sleeve and the whole robotic hand platform will not cause extra load to her arm as the total weight (150 g robotic hand and 162 g artificial skin) is almost the same as her previous unarticulated robotic hand which is 348 g. The paper also shows our test results with and without silicon artificial hand skin, and on Nadine robot.''

https://www.frontiersin.org/articles/10.3389/frobt.2017.00065/full

# 7
>>4859
Thanks, Nadine is a horrible looking fembot, but the article on her's and other hand designs is very interesting. I think we will need placeholder hands at the beginning and then we might try different development approaches with different priorities, before we will be able to join all of the traits later in one design:  
- Aesthetical hands for gestures and human like movement, but weak and without many sensors.
- Sensory hands, but less good looking and still weak.
- Hands for doing stuff, with some sensors, but probably not good looking, especially not human female alike.
Since we all have different priorities, tastes, and financial ressources, the end goal is IMHO going to be that we need to have a lot of options by variety in the designs.

For future reference, I'd like to link to a discussion on Sophias hands: >>4826

# 8
>>4863
YW. I agree on both points, and I too found the paper interesting in general. It seemed a decent overview if nothing else.

>3 variations of general hand designs
Seems like a good breakdown.
>Lots of options
That's one thing /robowaifu/ has tended to have up till now, numerous different ideas. I'd like artistic expression (eg, dancing etc) for my initial types of robowaifus, so grip strength and rugged utility is less important to me atm.

One thing I think unifies the significant majority of us and others is expense. We need to find ways to make robowaifu components very inexpensively.

Sophie is a very interesting robowaifu tbh. I wish Anon great prosperity in completing her quickly! :^)

# 9
>>4817
Thanks Anon, finally getting around to watching these joints videos now.

# 10
At the beginning and for cheap versions of the Robowaifu we might need to use the InMoov design. People improving that design a little bit, without going crazy, might then be particularly interesting. Especially if the designs are available: 
https://youtu.be/CIqzeBxkRws

The Raptor Reloaded Prosthetic Hand might also be a cheap starting point: https://youtu.be/ULTyu4ppk-s

The other extreme - A very complex design: https://youtu.be/K0RUxY3RKKo
Site: https://www.wevolver.com/wevolver.staff/anthropomorphic.robotic.finger/master/blob/Overview.wevolver

Ada Hand: https://www.wevolver.com/wevolver.staff/ada.hand/master/tree
Humanoid Robotic Hand: https://www.wevolver.com/wevolver.staff/humanoid.robotic.hand/master/tree
A page with overview of hand designs (link from the Sophie thread): https://www.frontiersin.org/articles/10.3389/frobt.2017.00065/

# 11
>>4876
Thanks. I quite like the integrated design of #2, and am intrigued with the apparent tensegrity-inspired approach of #3. I'm currently working on a very inexpensive tensegrity approach (thanks to /hover/-Anon!) for the long-bones and so my mind is particularly attuned to that area atm.

# 12
>>4877
should've posted this along with.

# 13
>>4878
BTW, please not the quite generous direct 'shaft' of open volume available with this 4-rod tensegrity design. I intend to mount a central tube down this space as a guideway for running Bowden cables out to the extremities all the way from the proximal major ball & socket joints located at the torso.

# 14
>>4879
>please note*
(check the shadow directly below the framework)

# 15
The guy improving the InMoov design I mentioned here >>4876 moved on in a similar direction than Will Cogley with his new hand, embedding little motors in the hand, using SLA printed pulleys. 
https://youtu.be/3DNVadMs5tE
Though, it needs to be noted that they are doing it because they might want to build a prothesis, which has other constraints than a robot arm. We should look at it, but also keep in mind that we have other priorities.

# 16
>>4883
That looks like a pretty promising approach actually.

# 17
>>4884
Thinks so too, though we might be able to combine it with Bowden cables and servos in the wrist later on. Just checked, I can turn my similar little motor in both directions if there's no torque applied.

# 18
>>4885
I think I missed description of the motors themselves. Can you fill us in Anon?

# 19
>>4887
Minute 2:34 and min 4. Micro metal geared motors: I've got the one on the pic for idk 1.50-3.50€, I guess around 2€. But I only bought one for testing and don't have the u-shaped one. He talks about SLS printed pulleys, but the one he has, can also be bought on Ali in sets with gears for 2€, some of mine are on the other pic.

# 20
>>4876
>>4863

some guy posted your board on g

i'm just driving by here but I'll drop you a hint

hyperboloids for the metacarpals

# 21
>>4892
>hyperboloids for the metacarpals
heh thanks for the hint, driveby-kun. :^)

https://en.wikipedia.org/wiki/Hyperboloid
https://en.wikipedia.org/wiki/Metacarpal_bones

My presumption is that Driveby-Anon intends us to understand a geometric behavior of the metacarpals. The tendons connect both above and below, and the particular curve they exhibit gives them a leverage advantage during gripping motion, for example.

# 22
>>4892
>>4893
Someone was claiming in this thread on /g/ the human hand was mostly made out of those and this was patented till 2040. Patents need to have a certain amount of innovation, though. Also, I'd need to look into these vids about joints if this true, and then it might still not be the best way.

# 23
>>4902
I see. Hmm, I don't think it's particularly problematic. There's far, far too much prior art in this arena (literally going back for millennia) to be in any way enforceable.

# 24
> Will Cogley
Progress intensifies: https://youtu.be/99RzNBQF6g8
It's of course quite to big for now, but I like where this goes.
> Skeletal prototype with windows to look into it, to see how well the gears are moving.
> MG996R Servos from Tower Pro bought on AliExpress
> Ultrahigh molecular weight Polyethylene, PTFE cube
Github: https://github.com/ikkalebob/NM-bionic-hand/

# 25
>>4945
Thank you for keeping us updated on his progress. The man is a real talent at this type of engineering and is obviously quite motivated as well. Good stuff, Anon.

# 26
>>4891
Someone having an opinion on which amount of RPM I should pick, when I order some of those motors? 
I guesstimated for the thumb it might move 2-4cm on the joint, the shaft of the motor has 3mm or so, which makes 30mm per second with 10 RPM, which is 3cm. So I think I'll really stay on the absolute low end of the scale. Any objections?

# 27
>>4974
>So I think I'll really stay on the absolute low end of the scale. Any objections?
It's simply a trade-off **like all engineering is** between velocity and torque. If you need more power, go slower. If you need more speed, expect less rotational force.

# 28
>>4975
Sure, I was already aware of that. Don't want the fingers move to slow, however. Then again, I can replace the motors later anyways, so I probably shouldn't overthink this. I'll take something around 10-15 RPM, but not 5, and not 30.

# 29
>>4976
Sounds good. As always, ''Test, Iterate, Improve''.

# 30
>>4883
There's a new vid of his hand with the microgear motors: https://youtu.be/Zi-s_RQNokw
Sadly he emphasizes that he thinks it's only possible to print the parts for the hand with a SLS printer, which is out of reach for most people. He's getting the parts from some paid service bc also hasn't one himself. As inspiration the approach might still be very relevant. I'm saying for a while hands are going to be very difficult.

# 31
5018

>SLS printer

A guy built his own?

https://www.instructables.com/id/DIY-SLS-3D-Printer/



Also, that's a high-end goal to exactly reproduce a prosthetic-capable hand. We'll be able to make due with far less refined designs for our robowaifus for years. It's a good goal to work towards, but we'll be able to create good (enough) hands much sooner.

# 32
>>5026
Fascinating, but it seems to be abandoned. Even with 5x5 cm this would be great, but it would need at least to work with PLA or better Nylon. He used tea with 95% sugar or alternatively Stearin, which is some kind of fat that melts at 48-50C.

However, I'm quite sure we'll get around needing some SLS printer for the hands. He used it for potentiometers, same as Will Cogley in his model. These seem to fail after a while anyways, so other sensors might be better. Also, with some little changes it might not be necessary, and resin printers might be good enough, or even FDM and standard parts which we can buy.

# 33
>>5043
Well, maybe someone with some resources can set up a good SLS printer and provide prints as a service bureau. Maybe someone already does this?

# 34
>>5018
Thanks Anon. I like his design in general. Quite simple and to the point. I particularly like how he thought ahead about ease-of-assembly in at least a couple of different points, and overall I think it seems a fairly good design approach for the fingers. Very utilitarian and not too expensive by the looks of it.

Did he give any cost estimates for the out-sourced parts printing?

# 35
>>5045
> Cost estimate
No, or I haven't seen it yet. Costs might not be the problem, if it's already finished. But for development it might be relevant, especially considering possible additional shipping costs and the delay.

# 36
>>5043
>Also, with some little changes it might not be necessary, and resin printers might be good enough, or even FDM and standard parts which we can buy.
Sounds interesting. Have anything specific in mind, Anon?

# 37
>>5047
No, or I don't remember something specific, but we can print small with FDM: 
https://youtu.be/gN7QMhBzd4E
https://youtu.be/LHg9phNSCEY

# 38
>>5048
>0.15mm
wow i didn't know there were even nozzles that small, looks almost like resin printing. looks like it takes some mods needed to make it work.

# 39
Chat transcript with Will Cogley:
https://hackaday.io/event/171045-animatronics-hack-chat/log/177852-hack-chat-transcript-part-1
https://hackaday.io/event/171045-animatronics-hack-chat/log/177853-hack-chat-transcript-part-2
Some notes: ABS ist better for sliding surfaces than PLA, CircuitPython for microcontrollers, different sensors are discussed e.g. ultrasonic, ...
https://www.bendshape.com/
https://singularityhub.com/2019/06/03/these-10-sensor-packed-gloves-could-give-robots-a-sense-of-touch/

His recent video: https://youtu.be/Wywru4K8GVU

# 40
A normal human hand is the ultimate multi-use tool. It isn't that hard to replicate one specific feature of a human hand, what seems impossible is to cram the feature list into the small space of one hand (plus forearm). How about this: Picture an android with two hands that look the same, but are different underneath. The wish list of features is split between the hands in some way (for example, one hand can be strong & the other one precise). As long as both hands working together can achieve what you want them to achieve, this is almost as good as each hand having the full feature set. Heck, when doing this you might find yourself suddenly with some extra space left and throw in a magnet or suction-cup function.

# 41
>>5592
Good idea. Noted, but I hope we can do better. Btw, if no one answers to a posting, it doesn't mean no one is interested in it or won't appreciate it, just that we shouldn't flood the forum with praises to each others ideas.

# 42
potentially-related xposts
>>699
>>704
>>705

# 43
Some tangentially related news from japan. It's a kind of hand-holding simulator:
https://archive.vn/7c2LR
Unfortunately, there's not much info available, apart from a two page pdf written in moonrunes

# 44
>>6489
i can't see it behind cuckflare. mind posting a link and i can see if wayback has it.

# 45
>>6490

https://soranews24.com/2020/11/03/japanese-inventors-create-robot-girlfriend-hand-for-lonely-people-to-hold-and-walk-with%E3%80%90video%E3%80%91/

# 46
>>6494
Thanks Anon. Yep they have it.
https://web.archive.org/web/20201102173143/https://soranews24.com/2020/11/03/japanese-inventors-create-robot-girlfriend-hand-for-lonely-people-to-hold-and-walk-with%E3%80%90video%E3%80%91/

Seems promising tbh.

# 47
Has anyone here investigated the Shadow Hand very much? Seems interesting and I like the way the 'tendons' actually travel up through the wrist into the hand itself.

# 48
Found this image from a news article promoting a project using a company's elastomeric touch sensors.
>
I thought the design of the fingers were interesting, if a little overdone.

www.extremetech.com/extreme/293610-mit-created-a-robot-that-maps-3d-objects-by-touch

# 49
Parallel Cable driven Anthropomorphic Robotic Hand: https://youtu.be/GzXvqFWgIs4

# 50
>>8632
Wow, thanks Anon! This is exactly the kind of approach that's been swirling around in my head for a few months (though mine have been mostly about the overall armature itself). It's particularly gratifying to see the idea working so well in something so detailed and technical as this human hand mimic. I'd be interested to see some numbers on strength and grip testing with it.

# 51
>>8632
This is too good to leave just on yt.

# 52
>>8637
This looks excellent...but I always have suspicions about actual functionality when they crop so much out of the video and only show the hand lying down - not attached to a moving arm. What about all the servos that presumably drive those cables? That's gotta add considerable weight and size to the end of the arm. Would be nice to see in greater detail.

# 53
>>8651
>Would be nice to see in greater detail.
Agreed. I'm too busy to dig around and try to get more details on their project work atm. Hopefully more information will be forthcoming here soon.

# 54
This guy https://youtu.be/qqBjBY4zf8I is still working on his DARA robot. It's a male robot, but might be useful to keep track of it. I mentioned him before in >>5327 bc he has some files on Thingyverse.

# 55
>>8700
Please keep us updated if you find this man makes a nice breakthrough that might help us out here. I like the lateral motion he's able to achieve thus far. Very life-like.

# 56
This hand design by a prosthetic company seems pretty useful:
https://www.youtube.com/watch?v=B-f0egEgKms

They changed the shape of the hand to make it easier to grip objects.

# 57
>>9690
Yes, looks like a decent, reasonably rugged design Anon. Thanks for bringing it to our attention. BTW, anon started a prosthetics thread here as well. Seems on-topic. >>417

# 58
I've been looking for attempts at playing piano with bionic hands. Someone made a rudimentary robot 11 years ago but they barely count as hands since they can only press the white keys.
https://www.youtube.com/watch?v=IwuiOwZrzCM

The closest thing I could find was this military prosthetic: https://www.youtube.com/watch?v=DP677lA_DEA
And this robot typing on a keyboard which is pretty cool: https://www.youtube.com/watch?v=Nek_yvvLRdQ

Are servos not fast or strong enough to make quick movements or is it more of a control problem? Could larger servos be stored in the chest and operate the hands with cables using pulleys?

# 59
>>10072
Bionic prosthetics normally don't have sensors. For  building a robot playing piano you would probably want that. Btw, I just got my heat sensitve plastics for making hands skeletons like therobotstudio did (16€/kg). Here: https://youtu.be/bVDneXZ_YfQ - related (various vids): >>9362 >>9471
Some of the hands related vids:
https://youtu.be/kWeJyduvhwA 
https://youtu.be/CfB8Mrh1dSI
https://youtu.be/1PYMT1U8qiM
https://youtu.be/tO3B_OyyqmQ
https://youtu.be/tZ-ouSmt5gw

# 60
>>10072
>Could larger servos be stored in the chest and operate the hands with cables using pulleys?
Not that anon, but you have a sound design idea there Anon. If we can figure out a way to ''entirely remove'' the weight and volume of servos out on the arms, then that will help everything move along better for us, physics-wise (and therefore, agility & energy-consumption wise).

It will take some creativity to figure out how to do this, but using some form of cable-only approach in all the extremities will pay off in spades for us all.

# 61
>related (>>10179)

# 62
A big problem I am having with robotic hands is that the fingers can grip quite well, but they don't open back up again. When the hand is the 'relaxed' position, the fingers will remain partially closed unless I physically push each one back. One solution to this maybe to run taught elastic bands or small springs over the top of each finger, so they are pulled to an open position when the finger servos are unpowered. 

I believe many makers solve this issue simply by stringing their fishing line tendons REALLY tight (maybe with the help of self-locking forceps or a small clamp), so that the fingers are forced back into position when not gripping. However, this makes each hand very difficult to string. Which is why I want to give external elastic a try.(I have used an image of a paper and string hand here because I don't have access to my robot at the moment but also the visible tendons illustrate exactly the same problem).

# 63
>>10999
Like so?

# 64
>>10999
This might not look very human, though. We have tendons on the back of our hand to open it. In your design approach the robot would need to spend energy to have the hand closed or keep it open.

# 65
>>10999
>>11000
I think many designers opt for exactly what you're describing, and simply weave a thin bungee-like or elastic band along the dorsal ridge of each finger. While this is a minor source of energy consumption during the finger contraction phase, it's obviously a passive benefit during the relaxation phase. And in fact it's probably fairly efficient energy-wise, as the normal state of hands tends to be in the relaxed pose.

**nice digits**

# 66
>>11002
LOL nice digits for a post about digits. I have some experimenting to do!

# 67
>>11003
Thanks!
>I have some experimenting to do!
I'd suggest you have a look at the ''Nano Hand'' by ''The Robot Studio'' guy. He has an arrangement using elastic bands.
Nano Hand - Finger Assembly
https://youtu.be/kWeJyduvhwA
Some other links anon posted here (>>10075).

There's another quite sophisticated hand design video posted here somewhere. Can't locate it ATM for you SophieDev, but I'll plan to link it back here for you in the future when I stumble across it. Cheers.

# 68
>>11002
Streched out is not relaxed, though.

>>11007
Here are some videos on hands by therobotstudio. Also look into the following postings. We probably should also link them in the other thread for the corresponding body parts.

# 69
>>11015
>Streched out is not relaxed, though.
Agreed, ofc. By 'relaxed' I mean the passive position of the fingers/hands/etc. where the actuators ''are not actively driving the part''. So, for the fingers that would mean 'not in the gripping position'. So, elastics can help 'passively' return fingers to this position, which is what I think SophieDev was talking about.

>We probably should also link them in the other thread for the corresponding body parts.
Yes good idea Anon. I'd say that having some kind of 'Anatomy Map' in the library thread might be good too.

# 70
>>11016
Maybe the elastic band or spring could be adjusted by a very small motor. In case of a band it could even be twisted to make it shorter and pull back stronger or the other way around. But mainly I was thinking about ajusting the length, to define the baseline of where the fingers should be if releaxed. So in other words, if the hand would be supposed to be rather closed, then the little motor would give some extra 'rope' to prevent it from flipping back.

# 71
>>11017
I like the idea of having an actuator-controlled re-tensioning system Anon. Good thinking.

>.''.if the hand would be supposed to be rather closed..''
Ahh, that's the source of my confusion: we were operating on different definitions of 'relaxed'. In the interests of unambiguous & clear communications I suggest we adopt the related term used in the animation industry, namely
'''Neutral Pose'''.

'Modified T-Pose' is the closest example to my meaning, and roughly-speaking represents the ''middle-position'' of a joint (as in ''animation-rig'' joint), roughly halfway between it's extreme positions.

Make sense?

# 72
>>4863

What about just something like this for a placeholder 'doing stuff' hand? It's just an elastic balloon filled with coffee grounds that serves as a useful gripper. Doesn't look very humanoid, but it does a good job of doing 'hand tasks'



I think having hands that serve different goals is a good point to develop for. Maybe even have a hot-swappable slot for the to switch to the right tool for the job. If you really wanted to polish the system you could even have a rack of hands somewhere in the house for the robot to go change its own equipment.

# 73
>>11146
Yep I like that idea Anon. Letting our robowaifus have multiple 'hands' to use would be pretty useful (and interesting). I don't think the majority of men would be particularly averse to the idea itself either.

# 74
>>11146
Also, breasts full of coffee grounds? Go to squeeze booba - booba squeezes you.

# 75
>>11153
Lel.
==In Soviet Russia...==

# 76
>>11029
>Modified T-Pose
Okay, but humans don't act like that. If possible I'd like to avoid very awkward behaviors. That said, it could be a fallback position. 

>>11146
All of us have slightly different goals and priorities. I want something quite human like, so this isn't really for me.

# 77
>>11167
Nice. Alita looks great with her long hair Anon. I liked her before, but I like her even better now.

# 78
>>8651

Cheap but reasonably powerful (like MG996R that can produce up to 15kg starting torque at 6V) analog servos weight around 55g each. There are 15 servos on that arm (3 for each finger it seems). So servos alone would weight 825g. And that's only for fingers actuation! There supposed to be more moving parts in that part of the arm but as you can see on the vid there's barely any space left and construction itself doesn't look like it was designed for anything more than this one demo.



There are smaller and lighter servos. And they cost a lot. I think they can weight something like 15g. That would make 15x15=225(g). Better but super expensive.Imagine paying 750-1500$ just for servos that move only fingers on only one hand. It seems like they are using something like that in their vid because servos are tiny.

# 79
>>11482
The mass of servos is ''exactly'' why I've been lobbying for relocating them into the 'central core' of the robowaifus, and transmitting force out to the extremities via Bowden cables instead. 
>tl;dr
Reducing thrown-weight in extremities is crucial to both agility/performance, and (much more importantly) reducing energy consumption in our robowaifus.

# 80
>>11007
>>10075
therobotstudio has a new videos and a website  about his Nano Hand online. Intro: https://youtu.be/uOeS_jklU2Y
Website: www.robotnanohand.com
Playlist with assembly: https://youtube.com/playlist?list=PLy7gxZH9jzfSGinQz8W42F5HdiTkT0Xm8

