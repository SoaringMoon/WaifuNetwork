# 1
What are the best sounding female robotic voices available? I want something that doesn't kill the boner, I think Siri has an okay voice, but I'm not sure if that would be available for my project

https://www.invidio.us/watch?v=l_4aAbAUoxk

# 2
The single greatest voice actress there is ofc--'''Tara Strong'''.

If she could do the same voice she did when she played the nurse in ''The Animatrix'' or the voice during the tutorial of the minority report video game(i know odd choice) it would be **literal sex** for your ears nonstop.

# 3
>>1239
>Tara Strong
Actually, a Twilicorn robowaifu would be pretty hot in fact of course.

# 4
github.com/alexa/alexa-avs-sample-app/wiki/Raspberry-Pi

idk where to post this but it might help. amazon echo is botnet af but as a software placeholder for someone who doesn't care about freedom, it might be helpful.

# 5
>>156
I imagine you'd probably want to start with a good VA to build up a general vocabulary, and then have software tweak the sounds to change emotional context, etc. I've never really heard a good fully synthesized artificial voice that I know of. Certainly nothing you'd want to hear in the middle of sex w/ your robot wife. Talented VAs like >>1239 are the way to go, at least for now.

# 6
>>156
www.vocalid.co/voicebank

This could be helpful, I'm just now realizing how important a robowaifu voice is, good luck developing!

# 7
>>1242
Vidya voice actors should be a good source of training data, since there's usually a way to export the raw audio for each line out of the game files without any additional noise. Sometimes even with corresponding subtitles.

# 8
>>1244
Yeah, that's an interesting idea anon. Have any specifics for us?

# 9
>>1245
Not really, other than:
>pick your favorite game voice actor
>go to IMDb and grab a list of all the games she ever voiced and install all of them
>export audio files for each line for each game either with corresponding text or listen to each line and write the text manually
>maybe attach emotions to each line, sort of a tag system. "anger", "fear", etc.
>feed that as training data to whatever you're using as the actual voice engine
>???
>profit!

# 10
https://www.invidio.us/watch?v=41U78QP8nBk

# 11
>>1247
Nice historical find Anon.

# 12
github.com/MycroftAI/mimic

I may try to build and play around with this in the next couple of months. If I make progress and can figure out how to make webms, I'll probably post results here.

# 13
Just waiting for 
lyrebird.ai 
to release their API - we could technically copy a person's voice

# 14
>>1250
Very interesting tech, but
>'Ethics' link on front page
>"We are the stewards of you're voice…"
==What could possibly go wrong?==

Sounds like it's going to turn into another libshitshow tbh anon. But still, it might be a good tech to watch for follow-on copycats. Maybe they will release their code, I doubt this bunch will. With copytext like the above they are simply greedy little shits by the sound of it.

# 15
voicebot.ai/

# 16
Does voice control systems belong here or another thread?
jasperproject.github.io/documentation/

Seems kind of like an Alexa afaik but runs on a RPi

>ed. maybe the Mycroft thread would be a better choice

# 17
>>156
pornstar plus babytalk equals hotness.

# 18
>>1243
Vocaloid is a bitch to use for serious Text To Speech. You have to compose every sentence syllable by syllable. The English voices aren't all that great either.

# 19
When I was in Japan I found the bus and train announcements to be incredibly sexy.  It seems that Japanese lends itself to text-to-speech better than English, since it's a very enunciated language (as opposed to lots of slurring in English).

If given a very limited vocabulary, I'm planning to make my robowaifu speak Japanese.  Now I just need to find the same source voices they use in Japan without spending too much on translation or on a popular voice actor.

# 20
>>1256
>Now I just need to find the same source voices they use in Japan without spending too much on translation or on a popular voice actor.
Good luck anon. Please keep us informed ~~if~~when you find good ones!

# 21
Festival vox for GNU+Linux has some decent utterances.

It runs a TCP server you can issue text to speech commands in Lisp syntax:
(SayText "Hello there.")

This system doesn't have inflections, but it's decent text to speech, and you could use the framework to create your own utterances (or pay a voice actor to).

The CMU Arctic pack is more natural than the dry robotic default voices:
festvox.org/cmu_arctic/

However, I find that in each utterance many words can be improved by adding an h or two, spelling phonetically, or inserting a small delay with one to three periods between words. 

I pass sentences through a simple word substitution filter per voice, and update it when I hear a word that sounds a bit odd. 
E.g.:

```cpp
[arctic_slt_female]
good : ghood.
to : to.
obey : obey..
your : your.
owner : ohner```

I rather like the sound of these and kind of don't mind the lack of inflections, but then again I'm right leaning on the /clang/ scale.

# 22
Shodan

