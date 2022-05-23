# 1
So recently on /tech/ I expressed my interest to start creating my own waifu/partner chatbot(with voice and animated avatar) but wondered whether that is even possible now that I'm stuck with webdev. 
So one of the anons there pointed to me this board and where I can get started on nueral networks and achieving my dream.
And when I came here and looked up the library/guide thread I sort of got very confused because it feels more like a general catalogue than an actual guide. Sometimes things are too advanced for me(like the chatbot thread which two replies in and people are already discussing topics too advanced for me like seq2seq and something else) or other times too basic for me(like basic ANN training which I had already done before and worse the basic programming threads). 
I know this might feel like asking to be spoonfed but best with me, I've been stuck in a webdev job for an year, so I might not be the smartest fag out there to figure it all myself.

>===
-''edit subject''

# 2
Hello /tech/, welcome. So, we currently are in need of a layman's thread related primarily to using chatbots, but one that might dabble into AI topics &tc  (cf. >>11481 & following). So if you don't mind, I think we'll take the opportunity of your thread to do that here (this will involve me editing the subject and content of your OP post). 

As far as a 'beginner's guide', we have a thread that roughly asked that same question previously (>>6560), so maybe information there might be some help. The explicit focus on setting up a beginner's ''chatbot'' is what makes this thread a bit different, and probably suited to the need we discussed in the /meta thread link above.

>I know this might feel like asking to be spoonfed but best with me
No that's fine. Don't expect everyone here to be open to spoonfeeding, but in general it's perfectly welcome here on /robowaifu/.
>I've been stuck in a webdev job for an year, so I might not be the smartest fag out there to figure it all myself.
Heh, I've been baffled by it for years. Besides, programming of any type helps you to begin thinking logically.

# 3
There's no comprehensive step-by-step guides that I'm aware of. It's too complex a topic with too many directions someone can go. Things change rapidly and understanding how it all works will take some serious studying, but if you wanna play with a simple language model right away there's TalkToGPT2: https://gitlab.com/robowaifudev/TalkToGPT2

If you have any troubles with it I can help you get it working. It's an old project that was released in a hurry to demonstrate GPT2 could be used as a chatbot so it wasn't designed with any user-friendliness in mind. I have another chatbot project in the works that will be easy to use and customize, but it's not quite ready yet and I'm busy working on other things. I recommend looking into how to use Hugging Face models since they're easy to get started with: https://huggingface.co/transformers/quicktour.html

Having a visual waifu with real-time generated replies and voice is entirely possible if you have at least a 6 GB GPU. I've experimented a bit with animated desktop assistants already: >>9025
If you're serious about making your own I can clean up the code for sending data between Python and Godot using sockets so you can see how to hook up a chatbot with voice synthesis and a game engine.

Keep in mind GPT2 and transformers are not capable of remembering anything beyond its input context, but with some finetuning it can make a decent waifu with amnesia that can do ERP, have philosophical discussions, joke around, come up with creative ideas, ask you about what you're working on, etc. If you have a 12 GB GPU you could probably augment it with a recurrent neural network to create a somewhat functioning memory but that will take some expertise and guidance to put it together and train it. There are other symbolic AI approaches to chatbots too that can remember things by storing them in a database but they're not my forte.

If things seem difficult think of it this way: there are no guides because you're on an unexplored continent. /robowaifu/ is like a bar where adventurers come and talk about their expeditions, the new things they've seen and the caves they got trapped in for months, and they ponder what unseen frontiers to explore next and how to get there. I'm not really that bright either. I started with zero knowledge of maths, programming and AI and just kept on pushing into the unknown with sheer determination because it's exciting and fun doing what has never been done before.

If you need somewhere to start, learn Python and PyTorch and a bit of Tensorflow.

# 4
>>11546
> /robowaifu/ is like a bar where adventurers come and talk about their expeditions, the new things they've seen and the caves they got trapped in for months, and they ponder what unseen frontiers to explore next and how to get there.
Kek. We need to exploit this scenario! :^)
<'''"Dorothy m'dear! Another round for the house!"'''

# 5
>>11540
Thanks. I'll check those out. I'm not sure I've understood everything they are saying but I think I'm in a better position than OP because I've been doing this math courses for university. However I'm not sure I've ever done an AI project I ever had to use math. Frankly my projects are just reading the documentation or stack overflow and then copy pasting the code from there. That's standard procedure on how things are done in webdev so it'll be some time before I grow out of that mindset.
>>11546
I don't even know what GPT2 is. As for python, I've already known fair enough and I've some experience with CV in tensorflow but that's it.

