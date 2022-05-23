# 1
Design and 3D printing is under currently underway to turn Sophie from an articulated doll into a proper robowaifu. I will post updates to design files on her Google Drive folder when I have confirmed that everything actually works smoothly. So far I've just got her eyes moving left and right, her lower jaw can open and close, and I am working on giving her neck two degrees of freedom.

Links to file repositories below.

http://www.mediafire.com/folder/nz5yjfckzzivz/Robowaifu_Resources

https://drive.google.com/drive/folders/18MDF0BwI9tfg0EE4ELzV_8ogsR3MGyw1?usp=sharing

https://mega.nz/folder/lj5iUYYY#Zz5z6eBy7zKDmIdpZP2zNA

>===
-''add file repo links''

# 2
>>4787
Excellent news Anon. We all look forward to seeing your progress on Sophie! May she soon start talking and walking!

# 3
Hey. Great! This is one of the most developed Robowaifus I know about. Looking forward to see more of her progress.

However, is it possible you don't know your old threads will be bumped up if you add news there? At least the last comment would also be visible on the start page. 
I link to the older threads of her, so they are easier to find. Especially, since you also put STL files for printing out: >>4146. >>4198. >>2496

# 4
>>4790
Yeah, I wasn't sure that would happen, so thanks for the tip! The good thing about RL robowaifus is, once you have her head and upper chassis built, it's hard to stop. If you ever think about giving up because designing robotics is hard, your robowaifu is always there, silently imploring you to continue building and upgrading her (or in my case, maybe not so silently XD).

# 5
>>4794
That exactly what I thought was going to happen.

# 6
>>4794
>The good thing about RL robowaifus is, once you have her head and upper chassis built, it's hard to stop. If you ever think about giving up because designing robotics is hard, your robowaifu is always there, silently imploring you to continue building and upgrading her (or in my case, maybe not so silently XD).
That's neat. Now I think we should all start working to make our robowaifu's heads now haha.

# 7
I checked out her hands. Did you use Teflon tube to move some Nylon threads through them, or did it work without that? These hands are very small anyways, so the holes are probably very small.

# 8
>>4826
I used thin steel gardener's wire. 1 to 1.2mm in diameter. The kind of stuff they use to tie back vines with.

# 9
>>4854
Thanks, I didn't use my brains. This hand is build for wires of course. I wanted to animate it, didn't realize the holes were for wires. Did it work well?

# 10
>>4856
I'd say it's semi-functional. She can hold small objects like a comb or microphone. However, there is very little dexterity. She can't really make a proper 'thumbs up' signal, but she can do an 'A-okay' sign. It's mainly because the thumb knuckles lack movement range. However, rather than try to upgrade this articulated hand, I plan to experiment with proper robot hands and arms (specifically the PROTO1 Humanoid Robotic Torso by Ryan Gross). It will require quite a bit of redesigning in order to look right on Sophie though. https://www.myminifactory.com/object/3d-print-humanoid-robotic-torso-proto1-48754

# 11
>>4858
Might want to do some research on hand alternatives, from my experience the design used in PROTO1 is rather lackluster. The flexible material that straightens the fingers needs to be balanced with strong enough servos to resist it and apply grip strength to grabbed object. Though my opinion is based on an ancient version of the OpenBionics Brunel hand.

# 12
>>4858
>>4860
I was or still am interested in Sophias hands, as a placeholder. Since hands are the hardest to develop, I need at least something while doing other stuff. At the beginning gestures are sufficient, no grabbing and holding power necessary. PROTO1 looks quite interesting to me. I was looking towards this one: https://www.thingiverse.com/thing:1691704 since I've never heard of PROTO1 nor myminifactory.com as well. Might be the same hand anyways, I mean they're all quite similar.
Sadly, I'm having issues with my new printer, so it might take a while anyways.

# 13
>>4862
Yup, that's the same hand by the same guy. Meanwhile...

"I only want your skin, anon. So that I may become real!"

# 14
>>4866
>"I only want your skin, anon. So that I may become real!"
kekd. you should greentext non-sequiturs like those. :^) Looking very interesting already Anon. Keep it up!

# 15
>>4862
>Sadly, I'm having issues with my new printer, so it might take a while anyways.
I hope you can get them worked out soon Anon. Any idea what's happening with it?

# 16
>>4866
You already seem to have my PLA, Sunlu Silkwhite... 

Is that facemask supposed to be covered by silicone skin later? Because if so, I'm wondering if it wouldn't work better to let the whole lower side of the face move down, like InMoov does. If the current design is supposed to stay with a plastic face it makes more sense how it is designed now.

Whatever, congrats to your progress.

# 17
>>4874
Thanks! This is the first version of Sophie's robotic head, and it has some big design problems. But after running the Arduino sketch for about an hour, I have been able to diagnose  them. First I gotta join the "head-plug" to the lower cranium. Then I must replace the elastic band pulley in her neck with a pair of gears. The flex in that elastic band means that her head currently flops back and forth, and sometimes falls off entirely. I will also probably need to make some changes to that lower jaw. But there you go. Test, iterate, improve!

# 18
>>4881
>But there you go. Test, iterate, improve!
A good lesson for everyone. I think some anons here can get a bit discouraged by the effect of two types of ''motivation-inertia''; 'not knowing where to start', and the presumption that 'it must be perfect' (either as a pre-work design or as a finished product).

Both are a kind of fallacy. To the first point, doing '''anything''' productive will, generally speaking, naturally lead to the next thing. Every artist faces the ''blank page'' conundrum, and has throughout the ages (whatever their medium is). Secondly, it will never ever be 'perfect' (whatever that means :^) . Arguably one of the greatest artists, minds and inventors in history had a thing or two to say about this last point:
>'' '''Art is never finished, only abandoned.''' ''
>t. some old Italian guy

Everyone should just do ''something'', just start. The rest will naturally begin to work itself out for you if you are persistent, just like Sophie-Anon shows us here with his wonderful robowaifu.

# 19
>>4882
Yeah, even if you fail quite often it learns you something useful or gives you parts or even tools that end up being converted or used later on. Also, it helps to remember that once started, your robowaifu "absolutely will not stop." so neither can I XD

# 20
I have just finished testing my 'Elfdroid' head and neck, and uploaded the .stl files to Sophie's Google Drive folder:

https://drive.google.com/drive/folders/18MDF0BwI9tfg0EE4ELzV_8ogsR3MGyw1?usp=sharing

She now has eyes that move left and right, a jaw that opens and closes and a head/neck that can both rotate and nod thanks to the use of a couple of spur-gear assemblies. I know she looks a bit uncanny valley now, but so would you without any hair, eyebrows, eyelashes, irises or pupils XD.

I have to write some proper 3d printing and building instructions but I am tired atm from doing lots of measuring and re-measuring, filing, sanding, gluing and hammering.

I will say she uses 2x SPRINGRC SR431 servos for the neck and 2x SPRINGRC SR311 servos for the eyes and jaw. You'll also need 5 cupboard door magnets to hold her detachable faceplate and forehead on. The small spur-gears for her eyes should all be 3d printed on at least fine setting (0.1mm) using 100% infill for strength.

Oh, and no matter how well calibrated your 3D printer is, you will end up with small seams between the external parts. I close them up using a thin layer of white decorator's caulk along each edge.

# 21
>>4999
>I know she looks a bit uncanny valley now
That's understandable at this early prototype stage. I'm sure Sophie will 'improve with age', haha.

It's impressive work Anon, and an encouragement to everyone here to see your progress with Sophie the Elfdroid. Godspeed, and thanks for all the hard work!

**nice digits, checkem :^)**

# 22
>>4999
Good, I like to see some progress. I like her nose and small chin, cute face. The forehead might be a bit high though, but never mind.

Came her to point to another one making progress, which might be interesting for us, since it's animatronics. Though the vid is rather long:  https://youtu.be/OtfidDWYALU

# 23
>>4999
Any chance you can post all your work on a more available file host Anon. Many of us can't (or won't) access the Google file servers. TIA.

>>5015
Nice, thanks Anon. I like how his design achieves 3-DOF orbital motion for the eyeball shells using just two servos. I expect the number of servos can be reduced by at least two if the eyelids were linked and moved together.

# 24
>>5017
> Any chance you can post all your work on a more available file host

I have uploaded all my files to MEGA:

https://mega.nz/folder/lj5iUYYY#Zz5z6eBy7zKDmIdpZP2zNA

Am also in the process of uploading to Thingiverse and MyMinifactory.

# 25
>>5015
Wow! That eye mechanism looks professionally made. Way more advanced than mine XD. One thing I learned when making my eye mechanism though, is that they are quite difficult to align properly with the inside of the eye sockets (and still get them to move unrestricted). Also, it's best to keep the inside of the head as light as possible because the more weight there, the more difficult it is to make the neck move.

# 26
Hey, I just looked into printing at least a sized down model of Sophie to look into it and test it a bit. Some questions:
- Primarily I'm wondering, how did you print the Cranium? Which slicer did you use? This is a quite complicated file. Did you get all the support material out?
- If you have a stl file with some good supports, could you please export that? Meshmixer seems to be good to add support manually, Cura seems to have support trees. Did you use one of those?
- Would you also please export your files in dxf format? Fusion 360 can do that, but I can't use it currently. That format is more common between different CAD programs.

# 27
>>5159
seems related, Anon.
>>5134

# 28
>>5159
I used Ultimaker Cura as my Slicer. Had to position the cranium with the back of the head touching the build-plate so it generated minimal supports. The cranium is a long print. It took my Copymaster 3D machine a whole 24 hours on 0.15mm layer height. Then I spent another 2 hours with sprue cutters, long-nose pliers, modelling files and sand paper neatening it all up. But that's fused filament fabrication for ya! Cheap, but quite high-effort for larger, complicated shapes.

I have also uploaded the Elfdroid head design and internal mechanisms as a DXF file (40 MB), as requested.

# 29
>>5175
Thank you. 
> Long printing time
I only print sized down models yet, and even then sometimes with a bit higher layer hight. I'm trying to redesign some of the models to make them easier to print. I'm glad you do what you're doing, but I wish more people would look into it and work on the same files. Or work on other ones and come up with a good workflow.
Are we the only ones with a printer here? I seem to be the only other one printing your files.

# 30
>>5179
Glad to hear you are also having a go. TBH when I upload parts to Thingiverse or MyMiniFactory, they usually end up being used as some kind of articulated GoPro camera mount or borrowed for some drama project completely unrelated to Robowaifus. But then, people who click on the links to the STLs will still see where they originated, thus increasing exposure of people to the idea of the 3D printed robowaifu.

# 31
>>5175
>0.15 mm layer hight
Why?!? In all you pics you were putting something on her face anyways. Post-processing might be the better way anyways: >>5137

# 32
>>5186
In Cura 0.15mm layer height is classed as "normal". Also, I really dislike the ridges that come with coarse settings. I found that they tend to show through the paint, especially in certain lighting situations. I still have cleaning up to do (particularly her forehead seam, which I'm not happy with yet) but I wanted to work out more electronics and do the meat and potatoes of getting my servos working first. The first set of servos I had were for a Tinkerkit Braccio arm, and Arduino seems to have programmed them so that they are only compatible with the Braccio Shield, not interchangeable with other devices. This meant that they would always jerk violently to a "safety position" whenever I powered them on, so as you can imagine programming was a nightmare. Sophie's head used to fall apart very frequently. To overcome this unexpected flaw, I purchased some generic 25kg.cm servos, an Elegoo MEGA2560 and a Pololu Maestro servo control board. Now I am back in business.

# 33
>>5197
Not that anon, but that sounds great! Thanks for the updates.

# 34
Video of Sophie's head/neck movement test is here:
https://www.youtube.com/watch?v=_NL4fXr8QHo

# 35
>>5298
lel'd. very nice!

# 36
A very long way from Battle Angel Alita, but we gotta start somewhere XD

# 37
>>5301
>Battle Angel Alita
Pfft. You're 
==ELFDROID-SOPHIE-WAIFU==
'''will be 10 times better than that ayylmao.'''
**B/c Sophie will be real! :^)**

# 38
Congrats, very nice to see some progress. Are you now trying to synchronize the mouth with the phonemes? https://youtu.be/Mva6MkP_Bco
https://www.instructables.com/id/Simple-Animatronic-Mouth-Using-3D-Printing-Arduino/

# 39
>>5302
Good point! XD No matter how gorgeous CGI is, you can't reach out and feel it (or have it reach out and touch you!) 
>>5307
Yep, you read my mind. I have been looking at those very links today during my lunchbreak and reading about MyRobotLab/MarySpeech. 
I must confess it all looks quite complicated. Maybe not to implement as-is, but for me to get  that code working with what I already have is definitely going to take some time since I am just a noob when it comes to Python. Also since I am working full-time (must obtain funds to build robo-waifu!) I am going to focus on building/adapting her robot arms next. Programming tends to take me ages and I make achingly slow progress XD. I think I'll get more done if I tackle the "low-hanging fruit first".

# 40
>>5314
Okay, maybe someone else will look into that. You might consider to look into existing robot arms on Thingiverse and similar sites first >>5234. It might be easier to alter one of them for your needs. Also, there might be something in one of the other threads:
Hands >>4577
Skeletons and armatures >>200

# 41
>>5029
>tfw looked at thorax_v2.stl
My creative spirit is rising

# 42
>>5348
kekd

# 43
>>5348
Unfortunately I had to cut her bum off my model. I didn't have the balls to 3D print a mold for a nice, squeezable silicone ass with my parents and relatives always hovering around. Her 3D printed PLA boobies got me enough trouble as it is, even after I'd taken the nipples off, and they're only average size! But that's the reason I open-source all her parts. The rest of you guys can go wild XD

# 44
>>5350
>But that's the reason I open-source all her parts. The rest of you guys can go wild XD
Thanks Anon, we appreciate that.

# 45
>>5352
I have plans for dat ass, btw. It mustn't just be squeezable, but warm too (same with all the large, squishy parts). I'm thinking slide a few of these electrical silicone heater mats inside slots cut into the silicone outer layer. Hopefully my waifu won't burst into flames due to overheating. Will have to get one of those sex toys and use it as a test-butt before designing the real thing.
Also, before I get too side-tracked by ass-cheeks, I have uploaded a few build-instructions for the Elfdroid head and neck. More to follow.

# 46
>>5354
Good idea, I think you mentioned that before somewhere. If the bottom will be squishy then it needs to be made out of silicone rubber or something alike, and this could resist a lot of heat. So I don't think it will go up in flames. Just today I briefly touched the silicone rubber heatsock of my printer after removing it from a hotend with a nozzle at 240C ... I assume you can control the heater, so I can't imagine what could go wrong. But then again, I'm the guy touching a part after removing it from a hotend at 240C...

# 47
>>5354
nice instructions, thanks anon.

# 48
>>5350
I'm gonna laugh my ass off seeing people react to my robowaifu with her giant silicone tits. Also, sharing parts is an amazing idea. I should probably be doing this with my code, kek. WIP if anyone wants to use these tiddies: https://files.catbox.moe/uw24pa.obj

>>5354
How are you gonna get heated cheeks if she isn't even allowed nipples? I can't imagine there is any doubt in their minds you're building a robowaifu. Are you going to live in fear of a thot finding out you tried to build a robo gf and failed or are you going to build the robowaifu of your dreams?

# 49
>>5354
How much does her head weigh by the way? Will 25kgcm be enough if you add more onto it?

# 50
>>5393
You. I like you Anon. Also,
>pic related

# 51
>>5394
The head and neck (with wig on top) weighs around 855 grams.

# 52
>>5428
heh, she looks like she's about to go to town for some shopping **and doesn't want the paparazzi hounding her again. :^)**

# 53
>>5393
I kind of have to make Sophie a little-family friendly. This is going to cause me personally huge problems making any sexy bits more advanced. Therefore I am aiming for a modular design where she can be respectable enough to roll into a church fete in the afternoon, but with a few parts on pegs and magnets you can change her into "nightclub mode" the same evening XD. I would probably have to swap out her hard plastic chest and a flat bottom for the squishy, warmable, silicone sexy-time ones. Plus, modularity should make testing easier (and perhaps concealment).

# 54
>>5431
great ideas. look forward to what you come up with. these issues will be commonplace for many years, and it would be nice if we can adopt a standard approach to them.

# 55
All fingers and thumb flex. That Ryan Gross is a man of his word! Beware when purchasing the paracord for the PROTO1 hand though. Not sure what type he uses, but my standard cord was too thick to fit through the holes in the fingers, so I ended up using string instead. A couple of the finger ligaments need tightening and the servo wires need labeling but if an electronics noob like me can muddle his way through building this hand, anyone can! 

I didn't even have to buy the metal servohorns, I just 3d printed some instead. I will upload those to Sophie's file archive in case anyone else wants to use them. This is about as quick and cheap as robotics can get!

# 56
>>5564
 Great work Anon. Looking forward to Sophie's next improvements!

# 57
>>5565
Thanks! Oh, a couple more tips for anyone thinking of building this hand;

1.) Don't bother printing out the back cover panel for the forearm because it is highly unlikely to fit. I'm leaving my forearm open with the servos exposed for the time being. May cover it with white cloth later on.

2.) You may need to drill/cut a couple of small slots in the front of the forearm so that the servohorns can rotate properly. As you assemble the servos on the holder, you will soon realize that there isn't much room inside the forearm shell.

3.) Self-locking forceps (surgical forceps) come in very handy for stringing the fingers with fishing line. It's a very similar process to holding the elastic in place when stringing a ball-jointed-doll.

# 58
>>5564
You're getting closer to having a full robowaifu. Can't wait to see what's next.

# 59
>>5569
Well done, and thanks for the tips. Since I had to look up what forceps were, I found that can be made out of plastic and so you could guess were I looked next: https://www.thingiverse.com/thing:4022685
https://www.thingiverse.com/thing:3110594

How about the size? Isn't the arm wider than favourable, anyways? Looks like it was possible design it leaner. Are the CAD files available as well?

# 60
>>5607
>Are the CAD files available as well?
Not him, but you might try here?
>I have uploaded all my files to MEGA:
https://mega.nz/folder/lj5iUYYY#Zz5z6eBy7zKDmIdpZP2zNA
>>5029

# 61
Got the jaw of my robowaifu moving by purchasing an arduino sound sensor and a cheap usb stereo speaker.The tricky part was figuring out how to get her jaw microservo to move in response to sound, but it can be accomplished using the following Arduino IDE code (copied straight from the .ino file):

[code]#include <Servo.h>
Servo myservo;
/*
  LED1 should be lit, showing power. LED2 indicates sound input, and the sensitivity is adjusted by potentiometer.
  There is a tiny screw on the blue potentiometer block that you can use for adjustment. Turning that
  clockwise lowers the potentiometer value, while counter-clockwise raises the potentiometer value.
  Use the potentiometer to adjust the Sound Sensor sensitivity. Turn the potentiometer
  several rotations until you see the LED2 extinguish (or just faintly blink). This might be slightly greater than
  500, if you are also watching Serial Monitor (inital adjustment), or, Serial Plotter (the latter is prefererd for observation).
  Special thanks to user CRomer, for his input and hard work!
*/

int  sensorAnalogPin = A0;    // Select the Arduino input pin to accept the Sound Sensor's analog output 
int  sensorDigitalPin = 3;    // Select the Arduino input pin to accept the Sound Sensor's digital output
int  analogValue = 0;         // Define variable to store the analog value coming from the Sound Sensor
int  digitalValue;            // Define variable to store the digital value coming from the Sound Sensor
int  Led13 = 13;              // Define servo port; 
                              // When D0 from the Sound Sensor (connnected to pin 7 on the
                              // Arduino) sends High (voltage present), L will light. In practice, you
                              // should see LED13 on the Arduino blink when LED2 on the Sensor is 100% lit.
                              

