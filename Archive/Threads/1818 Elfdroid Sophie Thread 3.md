# 1
New video of Sophie is now up:



https://www.youtube.com/watch?v=XOGrdHn7wBU



Finally got her head working in a reproducible manner.

I had completely broken about seven of her previous micro-servos. 



But the burnt-out ones weren't the big problem - I just connect suspect servos my Arduino UNO and if my control servo can run the 'Sweep' sketch but the suspect servo cannot, I know it's dead and in the bin it goes. 



However, one servo was damaged but still working - except it caused some kind of feedback that made all other micro servos connected to the same circuit go haywire - even brand new ones. Luckily the faulty servo in question was old and had spraypaint on it, so I could tell it apart from the others. But that was very confusing - at first I thought it might be related to the small magnets that hold her faceplate on, but this is not the case. Rogue servos are definitely something to watch out for in future. 



Anyway, now that I have measurable, standardised voltage going into all of the micro servos, I'd like to upgrade her neck again. She can actually shake her head (but not in the above video as it is addressed straight-to-camera), but she still cannot nod her head as it weighs too much and the neck servo overheats rapidly. Heads are relatively heavy things (especially with long hair).



The breakthrough with Sophie has been splitting her up into separate subsystems and separate circuits, then focusing on only ONE subsystem/circuit - in my case her head. 



For a beginner like me, it was just too confusing and labour intensive to attempt programming her head, speech, neck, arms and hands all simultaneously. When errors occured I was having a real hard time pinning down which motors were affected, how badly they were affected and why. Having to tear down one large, complex system is waaaay harder than troubleshooting something far smaller. So focusing only on her head solved this problem.



Also her head is the most important subsystem (because headpats) and is highly transportable. I just have to connect her to a laptop now instead of having her chained to my bulky tower PC.

# 2
Bravo

**goes in all fields! :^)**

# 3
>>15237

Ty, ty Chobitsu.

Now I gotta write down all the connections and

sort out her wiring again. It's still an awful mess and could do with properly cropping and mounting to a board. So I can move her about more easily without worrying so much about trailing cables, yanking out wires and bending pins.

# 4
>pic related
it's you

# 5
That video was adorable. Great to see you back!

# 6
>>15239

Isn't that the 'Gigachad' bodybuilder fella where they photoshopped his jaw? Together we will make a future where every man can be a "Chad" to his own robot companion! Nobody will ever have to be lonely or isolated again. Society's outcasts can stop hating other humans, because they have the option to love a robot instead. With the effort and persistence born out of this love, over time the robots will improve.



>>15242

It's great to be back, anon! Cheers.



(Sorry for the rant, I am obsessive and prone to fanaticism).

# 7
Bravo, good to see Sophie again. Looking decent though, coupling her eyes together to prevent going cross-eyed and lowering heads mass by a couple of servos would help.https://www.thingiverse.com/thing:1152248



Also, her head should really be made as a vase mode print to save a lot of mass.

# 8
>>15246

>coupling her eyes together to prevent going cross-eyed 



That's just me messing about. I didn't have time to program her properly, plus I am immature enough to get a kick out of moving her individual eyeballs like that :P



Not happy with her current eyes though TBH. They are hand-painted onto a spherical surface, and despite my best efforts there are large inaccuracies and differences between the two. I am working on some eyeballs that are more standardised and hopefully will incorporate epoxy lenses which naturally reflect and refract light, instead of trying to paint on fake reflectivity, which is incredibly difficult to do well. That way, I only have to concentrate on painting a pretty iris, not the whole thing.



Used this earlier post for reference.

>>10991



As for 'vase mode', I don't recall ever having used that before in Cura slicer. But yeah, her head is vaguely vase-shaped, except for the servo-mount inside.

# 9
>>15276

A really simple and cheap way to get cute eyes is gluing an anime girls eyes to the back of a glass or resin half sphere/gem. Here's a guide that includes making resin gems for mass production.

https://www.jadepixeldoll.com/making-resin-eyes-step-by-step/



Here's a basic guide to vase mode with Cura.

https://all3dp.com/2/cura-vase-mode-all-you-need-to-know/

# 10
>>15238
Y/w. I'm sure you'll get it all sorted as you just keep after it Anon. Simple things like proper wiring harnesses/routing management can be surprisingly important to systems engineering. Cheers.

# 11
>>15281

Thank you Kiwi! That resin anime-eye production method will certainly come in handy.

# 12
>>15321
Please post pics when you have new approaches working Anon.

# 13
Just watched this new video on AMECA/ Engineered Arts.



https://youtu.be/6iO6XhbVQfs



