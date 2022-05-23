# 1
Robotic control and data systems can be run by very small and inexpensive computers today. Please post info on SBCs & micro-controllers.

en.wikipedia.org/wiki/Single-board_computer
https://archive.is/0gKHz

beagleboard.org/black
https://archive.is/VNnAr

>===
-''combine 'microcontrollers' into single word''

# 2
www.techrepublic.com/article/inside-the-raspberry-pi-the-story-of-the-35-computer-that-changed-the-world/

Not a bad article about the founding of the Raspberry Pi phenomenon.

# 3
a $3 wifi module and micro-controller. it is a cheap and reliable solution for small automation projects.

# 4
>>16

>Intel ME™ inside™

>>1405

>proprietary jewberry

meh, use Olimex

# 5
>>1407
We're all well-aware of the botnet around here, and of striving to protect against it anon. Have anything better to contribute than simple grousing? At least post pics of good SBCs you approve of ITT if nothing else.

# 6
>>1406
I think I remember seeing that from the site before anon. Thanks for the pdfs especially.

# 7
>>1410

As for microcontrollers, there's the HiFive1, for example.



SoCs, there currently exists the  HiFive Unleashed (which costs a lot) and there's going to be lowRISC

# 8
>>1429
thanks anon.

# 9
>>1430
www.lowrisc.org/
www.sifive.com/boards/hifive1

# 10
neat little DIY raspi 'laptop' project

https://invidious.snopyta.org/watch?v=tDVWA3wdStY

# 11
Beaglebone has produced a new product they are touting as being for AI. 
Dual Arm Cortex-A15 microprocessors w/ dual C66x floating-point VLIW DSPs. I assume that's only 2 DSPs, but I'm not sure yet. TI has been in this game all the way from the very beginning of silicon-based computing, and they are arguably the world leader in DSP systems, so yea. It's probably a very powerful little SBC, maybe the best atm. Not sure yet about general support for common libs like TensorFlow or PyTorch yet, so YMMV.

https://beagleboard.org/ai
www.ti.com/product/AM5729

# 12
>>3722
>update:
It looks like the board is capable of doing Computer Vision directly in hardware.
>''"embedded-vision-engine (EVE) cores supported through an optimized TIDL machine learning OpenCL API with pre-installed tools."''
http://downloads.ti.com/mctools/esd/docs/tidl-api/example.html

If so, then to my knowledge this is the very first SBC to do so, at least for the inexpensive consumer device market. Probably means this would be a very nice dedicated board for running the robowaifu's eyes & vision.

# 13
>>3722
I believe this is the proper user guide for the DSP subsection of the chip.

# 14
>>3724
This one is probably a closer fit for our needs tbh.

# 15
TI's Deep Learning SDK (presumably) used on the board.
http://software-dl.ti.com/processor-sdk-linux/esd/docs/05_00_00_15/linux/Foundational_Components_TIDL.html

kek, this is turning into a cluster. I'm going to redo these posts into some kind of order. :^)

# 16
>>1431
Through a train of links via this post, I found this open-source hardware FPGA microcontroller board. They already have a working prototype stage ATP. This is the smallest-scale one of a planned family of these for their platform.
https://github.com/pulp-platform/pulpissimo
https://pulp-platform.org/

Also, there seems to be a growing movement for opensauce h/w as exemplified by lowRISC in Cambridge.
https://www.lowrisc.org/blog/2019/10/ibex-on-fpga-get-stuff-executed/
>>1429

# 17
>>3727
>kek, this is turning into a cluster. I'm going to redo these posts into some kind of order. :^)
ehh, I'm just going to dump everything here now and then see about deleting/cleaning it up into a couple of orderly posts later. more important to collect the into one place than to make it pretty at the same time.

>demo of programming the AI
https://beagleboard.org/p/175809/tidl-on-beaglebone-ai-1ee263

https://invidious.snopyta.org/watch?v=v3_hNBJbqME
https://invidious.snopyta.org/watch?v=1XTIi9Z_8x4

>programming the beaglebone PRU
https://beagleboard.org/pru

