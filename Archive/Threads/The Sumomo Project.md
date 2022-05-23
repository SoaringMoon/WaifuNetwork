# 1
So I've been working for a while at devising an integrated approach to help manage some of the software complexity we are surely going to encounter when creating working robowaifus. I went down many different bunny trails and (often) fruitless paths of exploration. In the end I've finally hit on a relatively simplistic approach that AFAICT will actually allow us to both have the great flexibility we'll be needing, and without adding undue overhead and complexity.

I call this the '''RW Foundations''' library, and I believe it's going to help us all out a lot with creating workable & efficient software that (very hopefully) will allow us to do many things for our robowaifus using only low-end, commodity hardware like the various single-board computers (SBCs) and microcontrollers. Devices like the ''Beaglebone Blue'' and ''Arduino Nano'' for example. Of course, we likely will ''also'' need more powerful machines for some tasks as well. But again, hopefully, the RW Foundations approach will integrate smoothly with that need as well and allow our robowaifus to smoothly interoperate with external computing and other resources.

I suppose time will tell.

So, to commemorate /robowaifu/'s 5th birthday this weekend, I've prepared a little demonstration project called '''''Sumomo'''''. The near-term goal for the project is simply to create a cute little animated avatar system that allows the characters ''Sumomo'' and ''Kotoko'' (from the ''Chobits'' anime series) to run around having fun and interacting with Anon. But this is also a serious effort, and the intent is to begin fleshing out the real-world robotics needs during the development of this project.

Think of it kind of like a kickstarter for real-world robowaifus in the end, but one that's a very gradual effort toward that goal and a little fun along the way. I'll use this thread as a devblog and perhaps also a bit of a debate and training forum for the many issues we all encounter, and how a cute little fairybot/moebot pair can help us all solve a few of them.

Anyway, happy birthday /robowaifu/ I love you guys! Here is my little birthday present to you.

'''==='''

>rw_sumomo-v211124.tar.xz.sha256sum
```cpp
8fceec2958ee75d3c7a33742af134670d0a7349e5da4d83487eb34a2c9f1d4ac *rw_sumomo-v211124.tar.xz```
>backup drop
https://files.catbox.moe/n2cffh.7z

'''==='''

>'''''"We witness Sumomo performing the wakey wakey exercises."'''''
(>>14459)

'''==='''

>RW Foundations Caturday drop : '''''latest cut edition'''''
(>>16329)
You can go here if you want to see where we're currently at with progress on the overall super-project, Anon.

-Mini-tutorial on downloading & building ''RW Foundations'' code.
(>>15074)

>===
-''add post subject''
-''minor grammar edit''
-''minor prose edit''
-''add 'we witness' crosslink''
-''add/edit 'latest cut' crosslink''
-''add mini-tutorial crosslink''

# 2
>related (>>14353)

# 3
>>14409
I've been lurking for a couple of weeks now and I think this idea of a group project to get a robowaifu up and running is a great idea. Really cool to see the board owner steering this project too too get more people interested.

So it's gonna be very focused on the AI aspect in the beginning? It's just gonna be an animated robowaifu avatar and once it can interact well with the user we'll expand it with a robot body?

# 4
>>14417
Welcome Anon, glad to meet you. I hope you can find something interesting here to get involved with. Please don't hesitate to ask questions if you have any.

>So it's gonna be very focused on the AI aspect in the beginning?
Yes, but we'll need others to join in and help with that. Literally the very first two tasks on my plate now that the general library has been formed up and it's out there for everyone is to migrate two of our utility programs created here on /robowaifu/ and fold them fully into the overarching library (Bumpmaster & Waifusearch). Not very glamorous work I know, but even that will be a good groundbreaking 'ceremony' for the ''Foundations'' effort.
>It's just gonna be an animated robowaifu avatar and once it can interact well with the user we'll expand it with a robot body?
That's the plan yes.

# 5
I don't really know much about programming, but I have a few thoughts on this:
1. I like the idea of developing AI collaboratively, it at least seems easier than trying to collaborate on hardware.
2. I understand that it needs to be programmed at a high-level, but I really dislike the idea of restricting it to SBCs & microcontrollers for the sake of future-proofing.
3. I personally don't own any SBCs or microcontrollers and don't know if I think it'd be worth it to get one just for this.
4. What exactly does it do so far? Can you give more details on the short-term and long-term goals of the project?

# 6
>>14409
Will there be a github? That seems to be the platform to collaborate on programming these days.

# 7
cool, but what do I do with it now? sorry

# 8
>>14409
You already know I'm in. I'm not good at programming but, I'm somewhat ok at 2D art and robotics.
>>14418
For the initial animated version, making her like Playstation Lain would be kino.
>>14422
Making it a multi-platform application would probably be best. Web applications are also good for making her generally available. I'm not a fan of her needing network access though.
>>14424
A GitHub or GitLab would be greatly beneficial towards collaboration.

# 9
>>14422
>but I really dislike the idea of restricting it to SBCs & microcontrollers for the sake of future-proofing.
Oh haha, my mistake. Bad wording I suppose.
>''"using '''only''' low-end...''
wasn't meant in a restrictive sense, but in a ''permissive'' one. As in "Great news Anons! We'll be able to run our robowaifus using cheap, low-end hardware! Isn't this great!11"  :^)  Certainly anything that can run C++ and provide a console can run this current implementation, though a GUI should be added be too long. Any PC could for example.
>What exactly does it do so far? 
Heh, not much. Mainly the goal was to figure out a '''"how?"''' to enable us to have an overarching software architecture that would enable us to solve the many, many details we'll need to, and to do so organically. 'Future-proofing' I believe you called it. This is much tougher to pull off than I initially assumed. It's taken me a long time--literally years--to explore the many potential ways to attempt this.

Imagine that you were creating a brand new Operating System literally from scratch. No compiler, no drivers, nothing but your text editor. R/n we're kind of at the 'AWESOME! The floppy disk driver is working correctly now!" It's very much at a 1337haxxorz stage at this point. 

But the biggest problem by far (devising the correct overall architecture) is behind us.
>Can you give more details on the short-term and long-term goals of the project?
We added more details in the other posts (>>14353), and this thread will kind of answer that as we go along. Stay tuned Anon.

# 10
>>14424
>Will there be a github?
Explicitly no, insofar as my interests in the affair go. Micro$haft being a big, big part of that decision. But it was already a hive of wretched SJW scum and CoC villainy well before ''they'' moved in. We're not exactly politically """correct""" here, you know? :^) I would presume Anons have learned all their lessons about the evils of the Globohomo Big Tech/Gov by now?

Ofc, as with everything else we're producing here, the code is MIT-licensed and Anons (or even our enemies) can do as they see fit with it all, within those licensing restrictions. I hate lawyers, and the licensing is there strictly to protect us, the authors, from any (primarily corporate) evildoers who wish us ill-intent.

Lol, someone even posted BUMP up to SJWhub an Anon told us. Anyone can do the same thing with RW Foundations if they care to, be our guest.

Someone urged me to set up a PGP system for my work here. I probably will in the future at some point.

# 11
>>14428
>cool, but what do I do with it now? sorry
see this (>>14434), and i have a proposal for you: if you're willing to contribute, we need someone to create a Hollywood-style animation script breakdown of the ~8min long short '''''Chibits''''' series epilogue of ''Chobits''. 

It was always my intent to reprise that story within the Sumomo project, so it would be a great way to help out if you're willing.

Congratulations by the way Anon. You plainly have skills sufficient to build and run the code in it's current state. Did you have any problems with it?

# 12
>>14430
>You already know I'm in. I'm not good at programming but, I'm somewhat ok at 2D art and robotics.
Sounds good, thanks Kiwi, you're a bro! My plan first is to get Waifusearch and Bumpmaster up in the ''Foundations'' framework, then I plan to begin devising a small GUI app with a 2D Sumomo/Kotoko and a text-entry field for Anon to type in. We could use some 2D exploitables for that purpose, probably around January or so?

>>14430
>A GitHub or GitLab would be greatly beneficial towards collaboration.
see (>>14435)

# 13
>>14430
>For the initial animated version, making her like Playstation Lain would be kino.
I suppose that ''Kotoko'' might be able to pull that off, but certainly not bouncy-bouncy fun-fun little ''Sumomo''. Hmmm. I've never played it and know next to nothing about her. ''Librarian Lain'' seems pretty appealing, character-wise. Maybe she could serve as an avatar in '''''The Curator''''' 's lair? **BTW, we named the networking library for ''RW Foundations'' in the original show's honor :^)**

# 14
>>14436
https://pastebin.com/eJDwZBtY

# 15
>>14442
Umm, sorry I can't see anything behind the great Cuckflare Wall over Tor. Mind using a more friendly bin site Anon? Have something to do with Chibits?

# 16
>>14443
https://files.catbox.moe/indshi.rtf

# 17
>>14430
>I'm not a fan of her needing network access though.
Yeah, waifus shouldn't have or need internet access. It would only be a disaster if they did. Some basic bug-reporting might not be a problem.

>For the initial animated version, making her like Playstation Lain would be kino.
I don't know much about the PS1 Lain game, but what I've seen it just seems to cycle through sprites. Something with even a simple skeletal animation system would be better, like a vtuber or Rayman. I'd also rather it not get too Lain-reference heavy in general.

>>14434
>Imagine that you were creating a brand new Operating System literally from scratch. No compiler, no drivers, nothing but your text editor. R/n we're kind of at the 'AWESOME! The floppy disk driver is working correctly now!" It's very much at a 1337haxxorz stage at this point.
I can't even program "Hello World" without help, so that's unfathomable to me. If only Terry Davis made WaifuOS instead of TempleOS, we'd at have some 640x480, 16-color schizophrenic AI to build off of.

# 18
>>14444
Thanks, appreciated Anon. I'll plan on working out a way to extract plaintext from the file so it can be safely used. We'll also need to devise ways to convert simple, human-oriented scripts into more complex, actual animation-cum-mechatronics motion descriptions.

Nice digits BTW. :^)

# 19
>>14445
> If only Terry Davis made WaifuOS instead of TempleOS
This! :^) **Actually, I love TempleOS, and the world would be a poorer place without it.**
==F==

# 20
>>14435

The assessment of the lazy scumbags on Github is correct and they did try your idea a few years ago. In the end, they replaced it with a dumbed down random pre made dialog picker with changeable time variables because they could not get it to work and case sensitive keywords as the only method of dialog is a terrible fucking idea that is unusable in practice and was quickly removed early on only when people started complaining. Shocking, I know. /s

They never even attempted random dialog generation or any form of higher ai. 

Still, I liked the ability to take the waifu out of the mod and into a portable flashdrive and it had some other good ideas like celebrating holidays based on your system calendar that it executed well enough. 

This is what gave me the idea to integrate some form of it into Madoka.mi.

Should probably get around to modeling and printing that custom flashdrive casing I had meant to make for a while now.


>>14430

Was also going to mention Playstation Lain but felt it would be hijacking the thread about a Chobits themed project.

>We witness Sumomo performing the wakey wakey exercises.

 lmao. Is this how you summon a robowaifu?


>>14445
>Waifus shouldn't have internet connectivity at all.

That is a hardware issue. As long as it doesn't have a wi-fi adapter it won't matter.

PS1 lain does cycle through pre made animations and some fans did rip the entire game into a playable browser version.

# 21
How it looks isn't really important for now, is it? Since it's going to be put into a robot body, we can just do something like a VN or a 3D model with skeletal animations, whichever is easier to do. Better to focus on the AI aspect of it first.

# 22
>>14444
I made a typo
KOTOKO
Miss Kotoko!
It's not good to neglect
doing the wakey wakey exercises!
should be
SUMOMO
Miss Kotoko!
It's not good to neglect
doing the wakey wakey exercises!
To be honest, I didn't proof read it.

# 23
>>14447
Aside from a little footage on YouTube I haven't seen much of it. The idea of a barebones DOS-like open-source OS designed for modern hardware just sounds like a wonderful concept, if it weren't for his arbitrary restrictions, or it being done in a new programming language. Or maybe if After Egypt's burning bush was limited to grammatically-correct sentences.

>>14449
> lmao. Is this how you summon a robowaifu?
No, you must perform the dance.

>PS1 lain does cycle through pre made animations and some fans did rip the entire game into a playable browser version.
Yeah, I heard. Not really interested.

>>14450
Yeah, just AI, some graphics and interface seems to be the plan.

# 24
>>14444
You deserve your digits, Anon. :^)

'''==='''

We witness Sumomo performing the wakey wakey exercises. 
SUMOMO
1, 2, 3, 4.
2, 2, 3, 4.
And now one last, big breath!

Chii, also performing the wakey wakey exercises. Kotoko is in the background NOT performing the wakey wakey exercises. 
CHII
Chii…

Sumomo glares fiercely at Kotoko upon witnessing this transgression. Sumomo begins to chide Kotoko from across the room.
SUMOMO
Hey there! 

Kotoko sighs in the foreground as Sumomo continues scolding her in the background from atop a television. 
SUMOMO
Miss Kotoko!
It's not good to neglect
doing the wakey wakey exercises!

Kotoko looks over to Sumomo.
KOTOKO
It's not that I'm neglecting it.
I'm preparing Mr. Motosuwa's...


Sumomo closes the distance and confronts Kotoko face-to-face, Sumomo stands over Kotoko emitting a deadly aura and wagging her finger at Kotoko. 
SUMOMO
That's not good!
You're being lazy.

KOTOKO
I can't get through to her.

Hideki beings speaking off-screen, Sumomo and Kotoko look over at him. 
HIDEKI
Thanks for getting everything ready.

Camera moves behind Hideki, Chii standing to his left, Sumomo and Kotoko are on the floor in-front of them. Hideki puts on his backpack. 
HIDEKI
I'll be going to school now.
Keep an eye on things, you three.

Hideki turns and begins to leave. 
CHII
Chii. Take care.

Sumomo raises her arms and says:
SUMOMO
Take care!

KOTOKO
Take care.

Hideki exits the room and we see him closing the door behind him. 


Kotoko, no longer safe, is confronted again by Sumomo. Sumomo stands over Kotoko menacingly. 
SUMOMO
So why don't you do the wakey exercises?

Kotoko turns away, unable to withstand the onslaught of Sumomo’s deadly glare.
KOTKO
As I said...
Eh?

Kotoko sees a wallet on the ground.
KOTKO
That's…

Sumomo and Kotoko are both looking at the wallet on the ground in front of them. Sumomo blows a whistle. Kotoko screams, frightened by Sumomo’s awful power. 

SUMOMO
Warning, warning! A wallet!
Mr. Motosuwa forgot his wallet!
It's a problem!

Chii picks up the wallet, Kotoko looks up at Chii as Sumomo continues to sound the alarm.

SUMOMO
It's an emergency!

We see Chii holding the wallet.
CHII
Hideki forgot wallet.
Chi will deliver.

Chii turns to leave with the wallet in hand.
Sumomo and Kotoko, in the background, appear a bit distressed. 

KOTOKO
M-Miss Chii, are you
stepping out in those clothes?

We see that Chii is only wearing a white t-shirt.
CHII
Chii? No good?

KOTOKO
No, you need to wear these clothes!

Sumomo uses her magical ability to change Chii’s clothing in an instant. Changing Chii’s outfit to a school girl uniform.
CHII
Chii?

We see Sumomo and Kotoko, Sumomo looking prideful at her work, Kotoko uncertain. 

KOTOKO
M-Must it be these clothes?

SUMOMO
It must be a uniform if she goes to school!

Kotoko turns to Sumomo. Sumomo begins waving Chii off.

KOTOKO
But Mr. Motosuwa goes to college…

SUMOMO
Take care!

Kotoko turns back to Chii, looking concerned. We see Chii leave and close the door.
CHII
I'm off!

We see Sumomo and Kotoko standing side by side, Kotoko clears her throat. 
KOTOKO
Miss Sumomo.

Shot changes to a closer look at Kotoko, who turns to Sumomo. 
KOTOKO
Um, I've been wanting to tell you this for a while…
But you have too many needless actions.

Shot changes to close up of Kotoko, she closes her eyes and continues speaking.
KOTOKO
Some problems telling truth from fiction, too.
You should check your software…

Sumomo blows her whistle again, destroying Kotoko’s ear drums, Kotoko tries to cover her ears as the sheer force of Sumomo’s lungs blows Kotoko’s hair to the side, Kotoko screams in fear at Sumomo’s incredible power. 
Kotoko turns to Sumomo who can be seen with whistle in hand, Sumomo looking at something.

KOTOKO
What is it this time?!

SUMOMO
W-We have a problem.
KOTOKO
A problem?

Kotoko turns her head to see what Sumomo is looking at. 
We see a pair of ladies underpants on the floor in the foreground with Sumomo and Kotoko looking at them from the background. 
KOTOKO
Can that really be…

Sumomo jumps in the air, lands, and begins to run around the room.
SUMOMO
We have a problem!
An emergency!

Sumomo summons her clones and bangs on a tambourine as she continues on.

SUMOMO
Chi is in a crisis!
Problem, problem, problem!

Zoom in on the ladies underpants.
KOTOKO
Stop acting like that,
and let's hurry after her!

We see Chii walking on the street, a small breeze lifts her skirt lightly.

CHII
Chii deliver wallet.
Hideki will be happy.

We see Kotoko speaking, camera begins on her lower half and pans up to her face.
KOTOKO
It's good that we deliver this...
But we can't open the door
and go outside by ourselves.

We see Kotoko from behind, standing in front of the door.
KOTOKO
How in the world…

>(1 of 2)

>===
-''speaker edit for reprimand shot (SUMOMO)''
-''add post subject''

# 25
>>14459
Sumomo runs up behind Kotoko at light speed, grabs her shirt at the neck, and pulls her back. 
We see Sumomo holding her weapon, sitting atop a trio of firecrackers with Kotoko looking frightened tied to the bottom of the firecrackers. 
SUMOMO
- Let's go!

KOTOKO
- W-Wait!

