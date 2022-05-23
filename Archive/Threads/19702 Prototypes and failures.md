# 1
Post your prototypes and failures.

I'll start with a failed mechanism, may we build upon each others ideas.

# 2
>>418
what was the intended function anon? did you ever solve it?

# 3
>>957
>Did solve it?
Getting closer, feel free to help.

-pic related are what I've been drawing for a leg mechanism where the foot is always parallel to the trunk, eliminating the need for strong ankle servos. Limits her ability to use them for sexual though, a worthy trade-off to me-

# 4
>>958
>feel free to help
I think someone already did anon.
>related
[[807

This simple mechanism already performs the specification you indicated. Just buy one and take it apart if you need to.

# 5
>>959
I forgot to mention all leg servos are localized within her hips to lower [the] inertial load [of] her legs on her servos.

# 6
>>960
Good idea, but I think you'll discover if you actually take my advice that [the swing-arm] mechanism is perfectly amenable to that design approach. You can think of the whole think upside down from a usual desk arm lamp with the weighted base as representing the mass of your servos. Still works identically. Don't forget to add in appropriately-scaled springs anon.

# 7


# 8
>>962
Mind giving us more written explanations of your design anon?

# 9
>>963
It's system that works like clocks, there's a motor connected directly to the rod which connecting its shaft to the shaft of the next joint. There's a concentric gear around the shafts which moves according to belts which transfer another motors motion to the final fixed gear.

# 10
Single motor walking mechanism, made in color to help illustrate its function. Capable of many different angles and speeds depending on lengths.

# 11
Simple single motor leg design.

# 12
Simplest single motor leg design I can come up with.

# 13
>>964
>>965
>>966
>>967
Have you created any physical models to experiment with your designs yet anon? I haven't played with them for a while, but I was thinking you could use K'NEX to prototype with. Maybe 3D-printing the parts? They look interesting BTW. Good luck.

# 14
Like I mentioned elsewhere, I'm starting with basic bots, working my way to more complex machines.  From left to right – line follower, dancing otto, walking hexapod, obstacle avoidance, bi-directional sumobot, and expanding sumobot.  So far only bots 1 and 4 work as intended.  The dancing bot version I made is trimmed to use as minimum plastic as possible… its legs keep falling off (no wonder there's a more expensive version that uses metal gear connections).  I still couldn't get the hexapod to work since the servo libraries I've tried don't work on an attiny85.   I'm currently working on the sumobots which I hope will be able to battle each other.

I'm starting to get the hang of designing and printing parts that actually fit the electronics and any existing modules I have.  I start by looking for easy-looking pieces on thingiverse then customizing them further then finally designing pieces from scratch. 

After the sumobots I plan to make a toy grade 3D printed RC car that uses phone bluetooth + arduino control as well as an RC tank.  Then I think I'll finally be able to make some waifubots, including the 1/8 scale rachnera-san and 1/3 scale wrestler bot.

# 15
>>969
>rachnera-san
</monster/ pls.

Wow, looks like you have been been busy anon! Good luck.

# 16
>>967
>>968
Tested physically, works but, not that well. Mostly just moves the lower leg segment

# 17
>>971
Maybe it would be cheaper/faster to prototype initial designs as cardboard cutouts instead?

# 18
Tried making a 10-spoke speed encoder wheel that fits the Tamiya 4WD tires, its too brittle and uneven.  My plan is to have the optical speed encoder just arch over the main wheels while they spin, instead of trying to read a separate encoder disc.  I will try 5 spokes and wont bother with concave shape, I'll just have the holes flat and square.  The diameter with the Tamiya wheels is 28.5mm, one revolution is 9cm, so two revolutions or 10 clicks is exactly one maze block traversed.

>>969
Repost but the sumobots in action: 
streamable.com/f2nqs

In the horizontal pic the bots in order of completion are 1,3,4,2,6,5.

Future bots are all waifu types, using some variation of the Fluffytail design and/or 3D doll pieces:

7. Micromouse (has its own current thread)
8. Cattymouse(larger micromouse with stepper motors)
9. Penguingirl balancebot(bluetooth control)
10. Kiwigirl balancebot(using 2.4Ghz RC radio and stepper motors)
11. Fluffy Rachnera-san(12-servo quadruped)
12. Fluffy Wresler(at least 14 metal gear servos)
13. Panzergirl waifutank (torso on tracked tank chassis)
14. Panzergirl devastator (torso on mecanum wheels).  13 and 14 will dress up like pic related.

Unfortunately neither of the future bots will stand taller than 40cm, I do not have the mechanical know-how to design for high torque, high weight applications.

I've noticed in related news, consumer home robots are closing shop: the makers of Kuri, Jibo, Cozmo, Vector.  Most of the AI of those robots are in private servers so the bots will essentially die unless the AI is open-sourced.

Apparently the only successful "robots" are the Roomba, Siri, Alexa, Google Home etc.  Either single-function tools or subsidized spyware.  That is not good.

We must change that.  Right now all I can do is work on creating a standard list of serial commands so that all my future waifubots can be controlled through a single universal arduino-compatible controller - either a physical controller that uses bluetooth or 2.4Ghz RC frequencies, or an app.  Later waifus will have audio and video processing so I'm hoping I can offload that to a desktop computer.

I'm just sharing this infodump since I hope even though our paths may be plagued by a thousand PLA carcasses, there is a clear vision of what progress should look like, for me at least.

# 19
>>973
>13 and 14 will dress up like pic related.
< robowaifu qt tankgrill enforcers
nice.

As for robot shops closing, it's neither unusual nor surprising for a nascent industry to have churn. One great thing that we have on our side is that the Wright Brothers/Henry Ford style home garage operations are a real possibility [for this industry atm], as you and others are proving. We certainly don't want the botnets to be the only possibility for anons to turn to in the future though, so we have to stay focused. Fortunately we still have  a few years before they manage to make it illegal to create your own waifu but have to use theirs instead. But it's definitely a race. If we make positive progress first and it becomes widely popular among hobbyists the world over, then we may be able to forestall such a move by the botnet vendors such as Jewgle & Amazon.

There are some command protocol works already out there, have you had a look at any of them?

Keep up the good work anon!

**Sorry for off-topic OP**

# 20
>>974
Thanks man.  It is indeed the only industry I can think of that is truly still in the garage phase.  Actual laws regulating humanoid robots don't exist yet outside of science fiction stories, so this is still a window of opportunity before corporate takes over.

>There are some command protocol works already out there, have you had a look at any of them?

I'm taking a look at various arduino smartcar bluetooth controller apps for Android, will try to find some common string between them so you can just download any one of them to control my bots.

# 21
>>975
>so this is still a window of opportunity before (((corporate))) takes over.
Exactly. But no one should just relax because there's a gap for now, and assume they just won't try to stop it. They will. We just have to move faster so there will simply be far too broad access to basic robowaifus before they can stonewall it.

# 22
My biggest failure in general was getting distracted and frustrated because of problems like computer failures and all kinds of things aka life. I need to avoid mind blockades, like doing sth only when I archived something else first (which doesn't happen then). 
Good example might be, not buying a 3d printer until one has learned CAD. Then not being motivated enough to learn it, which wouldn't be a problem if one had bought the printer first.

My biggest failure in so far in regard to outcome was overestimating the power of magnets, and therefore believing I could build a simple muscle based on that. I wanted to have piece of metal attached to a nylon string, getting dragged through a flexible tube. Somehow with magnets lined up outside of the muscle. I found out small pieces of metal cant hold much, and a bit of plastic isolates it quite good. 🤦🏼‍♂️

The other failure maybe isn't one, it's rather a bit of prototyping and testing. Though it failed in so far as I got stuck. Since I couldn't wait for my printer, which I want to buy after I moved, I started prototyping molds for thighs with pulpe aka  pappmache and plaster (pics realated). However, I would've needed liquid foam at some point, but I had difficulties to buy that where I live, so I stopped working on it. The approach isn't really good anyways, bc I wont be able to mirror two legs to make them fit together. I know that, though I think it might motivate me to look into building joints, using electronics to move them a bit and so on.... Better than doing nothing!

# 23
>>4429
>Better than doing nothing!
'''1000%''' better, at least! :^)

Actually, laying up laminates (like pappmache) is probably a good idea fundamentally. I'd suggest something like wheat paste for the adhesive instead of plaster to keep the result lighter weight.

# 24
>>4430
In that case here it's about a mold not an exoskeleton, weight doesn't matter. But you're right about us needing to use a lot of layers for the outside. It's because sensors and cooling tubes.

# 25
>>4435
>But you're right about us needing to use a lot of layers
>a lot
I'm not sure I would put it just that way, after all from the ME aspect, ''lightweight is king''. It's just that laminar structures can offer improved strength to weight ratios. For example, plywood is an a good type of laminar sheet with good properties (though generally probably too heavy for our specific use-case).

# 26
>>4437
We all have different approaches and varying priorities, so general assumtions don't work. 
I want to put in quite powerful motors and muscles, but bipedal walking isn't so important at the beginning. The first ones only need to bend their knees, spread their legs, and at some point turn around in bed on their own, ... The legs shouldn't be to light, bc this would feel strange if  I would holding them up.
Later iteration would be walking on all fours to the bathroom.

# 27
I spent all of yesterday trying to get a 3D model to use as a basis to start planning, and all of today trying to start it putting it together.

Not only is my computer a potato and declines to work with the more complex meshes that I try to throw at it, but even taking a full minute between movement and actions I get crashes.
Not that the crashes matter though, honestly I have no idea how to put the pieces of this mesh together. I've been trying to figure out which face is the top face, the bottom face, and even after going through a few hours of lectures and tutorials I am still no closer than I was a couple days ago despite the work put in.

I think I have a fix, but I can't be sure. I have a spare computer I got for cheap when a buddy of mine upgraded with a better gpu, which should help, but also just making an approximated model by hand instead of trying to assemble an accurate model so that I may refine it as I go could make things run far smoother. Hard to tell though.

A bit of a pain to have wasted a couple days though, I will admit.

# 28
>>4537
Fuck it, I'm going analog. Clay, physical references, a drawing board, and hand calculations only for the physical design. I'm not going to mass manufacture, so there is no need for computer designs. Clay and paper are far easier to manipulate and measure with.

# 29
>>4537
What program did you try?

# 30
>>4539
Fusion 360. Solid tool, but the files I used were fairly bulky, my computer is a potato, and I am not as experienced as I maybe should be, so I don't blame the program itself.
I've had far more sculpting experience than CAD experience, and it seems to be working better, although not by much. At the very least, it is making me rethink my approach.

# 31
I looked into it myself, without trying, since I need to rebuild my laptop, only have a Raspi and tablet working right now, and these would really be to weak: >>4549

# 32
I'm working on a similar spine than posted here: >>4563. It's just meant to be a test and early prototype, till I'll get my printer. The plastic is the lid/cap from water containers, I have some springs and two types of little spheres. Also some metal parts where a little fiber or line can run through, but I don't know their name.
I can tell so far that it's annoying to build. I put these little metal parts into some plastic hole and in between the end of a spring so they would hold the spring in place. Sometimes it works, sometimes I just won't get these into the spring. Then again, they won't hold the spring well, but thery are to short to put a washer in. 
Also, it's generally just trial and error. I want to get the idea how a spine could work.

# 33
>>4653
That sounds great Anon, keep experimenting. I like that you are using spare parts laying around to test things out with. Doing that will help us all understand how you would go about creating a robowaifu inexpensively. Don't be too annoyed at difficulties, just be patient and methodical. Remember that in a real factory situation (even a tiny factory of your own devising) manufacturing almost always spends the resources needed to create helpful rigs that help assemble/manufacture things. Be thinking about some kinds of rigs that might help you in the future as you're figuring out how to assemble parts.

>I want to get the idea how a spine could work.
That's both a neat goal, and an important topic. We won't be able to have good robowaifus without having good spines Anon, so work hard at it!

Thanks for sharing this here with us Anon.

# 34
I needed to a bit of a break from my software project(s). But I'm still on it! I finally started to get more serious about CAD, software will have to wait a little bit. I already tried out some stuff before, like beginning an eyeball were I wanted to put a camholder and magnets inside, also flexible lips out of TPU, possibly at some point an airmuscle with silicone rubber on the outside. I learned that I can import pictures into Solvespace to use it as pattern, which is exactly what I wanted. I used Avril Lavinge as pattern. However, I didn't get very far due lack of knowledge on how to use Solvespace and also made some conceptual mistakes. 
Now I finally got through some tutorials, being in a more relaxed mood and started to design a holder and lever for some small servo (PM35S) which I have for testing and maybe for an elbow. I also had the idea of using washers in a little case as holder for some axis. The holder can have an arm going into the disc which can rotate freely. It's a cheap and thin axle bearing if one has no ball bearing or there's no space for it.
So, that's not much, but still something. I will post more about those projects in the correct threads as soon as I archived something more. Doing this feels often better than working on software, since it's easier to have some result and hold it in my hands (after printing), even if something is wrong with it.

# 35
>>8034
Glad to see you're still going strong Anon! It's good to take a break from time to time and focus on other things. 'Variety is the spice of life' they say. I hope you succeed at the designs. I really like the fact you're trying to find extremely economical approaches to designs like the washer-as-axle-bearing. This sort of rigging is what will enable many more men eventually to find ways to create robowaifus on their own. I suppose if you put some kind of seal enclosure around the whole thing, then you could put machine grease into it for durability.

I hope you come up with lots of new designs this year Anon! :^)