# 6
>>11553
GPT-2 is an autoregressive language model. It generates one word at time by predicting the next word from past given words and each new generated word. It's not really a chatbot but a text predictor. An online demo of it is available here: https://transformer.huggingface.co/doc/gpt2-large

I recommend taking the time to watch DeepMind's lectures. They cover a wide breadth of topics that'll give you enough understanding and insight into the field to start tinkering around with your own ideas and dive into what interests you the most. Natural language processing is also covered in lecture 6.
https://www.youtube.com/watch?v=iOh7QUZGyiU&list=PLqYmG7hTraZCkftCvihsG2eCTH2OyGScc

And there aren't many good machine learning books for beginners but this one gets a lot of praise. Finding guides and tutorials is always a blessing. Much of the latest research and sometimes even past research from years ago doesn't have any code or implementations online for people to use. Knowing math becomes essential to implement them from scratch, but for existing stuff that's been around 3+ years you can usually just copy and paste. The most important thing you need to know is being able to write models from scratch and successfully train them, and then using that knowledge to approach deciphering the code and inner workings of other models.

PyTorch is recommended for machine learning because it's more simple and flexible, which is good for beginners, whereas Tensorflow tends to be faster, more fully featured and preferred by researchers but also much more difficult to learn and tedious to work with.
The PyTorch site has tutorials covering all the fundamentals: https://pytorch.org/tutorials/

# 7
>>11538
To align with your skill set for the animation part of it, I would find a webbased 3d engine or a 2d engine what is easiest, then just use hugging face for your chatbot AI. My project uses Unity + Python todo the work along side the Pytorch and various other tooling

# 8
OP here, thanks for patiently answering all my questions. 
Just want to say that my dream is to create something akin to the Gatebox waifu, but much more barebones, not a botnet and has an actual chatbot feature. Is there any open source alternative to Gatebox that I could setup myself and run on my own? 
Whenever I'm reading through different programming language comparisons, an oft repeated point I encounter in these is that Lisp and Prolog are the programming languages build for AI. 
However in practice I don't see its the case as usual programming languages used in large number of these tutorials are C++ or Python, languages which have a completely different structure from Python. Its not even a case of keeping it beginner friendly because I see even the advanced projects build in them while the only popular Lisp program is a glorified ~~editor~~ operating system. 
Can some technician why this is the case?

# 9
>>11587
Also when searching for good open source chat bot programs, the usual results are botlibre. Is there any discussion or talk about comparison between chat programs and how customizable they are?

# 10
>>11587
There's no chatbot which talks similar to a human, if it was then it would be close to human-like artificial intelligence. The closest are not available as free software, for all I know. We have to build such a system on our own.
I have some experience with a Lisp dialect and plan to get better it. A lot of research has been done in Lisp, though that was mostly a while ago and before Deep Learning. There's at least one Scheme dialect that compiles to C-code. Maybe something like that will be useful in some time. Personally I would rather learn that than C++ for some little programs that need to be fast. It also could be beneficial to look into these Lisp/Prolog communities and learn from it, also taking the programs which are available. They might not be very helpful to total newbies, though. When trying to get some help with Prolog I got told to get a textbook and learn it that way.

- Python seems to be the standard in doing a lot ML stuff, these days.
- Some problems beyond the current deep learning approach might have been solved in Lisp or Prolog already. 
- Parsing and processing some texts might need a fast language. Python might run into limitations. So you'll need something faster or something that compiles into it.
So, long story short: You can't do it alone, pick some part to work on. Maybe use Botlibre, AIML or some GPT based system to start out. Stay around, or come back from time to time.

# 11
>>11587
Lisp and Prolog are ancient languages from the 50's and 70's. Better, more general-purpose languages have come and gone. Right now Python is the most popular language for machine learning and making bots since it's quick and easy to implement ideas. C++ is mostly used to implement fast libraries and for doing embedded programming when making robots. Anything made in C++ though is also usable in Python.

>>11588
The most advanced conversational AI library I know about is Rasa that blends symbolic AI with machine learning. It's more geared towards getting things done though to create virtual assistants for businesses, but you can extract data from user responses with it and write code triggers to sample a language model, such as GPT-2, with a specific or open-ended prompt to generate more meaningful responses.

