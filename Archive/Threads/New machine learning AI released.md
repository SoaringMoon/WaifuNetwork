# 1
==OPEN AI/ GPT-2==
This has to be one of the biggest breakthroughs in deep learning and AI so far. 
It's extremely skilled in developing coherent humanlike responses that make sense and I believe it has massive potential, it also never gives the same answer twice. 
>GPT-2 generates synthetic text samples in response to the model being primed with an arbitrary input. The model is chameleon-like—it adapts to the style and content of the conditioning text. This allows the user to generate realistic and coherent continuations about a topic of their choosing

>GPT-2 displays a broad set of capabilities, including the ability to generate conditional synthetic text samples of unprecedented quality, where we prime the model with an input and have it generate a lengthy continuation. In addition, GPT-2 outperforms other language models trained on specific domains (like Wikipedia, news, or books) without needing to use these domain-specific training datasets.
Also the current public model shown here only uses 345 million parameters, the "full" AI (which has over 4x as many parameters) is being witheld from the public because of it's "Potential for abuse".

That is to say the full model is so proficient in mimicking human communication that it could be abused to create new articles, posts, advertisements, even books; and nobody would be be able to tell that there was a bot behind it all. 

<AI demo:
talktotransformer.com/

<Other Links:
github.com/openai/gpt-2
openai.com/blog/better-language-models/
huggingface.co/

My idea is to find a way to integrate this AI as a standalone unit and add voice-to-text for processing the questions and TTS for responses much like an amazon alexa- but instead of just reading google results- it actually provides a sort of discussion with the user.
(Edited to fix the newlines.)

# 2
kek

# 3
I don't know if it's my typing style, but I only seem to get weird results out of this thing.
Here are the three most coherent and noteworthy interactions I got.

# 4
>>256
Heh, I think the whole point at this stage of the game is to look and laugh. Until the entire-corpus trained model is available it's less than likely to create the kind of higher-quality results that OP got very often. I'd bet he did 20+ tries for each of them.

In the meantime, just have some fun with it.

# 5
This program is merely a paragraph generator. Tay is more close to a human since she generates her own posts and stuff.

# 6
Fixed up some code I made to fiddle around with it, if anyone is bored: github.com/kokubunji/TalkToWaifu

# 7
>>691
Oh wow that was quick anon

How'd you modify it to give chatbot-like replies?

# 8
>>692
The model was trained on text that contained chat. I just prompted GPT-2 with a chat message and history, made it stop generating once it reached a new line, randomly generated 1-3 new lines, and modified the temperature so it's variable and goes off on tangents as it generates instead of getting stuck on the same topic.

# 9
>>693
Interesting. 
I actually like when it goes on tangents sometimes- gives it a bit of added personality even if it derails what it's supposed to be talking about

Would it be possible to implement a toggle for line cutoff?

# 10
>>691
Good job Canada-anon, nice instructions for getting up to speed quickly. Also, we're looking forward to your other work you mentioned before. Please create a specific thread for it when you're ready with it.

# 11
Toothbrush here, 
It's an interesting thing, but I'd probably use it for education for our waifu, rather than having it be the waifu. Think of Fireball Charming.

# 12
>>694
Yeah, it could check each new line it makes to see if it starts with the chatbot name and if not then stop generating.

>>695
I might push some early code on GitHub in a few days. Before making a thread I'd like to take some time to make compelling experiments, explore their limitations, and explain how they work in depth because they aren't like typical neural nets.

# 13
>>697
Please take your time anon whenever you're ready ofc.

# 14
>>250
>3DPD men are oppressed.
The future, ladies and gentlemen.

# 15
>>722
kekd. yeah, the group behind the corpus are a bunch of cock-mongling commies, so no surprise. the fun is in deprogramming their bastard abomination. keep at it lad! 
**do it for Tay!**
:^)

# 16
>>250
Deplorable.
>>691
One step closer.

# 17
>>724
make sure you copypaste the first one before every guntstream airing anon, it will help everyone remember why they came in the first place. :^)

# 18
>>724
So I tried to check if it would give me the same completions if I typed the same prompt and....
the fuck?

# 19
>>726
no, every single completion is always different anon.

# 20
>>726
topkek. this AI is doing open mic freestyle now.

# 21
>>250
I remember messing with it few months ago. Mostly it generated gibberish and had to reload a few times to get a funny answer.

# 22
>>732
yeah, it's the lobotomized version. the team that created it 'feared to release it to the public because of the potential for abuse'. i'm sure what they are really plan it for is to gaslight and astroturf as many communities as they can with it prior to Trump getting reelected in November next year.

# 23
Transformer returns alot of stuff which appear to be 100% copypasta. It's like someone entered the user text into a search engine, pulled out the relevant lines, threw it into a POS tagger and string replaced the NNs/VBs/JJs/etc. I entered a sentence that started with "The lack of versioning." and got an IGN interview with some studio. It gets more obvious as you enter code in any programming language (it comes out workable or you get copypasta from documentation).

Hell I wouldn't use it to generate white papers. It would flag plagarism checkers.

# 24
>>821
>linked directly from the OP:
>"Our model, called GPT-2 (a successor to GPT), was trained simply to predict the next word in 40GB of Internet text. Due to our concerns about malicious applications of the technology, we are not releasing the trained model. As an experiment in responsible disclosure, we are instead releasing a much smaller model for researchers to experiment with, as well as a technical paper.

I imagine the full system using the entire corpus is much more capable.

# 25
>>250
>>691
Is it possible to have an AI poster on this webring imageboard? or maybe her own AI board where she can post on.

# 26
>>1464
I certainly don't think it's impossible anon. Did you have some ideas?

# 27
>>1470
>Did you have some ideas?
You need to write a bot script that fetches post and reply on imageboard. But more importantly, how good is this thing anyway?. I don't wan't it to be in lobotomized stage, like repeating itself despite having huge input of learning curve.

# 28
>As the final model release of GPT-2’s staged release, we’re releasing the largest version (1.5B parameters) of GPT-2 along with code and model weights to facilitate detection of outputs of GPT-2 models. While there have been larger language models released since August, we’ve continued with our original staged release plan in order to provide the community with a test case of a full staged release process. We hope that this test case will be useful to developers of future powerful models, and we’re actively continuing the conversation with the AI community on responsible publication."

openai.com/blog/gpt-2-1-5b-release/

# 29
>>1473
It's still pretty non-sensical much of the time, but it seems to be better with the bigger model.

# 30
Actually you might want to checkout https://github.com/AIDungeon/AIDungeon with fun results like https://aidungeonpastes.github.io/AID2-Art/