https://invidious.snopyta.org/watch?v=PZSxRHO59AI
https://invidious.snopyta.org/watch?v=ZNz45v9Uesg
https://invidious.snopyta.org/watch?v=y8-gwthzf-c

# 18
>>3729
>the beaglebone PRU
https://markayoder.github.io/PRUCookbook/

# 19
https://ftp.openbsd.org/pub/OpenBSD/6.7/armv7/
https://ftp.openbsd.org/pub/OpenBSD/6.7/armv7/INSTALL.armv7

# 20
Beaglebone AI repo
https://github.com/beagleboard/beaglebone-ai

# 21
>>3733
Beaglebone AI reference manual
https://github.com/beagleboard/beaglebone-ai/wiki/System-Reference-Manual

I'll see about turning this into a single pdf file later.

# 22
Projects that utilize the PRUs (2x available on the Beaglebone)
```cpp
Project 	Description 	Type 	Link

-LEDscape 	BeagleBone Black cape and firmware for driving a large number of WS281x LED strips 	
Code Library 	https://github.com/osresearch/LEDscape
Documentation and example projects 	http://trmm.net/LEDscape

-LDGraphy 	Laser direct lithography for printing PCBs 	
Code library and example project 	https://github.com/hzeller/ldgraphy/blob/master/README.md

-PRdUino 	This is a port of the Energia platform based on the Arduino framework allowing you to use Arduino software libraries on PRU. 	
Code Library 	https://github.com/lucas-ti/PRdUino

-DMX Lighting 	Controlling professional lighting systems
Project 	http://beagleboard.org/CapeContest/entries/BeagleBone+DMX+Cape/
Tutorial 	http://blog.boxysean.com/2012/08/12/first-steps-with-the-beaglebone-pru/
Code Library 	https://github.com/boxysean/beaglebone-DMX

-Interacto 	A cape making BeagleBone interactive with a triple-axis accelerometer, gyroscope and magnetometer plus a 640 x 480/30 fps camera. All sensors are digital and communicate via I²C to the BeagleBone. The camera frames are captured using the PRU-ICSS. The sensors on this cape give hobbyists and students a starting point to easily build robots and flying drones.
Project 1 	http://beagleboard.org/CapeContest/entries/Interacto/
Project 2 	http://www.hitchhikeree.org/beaglebone_capes/interacto/
code library 	https://github.com/cclark2/interacto_bbone_cape

-Replicape: 3D Printer 	Replicape is a high end 3D-printer electronics package in the form of a Cape that can be placed on a BeagleBone Black. It has five high power stepper motors with cool running MosFets and it has been designed to fit in small spaces without active cooling. For a Replicape Daemon that processes G-code, see the Redeem Project 	Project 	http://www.thing-printer.com/product/replicape/
Code Library 	https://bitbucket.org/intelligentagent/replicape/

-PyPRUSS: Python library 	PyPRUSS is a Python library for programming the PRUs on BeagleBone (Black) 	
Code Library 	http://hipstercircuits.com/pypruss-a-simple-pru-python-binding-for-beaglebone/

-Geiger 	The Geiger Cape, created by Matt Ranostay, is a design that measures radiation counts from background and test sources by utilising multiple Geiger tubes. The cape can be used to detect low-level radiation, which is needed in certain industries such as security and medical. 	
Project 1 	http://beagleboard.org/CapeContest/entries/Geiger+Cape/
Project 2 	http://elinux.org/BeagleBone/GeigerCapePrototype
Code library 	https://github.com/mranostay/beaglebone-telemetry-presentation

-Servo Controller Foosball Table 	Used for ball tracking and motor control 	
Project 	http://www.element14.com/community/community/knode/single-board_computers/next-gen_beaglebone/blog/2013/07/17/hackerspace-challenge--leeds-only-pru-can-make-the-leds-bright
Tutorial 	https://docs.google.com/spreadsheet/pub?key=0AmI_ryMKXUGJdDQ3LXB4X3VBWlpxQTFWbGh6RGJHUEE&output=html
Code library 	https://github.com/pbrook/pypruss

-Imaging with connected camera 	Low resolution imaging ideal for machine vision use-cases, robotics and movement detection 	
Project & Code library 	http://www.element14.com/community/community/knode/single-board_computers/next-gen_beaglebone/blog/2013/08/18/bbb--imaging-with-a-pru-connected-camera

-Computer Numerical Control (CNC) Translator 	Smooth stepper motor control; real embedded version of LinuxCNC 	
Tutorial 	http://www.buildlog.net/blog/2013/09/cnc-translator-for-beaglebone/
Tutorial 	http://bb-lcnc.blogspot.com/p/machinekit_16.html

-Robotic Control 	
Chubby 	
Project 	http://www.youtube.com/watch?v=dEes9k7-DYY
Code library 	https://github.com/cagdasc/Chubby1_v1
SpiderBot 	
Project 	http://www.youtube.com/watch?v=JXyewd98e9Q
Reference 	http://www.ti.com/lit/wp/spry235/spry235.pdf

-Software UART 	Soft-UART implementation on the PRU of AM335x 	
Code library & Reference 	http://processors.wiki.ti.com/index.php/Soft-UART_Implementation_on_AM335X_PRU_-_Software_Users_Guide

-Deviant LCD 	PRU bit-banged LCD interface @ 240x320 	
Project 	http://www.beagleboard.org/CapeContest/entries/DeviantLCD/
Code library 	https://github.com/cclark2/deviantlcd_bbone_cape

-Nixie tube interface 		
code library 	https://github.com/mranostay/beagle-nixie

-Thermal imaging camera 	Thermal camera using Beaglebone Black, a small LCD, and a thermal array sensor 	
project & Code library	https://element14.com/community/community/knode/single-board_computers/next-gen_beaglebone/blog/2013/06/07/bbb--building-a-thermal-imaging-camera

-Sine wave generator using PWMs 	Simulation of a pulse width modulation 	
Project & Reference 	http://elinux.org/ECE497_BeagleBone_PRU
Code library 	https://github.com/millerap/AM335x_PRU_BeagleBone

-Emulated memory interface 	ABX loads amovie into the Beaglebone's memory and then launches the memory emulator on the PRU sub-processor of the Beaglebone's ARM AM335x 	
Project 	https://github.com/lybrown/abx

-6502 memory interface 	System permitting communication between Linux and 6502 processor 	
Project 	http://elinux.org/images/a/ac/What's_Old_Is_New-_A_6502-based_Remote_Processor.pdf
Code library 	https://github.com/lybrown/abx

-JTAG/Debug 	Investigating the fastest way to program using JTAG and provide for debugging facilities built into the Beaglebone 	
Project 	http://beagleboard.org/project/PRUJTAG/

-High Speed Data Acquistion 	Reading data at high speeds 	
Reference 	http://www.element14.com/community/community/knode/single-board_computers/next-gen_beaglebone/blog/2013/08/04/bbb--high-speed-data-acquisition-and-web-based-ui

-Prufh (PRU Forth) 	Forth Programming Language and Compiler. It consists of a compiler, the forth system itself, and an optional program for loading and communicating with the forth code proper.
Compiler 	https://github.com/biocode3D/prufh

-VisualPRU 	VisualPRU is a minimal browser-based editor and debugger for the Beaglebone PRUs. The app runs from a local server on the Beaglebone. 	
Editor and Debugger 	https://github.com/mmcdan/visualpru

-libpruio 	Library for easy configuration and data handling at high speeds. This library can configure and control the devices from single source (no need for further overlays or the device tree compiler) 	
Documentation 	http://users.freebasic-portal.de/tjf/Projekte/libpruio/doc/html/index.html
Library (German) 	http://www.freebasic-portal.de/downloads/fb-on-arm/libpruio-325.html

-BeagleLogic 	100MHz 14channel logic analyzer using both PRUs (one to capture and one to transfer the data) 	
Project 	http://beaglelogic.net

-BeaglePilot 	Uses PRUs as part of code for a BeagleBone based autopilot 	
Code Library 	https://github.com/BeaglePilot/beaglepilot

-PRU Speak 	Implements BotSpeak, a platform independent interpreter for tools like Labview, on the PRUs 	
Code Library 	https://github.com/deepakkarki/pruspeak```

