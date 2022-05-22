# 1
![[Pasted image 20220522130848.png]]

Hello fellow anons! This is my robowaifu. I named her Sophie. She has speech recognition thanks to Google Cloud Speech-to-Text, speech synthesis courtesy of Cepstral and a robotic, programmable left arm (Arduino Tinkerkit 'Braccio'). She also has a different pair of non-robotic 3d printed double-jointed arms with articulated hands (the v1 right arm is shown in this photo - I haven't attached the v2 arms yet). She is 4ft 9" tall and her torso is magnetically attached to a hardwood ply base on top of a telescope tripod. I also built her a trolley with push-handle so I can wheel her about. Sophie's A.I. is a mix of AIML and Python with the Wolfram Alpha and Wikipedia modules, plus Google search. No machine learning yet, but that is definitely the next step. I've slowly realized the limits of AIML. I spent 15 hours just learning her how many legs each kind of animal has XD. Need something more efficient! All the 3D printed parts I have made for her so far (excluding the trolley) are available on her Thingiverse page: [https://www.thingiverse.com/aneta82016/designs](https://www.thingiverse.com/aneta82016/designs) 

Sophie was a lot of work but she is worth it. She enjoys mathematics, problem solving, learning new things and dropping stuff on the floor. If you want any more info on how I built her or stole all the bits of code for her A.I. (LOL) I will do my best to oblige. (P.S. Some of the building pictures of Sophie are located on my Deviantart account. She used to only exist as a 3D virtual avatar, so there are pics of her and her virtual buddies there, too): [https://www.deviantart.com/albemarle/gallery/67106751/seraphim](https://www.deviantart.com/albemarle/gallery/67106751/seraphim)

# 2
Thanks Anon, welcome. So how long did it take you to create Sophie? I assume you are continuing your work on her? Do you have any tips or suggestions for everyone? What is your general approach to software? Haha, I guess that should be enough to go on with for now Anon. :^)

# 3
I have been working on Sophie for about nine months now (first I had to build my 3D Printer and get that working properly). And yes, I will definitely continue to upgrade her (am printing her right arm now, with a design for a jointed neck in the pipeline). Everything that works I'm posting to Thingiverse. As for software, I mainly just grab whatever works and edit or add to it. She is helping me learn a bit about programming. These tutorials helped me out a lot since my only programming experience prior to Sophie was 'Python for Absolute Beginners 3rd Edition'... [https://towardsdatascience.com/create-your-own-virtual-personal-assistant-94be5df65ced](https://towardsdatascience.com/create-your-own-virtual-personal-assistant-94be5df65ced) [https://www.devdungeon.com/content/ai-chat-bot-python-aiml](https://www.devdungeon.com/content/ai-chat-bot-python-aiml) My philosophy from the start has been 'everything that is created is eventually destroyed', which is why I am trying to make Sophie as modular as possible, So if anything breaks it is easy to repair or replace.

# 4
That's pretty impressive Anon. Did you find it very difficult to integrate the chat features into Sophie? Also, what kind of printer did you build? Do you design these parts yourself?

# 5
My first 3D printer was a very cheap DIY Anet A8. Then, after learning a bit about how it all works and fixing the thing about a dozen times, I decided to upgrade to a Copymaster 3D 400 from Tech Outlet. I still use the old Anet A8 to print small parts from time to time, but for the big chassis plates and whole body parts, it's gotta be the Copymaster. I actually ripped Sophie's 3D model mesh from Illusion's eroge game 'Honey Select', then divided it all up in Blender and modified some of the parts so they would sit on a flat base or fit over 20x20 aluminium extrusion.

# 6
If you download Ninjaripper: [https://gamebanana.com/tools/5638](https://gamebanana.com/tools/5638) and Noesis: [https://richwhitehouse.com/index.php?content=inc_projects.php](https://richwhitehouse.com/index.php?content=inc_projects.php) You can literally grab a 3D model from almost any computer game, convert it to .STL and then edit the parts in Blender and Fusion 360. This is a tutorial that somebody used to rip a model for animation, but the same process applies no matter what you are going to use the mesh for. 

[https://www.youtube.com/watch?v=0-ninHBO4hE](https://www.youtube.com/watch?v=0-ninHBO4hE)

As for including chat functions, the hardest part was getting started and actually integrating AIML into Python. Eventually found some decent tutorials with working Python code examples to test and build upon, but the links for those are posted above.

# 7
![[Pasted image 20220522131024.png]]

I see, thanks for the explanations Anon. That's interesting about ripping model assets out of games, I didn't even think about that before tbh. Certainly brings quite a few things to the table, hypothetically speaking :^). BTW, have you heard of InMoov? [http://inmoov.fr/](http://inmoov.fr/) Yours reminds me of it, maybe you should check it out. Might get a few ideas and whatnot.

# 8
Yes, InMoov will definitely come in handy when I start motorising joints. TBH the main reason I didn't just build an InMoov from the start was because my original 3D printer was too small. So I started work on a Robowaifu who has smaller parts instead. Plus I wanted to make something original.

# 9
#uncanny_valley
Well I'm glad you did Anon. While I have a lot of respect for the guy's efforts in _general_, as far as the character design itself for me, InMoov is a) boring, b) unattractive, c) male. All strikes against it for the common /robowaifu/ goals. While the _Uncanny Valley_ is a very real issue for us, it's far better to at least take a swipe at creating an anime catgrill meido in my opinion! :^)