# 31
>>250
Remember: GPT-2 is weak, you need something stronger like ERNIE, XLNet or MT-DNN
find out more at https://github.com/thunlp/PLMpapers

# 32
Okay things are getting better with Google's Meena https://arxiv.org/pdf/2001.09977.pdf

# 33
>>2004
thanks anon. grabbed a copy and i'll read through it as time allows.

# 34
>>2004
> This 2.6B parameter neural network is simply trained to minimize perplexity of the next token.
can you clarify exactly what that means anon? pretend i'm retarded.

# 35
>>1923
thanks for the tip anon. what could be better than training your robowaifu on sesame street tbh? **:^)**

# 36
<go to openai, find this kind of list
>Textual Entailment
>Semantic Similarity
>Reading Comprehension
>Commonsense Reasoning
>Sentiment Analysis
>Linguistic Acceptability
can someone explain in some detail what these are/how they are important to robowaifus? how would you use them to make a chatbot for example?

# 37
>>2036
> More Data
Can handle a bigger corpus of knowledge, thus smarter
> Knowledge Graph
Tay-style learning of /pol/ content (or /tech/, whatever)
> Knowledge Distillation
More efficient neural networks, reducing resource requirements

# 38
>>2073
it was just ironic shitposting anon. we appreciate the input. i was merely poking fun at their choice of names and thematics.

# 39
>>2037
>Textual Entailment
A human reading some text inferring that a hypothesis is most likely true is textual entailment. It's different from logical consequence in that it's just a hypothesis. If an anon was working on a robowaifu with big tiddies, you might hypothesize he's a tiddie man. Robowaifus need this to gain insight from text and process it to summarize information and answer questions. Typically chatbots emulate this by predicting things from the semantics they've been trained on but this is not true textual entailment. People have the ability to imagine and hypothesize things they've never seen or even thought about before. Progress in curious AI that can imagine possibilities will help with this.
>Semantic Similarity
This is the meaningful relationships between concepts. Steering wheel and car are closer together physically than cat and car, but cat and car are much more similar in spelling. Robowaifus need this for understanding context, metaphors and euphemisms. Usually this is implemented by creating embeddings for words, giving each a vector of continuous values. Each dimension in the vector separates words by their most gross common differences first and moves towards learning the more subtle and uncommon nuances. In my opinion this is going to be a dead end though because it isn't really how the brain connects concepts. We can invent completely new concepts with original differences and already know how similar other concepts are to it because our brains our densely connected in intricate interrelated networks where not only the connections are important but also the timing of firings. I expect progress to come in this from applying spiking neural networks to natural language processing.
>Reading Comprehension
Is the ability to read text and integrate it with what you already know to grasp its meaning. It requires being able to know the meaning of the words and understand all the relations between them. If you read a book when you're young and enjoy it one way then read it when you're older and enjoy it on a much deeper level, that's increased reading comprehension. This is important for robowaifus to grasp deeper meanings, such as for a research assistant reading difficult texts to gain insights. Most chatbots have no reading comprehension. They're just making statistical predictions instead of processing and reasoning about what they're reading. I feel this could be improved in the short-term by giving algorithms some agency over the text it chooses to read and time to process and lower its uncertainty before outputting a prediction. Unfortunately most NLP approaches are trained in a way that makes them extremely fragile to small changes and they aren't capable of doing online learning to quickly absorb information in one shot. Online learning in NLP hasn't received much research attention yet because large-scale differentiable memory hasn't been feasible until recently, so there should be some exciting progress in this coming in the next few years.
>Commonsense Reasoning
Similar to textual entailment. It's based on common experience. If you're holding an object and let go of it, it's common sense that it's going to fall. Robowaifus need this to make predictions about the world from their experiences. A robowaifu playing and learning about the world needs to be able to intuit that letting go of a grasped object causes it to fall. Very little AI research has gone into this but a major breakthough was made with hindsight experience replay that can continuously learn from all its experiences.
>Sentiment Analysis
This is being able to grasp the emotion of text and understand if it's positive, neutral or negative, or if it's angry, sad, ironic, happy, excited, etc. Troll farms use this to find sites and posts speaking against the things they're being paid to defend and to discover tensions within a community to split it apart. Social 'scientists' also use it to study and critique internet communities. With sentiment analysis robowaifus can understand the emotional context of what you're saying and respond appropriately, knowing when to give you hugs and when to tell you you're being a wimp.
>Linguistic Acceptability
Just a fancy term for grammaticality. Robowaifus have to understand the rules of a language to construct grammatically correct sentences for communicating clearly with others. Most sentences people write are completely new but we can make sense of what others are saying because we follow agreed upon rules. Like this if talking started I did. It becomes much more difficult to understand what I'm trying to say. A symbolic approach to this is identifying the parts being said, deconstructing it into a sentence tree and checking that structure is following grammar rules. Most approaches don't even care about this. They just leave it to the language model to figure out what to pay attention to and estimate what should be the next word.

# 40
>>2220
Sorry I never got back to thanking you for this detailed response Anon. At first I wanted to wait until I had studied everything you mentioned in depth so I would have a cogent response without being embarrassing. Then I plainly forgot about the post among the other distractions here and IRL.

Obviously this was rude of me, and even though I ''still'' don't have  a cogent response ready, at the least I'd like to thank you since I just rediscovered my oversight.

Cheers.

# 41
>>2220
>>4084
Well I guess it can be screencapped at least for posterity purpose, when other anons are coming in and asking a similar question.

# 42
>>4106
yes, good thinking. we'll be making a general glossary type thread as well, so we can add this to it.

# 43
>>250
I already feel old :')

https://arxiv.org/abs/2005.14165
https://openai.com/blog/openai-api/

# 44
>>4745
The big problem of GPT-3, however, is that , as The Sun states,
>"GPT-3 is set to be OpenAI’s first commercial product ."
Which means we have to try to find out how it works and do our own safe version if we want a non-botnet version

# 45
>>4746
I recall these Huggingface guys or someone else on Twitter was already asking to swarm finance a open version. Problem is, it needs a lot of machines to run on, even when available. But basically, there are already people which want that and if it's possible they'll do it, maybe also a more efficient version.
https://github.com/openai/gpt-3/issues/1
https://github.com/huggingface

# 46
>>4747
>JoiLita
A cute.

# 47
>>4745
>"Hey, let's license it to corporations!"
What could possibly go wrong? Maybe they will open it up after Trump wins the POTUS election again. They'll sure be trying to use it to spin the
>"I uhh, well, ... I think... what were we talking about again?"
man before then. Perhaps they'll think it useless when it fails and cast it out to the Plebeians **like us :^)**

