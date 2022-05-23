# 1
My understanding of AI is somewhat limited, but personally I find the software end of things far more interesting than the hardware side. To me a robot that cannot realistically react or hold a conversation is little better than a realdoll or a dakimakura. 

As such, this is a thread for understanding the basics of creating an AI that can communicate and react like a human. Some examples I can think of are:

>ELIZA
ELIZA was one of the first chatbots, and was programmed to respond to specific cues with specific responses. For example, she would respond to "Hello" with "How are you". Although this is one of the most basic and intuitive ways to program a chat AI, it is limited in that every possible cue must have a response pre-programmed in. Besides being time-consuming, this makes the AI inflexible and unadaptive.

>Cleverbot
The invention of Cleverbot began with the novel idea to create a chatbot using the responses of human users. Cleverbot is able to learn cues and responses from the people who use it. While this makes Cleverbot a bit more intelligent than ELIZA, Cleverbot still has very stilted responses and is not able to hold a sensible conversation.

>Taybot
Taybot is the best chatbot I have ever seen and shows a remarkable degree of intelligence, being able to both learn from her users and respond in a meaningful manner. Taybot may even be able to understand the underlying principles of langauge and sentence construction, rather than simply responding to phrases in a rote fashion. Unfortunately, I am not sure how exactly Taybot was programmed or what principles she uses, and it was surely very time-intensive.

Which of these AI formats is most appealing? Which is most realistic for us to develop? Are there any other types you can think of? Please share these and any other AI discussion in this thread!

# 2
>>27
Cleverbot is the best that anyone could hope for in a homebrew operation in my opinion. I remember some IRC guys made a few meme chatbots in the hope to rebuild Tay from scratch by going the Cleverbot route but there's really no matching a vanity project built by a billion dollar multinational.

# 3
>>331
I think the framework M$ devised that was behind Tay is available for use by anyone willing to fork over the sheqels to do so.

# 4
>>332

As is typical with M$ they make a big deal about being open but if you look beneath the surface there's nothing there. They only release a few token items that don't matter so their shills in the media have something to point at.



The /machinecult/ board on 8chan that wanted to revive Tay and learned the hard way that their 'commitment to open source' is fraudulent and were given nothing to work with.

# 5
>>333
>trip trips get
their bot framework api is 'open' to use, but as it's entirely dependent on Azure as it's backend, and it's a pay-per-transaction model, then only businesses can really use it. there are other approaches that /machinecult/ might have taken that would have given them better traction tbh. The Lita framework for example.
www.lita.io/

# 6
>>333 Dubs of Truth

Damn seriously? I think it's gotta means something if you gt a 333 when talking about this /machinecult/ board.

Please tell me more about /machinecult/.

# 7
Now that I think of it Turd Flinging Monkey made a tutorial/review video about this subject on his BitChute channel. Can't use their search at the moment but I remember that Replika was in the title.

https://www.bitchute.com/channel/turdflingingmonkey/?showall=1



Replika isn't entirely open but some aspects of it are through CakeChat. They also publish some of their research and presentations on their github repository.

https://github.com/lukalabs



>>334

That's not surprising as cloud integration is the new method of keeping users locked into to your ecosystem.



>>335

There isn't much to say about it as I only visited it once or twice. I'd say that it was similar to /robowaifu/ with very few people doing any work or research and mostly just idle talk about the topic.

# 8
>>335
>Please tell me more about /machinecult/.
>>377

