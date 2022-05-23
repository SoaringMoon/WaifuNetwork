# 1
Basic design for an open source low cost robowaifu maid. Currently attempting to make a maid that looks like Ilulu from Miss Kobayashi's Dragon Maid. Right now she's an RC car with two servo steering. Will share designs when they're a tad better. Ultimate goal is cute dragon maid waifu that rolls around and gently listens to you while holding things for you.

# 2
>>11446
Cute! So I can't work out exactly how it moves. Are the two wheels going to be the powered wheels, or are they mostly for steering OP?

# 3
>>11447
She has a drive tail that  pushes her while her front servo "legs" steer her. I had problems getting small cheap motors to match their speeds without a microcontroller and encoders. This way is simpler and lower cost.

# 4
>>11446

>>11449

Very elegant design. I like how almost every part is either electronics or part of the structure. Of course the waifu decal holder too, nothing wasted XD



Also good idea with the rubber band tyres. I remember that wheels and grip were a pain when making small servo robots.

# 5
Nice work OP, I commend your initiative. We look forward to seeing your progress with your OSRM robowaifu!

# 6
Been working on a generic interconnect system to enable anyone to build full scale waifus that are reasonably durable cheaply and fast. Current system is going to use hooks that go on bamboo skewers that connect to groups of rings. This essentially allows for polygonal modeling in real space. Bamboo skewers are cheap, easily accessible and trimmed to exact lengths, and surprisingly durable when used as structural material. 

Picrel is first successful proof of concept and some ideas for a low poly body to try creating using this method.

# 7
>>11579
Neat. I have two modest packs of skewers I've been contemplating using in a tensegrity-type arrangement for structural components of a larger robowaifu. Pretty similar to yours, but using 3 or 4 skewers per structural element.

# 8
>>11580
I actually tried doing a tensegrity design with twine and bamboo. Unfortunately, the twine made the body really wobbly. The hook design also got really wobbly with anything substantial. I'm working on using clasps now. 

Some notes to help, simple knots in twine have a diameter of 3 mm, twine tends to be about 1.5 mm thick with a 1 mm slot being effective at holding the twine coming from the knot. I also recommend  printing a jig with two 1 mm slots spaced apart to repeatedly create lengths of string of a defined length. Tie a knot, pull the twine through the slots so that one knot is firmly against one slot then, tie a knot firmly against the other slot. This will give as many lengths of knot ended twine as you'd like.

If you get tensegrity to work, please share!

# 9
>>11581
>If you get tensegrity to work, please share!
I definitely will, but I'm not able to put a lot of focus on it atm, could be a long while.

# 10
>>11581
Though a failure, the concept of creating polygons in real space through clasp based lines and vertices is proven.

# 11
>>11586
Finally found a successful design

# 12
>>11595
Too floppy

# 13
>>11600
I'd recommend you investigate the space-frame designs used in racing cars Anon. Triangles, it's all about the triangles.

# 14
>>11606
Bretty cool advice anon. 
Started working with cheap TPU for simpler more durable connectors.

# 15
>>11613
Yup. The ancients back in the day figure out how/why tris work so well. There's a reason it's named '''Trig'''onometry, not Quadronometry. It's also why all polygonal meshes in 3D systems first decompose everything into triangles first before rendering, regardless of the higher-level forms they may be modeling.

# 16
Why don't you post the modeling/STL files for your connector designs somewhere for us to use here on /robowaifu/ Anon? Please license them as MIT (Expat) if you wouldn't mind thanks.

# 17
>>11613
Here's another nice example of space-frame oriented kit racecar chassis design.

http://spartanv8.com/

# 18
>>11614
>>11618
I'm constantly redesigning everything, each iteration usually being a major improvement. I'll start sharing designs when I've made ones that won't be immediately deprecated. 

I'm transitioning to a hybrid approach. I'll print "slices" of the waifu then connect them with triangles. See picrel for basic idea.

# 19
>>11651
Sounds good Anon, thanks. One thing you can do is glue paper, cloth, plastic sheets, etc., to the outer portion of your frames as a shell. Not only does this fill out the form of your robowaifu, but once the adhesive sets, the additional planar support to the frame struts actually helps to rigidize the entire spaceframe further.