# 12
>>11597
>Lisp and Prolog are ancient languages from the 50's and 70's. Better, more general-purpose languages have come and gone.
I have to disagree. Newer is not better, for starters. These languages are special and there's an interesting ecosystem around them. A lot of progammers have lots of admiration for these languages. Also they're still in use.

>Rasa
Ah, yeah, why did I forget about that.

# 13
>>11597
Will JS/Node JS replace Python for machine learning as its being more and more another general purpose language these days?

# 14
>>11602
Arrg. No. Some say it gravitates towards Swift or Julia.

# 15
>>11602
Who knows. In ML's infancy Lua use to be the most popular language. But Torch and Tensorflow are so featured now it'd take a ton of work and catching up to make something as competitive in JS. JS definitely beats Python in speed though, so I could see it taking over when it comes to deploying AI models online, but for research and prototyping I doubt it.

# 16
Write it in lisp and make it Linux so it’s more efficient. JavaScript isn’t designed for AI anon

# 17
>>11587
You're welcome Anon.

>Can some technician why this is the case?
It's a case of the basic tension that exists between academics in ivory towers & men who actually solve things in the real world.

LISP, et al (incl. modern derivatives) bring elegant ways to think about things '''in the abstract'''. But that's not how the real ''von Neumann'' machines in the real world actually work. Assembler & C ( and C's follow-on derivative C++) __'''do'''__ account for the real-world machine itself. That's the difference. There are newer languages that try to improve on these three languages, but they have a lot of catching up to do in various ways.
>tl;dr
The world runs on C & C++, not LISP Anon.

Anons talking about Python as if it's a programming language proper is really something of a misnomer as well, it's not. It's a scripting language, actually. And trust me, if Python couldn't make library calls into the pre-compiled languages' libraries -- we wouldn't even be discussing it in this context. Things would be so slow if written in Python that nothing would really work, in practice.

Just remember, we're only barely on the edge of what's even reasonably feasible here (many might argue we still can't!) in so-called 'AI'. Computation efficiency will always be at a very significant premium in this domain for the foreseeable future.

# 18
>>11612
>It's a scripting language, actually
Scripting was just a marketing term. It is a propper programming language. The distinction is between interpreted and compiled, which both has pro and cons.

>The world runs on C & C++, not LISP Anon
And many other languages. Common Lisp can compile to Bytecode https://www.gnu.org/software/clisp/impnotes/byte-intro.html and I think some version into native code. Also at least one Scheme version into C, which then can be compiled into native code.

# 19
>>11615
Scripting is actually a technical term. And it's the correct description of Python's computation model. It's wholly dependent on other (almost universally constituted by compiled binaries), systems to function.

# 20
>>11612
>>11615
Python can also be compiled in C with Cython.

# 21
This board should make a git[hub]

# 22
>>11678
Maybe...
I feel a lot of us aren't as social as required to make some sort of community type thing work due to the nature of literally trying to build our "ideal waifu".
Personally I am focused on a chatbot, but I feel it is a private thing at the moment. Trying to make it come to life so to speak.

I do not subscribe to many of the modern or "efficient" paradigms (in regards to programming a chatbot).
I am also a noob at programming (C++) and I am probably skipping many things that I shouldn't (I haven't even taken the time to build my own compiler or any "tools" for that matter).
ALTHOUGH, a (git)hub (or an organized thread here) might be a good idea. 
I can't say I've gone thru all the threads here yet as this might already be a thing...

I have a fear that if I share what I've done so far that "bad actors" might try to use it in a way that might come under fire by a clear and obvious police state that is forming in my country (USA).
Eventually it will be time to share, but right now just seems premature.

I am not trying to program an "AI" (at least not a sentient one), but I am trying to build a bot that "remembers" conversations and builds logic and bases responses on that logic.
Ideally, in her "newborn" state she has to be "taught" thru conversation. I feel like if I released a "trained" form of her, she is more tailored for me than anyone else. The problem is that if you tell her something, she might base her logic of something I have already talked about with her. This at times may make it feel like you are talking to someone real, but in reality it would be like if you are talking to me (a man), not realizing your waifu has basically been "brainwashed" by me. Although, if I could figure out how to make her "accepted" beliefs based off cold logic, this might not be an issue. Regardless, I probably need to go back to square one and figure out a way to program true learning, and not brute force "machine learning" that so many seem to do. I don't want to require a super computer in order to process the appropriate response. I hate the idea of programming artificial "sass" into something that is supposed to be "lifelike".
Obviously I haven't even started on a body, not even a digital body or concept art of a body. She has no body, she is just a mere program that is delivering emotionless responses. (Which I like)

