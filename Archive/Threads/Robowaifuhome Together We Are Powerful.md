# 1
The biggest hurdle to making quick progress in AI is the lack of compute to train our own original models, yet there are millions of gamers with GPUs sitting around barely getting used, potentially an order of magnitude more compute than Google and Amazon combined. I've figured out a way though we can connect hundreds of computers together to train AI models by using gradient accumulation.

How it works is by doing several training steps and accumulating the loss of each step, then dividing by the amount of accumulation steps taken before the optimizer step. If you have a batch size of 4 and do 256 training steps before an optimizer step, it's like training with a batch size of 1024. The larger the batch size and gradient accumulation steps are, the faster the model converges and the higher final accuracy it achieves. It's the most effective way to use a limited computing budget: https://www.youtube.com/watch?v=YX8LLYdQ-cA These training steps don't need to be calculated by a single computer but can be distributed across a network.

A decent amount of bandwidth will be required to send the gradients each optimizer step and the training data. Deep gradient compression achieves a gradient compression ratio from 270x to 600x without losing accuracy, but it's still going to be using about 0.5 MB download and upload to train something like GPT2-medium each optimizer step, or about 4-6 mbps on a Tesla T4. However, we can reduce this bandwidth by doing several training steps before contributing gradients to the server. Taking 25 would reduce it to about 0.2 mbps. Both slow and fast computers can contribute so long as they have the memory to hold the model. A slower computer might only send one training step whereas a fast one might contribute ten to the accumulated gradient. Some research needs to be done if a variable accumulation step size impacts training, but it could be adjusted as people join and leave the network.

All that's needed to do this is a VPS. Contributors wanting anonymity can use proxies or TOR, but project owners will need to use VPNs with sufficient bandwidth and dedicated IPs if they wish that much anonymity. The VPS doesn't need an expensive GPU rental either. The fastest computer in the group could be chosen to calculate the optimizer steps. The server would just need to collect the gradients, decompress them, add them together, compress again and send the accumulated gradient to the computer calculating the optimizer step. Or if the optimizing computer has sufficient bandwidth, it could download all the compressed gradients from the server and calculate the accumulated gradient itself. My internet has 200 mbps download so it could potentially handle up to 1000 computers by keeping the bandwidth to 0.2 mbps. Attacks on the network could be mitigated by analyzing the gradients, discarding nonsensical ones and banning clients that send junk, or possibly by using PGP keys to create a pseudo-anonymous web of trust.

Libraries for distributed training implementing DGC already exist, although not as advanced as I'm envisioning yet: https://github.com/synxlin/deep-gradient-compression

I think this will also be a good way to get more people involved. Most people don't know enough about AI or robotics enough to help but if they can contribute their GPU to someone's robowaifu AI they like and watch her improve each day they will feel good about it and get more involved. At scale though some care will need to be taken that people don't agree to run dangerous code on their computers, either through a library that constructs the models from instructions or something else. And where the gradients are calculated does not matter. They could come from all kinds of hardware, platforms and software like PyTorch, Tensorflow or mlpack.

# 2
>>8958
I think this is both a good idea and one that has been suggested here on /robowaifu/ before. But the basic fact is that very few have the knowledge to contribute meaningfully to the actual development of such a distributed system, even if they have favor towards the basic premise itself.

Accordingly, these issues all come immediately to my mind;
a) It will need to be a push-button-simple setup for Anons who are willing to contribute their electricity and bandwidth to this endeavor. Just like Folding@home is, for example.
b) The majority of anons can't be expected to understand the nuances of AI techniques & technologies. They just want their robowaifus to talk to them effectively.
c) As you already clearly suggested, both security and anonymity are issues. If Anons don't trust the basic infrastructure itself, they are quite unlikely to participate in it.

Perhaps the model that SETI@home and Folding@home follow (including the basic work-distribution framework) can be utilized here successfully. Oddly enough, they don't seem to have many issues with people worrying about security & anonymity (I've contributed to the latter myself personally). OTOH, they aren't working towards a goal that has the potential to cause more than half the world's Western, (((pozzed))), population to scream '''RAEEEEEEEEEP!1111111''' either. :^)