# 36
>>8034
Keep up the good work Anon.
>>8038

# 37
I'm preparing a print for a very simple forearm right now. Didn't start printing yet, we'll see how it's going. It's TPU, which is not easy to print.
I want to build at least something, ASAP, to demonstrate some progress. However, this is not a forearm with motors or muscles, but a soft TPU+foam placeholder, which is supposed to be connected to a elbow with a little servo. More a visual improvement than anything else. From there, we'll see how it goes. 
I also started to design other parts, but it's not easy. The arms and legs of a human are not round, but more complex shaped, which makes it more difficult to get it right. Also, I need not only molds or some TPU enclosure, but also air muscles and pseudo muscles to fill the inside of the body.

# 38
>>8350
Good on you anon! The more functional parts such as joints, hinges, levers and mounting plates that we have, the better! Even placeholder CAD for servos and servo horns are useful and can save other designers time when they are planning their robowaifu parts.

# 39
>>8350
Oh cool. Glad to see some new design progress Anon. Yeah, I've often thought about all the void spaces within a robowaifu's outer shells and how can we utilize that volume.

# 40
>>8350
I delayed my TPU forearm print bc my print didn't stick to the bed. I had gluestick on it, but heated the bed after the first layer. I guess this was the mistake, the PVA disintegrated. I will try again with a advanced design in a while. I need to come up with a solution for designing arm and leg shapes in CAD. The print would have cost 7-8€ and I want to have a better design before I drop so much fillament into it.

# 41
>>8371
After the fail with TPU I wanted to make a simpler print with a outer shell out of more expensive PLA and a inner core of cheaper PLA. To make the core bigger and the shell thinner, I changed the design. I tried different variants, but Solvespace always exports a mesh with a strange error. Maybe a bug, idk. Big F. Whatever, I might print the original model, still with a PLA core instead of foam, but bigger outer shell then I would like to have. Or, since I'm working on improving those designs anyways, maybe I won't print any of it now. I like printing parts, but it has to make some sense.

# 42
>>8372
That error looks like some kind of pole (the 3D mesh technical term). Any chance you might have some kind of vertices begin collapsed down together in your model?

# 43
>>8373
>''being'' collapsed down*

# 44
>>8373
It's not a sculpt and I don't know much about vertices. It's rendered from a CAD file. It actually doesn't show up as error in a MeshLab (non-manfold edges).

# 45
>>8350
I'm still on it. Since I have these little PM35S motors, but they have no means to hold a arm, I have to work something out. Like mentioned here >>5034 I was on my way to build a whole construction around it, to hold the motor in the middle. I stopped this approach for now, and work on a disk attached to the motor and holding the lever which is attached to a rather complex washer. Note: Don't buy motors without mount for some lever or arm.
>>8372
For now I only printed out the simplest version of the forearm shell in some cheap PLA, which is quite heavy bc I used to many perimeters. I might only use this as as stand to put hands on top of it and have them moving for tests. It's more or less just like a heavy vase with two perimeters, but without bottom.
>>thighs
I want to try now, to build legs and arms out of 4-8 parts, the problem is to align them. Not sure if that will ever succeed. Maybe it will be enough to print some structure out of TPU to hold other parts inside and will need some smoothing on the outside by adding fabric and silicone rubber.

# 46
>>8456
That's an interesting looking design Anon. I hope you get everything sorted to your satisfaction. One thing I'm learning for myself is that I have to start out on something literally as simple as I can, b/c that's usually just about as hard as I can successfully manage on my own. Once I solve one small step, then I usually back up and look at what I've managed to do that time and that often gives me guidance on where to go next. So, I just make dozens and dozens of little steps like that until I succeed. Takes some patience, but it usually works for me as long as I ''just don't quit''.

Keep at it Anon! :^)

# 47
>>8460
>just don't quit
I won't. Though, I might soon be busy for more than one month with moving. I'll try to still do something in that time. After that, I'll have more space to set up workplaces for different areas which we need to cover.
Doing CAD mostly works fine while listening to podcasts, talks on YouTube or audiobooks.

# 48
>>8464
I hope you have a successful move Anon. I should be moving myself in the next couple of months as well. I'm trying to get better at programming, and also thinking about our operating system/computer hardware choices to help make robowaifus safe, secure, and reliable. It's a big area to understand it all! Anyway, everyone helping everyone else here goes a long way towards us all moving forward together.

# 49
>>8456
Just some upgrade: I managed to find a solution how to build a holder for that motor, but it took me a lot of trying around. Felt quite fine working on it, for a while, but towards the end I started to get more and more distracted by other things. Probably bc I had enough of it. 
I also assumed that this cheap little motor is going to work, but didn't look into it. Turned out, if it's going to work I'll need a special driver or setup with a H-Bridge. Whatever, I'm currently focused on learning and training CAD, so there's no rush. It was more about learning how to solve a problem and generally about dealing with that specific one.  Turned out, I wasn't thinking enough about it before getting started. After trying complex designs, a rather simple solution works now. 
I'll upload the file soon, maybe later today.

# 50
>>8561
Actually, your persistence is laudable Anon. Just keep at it.
>After trying complex designs, a rather simple solution works now. 
This isn't uncommon. Many designs can only achieve simplicity after the complex route has revealed the elegant route. Not only is this true in design and engineering, but in things like writing as well. There's a well-known quote written by the French mathematician and philosopher Blaise Pascal:
>''"I have made this longer than usual because I have not had time to make it shorter."''

Pretty much every piece of software I've ever cared enough about to spend enough time to pay attention to it's structural design has been through this basic process.

# 51
>>8561
I linked the upload here, in the skeleton thread >>8584

>>8568
Thanks for your encouraging words. But this was me scolding myself for not using my time better. I could do more.

Next project: Early hamcat_mqq-style ball-joints. One thing I ask myself while starting: How round do these ball-joints need to be. Can they be a bit flat on one side? Pear-shape to reduce some material on the other side?

# 52
>>8585
Thanks for the pic of the hamcat_mqq Anon. That looks remarkably like the simplistic armature design I myself have been working towards. I may try to integrate your fittings/joints design in my own efforts. Thanks for your work.

# 53
>>8588
>hamcat_mqq
more of his stuff is in the projects dump: >>7707

# 54
>>8585
I was doing ball-joints today. Print-in-place was a difficulty, this means printing a mechanism at once, which then needs to break some supports of and being moveable. I got it working, by adding a hole to the bottom, so I could use a screwdriver to disconnect it from the ground of the cup. However, I'm still able to get the ball out and in again, which makes it pointless. It will most likely be better to print the parts separately, which makes them print cleaner. Currently it doesn't move smoothly.

# 55
>>8661
That's a neat idea about how to do mechanisms though. Just keep trying until you perfect things Anon. You get there! :^)

# 56
>>8662
I think I have to be careful with the print-in-place idea. It's not necessary and trying to make it work is eating most of my time with every prototype I design. Printing parts separate also means they are cleaner and therefore run smoother. Though, it's probably so, that we'll need to add something to the outer shell of the sphere (ball) anyways, to make it smooth when moving but also having more grip. I was thinking about silicone rubber, but not sure yet. However, this is one more reason to print the parts separate.

# 57
>>8690
I like the way you're coloring/rendering those parts in the diagrams. Makes them easier to understand actually.

# 58
>>8698
Yeah, but I should have converted the last pic into a jpeg, 5MB is obscene, the jpeg has 200K or so. These pics are the actual models, just with everything hidden. They look like that when I'm working on them, just with additional lines and points.
The pic here shows the difference in quality between print-in-place (middle) and separated (bottom). Don't mind the little gap in the bottom sphere, I'm printing with 15% infill. Also, the bottom sphere is bigger, bc I wanted to test if I would still get it into the cup if I increase the size of the sphere 10% (Answer: No).

# 59
>>8699
Actually to my eye, it seems you're already coming up with nice shapes. Put something like that through a resin printer and you would basically have production-ready parts ready to ship off to manufacturing.

You're making great progress Anon. Please continue doing so! :^)

# 60
>>8699
BTW, Anon posted a video about an android leg that uses a big ball-and-socket joint for an ankle.
>>8704

# 61
I was playing around with the idea of re-creating the mechanism of the InMoov neck accuator after my posting here >>8718. I didn't look at the details, just trying it on my own. The first part (pic 1) wasn't printable, even with these supports. It's to steep. Number two also wasn't that great. Don't know how to describe it well: The outer rails were too thin, since it's only the edges that turn. I played around with some changes, but nothing made sense. I was able to print it, but it was quite dirty. The third try was more similar to the original design. First I got it wrong again, but I'm sure V3 would work. I didn't really try to print it yet, but it looks the same than the original and I printed that already. The details matter, the outer lines have to be curvy. You can see it in the part I marked.    
Picture number four is the shoulder part for the doll >>8585. I didn't print it yet and it will need some adjustments till it's really finished. I partially disassembled my printer to exchange the heatbrake, so let's hope I won't break anything.