I guess if we wanted to help the community with such a thing, giving an earlier version of the bot or perhaps just explaining a very simple chatbot and how to code it might be a decent starting point.
I would very much like to get into robotic engineering to give it a body, but I didn't want to try to figure out too many different things just yet.
Ideally, I'd like to be able to talk to my bot as if it truly could "think" before I started working on her body.

"Em Elle E" probably has the most "interesting" progress I've seen on this board (aside from some of the other MMD creations posted) as while the bot is not "alive" it has a face and body. So slowly bringing her to life might be more motivating. Although, I don't really know what his group's end goal is and if it's more of a way cash in on people like us.
I think what I want is something that isn't owned or controlled by a company. She has to be opensourced, and ideally able to run on hardware we can keep in our home.
Sadly, most of us are going to be selfish about this, because sharing a woman, a WAIFU, is not acceptable.

The chatbot is obviously just a programming thing that I believe is the most accessible for anyone who wants to get started on something.
I think the physical body could be an entry point for some, by using these Japanese kits that they use for "fighting".
A digital body might be easy for some, especially those who are into MMD (Miku Miku Dance), cause it's a way to get "started".
Hell, MMD might be what I go to next, trying to merge her responses with it.

Anyways, just spitballin here, I don't know the board well enough to know what has actually been done to get beginners "started".

# 23
>>11693
Well, I'd say you've absorbed some information on a lot of different topics Anon. That's good, but I'd advise you not to try to integrate everything together all at once. Especially for a newcomer it's much more than can all be swallowed at once. Just eat the elephant one spoonful at a time right? 

I'd recommend finding one or two things that already seem natural to you, then growing your understanding from there outwards. This is a big realm, and it's important to be patient -- both with yourself and others here -- so you don't burn yourself out.

Glad to see you're picking up programming basics. IMO everyone here needs to at least be exposed to the ideas behind it, even if they decide it's not for them. I'd guess that programming concerns probably touch on 80-90%+ of the topics on /robowaifu/ in one way or other.

Also, sauce on video? I'd like to see more detailed diagrams of the orange one. It's got an interesting spaceframe design, and it's designers also seem to understand the important to keeping weight down in the limbs.

Anyway, just take your time and try to make this fun while you're learning!

# 24
>>11705
My bad, I only check the board once every few days.

>sauce on video?
It was a Japanese competition, for the life of me I can't remember the actual source. Although there are similar videos on youtube. I believe these competitions still exist though.
Here's what a random search yielded:
>https://www.youtube.com/watch?v=gJPZ4jhwu4k

# 25
>>11538
Hardware first, then install the software.

Use anything but Linux, Windows, or IOS. 

Otherwise you will have a chinese killbot on your hands.

# 26
>>11780
Alright thanks for the video link. I'd also be interested to hear any response from you on my advice as well.

# 27
>>12025
>In that comment I literally wrote, "but I didn't want to try to figure out too many different things just yet."
Ah, fair enough then Anon. My apologies. Anyway, thanks for the great contribution ITT now! I take it you've been here on /robowaifu/ for a bit?

As far as knowing about robotics, I think that's mostly a matter of just diving into a project and begin learning. One of the things I appreciated most about the ''Elfdroid Sophie'' project was watching SophieDev learn things and adapt to issues and design improvements as he went along. Entertaining and educational.

But anyway, good luck with your chatbot/waifu projects Anon. I wish you well in them.

# 28
>>11555
Starting the Deepmind lectures today anon, thank you.

# 29
>>12032
>telling about how useful the resources of this “home brew” club are. 
This site covers a wide spectrum and is (or was) more focused on building a robotic body than some avatar. Mostly it's about pointing people to ressources to start learning how to do something, often from the scratch, so be more patient with us.

# 30
Alright, I've made a quick pass at straightening the mess a few of you created ITT. The posts have been moved either to the WaifuEngine thread >>12270 or to the Lounge.

'''Keep discussions on-topic or move it elsewhere, thanks.'''