>sauce
processors.wiki.ti.com/index.php/PRU_Projects

# 23
>>3736
>>3723
I just realized there are 4x PRU and 4x EVE on each board.
```cpp
BeagleBone Black mechanical and header compatibility
TI AM5729 processor featuring 2x A15 CPU, 2x C66 DSP, 4x M4 MCU, 2x SGX544 3D, GC320 2D, IVA-HD, 4x PRU and 4x EVE
1GB RAM and 16GB on-board eMMC flash with high-speed interface
USB type-C for power and superspeed dual-role controller; and USB type-A host
Gigabit Ethernet, 2.4/5GHz WiFi, and Bluetooth
microHDMI
Zero-download out-of-box software experienceBeagleBone Black mechanical and header compatibility```

>sauce
https://beagleboard.org/p/products/beaglebone-ai

>>3722
>I assume that's only 2 DSPs, but I'm not sure yet. 
Correct.

# 24
This looks kind of cool tbh. I sort of want one of these. Not really a robowaifu thing, but it looks kind of fun.
https://www.okdo.com/us/p/piper-computer-kit-2/

# 25
crossposted from the embedded learning thread. a grab-bag of technical documents for arduino microcontrollers.

https://onlinedocs.microchip.com/

# 26
For anyone that can afford it this might be interesting.