You seem to have some solid ideas and suggestions. Perhaps if you fleshed out specific details and approaches for the development and production roll-out of it, that would help further. I imagine there are probably a fair number of anons who casually roll in and out of /robowaifu/ from time to time who have skills in web development and systems administration for example. If there was a clear-cut set of doable goals and methodologies spelled out clearly, then some of these visiting anons might actually decide to lend a hand to this project. 

Personally, I can program in C++ a bit, but don't really have much else to contribute to this specific project afaict. Not that I'm unwilling to help out with it, but I can't take more on my plate at the moment to learn whole other sets of skills. I'm not sure I can see that being an application developer would bring much to the table here -- please correct me if I'm wrong. So, in that sense I'm basically just another anon who can contribute a modest amount of compute cycles from my computers. But again, there are plenty of others who '''do''' have the needed skills who come through occasionally. Getting them interested could be key here.

This is definitely worth investigating. And as an anon here pointed out, the availability of inexpensive used -- but powerful -- GPUs could be just around the corner for us all >>8954 . Maybe the timing for having a Robowaifu@home project is fast approaching being ripe.

# 3
>related
>>5811 (and following)

# 4
One modest suggestion I'd make to the project is this, ''don't name it Robowaifu@home''. Having to explain to your parents this program you're running all hours of the day an night on their computers is actually intending to help give the world, well, ''robowaifus'' could be embarrassing at best.

IMO it would be much better to call it RW@home. 'Robot World' could be the acronym's alleged meaning ("Hey, it's so I can grow up and work for SpaceX Dad! Please just think of Elon Musk for once, OK?"), but ofc we in the know realize it's '''R'''obo'''W'''aifu@home. 

That's it.

# 5
>>8958
>Or if the optimizing computer has sufficient bandwidth, it could download all the compressed gradients from the server 
I'd suggest you take the former tack to optimize bandwidth consumption. GPU power-growth curve is still well outperforming so-called ''Moore's Law''. Bandwidth growth, however, isn't. Telecom infrastructure build-out is both slow and expensive and will likely remain that way for the foreseeable future.

Add on top of that housing unit demand for (((Netflix))), et al, and you have a recipe for high-competition for available bandwidth that will only grow over time. GPU power growth OTOH is actually still on a steady projection for ever-better price/performance.

# 6
The way hentai@home created a giant distributed CDN built off of bittorrent was to provide the people that run instances of it a local copy of the media they want that gets automatically updated with proper tags instead of having to deal with downloading it manually themselves. There's also a reward structure that lets users download at high speeds so it turns into an offsite backup service for their hentai collection.
https://ehwiki.org/wiki/Hentai@Home

Asides for the altruistic donation of bandwidth and GPU processing power to help speed development of an AI they might want to use what would running robowaifu@home provide as a benefit to the end user?

# 7
>>8963
>The majority of anons can't be expected to understand the nuances of AI techniques & technologies. They just want their robowaifus to talk to them effectively.
Yea, some thought is gonna have to go into how to utilize people's computers effectively and automatically. They might only have a 2 GB toaster GPU. While not ideal it could still help prototyping smaller models. I think feedback will be important otherwise people will shut the program off one night and forget to turn it back on when they don't see any results. Larger models could be compressed for people to use on their computers so they can directly reap the benefits of their contributions. It'll need to be able to run on Windows, Mac and Linux to reach the most amount of users.

I imagine when they boot up this distributed training program it shows a list of projects their hardware is capable of contributing to and the user selects which one they want to help. Part of the responsibility will be project owners making their project pages look good enough that people want to lend their GPUs. Users could also dedicate their GPU to a project owner so their GPU can be used for any project or prototype by them.

I plan on making a simple version soon to utilize all my computers and friends' computers. I'm sure a proof of concept will eventually attract other developers. The biggest issue will be securing it without nerfing what devs can do with it. The simplest solution would be to review code, manually approve projects and basically have package maintainers. And devs could choose to join untrusted projects that haven't been approved yet since they can review the code themselves. It wouldn't be much different from the risk taken when installing open-source software. But there could also be a sandboxed version where people can prototype vanilla models by defining hyper-parameters and network structure from existing modules.

