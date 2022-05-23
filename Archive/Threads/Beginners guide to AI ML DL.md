# 1
I already know we have a thread dedicated to books,videos,tutorials etc. But there are a lot of resources there and as a beginner it is pretty confusing to find the correct route to learn ML/DL advanced enough to be able contribute robowaifu project. That is why I thought we would need a thread like this.
Assuming that I only have basic programming in python, dedication, love for robowaifus but no maths, no statistics, no physics, no college education how can I get advanced enough to create AI waifus?
I need a complete pathway directing me to my aim. I've seen that some of you guys recommended books about reinforcement learning and some general books but can I really learn enough by just reading them? AI is a huge field so it's pretty easy to get lost.
What I did so far was to buy a non-english great book about AI, philosophycal discussions of it, general algorithms, problem solving techniques, history of it, limitations, gaming theories... But it's not a technical book. Because of that I also bought a few courses on this website called Udemy. They are about either Machine Learning or Deep Learning. I am hoping to learn basic algorithms through those books but because I don't have maths it is sometimes hard to understand the concept. For example even when learning linear regression, it is easy to use a python library but can't understand how it exactly works because of the lack of Calculus I have. Because of that issue I have hard time understanding algorithms.
>>5818
>>6550
Can those anons please help me? Which resources should I use in order to be able to produce robowaifus? If possible, you can even create a list of books/courses I need to follow one by one to be able to achieve that aim of mine. If not, I can send you the resources I got and you can help me to put those in an order. I also need some guide about maths as you can tell. Yesterday after deciding and promising myself that I will give whatever it takes to build robowaifus I bought 3 courses about linear alg, calculus, stats but I'm not really good at them.
I am waiting for your answers anons, thanks a lot!

# 2
Just letting you know I saw your post OP. I'm one of the two you linked. I'll have to think through before giving you a reply so please be patient. It may take me a few days. The other Anon may be able to reply sooner, as he's much more versed than I am.

Good thread topic for /robowaifu/ OP, so thanks for taking the time to spell things out well in your OP. :^)

# 3
First of all save your money for hardware and use http://libgen.rs/ for free books, I find the 'handbook' series from the publisher Springer has great work on a variety of topics relating to topics this board discusses. Also you can use https://torrentz2.is/ for online courses, this is what I found doing a search for 'udemy machine learning'. Be careful when pirating as the sites linked to on that torrent search engine aren't always safe.



I'd recommend against amassing a horde of learning materials as those courses or books won't do you any good if your goals are unrealistic. Start with the basics moving to more difficult topics and constantly reevaluate your goals.

# 4
>>6561
Okay anon, I'll be waiting for your response. Thank you for sparing your time to help me :)
>>6566
Oh, thanks for letting me know about that torrent site. Looks like there are a lot of great stuff there.
>I'd recommend against amassing a horde of learning materials as those courses or books won't do you any good if your goals are unrealistic
Yeah, I figured. That was the reason I bought some basic udemy courses in the first place. Thinking about starting with ML without heavy maths and learn basic consepts such as:
Data Preproccessing, Numpy, Pandas, Inferential Stats, Data Visualisation, Linear Regression, Polynomial Regression, Gradient Descent, KNN, Model Performance Metrics, Naive Bayes, Logistic Regression, SVM, SVR, Decision Trees, Decision Tree Regression, Random Forest Regression, Kernel SVM, K means Clustering, Hierarchical Clustering, Apriori, Eclat, UCB, Thompson Sampling, Ensembling, Unsupervised Learning, NLP, PCA, LDA, XGBoost
I bought 2 courses which covers the topics above. Both of them claim to have only prerequisite of "some basic high school maths and programming". I guess that those basic highschool math topics are simply Linear Alg, Calculus and maybe a little bit of stats. Course only gives you an idea about how the algorithms works, skipping the heavy math parts and shows you how to implement it using python libraries. I thought about finishing maths and stats courses first and then getting into machine learning but I know that won't happen. I will get bored and never finish those courses if I only focus on finishing them. While studying those 2 ML courses I'll try to learn linear algebra, limits, derivatives, integrals, some trig and stats. And after finishing them I will move on to a more theory-based course which teaches you how to implement those algorithms without using libraries with heavy math. Once I complete them I will move on to deep learning with again programming-based course and then move on to the theory-based course. And then implementing stuff, reading papers, doing kaggle competitions I will get used to create projects. Maybe after that I can start to read some of the books you guys recommended.