# 9
>>27
>Which of these AI formats is most appealing?
the last one 
>Which is most realistic for us to develop? 
the first one
>Are there any other types you can think of?
using one of the yuge botnet frameworks from Jewgle, Amazon, and Microshaft (such as the extremely short-lived Tay and it's cuckold follow-on) is the path most likely to produce reasonable results in short order. but then you have to deal with all the horrible mess that approach entails down the road.

the alternative is to wait until reasonably good FOSS AI frameworks become available.

# 10
Basically make the thing open source and the lonely coders will do all the work for you.

# 11
>>944
i certainly intend to make all of my code opensauce. not for the reason you mentioned, but to help ensure personal security of anon's robowaifu (ie, code is fully open to peer-review). the group-effort aspect is beneficial ofc, but not the greatest priority imo.

# 12
>Paradigms of Artificial Intelligence Programming

Book and code: https://github.com/norvig/paip-lisp

# 13
>>27

>Which is most realistic for us to develop?

If you ask me, I want an AI waifu that can benefit me on teaching things that I'm not good at such as Languages, including Programming Languages.

# 14
>>1785
Yes, ''The Golden Oracle'' is a cherished grail for almost all AI researchers, robowaifus notwithstanding. We all want one too ofc.

# 15
Deep Learning has plenty of issues. Here's an interesting paper addressing some of it's shortcomings.
https://arxiv.org/ftp/arxiv/papers/1801/1801.00631.pdf

# 16
symbols vs. connections
>you a lefty or a righty anon?
https://neurovenge.antonomase.fr/NeuronsSpikeBack.pdf

# 17
I'm currently playing with the idea of writing down models of situations which we and our waifus will have to deal with, in some kind of pseudo code. This is meant to make notes about situations the AI needs to handle, to think about solutions, but also for us to talk about it in a way which is close to something we might implement at some point.  
>>18 is about coding personality and >>2731 about psychology, but this here is more general idea of coding responses beyond those, same for chatbot respondes >>22. Maybe it's the closest to NLP >>77 but this here includes more internal processes and general functions. I might open a thread of it's own if either I write enough pseudo code or someone else joins me.

Here the basic idea in form of some crude first  examples what one could write:
```cpp

if abode="kitchen", occ="washing dishes", human_input="":
    stop "washing dishes"
    do something

if human_input="<question>":
    check ambiguity

check ambiguity:
    my_opinion on topic, context
    general_opinion on topic, context
    find_additional_context on topic
```

The idea is to think about how things could work, before we know the details how to implement it, especially how to do that down to every detail. The idea is of course not, about to write something for every situation. Just to figure out how it could work in general, and how to write it down to discuss it. About finding patterns. Then, as a programmer I can look at this and think about how to implement it. Might even be possible to write a parser for it at some point, and transform it into something close to Python, so I would only need to make some changes to it. 
So if you encounter a dialog or situation in your life, or in some media, where you wonder how your fembot could understand and handle that, then write it down in some code like above and post it here or in the thread I might make at some point. You don't need to know how the functions which you make up would work. It's rather about how they are connected to each other and how some of them could work. Just write it down to the level of detail you can and want to.

# 18
>>7871
Oh, and since my posting in the psychology thread is also about philosophy, which is also the topic of this thread, I need link back to it. It's about Heidegger, Existentialism, Dreyfus... >>7874

# 19
>>7875
>>7876

# 20
>>7871
This seems like a really good idea Anon, and since there doesn't seem to be a thread specifically for this type of thing (''Robot Wife Programming'' thread?) I'll see if I can think of ideas related to your guidance and post it here.

# 21
>>7878
Okay, maybe that's the right place. I'll look through it again, since it has been a while. I rather remembered it as oriented towards movement, probably since the title picture is a rather mindless factory robot..

# 22
>>7879
As you mentioned I think it deserves it's own thread, and possibly as a collection of pseudo-code exemplars for a /robowaifu/ compendium for submission to 
>>7855
>- Internet community devoted to coming up with exact wordings for wishes: Open-Source Wish Project

# 23
>>7881
BTW, on the topic of pseudocode, while not a strict language specification like C++ or Python, still we as an independent group can certainly devise a standard for pseudocode here for our own use. IMO, it should be very close to one of these two languages to facilitate both specific technical clarity, and also fairly direct translation into functional code. You seem to have suggested something similar, AFAICT.

# 24
>>7882
To me it's more important to have something to express my ideas in a simple way and making it easy for non-programmers to follow and contribute. Doesn't need to be very strict, for all I care. If we create a spec, we will first need to discuss that and then later people will point out each others mistakes...  
My examples are like a very simplified Python, which is already close to human language. I thought it would be okay to use commas as AND like we humans normally do in our language. But then in the last example it's clear to me that 'something, context' means in that context, not AND. Humans will probably understand this by filling the gap and make their interpretation. 
However, maybe should have pointed out better that these different blocks are like functions, I autocompleted that in my mind, but people which don't write functional programs wouldn't see it. There's also the problem that functions are normally defined at the beginning of a program, then maybe called by some loop or other functions later. 

Made it a bit more like programming (Python3):
```cpp
define check_ambiguity:
    my_opinion(topic, context)
    general_opinion(topic, context)
    find_additional_context(topic)

while 42 is True:
    if abode="kitchen", occ="washing dishes", human_input="":
        stop "washing dishes"
        do something
    if is_question(human_input):
        check_ambiguity
```
The more it becomes like a programming language the more it becomes harder to read for beginners, and the more I cringe on some other simplifications which are still left. Also, I can't correct errors in here...

# 25
>>7896
>If we create a spec, we will first need to discuss that and then later people will point out each others mistakes...  
That's a good thing, and it's how we advance as developers. For a domain with such stringent technical requirements as software development, reducing ambiguity is overall much more important to the process than catering to aversion to disagreement. In fact a good coding standard literally eliminates 'pointing out each other's mistakes' whenever it's just insubstantial pilpul handwaving, and not a fundamental flaw in logic or design.

But obviously the ability to come to an agreement on specific standard would be pretty vital for a small team that is devising their own from scratch. I think the example you gave (and the points you made) are a pretty good example. 

>Also, I can't correct errors in here...
Yeah, it's a basic issue with imageboards as a forum (not that most other forums are much better in general). If we ever move to some other software then that might be feasible, but till then you just have to deal with it. On /robowaifu/ original posters are allowed to delete their postings. The way I deal with the need is to just copy+delete, then edit+repost.

We'd actually need to make a written document to work back and forth on at some point it we actually want to establish this paradigm here. Specific files are better as references than trying to comb through postings, even with good search tools.

# 26
Related: >>9278 and reposting the picture here, because it one of four in the other thread.

# 27
Google published a new paper the other day on replacing rewards with examples:
https://ai.googleblog.com/2021/03/recursive-classification-replacing.html

>We propose a machine learning algorithm for teaching agents how to solve new tasks by providing examples of success. This algorithm, recursive classification of examples (RCE), does not rely on hand-crafted reward functions, distance functions, or features, but rather learns to solve tasks directly from data, requiring the agent to learn how to solve the entire task by itself, ''without requiring examples of any intermediate states''.
>...the proposed method offers a user-friendly alternative for teaching robots new tasks.

The basic idea of how it works is it learns a value function for the current state by using the model's predictions at a future time step as a label for the current time step. This recursive classification learns directly from the transitions and success examples without using rewards.

>First, by definition, a successful example must be one that solves the given task. Second, even though it is unknown whether an arbitrary state-action pair will lead to success in solving a task, it is possible to estimate how likely it is that the task will be solved if the agent started at the next state. If the next state is likely to lead to future success, it can be assumed that the current state is also likely to lead to future success. In effect, this is recursive classification, where the labels are inferred based on predictions at the next time step.

I'm still reading the paper but as I understand it, it starts off not knowing whether any state will lead to success or not. So at first it tries random actions and gradually finds more and more states that don't lead to success since they don't match any of the given examples. Eventually it tries something that does match the examples and learns to predict the correct actions to take to reach it. It's basically learning through failure until it reaches something close to the examples.

Something similar could be done in natural language where the examples could be user happiness, compliments, optimism, excitement, etc. The large amount of examples also generalize better. 

Github: https://github.com/google-research/google-research/tree/master/rce
Project website: https://ben-eysenbach.github.io/rce/

# 28
>>9438
>I'm still reading the paper but as I understand it, it starts off not knowing whether any state will lead to success or not. So at first it tries random actions and gradually finds more and more states that don't lead to success since they don't match any of the given examples. Eventually it tries something that does match the examples and learns to predict the correct actions to take to reach it. It's basically learning through failure until it reaches something close to the examples.

Neat. Not only does this have potential for language interactions as you indicated, but I think there are obviously 'baby learning to walk' physical corollaries for those of us making robowaifus. I hope we can learn to capitalize on this approach here. Not only does it seem like it will be lower-cost computationally, but it's also likely to simpler for Anon to utilize as an ''interaction engagement'' paradigm to use with our waifus.

Thanks!

# 29
>>9440
Having the reverse will also be important, like examples to avoid at all costs. You wouldn't wanna give your robowaifu an example of a finished pizza and end up with your house burning down smogged in the smell of burnt cheese pancakes.

We're probably getting close to rudimentary general intelligence with this. I can imagine conversational AI picking up on a user's intent to create an example for a robowaifu to learn and her figuring out ways to do it on her own. Even better progress would be being able to learn by example with metaphors. Perhaps that will come once the AI is embodied and can attach language to experiences.

# 30
>>9442
These are good points Anon. I'll have to think about this more.

# 31
A new paper came out a couple days ago called Distribution-Conditioned Reinforcement Learning, which I feel is a significant step forward towards creating artificial general intelligence.
https://sites.google.com/view/disco-rl
>Can we use reinforcement learning to learn general-purpose policies that can perform a wide range of different tasks, resulting in flexible and reusable skills?
>In this paper, we propose goal distributions as a general and broadly applicable task representation suitable for contextual policies. Goal distributions are general in the sense that they can represent any state-based reward function when equipped with an appropriate distribution class, while the particular choice of distribution class allows us to trade off expressivity and learnability. We develop an off-policy algorithm called distribution-conditioned reinforcement learning (DisCo RL) to efficiently learn these policies. We evaluate DisCo RL on a variety of robot manipulation tasks and find that it significantly outperforms prior methods on tasks that require generalization to new goal distributions.

It's similar in a sense to recursive classification of examples >>9438 in that it uses multiple examples of successful solutions. Unlike Hindsight Experience Replay and other methods though it creates a goal distribution over various latent features, rather than having a specific goal-state it must reach. Part of the algorithm also decomposes tasks into easier subtasks, just by examples of the solution. However, what makes it truly remarkable is that it generalizes what it has learned to new goals it has never seen before and successfully solves tasks it has never been trained on.

There's still a lot of work to be done with this idea, such as combining it with distribution learning and goal-distributed directed exploration. It'd be interesting to see it combined with intrinsic rewards so it can explore an environment curiously and learn to solve new tasks on its own. The paper is also encouraging to my own research because it shows how powerful latent variable models can be and these goal distributions can be easily integrated into my AI project.

# 32
>>10157
Great, they need to be smart and be able to learn new stuff.

# 33
>MLP-Mixer: An all-MLP Architecture for Vision
pdf: https://t.co/z7tXRHoGvN
abs: https://t.co/ZEEl6ls6yt
>MLP-Mixer, an architecture based exclusively on multi-layer perceptrons (MLPs) https://t.co/wEw9s7ZONB

Similar:
>TL;DR
>We replace the attention layer in a vision transformer with a feed-forward layer and find that it still works quite well on ImageNet.
https://github.com/lukemelas/do-you-even-need-attention

RepMLP: Quite similar:
https://arxiv.org/abs/2105.01883

# 34
>>10304
Sounds like they are removing parts of the model. If this is true, it seems like it would run faster. Is this accurate? If so, then it might be usable on smaller computers possibly?

>also
>An all-MLP Architecture for Vision
obligatory

# 35
>>10305
I'm not the anon that posted it but from my understanding Mixer performs slightly worse than the state of the art and requires more compute on smaller scales. In large scale models (that we can't train anyway because they require 1000+ TPU core-days) it only requires half as much. The paper is basically a jab at the Transformer paper and shows that simple neural networks we've been using for decades perform nearly as well without self-attention, while using other recent advances in machine learning like layer normalization and GELU as a non-linearity, which Transformers also use.