# 62
>>8760
This is actually really informative watching your progress and following your thinking Anon. You're already able to design a wide array of parts, it's pretty encouraging to see.

# 63
>>8760
I had some trouble with my printer after finally replacing the heatbreak with a all-metal one. Also some other distractions. I did still work a little bit on a prototype for a alternative shoulder joint, which is not a ball-joint. 
The blue part is supposed to be constraint to the body, the green part can then slide sideways on it, but is also supposed to tilt up and down. For lifting the arms sideways. Though the later I'll have to figure out by printing prototypes, which I can't do right now. The current design probably wouldn't work. I need to figure out the details and maybe add another moving part as well. The grey disc is a placeholder for a metal disc with bearings, so a attached arm on it could move without friction. This is for lifting the arm in front and back of the body. I wanted to have a holder for the disk integrated into the design at first, but realized that I want my parts to be printable with no or minimal supports. I need one plane side for that. So I added a hole to the later version of the design, for adding the disc with a holder using a screw. I might integrate some metal bearings into the other parts later as well, but this should be optional. 
However, I decided to build a prototype at some time (shipping problems currently) which will use motors in the chest and strings to move the shoulder. The idea is, that the strings can then later be replaced by airmuscles or other ones, so the motors shouldn't be necessary anymore. Though some might still be part of the design as a fallback solution. Since there won't be a motor in the shoulder the "bone" itself can therefore be kept small and be surrounded by some soft material. So her shoulder can look feminin and be soft like a human one. 

Btw, I'll plan to upload the files soon and also opening a Mega account so I won't need to use Catbox all the time. For now, in that case the idea is more important than the current execution anyways, and the signal that I'm still operational as well.

# 64
>>9142
Btw, the empty spaces in the middle of the organic looking part in the shoulder joint are for separating that part into two parts, for printing. So each one has a plane foundation, which will be on the printbed. They could be screwed or glued together, or I might later add some more space for a layer of machined metal inside, so they would be more durable. I will need to add contacts into the design as well, since I want to keep bending cables to a minimum. The hard parts of the joints are supposed to transfer energy and data through the body. The sliding parts need at least two metal layers to transport current, data might use some form of light communication based on LEDs with different colors. 

I still have to watch quite some videos on human anatomy and also read a little bit about it. There will also need to be a lot of trial an error. 

Then, I also spend some time trying to create a human-like ribcage in CAD. Not with much success. I used pictures from some scanned parts which I downloaded from Thingyverse or a similar site. It turned out to be hard to do that in Solvespace, at least with my skills. However, I want to do as much as possible in CAD instead of scultping, because it's easier to manipulate these files to add something later. So I'll try again at some point, probably after improving my skills in using the program first.

# 65
>>9143
I also found a front part, which would fit quite well to the chest of a hard-shell robot, but might also be interesting to print in a flexible material. It's a booby plate armor design, inspired by The Mandalorian. https://www.thingiverse.com/thing:2888954
I'm going to add this to the skeleton and armature thread as well, but only together with some other pics on my other device. I mention it here solely because it might be useful for adding a female look to some ribcage design very fast. Also, because it's part of the next picture.
I used Dia, to put some of my pictures of prototypes and pictures of patters I want to use together, into a kind of diagram of what I'm working on. So I can have a overview and decide where I want to try next to push something forward. The pictures are sorted to some extend, to be circa at the place where the parts would fit into a build of a body.

# 66
These are excellent posts Anon. Seeing your design progress is inspiring. I'm particularly glad to see you working on the shoulder-girdle and ribcage areas. I think about those a lot and did a small study on the design and kinematics of the shoulder-girdle back in school. It's an amazing design actually. Keep up the good work, and may you have good success at it! :^)

# 67
>>9144
So, I was watching videos on how to get a ribcage and shoulders right in CAD, because that's what worries me. I hope I'll try out Blender soon. However, after watching some video on how to draw a chest I got inspired. My problem might really be that I'm not trained in drawing people, and I found it's worth looking into that. 
I really wanted to do a ribcage ,build like a human one. Starting from drawing a chest I tried something else, what you can see on the pictures. One also shows the amount of complexity by showing all the lines. This is of course once again just crude prototyping which might not lead very far. Also, FYI this is meant to be printed in TPU when it's finished. So I might still put in some ribs on the outside (in PLA), but mainly for show to make them visible through the skin, without really having a full ribcage. The thick parts of the prototype would be made thinner or hollowed out to hold parts like small computers and such. Btw, here a no tiddies bc its not the outside, there would still go at least a a layer of power mesh with silicon on top of it. Also, it's far from finished, just wanted to give an update. The video was on a male ribcage anyways, so I have to feminize it anyways. I want our waifus to have a bit  unrealistic waist to hip ratio (wasp-like), tbh. Like they would be wearing a corset. 

I also put some silicon on top of a small printed face of Sophie to check if it sticks. Even without thinning it, so that it goes better into all the cavities it actually does. Silicone is known to not stick very well to anything that silicone, it only sticks better by having a huge surface to hug onto. I'm thinking of making experiences with some silicone on plastic faces. This isn't really the my preferred way, since I would rater like to create a skull and then add soft silicone parts, but one step at the time.  

My printer is still not working, if you are wondering why I don't try to print some parts. I'm working on it, from time to time, but have to keep an eye on my frustration management.

# 68
>>9620
> it's far from finished, just wanted to give an update.
That's fine Anon, I'm glad you did! It's enjoyable watching how you progress in your work to the final products.
> I want our waifus to have a bit  unrealistic waist to hip ratio (wasp-like), tbh. Like they would be wearing a corset. 
I think that's a really good idea from a character-appeal perspective. However, it may prove a little tricky that way from an engineering perspective. For example, Sophie Anon's challenges fitting all her new eye gear inside her head.

Regardless, I'm sure you'll manage Anon. BTW, any idea what's wrong with your printer ATM?

# 69
>>9620
>My problem might really be that I'm not trained in drawing people, and I found it's worth looking into that. 
You are absolutely correct Anon. Life drawing is basically the key to being able to 'see' how anatomy works. There are a large number of drawing tutorials out there in many places on the Internet. Our webring's own /loomis/ has some too:
https://anon.cafe/loomis/res/628.html#628

Good luck. It takes time, but you'll eventually get it if you just don't quit.

# 70
The important thing about >>9620 is that I realized that a really should work with subtraction in CAD. I had the wrong idea that I would need to keep my models ultra simple and also ideally not render something to then cut something of it away afterwards. Sense of perfection or the goal of keeping it simple can stand in one's way sometimes. Assembling of different files also works in Solvespace, but it is a pain to do with rather organic parts that don't really fit into each other, have to overlay partially, but still don't fit very well (see my try on a thigh in >>8456). 

>>9621
Don't want to discuss my printer problems here ( in this thread), that's why I didn't mention the specifics. I already have tutorials and advice, but thanks for asking.

>>9622
Some of the /loomis/ examples are directly useful, thanks. I'll have to look into how to use wget or curl to get all the images. Many are more interesting for drawing then for creating a 3D model, but I can use some of them. Also, maybe I might want to learn drawing one day.

# 71
>>9631
>...Sense of perfection or the goal of keeping it simple can stand in one's way sometimes.
I'll presume you are referring to the psychological state known as ''perfectionism'' in the first part here? While this is definitely a hindrance in many ways to a man's progress in whatever given field, I consider the latter to be practically a law for success. Conflating the two together is a fallacy.

The former is a kind of obstinate drive to perfect one's perceived notion or ideal about a thing or a system. These perceptions are obviously, necessarily, ''a priori'', __incomplete__. This pursuit is on the face of it misguided in a fundamental way, and will certainly lead to one's personal pain and suffering. Balance in all things, and knowing when to quit are two important characteristics of a man's growth to maturity. You'll never get things perfect in this life. Good enough is, well, ''good enough''. :^)

However, the latter 'law' of simplicity is '''the''' primary effective means ever discovered that lets men tackle the absolutely unchangeable nature of the world around us. It's one of the rather few means at our disposable in our ever-running 'battle' with ''The Second Law of Thermodynamics'' (commonly known as ''Entropy'').
https://www.grc.nasa.gov/WWW/k-12/airplane/thermo2.html
https://en.wikipedia.org/wiki/Second_law_of_thermodynamics

The insulting mnemonic phrase 'Keep It Simple Stupid', while a good admonition, is actually a blatant misnomer. Only the 'stupid' man doesn't work to keep things simple in their lives. The intelligent man works __hard__ to do so. This should be instead:
==Keep It Simple, Smartguy==

When you're dealing with the monumental complexity of devising a working, IRL, autonomous gynoid robotic companion -- which we as a team here on /robowaifu/ are endeavoring to -- then ''keeping it simple'' is literally the only possible pathway for us to eventual success.

>tl;dr
Put simply, all things around us tend to disorder. ''"Keep it simple"'' is a good way to keep this manageable, and maintain both order and sanity.

# 72
>>9631
>Some of the /loomis/ examples are directly useful, thanks. I'll have to look into how to use wget or curl to get all the images.
I can look into compiling an archive of the whole board and posting it for you somewhere Anon. Might also turn out to be a good resource for more than just /robowaifu/'s use tbh.

# 73
I didn't really archive much to report recently. I worked a bit on the chest, to put in spaces for ribs in another material and was also starting to work on a long term project of building the bones of a hand out of layers, which could then be PCBs (electronics) with sensors, plastics for the form and metal parts for strength. 
I also got some more stuff from AliExpress, but didn't really work with it. Some motors will arrive soon. I had some problems with my Raspi. I thought it was the software or my disc, since it got slower and slower, but it was the SD card which failed a while later. I finally looked into getting a new PC, which took me some time because I had to find out what to buy in the current situation and how to get it. I also finally worked on getting my Laptop running, which is weak, but better than my Raspi3. I had troubles to work on my design on my Raspi, I had to wait to often. I also had to look into not missing out too much on business opportunities, which I ignored in favor of my main dedication here. Not sure how much time I'll have during the next two month, but I'll work at least a little bit on my designs and with my new things. Though this might not lead to immediate results.

# 74
I also finally fixed this >>8372 >>8373 - In the configuration, the export chord tolerance (in mm) needs to be the same than chord tolerance (in percentage) which is also shown in mm.

# 75
>>10292
Ahh, good detective work.

# 76
>>10291
>I worked a bit on the chest, to put in spaces for ribs in another material and was also starting to work on a long term project of building the bones of a hand out of layers, which could then be PCBs (electronics) with sensors, plastics for the form and metal parts for strength. 
I've thought often about the field of Neuromorphic computing, specifically as it relates to designing/engineering robowaifus. Using structural and other ancillary parts ''embedded with sensors, batteries, microcontrollers, wiring, electronics parts, etc., right inside'' the structural and actuator components is not only very bio-mimetic in design essence, it also is very likely to help bring the extreme high-performance characteristics of neuromorphics to the table.