Is there anything wrong with that approach? Pls give me some feedback.

# 5
>>6560
>Assuming that I only have basic programming in python, dedication, love for robowaifus but no maths, no statistics, no physics, no college education how can I get advanced enough to create AI waifus?
Creating a simple chatbot AI with a seq2seq network in Python is possible without any mathematical knowledge. However, it won't be very good or keep your attention long and you won't be able to improve on it until you understand how it works. At the minimum you should study matrices, calculus, statistics, linear algebra and programming. Once you have a basic understanding of those fundamental topics, then you can jump into learning whatever area of AI that interests you and focus on studying topics that are relevant to you. I'll dump some good textbooks on these later in >>235

For a deeper understanding you should also study trigonometry, discrete mathematics, differential equations, Fourier transforms, and entropy and information theory. In discrete mathematics you'll wanna pay special attention to graphs and search algorithms.

I recommend 3Blue1Brown's channel for learning mathematics: https://www.youtube.com/c/3blue1brown/playlists
He also did a really good series explaining how neural networks work: https://www.youtube.com/watch?v=aircAruvnKk&list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi

DeepMind has a comprehensive deep learning course here: https://www.youtube.com/watch?v=iOh7QUZGyiU&list=PLqYmG7hTraZCkftCvihsG2eCTH2OyGScc
And a good reinforcement learning course: https://www.youtube.com/watch?v=ISk80iLhdfU&list=PLqYmG7hTraZBKeNJ-JE_eyJHZ7XgBoAyb

Henry AI Labs explains various AI topics: https://www.youtube.com/channel/UCHB9VepY6kYvZjj0Bgxnpbw
Yannic Kilcher covers recent advances in AI: https://www.youtube.com/channel/UCZHmQk67mSJgfCCTn7xBfew
Machine Learning Street Talk is a good AI podcast talking about the interesting stuff going on in AI: https://www.youtube.com/channel/UCMLtBahI5DMrt0NPvDSoIRQ

Schmidhuber's website covers a lot of interesting topics in AI research: http://people.idsia.ch/~juergen/

>Which resources should I use in order to be able to produce robowaifus?
At the minimum you'll need to know 3D modelling, 3D printing, C or C++ programming, electricity, microcontrollers, physics, classical mechanics, servos and power systems. Someone else will have to chime in on this since my specialty is AI.

>>6567
All those courses are overkill for a start. You should focus on:
>Data Preproccessing, Numpy, Pandas, Inferential Stats, Data Visualisation, Linear Regression, Polynomial Regression, Gradient Descent, ~~KNN~~, Model Performance Metrics, Naive Bayes, ~~Logistic Regression, SVM, SVR, Decision Trees, Decision Tree Regression, Random Forest Regression, Kernel SVM, K means Clustering, Hierarchical Clustering, Apriori, Eclat, UCB, Thompson Sampling,~~ Ensembling, Unsupervised Learning, NLP, ~~PCA, LDA, XGBoost~~
The other stuff is good to know but more advanced than you really need to know unless you want to study those areas.

You should soldier through basic mathematics and statistics first, just enough to be familiar with what you have to study deeper to take on an AI project you're interested in. If you don't understand the mathematical notation (particularly around summation, products, matrices and probability) being used in machine learning courses you'll become completely lost on what to do or learn. Once you dive into machine learning you'll see how important mathematics and statistics are and won't be bored studying them when you can see how much you need to know them. It's a good idea not to learn anything unless you understand why you're learning it, otherwise you may spend years learning stuff you'll never use.

# 6
>>6570
> It's a good idea not to learn anything unless you understand why you're learning it, otherwise you may spend years learning stuff you'll never use.
This. Not OP, but thanks for the great material in your post Anon. Very helpful.