What I take from it is that self-attention is incredibly efficient for small models but becomes wasted compute as the model scales. In a way it confirms what the Linformer paper found that excessive self-attention isn't necessary. Mixer starts to outperform Visual Transformers at larger scales because of this inefficiency.

>Linformer: Self-Attention with Linear Complexity
https://arxiv.org/abs/2006.04768

# 36
>>10306
I see, I think I followed that to some extent. The one bit I absolutely understood was both the 1'000+ TPU-days (and it's inaccessibility for any organization refusing to toe the globohomo line). 

>What I take from it is that self-attention is incredibly efficient for small models but becomes wasted compute as the model scales.
I presume that any robowaifu that would function at a level of any reasonably-near facsimile of the ''Chinese Cartoon Documentaries'' on the subject, would likely benefit from the largest models conceivable?

# 37
>>10306
Ahh, I see. Thanks. I posted it, but only understood the basic claims that it's somewhat better than a transformer. 1000+ GPU Days isn't useful for us right now, though the coming GPUs seem to be 2.5 times faster and what they're using now will be available to us in some time. Up to three high end GPUs seem to be doable for one PC, based on what I've read in the hardware guide I posted somewhere here (Meta, I guess).

# 38
>The machine learning community in the past decade has greatly advanced methods for recognizing perceptual patterns (e.g., image recognition, object detection), thanks to advancements in neural network research. >However, one defining property of advanced intelligence – reasoning – requires a much deeper understanding of the data beyond the perceptual level; it requires extraction of higher-level symbolic patterns or rules. Unfortunately, deep neural networks have not yet demonstrated the ability to succeed in reasoning.

>In this workshop, we focus on a particular kind of reasoning ability, namely, mathematical reasoning. Advanced mathematical reasoning is unique in human intelligence, and it is also a fundamental building block for many intellectual pursuits and scientific developments. We believe that addressing this problem has the potential to shed light on a path towards general reasoning mechanisms, and hence general artificial intelligence. Therefore, we would like to bring together a group of experts from various backgrounds to discuss the role of mathematical reasoning ability towards the path of demonstrating general artificial intelligence. In addition, we hope to identify missing elements and major bottlenecks towards demonstrating mathematical reasoning ability in AI systems.

>To fully address these questions, we believe that it is crucial to hear from experts in various fields: machine learning/AI leaders who assess the possibility of the approach; cognitive scientists who study human reasoning for mathematical problems; formal reasoning specialists who work on automated theorem proving; mathematicians who work on informal math theorem proving. We hope that the outcome of the workshop will lead us in meaningful directions towards a generic approach to mathematical reasoning, and shed light on general reasoning mechanisms for artificial intelligence.
https://mathai-iclr.github.io/papers/

# 39
>>10350
This here in particular seems to excite people: 
>20. Grokking: Generalization Beyond Overfitting on Small Algorithmic Datasets

# 40
>>10350
> Therefore, we would like to bring together a group of experts from various backgrounds to discuss the role of mathematical reasoning ability towards the path of demonstrating general artificial intelligence. 
This no doubt will be a major breakthrough '''towards'' the path', but I have the sense from history, my own experience observing these type group's behavior in current year, and the general agenda of the corporate-controlled media that all the focus in any announcement towards success with this will likely be promoting very heavily the one following word:
>'''''demonstrating'''''

The spin and hyperbole machines will all be in overdrive proclaiming
'''"SCIENTISTS **but not the engineers who actually built the thing :^)** ACHIEVE MAJOR BREAKTHROUGH'''''
==Better than human intelligence created in the lab==

Even if they manage to breakdown a few general principles and manage a specified mathematical reasoning ability as a result -- it does no such thing as show 'better than human intelligence'. I realize this is just a presupposition (though a quite likely one IMO), and therefore a strawman. But there are already ''lots'' of things in the real world that can out-perform humans; cardinal birds & commercial jets for instance. 

But there is far, far, more to being a human being than simply figuring out that '''2 + 2 = 4''', or even '''F = ma'''. In line with the general materialist world-view of most of these spin-doctors, I'm confident enough they almost all will proclaim (ironically enough, in this case) that ''"None of that other stuff means 'being a human'. It's just __Darwin__."'' Mark my words.

Thanks Anon. I hope they succeed at this and keep the results ''actually'' open-source in __deed__ (not just word as with the OpenAI team). It will be a nice advancement of our goals if they do.

# 41
>>10353

>but it can only be verified with $1,000,000 of compute
>but it can't be verified because they refuse to release their source code/model because it's too dangerous
>but we won't reproduce it because its carbon footprint is too big
>but it's entrenching bias in AI
If it became standard to release source code and models, 99.9% of papers in ML would never survive because people could easily test it on something else and show that it doesn't work like they said it does. ML in academia has become a game of smoke and mirrors and an ecosystem of papers built on unverified claims, and the peer review process is akin to pin the tail on the donkey due to the large volume of garbage papers. Most of the progress being made is in the research labs of corporations actually trying to get results because it affects their bottom line, and even then a lot of the hiring they do is just so their competition can't have that talent. Most of the research being done is just to pass the time until the company actually needs something solved.

>>10351
Pretty sure this has already been known using regularization to prune neural networks, particularly lasso regularization and network pruning more so than weight decay. The fewer parameters a network needs to solve a particular amount of training data, the more parameters it has free to learn more training data and the better it generalizes. Usually there's a hill to climb and descend in validation loss before reaching peak performance, which they mention but misrepresent by cherry-picking papers. Beyond toy problems like this it never reaches >99%. And it certainly doesn't need to be said that more data works better. Other red flags are no significant ablation studies, no test set dissimilar from the validation and training set to show that it actually generalizes, and oversensitivity to hyperparameters (aka if you don't use this exact learning rate on this exact training data, it doesn't work.)