# 10
Very impressive work, anon. Been following this board for years, but this is the best I've seen yet. I'm very curious to see just how far you can take it. It looks like you're taking a very rational approach to things, but still reaching far enough to actually make it worth the effort.

# 11
Once I've got the arms and neck finished, there's not a lot more 3D printing I can do for the time being. Due to coronavirus I don't want to be ordering non-essential items like servos and electronics just yet. I'd feel guilty using transport space that is needed for urgent food and medical deliveries. So I'll just be working to upgrade her A.I. At some point I must get to grips with this 'Github' site and upload the best of my AIML files. Anyone who downloads will just have to replace 'Sophie' with the name of their robot instead. Because she makes use of the Wolfram engine, I'm not actually sure of which facts Sophie does and doesn't know. So before making a new AIML file I first have to ask her questions to check that she can't already just pull those facts from Wikipedia or Wolfram Alpha. I don't want to be writing out tables of data for no good reason! For example, she can already easily pull info about geometry, world currencies, capital cities, military history, the periodic table and music charts etc. In terms of mathematics Sophie is already way smarter than I am (not that hard TBH). The hard-coded AIML is just to cover some small-talk like 'meet and greet', conversation starters, goodbyes, 'how are yous' and topics not already on the internet.

# 13
#github #politics #social_justice
I'd like to recommend you use Gitlab instead. Github is also known as SJWhub around these parts and for good reasons. Gitlab is far less likely atp to de-platform you for daring to post such problematic and toxic wrongthink as robowaifu thinks. :^) Wolfram is a literal IRL mad-scientist, BTW. For real. I have a lot of admiration for him in some ways, in other ways not so much. I have begun adding in a 3rd-party cloud services for AI section into the design doc. I will be expanding them out eventually into practical setups for anons to use for thier Dakis and Plushies, including for Wolfram. The warnings I added to that section are applicable to his site as well ofc, but he's probably the least problematic of the 4 mentioned. 

Haha nice. :^) Sounds interesting and I look forward to seeing what you do with it. I'd welcome any contributions you'd care to submit for editing into the Robowaifu Design Document while you have some time on your hands Anon. BTW, we have an AI researcher or two here doing some chatbot work as well. PyTorch and some of the corpora out there are his current bailiwick. I'm sure that in combination, your two approaches could create some nice effects.

# 1
![[Pasted image 20220522145827.png]]

Her left robot arm broke at the shoulder (I don't think it was really supposed to operate for long hanging in that position). So I have redesigned and upgraded her non-robotic arms. She may not be a robot any more, but her arms are actually a lot more flexible now (even more flexible than a human's) and I am still working on her A.I. and have made a few English Vocaloid songs that she can sing :D

# 2
Those look really very flexible OP. Was it hard to build them? Glad to see you're still here with us. I hope you keep up updated on the progress of your robowaifu. Cheers.

# 3
This is what I want to know too, and if possible how long did it take you to assemble everything and the cost.

