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

# 1
#project #arms 
![[Pasted image 20220522154053.jpg]]

Fully printed, it is quite the chonker.

Two heavy duty servos (110kg.cm torque or greater. 12 to 24 volt) in the shoulder.
Two 60kg.cm servos (DS5160SSG) in the bicep
Five 20kg.cm servos (PDI-6221MG) to move the forearm and fingers.
One micro-servo in the palm to drive the thumb.

# 2
Stupid question, what material did you print with? There are some nylon-based printing materials now that are apparently extremely strong, but also probably rather expensive.

# 3
Very exciting progress Anon. I'm sure we'd all like to see some motion tests for her arm soon. This is for Sophie, correct?

Heh, I'm sure she will lose some dieting. :^)

# 4
I just used PLA (20% triangular infill for the hand and forearm, increasing to I think it was 30% in the elbow and 40% octohedral infill in the shoulder pieces) . Nylon filament is more expensive and prints considerably hotter if I remember correctly - this is just a prototype so I could do.without the higher electricity cost and potential strain on my 3D Printer. I decided against PLA mainly because of the warping and cracking issues. Honestly, PLA is wonder-material for this sort of work! Cheap as chips, easy to work and surprisingly robust and reliable. I once left a PLA plant pot out in the garden for a year. Washed off the dirt and it was good as new!

# 5
D'oh! I meant to write "I decided against ABS due to heat warping and cracking issues". Not PLA. PLA has never cracked on me once in hundreds of prints! (Slight elephants foot in taller prints but that's all).

# 6
This arm has served as a test piece (first robot hand and arm I've ever constructed, so I learned quite a bit). The hand is already operational although the finger-stringing could do with some improvement (it's a bit arthritic at the moment XD). Just waiting to receive a heavy duty servo. I also have to run tests and get more familiar with my new benchtop power supply. Lots to do, but I must focus on electrical/fire safety first, then eventually I will be in a position to get the whole arm operational. After that, I plan to print out the lighter V2 arm which I am currently designing with Proto1 as a base. That will be the arm I upgrade Sophie with.

# 7
![[Pasted image 20220522154247.png]]
![[Pasted image 20220522154252.png]]

Have finished making a lighter version of Ryan Gross's "Proto1 Humanoid Robot Arm". I call my heavily cut-down version the "Protolite".
Have uploaded to the usual repositories:

Googly Drive
https://drive.google.com/drive/folders/18MDF0BwI9tfg0EE4ELzV_8ogsR3MGyw1
MEGA
https://mega.nz/fm/InpynKDL

I want to try and make a light robot arm that can be used as a no-frills base for robowaifus. The Proto1 is built like a bodybuilder's arm, but I wanted something a lot more slender. Have kept the elbow and shoulder joints the same (mainly for strength reasons). But I have also uploaded all of the simplified .stl meshes which have about 90% less geometric density and are intended to be easier to make changes to - in case any other anons fancy a crack at redesigning one part or the whole arm.

# 8
Correction, sorry. I have finished DESIGNING the Protolite v1. Now I just have to print it. Lots of things will go wrong. But at least I am at a stage where I have a design to test.

# 9
That's very good news to hear, thanks Anon! We hope the printing and other fabrication steps go very smoothly for you. Please keep us updated.

