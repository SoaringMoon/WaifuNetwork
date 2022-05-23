# 1
What programming language would suit us and our waifus best? For those of us with limited experience programming, it's a daunting question.
Would a language with a rigid structure be best?
Do we want an object-oriented language?
How much do ''you'' care about wether or not a given language is commonly used and widespread?
What the fuck does all that terminology mean?
Is LISP just a meme, or will it save us all?

In this thread, we will discuss these questions and more so those of us who aren't already settled into a language can find our way.

# 2
>>128
I'm hardly an unbiased developer, having worked in C++ professionally on and off for 10 years now. I consider it the world's most flexible language, and it's probably also the single most important language today for AI--an area obviously of much importance to /robowaifu/. I've used a few other languages in my career and hobbies, but C++ is certainly my favorite one. While not the most ''ideal'' language for a beginner to start with, it can be done, and if you begin with it then you will both understand the 'machine' very well, you also won't believe in 'magic' the way Python and other languages will feed you.
>How much do you care about wether or not a given language is commonly used and widespread?
Well, it certainly has an impact on the widespread availability of developers out there, and thus the likelihood of them connecting with us who might express interest in developing robowaifus. There are approaching 5 million professional programmers in C++ today, and every single one of them care about performance. I personally consider this a vital differentiator for the potential for success in devising our own robowaifus, but again, I'm hardly an unbiased source.
>>12