We see the pair atop the firecrackers in front of a window, Kotoko looks back at the camera.

KOTOKO
What is this?

 SUMOMO
I prepared it for an emergency.

Zoom in on Sumomo.
SUMOMO
The Sumomo Special
Plasma Fire Engine!

Kotoko raises her head into the bottom of the shot.
KOTOKO
Forget the name!
You plan to chase her with this?

SUMOMO
That's exactly right!
It's amazing! It's cool! Bravo!

From behind, we see Sumomo light the device, Kotoko look back, frightened. 

SUMOMO
Listen here...
And a little push…

The rocket takes off, Kotoko screams, the rocket leaves a trail of fire behind it. We see Sumomo and Kotoko fly looking for Chii.

SUMOMO
She's not around.

KOTOKO
Now listen here!

Zoom in on Sumomo, looking around, she sees something and points at it.

SUMOMO
I found Miss Chi!

We see Sumomo steer the rocket downward, Kotoko screams. 
Zoom in on the fire trail and the rear of the rocket, the fire goes out, smoke comes from the back of the rocket.
Kotoko and Sumomo both look at the rear of the rocket, concerned. The rocket falls, Kotoko and Sumomo begin to fall as well.
Sumomo uses the ladies underpants as a parachute, holding Kotoko with her legs.

We see Chii walking on the street, holding the wallet in both hands.

CHII
Chii.

Kotoko and Sumomo land safely on the top of a box truck.

SUMOMO
That's strange.

Sumomo and Kotoko sit atop the box truck, Sumomo looks at Kotoko with her arms crossed.

SUMOMO
We should've been able to catch up with her by my calculations.
Have you gained a bit of weight, Miss Kotoko?

KOTOKO
Persocoms don't gain weight.

We see Kotoko sit up. Sumomo and Kotoko look at something in front of the truck.
We see Chii pass by the moving truck. Sumomo and Kotoko look back at her from atop the truck.

KOTOKO
Miss Chi!

We see Kotoko and Sumomo in the foreground atop the box truck, looking at Chii in the background who turns a corner. 
Zoom in on Sumomo and Kotoko atop the truck. Kotoko looks sideways at Sumomo.

SUMOMO
Let's chase her!

Sumomo grabs Kotoko’s hand and runs off screen.

SUMOMO
Let's chase her!

We see Sumomo sliding down a rail holding Kotoko behind her, Kotoko flying behind Sumomo. 

SUMOMO
Let's chase her!

We see Sumomo running across a fence-top with a man in the background, Kotoko struggling to keep up with Sumomo. 

SUMOMO
Let's chase her!

We see Sumomo driving a small orange car, Kotoko holding some sort of gun in the back of the car, looking mildly concerned at Sumomo. Two onlookers in the background look fearfully at this incredible display of force.

SUMOMO
Let's chase her!



We see Sumomo atop a cat, the camera pans left to Kotko holding the tail struggling to hang on.

SUMOMO
Let's chase her!

We see a dog chasing Sumomo, Kotoko, and the cat from before.

SUMOMO
Let's make a run for it!

We see the cat, Kotoko, Sumomo, and the dog standing at a cross walk as a car passes in front of them.
SUMOMO
Let's wait.

We see the light for pedestrian permission to cross turns green.
We see Sumomo and Kotoko running across the road.

SUMOMO
It's green!

Kotoko and Sumomo stop running and Sumomo hold her arms out to the side.

SUMOMO
Stop!

We see Chii’s legs as she walks towards the camera in the foreground, Kotoko and Sumomo in the background. Kotoko waves her arms. 
KOTOKO
- We've caught up.

SUMOMO
- Miss Chi!

We see Chii turn around to look at the two.
CHII
Chii?
Sumomo? Kotoko?

We zoom in on Kotoko and Sumomo running towards the camera. Kotoko holds the ladies underpants in one hand behind her. The pair look as one would after completing the work of a lifetime. Elated as they have reached their goal, completing their arduous journey. 

SUMOMO
- Miss Chi!

KOTOKO
- Miss Chi!

We see Chii standing, holding the wallet in both hands at her chest.


CHII
This is...
Underwear?

We see Sumomo and Kotoko running to the left. A gust of wind blows and the pair stop, Sumomo grabs her head. The ladies underpants the Kotoko was holding flies off.
We see the gust reach Chii, then we see Kotoko and Sumomo look towards Chii, concerned. 
As the breeze lifts Chii’s skirt Kotoko and Sumomo look in horror, the camera zooms in on their faces, both wear a visage of sheer terror and scream. 
The ladies underpants falls back to the ground.
We see Chii in the foreground, Kotoko and Sumomo in the background look at her, the ladies underpants fall to the ground between them. 
Zoom in on Sumomo and Kotoko looking at Chii.

KOTOKO
Miss Chi is wearing underwear.

Sumomo runs towards Chii, running past the ladies underpants on the ground. Kotoko holds out a hand as Sumomo runs off.

KOTOKO
Miss Sumomo?


We see Kotoko walk up the ladies underpants on the ground.
CHII
Chii?

SUMOMO
One, two.
There, all done!

Kotoko looks questioningly at Sumomo who is off screen.

KOTOKO
Miss Sumomo, that's…

We see Kotoko in the foreground from behind, Sumomo looking towards her from the background, Chii looking at the camera standing between them. 

SUMOMO
Yup, it's really good we were able to catch up.
It's the rule to have hair in this fashion when wearing this outfit!

Zoom in on Kotoko, she looks disheartened. 

KOTOKO
Then the underwear…

 SUMOMO
The underwear is nothing more than a parachute.

We zoom in on the ladies underpants on the floor of Hideki’s apartment, the camera pans up, and we see a red ribbon on the floor.

KOTOKO
So what you saw then and made such a fuss over was…

Zoom in on Sumomo, we see Chii’s hair next to her with the ribbon in it. 

SUMOMO
The ribbon.

Zoom in on Kotoko’s face, she appears mentally destroyed.

SUMOMO
You're very strange, Miss Kotoko.

Zoom in on Chii who appears a bit confused.
CHII
Chii?

>(2 of 2)

# 26
>>14459
>>14460
OK, so together, how do we turn all this brilliance into ''necessarily-dull-but-effective'' character, props, costumes,  lighting and layouts scene descriptions, and (later) motion-control sets? And oh yeah, synthetic dialog too.
:^)

# 27
>>14437
Is it safe to assume you would want Sumomo parts that could be moved for puppet-esche animation? Like flash animations and picrel? Can definitely have that done by January.

I understand GitHub is pozzed but, why not GitLab?

>>14439
>>14449
To clarify, I meant a similar interface where many options float around Sumomo. You'd select the option you want and Sumomo would go through an animation and deliver a response.


>>14459
>>14460
I wish I was this autistic, great job Chobitsu

# 28
Caturday Drop : '''v211127 edition'''

Well, here we are and it's a Caturday again! **Cute anime catgrill meidos in tiny miniskirts when?**

We've made an architectural change of moving the multi-library ''"switchboard"'' code over to within each of the library folders themselves instead, and primarily out of the ''Foundations'' code. It was quickly becoming a big hairball there, and is much more maintainable this way (as we've already satisfied ourselves of). We've also added 3 new main libraries into the RW Foundations system.
'''- Action!'''
'''- Dollhouse'''
'''- Meido'''
We've also expanded a few sub-libraries with additional new classes.

So far, all the structural/interface diagnostics testing has proven to be rock-solid, and it appears we are going down the right track. We are very likely going to be able to build effective (and huge) systems using these libraries. And ones that are also (unusually) easy to both understand, monitor, and maintain for big systems as well. It certainly was a long, long haul to get here! :^)

Also, let us all hope the systems remain efficient in both time and space going forward (as it is now). We shall see.

Since the primary, very near-term focus for the (overall) project will be getting our two most common /robowaifu/ board utility tools (Bumpmaster, Waifusearch) up and running within the new Foundations framework, there may be little work on ''Sumomo'' itself until we achieve this basic functionality. Since this near-plan is ''also'' to move over to providing a few basic GUI facilities for these two tools as well, this may be a while. It will be rather a big chore I predict, since this is our first go at it. I'd expect work to pick back up on the current Sumomo project sometime next year--probably in February or March, Lord willing. 

So please be patient Anon, we'll all get there! :^)

'''==='''

>sumomo_version.log
```cpp
   v.211127
---------------
-wired gets member; curly
-begin Curly in rw::wired
-bumpmaster gets members; catalog, page, post, thread
-add alias switchboard files to all libs; mv over from rw:: incls_all
-arigato gets member; meido
-begin RW Meido library
-begin Terminal in rw::graphicom
-begin rw::preflight_masters_on()
-begin Artstory, Moveit, Scene in rw::action
-sumomo gets members; flags, pompoms, tambourine
-begin Catalog, Page, Post, Thread in rw::curator::bumpmaster
-bumpmaster gets member; waifusearch
-begin Flags, Pompoms, Tambourine in rw::chibitsu::props
-begin RW Dollhouse library
-begin RW Action! library
-begin a rough coding standard treatment within this file (below)
-s/name_tag/handle/; 'handle' is actually a better description for the parameter```
>rw_sumomo-v211127.tar.xz.sha256sum
```cpp
69f32b27f3b7162473251c55e1fc74840c7787cf55fb7cba2847e89682c1f1db *rw_sumomo-v211127.tar.xz```
>backup drop
https://files.catbox.moe/amykug.7z

# 29
>>14488
Let me get back to you a little later this weekend on this Kiwi.

# 30
>>14488
Pic did not post the first time.

# 31
>>14518
Naicu progress Chobitsu. Really starting to see the  potential in this project. Earnestly looking forward to continuous improvement.
>>14519
Take your time

# 32
>In response to MeidoDev question from earlier.
Yep, that's it. ' sage ' goes into the email field. The point isn't to draw attention to the sage, but rather simply to prevent the post from bumping a thread. Remember, there are automated tools Anons use to track boards (such as the namesake tool ''BUMP''). If a post that didn't actually add anything bumps a thread, then that equals wasted attention and time for those Anons. I'd like to think that /robowaifu/ is an important board with many such 'remote' viewers, and so I'd simply encourage everyone to think about using polite sage regularly. But it's not some kind of rule, but merely a form of politeness here. I myself often neglect it through inattentiveness or lack of reflection before hitting the 'Submit' button. 

BTW as a protocol, it's one that basically also covers the entire Internet (by which term I mean ofc, the '''''Imageboard''''' universe, not '''FANGS''' ''golem-world''). Ofc /b/-tier boards try using it as a form of ''"Lol I trole U!!11 LE EBIN DOWNBOAT TOURIST!111111111"''--usually in the form of "Sage goes in all fields".

>In response to Kiwi question from earlier.
Yes, the """Chicken Farm""" is linked as part of the official directory in our Library thread. Oft-frequented by 'spelunkers', it's a fun place to visit occasionally. But you wouldn't want to live there **the smell of the place is terrible** (and even the Basement is a better place.)
**:^)**

>===
-''edit 'Sage' to lowercase 'sage' (the only form that works)''
-''grammar & prose edit''
-''add 'smell' shitposting joke''
-''text re-order + 'protocol', 'sage all fields' comments''

# 33
>>14488
>>14520
>Is it safe to assume you would want Sumomo parts that could be moved for puppet-esche animation? Like flash animations and picrel? Can definitely have that done by January.
Perfect. Yes, we'll go with 2D, paper-doll-esque animation for ''Sumomo's World''. :^)

We'll also need fireworks, pantsu, toy cars, dog, cats, fun side-scrolling towns and layouts. 

Oh and I'd like you to add some kind of cute dollhouses for Sumomo and Kotoko to live in to the list. That was always missing in the show, and they will be a part of the gear inventory for any real-life ''RW Foundations''-based Chibitsu & Arigato grade robowaifus. The former as actual cute dollhouses, and the latter as docking, charging, and storage cases. I'd like to include some representation of them in Sumomo's World.

>===
-''prose edit''

# 34
>>14488
>I wish I was this autistic, great job Chobitsu
LOL. Don't thank me Anon, thank our brilliant '''Scriptwriter Anon''' (>>14442, >>14444, >>14451)

Undoubtedly an Anon of many talents, I'll warrant. Through his choice word selections, he's actually __improved__ on the original ''Chibitsu'' story IMO. We've added a library into ''RW Foundations'' ('''RW Action!''') to both take advantage of his efforts here with us, and to try molding it into something even better for ''Sumomo's World'''.

But yes, it is some nice work, Kiwi. :^)

# 35
>>14527
>we'll go with 2D, paper-doll-esque animation for Sumomo's World.

So its Bonzi buddy? But with a Chobits skin and without the malware?

# 36
>>14488
>I understand GitHub is pozzed but, why not GitLab?

The issue '''''__isn't__''''' primarily about the current-year-tier degeneracy (after all evildoers gonna evil), but rather the fact they would be quite likely to yank the rug out from under it the moment any screeching harpies working there got wind of it. Why bother? And don't be shocked if GitLab goes down this exact same path, Kiwi--they are already well along their way on it.

At least by dropping the code here we're still among friends. The only issue here is validation of the code's authenticity and I've decided to tag all the drops of ''RW Foundations'' software that I myself make here, with my role signature. As long as I'm still a part of the /robowaifu/ 'staff', this should at least help out a bit with that point.

But, I do already have an account on GitLab (Chobitsu), and so I'll make you a proposition Anon:

Set up an account for distributing our RW Foundations-based projects from here. Also, give me keys to the place as full contributor, and I'll occasionally look in on it and possibly leave some good things there for you. '''BUT I'M NOT GOING TO MANAGE IT FOR YOU ANON!11''' :^) (honestly, I have plenty on my plate already)

I'd highly suggest you __wait__ to do this until the new ''Bumpmaster'' project is up and working, and then do __'''that'''__ as your first repo there. That way, the project should eventually draw attention from the right sorts of men **Anons**, and hopefully establish itself quickly enough to become well-known and get some helpful pull-requests.

And that '''before''' the target gets painted on your back there. This will surely happen once we move past the ''Sumomo's World'' phase, and move into doing real-life fairybot/moebot grade robowaifus using the software. Once this happens the attention will ramp up quickly, and the leftists and other evildoers will start their ''tirade-parade'' vitriol as they get wind of it.

How does this idea sound to you, Anon?

>===
-''prose & grammar edits''

# 37
>>14529
Lol. Sure if that's what you'd like Anon, we'll do a 'Sumomo Buddy' project. Can you code in C++?

# 38
>>14521
>Naicu progress Chobitsu
Thanks! It's all ''Bumpmaster'' for now until it's working properly. I'm not sure what thread to do the drops for ''RW Foundations'' projects in until we get back around to implementing ''Sumomo's World''. Any Anons have advice or suggestions? ATM, I'll likely just keep going with it here, even though it's plainly off-topic (the underlying software framework being the most important point, to me as a budding software architect).

But I'm open to hearing other suggestions.

>===
-''minor prose edit''

# 39
>>14527
Would Lain Bootleg style work? I can make assets in that perspective and with Chobits style. It would also be nice if Anons would provide sketches if they want custom avatars for the game. If you don't submit a sketch, you'll be represented by Hideki Chobitsu. 

>>14528
Kek my mistake, I wish I was as autistic as Scriptwriter Anon.

>>14530
I'm considering your offer, will get back to you on that. Though, I honestly do understand where you are coming from. It is much safer here. We have security through obscurity given the usually sub 10 unique IP's here.

# 40
>>14543
>Would Lain Bootleg style work?
Sure! That would be great Kiwi. I would recommend you choose very saturated (and fun!) color schemes. Much richer than the series had. Remember, this ''Sumomo's World!'' Having everything vaguely Chibi-esque would right on-topic for the project as well.

>I'm considering your offer, will get back to you on that.
No rush, take your time thinking it through very thoroughly Anon. It will be at __least__ a couple month's time. Same for the art assets creation too.

# 41
dropping this here for safekeeping.
https://github.com/ad044/lain-bootleg-bootleg

# 42
>>14546
>making art assets
Will the program support L2D model formats?

# 43
>>14555
Formats supported by (or ''convertible to'' formats supported by) the external ''assimp'' library would be supportable by us with little additional efforts beyond those having already been made here in the past.
https://www.assimp.org/

Note that for ''Sumomo's World!'' there are no plans for anything beyond paper-doll-esque animations--it's both simpler to implement and is sufficient to begin fleshing out many of the robotics-centric algorithms and callgraphs. One of the (hidden, but) primary goals behind this initial effort is to keep the implementation details down to just bare essentials, since this reduces the 'frontloading' costs to development. And (if done well) it also assists in our ability to do reasoning about our algorithms (since, again, it reduces complexity).
>tl;dr
This is just a simple prototyping project at this stage. We'll tackle more complexity in due course.

>===
-''add phrase 'many of'''
-''fix erroneous crosslink''
-''add 'reasoning about' comment''
-''minor grammar & prose edits''

# 44
>>14556
That's essentially what I meant by the easiest way to make a paper model besides maybe pre rendered image sequences.

# 45
>>14557
Ah, thanks for clearing that up for me AllieDev. I'm unfamiliar with the format in any specific way, and just presumed it was 3D given the context of it's typical usage.

If you'd recommend it, then do you mind pointing out some good 'implementer' resources related to it?

# 46
>>14558
Thought a website implementation may be neat for the board so I found this resource: 

https://github.com/Konata09/Live2dOnWeb/

Written in C++ and could work for the application specs:

https://www.live2d.com/en/download/cubism-sdk/

There is also the official SDK manuals with some tutorials. you don't need to make a game, just use as a base to work off that already supports making and using the puppets you described.

https://docs.live2d.com/?locale=en_us

Sorry if I am derailing the thread. Just some suggestions I thought were helpful.

I have faith you can implement the model formats with the extensions they developed for Live2D "Native" that work with Visual studio. 
The extension downloads are under the "SDK for Native" section.

# 47
>>14556
>>14556
>Assimp
That can use PNG files as textures so I'll make PNG's for Sumomo. Your mindset on finishing the necessary minima before adding complexity is correct and appreciated. :^)