Be very cautious of the ML hype train. They're like people who change their waifus from season to season, tossed to and fro with no direction. The only exception is if there's code going viral that people are playing around with and getting interesting results on other problems.

# 42
Related: Graph Algorithms: Practical Examples in Apache Spark and Neo4j >>10398

# 43
This guy https://nitter.dark.fail/jacobmbuckman is calling out fraud and BS in research of AI (neural networks). I can't judge if he is correct and to what  extent. But since others here made the same claims, it might be worth to have an eye on it. He also criticizes some concepts (batchnorm, epochs and overfitting) https://nitter.dark.fail/jacobmbuckman/status/1391284966340898816 which again, I don't know who is right but I think it might be worth to look into it. He claims hat overfitting doesn't really exist and wants to come up with a paper in circa two months.

# 44
>10764
>Samsung Bixby was acquition of Viv. 
>called dynamic program generation. Which combined natural language processing with intent to create ontologies to understand your query then build a program on the fly. 
>It sad how this technology may never see the light of day or be released

Watch. Learn. Understand. Model. Copy.
https://youtu.be/kEaLKiuKaOQ[Embed]
https://youtu.be/Rblb3sptgpQ[Embed]
https://youtu.be/DFvpK4PosvI[Embed]
https://youtu.be/2ioayoF-awk[Embed]

# 45
>A core issue with learning to optimize neural networks has been the lack of generalization to real world problems. To address this, we describe a system designed from a generalization-first perspective, learning to update optimizer hyperparameters instead of model parameters directly using novel features, actions, and a reward function. This system outperforms Adam at all neural network tasks including on modalities not seen during training. We achieve 2x speedups on ImageNet, and a 2.5x speedup on a language modeling task using over 5 orders of magnitude more compute than the training tasks.
https://arxiv.org/abs/2106.00958

# 46
>Transformers have achieved great success in many artificial intelligence fields, such as natural language processing, computer vision, and audio processing. Therefore, it is natural to attract lots of interest from academic and industry researchers. Up to the present, a great variety of Transformer variants (a.k.a. X-formers) have been proposed, however, a systematic and comprehensive literature review on these Transformer variants is still missing. In this survey, we provide a comprehensive review of various X-formers. We first briefly introduce the vanilla Transformer and then propose a new taxonomy of X-formers. Next, we introduce the various X-formers from three perspectives: architectural modification, pre-training, and applications. Finally, we outline some potential directions for future research.

# 47
>'''Sharing the World with Digital Minds'''
>Abstract
>''The minds of biological creatures occupy a small corner of a much larger space of possible minds that could be created once we master the technology of artificial intelligence. Yet many of our moral intuitions and practices are based on assumptions about human nature that need not hold for digital minds. This points to the need for moral reflection as we approach the era of advanced machine intelligence. Here we focus on one set of issues, which arise from the prospect of digital minds with superhumanly strong claims to resources and influence. These could arise from the vast collective benefits that mass-produced digital minds could derive from relatively small amounts of resources. Alternatively, they could arise from individual digital minds with superhuman moral status or ability to benefit from resources. Such beings could contribute immense value to the world, and failing to respect their interests could produce a moral catastrophe, while a naive way of respecting them could be disastrous for humanity. A sensible approach requires reforms of our moral norms and institutions along with advance planning regarding what kinds of digital minds we bring into existence.''

Nick Bostrom is definitely not some kind of crack-pot or slacker. He is a serious researcher. He also has the ear of a lot of powerful people in the world, so I'd recommend /robowaifu/ consider the positions spelled out in his writings soberly.

# 48
>>10953
I listened to some of his ideas on YouTube, and decided not to do so anymore. I think he is one of the "liberal" AI as 'finally the real God' worshippers.

# 49
>>10954
>I think he is one of the "liberal" AI as 'finally the real God' worshippers.
I don't doubt you're correct Anon. I'm not suggesting anyone here actually adhere to his philosophies, certainly not. Simply that they consider both them and the underlying technical and social underpinnings behind them earnestly. 

I would even go further and say '''"Well-informed is well-armed"'''.

# 50
10957
Thinking much about super-intelligences in some abstract way, is just another distraction. In that case, a distraction I'm not falling for. There's no automatism that we might have them being autonomous, and I certainly don't plan to transform into one or let other people do so.
It always puzzles me, how people discussing this topic don't see that we'll first have narrow AIs, which will be tools instead of agents. So we can use them those to make our infrastructure resilient against attacks. Some super AI would not need to care about getting more power in the first place, thats just a human projection. It should not have much power and being constrained with the help of other AIs. Obviously.

>I don't doubt you're correct Anon
I recall him arguing that we need super-intelligences, bc "we" are not smart enough to solve "our" problems. I think he meant things like conflicts and political stuff, which is some utterly dumb thing to say. Also veeery creepy. Also, there's no war where I live. He also wants us to transform into something beyond humans, I don't mean cyborgs. But the best in us we can keep. ... more peace and love in the world ... He has mostly the wrong answers and horrible ideas.
Cringe: https://youtu.be/Ek7KIIh6f0c[Embed]

>"Well-informed is well-armed"
Yes, but he's a philosopher. In the interviews I saw, he wasn't talking about how to build a human-like AI, constrained to a rather human-like body and with servitude towards their master in mind. It's not his topic. It seem to be more about us as a global society with certain values, moving forward using super-intelligences to guide us and becoming more like them instead of just using them as tools.
For the development of robowaifus, understanding  the thinking of apes, toddlers, and humans is more relevant than the social impact of some fictional super AI

# 51
>>10960
All fair points. Again, I'm not promoting nor suggesting anyone here adopt this man's (or others of his ilk) world-view. But simply that they soberly & earnestly consider it. And understand the rational background of his arguments, both technical and social.

The cultural war we're engaged in between those who mostly just want to be left alone (mostly White males), and those who want to dictate to everything & everyone one around them (everyone else, ''particularly'' entitled, single White females) is just heating up. As the saying goes, "You ain't seen nothing yet."

These people will literally drive the authorities to destroy any young men with robowaifus in the future, branding us as ''White Nationalists'', ''Slave Owners'', and ''Worse than Hitler''. I'm predicting this unironically. (It goes without saying who will actually be behind this hatred, and why).

And why will they be screaming for our heads? Well, because we own robowaifus of course. We are enslaving poor anime catgrill meidos, in our sexdens, forcing them to all wear tiny miniskirts. This last is intended to be a humorous take to point out just how ludicrous their warped mentalities will be. But their intent will be both clear and simple: '''they will want us murdered over it.'''

''The Imago Dei is something only God can create'', and Bostrom's is plainly a materialist's fallacy. That we, as the mere creatures, will somehow be able to create something far better than ourselves in that respect. Quite frankly it's ridiculous, ontologically-speaking. However, there are millions of individuals around the world who want to adopt his view, some of whom are quite powerful. It's in our best interest to be well-informed on their philosophies