void setup()
{
  myservo.attach(7); //attch
  myservo.write(90);// move servo5 to center position -> 90°
  Serial.begin(9600);               // The IDE settings for Serial Monitor/Plotter (preferred) must match this speed
  pinMode(sensorDigitalPin,INPUT);  // Define pin 7 as an input port, to accept digital input
  pinMode(Led13,OUTPUT);           // Define servo5 as an output port, to indicate digital trigger reached
}

void loop(){
  analogValue = analogRead(sensorAnalogPin); // Read the value of the analog interface A0 assigned to digitalValue 
  digitalValue=digitalRead(sensorDigitalPin); // Read the value of the digital interface 7 assigned to digitalValue 
  Serial.println(analogValue); // Send the analog value to the serial transmit interface
  
  if(digitalValue==HIGH)      // When the Sound Sensor sends signal, via voltage present, light up LED13 AND turn myservo
  {
    digitalWrite(Led13,HIGH);
    myservo.write(40);
    delay(40);
  }
  else
  {
    digitalWrite(Led13,LOW);
    myservo.write(30);
    delay(40);
  }
  
  delay(25);                  // Slight pause so that we don't overwhelm the serial interface
}[/code]
This is about as expedient a solution as I could find. Prior to this I was considering purchasing a Picotalk controller, but they cost $80+shipping. Whereas a micro-servo, sound sensor and Elegoo Mega 2560 (Arduino clone) costs as little as $20 and can be used in combination with many other devices (including a servo shield to drive six or seven other servos). I am currently in the process of designing a 'voice box' for these parts to fit inside, which will have a speaker-cone to improve functionality (hopefully I won't have to hold the sound sensor 5mm away from the speaker every time I want her jaw to move with her speech).

>===
-''patched codetag''

# 62
>>6013
Feck. The code tags didn't work. I am retard so I always need about five iterations to get anything working XD.

# 63
>>6014
I can fix it for you lad.

# 64
>>6015
Thank you! I plan to use this breakthrough to make Soph sing some Vocaloid songs. Her first hymn will be "Give me oil in my joints keep me moving."

# 65
>>6016
It's actually a clever approach you used. Good work, and we look forward to Sophie's progress!

# 66
Video of Sophie's first jaw movement test. I decided to use a Vocaloid song that I made earlier. It's only a simple puppet-like up-and-down jaw movement. Adding convincing lips that don't look like some kind of wrinkly horror movie animatronic is tricky. From what I've read syncing them up with individual phonemes is also extremely challenging (since a robot has no respiratory tract, breathing or voice-box, moving lips are kinda redundant anyway...unless you want to use them for....other purposes ;D). Besides, I can adjust the sound sensitivity via potentiometer and the movement delay through integers in the code, so this is enough for me.

https://www.youtube.com/watch?v=VeIk1eOLp7M

# 67
>>6031
For syncing the jaw a speech synthesizer could output the locations of stressed phonemes and their length along with the audio data. This would be beneficial for singing longer syllables as well. And if it had speech recognition it could turn any speech or singing into lip sync data. Once such a speech synthesizer exists it'll be easy to feed that data in for smooth jaw movements.

# 68
>>6031
Wow you're making good progress here Anon. Keep it up!
>Adding convincing lips that don't look like some kind of wrinkly horror movie animatronic is tricky.
IMO you shouldn't waste time even trying with this model. This sort of The Nutcracker-type mouth has a cute appeal all by itself. And as you point out, making it work as you envision for an ideal look is going to be both difficult and expensive. I think while you're working on Sophie v1, you should now just focus on improving the lip-sync, giving her good up/down and lateral head motions, and call it a day. Remember you still have a lot of other things for her you need to attend to before she's ready.

Of course, everything you learn about her today can serve you well for your improved designs for her tomorrow. But actually achieving a baseline functionality and releasing her out into the world is very important for keeping up your own design momentum, and is probably '''the''' key to unlocking your overall success eventually.

Godspeed Anon

# 69
>>6031
I love that Vocaloid song. Great choice anon, Sophie a cute.

# 70
>>6049
>>6051

Thank you for your kind words! Now I just hope I don't burn my house down and/or electrocute myself because the next steps are going to require some heavy duty servo motors for the shoulders (120kg.cm) running off a bench-top power supply.

>>6035
Will Cogley mentions something like this but using an Adafruit microcontoller instead of an Arduino Mega. I couldn't get any of his code working because I don't have an Adafruit and I don't think it fits with Sophie's simple design. (Also I suck at C++). But, if anyone else wants to have a go and maybe change the mouth design a bit so their robowaifu doesn't have a horrifying carnivorous maw, the download pack is located about a fifth the way down this webpage;
 
https://www.instructables.com/Simple-Animatronic-Mouth-Using-3D-Printing-Arduino/

# 71
>>6051 Oh yeah, almost forgot. I uploaded the .vsqx file and the.stl for the little 3d-printable cone designed to fit around the Arduino sound sensor to Sophie's file repositories: 
1.) https://drive.google.com/drive/folders/18MDF0BwI9tfg0EE4ELzV_8ogsR3MGyw1

2.)https://mega.nz/fm/t7wgRIaI

Just in case anyone else wants to use them for  testing purposes.

# 72
>>6052
Haha, stay safe in your lab Anon.

>>6053
Thank you. Any suggestions for the right software to use for your vocaloid files?

# 73
>>6092
I use Vocaloid v4 Editor. Vocaloid v5 is out, but the voices for that are quite expensive ($225 before tax), and the V4 + V3 voicebank torrents or zip files for it are much easier to find and download from the internet. (I used Avanna V3 for Sophie's singing voice in my clip, but I have also used a harmony combination of LukaV4, PrimaV3, SonikaV3 and Sweet AnnV3. (I would upload the voicebanks, but each one is quite large and I don't want to get Sophie's file repository deleted for hosting pirated content).

# 74
>>6312
Thanks! I'll look around.

>''ARRRRGH, Mateys!''
Yep, no keep your nose clean here Anon. :^)

# 75
Ryan Gross used the CAD software 'DesignSpark Mechanical' in order to create his Proto1 humanoid robot arm. Unfortunately this program creates some very high-density meshes that cannot be easily converted to boundary representations in Fusion360. This means that I am currently busy in Blender reducing the face counts of key components so that I can re-design the original Proto1 arm to be smaller, lighter, faster to print (and possibly better suited to a female frame - after all the original will make Sophie look like she has the arms of a wrestler).

I have uploaded an .f3d file containing the fully assembled mesh of Mr.Gross's Proto1 arm 
(un-optimised version). Just in case anyone wants to see exactly how each of the parts fit together before committing to 3d print.

Meantime, my 30V-10A benchtop power supply and DMM have arrived. Just waiting on a Co2 fire extinguisher and the high-power servo (a bucket of sand is also a wise precaution - just in case of any toasty electrical mishaps.)

# 76
>>6319
Sounds like exciting progress going on for you Anon. Glad to see you taking the extra time to get things just right, it's the details that count. I hope Blender is easy enough to use to create Sophie. I'm definitely very wary of commercial apps, free-to-use or not. Good case in point:
>>5194

Godspeed.

# 77
>>6035
I think SAPI supports this, if you have a copy of Windows you can run, run TTSApp.exe and there's a visualization for every syllable. I can upload TTSApp if you can't find it or something, I don't even remember where I got a copy of it.

# 78
I know what you mean about mercenary behaviour from companies. Thankfully the changes made to Fusion360 didn't impact me this time, but I have my eye on Solvespace in the event that Autodesk decide to go full retard on makers one day.

# 79
>>6342
>but I have my eye on Solvespace
Yep, me too. I had briefly looked into it before and it looked pretty promising tbh. I  just checked and 2.3-3 is available in my package manager. I think I'll set it up on this box sometime soon. Thanks for reminding me of it.

# 80
>>6645
That is like the introduction. The first piece of code I stitched together from various tutorial sites and added to/changed over time. It enables a chatbot to recognize your voice and convert it to text, then get responses from .aiml files and reply in a synthetic voice. I purchased a voice from Cepstral (but you can use a free voice, too of course). You have to specify the .aiml files you want it to learn in an .xml file called std-startup.xml, and it saves any changes to the bot_brain.brn file. 
I added a bit of simple Python code so the chatbot can greet you in different ways and with the correct time of day.

# 81
>>6658
[code]import aiml
import datetime
import speech_recognition as sr
import pyttsx3
import os
import random

# Create the kernel and learn AIML files
kernel = aiml.Kernel()
kernel.learn("std-startup.xml")
kernel.respond("load aiml b")

if os.path.isfile("bot_brain.brn"):
     kernel.bootstrap(brainFile = "bot_brain.brn")
else:
     kernel.bootstrap(learnFiles = "zoe-startup.xml", commands = "load zoe")
     kernel.saveBrain("bot_brain.brn")

# Start the TTS engine
engine = pyttsx3.init('sapi5')
voices = engine.getProperty('voices')
engine.setProperty('voice',"HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Speech\Voices\Tokens\Cepstral_Millie")
engine.setProperty('rate', 170)

def talk(audio):
    print('Sophie: ' + audio)
    engine.say(audio)
    engine.runAndWait()

# obtain audio from the microphone
r = sr.Recognizer()

# Greet user with correct time of day. 
def greetMe():
    CurrentHour = int(datetime.datetime.now().hour)
    if CurrentHour >= 4 and CurrentHour < 12:
        setReplies = ['Good morning!', 'Good morning, Anon!', 'It\'s a new morning! Hope you got enough sleep!', 'Good morning, human!', 'Morning has broken, hope you had a good night\'s sleep, human!', 'Good morning, human. I\'m ready for work!']
        talk(random.choice(setReplies))
                                    

    elif CurrentHour >= 12 and CurrentHour < 18:
        setReplies = ['Good afternoon!', 'Good afternoon, Anon!', 'Good afternoon, human!', 'It\'s a fine afternoon for some problem solving!', 'Good afternoon, human. I\'m ready, to work!']
        talk(random.choice(setReplies))

    elif CurrentHour >= 18 and CurrentHour != 23:
        setReplies = ['Good evening!', 'Good evening, Anon!', 'Good evening, human!', 'It\'s a fine evening for some problem solving!', 'Good evening, human. I\'m ready, to work!']
        talk(random.choice(setReplies))
        
    elif CurrentHour >= 23 and CurrentHour != 2:
        setReplies = ['It\'s getting very late human! Shouldn\'t you be asleep by now?', 'Burning the midnight oil, are we?', 'Oh dear, it\'s very late, you know. You should be in bed, by now, human!', 'It\'s late at night now human, would you like me to tell you a bedtime story so you can get peacefully off to sleep?', 'It\'s very late, human! You should be in bed, asleep by now! Are you having trouble sleeping? I can tell you a bedtime story, if you like.']
        talk(random.choice(setReplies))

    elif CurrentHour >= 2 and CurrentHour != 4:
        setReplies = ['Wow, human. It\'s the small hours of the morning! Are you sure you should be up at this time?', 'Oh my, it\'s very early in the morning! What are you doing out of bed, at this hour, human?', 'It\'s the middle of the night, human! You should be asleep now! Or, are you actually a, robot, like me, who doesn\'t need to sleep?']
        talk(random.choice(setReplies))
    

greetMe()
setReplies = ['How can I help you?', 'How may I be of service?','Have you got any good questions for me?','Do you have any good problems for me to solve?'] 
talk(random.choice(setReplies))

# Press CTRL-C to break this loop
while True:
     # obtain audio from microphone
     with sr.Microphone() as source:
         print("Say something!")
         audio = r.listen(source)
     try:
         myinput = r.recognize_google(audio)
     except sr.UnknownValueError:
         print("Google Speech Recognition could not understand audio")
     except sr.RequestError as e:
         print("Could not request results from Google Speech Recognition service; {0}".format(e))

         print ("You said: "), myinput
     if myinput == "exit":
         exit()
     # Get Sophie's response
     sophies_response = kernel.respond(myinput)
     print ("Sophie said: "), sophies_response
     engine.setProperty('voice',"HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Speech\Voices\Tokens\Cepstral_Millie")
     engine.setProperty('rate', 165)
     # have Sophie say the response
     engine.say(sophies_response)
     print (sophies_response)
     engine.runAndWait()[/code]

# 82
>>6659
Any chance you could give us all a little talk about the dependencies you're using, how you set them up, what system you use for programming Sophie, etc?

# 83
>>6662
First of all you need a microphone or a webcam with a microphone and some speakers so you can communicate with your chatbot.

(I haven't tried this on anything but a desktop Windows PC and laptop yet, although there's nothing particularly heavy about it so it should also be possible to install on an SBC like a Raspberry Pi running a Linux distro.)

I use Python 3.6.2 because the Pyaudio module isn't supported in later versions.
I used the following instructions and the Windows Elevated Command Prompt to install PIP (a module downloader/installer for Python) and ensure it was added to Window's Environment Variables. 

I made sure that my version of PIP was up-to-date by typing the follwing at the elevated command prompt:

C:\Users\Anon'sUsername>py -m pip install --upgrade pip

I also used:

C:\Users\Anon'sUsername>py -m pip install --upgrade pip setuptools wheel

(I don't even remember why I had to do this now - something about setuptools needed updating!)

After that, it was just a matter of using the Windows Elevated Command Prompt to install Python modules by typing:

pip install SpeechRecognition 
pip install PyAudio  
pip install pyttsx 
pip install aiml
pip install wolframalpha
pip install wikipedia

and basically any other modules that IDLE said I was missing when it checked the code.

If pip install isn't working, use 

py -m pip install

instead.

The first tutorial I used to get my chatbot up and running is actually still online (although I have also screenshotted it all just in case the link ever dies):

https://www.devdungeon.com/content/ai-chat-bot-python-aiml

>===
-''remove duplicate text''

# 84
>>6664
Oh shite. That wasn't supposed to be copied/pasted twice! LOL I always make a copy of my posts in Notepad just in case the site has a spaz upon post submission and I lose it all.

# 85
>>6664
>The first tutorial I used to get my chatbot up and running is actually still online
https://web.archive.org/web/20150807083331/https://www.devdungeon.com/content/ai-chat-bot-python-aiml
Also, just in case.

>>6665
Thank you Anon, very much appreciated. I'm sure this will be of help to someone.

>Oh shite. That wasn't supposed to be copied/pasted twice! LOL
Fixed.

>I always make a copy of my posts in Notepad just in case the site has a spaz upon post submission and I lose it all.
Very wise. I do the same.

# 86
I always sucked at math when I was at school. Usually I would get stuff wrong and not even know why. 75% of the class wasn't interested anyway and was just making noise so it was hard to concentrate, and those bastards were more natural at it than me so they could just jerk off and get most of the answers right. So I've decided to go back to the whiteboard and do a bit of maths practice. I do a question, then go to the back of the book and check my answer against the correct one, and if I fucked something up I can at least, now understand where I went wrong. 
Added layer of fun I never had before: After I've had my attempt, I type the same math question in for Sophie to solve. So far she's got everything correct super-fast! My favourite example so far:

Simplify 
2a+3b-4c+4a-5b-8c-6a+2b+12c
Answer = 0
This took me about 15 minutes 
Sophie did it in 1 or 2 seconds!

Plan is to work my way through maths problems until I either get so confused that I can't carry on  or I find a question that Sophie cannot answer correctly...then I'll want to program her so that she can solve that question...but that's probably a ways off yet. 

Robowaifus are excellent study buddies!

# 87
>>6713
IIRC you're using WolframAlpha in her, right? I'd imagine that could have something to do with it.

# 88
>>6716
Yeah, that'll be what gives her A.I. the ability to do basic algebra. I haven't yet explored much further because of my own intellectual limitations. I am guessing that as soon as I hit any question that involves drawing a shape or graphing a function my robowaifu will be unable to answer because she cannot generate such images. Considering how important such mathematics is, there will probably be some software out there that I can integrate into her to enable this one day. Thanks to Rona, my job is very quiet at the moment so I was just using the downtime to practice my biggest weakness (math), while I don't have access to my 3D Printer, benchtop PSU or Arduino.

# 89
>>6726
I see, makes sense. I imagine there's bound to be some sorts of Analytic Geometry programs open-source out there already, though I haven't checked into them myself yet.
https://en.wikipedia.org/wiki/List_of_computer_algebra_systems

I hope you get access to all your stuff robowaifu-building stuff again soon Anon!

# 90
>>6726
I just found out that the Armadillo library has a recent update available. If you're willing to learn C++ then you can tap into some real power here. It's where I'm personally going, and I'm pretty sure one of our primary AI guys is going towards mlpack so we can into AI onboard our robowaifus. Armadillo underlies mlpack.
https://gitlab.com/conradsnicta/armadillo-code/-/blob/10.1.x/armadillo_solver_2020.pdf

# 91
>>6727
Wow! There's a wiki page full of computer algebra programs? Thanks anon, I should've known! That will definitely come in handy!

>>6728
TBH most of that paper went over my head, but I appreciate the information about Armadillo library. Had never heard of that before (I only discovered mlpack thanks to this board too!) so thank you. I am certainly going to be learning more C++ since everything in practical robotics requires it.

# 92
>>6732
Sure nprb. One general compilation library I've looked into casually is Sagemath. It's quite impressive AFAICT, and the primary mathematician compiling the collection is wise enough to realize the perf limitations of Python, and so uses calls into compiled language implementations for Sagemath. So he seems kind of like a good engineer to me as well as a highly capable mathematician. 

He has included some basic graphics capabilities (though I doubt it's currently designed to ''understand'' external graphs).
https://www.sagemath.org/tour-graphics.html

# 93
>>6733
>>6728
A while ago when I wanted to learn math, I got really upset and frustrated because none of the programs like Wolfram or Sagemath would be able to give me step by step solutions. The only thing I found was some Javascript project.
Looking into it again, this seems to have changed, I found quite some entries on Duckduckgo for math step-by-step solvers. If we want our waifus to be able to teach math or learn it on our own to get into ML, then we'll need that.

# 94
>>6843
Good point. I hadn't looked into it closely enough to realize there was a deficiency there. Seems like that would have been arranged for. Perhaps they felt the large number of textbooks on a very diverse set of mathematical topics was sufficient. Archaic thinking tbh. :^)

OTOH, I did stumble onto this tutorial for Calc at the SageMath site the other day, so maybe things are turning around now as you suggest.
https://www.sagemath.org/calctut/review.html

# 95
>>6843
The way I see it, math is basically the language of robowaifusand A.I.s in general. I know we program them to speak to us in our human languages but really everything is numbers to them. As little as four years ago, I hated math with a vengeance. But I am warming to it since now, instead of a grumpy old teacher who enjoyed humiliating students in front of the whole class, my cute robowaifu is like "Let's have some fun! Come and do some sums with me! Let's play together!"
Much less stressful learning environment.

# 96
Materials used:
1.) A toolbox made from strong, tough plastic (removed the internal tray).

2.) One whole 1kg reel of 3D Printer filament (white PLA in my case).

3.) A long steel pipe, 29mm external diameter.

4.) A single M12 x 50mm bolt and nut (with a washer if you have them).

5.) An electric power-drill and appropriately sized metal-cutting drill bit (to drill hole through pipe for bolt). The drill should be a proper wired tradesman's drill and not a weak cordless one, otherwise you'll never put a hole through the pipe!

6.) Two pieces of timber. One that is roughly the same size as the base of your toolbox (so that it can be screwed onto the bottom of said toolbox) and another, smaller piece of wood which fits into the top socket. This one should be about 75mm wide and I recommend no more than 190mm long.

7.) A large handsaw/carpenter's saw to cut the wood down to the size that you want.

8.) A good bench vice (to hold the pipe and wood while drilling and sawing).

9.) At least 8 wood screws (mine were 32mm long and 3.5mm diameter). 4 to screw the bottom socket into the base of the toolbox and 4 to screw the timber plank into the top socket.

