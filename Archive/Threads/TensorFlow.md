# 1
Tensorflow is currently the hot Deep Learning framework. The engine is written in C++, and the scripting API for it uses Python.

www.tensorflow.org/versions/r0.12/get_started/index.html
https://archive.is/0x7OR

en.wikipedia.org/wiki/TensorFlow
https://archive.is/7GvCZ

github.com/tensorflow/tensorflow
https://archive.is/Twslg

www.youtube.com/watch?v=l6K-MFgIEjc&index=7&list=PLlJy-eBtNFt4CSVWYqscHDdP58M3zFHIG
https://archive.is/svYnL

www.youtube.com/watch?v=bYeBL92v99Y&list=PLjJh1vlSEYgspxwsa5be5TVm3n9JNNC9G&index=6
https://archive.is/d3b1G

https://www.invidio.us/watch?v=3d34Hkf7KXA

# 2
For low power tensorflow on the go, tensorflow lite.

hackaday.com/2017/11/23/smarter-phones-in-your-hacks-with-tensorflow-lite/

# 3
>>1012
>Google has just released a new solution, the developer preview of TensofFlow Lite for iOS and Android and announced plans to support Raspberry Pi 3

I'm actually more excited about this anon:
>plans to support Raspberry Pi 3
as the Pi 3 is open sauce, effectively. Nice find, thanks!

# 4
I wonder if pic related is something how waifu2x works?

# 5
>>1014
You're not far off, waifu2x does use deep neural networks. Good eye Anon.