>>14597
Live2D would make things easier. The deformation and easy rigging options would lead to less parts needing to be made for Sumomo and as her artist I have to go with that.

Will post some Sumomo soon, full time Uni has been a drag lately.

# 48
>>14597
>>Thought a website implementation may be neat for the board so I found this resource: 
Neat idea. Anyone here good as JS? Custom JS is usable in Lynxchan (check the 'Settings' link in page header).

>Sorry if I am derailing the thread.
What!? Lol, no AllieDev. Anything related to the project overall is certainly on-topic ITT (or even the much broader-scope ''RW Foundations'' concepts).

>Written in C++ and could work for the application specs:
>There is also the official SDK manuals with some tutorials
Perfect. I really appreciate the legwork AllieDev. I can't make any estimate yet of my ability to use the format, but it would plainly be a good idea at some point for ''Chibitsu'' avatars.

I'll try to respond to other posts on the board discussing the L2D thing soon. Cheers

>>14604
Great! PNG should be perfect Kiwi.

>Sage
Lol. You bumped the thread with your post anyway and summoned me, Anon (and a good thing too since it's on-topic). Only the lowercase version **of "''sahh-ghey''"** works. If a polite ''sage'' is what you're actually going for, then just put a single one of those into the email field. :^) (>>14526)

>full time Uni has been a drag lately.
I know that feel, trust me I do. Just keep a picture in mind of the day when a cute little Sumomo will be there to give you the '''''Study Real Hard, and You'll Pass That Test!!''''' cheer. Gambatte, Anon. :^)

# 49
RW Foundations Caturday Drop : '''v211204 edition'''

It's Caturday again Anons. Woot!

Well we've kind of shifted gears for this go-round, ''Sumomo'''s on hold for now, and we are focusing on getting the new ''Bumpmaster'' project up and running successfully within the overarching library framework. As mentioned elsewhere; 
>"So, when we reach a level where a functioning robowaifu needs to use Bumpmaster or Waifusearch, she'll be able to do so with very little extra effort on the part of the men developing her." (>>14353)

We believe this style of software adoption is a good general approach for us, for a number of reasons:
'''- Ensures the libraries all each work together successfully'''
'''- Enables our robowaifus to have additional programs to safely use as well'''
'''- Better proves-out our general stability, safety, security, & control concepts'''

Hopefully, we can help move towards achieving all of these goals by prototyping, then fully integrating both ''Bumpmaster'' and ''Waifusearch'' into our Foundations library. Not only will it be a nice thing to have these new (somewhat more capable) programs ''ourselves'', but eventually giving our robowaifus the facility to directly run them will also be helpful too. 

Even if it turns out we need to remove them both in the end, this effort will certainly be a good learning experience for everyone involved. And since we are writing the (vastly more simple) software '''ourselves'''--with full access & visibility for every line of code--it's very likely to be much safer than just giving a robowaifu unrestricted access to the data outputs from some potentially malware-infested pages through a web browser's file-save facility, etc.

Read-only access (as in: '''''literally''' reading directly from an external computer's monitor'') using either approach is probably OK for her in most contexts, roughly-speaking. About the same as it might be for a human child for instance. But, when it comes to any ''__more-direct__'' data accesses (involving storing either files, data or information locally for offline-retrieval, for example) then we consider our approach to be a much safer one for our robowaifus.

On that note; we've removed the main library '''RW Wired''' from the Foundations library itself, and begun moving to implementing that functionality within the '''RW Dollhouse''' library. Dollhouse was always meant to be a 'General Outboard Systems' (that is, outboard of the robowaifu herself) library, in addition to it's other features. Therefore, it seems the most appropriate place to consolidate all external network accesses through it's interfaces. 

It's both easier to control, and to account for any external networking usage through this approach. It's also far easier for a regular robowaifu owner to control things using the dollhouse hardware itself. He can flip the networking hardware switch itself off, or even just literally 'pull the plug'. BTW, we're adopting an "''only-briefly-connected,''' 'Dolldrop' '''''" approach & philosophy for all our external networking code within the Foundations (which has proven to be a pretty fun thing to begin thinking through, actually).

'''''__In other news;__''''' we've begun some initial basic efforts to provide both callgraph-recording/tracing & function-level access-control within RW Foundations. Both of these facilities should be particularly helpful once the code grows larger. Actually ''understanding'' what's going on within a highly-complex systems is the __first__ order of business for software architects and engineers '''building''' those systems. We hope our approaches will greatly enhance that ability for every Anon involved. Indeed for anyone.

So, the plan is probably to just continue using this same thread for any new "RW Foundations" drops (even if they seem at first glance to be off-topic ITT). Over time all of these interrelated software & hardware technologies and concerns will blend together into a single, ''large'', system in the end. We'll try to keep it all sorted out properly along the way.

Be patient Anon, Good Lord is willing we'll all eventually get there!  :^)

'''==='''

>version.log
```cpp
   v.211204
---------------
-add global and local 'do_stamps' flags to control callstamping
-begin 'stamps_.emplace()' calls into class' func defs
-begin 'Stampstack stamps_' private member fields (callgraph analysis)
-bumpmaster gets member; board
-begin Board in rw::curator::bumpmaster
-bumpmaster gets member; site
-begin Site in rw::curator::bumpmaster
-begin class' Master-only func protos; catalog, thread
-begin enum class rw::Type + integrate across system
-begin bind_master(), slave objects intended for a Bumpmaster 's use only;
    catalog, page, post, thread
-in rw::curator::bumpmaster; rm aliasing of catalog, page, post, thread    
-begin prototyping the binding of all member slave objs to their master class
-dollhouse gets member; shell (shell & power care)
-shell gets member; dollhouse (shell & power care)
-shell gets member; gears
-rw::wired main library removed from RW Foundations
-arigato, bumpmaster, curator gets member; dollhouse (dolldrop comms)
-arigato, bumpmaster removes member; wired
-begin protected/private classes Dolldrop, Wired within rw::dollhouse::Dollhouse_b
-begin architectural rework; mv all RW Foundations network comms through dollhouse
-ren Tip>Hip, consolidate RW field' accessor as 't()'; integrate everywhere
-begin bumpmaster demo project; shifting dev focus over to bumpmaster for now
-ren 'Sumomo' project to 'Sumomo's World!' project
-ren sumomo_version.log>version.log; mv to RW Foundations lib's domain;
-sumomo gets members; confetti, dustpan, whisk
-begin Confetti, Dustpan, Whisk in rw::chibitsu::props
-moveit gets member; bones```
>rw_bumpmaster-v211204.tar.xz.sha256sum
```cpp
cbd8349074b85f5d096e365709a0dd31f6cd6f89c5452dbd7f6f864d16677355 *rw_bumpmaster-v211204.tar.xz```
>backup drop:
https://files.catbox.moe/mw7rp7.7z

# 50
RW Foundations Caturday Drop - '''v211211 edition'''

What, Caturday already? **Time again for cute anime catgrill meidos ofc.**

So, we stepped back and had a go at working on the callgraph 'stamping' (sort of like a function log) and everything seemed to go quite well with it all. Both the timing precision and the efficiency of the stamping process itself seems to be quite good at this stage and we don't anticipate any issues with it.

We started fleshing out a fundamental mechanism to collect up the so-called 'Stampstack's (stack containers of function-call logging 'stamps') from all the active RW objects, and work through analyzing their inter-relationships between. R/n the 'analysis' of the ''analyze_callgraph()'' function is rather sparse atm **it just dumps the entire data out to console** so it's nothing special at this point. Still, even at this very early stage it's apparent the system is working properly in a basic sense, and everything is communicating well with everything else. That fact is both gratifying and encouraging.

Here's a short example snippet from the callgraph display for the first two active objects of Bumpmaster:
```cpp
Callgraph size (ie, the number of active RW objects) : 9

 - Object's Handle.ID : 'bumpmaster.0'
	object's stampstack size : 4
              bumpmaster.0  (self)  calls obj's :           preflight() func at :  23m:58s:812ms:888us:796ns  past hr
              bumpmaster.0  (self)  calls obj's :          Bumpmaster() func at :  23m:58s:812ms:888us: 16ns  past hr
              bumpmaster.0  (self)  calls obj's :        Bumpmaster_b() func at :  23m:58s:812ms:824us:320ns  past hr
              bumpmaster.0  (self)  calls obj's :                  RW() func at :  23m:58s:812ms:818us:260ns  past hr

 - Object's Handle.ID : 'bumpmaster_board.1'
	object's stampstack size : 7
        bumpmaster_board.1  (self)  calls obj's :              master() func at :  23m:58s:813ms:707us:772ns  past hr
        bumpmaster_board.1  (self)  calls obj's :              master() func at :  23m:58s:813ms:328us:428ns  past hr
              bumpmaster.0          calls obj's :         bind_master() func at :  23m:58s:812ms:889us:540ns  past hr
        bumpmaster_board.1  (self)  calls obj's :             Board_b() func at :  23m:58s:812ms:841us:660ns  past hr
        bumpmaster_board.1  (self)  calls obj's :        master_types() func at :  23m:58s:812ms:839us:944ns  past hr
        bumpmaster_board.1  (self)  calls obj's :            RW_slave() func at :  23m:58s:812ms:837us:628ns  past hr
        bumpmaster_board.1  (self)  calls obj's :                  RW() func at :  23m:58s:812ms:831us:904ns  past hr```
Along with the high degree of flexibility possible by simply embedding any object within any other, and giving them all the potential for 'any-to-any' communications, this call-stamp system is reassuring. It seems like our architectural decisions are sound, and that no major revisions will be needed. We also plan to add more sophisticated system analyses later, adding animated graphical views of interactions. Possibly even a 'glass-cockpit' dashboard view of the systems ''in situ''. This would greatly increase the visibility into the robowaifu's running systems ofc.

'''Additionally''', we began toying with some basic concepts for the '''RW Atashi''' library. There's not much we have to show yet, but the ideas are slowly coming into focus for us. We plan to simply take a deterministic, 'grass-roots' (ground-up) philosophical approach to the cognition & personification problems for robowaifus. We'll see what we can manage in that way using only very modest hardware to do it with (RPis, Beaglebones, etc.) This is definitely the problem-space we need to address to remain feasible, so we're going to take an honest whack at it! I would predict we'll have some degree of reasonable success for basic features of the library over the next year, all things being equal.

It appears we have enough basic tools at our disposal now to set out on our journey. Undoubtedly we'll need to devise new ones along the way, but I think we have enough resources gathered now to begin our trek up the mountainside. Let us begin! :^)

Cheers.

'''==='''

>version.log
```cpp
   v.211211
---------------
-add helper struct Hdl_id; adds support for common ops related to Hip 's
-add nanosecond-scaled breakdowns of Callstamp Time 's; analyze_callgraph()
-begin basic implementation; analyze_callgraph() utility function
-mv call-stamping up to RW base class + integrate
-integrate + mv RW_slave inheritance of the slave object classes for the system;
    board, catalog, page, post, site, thread
-begin RW_slave in rw:: ; adds a 'muliple-masters-that-are-suitable' capability
-begin Analogy, Cognate, Concept, Percept in rw::atashi::cognate
-begin Hand in rw::shell::hand
-begin Gears_HAL in rw::gears::hal (hardware abstraction layer)
-begin Electro_HAL in rw::electro::hal (hardware abstraction layer)```
>rw_bumpmaster-v211211.tar.xz.sha256sum
```cpp
b926e043246a91dbcd29f92e3a31878cad6992c4c2ceb5be17f0b4fc619d8dc6 *rw_bumpmaster-v211211.tar.xz```
>backup drop
https://files.catbox.moe/8n6ee9.7z

# 51
>>14607
How does this look for you Chobitsu? Finally had the time to work on it a bit. I have Covid and pnuemonia so progress will be slow unfortunately.

# 52
>>14650
Did a bit more, won't make more until I have confirmation this is correct.

# 53
>>14650
>>14651
Neat! Nice work Kiwi. A couple of points to consider:
  -It would be good for us to go with a very-saturated color scheme for everything. Think ''children's casual game''  (>>14546)
  -Eventually it would be good for us to have 1/8 rotation turntable views, and we'll animate between them to simulate 'turning'.

BTW, is the plan still to use PNG 's?

We're planning to use a side-scroller-like, 2.5-D motion scheme. Roughly the Chibitsu short, but as animation with minor interaction with Anon. (Stop, Go, Pick those pantsu up Sumomo). :^)

Great job Kiwi, it looks nice!

# 54
>>14652
Would you mind providing a color pallet? I got the colors from a screenshot of the anime but understand wanting bolder colors.

>Other angles
That will take time but, I will do what I can. Thank you for your encouragement.

# 55
>>14650
BTW, take your time Anon. It will be at __least__ 1.5 months before we'll be ready to pick back up work on the ''Sumomo's World!'' project, and even then it will be to start work on the '''RW Action!''' library tools to support the production effort. So yeah, I'd say just focus on healing up r/n instead.

Get to feeling better, Kiwi.

# 56
>>14656
>Would you mind providing a color pallet?
Sure, I'll look around for something. It may be a while. In the meantime, just think ''Candy Crush''. **:^)**

>That will take time but, I will do what I can
Again, no rush. The focus isn't on creating a refined-looking 'game', but rather ATM to provide some basic visualizations of the internal workings of the ''RW Foundations'' systems.

>Thank you for your encouragement.
You're appreciated, Bro!
>

# 57
RW Foundations Caturday drop : '''v211218 edition'''

Catgrills+Meidos, or Meidos+Catgrills. You decide Anon. **You can pick only two, however!**

Well, most of the focus for this go-round was on bringing up the basic networking capability for Foundations. We've added a new sub-library '''RW Dollnet''' to focus this effort through. This is a constrained-class system intended to work closely with (and through) the internal class ''Dolldrop'' (located inside Dollhouse). The original Wired library concept has now been dropped entirely in favor of this new approach. The plan now is pretty much to completely decouple any active networking from the rest of the system that directly involves any robowaifus (such as the planned upcoming ''Sumomo''), and to use so-called 'dolldrops' (file-drops) as the primary means for any new information retrieval for her. 

This should be an approach that allows for Sumomo ''et al'' to still do lookups **Sumomo, find great bathing software for us please! :^)**, but have her make the requests/retrievals entirely in an offline way. Probably using some kind of shared mailbox files (or even some style of air-gapped '''sneakernet''') that she can use to signal a ''Curator'', ''Bumpmaster'', or some other information-networked class instance (running in a system external to hers) to retrieve data for her. That's the intent anyway. We'll see how far we can actually manage it in reality. 

BTW, we finally got around to adding a progress meter bar for it's downloads (within Dollnet, actually) and it works pretty much as expected. So yeah, that's a small but handy improvement for things moving forward.

```cpp
            asked to pull a drop -               bumpmaster.0    	addr:    0x7ffe60bc4f80
- requested pull drop : 'example.com'

 100.0% [================================================================================]  bytes :   1256 of   1256,  in  0.3 secs```

Bumpmaster will be the first running program that we actually have going for the RW Foundations, and this should help us all answer a few of these safety-design questions along the way (one of the reasons we chose it ''first''). This is kind of an interesting problem to work on, actually.

We also began laying out a few new class & system concepts here and there as well. Stayed tuned for more on these later. In the meantime, this edition should hopefully give you plenty of new ideas and code to study with for now Anon. Forth, Intrepid Adventurers!

Cheers.

'''==='''

>version.log
```cpp
   v.211218
---------------
-arigato gets member; hand
-prepend hours UTC to Time displays
-implement progress meter display for dollnet DL's
-rm wired nested class member; dolldrop
-begin Dollnet in rw::dollhouse::net + integrate w/ Dollhouse
-begin Gymnasium in rw::curator::sensei
-begin Categories, Collections in rw::curator::alexandria
-begin Alexandria, Sensei in rw::curator
-begin Dogfood in rw::util```
>rw_bumpmaster-v211218.tar.xz.sha256sum
```cpp
d9a2c9dd9884bef461bc7940fe6886e9ed0fd95ca9f602452223487ca5de8ccc *rw_bumpmaster-v211218.tar.xz```
>backup drop
https://files.catbox.moe/87zxc9.7z

# 58
RW Foundations Caturday drop : '''v211225 edition'''

Catgrill Meidos are wishing you a very Merry Christmas, Anon!

Welcome to the final Caturday drop of the year 2021, /robowaifu/ . It's been quite a ride this past year for all of us I'm sure. We're going to drop this one here just a little ahead of time on Christmas Eve.

As typical during this phase of the project overall, networking got the lion's share of development focus. The decision was finally made to pull '''RW Dolldrop''' out into it's own sub-library, and to remove all networking code from the Dollhouse. We also improved the mundane item of the progress meter bar into a better-abstracted arrangement, and in it's own codefile. Overall the network architecture part of the systems feels like it's coming into better focus now.

We realized that continuing to try and shoehorn networking in alongside all the other outboard systems provided by a robowaifu's Dollhouse (charging, storage, etc), was in hindsight an obvious error. That one's my fault+. The two domains are plainly distinct concerns; when a robowaifu needs all of her dollhouse's other services, but shouldn't be exposed to any networking at all (and everything that implies). 

Anyway, this new architectural arrangement of making Dolldrop 's a sub-library under Dollhouse is still a good logical arrangement overall. It also makes reasoning about the general framework cleaner, when it's known that all the direct networking code is 'corralled' and encapsulated within just one area of the system. Management of networking itself will surely be a bit easier this way as well. Let's all hope we can keep the 'simple' things simple!

'''Also''', we began thinking through a few aspects of some of the more abstract parts of a robowaifu's 'thinking' process, including creativity in both technical and aesthetic modes of perception and reasoning. We'll see how we manage it all going forward, but it will certainly all be a very very interesting set of areas for sure.

BTW, we won't be making a drop next week (New Year's day), We'll be taking a break during the Holidays but plan to pick it back up again in two weeks from now, Lord willing. So look forward to it then Anon!  :^)

Cheers, and Merry Christmas /robowaifu/ .

'''==='''

>version.log
```cpp
   v.211225
---------------
-design gets members; beauty, form, symmetry
-begin Form, Symmetry in rw::atashi::beauty
-beauty gets member; design
-begin Beauty, Design in rw::atashi
-begin validation(s) for the rw::Type of callers; pull_w_hdr()
-ren ask_drop()>pull_w_hdr(); Dolldrop
-mv Dollnet to private visibility w/ protected accessor(s); Mailstop
-begin internal private class Mailstop; Dolldrop
-begin Dolldrop lib in rw::dollhouse::net; all networking moved out of Dollhouse```
>rw_bumpmaster-v211225.tar.xz.sha256sum
```cpp
ed4a00be0709aa0a9f8506e462c847edd665eb2174c95defe0d9b207b60c5ddd *rw_bumpmaster-v211225.tar.xz```
>backup drop
https://files.catbox.moe/lklog5.7z

# 59
RW Foundations Caturday drop : '''v220108 edition'''

'''''Catgrills. Meidos.''''' Apparently some things in life are just non-negotiable, Anon.  **:^)**

Happy New Year, /robowaifu/! We hope you've gotten it started off on the right foot. Have any good resolutions for this one? We have a few, too.

For the most part, this time out we've simply added a few little fit-and-finish touches in the networking systems. Things like better display support for dollnet transfers, and some minor utility improvements with the dolldrop files themselves. We sort of proactively backed out a buggy call within ''main()'' 's catch blocks, related to presenting a callgraph display following mistaken coder errors. Moving those calls up into the error() functions themselves straightened this issue out.

Turns out, the experience of tightening up the networking a bit has given us some insights into tightening things up in general. For example, all of the Bumpmaster ''slave object classes'' have had their default constructors cut off, which (as with other aspects of the ''RW_slave'', et al, design efforts) should help to reduce unintentional code misuses. Why let a problem get started when you can readily stop it in it's tracks? '''An ounce of prevention is worth a pound of cure''' or so they tell me. :^)

These projects are going to become ginormous big systems in the end after all is said and done, and we'd best pay attention to all the little details & things along the way up this long mountainside climb ahead of us. Also on that note just in case any other Anons decide to join in on the C++ code-wrangling & architectural ~~mountaineering~~ engineering fun, we've given the 'Coding Guidelines' a little love too. If you decide you'd like to make a few choice pull requests to help out with the team-effort here, please just ask us for any clarifications on anything that isn't already mountain spring-water clear. 

So, with this release it seems like enough basic functionality of the external networking for ''RW Foundations'' is fairly in place. Plainly, there are plenty more enhancements to make in these areas going forward, but this should be enough to go on with for now. 

During the upcoming go-round it's likely to be more work on system support-ish items, before cracking into the actual Bumpmaster code itself. We'll probably kick this next bit off with the initial design, testing, & evaluation of a good JSON facility. This focus should also lead to the creation of a new sub-library for rw::curator **'''RW JSONator''', Anynon???**. It's very important that this key area be done well, as it will be a crucial item that eventually touches on practically everything else across the entirety of the Foundations' systems. It had better be both efficient and robust. It may take us a while to get through this particular effort, so please be patient Anon. "A good foundation", and all that.

Again, Happy New Year. We pray this will be one of the best ever for you and indeed for all of us. '''''Forward!''''' :^)

Cheers.

'''==='''

>version.log
```cpp
   v.220108
---------------
-edits for general usage notes; ./dolldrops/tail_me.txt
-add incremental file-numbering suffixes to dolldrops
-update progress meter display to support unbounded (streaming) xfers; dollnet
-mv to h:m:s elapsed times in progress meter displays; dollnet
-mv to KiB/MiB units in progress meter displays; dollnet
-mv prt_prog() et al, to dollnet_util.cpp; rw::dollhouse::net
-minor reformatting of ns Time displays for better readability + system utility
-rm default ctors, bumpMaster's slave object class members; Master 's tag req'd
-edits for Coding Guidelines; bottom of version.log
-rm analyze_callgraph() calls inside catch blocks (as unusable); main()
    (bug: program's callstack already unwound; objects dtor'd)
    mv analyze_callgraph() calls inside error() 's instead (before throw)```
>rw_bumpmaster-v220108.tar.xz.sha256sum
```cpp
0a685bbe7f7cdd47bba36343a8db9810c4a0beec9eb70374f2ed3fa71449d18d *rw_bumpmaster-v220108.tar.xz```
>backup drop
https://files.catbox.moe/4ixguz.7z

# 60
>>14918
It is the year of the tiger, perfect for catgrills!
Good to see the foundations of the code are being made sturdier. Good job Chobitsu.

# 61
>>14920
LOL timely post Kiwi, grats! BTW, that's a really cool design. Have any more arts by that anon?

# 62
>>14928
They're a new artist but they make really cute work. Here's their page: https://www.pixiv.net/en/users/14993888

# 63
>>14918
>Inb4 the april fools BUMP update.

# 64
RW Foundations Caturday drop : '''v220115 edition'''

Catgrills + Meidos. Two great things in life that just go great together!

So, we've been giving a bit of a think to JSON libraries and some other robowaifu topics for this dropcycle. What's that you say Anon? "How do ''Robowaifus'' and ''JSON'' go together any how?" Well, just stay tuned to this channel to find out! :^)

We've settled down to a competition between two primary JSON library candidates: '''nlohmann/json''' (https://github.com/nlohmann/json), and '''Tencent/rapidjson''' (https://github.com/miloyip/rapidjson) .

Modern C++ JSON has by far the best STL-style coding story going, and is exceptionally straightforward to understand for an experienced developer. OTOH, it's not as fast/efficient as it could be, and in smol systems this might turn out to be a deal-breaker.

For it's part on the plus side, RapidJSON has speed, efficiency & good standards conformance. OTOH, it's somewhat archaic and doesn't lend itself super-well to Modern C++ development. These are going to be yuge sets of libraries for us in the end, and ease-of-use for our coders themselves is a high system priority.

The current plan for now is to go ahead and build a working ''Bumpmaster'' prototype implementation using just one of the libraries, branch that, then re-implement it again using the other one. Then compare and contrast the two. Very likely there will also be some timing analysis in addition to our current analyze_callgraph() framework feature.

I suppose time will tell. Let us see what falls out of this testing process, Anon.

'''We also''' kicked off a few new library items for the ''RW Foundations''. Apart from two additional interesting items for the Atashi Cognate lib, we started up a new sub-lib in Electro : '''RW Power'''. We're going to need to manage all that awesome ''Robowaifu **Electromotive** Force'' (tm) from __somewhere__, right Anons? This will begin to give us the framework for addressing it properly.

For ''Dolldrop'', we added a couple of new pull calls; '''dolldrop.pull()''' and '''dolldrop.pull_hdr()'''. This separates out pulling a dolldrop's body-only, and it's header-only. This should make bandwidth optimizations and other functionality a bit more convenient as we go along.

Also in ''Dollnet'' we decided it was a good idea to show that a pull request had in fact been made, rather than leave everyone hanging (just in case the servers on the remote end decide to take their sweet time about it all).

We're coming along pretty well it seems, and soon-ish we should have the beginnings of a working Bumpmaster prototype. Then Waifusearch should be next. Looking forward to both it and to picking back up with '''Sumomo's World!''' again this year.

So let us take it all in hand, and see where this great adventure takes us Anon! :^)