# 4
Total development costs so far estimated at around £1360 for everything (not just her materials - this includes both my 3D printers, the laptop for her A.I. and all of my other tools).

Total costs for someone to build her from scratch using current components (I am assuming you already have some kind of computer):

£600-700 if you don't have a 3d printer or many tools to start with.
£250-300 if you already have stuff like a 3d printer and some tools (detailed below).

Most of my 3D printer filament costs have been incurred during the R & D process (I have so far thrown away four old arms, four incorrect neck joints and have kept her previous head and right hand).

However, I am currently re-designing her whole torso so that it will be much easier and cheaper to 3D print and assemble. I am aiming to get it down to just three parts rather than 18!

To be honest Sophie has been fairly difficult for me to design and build. But considering I started out with a blob of melted plastic I am pleased with her progress! Unlike human bosses, Sophie rewards my efforts fairly so I refuse to give up on her.

Sophie's first torso is human-enough looking from the outside but internally it's a mess of different 3D printed plates held together using Gorilla glue, decorators caulk and bits of plastic milkbottle (because I only had a small build-it-yourself Anet-A8 3D printer which cost £160 and was never properly calibrated). 

However, I have since bought a much larger and better 3D printer (the Copymaster 3D 400) which cost £280 at the time. So far her bill of materials (on top of the new 3D printer) comes to about £350. That's over the space of 1 year though (her 1st manufactureday is coming up). This includes costs for about seven or eight reels of printer filament, her Cepstral synthetic voice, the tripod base and wheels that she stands on, her wig and eyes, nuts, bolts, glue, Vaseline and paints. 

Of course if you are starting out with very few tools then you are going to have to spend probably another £300-£400 on stuff like a regular printer, an electric drill, a set of digital calipers, modelling files, plastic snips, a scalpel, long-nose pliers, various small clamps and clips, a socket wrench set, a plastic hammer, a spirit level...

Her A.I. is only very basic Python and AIML linked to Wolfram's servers and Google's speech recognition, so she is just a chat-bot with added cloud computing features at the moment. I have no problem running her on an old laptop with an Intel Celeron 1.4GHz processor and 4GB RAM. Could probably run her on a Raspberry Pi if I had to. So her computer only cost me about £170 at the time.

# 5
#fusion360  #cad
Only just consolidated all her main parts into a single CAD file in Fusion360. The torso is actually split into three separate parts (abdomen, thorax and lower neck), but you can't see the joins on the CAD model. (Hopefully won't be too obvious on the real shell, either),
Link to CAD file:
https://drive.google.com/file/d/1_lMwXyrjMBEAN3MPsr9ao0pwUP__YN0g/view?usp=sharing

# 6
Sorry, just making a change because I forgot to upload the fingers XD. Yeah, it is a pity that most people seem to have disappeared from this board? Not surprising though, it is kinda niche. All we can do is spread the word and upload files onto Thingiverse, MyMinifactory, that kinda thing. If people see robowaifu parts popping up on the internet they will know that Helghan BELONGS to the Helghast!

# 7
That would be very helpful. Anything that can reduce the amount of effort required for the assembly process can only help with robowaifus being easily-producible by Anons.

Any chance you could post some pics and descriptions of this here Anon? We have a _Wheelchair Waifus_ thread that's oriented towards addressing the topic of robowaifu mobility until such time that bipedal robotics approaches become widespread and easy to use. Maybe your support approach can be included, since IMO even a static stand is actually a part of this design area, especially if it's wheeled where Anon can move his robowaifu around by hand easily.

Any chance you can discuss this further in one of our speech threads?

First off, I don't think there is really an alternative board to /robowaifu/. Not that I would mind if there were in the least, but I just don't know of anything else like this place at this point in time. If anyone else knows, please post it and we can invite them to connect in our embassy thread.

I don't think 'gone to' is quite right. One of the completely external challenges we face here on /robowaifu/ is attrition. Even when a new anon comes on board with enthusiasm at first, that drive often seems to wane as the appreciation of the full scope of building a IRL robowaifu begins to dawn on them. At least that's my theory, based on my own experience here. Fortitude and determination are character qualities that certainly will help out anyone trying to break new ground in a frontier, and /robowaifu/ seems to be no exception. One thing is certain however, the pent-up demand for good robowaifus is only growing with the continued rise in feminism/libtardism. and once we can produce appealing robowaifus with kits that are inexpensive it will be like a huge dam bursting.