>>8964
>Would you guys contribute GPU cycles to create a GPT-3 clone?
The problem with trying to clone GPT-3 is the model is too big to fit on anyone's GPU or in memory. The full size GPT-3 requires around 16 x 48GB GPUs and likely they have a few hundred or thousand, not just 16, doing gradient accumulation. The heads can be split up across devices in parallel but the layers can't be so easily and would incur a huge cost going back and forth from GPU/RAM, plus there's the bandwidth cost of sending all that data to the next computer to perform the next substep of the training step. It would be really inefficient and the whole network would have to work together to do any inference on the model.

>>8965
Its purpose would be much more general. People could use the system for doing other projects unrelated to robowaifus and AI, such as finding twin primes or something else. It would be more like a crowd-sourced cloud computing platform. Adding a privacy mode is a good idea though in case people do give embarrassing names to their projects so other people using the computer only see 'Distributed Computing' or something like that.

>>8966
If necessary the bandwidth can be greatly reduced at the expense of accuracy. A little bit of noise from high compression doesn't seem to impact gradients too much since they're already quite noisy. We don't have to be too pessimistic about bandwidth growth though. Once Starlink finishes rolling out satellites it will have 1 Gbps connections. ISPs are already getting nervous their cartel is threatened and have been doubling bandwidth to customers to keep them.

>>8982
>what would running robowaifu@home provide as a benefit to the end user?
A virtual waifu and all her functions. Once basic chat is solved people are going to expand their virtual waifus to perform other functions such as playing video games, composing music, drawing, debating, summarizing research papers, searching the web, etc. People wanting these functions will contribute to those projects and receive a compressed version of the training results that their hardware can run or the full size version if they wish. Alternatively, someone could create a marketplace where people can pay crypto for compute, but I'm not familiar with how to do that. I think SingularityNET does something like that with AI services.

# 8
>>8990
> It would be more like a crowd-sourced cloud computing platform
I see. Then all the more argument not to name the system Robowaifu@home. Some variant of '''CrowdCloud''' might be a more appropriate choice. Actually, a name like that could probably attract investment money, if you can secure it.

# 9
>>8991
Once you get investors you no longer own your projects. It's theirs to exploit. I think the whole point of this is to decentralize AI and avoid nobodies telling us what we can and can't compute and to give us an edge to compete with Big Tech. If Big Tech owns the platform they're not going to let that happen.

# 10
>>8990
>If necessary the bandwidth can be greatly reduced at the expense of accuracy
I see. You did mention that before. That's actually rather convenient that you can make trade-offs and dial in functionality like that.
>Once Starlink finishes rolling out satellites it will have 1 Gbps connections.
I sure hope they pull it off, and then give it away practically for free. **A man can dream.** 

One point to mention here are goyphones *[shudders externally]*. If you could somehow quantify the 'total compute power potential' as a measure of which silicon die technology is being most heavily rolled out, I suspect the phones are already ahead of servers/desktops. Throw in Starlink etc. and mobile represents a sizable potential for raw compute power.

# 11
>>8990
>They might only have a 2 GB toaster GPU.
Even if they have a 16GB high end GPU it might be incompatible with some tasks as AMD uses a different memory structure that can't run many popular CUDA compute libraries. That's why my low end 4GB nvidia GPU almost tripled in price in the last year while similarly specced or slightly more powerful AMD cards haven't.

>But there could also be a sandboxed version
Nowadays thanks to PCI passthrough with virtualization this project could be 100% OS independent with little to no performance penalty on top of having built in security. That requires very modern hardware to work properly but virtualization is going to be a huge game changer in personal computing in the upcoming decade. Wendell from Level1Tech has been talking about the potential of this as it comes out of the server space for years now. He's also one of the few people that probably has 16 x 48GB GPUs in a server rack but is smart enough to both use them to keep quiet about it.

>A virtual waifu and all her functions.
I can understand a collaborative effort at optimizing AI rather than having everyone do their own thing or replicate the same work but what would be the benefits of running RW@H compared to just downloading the models it has done and running it on your own hardware without using up extra bandwidth or electricity? That's the hard thing to come up with and would really sell this project.

# 12
>>8995
>That's the hard thing to come up with and would really sell this project.
Honestly, if the only pitch is 'results-driven' then not likely to even get off the ground (much). The altruism that have made all the '''X@home''' projects successful is White people with a sense of 'helping out for the greater good'. It's very culture-specific. If it simply boils down to nothing but shekel-grubbing, 'what's in it for me?' mentality then no probably not going anywhere.