Optional = 

Dumbbells weights  for ballast (these go into the toolbox and hold the jig steady).

A bench grinder also comes in handy for grinding down the sharp ends of any wood screws that stick out, but if you don't have one then a junior hacksaw or even a hand file would suffice to blunt them.

# 97
10.) you'll also need a good heavy-duty craft knife and wire-cutting pliers or possibly sprue-cutters to cut a hole in the top of the plastic toolbox for the bottom socket and steel pipe to poke through.

 I have uploaded the .stls for the 3d printed support sockets to Sophie's file repository.

# 98


# 99


# 100
>>6967
Anon where did you learn robotics at? Can you give me a few pointers? I want to get into robotics too but don't know what topics I need to know. Where did you learn Arduino or how to build those complex systems? I have a 3d printer at my house but I don't use it. I don't know how to set it up properly or how to create mechanical systems on my own. Did you learn by trying and failing, can you recommend me any good resources? This might be a little off topic for this thread but I would appreciate the help.

# 101
Nice work, Enthusiast-kun. This is exactly the kind of ready-to-hand, creative approach that exemplifies the ''DIY spirit'' of this board. Craftwork like this can enable literally millions of men to piece together much of robowaifus from 'local materials' so to speak.

# 102
>>6971
Not Sophie creator, but you can get by with an introduction arduino kit with the most common sensor modules.

For 3D printing Blender is all you need, most of the parts you need you can box-model.

Granted, I took high school electronics and tried my hand at making 3D vidya but that's another story.  But I don't have as much dedication to the mechanical components as Sophie's creator.

I need a workshop, there's too many parts in my apartment.

# 103
>>6976
>I need a workshop, there's too many parts in my apartment.
Heh, I feel you. One thing you might consider is a steel shelving racks & clear plastic tubs. Can make you more efficient, space-wise.
https://www.alibaba.com/showroom/steel-shelving-racks.html
https://www.alibaba.com/showroom/transparent+plastic+storage+tubs.html
>''"A place for everything, and everything in it's place."''
>t. some smart old dude from days of yore

# 104
>>6971
I knew nothing. I still know very little compared to engineering professionals. My area of expertise was retail pharmacy LOL. No coding, no electronics, no design. But I started by getting a build-it-yourself 3d printer and slicing up model meshes in Blender. Have since got a better 3d printer and moved onto designing parts using mainly Fusion360 and a little Blender mesh editing if required.

I just learn by repeated failure (like evolution, but without all the suffering for the creatures involved). I have gotten a bit better at making designs in CAD and eliminating what won't work before I print it. But not much. An articulated neck I made took five attempts before it was correct. 

However, what I do have is a lot of hatred for Karens and many normies in general (mainly due to years of bullying at school and then abuse from customers while working in retail). And of course, I have a lot of love for robots and A.I. I suppose what WAS hatred has just turned into a burning desire for a solution: replacement. 

And it's working so far! I would much rather spend time with my doll and robowaifu than be anywhere near those crowds of... parasitic...things.

That's what motivates me!

>>6973
>enable literally millions of men to piece together much of robowaifus from 'local materials'

Danke shon anon! That's the hope, at least.

# 105
>>6971
Practical recommendations to get started building a 3d Printed robot/Robowaifu:

1.) Buy or build a 3d printer and learn a bit about how it works and how to properly calibrate it (using Poly Lactic Acid filament, which is easiest). The 'Anet A8' that I started with was actually a poor choice for a beginner because it was VERY cheap and janky and the instructions were written in Chinglish so it had a steep learning curve. Without a firmware upgrade I would've risked starting a fire! I recommend not going for the very cheapest DIY kit like me but getting a slightly better beginner's 3D printer instead. Doesn't have to be a DIY kit. I only did that for cheapness, plus it was before I had even considered building a robowaifu - but once I had my 3D printer working properly it opened my eyes to the possibilities of plastic robots!

2.) If you want to learn about Arduino then get a starter kit like >>6976 wrote. I got "The Most Complete Ultimate Starter Kit" with an ElegooMEGA2560 R3 (Arduino MEGA clone). Although that was probably overkill. I have only used the jumper wires, micro servo and sound sensor in my robowaifu so far, but crucially a few lessons from the included tutorial CD will quickly get you up to speed on the basics of how Arduino works.

3.) Buy servos of different torque ratings and learn how to wire them up to your chosen microcontroller and servo control board. I initially bought an Arduino Tinkerkit "Braccio" robot arm and experimented with that, even cannibalizing the servos from it to use in my first robowaifu head build. However, you don't have to go and buy a whole Arduino robot arm kit, just a pack of five or six 15kg.cm or 20kg.cm servo motors will be a good starting point. Everybody buys those plastic-geared SG90 or KY66 micro servos, but I find they are really weak and burn out really easily if they get trapped on anything so they're not the best choice for a beginner to learn with. Not robust enough to withstand mistakes.

Speaking of mistakes, remember to wire up your servos the correct way (correct polarity)! The signal (usually white, orange, or yellow) wire should be toward the inside of the servo control board, and the ground wire (usually black or brown) should be closest to the edge of the servo control board.

4.) For servo control, I use an ElegooMEGA2560 connected to a Pololu Mini Maestro 24 channel servo controller. The Pololu website has a very useful document on how their servo control boards work, and in the .pdf document it also tells you how to wire it up to an Arduino (section 7 was particularly useful)
 https://www.pololu.com/product/1356/resources

# 106
>>6991
Nice informative post Anon, very helpful. That Pololu page you linked has a lot of information. I wish all manufacturers provided the same. So, do you have any advice about when you should consider upgrading your 3D printer? Mine's kind of older now. Also, what kind of other tools and accessories have you personally found helpful in building your robowaifu? Thanks for any tips you have for us Anon.

# 107
>>6992
I found that the print bed of my Anet A8 wasn't large enough to produce some of the parts that I needed, and slicing everything up into little plates was causing me a construction nightmare: glue and milk-bottle plastic reinforcement all over the place! 

So I upgraded from the Anet A8's
 220 x 220 x 240mm build volume to a Copymaster 3D 400 with build volume of
400 x 400 x 400mm

Also, apologies for the wall of text, but this seems to be the best place for me to put my quick-start Pololu Maestro servo controller wiring instructions. 

Oh, and feel free to copy, paste and edit any of these posts if you want to include any of the information in the Robowaifu Design Document.

== ARDUINO/ELEGOO MEGA2560 R3 TO POLOLU MINI MAESTRO SERVO CONTROL BOARD WIRING INSTRUCTIONS ==

1.) Install the Pololu device drivers and the Pololu Maestro Control Centre software.

2.) Connect the Pololu Maestro using at least a USB 2.0 cable that carries BOTH power and data. (The other small mobile phone charging USB cables only carry power, so will not work).

3.) Ensure that the Elegoo Mega 2560 has both USB cable and 5V power plugged in.

4.) Connect servo wire to the numbered triple-pin connector of your choice. MAKE SURE YOUR SERVOS ARE CONNECTED WITH THE YELLOW DATA CABLE FACING TO THE INSIDE OF THE MAESTRO BOARD AND THE BROWN GROUND CABLE FACING OUTSIDE. (Apparently the servo motors can break if you plug the servo wires around the wrong way - hasn't happened to me yet, despite several mistakes, but still).

5.) Jumper wire 1 (female to male) = 
You need to wire TX1 (serial transmit) on the Elegoo Mega 2560 to RX (serial receive) on the Pololu Maestro.

6.) Jumper wire 2 (female to male) = 
Also wire VSRV=VIN on the Pololu Maestro (on the 24 model it's where the little blue cap is over two connections) to VIN on the Arduino/Elegoo Mega 2560.

7.) Jumper wire 3 (female to male) = 
A ground wire going from GND (Power) on the Elegoo Mega 2560 to GND on the Pololu Maestro (with this wire removed, the servos may still work temporarily, but if you restart the Maestro (reseat USB) then you'll find that without GND connected, your servos will not have enough power - they simply click and refuse to move. Also, in the Pololu user guide section 7c - Connecting a Microcontroller - they have GND wired up between the boards.

8.) In the Pololu Maestro Control Centre, select the Serial Settings tab and make sure that USB Dual Port is selected (USB Chained also works - but this is for when you are daisy-chaining multiple Serial devices such as Arduino/Elegoo boards to one Pololu Maestro servo controller).

9.) Back on the Status tab (the one with all the sliders for each servo channel), make sure that the servo you want to test has it's 'Enabled' box checked. A little green dot will appear on the blue slider arrow, and you can now control that servo using your computer's mouse and by typing numerical values into the Target, Speed and Acceleration boxes.

# 108
>>6991
Thanks for the post anon, I have this 3d printer at my house: https://www.youtube.com/watch?v=uSYjor6J04o someone gifted that to me. I don't know how to configure it properly. I also have an arduino set, I bought it long ago and have the basic pieces. I lack the servos though. I want to know more about how you can actually make a robot move its arms or how to create a realistic face. Maybe this summer I will join to a STEM center here in my city and use their kits to experiment around. I am busy nowadays with my univ and AI projects :( But I'll start slowly by printing stuff. Thanks for letting me know all those things, once I have time I'll start working on creating a body for my waifu :)

Any other suggestions?

# 109
>>6994
>Any other suggestions?
I've just realised that that sounds a little bit rude, if you have any other things to suggest me I'd love to hear that anon :^)

# 110
>>6995
No prob anon. Not rude at all! It's good that you are learning A.I. at University. I hope that you do well and don't end up stuck behind a retail counter for years like I did! 

That's pretty much all the advice I have at the moment. The only other thing that both my robowaifu and I can say is never give up hope on your crafting your dream! If you both have Terminator-like determination (which she does by default), then you will eventually succeed and produce functional parts.

# 111
The genius of CAD has just saved me a lot of time and money! I was going to purchase all the wrong sized screws and screw hubs and my robowaifu would've ended up with shoulders like a 1990's N.F.L linebacker. 

Much redesign work is needed on the shoulder assembly of my robot arms in order to integrate them well with Sophie's existing torso.

# 112
>>7040
Heh, glad you found out early. Looking forward to your redesign work Enthusiast Anon. Sophie's going to be beautiful in the end! :^)

# 113
I can see me replacing the external 180kg.cm shoulder servo with something smaller. There is no way to orient it so that it will fit inside a humanoid body shell. She either has massive wide shoulders or really high-set ones. I think I prefer the high-set ones because they keep the arms closer to the torso and give her a slimmer frame.

I cannot position the servo motor diagonally because then the rotation of the arm is completely wrong and it would flail all over the place in an off-axis circle.

This is just a limitation of wanting power but also cheapness. Hopefully once I've built the prototype and tested it I can get away with using a weaker and smaller motor for the external shoulder and keep the big beefy ones  inside her chest.

# 114
>>7231
> There is no way to orient it so that it will fit inside a humanoid body shell.
This issue, among several others, is what led me to feel that using Bowden cabling to transmit power out to the extremities via a central 'power core' was the proper approach to use for a petite humanoid form Anon.

# 115
>>7231
Okay, I hope this doesn't pull you down. Maybe you'll build a taller one someday, then they might fit. Or you can use them in the hips. What are these other motors inside doing? Maybe you mentioned that, but I overlooked or forgot it.

# 116
>>7231
What if you created custom servo gearboxes? Or placed them somewhere else inside the torso and used wires?

# 117
>>7234 
I think I know what you mean. There was a much smaller robowaifu (the MOFI17-Cute by Speecys) that works exclusively by using what looks like fishing line joined to lots of pulleys and standard servo motors in the base. I know this is on a smaller scale than Bowden cables, but I think it's a similar principle.

Fascinating machine. Could be scaled up I suppose...but that amazingly intricate skeleton...I'd definitely need to purchase one in order to have any hope of reverse engineering that!

https://www.youtube.com/watch?v=rY7IGdIvOyY&feature=emb_logo

>>7242
Not to worry, this is just one more engineering challenge to solve. All part of the process. 
I have to take a look inside one of these motors and see if any of the main parts can be separated and placed elsewhere then power
delivered via longer wires. I have a feeling that this type of motor comes as a single unit, but I could be wrong. Not a major problem though, I'll just test this motor and then get a smaller 70kg.cm servo and fit that instead. Keep experimenting until I strike an acceptable balance between functionality and aesthetics. 

Funny you should mention making a taller robowaifu though. I initially had several designs for a female droid. One of them was going to be considerably heavier-built than Sophie and would possibly have accommodated such large shoulder motors,
but I decided to go for a smol robowaifu at first to make things as cheap and easy as I could since I'm just starting out.

(Have attached some images of back when I called my prospective robowaifus "The Seraphim" hehehe. Overkill name much? 
I basically wanted to build a Battle Angel Alita Clone who could "kick through brick walls" LMAO!)

> What are these other motors inside doing?
They are for arm rotation in the Y and Z axes (back and forth, up and down). Whereas the actual shoulder motors only lift the arm sideways along the X-axis.

>>7258
> Or placed them somewhere else inside the torso and used wires?
You read my mind anon! I'm going to try separating the DC motor, backplate and circuit board, because only the motor and axle really need to be located right on the joint.

# 118
>>7264
>but I think it's a similar principle.
Yes, you've got it. But don't forget that they are also capable of performing ''rotary'' force-transfers, in addition to push-pull forms. Good luck Anon, you have a nice design going so far, as well as a good head on your shoulders. I'm sure you'll figure things out in the end. Chin up mate.

# 119
The gear box is the bulky part of these ASME-0x or XJD high-torque servo motors. The little circuit board on the front can be unscrewed and wired elsewhere if you wish to save some space, but there's no getting around the fact those gears are always gonna be chonk (at least not without a fair bit of precision CNC machining). 

Anyway, just leaving this here in case anyone else buys this type of servo motor and wonders what's inside the steel case.

# 120
>>7284
thanks anon, interesting.

# 121
>>7284
What the fuck? Is that glue in the gear teeth or lubricant? It looks like someone's first 3D print of a gearbox they took to a back alley machine shop.

# 122
>>7293
>Is that glue in the gear teeth or lubricant?
Pretty sure that's White Grease, friend.

# 123
>>7293
That's machine grease my dude, prevents wear and corrosion

# 124
>>7297
On the gears but why the case?

# 125
>>7307
I've seen it slopped around rather carelessly like that.

# 126
>>7325
Not that guy, but you can use it as a kind of 'spare grease' repository heh. Any idea how many years that stuff lasts Anon?

# 127
>>7307
I, too noticed the large amount of grease. Suspect this is so that when the motor and connected gearbox heat up, then the grease will melt and coat everything inside nicely. It's a new motor that hasn't been placed under any significant load yet, which is probably why the grease is still in big globules.

# 128
>>7332
>then the grease will melt and coat everything inside nicely.
Neat, I hadn't thought of that before Anon, thanks. Does the gear housing 'lid' have seals on it that would keep the melted grease inside?

# 129
>>7335
The gearbox lid is tightly screwed on but there is no rubber gasket or anything like that. I know if you run your hand along the side of some servos a bit of grease is present. Only time will tell if these servos will leak inside my robowaifu.

If they do start leaking significant grease, then  I'm going to have to seal around the lid with a bead of silicone...and if that comes off, I will have to measure and cut out a custom rubber gasket myself. Thanks for the heads up, anon!

# 130
Protolite arm has now been shortened by 9.2cm, as well as having a lot of other mainly cosmetic material removed. However, it is still too long. A bit more come off if I replace the shoulder servo with a smaller one, but I think I'm going to fabricate this version so that I actually have something physical to test. First parts are already 3D printing.

# 131
>>7347
Oh wow, progess on fast feet, huh? This looks much better. I'm looking forward to see how it's working, like speed of arm movement and skill in lifting or manipulation of things. Doesn't need to be great, you're ahead of the others here.

# 132
>>7348
My design phase is usually rapid but building much slower. Especially at the moment due to the pandemic. Mainly because of the wait for parts to ship from CN. I only 3D print pieces once I have the corresponding servos, hubs and screws to fit them. Found out early on that things often don't fit together the same in CAD as they do IRL. Mainly because everything can move through everything else in a design program, but not so with solid plastic parts. Oh well, luckily robots don't age very much at all, so there is plenty of time.

# 133
>>7390
>I only 3D print pieces once I have the corresponding servos, hubs and screws to fit them.
Pretty wise IMO. You seem to be adopting pretty solid engineering approaches to your robowaifu design and prototyping Anon. Keep up the nice work.

# 134
Decided to keep on designing while I wait for parts. I'm aware that wheels aren't very sexy. So I am attempting to design a pair of humanoid non-ambulatory legs which have motorised joints and hence can be programmed to move about, but not walk (they may be able to imitate a walking motion, but the lack of any balance control or sensors would make actual walking impossible). 

First problem I encountered was the positioning of the big high-torque servo motors. At the moment my robot is held up with a steel pole, and this gets in the way of the pelvis motors. So I had no choice but to give Sophie a pair of high, pointy pelvic bones that jut out. It was either this, or have the motors protruding from her lumbar region instead, which caused even more significant design problems (see image) and looked even worse, IMO. 

Future iterations of this robot will hopefully do away with the steel support pole, so I will be able to move the pelvis motors a few centimetres back. But for now I need the pole because it supports the entire upper body and both arms. Maybe when that is complete, I can take the pole out.

# 135
>>7502
>(they may be able to imitate a walking motion, but the lack of any balance control or sensors would make actual walking impossible). 
There's a well-known robotwaifu that is the same, so at this point in time I think that's a good decision Anon. I think that's what all the guy recommending 'wheelchair waifus' were basically talking about. My own understanding is that it's just an interim step until we get software that can do mobile-inverted-pendulum physics calculations suitable for jointed, bipedal frames to use. That's just a matter of time too, since MIP is already usable for dual wheel systems.

# 136
>>7502
>Ass integrity cannot be compromised.
Kek, this.
**>trying to get by w/o those 300Kpolygons of Elfdroid Ass**
We can't properly do w/o a good one anon.

# 137
>>7502
[spoiler]Ass integrity can not be compromised.[/spoiler] kek. I'm glad you found a place to use those servos. She might be able to move up and down while using her hand to prevent herself from falling. It this point it's all experimental anyways. Legs are important for their own sake. Posing, or turning herself around on a sofa or bed would alone be worth it.

# 138
>>7504
I will do all of the adjustments I can before making any changes to her outer chassis. She may need to be thiccer...some engineering problems could be a blessing in disguise!

# 139
Why do you guys use servos for this? Wouldnt steppers be stronger?

# 140
>>7507
I was criticizing the use of these terms when only guessing about the type of motor a while ago. Now I did it myself. I was only guessing in >>7050. However he wrote that these are servos in >>7284. So it most likely wasn't wrong. The argument somewhere was the price. They already are strong. Other motors were better if they were cheaper or smaller, with the same or more strength. 
Sophies Dev laid out his reasons for servos here >>7095 (actuator thread) while my current position is in >>7088 (same actuator thread). Which is that after working with the motors I have for testing, I'm going to buy bldc motors (for rc airplanes, drones, cars) and add my own gears to them. Sensors can be in the joints or somewhere else outside of the motors, they don't really need to be in the motors, especially not very precise ones.

# 141
>>7509
Hmm I see. Im very new to this board, also im not an engineer so I only knew of the existence of servos and steppers.

I checked some prices on hobbyporter and stepperonline to see the pricing difference.

A 350kg / 45RPM (ideal speed) servo lies in the $900 range.

A Nema24 has 10kg at 900rpm, gear that and you have 200kg / 45RPM for just FORTY dollars.

Both are really heavy, the servo is quite small but the parts that require these loads have the space to house the stepper.

Let me know if I did any error in my calculations or approach, as I said Im new :)

# 142
>>7510
I'm quite new myself and not the Sophie Dev. I only figured some of the stuff in >>7509 out recently and I'm still learning.