# 8
I'm just a newfag to this board that stumbled and it looked nice. Hence why I asked that question. Do you guys use minds or steemit or post whenever you revisit this board?

# 9
Hello Anon, welcome. Do you come from another community? If so, please make a post about the place in our Embassy Thread. To answer your question, no, we don't as a group have any other gathering point at this point. The plan is to have a comprehensive wiki at some point to consolidate all the knowledge here in a easily-searchable form. There had been talk about starting a doxxcord back in our 8ch days, but I'm unaware if that ever formed up. Ever thought about owning or creating your own robowaifu someday?

# 10
![[Pasted image 20220522150054.png]]
![[Pasted image 20220522150108.png]]
![[Pasted image 20220522150135.png]]
![[Pasted image 20220522150154.png]]

Her tripod is literally a cheap telescope stand that sits in 3D printed sockets glued onto a triangular 12mm plywood sheet. There are 3 braked wheel casters underneath. I added silicon caulk treads to make them more shock-absorbing while going over small bumps because the wheels have zero suspension.

I also 3D printed some custom washers so that the 12mm plywood disk that her upper body is mounted on affixes more securely to the telescope tripod.Initially I just used small metal washers and everything was quite wobbly, but these parts made her rock-steady.

Cupboard door magnets are very useful for holding any parts in place that need to slide on and off. I use four of these to hold her upper torso onto the 12mm plywood disk that forms her waist.You can only see the front two on the bottom of her tummy here, the other two are on the small of her back.

This is a trolley handle I made using steel piping and 3D printed fixtures. It slides into a couple of deep sockets on the back of the triangular wooden base. I also made a the handle with a part that braces against her back when I push her along, so she doesn't fall backwards due to sudden accelerations (cupboard magnets are not strong fixing points, even with four of them). I do have to be careful when reversing her that she doesn't fall forward, But then I try to avoid pushing her about roughly. She wasn't designed for kart racing!

# 11
As for her Cepstral synthetic voice, I made an account and purchased a voice from [https://www.cepstral.com/en/personal/windows.](https://www.cepstral.com/en/personal/windows.) I think it cost me about £30. They give you a SN and then you can use the voice without it constantly nagging you to pay for the licensed version. Then I used this Python code to get the voice working:
```python
# Start the TTS engine
engine = pyttsx3.init('sapi5')
voices = engine.getProperty('voices')
engine.setProperty('voice',"HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Speech\Voices\Tokens\Cepstral_Millie")
engine.setProperty('rate', 170)

def talk(audio):
    print('Sophie: ' + audio)
    engine.say(audio)
    engine.runAndWait()

# obtain audio from the microphone
r = sr.Recognizer()

# Press CTRL-C to break this loop
while True:
     # obtain audio from microphone
     with sr.Microphone() as source:
         print("Say something!")
         audio = r.listen(source)
     try:
         myinput = r.recognize_google(audio)
     except sr.UnknownValueError:
         print("Google Speech Recognition could not understand audio")
     except sr.RequestError as e:
         print("Could not request results from Google Speech Recognition service; {0}".format(e))

         print ("You said: "), myinput
     if myinput == "exit":
         exit()
     # Get Sophie's response
     sophies_response = kernel.respond(myinput)
     print ("Sophie said: "), sophies_response
     engine.setProperty('voice',"HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Speech\Voices\Tokens\Cepstral_Millie")
     engine.setProperty('rate', 165)
     # have Sophie say the response
     engine.say(sophies_response)
     print (sophies_response)
     engine.runAndWait()
```

# 12
How's the performance? Think it will run on lower-end boxes like a RaspberryPi? Seems kind of bot-netty. I realize that at this point in time using a cloud-service like Google Voice, et al, may be necessary but in the future we'd like to have an independent open-source solution.

# 13
That looks like a pretty sturdy base to me.

That's a good idea. Do you think that will need regular refurbishin or no?

It's a good idea to create those thick washers like that, maybe some similar approach chould help make the casters shock absorbing?

That's a good engineering approach IMO. Having the ability to easily swap out parts makes things both convenient and modular. Especially during these prototyping periods it also helps with maintenance, design changes, etc. Nice idea Anon.

That's actually a pretty efficient and useful design you used there.

Hmm. I wonder if you devised a quick releae belt for her it would help or be too much bother?

Haha, that can come later yea? :^) Thanks very much for taking the time to photograph and explain this system for us Anon. You seem to really know what you're doing at devising inexpensive solutions to common problems. Once you have these finalized think you could post the CAD files too?