Regardless, even things like BitTorrent have proven successful when only a very small number of us seed and 98% of only-self-interested exploiters don't. While that's quite a different model than this, it at least can be somewhat informative for the social dynamics of the thing.
>tl;dr
People will do it b/c they want to help. You know, give then bonus points for e-peen or jewel power-ups or something.

# 13
I think this is a brilliant idea, anon! I once joined a distributed computing group called "Mindmodelling@home" using BOINC (they were interested in curing neurological diseases, but of course I was there in the hopes of advancing A.I. for future robowaifus). But I left after a few months because they never seemed to post any updates and their project appeared to be dead. 

If something like this were to become reality, I'd upgrade my PC just to help crunch work units! We already have various options for robot bodies and synthetic voices, but it's the A.I. where we are severely behind. 

I also agree with >>8965 though, that we should name it something agreeable and generic like "robotworld@home" or "droidschool@home". So that the Western MSM has less to latch onto.

# 14
>>9000
>"droidschool@home"
That's not bad IMO. What about something like "Mindschool@home" ? That seems like it could basically be construed to mean just about anything. Mommies might even approve of something named that! :^)
>"How many roads must a man walk down?"
**>42**

# 15
>>8993
This is a very good point. I think we should keep things BSD/MIT licensed so any anons can take our ideas and run with it. But you're correct about investors basically being sharks. In fact most of them have a fundamental MO of ousting the founders before long. E.G., ''Cisco Systems'', and countless others.

# 16
>>8990
>The problem with trying to clone GPT-3 is the model is too big to fit on anyone's GPU or in memory.
Hmm, I see. Well, my guess is that this system could be re-purposed relatively easily for different types of AI problems/solutions correct? What about something like Pattern-Exploiting Training (PET) ?
(>>5793, >>5799 and following)

Also, I think what Anon mentioned here >>9000
>BOINC
Isn't that a generalizable type of flexible framework for this kind of thing? Do you think your project could utilize this?

# 17
>>8995
>but what would be the benefits of running RW@H compared to just downloading the models it has done and running it on your own hardware
It would be good if people prefer giving their hardware to train new models and functions that don't exist yet instead of wasting power reinventing the wheel or trying to get a 1% improvement on old models. If someone has a good idea people will want to try it and help out, then move on to the next project once the model reaches an acceptable result.

>>9009
I'm not familiar with BOINC but it appears capable of running Python with some headaches to deal with to make sure package versions are consistent across different platforms and systems. Using virtual environments should take care of that, but it's not really clear what their API is capable of doing and the Python wrapper has limited functionality, which might be missing necessary things for distributed training. I couldn't find any Python machine learning projects on it so I imagine it's lacking something.

>this system could be re-purposed relatively easily for different types of AI problems/solutions correct? What about something like Pattern-Exploiting Training (PET) ?
Yeah, any model that people want to create. The PET model is doable with 223M parameters. That's 2/3rds the size of GPT-2 medium. Beating GPT-3 in a small domain of few shot learning is remarkable with 0.1% of the parameters but it doesn't mean that PET excels in everything else.

GPT-3 has other glaring flaws in it as well like seeing everything as byte-pair encoded tokens, which gives it trouble with misspelled words and discerning patterns in long strings like ABC.. etc. that a tiny character-level model can pick up on easily. Some informal research has found that GPT-3 seems to be just using the structure of the sentences and the parts of speech to predict text, rather than the actual meaning of the words. VAEs on the other hand can interpolate between the meanings of sentences. For example, incrementally changing a bad review into a good one. They're notoriously difficult to train with GPUs but can still benefit from gradient accumulation and distributed training.

There's a lot of other cool models we could try out even with only seven computers contributing. That would reduce a week of training into one day. With 24 what would take two years could be done in only a month, assuming similar performance between them. With 100 or 200 we would have no problem rapidly iterating prototypes and advancing, and for most models we wouldn't reach diminishing returns until hitting around 1k, with benefits vanishing completely by 10k.

# 18
>>9018
>VAEs
Just in case this guy has dug up something important to us here.
https://github.com/matthewvowels1/Awesome-VAEs

