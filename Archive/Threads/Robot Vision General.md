# 1
'''Cameras, Lenses, Actuators, Control Systems'''

Unless you want to deck out you're waifubot in dark glasses and a white cane, learning about vision systems is a good idea. Please post resources here.

opencv.org/
https://archive.is/7dFuu

github.com/opencv/opencv
https://archive.is/PEFzq

www.robotshop.com/en/cameras-vision-sensors.html
https://archive.is/7ESmt

# 2
>Unless you want to deck out you're waifubot in dark glasses and a white cane
But, OP, what if the model for the waifubot is supposed to be blind? #triggered

# 3
>>97
The inmoov project managed to use the playstation move(?) to give the robot vision, the script is freely available for it. They also use purchasable cameras for the eyes.
inmoov.fr/eye-mechanism.

https://www.invidio.us/watch?v=H4Z09edx52E

# 4
>>1107
KEK

>>1108
That's cool anon thanks. I had planned on using the open sauce version of kinect (Willow Garage) and a couple of hi quality 1080p webcams.

# 5
I just purchased a couple of the JeVois cameras. I plan to try using them on a little moebot. What's neat about them, is the have a dedicated 4-core CPU running Linux and any other vision software like OpenCV right in the camera. This pretty much entirely offloads the vision processing computation from the robowaifu's other onboard processors. Thanks to the anon in other thread for first posting the camera for us.

https://www.invidio.us/watch?v=7cMtD-ef83E

# 6
>>1107
Blindfolded girls a cute.

On topic: a new Google vision kit
www.google.com/amp/s/www.theverge.com/platform/amp/2017/11/30/16720322/google-aiy-vision-kit-raspberry-pi-announce-release

# 7
>>1111
Thanks anon, I'll check it out come New Year. If I feel it doesn't feed their botnet, I'll recommend it. Either way, I'll post back here and let you know what I think about it in roughly a month or so.

>ed. surely anon will deliver...