https://www.anandtech.com/show/15856/qualcomm-announces-rb5-robotics-platform-a-powerful-sbc

# 27
>>3851
That does look interesting Anon, thanks. A bit pricey atm for our purposes IMO, but still worth a look-see.

# 28
I suppose this is the most relevant thread atm on /robowaifu/ to post this. There has been a slow push for open sauce RISC chip designs & manufacturing. This movement has recently gotten a potentially big boost from Google **what could possibly go wrong, Anon?** with their Skywater PDK (process design kit).
https://github.com/google/skywater-pdk
https://en.wikipedia.org/wiki/Process_design_kit

> via nano /g/4908

# 29
>>4128
>**yfw the main tech company Google is fronting on this project starts the '''actua'''l skynet**

# 30
>>4128
related.
https://invidio.us/watch?v=EczW2IWdnOM

fair warning, this group he represents are **hyper CoC-suckers**

# 31
I asked about some infos about FPGAs on lain/diy. Even if many there might not like /robowaifu/, we could still pick their brains. I'm using all kinds of sites to ask stuff, and might link to it then. Must be careful not to dox myself, though wouldn't matter that much anyways.

 "Hi! I would like to know if it might make sense to preprocess images with an (Icestorm) fpga for interference in image recognition. Could I take images from a video stream when something changes beyond a certain treashold? Could I get a image e.g. every 10 frames in b/w and some others with a lower resolution? Would it make sense to do this with an FPGA, when the images then go to a SBC like Jetson Nano with a GPU anyways? Is it much more efficient?
I would also like to compare images, like finding a difference, by checking for color changes in any area.

The other thing is voice alternation, like from espeak or festival, then changing it. Could I develop these changes in a software like Audacity or train a neural network, and then import these changes into a FPGA toolchain?" https://lainchan.org/diy/res/2899.html#4795

# 32
>>4474
Sure, sounds like a good idea. There is plenty of good resources on lainchan, and a few smart ppl there. I would prefer us to be allies, for my part.

Yes, don't dox yourself Anon.

# 33
>>4474
It depends on how fast the SBC's CPU and how much RAM you have. For initial testing you could probably just do the image processing on the SBC, where you can quickly test different algos. 
To prepare your design for FPGA will take longer, so you better have a working design first. The main advantage is you could offload a lot of the processing to the FPGA, leaving your SBC to do voice or something else. I've been learning about formal verification for FPGAs for the last few months here:
https://zipcpu.com/tutorial/
I strongly recommend it if you have the time, before starting my testing was very basic XD