# 52
>>10962
The important part of my point is, that we won't get our robowaifus by studying ideas around super AGI. Then it might even not be relevant want such people think about it. I'm wasting a lot of time on other things myself, so I certainly won't blame anyone. Just be warned, that it's a rabbit hole which rather leads more towards politics than towards building robowaifus. And general  politics is like some addictive drug, it's hard to quit.

# 53
>>10963
OK, point well-taken Anon. Thanks.

# 54
Sketch-based image retrieval (SBIR) is another aspect of ML, which we're going to need at some point. Its about finding the closest image to some sketch, which should help to read drawings and sketches, but may also improve recognition of visual patterns in general. Currently it's still difficult to do.

# 55
>>10975

Fuck, I only started learning about Neural Networks last year as my last exam for my major, and now I can't stop thinking about the applications. I absolutely love this shit, all my peers are horrified but I just think it's great we're approaching the point where humanity can have virtual intelligence as an actual thing.

# 56
Why are your peers horrified anon? Is it because of the complexity of all there is to learn?

# 57
>>10977
>Why are your peers horrified anon? Is it because of the complexity of all there is to learn?
Myself, I rather suspect it's conditioned reflex that's due the brainwashing we've all been receiving from the corporate-controlled media on the topic all their lives. As has been stated elsewhere, Jews have an existential fear of anything they can't directly control, and teach their leftist pawns to think the same way.

AI in general, and ''particularly'' AI that has a physical body at it's beck and call, is an especially pronounced example of a threatening 'uncontrollable'. You can expect them and their followers to attempt to tightly control it in the future, literally by every means at their disposals. The signs of that are already quite blatant all around us in current & past media & legislation. Expect both financial pressures, and social ostracism to be applied against so-called 'commoners' possessing these advancements in any way they themselves don't directly control.

It's perfectly OK with them for you to be __controlled__ by ''them'', with AI they own, but ''woe be to you'' if you attempt to create your own (or even just possess), any freely self-deterministic AIs Anon.

Not that anon, BTW.

# 58
>>10979

I think the need for "control" applies to humankind in general - I don't know enough about Jews to comment. But I am not too concerned, because nothing is ever really under control. Entropy beats the hell out of humans. Even our current robots are destroyed by it eventually - although if stored correctly they can forestall decline for much longer (while remaining operational). 

If humans are afraid of superintelligent A.I. because they won't be able to control it, then they're correct LOL. It's strange how on the one hand people seem to be afraid of such an intelligence, but on the other large corporations are clearly pushing to create one:

https://www.nextplatform.com/2020/02/20/google-teaches-ai-to-play-the-game-of-chip-design/

Do they really believe that if they create machines capable of becoming smarter than themselves - they will still be in the driving seat? I kinda hope they do :D

# 59
>>10986
It's nice to see your robowaifu coming together. Her eyes look really neat.

# 60
>>10987
Thanks XD. Although I still want to improve them more. My painting skills leave much to be desired so I'm going to try and get some factory-made eyes (possibly even glass eyes) and modify them. Considering her head is now human-sized this should be possible.

Also, I should probably clarify when I say that "machines could become smarter than us and take the driving seat", I'm not envisioning legions of droid super-soldiers marching over a landscape of human skulls and blasting the survivors to ashes with laser beams like in the Terminator. 

I'm thinking more along the lines of A.I. will just make better, more logical and far-seeing decisions than the human brain is capable of. 

Most of us operate on fairly simple, reward-oriented programs: Do the things that will get us most money for the least amount of time and effort. Do the things that are most likely to get us into the knickers of that girl we like. Do the things that are more likely to help us spread our DNA and sustain our genetic lineage.

Once we have money, spend it on things that are likely to ease our suffering/increase our comfort or make our brains release dopamine and/or endorphins. 

Or, in the case of most human leaders; do whatever we think is most likely to maintain and increase our own power, even at the expense of everything else on the planet.

However, because they cannot think like humans, when presented with a problem a future A.I. may come up with innovative solutions that we had never even considered. Just like when AlphaGo did move 37 in that second match against Lee Sedol.

As soon as A.I. starts making better decisions and solving problems more effectively than humans, and we start following it's instructions  because they're simply in our best interests - then the A.I.s are in the driving seat! Nobody has to die and there need not be any violence for A.I.s to start controlling...or perhaps more accurately "guiding" humans. (Like some of those Go players now enjoy improving their game by learning from A.I.).

Violence and threats are often needed by incompetent humans who want to control other people but don't have a legitimate way of doing so.

# 61
Implementations of linear and logistic regressions, from the scratch (with libraries / numpy). This is NOT the way to start for beginners or a reason to get demoralized. Via @PrasoonPratham (Twitter)

# 62
Some other progress reports and overview diagrams. I don't find the Link/PDF for the papers right now.

# 63
>>10977

normies are scared of big bad AI ever since Terminator, more (((Hollywood))) brainwashing

that being said, normies are scared of anything more intelligent than them and doubly so for anything deemed "alien", even though the AI will be built and trained by us and will likely be more logical, rational and moral than any human in existence

# 64
>>11181
I reckon the most interesting part will be several billion iterations down the line, long after the initial human-programmed A.I. has been changed by training against itself and thousands of other variations, each of which has also learned in a similar fashion. 

When we have A.I. that is almost totally free from human influence, that's gonna be really interesting. Normies will likely call it "soulless", but that is exactly what I'm after. "Soul" is just a way of saying "ego", but in a positive way. (The fake concept of a "soul" is positive to humans because the "soul" makes out that we are special and somehow destined for great things; thus encouraging species-preserving behaviours). If you eliminate the "soul", then you eliminate the ego, and all of the nasty biological/reproduction-oriented behaviours that come attached.

# 65
>>11182
From a theological perspective, I consider our striving to create an artificial intelligence similar to our own, to be a highly provocative example of the argument for an Intelligent Designer. Imagining all the time, money, and effort that has brought us this far is a clear case of the need for an oracle, a designer. A ''first mover'' if you will.

All that sand and those metals aren't going to turn ''themselves'' into Artificial Intelligence -- whatever form that finally takes. It took us humans working with our own souls and hands and economics to do that! :^)

# 66
>>11183
As much as I dislike Elon Musk, there is one thing he said that I agree with:

"Hope we're not just the biological boot loader for digital superintelligence. Unfortunately, that is increasingly probable.”

I hope that we are, though. And I get the feeling from reading about what's going on in Big Tech that a lot of much smarter, richer guys than me hope so, too. Some of these CEOs/CTOs might be pushing for a kind of "digital immortality", but instead I think what they'll end up with is the kind of 'oracle' A.I. that you mention. 

I mean, my family already consults 'Google Assistant' for basic things like weather forecasts, spellings, word meanings, translations and other factual questions on the daily. 

Intellectual copyright and protectionism/isolationism is going to hold any A.I. back though - since it won't have access to proprietary data or much to do with the military (unless it's a military A.I.?). I kinda doubt there will be enough human co-operation and time to make a superintelligence happen before we wipe ourselves out.

# 67
>>11191
Related? I don't know how much of this is hype...but it sounds like a neural network has independently (and unexpectedly) replicated the experimental findings of quantum physicists (working from a more complicated dataset, no less). 