When I look at all the time they spent making a bulky neck and how they've gone through eight iterations to make the neck mechanism, I realise that they aren't actually that much smarter than us. Will Jackson is just loaded and can afford to use way better materials/buy a way better workshop.



I literally have the files on my computer for a design similar to his eighth-gen neck mechanism. I found it after less than hour of Google searching:



https://www.youtube.com/watch?v=1NAlPKeRZTM. 



But it will need significant alterations to fit Sophie, which means I'd have to start a shitload of 3D printing. Which I cannot afford right now due to the energy price explosion :(

This is why I am just keeping things virtual and  playing about with Elfy and M-66 in Blender. 



I'd apply to work for engineered arts if it didn't mean moving house LOL. Although AMECA is not personally my taste at all. It's too corpse-like and not cartoony at all. Also, I dislike that they have literally created a robot NPC-wojak.

# 14
>>15536
I think I had recommended to you before to see about work with them SophieDev? Even if it's difficult to work out, still, if you can manage it I think it would be an amazing couple of year's adventure for you.

> Also, I dislike that they have literally created a robot NPC-wojak.
I despise it, actually. They've very intentionally chosen a character design that could hardly have less appeal to it. My guess is the bossman is looking to cash in on the military's drive for Terminators in the future.

# 15
>>15606

>literal npcbot



Lol looks like an overhyped speaker with arms and legs tbh.

# 16
>>15607
>speakerbot
Haha, now that you mention it, it does kinda remind me of those crappy looking over-blingbling'd ghettoblasters. I wonder if the ring in the chest is supposed to be emotive of ''Tony Stark'' 's power pack or something?

There's little doubt about the amount of money being poured into these things though, and it's pretty obvious that they will be able to start selling them eventually to local police departments as ''Intimidators'' and whatnot.

>tl;dr
As mentioned by Anon in the other thread, we'd better get moving! :^)

# 17
With ears like those, Elves must be able to hear even the most silent of farts from a great distance.

# 18
>>15738
Excellent! What'd you figure out that did the trick exactly, SophieDev? The textures look just fine AFAICT.
>sensitive ears
lol

# 19
>>15739

The UVs were normal (not scrambled/encrypted) I think. I am a total noob at Unity and was just following a character export tutorial for Final Fantasy XIV Online. Very specific to that game and it's assets. (Although I now want to mess about with some Honey Select assets too and test what happens with those textures). It has been very interesting to learn about all the different texture maps like albedo, colour, normal, occlusion and specular.



If there is one thing I have realised though - there is a very good reason that rigging and animation are a whole separate discipline to 3D modelling. It's complicated AF (unless you can just be happy with MIXAMO animations - which I am). 



For example, suppose you want to make a VR Chat avatar...



1.) You need the patience of a Saint to deal with all of the software version conflicts and different plugins required.



2.) (This applies to many different programs not just VR chat + Unity) you can come back to a project after two weeks having not touched it, and both your tools and your assets will have broken themselves due to an "update".  (Imagine if this happened to tradesmen IRL). You then have to spend several hours un-fucking things before you can make any more progress. 



3.) Unless you've got ```$$$``` of motion and facial capture hardware, it is extremely difficult and hella time-consuming to smoothly animate a convincing humanoid in 3DCG. 



I have learned to be happy with relatively simple things like just posing a rigged character or making new assets in Blender. If a process requires more than two different plugins to work or uses more than two programs, I am avoiding it like the plague. Because even if I do get it all to work today, version 4.8.6.3.51 (hotfix B) will doubtless auto-fuckup everything in a months time.

# 20
>>15744

Sorry about the rant. But I have confirmed that Honey Select UVs are scrambled, as suspected. This is inside Unity, following the exact same process I did to texture the Elf from Final Fantasy 14, above. Textures are completely effed, even though I know I have at least three of the five texture maps applied to the material properly.

# 21
>>15751
>>15744
>project after two weeks having not touched it, and both your tools and your assets will have broken themselves due to an "update". 
You don't need to use the current version though. Especially older versions of FOSSoftware are openly available. You could also look into Guix or Nix package managers to install older and newer versions of the same software and the necessary libraries.

Apologies about that Anon. Good advice.

# 22
>>15744
>>15745
Nice effort SophieDev. Good detective work.
>Sorry about the rant
Lolwut. No you're absolutely right **and it's far worse than you imagine tbh. Research the role of  'Pipeline TD' for any major studio.**

Looking forward to see what you do in Unity Anon.

# 23
>>15745

Its less to do with unity and more to do with texture map exporting fuckery.