Python is probably the single language with the most promise for a beginner IMO. It's widely used as a general language and scripting tool for admins. It's used all over the sciences now, especially in combination with the R platform. It's the scripting API for Tensorflow (the single most important Deep Learning framework today). The downside is that if you ever decide to go deeper into programming and actually '''understand''' how everything works, you'll have to spend quite a while unlearning the belief in 'magic' that Python will inevitably force on the beginner.
https ://www.python.org/

Scala is probably a very good choice for a beginner as well. Kind of a mashup of several languages, it lays a great foundation for functional programming in general.
https ://scala-lang.org/

# 3
I have minimal experience programming. I've dabbled with Python, HTML, CSS, and know very little beyond the very basics.
That being said, I'm not afriad to go in any direction I see fit, and I work well under a steep learning curve if the topic at hand interests me.
With that in mind, no languages are off the table as far as I'm concerned. Only problem is I have basically no fucking idea about what language I should really use.
If it helps narrow things down, I'm not concerned with the hardware aspect of things at the moment. I'm just concerned about making the personality, and I'm looking to have her be an emergent system. The more heavy lifting I can offload to the computer, the better. I also want her scope to be easily expandable.
For instance: let's say I've already succeeded in getting her to be fairly competent, and I want to see if I can get her to play a game to test her capability for logical reasoning. This hypothetical game is a game that I didn't program myself. I'll want to build that bridge as easily as possible.

On a final note, both logical reasoning and abstraction tend to come naturally to me, but usually from weird angles.

>>130
Kek, you posted literally right as I was finishing typing all this shit.

# 4
>>131
>Kek, you posted literally right as I was finishing typing all this shit.
Heh, synchronicity.

TBH, you're dealing with a question I think every guy who wants to learn programming for real faces. I can probably give you some ideas about the theoretical basics, and general architecture questions. But truth be told, I think like a C++ developer, having done it now for all these years. I dove into it intentionally, and ultimately because I wanted to create both AI and robots. But even if I hadn't had that as a long-term goal in life, I still consider it to have been one of the better choices I've ever made. It's paid many bills, and there are lots of well-paying jobs out there for talented C++ devs.

AMA, but in the end you'll still be faced with the original conundrum anon: You still have to decide. This will probably means months (years?) of serious research and trial and error. You've stated that logical thinking comes easy to you, so that should ease the process for you.

# 5
>>132
I guess the two biggest questions I have for you right now are:
1 - In regards to my previously posted concerns about expandibility, how does this play into the equation? Is C++ a good language for that, is it something that can be done with just about any language, or am I looking for something that doesn't really exist?
2 - I should have mentioned this earlier, but both of my servers use archaic architectures (Alpha64). If at all possible, I want to incorporate those into my designs. Essentially this would mean having them mostly do behind-the-scenes number crunching, and little else. Of course, I also have a modern desktop which is considerably more powerful, so it's not a matter of life or death, but the inclusion of those servers is ideal.

# 6
>>133
tbh, you'd have to very explicitly and specifically define your meaning of the word 'expandability'. To me the word naturally connotes 'flexibility' and as I've already stated ITT, IMO C++ is literally the most '''flexible''' language in the world. Several other languages have been literally written using C++ underneath, to give you some idea.

However, 'flexibility' definitely doesn't equate to 'developer productivity' which I suspect is actually closer to your underlying definition of the word. As with other areas of engineering, everything is a tradeoff. Other languages may make you more productive at the cost of flexibility. In other words, if you can accomplish exactly what you want and achieve all the engineering requirements in a particular language, then you're ahead--as long as you don't need to change that scope later.

This kind of knowledge honestly takes years to acquire.

BTW, iirc correctly GCC supports Alpha architecture, so probably any front end language it supports will be OK with it's compiler. C++, for example. YMMV, so you'll have to confirm this specifically. I'm unable to. If you can a 'hello world', then you should be good. EG, file named main.cpp :
```cpp
#include <iostream>
int main() {
  std::cout << "Hello World\n";
}```

compile & run with:
```cpp
g++ main.cpp && ./a```

If you see 
Hello World

then you're golden.

# 7
>>134
hmm. looks like newlines don't render inside code tags. :/

# 8
>>134
Certainly food for thought.
By "expandability" I mean: Taking a program I wrote, and making it do something that wasn't accounted for in the original code.
As an example, let's take my general plan for developing the presently hypothetical AI.
I will probably just have her start out as a really basic chatbot that can read large datasets. But later on, I will want her to be able to interface with other programs. This may include: playing a game, crawling the web for more data, maybe even communicating with different AIs that other anons programmed.
I might also want her to have a graphical interface later on. I will even want her to be able to make her ''own'' programs at some point.
One thing I will certainly want to do over time is optimize and adjust the way she parses data, and at some point have her be able to do that herself.

Of course, I won't be jumping straight into all that shit from the get-go like a maniac. Version 1.0 is going to be so basic that she won't even be able to count to potato. But I will want a language that makes the process of adding random shit like that as easy as possible.

# 9
>>136
Heh, I was following you right up until the very last sentence.
>But I will want a language that makes the process of adding random shit like that as easy as possible.
You were describing again and again the need for incredible flexibility, and C++ certainly fits the bill. Then at the last second you jumped all the way over to the other end of the spectrum and made ease of use the priority. C++ definitely ''doesn't'' fit that bill heh.

See what I mean? Everything in engineering is a tradeoff. Using well-defined approaches to software engineering can reduce dependencies on specific language features somewhat, but has it's limits. The language choice for a project often dictates the limits of what can actually be accomplished, practically speaking.

I'm not trying to overcomplicate things, honestly. Real-world engineering is already complicated af all by itself.

My instinct is you should try Scala anon. It will give you a great learning platform, both flexible and powerful, yet pretty easy to use as well. If in the end you find you need even more power **and you will, i'll bet** then you'll have a smooth transition to an even more flexible and powerful platform like C++ .

BTW, I may be 'logging off' before long, but I'll be back and answer anything else later on.

# 10
>>136
Also BTW
**Nano best gril**

# 11
>>137
When I said "easy", I wasn't really thinking my words through. I apologize.
What I really meant was that I want a language that's built to do the kind of shit I described, as opposed to something super rigid or limited that I'd have to use fucky workarounds with.

Also, I briefly spoke with one of my professors earlier today about it (though not in so much detail).
His recommendations were: C++, R, or Clojure. He also mentioned another language I can't remember the name of that's supposed to be C++ on steroids or something.

# 12
>>142
I see. Well, there's certainly no magic 'make robowaifu' button to press anon. As with Sir Isaac, I'd recommend you stand on other's shoulders the way we all do. Find an opensauce project that's sort of close to what you imagine, then start digging. Build and run the system as is. Start tinkering around with it. With any luck in a few weeks or months you'll have a good idea what makes it tick and then you can start over from scratch and use your own ideas instead. 

There simply is no replacement at this time for human ingenuity in the software engineering field. It's a very creative process after all.

>R
Not sure how that would serve very well in a general sense for our endeavors anon. I could be wrong, but it's not something I would recommend you pursue atp.
>Clojure
Wouldn't be a bad choice, if rather esoteric. Scala has most of the good things about Clojure and is far more mainstream, as opposed to academic.

>'C++ on steroids'
Hmm, can't say I've ever heard of that. C++ literally ''is'' pure steroids, almost by definition.

# 13
>>145
**I really wish we had more than just three people here, it's hard to get fired up in a ghost town**
I already have a somewhat abstract plan of attack. Study a language, make a bunch of tiny programs and fuck around with features as I do so, study existing examples of AI, make note of interesting things, repeat ad nauseam until I get to the point where I feel like I can write something basic that is only 99% terrible, and build up from there. I have no delusions of this being any less impossibly difficult and time consuming than I'm imagining.
At this point, as far as I'm concerned, it's a choice between C++ or Clojure. I'll sleep on it and make my choice in the morning. Whatever I choose, I'll shell out some shekels for a few books and just get into it.
If I don't force myself in a direction while there's still a fire under my ass, then it'll be a long-ass time before that fire comes again.

# 14
>>146
>I really wish we had more than just three people here, it's hard to get fired up in a ghost town
There's the Meta thread for discussing such topics anon. I personally need just the internal vision in my heart of literally millions men dispossessed by the evils of feminism to give me the motivation I need. For me it's literally a spiritual issue.

# 15
>>146
>repeat ad nauseam until I get to the point where I feel like I can write something basic that is only 99% terrible, and build up from there.
Heh, sounds like a plan. :^)

Yeah, it's important in life to move while you have momentum anon. Whatever you decide on, I'll try to help you to the degree I can.

# 16
>>147
>>148
The three people %% possibly 4, I don't know if you are including me. %% are loyal men to their brothers in arms. I am glad I found a small wholesome community like this where we can freely share ideas between each other without the fear of losing our jobs or being grounded by our parents.%% (^: %% I mean this in the most literal sense, I love this community. Also when you guys get time, I wanna speak about something concerning in the meta thread. 

Sage for off topic

# 17
>>146
I plan to set up my box with Clojure and follow along with you anon, so hopefully the guys get code tags working properly here soon.

# 18
>>161
>that pic
lol nice

# 19
>>175
I got it from /b2/ on the final days of 8chan before it was shut down. It's a little scary to think about. I guess it's kind of like reading a German news paper from early 1945...

# 20
I'm back, and I decided to go with C++.
Clojure was certainly tempting, being a LISP dialect with full Java support and a growing corporate userbase. In the end though I coudn't deny the far superior wealth of support and documentation that already exists for C++.
Bought a guide for learning it, and a book about algorithms because I have a feeling I'll need that down the line.

# 21
>>190
OK, sounds good. AMA I should be able to help you with C++ and using it well. ''May or may not'' be able to help with original algorithm designs. OFC the C++ bread already has important links not the least of which is getting familiar with the book list maintained over on stackoverflow. Welcome aboard the coder train anon. May we have robowaifus in our hearts and homes soon!

BTW, you'll need to figure out a good editor that you can be comfortable with soon.

# 22
I hope your C++ studies work out for you anon.

# 23
>>130
This is good advice. I'd modify it slightly to say that a true novice should cut their teeth on Python (I hear that Python The Hard Way is a good primer) and then add some C on embedded systems - preferably something real-time - before touching C++. Python, "magic" and all, has the main advantage of laying down fundamental patterns of thought, and time-sensitive embedded C gets you close to the machine so that Python's abstractions won't damage long-term development. All learning consists of telling lies to small children; the trick is knowing when to take the lies away and replace them with the next, slightly less untrue set. In any case don't learn with JavaScript and definitely don't touch PHP until you have several better languages under your belt. I've observed that people who start with either of those two languages seem to suffer some kind of brain damage that carries over insufferably into other languages.

Clojure is also a decent choice as a first functional language. Functional experience pays dividends in any language. I hear that "Clojure for the Brave and True" is a good primer.

Don't neglect your tradecraft. Learn version control early. Understand how to collaborate with your future and past selves. Learn what good, disciplined thought feels and smells like and what sloppy thought feels and smells like. The Jargon File is a decent source of tips on developing your mindset, although some of it must be understood in its historical context.

# 24
>>428
>All learning consists of telling lies to small children; the trick is knowing when to take the lies away and replace them with the next, slightly less untrue set.
heh, creative way to word that anon. Great advice overall. What can I say, I love C++. I make no bones about it tbh. I learned C first, and wish I hadn't. If I'd had Ch27 of Stroustrup's PPP2 back then I would have both understood C better, and would have much more quickly transitioned to C++ thereafter.

Anyway, thanks for the advice and the tips. That kind of post helps out here a lot.

# 25
>>428
>The Jargon File
Thanks anon.

# 26
>>134
Could you please tell me the browser and OS you made this post on? Thanks.

# 27
>>539
Chromium derivative & Ubuntu.

# 28
>>428
It's funny, but I keep rethinking back to your words anon, especially the "Understand how to collaborate with your future and past selves." bit. That idea is helping to guide me in how to choose better function and variable naming, how to refactor code out to stay focused in the 'inner core' of a program, and generally how to do better architecture of my stuff. Thanks for the tip anon!

# 29
>>1271
I am glad that the words helped you, but don’t thank me, Anon - thank Master Foo: http://www.catb.org/~esr/writings/unix-koans/prodigy.html

>“Moving in accordance with the law of nature, it unfolds inexorably in the minds of programmers, assimilating designs to its own nature. All software that would compete with it must become like to it; empty, empty, profoundly empty, perfectly void, hail!”

# 30
>>1272
very nice, here's one for you anon (though regrettably you'd probably have to get the 'made-from-atoms' version to enjoy it.

www.goodreads.com/book/show/106728.The_Timeless_Way_of_Building

# 31
Some lisp and AI related books:
>Structure and Interpretation of Computer Programs (SICP)
Book: https://mitpress.mit.edu/sites/default/files/sicp/full-text/book/book.html
Lectures: https://www.youtube.com/watch?v=-J_xL4IGhJA&list=PLE18841CABEA24090&index=1

>Paradigms of Artificial Intelligence Programming
Book and code: https://github.com/norvig/paip-lisp

>Practical Common Lisp
Book and code: http://www.gigamonkeys.com/book/

>The Common Lisp Cookbook
Book: https://lispcookbook.github.io/cl-cookbook/

>Clojure For The Brave and True
Book: https://www.braveclojure.com/clojure-for-the-brave-and-true/

>>128
>Is LISP just a meme, or will it save us all? 
Lisp is good for learning (Scheme and SICP) and it allows one to build working programs fast (Clojure and Common Lisp), in addition, lisp has been traditionally used in AI programming.

>How much do you care about wether or not a given language is commonly used and widespread? 
It's important that the language...
1) is tested and that it actually works
2) has a community, so you can get libraries, tools, learning resources and help
lisp (Common Lisp and Clojure), java and C++ are examples of languages that fulfill these requirements.

>What the fuck does all that terminology mean?
Object-oriented programming (OOP) just means that the language support one particular way of programming. nowadays, OOP is most widely used in the industry but functional programming is gaining a lot attention lately.

# 32
>>1322
Thanks for the links, Lisper-Anon.

# 33
This is an open-ended question so feel free to respond with your own opinion or thoughts.

As I understand it, compilers are continuing to improve to the point where even very savvy coders have a hard time beating them. So if a higher level programming language still compiles to fast code, then what are some advantages of using a lower level language in the context of AI and robotics?

# 34
>>1515
Well, I'm no expert in compiler design, and for the men who are, the phrase 'higher level programming language' applies to C and basically everything else outside of assembler or actual machine code.

You're making what is a mistake atp of just lumping everything into black and white. 'Very savvy coders' can probably implement a 'better' generic programming implementation than say, C++ template meta-programming by hand-writing assembler, but that would come with a few trade-offs;
-1. It would only be for a specific example, whereas the high-level meta-programming approach is fully generic.
-2. It would require months of the developers concentrated effort to produce a more performant version than say, GCC right out of the box.
-3. It would only work on a specific type of CPU, for example Intel or ARM.
-4. It would be a bitch to maintain that code after the fact (IMO).

So yea higher-level languages like C++ are certainly 'better' than low-level languages in that case.

Further, I'll presume the question is related to the common perception of 'higher-level' **and please define that explicitly w/o using 'well, kinda like Haskell, you know' heh**. While there are literally millions of professionals programming in C++ daily for a living, most amateurs consider it some a small niche thing (and therefore automatically both difficult and not worth learning).

Python certainly has more popularity and is considered higher-level. Examples of it's use abound in the sciences. But you certainly wouldn't write a 120fps FPS using it. In engineering, everything is a trade-off, and there's no free lunch--only elegant and inelegant approaches.

I use Python and C++ specifically because of OP's topic ITT: What programming language would suit us and our [robo]waifus best?

TensorFlow is arguably the single most import AI ML/DL framework right now. There's rather a good user API for the tool using Python. But the engine itself isn't written in Python, but rather in C++ (there's also an API in that language too ofc). TF performs metric shittons of intensive math operations and you definitely wouldn't be too happy with the performance if those were done in Python instead of C++. Yet calling ''into'' the C++ code w/ Python is a great idea.

Each language has it's place and there are definitely still quite wide performance gaps between very mature, highly-optimizable languages like C, C++, and FORTRAN, and modern coffee languages like Python, JavaScript, and C#, when performing math-intensive operations like performing tensor calculus on billion-cell matrices.

# 35
I don't think it's a good idea to advice beginners today to learn C++ as a start, bc its seems to be hard to work with. Python is what many scientists and beginners use. We'll need to glue different existing programs together, we won't write them completely on our own. For that, Python is the way to go. Speed only matters in some cases, btw.

# 36
>>4338
I understand your point Anon, but honestly, C++ isn't that hard to learn if you focus on the proper essentials. The problem is there's such yuge boatload of terrible, terrible educational material on C++ out there. It's really given guys the wrong impression of the language imo. I hope to correct some of that with the TDD.
>Speed only matters in some cases, btw.
Maybe in a general-purpose app or program. For practically the entire spectrum of software engineering related to robowaifus, ''speed is king''. We literally will not be able to solve this domain successfully without well-written C & C++ programming. 

But yes, once the core engines are written and debugged, then adding in Python scripting on top of that will be suitable ofc.

# 37
>>4358
>I hope to correct some of that with the ''RDD''.*
derp.
>>3001

# 38
>>4358
The engines for everything I can think of are general purpose, other people are using those and are working on improvements. 
Could you give me any example where we need fast software which isn't used outside of this project? 

Btw, there are ways to make Python code faster if necessary, same for many Lisp variants. However, I have no intenion to start one of these famous fights about programming languages here. I never tried CPP really, had no reason so far.

# 39
>>4376
>Could you give me any example where we need fast software
Two words, Anon:  
Hard Real-time
**OK maybe that's 3 words heh**

There is literally nothing that is software controlled inside a safety-critical system (such as a Gynoid Robot expected to be around naive humans like children, for example) that isn't absolutely dependent on (billions of) calculations being done not only properly, but within a hard-limit time budget.

I can go on about this for a while, but to save some time, do a little research of your own on those two words first Anon, and then come back and ask further ITT.

# 40
>>128
Good day fellow robo-lover!
In reality, if we consider waifus to be both hardware and software, then there will be several groups of languages used:
-Low-level languages such as architecture-specific assembly, C, maybe (unlikely) C++, which will be needed for embedded controllers with limited RAM and processing power.
-Languages that will be running within an OS environment for machine-learning, bigger data proccessing etc. Those could be C++, Python, Go...you name it XD

Coming from an electronics background, I think the topology of the waifu bot should be:
-Simple, minimum driver code for interfacing to the hardware which by itself can execute a set of actions/steps
-Higher level system for managing the overall state of the bot by aggregating data via APIs
-I'm not fond of IoT, so I'd prefer the network connectivity to either not be present, or disconnected from the hardware control.

I'll always recommend starting with C, just because it forces you to study the underlying architecture. However you should learn from a guide/book (like Ken and Ritchie's C) as learning it on your own is more frustrating without enough background.
If you want to focus on higher level, I'm not sure what to offer. I use Python, but as mentioned earlier, it hides a lot from the beginner.

# 41
>>4403
>However you should learn from a guide/book (like [Kernighan] and Ritchie's C)
Here's the bookcover. You literally cannot be involved in the C community w/o running into this.

# 42
>>4405
Hehe
It's a well written book (though I've only read the first two chapters and usually use the others for reference).

Also, perhaps you chaps might point me to the right thread, as this a little off-topic. If there's no thread I could create one.
I wonder if anyone considered using alternative CPU architectures (i.e. not x86/amd64 or Arm) to make sure the waifu bot runs on an open architecture where the documentation can be readily acquired. For me this is important from a security perspective (Intel ME...) because a waifu bot is a very personal object and may be able to acquire a lot of info about you.
I was once hyped about RISCV until I heard some open source projects struggling to get the necessary changes added to the standard (Libre-SoC). OpenPOWER might be interesting as it is well established.

# 43
>>4406
We are very concerned about the botnet issues here, both from security and privacy perspectives. We don't have a specified thread, but it is touched on in our SBC & microcontrollers thread.
>>16

Please feel free to start an entirely new thread on the topic Anon if you feel qualified. Since this is such a technical topic, if you wouldn't mind make it an effort-post OP, detailing both the hazards of commodity processors, maybe something about the efforts in the alternative communities so far. Plenty of links always help round out a good OP ofc.

Thank you.

# 44
>>4407
Sure, I'm quite busy on weekdays, but I'll see if I can do a little write-up for the weekend.
I'm glad I found this place, as for once I can have a serious conversation about implementing waifuswith current technology, not just wishing and hoping!
Thanks!

# 45
>>4406
BTW, this might be a good post to introduce to newcomers.
>>2701

# 46
>>4408
>Thanks!
You're welcome. Glad to have you here.

# 47
>related xpost
>>6712

# 48
Here's something that might be useful. It seems to be picking up a lot of adherents. Nim

https://nim-lang.org/

It's supposed to be easy to use like python but has a lot of advanced features without so much complication. Some features.

It has macros which can make programs rewrite themselves according to situations and is supposed to raise productivity if you know how to use them. Macros are a big deal in LISP and C++.

It can compile itself or to C or javascript. It has more than one level of garbage protection and memory protection so you can dash off stuff to test then advance speed by allocating memory yourself if what you wrote works well.

Seems like something easier to use than C++ and LISP but more useful than python without being so big.

# 49
>>8524
Python is very common in science and education, though. It also has a lot of libraries, and speed isn't always a matter. However, I wanted to try out NIM for a while now. If it  becomes popular here, I'm quite sure I will do so.

# 50
One thing is that if we're going to have different languages interacting then the language that will make this happen is C.
Additionally, robowaifus are cutting edge tech, so we won't be able to cut ourselves some slack with convenient off the shelf hardware and operating systems, we'll have to deal with purpose-built hardware and software which inevitably comes with odd behaviors and optimizations, and to create and make use of those knowing the theory behind assembly is required, so that when the hardware pops up an assembly programmer will already know all about memory models and vector instructions and whatnot and be able to pick up programming for this new hardware with just an instruction set listing.
Why are soundcards cheap? Because inside them is a DSP with a native word size of 24 bits and which can only read and manipulate data in that one size, it also has weird instructions that optimize reading an array in an unusual order common in DSPs, not a full-blown ARM core that's made with many more millions of transistors providing features a soundcard will never use. 
Similarly, the average router until recently had a MIPS CPU with no floating point unit, floats aren't relevant for router tasks.

At this point the whole range of programming languages is required somewhere. Straight up machine code, compiled languages, and scripting languages.

Focus on theory, general experience, and topics related to robowaifu engineering. Whatever you know will likely be of use somewhere.

# 51
>>8608
>At this point the whole range of programming languages is required somewhere.
This Anon gets it. We're going to be having all sorts of hardware too. Probably broadly divisible into mobile (ie, onboard the robowaifu) and immobile.
>mobile:
At least three types and probably more:
-edge sensors/actuators. Neuromorphics wants to both combine these together and push large numbers of them out to the edges of the robowaifu.
-microcontrollers. Shepherds after a fashion directing all those edge devices, and reporting up and down the chain with the SBCs.
-sbcs. The mobile 'brains' that will manage most of the heuristic-type work for the systems. Ofc, they will stay in touch at least intermittently with the immobile resources.
>immobile:
At least 3 types of systems, probably more:
-servers for data, mostly big storage devices.
-servers for AI training, lots of GPU horsepower.
-gateway systems for securing and defending the rest.

On top of that is typical networking, etc. already common in anon's homes.
>tl;dr
We'll all need a lot of different types of software in the end. So, just make a choice and dive in.

# 52
I'm probably going to look into this at some time: GraphIt - a domain specified language for graphs. https://graphit-lang.org/  
https://youtu.be/ptIVf-YlkhY
It outputs C++, but optimizes the code based on search algorithms for graphs. Or something like that, lol.

# 53
My two cents being an delivering Waifu Engine. Which the renderer is built with C# using unity, then the AI core is built with Python.

With Python learn the basics, then learn about what duck typing is vs every other language type system. 
Then learn how to work with a team by building a domain language around how you communicate.
Worst case scenario you end up with a job, but the best thing about Python is there are many resources if you get stuck.
A lot of languages like CPP and Lisp or Haskell there are few resources. 
I know this because I came from a Haskell background, and used it to parallize data workflows using DAGs.

You want the language that will have the lowest barrier of entry, any other language will discourage you as a learner. Theres a lot to learn in programming, though the mental models transfer over to other languages, you just need to learn the details and nuances.

# 54
>>10495
Thanks very much Anon, I'll look into it!

>>10497
>You want the language that will have the lowest barrier of entry, any other language will discourage you as a learner. Theres a lot to learn in programming, though the mental models transfer over to other languages, you just need to learn the details and nuances.
I absolutely agree with this notion for a true beginner. 

But compiled languages like C & C++ bring a critical robowaifu engineering requirement to the table. Namely, '''efficiency & performance'''. Because these two compiled languages output machine code that is actually quite close to mirroring the actual underlying hardware (at least when well-written), they don't unduly introduce artificial energy-consumption and wall-clock hits.

And particularly for physical robowaifus where ''Energy is everything'', keeping battery drain low is absolutely vital. C & C++ both handle this like a boss.

# 55
Common Lisp would be the best option, however you'll need at least some level of proficiency with it to actually use it effectively, which is why something simpler would be better.

# 56
Fast.ai will use Swift for Tensorflow in a few years, and already uses it in some paces under the hood.  For now they advice using fast.ai and Pytorch to beginners. https://youtu.be/XHyASP49ses

>>10553
I have experience in some Lisp, and will go on using it and learn more dialects. However, it always depends on the job, because of libraries and such.

# 57
>>128
Probably a more advanced set of programming than what we already have with c++ and machine code with manufacturing machines to make the waifu have perception and be able to not try to punch a hole in a wall trying to reach for the remote.

# 58
>>12329
So, have any productive suggestions Anon, or just plying dystopic imagery here?

# 59
>>12335
You clearly don’t anon

# 60
>>12329
this isn't resolved via language but mechanical strength stepping via complex algorithm
tl;dr there's a reason we as biological organisms have adrenaline and super strength when we are under its effects. In a clam relaxed state we are "Weaker" but this is why we don't constantly injure ourselves or break tools and utensils. This is also why we have superior fine motor coordination and dexterity relative to other primates (who have superior strength and power). 
Our R/Ws are going to need to have different types of actuators for soft touch versus when power is needed (to lift, walk, jump, etc). Otherwise a missed line of code would result in a hole in the wall or worse a sensitive part getting pinched or ending up seriously injured. Simply put, when a R/W is in intimate mode, turn off hydraulic/strong pneumatic actuators and only run e/m servos, solenoids (with resisting springs, counterweights, etc) and nitrile fiber. When R/W has the "all clear" to do outdoor type activity, resume full power. 
Just one example. Anyway probably belongs in the actuator thread >>12131 or another thread but I've been sitting on this concept for a while and wanted to type it out before it's lost.

# 61
>>12361
It's a good point that we'll need multi-level forces within our robowaifus for them to work properly for us Anon

# 62
A good, actually very good alternative would be Forth

https://en.wikipedia.org/wiki/Forth_(programming_language)

Forth was designed when computers had very little memory or power. It's very concise and is productive in an environment where speed and close to the hardware work is needed. It's very small and fast. One of the big benefits is it is made up of words that can be combined. So once you write a routine you can use the word to preform and action. It's used for all kinds of task that demand productivity, speed and are based on limited one of kind type programming jobs or very specific hardware. Look it up I think you will be impressed.

There is also a version for ESP32 microcontrollers which I think look to be some of the most powerful best cost versatile microcontrollers built today.

# 63
>>12859
Interesting. Is it low-level enough though? We'd need direct access to hardware resources via pointers to do many to the practical things we'd need to to build software for a robowaifu. I know C & C++ offer this, and I'm ''pretty'' sure that Ada and D do as well. There are probably others, but tbh there are pretty solid reasons that C & C++ absolutely dominate the systems programming world. And it's not b/c politics or power really, but that '''other''' p-word; P**ointers**.

# 64
>>12951
>Interesting. Is it low-level enough though?

Yes. Forth used to be, not sure now, THE language that motherboard manufacturers used to boot the computer and set up all the hardware for the OS.

It was originally invented by this guy to run a big science telescope.

When micro-processors had limited memory and power Forth was used a lot because it's small and very versatile.

# 65
>>12951
>Pointers
"...A compiled Forth program is a collection of words, each of which contains a statically allocated list of pointers to other words..."

"...Forth programmers traditionally value complete understanding and control over the machine and their programming environment. Therefore, what Forth compilers don't do reveals something about the language and its use. Type checking, macro preprocessing, common subexpression elimination, and other traditional compiler services are feasible, but usually not included in Forth compilers. This simplicity allows Forth development systems to be small enough to fit in the on-chip ROM of an 8-bit microcontroller. On the other hand, Forth's extensibility allows "full-featured" systems to consume over 100K bytes and provide comprehensive window-based programming environments. Forth also allows (and often encourages) programmers to completely understand the entire compiler and run-time system. Forth supports extremely flexible and productive application development while making ultimate control of both the language and hardware easily attainable. ..."

http://users.ece.cmu.edu/~koopman/forth/hopl.html

Since most waifus will revolve around passing messages and reading positions you don't need any large OS. So forth is likely good for waifus.

# 66
>>12981
Wow sounds like a pretty compelling position Anon. I'll plan to make time at some point to have a go with it. Thanks.

# 67
Here's a link to the history of forth and should give a better idea of it's strengths and weaknesses.

https://www.forth.com/resources/forth-programming-language/

# 68
One more forth link. It's microForth which is written in C so it's portable. If you search for microForth you get manuals.

https://github.com/Earlz/microforth

This is just one there ar emany Forths because it's so small people write their own.

# 69
>>12986
Thanks Anon I'll look into it.

# 70
>>13025

To be fair I need to point out some disadvantages. The way it's constructed you have to think about what you are doing. Modern languages have a ton of programs written already so a lot of it is just stringing together already written code. Forth you will write a lot of it yourself. Since it's a little different it might be harder to read and figure what's going on.

My perception is that Forth is kind of like LISP, not that it's any way LISP but since it's a little different and takes some thought to  get things going people have a harder time with it. Meaning that it doesn;t grow. It's the same as comparing C++, C, Python and then HTML you have less people able to make good use of these in turn because the level of thought is a little higher in each case with HTML being much easier to grasp than C++.

To end on a high note building waifus is not likely to have a lot of ready to burn code for it so Forth is a fast way to prototype and build working devices. The other languages that are easy to use like Python and Java will be too slow and C is too cryptic and liable to errors frequently.

# 71
>>13027
"Meaning that it doesn;t grow."

Strike that out. I have no idea even what I was trying to say there but that's not right. It happens sometimes you start a sentence thinking about one thing, stop then when you continue you don't tie it together then miss correcting it when proof reading.

# 72
>>13028
Heh, no worries Anon it's fine. We all do that. :^)

# 73
I've been a C/C++ programmer for 5 years. While the languages are excellent at low-level abstraction work, they come with a number of unignorable safety issues. A language that is designed to be safe from the ground up, can do everything C can do, and just as fast, is Rust. 

Rust is not easy to learn, but it has an already large and growing community with many resources.

# 74
Just want to throw this in here as a reminder to myself, that I might have to learn Haskell:

Swish is a framework, written in the purely functional programming language Haskell, for performing deductions in RDF data using a variety of techniques. Swish is conceived as a toolkit for experimenting with RDF inference, and for implementing stand-alone RDF file processors (usable in similar style to CWM, but with a view to being extensible in declarative style through added Haskell function and data value declarations). It explores Haskell as "a scripting language for the Semantic Web".

Swish is a work-in-progress, and currently incorporates:
Turtle, Notation3 and NTriples input and output. The N3 support is incomplete (no handling of @forAll).
RDF graph isomorphism testing and merging.
Display of differences between RDF graphs.
Inference operations in forward chaining, backward chaining and proof-checking modes.
Simple Horn-style rule implementations, extendable through variable binding modifiers and filters.
Class restriction rule implementation, primarily for datatype inferences.
RDF formal semantics entailment rule implementation.
Complete, ready-to-run, command-line and script-driven programs.

Though, the development has currently stalled: https://hackage.haskell.org/package/swish

# 75
>>13847
Did you compile in --release mode?

# 76
C and Scheme.
C for power and speed, generally minding the machine as low level languages do.
Scheme for simplicity, ease of use, and speed of writing the code, as well as convenience while ignoring the machine's details.
Not that Scheme is slow or C is hard, but that is where one beats the other.

These are well designed languages with standards, high quality implementations, and which are widely supported. They're also the languages used in many good books that could be used for self teaching.

Forget jobs, forget what people use, forget what companies use, forget what has the frameworks for webshitting, forget everything else but this question: which are some good programming languages? C and Scheme tower far above all else.

# 77
>>13850
>look at this ruffle code
That's a fast and well optimized DoS resistant hash function (1). While it's not the same, you can find similar assembly with a sip hash in C at -03 (2, hashmap_sip). Ruffle is slow because it's a proof of concept and not feature complete, it says so in the readme (3). I'm not sure why you have a problem with stack pointers, is it panic unwinding the call stack? You can disable that for embedded programming (4). If you would like to learn panic-free Rust, I found a neat guide that was written for you (5).
(1) https://github.com/tkaitchuck/aHash/blob/master/compare/readme.md#Speed
(2) https://github.com/tidwall/hashmap.c
(3) https://github.com/ruffle-rs/ruffle#project-status
(4) https://docs.rust-embedded.org/embedonomicon/smallest-no-std.html
(5) https://docs.opentitan.org/doc/ug/rust_for_c/

# 78
>>13877
I'm another anon. I barely know anything about that stuff. I wonder what you think of other languages compiling to C. I recall some version of Scheme doing that and I also Dylan: http://www.cs.cmu.edu/~gwydion/dylan-release/docs/htdocs/d2c.html
I always wondered how good the code of such languages is and how hard it would be to update their behavior to create better code.

# 79
>>13883
why would you compile to c? you wouldnt get any performance benefit since the problem is the way the code is written, heavily abstracted languages just dont translate well compared to c, you cant just rip out the abstraction unless you were coding without it in the first place, just look at c--, its basically c yet c-- is almost always slower than c, only because idiomatic c-- is stupidly more abstract and the retard oop mentality promotes an inefficient way to write code, translating those abstractions like oop into procedural code ( which is the only real way a computer works ) is inevitably going to produce inefficiency and bloat
you can still optimize with c in another language though, most languages have ways to call external c functions precisely for optimization, just look up "c call in (language)" people usually just write performance critical code in c, compile to an object file or shared library, and call it from from inside the program, python scripts do this all the time because of how slow python is
you could probably go further with the optimization, I know c and c-- have inline assembly too, so you can optimize on the hardware, I dont know every language but I assume other languages would have this too or at least a way to link a custom object file during compilation or with a shared library

# 80
>>13884
>you wouldnt get any performance benefit since the problem is the way the code is written
What?!? Benefit compared to what? Do you honestly believe compiling some high level language code into C doesn't make the resulting code faster? If so, then I'd like to see some sources. 
>you cant just rip out the abstraction unless you were coding without it in the first place
You lack fantasy and I'm sure this is wrong.

# 81
>>13887
Why not use Java?

# 82
>>13887
do you not know how a compiler works, all compilers just compile to assembly, theres nothing special about the c compiler its only better at optimizing only because c code is way more explicit and deterministic with the least abstraction from assembly, your giving the compiler so much information to work with that theres little guessing for the compiler, thats all code is, youre just instructing the compiler what you want to do and it figures out the assembly for it and optimizes it, the c compiler just demands more for less, higher languages do the opposite more abstraction, more implicity and less code, its easier to write but the compiler has more guesswork to fill in the blanks and figure out what youre trying to do
compilers for high level languages are already specialized around optimizing implicities and the guesswork required,  trying to compile an abstract language to c is just as difficult as trying to compile it to assembly, your not going to outperform the regular compiler unless you actually rewrite abstract code to be less abstract and less implicit, the only way to do that is to just use a more expressive language

# 83
>>13900
You're comparing coding in C to compiling from some language into C. That wasn't the question. Let me in peace with your nonsense. No one will write everything in C. That's is even dumber than writing everything in C++. This might be a sabotage attempt and if so, it will not succeed.
We generally need no flameware on languages here. This thread should be about languages and their use case. Righ tool for the job and so on. For most of us it's going to be Python and maybe some variant of Lisp and specialized languages for specific use cases.
I know that programs written C, C++ and other languages can be embedded into high level code or being called by other programs, which is exactly why I won't write in any of this till I need it. Then there might be languages which compile down to C, machine code or bytecode, whatever. Case closed, goodbye

# 84
>>13906
Yeah it's enough, I wrote that already. Im even not going to read this. The question in >>13883 is still open, but you're not willing or capable to answer it. And I don't need it answered here. You're just picking fights fot trolling. Should be moved to the basement later.

# 85
GraphQL is a query lanuage, it might be interesting for creating APIs between different internal databases. It seems to be popular with the web crowd and it's open source. https://youtu.be/8l7TxqWI1XA - It helps clients to only aks for specific data and get that, especially useful if data comes from different sources.

# 86
>>13923
The other language I'd like to bring to your attention is Grakn: https://en.m.wikipedia.org/wiki/GRAKN.AI
>Grakn is an open-source, distributed knowledge graph database for knowledge-oriented systems. It is an evolution of the relational database for highly interconnected data as it provides a concept-level schema that fully implements the Entity-Relationship (ER) model. However, Grakn’s schema is a type system that implements the principles of knowledge representation and reasoning. This enables Grakn's declarative query language, Graql (Grakn’s reasoning and analytics query language), to provide a more expressive modelling language and the ability to perform deductive reasoning over large amounts of complex data. Effectively, Grakn is a knowledge base for artificial intelligence and cognitive computing systems.

# 87
>>10565
>Fast AI, Python, Swift
>>13539
>Rust
>>13826
>Haskell
>>13883
>Scheme, other Lisps, Dylan
>>13923
>GraphQL
>>13926
>Grakn

Ignore the trolling. Stay focused. Use the best tool for each job or the one you get along with.

# 88
>>13958
more like an inflatable hammer
it looks solid and shinny, it looks useful, you start thinking about all the things you could build using that hammer
then you pick it up and realize its just full of air and utterly useless