# 23
>>1258
Festival sounds worse than a Speak & Spell. All the voices have this ear piercing scratching sound. It does not even sound like a robotic effect, it just sounds like someone speaking through a broken microphone.

# 24
(((Jewgle Jewplex)))
www.tomsguide.com/us/google-duplex-faq,news-27185.html

# 25
Do you want a flange or not?

# 26
>>1850
Can you clarify what you mean Anon?

# 27
>>1851
Well, do you want something that sounds like an ordinary woman, no frills, no bells and whistles?  Or do you want one that sounds like a science fiction robot, with a reverb or "metallic" effect?

# 28
>>156
I mentioned in another thread about voice generation that I'm interested in trying to devise a way to automatically process audio clips and add sound effects like SHODAN. There was also brief discussion of using Terri Brosius' own voice to train a neural network, but it's not clear how practical that is. I don't know what your personal preferences are, but I do know that there are a number of people (including myself) who would love to hear SHODAN say dirty things. I'd like to get started working on this, but unfortunately other obligations are keeping me from investing too much time in it currently (work, school, family, etc.). Hopefully I can do more in-depth research on this idea and potentially have some sort of prototype working in the next few months, but I don't want to promise anything. I'd hate to get someone's hopes up and not deliver anything.

# 29
So 20 years or so ago I got an IMac. Played with it's text to speech and voice control systems that came with it. I figured quick the T2S was not very good. However if the text was misspelled intentionally to emphasize vowels like "mooz end skweer ahl" I could cobble together a bad accent. Then I edited common error code message base to reflect the accent (Airor koad noombar... ect) then it would read the number. Then added a custom alert sound of a Russian lady cursing. So then when the computer had an error it would curse in a foreign language then carefully sound out what the error was in a kind of "ESL".  
This was a shitbox computer and it was frustrating to work with. I realized the voice control was only associating a sound to a command so instead of a voice queue I used the sound of smacking it on the left side (for stress relief). Now an IMac is built like a bongo drum so there are many ways to hit the thing and get different noises. Flicking the front acted like alt tab rotating through windows, gentle pat to the top put it into sleep mode. Right? Then voice commands like "fuck that!" (to close windows), "fuck all this" (close all windows), "more" for full screen, "shut up" for mute and "earmuffs!) to stop voice recognition and a few more. The cache would bog down constantly and have to be purged. I made this a macro tied into the phrase "go clean yourself up!".
Now combine all this together with furious Jolt cola fueled work flow. The look on my roommates face when they watched me smack it upside the head and it curses at me (acknowledgment sound), I flick it a few times cycling through windows, say "fuck that" closing them out. Another smack (more cursing) search "for stuff" (slows to a crawl because of the cache). Get frustrated. Smack it again (more curses) "fuck all this" (all windows close), Smack (more curses) "go clean your self up!" (runs through an auto purge and defrag). Get up and say I'm done for now. night night and pat its head (gentle thumping sound initiating sleep mode).
I basically turned an IMac into an abused angry mail order bride by default of tinkering.

# 30
>>8423
Funny. I can just imagine your flatmate's faces.

# 31
>>8423
Wow, this is a great anecdote. You already took some steps towards having your own robowaifu back then.

# 32
>>1239
>>1240
Not a local, but I'm wondering if a current tool like MycroftAI (the virtual assistant) can currently pipe it's output text through the fifteenAI API to make a character voice.
I haven't used fifteenai or Mycroft yet, but I suspect you could make a half-decent Twilight home assistant now with a RaspPi and a plushie.

# 33
>>9092
>but I suspect you could make a half-decent Twilight home assistant now with a RaspPi and a plushie.
I suspect you can now, yes. And with the further info here on /robowaifu/ she could even move at least a bit. Just search around in the ''Speech Synthesis general'' bread >>199 and you could get some ideas.

# 34
>>1246
BTW Anon, just in case you're ''not'' RobowaifuDev, I wanted to let you know that he actually did it (your idea that is, >>9121). Just in case you missed it.

# 35
I was thinking of using something like FastPitch, but with an added effect to make it sound more robotic to keep it from getting to an uncanny valley sound. Either that or making the voice kinda high pitched and childlike, to make it easier to accept when it says something stupid.

Has anyone here considered hardware-based speech synthesis so it'll actually sync up with mouth movements? Everything professional I've seen just seem like horrid screaming fleshlights that never really try to resemble actual heads.

# 36
>>13164
>Has anyone here considered hardware-based speech synthesis so it'll actually sync up with mouth movements?
Voice modulation, but not complete synthesis. But I don't know how yet. Your picrel is what I knew about, I posted some related video before. However, I was thinking about small internal speakers (mini maze speakers?) but with additional silicone parts that could move and change the voice that way. But nothing specific yet