# 6
NLP course
[[1474

# 7
github.com/astorfi/TensorFlow-World-Resources

# 8
The new NVidia Xavier has TF processors (TensorFlow processing directly on specialized hardware) on board.

# 9
>>1018
yeah they're optimized for inference but not learning iirc, so glass half something… you're going to have to do more than just flash some tensorRT code, you might need to install and run tensorflow on the board too if you need continuous learning

# 10
>>1019
>optimized for inference but not learning iirc
Are they? Hmm, I suppose you could find ways to burn most of the electrons up front. But yeah I'd like to study that. Sauce?

The issue w/ offline training is the need for (lots of) data itself. Maybe we can simply capture the telemetry and other data in a compacted raw form from the robowaifu in realtime, and then ship that over and process that on the home servers? Something like an offline 'Dream time'?

I think it would also be wise, especially during the early phases, to find a way to agglomerate various robowaifu's real-world experiences without actually surveilling anons. Having a wide variety of stimulus inputs to the networks and other systems would help speed up the process of moving her mind out of the 'mental uncanny valley' if you will. Again, a data input issue.

One relatively unobtrusive way to at least accelerate the semantic understanding process would be to create a shitposting robowaifu-chatbot. So I wonder if we can integrate one of these Xavier devices into the heart of a chatbot server with an eye towards eventual integration into an irl robowaifu

# 11
>>1020
>integration into an irl robowaifu as it's NLP core*

# 12
>>1020
I bring you sauce

>capture the telemetry and other data in a compacted raw form
Absolutely, then use some kind of async method to update the models, kinda standardize some of the models in that way

>without actually surveilling anons
I think this can be done, you can actually anonymize the data post collection too
(I might be talking out of my ass but it seems like it could be done using vector arithmetic- never tried it)

>accelerate the semantic understanding process would be to create a shitposting robowaifu-chatbot
Actually a friend and I were discussing using an EC2 instance to essentially crawl the web and create a giant semantic model of all the information we can get from the net as a jumping off point (compress everything on the net), not sure of its feasibility primarily due to cost. 

>integration into an irl robowaifu as it's NLP core
you have any specific chat engines in mind?

# 13
>>1022
I think you understand my idea correctly, and yes by your diagram if TF-RT is the runtime, then offline training will be the only viable onboard option. We can ofc have additional more general purpose h/w on board to take that load but why would we at this stage?

>anonymize
I want actual guarantees. The personal me is very, very concerned about Anon's security and privacy (including my own ofc). The nerd me trying to help solve this sees hordes of robowaifus in the wild as a ripe data source to help improve everyone's experience. We need to walk very carefully in this area. Again, I want guarantees. So for now it's strictly just an idea on the mind-map table, not a design goal.

>Chii keeps her own instantly-updated copy of the entire Interwebz on her local storage.
Kek. I admire the bravura. But just a simple shitposting-bot would be more than enough for now. :^)

>you have any specific chat engines in mind?
I assume we'll build it. I'm certainly open to suggestions but at this stage this is just floating ideas for me.

# 14
>>1023
kek to the ribs
yes ms

# 15
>>1024
Heh. BTW, rather than starting out with a big investment of your own time and energy, you and your friend might consider taking advantage of some of the the prior art in this field. There are several corpora already freely available. For example:
en.wikipedia.org/wiki/List_of_text_corpora

Stanford maintains a list particularly suited to NLP:
nlp.stanford.edu/links/statnlp.html

# 16
There's a web-based TensorFlow system you can't break.
playground.tensorflow.org

# 17
>related
[[4466

# 18
Relevant YT playlist.

TF training by an ML/AI researcher. In this I discovered Jewgle has a free, online facility to run your TF Python code on an honest TPU! or a GPU or a CPU, your choice. Did I mention it's free?

www.youtube.com/watch?v=er8RQZoX3yk&list=PL9Hr9sNUjfsmEu1ZniY0XpHSzl5uihcXZ

# 19
>>1029

# 20
Introducing TF-Coder, a tool that writes tricky TensorFlow expressions for you: https://blog.tensorflow.org/2020/08/introducing-tensorflow-coder-tool.html

"When manipulating tensors, one must keep track of multiple dimensions, tensor shape and DType compatibility, and of course mathematical correctness. Additionally, there are hundreds of TensorFlow operations, and finding the right ones to use can be a challenge.

Instead of coding your tensor manipulation directly, what if you could just demonstrate it through an illustrative example and get the corresponding code automatically? TensorFlow Coder (TF-Coder) makes this possible"

Not sure if it makes sense to post stuff like this here, since people using some software should probably follow all kinds of blogs via RSS. However, got this recommendation when I looked into Twitter after some time...

# 21
>>5777
>Not sure if it makes sense to post stuff like this here
No perfectly fine. Anything Tensorflow related goes ITT. Nice tool by the looks of it as well. Thanks Anon.

# 22
>>5777
noice

# 23
Would you guys contribute GPU cycles to create a GPT-3 clone?

# 24
>>5811
I'm certainly willing, but the need for obfuscation of the source (IP addresses for example) is a concern. What kind of an approach could be used for that?

# 25
>>5811
How many cores of my Raspi3 would be occupied by that?!? I have two of them, soon maybe also a Raspi4 or Jetson Nano. Then you could have one of the Raspies os so.
That aside, stuff like that is rather being done in datacenters. Alone our energy costs would be higher than theirs. Then, it would also depend who would be asking for it and how serious this was. Huggingface vs some anon on a imageboard...
Next issue would be, that the GPT approach has always been critizised, and now it seems to be done: >>5799

# 26
>>5814
>How many cores of my Raspi3 would be occupied by that
The Broadcom chips inside RPis actually have a pretty decent GPU for the power it consumes (low-power). Someone would have to create a system that could use that in a practical way for processing AI loads. So if someone solves that, then your GPU would be maxed pretty much (you'd want a heat sink kit for it), but the cores load could be kept to just one of the 4 available cores.

>Alone our energy costs would be higher than theirs.
I kind of think it's the other way around, but that aside the whole point of donating compute is that each of us bear a small(ish) part of the hardware and electricity costs.

Together if there are enough of us doing that can represent a total system far larger than any of us individually is likely to afford.

>trust
Yes, we'd need to have both a well-written description of the goal (each project for ''folding@home'' has something like this for example), and then some mechanism for accountability in the beginning would be essential as well, IMO.

Once a '''robowaifu@home''' system was up and running, and good AI results are coming from it for everyone, then I think that would speak pretty clearly all on it's own.

# 27
>>5812
Work requests could be posted somewhere online with the code and training data and the results uploaded to anonfiles or somewhere else. I think we're still a long way from doing any sort of distributed computing though. An easy way to do transfer learning needs to be made first, otherwise we'll just be training models from scratch again and again or getting stuck on a performance plateau, rather than adapting and evolving as new AI techniques come out and everything rapidly changes.

# 28
>>5816
>>5817
There's plenty of free and open source software for distributed computing like this available, making them execute TF training should not be too complex of a task. Package that into a container that has no filesystem acces and that runs through tor or something similar and we would have a start of a solution. 
Some of the software options run through a custom screensaver so we could even make it robowaifu themed.

# 29
>>5852
>Package that into a container that has no filesystem acces and that runs through tor or something similar and we would have a start of a solution. 
Yes, that's an interesting idea. If we can simplify that to the point it's easily security-auditable this approach might just work.