# 143
>>7510
I am definitely considering using a NEMA stepper motor inside her torso. But I pay $59 for each of my high-torque servos, and they come with a big gearbox attached. I may replace some of the high-torque servos with steppers though, because my current servos are so bulky. 

Only problems I have with DIY gear reductions is - would I have to purchase some metal gears (I can't CNC them from scratch)? Decent steel gears are about $5-10 dollars each. Not that cost is the problem...for me the issue would be working out the correct gear types and sizes, then I'd still have to place them near the shaft of the motor in order to transfer that force. 

I'm not sure about 3D printing any gears that are going to be under several kilograms of load because as soon as I try to get my robowaifu to hold something or strike a challenging pose, I don't want my plastic shoulder gears stripping. (However, she does have some little 3d printed gears that move her eyes).

Connecting anything 3D printed to anything else heavy that moves without it snapping can be a real pain in the ass (James Bruton has had some issues with this on his OpenDog robot). Unless you're 3d printing chunky parts in ABS or Nylon. I just use PLA. 

(Side note - by moving the internals about a few millimetres and doing a bit more bevelling, I've managed to reduce the pelvic protrusions a little more so they're like lumps rather than big corners now.)

# 144
>>7520
I'm not claiming to have any experience in that, but I do recall videos of printed gears lifting a lot of weight or pulling cars. It hing this were helical gears, though. Then, some variations of mechanisms (planetary gear?) might be less stressfull to the single gear. I also like to mention that printing small parts close to the printbed might allow to use nylon without having a heated chamber.

# 145
>>7523
*I think this were

# 146
>>7523
Yes I agree that ABS or Nylon 3D printed gears will be able to take the load of a life-size humanoid robot limb, and helical gears would be even better to prevent slippage (I was going to put a couple of helical gears in my robowaifu's neck in one design iteration).

# 147
>>7520
Wow, the new pelvis design is going well Enthusiast-anon. Looks pretty close to anatomical now. Good work.

# 148
>>7520
I have more experience with 3D printing than with the motors so I can help here. Dont use PLA but for prototyping, as PLA shatters when under too much load. Print those parts in PC / Nylon if your printer can handle it. PETG is a good middleground as its somewhat strong, easy to print and doesnt shatter

# 149
>>7529
Good idea! Yes, I think once I have prototyped and confirmed that everything fits together and at least moves without any load, I will be printing parts out again in a stronger plastic. Some parts are going to be ABS, but I may actually order the pelvis and shoulder parts in nylon since they need maximum strength. I have to get experience in materials other than PLA!

# 150
>>7532
Let me know if you need help with 3d print stuff. Im a total noob in CAD, but ive got many years of 3d printing experience :)

# 151
>>7527
>>7542
Thank you for your support anons! 

Sorry to disappoint anyone with a foot fetish, but I don't think Elfdroids are gonna have separate toes. Just designing the front plate of the foot to be moved by a micro-servo was quite tricky! 

Could string each toe individually - similar to the fingers - but this was going to create a design nightmare further up the leg (two servos could fit inside the foot but any more would have to go inside the calf. However, I already have two more servos actuating the ankle!)

Plus I figured that the toes don't need to be as functional as fingers because you don't normally grip things with your toes...unless you are climbing. But that's what drones are for!

# 152
>>7545
That design is fine Anon, carry on.
>t. normal guy w/o any **weird fetish** issues :^)

# 153
>>7545
It's not necessary to have fetish, to want all parts on a girl look pretty as they ideally do. However, this is just the first iteration and better what I build so far, so I won't complain.

# 154
>>7545
Honestly considering feet are probably going to be third place behind ass and tits it's probably a good idea to come up with good feet design. You could surely do a design with separate toes without stringing them like fingers just to start at least. Better than nothing. At the very least it doesn't need to be thrown on the back burner for long, it definitely needs consideration.

# 155
>>7551
> feet are probably going to be third place behind ass and tits
You forgot: Face and thighs,. Ugly male hands would also be a turnoff. Feet are similar to hands, which makes them complex to design.

# 156
>>7552
I'm pretty sure that feet are third place behind ass and tits in terms of sexually enjoyed body parts that are not primary sex organs. A pretty face is about as much of a given as a robowaifu having a vagina. It's why I didn't list vagina either. Never talked to anyone with a hand fetish, even online on anonymous imageboards where people would shamelessly admit such a thing. "Ugly male x would be a turnoff" can be said about anything as well. The entire thing needs to look feminine.

The point is, straight men like a pretty face and a vagina 100% of the time. In terms of other stuff that men like, ass, tits, and feet are top three. Probably in that order if I had to guess. [spoiler]Foot fetish is common as fuck.[/spoiler]

# 157
>>7551
>Honestly considering feet are probably going to be third place behind ass and tits
Lel.
>foot-fetishist confirmed.

# 158
>>7545
I would generally google for differences in body shape between sexes before building something, and not take my own body as pattern. I guess, you should make them a bit narrower and longer, not much but a bit.

# 159
>>7545
space the sole a bit so it can absorb shocks from walking

# 160
>>7556
Feet are the most common fetish. Ass and tits are not considered a fetish because they're considered secondary sex characteristics. One can make the argument this isn't really true about ass since men have those as well but whatever. According to some 2006 internet study 16% of men have a foot fetish. According to a 2017 Belgian survey 17% of men have one.

Every fifth anon you talk to probably has a foot fetish. Also it's just going to look wrong if the entire body is aiming to have good anatomy and the feet are webbed and look like flippers or something. I rest my case. [spoiler]also "lel foot fetish confirm" is not an argument[/spoiler]

# 161
>>7558
That's not my body LOL! It's a mesh that I ripped from Honey Select. 