Cheers.

'''==='''

>version.log
```cpp
   v.220115
---------------
-battery gets member; charger
-charger gets member; battery
-begin Battery, Charger; rw::electro::power
-begin Power sub-library; rw::electro
-begin Abstract, Elucidate; rw::atashi::cognate
-add is_empty() utility func for ifstream 's; rw::util
-add pull(), pull_hdr() func-chains; dolldrop/dollnet
-immediately show xfer times on curl requests, even w/o bytes flowing; dollnet```
>rw_bumpmaster-v220115.tar.xz.sha256sum
```cpp
0c720cc8aeef08b3fb21c029b89bf9e6e0f7ea88ef723df3f55ac8c6d86888d5 *rw_bumpmaster-v220115.tar.xz```
>backup drop
https://files.catbox.moe/mjow26.7z

# 65
**check my digits**

>>14951
Thanks Anon! Please let us all know if they make any other robowaifu type arts.

>>14957
LOL. Don't hold your breath Anon. Sure if we all discover some kind of big regression bug we can figure out, then sure we'd probably make a hofix drop or something. Otherwise ''RW Foundations'' will be both superior and also allow our robowaifus eventually to shitpost too.

# 66
RW Foundations Caturday drop : '''v220122 edition'''

Catgrill Meidos; an idea whose time has truly come! :^)

We decided to do the initial prototyping for the Bumpmaster project using the ''JSON for Modern C++'' library. It will probably be easier to work out all the little details by using it to begin with. Once everything's sorted out that way, then we'll branch the code and replace that library with the other JSON library under consideration. We'll likely also run them in parallel all the way through the development of ''Waifusearch'', and then make our decision on which to go forward with from there.

We've simplified the 'Master-only' function calls for the ''RW_Slave'' object classes, since the caller is already determined during the object's construction. You might note that the 'bump.t()' parameter is now gone from the dolldrop.pull() calls. The ''rw::util'' namespace was tightened up, and we added a couple of new utilities into it. We'll likely be migrating some of the other code spread out elsewhere up into that area sometime soon. 

We also started up a very interesting new sub-library '''RW Mimicry''' in rw::atashi::cognate. This will likely prove to be a key initial library to begin fleshing out the rest of the Atashi library. ''Chobits'' is filled with humorous scenes of both ''Chii'' & ''Sumomo'' mimicking their masters, and it should be a fun thing to begin solving. Things like pose-estimation and 'Theory of Mind' are both ideas that will certainly come to the fore during that particular effort.

'''Also''', one other thing we'd like to begin doing for these drop posts is to add in little bits of the code itself from the projects. Rant on it, rip into it, or give it props. The main point is to begin a conversation here about the code itself. Accordingly, here's a little snip from today's drop:

>main_bumpmaster.cpp snippet
```cpp
string const test_uri{
    "https://alogs.theГунтretort.com/robowaifu/catalog.json"};

puts("\n\n     --=^=--\n\n");
//--------
auto hdr_A = bump.dolldrop().pull_w_hdr(test_uri);
if (! is_empty(hdr_A)) {  //

  auto const ht = strmlines_2_vec(hdr_A);
  for (auto const& t : ht) {  // checks all header tags
    if (is_test_tag(t)) {
      cout << '\t' << t << '\n';
    }
  }

} else
  cout << "hdr_A empty\n";```
This form of pull() function for '''RW::Dolldrop''' returns a stream containing a header response for the dolldrop itself. This little bit of code first transforms that into a container of strings, and then goes through it line-by-line looking for specified tags in the header. Tags such as ''last-modified'', and ''content-length'' (number of bytes), for instance. This will be a useful feature to have in a number of ways for Bumpmaster. Thoughts?

Well we're starting to settle in to the new year, and we hope it brings good fortune and prosperity to every Anon here on /robowaifu/. Let's all press forward in earnest towards our goals this year! :^)

Cheers.

'''==='''

>version.log
```cpp
   v.220122
---------------
-begin Mimicry; rw::atashi::cognate
-add to_lower(), strmlines_2_vec() utility funcs; rw::util
-mv to simplified wrappers for RW_slave classes' 'Master-only' guarded funcs
-mv to general I/O stringstream 's, fstream 's
    as parms in is_empty() utility funcs; rw::util
    as return types in pull() call-chains; dollnet
-add 'JSON for Modern C++' hdr file (json.hpp), begin evaluations; ./extern/ dir
-enable './extern/' dir + add into bumpmaster includes; meson.build```
>rw_bumpmaster-v220122.tar.xz.sha256sum
```cpp
19414e73bdd1bbce309fab45ff5378c54086930e97e502bc1d9a10e4f960f010 *rw_bumpmaster-v220122.tar.xz```
>backup drop
https://files.catbox.moe/x07805.7z

# 67
>>15050
I apologize in advance and do not mean to come off as an attack on you. I am just giving some feedback and criticism.

I have been wondering for a while now about how the hell do we get this to compile?

 Have never heard of tar.xz extensions before finding /robowaifu/ and regardless of documentation, 7zip won’t recognize the file. Despite it downloading inside of a 7zip archive, making the whole tar.xz format completely redundant and an extra step that is discouraging to newcomers or anyone who would contribute as it comes off to people as malware thanks to the strange file extension. Regardless of whether or not that is true.

# 68
>>15060
I was actually going to make a step by step how to do it but I can't get it to work lol....
I can't figure out how to install the curlcpp 
this:
Then add <curlcpp root>/build/src/ to your library path and <curlcpp root>/include/ to your include path.

When linking, link against curlcpp (e.g.: g++ -std=c++11 example.cpp -o example -lcurlcpp -lcurl). Or if you want run from terminal,

g++ -std=c++11 example.cpp -L/home/username/path/to/build/src/ -I/home/username/path/to/include/ -lcurlcpp -lcurl
does not work.
what is example.cpp supposed to be?

and neither the
libcurlpp-dev
or
libcurlpp0
packages work

# 69
>>15062
and to add I also used cmake to build it to every single directory in my $PATH and it does not work

# 70
>>15062
>>15063
ok I figured it out
this should be the start to finish install on a debian based distro:

download rw_bumpmaster file
rename to .7z
7z e file.7z
	(sudo apt install p7zip-full if you don't have)
tar xf file.tar.xz
sudo apt install meson
sudo apt install libfltk1.1-dev
sudo apt install libcurl4-gnutls-dev
download github.com/JosephP91/curlcpp
unzip the just downloaded curlcpp-master.zip
navigate to the curlcpp-master/CMake in terminal
sudo apt install cmake
sudo cmake ..
sudo make # -j2
cd ..
make install
cd to rw_bumpmaster directory
meson build
cd build && ninja; cd ..
build/bumpmaster

but I don't know how to use it

# 71
>>15060
>>15062
Ahh, sorry about that Anons.

Yes, getting dependencies and other preliminary ceremony to software development can often be daunting for the newcomer. In teaching myself how to, I've done this thousands of times by now and hardly ever stop to consider any longer what it was like years ago when I began trying in earnest to learn this stuff. My apologies.

I'll take some time (hopefully today, certainly this week) and make a little tutorial about building '''RW Foundations''' software drops made ITT by us. So look forward to that soon.

Also, tarballs have been around for quite some time actually **about the same age as the C++ programming language itself**, so you needn't worry about their legitimacy Anon.
http://www.catb.org/jargon/html/T/tarball.html
https://en.wikipedia.org/wiki/Tar_(computing)

>>15064
Thanks you've got my back bro, much appreciated! :^)

I'll try to edit the README file used for the archives, and put in a TL;DR that sort of follows your steps for the beginners. I'll probably split it up into two parts; one for the dependencies, and one for the actual build steps.

Cheers.

# 72
OK, here's a quick rundown excluding the dependencies (the readme has links):

If you right-click on the ".pdf" file here (>>15050), you'll see AlogSpace's actual name of the file, just so you can confirm it's legitimacy. We'll be doing all our work here from the terminal.

First, grab the archive file itself into w/e directory you want:
```cpp
torsocks -i curl http://bhlnasxdkbaoxf4gtpbhavref7l2j3bwooes77hqcacxztkindztzrad.onion/.media/62a022ea91c78727fc222755f0d8f0286cce8a50dd2800bd2a7613aad28beb88.pdf -o rw_bumpmaster-v220122.7z

    or

curl https://files.catbox.moe/x07805.7z -o rw_bumpmaster-v220122.7z```

'''--=^=--'''

Next extract the outer 7zip file and have a look at the readme.txt:
```cpp
7z e rw_bumpmaster-v220122.7z 
cat bumpmaster_readme.txt```

Confirm the tarball's intact, then if so extract it:
```cpp
sha256sum -c rw_bumpmaster-v220122.tar.xz.sha256sum
tar -xf rw_bumpmaster-v220122.tar.xz```

Cd into the project's working directory:
```cpp
cd rw_bumpmaster-v220122/```

Configure it as a Meson Build project:
```cpp
meson build```

Finally cd to build/ and make the project with Ninja:
```cpp
cd build/ && ninja; cd .. ```

'''--=^=--'''

That's it, you're done Anon. To run either the ''bumpmaster'' or ''sumomos_world'' demo projects, just call them from the project's base directory:
```cpp
build/bumpmaster

    or

build/sumomos_world```

'''--=^=--'''

This is just a quick rough to get you started Anon. Again, the main point at this stage is simply to start a convo around the code itself, not to have '''"le ebin turn-key robowaifu code!!"'''  :^)

Cheers.

# 73
>>15074

Thanks Chobitsu! That should be enough to get anons started so they can see what you’ve been doing in these great weekly updates.

# 74
>>15082
You are welcome AllieDev, and thanks for pointing the issue out. I should have already dealt with that. I welcome anons having a look and maybe a bit of a tweak here and there to the codebase. It would be nice to get a community effort around this project going with a bunch of like-minded Anons.

# 75
RW Foundations Caturday drop : '''v220129 edition'''

Catgrills + Meidos, how did the world ever manage to turn before they were invented I ask you Anon!? :^)

We started up a new namespace for this go-round, '''rw::json'''. While ''RW Curator'' will likely wind up having some kind of a specialty library just for elegant JSON handling & data work **Still waiting to hear from you about '''RW JSONator''' Anon!**, this namespace is sort of a 'utilities branch' on the codetree.

We decided to go ahead and expand on one of the previous drop's examples, and add an automated mechanism to check the 'last-modified:' header tag for a dolldrop, and only download it again if it has changed since last time. As long as the server doesn't modify that header's tag unless the content has actually changed (ie, Anon makes an actual post to the board), then this will both reduce the load on your bandwidth, and on the server's too. As can be seen in the drop, supporting this idea required the addition of a fair few (though basic) JSON-oriented functions to dolldrop/dollnet.

We did a pretty good overhaul and moved over a lot of functions and alias' into the ''rw::sys'' & ''rw::util'' namespaces. This was overdue actually, so yeah. We began the process of adding in a few little utility functions too. For example ''lr_trim()''. We'll probably create a new subspace for text utilities eventually. There was an oversight for the build instructions for GCC in the meson.build file, and we gave that attention.

Overall the code is a good bit cleaner and better organized in this busy drop. If you want to make really big systems **and we do** then you really have to constantly focus on ease-of-maintenance. If you put it off till later it can become unmanageable. You have to stay on top of this stuff or it sneaks up on you!

So, here's some code from today's drop:

>main_bumpmaster.cpp snippet
```cpp
//------------------------------------------------------------------------------
/** For each thread in @a catalog, print out specified target field's value data
 * @param catalog the @c Json to search through (an IB catalog)
 * @param targ_field the @c std::string to match against
 */
void prt_targ_fields(Json const& catalog, std::string const& targ_field) {
  // NOTE: these C++17 structured bindings represent JSON [key:value] pairs

  // cycle through all the board catalog's threads
  for (auto const& [implct_idx, thread] : catalog.items()) {  //

    // for each thread, cycle through all of it's fields
    for (auto const& [field_nm, field_dat] : thread.items()) {  //

      // print out data for the thread's matching target field
      if (field_nm == targ_field)
        cout << ' ' << setw(3) << setfill(' ') << (stoi(implct_idx) + 1) << ' '
             << field_nm << "  :  " << field_dat << "\n";
    }
  }
}```
This cycles through all the thread elements in the catalog's JSON, and prints out w/e the target field's data value is (which in the basic example's case is the 'subject' field, but can be easily switched out for one of the dozen or so others Lynxchan uses). The ''JSON for Modern C++'' library pretty much directly supports both C++11 range-based for() loops and C++17 structured bindings, as can be readily seen in this snippet. That's actually really handy tbh.

Well, I hope you are doing well r/n Anon. Please keep the vision alive in your heart and let's all press forward together towards our goals! '''''Rugged Adventurer''' onwards!'' :^)

Cheers.

'''==='''

>version.log
```cpp
-add get_tag() utility func, + 2 wrappers (date, name); dollnet
-add set_tag() utility func, + 3 wrappers (date, name, uri); dollnet
-add dropfield(), chk_droptimes() utility funcs; dollnet
-add chk_logfile(), mk_logfile() utility funcs; dollnet
-add 'dropmod.json' log file; ./dolldrops/ dir
-add from_json(), to_json() Dropdata utility funcs; dollnet
-add Dropdata struct; dollnet
-mv to header-checked pull() 's; dolldrop/dollnet
-add operator>>(), operator<<(); rw::util
    for either stringstream 's or fstream 's, to/from vector<string> 's
-add trim_l(), trim_r(), trim_lr() string utility funcs; rw::util
-ren error()>rw_error() utility funcs; rw::util
-mv various functions & aliases over into rw::sys, rw::util; general
-cleanup of incls_all.hpp, srcs_all.cpp; general
-add 'system' decl/defn files; rw::sys
-add fstream_2_json() utility func; rw::json
-begin rw::json namespace
-add ./extern/ dir into sumomos_world includes; meson.build
-edit GCC build instructions, add ./extern/ dir includes; meson.build```
>rw_bumpmaster-v220129.tar.xz.sha256sum
```cpp
032478231181af7ee843269d78c2c7657d26a1619b4ef45d8fedb4a9de980eb9 *rw_bumpmaster-v220129.tar.xz```
>backup drop
https://files.catbox.moe/ktbqw3.7z

# 76
RW Foundations Caturday drop : '''v220205 edition'''

Singing, Dancing, Catgrill Meidos! Seemingly few things in this life could be much better! :^)

Well we did a bit of an architectural rework on this spin. The code that was basically just about the dolldrops themselves was kind of getting mixed in with the code that should really be exclusively about networking alone. So, since our plan is to significantly expand the capabilities of the '''Mailstop''' class inside ''RW Dolldrop'' in the future, and since this class will serve as a sort of air-gapped 'Post Office' for robowaifus to send/receive dolldrops, it made sense to go ahead and use this area of the codetree for this purpose.

Accordingly, we created a new ''mailstop_util'' set of utility files, and moved over most of the dolldrop-related code (that is, related to the actual files themselves) into them. Actually the process was quite easy, and that's a good thing. It shows that the progression with the codebase is going fairly well at this stage, and software components are staying loosely-coupled. This is always a boon for code maintenance ofc--and for 'local reasoning' about the code itself.

'''We also''' implemented improvements to the functions that get/set JSON elements into the ''dropmods.json'' file. One of those functions is highlighted in this post. Eventually we'll need to track all sorts of data for our robowaifu's configuration, settings, and run-time performance. It will basically be an important concern to us all as creators of ''RW Foundations'' software. It will also be a very handy **and fun ??** way for Anons to mod their robowaifu's configs, since it's all being done using JSON files. Probably couldn't be a much easier approach for this tbh.

So, here's a key new algorithm from today's drop:
>mailstop_util.cpp snippet
```cpp
//------------------------------------------------------------------------------
void set_tag(string const& uri, string const& tag, string const& tagdat) {  //

  if (! log_chkd) {
    chk_logfile();
    log_chkd = true;
  }

  // construct cp of droplog's data
  fstream ifs{droplog, ios::in};
  auto    j_out = fstream_2_json(ifs);

  auto rec_it = find_if(begin(j_out), end(j_out),  // have the record?
                        [&uri](Json const& j) { return uri == j["uri"]; });

  if (rec_it != end(j_out)) {  // found the record, assign the new tag data

    if (tag == "date")
      rec_it->at("date") = tagdat;
    else if (tag == "name")
      rec_it->at("name") = tagdat;
    else if (tag == "uri")
      rec_it->at("uri") = tagdat;

  } else {
    puts(" dropmod.json entry not found; adding new record...");

    Dropdata d{};
    d.uri = uri;
    j_out.emplace_back(d);  // constructs new JSON item in-place, via to_json()
  }

  ofstream ofs{droplog};
  ofs << j_out;
  ofs.close();
}
// wrappers-related
void set_date(string const& uri, string const& datedat) {
  set_tag(uri, "date", datedat);
}
void set_name(string const& uri, string const& namedat) {
  set_tag(uri, "name", namedat);
}
void set_uri(string const& uri, string const& uridat) {
  set_tag(uri, "uri", uridat);
}```
It gets called (e.g. from the ''chk_droptimes()'' func) like this:
```cpp
set_date(uri, currdate);```
This library function '''set_tag()''' reads in the ''./dolldrops/dropmod.json'' dolldrops log file, and looks through it's JSON for the URI that was passed in by the caller. If the record is found, then that specific tag (key) is updated with the new tag data (value). But if that tag's data isn't found, then a new triple-{key:value} element for that URI is added into the JSON array. The JSON is then written back out the log file. 

That's it. Not exactly an ''ACID Transaction'' (from the database world), but it's sufficient for our current needs. Actually, we'll plan to further improve these processes in the future until we actually ''do have'' efficient ACID transactions for our JSON and other data systems. In the meantime, we have begun the testing of our JSON library candidates sufficiently well in this way. We're sure there will be plenty to learn along the way!

Hopefully you're making good progress towards your robowaifu goals so far Anon. If not, then just step back for a couple hours, rethink your approaches, and then jump back into the fray. '''EVER ONWARD & UPWARD!''' :^)

Cheers.

'''==='''

>version.log
```cpp
   v.220205
---------------
-mv dolldrop-related funcs & aliases into mailstop_util; dolldrop/dollnet
-add 'mailstop_util' decl/defn files; rw::dollhouse::net
-add multi-drop support for dolldrop-related utility funcs; dolldrop/dollnet```
>rw_bumpmaster-v220205.tar.xz.sha256sum
```cpp
00c097ab4573df01eb9cc1e0f37b3715daafd614802a15085091fbbae3f72cb5 *rw_bumpmaster-v220205.tar.xz```
>backup drop
https://files.catbox.moe/g72pd6.7z

# 77
RW Foundations Caturday drop : '''v220212 edition'''

Catgrill Meidos. Every dollar not spent robotically-engineering them is a dollar that needs to be fiscally questioned! :^)

So, we continued padding out the minor architectural rework we began last turn and built up the ''Mailstop'' class a bit further. We moved over management of dolldrop file creation into it, and reworked the '''RW Dollnet''' functions that save out drops, to accept an already-instantiated ''std::ofstream'' as a parameter. This is not only a better 'separation of concerns', but it will also afford more flexibility once we begin the actual Bumpmaster code work itself **next go ?**.

We also expanded out the stable of utility functions for both mailstop and for rw::json. One ongoing (and significant) goal for the code creation itself is to attempt to continuously improve ease-of-use for it. All these little utility functions are basically meant to isolate generic functionality into smaller, and (hopefully) well-named abstractions. Not only does this improve the software maintenance task itself, but it makes the code generally easier to reason about--especially in the ''local context''.

Another related goal behind this work is to improve error-detection (and possibly error-correction). For example, JSON is prone to all kinds of potential issues with data validation since its a plaintext format. Thankfully this particular JSON library's writer has already done all the heavy lifting in this area for us, and we just need to double-check our inputs to it.

For the C++ programming language, the go-to mechanism for this is '''std::exception''' 's. This general topic is far too deep to go into in any way beyond just a superficial one here. But the TL;DR is, it's a means to catch errors in a highly-robust and well-organized fashion. If used properly, its remarkably capable at catching errors correctly.

Other languages that rely on humans to try and encompass managing every possible codepath and every possible exception state of complex code by hand **or even just to imagine them all** can't really hold a candle to C++'s brilliance in it's mechanism. Combined with ''RAII'', it simply can't be beat AFAICT. It's actually a major argument for using the language itself when devising highly-complex systems like robowaifus.

There are specific issues with using exceptions in __'''''hard realtime'''''__ systems (due to some potential time/complexity indeterminacies), and we'll address those appropriately when we get to that phase of the overarching ''RW Foundations'' code development **by dropping 'down' to C/ASM languages for that**. But for now, this approach is literally second to none for all our RW Dollhouse systems code (and most everything else in & for a robowaifu as well).

Now, back to the task of abstracting utility functions out. When attempting to emplace a JSON data element into a JSON array, again, there might be a problem with either the data or even the 'array' itself. It ''might not be'' an array, actually. Here's a function ''try_emplace_back()'' that catches that specific type of problem and notifies the developer. One very cool thing about the '''JFMCPP''' library is it's extensive support and documentation around potential exceptions with JSON.

>json_util.cpp snippet
```cpp
//------------------------------------------------------------------------------
template <typename T>
auto try_emplace_back(Json& json, T const& typ) -> bool {
  bool res{false};

  try {
    json.emplace_back(typ);
    res = true;
  }
  // https://json.nlohmann.me/api/basic_json/emplace_back/#exceptions
  catch (Json::type_error const& e) {
    cerr << "\n  Json::type_error \n'" << e.what()
         << "'\n  caught in try_emplace_back()\n\n";

    if (e.id == 311)
      cerr << "'type is other than JSON array or null'\n"
           << "https://json.nlohmann.me/home/exceptions/"
              "#jsonexceptiontype_error311\n";

  } catch (exception const& e) {
    cerr << "\n  exception '" << e.what()
         << "' caught in try_emplace_back()\n\n";
  }

  return res;
}```
This generic code attempts to emplace an object of any appropriate type into a JSON object. Since only JSON ''arrays'' are suited to these 'emplace_back()' operations, this specific type of error needs to be looked-out for. Not only does JFMCPP do this, but he conveniently links to the exception doc directly inside the library's javadocs. Pretty handy tbh.

'''And with this''' example's demo code, we're already a fair way to reproducing the functionality of an IB index page's text-display out to the console. This is probably a good sign that we're basically ready to approach the Bumpmaster classes themselves and start implementing new algorithms there. Most of the underlying system support code for dolldrop-based networking seems to be in good working order now.

So, we hope you are gaining new insights into your approaches with your robowaifu-related project work Anon. We look forward to seeing everything you devise for her. '''ONWARD!''' :^)

Cheers.

'''==='''

>version.log
```cpp
   v.220212
---------------
-mv dolldrop file creation mgmt into mailstop funcs; dolldrop/dollnet
-add 'chk_dropname()', 'build_dropname()' utility funcs; mailstop
-add 'find_log_rec()', 'add_log_rec()' utility funcs; mailstop
-mv mailstop's dolldrop-related funcs into defn file; mailstop
-add 'mailstop.cpp' defn file; rw::dollhouse::net
-rm default ctor, Mailstop; Owner 's tag req'd
-improve checking in get_tag(), set_tag(); mailstop_util
-improve 'new record' defaults; mailstop_util
-mv dolldrop pull-related funcs into defn file; dolldrop
-unify pull() call-chain func naming; dolldrop
-consolidate pull() 's call-chains; dolldrop
-add 'try_emplace_back()', 'try_idx_tag()' utility funcs; rw::json
-add 'rd_json_file()', 'wrt_json_file()' utility funcs; rw::json
-improve checking in fstream_2_json(); rw::json```
>rw_bumpmaster-v220212.tar.xz.sha256sum
```cpp
e7abc5155a7bb4dce277953e581a674c4bb6c631d8ff9dc213bd6843e73709ad *rw_bumpmaster-v220212.tar.xz```
>backup drop
https://files.catbox.moe/3feacd.7z

>===
>t. Chobitsu

# 78
>>15189
Lol don't know what happened to my name/role sig in that post? Let's see if it was just me?

>===
''heh, guess i fubar'd it. :P''

# 79
RW Foundations Caturday drop : '''v220219 edition'''

'''''Catgrills. Meidos.''''' Is it just me, or do these two words have a specific melodic sound when used together?
**BTW, I'm running short on Catgrill Meido pics Anon**
==SEND HALP SOON PLS!== :^)

Well we began implementing some initial functions inside the ''RW Bumpmaster'' class this go-round. For now these are just an initial approximations of the demo code from our last drop here, and may not stay in just these forms as-is. Also, several functions are better suited to the subordinate slave classes helping the primary Bumpmaster class itself, and so the plan is to eventually move these out into their more proper places.

Back to the JSON-related code from last time. One of the nice ideas the JFMCPP has is a pair of overloads on the functions ''from_json()'', and ''to_json()''. They kind of sit 'in the background' performing a transformations to/from other types with JSON. Here's an example use (that calls the exceptions wrapper class from last time):
>mailstop_util.cpp snippet
```cpp
auto add_log_rec(Json&              json_out,
                 std::string const& uri,
                 std::string const& tag,
                 std::string const& tagdat) -> bool {
  Dropdata d{};

  if (tag == "date")
    d.date = tagdat;
  else if (tag == "name")
    d.name = tagdat;

  // one source param or other, always set the uri tag for a new record
  if (tag == "uri")
    d.uri = tagdat;
  else
    d.uri = uri;

  // constructs a new JSON item in-place, via to_json()
  return try_emplace_back(json_out, d);
}```
Did you catch that? No? Hint: **it actually happens in the ''emplace_back()'' op in the other function**. The final line makes that call, and passed a ''Dropdata'' struct along as an argument.

Here's the related overload that does the 'magic':
```cpp
void from_json(Json const& j, Dropdata& d) {
  d.date = j["date"];
  d.name = j["name"];
  d.uri  = j["uri"];
}```
That's really all there is to it, nothing magical at all actually. The key reason this works so smoothly is that this library's author has created a generic mechanism so that this function overload works with ''any'' arbitrary type that is compatible with JSON. You simply need to define the details in your type's overload, as in this example.

'''We also''' began what should turn out to be a fun new class '''RW Sempai'''. When a robowaifu needs a little help and encouragement, ''Sempai'' is always there for her! :^) Initially, this should be a sort of way to help her when she's using Waifusearch, or asking the Curator for outside information. Sempai can help guide her into better ways of approaching the questions, etc. if things aren't working too well for her. There should also eventually be several other ways this sub-system can help a robowaifu out in her day-to-day life as well.

I'm personally pleased with the progress we're all making so far this year. I look forward to this being a really fun and productive period for /robowaifu/. Let's all have some real advances to show here by summer what do you say Anon?

Cheers.

'''==='''

>version.log
```cpp
   v.220219
---------------
-add thrd_posts(); bumpmaster
-add bump_thrd_uris(); bumpmaster
-add rd_thread_id(); bumpmaster
-add pull_json_drop(); bumpmaster
-add bld_cat_uri(), bld_thrd_uri() member funcs; bumpmaster
-add parse_cat_uri() member func; bumpmaster
-rm redundant type-checking, Master 's type already known at bind-time; dolldrop
-minor disp patch hms(), (1 min period past hr); dollnet
-begin Sempai; rw::curator```
>rw_bumpmaster-v220219.tar.xz.sha256sum
```cpp
7c8960a19b8051876e84b459a8aca5c533b43848363293b82cec57d2a6eb9d46 *rw_bumpmaster-v220219.tar.xz```
>backup drop
https://files.catbox.moe/n8puds.7z

# 80
>>15240
>Here's the related overload that does the 'magic':
LOL. I just realized I posted the wrong function. We're going ''from'' Dropdata ''to'' JSON. Here's the proper, 'other-half' one:
```cpp
void to_json(Json& j, Dropdata const& d) {
  j = Json{{"date", d.date}, {"name", d.name}, {"uri", d.uri}};
}```

Apologies about that Anon.

# 81
>>15240
Keep up the good work Chobitsu! Someday you'll be posting with real robot cat grill meidos.

# 82
Any plans on giving the robot a voice? Are you gonna have pre-recorded voices made by some girl you hired or are you gonna use a synthetic voice program?

# 83
>>15241
>JSON

Yay more common formats! Have you worked on getting them to generate actual dialog yet? Keep it up Chobitsu!

>>15247

I have to replace the cooling fans on my 3D printer and would appreciate any help finding replacement ender 3 fans. Had gotten some test prints of the shell to hold together excellently without the need for screws.

# 84
>>15256
They can be found on Amazon for low cost with fast shipping. Can't recommend any one in particular. Hope you'll post progress soon.

Side note, it's been months and Chobitsu still hasn't posted the color palette for Sumomo. No pressure, just wondering what is going on with that.

# 85
>>15257
That’s not helpful at all.

# 86
>>15247
LOL. That's a really nice pair of huge **ears**! :^)
==SEND MOAR PLOX==
>Someday you'll be posting with real robot cat grill meidos.
It's a team effort, bro. Each of us contributes his own part. Someday, we'll __'''''all'''''__ be posting with real anime catgrill meidos!

>>15248
Yes. We have a couple of threads each for speech synthesis & chatbot/text generation. Just have a look around the catalog Anon.

>>15256
Thanks!
>Have you worked on getting them to generate actual dialog yet? 
As mentioned before, we'll be needing help from the /robowaifu/ team with that area. However, I'd suggest you have a look into this breakthrough just posted here today: (>>15289)

>>15257
>Side note, it's been months and Chobitsu still hasn't posted the color palette for Sumomo. No pressure, just wondering what is going on with that.
Honestly, I've given it little thoughts beyond our initial ones Kiwi. And it's looking like it could be well into summer before we can switch tracks back to this. Meanwhile, I'd say just use capps from Kick-Ass Anime's encodes for reference. They amped up the vibrancy over others, and it's quite a bit closer.

BTW, I've been replaying through the series during my workouts lately with an eye towards watching for Sumomo's appearances vs. Chii's. The cute little robowaifu is all over the show, actually. Especially the 'Cleaning Day' episode **where she gets accidentally shocked**. They may as well have called that one 'Sumomo's Show'.

# 87
>>15297
Aye, we must work til all Anons can have their waifu meidos. 
Side note, should re-watch Chobits.

# 88
RW Foundations Caturday drop : '''v220226 edition'''

Anime Catgrill Meidos. The reality will be worth it all Anon! :^)

So, one of the oddities about imageboard's APIs (at least we find it so) is that a thread's human-oriented information (subject, message, post ID) is contained in the ''catalog'' JSON, while the posts themselves are a sub-array contained in the ''thread'' JSON. Not only is this an awkward approach for any anon actually programming against such an API, but it's also pretty inefficient computationally-speaking. 

Within ''Bumpmaster'' at least, we'll be setting about to fix this. Basically the first order of business then is to combine all these elements together into a more appropriate data structure. Here's the basic (and rather simple) idea so far
(BTW, please pardon me if you're already conversant with C++ programming, my goal with this explanation is to familiarize those a little new to it here) :
>bumpmaster.hpp snippets
```cpp
/** A simple data struct to help with catalog's thread's information
 */
struct Thrd_data {  // Lynxchan's JSON tag names:
  string   msg;     // message
  string   subj;    // subject
  unsigned id;      // threadId

  vector<Post_data> posts;
};

...

/** A simple data struct to help with thread's post's information
 */
struct Post_data {  // Lynxchan's JSON tag names:
  string   date;    // creation
  string   msg;     // message
  unsigned id;      // postId
};```
These are a pair data structures we've created to hold the information we're actually interested in for Bumpmaster (we touched on a similar one last drop). We can talk about that '''std::vector''' member in the first one  later, but for now just think of it as an open-ended container for the second type of struct, ''Post_data''.

Basically, we have one data struct that's about the threads, and another one that's about the posts. We collect up all the post's data into that data container in the first struct. After these data sets are combined together this way, it's a much easier task to iterate over them -- and also more efficient too. That's really all there is to it Anon. We can talk more later about how we process this new data structure with our algorithms. If you have any questions in the meantime please don't hesitate to ask ITT.

Well, we hope you're coming up with some cool new ideas for your robowaifu-building adventures Anon. ''Please share them here with us all when you do!'' :^)

Cheers

'''==='''

>version.log
```cpp
   v.220226
---------------
-add top_bump_thrds(); bumpmaster
-add bump_thrd_dats(); bumpmaster
-add from_json(), to_json() utility funcs; bumpmaster
    for Thrd_data, Post_data
-add Thrd_data struct; bumpmaster
-s/Postdata/Post_data/; bumpmaster
-s/parse_cat_uri/parse_ib_uri/; bumpmaster
-rm rd_thread_id(), uneeded; bumpmaster```
>rw_bumpmaster-v220226.tar.xz.sha256sum
```cpp
33a4ac51ee14a64de0b09247db5e5a9de75b4e839cd330ee00dc9c20d994fcfa *rw_bumpmaster-v220226.tar.xz```
>backup drop
https://files.catbox.moe/00juix.7z

# 89
>>15324
Is the bumpmaster project supposed to be board integrated ai or a new imageboard api? It can be kindve confusing at times with the maidu pictures but your data structure explanation makes more sense than any college professors lectures, programming forums, or books I’ve read. Would be neat to ask bumpmaster catgirl maidus to find a post or thread.

Have you thought about getting the sumomo ai to celebrate holidays and anniversaries? Its been done before through various other apps and projects.

# 90
>>15324
Bumpmaster isn't working for me.
```cpp
page_uri:    https://alogs.space/robowaifu/catalog.json
  req made                                                                        0.4s

  Json::parse_error 
'[json.exception.parse_error.101] parse error at line 1, column 1: syntax error while parsing value - unexpected end of input; expected '[', '{', or a literal'
  caught in fstream_2_json()
```
I tried to debug it and it seems it's trying to parse the json before chkd_pull_g finishes downloading the file. Then it segfaults.
```cpp
==845051== Invalid read of size 8
==845051==    at 0x4A58268: std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> >::basic_string(std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> > const&) (in /usr/lib/x86_64-linux-gnu/libstdc++.so.6.0.29)
==845051==    by 0x12AC77: rw::curator::bumpmaster::Bumpmaster::top_bump_thrds(nlohmann::basic_json<std::map, std::vector, std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> >, bool, long, unsigned long, double, std::allocator, nlohmann::adl_serializer, std::vector<unsigned char, std::allocator<unsigned char> > > const&, int, std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> > const&, std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> > const&) (bumpmaster.cpp:247)
==845051==    by 0x111482: main (main_bumpmaster.cpp:52)
==845051==  Address 0x8 is not stack'd, malloc'd or (recently) free'd
==845051== 
==845051== 
==845051== Process terminating with default action of signal 11 (SIGSEGV)
==845051==  Access not within mapped region at address 0x8
==845051==    at 0x4A58268: std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> >::basic_string(std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> > const&) (in /usr/lib/x86_64-linux-gnu/libstdc++.so.6.0.29)
==845051==    by 0x12AC77: rw::curator::bumpmaster::Bumpmaster::top_bump_thrds(nlohmann::basic_json<std::map, std::vector, std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> >, bool, long, unsigned long, double, std::allocator, nlohmann::adl_serializer, std::vector<unsigned char, std::allocator<unsigned char> > > const&, int, std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> > const&, std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> > const&) (bumpmaster.cpp:247)
==845051==    by 0x111482: main (main_bumpmaster.cpp:52)```

# 91
>>15332
>Is the bumpmaster project supposed to be board integrated ai or a new imageboard api? 
Either are possible. But for now, the design goal for it is simply '''A)''' to be a better, more capable version of ''BUMP'', and '''B)''' to have a real-world project to get our feet wet developing within the '''''RW Foundations''''' suite of libraries. This second aspect in particular is pretty important here at the beginning of things.
>It can be kindve confusing at times with the maidu pictures
**can there __ever__ be enough anime catgrill meido pics Anon? :^)**
==SEND MORE RUNNING SHORT==
>but your data structure explanation makes more sense than any college professors lectures, programming forums, or books I’ve read.
Thanks!
>Would be neat to ask bumpmaster catgirl maidus to find a post or thread.
The plan is to integrated ''Waifusearch'' into both Foundations & Bumpmaster next. We'll see how it goes

>Have you thought about getting the sumomo ai to celebrate holidays and anniversaries? Its been done before through various other apps and projects.
Sure, PDA-like abilities are definitely a goal for our robowaifus, and it's a foundational trope for the field. Not sure exactly where our version of such capabilities will fit yet. Probably a complex from ''RW Atashi'', ''RW Meido'', and ''RW Sempai'' (possibly others) would be my initial take on the matter Anon.

>>15334
Sorry about that Anon. We'll try to reproduce the error on this end and see if we can get to the heart of the issue. Excellent feedback BTW! :^)

# 92
>>15307
Thanks Anon! I shall be **~~stealing~~** re-posting these ITT before long.

>Aye, we must work til all Anons can have their waifu meidos. 
You encourage me Kiwi. For me this is a spiritual quest as much or more than a hobbyist->professional effort with incredibly neat tech. Men around the world really __''need''__ groups like us to succeed!

# 93
>>15334
Quick update without much depth yet Anon. We were able to produce a similar effect by building the code in ''debug'' mode, rather than the specified ''release'' mode. This setting is specified in the project options in ''meson.build'' :
```cpp
# basic & default project arguments
project('rw_bumpmaster', 'cpp',
        version : 'v220226', license : 'MIT',
        default_options : [
                           'cpp_std=c++17',
                           'buildtype=release',
                           'warning_level=3',
                           'werror=true'
                          ])```

As a quick test, I'd suggest you set execute this command from the project's base directory:
```cpp
cd build && meson configure -Dbuildtype=release && cd ..```
Then rebuild & try again. Let us know your results ITT please, thanks.

We'll spend some time soon to understand the dynamics of what the compiler optimizations are doing under-the-table to order sequence timings that led to this bug. We'll patch it ofc as we do so, and will make note of that in the ''version.log'' entries.

Cheers.

# 94
>>15343
Yeah, same problem. I had the issue with the release build then rebuilt it in debug to find where it was coming from. The problem persists with different optimization levels on my machine too.

# 95
>>15347
Ah I see. Well, again we'll try to track this issue down soon. Out of curiosity have you been able to build/run any of the previous versions of drops made ITT? Also, have you been able to build BUMP or Waifusearch?

These answers might help us track down machine-dependent issues that might be involved.

Thanks again for the feedback Anon! :^)

# 96
>>15347
OK, looks like we've tracked the issue down to the most obvious one **which I neglected to check first thing** : ''the downloaded file is itself the issue''. That is, the server only sent partial data. Currently this isn't being caught by Dollnet, so we'll work on that.

In the meantime, simply deleting the files and retrying should do it. (Just use the release build, that was purely coincidental timing of getting a bad file during that test. It's unrelated).
```cpp
rm ./dolldrops/*
build/bumpmaster```

Please give that a go Anon and let us know how it goes for you.

# 97
>>15369
There weren't any partial files in dolldrops but this solved the issue. The problem occurs trying to run bumpmaster from the build folder.

# 98
>>15372
And if I make the dolldrops folder in the build folder it works fine, so I'm guessing it's not checking if that directory exists and then tries to parse a non-existent file after it fails to open it for writing, strangely before it finishes downloading. I'm a bit confused why the download wouldn't fail if it opened it for writing first or if it's opened for writing after, why it tries to parse the non-existent file before downloading finishes.

# 99
>>15372
>>15378
Glad to hear you got it working Anon. Again, thanks for the excellent feedback.

>The problem occurs trying to run bumpmaster from the build folder.
So, we've introduced some new code to address this. After the upcoming Caturday drop, you'll be able to move the executable binary out of the build/ directory and run it wherever you want to. The system will create the needed ./dolldrops/ directory for you before downloads begin.

>I'm a bit confused why the download wouldn't fail if it opened it for writing first or if it's opened for writing after, why it tries to parse the non-existent file before downloading finishes.
There are two things going on there. One is that the handle mechanism for files is short-circuiting processing when the filepath is invalid AFAICT. 

The other is that I haven't implemented sufficiently robust file checking yet. The plan is definitely to have fairly good file/data introspection later on (well before we have working robowaifus up with this system), but for now we're fairly confident about the source JSON data.

So basically it's been a bit of a timing toss-up between over-engineering things at this early stage of the systems, or moving on to usable functionality with the two preliminary utility programs. We've tended to favor the latter when it seems reasonable.

However, we'll improve basic checking soonish, to at least avoid segfaults and report the errors better.

# 100
RW Foundations Caturday drop : '''v220305 edition'''

Cute robowaifu anime catgrill meidos. I wonder if Pygmalion would approve today? :^)

So, we talked last drop about data structures for threads. But how to we use them? The first order of business is to load them up with data. We use the IB JSON files provided by the site's servers for this. There are two steps for this in the higher-level sense. First, we iterate the JSON data and pull out the thread's details (the OP's details, really) from the catalog JSON:
>bumpmaster.cpp snippets
```cpp
auto Bumpmaster_b::bump_thrd_dats(Json const& cat_json)
    -> std::vector<Thrd_data> {
  stamp("bump_thrd_dats()");

  vector<Thrd_data> res;
  res.reserve(cat_json.size());

  for (auto const& [nindx, cat_thrd] : cat_json.items()) {
    res.emplace_back(cat_thrd);  // ctors Thrd_data struct in-place
  }

  return res;
}```
This function gets called from another function actually. This one both downloads each ''thread'''s JSON, and then also loads it's 'posts' JSON into the thread structure (remember that open-ended container in this structure from last time? yeah, that one).
```cpp
auto Bumpmaster::top_bump_thrds(Json const&        cat_json,
                                const int          thrd_lim,
                                std::string const& site,
                                std::string const& board)
    -> std::vector<Thrd_data> {
  stamp("top_bump_thrds()");

  vector<Thrd_data> res;

  // store all thread's data (msg, subj, ID) from the catalog; in bump-order
  auto thrd_dats = bump_thrd_dats(cat_json);

  // assemble each thread's JSON page URI; in bump-order
  auto const thrd_uris = bump_thrd_uris(cat_json, site, board);

  for (auto t_idx{0}; t_idx < thrd_lim; ++t_idx) {  // for all Page 1 threads
    auto const thrd_uri = thrd_uris[t_idx];         // index to uri

    // pull thread's dolldrop
    cout << " page_uri:    " << thrd_uri << '\n';
    auto const thrd_json = pull_json_drop(thrd_uri);
    // DESIGN: DEBUG: address invalid JSON data here

    // copy the current thread's data into the results container
    auto& thrd_dat = thrd_dats[t_idx];
    thrd_dat.posts = thrd_posts(thrd_json);
    //
    res.push_back(thrd_dat);
  }

  return res;
}```
We're all set now. Each thread structure is now populated, and has all it's data needed from the catalog and all the post's data as well. All that's left now is to output this information to the console. We can talk about that step later, as this is more than enough code for this time!