# 7
>>6570
Well, after reading your post I can clearly understand that I'll need maths, physics at the end.
>All those courses are overkill for a start.
>You should soldier through basic mathematics and statistics first
I think I will study both of those 2 courses till the end even if it is overkill. Because rather than only studying maths I would prefer dividing my time fifty-fifty and study both programming/ML and Maths. I don't know which anon you are but one of you said that he isn't good at maths or physics, he improved himself by playing around programming like a lot. I am kinda on the same train but it is pretty clear to me that I will need to learn maths and physics anyways. I believe that if I divide my time in two pieces and study maths and programming/ML at the same time by the end of those 2 ML courses I will have finished Trigonometry, Linear Algebra, Calculus 1-2, Statistics and Probability.
After that I can study more advanced maths such as those topics;
>discrete mathematics, differential equations, Fourier transforms, and entropy and information theory
as well as deep learning. This way I will have time to both improve my math and programming skills. Even though my motivation is to create a robowaifu I want to improve myself as much as I can in the field of AI. I will try to improve my programming too. Starting from today I will start with one of those ML courses and a trig course. I don't think I will be able to get into robotic stuff at least for a year. I will also spare physics for future. Maybe once I get into college for CS I can work with other engineers to learn from them about robotics.

Thank you a lot for helping, I wonder what the other anon is going to recommend me. But I think the path I should be following is clear right now. I will take one left step and then one right step so that I won't fall because of lacking skills for maths or programming.

# 8
>>6573
>>6979

# 9
>>6573
OK, Anon, I've made my birthday present to /robowaifu/ today. Thank you as your question was the spur for me to finally dig in and get this ball rolling for us. Hopefully it will be an ongoing help to all of us!

Cheers.

>>7143

# 10
>>6573
Godspeed anon! Remember to have a break if you are getting a headache! Not kind on the old grey matter, some of that stuff.

# 11
>>7214
Thank you anon! Sorry for the late reply, I've been busy studying :^)
>Remember to have a break if you are getting a headache!
I will, thank you. But I wish I hade more brain processing power and ability to focus. I put in ~4 hours daily, I can't focus more than that. I am trying to get it up to 6 hours for now. Any suggestions on that topic?

# 12
>>7374
Not that anon, but I'd say just relax and don't unduly pressure yourself. Work hard, but also take time to relax and remember the fun of why you're doing this. Just remember the old adage ''Rome wasn't built in a day'' has stood the test of time for a reason.

Keep your nutrition levels up and take regular short breaks at the very least.

# 13
>>7374
Don't study to hard, this won't make it better. Resting is part of the process. I try to follow some of the advice in A Mind For Numbers: How to Excel at Math and Science, you could also listen to as mp3 (magnet-link in textfile, book and mp3 on limetorrents.info or in the linked textfile, can't upload any of it here). You might listen to the book, while going for a walk, which would have the downside of not being able to make notes, though.
https://files.catbox.moe/2bvsmk.epub
https://files.catbox.moe/tcm2is.txt

# 14
Stolen from Twitter for us here. Mainly overviews. Cheat sheets will follow.

# 15
More...

# 16


# 17


# 18
Think I got the last few from here: https://www.datasciencecentral.com/page/search?q=cheat+sheet

The last one is an example how to make a list of ressources related to a topic and then learn it step by step, not trying to understand it at the first try.

# 19
Thanks for all the effort Anon, much appreciated.

# 20
Collection of 50+ cheat sheets collected from the web: https://www.theinsaneapp.com/2020/12/machine-learning-and-data-science-cheat-sheets-pdf.html

# 21
>>8247
Thanks!

# 22


# 23


# 24


# 25


# 26


# 27


# 28


# 29
Okay, thanks. That's the better way to do it.

# 30
>>8256
Y/w. There's still the pdfs to get if you're interested.

# 31
Here's a good example for a little lecture on how to understand some AI problem better: https://nitter.dark.fail/svpino/status/1357302018428256258#m - I saved it as a pdf, no idea if that's usefull, but that Nitter instance might not be there forever.

# 32
>>8447
Neat, thanks Anon.

# 33
Posted on Twitter by data scientists.

# 34
>A curated list of awesome, free machine learning and artificial intelligence courses with video lectures. All courses are available as high-quality video lectures by some of the best AI researchers and teachers on this planet.
>Besides the video lectures, I linked course websites with lecture notes, additional readings and assignments.
https://github.com/luspr/awesome-ml-courses

# 35
>>8495
Thanks! That's a lot of content. It would be great if we can find someplace to keep this stuff safe off of Youtube somewhere.

# 36
Has anyone here read the book "Artificial Intelligence: A Modern Approach"? Any thoughts on it?

# 37
>>8609
Not yet, but noted in case I haven't already. I guess I downloaded and noted the name of reading material which would take me 10yrs or more to read and work through, though. I'll start with anything beyond simple chatbots, image and voice recognition when I mastered all these basic things, and the stuff I'm already working on, and when have a functional female body which needs to get smarter. Which will be the case in 5-10yrs, I hope.
Related: Uploaded file and https://github.com/aimacode

# 38
I'll probably go with that, as soon as I have the time:
>Dive into Deep Learning: An interactive deep learning book with code, math, and discussions, based on the NumPy interface.
>Implemented with NumPy/MXNet, PyTorch, and TensorFlow
>Adopted at 175 universities from 40 countries
>Each section is an executable Jupyter notebook
>You can modify the code and tune hyperparameters to get instant feedback to accumulate practical experiences in deep learning.
http://d2l.ai/

# 39


# 40
https://github.com/aaronwangy/Data-Science-Cheatsheet

# 41


# 42


# 43
>>9266
> #1
That actually helps me understand that term a lot better now. I still don't understand the implications of one way or other, but at least I kind of have an idea what it means now.

> #2
I know exactly what that is -- personally -- but I can also add that eventually you'll holistically put everything together in your head if you just ==keep moving forward==. Don't quit and you'll succeed.

> #3
Somehow, I can understand an idea when it's represented graphically like that, rather than a bunch of 'indecipherable' math symbols of a formula. I don't think I'm alone in this either.

> #4
LOL. Surely this is a simple thing to pick up over the weekend. R-right, Anon?
**:^)**