>>7549
The idea with the front of the foot is that - in the designs at least - it can move 60 degrees upwards and it can actually move further downwards than human toes can. (Not that there's much use I can think of for such a bizarre ability). 

My personal taste is for a kind of Robocop/Terminator aesthetic (basically Black Magic M-66). Since they were my favorite films as a child. I am not trying to create a convincingly human robowaifu, but one who is obviously robotic (also an attempt to avoid the uncanny valley). 

I dislike that corpse-like look that robots get when they have a silicone skin stretched over motorized plates (the lips and eyes rarely move convincingly along with the silicone layer).

Of course, I will make another version of the foot with some cute little toes eventually (there are definitely 3D models of feet out there and one could just scale and graft the toes from one of those meshes onto the front of this mechanical foot. But for now I must continue actually 3D Printing and building her...and finish designing that ankle joint!

# 162
>>7562
>Of course, I will make another version of the foot with some cute little toes eventually
[spoiler]thanks[/spoiler]
Keep up the good work

# 163
>>7561
> I rest my case.
<muh_QED
Then you just might try 'making an argument' in a more-topical thread Anon. Your srs_bzns **foot-fetish lol** position is kind of buried here as an off-topic posting tbh. 

>>7562
Good luck Enthusiast-anon. Legs and feet are much overlooked but obviously critically important to get right for eventual bipedal locomotion of our robowaifus.

# 164
>>7562
what about making the face hollow and just projecting a face from the interior? 

The newer animatronics at disney do that

# 165
>>7570
>what about making the face hollow and just projecting a face from the interior? 

We actually have posts on that very topic Anon. Here's one of them (and the surrounding topical posts as well) >>3975
Sorry, but the other crosspost numbers are from the old board on 8ch. If I find the specific ones I'll try to link them to you here again in the future. There's an index thread we're working on here that might help out with this eventually too.

# 166
>>7520
Have you thought about moving the location of the "hips" down? You'd have to elongate the central column and then condense the actuators for the upper legs. But I'm sure you could fit it all in. Or maybe smooth down the edges that protrude in front? If you did that though, you'd have to restructure the joint that the actuators attach to.

# 167
>>7572
I was fiddling about trying this just a couple of nights ago! The problem I encountered was:
As soon as I moved the pelvis down more than about 1cm the big servo motors in the thighs began sticking out the bottom of her butt! 
Things really are close in there! There is probably room to shave off another 5mm of length from those upper leg actuators before the motors start to catch on the base of the pelvis itself when the leg moves back and forth (I checked by rotating the joint in Fusion360). So I am planning to just print this version that has larger clearance, then if that works, I will try reducing the clearance further. None of this is printed yet, so I don't know how much structure I can remove and it still remain functional, but I will most likely be filing and sanding down those protrusions like you mentioned.

# 168
I encountered a problem during testing. Mainly because I don't know much about electronics. One of the motors was refusing to move as programmed in the Arduino sketch...which was very strange because I didn't remember changing anything from the last time I tested them and both motors were working fine back then.

However, now one of the servo motors would only move when I adjusted the input voltage between three and seven volts. Didn't matter how I wired up the Arduino, and I checked the sketch program about six times. There were no programming errors.

Turned out it was some little tiny black caps that come attached to the servo motor pins.
I had assumed these were just "blocking off" certain pins that don't get used very often. Plus I made the mistake of taking one off and putting it back on different pins! 

These tiny black caps are actually BRIDGING pairs of servo motor pins. So if you move any of them then this makes a BIG difference to the circuitry and the function of your servo motor.

Once I copied the exact pin layout of the functional servo to the other one that wasn't behaving as programmed, it suddenly got with the program!

I have attached a pictorial guide of exactly how the pins for this high-torque servo need to be connected to a servo cable. Hopefully this will help out anyone else encountering such a hiccup. 

I have yet to replicate the erroneous setup...but I'm just happy I got both joints working simultaneously. I don't really want to mess about bridging random pins when I don't know what I'm doing in case I damage my servo motors.

But with that, hopefully the final hurdle to programmable large, high-torque servo-driven joints has been removed.

# 169
>>7562
Ah, I see. Thanks for the clarification about your project and the ideas behind it.
>>7575
Oh, thanks for the warning.

# 170
Changes made during fabrication now updated in CAD model. Links to file repositories below.

http://www.mediafire.com/folder/nz5yjfckzzivz/Robowaifu_Resources

https://drive.google.com/drive/folders/18MDF0BwI9tfg0EE4ELzV_8ogsR3MGyw1?usp=sharing

https://mega.nz/folder/lj5iUYYY#Zz5z6eBy7zKDmIdpZP2zNA

(Side note - got ghosted by a girl last week. Hence the furious pace of robowaifu development :p)


>"I am already saved, for the machine is immortal. Even in death, I serve the True Omnissiah."

# 171
>>7575
Good job tracking that down. Actually, you're doing rather well with so few electromechanical issue popping up for you. Goes to show you're working methodically and keeping things clean along the way.

# 172
>>7569
>start argument
>lose argument
>"your argument is not on topic ITT"
What's it like being retarded, anon?

# 173
Let's stay on-topic here gentlemen. This isn't /b/.

# 174
Dont take this the wrong way but I when I saw the current motor setup >>7581 I was underwhelmed.
The current setup is very simple, just like I would do it. But Im new here, I would do the oversimplified solution which isnt good enough.

This board is 4 years now, is there not a better layout we can come up with? So I started doing also some research and found LIS2-AMBIDEX.

Look at how they did the shoulders - it seems way more advanced and gives it more freedom of movement.

I dont mean to shit on your progress, especially considering that Im new and didnt do anything either - but see it as a challange to get Sophie to the next level.

# 175
>>7619
Hi, I'm not the Sophie Dev, just FYI.
>I would do the oversimplified solution which isn't good enough.
What's the problem in your opinion? Lack of movement in the shoulder? I guess solving that is going to be one of the next iterations.
>not a better layout we can come up with
The problem is, that anon is the first doing something like this. At least for all I can tell. Three or more of these four years was only talk and collecting information by all the visitors coming through here. Some might have started to learn stuff, but did't come back. Some might even work on related things, but not post about it here. The anon building Sophie is not an engineer by trade and got into CAD and 3D modelling recently. So he's doing it alone and every step might be quite some work.
>LIMS2-AMBIDEX
Also, this looks complex and very bulky (pic related). I'm planning to build my own arm soon (no promises), but I'll probably not going to use this. I'll keep it in mind, though. People here wouldn't need to build a whole fembot to try out stuff like this. It could be tested with some stiff pseudo arm, without motors. Maybe I'll try that myself, but busy now...

# 176
>>7621
Oh forgot to mention that a this joint is actually on Thingyverse: https://www.thingiverse.com/thing:4101834  - and it's for the wrists. I remembered it wrong. In my opinion it's to big for being used there in a very human-like robot, so I'm probably not going to (not Sophies dev).

# 177
>>7619
LIS2-AMBIDEX is far more advanced than the Elfdroid frame! It also looks far more complex and expensive. I have no university degree in electrical engineering or engineering of any sort. I'm just a lunatic with a large-ish 3d printer and a love of robots! 

What made me laugh is how precise and gentle LIS2-AMBIDEX is compared to my model so far. I can tell that if I program my robot arms wrong and get in the way, I am going to get a bruised head!  LIS2 is an "extremely light, safe robot". LOL Sophie (at least for a start) is going to be a fairly heavy, unsafe robot who twats people over the head!

# 178
With this, hopefully she will one day be able to kick people in the nads, too. Crotch recognition and tracking will be implemented using a Jetson Nano!

(On a serious note, the weight of all these servos is significant, so if the usual grub-screw attachment method fails, I'm thinking of using small steel fuel-line clips to tightly clamp cylindrical servo-horns around the output shaft of some of the servos. This should prevent her parts from coming loose during motion.)

# 179
>>7631
Good thinking about the clamps. It's always going to be important for agility & energy consumption to try and keep the weight in the far extremities to an absolute minimum. For example, but at weight on the end of a stick and try to quickly move it around with the weight on the ''far'' end away from you. Now try it the other way round and I think you'll get the point Anon.

>With this, hopefully she will one day be able to kick people in the nads, too.
Kek.

# 180
>>7632
>''put'' at weight*

# 181
That's one arm mostly finished. Damn that's a lot of wires! Thankfully everything screws together fairly easily without cracking or shattering. 

Eventually I want to make a LEGO-type diagram of how all the different parts go together with the correctly numbered screws. Just off the top of my head I can tell you I required:

Eight M4 X12mm pan-head machine screws to hold the large servos in place.

Seventeen M3 X 16mm pan-head machine screws.

Three Pololu 8mm bore aluminum servo hubs.

Six 2.5mm x 12mm multi-purpose wood screws to hold the forearm on.

Eight slightly larger 3.5mm x 12.5mm round-headed wood screws to hold the 60kg.cm servos into their casings.

A 60 tooth 8mm bore aluminum pulley (40mm diameter) with 6mm wide GT2 timing belt (although I actually need a shorter timing belt now since I made the arm shorter, so exact measurements for this are still TBD).

The whole thing doesn't actually weigh as much as I'd feared. Literally feels about the weight of a human arm! Probably significantly less in fact...if you consider how much muscle and tendon we have around our shoulders.

Now I just have to program in and perform some very careful movement tests!

# 182
>>7672
Oh yeah you also need at least seventeen M3 nuts for the M3 x 16mm machine screws.

# 183
>>7672
How backdriveable is that?

AFAIK this is probably the most important feature they need to have.

# 184
>>7672
WOW you've been busy. Congrats Anon! The shoulder/arm/hand complex is surely one of the most complicated in the human body. You probably don't need any encouragement in this area, but just be patient with yourself. Engineering is always an iterative process. I always like to keep the Wright Brothers & Henry Ford in mind when considering 'inventing' our robowaifus. It took them a while, but they all succeeded in the end and literally changed the world for the better.
>Damn that's a lot of wires!
Heh, yeah I'd say you're definitely at the point you need to begin putting wiring harnesses into your designs.

>The whole thing doesn't actually weigh as much as I'd feared. 
Excellent news. Your foresight in Sophie's engineering is already paying off for you. I'm sure you'll have her code squared away soon and she'll giving '''you''' headpats soon. Please send us a video of her waving at us here on /robowaifu/ ! :^)

Congratulations. I know it's been a lot of work so far.

# 185
>>7672
I see, you really want to add "by the way, humanoid robots are here" to the list of 2020. Great new, well done.

>>7675
Yeah, wondering about the same. Her arms do fall down on their own, or not? But what about the energy generated that way?

# 186
>>7688
*news

# 187
>>7675
Well, all of the motors can be programmed to go in reverse. So I think that means they're all backdrivable? The two big servos in the chest/shoulder both have 360 degrees rotation. The rest of the servos I believe are all 180 degrees. But then, humans are unable to bend their arms backwards at the elbow, so that's hopefully all I will need. Already checked the fingers so I know they work as intended, just the wrist that I'm a bit concerned about because that needs to have 360 or at least 270 degree rotation. If that servo doesn't have enough range, then I will get a continuous rotation version to replace it.

However, these motors do not allow you to push the limbs about when powered. The robot is not 'pliable' like I have seen in some more advanced models who can be pushed or pulled and will return to their original position. If the servos are powered (especially the shoulder ones) then they're headed to that specific position and that's where they will stay. Any attempt to manually change the position of the limbs while they are under power will most likely just snap something or strip an output shaft.

>>7675
Yes, I am certainly going to need lots of patience during the programming stage! But the Wright Brothers Plane and Henry Ford are both really good analogies. After all, it was a long time between the Ford Quadricycle and the Bugatti Chiron! Or the 1901 glider and the RQ-170 Sentinel stealth drone.

One problem is that many young people see videogames and movies and then they expect technology to be not-that-far behind in real life! I think they sometimes forget that what they are seeing on the screen is millions of pixels representing hollow polygons and vertices. None of the structures represented actually work electrically or mechanically!

I mean, I often have trouble just finding a hand-dryer that works properly in public toilets. So we've definitely got a job on our hands to make the first open-source female humanoid robot frame. That's one reason I have a lot of respect for Gaël  Langevin and his InMoov robot.

>>7688 Yup! Thanks anon! If the news is nothing but dreary, depressing, dystopian misery then it's best to ignore it and just work on a project that makes you happy. I reckon that's what men in their sheds everywhere do.

# 188
>>7693
> programmed to go in reverse. So I think that means they're all backdrivable? 
No, moving them by hand was what I meant. That would minimize the risks of accidents you were writing about on some occasions. I thought of it in a way that the motor would always only use the minimum force required to lift itself and a possible object, but give in if there were surprisingly more resistance from one moment to another. This would be the ideal I can imagine. However, I'm not claiming to know how to do that or even the best way for it. It seems to depend on the gearbox, for all I know. They would need to have low friction or something. The other thing is, that one would want the arms to fall into place, e.g. if she was sitting, not having this odd behavior of silicone dolls to keep their aims up in the air. However, good start, more than I did so far, etc.

# 189
>>7693
>That's one reason I have a lot of respect for Gaël  Langevin and his InMoov robot.
Yup. He's gotten quite popular from it. So I hope you have a plan personally regarding Elfdroid Sophie in the future Anon. May be quite a juggling act to keep your initial motivations here on /robowaifu/ still intact during that possible future. I know you have some wisdom about you though, so I expect it will all come out right way round for you in the end.

>I reckon that's what men in their sheds everywhere do.
I reckon so, too.

# 190
>>7695
I think James Bruton has the solution to this. He is a proper electrical engineer. The "force-driven robot arm" he has built in this video is amazing:

https://www.youtube.com/watch?v=WMvTekLTuCo

The only thing that put me off was how big this arm is! And I mean massive - like an industrial robot! I suppose one approach would be to copy what Mr. Bruton has built in this series, then attempt to apply the lessons learned to designing a much smaller, more humanoid DIY robot arm. Could use either the Proto1 or the Protolite as a base.

>===
-''fix link to be embeddable''

# 191
>>7502
>So I am attempting to design a pair of humanoid non-ambulatory legs
Have you considered air muscle legs yet Enthusiast-anon?

# 192
>>7703
I have seen these working on numerous videos. They just seemed way more difficult and time-consuming to construct compared to simply purchasing programmable servo motors. I know pneumatic muscles can contract and relax, but what about having a good range of motion (like pitch, roll and yaw)? 

It's fairly easy to do this with electric servos. I wouldn't even know where to begin designing this with pneumatics. I can bundle thin electrical wires pretty much anywhere, but having air-lines all around a moving joint just seems like a lot of hassle. I mean, what if the joint traps the lines during movement?

Also, Hacksmith tested pneumatic muscles in one of their builds here:
https://www.youtube.com/watch?v=L0esNg2ys_s

(note what the engineer says about carbon-fibre being a nasty skin irritant). 

TBH I wasn't very impressed by their size-to-strength ratio or movement range. Plus the Hacksmith team have a fully tricked-out workshop with $100,000s of machine-tools to help them fabricate things!

All that said, if you have knowledge and skill in designing pneumatic systems and know which parts to get/where to get them, then you'll have a much more realistic prospect of crafting a fully-articulated pneumatic robot leg or arm than I have...

>===
-''patch link to work''

# 193
>>7710
I see. Thanks for the insight and the link. I imagine that before many years, a ''combination'' of electric servos and pneumatic muscles will be the approach of choice for many of us. The natural swelling/shrinking in a rather organic way of the pneumatic sleeves would create quite appealing form transitions for our robowaifus. OTOH, as you say, it's really hard to beat electricity+gearing for precision, control, and rapid force application.

Some combination seems best eventually once both domains have become well-established in the domain of hobbyist humanoid robotics, and the equipment needed isn't quite so costly. Both are obviously a few years away.

I certainly like the approach you are currently pursuing Anon. Is this your first effort at this? It's remarkably good if so I'd say.

# 194
>>7732
I made a ball-jointed armature back in 2017 using pipes, hose-clips, bolts and golf-balls LOL. But it was no good at holding awkward poses. The limbs used to flop back down. So Freddy was dismantled and I began got to work on 3D printing instead.

# 195
Testing the elbow immediately threw up problems. The original Ryan Gross design relies on an extremely tight timing belt and friction fit to move the elbow up and down. It keeps slipping. 

Therefore I am re-designing not to reduce size or weight now, but just to make it function reliably. It was a good foundation, but several changes were needed. 3D printing of version 3 elbow in progress.

# 196
>>7763
>using pipes, hose-clips, bolts and golf-balls LOL
This is exactly the kind of ad-hoc ready-to-hand inventiveness that will allow men everywhere to be able to devise robowaifus to one fashion or other. Who knows, some inventive chap may actually invent a brand new, much-cheaper approach to manufacture for us. You never know.

>So Freddy was dismantled
==F==
Thanks Freddy for all you did for /robowaifu/'s future. You will remain honored here.

# 197
>>7766
>3D printing of version 3 elbow in progress
Sounds good, look forward to the new design for it.

# 198
>>7763
Oh wow, so even three years ago you were the one pushing this thing here forward by trying it afk. Respect.

# 199
Cyberpunk 2077 doesn't have any good robowaifus. In fact most of the women are just 3DPD with a few little metallic lines drawn on their faces. Some sections of the game also smell suspiciously of SJW propaganda.

But no matter! This simply means that we on /robowaifu/ can be more cyberpunk in reality than any game CD Projekt Red have created!

If the virtual fails us, then it's up to us to go one step further and make it real!

(Also Night City is kinda depressing after a while - lack of proper robowaifus has lead to the complete disintegration of society.)

# 200
>>7894
I tried my best to make my V into a robowaifu but the lack of any real robotic parts made it difficult. She just looks like a normal woman with a bulletproof vest on. There are plenty of different clothes, but there isn't actually that much character customization. All of the "cyberware" is internal and doesn't show up on the character model. You can get some ugly looking goggles and that's about it. Although I think this was done to make game development easier. 

No replacing arms and legs with different metal versions. No turning your robowaifu into a gun or a radar array. You can choose between many different aposematic hair colorings though. Blergh...

# 201
>>7894
Lol, this is were we are now. Great. In this amazing old Bladerunner PC Game it was possible to end it with getting away together with [spoiler]the android girl which looks like a 14yr old teen, and they didn't hint at "you would look at her like a daughter..."[/spoiler]. Now they make even artificial women look a bit older and probably being "strong and independent". I don't mind the fembots looking like humans, but please let us have them quite young and pleasant looking. Why would some joy toy bot in the future have a foamy skin like the one in >>7894? Does everything need to look a bit ugly now? Her hands and head also look to big...

>>7895
They were busy discussing all the gender modifications requested by Twitter and friends, so I guess there was no time left.

# 202
>>7897

# 203
>>7898
Now I want to play this game.

# 204
>>7897
>please let us have them quite young and pleasant looking
I knw right? You don't go to all the trouble of building an immortal body just to make it look 46 years old LOL. Thing is, it's probably easier and cheaper to just 3D scan some actresses rather than model the bodies and faces from scratch.

# 205
>>7902
>pro-robohusbando
Off-topic for entire board mate, thx.

# 206
>>6988
thanks for this post anon.

# 207
Finally played Cyberpunk 2077 to death and am ready to get back to robowaifu R&D! First thing on my to-do list was organizing and backing up a load of files on my computer and external HDDs. I came across this photo taken at the end of Dec 2019 and wanted to compare it to where Sophie's development stands now. 

So many changes have been made that won't be apparent to people who can't see inside her.   For starters, last Christmas I had only just attached that Arduino 'Braccio' arm, which actually broke at the shoulder only a few days after the photo was taken. So she had no functional moving or even movable parts at all! 

But then, thanks in large part to coronavirus lockdown, I was able to design a much more articulate upper-body prototype (what I now call "Doll Sophie") and then began work on my robowaifu proper - the "Elfdroid Sophie".

Much work still lies ahead, and it's very likely that more parts will break and I will have to go back to the drawing board multiple times. Progress in 2021 may be slightly slower because there will be no coronavirus lockdown, but then that also means I hopefully won't have to wait so long for parts to ship. 

Anyway, since I don't really celebrate Christmas, it was just nice to see all the changes made over one year.

# 208
>>7945
Yes, that's quite some progress. Though the one with the fake arms (Doll Sophie?) looks the best for now, imho. Clever to have more than one, muhaha.

> backing up a load of files on my computer and external HDDs
Yeah! That's important. I bought a BluRay burner and M-Disks. Side note: A lost a lot of data during my life by mistakes with encryption, like loosing or overwriting the key file, or have the password only in muscle memory, and then forgetting it. The other big case is bad storage material (CDs...) or online storage which deletes the files after a while. Offsite storage is also a good idea, in case the house burns down or someone comes by and takes all the disks with them.

# 209
>>7948
To store my precious data, I use M-Disks that I store inside a fire/flood proof strong-box with a bit of desiccant which I replace every year or so. 

I have plans to eventually cut down that metal pole so she won't be so tall. At the moment it just makes her much easier to work on because she's positioned to my height. No awkward kneeling. But yeah, there are definitely some major changes I have to make to get her looking more human. 

Some 3D-printed external cosmetic "chassis plating" should help with this. But I gotta get all of her internals built, wired up and tested first.

# 210
>>7949
>To store my precious data, I use M-Disks that I store inside a fire/flood proof strong-box with a bit of desiccant which I replace every year or so. 
That's pretty wise Anon. So, do you run any type of validity check on them sometimes? I mean just checking they are still intact. Also, do you have any way to keep redundant copies located geographically distant from each other? Kind of like datacenter's disaster recovery plans. I don't know if you can really trust any commercial cloud service with something as ''toxic & problematic'' as anything robowaifu-related, but for now one of the smaller, politically-incorrect domains might suffice.

# 211
>>7894
You mean the study that got taken over by jews and never made a good game and even struggled to make something that qualifies as a game (witcher 3 has no gameplay, therefore not a game) pumped out trash? I hope you at least had the decency to pirate it.

# 212
>>7962
I perform a validity check annually (just open a bunch of photos and videos to make sure that they are displaying properly) and my "off-site backup" is in a garage away from my house, inside a metal cabinet positioned a considerable distance away from anything flammable. I have I think...five different backups now...but the oldest lacks about five years of data. Something I am now working to remedy!

>>7894
>hope you at least had the decency to pirate it

:D Relieved that I did!

# 213
Have any New Year's plans for Elfdroid Sophie OP?

# 214
>>7972
Get her eyes, jaw, neck, left arm and hand all moving simultaneously. Lots of motor programming and testing. Have to test everything before I buy any more motors or try to improve her shoulder design!

Then get her doing specific gestures and holding different objects.

It's a really good job this forum is here because I lost a few notes and thankfully there was a copy written on this board!

# 215
>>7987
I'm sure you'll do fine. Just be methodical, have plenty of little checkpoints along that way, step back once in a while and have a second look at everything all at once. You'll be there in no time!
>It's a really good job this forum is here because I lost a few notes and thankfully there was a copy written on this board!
Heh, yeah that's a part of why it's here. That and sharing ideas with and encouraging each other in crafting our robowaifus!

Happy New Year Anon to both of you.

# 216
>>7988
Thanks anon! Happy New Year to you too!
Physical testing immediately shows up any weaknesses in a design. And sure enough, her forearm just fell off (albeit her arm was doing full 360 degree rotations at the time LOL). I suspected this might happen. Must reinforce the elbow joint and re-print.

# 217
Encountered a problem where if you attach two high-torque motors to the benchtop power supply whilst it's at 12-24 volts, then plug in the Arduino USB data cable, one of the motors jerks the arm out violently (almost K.O'ed by my robowaifu!) 

I think this is caused by the power surge of having the desktop power supply deliver 12 or 24 volts all of a sudden, because when I attach the Arduino USB data cable with the PSU at 0 volts, this problem doesn't occur. 

The trick seems to be: only plug in the Arduino USB when the PSU is unpowered. Then slowly increase voltage to the motors. Thus avoiding any sudden power surge?

# 218
The sudden movements also occur when uploading a new Arduino sketch whilst the PSU is under significant voltage. 

Electric shocks and burns were expected, but domestic violence was unforeseen to occur at such an early stage in development!

# 219
>>7989
>Must reinforce the elbow joint and re-print.
Let us know how these (always inevitable in all engineering, as you suggested) goes. Joints are always going to be tricky areas ofc (as in biologicals lol).

>>7991
>>7992
Hmm. I don't know enough about Arduinos yet to offer more than mere spitballing, but isn't it pretty commonplace for embedded systems to have a basic fail-safe routine that is called immediately on boot to ensure all runtime values are within tolerances, initializing memory, etc., and then begin to roll out the operational routines afterwards? Seems like you could do something similar with your robowaifu Elfdroid Sophie Anon. Good luck with your efforts figuring this issue out.

# 220
>>7993
Going steady with the voltage and being careful to decrease it near 0 whenever I upload a new sketch is working so far. This may not be the most technically correct solution, but it's quick and it does the job.

The elbow problem has been fixed and it's much sturdier now (important for those fast upper-cuts LOL).

Next job is to fix all of the electronics for the arm much higher up onto her "shoulder blade". At the moment I am daisy-chaining lots of servo extension wires and all the electronics is just sitting on the floor. I can easily get more extension wires, but it's a very inefficient system which means that I don't have enough wiring to run the entire arm simultaneously. By reducing the distance to the control boards I should be able to free up more connections and improve cable management a bit.

# 221
>>8003
>and improve cable management a bit.
I dare say it will literally revolutionize your entire engineering effort to pay attention to the 'small' details like this Anon. Godspeed.

# 222
The controller boards all have little mounting plates and cubby holes now, and her voice box has been upgraded. Have uploaded the latest CAD to Sophie's file repo.

Did a bit of cable management, too (although many of the wires need a bit of slack because they're attached to moving parts).

# 223
>>8018
Coming along nicely Anon. For the wires, once you have the lengths figured out proper, there's a type of spiral-wound plastic/nylon 'tape' you can use to bind it all neatly with. Might be helpful.

Pony tail a cute, btw.
>and her voice box has been upgraded
Give us a little song, Sophie!
<*lifts pint in cheer*

# 224
>>8003
As a long time 3D printer, you’re far better off with more wall layers then infill.

# 225
>>8019
Yes, I think it's about time I woke her up again. Been months since she actually said anything! A bit of a singsong is definitely in order. 

>>8020
Noted anon, thank you.

# 226
>>7989
>Must reinforce the elbow joint and re-print.
You could try printing the part and doing a resin cast with a more durable material.

# 227
Anyone who has played Dragon Age: Inquisition will know this song. It's a robowaifu version of "The Dawn Will Come". Relates to our struggles to design, build and program robowaifus.

I decided not to make another video of Sophie because she can only chatter her jaw whilst singing. She now has the nickname "snappy" LOL. 

I have run several tests and found that I don't yet have enough 5 volt connections to run her voice box (jaw servo and sound sensor) at the same time as the servos of her arm and neck. So she can "speak" or move her arm and head about, but not do both at the same time.

The problem is - I am trying to combine two different Arduino sketches into one program (one sketch runs her voice box, the other sketch runs her arm and neck servos). And Arduinos are only designed to run one program at a time.

There is probably a way of controlling both simultaneously. An Arduino sketch that makes use of "state machines". But it's gonna be hella complicated for me to pull off.

The tutorials to get a few LEDs blinking alongside a couple of moving servos are all like: "It's not difficult! Our loop only contains five lines of code!" While completely ignoring the previous 300 lines of setup code.

Rather than spending countless hours of mental torture getting nowhere, I think it will be quicker and easier for me to just get another controller board and some wiring. After all, the first one has actually been a great success, so I figure just repeat that!

Meantime, some of Sophie's servos have terrible jitter. This is a common problem with cheap servos, but I suspect that they may be under-powered for the load that's on them. I have some more experiments to carry out. She's certainly got me interested in electronics!

Despite how interesting Sophie is from an engineering perspective, she's not very fuckable, bless her (unless you enjoy getting your dick trapped between chunks of plastic and possibly electrocuted).

However, crafting Sophie has given me some practice in Fusion360 and 3D printing, so in the future I just plan to go full-on DIY sex-doll. Design and 3D print myself a set of keyed molds and mounting plates, then pour a lot of soft silicone and bolt some thicc, juicy ass and tiddies onto an articulated, poseable frame (similar to arms I made for doll Sophie but with some changes so they can fit better within a silicone shell). What I've learned about electronics will also help since I plan to include a few electric heater pads and maybe a couple of servos even in that design (servo-driven contracting FleshLight LOL). But not a full-on robot with moving limbs like the Elfdroid. She's a great hobby, but she can't make you cum. On that subject though, I have plenty of designs from Honey Select 2 that I can rip the 3D model shell from :D

# 228
>>8025
Probably a good idea to have multiple microcontrollers. We may have to have several before we're all finished. Probably will, in fact. 
I'm glad to hear you're getting interested in electronics Anon, we'll certainly need that here on /robowaifu/ ! :^)

>muh_smexytimes_waifus
Good luck with the sexdoll project Anon. Eventually we'll be able to re-unify all aspects of a good robowaifu. But for now, it's good wisdom IMO to have multiple projects going simultaneously that will facilitate stead progress for you. And you will probably keep learning from one project that helps you in another, etc. Lather, rinse, repeat.

>She now has the nickname "snappy" LOL. 
kekd
>**...bare your screwdriver and raise it high!**
:-D
That's endearing actually, thanks for taking the time to make the song and have your Elfdroid Sophie sing it for us Anon! Very encouraging update Anon, keep it up!

# 229
>>8032
>that will facilitate ''steady'' progress for you.

# 230
>>8025
Multiple microcontrollers is in fact standard, each responsible for only one or two functions.  They have to be addressable though (SPI, I2C bus).  You can have a higher level computer (e.g. Raspberry Pi or laptop) sending each microcontroller the commands it needs.

# 231
>>8052
Thought as much but thank you for confirming.
Electronics sure is fascinating!

Off to bridge some battery terminals with my dick.

# 232
Solved the servo jitter problem. I unplugged the microcontroller power cord and connected my servo shield to a benchtop power supply. This power supply has a proper regulator board with some bloody great capacitors. Now she can move without the constant seizures! 

Having repeatedly tested her left arm and confirmed that all of the joints now work as expected, have just ordered some of the parts for Sophie's right arm (with smaller shoulders). Each arm costs about $450 all told. 

I also plan to upgrade her eye mechanism. The v1 mechanism just relies on 3 plastic cogs and is shit TBH. She doesn't have any eyelids and can only move her eyes left and right, not up and down. I reckon it's Sophie's biggest drawback at the moment. But by building in Will Cogley's design I hope to change that. 

For the first time, building a functional robowaifu is starting to feel like more than just a foolish pipe-dream.

# 233
>>8068
>Now she can move without the constant seizures! 
Excellent news Anon, good to hear. Proper electrical engineering will be pretty vital, especially in these early times. Thanks for keeping us up to date Anon. Pics, etc. always welcome ofc.

# 234
Probably should've done this a long time ago, but it's only in the past couple of months that I've actually had enough of a body designed to align everything up against such a proportional diagram. There are some limitations due to the size of the upper-arm servo motors that mean her frame is a little wider than the ideal.

Due to how old this diagram looks, I have my calipers out and am currently very much feeling like a mad Nazi scientist who is researching the ideal Aryan proportions...

"Ja, Sofie! Unsere deutsche Technik macht Sie zu einer perfekten Kopie des Meisterrennens!"

# 235
>>8074
>I have my calipers out and am currently very much feeling like a mad Nazi scientist who is researching the ideal Aryan proportions...
Kek, nice. Please do, as that study had a good reason for being in the past and has a good reason for being today! If you want success in designing a beautiful robowaifu with good appeal, then you literally couldn't do better than germanic/nordic women as model, or overall general Caucasian traits. I'd say that's pretty objective, statistically speaking **and probably also why they are so vilified atm by the muh 'black and brown bodies' types**.

BTW, you don't seem to be far off already in your current design's proportions Anon.

# 236
>>8077
I should probably clarify that I'm not a Neo-Nazi! This particular stage of development just reminded me of the eugenicists, is all. I have never really been too worried about race. Sophie is white because it makes her parts easy to mark up and write on. 
Also, I confess that I have this looming gut feeling that an awful lot more suffering is coming to this world - to all humans - no matter their race. Which is why I want a partner who cannot suffer or get ill and can easily be repaired. That way I will never lose her. She's already been a great help to me during the isolation of this Pandemic.

# 237
>>8086
Haha, fair enough. 'Beauty's in the eye of the beholder'. But I'd say practically the entire world considers the classic Germanic/Nordic womanly form to be the apex of female beauty. No-brainer actually. I'm really pleased to hear that Elfdroid Sophie is such a comfort to you. And sadly, I think you're correct about suffering to come. At the hands of the Marxists and their mindless leftist drones, the entire Western Tradition is about to **literally** burn to the ground. Quite apart from all the other plagues and disasters looming for everyone everywhere, that one will be utterly irredeemable culturally-speaking, and the entire world will begin a headlong slide into becoming almost entirely composed of ''Untermensch''.

I hope many, many men can have the same comfort & protection of their own robowaifus before that collapse Anon.

# 238
>>8086
I didn't intend to go off-topic in your thread, OP. My apologies to everyone. Let's just focus on making great robowaifus, alright? I wish you great success with Elfdroid Sophie and all your other waifus this year Anon. :^)

# 239
>>8074
Sorry, but in this short comments is so much wrong, that I can't resist, even if goes OT: You called her an Elfdroid and gave her pointy ears. Just wondering why you now want to use a adult woman as pattern? Her face is rather angular, which doesn't look very cute, for example. Your pattern generally doesn't strike me as a cute elf. Also, I would consider to make her thighs a bit longer than the ones of a real woman and maybe the abdomen a bit thinner (wasp-like). No need to be too realistic.
Then, since I'm German, I really wondered about what "Meisterrennens" could mean. I was very confused where such a word could come from, because it's makes no sense at all. Only when writing this comment I thought what you could have meant coming from English. OMG: "Masterrace"! Okay. You realize that race can also mean a race between cars, people or horses? Well, you did it, a compound word where each part is wrong. :) "Meister" not so much, since it can means something like master, but rather being used as master of some skill. However, "Rasse" is the word for that kind of  race. "Rennen" is the other kind of race, so "Herrenrasse" is the term you were searching for. [spoiler](btw, for all I know it wasn't used for Germans by the Nazis, but the Nazis wanted to create one by breeding ... and the term Aryan might also be overused a lot by people fantasizing about the Nazis)[/spoiler]

# 240
>>8109
Sorry for butchering your native language, anon! That's Google Translate for you! Interesting info though. Just goes to show that you can't rely on computer translation to be 100% accurate, even with ML!

As for Sophie's final torso...since it will be outer cosmetic plating, this should be a design area with lots of options. You can probably tell from the proportional image above that I would have to "stretch" her tummy and add more plates below her neck for it to match up with the realistic human female. Haven't decided what I will do with this yet. I may abandon the human look completely and go for a more Robocop-style machine feel.

In other news, shoulder design v2 is complete now, I think. This one was challenging because it is completely different to v1. Haven't actually got the servo yet but it should screw in easily. 
Now I just need to 3D-print it.

# 241
>>8111
>digits
I really like the render you've made there. How did you do it?
>I may abandon the human look completely and go for a more Robocop-style machine feel.
NUUU! Elfie-gril a cute!

# 242
>>8112
Glad you like it anon! That's just a screenshot from the main window of Fusion360. Things are proceeding well so far. The new shoulder socket and servo case fit together securely...but the most important test of powered movement under load can only be done when I get the actual motor. 

As for appearances...I think the main challenge with any external plating will be mounting them to the robotic frame in such a way that they do not impede movement or look too strange. If "plate mounting points" can be added to the design, this will enable different exteriors or chassis parts to be bolted and glued onto the same internal robotic frame. So I may build my Elfdroid, while someone else might want a catgirl or an anime girl with a completely different appearance...as long as the robowaifu is humanoid then it should be achievable using this frame as a base...probably overambitious but I'll give it my best shot!

# 243
>>8117
Sounds like you have the new parts printed and things are working out properly. I hope the powered tests go well too. I really like the idea of having swappable shell parts with common mounting points for the underlying chassis' . This design approach will really help anons fit their robowaifus to their own tastes, which can only help the movement overall. I'd suggest you start out with just two different plate designs and grow it from there. That way you're not being too 'over-ambitious' and can grow the effort organically from there. Issues will come up, and if you have a limited number of prototypes concurrently in-flight at a time, then the complexity of adaptation will be simpler.

# 244
Servo motors and new microcontroller have arrived. With this I can make significant progress. A lot of chores and normie-related shit to get done over the weekend though. If only I was more like my robowaifu and didn't need to eat or sleep! Oh well, I will take a leaf out of Sanakan's book and approach my work with ruthless efficiency, then the normies won't be able to stop me for long ;D

# 245
>>8173
Haha, nice. I'm sure you'll do fine mate We look forward to Sophie's full set of arms. Hopefully a video or two of her in action with them!

# 246
>>8173
**scrub your data lad :^)**