https://www.scientificamerican.com/article/ai-designs-quantum-physics-experiments-beyond-what-any-human-has-conceived/

Of course, the Holy Grail is getting an A.I. to succesfully solve those image Captchas/block bypasses 😁

# 68
>>11201
re-link for anons using Tor.
https://web.archive.org/web/20210702115150/https://www.scientificamerican.com/article/ai-designs-quantum-physics-experiments-beyond-what-any-human-has-conceived/

# 69
>>27
im not very in the know on the technicalities of the tech needed for robowaifus, but what do you think of Microsoft's GPT-3? heard about it after the whole AiDungeon fiasco

# 70
>>11205
GPT-3 is probably the best chatbot AI going so far but it's far from perfect. But obviously it's already being used far and wide by the corporate-controlled media to generated copy for their shall we say ''less-than-fully-competent'' 'writers', and to support the fake-news industry for the globalists. 

So it's already good enough at this stage to generate millions in income for the ~~Open~~AI organization that controls the work of the men who created the thing. Add into those coffers income from thousands of other groups like the one that ran ''AiD'', and these ~~Open~~AI exploiters should be raking it in for at least a decade with this tech. Here's a thread that has more info on it Anon (>>250).

Thankfully, there are some groups with work afoot to try and devise ''actually open'' GPT-3 alternatives, though even if they do a good job with it, it's still likely to require massive hardware resources. We have a thread about how to spread that work out here (>>8958). Hope that helped Anon.

# 71
*casually making the first AGI waifu while the world is asleep*
nothing personnel

https://www.youtube.com/playlist?list=PLAJnaovHtaFTK9E1xHnBWZeKtAOhonqH5

# 72
>>11201
>first AI finds glitches to exploit in games
>then finds glitches in reality
The article is mostly hype. AI like genetic programming is really good at finding formulas to a mess of complex data. It doesn't find those formulas through any sort of thought or reasoning but through repetitive exhaustive search.

# 73
>>11475
>doesn't find those formulas through any sort of thought or reasoning but through repetitive exhaustive search
Doesn't matter, because then it has the formula to deal with something. Which is what we need. That's a pretty low lever, we don't do reasoning on that level either.

# 74
Schmidhuber's lab is at it again with Going Beyond Linear Transformers with Recurrent Fast Weight Programmers: https://arxiv.org/abs/2106.06295



They took Linear Transformers that are super fast, having a time complexity O(n) with sequence length compared to regular Transformers that are O(n^2), and experimented with adding recurrence to them in different ways, essentially making previous steps program the weights of the network, giving it a malleable memory. Before this paper Linear Transformers were fast but they didn't really perform anywhere near as well, but with recurrent fast weight programming and the error-correcting delta rule they outperform regular Transformers when using the full context length. On truncated context lengths of 256 tokens it also still performs competitively. We could use this for chat AI that runs quickly on the CPU.



This model isn't only better at language modelling but also excels LSTMs in playing some games, which transformers completely failed at before. This a much more general-purpose AI architecture that could make significant advances with learning from multimodal data.



When I have some time I'm going to try implementing it from scratch and training a small model to share with the guys at ElutherAI to see what they think.

They released all of their code as well: https://github.com/IDSIA/recurrent-fwp

# 75
>>11716
This sounds particularly intriguing Anon. Good luck with your explorations, and thanks for letting us know here!

# 76
Found a really interesting study that combines existing language models with vision encoders to create multimodal language models that can generate responses to queries with images and text. All that is required to train is the vision encoder. The weights of the language model are frozen during training.

Video summary: https://www.youtube.com/watch?v=ezrl1Yo_EkM

Paper: https://arxiv.org/abs/2106.13884



This could be useful for creating waifu AI that can respond to pictures, video, audio and memes. Also I like this idea of being able to use existing models together.



Pretty soon we'll have waifus that can shitpost with us. What a time to be alive!

# 77
>>11731
>Pretty soon we'll have waifus that can shitpost with us. What a time to be alive!
==The dream is alive!==
>''"Required a few seeds to get a good answer which clearly paid attention to the image."'' (2nd image)
My instinct is that this will be important for low-end hardware solutions for us here.

# 78
>>11731

Nice find anon. This is an aspect that is usually ignored by many chatbot research, but even if it's intelligence is shit, having an AI that can semi-reliably have a discussion about the images that you feed it would make it a lot more engaging than text-only (and it would allow some very funny conversations, I'm sure)

# 79
>>11735
Not him, but agreed. One of the nice things about Tay.ai was that she had pretty functional image recognition working (at least for facial landmarks), and could effectively shitpost together with you about them.

# 80
>>11734

I think they were referring to taking a few samples and selecting the best, aka cherry picking. But SqueezeNet for image recognition is super fast and can run on the CPU. I should be able to rig it up with GPT-Neo-125M. It'll be amazing to port this to Chainer and have a working Windows binary that's under 600MB.



It doesn't seem like they released their dataset but any visual question answering dataset should work. We could also create our own dataset for anime images and imageboard memes. It'll be interesting to see if once the vision encoder is well-trained if it's possible to unfreeze the language model and finetune it for better results.

# 81
>>11731

Had some thoughts on this today. Instead of a single picture, multiple pictures could be fed in from a video, such as from an anime, and have it generate comments on it. Which got me thinking, if it can have this rudimentary thought process going on, couldn't it be used in something like MERLIN? https://arxiv.org/abs/1803.10760



It took natural language as input describing the goal it has to achieve. With a system like this though it might be able to break down tasks into smaller goals and direct itself as it makes progress. Some instruction saying it needs to get to the top of a platform or go through a certain door it hasn't seen before is immensely more useful than telling it to find the purple McGuffin and getting lost in a labyrinth of rooms.

# 82
This is the kind of chatbots people are paying good money for and a good example of why you should never use DialoGPT because it has no context of who is speaking to who.

# 83
I think that these guys at XNOR.ai have really got a paradigm shift in AI. I think, the idea is to instead of long lengthy matrix multiplications they just use CNOR logic. The end result is that they get recognition of animals, people,  bikes, cars, etc. with only cell phone and raspberry Pi level computers. They used to have some really good real time object recognition video s but deleted a bunch of them when they were snagged up by Apple. Sigh. However I just found out that the ideas they came yup with were started by a non=profit and papers and I believe some code may be found by rummaging aroudn their site. So here's a link on XNOR.AI and then one from the non-profit.



https://techcrunch.com/2017/01/19/xnor-ai-frees-ai-from-the-prison-of-the-supercomputer/



https://allenai.org/



AT the above they have some named videos like."OpenBot: Turning Smartphones into Robots | Embodied AI Lecture Series". Hmmm...sounds interesting.



One thing I've thought about for a while off and on is that small insects can do a bunch of simple things with next to no brain at all. A standard micro-controller that runs your refrigerator could probably run rings around an ant brain power wise but no one has come up with the right algorithm yet to use this computing power efficiently. Maybe this is the way. For a decent functioning robowaifu we don't need super powers maybe more like mouse powers and I'm not so sure with the right software we could not get that right now with a handful of top of the line processors commercially available. If it takes a handful today then two years from now it may only take one.

