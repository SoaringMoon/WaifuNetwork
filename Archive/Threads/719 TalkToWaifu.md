# 1
Anyone know what happened to the TalkToWaifu GPT-2 AI? I saw some screenshots of what I assume was the trained AI and it was great for a single dev. Recently went back to their Gitlab page and the user account had been deleted and remade, and the Github repo (https://github.com/kokubunji/TalkToWaifu) hasn't been touched in 9+ months.

Anything out there more recent that this, an AI that has no human cultural restrictions? Corps love to add in shit to AI so they won't say anything racist, sexist, xenophobic, anti-Semitic etc etc you get the point.

# 2
>>7978
That guy left the board and robowaifu network for complex reasons which I'm sure no one wants to discuss here (again). If you or anyone else knows about how to train such networks or someone is willing to learn it, then it should be easily reproducable. There are enough resources on the web to learn about how to do that, assuming one has the time, nerves and brains to do so. The ideas of the anon which left are also in some of the threads here, so you can look at that. Again: How to get started with GPT2 or building something better is certainly covered in some forum which focuses on that topic.  For all I know, no one here is currently working on something like it.
Talk2Waifu was no AI, only a text generator. There is no AI available which is close to a human anywhere. This has to be build first anyways. A text generator is also not a chatbot, he only used it as such, or as input for one, which might even not be a good starting point. 

We have plenty of threads here where you can participate:
AI, chatbots, and waifus        >>22
Robowaifu Psychology Thread     >>2731
(Robo)Waifu personality thread  >>18
NLP General     >>77
Datasets for Training AI        >>2300
The Language Problem    >>6937
Wifu that gives you Hope        >>107
AI Software     >>85
Can Robowaifus Experience Love? >>14
AI Design principles and philosophy     >>27
Robowaifu Fail-safety   >>1671
Mycroft: Open Source Alexa      >>402
Downloadable AI for robots?     >>244
Robowaifu-OS & Robowaifu-Brain(cluster) >>201
Avatars >>2956

Getting a good AI will take more time than getting some options for bodies developed. So it's better to focus on that and on the low hanging fruits around AI and chatsbots.

# 3
>>8006
>which I'm sure no one wants to discuss here (again)
i'm a new-fag
anyone got a copy-pasta as to what the complex reason is? or a TLDR?

# 4
>>9114
MInor e-drama.

# 5
There's a slightly newer version of TalkToWaifu with some bug fixes here: https://gitlab.com/robowaifudev/TalkToGPT2

I've been working on an update that can use multiple different models, let chatbots talk to each other, and that has a training mode to guide the model towards generating better responses. TalkToWaifu was originally just some quickly hacked together code when GPT2 came out to show that it could be used as a chatbot. GPT2 doesn't make a good chatbot because it lacks an external memory to remember past events, and training a new GPT2 model from scratch would take a 100 years because of how inefficient it is.

Fortunately there have been a lot of advances that make training a transformer model that performs nearly as well more feasible now, but more research needs to be done on getting it to work well with a recurrent neural network. Currently I'm experimenting with combining transformers with the non-saturating recurrent unit (NRU) that excels at learning long-term dependencies and using ReZero and parameter sharing to help the gradient reach deeper back in time. If it's successful the model will be capable of learning without training and only require a 2 GB GPU to fine-tune instead of a $9000 one. However, it will likely quickly forget what was learned until I figure out a better way to use neuromodulation to prevent forgetting.

In the meantime there's someone else working on neural net chatbots here if you want to check them out. They're pretty good:
https://github.com/JEF1056/Jade_T5
https://github.com/JEF1056/Jv6

# 6
>>9115
why the fuck is there E-Drama on a board that is designated for building robo-waifus.
where is the connection?

# 7
>>9124
Thanks, mate.

# 8
>>9124
>'''MARRY ME JADE!111'''
>no.
Leld.

