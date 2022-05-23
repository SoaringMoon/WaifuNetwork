# 1
We could install a modified version of Mycroft as the personalities of our waifus, at least until we get something better:

www.youtube.com/watch?v=Ud3XLEGIu8U

A Raspberry Pi and a display can be gotten for $70:
www.amazon.com/LANDZO-Touch-Screen-320480-Raspberry/dp/B01IGBDT02/

Of course the battery is another ~$50.

# 2
Proprietary Russian Alexa clone. at least it's not Amazon.
lexybot.com/en/

# 3
>Open Source
It still relies on google's speech APIs, which is a pure cloud service.

# 4
>>470
After giving up on their own speech to text backend they've partnered with Mozilla.
mycroft.ai/blog/mycroft-speech-to-text-and-balance/

The main project uses Google for the time being but that's because it lets them offload computation. You need really powerful hardware to do accurate speech analysis in real time using Deepspeech while Google provides that service for free in exchange for data.

If you want a fully open source non cloud based Mycroft you can set it up that way.

# 5
>>471
DeepSpeech looks interesting. And the hardware you need to run it only has to be "powerful" for an IoT device, a modern desktop or gaming PC (with an Nvidia GPU) is more than enough to run it several times faster than realtime.

# 6
So, has anyone here set up Deepspeech on their own machine yet and tried it out? How good is it?

# 7
It would be an interesting way around putting too much hardware in a body sized body, have the thinking done on a server with it puppeting your robo-meido,

# 8
>>503
>have the thinking done on a server with it puppeting your robo-meido,
Yes, anon. I think that's more or less the idea. Have an in-home server setup designed and built for heavy processing, connect your robowaifu into it wirelessly (and securely!), and just offload the bulk of the computation onto the server. This would add a bit of complexity into the final solution, but not much.

The robowaifu's systems will necessarily be so complex in general, that a modest redistribution of the computing load will be only a relatively minor detail in the overall scheme of things.

# 9
Eh how the hell do you use this thing? Is it even possible to interact with this program without a microphone? I tried looking around at its skills repository and there is no sort of advanced AI chatbot available, what a let down.

# 10
>>4074
>what a let down.
It's kind of a botnet if it's relying on a cloud anyway, so yea we'll need to devise our own Anon.

# 11
>>4078
I agree, it seems to be a bit useless at its current stage and the "chatbot" if it can be called as it is even worse than the ParlAI I tested. I tried following the steps that removes this cloud feature and it doesn't seem to be working, welp.

# 12
>>4080
You might have a look at the TacoTron thread Anon. The more current version (not sure if it's linked in that thread yet) seems to be doing a breddy gud job of TTS. I think a simple patch to say TalkToWaifu to turn it's output into speech should be both doable and would be a nice addition to what we currently have going here. Good luck Anon.

# 13
>>4081
>You might have a look at the TacoTron thread Anon. The more current version (not sure if it's linked in that thread yet) seems to be doing a breddy gud job of TTS.
Alright I check that one out soon. 
> I think a simple patch to say TalkToWaifu to turn it's output into speech should be both doable and would be a nice addition to what we currently have going here. Good luck Anon.
That would be definitely great, though I'm myself just a programmer pleb and I am busy doing other project types which is more text game related not (robo-)waifu, so I cannot add those functionalities myself.

# 14
>>4082
>so I cannot add those functionalities myself.
perfectly ok, we're all busy with our own interests here. don't worry about being 'pleb', it's a skill that gets better with practice. just don't quit is how you get better all the time.