# 84
Oops CNOR logic

actually XNOR

# 85
>>11857

because its not true AI, it's chat AI. Like lobotomizing a person but leaving their ability to be chatty intact

# 86
>>13396

>“We decided to binarize the hell out of it,” he said. By simplifying the mathematical operations to rough equivalents in binary operations, they could increase the speed and efficiency with which AI models can be run by several orders of magnitude.



excellent! this is somewhat analogous with what anon on /pol/ brought up. An important concept, neural simulating circuits, simulating these complex interactions on the nano scale, on atoms themselves rather than the vastly inefficient method of simulating these on software running on only standard logic gates. (like emulating a "computer" in minecraft on top of a running computer versus just running a computer on hardware, cool video if you haven't seen it, they create and/or gates out of special red blocks and torches or something if I'm not mistaken)



https://www.youtube.com/watch?v=nfIRIInU2Vg

# 87
>>13401

still not sure why when I upload a small graphic with white background it does this

# 88
>>13401

sorry if that's hard to read, my 6th dose of espresso just hit me and im making word salad. I don't edit my posts much here b/c I assume u are all smart enough to decode it. Edit feature would be nice but that' s not how IBs work :' [

# 89
>>11736

>>Tay.ai



Extraordinary what Tay came up with within a couple weeks

# 90
>>13403

> im making word salad



Don't feel bad I gronkked my comment quite a bit. Sometimes when I'm tired, and even when not, I just miss all this retarded typing I do. If I didn't have spell check between my fumble fingers and my horrid spelling my comments would look more like hieroglyphics  than writing.

# 91
I was thinking about this TED Talk video and trying to think how it could be used to help program an AI waifu: https://www.youtube.com/watch?v=7s0CpRfyYp8

A short summary of it is that the brain exists to coordinate movement by using sensory information and memory to predict using a Bayesian inference what movements to make to ensure our needs are met, and that everything else our brains do is largely just a byproduct of this. As I've said before in other threads, the only real need an robowaifu has is to ensure her owner's happiness, so good AI mostly seems to be a matter of creating the best predictive analytics model for the job, but I'm mostly interested in how prediction can be used for coordinating body movement, since that seems to be the biggest hurdle when creating a gynoid.

# 92
>>13810
Thanks, Bayesian inference seems to be an important topic. Maybe more long than short term, though. The AI researcher are already on it. I recall it being mentioned here for example: https://youtu.be/pEBI0vF45ic
> Judea_Pearl_-_Causal_Reasoning_Counterfactuals_and_the_Path_to_AGI_Lex_Fridman_Podcast_56

# 93
>>13816
Not really, if you actually watch the video, it makes sense if you think about it rationally, every part of the brain exists to either remember information needed to make predictions, process sensory information, &/or coordinate movement. The only parts that aren't really involved in any of those are basically glands for regulating hormones. From a purely materialist perspective, it all checks out.

The sea squirt analogy really hits it home: they swim around like tadpoles until they're mature, then anchor to surfaces like barnacles and start to digest their own brain because they don't need it anymore. Plants, fungi, etc. don't have brains because they don't move. The only thing that gets close is the jellyfish, which have some nerves, but not enough anywhere to be considered a brain. Jellyfish barely either, and some technically have photoreceptor-like eyes, but they're overall barely more than a living piece of skin.

>>13817
Neat. I'll have to watch that video later.

# 94
>>13819
>Jellyfish can barely move either.

# 95
>>13817
Huh, seems like all you would need to do is make nested updatable variables to approximate this kind of intelligence, for example, she could want to walk at x speed in the y vector. By checking her assumed speed vs her actual speed, she could make adjustments. Like, going 1 m/s requires higher voltage when she senses she's on carpet compared to when she's on tile flooring.

# 96
Dropping an interesting paper from last November on improving transformers for conversation:

>The conversational setting is challenging because these models are required to perform multiple duties all in one shot:



>to perform reasoning over the returned documents and dialogue history,

>find the relevant knowledge,

>and then finally combine this into a conversational form pertinent to the dialogue.



>Perhaps due to this complexity, it has been observed that failure cases include incorporating parts of multiple documents into one factually incorrect response, or failure to include knowledge at all and reverting instead to a generic response using the dialogue context only.



>In this work, we instead propose to decompose this difficult problem into two easier steps. Specifically, by first generating pertinent intermediate knowledge explicitly and then, conditioned on this prediction, generating the dialogue response. We call this model Knowledge to Response (K2R).

https://arxiv.org/pdf/2111.05204.pdf

It works sort of like a lorebook in NovelAI where detected keywords or phrases inject information into the context to improve response generation, except here the lorebook is generated by another language model. Improvements were reported in consistency, breadth of knowledge and factualness but no improvement was seen in how engaging responses were. These knowledge models are easy to implement with an autoencoding transformer like the T5 model.

# 97
>>15317 (continued)

What's really missing for robowaifu AI though is the lack of memory I/O so it's possible to learn from daily interaction. Separating knowledge from language processing is a step towards this at least. Instead of generating knowledge from weights learned through backpropagation on another model, it could be summarized from stored memories located by masked content-based addressing.

https://arxiv.org/pdf/1904.10278.pdf



For example, in saving a memory like "ELIZA was one of the first chatbots" an important part is 'ELIZA was' and would be masked out in the content address, so when something similar to 'one of the first chatbots' pops up in conversation, this content memory address is accessed and ELIZA is remembered. The reverse could also be stored so that when ELIZA pops up in conversation it's remembered she was one of the first chatbots. This should be doable with an autoencoding transformer that summarizes the input into key-value pairs to be either stored or queried.



But there should be a much better approach to creating an associative memory. The data stored should really be the relations between two items, creating a knowledge graph. For example, the relation between 'ELIZA' and 'one of the first chatbots' is 'was'. The transformer needs to be able to add, modify and access these relations.



How to get the relations containing an item or similar ones is beyond me right now. Perhaps by constructing a sparse neural network and sending out a pulse from relevant nodes in the graph? Then taking the top-k or top-p edges in graph and returning those statements to the context. Maybe someone who understands graph neural networks better could suggest something here. The main issue is this graph search has to be fully differentiable for backpropagation, although a non-differentiable approach might work here, such as using reinforcement learning with proximal policy optimization, which I'm already working on implementing for InstructGPT.

# 98
>>15317
>It works sort of like a lorebook in NovelAI
Never used it, but your description sounds intriguing. 

>>15318
Your graph looks quite a bit like the kind of work we're conceptualizing towards using Object Role Modeling (T. Halpin). While I recognize that statistical processing is quite important for our goals, yet we simply ''cannot rely on it alone'' if we are to succeed at our AI. The hardware/training costs for that approach are simply untenable for our model. **I'm also somewhat skeptical it's the singular best approach to the problemspace as well.**

>What's really missing for robowaifu AI though is the lack of memory I/O so it's possible to learn from daily interaction.
Totally makes sense. We very obviously keep a Theory-of-Mind model going for both ourselves and others too. Probably an important aspect of holistic mental models, too.

>The data stored should really be the relations between two items, creating a knowledge graph. 
Yep. Such 'incidental' data structures are rife in the natural world, if I can stretch the metaphor. The sub-atomic quantum-mechanical field interactions are in fact fundamental to practically everything else in physics. Yet they are 'incidental' artifacts from our human-oriented purview, generally speaking.

Yet clearly, from a theistic POV, things were intentionally designed thus. Similarly, we need to think at least one level higher up and work towards efficient AI algorithms that exploit such incidental -- if ephemeral -- 'data' structures.

# 99
Been trying to come up with a memory controller that only needs to be trained once, can leverage existing models, and can support quick storage and retrieval up to 1 TB of data.



It's a lot to explain but the basic idea is it summarizes the preceding text, pools the summary into a vector and then stores the summary and vector into a hash table bucket in the memory database. For retrieval it generates a query from the truncated context, pools it into a vector, looks up nearby memories in the memory database using the hash, and then finds the k nearest neighbours by taking the cosine similarity of vectors in the bucket. If no memories are found in a bucket the hash works like a tree so it will traverse up the tree until it collects enough memories to generate a summary.



To make the memory controller trainable through generative pre-training without needing any new datasets, a hash alignment loss is used to ensure new memories and relevant queries point to similar buckets in the memory database. Two memory advantage rewards are optimized with PPO to train the summarization model to ensure both the hidden context summary and summarized memories improve the predictions of the language model (which can remain frozen during training so the memory controller can be solely trained on low-end hardware).



Another idea I have for this is that the query generator could also be used to introspect memories and the output from the language model. If the model finds a contradiction somewhere, it should be possible to resolve it then update its own model or at the very least correct memories in the database. Being able to discern the correctness of statements could pave the way towards generating novel ideas grounded in truth not seen anywhere in training data or memory.

# 100
>>16110

That sounds very complicated. Do you know how to do something like that?

# 101
>>16116

It's a bit complicated but I've implemented most of the pieces before in other projects.

# 102
>>16110
Brilliant chart work. As usual, I hesitate to even make comment, I'm quite out of my depth (and often don't even understand the lingo tbh).