This is a common technique with race cars, and is clearly visible in 2nd pic related, where welding of aluminum sheets to the tube frame was performed.
>>11614

# 20
>>11654
Published some  bamboo connectors here. https://www.thingiverse.com/thing:4914882

Any suggestions on what plastic to use as a support wrap for her frame? Keep in mind this needs to be inexpensive and easy for fellow anons to build

# 21
>>11667
As I recommended to Sophie Anon recently, you might be interested nine EVA foam and how it is used in cosplaying. This is probably the lightest material, which isn't paper or some film. 
Otherwise, I'm not sure if it can be handled carefully enough to make it save, but a lot of bottles for things like milk or some cleaners (cloride) are made of HDPE, which has a low melting point. 
Also, this guy from India in the video I posted a while ago used some kind of foam. Probably the same which is used for resin casting.

We have thread for materials by the way: >>154

# 22
>>11667
Settled on a simplified leg design that'll function as her driving suspension with a rubber band for a spring.

# 23
>>11681
Cool. You might check the ''Prototypes & Failures'' thread for some discussion on a somewhat similar design (>>418). Keep up with the design explorations Anon, you're making some headway!

# 24
>>11682
I actually started out with that design. From there, I simplified things to be as simple as possible. The key was that the knee joints needs to be exactly half the length of the hip joints.

Now I'm printing her modular ass but it'll take a long time.

# 25
>>11669
>>10315 is on the foam robot from that (probably) Indian guy.

# 26
>>11685
Nice. Good to see someone else attempting to build their robowaifu!

# 27
How are things going with OSRM-waifu OP? Any new progress?

# 28
>>11973
Steadily plugging away. Made some parts then realized the proportions and scale were wrong. A major revelation on how long it would take to 3D print parts at adult woman scale has complicated things. The problem with the bamboo plan was that cutting the skewers to length is getting increasingly labor and time intensive as more complexity is needed for her to function at human scale. I overestimated the strength of bamboo. 

The ultimate design goal is a simple to build open source robot waifu that would be cheap enough for everyone to build without being frustrating. 

Juggling these design goals has proven difficult at 1.5 m scale. I could easily build a 1 m roribot but, that would be "problematic."

# 29
>>11989
A 1m robot certainly wouldn't be problematic for me anon

# 30
>>11989
Those look like some very nicely-shaped parts Anon. The hips part especially has a great form. Nice mons, nice bunns, good overall design. I'd like to see a collage of several angles to judge these a little better too.

Yep, 3D printing takes time especially if it's one of the lower-end ones like mine is. There are little infill tricks and tips for making printing speed trade-offs. Remember you're a prototype maker, a frontiersman. It's naturally going to be taking you (and all the rest of us) several tries to get designs worked out and tweaked fully. That's why prototyping stages are basically always more expensive than final production. Keep this in mind and try to be patient.

Remember, a future anon who takes a fancy to your designs and decides he's like to use __your__ particular robowaifu project, will have relatively smooth-sailing, since you've already borne all the design headaches for him and other ahead of time!