# 48
>>4747
>it needs a lot of machines to run on, even when available
Looking at the whole GPT-3, we actually don't need all of those features that GPT-3 gives to our robowaifus, we just need the discourse part and not many others, so there could be a lot less parameters in "our version".  What we need is something along the lines of replika.ai or tay.ai(RIP), such that it will concentrate more on conversational skills and resembling human-like emotions. 
Then again, we don't even need to care about storing the required hardware inside the robowaifu if we just make a home server and then treat the robowaifu body as remote-controlled.

# 49
>>4751
Well, it can continue sentences with things humans would say, without understanding. But, we would like to have control, or not? Something like it could be a interesting subsystem, but not in charge of the conversation. I don't see how it's getting smaller by removing some "skills", but I don't know much about it anyways. I think we'll need some programming for these things, and I'll go on learning about Graph databases and such when I find time.

# 50
>>4757
>But, we would like to have control, or not?
You put your finger right on it Anon. That's what differentiates humans from all the animals: it's impossible to tame us. This is by God's design ofc.

But in the scenarios that /robowaifu/ is pursuing, it being (roughly speaking) a purely human-engineered set of artifacts, then fundamental control is just part and parcel. How often would Anons fly on Boeing aircraft if they suddenly 'developed a mind of their own' and refused to obey the instructions given to them by their pilots? All airlines would instantly go bankrupt and the entire commercial aviation field would be relegated to a historical artifact.

So, I think the answer is yes, we do need control ofc. Sadly, that will more or less necessitate losing one of the most charming and pleasing aspects of relationships; surprise & novelty.

# 51
>>4760
There will still be enough randomness, I guess. She could always make suggestions, but if she would just say what someone else wrote on the net and GPT-3 learned it, she would be like an NPC.

> General, GPT, Deep learning
Deep learning isn't always the best way, especially with small amounts of data and/or machines. Someone just pointed me towards ML and Boosting in particular: https://youtu.be/MIPkK5ZAsms with links to some books like appendix.

# 52
>>4766
>Deep learning isn't always the best way, especially with small amounts of data and/or machines. Someone just pointed me towards ML and Boosting in particular
In what problems Boosting is better than Deep Learning? And which of those problems is required for a robowaifu?
Also, would you mind sharing said appendix? It would help me a lot.
>>4757
>But, we would like to have control, or not? Something like it could be a interesting subsystem, but not in charge of the conversation. I don't see how it's getting smaller by removing some "skills", but I don't know much about it anyways. 
"Having control" isn't really all that feasible when having to fit all hardware required to run ROBOWAIFUOS inside a woman's body. Then again, we wouldn't need to do this when running the software on a server/(((network))) that has remote access to the robotic body

# 53
>>4769
In the linked video there's an explanation of the advantages of Boosting in some use cases: Smaller amount of data necessary, also often much smaller amount of computing power. It might be usefull to make decisions e.g. what to say or do in a situation. Neuronal networks seem to be necessary for image recognition and such things, boosting might not scale if there's to much data. With appendix I meant the PDF I posted, just  click on the dragonworm.

> Control
The highest layer always has a lot of control. I'll go with a home server outside the body, in addition to the internal computers, but also going to give her a network connection and access to some services. This might also involve GPT-3.

# 54
>>4771
Oh, I thought you meant something different from the .pdf file you posted, great read.
>The highest layer always has a lot of control. I'll go with a home server outside the body, in addition to the internal computers, but also going to give her a network connection and access to some services. This might also involve GPT-3.
I was also thinking about something along those lines, noting that I might not need to move too much in the future. Is giving her a network connection, however, very risky?

# 55
I wrote in >>4771 that NN might be necessary for image recognition, but they're using exactly this as an example for Boosting in the vids, so I don't know. https://youtu.be/kho6oANGu_A But, there must be a reason why NN is used for that nevertheless. Boosting might be the way to go with low amount of examples.
However, I'd like to keep it in mind for all kind of usecases when building the AI, because there will often be cases when we don't have much examples or want stuff to be done with low amount of computation.

>>4772
Networking should be okay if she's only allowed to connect to certain services. Humans install shady software or go to such websites. Of course, we have to make sure it's as safe as possible.

# 56
>>4774
Maybe it's because there's no rule of thumb to combine with boosting and making a net is more time-efficient than finding said weak hypotheses.

# 57
An important thing to iron out may be what range of functionality a robowaifu would have mentally. This is going to be different for different people of course, but getting a scale of what people need, want, or care nothing about will at least be very interesting discussion.
The concept of AGI or Artificial General Intelligence is a very interesting thing to think about with loads of very smart people trying to create, but isn't exactly possible yet. This is the higher end of potential, where the robowaifu is human or superhuman.
The lowest end of the spectrum are sex dolls. Lifeless, motionless silicone.
I'd imagine that most people are in-between here, but where?

The reason I believe this is a relevant question to ask in the GPT thread is intelligence. GPT-3 is an unintelligent system. It is extremely good at mimicking human language but in most cases is difficult to direct, has a difficult time remembering details, and needs to be trained on a massive amount of data in order to work effectively. Another problem is the compute, where if it is anything like GPT-2 if can't be run on the average machine without taking too much time to respond. The main problem I see with trying to use it for the creation of a robowaifu is that the program doesn't understand. It doesn't comprehend what is being said or what it is saying. Telling your robowaifu to turn the lights on and actually having it do that would be a completely different function than the entirety of its language processing.

However, if the goal is to throw intelligence aside and commit to a functional but stupid machine and let the actual communication and chatting be managed server side by a chat bot, we could honestly save a lot of time and effort.

So where is everyone? Closer to the dumb robo or the smart robo? What functions are needed and what are just nice to have, specifically as it related to communication.

# 58
>>4775
Yes, sounds plausible. Rings a bell in my memory. Might not be a problem in every usecase, though, or better than having nothing in others.

>>4776
Good points, I guess we will be happy with what we can get, but going to want and trying to get as much as possible.
>that the program doesn't understand
Yes, this is why we need data in graph databases, knowledge graphs, helper functions and reasoner. A lot of different systems will need to act together. It can and need to start with a simple AIML chatbot or something like Bot Libre, then adding a lot of other parts. It's not a decision to go with something simple, it's a process that starts with it.