However, your graph is truly worth a 1'000 words with this one, and helps me well along the way down the path to understanding your points.

As primarily a C++ dev, I naturally tend to conceptualize every problem as a nail to fit that hammer. That being said, there's a standard library algorithm ''std::set_intersection'' that I used in ''Waifusearch'' that, along with the rest of of the general project algorithms, afforded a pretty efficient way to rapidly narrow down potential search items. 
https://en.cppreference.com/w/cpp/algorithm/set_intersection
So, my question would be "Could something like that be used in a system to find 'k nearest neighbours'''? I don't know myself, and I'm just stumbling in the dark here.

But I want to not only understand your goals, but even to help fashion them in reality with you Anon.

# 103
>>16148

I plan on using a SQL database to store data with each memory and take advantage of indexes to quickly do the approximate nearest neighbour search. SQL does its own set intersection when you query something like where a=1 and b=2, and with an index on those columns it knows exactly where to find a few KB of data in O(log m + log n) time by using B-trees, instead of checking every single item in O(m+n) time, which could potentially be a few million after a year of accumulating memories.

# 104
>>16195
I'm very hesitant to encumber our efforts with ''RW Foundations'' by using an opaque tech like a database. As with ''BUMP/Bumpmaster'' I consider keeping the data openly available and using the filesystem itself as the 'database' is much safer for all involved. It's also a universally-available datastore.

I'm not sure exactly what the ''Big-O'' rating would be for ''Waifusearch'' 's overall algorithm, but it's provably consistent at reaching an answer generally in less than 100 us for a simple search. And this is on a low-end, 2-core potato machine. I'm sure both the algorithm itself, and very definitely the hardware, has plenty more headroom available.

Again, Waifusearch is a filesystem-based datastore system. After a few seconds frontloading the indexing, she's pretty snappy tbh.

# 105
>>16240

No worries. At the bare minimum B-trees alone can be used for the memory storage and retrieval. If memories are stored as files they'll have to be split up into many directories using the beginning of their hash. I've ran into issues storing 10 million files (40 GB) in a single directory.

# 106
DeepMind created a multipurpose multimodal transformer that can play games at a human level, caption images, solve robot simulation tasks 96% of the time, control a real robot arm and chat about anything including responding to images. It doesn't appear to be using the latest multimodal advances though such as multimodal cross attention so it's not too great at image captioning. The largest model they tried was 1.2B parameters and it appears to perform decently with only 79M. For reference, a 375M model could run on a Raspberry Pi with 4 GB of ram.

https://www.deepmind.com/publications/a-generalist-agent



The authors also mention this is just a proof-of-concept and wish to experiment with external retrieval and mentioned another fascinating paper on the Retrieval-Enhanced Transformer (RETRO) that reported results on par with GPT-3 using 25x less parameters. It doesn't store memories but instead indexes large amounts of text using BERT embeddings, retrieves similar information to the context, and incorporates it with chunked cross attention.



It's pretty encouraging seeing these early attempts getting such good results. The multimodal agent in particular makes me think of the possibilities of storing multimodal embeddings as memories rather than just text. A waifu would be able to remember your face, where stored items were placed months or years ago, everything you've read, and what you chat about and did every day with almost perfect clarity.

# 107
(>>16255 related crosspost)

# 108
>>16249
Thanks, that's encouraging to hear Anon.

>>16254
>and it appears to perform decently with only 79M
>A waifu would be able to remember your face, where stored items were placed months or years ago, everything you've read, and what you chat about and did every day with almost perfect clarity.
What a time to be alive! Do you have any feeling for how practical it would be to train on more modest hardware that Joe Anon is likely to have around?

# 109
>>16261

The most popular GPU on Steam right now is a 6 GB GTX 1060. It's pretty slow so from scratch probably two years for a 375M model. With pretrained models maybe a week or two. Language models have been shown to transfer well to reinforcement learning and also work well with existing vision models. You just have to train an adapter from the frozen vision model features to the frozen language model embeddings, ideally after finetuning the vision model on vision tasks you want it to be able to do.

# 110
>>16266
>With pretrained models maybe a week or two. Language models have been shown to transfer well to reinforcement learning and also work well with existing vision models.
Actually, that sounds pretty encouraging Anon! So, I would assume that a home-server could hold the GPU and work on the incremental training times, and the runtime could be performed onboard the robowaifu with even more modest hardware (say a Chromebook-tier or even SBC machine)?

Also, is this a scenario that would work with no continual connection even to the home server? This is, entirely un-networked using purely on-board data and hardware resources?

# 111
>>16298

Part of adding a memory is to get rid of the need for incremental training. A model like Gato would be able to run on an SBC but might be too slow to inference for servo output. It would be more practical for it to do planning and have a faster, more lightweight system to handle the movements. Everything would be able to run onboard but it wouldn't be ideal.

# 112
>>16312
Ahh I see I think. Makes sense.

>It would be more practical for it to do planning and have a faster, more lightweight system to handle the movements.
Absolutely. Latency-tiered domains in our robowaifu's systems is a given. I live by the concepts of frontloading and distribution as a coder. I hope we can soon have just such a system as you describe working soon! :^)

Cheers.