# 34
>>4487
>https://zipcpu.com/tutorial/
Not that anon, Anon, but thanks I was trying to remember that project name earlier today.

# 35
>>4488
You're welcome m8 ;)

# 36
>>4487
>The main advantage is you could offload a lot of the processing to the FPGA, leaving your SBC to do voice or something else.
Hi, I didn't plan to offload interference to the FPGA since some of then newer SBC even have specialized Asics for that. I was thinking about using the FPGA for preparations, like only picking some pictures from a live feed, send them only to the SBC if something changes beyond a threshold. Or generaly only sending some pictures from the feed dependent on the situation and maybe doing some processing on them before doing so.
I probably shouldn't get into FPGA now, have already enough other stuff on my table. I'm njust keeping a eye on it. Thanks for the link nevertheless.

# 37
>>4490
>have already enough other stuff on my table
Very relatable XD

# 38
Here's a separate thread about alternative CPU designs >>4506, like Risc-V.

# 39
>>4511
It's a very good thread, thanks Anon.

# 40
>>4487
>FPGA
I'm definitely interested in learning more about this. Will there ever be FPGAs inexpensive enough for the average anon to use them for his robowaifus I wonder?

also, very-related X-link
>>4969
>>4895

# 41
>>5150
Yes, I think so. Depends on how much money the "average anon" here has, but also the use case. Cheap and weak ones aren't so expensive.

# 42
offtopic guys but i recently bought a small fake phone with rather decent specs for just 1000 peso
orange pi seems promising but they say its buggy

i succesfully rooted the android 4.0 OS and took the phone apart
lcd screen and camera is pretty decent depite the price
how do i connect it to my arduino (will my device count as SBC)

# 43
>>5315
>how do i connect it to my arduino
if it's got a usb connector, then you'd use a serial-to-usb connector. i think this type of connection was brought in our embedded group learning thread.
>>367

# 44
There's now a cheaper version of Jetson Nano, with fewer RAM: https://youtu.be/UNCsNH3tdcg for around 60$, while the original is 99$ and the bigger brother 500$ or so.

# 45
>>5699
That's good news, thanks Anon.

# 46
Also, OpenCV is coming out with a kit, similar to Google TPU: https://opencv-ai-kit.backerkit.com/hosted_preorders
We missed the campaign, when it was probably cheaper. Starts at 150$ now, same price as Google's Coral board. It uses OpenVino: https://youtu.be/kY9nZbX1DWM and aXelerate (own device) or Luxonis (Web API) https://docs.luxonis.com/tutorials/openvino_model_zoo_pretrained_model/ 

Test: https://youtu.be/dFh0rrKEVJc
IMHO, even the smaller board is to big for a camera board, if one wants to build a humanoid with two eyes. It might fit into an eyeball, but probably won't. I'll hope there will be a version with two layers, half the size. Since it's open source, my hopes might not be futile.

Anyone here compared Jetson Nano vs Beaglebone AI or other?

# 47
>>5705
Wow, also really good news. OpenCV is a great platform. Easy to use (relatively) and very powerful as well. And unlike many other libraries, is much more open and available to everyone, at the least it's not nearly so leveraged against commercial platforms as many others are.

# 48
>>5705
>if one wants to build a humanoid with two eyes. It might fit into an eyeball, but probably won't
I have two JeVois cameras which are ~2cm flattened 'cubes'. They are light & self-cooled and run Linux+OpenCV right onboard.

# 49
>>5707
Oh wow, cool. I recalled to have watched a video about them quite a while ago. However, just realized my posting of OAK was rather OT, since we have a thread for cameras, vision, and control boards. I posted some extra infos there and crosslink it: >>5714

# 50
no posts for one month really BUMP
im quite surprised nobody mentioned mini PC's like intel NUC
speaking of mini pc is there a way to install linux on my H96 box (its just 1500 lol)
modern windows boxes are quite expensive (about 7000 peso)

also i accidentally broke my fake phone while unsoldering the csi camera ribbon cable (its not that severe)
where can i buy one of these fake iphones (or android) (RPI camera and screen is too expensive)
video related https://www.youtube.com/watch?v=GwhzГунт4Xg (i kinda like this channel)