For example, embedding temperature sensors directly within the finger bones, and also keeping the robowaifu's self-protection 'sense/react response cycle' to pull away from the heat, say, all 'short-circuited' ''locally'' right inside a simplified hand-local electronics/microcontroller/actuator system. This design approach can allow the response times for such a system to be very fast relative to a more traditional, hierarchically-networked command & control mechanisms.

Basically, in a somewhat similar way to biologic adrenergic nervous system response mechanisms, you want to push the 'computation' for such a system out to the edges of the physical structure, and not be so dependent with always 'phoning home'' first to the higher-level computation systems of the robowaifu's 'mind'. This latter approach encompasses costly communications and other delays. 

Not that the signals wouldn't be sent on their way 'back up the chain' though. You definitely want the ability of higher-level control to override lower-level ones when needed. Forging ahead into dangerous environments to protect her master for instance, even when doing so conflicts with the most basic of self-preservation dictums. This round-trip would hopefully be completed within milliseconds (vs. the hopefully ''microseconds-level'' desired for pure local response times).

My apologies for my probably confusing writing here Anon. This is a complicated topic and it's difficult for me to describe it concisely.

# 77
>>10297
As an additional thought on the specific example of '''HOT! PULL HAND AWAY IMMEDIATELY!''' example, the control devices could perhaps either open, or reuse, an ''emergency response'' communications channel up to further-up actuator systems in the robowaifu's skeletal chain.

So for example, the hand-local would attempt to instantly flex fingers back, but then emergency-response channels can be opened to the wrist, elbow, shoulder, and torso actuators, all in  a tiered-priority chain, to enable fully pulling the hand entirely away from the danger, same as we ourselves would do accidentally touching a hot iron for instance.

Each of these chained-actuators would quickly add their own kinematic dynamic in the movement, and the effect would be propagating and progressive. The idea behind the 'emergency response' is that the higher-level analysis would be bypassed in a first-order response time, simply to quickly save the robowaifu from immediate damage.

# 78
>>10298
One additional thing that will need to be solved for this hypothetical situation. As we grow up, our entire physical being develops a kind of physical awareness that let's us intuitively discern where sensations are coming from in our body by mere touch, and usually more or less instantly. Vision and audio, for instance, are __not__ needed to know you've just touched a /comfy/ soft blanket, or a cold ice cube spilled onto the counter.

And not only do you recognize immediately these kinds of sensorial cues basically immediately, you also know ''where'' (to a first approximation) the touched item of interest is located, relative to your general body position. Again this is all instinctive to us, and happens 'automatically' with little attention needed for most cases to figure these things out.

Back to the HOT! emergency response, the robowaifu's system will need some kind of ''touch location-finder'' mechanism so she knows instantly ''where'' the hot plate is, and ''which way'' to yank her hand back out of danger. If this isn't done accurately, she could make a clumsy move in the reaction, and possibly damage herself, you, or something else.

Again, this is something we all develop instinctively as we grow up, but for us as designers and engineers we'll have to solve this kind of thing explicitly. I'd guess that a first-approximation approach would be to keep a general sense of all the items in her local body space area's ''surface normal''. This should at the least give her the direction to quickly move out of the contact danger (ie, out along the surface normal of the object and away). This situational-awareness solution needs to account that this 'normal-map' of her environment is dynamic, as both she and the elements in her environment are potentially in motion with respect to each other.

This is really quite a remarkable domain to tackle from a systems-engineering perspective. Now that I've been applying myself to consider some of the many things all needed, most other design & engineering endeavors seem rather boring to me now. :^)