# 19
>>9018
>BOINC
>virtual environments
<"Volunteer Computing and Virtualization - CERN Indico"
>

>There's a lot of other cool models we could try out even with only seven computers contributing. That would reduce a week of training into one day. With 24 what would take two years could be done in only a month, assuming similar performance between them. With 100 or 200 we would have no problem rapidly iterating prototypes and advancing, and for most models we wouldn't reach diminishing returns until hitting around 1k, with benefits vanishing completely by 10k.
You don't have to convince me Anon, I'm already 'part of the choir' with you. OTOH, how do you convince this Anon >>8995 ? While I wish his point was entirely invalid, the simple fact is he's right. The vast majority of unused power out there resides on anon's computers who have grown accustomed to a 'gibbs me dat' mentality (not that I'm impugning ''him'' in any way in this regards, he's simply pointing the issue out). OTO-OH, many of these ''X@home'' projects '''do''' succeed at attracting numerous volunteer contributors -- even up to 100'000 of them.
https://en.wikipedia.org/wiki/Folding_@Home#Patterns_of_participation
>

So, how do we successfully promote your idea far and wide? It will take a large exposure IMO to overcome the greed factor already mentioned and find sufficient altruism needed for good success.

https://en.wikipedia.org/wiki/Distributed_computing
https://en.wikipedia.org/wiki/Citizen_science

# 20
>>9021
>So, how do we successfully promote your idea far and wide? It will take a large exposure IMO to overcome the greed factor already mentioned and find sufficient altruism needed for good success.
I was thinking of the game route, where gamers literally train their in-game waifus.
I was thinking a "gacha" game originally, but maybe a PC option awards some sort of in-game cosmetic or reward for contributing processing power.
Although, if it was to become a PC game, then my original plan of simplicity for mobile phone purposes means I have to actually attempt to think up an entertaining game that would attract gamers who need an excuse to donate such processing power.
I am currently looking into certain legal aspects, and also the huge issue of making such "gacha" games addicting...the art.
It seems that finding a good artist that wouldn't break the game on a rando niche start-up is going to be difficult. I rather program, but taking some time so I can learn how to draw might be my last resort just to get something started.

# 21
Idea: What if we tried to make a game of some kind out of Robowaifu@home OP? Like the ''Foldit'' guys did. Can't we sort of interactively 'give grades' to the AI's work and help accelerate it towards actual semantic understanding that way?
>

# 22
>>8990
>Yea, some thought is gonna have to go into how to utilize people's computers effectively and automatically. 
That's going to take expertise to determine. The local client hardware can be probed for capabilities easily enough, but associating that with actual AI modeling potentials isn't something for a neophyte.

>They might only have a 2 GB toaster GPU. While not ideal it could still help prototyping smaller models. 
True enough. Hopefully these 'smaller models' will become ever-more important in the future as our capabilities improve with time.

>I think feedback will be important otherwise people will shut the program off one night and forget to turn it back on when they don't see any results. 
Very true. Even if it's simply some kind of graphic related to the actual work going on, similar to ''Folding@home'''s approach.

>Larger models could be compressed for people to use on their computers so they can directly reap the benefits of their contributions. 
Some kind of reduction pre-processing?

>It'll need to be able to run on Windows, Mac and Linux to reach the most amount of users.
Obviously. I'd also suggest the potential of smartphones be investigated too.

>I imagine when they boot up this distributed training program it shows a list of projects their hardware is capable of contributing to and the user selects which one they want to help.
Sounds like a good plan.

>Part of the responsibility will be project owners making their project pages look good enough that people want to lend their GPUs. Users could also dedicate their GPU to a project owner so their GPU can be used for any project or prototype by them.
Please tell us more about project managers and their roles?

>I plan on making a simple version soon to utilize all my computers and friends' computers. I'm sure a proof of concept will eventually attract other developers. 
I'm sure we'd all be interested in seeing the specific progress you're making as you go along with that Anon.

>The biggest issue will be securing it without nerfing what devs can do with it. 
It's easy to see why that could be a tension of interests. Some kind of sandboxing springs to mind just offhand.