# 44
>>9274
Tha last pic is more about  having an overview and being aware that there's more than deep learning. In some cases another thing might work better or be good enough but easier to archive. It's also useful to use these terms to look for videos to get an idea about something. Maybe it fits to a problem that one wants to solve.

# 45
>>9278
Makes sense, thanks Anon. It's a big field.

# 46
> completely removing the background of a picture (robust PCA) 
> PCA's main goal: dimensionality reduction.
>You can take a bunch of features that describe an object and, using PCA, come up with the list of those that matter the most.
>You can then throw away the rest without losing the essence of your object.
https://nitter.dark.fail/svpino/status/1377255703933501445

# 47
>>9375
That's pretty powerful. I imagine glowniggers are using this idea extensively for surveillance isolation. Not only would this work with a 'pre-prepared' empty background plate for extraction, but a separate system could conceivably create (and keep updated under varying lighting conditions, say) an 'empty' plate from a crowded scene simply by continuously sweeping the scene and finding areas that don't change much frame-to-frame. These blank sections can then all be stitched together to create the base plate to use during main extraction process. Make sense?

Ofc, a robowaifu can use this exact same technique for good instead to stay alert to important changes in a scene, alerting her master to anything she sees that might be an impending threat, or even take action herself to intervene.

Simplification is the key to both understanding, and to efficiency in visual processing and other areas.

# 48
>>9375
PCA explained in StatQuest
https://youtu.be/HMOI_lkzW08
https://youtu.be/FgakZw6K1QQ
https://youtu.be/_UVHneBUBW0
https://youtu.be/oRvgq966yZg
https://youtu.be/Lsue2gEM9D0
https://youtu.be/0Jp4gsfOLMs

# 49
Related: GPT-2 for beginners >>9371

# 50
Illustrated guide to transformers, a step by step introduction: https://youtu.be/4Bdc55j80l8

# 51
This could also fit in the math thread, but it's notation used in ML.

# 52
>>6560
Heres a wholistic beginners understanding all that you see, the framework that people take for machine learning is to build a mathematical function that can make a prediction. That mathematical function can be created in many ways, at the end of the day its supposed to provide you with a value of some kind that you action, or output.

More recently that function is created using deep learning = parametric system that learns how to capture data and create regions between high dimensional datapoints, to segment partitions of that data to do classification or make predictions through regression, obviously there are many other way to this these are the high level constructions.

I would suggest you buy grokking deep learning by Andrew trask, he gives you  a really good deep insight into DL,

In practice however, a lot of the algorithms we use supplement DL techniques we generally use some older ML algorithms and Feature Engineer through PCA or various other Engineering techniques.

# 53
10 Must-Know Statistical Concepts for Data Scientists: https://www.kdnuggets.com/2021/04/10-statistical-concepts-data-scientists.html

# 54
>related crosspost (>>10613, >>10614)

# 55
>>10607
Thanks very much Anon! Bookmarked.