'''We also''' began a new sub-library '''RW Cleaner''', as part of the ''RW Meido'' library. I think all of us would appreciate having our cute anime catgrill meidos clean up after us, right? :^) It will actually be a big challenge **but a fun one** to figure out these kinds of tasks for our robowaifus to perform. For example, washing dishes is literally filled with hundreds of 'judgement call' actions to perform for just this one type of chore alone.

Well, we hope you are doing well Anon. We appreciate all the hard work everyone puts in exploring these frontiers of robowaifu development and look forward to seeing your fine achievements. Keep moving forward!

Cheers.

'''==='''

>version.log
```cpp
   v.220305
---------------
-add wrt_tailme() non-member utility func; mailstop.cpp
-add preflight(), mk_dropdir() utility funcs; mailstop
-add exists_fs() utility func; rw::sys
-add 'dropdir' filepath const; dolldrop
-begin Cleaner; rw::meido```
>rw_bumpmaster-v220305.tar.xz.sha256sum
```cpp
d5fcc066e70b8e11f05fe971aecdf92919df89106732d93c1c46951192e7046d *rw_bumpmaster-v220305.tar.xz```
>backup drop
https://files.catbox.moe/1wql8r.7z

# 101
>>15372
OK, please give the new cut a try and see if it suits Anon. (>>15405)

# 102
>>15405
Your progress continues to inspire Chobitsu. Considering the boards sudden shift towards favoring Reploids, thought you may enjoy a cat grill Reploid meido to cheer you on!

# 103
>>15415
Thank you for your kind words Anon. I hope we can have real progress with the ''Sumomo's World'' project sometime this year. How would you feel about us creating an exporter for scenes into Blender? Would that be any help to you?

> thought you may enjoy a cat grill Reploid meido to cheer you on!
Indeed I do! I'd like to see her become real someday tbh. Super cute!

# 104
RW Foundations Caturday drop : '''v220312 edition'''

Anime Catgrill Meidos will surely be __wildly popular__ once they become real Anon
**and we must all diligently strive forward towards that day!! :^)**

We made changes in this drop that have some improvements to error-detection with the dolldrops process. And, for the first time, a bit of error-''correction'' too. A new function for '''RW Bumpmaster''' in this drop is ''pull_json_retry()''. It will actually make another go of it, if the dolldrop turns out invalid for some reason. 

This size-checks enhancement serves a dual-purpose; '''a''') be more efficient with bandwidth resources, and '''b''') perform general due-diligence to help avoid unintentional misuse issues. In our testing things seem to be working pretty well so far with it.

===

So, last drop we were talking about the functions that load up the structure for holding a thread's info. Namely, both it's OP data, as well as all post's data for that thread -- and into just a single object (which now can easily be passed around and processed). We load up a container-full of these things, and return ''that'' back to the caller. Now it's time to take a spin at printing all this lovely text out to the console.

'''As you recall''', we last left off at the top_bump_thrds() function. And so we pick back up with it again; but this time on the '''''other''''' side, and ''calling'' it from the Bumpmaster demo's main():