# 8
facial recognition convo:
[[1129

# 9
Anon linked a nice OpenCV training source:
[[1154

OpenCV tutorial site
[[1161

JeVois camera set up:
[[1163

# 10
https://www.invidio.us/watch?v=BaWostkMClA

# 11
I just found this;
hackaday.com/2018/02/15/student-3d-prints-eyes/

# 12
I'm thinking of using an acrylic light guide / light splitter that reads a single image from a TFT display and duplicates it for two small eyeballs. The eyeballs can be physical, so this will save some logic and wonkiness and I can just focus on making a nice retina pattern; the light guide can be a bunch of optical fibers. Pic is supposed to be a Lego piece, wish there was a better illustration.

# 13
>>1117
Sounds interesting FluffyDev, can't say I really 'get it' specifically just yet, but I am familiar with optical fibers.

# 14
>>1107
>>1111
>>1118
Upon VERY SERIOUS consideration, one-eyed girls may work for our purpose, either temporarily one-eyed or even permanently, since the space behind the other eye can be used for additional electronics and actuators (much needed space especially for a smaller 80cm bot such as mine). A tube guide consisting of either solid plastic tubing or bundled optical fibers and a mirror system will make it possible to have both a real camera vision system as well as fancy pupil/retina graphics. Plus with a physically moving eye, the camera will be able to pan also. (Yes it will be a huge eye mechanism, hence the SERIOUS CONSIDERATION of making the waifu one-eyed on purpose). But she will actually have vision which you can display on the debug computer!

# 15
>>1119
>not just having a leela robowaifu
plebeian pls

# 16
>>1119
Eye patch is beauty

# 17
>>1122

# 18
I'm not really a fan of this eye mechanism since it doesn't support a camera but it could be redesigned to support one. The eyes look pretty good and the process could be adapted to creating anime doll eyes too.

>How to Make Realistic Eyes Using 3D Printing for Animatronic Eye Mechanisms
https://www.youtube.com/watch?v=RqZRKUbA_p0

>How to Build a Simple 3D Printed Arduino Animatronic Eye Mechanism
https://www.youtube.com/watch?v=Ftt9e8xnKE4

# 19
>>1657
Yes, I think I remembered that one from before. I like the face the parts are mostly 3D-printable with a cheap printer. Can probably use a resin-based UV printer for the more precision parts like the eyeballs/lids themselves. I don't see any reason small cameras couldn't be fitted inside the interior globes of the eyeballs anon. Even the Jevois camaeras (that have actual tiny fans on them b/c Linux+OpenCV coprocessor right on board) should work with the half-open design of the eyeball.

# 20
>>1664
>I like the fact*

# 21
>>1657
reminds me of the Robot from Lexx

# 22
Here's one with two cameras and low amount of space: https://youtu.be/DY4as7Lc9KY

My own thinking is, that ideally we should be able to take eyeballs out from the front. The sockets should be expandable four maintenance. If taken out, the servos should be replaceable as well. But then, I'd like my waifu to be waterproof (shower) and she should have tears. So the servos need to be separated with a layer of silicone somehow, maybe they move a magnet and the eyeballs have some metal inside?

# 23
>>4335
>that ideally we should be able to take eyeballs out from the front. The sockets should be expandable four maintenance.

That's a great idea Anon. It will allow for easy upgrading of the cameras, and as the control mechanisms will be moving thousands of times a day (even if only for small distance) affords maintenance access. I propose that the entire assembly be able to slide forward on a tray to afford easy access from most angles.

# 24
>>4337
That sounds good, but it would add more moving parts. Might make sense i n some designs, but I'd prefer to avoid it. Maybe you're thinking of a moe bot with small eyeballs? 
If the eyeballs in a bigger one are quite huge and you can get the eyeball out first, then you would need to cut through some silicone, then getting the servos out should work as well. 
My point is the balls should be held only by the eyesocked (circle) as part of the skull, but if needed it could expand and form a bigger circle.

# 25
>>4335
After thinking about this a bit more, it came to mind that using a magnet connected to the servo  and metal part to the eyeball, while the eyeball is also connected to a cable might not work. I'm concerned that the position of the eyeball couldn't be controlled very well. 
However, I tested it with a hollow flexible ball and a weak magnet (without servo). Now I can imagine it better and I'm more confident. However it might need a automatic re-adjustement mechanism. In case the servo looses connection to the eyeball it might move without the eyeball and then not know where it is.

# 26
>>4341
>That sounds good, but it would add more moving parts.
This is a good example of the basic eye-control mechanism I have in mind:
>>1657 (1st pic)
The access mechanism would simply add a slide-out frame for the entire assembly to rest on.

>then you would need to cut through some silicone,
I would propose a design that had firm plastic 'frames' around the eye sockets, with a clearly-delineated seam that wouldn't require any special treatment to slide the eyes out for access.

# 27
>>4351
Okay, that's different from mine, bc it will probably not be a seamless skin or plastic face on the outside. Which is okay, we need different approaches for every taste and use case.
In such a case you might want to embrace the seams and color the face in different colors, bit like Marvels Nebula for example.

# 28
>>4355
Yeah, maybe a good idea. I'm not a art-designer ''per se'', but I'll dabble around with different styles once my efforts have matured a bit.

# 29
Here's a lot of discussion towards moving eyes, following eyes and blinking eyes.
https://dollforum.com/forum/viewtopic.php?f=6&t=103291
They're having a lot of trouble with space. Putting all kinds of stuff into a skull won't be easy.

I thought about how to get the whole eye movement contraption smaller, thought the eyeballs would need to be bigger than human ones for anime eyes. 
One thing is, using servos as small as possible, not these bulky ones. If we can do it with normal dc motors then those would be even better. Of course, they are not so precise... I also thought I had a good idea, by putting one motor in the quite big eyeball. Problem is, I'd like to have the noise dampened. I also had the idea of using one motor for both eyes before, but human eyes can move independently. However, this does not apply for up/down movement, so we are down to three small motors then. The one in the middle would need to have an axis in both directions. Even better would be if the motors could be a bit deeper in the skull and also being used for something else (just a crude idea yet).

# 30
I just listened to that interview here just by chance, while doing some chores: https://youtu.be/bnsgsPjILyQ - Very fascinating. How image recognition needs to work, so the system can think about it. It's one model that looks for different things in a image. It's inspired by neuroscience. Idea is that perception and cognition can't be disconnected from each other.
Natural signals, segmentation and top down controllability are the keywords, the latter means for example when we're zooming into a picture in our minds.

# 31
>>4541
>Putting all kinds of stuff into a skull won't be easy.
Yeah, I think that's mostly a misguided idea. Trying to bio-mimic absolutely everything that's been so elegantly designed into humans is, well, ''humanly'' impossible. :^)

Better to keep most of the componentry safely protected inside the torso, etc, IMO.

>>4777
>perception and cognition can't be disconnected from each other.
Yeah, that's probably correct. Certainly it seems to ring true with some of the positions Carver Mead suggests for the field of Neuromorphic Computing he basically originated. Much of what we think of as 'cognition' is in fact neurological at a basic level instead of a higher level, and the perceptions are pushed as far out towards the extremity of sensory perception as possible in most the the higher life form's biological systems.

# 32
>>4786
IMHO at least one relevant computer should be in the head, to imitate humans. Also, stuff we have to put into the head isn't only that, but we'll need a lot of mechanisms in general there, so space matters. Think of facial expressions, microphones, speakers (mb in the throat), heating for the skin,  tongue moving around while still leaving some space... Cleaning mechanisms... Okay, this is going OT towards >>9 (face/head general). Further discussion on what to put into the head maybe better there?

# 33
>>4792
Yup, all good points Anon.

# 34
Boards with cameras attached came up in the thread on SBCs, here: >>5705
OAK from OpenCV and a cam from Jevois where the computer is part of the camera. Fascinating, but might be a problem if one wants to put it in eyeballs and also make thouse water proof. OAK seems to be a bit big and the cams from Jevois have aircoolers... On the other hand for development my concerns might be irrelevant, since one can build something with them and replace them later with something smaller and cooler.

The Jevois camera has shutter sensor with inertial measure unit and digital motion unit, gyroscope and all kind of sensors, wow: https://youtu.be/MFGpN_Vp7mg

# 35
Here's a video on eye movement. https://youtu.be/FaC2RXBss2c The human eye has six muscles, it can even roll sideways a bit. However, what always bothered me, is that so many fembot eyes can move independently up and down. I still think this isn't necessary. I'll look for a motor with two axes, for up and down movement.

# 36
>related xpost
>>8659

# 37
Someone with no maths/science background looking to get into openCV or just computer vision in general.
My problem would be that I don't know how to approach the topic. I haven't looked into any code yet, because I want to learn how openCV works first. Though now that I'm typing it out, it does sound stupid to learn how openCV works without looking at the code.
I thought to start by looking into the various algorithms but I hardly found any on DDG. Found this one site: https://www.upgrad.com/blog/computer-vision-algorithms/ but the more I look into the unknown terms, the more I went down a rabbit hole of unknown math terms. How do you guys recommend I get started with openCV? Should I only tackle algorithms when I see/need them in youtube tutorials I watch? What are some great resources to help get into openCV? I don't want to turn into a code monkey who only copies and pastes code to get their CV project working...

# 38
>>9296
I wanted to let you know I saw your post, and I'll attempt an answer suited to it. But that will be a while till I can. In the meantime, mind giving us a little better idea of both your experiences & level in technical work & programming? Do you know C++ already for example? Also, do you already have some small cameras or mobile platforms available, say like an RC car or something?

It's OK if you don't have any of this stuff. You can get by without any at the beginning. But letting us know your situation will assist us with giving you a better answer.

# 39
>>9296
OK, the obvious first step is simply to get your news ''straight from the horse's mouth'' Anon.
https://web.archive.org/web/20210308213203/https://docs.opencv.org/master/

There are tutorials there that will get you up and running quickly. The library's software is written in the C++ programming language. So, if you really want to dig into their system as an engineer, then I'd recommend you take that path through both the tutorials and the codebase. This will help you with gaining a deeper understanding of the library itself if you do.
https://github.com/opencv/opencv
Additionally, if you choose this path, then I can also be of more assistance to you here since I have some experience both with C++, and with using OpenCV in the context of C++ engineering aimed at some basic image processing tasks.

OTOH, if your intent is more as a hobbyist simply exploring the ideas for CV that are out there, then there are both Python & JS tutorial pathways as well. I'm pretty sure Java is supported as well. The API of the system are quite similar for all the languages. The basic, fundamental idea to get your head around to start with is that OpenCV treats images as a big matrix (as in, the linear algebra matrix) of data. All image-processing operations orbit around this fundamental paradigm. Get your head around that notion from the beginning, and the rest of the library can quickly come into focus for you.

Given your post, it sounds like perhaps you are just trying to get your head around the general field itself for the time being. In that case, you can just keep scouring the Internet for general articles, various forum posts, all the other imageboards like /robowaifu/ **that's a joke BTW :^)**, blogs, and various YT feeds. There are also many scientific papers on the subject. Eventually you'll get the hang of it Anon.

So it kind of depends on both your experience level and where you want to go with this as to what I'd suggest to you here Anon. Others here may have alternate perspectives they might choose to share with you.

>===
-''various prose edits''

# 40
>>9297
>experiences & level in technical work & programming?
Not much I'd say. Been using python for little over a year learning/doing web scraping and GUI building (with pyqt5).
>Do you know C++ already?
I forgot to mention but I was referring to openCV in python, would I still need to know C++ for that? I did go from C++ to python so its not completely unknown to me.
>do you already have some small cameras or mobile platforms available?
The only thing I have is a USB webcam.
>>9298
I'd say my intent is more as a hobbyist. I just want to create programs for myself right now.
>trying to get your head around the general field itself for now.
Yeah. I guess as with anything, patience is the key.
Thanks, anon.

# 41
>>9312
OK, that's all fine. Python and a webcam is just fine. I'd suggest you simply work through getting the system installed now, and working through all the Python tutorials. You can use some of them with your camera as well.
https://web.archive.org/web/20201102214056/https://docs.opencv.org/master/d6/d00/tutorial_py_root.html

Once you've worked through that as far as you can, then I would advise you to take a break from it all for a bit and then reconsider what you've learned and where you want to go next.

I wasn't exactly clear yet Anon; do you think you're wanting to make your own robowaifu eventually?

# 42
>>9316
Thanks for the advice, anon.
>do you think you're wanting to make your own robowaifu eventually?
Yes.

# 43
>>9317
YW, and glad to hear it. Good luck with your robowaifu's design Anon!

# 44
Trying to do some computer vision experiments/projects on python with my xbox 360 kinect. Installed/built freenect module via https://github.com/OpenKinect/libfreenect and https://github.com/amiller/libfreenect-goodies. However, I can't seem to find any documentation on what functions it has or what one can do with it. All I have are the example scripts in those github repos. Is there any documentation or guides on this?

# 45
>>9793
>Is there any documentation or guides on this?
I haven't looked into this yet Anon, but Willow Garage (of OpenCV, etc. fame) had the original open-sauce libraries surrounding 360 Kinect et al cameras for stereoscopy. You might research these venues for more information, if not documentation on your particular setup.

# 46
>>9795
I see. Thanks Anon, I'll look into Willow Garage.

# 47
>>9296
A wall has been hit! Doesn't look like I'll get past contours https://web.archive.org/web/20201102214056/https://docs.opencv.org/master/d6/d00/tutorial_py_root.html in the image processing sub-topic or any other sub-topic after without knowledge in mathematics. What do I need to get a deep understanding of to move forward with computer vision (and machine learning)? Apart from the obvious linear algebra, of course. Who would've thought, making fun of math classes back in school was ''not'' the way to go.

# 48
>>9970
Correction: I can move forward without math knowledge but it will limit my understanding to just knowing what the code does. I wont have any idea ''how'' the code does what it does.

# 49
>>9970
I don't know what exactly you need, but there are YouTube lessions, Coursera (also as Torrents) and the Brilliant app.

# 50
>>9971
>I wont have any idea how the code does what it does.
I hesitate to encourage you in this one way or other beyond what I've already done ITT:
>>9298
>So, if you really want to dig into their system as an engineer, then I'd recommend you take that path through both the tutorials and the codebase. This will help you with gaining a deeper understanding of the library itself if you do.

However, I'm well aware that can be a literally years-long process, with no guarantees of success. The journey ''itself'' has plenty of rewards IMO
>

One of the basic lessons to learn early in life -- particularly in an engineering/design life -- is:
==Keep moving forward.==

That's it. Just don't quit Anon. Very likely if you can imagine something, then it can actually be done. No guarantees how long or short the journey to success may turn out to be however. This depends in large part on yourself, and the groundwork of effort you've already laid for/in yourself.

Keep looking for another way past that mountain Anon. Over, under, around, or '''through''' ... you can make it! And as far as creating your own robowaifus goes, you could do worse than making your way here to our board. You're already a bit ahead of the game in that regard, Anon.

Now, with that out of the way **:^)**, can you clarify a bit more?
>''contours''
and the link you provided have a bit of a disconnect. What about 'contours' is your current problem, can you explain specifically?

# 51
>>9976
>and the link you provided have a bit of a disconnect. What about 'contours' is your current problem, can you explain specifically?
>'''UD:'''
I presume this is the link of interest here, Anon?
https://web.archive.org/web/20201028001740/https://docs.opencv.org/master/d3/d05/tutorial_py_table_of_contents_contours.html

# 52
I just want to summarize my observations so far regarding this topic.  I've been looking at various self-driving robot/rc car projects by students on youtube.  They usually fall into the following:

1. Raspberry Pi + OpenCV.   The video from the camera has to be segmented... i.e. turned into grayscale, edge-detected, and lane markers drawn.  You then just need to draw a line right through the center of the road, that will be the steering vector which you then command the steering servo.  I haven't touched OpenCV yet though, and I might just bypass the raspberry pi entirely since the trend is to use Nvidia Jetson boards now which have their own preinstalled things.

2. Nvidia Jetson (Nano or other boards).  There's the Jetracer:  https://github.com/NVIDIA-AI-IOT/jetracer  which comes with its own precompiled software as a Jetcard image.  (I was able to secure a TT02 chassis for only 90 bucks, it's going to be delivered any day now so i can't wait to start on this.  I find it easier to customize hobby kits as you're building it rather than risk destroying a ready to run with irreversible changes.)

Now does this apply to robowaifus?  Well if she is on wheels at least, the steering vector would be fed into a differential H-bridge DC motor driver.

Now that's just one side of robot vision -- the ability to navigate.  How about FPV?  Though I don't have a drone (I don't want to start a hobby where EVERYTHING comes from China, unlike RC cars at least), I've been looking at various FPV setups.  They usually go like this:

1. 1000TVL type of analog FPV camera + OSD (onscreen display board, usually based on MAX7456) + VTX (video transmitter, usually an Eachine or whatever is compatible with the 5.8Ghz headset).  So yeah, apparently analog is still applicable since it has low latency.  If you want to record video, best practice is to just attach a second HD lens and make sure it is pointing at the same direction as the analog camera, they usually call this hybrid cameras.

2.  Wifi FPV -- I actually tried this with my RC cars, it's blegh... you would have to drive really, really slow for it to be usable, but for slow H-bridge DC motor robots it would be perfect.  The advantage is that if you are viewing through a high spec machine such as a laptop you can have a fancy overlay for your onscreen display (cue the awesome video game style HUDs) and just record your stream directly to your disk.

So first I have to actually make one of those self driving robots, then I can prove if its practical to just use the camera input (usually a raspberry pi class of camera), Y-split that into an FPV feed and a navigation feed.  The navigation feed will be turned into grayscale or color segmented blocks and lines, while the FPV feed will be wi-fied to the client machine which will handle most of the OSD processing.

# 53
Oh by the way, a few weeks back I was looking at the cheapest way to get into camera robots.  Apparently an ESP32 has just barely enough capability to capture and stream images, previously they paired discrete ESP32s with OV-series basic cameras, until they decided to directly sell combos such as this ESP32-cam.  It is too slow to be used for RC-speed vehicles, but for slow indoor robots such as this:

https://github.com/gitnabeshin/ESP32CamRobot

it is fine.

I'm posting this since it's what go my feet wet with non-AI computer vision and control, so now I have enough confidence to actually try
AI self-driving as the next step.

# 54
>>9973
Didn't know brilliant was free.
Well there ''are'' YouTube lessons and such but I don't know what I need to look up the YouTube lessons for. I've been following 3blue1brown and MyWhyU for lessons in linear algebra. Guess I'll just have to cover the math topics when they appear in the way to learning OpenCV.
>>9979
Yeah, that's the link. More specifically, this is where my confusions started: https://web.archive.org/web/20201031223524/https://docs.opencv.org/master/dd/d49/tutorial_py_contour_features.html
>>9976
Everything past the contours section in the "Image processing with OpenCV" sub-topic in https://web.archive.org/web/20201102214056/https://docs.opencv.org/master/d6/d00/tutorial_py_root.html and all the other sub-topics past "Image processing with OpenCV" (i.e. Feature Detection and Description, and onwards) seem to explain their workings in mathematical terms with formulae I have no hopes of understanding right now.
>What about 'contours' is your current problem, can you explain specifically?
I don't know what "moments" (which seems to be a math derived term) of an image are. And nor am I understanding what ```cpp
cv.Moments()``` returns.
**That's an inspirational image!**

# 55
>>10018
>>10019
Quality information, thank you Anon.

>>10021
>I don't know what "moments" (which seems to be a math derived term) of an image are. 
It's just a ~~ab~~re-use of the idea of 'moments' from physics (cf. >>9887, et al). In that context a 'moment' is kind of a calculus notion, and can be thought of as sort of an instantaneous 'snapshot' or ''moment'' of the rate of change in something. In the physics context the implication is that it's a description of some particular force being imparted by the inertia of some particular mass under consideration.

This ~~ab~~re-use of this term by OpenCV devs is simply that there are 'rates-of-change' types of things going on in an image (for example, it's ''contour'' lines) that you would want to track. For example the rate of change of brightness of pixels in a given direction forms a 'contour' of that change, kind of like a contour map in geography typically describes the changes in elevation for instance. Make sense?
https://www.quora.com/What-exactly-are-moments-in-OpenCV?share=1

>And nor am I understanding what cv.Moments() returns.
Well remember how I said all image data (and practically every other form of data) in OpenCV is a big matrix? Well, that's what gets returned. A set of matrices describing contour characteristics of that input image, etc.
https://web.archive.org/web/20170815042506/http://docs.opencv.org/master/d8/d23/classcv_1_1Moments.html

# 56
>>10018 >>10019
Yes, this is good to know. Thanks.

>>10021
Using the Brilliant app isn't free, or wasn't last time I checked. Only the introduction. To access everything it did cost 60-80€ per year. 
In general, when I get stuck at something, I'll look into other sources of information. Reddit isn't popular on image boards, but having an account there, completely focused on learning stuff und asking around on tech questions might be a good idea. I'm also sure there are good videos on YouTube on OpenCV and tutorials on the net which are even related to using it with Raspberry Pi.

>>10023
Not the anon asking, but this was interesting to me as well. Thanks.

# 57
Since we don't have some kind of general ''Robowaifu Sensornets'' or something like it yet, I'm just going to drop this here since it's probably the closest thing we have atm.

So, a newly-reported spying mechanism invented to keep all the population under close, real-time surveillance via their goyphones uses bat-like echolocation to synthesize an environment's image data. Including the people and pets in it.

While they themselves mean it purely for evil purposes (George Orwell's ''Telescreens'' spying system, but mobile & no need for a fixed camera), perhaps we can in fact use the same technology approach for good? I expect this can certainly enhance a robowaifu's realtime situational awareness capabilities?

https://web.archive.org/web/20210501015028/https://www.dailymail.co.uk/sciencetech/article-9525529/Scientists-equip-smartphones-bat-sense-technology-generate-images-sound.html

# 58
>>10217
Paper is titled, "3D imaging from multipath temporal echoes" for anyone interested.
PDF available:
https://arxiv.org/abs/2011.09284

# 59
>>10630
Briefly skimming the paper, they seem to use a 3D camera to collect training data (like a Kinect, but more expensive), whilst the actual sensor for the acoustic system consists of a stock-standard Logitech PC speaker, and a microphone. Echos are recorded, passed into a network which reconstructs a depth map. All-in-all, it's a super simple system to replicate, and one that could easily be made for almost no cost, and very compact.

Creating training data might be a pain, but given that I already have a Kinect, I'd be happy to volunteer to rig up a Kinect+Pi+mic+speaker and just walk around my local area collecting huge amounts of data.

Let me know if anyone's interested. I'll probably do it myself anyway, but if there's any specific areas you'd like data for, write it down and I'll see what I can do.

# 60
>>10630
>>10631
Wow, great work Anon. Much appreciated.

>Let me know if anyone's interested.
I'm certainly interested to know about your results, though I don't have any personal requests ATM. 

>Kinect
Hmm. Hasn't that product been discontinued now? I wonder what good alternatives exist for us today if any?

>PDF available
Always a good idea to archive a copy here on the board for access in case anything is ever pulled in the future.
>

# 61
>>10632
I suggested the Kinect because it's the most common consumer level depth camera, and I already have one. Any 3D camera can be used, as long as you can get a depth map image from it.

Regarding alternatives, they use an Intel Realsense D435, but that's about $300 new. Even at that price, it's still considered one of the cheaper depth cameras.

Note that the 3D camera is only needed for training data collection. Once you've got your data, the system only requires a directional speaker (i.e a standard speaker), and a microphone. In theory, you could probably use the voice speaker + ears of the robowaifu, but you'd want to tweak your training data if you did.

# 62
>>10633
There are some other options: 
JeVois: https://youtu.be/MFGpN_Vp7mg
eYs3D: https://youtu.be/NXWHYH0v638
e-con: https://youtu.be/vzXzz7VmWzo
SceneScan from Nerian: https://youtu.be/mJ5UlXNguvg
SP1 from Nerian: https://youtu.be/vVVjFqUkG4E
Cadence: https://youtu.be/wPxi4ZYSJC0
Stereolabs ZED: https://youtu.be/7_8XLI99dno

This here is software, trying to do depth perception on any camera:
KudanSLAM: https://youtu.be/Pgami8jglmE

# 63
>>10646
Thanks for the work Anon.

# 64
>'''NIKKOR Lens Simulator'''
https://imaging.nikon.com/lineup/lens/simulator/
An interesting utility the fine Anons on /p/ mentioned.

# 65
>related crosslink (>>10645, ...)

# 66
M-LSD: Towards Light-weight and Real-time Line Segment Detection: https://github.com/navervision/mlsd

You Only Look at One Sequence
https://github.com/hustvl/YOLOS
>TL;DR: We study the transferability of the vanilla ViT pre-trained on mid-sized ImageNet-1k to the more challenging COCO object detection benchmark.
>Directly inherited from ViT (DeiT), YOLOS is not designed to be yet another high-performance object detector, but to unveil the versatility and transferability of Transformer from image recognition to object detection.

CLIP (Contrastive Language-Image Pre-Training)
https://github.com/openai/CLIP
> CLIP is a neural network trained on a variety of (image, text) pairs. It can be instructed in natural language to predict the most relevant text snippet, given an image, without directly optimizing for the task, similarly to the zero-shot capabilities of GPT-2 and >3. We found CLIP matches the performance of the original ResNet50 on ImageNet “zero-shot” without using any of the original 1.28M labeled examples, overcoming several major challenges in computer vision.

Dynamic Vision Transformer (DVT)
>We develop a Dynamic Vision Transformer (DVT) to automatically configure a proper number of tokens for each individual image, leading to a significant improvement in computational efficiency, both theoretically and empirically.
https://github.com/blackfeather-wang/Dynamic-Vision-Transformer

# 67
>>10759
> Towards Light-weight and Real-time Line Segment Detection
< Light-weight '''and''' Real-time
Well I certainly find that combination of terms very encouraging Anon. Simply b/c that's the __only__ combination that's going to be successful for devising reasonably inexpensive, mobile, autonomous gynoid companions robots. AKA ''robowaifus''.

It's gratifying seeing a small cadre of researchers seeming to be breaking off from the standard-issue Globohomo toadies, and tackling the real-world concerns of the billions of regular people, regarding AI advancement at the personal level.

>tl;dr
We'll never achieve an AI/Robowaifu Renaissance if we every one have to be beholden to the Globohomo cloud, hat in hand, begging ''"Please sir, may I have some more?"''

# 68
>>10761
test

# 69
Found this reference image that is used by 'Ocularists' who paint glass eyes/ocular prosthesis. Might help some anon who is trying to paint their robowaifu a pair of pretty peepers. 

A note about eye lighting/refractive highlights:
Despite what anime has taught us, I think it may be best not to paint on any lighting effects/refractive highlights (at least on non-cartoon irises). The highlights are best formed by a coating of clear epoxy resin. I say this because such refractive highlights move throughout the lens of the eye and across the surface of the sclera. So if they are painted on, they will be static...and this just looks wrong. Especially if the eye is also coated in clear resin. Because then you have the natural light reflected off the resin along with the static painted highlights.

I think this is why Will Cogley leaves a concave depression inside his eye mold so that clear epoxy resin can set inside and form a lens shape, which reflects and refracts the light just like a real eye.

Some measurements: (from the Wikipedia article on the human eyeball, and a scientific paper on the human iris).

Human eyeball average height = 23.7mm (0.93 in)

Human eyeball average width = 24.2mm (0.95 in) the eyeball is slightly wider than it is tall - which is why I didn't just give one diameter, but I know for the sake of simplicity that a 25.4mm (1 inch) diameter eyeball looks correct inside a life-sized human head.

Human eyeball average anterior to posterior diameter = 24mm (0.94 in)
This may be less important for a robowaifu since often they only use the front half of the eyeball, with the back/interior being fastened to a servohorn or pushrod in some way.

Human eyeball average volume = 6 cubic centimeters (0.37 cu in)

Iris size range = 10.2 to 13.0 mm in diameter with an average size of 12 mm in diameter, and a circumference of 37 mm.
(From this paper: https://www.di.ubi.pt/~lfbaa/pubs/iscit2013.pdf
'Iris Surface Deformation and Normalization' by Somying Thainimit, Luis A. Alexandre and Vasco M.N. de Almeida.

Fully dilated pupil = 4 to 8mm in diameter 
Fully constricted pupil = 2 to 4 mm in diameter
(larger doe-eyed pupils are usually better since small ones can make the eyes look angry/scary/psycho - unless you are going for that, of course LOL).

Also, please note that if you are mixing and pouring clear epoxy resin into those half-sphere (cabochon) silicone molds, remember to:

A.) Wear an apron or some cheap clothes  since that stuff sticks to everything worse than shit to a blanket. 

B.) Make sure that your mixing cups and stirrer are both disposable and as clean as possible (wear latex or nitrile gloves to avoid getting the molds greasy and wash everything with warm water, soap and even an isopropyl alcohol rinse if you have that). 

C.) Pour/mix the resin and hardener SLOWLY. There is plenty of time. Even with a thin layer of epoxy you've got about half an hour before it really starts to set, and I know from experience that 1 inch lenses made with the stuff take over 24 hours to set through completely. If you rush and try to beat epoxy resin like eggs in an omlette then you will just end up with thousands of tiny bubbles and a pair of cloudy looking lenses. (Also, don't do what I did and poke the back of your resin lense at about 20 hours in just to see if it has set yet. Because you end up with a dented, ruined lense. Best to wait for about 30 hours before popping them out just to be safe.)

# 70
>>10991
I should also mention that even if you get the best epoxy resin on the market, it will eventually yellow with time. UV light exites the chemical bonds and turns the resin yellow from the outside, in. If your robowaifu has eyelids that move, this is a good reason to close her eyes while she is inactive.

It also means that the eyeballs themselves should be made with a degree of replacability, since you'll want to swap them out after a couple of years when they start to yellow noticeably. So maybe spend an hour or two painting in the irises but it's probably best not to try crafting a masterwork prosthesis ;D

# 71
>>10991
>>10992
Excellent information on this topic. The effort here is much appreciated Anon.

# 72
>>10993
Yes, good infos. I drop some videos into it, which I watched a while ago.
https://youtu.be/_KAlB_toNDg
https://youtu.be/RO88zp5Pblg
https://youtu.be/VMlZfpO1vPA
https://youtu.be/KrLGnCC0C8E

# 73
>>10995
Thank you kindly Anon.

# 74
I already mentioned there's open source software that can see heartbeats and micro facial movements called Eulerian Video Magnification in another thread, but I figure I might as well mention it here too: https://www.youtube.com/watch?v=ONZcjs1Pjmk

As for hardware, I was thinking simple solid black camera eyes if I couldn't get 3-axis movement (vertical, horizontal, convergence) working with cameras without taking up too much space. I haven't thought too much about eyes other than that, except that I was thinking she should see in IR, to help in poor lighting without blinding me with LEDs on her face. I remember reading about something called a Modulo Camera that supposedly never over-exposes or something, so maybe it could just use a bigger camera for better night vision? There's also something called a "Light field camera" that keeps everything in focus, but I'm not sure how useful that is for robot vision, I just think it's neat.

# 75
>>13163
That's an interesting concept Anon, thanks. Yes, I think cameras and image analysis have '''very''' long legs yet, and we still have several orders of magnitude improvements yet to come in the future. It would be nice if our robowaifus (and not just our enemies) can take advantage of this for us. We need to really be thinking ahead in this area tbh.

# 76
It seems like CMOS is the default sensor for most CV applications due to cost. But seeing all these beautiful eye designs makes me consider carefully how those photons get processed into signal for the robowaifus.
Cost aside, CCD as a technology seems better because the entire image is processed monolithically, as one crisp frame, instead of a huge array of individual pixel sensors, which I think causes noise which has to be dealt with in post image processing.  CCD looks like its still the go-to for scientific instruments today. 

In astrophotography everyone drools over cameras with CCD, while CMOS is -ok- and fits most amateur needs, the pros use CCD. 

Astrophotography / scientific
www.atik-cameras(dot)com/news/difference-between-ccd-cmos-sensors/

This article breaks it down pretty well from a strictly CV standpoint. 

www.adimec(dot)com/ccd-vs-cmos-image-sensors-in-machine-vision-cameras/

# 77
>>14751
That looks very cool Anon. I think you're right about CCDs being very good sensor tech. Certainly I think that if we can find ones that suit our specific mobile robowaifu design needs, then that would certainly be a great choice. Thanks for the post!

# 78
'''iLab Neuromorphic Vision C++ Toolkit'''
The USC iLab is headed up by the PhD behind the ''Jevois'' cameras and systems.
http://ilab.usc.edu/toolkit/

# 79
>(>>15997, ... loosely related)