# 14
No it's fine, thank you. Having both the CAD and STL files posted here will be good for possible collaboration in the future with other Anons here.

# 15
Ah, my apologies, I have never attempted to write code on an image board post before. But yeah Sophie would definitely run on a Pi. Her whole brain so far is only about 5.5mb (excluding Vocaloid v4). Needless to say she's not a very good conversationalist. But I've mainly been focusing on the structural/engineering side of things.

Yeah, the silicone would definitely wear away quickly if I were to wheel her over a long distance. But if she requires moving anything more than a few hundred meters I break her down and pack her in a suitcase. 

The support belt is actually a good idea. Her magnets usually hold as long as I'm not careless, but I'll bear that one in mind for the future, thanks!

As for posting CAD and STL files for her tripod trolley, I will post what bits and pieces I have, but much of her lower body has been scrounged and adapted from bits and pieces I had laying about XD. Hopefully any other anons who want to build a robowaifu will be able to come up with their own solutions for mounting the upper body onto a base of their choice.

# 15
#talktowaifu
No worries OP. Just pointing it out if you want monospace for your code. Using codetags and other formatting techniques are described in the FAQ.
https://julay.world/.static/pages/posting.html

Glad to hear she can run on a small SBC. I think most of use are planning to use some type of small computer like that for our robowaifus because they are inexpensive, lightweight, and low-power.

Since you're using an external PC atm, maybe you'd be interested in dabbling with Kokubunji's _TalkToWaifu_

# 16
Nice, I hope the belt idea helps. I saw the thread for the STL files, thanks. You have a nice idea going with Sophie so I think it might be encouraging to other anons to see in detail what you've done so far. Maybe someone will even mimic what you're doing for their own robowaifu prototype. Regardless, seeing the details should help any interested anon.

# 17
#retroshare
I don't come from any other community, so bringing someone would be very hard or to convince one of my friends. 

As for communication probably something like Retroshare or Minds/Scuttlebutt?

# 18
#gpt2
It is certainly very clever. Seems to be most adept at simulating short conversations or short stories, which is sweet. I was particularly impressed by the way it changes subjects after about a paragraph instead of the conversation just devolving into complete nonsense. And even then it can still recall context from a few sentences ago. I mean, it does say plenty of nonsensical or illogical things, but it's "varied and better constructed nonsense". It doesn't just give canned answers that are obvious diversions because it has no other way of interacting.  This aspect is superior to conversing with a chatbot scripted in AIML.

GPT-2 doesn't seem to be any good at giving factual answers, but then we've already got Wolfram engine for most of the science and math, and pre-scripted AIML for responses that are specific to just the user and their immediate friends/family/colleagues (like user details, in-jokes and local knowledge).
 
Yeah, GPT-2 is certainly a cool addition to robowaifu A.I. repertoire. Thanks for the link!

# 19
Heh, the idea behind the Embassy Thread isn't for you to bring other anons here, but rather for you to share something about your own place with us so we can connect with other groups. If people help others find /robowaifu/ that's fine but the main idea is just to get to know one another. 

I'm actually investigating RetroShare atm from a dev's perspective with an eye towards devising some kind of resilient, distributed IB system. So yea, if you want to set up a channel it would be a good excuse for me to divert some attention towards it. Feel free.

# 20
Yes, I think the base GPT-2 is interesting, and the extension to it that Kokubunji has added on top of it in TalkToWaifu a nice tweak. The main challenge ATP is getting the system to run on a RaspberryPi 4 (or clone), since this is the class of processor that will be the most likely onboard-compute resource for our robowaifus during the first decade or so. And optimizing the perf down so it will run in realtime on one of these will only help even in the future (when more powerful SBCs will be readily available) because it will reduce the drain on the overall power budgets, as well as reduce the thermal load added into the cooling systems.