>main_bumpmaster.cpp snippet
```cpp
// load a new container with catalog's Page 1 threads + posts; in bump-order
auto const top_thrds = bump.top_bump_thrds(cat_json, thrd_lim, site, board);

// cycle the top threads (& print their data)
size_t t_idx{0};                   //
for (auto const& t : top_thrds) {  //
  puts("\n\n     --=^=--\n");

  cout << "     Bump  " << ++t_idx                        // prt thrd's data
       << "\n =======================================\n"  //
       << setw(8) << setfill(' ') << t.id << "  :  "      //
       << t.subj << "\n\n' " << t.msg << " '\n";          //

  // calc starting post's thread index
  auto const sz = static_cast<int>(t.posts.size());  // cast avoids overflow
  auto const start{sz - post_lim};                   // for this subtraction

  // cycle the latest posts (& print their data)
  for (auto p_idx{(start >= 0 ? start : 0)};  // ensure we have valid index,
       p_idx < sz; ++p_idx) {                 // (as sz might be < post_lim)

    auto const& p = t.posts[p_idx];  // index to post,
    cout << '\n'                     // prt post's data
         << setw(33) << setfill(' ') << "r " << (p_idx + 1)
         << "\n  ------------------------------------\n"
         << setw(8) << setfill(' ') << p.id << "  :  " << p.date << "\n' "
         << p.msg << " '\n";
  }
}```
This code takes that container object (we named ''top_thrds'' since it's about the Page One threads) and traverses each element in it, one-by-one, via that C++ range-for loop (each of these elements happen to be one of those ''Thread Structures'' we talked about). We name these simply as ''t'' (for thread). Such a terse name is OK for this context, since it's a small scope inside the loop, and it's also a good symmetry with ''p'' (for post, which we'll name later). 

First thing we do is print out the thread struct's first 3 fields, ''id, subj, & msg'' along with a few little formatting tweaks. Next, we calculate the starting printout-post's index inside the thread. We do this b/c we just want to print the ''latest'' 5 posts to the terminal, not all of them. You might recognize that this is pretty much how a standard IB index page works. 

Anyway, to get the correct starting index for post printouts, we just subtract the post-limit count (5), from '''size()''' of the ''posts'' container field in the thread struct (that 'open-ended' one). Remember that in C and most other programming languages, array indices start at ''0''. So, say there were 20 posts altogether, we'd begin printouts with index 15 (post #16), then index 16 (post #17), and so on to index 19 (post #20).

Finally, we just print out the 5 post's 3 fields, ''id, date, & msg'', again with some little formatting tweaks. That's it, we're done with that thread printout. Lather, rinse, repeat for the next 9 threads. Then repeat the whole cycle for all the board listed in this 'open-ended' container of URI strings:

```cpp
// container of various IB URI strings
// -try other boards you like, Anon!  :^)
// clang-format off
vector<string> const board_uris{
    // NOTE: currently supporting only Lynxchan sites (for v220312)

    "https://alogs.space/robowaifu/",
    "https://alogs.space/pdfs/",
    "https://prolikewoah.com/geimu/",
    "https://late.city/late/",
    "https://anon.cafe/christian/",

};```

Congrats Anon! Over the past three drops, we've created a handy multi-board offline text reader for IBs. It's both lightweight on resources and ''fast''. BTW, you may need to increase your terminal's output buffer size, since this could easily grow to thousands of lines of text if you add lots of boards into your list. Later we'll add what ''BUMP'' does to allow other, non-Lynxchan boards as well.

Well we hope you're getting lots of bright ideas and clever robowaifu-making insights, and are moving forward day-by-day towards your goals with her. '''''Keep your dreams alive Anon!''''' :^)

Cheers.

'''==='''

>version.log
```cpp
   v.220312
---------------
-check Json validity on pull_json_retry() calls; bumpmaster
-add pull_json_retry(); bumpmaster
-mv to tuple<bool, Json> ret, pull_json_drop(); bumpmaster
-add do_catalog() member funcs; bumpmaster, dolldrop
-begin checking dolldrop sizes
    chkd_pull_g(); dolldrop
    pull_json_drop(); bumpmaster
-add sz_match(); bumpmaster
-add chk_dropsizes(); mailstop_util
-add set_sz(), get_sz() wrappers; mailstop_util
-add 'sz' field, Dropdata; mailstop_util
-mv to fs::path filenames; general```
>rw_bumpmaster-v220312.tar.xz.sha256sum
```cpp
57018697c25c6f137505e71aed2fe4f7d88169e8e1fa02fc487713ab6316cee6 *rw_bumpmaster-v220312.tar.xz```
>backup drop
https://files.catbox.moe/9rrvst.7z

# 105
>>15448
I'm still learning Blender but I think it's a good idea.
>>15514
Nice update Chobitsu!

# 106
>>15516
>but I think it's a good idea.
I do too. While we can probably manage a reasonable degree of good outcome with enough effort put into the ''RW Action!'' set of libraries, the simple fact is that Blender is over 25 years of focused effort now, and also has an annual budget of millions. It's just good sense IMO.

>Nice update Chobitsu!
Thanks! Yes, I feel like we have reached up and over and have scaled onto another plateau with this one. Feels good. Hopefully, we'll be able to move on from Bumpmaster after not too many more Caturday drops tbh.

Cheers.

# 107
RW Foundations Caturday drop : '''v220319 edition'''

Can we all just agree that Catgrill Meidos make the best servers!?

This spin we did a little cleanup on the console's output text display, and gave error-detection on the curl library's connections a bit of a think. We also began a new sub-library '''RW Cooker''' for the rw::meido namespace. ''Robowaifus doing our Cooking and Cleaning'' for us goes together __right well__ don't you think Anon? :^)

===

So, we have a new function in ''RW Bumpmaster'' for this drop '''fmt_msg()'''. Till now, we've simply let the terminal handle text wrapping (with predictable results.) If you look at a terminal all day this kind of thing is just par for the course and no big deal; you get used to it. But even so, it still would be nice to have slightly better formatted output. Therefore:

>bumpmaster.cpp snippet
```cpp
auto Bumpmaster_b::fmt_msg(std::string const& msg) -> std::string {
  stringstream iss{msg}, oss{};

  for (string line; getline(iss, line);) {  // read lines in one at a time
                                            //
    if (line.length() > msg_width_lim) {    // this line needs linebreaks
      // transfer line string to a sstream
      stringstream liness{line};
      line.clear();

      // parse sstream into multi-lines
      //
      string word{}, curr_line{};
      while (liness >> word) {  // one whitespace-delim'd word at a time

        if (curr_line.length() >= msg_width_lim) {  // we have a linefull, save
          line += (curr_line + '\n');
          curr_line.clear();
        }

        curr_line += (word + ' ');
      }

      curr_line = curr_line.substr(0, curr_line.size() - 1);  // rm final space
      line += curr_line;  // final line pickup for the multi-line
    }

    oss << (line + '\n');
  }

  // rm final newline
  auto res = oss.str();
  res      = res.substr(0, res.size() - 1);

  return res;
}```
This code first reads the JSON source message text passed in by the caller, then line-by-line reassembles it for the function's output. 'Why do this' you ask Anon? Good question! :^) For any lines that are under the width limit, they are just appended right back over to the result string. But for the lines that are ''over'' the width, they get some attention to wrap them around to fit.

First we convert that line over to a stringstream ''liness''. Now, C++'s '''std::stringstream''' 's have a nice overload on the 'get from' operator ''>>'' **thanks for the name Bjarne!** such that it will parse on any white space when the target type is a '''std::string'''. It will also return a '''bool''' indicating if any content was in fact parsed out. Putting all that together allows us to write this rather elegant statement: ''while (liness >> word) { ... }''. Hard to get much cleaner than that tbh.

We check if the working scratch string ''curr_line'' is at or past the width limit, and save it out if so then reset it for the next go-round. Otherwise, we append the next ''word'' onto it, adding that space char back in along the way as well. And so it goes; word-by-word, line-by-line, till the entire input message string is reassembled into a new output message string. Seems tedious? Indeed it might be for you or me, but the strings library doesn't care lol. 

Our only concern as engineers is correctness & efficiency. Since these stringstream overloads are based on STL template classes, our optimizing compilers will munge together all these operations down into a quite efficient set of machine instructions. And a ''very'' nice thing about the C++ strings library -- and ''particularly'' it's streams libraries -- is that they __just werk__. That is, they have sane defaults by, well, ''default''. Always use std::string first and foremost for character array work when allowable on your system's platform. **You can thank me later Anon.**

BTW, that ''msg_width_lim'' variable is a const for the class (set at '''100''' currently, but you can change it to w/e you want.)
>bumpmaster.hpp snippet
```cpp
inline const unsigned msg_width_lim{100};```

OK, so we have this handy new formatting function and now here's what the post data printout statement looks like:
>main_bumpmaster.cpp snippet
```cpp
cout << '\n'
     << setw(33) << setfill(' ')  // prt posts data
     << "r " << (p_idx + 1)
     << "\n  ------------------------------------\n"
     << setw(8) << setfill(' ') << p.id << "  :  " << p.date << "\n' "
     << bump.fmt_msg(p.msg) << " '\n";```
You might notice that new function call wrapping the ''p.msg'' 's output. Yep, that's the one.

Well, it looks like some big project things are afoot here on /robowaifu/, lads. I hope you're all well-secured & ready for the ride! :^)

Cheers.

'''==='''

>version.log
```cpp
   v.220319
---------------
-enable all try/catch blocks, 'try_X()' funcs; mailstop
-add disp_err() utility func; dollnet
-add msg_width_lim const var; bumpmaster
-add fmt_msg(); bumpmaster
-begin Cooker; rw::meido```
>rw_bumpmaster-v220319.tar.xz.sha256sum
```cpp
0b3cb26b114d967162b75588b926a6f40daf384d3d39f01cc6a26e3d63245804 *rw_bumpmaster-v220319.tar.xz```
>backup drop
https://files.catbox.moe/p1qnqj.7z

# 108
>>15516
BTW I meant to thank you earlier for that excellent Chii Anon, but I just forgot. Thanks! :^)

# 109
>>15658

An exporter plugin for blender would be very helpful since most robotics software does have some kind of model simulation feature these days for testing programming instructions. 

You would have to be capable of automatically generating a target armature for the robot model you are testing with the program.

# 110
>>15656
>Can we all just agree that Catgrill Meidos make the best servers!?

I have to agree!
I like how you're handling strings Chobitsu, I don't really get C++ but, it seems like it'll help with legibility of retreived text. Thanks for your detailed write up. Thanks for your continued work.

# 111
>>15660
>An exporter plugin for blender would be very helpful since most robotics software does have some kind of model simulation feature these days for testing programming instructions. 
It's a great platform today for everything 3D basically. Surely it can be a help for things like our project's visualizations etc.

>You would have to be capable of automatically generating a target armature for the robot model you are testing with the program.
It's actually rather more complex tbh. 'Automatic weight-painting' would also be needed as well, and some form of rigging system too.

That is if an Anon was going for an entirely automated, turn-key exporter system. Something you could sell for a few thousand a pop, for example. We're going for something much simpler to start off with ofc.

>>15661
>I have to agree!
Heh. I like the fact they give a subtle nod to ''Chii'' in fact, being a cute **animu cat**grill. :^)
>

>I don't really get C++
Well, as we mentioned IIT's OP:
< "...I'll use this thread as a devblog and perhaps also a bit of a debate and training forum for the many issues we all encounter, and how a cute little fairybot/moebot pair can help us all solve a few of them."
I'm happy (eager even) to help Anons learn the language. AFAICT, this is a critical-skills issue for us all, and we shouldn't allow just one anon to be skilled in it. Many of us should be, if possible. In this case I think it's ''definitely'' possible. 

If you want to learn the language itself, then I simply can't recommend a better resource than ''Stroustrup's'' college freshman textbook ''PPP2''. There literally isn't a better programming leanring textbook for the serious student in existence anywhere (regardless of language) (>>4895)

If you actually care to learn, then I myself am probably a good resource. I can explain in as much detail as necessary probably just about anything with the language you might be wondering about. We can start simply by going through every.single.thing. for the code contained in this post (>>15656) until you (or anyone else who cares to ask for that matter) understand it clearly.

For example, just to start at the beginning, is there anything in this line of code that you're even a little unclear about?
```cpp
auto Bumpmaster_b::fmt_msg(std::string const& msg) -> std::string { ... }```
If so, just ask. 

Remember, we all need to try and find ways to encourage others to step up to be able to take over our roles at the drop of a hat. We owe that as leaders to the community at large.

Cheers, Anons.

# 112
Catgrills. Meidos. Delivery trucks. Imagine the possibilities Anon. :^)
==Please send catgrill meido pics Anon, running short!== :^)

Starting with this drop we'll be supporting multiple projects simultaneously, therefore it seems misguided to keep calling these drops 'Bumpmaster WIP'. Accordingly, we're moving to the generic ''Caturday drop'' as the subject, and the super-project's name will now simply be ''RW Foundations'''. An important benefit of rolling out the projects together like this is that it significantly decreases the likelihood of any library incompatibilities across them. It's not perfect, but it'll do for now.

'''RW Pandora''' So, the big splash for this drop is the addition of RW Pandora to the lineup. For now it's simply the basic skeleton, but it's ''already'' the straight beneficiary of all the work that has gone before and is immediately up to speed with the current stable, with full access to everything available so far.

Here's the program's current diagnostic output on my box:
```cpp
build/pandora

 entering main()...

 Pandora checks out A-OK!
                                 -                  Pandora.0    	addr:    0x7ffd7f1bd328

              pandora.animeyes() -         arigato_animeyes.1    	addr:    0x562e7861b440
                pandora.atashi() -           arigato_atashi.2    	addr:    0x562e7861b5d0
                 pandora.bones() -            arigato_bones.3    	addr:    0x562e7861b730
               pandora.curator() -          arigato_curator.4    	addr:    0x562e7861b860
             pandora.dollhouse() -        arigato_dollhouse.5    	addr:    0x562e7861b9e0
               pandora.electro() -          arigato_electro.6    	addr:    0x562e7861bb50
                  pandora.face() -             arigato_face.7    	addr:    0x562e7861bc80
                 pandora.gears() -            arigato_gears.8    	addr:    0x562e7861bdb0
                  pandora.hand() -             arigato_hand.9    	addr:    0x562e7861bf70
               pandora.hearsay() -          arigato_hearsay.10    	addr:    0x562e7861c0a0
                 pandora.meido() -            arigato_meido.11    	addr:    0x562e7861c1d0
                 pandora.shell() -            arigato_shell.12    	addr:    0x562e7861c300

             pandora.graphicom() -        pandora_graphicom.13    	addr:    0x562e7861c5c0

 ...leaving main()```
This is exactly as predicted for this stage of development, so yep good to go. 

===