I think if you'll attempt to use '''triangles''' (not just deltoid or any other angles) in your bamboo frame designs, you'll be shocked to discover just how strong it actually is. Remember: all 3 edges need to be securely fastened together at their vertex points. This is what makes a space frame out of it (look the term up).

As far as a roribot goes, do what you want. It's an engineering challenge, and one that's well-known. The '''Square-Cube Law''' bends it's knee to no man, same as all the laws of physics too. While you're in the prototyping phases -- particularly to keep testing costs down -- I'd actually suggest you specifically work on a 1m robowaifu prototype. Smaller is much cheaper and faster, and it's why toy manufacturers basically always have lower overheads than real hardware manufacturers.

Just stay aware that the smaller design is just a prototype, and you won't be allowed to market anything that looks childlike to the average boomer eyes.

Good luck Anon, you've already come well along in my opinion. Keep it up! :^)

# 31
>>11991
>>11994
Screw it, I'm building a 1 m fox girl.

Side note, is there any good place to upload non-final .obj and .stl files for other anons to collaborate on the design?

# 32
>>12027
Mega.io seems to work for that. Sophie Anon uses it. I didn't sign up yet, for unrelated reasons (computer/ broser). I should do that as well.

# 33
>>11989

A lot of the Japanese robowaifu devs tend to make theirs about 1m tall or smaller. I don't have a 3D printer yet but I imagine it would be best to prototype the parts on a smaller scale first before printing full-size ones. Personally I want to make my robowaifu prototype as small as possible: 1) to avoid issues with Normans 2) to save money 3) it's just cute. @DancingDoll_rz has made some awesome robotic dolls with full-body motion: http://dancingdoll-rz.com/main.htm

# 34
>>12027
As long as it's not over 200MB final, you can make a zip file and push it up to catbox.moe . It's what the board uses mostly.

# 35
>>12033
Sumomo-chan is such an adorabru moebot. I definitely want to make a line of robowaifus like this.

# 36
>>12033
Trouble is, to work with such small motors and fit all kind of things into such a small body. Think of the SBC and electronics alone. But good luck. One meter is more realistic.

# 37
>>12061
Not him, but you make a good point. OTOH, all engineering is a series of tradeoffs. 

Overall, situating components in a tight space is an easier problem to solve, particularly using CAD and 3D. But the laws of physics (and their indirectly corollaries such as the Square-Cube Law) are absolutely immovable.

Extra volume is a more-achievable luxury one can enjoy and take advantage of, with the more focus that's spent on reducing robowaifu mass overall. OSMR-Dev Anon is already on a good path in this area, as he is trying to make a fusion of 3D-printed parts + lightweight & strong organic bamboo structural spars. 

Good combination, you ask me.

# 38
>>12064
>Overall, situating components in a tight space is an easier problem to solve, particularly using CAD and 3D. 
If there's no space, none of that helps. Very small means smaler options of movement, bc no space for motors. If the chest would be smaller than a Raspi Zero, it would also be the question what kind of computer would be used. Sumomo can go everywhere. In reality she needs at least a small SBC which connect to others, or she alternativly would only have electronics relaying data to some external system.

# 39
>>12074
>If there's no space, none of that helps.
Fair enough, but I'd suggest an approach to solutions that doesn't involve anon going ''"It's impossible! Can't be done!11"'' It's can be fairly easy sometimes to jump to that kind of conclusion, particularly for something as **monumentally** complex as robowaifus.

The primary points are:
'''A''') All engineering is a series of tradeoffs. Find a combination that is sufficient along several axis-of-need's simultaneously. Pick any two (but only two):
'''cheap -- fast -- good'''
'''B''') The laws of physics ''cannot be violated''. Period, end of story. Our job here is to try and find the ways to work alongside them and still build cool and useful robowaifus.

# 40
>>12087
Since we're a robotics concern here, I'll just clarify that that ''fast'' means 'fast time-to-market', not 'high-velocity'. That triangle is a business notion for engineers and managers.

# 41
>>12033
>>12046
Sumomo scale is an interesting challenge. Both >>12061 and >>12064 are correct depending on functionality. A fully functioning Sumomo is impossible. A minimally functioning robowaifu that resembles Sumomo is completely possible. Once a 1 m robowaifu is made, a 1.5 will come next but, a handheld waifu would be a fun future challenge. 

Currently the 1 m fox girl has a new chest and waist. They're designed so that a 10 mm cube will function as modular connectors. They are far from perfect but, pleasant in the hand. I've decided to shoot for good enough until an initial full body prototype is finished. I've wasted too much time and plastic trying for perfect. Good enough is enough for a prototype.

# 42
>>12095
It looks like you're already on your way with re-scaled parts.

>I've decided to shoot for good enough until an initial full body prototype is finished
>Good enough is enough for a prototype.
That's the spirit that will lead you to success in the end Anon. Keep it up!

# 43
>>12095
Will those parts be mounted onto her wheeled base?

Hopefully she wil still balance while moving about on her original wheels. But if you run into problems, I imagine at that scale a standard R/C car could be used as a mobile platform.

# 44
>>12102
Thanks for your encouragement 
>>12108
She's being built with with legs that act as suspension, her waist is her base. I forgot her support tail so, for now she just topples over.

Atleast the triangle support spars work.

# 45
>>12165
Excellent work Anon. Might I suggest you add two additional bamboo spars to your design? I recommend that you add two new ones + 5 connectors into the same spaceframe you've already built.

One of these would cross fore-to-aft and affixed to the very center of the the two triangle 'bases' (that is, it starts from the top-front, and travels downwards and to the rear). And conversely, another one does just the opposite (that is, it starts from the top-rear, and travels downwards and to the fore), and affix it to the center of the two triangle 'points'. They will now form an 'X' shape where they cross in the center. Affix them each securely to these 4 new positions, ''and also to __each other__'' at their common intersection point in the very middle. To recap, that's five fixation points, for the two additional spars.

I believe if you'll make this modification with these new, additional triangles in the spaceframe, you'll discover it will be well-rigidized, strengthened, and enhanced against torsional and bending stresses with very little mass addition. The tendency of fore & aft shear, in particular, will be significantly reduced.

Look forward to seeing all the progress with your foxgrill robowaifu Anon!

# 46
>>12165
Great, but try using Imagepipe or something else to make your pics smaller.

# 47
>>12169
I'm definitely going to use that cross spar idea for the full size waifu. There will be 4 sets of spars and two sets of cross spars for the full scale waifu. I've remade her bust and butt to be easier and faster to print while being stronger. Good enough to scale up now. I'm moving forward to the full scale now and will make videos. I'm not good at writing so, I hope that will help spread the knowledge efficiently.  I was thinking of posting to bitchute and YouTube.
>>12046
I'll try to post some files to catbox soon, can't really say when exactly.
>>12239
Is this size better?

# 48
>>12242
This looks wonderful Anon. I think you're going on the correct pathway to success in a number of ways at once. Primarily low mass, but also inexpensive construction techniques, and simplicity of construction. All these (and more) will turn out to be vital for widespread robowaifu kits in the end.

Videos are a good idea **thanks for paying attention to image size now, btw** in my opinion. Be aware you'll probably eventually cancelled by Google for it though. Also, I'd suggest you don't use accounts either there or elsewhere that can easily be associated with your real identity by ~~stronk, independynt~~ ''amateur'' """investigators""". BTW, I think your writing is just fine Anon. Just apply yourself further.

Look forward to your robowaifu getting her tail and motors soon! Good luck.

# 49
>>12242
This is shaping up to be a very original robowaifu, anon. The lightweight construction should make it easy to have her zipping about at high speed! 

With the wheels for feet she reminds me a bit of Motorball Alita.

# 50
>>12298
>With the wheels for feet she reminds me a bit of Motorball Alita.
Neat thinking. Now, will Motorball have a division for cute foxgrill meido waifus I wonder?

# 51
>>12243
Through the use of a .8 mm nozzle, I was actually able to print 1.5 m scale chest and waist parts at the same mass as 1 m scaled parts. Thicker walls enable huge gains in strength to weight ratios in prints. Unfortunately, the support structure of cross spars didn't work because my bamboo is too springy. Would have worked if the spars were supported in the middle per this anons suggestion >>12169.  Laying on it showed it to be surprisingly strong and resilient given the sub 300 gram mass for the entire structure.


>>12298
>>12308
>Foxgrill meido Motorball
Kek, once we make DIY instructions and kits, it would be great to have anons run their own robowaifu Motorball competitions.

# 52
>>12428
So, mind spelling out what's going on here lad? Is this an 'after' shot of a 'test-to-failure' strength test or what? How did it do BTW? Do you have a 'before' shot? Kind of hard to tell the exact design before the test. Looks like you have entirely new system with entirely new parts?

Regardless, sounds like you are making steady progress, and that generally it's good news overall. Hope so lad, keep at it!

# 53
>>12444
>>12444
Unfortunately there is no before shot. The inserts that held the bamboo couldn't take take the pressure when tested. I've redesigned it to be simpler with less spars that are more strategically placed for a balance of strength and weight.
I redesigned her chest and waist slightly to be easier to print faster. I want to fail faster to reach the goal faster. Unfortunately, it still takes a whole day to print a 1.5 m scale chest and waist. Now it's onward to designing suspension legs that work.

# 54
>>12463
Thanks for the status update. Good luck with the legs. We've talked before about those swing-arm lamps as a possible basic frame design for the legs, maybe you can have a look at those if you haven't yet? (>>961, ...)

# 55
>>12027
>Screw it, I'm building a 1 m fox girl.

# 56
>>12464
Another step closer. With a head, she would be close to 1.5 m. My bamboo isn't long enough for properly scaled legs. Unfortunate, she's super floppy and hard to balance. She needs rigidity at this scale that 3 mm thick bamboo just won't provide unless many are used, which nullifies their weight advantage while increasing construction complexity.  Any low cost alternative ideas?

# 57
>>12485
Excellent progress Anon.
>Any low cost alternative ideas?
Use triangles. For example run two cross-braces on the thighs each (one on the front, one ''the other angle'' on the back). Repeat for the tail's joints, and the lower leg's joints. So for the front thighs, you'd run one diagonally from the inner crotch, down the thigh, then attached to the outer knee. Do the exact opposite angle (outer butt to inner knee) on the backside. Mirror on the opposite side (the other way round). Do the same thing for the other 4 remaining 'limb' parts.

That should help with individual limb parts rigidity. You now can think about ''stability'' (not the same issue). For that, you can think about angling the two legs outward slightly to form more of a 'bow-legged' tripod form in space. Slightly awkward ATM, but in the future as you begin to turn her into a real robowaifu, she'll have active balancing mechanisms available -- same as we humans do.

Those stabilizing gyroscope cubes we've talked about here for instance, might be a feasible way to improve her balance and stability. (>>5645, >>9057)

Lastly, as you move forward with her design, attempt to locate as many high-mass items (batteries & motors for example) ''inside'' her pelvic volume. '''Not''' in the higher, upper volume of the chest/head. I believe you'll quickly discover this engineering approach will assist you in many ways with your designs, not the least of which will be the balancing your robowaifu.

# 58
>>12485
BTW, any chance you can place some 'common' item within the shots of your robowaifu to assist us in judging her scale Anon. A box of cereal, or a gallon milk jug for instance, might be helpful to improving our ability to perceive her size. Or whatever else you have handy that you think would look better than either of these two choices.

Regardless, you're making solid progress for your stated goals ITT. Good luck with her!

# 59
>>12486
The double cross does help but, even with added stabilizers, it's just not enough. It's a big let down given how well bamboo skewers work on very small scales. I actually do plan to use leg geometry to help with balance and stability down the line. Because she's designed to roll around, I'm going to try to localize as much mass as possible into her legs to keep her naturally stable. Active stability is a waste of watts if the problem can be solved by design. I'm obsessed with efficiency and reducing mass and energy consumption. Of course she'll need active stabilization but, the less it's needed, the better.
>>12487
Cheerios for scale, thanks for the luck!

# 60
>>12495
As the old saying goes, 'Success is 99% percent perspiration, and 1% genius'. Please don't let a minor design setback discourage you. You're on the right track, I'd say Anon.

# 61
>>12485
>Any low cost alternative ideas?
Would some thin ropes, additional to the bamboo, help? Tensigrity? The other thing which was discussed here before were using a bundle of drinking staws. In that case you could also consider flexible plastic or silicone tubes for water. Then there's also the approach Poppy Project uses, a mesh on the outside, which could be flexible to pressure if you want soft thighs.
In general, I was assuming you would add something in between the bamboo anyways, so think about using that to create tensigrity and as a constraint for the bamboo moving around. In that regard, what about trying to use rubber bands between the bamboo, to constrain the movements?
Or it's generally the wrong approach: Even thin metal tubes for broom sticks or thinner ones from a hardware store, or plastic water tubes, the aren't really very heavy.

# 62
>>12495
With all due respect Anon, and again, I applaud your efforts; but quite frankly, you aren't following my advice just yet. I mentioned using '''triangles'''. So far, you aren't really doing so. 

Compare:
> #1 #2
with
> #3 #4

There's a difference. Triangles always have 3 edges, and their common vertices are always __localized__ together into common points. Triangles have a unique geometric characteristic that allows them to form effective space-frames. Try using using as many strictly-defined triangles as possible, and I'm sure you'll see a marked improvement in your waifu's frame rigidity.

'''OTOH''', you __did__ produce one example that was composed of 4 interlocking triangles (>>11613). I bet ''that'' one wasn't floppy or wobbly, right?

Good luck Anon. You have some great ideas, and especially 
>''"I'm obsessed with efficiency and reducing mass and energy consumption. Of course she'll need active stabilization but, the less it's needed, the better."''
is right on track. Keep going Anon, you can do it! :^)

# 63
>>12517
Ah, right. Like the Poppy Project I mentioned, but of course he could do it further inside instead around the whole outside of the leg.

# 64
>>12517
>and their common vertices are always localized together into ''three'' ('''3''') common points. *
I felt I should probably clarify that, since it might not be perfectly clear. So, 3 edges, three vertices (two end-points each) forming 3 points in space. Note that you ''can'' obtain a couple of triangles for 'free' with two cross-spars, but only if you rigidly fix their common intersection into a fixed point. Otherwise, you only have two cross-spars and no triangles.

# 65
>>12517
The cross spar arrangement makes double triangles under tension. Having two at 90 degrees with overlap actually produces greater rigidity then pure triangles. The bamboo is strong enough in this configuration for 1 m scale. At 1.5 m scale, the bamboos just becomes too flimsy. Pure triangles are good at lower scales like .7 m or below,  which the first chest and waist were. I'm moving towards cedar dowels at 6.25 mm diameter for greater rigidity. Triangles should be ideal for those rods and the next 1.5 m scale prototype will use a space frame with tensegrity principles per >>12513 's suggestion. 
>>12506
Thanks for the encouragement Chobitsu, I'm probably going to fail a lot more but, that Tesla bot really lit a fire. We need to beat Tesla to market.

# 66
>>12519
I actually did rigidly the intersections but, the braces break and pop off when put under any strain. PLA couldn't handle it and string just moves around. It feels incredibly sturdy until they pop

# 67
>>12518
Yep. The Poppy-Project team (wisely) adopted a variation of the so-called 'box girder' trussed space frame for Poppy's armature. It's a good & lightweight design that we Anon's would be smart to ~~steal~~ ''mimic''...

# 68
>>12521
Then strengthen the joint, obviously. This is how engineering goes Anon, but 'keep throwing stuff against the wall'. Eventually something will stick.

# 69
>>12520
You're quite welcome. You have our heartfelt encouragement for your project Anon. Godspeed OSRM, may ''she'' give all of us good insight and wise design councils. I added a Tensegrity waifusearch to the Library on your thread's behalf OP. >>12524

>===
-''minor prose edit''

# 70
>>12522
>Poppy
Looks interesting, thanks for the heads-up 
>>12525
Neat, thanks

Any thoughts on the Tesla Bot design? I'm considering a cloth outer covering like Tesla is using. Feels like a waste of mass and cost but, the aesthetic value may be worthwhile

# 71
>>12529
6.3 mm (1/4 inch) birch dowels have phenomenal strength and rigidity for their mass. With these, I am very confident in the future of this project! KitsuMeido unit 1 as soon as I can build her. Also, really need help with the face

# 72
>>12547
Sweet looks good Anon, sounds like you found a good stock material for your goals! 
>Also, really need help with the face
Can you spell out in more details what you mean please?

# 73
>>12548
I have the basic design down and somewhat tested, ready to go for the actual design. The major problem is, she doesn't have a head. I'm not sure how to give her a face that will work. I  originally used a print out of Ilulu but, it feels weird.

# 74
>>12549
I see. SophieDev just used an exported game asset mesh for his beloved ''Elfdroid Sophie'' robowaifu Anon. He's freely posted the STL files, etc. for Sophie, why not just start there? She's very cute and at the very least it's a good place to start I'd say.
>''"I am currently printing a bunch of smaller bits and pieces for the new head - ears, new bolting plates, electronics mounts. Once that's all assembled I think it will be time for me to upload her parts onto some 3D printing websites and try to spread the robo-love ;D"'' (>>9863)

SophieDev are you around? What do you yourself think of Anon using Elfdroid Sophie's face?

# 75
>>12554
Using Sophie's face is certainly one option. Ofc if you can learn to use Noesis and Ninjaripper then you can export a much wider variety of heads from either Honey Select or Honey Select 2. 

One thing that is especially good nowadays is that those games come in ready-to-install packages (check out 'ScrewThisNoise' repacks). Originally I spent hours setting up Japanese Honey Select, downloading fixes, expansions, mods, user tools, translations etc. But now it's all-in-one!

If you don't want to go the game asset-rip to 3D-printing route, I suggest purchasing a Dollfie head (or a head from one of the many Volks line of dolls) or maybe the head from another fashion doll line such as Smartdoll? Although many of these will be 1/3 scale at most. That's a big problem with most non 3D-printed doll heads. Many of them are just too small to be useful.

# 76
>>12566
>rip a game asset for her face
That's not a bad idea.
I've been doing some doodlengineering and looking through other threads. I think giving her a gravity compensation spring for her legs and a passive mass dampener for her torso could help with efficient stability. Also, I came up with an artificial muscle idea, a dual ended differential windlass that uses pulleys for tendons, the pulleys would push and pull, just like agonist and protagonist muscles. This give great gear ratios without the weight or cost of gears.

# 77
>>12521
TPU? Nylon might also work with such low hights and no enclosure.

# 78
>>12589
Belts can certainly work if the right size tensioner is used (see James Bruton's "Open Dog" project and many of his others). The main worry I have with any kind of pulley system is keeping it from collapsing or slipping. Since a pulley usually relies on some kind of rope or belt and the mass of the pulled object + gravity for tension. 

Initially I tried using a belt system in my robot arms, but it kept slipping just with the weight of the forearm and hand attached. Which is why I eventually opted for pair of fairly large helical gears at the elbows, instead. 

Still, I wish you eventual success with your chosen mechanism. Your efforts to push the boundaries of practical robowaifu development are admirable!

# 79
>>12614
>belts
Nah mate, it's two coaxial differential windlasses. It functions by letting out string equal to the difference in drum circumference on one end while taking in the same length from the other end. This allows for cheap high ratio linear actuators. They're also very efficient and light weight. This demo actuator though not very useful, has a sub 10 gram total mass. 
I've been considering between motors right now I'm currently on 130m motors.. Normal brushed are cheap as dirt. Can get large quantities for 30 to 60 cents each easily, their design lends them to easy integration into designs (lowers manufacturing complexity, time, and  reduces faulty parts). The main problem is the abysmal 40 percent efficiency.

# 80
>>12654
This is a good idea. I'd suggest you add a small & simple gearbox between the motor and the spindle to increase torque. My windlass designs are involving 'silk' ribbons (usually a synthetic instead) as they are particularly good for this. Good luck anon.

# 81
>>12656
Please do share your design. I'm still actively developing the windlass design to optimize mass cost and manufactuability

# 82
>>12549

Get a Vroid Studio model, import it into Blender, and just get the head?  If you want the most anime head without the trouble of modeling from scratch.

# 83
>>13007
Sounds like a good idea. We also have a thread for faces >>9 and looking in Youtube gets you videos for how to model an anime head in Blender: https://youtu.be/fQZ7TEdFdMU also you could probably use Sofies head. In all cases printing might be difficult.

# 84
>>13007
I've tried but, the internal geometry of vroid  studio model heads means they'd take a day to print and would be heavy. 
>>13020
That's a great video tutorial. Hopefully I can figure out a good head that's printable.

I've been working on her drive. I simplified things down to two drive motors because servo based steering didn't work well. Unfortunately, her legs drove off her body so, work still needs to be done there.

# 85
>>13020
I'm surprised by that video Anon. His approach is very methodical, but it's not bad as a beginning and he got to it in a short timeframe. Also, focusing on low-poly at the front of a project as he is doing I consider to be vitally important for success. Thanks!

# 86
After many failures trying to get her to balance,  I'm going to try wider bigger wheels.

# 87
>>13569

Have you tried a wider pyramid shape?



.

# 88
>>13570
Thanks for the suggestion. I'll try increasing her grounded surface area.

# 89
>>13582



>Also, since you're having problems too, want to team up on OSRM? I already have a decent chest and pelvis. I've been stuck for months since and you seem to have good ideas.



1: where are you stuck?



2: is this like pic related?



I guess we could start with a clear mission statement. What functions does it need to perform, what are the aesthetic and design limitations or standards?

# 90
>>13608
The biggest problem is the lack of a clear mission statement. I started out just wanting Iruru then wanting Senko San and modeling her chest and pelvis. I'm stuck on making the rest. Working on a mission statement together would help. I want her to be able to talk to me, follow me around, and snu snu. Her ideal design is basically Senko San

# 91
MeidoDev I want to help you, this will help me to focus on doing something rather than scattering my attention all over the place. Looks like a fun and reasonably feasible project. I'm assuming we're ok with wheels, and you want her/it to look like Senko San. 

Must

- talk, and I assume process what is said to it as well, understand basic commands, doesn't need to be intelligent, but "just work"

- follows you, so it needs to have a way to distinguish you from say, another person, dog or roombah. Cheap method: gps tracker fob you carry. More difficult: Facial / sillhouette recognition

- Ambulatory but wheels or treads are acceptable, seems simple, you mentioned balance was an issue, how about angled wheels and gyroscopic stabilization?

- Snu Snu: well enough said, if you're going to get intimate with this Meidobot then it depends what level of interaction you want and how tall does she need to be? I mean I'm assuming you want more than a fleshlight on wheels.

I'm downloading Fusion 360 and I'm going to teach myself how to use it. Initially though I can provide pencil/paper sketches, I have large sheets of graph paper for this so it will be a notch above just scribbles on notebook paper hopefully. I'll update you with progress ITT.

# 92
>>13691
Thanks and welcome to the project Meta Ronin. Senko is the pretty much the goal. 
>talk
I also want her to say "kon" at the end of sentences to emphasize her kitsune more
>following 
GPS is a great idea
>movement 
Angling her wheels for camber is a good idea.  Any examples of it helping with balancing? I know it helps cars stay stable. 
>snu snu 
Hm, it would be nice if she said things like "daisuke" and other cute and loving things during and moved around a little. Senko Sans official height is 125cm with 10cm ears so, that should be fine. I suppose she'd be a skater in the moe fox danger zone to go by the classifications I saw in a thread a bit ago. 
Notebook sketches will be appreciated. Wishing you luck with Fusion 360, I use Blender and Meshmixer. Sk8o and Ascento look like good designs we could learn from.

# 93
>>13692

well given that its a prototype I don't think anyone's gonna be breaking doors down for making a 4' tall robot on wheels lol

>I also want her to say "kon" at the end of sentences to emphasize her kitsune more

probably the easiest thing to do out of any of it. Good examples there, I like the idea of separating the wheels so they can climb. I think bigger is better for stability and traction. I'm picturing something like chunky Megaman/Roll feet but with a wheel "inside" partially but I'm going to play with that concept a bit and see if I can innovate something "outside of the box". I'll post some sketches.

# 94
>>13693
I'm also hoping her being like a fox will help her be more acceptable in conventions and faires
I agree that bigger is better. Chunky roll fox would be perfect. I bought her a tail. Wanted a normal one but, they had really faded color so got a silver one.

# 95
>>13071
>internal geometry of vroid  studio model heads means they'd take a day to print and would be heavy.
Please elaborate on that. Maybe in the thread for 3D design software or in the one for faces. Or upload some example. Thanks.

# 96
>>13718
I guess it's just optimized for creating avatars.

# 97
>>13715
Posted about it in the 3D modeling/printing thread.
>>13721
>>13719
This is correct. The models were made specifically for animation and not for printing.

# 98
>>13722
> the 3D modeling/printing thread.
What? I only realized that now. How is it the thread for a specific build or development but also the general thread for two other topics?

# 99
>>13743
I have no Idea. Chobitsu just decided it was that way.

# 100
>>13744
I'm going to crosslink every general comment in the other theads related to these topics.

# 101
>>13743
The 3D printing thread should naturally include modeling for printing. All of those general posts belong in.
>>94

# 102
>>13693
Found cute inspirations

# 103
>>13895
Simplified faves may be the way to go

# 104
>>13896
Those big dopey eyes are cute.

# 105
>>13895

Thanks!

Sorry for my recent absence. I'd like to continue work on this on the robowaifu.club until it can be determined what happened to the BO/Chobitsu or if this place is dead in the water.

# 106
>>14081
I'll make a new thread over there and all updates will be made over there until moderation returns.

# 107
>>14082
Posted the new thread

# 108
This is exactly what I want. A beautiful dedicated maid filled with love and affection

# 109
>>14093
Hope you are doing well MeidoDev. It would be nice to see what you're up lately. BTW, that waifu is wonderful. I hope you make her someday! :^)