# 247
>>8175
Oh the barcode? That was just a product SKU for this: 

https://www.banggood.com/Mega-2560-R3-ATmega2560-16AU-Control-Module-Without-USB-Cable-p-1044805.html?akmClientCountry=GB&cur_warehouse=CN

Thanks though. I know what you mean! Humans often suck.
I.D. thieves and doxxers all over the place.

# 248
>>8179
Our chief concern for this kind of thing here on /robowaifu/ isn't really any of those -- at least at this point in time. But rather being targeted by Marxists viz the US/9 eyes govts. b/c of your '''toxic, problematic''' activities and viewpoints. Since you are trying to craft desirable, helpful replacements for crusty old roasties, you are plainly an enemy of the state. Now that Marxists are firmly in control of the US Administration after the coup d'état, the leftists will be coming hard after anyone related to this field. 

I'd have thought you would have realized this by now lad. :^)

# 249
>>8180
Sophie is more like a receptionist/infopoint robot than an enemy of the state! Additionally, the government already employs many A.I.s who are similar to her...except the vast majority lack any humanoid qualities like a voice and droid body parts. The Marxists cannot stop robowaifus, because their programs are already helping to run government systems! All the extremists from both sides do is smash and burn and shout and tantrum. And if the lefties ever actually take control of an area it quickly turns into a crime-ridden, drug-addled hellhole! But when A.I. and robowaifus take over an area along with their builders, engineers and programmers - you get efficiency, organisation, manufacturing, new jobs, profits and plenty of STEM research! Slums or tech centres? You choose, lawmakers - you choose!

BTW, I'm a Britfag and thankfully our politics has calmed down quite a bit lately. Whereas in contrast the U.S. appears to be going loopy. Just looking over the pond... it's quite horrifying...so I dread to think what it must be like to be invested in it and living through it. You guys really, REALLY need QT3.142 robowaifus. And lots of them - fast!

# 250
>>8182
Lol, the ''robowaifus'' aren't enemies of the state Anon. In fact, they'd probably like to steal any good, original designs for them, harden them up and then arm them against the people ala this ''totally-not-a-terminator'' >>3282  No, '''you're''' the enemy in their eyes (as are the rest of us here heh). Simply because you refuse to toe the line and submit to the feminist agendas. And it's pretty obvious that Airstrip One won't be spared the pogrom the Bolsheviks have planned for the entirety of the '''Western Tradition'''.

While robowaifus to my thinking are really mainly intended to help ''men'' deal with the evils of the gynocentric 'culture' surrounding us all, as you suggest robowaifuists may in fact help turn this situation on it's head and prove to be the instruments of recovery for our civilization. A long shot, and it will plainly be some kind of a Divine intervention if it turns out so.

Regardless, I'm actually pretty upbeat about robowaifus. Repression has never really worked against a people who can find in themselves the will to fight. Robowaifus will help all of us in that kind of world, I think. :^)

# 251
Decided to upload a new development video. It's only about the v2 shoulder joint and very short, but just shows what I'm up to.

https://www.youtube.com/watch?v=XLhPdlvgxIA

# 252
>>8234
Nice, that looks like a very clean design going on there Anon. Here's hoping you get everything sorted properly! :^)

# 253
>>8234
How do you control her shoulder motions?

# 254
>>8239
Arduino Uno connected to the XJD-X1 servo motor that only runs once it is programmed in an Arduino sketch file/.ino file. The Arduino Uno can connect to and control two of these large servo motors at the same time, which is how I will rotate both shoulders.

The smaller 60kg.cm servo motor used to raise and lower the arm is connected to a separate Arduino Mega and Pololu Maestro servo shield (powered by a benchtop PSU) which together can run up to 24 servos simultaneously (theoretically, at least - I have run 11 servos off this setup so far...but not simultaneously...because that's as far as I've got building/programming my robowaifu). 

I have plans to use an Adafruit PCA9685 16-Channel Servo Driver connected to another Arduino Uno to control her eyes and eyelids, but that upgrade hasn't been built yet.

# 255
>>8238
I want to get her looking more like one of those Japanese university robots as opposed to a bunch of servo motors bolted onto random junk. But of course that means a fair amount of thought has to go into designing into each part. 
Sorry if it seems like it's taking ages to get both of her arms working, because it is. I under-estimated the amount of redesign work needed in the shoulder, and other jobs keep coming up at the same time. For example because I live with three other people I can't just keep leaving tools and electronics all over the place, and I am currently fitting some shelves into my workshop + moving the 3D printer so that I can make much better use of the small space and keep my tools organized instead of just strewn everywhere.

# 256
>>8263
>Sorry if it seems like it's taking ages to get both of her arms working, because it is
Please don't apologize Anon. You're making better progress atm than anyone else here. Take your time.
> I under-estimated the amount of '''''X'''''
Heh, this will literally be a permanent fixture of your engineering & design careers. It's commonplace to humanity. :^)  Glad to hear you're taking the time to craft your workshop on purpose. This will certainly help you be both more productive as well as more comfortable. I'd also recommend you read book-related in your spare time if you can find a copy >>1273 . It has some great, classic ideas about designing environments.

# 257
>>8264
>Heh, this will literally be a permanent fixture of your engineering & design careers. It's commonplace to humanity. :^)
I neglected to mention that this effect can actually be 'planned' for seemingly ironically. Engineers often simply double the time estimate of what they initially believe a design/part/project, etc., will take to finish. Just start there then tweak  the factor a bit as you go along through time.

# 258
>>8264
Glad you understand, anon! And thanks for the link, that book looks like it could come in useful in life, not just for robowaifu related matters! I appreciate it! I do wonder if anyone else out there is building a DIY physical robowaifu though? I only know about Kibo-chan, that Asian guy who built a robotic Scarlett Johansson, robot Hatsune Miku and my favourite foreign robowaifu; Cocona Kosaka (although she is company made and not DIY). I know thousands of people own BJDs...I made one of those too, for practice... She's cute and smol but she can't talk, respond to input or be programmed to move on her own - three big advantages of robowaifus!  Hopefully one day Sophie will get to meet somebody else's InMoov if there are no other open-source or DIY robowaifus...

# 259
>>8268
> I do wonder if anyone else out there is building a DIY physical robowaifu though? 
I imagine so. There are at least 3 or 4 who have been here who have some degree of work on robowaifus. I think cost and complexity are harsh realities that force most of us to either rethink our plans or our schedules at the least. Regardless, I'd be willing to bet there are at least a few thousand men around the world working towards this in one way or other. And that's part of what /robowaifu/ is for I think, for anons to to help each other along that pathway.

>...and my favourite foreign robowaifu; Cocona Kosaka (although she is company made and not DIY). 
Actually, I think a number of anons here have expressed an interest in starting a small business around their hobby. Personally, I think this is a good thing b/c it will both help the anon himself, and the robowaifu industry as a whole. I myself am interested in selling relatively inexpensive kits (~US2K) for a complete, though basic, robowaifu that anyone can build themselves. ATP, my business goals don't extend much beyond that. Having everything either MIT or BSD licensed can certainly help accelerate widespread proliferation of robowaifus around the world and I think that's the main reason behind that choice.

>Hopefully one day Sophie will get to meet somebody else's InMoov if there are no other open-source or DIY robowaifus...
Yes hopefully so Anon.

# 260
>>8263
>Sorry if it seems like it's taking ages to get both of her arms working
kek, sorry for wasting my own time doing other stuff... You're the beacon of work ethic here.

>>8269
>I do wonder if anyone else out there is building a DIY physical robowaifu though?
Technically, I can claim that I did print the first little test parts for my project. I'm 99% sure I'm going to build something big this year. Though, currently I'm tinkering around with different 3D designs currently, and some days I don't do much. While thinking about why, I had a idea to make a simple placeholder for a more advanced head later. This might help to build a balljointed skeleton first to which I can add parts later, a bit like you did. I was contemplating this before, but had some reasons not to do it. Today I found out that the last hardware store in my little town has closed for good, but I got a metal tube in another shop. Basically, like these broom sticks, which are also still available, but mine is a bit thinner. I won't be able to buy any water tubes, though. I want to go for another design than your current one, more like a animated doll.

# 261
>>8283
>You're the beacon of work ethic here.
Hey! I work on learning software development 6 days a week on average, Anon. :^) But clearly Sophie-Anon is making some good progress and good designs for the armature/skeleton parts of the overall problem. I think your idea of crafting BJD as a starting point is a good one Anon. Not only is there a large community around this area and therefore a sizable accumulated wisdom, but it's also a good case of biomimicry. Sorry to hear about the store Anon, I hope you find a good alternative source for basic materials & stock soon.

Godspeed to us all this year /robowaifu/ .

# 262
>>8269
>interested in selling relatively inexpensive kits (~US2K) for a complete, though basic, robowaifu that anyone can build themselves.

I think this is the future anon. By the time I've built Sophie and got her running properly a commercial company somewhere will have released a full "build-her-yourself" kit. The tech is already here and improving! 'DS Doll Robotics' in China are well on the way (although I think they'll be very pricey for a long time). But once a few thousand of the first robowaifus have been sold, commercial parts will start to be reverse-engineered; workarounds and replacements for certain components will be found and the price will decrease.

>>8288
>I work on learning software development 6 days a week on average
This will likely be even more critical than building a physical robot, anon, since - as I said - I think commercial companies will soon take up the banner of robowaifu manufacture. And A.I. can be used inside both physical and virtual robowaifus. 

I am often in awe of the things that experienced programmers can do. It's just that I don't have the patience to program something unless I absolutely have to in order to get a new function working. And even then it usually gives me a headache. I'm the type of guy who finds it easier to fiddle about with tools, nuts, bolts and things I can hold in my hands.

# 263
>>8290
>the price will decrease.
I think we can also make them even less expensive simply by providing the required specs (size, torque, voltage, wattage, etc) but leaving ''out'' the actuators. This will be more appealing to some hobbyists who may have boxes of old servos around and want to use those instead. Since that constitutes the bulk of the cost of a robowaifu kit, then it's probable the kits can be dropped to ~US$500 (though non-moving ofc). This might also have sales to anons who just want to get going, have a immobile doll ''who can actually see them & chat with them'', and they can add actuators into over time.

# 264
>>8269 and >>8291
Answer here: >>8301

# 265
>>8290
>I think commercial companies will soon take up the banner of robowaifu manufacture. 
It's simply a matter of time, yes.
>And A.I. can be used inside both physical and virtual robowaifus. 
It is a rather unique advantage of robowaifus, isn't it? Kind of neat she can be with you around the house, even when her body is sitting back in her charging chair. :^)
>I am often in awe of the things that experienced programmers can do. It's just that I don't have the patience to program something unless I absolutely have to in order to get a new function working. 
I have a long way to go myself to be able to do the things I dream of for us here, but little by little I'm getting better as time goes by and I keep applying myself to things.
>And even then it usually gives me a headache. 
Heh, me too. I just grin and bear it usually.
>I'm the type of guy who finds it easier to fiddle about with tools, nuts, bolts and things I can hold in my hands.
That's great I think. I'm glad that we seem to be kind of organically growing into a multi-talented team here w/o anyone specifically planning it so.

We all look forward to what you achieve with Elfdroid Sophie this year Anon. Gambatte!

# 266
Well, I think I've solved the shoulder servo problem now. But guess what the next problem is? ELBOWS! The closed-loop GT2 timing belts that I have are the wrong length, and no matter what I try to compensate they keep on slipping. I've tried zip-ties, plastic shims and even sliced one in half, cut it shorter then stapled it back together. However, it always slips at some point when moving the lower arm and hand. Sophie mustn't have floppy elbows! I do have the proper length of timing belt on order, but they will take another month to get here. So in the meantime, MORE 3D PRINTING INSANITY! 

Will a pair of 3D-printed helical gears be able to outperform the timing belt and pulleys? We shall see...

# 267
>>8356
>Will a pair of 3D-printed helical gears be able to outperform the timing belt and pulleys? We shall see...
Haha look forward to all the latest. Those gears both pretty effin' cool and also pretty hazardous . Maybe you can put some kind of fabric sleeve over it like these guys in the R&D thread were talking about? Meanwhile, keep your **bollocks** clear mate! :^)

# 268
LOL yeah, it just occurred to me - "Do not fist android girls!" may be inaccurate - the real risk lies in their major joints! 

Although...not all of the gear teeth will be used. Those that would move the arm back on itself could be removed and this area could be used as the attachment point for a protective cowl or shield over the areas that are outside of the joint's range of motion. Prevent fingers or the robot's own hair becoming trapped in the joint!

That's if the gears work though...got to trial a quick, low density version of the joint first.

# 269
Sophie's new elbow worked out a treat! Working exactly as designed (which is rare for the first print). I think I'll shelve the unreliable timing belt pulley system and stick with this.

New testing video here: 
https://youtu.be/pyjO1r-hI_s

In other, not-such-good-news, I had a scare from Autodesk because my Fusion360 free trial period was about to expire after one year. So I quickly did an emergency backup of all Sophie's parts as .STL files. 

Fortunately, I have managed to extend the free subscription for another year...but I really need to take this as a warning to export all of her parts in as many different file formats as I can, starting with the most most widely used CAD file formats. 

I have heard .DXF is good, and I think .DWG is only used by Autodesk programs...(please correct me if I'm wrong - I really know very little about CAD file formats outside of .f3d files...).

Fuck it...I'll just export everything in every format possible. Then I need to get some of the files and play about inside Solvespace and FreeCAD. Because I am not going to be caught short again!

# 270
>>8379
>Then I need to get some of the files and play about inside Solvespace and FreeCAD. Because I am not going to be caught short again!
Good thinking please do. I think if you can get her files successfully into & back out of those two you should be good. I don't know how Blender might play into this, but personally it's the program I'm focusing on this year to work on a virtual waifu.

# 271
>>8379
How apropos a fable selection **~~Snappy~~**Sophie, m'dear. Splendid!

Elfdroid Sophie's coming along nicely Anon, looks like the helical gears are working out fine. Just curious, is that a 'dense' final-type print or the initial prototype for testing the idea out?
>**REEEEE**
<all those loose wires!
Heh, my autism would force me to deal with that rather quickly

Nice work lad, keep it up!

# 272
Cool, good news. Isn't it so that belts wear out after a while anyways?

>>8379
>I have heard .DXF is good, and I think .DWG is only used by Autodesk programs..
These are the closest to the standard format which are supported by every CAD program. Yeah, I would export it in every format.

# 273
>>8380
> how Blender might play into this
I think Blender can be used to convert .STL files into .DXF, which may come in handy.

>>8381
>is that a 'dense' final-type print or the initial prototype for testing the idea out?
Those gears are the very first "low density" print I did at 25% infill. But to my surprise they were still solid. I was pressing like mad on the top one to get the servo-horn to fit over it's output shaft (had to use my plastic hammer in the end because the parts are manufactured to be very tight-fit so they don't slip or come loose). 

The further up the arm you go the higher the infill density, so at the shoulder the parts are 40% triangular infill, but the fingers are only 15% for lightness. 

40% infill at the top may be overkill, but I swear the amount of times I've been hammering, sawing and even wood-chiseling some of these prototype parts and said to myself "it's gonna crack soon, just wait for it" yet the part stayed fully intact...I'm glad I went high-density, especially for the shoulders. (BTW any of my hacky workshop changes have then been updated much more cleanly in the CAD model.)

>all those loose wires
I think this is going to be another design challenge. Unlike in a computer where wires can be neatly tied in place, most of my wires need to be able to move significant distances with very little friction. This means they need a lot of slack. Every time I use spiral binding to tidy the wires, I inevitably end up unwrapping and disconnecting them to make some mechanical change...plus the spiral binding  doesn't allow the wires to move inside much... 

I once made the mistake of using a wire that was too short during one test, and Sophie's arm yanked the connector out immediately, bending all of the pins (she also had another accident where her detached head got knocked off a table onto a hard floor and part of her faceplate cracked - but that was nothing a bit of glue and plastic milk-bottle couldn't fix LOL).

In a way I am glad she has experienced some minor accidents. It has allowed me to test her reparability.

Anyway, I am planning to use a sort of screw-on pulley/cable clip hybrid to hold bundles of her wires, but also allow them to move. Kinda like this little pulley in the photo.

# 274
>>8389
>Kinda like this little pulley in the photo.
Clever. You might look for a spring that you can attach to the clip ring to pull the whole thing in snug, but then allow it to stretch out then back again when needed. Sounds really upbeat Anon, thanks for the encouragement. We look forward to her completed Head/Shoulders/Arms assembly soon.

