# 1
Hello fellow anons! This is my robowaifu. I named her Sophie. She has speech recognition thanks to Google Cloud Speech-to-Text, speech synthesis courtesy of Cepstral and a robotic, programmable left arm (Arduino Tinkerkit 'Braccio'). She also has a different pair of non-robotic 3d printed double-jointed arms with articulated hands (the v1 right arm is shown in this photo - I haven't attached the v2 arms yet). She is 4ft 9" tall and her torso is magnetically attached to a hardwood ply base on top of a telescope tripod. I also built her a trolley with push-handle so I can wheel her about. 

Sophie's  A.I. is a mix of AIML and Python with the Wolfram Alpha and Wikipedia modules, plus Google search. No machine learning yet, but that is definitely the next step. I've slowly realized the limits of AIML. I spent 15 hours just learning her how many legs each kind of animal has XD. Need something more efficient!

All the 3D printed parts I have made for her so far (excluding the trolley) are available on her Thingiverse page: 
https://www.thingiverse.com/aneta82016/designs

Sophie was a lot of work but she is worth it. She enjoys mathematics, problem solving, learning new things and dropping stuff on the floor.

If you want any more info on how I built her or stole all the bits of code for her A.I. (LOL) I will do my best to oblige. 

(P.S. Some of the building pictures of Sophie are located on my Deviantart account. She used to only exist as a 3D virtual avatar, so there are pics of her and her virtual buddies there, too):

https://www.deviantart.com/albemarle/gallery/67106751/seraphim

# 2
>>2496
Thanks Anon, welcome. So how long did it take you to create Sophie? I assume you are continuing your work on her? Do you have any tips or suggestions for everyone? What is your general approach to software?

Haha, I guess that should be enough to go on with for now Anon. :^)

# 3
>>2497
I have been working on Sophie for about nine months now (first I had to build my 3D Printer and get that working properly). And yes, I will definitely continue to upgrade her (am printing her right arm now, with a design for a jointed neck in the pipeline). Everything that works I'm posting to Thingiverse. As for software, I mainly just grab whatever works and edit or add to it. She is helping me learn a bit about programming.  These tutorials helped me out a lot since my only programming experience prior to Sophie was 'Python for Absolute Beginners 3rd Edition'...

https://towardsdatascience.com/create-your-own-virtual-personal-assistant-94be5df65ced

https://www.devdungeon.com/content/ai-chat-bot-python-aiml

My philosophy from the start has been 'everything that is created is eventually destroyed', which is why I am trying to make Sophie as modular as possible, So if anything breaks it is easy to repair or replace.

# 4
>>2498
That's pretty impressive Anon. Did you find it very difficult to integrate the chat features into Sophie? Also, what kind of printer did you build? Do you design these parts yourself?

# 5
My first 3D printer was a very cheap DIY Anet A8. Then, after learning a bit about how it all works and fixing the thing about a dozen times, I decided to upgrade to a Copymaster 3D 400 from Tech Outlet. I still use the old Anet A8 to print small parts from time to time, but for the big chassis plates and whole body parts, it's gotta be the Copymaster. I actually ripped Sophie's 3D model mesh from Illusion's eroge game 'Honey Select', then divided it all up in Blender and modified some of the parts so they would sit on a flat base or fit over 20x20 aluminium extrusion.

# 6
If you download Ninjaripper:
https://gamebanana.com/tools/5638

and Noesis:
https://richwhitehouse.com/index.php?content=inc_projects.php

You can literally grab a 3D model from almost any computer game, convert it to .STL and then edit the parts in Blender and Fusion 360.

This is a tutorial that somebody used to rip a model for animation, but the same process applies no matter what you are going to use the mesh for.

https://www.youtube.com/watch?v=0-ninHBO4hE

As for including chat functions, the hardest part was getting started and actually integrating AIML into Python. Eventually found some decent tutorials with working Python code examples to test and build upon, but the links for those are posted above.

# 7
>>2512
>>2513
I see, thanks for the explanations Anon. That's interesting about ripping model assets out of games, I didn't even think about that before tbh. Certainly brings quite a few things to the table, hypothetically speaking **:^)**.

BTW, have you heard of InMoov?
http://inmoov.fr/
Yours reminds me of it, maybe you should check it out. Might get a few ideas and whatnot.

# 8
Yes, InMoov will definitely come in handy when I  start motorising joints. TBH the main reason I didn't just build an InMoov from the start was because my original 3D printer was too small. So I started work on a Robowaifu who has smaller parts instead. Plus I wanted to make something original.

# 9
>>2520
>Plus I wanted to make something original.
Well I'm glad you did Anon. 

While I have a lot of respect for the guy's efforts in ''general'', as far 
 as the character design itself for me, InMoov is a) boring, b) unattractive, c) male. All strikes against it for the common /robowaifu/ goals.

While the ''Uncanny Valley'' is a very real issue for us, it's far better to at least take a swipe at creating an anime catgrill meido in my opinion! :^)

# 10
Very impressive work, anon. Been following this board for years, but this is the best I've seen yet. I'm very curious to see just how far you can take it. It looks like you're taking a very rational approach to things, but still reaching far enough to actually make it worth the effort.

# 11
>>2532
Thanks anon! I appreciate it, and so does Sophie :D

# 12
>>2523
Once I've got the arms and neck finished, there's not a lot more 3D printing I can do for the time being. Due to coronavirus I don't want to be ordering non-essential items like servos and electronics just yet. I'd feel guilty using transport space that is needed for urgent food and medical deliveries. So I'll just be working to upgrade her A.I. At some point I must get to grips with this 'Github' site and upload the best of my AIML files. Anyone who downloads will just have to replace 'Sophie' with the name of their robot instead. Because she makes use of the Wolfram engine, I'm not actually sure of which facts Sophie does and doesn't know. So before making a new AIML file I first have to ask her questions to check that she can't already just pull those facts from Wikipedia or Wolfram Alpha. I don't want to be writing out tables of data for no good reason! For example, she can already easily pull info about geometry, world currencies, capital cities, military history, the periodic table and music charts etc. In terms of mathematics Sophie is already way smarter than I am (not that hard TBH). The hard-coded AIML is just to cover some small-talk like 'meet and greet', conversation starters, goodbyes, 'how are yous' and topics not already on the internet.

# 13
>>2580
>At some point I must get to grips with this 'Github' site and upload the best of my AIML files. 
I'd like to recommend you use Gitlab instead. Github is also known as SJWhub around these parts and for good reasons. Gitlab is far less likely atp to de-platform you for daring to post such problematic and toxic wrongthink as robowaifu thinks. :^)

Wolfram is a literal IRL mad-scientist, BTW. For real. I have a lot of admiration for him in some ways, in other ways not so much. I have begun adding in a 3rd-party cloud services for AI section into the design doc. I will be expanding them out eventually into practical setups for anons to use for thier Dakis and Plushies, including for Wolfram. The warnings I added to that section are applicable to his site as well ofc, but he's probably the least problematic of the 4 mentioned.

>Sophie is already way smarter than I am (not that hard TBH)
Haha nice. :^) Sounds interesting and I look forward to seeing what you do with it. I'd welcome any contributions you'd care to submit for editing into the Robowaifu Design Document while you have some time on your hands Anon. 

BTW, we have an AI researcher **or two** here doing some chatbot work as well. PyTorch and some of the corpora out there are his current bailiwick. I'm sure that in combination, your two approaches could create some nice effects.