# 10
I have considered getting a CNC machine for a while now which would really open a lot of doors for me in designing and fabricating parts out of stronger materials. Upfront cost would be worse (and I'd want something quality) but the durability would be especially helpful especially with things like joints. If I ever get one I'll take pictures of it and cut parts with design advice from anons.

Good luck on your work anon, hoping to see more news drop from you, it's inspiring.

# 11
Actually it might be more cost effective for me to build a CNC machine and I have not considered that possibility until now. Might be more in the spirit of this board as well, as buying a CNC machine might be too out of reach for many anons. Obviously, work with 3D printing is still extremely valuable and should not be stopped. Good luck and godspeed.

# 12
Nylon isn't that expensive, but it's harder to print. The printer should have an enclosure, and maybe even an heater insinde. That makes the printer more expensive. Same for Polycarbonate, which would probably even work better.

However, this would most likely the better route compared to using a CNC machine to build metal parts. 

Well done, progress much appreciated.

# 13
Nylon is not much more expensive than PLA, but when I said nylon-based I meant the ones that mix in other materials like carbon fiber for strength. Just checked price on one website and the material is about twice the price of PLA. I'm not sure how it would hold up against metal for smaller parts that need high durability but it's worth a try. I have heavily considered getting a CNC machine so if I actually owned one, I personally can't see not using it. Obviously it wouldn't be used for everything, but I can see a lot of value in metal joints. Not trying to break my waifu's legs during sex after all.

# 14
In my experience so far, the main failure point in this kind of cheaply manufactured robot is the servo horns. Very difficult if not impossible to make functional servo horns out of PLA for anything above micro servos (I have tried and after a few dozen movements, the metal servo output shaft always wears the gripping teeth of the PLA servo horn away, which means that the output shaft just rotates inside the servo horn and the joint won't move) This is a common problem with cheap, plastic robot parts. It even happened to a cheap factory-made Arduino robot arm that I purchased. Most standard strength (20kg.cm to 60kg.cm) servos come with ABS plastic servo horns. As long as you don't exceed the carrying weight that the motor is designed for, these should be fine. But if you want long-lasting shoulder or hip joints, it's gotta be metal servohorns all the way...

Also, I think a problem that I am going to encounter making a robot arm out of PLA is heat deformation of the biopolymer closest to the larger servomotors when they get hot. I haven't encountered this problem yet, but if it happens, I plan to widen the boxes which contain each servo motor and insulate the base and sides with small blocks of wood. This will hopefully mean that the servo motors can heat up without melting the very parts that hold them!

# 15
I wonder if some kind of sheet aluminum (spun aluminum is best) might be a better heat dissipation choice? After all, you don't really want to insulate the servo motors either, but rather draw heat off. Probably some kinds of ideas in the Robowaifu Thermal Management thread  could help.

# 16
Interesting. Thanks, anon! I may just leave vent holes over any servo areas that get especially hot...as long as the arm structure remains strong enough not to snap. Plus this has the added benefit of reducing weight and material use even further. We'll see...

# 17
Considering CNC is also used heavily for making wood parts I was wondering if there would be any use for wood as a material in building.

Copper would conduct heat better. This would also be interesting for discussion about using the heat generated from batteries, processors, any and all electronics in order to warm the robowaifu up. After all you'd especially want the pussy to be warm, so conserving at least some of this heat and reusing it would be smart

# 18
Like all engineering, everything's a trade-off. While copper would undoubtedly be a better thermal conductor than normal aluminum, it's also notably heavier/weaker. And _spun_-aluminum is already pretty remarkable in it's cooling abilities as is.

Yep. It's already being discussed in some depth in ==post==.

# 19
If your robowaifu is going to have moving legs then creating a warm vag may be simpler than expected. After all, two of the largest servos or stepper motors will have to be located within the pelvic area, and these motors soon warm up after about 15 minutes of operating under load. I have a NEMA17 at the front of my 3D printer and it gets toasty warm just from moving the buildplate back and forth.

# 20
Significant breakthrough! The 180kg.cm high-torque servo motor is now operational. Posting guide here to show how I got it working. 

I realized that this kind of complicated looking electronic hardware is a BIG turnoff to a lot of people who are trying to make a large robot. Most instructions online either had parts missing and were written in Chinglish or videos by a couple of Indians whom I could barely understand.

Fuck that. I just wanted it to work ASAP. So without further ado:

Hardware Used:

High Torque (180kg.cm) Servo Motor DC12 Volt to 24 Volt with steel gearing.
£30 ($39.58) each at time of writing.

Elegoo MEGA2560 R3 (Arduino MEGA2560 Clone) about £13 ($17.15) at time of writing. You can get cheaper ones but MAKE SURE THAT YOURS COMES WITH A USB CABLE! 
(You don't actually need a power adaptor because the benchtop PSU will be providing the electricity, but it's a good idea to make sure that a plug is also included so that you can use your microcontroller for other applications as well).

The power plug I got with mine was an Elegoo brand AC-DC adaptor
Input:100-240 Volts AC 
Output: 9 Volts - 1 Amp DC
The data cable was a blue type A to type B USB 2.0 cable.
The type A end goes in your computer's USB port, 
The type B end fits into the socket on your Arduino/Elegoo Mega.

Eventek KPS3010D DC 0-30 Volt 0-10 Amp Benchtop Variable Power Supply 
Mine cost £75.99 ($100) and included a power cord and two sets of crocodile clips.

Jumper wires - male to female 
You can get over 100 of these for about £5-6 ($6-8) off Amazon. 
Male to male ones are often included in the pack as well.
You'll only need a couple of jumper wires to connect one high-torque servo, but of course robowaifus include many circuits and servo motors so a pack of 100+ is useful!

Standard Household Electrical Cable  
A 2m extension lead costs about £5-6 ($6-8) or you can get 10m of cabling for about £11 ($14.50).

I used a craft knife and metal snips to strip the outer cable wall off and get a couple of 30cm (1ft) lengths of power and neutral cable. 

I then used a wire stripper to strip about half a centimeter of covering from each end
and wound the exposed copper filaments into a tight helix between my fingers.
These wires can then be connected between your PSU and the positive and negative screw terminals on your high-torque servo motor (see wiring diagram).
 
I know these benchtop power supplies expect you to attach a black negative cable and a red positive power cable but in the U.K. the power cable (positive) is brown and the negative cable is blue.

Wiring (also see circuit diagram)

Negative terminal on PSU ----> Negative screw terminal on servo motor
Positive terminal on PSU ----> Positive screw terminal on servo motor

GND on servo motor ---->GND on Arduino MEGA
PWM on servo motor ---->PWM Pin 9 on Arduino MEGA

Once your high-torque servo motor is connected to the ArduinoMEGA and PSU, 
load up ArduinoIDE and make sure that you have selected the correct microcontroller from the

Tools> Board:> ArduinoAVR Boards menu 
(in this case ArduinoMEGA or MEGA2560).

Then make sure that serial port is operational by checking 

Tools> Port:>"COM X" 

For example, mine was set to COM3. 

If you have problems here you'll need to open Device Manager and troubleshoot it.
Ports (COM & LPT) is just below Portable Devices. If you can't see any Ports (COM & LPT) option, press 

View> Show hidden devices 

and it should appear.

Once your board and port are set, you should copy and paste the following code into Arduino IDE. This is the "Sweep" servo example sketch.

```cpp
/* Sweep
 by BARRAGAN <http://barraganstudio.com>
 This example code is in the public domain.

 modified 8 Nov 2013
 by Scott Fitzgerald
 http://www.arduino.cc/en/Tutorial/Sweep
*/

#include <Servo.h>

Servo myservo;  // create servo object to control a servo
// twelve servo objects can be created on most boards

int pos = 0;    // variable to store the servo position

void setup() {
  myservo.attach(9);  // attaches the servo on pin 9 to the servo object
}

void loop() {
  for (pos = 0; pos <= 180; pos += 1) { // goes from 0 degrees to 180 degrees
    // in steps of 1 degree
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
  for (pos = 180; pos >= 0; pos -= 1) { // goes from 180 degrees to 0 degrees
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
}

```

Then press the Upload button.

As soon as the code uploads successfully to your ArduinoMEGA, then the high-torque servo
shaft should repeatedly move between 0 and 180 degrees.

Thats it. Functional high-torque servo!

# 21
Freakin' awesome. Thanks alot Anon. This has been a long term concern for me for our robowaifu's shoulder and hip joints. All the hard work for your careful post appreciated! :^)

# 22
A pleasure! 

Now I just have to get more than one high-powered servo working. It should be fairly easy. Pretty sure I can screw another motor directly into the PSU's front terminals. For more, I'll probably need a breadboard or some kind of splitting device so that several more connections can be made to further motors. Whatever I try, I must keep exposed conductors to a minimum. More high-torque motors will draw more current of course, but this kind of experimentation is exactly what a benchtop power supply is made for. 

(BTW, my high-torque servo came with a servo wire and a 10K potentiometer, but you can get this working without having to use either of them.)

# 23
![[Pasted image 20220522160631.png]]

It was easy to get two running. That's enough to move one shoulder in the Protolite arm. Any more is gonna require some careful wire splicing. The 60kg.cm servos and 25kg.cm servos I have already operated because they can just run off a couple of Arduinos with servo shields like most hobby electronics. Just gonna leave this very short side-by-side comparison of the code here.

# 24
Okay, if you wanted some CNC anyways it's another thing. I just think plastics is quite durable, also one can use standard metal parts for reinforcement. I personally think about building a CNC mill for cutting metal sheets. This shouldn't need to much power. These parts could then be separated from each other with layers out of other materials, and so the metal layers could be used to transport electricity for power and communication while adding strength.

How big are these motors? And where exactly do you want to put them? Maybe you wrote that already and I overlooked it.

# 25
![[Pasted image 20220522160706.png]]

They're 9.55cm long and 6.5cm wide. Two of them are needed in each shoulder so that it can move in x,y,z. They are common and cheap, but heavy (each one weighs 530g) and noisy. But I don't really care about the noise.

 # 26
 Okay, thanks. That's not small but also not that huge. So she might be able to lift 4kg using both arms, which is sufficient. Noise might later be mitigated using quarz sand or other material, noise cancellation or some sound overlay.
 
 # 27
 This kind of servomotor can be purchased upto a torque of 380kg.cm. It obviously costs more, and Ryan Gross recommends servos rated at 110kg.cm+ for the full-size Proto1 arm, so this 180kg.cm is probably overkill but they were on offer so I went for it. I'll probably use a couple of 380s eventually. However these very strong motors are used to drive the wheels on 1:1 scale RC cars. So I if I make a programming error my robowaifu may inadvertantly crush me to death. Maybe I can become the first recorded case of death by robo-snu-snu?
 
  # 28
  ![[Pasted image 20220522160742.png]]
  
  Well, the Protolite hand is very nearly finished. The only problem I'm having is with that little blue micro servo that is supposed to flex the thumb left and right. I was stupid and bought a small pack of what are very probably counterfeit TowerPro micro servos from some Chinese supplier on Amazon. They make excellent finger-burners, but are otherwise useless. Gonna be more careful who I get them from next time!
  
  # 29
  Wow, that's quite an improvement you've made there Anon. If you keep going on like this, you apparently will come up with a state-of-the-art robowaifu arm/hand design. Go, go, go! :^)