>The simplest solution would be to review code, manually approve projects and basically have package maintainers. And devs could choose to join untrusted projects that haven't been approved yet since they can review the code themselves. It wouldn't be much different from the risk taken when installing open-source software. 
I like the basic idea of 'trustworthy' package maintainers. We're all basically dependent on them today, and that approach generally seems to work out OK.

>But there could also be a sandboxed version where people can prototype vanilla models by defining hyper-parameters and network structure from existing modules.
>"by defining hyper-parameters and network structure from existing modules"
Mind clarifying that for us with more detail. Not sure I understand what that really means Anon.

# 23
>>9028
It depends on the model but people could do this for their projects.

>>9029
>The local client hardware can be probed for capabilities easily enough, but associating that with actual AI modeling potentials isn't something for a neophyte.
Performance tests can be done on various tasks like matrix multiplication, FFT, CNNs, RNNs, transformers, etc. and projects can be profiled and estimated with the parameters. It'll be a big task but I don't think it'll be something to worry about in the beginning. We'll likely be throwing every CPU and GPU we have at one task at a time rather than distributing them across multiple. Even with 2-5 projects the biggest performance difference will be from allocating GPUs to CNNs and letting RNNs have the CPUs.

>Some kind of reduction pre-processing?
Most of the weights of models can be pruned without much accuracy loss due to the sparsity of useful parameters. This allows massive models to run on mobile devices. It will be necessary for the work produced to be useful to people. If you use unpruned models for speech recognition, speech synthesis, and text generation together, you're looking at needing 16+ GB to run all that. With pruning though that can be brought down to 2-4 GB or even less by accepting a lower accuracy.

>Please tell us more about project managers and their roles?
It'd be like managing and maintaining any open-source project. I imagine some work will be involved checking that contributors are sending good data and not using incorrect training data until such tests are automated. Some additional work will be needed later to profile a project and make the information available to others so they can see if their hardware is a good match to contribute. And of course pruning models according to baseline contributor performance and resolving issues so everyone use them.

>"by defining hyper-parameters and network structure from existing modules"
>Mind clarifying that for us with more detail.
Rather than writing Python code for models the sandboxed version could use its own model format that just specifies pre-built modules, the hyper-parameters defining how many parameters those modules use, and the connections between them. It goes in hand with the idea of an AI toolkit where you can drag and drop modules and connect them in a graphical interface without coding anything. These models would be generally safe to run from untrusted sources, far safer than stuff installed from Python's pip, so long as security exploits are minimized in the software itself.

# 24
>>9026
It will be interesting to see what you come up with exactly, Anon.

>>9031
>f you use unpruned models for speech recognition, speech synthesis, and text generation together
Yes, I suppose all 3 will be needed for suitable virtual waifu apps (including animation too ofc, but that should be pretty lightweight, computation-wise).

>It goes in hand with the idea of an AI toolkit where you can drag and drop modules and connect them in a graphical interface without coding anything.
That's actually a very nice idea Anon. And as far as the specified code/models being safer than using python's pip, that would be very welcome. I hope someday we can just move away from the python ecosystem entirely. It seems fraught with numerous difficulties to me. OTOH, I'm obviously in the minority here. 'Computer Scientists' from the most prestigious universities today obviously think it's the single best thing since anything ever. :^)

# 25
>>8990
>Starlink
I don't really trust Elon with these things, look at Tesla's services. He definitely isn't /ourguy/ and will provide it at a cost of "freedom".
> Once basic chat is solved people are going to expand their virtual waifus to perform other functions such as playing video games
This has a ltot of potential but it's prob not a good idea, since there doesn't exist just one game and it would become a Herculian task to try to appease everyone.
>composing music, drawing
Again, it's very vague and doesn't necessarily help the project in of itself nor necessarily appease our interests. 
>debating
We already have many bots who can do that and we know for a fact it's not that good of an idea.
>summarizing research papers
This is actually very realistic. There has been made a paper around this and an AI which can do it so it's very easy to implement (we just need codemonkeys for that)
>searching the web
Unless it can do it in a non-pozzed way, it's practically useless.
>Alternatively, someone could create a marketplace where people can pay crypto for compute, but I'm not familiar with how to do that.
Don't care about that too much, it's still not worth it to enough people for it.
My suggestion would be to first make an AI that, just like GPT-3, can code programs that we tell it to. Once we automate the coding part, the rest will become much easier and we won't have to worry too much about it.