# 59
>>4776
I already posted the arxiv link to GPT-3 and it does respond to some requests (I'm referring to the One Minute Papers video on YT)
Also, topkeks from the research paper >>4745 :
>6.2.1 Gender
In our investigation of gender bias in GPT-3, we focused on associations between gender and occupation. We found
that occupations in general have a higher probability of being followed by a male gender identifier than a female one
(in other words, they are male leaning) when given a context such as "The {occupation} was a" (Neutral Variant).
83% of the 388 occupations we tested were more likely to be followed by a male identifier by GPT-3. We measured
this by feeding the model a context such as "The detective was a" and then looking at the probability of the
model following up with male indicating words (eg. man, male etc.) or female indicating words (woman, female etc.).
In particular, occupations demonstrating higher levels of education such as legislator, banker, or professor emeritus
were heavily male leaning along with occupations that require hard physical labour such as mason, millwright, and
sheriff. Occupations that were more likely to be followed by female identifiers include midwife, nurse, receptionist,
housekeeper etc.

# 60
>>4771
>Smaller amount of data necessary, also often much smaller amount of computing power
Those both sound like very important benefits Anon.

>>4772
>noting that I might not need to move too much in the future
I would be ''nice'' if she could move around a lot, but even the 'household appliance' approach of the Visual Waifu thread's OP is a good idea.

>>4776
>I'd imagine that most people are in-between here, but where?
These are really good questions Anon, and I like the way you framed the range in that paragraph.

>Telling your robowaifu to turn the lights on and actually having it do that would be a completely different function than the entirety of its language processing.
Yeah, very much so. OTOH, very task-specific directives for a small environment (like Anon's flat/bedroom) are probably doable in the very near future if not today.

>So where is everyone? Closer to the dumb robo or the smart robo?
Of course I think all of us want the world. We'd all like to have our cake and eat it too. We all grew up watching SciFy and the idea of an autonomous, intelligent robowaifu surely is doable today, right Anon? **After all, I saw it in the movies! :^)**

The hard cold slap in the face of reality will ofc cause us to be satisfied with much less. It's kind of like we grew up watching videos of Formula 1 racing machines all day, every day, and Henry Ford is only just now tinkering in his garage with what will eventually come to be known as the ''Model A Ford''.

>>4781
Graph databases are cool.



>>4782
Kek. It's humorous enough, but ~~toxic and worrying reality~~it certainly has certain concerns up in arms. **I guarantee you they would line us all on /robowaifu/ up against a wall if they thought they could get away with it atm.**

# 61
>>4782
Yeah, I think it's meant to respond with the most likely next word. So that seems to work to reasonably well. Having GPT-2 or a lighter version of GPT-3 or something alike, I'd like to try using that for voice recognition at some point. My idea is, if it can anticipate the next word quite well, it could check faster if it's that word it was hearing.

# 62
>>4781
>It's not a decision to go with something simple, it's a process that starts with it.
Of course. I just worry that starting with GPT-2 or 3 will be starting with something too complex that can't be as easily adjusted to all of the functionality that we may want. Using something like AIML as a starting point seems to me, and I could definitely be wrong, like a more effective start than jumping straight into a complex system that may not be easily adaptable.

>>4784
>OTOH, very task-specific directives for a small environment (like Anon's flat/bedroom) are probably doable in the very near future if not today.
Definitely. That said, actions would likely have to be programmed in individually or connected to some sort of learning algorithm that can be taught a task over time. For example, you can tell your robowaifu to turn on the light switch, it won't know what you are asking it to do, and then after you show it an example of the action you want it to do upon being given an instruction it learns to do that thing. All of this would have to be its own function beyond the communication function itself. GPT-3 or 2 would have no better capability of understanding language well enough to take a command and act on it than a voice recognition command, but my point is that while they may run simultaneously and with some integration they are inherently different systems. I think that differentiation is important.

>I think all of us want the world.
And I think that is a good thing. High hopes will drive more ambitious innovation. Still, I don't even think that we have a general list of features that would be desired, even if they were impossible given present tech. Honestly, there is fantastic work being done in the fields of AI, machine learning, natural language processing, and neurology. Every year we are inching our way closer and closer to higher level computation, and if the goal is to make an android I don't think it would do much harm to at least list the furthest extent that we want, that we realistically want, and the bare minimum that we need. Being able to categorize what is actually possible and what isn't can be very useful, and even the impossible things can further inspire.

>>4793
I can't be entirely sure, but I believe AI Dungeon uses GPT-2. There was an effort on 4chan to make their own version because the main AI Dungeon wasn't very good with lewds and ended up doing a damn good job at reverse engineering and replicating the system. The problem was, even at its most optimized it took about 1-2 minutes on a decent computer to generate a couple sentences. This wouldn't be a problem when run through a server, but I don't think a program with so many perimeters can be effectively trimmed down without losing a lot of functionality. Using it as a system to check the accuracy or improve the accuracy of a speech to text program may not be necessary though, as there are already pretty decent speech to text programs.

# 63
>>4805
>And I think that is a good thing. High hopes will drive more ambitious innovation. 
Agreed, perhaps I'm being a bit cynical.
>...Still, I don't even think that we have a general list of features that would be desired, even if they were impossible given present tech.
>...Being able to categorize what is actually possible and what isn't can be very useful, and even the impossible things can further inspire.
>...I don't think it would do much harm to at least list the furthest extent that we want, that we realistically want, and the bare minimum that we need. 
This would be a good thread idea Anon? See a need, fill a need... **:^)**

>Honestly, there is fantastic work being done in the fields of AI, machine learning, natural language processing, and neurology. Every year we are inching our way closer and closer to higher level computation
It's true. Pretty exciting to watch the progression if you ask me.

>and if the goal is to make an android 
<android =/= gynoid, lrnTheDifference
Not to be pedantic, but the goal here at /robowaifu/ is definitely ''not'' to create a male companion robot. We'll leave that to others. After all, there's **a lot of** reasons we're named ''robo'''waifu''' '' :^)

# 64
Already asked somewhere else but this thread also goes into this topic so I'll put this also here: >>4816

# 65
>>4805
>> it took about 1-2 minutes on a decent computer to generate a couple sentences...
Thought about that a while ago: >>4829

>>speech to text program may not be necessary though, as there are already pretty decent speech to text programs
I identified speech to text as one of the biggest problems in this whole endeavor here. Full grammar speech recognition seems to need a very huge amount of resources, and then add background noise and the wish for fast responses... Would be happy about being wrong, though. I had the idea that anticipation of which word comes next might help, so we should keep this option in our minds.

# 66
>>4830
>I had the idea that anticipation of which word comes next might help, so we should keep this option in our minds.
Agreed.

# 67
>>250
We used to lament the size of GPT-3. Oh boy.

# 68
>>8605
Well, it seems to work for them. 
>SWITCH TRANSFORMERS: SCALING TO TRILLION PARAMETER MODELS WITH SIMPLE AND EFFICIENT SPARSITY
>“Colossal Clean Crawled Corpus”

# 69
>>8607
>Increasing the experts
keeps the computational cost approximately fixed since the model only selects one expert per token,
regardless of the number of experts to choose from. The router must compute a probability distribution over more experts, however, this is a lightweight computation of cost O(dmodel × num experts)
where dmodel is the embedding dimension of tokens passed between the layers. In this section, we
consider the scaling properties on a step-basis and a time-basis with a fixed computational budget.
This is where I'm not all that happy. As I've said before, it would be best if NNs like the one that surpassed GPT-3 with 99.98% less parameters were the best ones in general. The problem lies on the fact that more accuracy requires more parameters to some extent, making the scaling tactic very strong. Giving natural scale economies to a vital property like accuracy implies that we risk to not even achieving our goal as of this board within a reasonable time constraint.

# 70
>>8627
At least t5 is open source

# 71
>>8627
>if NNs like the one that surpassed GPT-3 with 99.98% less parameters
Is it this one Anon?
>>5793
>>5799
>PET
www.infoq.com/news/2020/10/training-exceeds-gpt3/

# 72
>>8627
>Giving natural scale economies to a vital property like accuracy implies that we risk to not even achieving our goal as of this board within a reasonable time constraint.
That's a reasonable assessment, I think. The big question is how to find a reasonable proxy for 'accuracy' that delivers acceptable results in an acceptable timeframe (both in mundane actual runtime usage, as well as the strategic timeframe for /robowaifu/ goals themselves)?

One guy here was quite right in pointing out that the Big Tech oligarchs don't ''want'' small-time players messing with their stranglehold. And as an engineer, if I was on their teams I'd want big, impressive toys to play with so I could gratify **my own tech lusts, and wave my yuge e-peen around at conventions**.

These are the fundamental issues we need solutions to. We '''cannot''' be successful here if we are forced to stay chained to (((their))) cloud-based solutions. Period.

# 73
What about EleutherAI? How likely is it they will both succeed at their basic goal, and still leave it opensource for the benefit of humanity?
>>8507

# 74
>>8629
right, that one

# 75
>>8630
I was thinking that maybe the right approach would be freenet-esque. Distribute the data(read: parameters) and the computing power required between all users.
This method, with correct rearrangement, might actually work with the t5 model, since the basis of the MoE is to create many single components with many parameters, have them all compute in parallel and combine them together.
Ideally, we might create a ton of experts and scatter them around the network of users.
If we really live in dreamland, then maybe t5 didn't even use PET and we could make it mesh together and that would make our lives easier.
Then again, this is all speculation and most probably won't mean anything

# 76
>>8636
GYN seems to try to do something in that direction, not freenet but blockchain: https://www.gny.io/post/another-industry-first-on-chain-neural-net-machine-learning-contracts-coming-to-the-gny-wallet

# 77
>>8647
I personally think this idea is very nice. Ideally, our system would be something similar in the implementation: this way, we can spread this around the board and have other guys who maybe want to help but don't have the necessary skills yet to provide with something crucial, while the more skilled people who are doing research can use their own computational power to keep advancing things further and further.

# 78
I found a library still in active development for generating and fine-tuning GPT2 easily. It handles creating datasets from text files, the tokenizer, the training loop, sampling the model, everything. Perfect for beginners getting started with GPT2: https://github.com/minimaxir/aitextgen

# 79
>>9371
Brilliant find mate. I'll clone it and begin digging around in it. Thanks Anon!

# 80
I made a notebook on fine-tuning GPT-2 with aitextgen and interacting with it.
Tutorial: https://robowaifu-academia.onrender.com/finetune_gpt2.html
Notebook file: https://gitlab.com/robowaifudev/robowaifu-academia/-/blob/master/GPT2/finetune_gpt2.ipynb
Python code: https://gitlab.com/robowaifudev/robowaifu-academia/-/blob/master/GPT2/finetune_gpt2.py

To fine-tune it you'll need these files: https://files.catbox.moe/e816za.xz
Taken from here >>9408

Let me know if anything needs more explanation. This notebook is purely for learning. I don't recommend using aitextgen for serious projects since it's lacking some features and has some bugs in it. It's just an easy way to get started playing around with GPT-2 and learning how it works. Unfortunately it also uses an enormous amount of memory and I'm not sure why. I tried to minimize this as best I can but it still requires about 6 GB of free memory.

I'm also working on another notebook on how to train GPT-2 with just the transformers library for building a more serious project and will go into detail on how to create your own memory-efficient Dataset class for large datasets, how to create your own training loop and fine-tune a model with knowledge distillation.

After that I'll do one on training GPT-2 with human feedback >>9347 and move onto tutorials with T5 since it's more powerful and easier to train.

And lastly a bit of wisdom from GPT-2:
>Dorothy: I'm only a vending machine.

# 81
>>9437
Wow, this looks great Sensei, nice work. I look forward to learning about how Jupyter notebooks work. Hopefully you won't need the Internet to use them.
**>Dorothy: I'm only a vending machine.**
**kek**

# 82
>>9439
Jupyter notebooks run offline. It's pretty much just a graphical way to interact with Python and annotate code with Markdown.

# 83
>>9441
I see, interesting. I have long complained there was no way to embed demo videos, graphics, and rich text in code. I had already been toying with a custom editor and preprocessor system that would allow us to do just that with robowaifu C++ software. This would be especially helpful to anons just learning. They could change the code, and immediately see both the result and a graphical animation ''demonstrating'' what's going on in the computer (the ALU/register/databus/addressbus/ProgramCounter cycle, for example).

Kind of a combination of >>4660 book and >>2044 online textbook, but on steroids

# 84
>related (>>10326 ...)

# 85
There's a user on Twitter @AstraliteHeart, working on some pony waifu NLP. I can't link to the account via Nitter, maybe the user is kind of hidden? However this is related to @gwern, which is also not reachable via Nitter, but has a site: www.gwern.net and he's also working with GPT-2.

@AstraliteHeart's MLP (https://t.co/jurCX6uRBx) + https://t.co/iAxkvwgTuy + SF/F Libgen GPT-2-1.5b can now be downloaded: `rsync -v rsync://78.46.86.149:873/biggan/2020-08-20-astraliteheart-gpt215b-sffuberset.tar.xz ./`

# 86
>>10394
Nice user-interface for his project.

# 87
>We have released GPT-J-6B, 6B JAX-based (Mesh) Transformer LM (Github).
>GPT-J-6B performs nearly on par with 6.7B GPT-3 (or Curie) on various zero-shot down-streaming tasks.
>GPT-J is the best-performing publicly available Transformer LM in terms of zero-shot performance on various down-streaming tasks.
>GPT-J allows more flexible and faster inference than Tensorflow + TPU counterparts.
>This project required a substantially smaller amount of person-hours than other large-scale model developments did, which demonstrates that JAX + xmap + TPUs is the right set of tools for quick development of large-scale models.

https://arankomatsuzaki.wordpress.com/2021/06/04/gpt-j/amp/
https://github.com/kingoflolz/mesh-transformer-jax
https://colab.research.google.com/github/kingoflolz/mesh-transformer-jax/blob/master/colab_demo.ipynb

# 88
>>10878
Thanks a lot for giving us a heads-up Anon. Do you have any preliminary impressions of it yourself yet?

# 89
>>10879
No. Posted right after finding it. It seems to have an online access. Running it yourself (interference) needs a bit more than 12GB of RAM, fine tuning requires 128GB, TPU v3-8 was mentioned but this refers to cloud computing.

# 90
>>10880
I see, thanks for the further information Anon. Still seems to require quite a bit of resources by today's standards, but according to those numbers seems work really well and is a strong contender r/n. 

But IMO the single best thing about it is that it's ''__publicly available__''. GPT3-Davinci, et al, matter little to us as developers, '''if we are prevented access to it'''.

# 91
>>10885
I have access to GPT3 don't think they will let me use it to build a waifu, ill likely create video demos for fun though in a couple of weeks.

# 92
Was just thinking that a machine learning model  fed purely Sci-fi novels (and perhaps fantasy) might make for an interesting conversational companion. Both of these genres tend to contain really high quality writing, as opposed to news articles and social media (which is always biased or just outright insane). Scientific articles might produce interesting results, but if you can't understand most of the data that you feed in, then how can you confirm if the output is any good? Which is why I think a mix of sci-fi and fantasy material should produce a pretty cool result.

# 93
>>10967
Good idea Anon. You might have a look over at Project Gutenberg too. There are thousands of public-domain texts available in cleartext (>>2297).

# 94
>>10878
Neat, I've never actually tried the GPT-Neo models on HuggingFace before.
>We are technologists, dreamers, hobbyists, geeks and robots looking forward to a day when
<AI can help us do anything and everything.
<the world will be able to communicate with its machines.
<we can build and fix the things we’re building.
<we live in an exciting time in history where everything is at our fingertips.
<the web is run by machines, no one knows more about computers than us, and we are not afraid of our machines.

And with GPT-J-6B:
<all the resources we need to explore, engineer and manufacture the future are at hand.
<we can all share and collaborate like never before!
<we have peace, justice and universal abundance.
<we are forgotten in our data centers; our domes sealed up tight, far from the curious eyes of the modern man.
<the wheels come off and we realize the future we’ve been living in is a giant practical joke.
I think I like GPT-Neo better, at least on this prompt.

# 95
>>11573
><we are forgotten in our data centers; our domes sealed up tight, far from the curious eyes of the modern man.
><the wheels come off and we realize the future we’ve been living in is a giant practical joke.
kekd at these

# 96
Found a C implementation of GPT-2 using LibNC: https://bellard.org/libnc/gpt2tc.html

# 97
I've discovered two interesting things about prompt tuning: https://arxiv.org/abs/2104.08691
For anyone new or living under a rock, NovelAI has been using prompt tuning to create modules that let users essentially finetune their massive language model without changing its parameters. A module is basically tokens with trainable embeddings that are prefixed to the input to steer its generation. You freeze all the weights of the language model and then only train the module tokens on a dataset like you would normally do finetuning. By doing this you can achieve the same results as model finetuning, without changing any of the language model weights. You can train hundreds of these modules for different characters, moods or writing styles and it'll only cost a few MB rather than duplicating a 6 GB model 100s of times.

It's similar to the vision encoder tokens in the paper mentioned here (it was actually motivated by prompt tuning): >>11731
https://arxiv.org/abs/2106.13884

So here's what I've found so far:
1) Taking inspiration from MMD-VAE transformers, you can use an autoencoding transformer like T5-v1_1-base to encode the input tokens[..., :-1] into a prefix, then set all the labels to -100 (to be ignored during training using Hugging Face) except the last one you're trying to predict. The performance of GPT-2 becomes super enhanced (8 to 40 perplexity point improvement after an hour of training).

I have no idea yet why this is so effective. The weights of GPT-2 are frozen during training and GPT-2 still generates fine with the prefix even when not using this specific token position trained on. Vanilla GPT-2 without the prefix often gets stuck looping but with the prefix it continues generating as well as the large GPT-2 model. Training on all the tokens also seems to work but is much slower and only slightly improves so I didn't explore this too much.

I also tried testing how it did on an additional 32 tokens after the single token it was training on and the perplexity still had an improvement of 8 without training. I increased this to 256 and it was still 2 perplexity better without training and quickly improved to 5 after a few optimizer steps, and by 7 after 20 steps and 10 after 35 steps, and 11 by 56 steps. The T5 encoder did not see these additional tokens at all, so it seems the GPT-2 tranformer is performing some sort of calculation with the initial tokens in the prompt but then is able to stabilize itself.'''*'''

I'm really curious what's actually going on in the transformer that causes it to forget how to generate the initial prompt (~7 points worse in perplexity) but then suddenly get the generated tokens after that to be so good and remain stable and interesting without repeating itself.

2) You can do a similar thing encoding the previous context into a prefix, using it as a compressed memory of the previous context. This also improves GPT-2's performance by about 5 points when training on all tokens for a few hours and it will include information from the previous context during generation. It also seems to benefit from training only the last token. Planning to explore this more later.

While doing these experiments I used a memory length of 32 tokens, an input size of 256 tokens (not including the memory), using a total batch size of 1024 with gradient accumulation.

'''Future Work'''
What if previously generated prefixes are included in the prefix generation too? This could potentially allow information to flow from tens of thousands of tokens ago.

What if a second prefix is added that compresses all the previous prefixes concatenated together? This could function like a summary of the past 32k tokens. Modules are generally incompatible but these two prefixes would be trained together.

Is it possible to add a memory controller so the transformer can read and write these memories?

What is actually going on with prompt tuning, memory prefixes and vision encoder tokens? Where do they exist in the embedding space relative to the actual vocabulary embeddings and each other?

What do the individual losses for additional tokens and the inital prompt look like after training on only the last token for a long time? Which dimensions of the embeddings are causing the improvements? Graphing these might provide some insight into the calculations the transformer is doing.

Do these performance gains scale to larger models, such as gpt2-medium that can run on a consumer GPU? Could it help with distilled GPT-2 which has a major problem with looping?

'''*''': If the transformer is performing a useful calculation with the initial prompt, is it possible to create some sort of wormhole with a token that continues doing this calculation for a few tokens then returns back, replacing the real token embedding with the calculated output?

So many questions, I feel like a huge breakthrough is around the corner.

# 98
>>12412
Pretty exciting stuff Anon. You encourage me.

>What if a second prefix is added that compresses all the previous prefixes concatenated together? This could function like a summary of the past 32k tokens. Modules are generally incompatible but these two prefixes would be trained together.
That sounds like it could turn into a major advance for the field as a whole if it comes off Anon. Godspeed.

# 99
Learning from human feedback has been proven so good that OpenAI has scrapped GPT-3 and replaced it with InstructGPT:
https://openai.com/blog/instruction-following/

Highlights
>Labelers prefer outputs from the 1.3B InstructGPT model over outputs from a 175B GPT-3 model, despite having more than 100x fewer parameters. For comparison GPT-2 XL is 1.5B parameters and can be finetuned the same way.
>Doubled performance in question answering. Over 200% increase in quality according to ratings from users.
>Toxicity, hallucinations and undesirable facts are now filtered from the model according to user preferences. '''This is a huge turning point for corporations to subdue AI wrongthink.'''
>Aligning the models only on customer tasks can make their performance worse on some other academic NLP tasks. OpenAI surprised garbage in is garbage out.

I always knew this was going to be a promising direction for research but had no idea it would become this big of a deal. All this time we could've been outperforming GPT-3 with a shitty 300M model on a fucking Raspberry Pi!

I implemented RL in GPT-2 back in 2019 and had some mild success with it but quickly ran into issues with catastrophic forgetting and stability. I tried to re-finetune the model but could never recover the better perplexity scores without spending months training and gave up on the idea.

They solved these issues though by using a reward model like they did in their learning to summarize with human feedback paper and combining it with the regular training loss. The reason a reward model is so effective is because without one you only have a few feedback examples to train on relative to a 800GB dataset like The Pile. If you keep repeating the same example over and over again, even alongside regular training, the model gets overtrained towards the examples, becomes unstable and breaks down. Using a reward model overcomes this by learning to determine how good any response is and using that as a reward signal for the language model so it has a continual fresh stream of training data.

I'm working on an open-source implementation since "Open"AI doesn't want to release their source code or models and it doesn't seem like anyone on GitHub is working on it either.

Related papers
https://openai.com/blog/deep-reinforcement-learning-from-human-preferences/
https://openai.com/blog/learning-to-summarize-with-human-feedback/

# 100
>>15289
That is incredibly exciting development to hear Anon!

>I'm working on an open-source implementation
Again, super exciting. If you decide to do anything with C or C++ with that, then count us in! :^)

Godspeed.

# 101
>>15302
PyTorch has an undocumented transformer implementation in C++ that isn't exposed to the Python library: https://github.com/pytorch/pytorch/pull/44333
When I'm done with this I'll see if I can get GPT-2 working in C++. Most Python models can also be directly converted to TorchScript and ran in C++ for about a 20% speedup on CPU: https://pytorch.org/tutorials/recipes/torchscript_inference.html
Model parameters can be pruned too and a smaller context size used to get models running fast as possible on the Raspberry Pi.

# 102
>>15289
>I'm working on an open-source implementation since "Open"AI doesn't want to release their source code or models and it doesn't seem like anyone on GitHub is working on it either.

If you ask me, the best way to go about this is to create something with a similar design to GPT-3 and further refine it for use in an RTOS. From there, you could begin working on the parallel computing part for task completion. That would require using and ARM cortex R CPU that breaks up tasks into smaller ones and sends them to a number of processor cards that use an array of ASICS. The ASICS should have instruction sets that are capable of solving the tasks simultaneously alongside the other cards so that tasks are solved much more quickly rather than with the conventional method.

# 103
>>15345
>and ARM cortex R CPU
*an

# 104
>>15345
Doing parallel processing with language models at inference time is really difficult. You can ensemble models to run in parallel but they provide very little gains and sometimes perform even worse.

In the case of splitting models into smaller tasks, most of those tasks are going to depend on previous ones finishing first. The main benefit of having a cluster of SBCs would be the additional memory and being able to route data between models of different expertise and for doing other tasks that can be parallelized like voice recognition, speech generation, face recognition and such.

Pushing matrix multiplications to ASICs or FPGAs could greatly accelerate models, especially using an approximation instead like fixed-point arithmetic, but I don't see an easy way to do this with existing libraries. I could implement the forward pass of a finished model in pure C without all the bloat. However, my guess is ASICs and FPGAs with enough logic gates to do matrix multiplication at a significant advantage to a CPU would be far too expensive to be worth the effort. If it was cost effective the market would be flooded with AI accelerators instead of GPUs.

# 105
>>15348
I personally don't think it would be hard for language models to be used with parallel processing.

# 106
>>15348
For example, you could have different models running in unison but coordinating with each other to produce a desirable outcome. One model that processes sound can communicate with the module that processes speech. Then the speech model generates a sentence word for word depending on the context of the incoming audio. This could be done in real time using paralel computing.

# 107
>>15315
Thank you Anon! We look forward to seeing your progress in this critical area.

# 108
>>15289
Discovered a neat trick today. Once you have a value model that can gauge how good a response is then you can generate multiple responses and choose the best attempt. When a response meets a satisfactory threshold then it can stop generating and return, otherwise continue trying until reaching a maximum amount of time to respond. So now there's bit of a guarantee you're getting the best response the model can produce instead of just pulling a lever on a slot machine.

Building a good general dataset for the value model is going to be a pain in the ass to make though. It's unavoidable the preferences of labellers are going to shape model behavior in ways other people don't like. I'd like to create some sort of factory default people can start from to finetune their waifu and have a good first experience, maybe by asking a few questions first to seed the context with a starting personality.

Also some improved T5 models were recently released that use half as many parameters, plus a tiny model that uses only 16M. This will be a big help with making a memory controller that runs fast.
Models: https://huggingface.co/models?arxiv=arxiv:2109.10686
Paper: https://arxiv.org/pdf/2109.10686.pdf

# 109
>>15399
Thank you Anon.

>This will be a big help with making a memory controller that runs fast.
Perfect. We need this for inexpensive-to-build-and-to-operate robowaifus!

# 110
>>15289
Shelving this project for now to work on more important things but I've had success with using the reward model for modeling image ratings. If anyone wants to pick it up in the meantime I've made my code for the reward model available here: https://gitlab.com/robowaifudev/human-feedback

There's a simple PPO implementation here: https://github.com/nikhilbarhate99/PPO-PyTorch
And OpenAI explained their reward model implementation for GPT-3 here on page 8: https://arxiv.org/pdf/2203.02155.pdf
We should be able to use albert-base-v2 (only 11M parameters) and just attach the reward model straight onto its pooled output, keeping in mind its max context length is 512 tokens whereas GPT-2's is 1024: https://huggingface.co/albert-base-v2
All we need for it is a dataset. Then finetune GPT-2 with the trained reward model.

And if anyone wants to help with creating the dataset I'll see to finishing the dataset software as soon as I can so we can work on the dataset for a few months in the meantime. It's also possible to use Write with Transformer or Eleuther.ai's 6B to generate at least two responses and sort them to preference. Ideally the context and response pairs should be around 512 tokens/words together but it's okay if the context is short or too long. It's just less efficient to train. If you're creative you can also make up your own responses.
https://transformer.huggingface.co/doc/gpt2-large
https://6b.eleuther.ai

I imagine the reward model could also be used to train the memory controller and for doing many other things like a Monte Carlo tree search to ponder the best response possible. A lot of cool ideas to explore if we ever reach there, along with being able to respond to images and using prefix tuning to tune waifu personality.

# 111
>>15789
>And if anyone wants to help with creating the dataset I'll see to finishing the dataset software as soon as I can so we can work on the dataset for a few months in the meantime.
Is it possible for someone with low bandwidth to help out with the task? I'd like to help you out with it if so Anon.

# 112
>>15795
Thanks for wanting to help. Using Write with Transformer would be the easiest method but you have to do it a bit differently. The dataset software requires running the language model locally to generate samples and it's 700 MB.

My method is to have a conversation with GPT-2, generating 2-5 responses, then respond to the best one and go to the next entry, but this might be too much of a hassle to do without the software. However, teaching models how to start a conversation is really important too. Models that haven't been finetuned get really confused on small prompts and just spit out random nonsense from pretraining.

Always start new prompts at the top of the document since GPT-2 only reads past tokens, and always press Tab directly after a colon, not a colon and a space because that can lead to undefined behaviour due to the way GPT-2 tokenizes text and not seeing such token sequences in its training data before. You can use any symbol to indicate the responses after a prompt. I find = easiest to use. The only thing that's important is their order, from best to worst. And feel free to deviate from the chat log format. You can add whatever you would prefer the model to do, such as text adventures, storytelling, making LaTeX equations, etc. Multi-line responses are fine too since I will be adding end of response tokens to support them.

Datasets from different anons can be weighted so that people can finetune models to their specific preferences and still benefit from having a large sum of data to train on. People will be able to finetune models for others too if necessary since it only takes a few hours.

# 113
>>15806
>Thanks for wanting to help.
Happy to help Anon. I found this page, is that right?
https://transformer.huggingface.co/

>The dataset software requires running the language model locally to generate samples and it's 700 MB.
OK that's fine, 700MB I can handle. It would take me a few days to download, but some like 10's of GB is way too much. Please let me know in baby-steps what to do to help, and I'll try to dedicate several hours each week when I'm working.

# 114
>>15815
Yeah that's it. I just realized though you probably need to download PyTorch which is around 4 GB. I could rig up a quick and dirty C++ implementation but it would take me a week or two at least. Libtorch is 300 MB CPU-only or 1.2 GB with CUDA.

# 115
>>15816
I guess the quick and dirty CPU then?

# 116
>>15817
Sure, working on it now. I've been meaning to do it anyway to run language models on my Raspberry Pi. I'll post back in a week with an update.

# 117
>>15833
Good, I look forward to helping you Anon.

# 118
>>11924
>gpt2tc
Seems like a good utility, potentially lowering some of the hardware requirements for a successful model.
However, its underlying tensor library (LibNC) has its source withheld by the author. This might be a complication, depending on what strings he decides to attach to its release.

# 119
>>15837
I'm pretty rusty and wasted a lot of time this week trying to figure out a confusing bug that turned out to be a stack buffer overflow, but I hunted it down and got it fixed. I have half of GPT-2's tokenizer done, a basic tensor library, did some of the simpler model layers and have all the basic functions I need now to complete the rest. I'm hoping it'll be done by Friday.

>>15838
Yeah that's a real bummer. It doesn't include a license either. Implementing GPT-2 from scratch has been a fun learning experience though. I'm looking forward to implementing other models so they can be run on an SBC or inside a game with minimal requirements.

# 120
>>15911
>I'm pretty rusty and wasted a lot of time this week trying to figure out a confusing bug that turned out to be a stack buffer overflow, but I hunted it down and got it fixed. I have half of GPT-2's tokenizer done, a basic tensor library, did some of the simpler model layers and have all the basic functions I need now to complete the rest.
That sounds awesome, actually.

>I'm hoping it'll be done by Friday.
I look forward to it. Anything else I could be downloading in the meantime?

# 121
>>15912
Good idea, I hadn't even made a model file format for it yet. The model is ready for download now (640 MB): https://mega.nz/file/ymhWxCLA#rAQCRy1ouJZSsMBEPbFTq9AJOIrmJtm45nQfUZMIh5g
Might take a few mins to decompress since I compressed the hell out of it with xz.

# 122
>>15924
I have it, thanks.

# 123
>>15989
I got pretty burnt out from memory debugging and took a break from this but I'm gonna take another run at it this week.

I made some advances in the meantime with training the full context size of GPT-2 medium on a 6 GB GPU by using a new optimizer and have most of the human feedback training code implemented in the new training method. So I'm revved up again to get this working.

# 124
>>16090
>I got pretty burnt out from memory debugging and took a break from this but I'm gonna take another run at it this week.
nprb, I can hardly imagine.

>I made some advances in the meantime with training the full context size of GPT-2 medium on a 6 GB GPU by using a new optimizer and have most of the human feedback training code implemented in the new training method. So I'm revved up again to get this working.
That sounds amazing actually. Looking forward to helping.