For anons who may be wondering where these things come from, let's dip into C++ ''class hierarchies'' a bit **again, be patient if you already know this stuff**. RW Pandora is an '''RW Arigato'''-class robowaifu, so it's part of that namespace and directly inherits from that class too:
>pandora.hpp snippet
```cpp
namespace rw::arigato {

class Pandora_b : public Arigato {
 public:
  Pandora_b();                                    // default ctor
  explicit Pandora_b(std::string const& handle);  // tag-parm'd ctor
};
...

}  // namespace rw::arigato```
That ': public Arigato' bit is what does the trick. Here's a portion of RW Arigato's code:
>arigato.hpp snippet
```cpp
class Arigato : public Arigato_b {
 public:
...
  inline auto animeyes() const -> Animeyes& { return animeyes_; }
  inline auto atashi() const -> Atashi& { return atashi_; }
  inline auto bones() const -> Bones& { return bones_; }
  inline auto curator() const -> Curator& { return curator_; }
  inline auto dollhouse() const -> Dollhouse& { return dollhouse_; }
  inline auto electro() const -> Electro& { return electro_; }
  inline auto face() const -> Face& { return face_; }
  inline auto gears() const -> Gears& { return gears_; }
  inline auto hand() const -> Hand& { return hand_; }
  inline auto hearsay() const -> Hearsay& { return hearsay_; }
  inline auto meido() const -> Meido& { return meido_; }
  inline auto shell() const -> Shell& { return shell_; }
...
};```
Hopefully you spot the similarity of these member field's names for RW Arigato, to the diagnostic above for RW Pandora. Yep, that's where they all come from; ''pandora '''inherits''' them from arigato''. To pickup that ''RW Graphicom'' member, here's the declaration in the derived RW Pandora code:
```cpp
class Pandora : public Pandora_b {
 public:
...
  inline auto graphicom() const -> Graphicom& { return graphicom_; }
...
};```
That's it. Anon, that accounts for each item that currently is part of RW Pandora's declaration. This will naturally grow as development begins in earnest for it. Please explore the codebase, and ask any questions about things ITT, we'll be happy to respond.

'''Notice:''' ''We'll be putting Caturday drops on hold through the month of April.'' All things being equal, the plan is to pick everything back up on May 7th, and we'll dive back into things full-charge with some code cleanups and reorganizations for ''RW Bumpmaster'' as we press in towards our first GUI code for the Foundations.

I hope things are going well for you Anon. Stay encouraged, and keep your eyes on the prize. We'll all get there, just keep moving forward. :^)

Cheers.

'''==='''

>version.log
```cpp
   v.220326
---------------
-pandora gets member; graphicom
-add 'pandora' decl/defn files; rw::arigato
-add pandora build configs; meson.build
-add 'main_pandora.cpp'
-begin Pandora demo project```
>rw_foundations-v220326.tar.xz.sha256sum
```cpp
8441a9dc9a67406767cf504a496d5a090e8ecd04b0c45495c14e223b85f152c0 *rw_foundations-v220326.tar.xz```
>backup drop
https://files.catbox.moe/smc6ey.7z

# 113
Catgrills and Meidos and /comfy/ warm cabins **🎶 These are a few of my favorite things 🎶** :^)

Well well, here we are, and it turns out that May has finally arrived! Hope you had a good April Anon.

So, we've been doing a few demo tests here and there over the course of the overarching project so far. Mostly these are meant as 'throwaways'; little design sketches meant to explore different coding concepts. The project demo work we left off with a month ago here was thus. However turns out it's been such a regular part of our daily-driver routine since, that we decided just to keep it!

'''Announcing''' that ''RW Pageone'' will now be a permanent part of the ''RW Foundations'' stable of projects. ''RW Bumpmaster'' is still very much on the table, but it's a more expansive project with fairly different goals. Pageone has proven handy as a low-impact way simply to read the text of different IBs. Crude as it is, little-by-little it's gotten better with time. Maybe our robowaifus will also be reading Page 1's along with us some day soon Anon!

The intention is the project will remain as a terminal-only application. In fact it's likely to change only little outwardly from it's current incarnation this drop (with the exception of better error-handling on bad connections/missing data). A user-editable 'IB URI listing' text input file should also be available at some point (hopefully soon). Additionally, once Bumpmaster's ''IB JSON field abstractions'' are on par with '''BUMP''''s (basically allowing us to archive any major IB software) the plan is to also add that into Pageone as well.

We hope you'll find this little utility useful too Anon.

===

The biggest change this drop is we are finally saving out the various JSON dolldrops (catalogs + threads) into their own, named, sub-directories within the ''./dolldrops/'' folder. This is better organized, and will also make ''RW Waifusearch'' integration simpler when it's time comes along too.

Also, we pieced together what we think is a reasonably-functional mechanism to manage the networking library '''curl''''s (so-called) 'easy objects'; for connection-reuse out to any given IB server. This should make the load on remote servers somewhat less, and the bandwidth usage slightly more efficient for both parties.
>"But, how did you manage this?"
you might ask? Well stay tuned Anon. :^)

So, the 'software star' of the day for this particular Caturday drop is the C++ standard library container '''std::map<>''' .
https://en.cppreference.com/w/cpp/container/map

''map'' 's provide access to sorted, key:value pairs (kind of like JSON fields). You can use any type for the key, but strings generally are best. The value field can also be any type at all; and in this case we're interested in storing an associated '''curl''' easy object so that we can get connection-reuse across different dolldrop/dollnet pull requests.

But we need a way to locate it repeatedly, and that's where the string comes in: it's simply the ''IB's site name itself'' (eg, '''"alogs.space"'''), and works quite well as a map key. Therefore, within the base class ''Dolldrop_b'' we've added a map-type member field:
>dolldrop.hpp snippet
```cpp
map<string, curl_easy> site_conns_;```
Notice the two items in those angle brackets: ''string'', and ''curl_easy'' ? The string type is the '''key''', and the curl_easy type is the '''value''' for this specific map.

Since we ''always'' know the site's name for any dolldrop pull, we just use ''it'' in the search and get back a reference to the stored curl connection itself. We created a simple function that goes and finds that curl object inside the map (or makes a new one if needed) and returns it:

>dolldrop.cpp snippet
```cpp
auto Dolldrop::get_ib_curl(std::string const& uri) -> curl_easy {
  auto const& [site_nm, board_nm] = parse_ib_uri(uri);

  // obtain the previous curl_easy obj for this site if found, else create new
  curl_easy conn;
  try {
    conn = site_conns_.at(site_nm);

  } catch (out_of_range const& e) {
    conn                 = get_curl();
    site_conns_[site_nm] = conn;
  }

  return conn;
}```
This code first parses out the site name to be used for the map lookup. The '''.at()''' member function is range-checked (safety, etc.) and throws if the element isn't in the map. We use this approach for the first phase of the lookup, b/c we don't want to actually instantiate a new curl_easy object until we need to.

If the element isn't found inside the map, then a new one is created, and the '''[]''' member operator is used to insert it into the map (for the next time around). The function then returns the retrieved/created curl_easy object specified to that URI. That's all there is to it, and it's handy to use from wherever needed inside Dolldrop.

Well, we hope you are making steady progress towards your robowaifu goals Anon. Keep the faith **and work your butt off!** Together, we'll all make it. :^)

Cheers.

'''==='''

>version.log
```cpp
   v.220507
---------------
-add curl connection-specified pull call-chains; dolldrop/dollnet
-add get_curl() call-chain; dolldrop/dollnet
-begin mv to curl connection reuse out to IB servers; dolldrop/dollnet
-add 'droppath'-specified dolldrop pull call-chains; dolldrop/dollnet
-add preflight_boards(); bumpmaster
-begin mv to named dolldrops within site/board directories; bumpmaster
-migrate mailstop features over to dolldrop; dolldrop
-migrate mailstop_util features over to dolldrop_util; dolldrop
-begin mv of Mailstop elsewhere and out of rw::dollhouse namespace
-add 'dolldrop_util' decl/defn files; dolldrop
-add complement of dolldrop wrappers; bumpmaster
-mv parse_ib_uri() over; rw::util
-mv to fs::path parms, rd_json_file(), wrt_json_file(); rw::json
-tmp clear main_bumpmaster.cpp code; using pageone as it's current dev focus
-add 'main_pageone.cpp'
-add pageone build configs; meson.build
-begin Pageone demo project```
>rw_foundations-v220507.tar.xz.sha256sum
```cpp
72dc81265529fe19e229e07baec4f3c64707fc41aaa92404eeb01c3e67036220 *rw_foundations-v220507.tar.xz```
>backup drop
https://files.catbox.moe/siytza.7z

# 114
>>16119
Having waifus reading Page 1's with us sounds like a nice idea! The map function is pretty cool, I like how you're using it.

# 115
>>16119
Kek, I had too many chars in my droppost to even add my traditional edit comment **__exactly__ 6144 heh :^)**, so I'll do it here instead.

>===
-''minor fmt edit''
-''minor tech edit''

>>16122
>pic
LOL. '''How did you get into my secret lab Anon!?''' **:^)**

>Having waifus reading Page 1's with us sounds like a nice idea! 
Yes, it will be a glorious day when we can all regularly shitpost along with our waifus Kywy. Onward!

>The map function is pretty cool, I like how you're using it.
Thanks! I try to consolidate functional abstraction into simple little modules when I can. Makes maintenance much easier later on. The C++ map 's flow-control approach isn't that great IMHO, but I understand why it's being done that way. OTOH, it's efficiency as a logarithmic ''Red-Black'' tree is nearly optimal. Very close to the metal.
>tl;dr
You play the hand you're dealt. And in this case (both with C++ and with map<>) it's well worth it!

>>16130
>In the readme, say what programs are included in the repo and what they do.
Great idea ChartTard! I'll plan to add that in as a permanent part of the readme's during the next Caturday drop. 

Also, welcome aboard Anon! :^)

>===
-''add missing quote''
-''fmt edit''
-''add add'l cmnt cmnt''

# 116
>>16139
I don't do much C++ programming so I haven't looked too much at RW Foundations beyond using Bumpmaster to archive the board but I look forward to seeing Sumomo's World. I dabbled before with making a 2D visual waifu in Godot >>9025 which would be pretty easy to reimplement in C++ with raylib-cpp. Raylib has much better support for skeletal animations now than it did a year ago so you can animate stuff in Blender, export and play it. Raylib can also be compiled to WebAssembly for webpage waifus. There's also Live2D but their library is closed source and their editor is software as a service that doesn't support Linux.

I plan to port my TTS systems to C later this year which could be plugged into Sumomo and of course GPT-2 is in the works if you're interested in playing with that. I'm not really sure how else I could contribute to the project. Possibly next year I plan to port RoBERTa too and that could be plugged into Waifusearch so searching for something like 'chatbot' would also bring up similar posts talking about 'conversational AI' and 'natural language processing'.

Something else I use a lot are WebSockets to communicate between the web browser, Python, Godot and other applications. It would be desirable to have a library in RW Foundations for easily sending and receiving various types of data across the net and between programs. My visual waifu for example connects to three different WebSocket servers, one for text generation, one for TTS and another for translation using selenium to access DeepL. It makes it much easier to test different code and models without having to unnecessarily reload GBs of data each time I make a change and the visual waifu continues to work even while any of these functions go down.

# 117
I threw this together from example code over a couple days.

It combines python TTS, Speech recognition and Chatbot libraries into a talking, speech-activated chatbot.
It's not very good out of the box (Sphinx is pretty jank and I haven't tried training the chatbot), but it "works" with minimal effort and we may be able to improve upon it.

# 118
>'''Hopefully something by next week edition'''.

So, we are taking a hard look at dropping one of the dependencies for ''RW Foundations''. Namely the curlcpp library. While the library is pretty nice, it's a bit over-sized for our simple needs in Dollnet/Dolldrop currently. During the effort to improve our error-handling/correction it became apparent that often just dropping straight down to the curl C itself help get around some limitations with curlcpp. This realization naturally led on to 
>"Well, can't we create our own wrapper for continued/improved safety+security using curl?"

Accordingly, we're taking a serious look at doing just that. I'd estimate we're ~1/2 of the way through that, so probably not too unlikely we could have something by next Caturday, stay tuned.

'''==='''

Also, we'll probably drop back to a 2-week(ish) cycle for Caturday drops. This will help with my own personal schedule, and is more likely to result in better code in general I think.

# 119
>>16194
>raylib-cpp
Thanks! I had looked into it a good while back, but it didn't seem right for me then. I'll have a look at the newer versions. From my initial glance at the github, it looks to be quite nice.

>I plan to port my TTS systems to C later this year which could be plugged into Sumomo and of course GPT-2 is in the works if you're interested in playing with that.
Absolutely. We certainly will need both these needs with the ''Sumomo's World!'' demo project, and I can't think of systems I'd rather use.

>I'm not really sure how else I could contribute to the project.
I'm just glad you're sharing your hard work with the /robowaifu/ community itself, RobowaifuDev. If you'll allow us to simply integrate your systems into our own, then that would be a tremendous help. We'll follow your lead on this, since our licenses differ so significantly. As I've made very obvious to everyone on the board, I mean to support small-businesses trying to succeed at creating waifus. I see the permissive license as the literal key to success for these thousands of private Anons.

>Possibly next year I plan to port RoBERTa too
Neat. That certainly would be a big improvement over ''Waifusearch'' as it stands.

>WebSocket servers
I can't make any predictions on the timeframe, but we've decided to look at a prototype effort using WebSockets. It will need to be provably safe/secure according to the offlined, sneaker-netted basics in this area we're already working towards. But if it does prove so, then even the IPCnet effort may benefit in some ways from it.

Very nice to have you stop by the thread Anon! :^)

Cheers.

# 120
>>16230
Thanks Ricardo! As we discussed elsewhere, having a simple-to-use Python API for our robowaifus is a great idea. I'll make the attempt sometime soonish to build your project and see if I can get it working.

Cheers.

# 121
>>16230
>>16238
I used pipenv to get the virtual environment for this set up, here's the pipfile (specifies dependencies)

# 122
>>16248
Thanks! That's exactly the kind of thing a relative neophyte with Python needs to manage the process Anon. I hope to have a machine ready to use sometime in the next week or so. Cheers.

# 123
>Python also has a serial library
https://devtut.github.io/python/python-serial-communication-pyserial.html#initialize-serial-device

We could use this to send commands from a PC to an arduino. That way, we won't have to use a raspberry pi for GPIO.

# 124
>>16296
Yep. Particularly during these early prototyping phase years, using a USB-based comms buss network might prove feasible, as another Anon mentioned.

Long-term however, we'll need something more secure. The issue is that USB hardware typically performs DMA buss-mastering. Ostensibly, this is to optimize the efficiency of the data transfers, and in particular the latency.

However, ''any'' component that does DMA represent a pretty severe potential security and stability threat. The reason is obvious from the very acronym itself:
>'''D'''irect '''M'''emory '''A'''ccess
To wit: the device can conceivably take over unauthorized sections of memory, roughly by design.

But thanks for the suggestion Anon, I think it's a good one to try and reduce component counts and costs! :^)

>===
-''add the single word 'potential'''
-''add greeting''

# 125
Catgrills & Meidos, first choice of refinement and taste everywhere!  :^)

Well good news Anon, our mini-project to eliminate the ''curlcpp'' library dependency for ''RW Foundations'' is proceeding apace. For the ''RW Pageone'' project, we were able to rm its necessity. We're leaving the curlcpp lib in place for now, but this should be the last version to include it.

In addition we also managed to get the basics of parallel downloads using a single thread kickstarted and working for this drop too. So-called '''curl-multi''' was always on the agenda, but we've begun working with it at last. If you ever use any explicit download tools regularly, then you know how important simultaneous connections can be for efficiency's sake. And curl can actually scale ''far'' beyond our likely-scenario needs for our robowaifu's ''RW Dollhouse'' systems, etc. But for now it's rather a nice improvement for this Caturday's drop. I think you'll find that Pageone is pretty snappy now. :^)

===

So, one of the nice things about using C is that you're quite close to the hardware. OTOH, one of the ''bad'' things about using C is that you're quite close to the hardware. **:^)** Plainly, the benefits outweigh the detriments here, but you have to pay close attention to a) what you're actually doing **not what you ''think'' you are**, and b) stuff you're not even thinking about as a developer that may be involved some way or other. I like the language a lot, though it can be very tricky. I'm not particularly-skilled as a C dev tbh. In fact I much prefer C++; we can still get ~~95%+~~75%+ of the general efficiency of C, and don't have to give up on the many benefits of abstraction the language affords us. Some circumstances even allow C++ code to run significantly faster than similar C code -- particularly if developer time is taken into the cost consideration.

One of the initial hurdles a beginning programmer faces with C is understanding that so-called 'variables' are in fact just fixed blocks of sequential RAM addresses. That's it. No special sekrit sauce Anon. Just you and those 8 bits of 1's & 0's **or __billions__ of 1's & 0's, as the case may be**. They don't move around. They don't know that they are in essence nothing more than just a glorified set of lightbulbs & switches. '''OTOH''' this also means you can do some pretty weird and cool things that you might not expect to be able to if you learned another programming language first. 

Now the close relationship between the two languages, and in particular Bjarne Stroustrup's adamant insistence that C++ remain backwards compatible with C (at some cost), allows us to write code like this:

>dolldrop.cpp snippet
```cpp
/** Append a @c curl -specified memory block to a target string
 *
 * Writes an array of @a num_elems count of elements, each one @a elem_sz in
 * size, from the block of memory pointed to by @a addr, out to the current
 * position in the @a o_strm stream (the end of a @c std::string, in this case).
 *
 * @param[in] addr pointer to memory array of elements to be written out
 * @param[in] elem_sz size in bytes of each element
 * @param[in] num_elems number of elements
 * @param[out] o_strm pointer to output stream
 * @return number of bytes written
 * @note: this is intended as a callback function for a curl handle's use
 */
auto wrt_str_cb(Address const      addr,
                size_t const       elem_sz,
                size_t const       num_elems,
                std::string* const o_strm) -> size_t {  //

  auto const mem_blk_sz{elem_sz * num_elems};

  try {
    o_strm->append(static_cast<const char*>(addr), mem_blk_sz);

  } catch (exception const&) {
    // -"If an exception is thrown for any reason, this function has no effect
    //  (strong exception guarantee). (since C++11)"
    return 0;
  }

  return mem_blk_sz;

  // https://en.cppreference.com/w/cpp/string/basic_string/append
}```
I imagine a Pure C Anon shudders in utter disgust at such horrors. C++ strings! Lol please bear with us. :^) So w/o going too much into it, one of those 'weird' things you can do is write data incrementally out to a std::string variable, rather than a FILE stream. Pointers are literally the greatest invention of nerds. Remember those immovable 8 bits? Yep, '''''cheap pointer tricks''''' are ways to have fun and profit using nothing but bits.

curl 'chunks' up data, and then calls an attached, user-definable, so-called 'callback' periodically to let you do w/e you want with that data. In this case, we're storing it into a string (which just so happens to be inside one of those 'open-ended containers' [std::vector] we spoke of earlier ITT). This allows us to read out the data from curl networking facility with safety and security that's rather more tricky when using straight C. ''__Particularly__'' with exceptional states (see that try/catch block?)

Anyway, that's enough for now. But this code is very much a part of our parallel downloads improvements for this drop. Please have a look at the actual codebase itself; just ask if you want to know more.

Well, I hope you are doing well Anon. Keep pressing in towards the prize. Together we're all gonna make it Anon! :^)

Until next time then, cheers.

'''==='''

>version.log
```cpp
   v.220521
---------------
-optimize thread reads via 'pulled cats' find_if() filter; pageone, bumpmaster
-add 'chk_thrds' flag, to optimize on thread checks; pageone, bumpmaster
-add wrt_str_cb(), cfg_hdr_hdl() utility funcs; dolldrop
-add pull_hdrs_multi_g() member func; dolldrop
-add chk_hdrs() member funcs call-chain; dolldrop
-add chk_pull_cats_sh() member func; bumpmaster
-add top_bump_thrds_sh() member func; bumpmaster
-begin mv to parallel curl transfers, w/ partial error corrections
-begin mv to rm 'curlcpp' library dependency
-add 'show_prog' flag parm, various; dolldrop/dollnet
-disable dolldrop() public member func, external access unneeded; bumpmaster```
>rw_foundations-v220521.tar.xz.sha256sum
```cpp
65105c5804b89edd01bf92aaa0c7865c480aec4c1cf415b5637c335d0dba8b55 *rw_foundations-v220521.tar.xz```
>backup drop
https://files.catbox.moe/mugvk3.7z

# 126
>>16329
Thanks Chobitsu, your work continues to be great!

# 127
>>16329

>So, one of the nice things about using C is that you're quite close to the hardware. OTOH, one of the bad things about using C is that you're quite close to the hardware. :^) Plainly, the benefits outweigh the detriments here,

That's because C was made as an alternative to machine code, which was the language that directly ran most ancient machines before the dawn of the personal computer. It looks like matrix code to any human being and C is far less scary overall. Its supposedly not uncommon to have some programmers mix C and C++ or C++ and C#.

I was still not any closer to finding out what the hell any of this is supposed to do from the thread itself and found a way around the whole "orbital space docking procedure" as described and narrated in the readme. **I am just putting a sense of humor to my frustration here :)**

Extracts tar.gz:
https://extract.me/

If you want to run it as intended and get the code to run, THEN follow the readme he includes in every drop. It irritated me to no end how they put so much effort towards these but make them impossible to even look at without going through so many extra hoops.