>finger-burners

I'm unfamiliar with that concept

# 30
LOL I noticed that while the rest of my servos operated normally, these would just heat up where the 555 timer is. One of them even melted through the external casing. So to prevent them getting too hot, I hold a finger over the bottom every time I test them. Hence the "finger burner". This happens even at just 5V so not sure what the problem is. Just a helluva lot of resistance and heat coming from somewhere in the servo driver circuit. Gears move okay when checked manually.

# 31
Great work, and thanks for sharing.
I looked up the servos in the forearm: http://www.jx-servo.com/en/Product/STANDARD/SD/555.html

Did you or the original creator consider to put them in a line, so the arm would be thinner and longer? Is there a reason not to do that? They are circa 4x2x4 cm, so five would be 20 cm, which is a bit much, but four would fit that way.

Also, how much will the fingers then be able to hold and lift? How is it calculated, considering they're connected to strings? Seem to be quite strong...

# 32
My pleasure anon! The original creator (Ryan Gross) positioned the forearm servos like that because the next part up the arm is another 20kg.cm servo which connects to the back of the forearm case (effectively the wrist is above the forearm rather than below). 

You could change it so that the 4 servos are all in a line, but you need a gap between each servo for the mounting tabs+wires. By all means download the Protolite arm from Sophie's file repository and experiment with the .f3d file in Fusion360, but I reckon you'll end up with overly long forearms. TBH I am still working on shortening and downscaling the joints because the rest of the arm is still too long for the size of my robowaifu. She's only a little lady, but then that makes her parts easier and cheaper to prototype.

# 33
Oh yeah. The hands can definitely hold light things like cups, a comb, a toothbrush etc. I have to find some rubber pads for her palm and I'm going to squeeze silicone caulk on the inside of the fingers to make the hand more grippy. Then hopefully she will be able to hold heavier things such as my socket wrench. The "ligament" material is BZS monofilament 40lb (18.4kg) clear fishing line. It is very strong, stronger than the ligaments in my own fingers. 

So it's just the weakness of PLA biopolymer coupled with the relatively small size and torque rating of the forearm servos that limit grip strength. If you were to 3D Print the forearm in ABS or Nylon and maybe scale it up 20% or so, you could definitely fit more powerful servos in. Then your robowaifu would have an iron grip!