# 51
>>7344
welcome, back happy thanksgiving. you're just in time to celebrate our 4th birthday here anon. 
>linux on h96
I don't see why not
https://forum.armbian.com/topic/8210-linux-on-h96-max-rk3399-variants/

https://blog.nobugware.com/post/2019/h96-max-android-box-as-a-linux-server/

https://www.youtube.com/watch?v=nSCj1b6PbaQ

# 52
Anyone know anything/hear anything about Propeller processors? From their promo copy on the site, it seems to not need an OS to function properly.
https://www.parallax.com/propeller/

# 53
>>8051
Thanks for posting this. It looks very interesting. It's some micro controller which special innovations. Also supports quite some programming languages to use it, one being a visual one for beginners, similar to Scratch. However, this ecosystem strikes me as rather expensive. Arduino is open source and available as cheap clones from China, this here seem to be tailored for education and ease of use. I guess it's good for that, but will be more expensive. I just figure that from a price of a sensor package of ~1600$, though I didn't look much further, might be a lot of them for a whole class or school. This whole concept might also be more relevant for small robots, where there isn't so much space for many controller boards and so the one needs to be more powerful.

# 54
Sorry I couldn't resist. :^)

# 55
Nano /g/ had an interesting post about what appears to be a PDA. Haven't checked into this yet, so caveat emptor.
>What about this? Ignore the price for a second...
>https://www.crowdsupply.com/sutajio-kosagi/precursor
>Verifiable botnet-free. You can even build the gateware for the SoC yourself. A similar setup could be achieved with a custom pcb and probably just more ice40up5k's, at the cost of effort and bulk.
>I'm interested in having a portable device that can use technologies free from the internet/infrastructure you pay for that is run by corporations. For example, https://www.meshtastic.org/ which is a mesh network using LoRa.

If it's 'verifiable' botnet-free then that would certainly be a big step forward for freedom.

aHR0cDovL25hbm9jaGFucXpheXR3bHlkeWtiZzVueGtneWp4azN6c3JjdHh1b3hkbWJ4NWpiaDJ5 ZHlwcmlkLm9uaW9uL2cvMzQ2MDUjcG9zdDM1NDE2Cg==

# 56
>>8146

The use of FPGAs has already been mentioned briefly here >>6861 in the alternative ISA thread.



I don't expect ISA implementations on FPGAs to be a huge hit as you're paying an enormous premium for security or emulation cycle accuracy compared to exponentially more computing power a locked down but affordable mass produced SBC using ARM or x86-64 provides. Maybe as a password manager/crypto wallet/YubiKey that PDA project will find an audience.

# 57
>>8148
>Maybe as a password manager/crypto wallet/YubiKey that PDA project will find an audience.
I think I understand. Well, I think it's probably going to be a common scenario to have some kind of home server/routing system serving as a protected gateway for our robowaifus out into the broader world, and to offload local computations. Maybe some kind of FPGA solutions can be a part of those. Thanks for the feedback Anon.

# 58
There are small devices which can run ML models coming from TinyML. Maybe this is usefull for some reflexes or chaper waifus. It coming from Nordic Semiconductor in a partnership with Edge Impulse. It seem to work for continuous motion recognition, responding to voice and recognizing sounds from audio.
https://www.nordicsemi.com/News/2021/01/Edge-Inpulse-and-Nordic-partnership

# 59
>>8160
>BlueTooth IoT
While vaguely similar to our use case, one of the things we're quite concerned with here on /robowaifu/ is botnet infestations in our waifus. The entire IoT world is famous at this stage for blatantly embracing just that (that supports these corpo's business models, after all). So, I'll look into this but with a grain of salt. But regardless, it's affirming to see groups focusing on issues we predicted here all the way back at our beginning. Hopefully innocuous systems will appear eventually.
>tinyML
Thanks I didn't know about them. Seems right up our alley if they are opensource. I'll be researching them and will post in one of the AI threads if it seems good. Thanks Anon.
https://www.tinyml.org/home/