# 79
>>10299
Also,
**once you check my digits**
another thing we might do is develop a sort of 'contact-pad volumetric triangulation' sensor model. The idea is you have many tiny pressure, etc. pads embedded into the robowaifu's 'skin'. Whenever she touched something, and approximation of it's shape (and by implication, it's surface normals) can be quickly simulated in her world model.

For example, if 18 different pads on two of her fingertips all register a contact, then based on the kinematic/skeletal/etc body model simulation of her current physical position, then she can 'triangulate' the surface shape of that object at it's contact points with her fingers. Again, all instinctive for ''us''...but for her will need to be explicitly worked out in advance by trial and error during design.

# 80
>>10291
I finally made a Mega account for my designs and testing results:  https://mega.nz/folder/nv42EbzT#1MUblavva2UG6DukgD0moA
Not that something happens to me and all would be gone. Also, SophieAnon shouldn't be the only one uploading design files. 
- They are all made in Solvespace for now.
- Didn't add some copyright licence for now, because I wasn't able to decide yet. 
- I didn't add all my tests and failures, the other files are quite messy and I need to look through them first.
- The structure of the folders might also change, it all just provisionally.
- Didn't add stl files yet, I would first need to open the files and export them. You can do that yourself, but these are just prototypes anyways.
- I want to try out more modelling with OpenSCAD, IceSL, Blender and maybe importing stl files into Solvespace as well. STL import is available in some some alpha version, but I didn't test it yet.
- I want to try OpenSCAD and IceSL, because organic forms are just to difficult to do in CAD. But also because complex models would have bones which are dependent on each other. Think of the bones in a spine. I want changes applied if I change some part. I think more and more that this is only possible in code. Sculpting and mouse-based CAD might not work.
- I also consider paying some professional to make a model of some face from an actress for me. Then, later an anime version of it. There seem to be cheap designers in poor countries offering that (3D/face modelling) as a service. At some point in the future I would like to build a AI generator to do this from photos, but I would need some examples anyways. 
- I will open my own thread as soon as I have more to show for. For now I call my project "Genera Project", but this might change. I want the project and my specific build (my robowaifu I'll build one day) to have different names.

# 81
>>12661
Glad to hear you're beginning archive your work online. I think SophieDev used more than one site in case his work was taken down by snowflake leftists b/c robowaifu wrongthink? Might be a good idea tbh.
>For now I call my project "Genera Project"
Good luck with Genera Project, Anon.

# 82
>>12661
I worked on a simplified model of a spine tonight. Well, one section of it. Kind of had a blockade about what to try next before I got started. Didn't know what I could and should try next. Can't work on the chest because it got to complex for my Raspi to handle, tried to install some Linux distro on my Laptop which gives me troubles. I might soon just install some random distro that works, and use it just for my CAD until I get my PC.
I wanted to wait till I can use OpenScad and Blender on my laptop so I can try to design a good spine with that. I don't think I can do it in Solvespace, because it's to complex with parts dependent on each other.
Decided eventually not to go for a perfect human-like s-curved spine for now and just try something out. It's supposed to work with twisted string actuators. Though, I don't plan to use them as sole actuators. It's just a incomplete model right now. I didn't add holes for the forward movement yet, because I might use other 'ribs' for that. I also could add them easily if I need to. The pink ball is just like some flexible ball out of plastic I bought for my cat. Maybe the size is good or maybe I have to find something else, for my prototype it will suffice since relation to other body parts won't matter. 

I also ordered some simple bags for 200 ml of liquid, which I hope to use in experiments for my overall design. I'm thinking of having horizontal layers in the waifu chest, containing bags out of fiber reinforced silicone, which then can be filled with air. Two would be on one layer with at least one normally closed valve in the middle. The valve would be in line with the spine, while the bags would be  spread out on each side. 
This could provide some holding torque without e.g. having some motor providing torque all the time. The side with more air would keep the chest leaning in one direction, while it could also react very fast to high pressure or to some sensor, if the body is being forced to move by experiencing some force against itself (compliance in robotics). 
I also plan to try to combine this with horizontal layers of plastic sheet moved by magnets which would compress one side of such layer. So if the valve in the middle between two bags is open while the magnet compression on one side snaps, the air should go to the other side, moving the chest very fast (but without much force) to one side. 
Alternatively some pump might remove the air from the silicone bag on one side, while the air from the other side can't move over or maybe the amount of air is even additionally increased on that side, creating the same effect. Though, this version might be a bit slower, and make more noise.

I also might have fixed my printer. Found some part which might belong into it, will need to find out about that and I didn't test it yet. Had no motivation to fix it for a while, because of frustration about the whole thing, so it stood around for a few months.

# 83
>>12882
This is very interesting Anon. Any chance you can piece together a render of a fully-assembled group of these into a complete spine? We'd certainly like to see it if you would for us please.

# 84
>>12887
I'll order some drone motors and then print it for testing. I have motors, but only one per type. They're very small, I wanted to use them with a cycloidal drive but failed in designing that in Solvespace.

# 85
>>12661
I just made a little test with a part (bottom/back) of the pelvis from >>12878. Not sure if it is taken from a male or female, there's not indicator of it. I didn't do much anyways, just slicing it in a crude way to make it possible to have a look at it and contemplate how it could be designed in some CAD program. It's for parts, two are always (more or less) the same as their mirror. So assuming the parts were simple enough now, designing two parts and then mirroring them would be enough. Related: >>12884

# 86
>>12905
*It consists of four parts, two are ...

# 87
>>12905
Nice work Anon. I think some degree of intentional biomimetics will be a key to success for us here.

# 88
>>12882
I went on working on it a little bit. Experimented with a chamfer to to make the edges less sharp, since the rope would rub there all the time. Making the design separable for printing worked and I added some holes for screws and nuts. However, I didn't print it yet so I can't know if screwing it together will work well, but it could be glued as well.

# 89
>>12923
Exciting to see your progress, both on this effort, and ''especially'' as a designer. You're becoming quite skilled at your work, Anon. Keep it up!

# 90
>>12926
>becoming quite skilled at your work
Thanks, but it mostly isn't really difficult. Till it is. So far I failed in transfering Levi Janssen's approach to create good cycloidal disks to Solvespace.

Yesterday, I also looked into how thick we can make a femure (upper leg) bone and how many LTO batteries could fit into each. It's also just a sketchy model so far. Six is the number I came up with, for now. Which gives us 10Ah with 14V or 20Ah with 28V. I guesstimate that three might fit into the lower leg bones.

# 91
>>12935
> guesstimate that three might fit into the lower leg bones.
It's good thinking to distribute things around and utilize any available, latent, volumes. 

However, batteries and other massive (in the physics sense) items bring some additional caveats to the table for us as well. The concept of ' '''''Thrown Weight''''' ' (as used in race-car and other forms of dynamical-systems engineering) is something that directly affects our robowaifu engineering too. 

To wit; we need to keep as much of the mass centered around the pelvis volume as is feasible, and to not put it out in the extremities (head, limbs, hands, feet, etc) to the degree at all feasible. The further out from the center-of-gravity the mass goes, the ''exponentially worse'' the effect is in terms of kinematic and energy consumption, etc., penalties becomes.

As you seem well-aware already, keeping the robowaifu's overall mass itself down is an important consideration in many ways. In like fashion, keeping the ''thrown-weight'' down is also very important to us. I'd suggest at the least not putting any batteries out past the elbows or knees to help alleviate the issue. Ideally, they would ''all'' go right into the pelvis/hip area.

# 92
>>12937
Thanks for your input, but please stop repeating that same standard text over and over again. I've read it 10 times already. I'm ignoring your conclusions on this topic anyways, because it doesn't work for me. Thank you.
There's no way I'll put everything into the chest. First of all, when I'll lift her legs while she's lying they can't be to light. Then there's not enough space in the chest, especially not in a soft doll-like body. Also, she doesn't need to walk for miles. Five or ten minutes max is sufficient. While doing so, she mostly needs to lift her feet 1-2 cm of the ground. Last but not least, it would only matter if the downside for putting more batteries into her would be higher than to leave them out. Which most likely won't be the case if she's sitting, standing or lying down most of the time. I don't know how to calculate this but 20Ah aren't nothing.
So her weight will be 30-40 kg, I guess. If it's less and I like it, then fine, if I won't like it I might even put more water into her internal tanks. On purpose, to make her heavier. I'm not MeidoDev >>11446, he's going for ultralight. Tbh, I might not do that thing with the additional water, but try to put more batteries, dielectric fluid or bigger motors into her design.

# 93
>>12949
lol. sorry, but you won't badger me by such talk. we're not women here on /robowaifu/. disprove my position with physics if you're so set against my point. I've encountered and proven sufficiently well the issue numerous times with racing designs.

it's simple lever mechanics: take a 1m long stick and and 1kg weight. Perform two experiments with said setup:
1. Pivot the lever with the weight attached to it down right at the pivot point.
2. Pivot the lever with the weight attached to it out at the end of the lever.

What else do I need say? That's the 'thrown-weight' issue in a nutshell.

Exerting unnecessary energy through poor designs will be detrimental to a robowaifu in every way. Extra energy consumption, extra heat production, extra mass added to joints, connectors, fasteners, etc., to deal with the extra forces needed. Awkward motions in the kinematics. Slow motions in the kinematics. 

Costs go up in every area, financially and otherwise. 

Keep mass inboard, and you'll improve basically every area of your designs.

# 94
>>12952
>disprove my position with physics 
I didn't attack your arguments fundamentals based in physics. It's about repeating it at every opportunity again. I don't build a robot optimized for walking. Context, priorities and constraints matter. Feel free to build one without the batteries in the legs, and make them as light as empty bottles. But I wont.

# 95
>>12935
Here're my early and crude prototypes for the femure (upper leg bone) so far. The challenge is to make the part as huge as possible to hold as many batteries or other things (maybe motors), but make it so that the bone can't be felt from the outside and also leave space for soft tissue, the muscle movement and muscle mimicry on the outside. Currently I'm assuming that 9x9 or better 8x8 cm femure bone diameter might be the maximum, and that only in a rather tall or thick robowaifu. 
Transitional elements between parts with different sizes are still difficult to me to do in Solvespace, but here it wouldn't be visible anyways and it's just me trying something out anyways. Maybe such parts need to be sculpted in something like Blender and then imported. Also, blue was maybe a bad choice for the sample, looks rather sick.
The smaller holes in the first part are also just an example. Those might be used for steel rods or these hollow metal tubes similar to broom sticks, to make the thing more resilient against shocks. But could also hold cables or water tubes/hoses, or guide some strings, though I think except of the cables these things would rater go into the soft part outside the bone.
What's also missing in that model so far, are the heat exchangers for watercooling the batteries, which would need connectors to the water hoses inside or outside the bones. Later I will also need to think about how to transfer water from one part of the body to another, since all hoses tend to break when being bend very often.

# 96
>>12954
This is a nice design Anon. Looks like it would have a good strength-to-weight ratio too. Please keep going with it!

# 97
>>13091
Thanks, I will keep going but have various things to do. My motors for testing the spine also seem to be already in the country. I see often videos on problems with backlog in logistics but I'm still getting my stiff surprisingly fast.

# 98
My 2019 prototype, it costs me 100 usd to build it w/o sex doll price.

Now I am thinking to a whole new design but I would need a lot more money to do that, so have to wait.

I used an Arduino Leonardo board and 4 or 5 servo motors.

The mechanism was to use a lot of strings as tendon, similar as this prototype https://www.youtube.com/watch?v=0ZBD2tcKOU4

# 99
I used 500lb braided fishing line as string/tendon.

# 100
>>13541
Post her mechanics and circuits. Nice job

# 101
>>13544

Thank you :p

Since it's an old prototype, ive deleted everything except this.

But here's how I did it globally:
Red are servo and green is the fishing line.
One fishing line per axis, thus 4 servos.

The circuit is not that complex, It's similar as https://www.youtube.com/watch?v=ZySGP4AwGCY[Embed]

The servo were initially 180 degree locked but ive unlocked to 360 degree.
https://www.youtube.com/watch?v=JhHSXCLsN4k

The servo I used is https://www.aliexpress.com/item/33010787343.html
And its battery: https://www.aliexpress.com/item/1005003043860597.html

Small and high torque, perfectly fit into my 100cm sex doll

For the new prototype, I plan to work on a 128cm sex doll from now on, I will have more space for servos and electronic board.

And I will switch to STM32 black pill board, I found its programming way more interesting.

Basically I will deport the leg mechanism to the thigh instead and will reserve the chest for other further mechanism.

# 102
Oh no, I am realizing that the new design has a flaw, if it's designed like that it's the leg that will lift the whole body by its own, it's good but I also want the opposite.

Now I am aware it's the abdominal muscles that are responsible of the lifting leg mechanism.

Rip, thus I have to combine old and new design to have a full leg mechanism.

# 103
>>13552
Judging from her high mass and the use of a set doll, she's going to lay in bed and be a sex robot only, right? You did a good job on her skeleton and you're using good electronics to animate her. Looking forward to seeing how this goes. Also, I'd put her servos in her belly, then she won't have to move there mass.

# 104
>>13557

For now yes, I have in mind that we can only produce the first Humanoid with the help of sex industry since the amount of money it produces.

So now she belong to the bed lole

Thank you and yes, I am ignoring the belly too much, it's also due to the sex doll shape that has wasp waist.

I should buy one with a normal shaped waist and also make my own skeleton to optimize the space even more.

# 105
Thanks for sharing. 
You might want to check out my Genera Platform (aka Genera Project) from time to time. I doesn't have a thread on it's own yet, and only making slow progress. It's also based on a endoskeleton instead of a shell. I'm currently posting my prototypes in the thread for prototypes and failures: >>418

# 106
>>12954
So, I uploaded some new files to my Mega account, which I linked here: >>12661
I got my JMT FN15844 BLDC motors which I want to use, for testing at least.  For my spine and for some arm. I designed some files to add other parts to each of them. One way is using twisted string actuators, but I now hopefully found a way to finally get some cycloidal disks as well. 
This is all sketchy for now, I didn't print not test them yet. Just wanted to give some update.

# 107
>>13704
Still using Solvespaace? Your designs are getting really good considering the software limitations. Hope to see them irl soon

# 108
>>13704
I also created some way to create a diagram in Solvespace to have an overview over the system. I just realized it also needs some minor fine work till it's finished and can be used by others. I want it to look like in the last picture, so without the green squares, but then with the added parts and pointers. It is meant to be used by others to make such a diagram, but also to show off my design approach in a version of it. Like in picture one. The second picture is a well known pattern for drawing anime waifus which I uploaded already somewhere else. I used that to make the female form in the diagram, which should be usable by others for their designs as well.

# 109
>>13709
I was also working on some human-like knee. Just a test or feasibility study. Also unfinished. BTW, I decided to upload my files faster, but if I didn't even rename the internal parts properly then the files are in a subfolder named 'sketchy-in-progress' or so. Those will need some workover but they are now there as a backup.
>>13708
>Still using Solvespace? 
It's lightweight and I want to do as much as possible in parametric design (CAD).

# 110
>>13710
Two other parts which I didn't even upload yet, are my first test on a 3D printable 'helmet hair' which would be printable in TPU and would then house some parts, so the rest of the head would therefore be smaller (if anyone wanted to complain about weight). This is also just some idea I want to try out since I saw something in an anime inspiring me to that. Doesn't mean I'll end up with that, but I'd like to develop it a bit to be an option to 'normal' hair. The helmet-hair could be printed with low infill and then be quite soft, but still house some electronics.
The other one is my idea for a loaded-spring actuator for the arm, where the motor in the elbow loads a spring via some kind of chain, while the arm is down. Some mechanism, most likely a solenoid, would then block the spring till the arm needs to be lifted, and add some initial force to the whole thing. The chain or 'snake' would internally bend around the elbow and moving up while doing so. 
Don't know if this is going to work, but I intent to try it out. Some of the robots from therobotstudio use rubber bands to do something similar, which inspired me to try something like it. But I'd prefer a spring over a rubber band since it should last longer.

# 111
>>13702
Impressive, Iam far from doing research on skeleton mechanism with the help of CAD tool due to the lack of knowledge of that, I barely know how to make a bunny with a 3D printer lol

When I will start doing the skeleton design, it might be a good idea to take a closer look of CAD mechanism design, thanks for the link.

# 112
>>13717
Solvespace and probably parametric design skills in general aren't that hard to learn. After going through some tutorials it's just about training and experience. Difficult is it, if you want a skeleton being very close to a human one and that might require combining CAD and sculpting or importing STL files. If you just want some tubes which move, that should be easy to do. 
I'm getting stuck on being to ambitious sometimes, then failing, getting a frustrated or tired of it and then getting distracted. Problem is, I'm going for the most ambitious version of robwaifus - the very human looking ones.

# 113
>>13720

Nice, I think Ive already heard those word years before, the parametric design stuff, thanks for the sum up.

Ye, that's the problem with project, if we do not get fast result we can be happy with, we can be quickly demoralized.

I wanted to make the perfect robot in the first design draft but the reality is the lack of money and I wish to build an acceptable robot sex doll at around 10k $

It's a real challenge and I cannot afford making very complex mechanism since it will cost too high at production chain. thus the challenge is to find existent mechanism and to deal with it.

So I did it with this 3rd prototype and when I seen the leg moving up, it was so exciting heh, the first discover of a new lifeform :D

# 114
>>13720

https://www.aliexpress.com/item/33007068179.html
Here, a 100cm humanoid that cost €35k lole

I wonder if this robot can move with a silicon skin on

# 115
>>13753
Not sure if this posting was serious or if you're trolling. The 3rd prototype refers to the one in the first posting, or to the dog?
>>13766
Too expensive and not good enough.

# 116
>>13786

lole, the 3rd prototype was in the first posting ye and this dog is here to fill the post space :D

# 117
>>13796
Then I'm glad, because of this concerned me:
> when I seen the leg moving up, it was so exciting heh

# 118
>>13704
So, I'm on it. Time to make a separate thread soon, I guess. Tested the twisted sting actuator a few minutes ago a little bit. It felt strong, but my whole setup is currently too finicky to do propper testing.
Getting the connectors and holders printed was also a bit harder than anticipated. The holes on the lower end of the motors aren't really parallel, I guess. Will need to improve that, now only two screws hold the "arm". Getting the twister on top  (holder for the strings) right was also quite some trial and error. 
Also ran into another issue with my printer because I forget to fasten the nozzle while it was hot. So it created some hot plastic mess around the hotend, and the nozzle came out further through the pressure and so it got closer to the printbed nearly scratching it.
Whatever, the robowaifus will come.

# 119
>>13931
Good to see progress. Do keep in mind that she will need a agonist and antagonist pair. I would recommend adding gears so that one pair winds as the other unwinds.

# 120
>>13937
>adding gears
Ah, I think I know what you mean. I'll keep that idea in mind. Thanks. However, I plant to use very different muscles dependent on the movement, and this is a very early design. I'll try at first to get an arm lifting itself up and then going down through gravity after release. I also plan to add a cycloidal drive to the ellbow.

# 121
>>13962
You should draw a general picture of what you're trying to make. It will help your fellow anons understand your intentions and provide better guidance and advice.

# 122
>>13970
Maybe I will. Though, I haven't decided on every detail myself. It's more of a general thing to mention, that the arm won't need the same force to lift than to fall down again. Then for pushing something, another actuator might be better than a twisted string actuator.

# 123
I printed some parts of the spine prototype based on my design above >>12923. I printed one in full size and five at 40% or so, to build a little model without motors but screws instead to test it. Just need to buy some glue, and then design and print a rack for the whole thing.
Also printed some shoulder part here >>9142 to test it. It helps to have it in my hands to imagine where to go with it. Now I have some more specific ideas how to use it. I already flattend the edge, so I can add motors to both sides. Other movements will probably be done with some string actuators.

# 124
>>13998
Glad you're learning how to improve it as you go. Do remember that walls bring prints strength, not infill. You can save a lot of mass without losing any strength by keeping parts like this 2 walls with 5 percent infill to help with bridging the large flat tops.

# 125
>>14003
Yeah, I was using 15% infill and two walls, which is probably more than necessary for a test. Thanks for the hint. However, printing isn't what's eating my time, designing and doing other unrelated  things takes much more of it.

# 126
>>13541

OP, I'm going to be merging your prototype thread into our already-standing general prototype thread soon. Please keep us all up to date on your work, good luck.

# 127
>>14092

Oke and about this project I cannot do much now since the ongoing prototype will cost much more, thus I pause this project and do others meanwhile.

Finding a job might be a good idea for the sake of that project lol

# 128
>>14092
Maybe it would fit better into the prototypes and failures thread. It's a prototype, not general engineering, and also conceptually closer to my Genera Plattform than other approaches, and I'm posting my files there for now.

# 129
>>13998
So, my progress is still very sluggish. I looked a bit into imageboards and hosting while the board seemed to be under peril. Got a bit stuck on 4chan as well, and also looked into which Linux distro to choose for the future. Which is kind of related anyways. However, I started to work on the rack to hold the spine.
Picrel is just held up by a toothpick, and that's not what I meant. I'm designing a small holder with manual twisters to roll up some strings, so I can see how it behaves in this small model. Then I'll print one which holds the motors for the bigger one. 
I really need only a few hours per design, to get at least something interesting, so it should go faster now

# 130
>>14111
I started to use the references for the bigger one, till I realized this could be a problem if I want to use it on the small one. I probably can't just scale everything down in form of the STL file, bc some parts might be to small then. I hope I'll finish this tomorrow.

- I will also need to buy some protective goggles to use while cutting down steel tube for the bones. 

- I was also already spending time on renaming the different workplane layers in my 3D files, so I can upload the files as polished version. It gets messy without proper naming. I already try to start naming these layers directly after creating them, so I don't have to look into it later and also to make my own work easier.

- Then I also need to write some intro for the first posting to finally create the official thread to this project.

# 131
>>14111
Just some helpful advice, your printers bed needs to be leveled and you have some minor over extrusion. I've had those problems too and fixing them sooner is better then later. As for your design, it's pretty complex. I mean you'd just fine having a few with a semi flexible spinal material running through them. It would make the design easier to articulate while reducing mass.
https://www.youtube.com/watch?v=EUEp-AfvvzE

# 132
>>14113
Sorry, but I have to more or less deny all of this. My printer bed is quite well leveled out. I also don't believe you can tell that from looking at these pics. Then I know about the overextension, but I don't think this is important. Getting FDM prints perfect can also be quite a waste of time, and here its about prototypes and internal elements. I spend way too much time tuning my printer when I got it. The real problem I detected is, that gluing the parts together can produce irregularities. Might be less of a problem with the bigger parts, though. I also wasn't careful when I worked on that.
As for you alternate design, I'm not interested in a simplified model. Otherwise I would have gone with that. It absolutely doesn't fit into my plans. I'll make it even much more complex, by adding a human-like s-curve to it later. This is the most  simplified version already. Though, I might try out other approaches as well.

# 133
>>14102

>>14104

Alright, will do. I'll merge your thread here soon: >>418

# 134
>>14114
Hey, spine-guy, how much do you actually know about the human spine? I've been trying to figure out which thoracic vertebra would be the hardest to reach with the hands. I was thinking of having a rod sticking out of the back, somewhere it couldn't get in the way, to help support the body while trying to figure out movement. From this diagram I'm going to guess it's the 4th or 5th from the top.

# 135
>>14159
Sorry I don't know and I'm not sure if I understand your question. If you look at the back of someone bending forward, afk or in a video, you'll probably see all bones of the vertebrae. I think the ribs around the 7th from the top might be harder to see and feel, because of the shoulder plates and muscles.

# 136
>>14112
Still on it, but it's trial and error. I made some mistakes and had to change and reprint it every time. Now it's glued together. Though, it hasn't been tested with the strings yet. The final version also needs to be printed with more infill, since the base gave in to pressure I had to put on it. I also took care of overextrusion like >>14113 above recommended. I had the Gcode for it in my config already anyways. The print still isn't pretty, but this doesn't matter and can be minimized easily.
Then, I got a bit into face design in this paper craft style here >>271, but printed out of plastics, like mentioned here >>14124. It's also just a case study or early prototype for now, though. I'll post the images from my other computer.

# 137
>>14165
Your project has much potential. It'll be a long road to get things just right, stay strong.
>Papercraft face
Please do share your work in the waifu face dev thread. We can all use this. Face development is one of the hardest nuts to crack.

# 138
>>14165
I'm working with my current spine model now, trying to add some strings. Which is as annoying as it sounds. The thought crossed my mind, that this approach was a mistake and I should've printed it bigger from the start, since I'm using cheap plastics anyways. I'm glad that the twisters at least hold onto the knobs at the plate. I was concerned that I might need some more complex design and redo the whole thing. 
>>14167
>Please do share your work in the waifu face dev thread. We can all use this. 
My current policy or MO is to upload my prototype designs here in this thread. Then I add crosslinks to the other threads where it might fit in, which ideally other people should do more as well with their postings of designs. I also upload my designs to my Megashare account after a while. It's some additional work to do, so I only do that once a week or so. I then intent to link it again sometime in the threads covering some specific topic, when I reach a real milestone.
I think the papercraft inspired chibi design in plastic idea is promising. For placeholders or simple robowaifus. The face can be a little bit 3D, and it could alternatively also be molded with silicone to be soft and skin-like. Designing and printing a fitting head should also be rather easy, in a simple form or more complex with a round back out of TPU (soft plastic). However, as you can see, I'm not an artist with drawing experience, so I'll need to do some work on it. This early design also has some error, indicated by the red edges.
>Face development is one of the hardest nuts to crack.
Yes, it's even harder if you want some kind of skull and soft skin. Everything very human-like. The Alita Battle Angel bust is the reference for the top notch model, but it also has to move, needs a mouth with a moving tongue and needs to have facial expressions >:-D ... long way to go :-c

# 139
>>14160
I really don't know how to explain what I said any better than I did. Trying to scratch your own back with your bare hands, which vertebrae do you think would be hardest to reach?

# 140
>>14170
I can reach all, but I'd say 6th or 7th. However, I don't really know.There might be articles to find on this.

# 141
>>14168
I caught some passion for that side-project, and went on designed a simple head. Finally found out about how to pick any color, since the color picker doesn't really work. So I can use some skin tones now, besides orange, yellow and brown. However, adding even more and more complex hair made my system starting to get sluggish, at least while having other programs open, so I might look into installing my Linux on the laptop first. Or I can still work on the spine and the face. We'll see.

# 142
>>14168
I think I have to give the spine model a work over. I didn't consider that it wants to fall over to much in one direction. It's also difficult in general to roll the stings up and to keep it from moving in unwanted ways. This might be in part due irregularities in the balls I'm using, and in part simply because it is based on spheres in the first place. 
Now I'm considering something even more similar to the human spine, since this might work better: Something flatter instead of balls, but with round corners. Maybe also higher at the back than the front to mitigate the tendency to bend backwards. I considered such adjustments anyways, but I thought to introduce them later to keep it simple at first.

I also had the idea of putting up a paper diagram on some door with all the parts I'm currently or soon working on, with a progress score attached to each. Like 'Arm TSA 1', 'Pelvis 0' or 'Knee 1'. Currently it has 15 points with low scores. From time to time I'm picking the one I'm most motivated to work on, instead of getting stuck with one part.

# 143
>>14199
I made some progress during the last few days, but nothing big. 
First, a kind of rig for my current shoulder joint design, with also some holes added. I want to try out  different approaches in terms how to add motors or muscles to it, so I came up with this. The red holes go through the part and may be able to move the other part attached on the other side (right/outside) in two different directions. Obviously, a motor could be at the joint (in pink) moving it in both directions, but I want this to be fixed in that direction while strings pull the other part, which might be the arm, along the bigger part. In this test rig the outer part may or may not be fixed to the plate and then move the outer part or the big blue one. 
I also started do to design a "simple" elbow joint, which got more and more complex. It's just for testing my twisted string actuator, while not having a motor in the elbow for now. The red bars are supports. I added them in the design, so I don't need the slicer to add them, which would be much worse. Screws should go into the place where these bars are, though I might try to put in some roller bearings in a later version.  
Then, I had to come up with a new way of designing an eye for my face. Because the old one didn't work and trying to fix it cost me time without any gain beyond some experience. The new one is just a sketch so far, but it's way simpler to change. Surprisingly it's easier to use a Bezier spline with defined constraints, than using arches and line segments.
I also made a calculation, that I could more or less design on part in one day or make a mayor improvement in the same time. Even if printing, testing and correcting takes another day or a bit more and I'll have sometimes other things to do, or slacking off for some time, it should be possible to create 100 parts or improvements per year. I plan to use this as a benchmark for myself from now on. Hundred new designs or improvements per year should be the minimum.

# 144
>>14274
Very impressive work Anon. Your efforts just continue to improve as is evident for all to see. On another level, you're also an encouragement to me personally. I too have been working to improve my craft towards achievements of reliable robowaifu software. It's a long and challenging road for me, but I too have made some nice progress in the last few days. I'll plan to post an concept intro release  sometime over the coming weekend.

Please stay encouraged Anon, you're a blessing to us all.

# 145
>>14199
>I didn't consider that it wants to fall over to much in one direction.

Yes, gravity is a swine when it comes ball joints (well, any joint not linked to a powered servo, really). Can't really model it without a proper simulation either, so it's easy to make mistakes. I found it was best to constrain joints to certain axis of motion like X and Y. Which you appear to be already doing in >>14274, so nice progress!

One question tho, anon. What are the threaded rods at the bottom of the torso going to be for? Are they intended to let the whole spine assembly move up and down?

# 146
>>14275
Thanks. Looking forward to it.

>>14280
The problem with the ball joints is something I should have seen coming, but overlooked it. I'll find another way. I remembered, that my first ideas was to go with some kind of saddle joint anyways. Just went with the idea of ball joints on a whim. There are other options.
>What are the threaded rods at the bottom of the torso going to be for? Are they intended to let the whole spine assembly move up and down?
They are meant to hold the whole thing in place, till it's pulled in one direction but still restrained by the other stings. Which was a naive idea, I know. Wanted to try it out and thought it was easier to do so than it really was. These rods also represent the twisted string actuators I plan to put into the full scale model.

>>14274
Today and yesterday night I worked on some improvements:
I gave up on the bad design of the eyes in my test face, and implemented the new approach I mentioned before, based on Bezier splines. It's still not good looking but the underlying technique is way better now, and I can change it more easily. I'm glad I found that way by just trying out something. It only works with creating the Bezier spline in a certain way, otherwise it has more than four points which need to be constrained. Though, the whole idea of the printed face might go nowhere, since printed paper faces of anime characters might look better anyways. Then again, not anyone has a color printer for dead trees or a printshop close by and there might be other benefits. It's slightly 3D for example. The old design was severely flawed, because I made the mistake of picking the wrong layer to build upon. This is something to look out for, happens sometimes to me and can be very annoying. Let's say the eyes and eyebrows weren't really attached to the face in the old design, it only looked like it from the front, but there was a gap in between. That is solved now. For the future I will need to look at some more anime faces to see if and how I can improve the new design.
Then I had to add some supports to my shoulder joint design, which I don't even know if it will go anywhere. I have a few other approaches in mind as well. However, the holes for the strings needed some support and I prefer to put such into the CAD design myself. This also proved more tricky than anticipated since it's fairly complex. I printed a sized down model of it and it looks good so far, but the test setup still isn't finished. 
Then, my elbow joint also made some progress and has been (partially) printed. 

The photos of my prints are on my tablet, so no photos here but nothing special to see anyways. I hope to focus on the elbow joint and motor holder next, so I can test part of my arm design with the twisted string actuator soon. Also need to cut the tubes and need to make the electronic wire setup less flimsy first, though.

# 147
>>14299
Today was a bit of a dud. Got a clog in my printer. Most likely kind of my fault, I hope, since this is better than a problem with the printer. Fell out of routine during my time without printing, and forgot stuff. I pulled on the filament to get it out, while the nozzle was at 100°C. Should have heated it up to 160-200 first. It broke within the heatpipe, and now I have to disassemble the thing and push it out with a toothpick (again). The upside is, that I'm getting more and more used to this sh...stuff. Like a soldier reassembling his weapon.
However, maybe I'll still model something today, so I'll get something done. Days with archievements are just better. The pics are from yesterday. Got my waterbags, for testing my idea with using something alike as a muscle to hold the body bend in some way, without using the motors: Two bags with air, connected in the middle through a valve. Air is on one side through some movement, valve closes, body won't move back to the old state.

# 148
>>14312 
I had difficulties the last time I tried to design a motor holder mentioned here >>13931 since the holes on the bottom are kind of skewed. I think I found a way of getting around that, by looking at it in a different way. It's important to ignore the openings for cooling, and just focus on the relation of the holes to each other. 
Also had an idea for the holder of the motor, attached to the arm. I will probably use some slider lanes. I'll put the screws onto the bottom of the motor, sticking out, then it can be hanged into these lanes. Only the heads and some plastic would hold the motor, though. However, I could make the screws longer and plastic thicker, or at some point later make the holder at least partially out of metal.
Didn't print any of for now, since I didn't fix my printer yet. But I will, tonight.

# 149
>>14327
Is the pic #3 the one with 'slider lanes' Anon? Those look like they will hold another piece that fits into it very securely.

# 150
>>14327
These designs are very helpful for visualizing the general support structures inside a robowaifu's shell.

Thank you for making these.

# 151
>>14327
My printer works again. I'm really used to disassemble the head by now. It's still stressful, but I won't put it aside for two months again.
After printing my elbow design, I found several things to improve, some are already implemented. This includes the issue that I didn't think all things through and I have to do it now. Especially how to exactly holding these part together. No big deal, some more modelling, with try and error. Currently it is way to noisy when moving them around, even without motor. I'll make sure to reduce the friction and let smooth metal run on smooth metal. However, a more general test with a more crude design and the twisted string actuator might come first, since this is what I'm longing for.

>>14328
>Is the pic #3 the one with 'slider lanes' Anon?
Yes, pic #3 in >>14327, pic #2 should give you the idea. The screws are like a cross, the two screws in the middle need to slide down further.

# 152
>>14299
>Thanks. Looking forward to it.
Y/W. Here's the little intro project Anon. (>>14353)

# 153
>>14349
Several things kept me from maintaining my speed. 
First of all, I started to think my current approach through a bit more. I wanted to build an arm out of tubes first. However, even a 18 mm tube might be a bit much for the lower arm. I probably should go with something more like picrel 4 from Hamcat_mmq, but with a motor. I also realized that with my current approach the elbow might get too thick, especially since I want to fit in a motor into the elbow later. I realized that if I don't try to get the full tube size from one part of the arm to the other, then I only need something very similar to two shelf holders connected with a pivot. I actually already tried to build something like Hamcat did, though not very good (picrel 5)  
While thinking about those things, I got back to work at some point and tried to finish the motor holder (picrel 1-3). Well. I had and still have problems, because I don't know how to properly add skewed parts. I need it to be skewed in relation to the arm (picrel 3). Maybe I can do it with two different parts on the bottom, to connect the tube, which I then screw together. Though, the problem also affected my ability to design a hook (picrel 1-3), which I need to test the whole design. I don't even know if that is going to work. I had the idea to make a hook and hang it onto some knob of my drawer, so I can test the motor.
Then I also ordered proper connectors for my ESC, since it needs XT-60 connectors and I only have the breadboard connectors to stick into it, which always fall out when the motor moves wildly around. Though, at least so nothing can go to wrong, since it stops automatically.
Finally, my printer has problems again. I managed to get brittle PLA, and I think a part is stuck in the extruder. So I might need to disassemble it once again, or twice if the heat break is clogged again.

# 154
>>14373
Turned out my printer is fine. It's just that cheap (and a bit old) PLA filament might get brittle if it rests without being rolled up again: https://youtu.be/SvpSxHLotMI - don't have a Boden tube but direct drive, but this is what happened. Gladly, I was able to push out the broken filament without disassembly.
I'm currently working a bit on that lower arm, since I looked at it again and think I can do it. Related: >>14397
I could do more, but I'm watching a bit too much YouTube again...

# 155
>>14399
Looks good, but failed for now. I still think this approach to the lower arm is what I want to go with. However, after printing a miniature version I realized that it is harder to do than I hoped for. Ideal would be some simulation with movements, that marks or even subtracts conflicting parts of the design. The white bone needs to be able to role left and right, but in either case it needs to roll over the blue bone. In the best case, these two would touch each other the hole time, so they would support each other. However, since this might not be necessary, that's one ideal that I should better give up. It might have been the reason why it failed.
I might be able to do it without such a simulation, but it will take quite some trial and error. So I should focus on other parts for now. I'll try it again at some point. Being able to print a miniature really helps. This whole thing is generally just part of the bigger ideal of her being very human-like. Making humans is hard. So, maybe I should go with something simpler for the start.

# 156
>>14474
Oh, I forgot: Picrel one above is something I gave up on already, but I might need to revive later. Cutting out the white bone from the side, using a Bezier spline. I messed up saving the file after I did that, though. Then I thought I don't need it anyways, which kept me going.

# 157
>>14474
wow, that looks like a very clever approach. nice one anon.

# 158
>>14474
I made progress with my elbow and arm design, but can't test it right now at nighttime. I already connected the motor mount and tested it, including the strength of the twisted string actuator a little bit. I had to change some parts of the "simple" elbow hinge, which took me some time. Also needed to create some mount to attach the whole thing to my drawer, so I can test the arm (picrel 1). 
I also started to work on a design for a pelvis (picrel 2 and 3). I planed to use a stl file based on a human bone model, slice it, simplify it and make it malleable with parts in parametric design. But now I started a model from the scratch. Don't know if that will work out, but I can do it now and it might be less stressful. It's just important anyways, that the parts which are visible or perceptible to touch through the skin are similar to a human female. Internally I need to use the space differently, since for example the hips should hold two motors with cycloidal drives.

# 159
>>14567
> It's just important anyways, that the parts which are visible or perceptible to touch through the skin are similar to a human female.
This. Really good insights, Anon. There's little doubt that doing our best to mimic real female body structures will greatly enhance the pleasure and comfort of owning such a robowaifu.

# 160
>>14567
So, technically the first build of the Genera Plattform moved a limb for the first time today. Some minutes ago.
I got the elbow moving, also with various provisional arms attached. Of course, I directly ran into several problems, but it still looks very promising. 
- The motor is not a servo. It can't measure where it is, nor can the arm signal it to the motor where it is, since there are no sensors at all yet. So, the arm goes up, then I have to turn the motor of and the arm goes down. Not a problem. Won't be the only actuator anyways and I realized that it only needs to lift the arm up to 90°, then a weaker but more precise one can take over. I also plan to track the position of the arm of course, and hope the twisted string actuator will be a bit more controllable that way. With no load, I can even not look at it, only give a brief burst and it is up. 
- Brings us to the other problem, that my holder for the motor isn't very strong, so if the movement goes to far then it takes the whole thing apart and even twists the cables of the motor.
- Last but not least, rewinding the strings is a problem. Though, this might be in part because my test controller for the bldc motor doesn't do reverse. Just adding a counter actuator will definitely not work. The strings can twist so hard that it is difficult to unroll them. The arm going down also doesn't mean that it unrolls. Maybe then sting is to flexible and long. Need to learn more about it.

# 161
>>14572
Little clarification: The arm might need to go up 90-180° till another (mybe weaker) motor can take over alone. It depends where it starts and if the shoulder moves as well.

# 162
>>14572
>So, technically the first build of the Genera Plattform moved a limb for the first time today. 
Grats! You're making solid progress now, Anon. I also appreciate the improvisational approach for adapting to the environment for you robowaifu R&D lab, whatever the circumstances! :^)

# 163
>>14572
Great job but, your motor mount is very thin for an actuator with the kind of power that bldc can give off. The base would also benefit from being able to pivot. You will need to implement a controller that can reverse and an opposing twisted string so the arm can move forward and back as needed. 

I also recommend using a non backdrivable geartrain to prevent unwanted unwinding.

# 164
>>14592
>motor mount is  very thin 
Yes, I'm going to make it stronger. Currently the problem is rather that it is even only sticked together. Not one print nor welded or glued. PLA is very strong, so I'm not worried about the strength of the part, really.
>The base would also benefit from being able to pivot. 
I don't know how you mean that, but I'm going to  watch some TWSA videos, which might have similar advice.
>need ... controller that can reverse 
That I already realized.
>and an opposing twisted string 
That you told me before, but I don't know how yet and not sure if I need it (at this point). The arm would fall down due gravity, just by unrolling the string. It even does so, by stopping the motor, but it doesn't unroll completely.
>also recommend using a non backdrivable geartrain to prevent unwanted unwinding.
Thanks, I'll look into that.

# 165
>>14594



Hi, long time no see



I have an idea that aim to resolve the freedom of rotation of joint.



It's to use a stainless steel chain and to allow roll axis maybe adding more links will make the roll rotation even better.



I am skipping the joint ball prototyping because it's too much difficult to put it in place.



Hope I will be able to rework on that project soon, it miss me so much heh.



Cheers

# 166
>>15293
Hi Evodoll, good to hear from you!

# 167
>>15293

Welcome back Evodoll, your idea to use a chain a flexible shaft is pretty clever and I look forward to seeing how it works out. Wishing you the best!

# 168
>>15303

>>15304



Thank you guys, challenges await me !

# 169
Almost done developing a simple easy to print and assemble omni wheel. Most of the ones I found online for printing are not designed to be circular and are harder to assemble. This just requires bar-b-q stiks which are eaily gotten at the Dollar Tree rather then screws. This is the first working protoype with a 4 inch (100 mm) diameter.

# 170
>>15686
Brilliant work lad. So question; is this primarily to be a passive 'roller', or do you intend it to be an active 'locomotor' eventually?

>This just requires bar-b-q stiks which are eaily gotten at the Dollar Tree rather then screws.
I assume some kind of glue or other fastening mechanism is req'd for the stick ends? Or maybe they're tight fit enough?

BTW, I greatly applaud your focus on 'cheap & easy' Anon. This is exactly how we'll see robowaifus reach a very broad segment of men everywhere.

# 171
>>15689

Designed to work both passively and actively.

>Maybe they're tight fit enough?

This is correct, designed to be easily put together by shoving the stick in then cutting the end off.



Here's the next result, it works but is a tad big at 2.5 inches thick and 4 inches in diameter though it barely costs anything to make.

# 172
>>15695
Curious how the locomotion version is going to, well, ''locomote'' Anon? Do you have a clear vision worked out for that yet, prototypes maybe even?

I'm really glad to hear the manufacture is both easy and inexpensive Kiwi. Perfect combo!

Cheers.

# 173
>>15761

By rolling Chobitsu Kun. The friction between wood and PETG/PLA is pretty low. Right now I'm trying to make the mechanism flatter and print faster. PETG/PLA also don't have a high coefficient of friction on most materials. Due to this, I'm looking into materials that will help in the transfer of kinetic energy from wheel to surface. I'm thinking of O-rings at the moment.

# 174
>>15765
>By rolling Chobitsu Kun.
haha, make sense. I suppose your mention of the O-rings, along with your previous posts about elastic bands as force & rotation drivers pretty much answers my questions.

It's going to be great to see unified, modular roller 'feet' available to all our robowaifu kits Kiwi. Drive on! :^)

# 175
Nylon planetary gearset with 78 ring teeth, 32 planetary teeth, and 12 sun for a 7.5 gear reduction ratio. I fucked up the ratio (78-12)/2=33, which is the correct number of planet gear teeth. I also had bad warping on the gear teeth.

# 176
>>15890

Looks really cool. But if the nylon is warping why not try printing it in PLA?

# 177
>>15890
Looks pretty cool though Anon. Can someone here explain to the uninitiate what a planetary gearset is for? I mean what is the primary purpose/benefit it serves? Can they improve some things?

# 178
>>15894

>What is a planetary gearset (they are also known as epicyclic gearing)?

A gear train which relies on three basic element types: sun gear in the center, planet gears which "orbit" the sun gear, and a ring or annular gear which has internal teeth that engage the planet gears. The calculations for gear ratios depend on what element is being driven and which element is used as the output. 

This website provides a very helpful visual interface for understanding the relationship between the elements: https://www.thecatalystis.com/gears/

This website provides some good general knowledge with helpful explanations on the math involved in calculating gear ratios: https://woodgears.ca/gear/planetary.html



>Why use it?

Planetary geartrains are legendary in many engineering applications for their high efficiency (generally over 95%) and their ability to create large gear ratios in compact spaces with few gears. A notable advantage they have for 3D printing is the distribution of torque across multiple planets which engage the sun and outer ring. This allows for a higher torque density (the gears can be smaller than other geartrain types for the same torque requirements). Though I would suggest always designing 3D printed gears to be thicker with stronger teeth than is required. 



They also look cool.

(Pic actually related, she is a clock/automata with planetary and many other geartrains)

# 179
>>15899
Ahh. So, could the outer, ring-gear be affixed to say, a thigh-strut framework, and the inner, sun-gear be affixed to a drive motor? Sort of as a way to increase the torque for driving the upper leg motions of a robowaifu? Is this a legit way to understand these things or no?

>(Pic actually related, she is a clock/automata with planetary and many other geartrains)
She's pretty wonderful robowaifu too.

# 180
>>15904

>Outer ring as output, driven by the sun gear, with stationary planets.

That's definitely an option, would look really cool too. 

**It's really nice to find someone else who appreciates RyuZU, she's been a favorite of mine since the Clockwork Planet anime aired years ago, actually got me into automata and clockwork mechanics. Hidden for off topic**

# 181
>>15907
Great thanks! That helps me out understanding things quite a bit Anon.

>also
**>inb4 Kiwi is henceforth known simply as the entity ''' 'Y' '''**
AnchoR is breddy wonderful too. In fact, scene-related is one of the most touching moments in all animu IMO. Certainly it touches on an incredibly broad swath of topics and interests for us here on /robowaifu/.
>

# 182
>>15909

Finally starting get the hang of resin printing. It's actually pretty easy, and with way better mechanical accuracy then filament prints. Shout out to RiCODev, his advice saved me a lot of trouble and trial and error. No idea what he was going on about with needing supports, I don't use them and everything is fine. Don't overshake your resin, your prints will have many bubbles like these do. Also, you must be very careful with cleaning the build plate after every print or else your print may end up stuck to the platic on the bottom of the resin vat. The key to successful designs is to shrink the part which touches the build plate to accomodate the first few layers expansion. Also, larger prints should be hollow with holes punched into the shell to releive hydrolic pressure, very grateful to have learned that from RiCODev's warnings. Also, rounding edges to create continuous edges helps, as you can see the overhang is a continuous rounded feature.



>Y

Very tempting, I've been thinking of changing my name as I do not wish to be associated with KiwiCo and other existing businesses that I'm not affiliated with.

# 183
>>15904
You'd usually get your highest gear ratio from having the ring embedded in the robot frame and the output shaft connected to the planetary gears, with an "carrier arm" attached to the bearings.

# 184
>>15914

I hate my ender printer and im sure sticking to the bed in the first place would not be as much of an issue with resin printing. What would be a good resin printer to buy?

# 185
>>15926

I've only used the Anycubic Photon Mono 4K so, I would have to recommend that. This is a good price for it: https://www.amazon.com/ANYCUBIC-Photon-Resin-Printer-Clear/dp/B09Q93Y374 I too hate my Ender 3, though for bed adhesion resin printers need the metal plate to be cleaned between every print, I use a paper towel to do this. I would also recommend a magnetic plate for the bed like: https://www.amazon.com/Sovol-3D-Upgraded-Platform-Magnetic/dp/B08LYP2VTT/ref=sr_1_2?crid=155V9SBK8WNCS&keywords=photon%2Bmono%2B4k%2Bflex&qid=1650305462&s=industrial&sprefix=photon%2Bmono%2B4k%2Bfle%2Cindustrial%2C184&sr=1-2&th=1 these make print removal much easier. Wishing you luck and success in your printing endevours.

# 186
Working on connectors that will work with both resin and filament printers, does anyone know why my resin sometimes creates a large protrusion where a substantial curve meets the build plate? I think it may be my resin, it's Sunlu and seems oddly difficult to work with compared to my friends Anycubic resin. (This failed design can only sustain a few pounds of force before catastrophic failure, oddly always on the left side.)

# 187
>>15964
Good shots, Kywy. Nice detail, good focus. May I suggest you add a soft fill light (checkout '3-point lighting') as well? It might give us all a better look at the details on the 'backside'. Just a 'reverse' white placard should be sufficient for a shot lit as in your picrel. No need for a bulb.

I'm unable to give you any information on the resin printing issue haven't done any myself yet. However, I want to encourage you again in your goals of inexpensive, easily-mastered construction techniques (and kits eventually?) This will be a tremendous benefit to the unskilled man who wants to create his own robowaifus but doesn't have any clue how to begin at first.

>tl;dr
Just imagine what the benefits would be to us if we could somehow travel back in time, and deliver our completed designs to our younger selves! :^)

Really looking forward to your designs to come Anon. Indeed for all of ours. Onward!

>===
-''add 'white placard' comment''

# 188
>>15926

I would encourage you to look at the larger machines (Elegoo saturn/Anycubic photon x), I know they cost a little more but the extra build area makes the difference between a toy with niche uses and a truly usable machine. Even if you only plan to do small parts, being able to shoot off an entire set at once is a game changer. I was able to make RiCOs arm overnight whereas it would have taken a few days on my old machine.



The extra resolution on the small 4K machines only offers a marginal quality improvement. Not worth trading for build volume.

# 189
>>15974

Been considering a Elegoo saturn myself as it has a similar build volume to what I already have with traditional 3D printing. 



Is it really worth getting? Have seen a lot of reviews claiming their units were defective or talking about how it's hit or miss whether resin printing is hazardous material cleaning time or 3D printing fun.

# 190
>>14572

Brief update. I'm learning OpenSCAD now. I want to be able to change files with only a few commands.

# 191
>>15975

If you need smooth organic features (no layer lines!) then yes. Otherwise, no. See my post in the Rico thread. 



Yes, the resin is toxic until cured. Read the MSDS for common resins, TL;DR: wear gloves, don't huff it, and you should be OK. Cleaning IS a PITA, you will probably find yourself avoiding resin printing in favor of FDM whenever possible. You will need a dedicated cleaning area.

# 192
>>15975

In the 3D printing thread >>94 other smoothing methods have been mentioned. Resin printing might be only worth if you want to print small models which need to be smooth, or for ones which need to be precise and smooth. FDM is the to-go method for a reason. I would rather buy small metal gears from Ali Express instead of printing them out of resin, but for prototyping it might be nice to print some placeholders.

# 193
>>15976
Great! Glad to hear from you again, GenerAnon. Good luck with your new efforts, keep going.

# 194
>>15976

Using OpenSCAD for this seems to be quite unexplored, but I had a hunch it would be the right way to go. Some things work quite simple. I wanted to cut out a chest from a cylinder using four half rings, and now I see even quite good results using just one. 



Other parts are just distorted spheres which are then surrounded by a hull, using the hull() operator.



robowaifu-OpenSCAD-tests.tar.gz: https://files.catbox.moe/v8rdf0.gz

# 195
>>15993
Neat! Looking forward to your prototype explorations Anon.