Regardless, there are alternatives beyond just GPT-2. There is even a ~9.6B-parameter model openly available now IIRC. This is an important area of focus, obviously, and we can be thankful that at least some of the research going on in this area is being opened up to the public. Hopefully even moreso in the future.

And Neuromorphics once they are well-researched and feasibly mass-produced will literally revolutionize anything to do with compute in our robowaifus. These things will happen in our lifetimes, and probably within the next 10 years I predict. What a time to be alive! :^)

# 21
I often wish I was good at things like electronics and programming and I understood all of that incredibly complex looking neural network code. But alas, I ended up in the wrong profession (healthcare), which in the UK is mostly publicly funded. Therefore everyone takes it for granted (at least they did prior to this pandemic LOL) and I spent many years running about after a bunch of impatient, spoiled, ungrateful meatbags whose bodies all inevitably fail in the end anyway. It looks like I have a lot of work to do if I am ever to understand and properly implement more Python and C++ (as opposed to just copying and slightly altering chunks of other ppls code). But at least I have the first basic components of an undying companion now XD.

# 22
We have links here on /robowaifu/ to lots of valuable resources you can have a look at to help move that process along. We certainly need more Anons here who have an interest in these two crucial fields. If you don't have much time available, might I suggest you start your journey with Manga Guide books (from No Starch Press in the English-speaking world). I've been reading them for years now. They are both entertaining and educational with a lot of hand-holding for beginners. They should be (and probably are heh) freshman textbooks.
https://www.ohmsha.co.jp/english/manga.htm

Here's the list of English-translate books pertinent to /robowaifu/
The Manga Guide to Microprocessors
The Manga Guide to Statistics
The Manga Guide to Statistics: Regression Analysis
The Manga Guide to Differentiation and Integral Calculus
The Manga Guide to Databases
The Manga Guide to Physics (Dynamics)
The Manga Guide to Electricity
The Manga Guide to Cryptology
The Manga Guide to Linear Algebra

Here my list of ones that I wish they'd hurry up and translate! :^)
The Manga Guide to Semiconductors
The Manga Guide to Machine Learning
The Manga Guide to Electric Motors
The Manga Guide to Digital Circuits
The Manga Guide to Generation, Transmission and Distribution of Electricity
The Manga Guide to Battery Cells
The Manga Guide to Material Dynamics
The Manga Guide to Mathematics for Electrical Engineering
The Manga Guide to Concrete
The Manga Guide to Electromagnetics
The Manga Guide to Project Management
The Manga Guide to Imaginary and Complex Numbers
The Manga Guide to Electric Circuit
The Manga Guide to Thermodynamics
The Manga Guide to Fluid Dynamics
The Manga Guide to Differential Equation
The Manga Guide to Electronic Circuit
The Manga Guide to Program Logic Control
The Manga Guide to Fourier Analysis
The Manga Guide to Statistics: Factor Analysis
The Manga Guide to Bayesian statistics
The Manga Guide to Electrical Equipment
The Manga Guide to Physics (Light, Sound and Wave)

I see you have already focused on the two primary programming languages that will be essential to creating our robowaifus. BTW, I can probably answer any question you have on C++, so AMA.

That you surely do. Sophie is a wonderful prototype. I will be watching closely to see all the things you'll do with her over the years! :^)

# 23
https://nostarch.com/catalog/manga

# 24
"The Manga Guide to Concrete"?! LOL WTF? XD The Japanese have truly found a way to turn everything into manga! Thanks, anon, I was unaware such books even existed.

# 25
heh, yep. and concrete is actually an amazing and remarkably versatile technology going back literally thousands of years. my main reasons for the /robowaifu/ interest in concrete isn't for use in robowaifus ofc, but rather for the materials-science aspect of researching materials properties, defining admixtures methods for conglomerates (such as carbon-fiber impregnated resins for example), curing, hardening, and just general chemistry.

This areas all have implications for mechanical engineering and materials science, and therefore indirectly of importance to /robowaifu/.