# 60
>>8163
>update:
In pretty short order I've discovered enough opensource hardware and software to probably be able to start an 'AI-on-microcontrollers' thread here, primarily ones based on ''TensorFlow Lite for Microcontrollers'' for now.
https://www.tensorflow.org/lite/microcontrollers

Thanks again, stay tuned.

# 61
Here a comparison video between Teensy, Arduino and Arduino clones: https://youtu.be/75IvTqRwNsE - Teensy has some advantages, but cost 20$ and has a proprietory bootloader, also seems to be a bit harder to learn for beginners. I bought cheep Arduino clones, but haven't tested them yet, for lack of time. So I don't know if thy are relly bad. I think for prototyping they will most likely be good enough. ESPs are also an option, which are cheap but  harder to get into.

# 62
>>8165

I don't get the beef he had with cheap arduino clones.  Those are pretty much all I use and I found most of the errors come from my breadboard rather than the quality of the chips.



ESP8266s are good, especially the D1 Minis.  They only have a few digital pins but you can easily download their libraries in the Arduino IDE and are as close to plug and play, especially with the Blynk app that sets up the wifi for you. Though I want to get off proprietary eventually, it's still a good stepping stone.



I've tried ESP32s but the only reason to use them is because they're fast enough to stream videos, thus most ESP combo chips are camera chips, I have a couple of ESP32-Cams heading my way.



The absolute cheapest though is the STM32, in the ESP32 you had to hold the reset button while uploading, well in this one you have to change the jumper every time to boot mode from running mode.  The STM32 was impossible to get running until I realized I was using the Windows Store version of Arduino instead of the simple download version.  Remember the electrical engineer back on 8chan who taught lessons on AVR using Debian and register notations, even when what we were using already had ready libraries in Arduino IDE?  Well crank that up a notch and what you get is literally multiplexed registers which only someone who slept on the STM32 datasheet can begin to comprehend.  Thankfully there are some libraries of the common use cases already.



In summary these are the use cases which I justify for the following:



*arduino clone -- if you just want to flash an led or drive a DC motor

*STM32 - if you want to drive a 1.8" display or have tons of interrupts (e.g. reading a radio control receiver)

*ESP8266 - if you want to get into those app-controlled internet of things (there is a noticeable delay though from touching the virtual button and the LED lighting up)

*ESP32 - similar to ESP8266, but the justification would be it's faster so better with cameras, so just get them combined with camera modules, they're just 5-10 bucks.  The closest I can get to DIY wireless FPV without shelling out for those sketchy 5 Gigahertz Chinese things.



Oh yeah, I have a Raspberry Pi and Jetson Nano but I consider them to be small form factor computer desktops rather than something I'd embed then forget.

# 63
>>8366
It would sure be nice if you taught everyone else here how to do this kind of stuff. Ever consider a /robowaifu/ teaching thread on these topics Anon?

# 64
Found out on nano/g about a new Raspberry Foundation's new Arduino microcontroller competitor called ''Pi Pico''.

>"$4 Raspberry Pi Pico board features RP2040 dual-core Cortex-M0+ MCU"
https://web.archive.org/web/20210121070023/https://www.cnx-software.com/2021/01/21/raspberry-pi-pico-board-features-rp2040-dual-core-cortex-m0-mcu/

# 65
>>8437
related
https://electronics360.globalspec.com/article/16251/video-raspberry-pi-launches-4-board-built-with-its-first-proprietary-mcu

# 66
Wiki dedicated to Arm-based IoT & embedded. Seems like it's been around for a number of years.
https://wiki.friendlyarm.com/wiki/index.php/Main_Page
https://github.com/friendlyarm

# 67
https://en.wikipedia.org/wiki/Reconfigurable_computing

# 68
Simple-to-install RaspberryPi 3 & 4 images, with Ubuntu 20.04 LTS + ROS Noetic included & preconfigured. Probably the single easiest/fastest way to get started with ROS.

https://learn.ubiquityrobotics.com/noetic_pi_image_downloads