# 26
>>9086
>My suggestion would be to first make an AI that, just like GPT-3, can code programs that we tell it to.
I'm quite skeptical of the fundamentals of that claim. I'm familiar with the article that made the statement, but he basically pinned the entire notion on a single addition operation. It just returned an exemplar from it's working corpus that performed that exact operation already. I would argue the lexicographic problem of the AI digesting the command "Waifu, add 3 plus 4 for me" is much more difficult.

We'll probably get there in the future with ''software programming waifus'', but it certainly isn't here just now.

# 27
>>9000
https://www.mlcathome.org/mlcathome/
I've managed to find a new project that's just popped up using BOINC. It seems to be something for "Un-black-box-ifying" a lot of traditional machine learning algorithms.

# 28
>>9105
Thanks! Just in case anyone, like me,  can't get to it via Tor:
https://web.archive.org/web/20201225185201/https://www.mlcathome.org/mlcathome/

# 29
Seems like this could be somewhat related to your goals OP.
https://github.com/tensorflow/mesh

Please forgive my naivete if this isn't related.

# 30
>>8995
So does that mean even AMD GPUs with support for ROCam and having the appropriate motherboards would not be able to support this future crowd computed robowaifu project?

# 31
>>10532
It would depend on the code libraries that are used. Right now most of the most popular ones for AI are designed for Nvidia thanks to CUDA being the industry and academic standard. It might be possible to port it over to run on AMD's GPU computing platform if there's enough demand.

My comment was about how the memory was laid out on some AMD card, this isn't the first time this problem comes up in the GPU world. Last time it was with the GTX 970 which ended in a class action lawsuit. This time it's just an issue with cryptocurrencies that need large amounts to store the entire blockchain, some of them can't be mined on AMD cards even if the CUDA code was ported over.

What I'm going to do in the future is get two cards, a powerful AMD one due to better drivers on GNU/Linux and a weaker CUDA capable one for use in a virtual machine so all my bases are covered.

# 32
>>10533
Not him, but thanks for the explanation Anon.

# 33
>>10533
So OpenCL is dead in the water or something?

# 34
>>10550
(Not the same anon) AMD uses Rocm which is supported by PyTorch since recently. AMD has professional cards, Rocm seems to primarily support those: https://www.reddit.com/r/hardware/comments/ly6j3h/pytorch_18_supports_amd_rocm/gpr91eq and https://www.reddit.com/r/Amd/comments/nhpsnf/state_of_rocm_for_deep_learning
Long story short, till AMD invests much more into the eco system: Forget it.

# 35
>>10556
Welp that is quite unfortunate that AMD doesn't bother to improve Rocm support. I find it a bit odd that AMD doesn't try to compete with Nvidia on this part too and instead allows Nvidia to gain a whopping market share in machine learning.

# 36
>>10563
What people tend to forget: AMD is much smaller than Nvida. They didn't have the money to do this, thanks to their underdog status in the past. That market might also be less relevant. 
But then, RocM and underlying technologies like OpenCL are open source, and Intel will release their own discrete GPUs soon, and there might be other players, like Apple for example, or other companies working with Arm based chips and a GPU.

# 37
>>10568
> or other companies working with Arm based chips and a GPU.
Sadly, certain (((interests))) in the US Govt approved Nvidia's buyout of ARM, and the sale has been completed. 

Nvidia owns ARM now, lock, stock, and barrel.

# 38
>>10568
Hmm right, I recall there was a news or blog post what's the difference? I forget, anyway which says that only the bri'ish people buy AMD because it is cheaper and the other people are all buying Nvidia only. 
>>10577
>Nvidia owns ARM completely now
>US Gov' sees no problem with a giant getting even bigger
This shit just makes me sad.

# 39
>>10591
>This shit just makes me sad.
It makes me __''angry''__, actually. Just follow the money, Anon, just follow the money.

# 40
>>10577
A month or so ago, the talk was that Nvidia buying ARM isn't finished bc Europe and China. Though, I didn't look into it today. ARM also licences it's designs to others, and they certainly won't be allowed to just stop that, if they even want to. I also assume this would only be relevant for future designs, hypothetically. Apple might already be quite independent in designing their own stuff, and there's still Power and Risc-V.