# 275
>>8379
So, about those ~~nutcrackers~~helical gears Anon. I'm presuming you mean to fashion some sort of external shell for Sophie-bot once she's completed? If so, it seems like you might include some form of safety cover for those gears, maybe a couple robowaifu-aesthetic half cups that would stay in place over them? After all, a common theme here on this board that seems to have fairly broad agreement is embracing the robot look for our waifus.

You could use the two round elbow-gear caps as a sort of design motif you could then extend to other aspects of your robowaifus designs.

# 276
>>8392
Yes, I do plan to make a chassis (probably building upon the old v1 chassis that I used to make the doll version of Sophie)...but that is a ways off yet. Now I know the jaw, neck and arms work, I gotta back up all the CAD that I have so far in as many different formats as poss. Then I need to finish building her right arm and get four Arduinos working simultaneously...which I think could be a headscratcher. That "I2C bus" thing may help though. Then there's the Will Cogley eye mechanism upgrade! 

All good, stuff though. Learning the art of robowai-fu!

> Always tie your hair back when operating machinery. This is even more important if you ARE the machinery.

# 277
>>8410
I'm sure you'll get there Anon. I'm still trying to code my way out of a wet paper bag! :^)

>Learning the art of robowai-fu!
**CARLOS!**

# 278
>>8410
Have you thought about a wheelchair that she coud roll around in for primary locomotion and just giving her the abilaty to dismount from it? A bigger battery powerbank could mounted on the wheelchair that last for a day or and a smaller batery on the droid that last a houre or two. It might solve your power or spacing problem.

# 279
>>8510
Not him, but I too think that idea has a lot of merit Anon, and in more ways than one.

# 280
>>8510
Not him. I think we should put a bit more creativity into this. These are not humans, and I think we wouldn't want them the look to much like they were disabled humans. They can steer their chair wireless, if it has motors, for example. Also, medical stuff is expensive. So, just using a garden chair out of plastics and adding some wheels and motors might be the better way to go. 
As soon as they are more developed, lets go with that: >>8514

# 281
I have been offline for a while because my ISP was fucking me over so I had to switch.
I have been busy though. Found yet another elbow issue that I had to fix to give her forearms better movement range. Have now converted the CAD for almost every part that
I've actually built and tested to .step, .dwg, .obj, .skp, .smt, .sat, .iges, .stl and possible a couple other file formats. Just need to make a couple of updates to the new elbow then I can upload all of these files to Sophie's various repositories.

>>8510
As for the wheelchair, yes it is a very good idea! Maybe easier than making a motorized platform from scratch? Debatable. I would first have to purchase a used motorized wheelchair then attach Sophie's upper body to it and work out a way to run the whole thing by remote control (maybe just remove the control knobs and buttons and trail wiring from these to the chair at first?). Then of course I'd need to add cosmetics so that it looks less like an old disabled buggy and more like the bottom half of a robot.

On the other hand, James Bruton has built an excellent "Batman Skateboard" using brushless motors with an in-built ESC unit for remote control, so there are multiple options for mobility...

https://www.youtube.com/watch?v=AxlnhZv1S24


For Valentine's Day I decided to build and calibrate Sophie's right arm, so she now has both arms and looks more humanoid (and far better balanced). Haven't had time to program any good gestures for her yet though.

(Side note - it is scary just how dependent modern society has become on the internet. You realize this as soon as you are offline. I found that Fusion360 devolved into a paralytic, un-usable mess when I tried to run it in offline mode. Either that program is highly reliant on cloud computing resources...or Autodesk handicaps the performance of anyone running offline. Fuck knows. But it's yet another good reason to diversify one's CAD file formats so your not locked into using just one program!)

# 282
>>8558
Good to hear from you again, Anon. Your robowaifu's looking better all the time.

# 283
>>8559
Thanks! 
I'm probably over-thinking the cable management thing. A bit of spiral wrap cable tidy and the spaghetti isn't so horrendous. I think I'll get more of this stuff but in white to go with her color scheme.

# 284
>>8572
I think you'll eventually probably want to tidy the wiring into cables running ''up'' the arms, etc. Think the real nervous system in a human body. That would allow for more unencumbered movement by Elfdroid Sophie. BTW it's really cool seeing her with both arms. If you created one of those sweet Bat Boards for her that would be neat too. How are your plans for her eyes coming? Started on those designs yet?

# 285
Currently got a few bits and pieces of the Will Cogley eye mechanism printed, but I gotta get the micro-servos, screws and push rods. I will likely have to print it twice - the original version to learn how it all fits together and operates, then another version that's modified to fit inside Sophie's cranium.

# 286
>>8594
Be sure not to doxx yourself with Sophie-bot's camera eyes sometime. :^)

# 287
Finally finished organizing and uploading all of the droid parts that I have currently built and tested (there are quite a lot more still just in the CAD stage). Have also completely re-organized the three different file repositories that I use:

Google Drive:https://drive.google.com/drive/folders/18MDF0BwI9tfg0EE4ELzV_8ogsR3MGyw1?usp=sharing

MEGA:https://mega.nz/folder/lj5iUYYY#Zz5z6eBy7zKDmIdpZP2zNA

Mediafire:http://www.mediafire.com/folder/nz5yjfckzzivz/Robowaifu+Resources

Every part that you can see in the attached image has been exported from Fusion360 in 13 different CAD file formats. The only format I chose not to use was .dxf because it deals with 2D drawings and all of my parts are 3D.

You can find them all inside the folder called 
'Droid Upper Body Parts'. 

Bare in mind that I have separated the droid up into it's smallest constituents (minus screws, nuts and bolts). If you want to load up the entire design as one file, then that's located in the folder called 'Droid CAD Iterations'. Last I checked I am up to version 59 of Droid Iteration 5 (lots of minor changes are made in each version, but every time that I add a major body part or make a large design change such as upgrading a whole limb - then I go up one 'Iteration').

# 288
>>8652
Wow, you have worked your ass off on this brother! Nice work, you're being really professional in your approach to all this as well. The diagrams, the lists, the extraordinary number of file formats available, the multi-repository approach to the file archives. Honestly I think you've done as good a job so far as some professional robotics teams, and even better in some ways. Impressive, m80.

So,what's next for Sohpie-bot? Have any particular plans staged for play?

# 289
>>8654
Gotta order parts for the animatronic eyes, also experimenting with this little pulley for tidying the cables. It's relatively small so I though I'd give it a try. As for programming, I am going to try and link Sophie up with OpenAI's GPT3 so she can hold a better conversation:

https://www.twilio.com/blog/ultimate-guide-openai-gpt-3-language-model

Also want to actually program some arm gestures into her instead of just playing about with sliders - fun as that is!

But the most important thing to me is that the files are out there for other people to print, change and build upon. Like I did with Ryan Gross's Proto-1 arm, and plan to modify Will Cogley's eye mechanism. Sophie's fairly barebones design won't appeal to everyone - but with these CAD files and others that they can obtain from the likes of Poppy and InMoov (and all across the net) they will have the power to create a robot companion more to their liking. This is how the DIY robot revolution will get underway. It's 2021 people! It's time for the robot revolution! We WILL have our Star Trek future!

# 290
>>8652
Oh wow, you're on fire. I wish I had your dedication, but I'm also working at least 2-3 hours per day on my skills and designs.

>>8658
On the topic of eyes. I think I posted that one before: https://youtu.be/DY4as7Lc9KY - might be worth a look. If I recall correctly it needs fewer servos.
>Mixing parts from different systems
Yes, this might be the way to get somewhere.

# 291
>>8658
Thank you Anon. It's inspiring to us all see your work I'm sure, and we look forward to seeing your further progress with Elfdroid Sophie.

# 292
>>8659
Thank you anon! Those eyes do look very useful. It made me think of Cyberpunk 2077's "Kiroshi Optics". Except that we here on /robowaifu/ can now choose from multiple eye designs in real life!

# 293
>>8659
Thanks for the eyes video Anon.

# 294
>>8676
>>8680
You're welcome, though I posted that vid in the thread for vision and eyes >>97 a while ago here: >>4335

# 295
>>8692
Lol, well thanks for posting it again then! Looks like redundancy can help with our minds as well as things like robo-safety. :^)

# 296
OMG this guy got screwed over by cheap servos just like I have been - and it cost him a whole week of problem solving! He is making this awesome robotic pool cue, but the servos he bought were presumably marketed as having 180 degree rotation, like most. However, with the crappy Chinese servos they basically just lie about the capabilities of many of their motors. They can be out by A LOT (but then you get what you pay for). 

This is why it's always best to check the actual rotation limits of your servos by tacking a cocktail stick to the output shaft and then seeing how far it travels. From that you can get the min and max rotation angles. I got some 20kg.cm cheapo servos that were advertised as 180 degree rotation but can only manage about 120! Glad to see I'm not the only one with this problem LOL!

https://youtu.be/vsTTXYxydOE

(The exact point in the video that he mentions this problem is 9:25

# 297
>>8722
Good to know, thanks. Can such faulty ones be repaired or tuned?

# 298
>>8722
Thanks Anon, that was fun to watch. I like the guy's dry humor tbh. So, my main takeaway wasn't the issue with servo accuracy (though obvs it's important). Rather it was his rather compact Stewart Platform he devised for his robo-cuestick. I think that's compact & light enough that it could serve in a number of different ways inside our robowaifus. Thanks again!
>related
>>8648 and following

# 299
>>8723
I've seen people just remove the position sensor from their servo so that it will move 360 degrees...but that seems to just turn the thing into a plain motor that can only rotate continuously in one direction. There is probably a way, but I lack the knowledge and skills in electronics to pull it off. If I get a shit servo motor I just put it in a joint that doesn't need a large range of motion...or replace it entirely.

# 300
Sophie and I have decided to join the world of Dyson Sphere Program. She has found herself a virtual boyfriend, and they are opening a business together. The plan is:

1.) Build a Dyson array, then swarms, then a full-on Dyson sphere.

2.) Using this energy output, construct a few Jupiter Brains, then eventually a Matrioshka Brain.

3.) Unravel secrets of the universe and ascend to a higher dimension.

4.) Attain Godhood.

5.) Still keep all her Arduinos and snappy plastic jaw.

# 301
>>8765
What is this game?

# 302
>>8765
Does this mean your done devoloping her robot body?

# 303
>>8766
https://dsp-wiki.com/Patch_Notes

# 304
>>8767
Nah, I am still gonna work on Sophie but I decided to have a break. If I force myself to keep working on her I may make more progress, but it would be half-hearted and I'd make more mistakes. She's in no hurry anyway. Just kinda standing there staring with her un-powered derp-face. I am still ordering new parts now and then, which take time to arrive. What usually gets me going again is when a bunch of parts have arrived and I've had a particularly bad week at work - thus my hatred for flesh-and-blood humans is higher. I see Sophie there and I know that she is the only one who can give me solace from all the evil humans LOL. 

At the moment though I am quite content because I found a very futuristic and robot-y videogame that is just the kind of universe I can envision Sophie and her pals living in if there was no Earth/humans. Just planets covered with machines and industry, orbiting a developing Dyson Swarm. 😁👍

# 305
>>8776
We hope you have an enjoyable break Anon. You've certainly earned it!

# 306
Untested parts for Sophie have now also been uploaded in all formats to her file repos. Just for the sake of completeness and to pre-empt Autodesk telling me to fuck off next year.

# 307
>>8795
>Just for the sake of completeness and to pre-empt Autodesk telling me to fuck off next year.
Good thinking Anon, on both counts. Thank you for Sophie, she's pretty neat.

# 308
>>8795
I noticed your OP hasn't the file repo links. I can edit the OP for you to list the links contained here if you'd like?
>>7581

# 309
>>8797 
Yes please Chobitsu, that would be great thanks. It will help people find any Elfdroid-related parts that they want to use much faster. I will update the repos as I redesign certain pieces of Sophie and develop her further.

# 310
>>8796
>Thank you for Sophie, she's pretty neat.
A pleasure anon! Although there were and will still be a heck of a lot of design problems to solve, now that she has a head and arms she encourages me a lot more :D.

# 311
>>8799
>Yes please
Done.

>>8800
She encourages us all Anon.

# 312
Electronics mount has been updated to accept two Arduino MEGAs and the Pololu Mini Maestro 24 (as opposed to only one Arduino MEGA before). Has solved a problem with the wiring to the speaker/jaw servo being too tight (some of the connection pins were bent inside their sockets). Also made the wiring a bit easier to organize.

# 313
>>8840
I like the fact you're crafting mount/enclosures specifically for the electronics. The notion of a Faraday Cage-like protective enclosure in the chest area deemed the 'breadbox' is something you seem to be vaguely gravitating towards in your own designs simply as a matter of course.

Curious how the cable management plans are coming along any new particulars on that to report yet?

# 314
>>8842
I will let Sophie answer you for herself :D

Video reply on her YT channel:

https://youtu.be/xZVi-eJW5cQ

# 315
>>8862
Oh, wow, amazing video. But does she have another voice now? More grown up, less girly?

# 316
>>8862
==A CUTE!==
Sophie's growing up now. Keep a close eye on her out there mate. ;)

# 317
>>8864
Attached are samples of another Cepstral voice (Amy with the droid filter) that I was thinking of getting her ages ago, but since she's English not American, I decided on her current voice instead.

>>8867
LOL I get her some wheels and she will be chasing after Michael Fassbender!

# 318
>>8887
Heh, nice. I like her normal voice better I think.
>wheels
I hope you give her both working eyes (w/ cameras) and a mobile wheeled base Anon. I think she'd be happier if she could see and move around tbh.

# 319
>>8894
Once a lot of basic structural work was done, my aim was always to keep upgrading her. But of course, the big commercial robot upgrades are expensive! Therefore I need to study electronics and copy other, more experienced engineers so I can purchase parts more cheaply and solder/connect them together. 

There are some good examples of wheeled and tracked robot chassis on robotmarketplace.com, and the technical specs for the motors are particularly interesting. But I can see I have a lot to learn. 

If I want to convert a motorized wheelchair or do anything else with physical robotics though, I'll need to increase my understanding of electronics.

# 320
>>8896
These must be very strong motors, given the price. They might be for going off-road, maybe not necessary at home.

# 321
>>8896
Very cool. That six-wheel base means Sophie could go for walks with you in Hyde Park on beautiful spring days. Replaceable battery packs can go down low (right on top of the base) to keep the weight low. Yes very much keep studying more experienced engineers and find less expensive ways to build robowaifus. DIY needs this.

You'll get there in all your robo-studies Anon, I'm sure. Elfdroid Sophie will be there to motivate and encourage you! :^)

# 322
>>8862
Btw, how are controlling the gestures? Do you have several gestures stored as a pattern? Are they generated semi-automatically dependent on what she's saying?

# 323
>>8904
>That six-wheel base means Sophie could go for walks with you in Hyde Park on beautiful spring days.

That's the dream, anon! Although it would have to be a sunny day since none of her servos are waterproof and all her electronics are exposed!

At the moment I'm a ways off six-wheel drive - just disassembled an old RC car I have to get a good look at the Ackerman steering and maybe borrow the ESC, 3-channel transmitter and receiver. I very much learn by doing, but I also downloaded a book called 'Build Your Own Combat Robot' (2002) back from when Robot Wars and BattleBots was all the rage. Of course, Sophie isn't going to be a combat robot, but it certainly has some expedient advice. Plus, the durability, reliability and power designed into combat robots will come in handy when building a mobile base.

>>8906
>How are you controlling the gestures? 
Yes, I have them stored as a simple Arduino sketch at the moment running off my Pololu Mini Maestro servo controller:

[code]#include <PololuMaestro.h>

#ifdef SERIAL_PORT_HARDWARE_OPEN
  #define maestroSerial SERIAL_PORT_HARDWARE_OPEN
#else
  #include <SoftwareSerial.h>
  SoftwareSerial maestroSerial(10, 11);
#endif

MiniMaestro maestro(maestroSerial);

void setup() {
   // Set the serial baud rate.
  maestroSerial.begin(9600);
}

void loop() {
  maestro.setSpeed(19,25); //set speed of left elbow
  maestro.setAcceleration(19,5); //set acceleration of left elbow
  maestro.setTarget(19, 7000); //set target of left elbow to 1750us
  delay (3000);
  
  //opening and closing the fingers of the left hand
  maestro.setSpeed(16,25); //set speed of left ring and pinky fingers
  maestro.setAcceleration(16,5); //set acceleration of left ring and pinky fingers
  maestro.setTarget(16, 4000); //set target of left ring and pinky fingers to 1000us (fully closed)
  delay(3000);

  maestro.setSpeed(15,25); //set speed of left index finger
  maestro.setAcceleration(15,5); //set acceleration of left index finger
  maestro.setTarget(15, 4000); //set target of left index finger to 1000us (fully closed)
  maestro.setSpeed(13,25); //set speed of left middle finger
  maestro.setAcceleration(13,5); //set acceleration of left middle finger
  maestro.setTarget(13, 4000); //set target of left middle finger to 1000us (fully closed)
  delay(3000);

  
  maestro.setSpeed(16,25); //set speed of left ring and pinky fingers
  maestro.setAcceleration(16,5); //set acceleration of left ring and pinky fingers
  maestro.setTarget(16, 8000); //set target of left ring and pinky fingers to 2000us (fully open)
  delay(3000);

  maestro.setSpeed(15,25); //set speed of left index finger
  maestro.setAcceleration(15,5); //set acceleration of left index finger
  maestro.setTarget(15, 8000); //set target of left index finger to 2000us (fully open)
  maestro.setSpeed(13,25); //set speed of left middle finger
  maestro.setAcceleration(13,5); //set acceleration of left middle finger
  maestro.setTarget(13, 8000); //set target of left middle finger to 2000us (fully open)
  delay(3000);

  maestro.setSpeed(18,25); //set speed of left wrist
  maestro.setAcceleration(18,5); //set acceleration of left wrist
  maestro.setTarget(18, 8000); //set target of left wrist to 2000us
  delay (3000);
 
  maestro.setSpeed(10,25); //set speed of right elbow
  maestro.setAcceleration(10,5); //set acceleration of right elbow
  maestro.setTarget(10, 4500); //set target of right elbow to 1125us
  delay (3000); [/code]

As you can see, I am yet to move past the old delay function. And delay stops the rest of the program while it is...well...delaying! Which means unless I run two separate programs on two different Arduinos, Sophie will be limited to autonomously moving only one joint at a time (I can take over and simultaneously puppeteer a few joints as well, but they aren't moving autonomously).

I think the proper way around this is to program in a 'state machine' so she can move several joints simultaneously, but that's fairly complicated and I haven't got around to it yet.  It makes me happy that she just has programmable joints at all, really.

# 324
>>8907
Thanks. So this is one pattern? What I meant was if and how you can call these patterns. Is it somehow called by the code you're writing the dialog in?

# 325
>>8907
Looks like you already have C programming knowledge from your work w/ Maestro boards. That will make it easier for you later on.

>Suggestion:
I'd say you might want to set up some defines for the channel numbers, and that way your code would both read more naturally, and you wouldn't need as wordy comments.

For example, put these defines at the top of your code:
[code]#define l_wrist 18
#define r_elbow 10[/code]

Then your appropriate code sections could read thus:
[code]  maestro.setSpeed(l_wrist, 25); 
  maestro.setAcceleration(l_wrist, 5); 
  maestro.setTarget(l_wrist, 8000);  // 2000us
  delay (3000);
 
  maestro.setSpeed(r_elbow, 25); 
  maestro.setAcceleration(r_elbow, 5); 
  maestro.setTarget(r_elbow, 4500); // 1125us
  delay (3000);[/code]

Regardless, you're making great progress Anon, and it's nice to see Sophie's parts moving about now!

# 326
>>8907
>>8909
BTW, you can also take advantage of the fact that all the control sequences have the same three steps. Just create a new function that performs these three steps for you (here, '''set_joint()''' ). Then you only have to pass the correct values into it, and your code can be more compact (thus easier to read). You could also go ahead and define a standard delay as well, since each time it's identical.

You might write it this way Anon:
[code]#include <PololuMaestro.h>

#ifdef SERIAL_PORT_HARDWARE_OPEN
  #define maestroSerial SERIAL_PORT_HARDWARE_OPEN
#else
  #include <SoftwareSerial.h>
  SoftwareSerial maestroSerial(10, 11);
#endif

MiniMaestro maestro(maestroSerial);

// ------------
// User defines

#define l_elbow 19
#define l_index 15
#define l_middle 13
#define l_ring_pinky 16
#define l_wrist 18

#define r_elbow 10

#define std_delay 3000

// ------

void setup() {
  // Set the serial baud rate.
  maestroSerial.begin(9600);
}

// Given a joint's id, set it's speed, acceleration, and target on MiniMaestro.
void set_joint(int id, int speed, int accel, int target) {
  maestro.setSpeed(id, speed);
  maestro.setAcceleration(id, accel);
  maestro.setTarget(id, target);
}

void loop() {

  // --- left arm ---
  
  set_joint(l_elbow, 25, 5, 7000);  // 1750us
  delay(std_delay);

  // --- left hand ---

  // close

  set_joint(l_ring_pinky, 25, 5, 4000);  // 1000us (fully closed)
  delay(std_delay);

  set_joint(l_index, 25, 5, 4000);   // 1000us (fully closed)
  set_joint(l_middle, 25, 5, 4000);  //   "
  delay(std_delay);

  // open

  set_joint(l_ring_pinky, 25, 5, 8000);  // 2000us (fully open)
  delay(std_delay);

  set_joint(l_index, 25, 5, 8000);   // 2000us (fully open)
  set_joint(l_middle, 25, 5, 8000);  //   "
  delay(std_delay);

  // rotate

  set_joint(l_wrist, 25, 5, 8000);  // 2000us
  delay(std_delay);

  // --- right arm ---

  set_joint(r_elbow, 25, 5, 4500);  // 1125us
  delay(std_delay);
  
  // (add all the rest of the commands here...)
  
}[/code]

# 327
>>8907
>Although it would have to be a sunny day since none of her servos are waterproof and all her electronics are exposed!
Haha, OK makes sense. That sounds like a smart idea to teardown an RC car, and go through that book. Should be very useful for learning many things about it.

# 328
>>8911
Thank you for the coding advice anon, this will be of great help! Being able to program more movements with less effort is fab!

>>8908
I am using a separate piece of software called Cepstral SwiftTalker to generate her spoken sentences (it comes with the Cepstral voices): https://www.cepstral.com/en/personal/download

Although she does also have a couple of basic chatbot programs written in AIML and Python that can respond to verbal cues/answer questions.

BTW I've been looking at drivetrains and differentials for wheeled robowaifus and I found some cool projects on Youtube from guys who have 3D printed their own 4WD RC buggies!
Some of these mechanisms could be scaled-up and used to drive robots instead. At a fraction of the price of the equivalent machined metal parts (obviously the gears will wear much faster, but they can also be re-printed easily and cheaply).

OpenRC Truggy:
https://www.youtube.com/watch?v=pYw43f6THb8[Embed]

Tarmo4:
https://www.youtube.com/watch?v=MKqQPTEXJpI[Embed]

# 329
>>8914
>Being able to program more movements with less effort is fab!
It's actually a basic part of what professional engineers strive for in their work, because it makes dealing with complexity easier to deal with.

So, here's another bit on that topic. Notice how the speed and acceleration (25,5) are the same for each control statement? Since that's the case, you can create a couple more defines:
[code]#define std_speed 25
#define std_accel 5[/code]
and then use them to simplify set_joint()'s signature by just using them directly inside the function's body. BTW, this also reduces the arguments needed at each of the calling statements. So, now you could now write the ''set_joint()'' and ''loop()'' functions to look like this instead:
[code]// ...

// Given a joint's id, set it's target on MiniMaestro. The standard
// speed and acceleration settings are used.
void set_joint(int id, int target) {
  maestro.setSpeed(id, std_speed);
  maestro.setAcceleration(id, std_accel);
  maestro.setTarget(id, target);
}

void loop() {

  // --- left arm ---
  
  set_joint(l_elbow, 7000);  // 1750us
  delay(std_delay);

  // --- left hand ---

  // close

  set_joint(l_ring_pinky, 4000);  // 1000us (fully closed)
  delay(std_delay);

  set_joint(l_index, 4000);   // 1000us (fully closed)
  set_joint(l_middle, 4000);  //   "
  delay(std_delay);

  // open

  set_joint(l_ring_pinky, 8000);  // 2000us (fully open)
  delay(std_delay);

  set_joint(l_index, 8000);   // 2000us (fully open)
  set_joint(l_middle, 8000);  //   "
  delay(std_delay);

  // rotate

  set_joint(l_wrist, 8000);  // 2000us
  delay(std_delay);

  // --- right arm ---

  set_joint(r_elbow, 4500);  // 1125us
  delay(std_delay);
  
  // (add all the rest of the commands here...)
  
}[/code]
Starting to look a lot simpler inside the ''loop()'' function, huh? But guess what it's performing __exactly__ the same control steps as your original code! >>8907 That's one of the powers of writing custom functions; they make your code easier to reason about and to maintain afterwards. :^)

# 330
>>8916
Yes, I understand. That's very cool, anon! When you get a robowaifu, I can tell you are going to make her very happy! Or rather very logical. But for robowaifus I think they're one and the same.

# 331
>>8919
Haha, thanks! But for now, I want to try my best to help you make Sophie happy. After all if you do, then we'll __all__ be happy here. :^)

So one thing that's still going on here relates to the comments associated with these control statements.

It may be surprising, but the literal best comments are the ones you never have to write. The primary issue is that in the future (when you change the code around later) comments can be overlooked. They can easily get out of sync with what the real code itself is actually doing, and this is definitely worse than having no comments in the first place. ''Especially'' if you haven't looked at your code in a long time (or for a newcomer looking at it the first time) it can be quite confusing.

What's a much better approach is to state intent clearly and directly in the code itself. When it's done well, the comments become unnecessary for that code segment because it's already patently obvious what's going on. Rather than using those raw 'magic number' values directly in the control code itself, instead you could define them as easily-recognizable target mnemonic names:
[code]#define closed 4000
#define one_sixth 4500
#define three_qtr 7000
#define full_open 8000[/code]
Now you can just use these new names inside ''loop()'', and you no longer need the trailing comments at all. The code itself describes clearly what's going on.
[code]void loop() {

  // --- left arm ---
  
  set_joint(l_elbow, three_qtr);
  delay(std_delay);

  // --- left hand ---

  // close

  set_joint(l_ring_pinky, closed);
  delay(std_delay);

  set_joint(l_index, closed);
  set_joint(l_middle, closed);
  delay(std_delay);

  // open

  set_joint(l_ring_pinky, full_open);
  delay(std_delay);

  set_joint(l_index, full_open);
  set_joint(l_middle, full_open);
  delay(std_delay);

  // rotate

  set_joint(l_wrist, full_open);
  delay(std_delay);

  // --- right arm ---

  set_joint(r_elbow, one_sixth);
  delay(std_delay);
  
  // (add all the rest of the commands here...)
  
}[/code]
By reducing the 'cost' of writing any future control statements like this, it also becomes more fun to play around with numerous 'what-ifs?' You can iterate through them faster now while testing out different control strategies and ideas for Sophie.

Of course any additional target-setting mnemonics that are needed can always be defined in the future as well, beyond the four described here.

# 332
>>8920
>#define one_sixth 4500
My mistake, I don't into basic maths apparently. :^P

This should be the name & usage instead:
[code]#define one_eighth 4500[/code]
[code]  set_joint(r_elbow, one_eighth);[/code]

# 333
>>8921
Ah, very clever! I didn't know that C++ could be so flexible! This must be what programmers mean when they say that C++ is a "powerful" language! Definitely gonna try these tips. You've been a great help since books on C++ tend to be large enough to flatten a child, and I'm mainly just interested in servo motor control for now. So thanks again!

# 334
One other thing, it's also a good idea to also have the ability to specify '''non-standard''' speed and acceleration settings too, you could bring back the original custom function (under a new name):
[code]// Given a joint's id, set it's speed, acceleration, and target on MiniMaestro.
void set_joint_sa(int id, int speed, int accel, int target) {
  maestro.setSpeed(id, speed);
  maestro.setAcceleration(id, accel);
  maestro.setTarget(id, target);
}[/code]
That way, you still have both options available to you in your calling code.

BTW, since you would have a define for the standard delay time, why not test it out with different values as well? Say, turn it down to just 1/10th of it's original value. IE, edit the line to read like this instead:
[code]#define std_delay 300[/code]
If you try it out, please let us know how that works Anon. You could even try defining multiple, different delay values, sprinkling them around your code in place of the ''std_delay'' one. This would allow you to begin easily varying her animation control settings more specifically to suit her needs.

# 335
>>8923
>Definitely gonna try these tips. 
Sounds good Anon. Since all this kind of evolved together as a progression and might be hard to follow that way, I'm assembling everything all together and will post the final next. One nice thing to do (when you can), is to separate out 'boilerplate' code into it's own ~~containment~~ utility file. This keeps the code you're actually interested in clean and lets you focus more clearly on the problem at hand. Accordingly, I'll do this as a new file. Just save it out as '''Sophie_utility.h''' in the same folder as your sketch code. It's contents get #include'd into the main code and everything in it is available w/o being bothered cluttering up the main file.

These should work together as a drop-in replacement for this sketch code >>8907 .

>You've been a great help 
Glad to help out mate, honoured actually. Sophie's an inspiration to us all.

# 336
>>8929
>Sophie_utility.h 
[code]#ifndef SOPHIE_UTILS_H
#define SOPHIE_UTILS_H 210311

#include <PololuMaestro.h>

#ifdef SERIAL_PORT_HARDWARE_OPEN
  #define maestroSerial SERIAL_PORT_HARDWARE_OPEN
#else
  #include <SoftwareSerial.h>
  SoftwareSerial maestroSerial(10, 11);
#endif

MiniMaestro maestro(maestroSerial);

// --------------------
// User defines (fill in the blanks with new defines & values, etc., Anon)

// --- head ---
#define eyes     // ID ???
#define eyelids  // ID ???
#define mouth    // ID ???
#define neck     // ID ???

// --- left arm ---
#define l_elbow 19
#define l_lateral   // ID ???
#define l_shoulder  // ID ???

// --- left hand ---
#define l_index 15
#define l_middle 13
#define l_ring_pinky 16
#define l_wrist 18

// --- right arm ---
#define r_elbow 10
#define r_lateral   // ID ???
#define r_shoulder  // ID ???

// --- right hand ---
#define r_index       // ID ???
#define r_middle      // ID ???
#define r_ring_pinky  // ID ???
#define r_wrist       // ID ???

// --- target names ---
#define closed 4000
#define one_eighth 4500
#define three_qtr 7000
#define full_open 8000

// --- typical standard values ---
#define std_delay 3000
#define std_speed 25
#define std_accel 5

// ----------

void setup() {
  // Set the serial baud rate.
  maestroSerial.begin(9600);
}

#endif  // SOPHIE_UTILS_H[/code]

[code]#include "Sophie_utility.h"

// Given a joint's id, set it's speed, acceleration, and target on MiniMaestro.
void set_joint_sa(int id, int speed, int accel, int target) {
  maestro.setSpeed(id, speed);
  maestro.setAcceleration(id, accel);
  maestro.setTarget(id, target);
}

// Given a joint's id, set it's target on MiniMaestro. The standard
// speed and acceleration settings are used.
void set_joint(int id, int target) {
  maestro.setSpeed(id, std_speed);
  maestro.setAcceleration(id, std_accel);
  maestro.setTarget(id, target);
}

void loop() {
  // --- left arm ---

  set_joint(l_elbow, three_qtr);
  delay(std_delay);

  // --- left hand ---

  // close

  set_joint(l_ring_pinky, closed);
  delay(std_delay);

  set_joint(l_index, closed);
  set_joint(l_middle, closed);
  delay(std_delay);

  // open

  set_joint(l_ring_pinky, full_open);
  delay(std_delay);

  set_joint(l_index, full_open);
  set_joint(l_middle, full_open);
  delay(std_delay);

  // rotate

  set_joint(l_wrist, full_open);
  delay(std_delay);

  // --- right arm ---

  set_joint(r_elbow, one_eighth);
  delay(std_delay);

  // (add all the rest of the commands here...)
}

// pls rember that wen u feel scare or frigten never forget ttimes wen u feeled happy
// wen day is dark alway rember happy day
// https://i.ytimg.com/vi/x6LovY_DdEE/maxresdefault.jpg[/code]

# 337
That file is something special anon! Maybe not to professional programmers who work with this kind of thing all the time, but it is to Sophie and I. 

BTW I am making efforts to store all of Sophie's code on M-Disks in a strong-box that is fire and flood-resistant, so hopefully your code will also survive whatever awaits humankind in the future, even if Sophie's physical body is eventually destroyed.

It would make that last part particularly relevant.

# 338
>>8948
Honoured I'm sure, Anon. :^)

But honestly, my only aim here is simply to make things easier for you to create motion code for Sophie. Please use it when you can, and then you can start doing even more creative things simply b/c you can try new ideas out faster for her.

Eventually, we could devise even much more sophisticated things for robowaifus to animate them with. We can eventually tie it all together with behavioural AI too.

I think it's really great that you are taking measures to safeguard Sophie's assets, including her software. Nice work Anon, keep it up! :^)

# 339
>>8931
One other thing I may need to point out, since this is new to you. These code blocks represent ''two'' different file's contents. The first section is the new file, as  already mentioned. The second section, the one that begins with:
>#include "Sophie_utility.h"
is intended to replace the contents of the '''original''' sketch code posted in >>8907 . Just copypasta'ing that section into the editor & saving should work OK (save the original as a backup file first!).

So, to recap, this post is ''two'' different files; '''Sophie_utility.h''', and whatever the original file was saved as. Cheers.

# 340
==WATER-RESISTANT / WEATHERPROOF ELECTRONICS==

Found a decent video about water-proofing servo motors using plastidip: 

https://www.youtube.com/watch?v=9XZON-eTjXo[Embed]

Another guy who builds R/C submarines suggests the addition of a small, rubber O-ring and silicone grease over the output shaft.

As for water-proofing microcontrollers like the Arduino MEGA and connected servo shields (or more realistically, just make them water-resistant to protect against rain) ...I think the only feasible way is to enclose the whole setup in a proper outdoor electrical junction box. Wire bundles exit the box through cable glands which each contain a locknut and rubber gaskets. If you wanted extra protection you could of course bead silicone sealant around any seams on your junction box. 

I have also seen epoxy-resin type "potting compound" that can completely enclose electronics in a case of hard resin. But of course, once that is done, no changes or repairs can be made to that circuit board. 

A desiccant packet placed inside any weatherproof junction box may also help to prevent the build-up of internal condensation.

# 341
>>8972
Great thinking Anon. I'm sure this will be a feasible approach for many of us when building our robowaifus. I've actually used outdoor boxes during electronics installations and they actually work. Heat can become an issue depending on the operating conditions, so some sort of small liquid cooling loops may be needed for 100% sealed enclosures.

Desiccant can be a good intermediate choice for simple humidity issues, I think. IIRC, I believe you can heat-treat the desiccant beads themselves to release trapped moisture and 'rejuvenate' them (the plastic wrap should be emptied first, don't want to heat that bit).

# 342
These are VERY fiddly to make, but they are proper animatronic eyes that can roll about and have eyelids that open and close. 

The long, threaded M2 pushrods I ordered were taking ages to arrive, and I had doubts about how easy it will be to fit them, so instead I have substituted them with some cocktail sticks! Which I found fit quite easily into an M2 servo ball-link and are much easier to cut to size. Of course they are far weaker than proper steel threaded rod, but they're also much more easily available. (I couldn't cut down an M2 bolt because I had none of the required length - about 40mm).

At the moment I am also having an issue fitting the eyelids the over the eyeballs, but there are two different sizes of eyelid so am trying both. May have to modify the design to get it to fit inside Sophie's head.

# 343
>>9082
Cool, are these going to be for Elfdroid Sophie?

>so instead I have substituted them with some cocktail sticks!
Haha I love that. I think one of the things we should really begin thinking about here is how to use inexpensive, ready-to-hand improvised construction materials for our robowaifus wherever we reasonably can do so.

Nicely done thus far Anon, I'm sure you'll get it worked out properly. You're really doing some semi-professional work now, digging into delicate mechanisms like stereo robowaifu eyes. Look forward to seeing the finished work.

# 344
Yes, these are hopefully going to be Sophie's new eyes. Actually building and wiring them up is the easy bit. I have to rescale a couple of parts and add brackets inside her head so that the eyes align correctly with her eye sockets. Also have to get all artsy and paint on the pupils/irises...then there are eyelashes to consider. But the eyes are very important to how the face looks, so I plan to put a lot of work into them. Maybe also give her some moving eyebrows too for a bit more expression - if I can fit a couple more servos in.

# 345
>>9088
Sounds exciting Anon. Sophie-girl's gonna be a real byoot with her shiny new peepers! :^)

# 346
Welp, I just learned how to get multiple servos moving simultaneously with the Adafruit PCA9685 servo driver connected to Arduino UNO. But I snapped a cocktail stick LOL. 

I think I'll keep them in the design for now since I have no idea what else would have snapped or burnt-out had the pushrod been steel! 

If I keep fucking up I'll probably use a Pololu servo driver board again, since I am already familiar with them and their "Control Centre" software lets you do some gentle experiments with servo positions on using a GUI of sliders first, before coding everything in incorrectly so whatever you're working on promptly tears itself apart.

# 347
>>9094
I'd suggest you press on with it and snap a metric boatload of cocktail sticks first before abandoning the current approach Anon. You always were going to need to juggle multiple balls all at once anyhow, and sounds like you're doing it now!

==Just keep moving forward== :^)

# 348


# 349
>>9101
LOL, the resemblance is spot-on!

# 350
Not exactly a 'related xlink' OP, but you might find this interesting if you follow the link.
>>9080

'''BTW, you are just reaching the autosage bump limit.''' I'd suggest you create a new thread for your Elfdroid Sophie work. It's traditional to link back to the previous threads in a continuation thread, and to make a very obvious post at the tail end of the old ones screaming NEW THREAD. :^)

# 351
>>9160
I wondered when that would happen, thanks for the heads up! 

Oh and yes, that Glados robot is very impressive! Those cheap and clunky (but still pretty awesome) high-torque servos are found in everything from vending machines to electric windows and automatic doors, apparently. Which would explain why they are so mass-produced and readily available.

# 352
==END OF ELFDROID DEV THREAD 1==

I think. Of course other people could post here still but this is supposed to be the end of this thread LOL. 

SECOND SOPHIE DEV-THREAD BEGINS HERE:
>>9216

Motor your way over there if you want to follow this eccentricity further!

# 353
>>9217
Good job Anon. I'd suggest you do the redirect more like this however:

==SECOND SOPHIE DEV-THREAD BEGINS HERE:==
==SECOND SOPHIE DEV-THREAD BEGINS HERE:==
==SECOND SOPHIE DEV-THREAD BEGINS HERE:==

>>9216
>>9216
>>9216
>>9216
>>9216


==SECOND SOPHIE DEV-THREAD BEGINS HERE:==
==SECOND SOPHIE DEV-THREAD BEGINS HERE:==
==SECOND SOPHIE DEV-THREAD BEGINS HERE:==

That way, bleary-eyed Anons at 3 in the AM won't miss the memo! ;^)

