# 1
Embedded Programming Group Learning Thread 001

Greetings robowaifufags.
As promised in the meta thread, this is the first installment in a series of threads where we work together on mastering the basics of embedded programming, starting with a popular, beginner-friendly AVR 8-bit microcontroller, programming it in C on linux. 

>why work together on learning and making small projects that build up to the basis of a complete robot control system instead of just posting links to random microcontrollers, popular science robot articles, and coding tutorials and pretending we're helping while cheerleading and hoping others will do something so we don't have to?
Because, dumbass, noone else is going to do it. You know why in emergency response training they teach you to, instead of yelling "somebody call an ambulance!," you should always point to or grab someone and tell that person to do it? Because everyone assumes someone else will do it, and in the end, noone does. Well, I'm talking to YOU now. Yeah, you. Buy about 20 USD worth of hardware and follow the fuck along. We're starting from zero, and I will be aiming this at people with no programming or electronics background.

>I suppose I could get off my ass and learn enough to contribute something. I mean, after all, if all of us work together we can totally build a robowaifu in no time, right?
No, the final goal of these threads is not a completed robowaifu. That's ridiculous. What we will do though, by hands-on tackling many of the problems facing robot development today, is gain practical and useful knowledge of embedding programming as well as a more grounded perspective on things.

>so we're just going to be blinking a bunch of LEDs and shit? lame.
Not quite. We will try to cover everything embedded here: basic I/O, serial communications, servo/motor control, sensor interfacing, analog/digital conversion, pulse-width modulation, timers, interrupts, I2C, SPI, microcontroller-PC interfacing, wireless communications, and more.

# 2
>>367
Part 2 since I don't know how many characters posts can be.

>well OK, that sounds cool I guess. what do I need to join in?
I will post the parts list in the next post or two, along with links to buy stuff cheap. For the beginning, though, you will need an Arduino Nano, or preferably, one of the 3-4 dollar clone boards. Same thing. We will be using the ones with the Atmega328p at 5V and 16Mhz. Besides the Nano board, you will need a breadboard, wires to hook things together, LEDs and resistors for some basic visual feedback, an In System Programmer for AVR chips, and a USB to Serial converter (cp2102 or ftdi1232 or similar) so we can talk to it.

>OK. that's the hardware, what about software and stuff?
We will be programming in a linux environment. I don't really care what you use. Linux Mint and Ubuntu are what I'd recommend if you don't have a linux install on hand. If you don't have a linux system and can't/don't want to dual boot, get a raspberry pi or something and dev on there. Our language of choice is AVR-C (avr-libc). Compiler, linker and such are GNU (avr-gcc). We will be using hand-crafted GNU Makefiles for compilation, linking, flashing, etc.

>why can't I use the Arduino IDE on my Windows 10 machine?
Half the point of a cooperative thread is so that we can share code and help others debug theirs. We can't do that if everyone has a different setup.

I want as many of us as possible in on this. Really, I'd like everyone on the board trying their hand at it. It's not hard. Let me know if you have any questions at all. Follow-up posts to come.

# 3
Greetings, anon. Art thou still out there? I'm interested in this group learning & have been wanting to fiddle with embedded programming for a while. Will periodically check back. If you're no longer here, take care friend.

# 4
>>1936

Hi. Can't say I've been active but, I'm here. I see the first couple of posts from the old 8chan thread were copied over minus newlines. Wew. Not sure if I'd make another thread but at least I'm down to talk to anyone.

# 5
>>2005
hi there notsojapanon, glad to see you found us. i still have all the old threads including this one. i hope you pick back up with the class again. how's the job going?
>t. chobitsu

# 6
>>2006

Oh hey, it's the old BO. Good to see you're still alive and waifu'ing it up. What's the userbase like right now? Any discussion going on anywhere?

# 7
>>2007
good to see you again. there are a few of us here, i hope the others who don't know we're here will figure it out eventually. 

after the false flag at 8ch, i came here to julay about a month later and began to try to rebuild the board slowly by hand. i planned to try to automate it and began to write some archiving software, but it's only in a half-completed state atp. it grabs archives ok, but still doesn't migrate them yet.
https://fatpeople.lol/tech/thread/76.html#270
 i may pick it back up as a prototype for Robi & Co's ''Final Solution'' project (as a standalone), and if i can manage it i'll restore every thread from the old board here (this thread being one of the more important ones) and the bunker-bunker over at fatchan.

>related
i did get some nanos to work on projects with your thread, i may have shown you already?

# 8
>>2008

>nano 5-pack

Can't remember if I saw that, sorry. I wouldn't mind trying my hand at another thread, since my skills have progressed a lot since last time, with a few commercial products under my belt too. That said though, right now the timing isn't the best for me. I have two major projects I'm heading up and  I'm working on a lateral career move that will, at the very least, let me die from the corona virus in my home country.

# 9
>>2013
haha, ok fine then. **don't die bro**
i've been progressing in my skills with programming, so i hope i can devise some very simple-to-use library code we can all use from C/C++/Python/JS , at least that's my goal. keep us up to date here with everything going on with you anon.

# 10
>>2014

Will do.

# 11
Looking forward to this OP.

# 12
Shopping List

Note: The following links are EXAMPLES of what we will be using, and may not be the cheapest/highest quality available. A little bit of research and shopping around may be required to get the best deals/not wait months for shipping/minimize the risk of DOA parts/etc.

1 x Arduino Nano compatible dev board, 5V 16Mhz version: 4~7 USD
I highly recommend getting one that is pre-soldered, just pay the extra 50 cents so you don't have to fuck around. Buy 2 if you are worried about bricking or frying it.
Amazon - https://www.amazon.com/HiLetgo-ATmega328P-Micro-controller-Development-Compatible/dp/B00E87VWY4/dealextreme - https://www.dx.com/p/improved-version-nano-3-0-atmel-atmega328p-mini-usb-board-for-arduino-452880?TC=USD&
banggood - https://www.banggood.com/ATmega328P-Arduino-Compatible-Nano-V3-Improved-Version-No-Cable-p-959231.html?rmmds=search
gearbest - https://www.gearbest.com/boards-shields/pp_1620227.html?wid=1433363

1 x In-System Programmer (ISP): 6~11 USD
Try to get one with a 6-pin header so you can plug it right into the Nano. I really have only had good experiences with the usbtiny types and recommend that. Do not think that you can program with the cheap USB-TTY adapters, those require the arduino bootloader, which we will not be using. The USBASP types seem to work as well, but you'll have to do your own research there.
amazon - https://www.amazon.com/USBtinyISP-Programmer-Bootloader-Download-Interface/dp/B01FDD4EP0 what I use
banggood - https://www.banggood.com/USBASP-USBISP-3_3-5V-AVR-Downloader-Programmer-With-ATMEGA8-ATMEGA128-p-934425.html? cheap, but supported??
dealextreme - https://www.dx.com/p/usbasp-usbisp-downloader-programmer-for-51-avr-blue-black-265121
dealextreme - https://www.dx.com/p/avrisp-usbasp-stk500-10pin-to-6pin-converting-board-deep-blue-295913
gearbest - https://www.gearbest.com/other-accessories/pp_009877473243.html?wid=1433363

1 x USB to serial adapter:
I've never had a problem with either cp2102, pl2303, or ftdi1232 based boards. Anything should work, really.
amazon - https://www.amazon.com/DSD-TECH-Converter-Compatible-Windows/dp/B072K3Z3TL/
dealextreme - https://www.dx.com/p/pl2303hx-usb-to-ttl-serial-communications-module-white-307649
gearbest - https://www.gearbest.com/development-boards/pp_47013.html?wid=1433363

# 13
Shopping List Continued

Note - forgot in last post: USB serial adapter prices: 3~10 USD

1 x breadboard 4~12 USD
Try to get as large of a breadboard as you can afford, although anything over 800 holes or so should be plenty for now. You can always get more later as you projects expand in size and complexity. Having a steel backplate on it is nice too. Warning: some breadboards have a discontinuity in the side power/gnd rails. Look for a board with solid blue and red lines on the sides. A gap in the lines may indicate a gap in the conductor inside. See pic for one of mine like that. Sure, you can use two different voltages on the same board if you wanted to, but for our purposes, try to get a board with solid lines.
amazon - https://www.amazon.com/UCEC-830-Point-Solderless-Breadboard-400-Point/dp/B01ELGR26I/
amazon - https://www.amazon.com/EL-CP-003-Breadboard-Solderless-Distribution-Connecting/dp/B01EV6LJ7G/
dealextreme - https://www.dx.com/p/zy-204-solder-free-1660-hole-bread-board-breadboard-black-white-425979
dealextreme - https://www.dx.com/p/solderless-breadboard-white-large-size-121529
gearbest - https://www.gearbest.com/kits/pp_266543.html?wid=1433363
banggood - https://www.banggood.com/Wholesale-Test-Develop-DIY-830-Point-Solderless-PCB-Bread-Board-For-MB-102-MB102-p-51331.html
banggood - https://www.banggood.com/MB-102-MB102-Solderless-Breadboard-Power-Supply-Jumper-Cable-Kits-Dupont-Wire-For-Arduino-p-933600.html?rmmds=search

50+ hookup wires/dupont cables/breadboard jumpers: 3~8 USD
These have many names and shapes but all do the same thing: connect two points on a breadboard, or from male or female pins on a sensor or dev board or whatever to a breadboard, or another similar device using the same pin size and spacing. If you aren't familiar with these, I would read up a bit on them:
https://www.allaboutcircuits.com/news/the-best-wire-for-breadboarding/
You may be able to get away with just male-male jumper wires for now if your ISP and USB-serial come with their own connectors, but I would prefer everyone got a 3-piece set of something like 30 male-male, 30 male-female, and 30 female-female. This covers all the bases and you'll thank yourself when you buy a sensor with a two-row header that won't plug into a breadboard. Some examples of what's out there:
banggood - https://www.banggood.com/120pcs-20cm-Male-To-Female-Female-To-Female-Male-To-Male-Color-Breadboard-Jumper-Cable-Dupont-Wire-Combination-For-Arduino-p-974006.html?rmmds=search
banggood - https://www.banggood.com/400pcs-6cm-Breadboard-Jumper-Cable-Dupont-Wire-Electronic-Wires-Black-Red-Color-p-949895.html?rmmds=search
banggood - https://www.banggood.com/140pcs-U-Shape-Solderless-Breadboard-Jumper-Cable-Dupont-Wire-Arduino-Shield-p-78680.html?rmmds=search
amazon - https://www.amazon.com/Solderless-Flexible-Breadboard-Jumper-100pcs/dp/B005TZJ0AM/

Let me know if you have any questions so far. I can help you check if something would work or not. Or, if you find any real good deals, please post them. Let me know if you're interested and following. I would like to get a feel for how many people would like to get involved and what kind of skill level/background everyone has.

# 14
>>3752
And I forget my images like a retard. Pic 1 is a decent breadboard with the rails connected. Pic 2 is some 3 dollar chink one with the rails split in the middle (why only some of the LEDs are lit).

# 15
Shopping List - final

Last but not least, for some I/O practice and visual feedback for debugging and such: LEDs. These can be any color you want, but you're on your own with resistor values if you're using shit like blue, white, teal, or whatever. I will be assuming you're using el cheapo 3mm or 5mm green, red, or yellow ~2V through-hole ones. Get as many as you like, but at the very least get 2 colors and 8 or more of a single color so that we can represent an 8-bit value with them. Unless buying as a set, you will need to buy resistors for them. Minimum value: 330 ohms, max: 1k ohms. If we end up using shift registers later I'll make sure everyone has high enough value resistors so that eight of them on at once doesn't burn out the shift register. In fact, buy a set containing all of the popular resistor values, we'll need ones like 4.7k and 10k for pull-ups and stuff too.

8+ x LEDs: 3~8 USD
amazon - https://www.amazon.com/Willwin-100Pcs-Assorted-Emitting-Resistor/dp/B0759FK7QK
dealextreme - https://www.dx.com/p/3mm-5mm-red-yellow-blue-green-white-leds-diy-kit-150-pcs-420734
banggood - https://www.banggood.com/100pcs-20Ma-F5-5MM-5Colors-Ultra-Bright-LED-Diode-p-966103.html?rmmds=search

10s/100s of Resistors: 3~10 USD
amazon - 
dealextreme - https://www.dx.com/p/diy-1-4w-accurate-carbon-film-resistors-blue-20-x-20-pcs-369256
gearbest - https://www.gearbest.com/diy-parts-components/pp_1291390.html?wid=1433363

LED + resistors + extras sets
amazon - https://www.amazon.com/ELEGOO-Electronics-Component-resistors-Potentiometer/dp/B01ERPXFZK/
amazon - https://www.amazon.com/HJ-Garden-Electronic-Component-Breadboard/dp/B077SLZWCR/
https://www.amazon.com/REXQualis-Electronics-tie-points-Breadboard-Potentiometer/dp/B073ZC68QG

There are also sets you can buy that include several items on this shopping list and might be a good value if you can find one without too much extra junk. To sum it up, you will need:
1 x Nano
1 x ISP
1 x USB-Serial
1 x breadboard
30-150 hook up wires
8+ LEDs
100s of resistors (all values)

Next post will deal with setting up our dev environment while we wait for our Chinese e-waste to arrive. Let me know if you have any questions or feedback.

# 16
>why can't I use the Arduino IDE on my Windows 10 machine?

They can if they use a virtual machine. It's very easy to set up with Virtual Box and it lets you passthrough USB ports to the VM, any computer made in the last 10 years will have basic virtualization compatibility built into the CPU(it might have to be enabled in BIOS though) so performance will be more than adequate for dev work even on a low powered machine. Much less hassle then dual booting and you can SSH into it.

I've been using DX for years but shipping times can be very slow with them and they might split up your order into several packages.

# 17
OP one question I had is about power. Maybe I missed it but I'm unsure how everything will be powered to operate. Does it come from the computer USB port, can we use batteries, or is there something else needed?

# 18
>>3754
Purchase made. Thanks Japanon, looking forward to it. Now I just have to install Linux on my laptop.

# 19
>>3755
I meant that we aren't going to be using that typical windows/arduino setup, but rather linux. If you can run and develop on linux in a VM, by all means, go for it. I used to use DX years ago in the States, but I've been using banggood recently. Better prices in my experience and shipping takes about 1-2 weeks (right next door to Japan, YMMV.)

>why linux anyway?
Because all decent robots run it or a variant thereof. When we use an SBC for higher-level control or a server for data logging, that's going to be running linux too, so we might as well get familiar.

>>3756
For now, we can pull power through either the ISP or the USB-Serial converter. It's only when we get into powering servos and motors that we would need a dedicated breadboard power supply or external higher-voltage supply (like 12V for BLDC motors.)

>>3757
Cool shit.

# 20
>>3758
>For now, we can pull power through either the ISP or the USB-Serial converter
Thanks for the info OP.

>Linux
I absolutely support this myself.

# 21
Any chance we can do this on OpenBSD OP? Apparently Linux is going down the tubes. :(
https://lkml.org/lkml/2018/9/16/167
https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=8a104f8b5867c682d994ffa7a74093c54469c11f

# 22
>>3759
>I absolutely support this myself.
No longer. Still better than Windows for the time being.

# 23
>>3760
I read that, too. That's a giant poz load up our collective ass. I guess we can put that on the to-do list then: find a lightweight Linux alternative for SBCs. In the meantime, though, Linux is what we got. Which we'll be setting up to program with real soon once I get a feel for where everyone is at and just how basic we have to start from. 

Right now, I just finished a serial control system with the Atmega328p for an automated indoor grow setup I've been working on. Takes 1-byte commands over uart from a PC into a ring buffer, executes them, and sends the results back. Got it taking ambient temp, humidity, LED heatsink temp, controlling pumps and LEDs via relays, PWM fan control, the works. Practice, practice. Also getting some resources together for people to look over while we wait for our parts and shit.

# 24
Some reading material while you wait:

Pic related. The Nano pinout. Save this, you'll want to refer it before plugging stuff in since the port and pin names do not match up with what's printed on the PCB.

The Atmega328p datasheet. This is your bible. Yes, it's a million pages. No, you don't have to read it all. We'll be referring to it a lot though, mainly to get the names of important registers and which bits to flip to get them to do what we want.
http://ww1.microchip.com/downloads/en/DeviceDoc/Atmel-42735-8-bit-AVR-Microcontroller-ATmega328-328P_Datasheet.pdf

A decent little introduction to C programming in an embedded context. First half, up until it gets into Arduino-specific functions, is worth a read.
http://www.dissidents.com/resources/EmbeddedControllers.pdf

# 25
>>3760
I think the most important thing is that you are using something Unix-like, that is to say you are working from Bash (or Zsh or w/e) and not a GUI. 

If you don't have a lot of Linux or Unix experience, you should use Ubuntu (inb4 "Ubuntu is hugely pozzed", the important part for newbs is they don't get blocked figuring out how to get their WiFi to connect or w/e). If you have a lot of Linux or Unix experience, then you already know that choosing a BSD or other non-Linux might introduce some issues that we won't be able to debug, and the choice is yours.

Linux only got pozzed yesterday. We still don't know how it will shake out. In a year or two we'll know better if there is some need to move to a different kernel. Frankly, this probably doesn't matter that much unless you are a regular Linux contributor. From a userspace perspective, the kernel is pretty irrelevant. Most of the BSDs run Gnome and KDE. Whatever OS/kernel you choose, the Arduino programming tools are either going to be exactly the same or not provided/compile yourself. Your mileage may vary.

Just to reiterate, if you are a Linux/Unix newb, use a beginner friendly distro, such as Ubuntu, and join the IRC so me or Waifubots can support you. (The more popular distros also have lots of support everywhere on the internet.) If you don't have a second machine, use a virtual machine, because its much harder to fix Linux issues when your only box can't open a web browser.

# 26
OK, I ordered my parts OP.
https://www.amazon.com/gp/product/B0775XQXRB - nano 5pk
https://www.amazon.com/gp/product/B01FDD4EP0 - usbtinyisp
https://www.amazon.com/gp/product/B072K3Z3TL - usb to ttl
https://www.amazon.com/gp/product/B073ZC68QG/ - breadboard kit + pwr
https://www.amazon.com/gp/product/B01N8W9LQ7 - 9V 2A adapter
Jeff Bezos promised me personally that everything would be here by Wednesday. :^)

I hope that should cover what I need for now. I wanted to have more than one nano in case i bricked one and also to play around with I2C and other internetworking approaches.

# 27
>>3764
Basically this.

>>3765
That's a nice setup there. You really went all out.

# 28
>>3766
Thanks. Really looking forward to these classes Sensei.

# 29
Excellent help, even though I have my own Chinese kit which I still haven't gotten to, I may want to get some of the recommended parts so we're on the same page. Thanks to topics like this and the thingiverse links I can see the general direction where we are headed and an actual way to start prototyping, since before I only see Disney imagineer and university level animatronics which look impossible and expensive to replicate.

# 30
>>3766
Japanon, can you tell us what packages we need to install, such as for a standard Debian derivative?

# 31
>>3769
Right, might as well get started with the PC side stuff while we wait for our parts. 

LESSON 1 - LINUX DEVELOPMENT ENVIRONMENT SETUP and INTRO TO AVR-C PROGRAMMING

I will assume you have a Linux environment set up and can use your respective package manager to install stuff, apt, pacman, whatever it may be. If not, speak up and we'll straighten you out.

To develop with AVR C, will need to install the following packages: make, avr-libc, avrdude, binutils-avr, gcc-avr, and gdb-avr

On a debian-based distro at least, open up a terminal, update your lists with:

```cpp
sudo apt-get update```

and then run the following:

```cpp
sudo apt-get install make avr-libc avrdude binutils-avr gcc-avr gdb-avr```

Reply yes to everything. There may be more dependencies installed depending on your system. Go ahead and install those too.

Now you're going to want a programming-oriented text editor of some sort. I've used and liked notepad++ and Geany, using Geany now. If you're just getting into programming, keep it simple and use a basic editor like the ones I mentioned and not a full-blown IDE like eclipse or visual studio. Let me know if anyone uses anything else they'd recommend.

Next, we'll set up a project folder, makefile, and compile a simple AVR C project to test.

# 32
>>3771
OK, I followed your instructions on my Ubuntu box and everything went fine, no errors.

>Let me know if anyone uses anything else they'd recommend.
I use jucipp. It is in fact a simple IDE but a quite simple one. It supports CMake and Ninja directly. I've been using it for a good while now.
https://gitlab.com/cppit/jucipp
And regrettably since virtue-signalling politics apparently must now be considered in any software project (uggh) I can also tell you that the project is run by a small team of Scandinavian White men, has recently moved off SJWhub and over to GitLab instead, has no CoC, and uses the MIT license.

>Next, we'll set up a project folder, makefile, and compile a simple AVR C project to test.
Sounds good, I think I'm ready!

# 33
>>3771
>Reply yes to everything.
Yes.
>Not Vim Mustard Race
Tsk.
For newbs that aren't ready for the glory of modal editing, what about sublime? That's what I used before I ascended.

# 34
>>3773
==VIM MUSTARD RACE==
Yes, I agree Dollfan. I think Sublime is probably a good choice for beginners as well.

# 35
LESSON 1 CONTINUED - BARE MINIMUM PROJECT

Alright, let's set up a little test project. Don't need to worry about the code yet, just copy and paste for now. First, let's make a new folder for our code. Call it avr_test or waifu_test or whatever you want. Inside that folder, let's make three new files and call them: "main.c", "main.h", and "Makefile". Open all three of them with your text editor. Into main.c paste the following:

```cpp
#include <avr/io.h>
#include <util/delay.h>
#include "main.h"

int main(void)
{
    DDRB |= _BV(DDB5); // set pin 5 of PORTB for output

    PORTB = 0x00; // set all PORTB pins low
    
    while (1)
    {
        PORTB = PORTB ^ (1 << DDB5); // toggle pin 5 of PORTB
        
        _delay_ms(1000); // wait 1 second
    }
    
    return 0;
}```

Into main.h paste the following line:

```cpp
int main(void);```

And lastly, into Makefile, paste this:

```cpp
CC=avr-gcc
OBJCOPY=avr-objcopy

CFLAGS=-Os -Wall -DF_CPU=16000000UL -mmcu=atmega328p

main.hex: main.elf
	${OBJCOPY} -O ihex -R .eeprom main.elf main.hex

main.elf: main.o
	${CC} $(CFLAGS) -o main.elf main.o
	
main.o: main.c
	${CC} $(CFLAGS) -c main.c -o main.o

flash: main.hex
	avrdude -F -V -c usbtiny -p ATMEGA328P -b 115200 -U flash:w:main.hex

clean:
	rm main.elf main.hex main.o```

Save all three of those files and you should be all set to compile.

# 36
OK. Now open up a terminal and type "make". If all goes well, you'll get the following:

```cpp
avr-gcc -Os -Wall -DF_CPU=16000000UL -mmcu=atmega328p -c main.c -o main.o
avr-gcc -Os -Wall -DF_CPU=16000000UL -mmcu=atmega328p -o main.elf main.o
avr-objcopy -O ihex -R .eeprom main.elf main.hex```

You should now have three more files in your folder: "main.elf", "main.hex", and "main.o". The hex file is what we burn onto the AVR. Now type "make flash". If you have a usbtiny ISP plugged in and hooked up to your Nano, you'll get the following:

```cpp
avrdude -F -V -c usbtiny -p ATMEGA328P -b 115200 -U flash:w:main.hex

avrdude: AVR device initialized and ready to accept instructions

Reading | ################################################## | 100% 0.01s

avrdude: Device signature = 0x1e950f (probably m328p)
avrdude: NOTE: "flash" memory has been specified, an erase cycle will be performed
         To disable this feature, specify the -D option.
avrdude: erasing chip
avrdude: reading input file "main.hex"
avrdude: input file main.hex auto detected as Intel Hex
avrdude: writing flash (164 bytes):

Writing | ################################################## | 100% 0.49s

avrdude: 164 bytes of flash written

avrdude: safemode: Fuses OK (E:FF, H:D9, L:FF)

avrdude done.  Thank you.```

and your LED should be blinking away.
If not, you'll get the following error:

```cpp
avrdude -F -V -c usbtiny -p ATMEGA328P -b 115200 -U flash:w:main.hex
avrdude: Error: Could not find USBtiny device (0x1781/0xc9f)

avrdude done.  Thank you.

Makefile:16: recipe for target 'flash' failed
make: *** [flash] Error 1```

That's all there is to it.

# 37
I don't have my hardware in yet, but I got these from the compile so all seems good so far:

```cpp
avr-gcc -Os -Wall -DF_CPU=16000000UL -mmcu=atmega328p -c main.c -o main.o
avr-gcc -Os -Wall -DF_CPU=16000000UL -mmcu=atmega328p -o main.elf main.o
avr-objcopy -O ihex -R .eeprom main.elf main.hex```

# 38
Can you describe the Makefile and what it's doing for us please?

# 39
Probably getting ahead of myself but also one other question I had
>and your LED should be blinking away.
Is this an LED directly on the Nano package, or do we need to do breadboard wiring up first? Pin 5 on Port B?

```cpp
        PORTB = PORTB ^ (1 << DDB5); // toggle pin 5 of PORTB```

# 40
>>3779
Yeah, PB5 is wired to the LED on the board, the rightmost of the 4 LEDs on the pinout, the one marked "L". But, if you wire up an LED and a resistor to that pin, that will blink too.

# 41
>>3780
I see thanks. My hardware should be in later today so I'll try this then.

# 42
>>3778
Makefiles are like magic to me sometimes but I'll try. These first three lines are variable definitions. The contents of those lines get copied into the lines below. For instance, 

```cpp
CC=avr-gcc```

```cpp
CFLAGS=-Os -Wall -DF_CPU=16000000UL -mmcu=atmega328p```

means that wherever we see ${CC} and ${CFLAGS}, those values get copied in and we end up with lines like

```cpp
avr-gcc -Os -Wall -DF_CPU=16000000UL -mmcu=atmega328p -c main.c -o main.o```

You probably saw that in the output when you compiled.

What else… The bits on the left, like "main.hex", are our make targets. To the right of the ":" are the dependencies for that target. So when you type "make", make starts are the first target, which is our hex file we need to flash, main.hex, which requires main.elf, which requires main.o, which requires main.c. main.c exists already, so everything besides that gets compiled and linked and all that and we end up with main.hex.
This bit

```cpp
flash: main.hex
	avrdude -F -V -c usbtiny -p ATMEGA328P -b 115200 -U flash:w:main.hex```

is not required by anything else, so we need to call it by name by typing "make flash". Notice it requires main.hex? If you didn't make that already, it'll get made now. Typing "make clean" will run the following:

```cpp
clean:
	rm main.elf main.hex main.o```

which doesn't require anything, and just deletes all the intermediate files we got in the make process. Run that and you'll notice main.o, main.elf, and main.hex are gone now. Don't fuck up and add your .c files to this.

# 43
>>3782
Thanks you explained that pretty well actually.

# 44
>>3783
I'll go into more detail about the compiling and linking process later, as well as why we need to pass certain cflags to the compiler and linker and stuff (because it will break in extremely hard to debug ways if we don't, see this bit about the 8515 here https://www.microchip.com/webdoc/AVRLibcReferenceManual/groupdemoproject_1demo_project_compile.html)

# 45
>>3784
Posted that because I remember a while back struggling with inexplicable behavior in perfectly good code for probably a solid week because I forgot to pass the processor type to the linker as well as the compiler.

# 46
>>3785
thanks, i see it's packed with info.

# 47
OK, good news on my update. Everything came in safe and sound and after a bit of fiddling with the host/guest config for Virtualbox I got everything connected up properly and voilà, I was able to perform the flash and the Nano promptly began flashing as expected. It now flashes correctly whenever power is applied, not ISP needed.

I'm currently on a Windows host with the machine I'm currently working with, and I had to go download the proper drivers for the USBtinyISP first before the platform would recognize it.
https://learn.adafruit.com/usbtinyisp/download

After that, I had to get the client to see it across the virtual USB port provided by Virtualbox.
1. Shutdown the guest.
2. Plug in the device, let the host grab it.
3. In the host, go to virtual box, and edit the configuration for the guest. In the "Ports" tab, go to USB and add a filter to include the plugged in device.
4. Unplug the device.
5. Start the guest OS.
6. When the guest os is running, plug in the device.

Then as I said I was able to flash the Nano successfully first time, so I guess I'm good to go at this stage Sensei.

http://magaimg.net/img/6780.jpg
http://magaimg.net/img/677y.png

# 48
>>3787
>began blinking as expected*
etc…

# 49
>>3787
Thanks for the heads up, I'm currently tinkering with my Uno devkit in a Windows environment, but I just bought a Nano (the seller mentioned there was a bootloader installed in it, I guess I'll have to flush it out) and I was worried there about the USBtinyISP as it was mostly out of stock except for one that I'm crossing fingers on.

(In case you are wondering why I don't order from Amazon, I was burned by Customs countless times so I'm using the Alibaba-affiliated e-commerce site Lazada which already paid its bribes so all my packages actually arrive)

# 50
>>3787
Nice. Glad to see your fuses were burned right out of the box. I was going to touch on those before someone got the ol' slow blink because their chip is set to run off the internal 1Mhz oscillator.

>>3789
It looks like you've already ordered the USBtinyISP but have you looked into "AVR as ISP"? That's where you program your uno to be a USB programmer for other AVRs, which is basically what the USBtinyISP is with it's ATTINY2313.

# 51
==LESSON 2 BLINK REVISITED - FUSES, FUNCTIONS, and MULTI-FILE COMPILATION==

In this lesson we break the blinking LED functionality into it's one function in its own .c file. We edit main to include this file and use its functions. We also tweak the makefile to make it more flexible, and also add an option to quickly burn the fuse bits (I will go into a little detail on these, but not so much).

Let's start by switching up our project folder structure a bit. Before, we had main.c, main.h, and a Makefile in our project folder. Let's move the three of those (and any object and binary files left over) into a new folder in this directory, and let's call it "01_blink". Make a new folder alongside that one and let's call it "02_blink_again". From 01_blink, let's copy those three files we've been working on: main.c, main.h, and Makefile. We're not going to make so many changes this time, so editing those will save a little typing at least. Now, in addition to those three, we need a couple of new files as well so go ahead and make them now: "blink.c" and "blink.h". See pics. Even if you aren't familiar with coding in C yet, you may have noticed a trend at this point: main.c and main.h, blink.c and blink.h. The ".h" files are header files. They contain function and struct declarations, macro declarations, and similar. Their ".c" counterparts contain the actual code, the function definitions and such. Don't worry too much about them right now.

Let's get to the code now. Open up those five files in your editor, hopefully it will let you move between them quickly like browser tabs, because we're going to jump around a bit. First, let's make that Makefile a little more generic and useful. All Makefiles are named just that: "Makefile". That's what make looks for when you run it. Let's add a comment at the top of ours so while we can't change the name, at least while editing it we know which one it is. On the first line, insert a comment starting with a "#" letting you know what it's for. I did

```cpp
# robowaifu learning project 02 - blink again```

You can write whatever; it won't be used by make in any way. I know a couple of you guys went and ordered USBtinyISPs, that's cool. However, there are different programmers out there, like the popular USBASP or AVRasISP, so I want to make the makefile a little more flexible to accommodate everyone. After the CFLAGS variable definition, let's add the following two lines:

```cpp
ISP=usbtiny
BAUD=115200```

This specifies which programmer we're using at and what baud (bits per second, speed) we're talking to the chip at. For the USBtinyISP, 115200 baud works great, for others, you may need to go slower to flash without errors. You can change both parameters here and not have to mess with the rest of the file. We're not done with the Makefile yet but me up with any questions or comments you might have so far.

Next post: FUSES

# 52
>>3793
MINT MUSTARD RACE
Cinnamon really is the best DE tbh.

look forward to the next lesson Sensei.

# 53
==LESSON 2 CONTINUED - FUCKING FUSES==

"Fuses" are bytes we burn onto the AVR chip to alter some settings affecting how it boots, runs, and more. Here we can set the clock source, whether it's the internal resonator or an external crystal. We can set the start-up time, more to give your voltage source time to stabilize after a power-on, or less if you need it running code within a few milliseconds of being powered up. You can change these settings in all sorts of ways, some of which will leave it unable to talk to the ISP, which will BRICK it. So don't play with setting them randomly just to experiment. There are three fuses for the AVR, the high fuse, the low fuse, and the extended fuse. Each one is 1-byte in size and typically written in hexidecimal format. Look up binary, decimal, and hexidecimal if you aren't familiar with those. Also save pic related for a quick reference if you need it. As for what values to burn onto our Atmega328p, you can calculate them by reading the datasheet and seeing which features you need and which bits to toggle to get them. Or, you can use a handy calculator like the one at http://eleccelerator.com/fusecalc/fusecalc.php?chip=atmega328p Or, you can do like we're going to do and use the default settings for the Arduino Nano, which are as follows: extended fuse - 0xFD, high fuse - 0xDA, and low fuse - 0xFF. Let's add those to our Makefile. That will give us an easy way to flash new boards we might acquire, or if we need to change the fuse settings, to be able to do it in just one place in the file. After ISP and BAUD, add the following three lines:

```cpp
EFUSE=0xFD
HFUSE=0xDA
LFUSE=0xFF```

OK. Now let's use all of these new variables that we've set up. Go down a few lines and find the "flash" make target. It should look like this:

```cpp
flash: main.hex
	avrdude -F -V -c usbtiny -p ATMEGA328P -b 115200 -U flash:w:main.hex```

Note that the programmer type and baud rate are hard coded in there. Let's change that now to use our variables we defined last post:

```cpp
flash: main.hex
	avrdude -F -V -c ${ISP} -p ATMEGA328P -b ${BAUD} -U flash:w:main.hex```

Cool. Now about those fuses, how are we going to burn them onto the chip? With a new make target we'll call "fuses". Add the following two lines between the "flash" and "clean" targets:

```cpp
fuses:
	avrdude -F -V -c ${ISP} -p ATMEGA328P -b ${BAUD} -U efuse:w:${EFUSE}:m -U hfuse:w:${HFUSE}:m -U lfuse:w:${LFUSE}:m```

We can now burn the fuses simply by typing "make fuses" into the terminal. Notice where our variables are inserted into the line. Typing make fuses should give you the output in pic 2. This line will tell you the final fuse settings after burning:

```cpp
avrdude: safemode: Fuses OK (E:FD, H:DA, L:FF)```

Let me know if you don't know wtf we're doing or why. Also taking requests for topics anyone would like to see covered eventually, like a sensor they'd like to use or whatever.

NEXT - MULTI-FILE COMPILATION

# 54
>>3796
I'll get the code up on gitlab or bitbucket too then, when I get the time. Makefile up to this point:

```cpp
# robowaifu learning project 02 - blink again

CC=avr-gcc
OBJCOPY=avr-objcopy

CFLAGS=-Os -Wall -DF_CPU=16000000UL -mmcu=atmega328p

ISP=usbtiny
BAUD=115200

EFUSE=0xFD
HFUSE=0xDA
LFUSE=0xFF

main.hex: main.elf
	${OBJCOPY} -O ihex -R .eeprom main.elf main.hex

main.elf: main.o
	${CC} $(CFLAGS) -o main.elf main.o
	
main.o: main.c
	${CC} $(CFLAGS) -c main.c -o main.o

flash: main.hex
	avrdude -F -V -c ${ISP} -p ATMEGA328P -b ${BAUD} -U flash:w:main.hex
	
fuses:
	avrdude -F -V -c ${ISP} -p ATMEGA328P -b ${BAUD} -U efuse:w:${EFUSE}:m -U hfuse:w:${HFUSE}:m -U lfuse:w:${LFUSE}:m  

clean:
	rm main.elf main.hex main.o```

# 55
==LESSON 2 CONTINUED - MULTI-FILE COMPILATION==

I said earlier that we were going to break out the LED functionality to another file. Why? Because it's just good practice. Keep all the LED blinking code in one file and, when we need to blink an LED in a project (or interface with a sensor, drive a motor, whatever your .c file handles), we can just include it. Anyway, let's just get the code out there and then I'll go over it all. Again, don't worry if I skim over the code too much, the goal here is learning to compile and link multiple files in a project.
The updated main.c:

```cpp
#include <avr/io.h>
#include <util/delay.h>
#include "main.h"
#include "blink.h"

int main(void)
{
    DDRB |= (1 << DDB5); // set pin 5 of PORTB for output

    PORTB = 0x00; // set all PORTB pins low
    
    while (1)
    {
        blink_once(); // blink once a second
        
        blink_twice(); // blink twice a second
        
        blink_four_times(); // blink four times a second
        
        blink_eight_times(); // blink eight times a second
        
        _delay_ms(1000); // pause for a second before looping back to beginning
    }
    
    return 0;
}```

main.h:

```cpp
int main(void);```

blink.c:

```cpp
#include <avr/io.h>
#include <util/delay.h>
#include "blink.h"

void blink_once(void)
{
    PORTB |= (1 << PB5); // set pin 5 of PORTB high
        
    _delay_ms(500); // wait 500 milliseconds
    
    PORTB &= ~(1 << PB5); // set pin 5 of PORTB low
        
    _delay_ms(500); // wait 500 milliseconds
}

void blink_twice(void)
{
    uint8_t i = 0;
    
    for (i = 0; i < 2; i++) // do the following two times
    {
        PORTB |= (1 << PB5); // set pin 5 of PORTB high
        
        _delay_ms(250); // wait 250 milliseconds
    
        PORTB &= ~(1 << PB5); // set pin 5 of PORTB low
        
        _delay_ms(250); // wait 250 milliseconds
    }
}

void blink_four_times(void)
{
    uint8_t i = 0;
    
    for (i = 0; i < 4; i++) // do the following four times
    {
        PORTB |= (1 << PB5); // set pin 5 of PORTB high
        
        _delay_ms(125); // wait 125 milliseconds
    
        PORTB &= ~(1 << PB5); // set pin 5 of PORTB low
        
        _delay_ms(125); // wait 125 milliseconds
    }
}

void blink_eight_times(void)
{
    uint8_t i = 0;
    
    for (i = 0; i < 8; i++) // do the following four times
    {
        PORTB |= (1 << PB5); // set pin 5 of PORTB high
        
        _delay_ms(63); // wait 63 milliseconds
    
        PORTB &= ~(1 << PB5); // set pin 5 of PORTB low
        
        _delay_ms(62); // wait 62 milliseconds
    }
}```

blink.h

```cpp
void blink_once(void);
void blink_twice(void);
void blink_four_times(void);
void blink_eight_times(void);```

Next - updated Makefile and explanation

# 56
>>3789
Glad to help. Hope everything arrives safe and sound and works right out of the gate bro. Good luck.

# 57
Updated Makefile:

```cpp
# robowaifu learning project 02 - blink again

CC=avr-gcc
OBJCOPY=avr-objcopy

CFLAGS=-Os -Wall -DF_CPU=16000000UL -mmcu=atmega328p

ISP=usbtiny
BAUD=115200

EFUSE=0xFD
HFUSE=0xDA
LFUSE=0xFF

main.hex: main.elf
	${OBJCOPY} -O ihex -R .eeprom main.elf main.hex

main.elf: main.o blink.o
	${CC} $(CFLAGS) -o main.elf main.o blink.o
	
main.o: main.c
	${CC} $(CFLAGS) -c main.c -o main.o
	
blink.o: blink.c
	${CC} $(CFLAGS) -c blink.c -o blink.o

flash: main.hex
	avrdude -F -V -c ${ISP} -p ATMEGA328P -b ${BAUD} -U flash:w:main.hex
	
fuses:
	avrdude -F -V -c ${ISP} -p ATMEGA328P -b ${BAUD} -U efuse:w:${EFUSE}:m -U hfuse:w:${HFUSE}:m -U lfuse:w:${LFUSE}:m  

clean:
	rm main.elf main.hex *.o```

OK. Let's take a look at main.c. Look at line 4 - we have one more include: "blink.h". Take a look at blink.h. It's just 4 lines with the names of functions (don't worry about the "void" bits right now). What '#include "blink.h"' does is basically copying and pasting the contents of blink.h right into main.c. This must be before those functions are called. This lets the compiler know that when it sees one of these functions called down below in main.c, like "blink_once();" on line 14, that this is a function that exists (somewhere) and that we don't need to supply any extra parameters to use it. What those functions do, however, is all up to blink.c. Take a look in blink.c to see how those functions are implemented. Don't sweat the details right now but the comments should clue you in on the workings. Inside the while (1) infinite loop, you'll see those 4 functions called in order, followed by a 1 second pause. Now that we've included blink.h in main.c, we can use these functions in any combination, any way we like.
>What's a function, anyway?
A function is a reusable piece of modular code. It can be called any number of times, from wherever it's included. Functions can call other functions. Large functions can contain many smaller functions. I suggest looking them up. We'll touch on them again when we need to pass parameters and return stuff.

And finally, the multiple compilation part. Take a look at the new Makefile. We have a new make target now: blink.o. This is compiled just like main.o. But what do we need blink.o for anyway? It's a requirement of main.elf now:

```cpp
main.elf: main.o blink.o```

What this basically says is that to use the code contained within blink.c in our main executable, our binary, we need to link the compiled main.c code (the object file main.o) and the compiled blink.c code (blink.o) together (so when we call those blink functions from main, stuff actually happens). And that's the gist of it. Go ahead and call "make flash" if you want to see the new code in action.

The nitty-gritty of compiling, linking, objects, and whatnot are really outside the scope of what I'm trying to teach here but I'll be glad to field any questions you might have. Let me know if I can clarify anything; I'd like these threads to be more discussion-based rather than lecture-based, especially once we get in deep and have to lean on each more for research and debugging.

# 58
ありがと, ありがと Sensei.

This is truly excellent help. Thank you.

# 59
>>3801
いいえ、いいえ。どういたしまして。
こちらこそ、興味を持ってこのスレに参加してくれてありがとう。

Going on vacation for a couple of days from tomorrow so I won't be posting anything new but, I'll be around to discuss for the next few hours at least. Do some experimenting with what we've got so far though. Break it! Comment out lines in the files (# for Makefile, // for C files and headers). Look at the errors you get. Look them up. Move stuff around. Change the values in the delay functions. Notice the LED on times are the same as the off times. What if an LED was on for 100 ms and off for 900? On for 1ms and off for 9ms?

# 60
>>3802
このスレッドは文字通り /robowaifu/ の成功の鍵です。 拍手はあなたのものです。

good rest, Sensei.

# 61
>>3798
Also spot the typo from where I copy-pasted some code and didn't change the comment. kek

# 62
>>3805
>// do the following four times

# 63
>>3796
I have a question about text formatting in Makefiles. The 'fuses' make target runs pretty long and doesn't fit too well in my editor's view. Is there an accepted, standard way to continue this kind of statement on a new line? One that won't interfere with it's processing by the make program ofc. If that was doable I think it would help me out a bit.

# 64
OK, everything went well and seems to be OK. The Nano's LED is cycling through a blinking pattern and changing it's rate. Also thanks for the detailed explanations Sensei.

http://magaimg.net/img/67ha.png

# 65
I know you already went over the Makefile, but I still am not quite clear on how make choose which make target to perform when you issue it's command with no arguments like this

```cpp
make```

I'm guessing it just executes the first one in the Makefile or something? This one in our case

```cpp
main.hex: main.elf
	${OBJCOPY} -O ihex -R .eeprom main.elf main.hex```

then picks up the other dependencies from that first one? I do think I understand when you explicitly specify the make target to the command like this

```cpp
make flash```

Please pardon me if I missed it and you already answered this question.

# 66
>>3809
I did mention this above, yeah. When make is not supplied a target, it makes the first target in the file, which is main.hex. You can build each of the intermediate components by name if you really wanted to like:

```cpp
make blink.o
make main.o
make main.elf
make main.hex
make flash```

Use "make flash" if you want to make everything and flash in a single command.

# 67
>>3807
You can use a backslash to escape a newline character like 

```cpp
fuses:
	avrdude -F -V -c ${ISP} -p ATMEGA328P -b ${BAUD} -U efuse:w:${EFUSE}:m \
	-U hfuse:w:${HFUSE}:m -U lfuse:w:${LFUSE}:m  ```

Check out the manual for details on that at https://www.gnu.org/software/make/manual/html_node/Splitting-Recipe-Lines.html#Splitting-Recipe-Lines I just looked that up now btw, I didn't know it either.

# 68
So I'm working on the next lesson and I'd like some feedback. If you're following or interested in following along/contributing, let me know a bit about you. What direction would you like to see the curriculum go in? What is your skill level with electronics? Can you wire up a breadboard? Can you do Ohm's law and RC calculations? Can you program in C at all? Help me get a feel for your level and I can adjust the pace accordingly. Right now I'm trying to be as newbie friendly as possible. For instance, the next lesson will be all about low level stuff like AVR ports and pins, bit manipulation, and binary/hex/decimal/ascii conversion. What does everyone think so far?

# 69
>>3811
Ah, thank you. That's probably how I had the right instinct the first place – I subconsciously remembered the info from earlier.

>>3812
Oh good thanks. I was hoping it was something like that.

# 70
>>3813
>let me know a bit about you. 
I'm very hopeful we'll actually create real, working robowaifus from this board.

>What direction would you like to see the curriculum go in? 
Eventually I'd like to see these classes move on to the Beagle Bone Blue, once you've finished everything you want to do with simpler, cheaper boards like the Nano.

>What is your skill level with electronics? 
Basic. I have a feel for resistors, diodes, and SCRs and how to use them in very simple circuits.

>Can you wire up a breadboard? 
With pictures, yes certainly.

>Can you do Ohm's law and RC calculations? 
Probably, But I'd always have to look it up.

>Can you program in C at all? 
Yes.

>What does everyone think so far?
I think you're doing a great job. I hope eventually everyone here participates. Maybe there's a way to arrange things as a Beginner's class, and a Intermediate class?

# 71
>>3813
I actually have an EE degree though I work as an IT admin and I don't trust myself fully to take on electrical projects compared to a licensed engineer.  But otherwise yes to everything.  I'm new to the Arduino, single board computers such as raspberry pi and 3D printing though, since I spent most of my free time in the last decade in game development software plus its only recently that I actually have a decent living space to set up a 3D printer and work in robotics. I'm rushing through some windows tutorials and as soon as I finish setting up my linux environment and the Nano accessories arrive I'll go through lesson 1 here.  Playing with arduino on windows though, it's ridiculous what used to take a few hours erasing EPROMs and etching PC boards and programming in assembly language can be done in 30 minutes.  I also saw a kit… 16 sensors for roughly $11, looked like a steal and it seems as if they overproduced all these kits so if you want sensors its better to just buy these kits rather than buy them individually.  The major limitation to my project would be access to specialized chips and assemblies,  And just like Radio Shack in the US, local electronics parts stores all but disappeared so there's just online plus the superstore that carries only the most common components.

I'm also worried about mechanical designs since that is where I have zero experience in.

>>3815
Beagle Bone looks interesting.  But what do you think of a robowaifu being just a little bit more complex than your usual arduino kit, or just being a glorified Tickle Me Elmo TMX?  On the other hand we could work with progressively more complex motherboards, until such a time it would be great to have a full x86-64 machine (perhaps an Atom board?) running the robowaifu since that would make them full fledged Persocoms (although pozzed)

I suppose the theme of the board being DIY waifus pretty much means we will have to work with consumer grade, easily available stuff.

# 72
>>3816
>we will have to work with consumer grade, easily available stuff.
I concur, particularly the ARM platform. And the BB Blue is easily available and consumer-grade (<US$100) imo.

I think one thing we've learned at this stage is that many different paradigms are being explored all at the same time, as well it should be. Even along different paths some of us are working progressively towards an ultimate goal. 

For example in my case I'm approaching my ultimate goal **full-on Persocoms b/c raisins** like this:
>basic robowaifu software framework =>
>functional Visual Waifu to support viz and basic animations studies =>
>internal structural rigging and simulations to study kinematics and dynamics simulations =>
>AI development using the previous 3 systems for NN & ML tuned for irl control systems + =>
>Additional AI NLP work resulting in a reasonably functional chatbot waifu that can interact both with you and + =>
>A robowaifu simulation playground where she can live with you virtually and you can begin teaching her =>
>IRL structural designs based off all the foregoing lessons, initially prioritizing economy and lean design, ie, her working skeleton and the basics of audio and visual interaction w/ you and the real world =>
>Refined shell designs and fabrication techniques of her outer shell to go over her endoskeleton, along with numerous revisions all (re)integrating further refinements of all the s/w and h/w systems. By this stage we will well and truly be deep into the Systems Engineering territory =>
>Once we have a complex prototype working in the real world, it will be time to tackle the hard part: namely, making it simple and cheap while losing none of the research benefits =>
>Form legal entities and arrange for mass-production of the v1.0 RoboWaifu System =>
>??? =>
>Profit.

See? It's all so simple.
**                                         :^)**

But this literally is my plan. I estimate roughly 5 years to the first commercial robowaifus using this approach if all goes pretty much perfectly. This is no short-term approach tbh.

# 73
>>3817
>ie, just her working skeleton*

# 74
>>3813
>let me know a bit about you.
I'm a professional procrastinator. I wanted to experiment with this stuff for a while but it's thanks to you that I actually pulled the trigger. I bought what was needed to start out, set up a linux machine to dev on and started to blink some LEDs.

>What direction would you like to see the curriculum go in?
I don't really know, I catch myself aiming at the stars too often to be sure of saying something grounded. Is it feasible in the future to tackle FPGAs and do something simple for beginners with them?

>What is your skill level with electronics?
Hopefully I know the Basics. I had pic related as a kid, does it count?

>Can you wire up a breadboard?
Sure, seemed easy to me, maybe less so avoiding spagetti but everything was functional and I make sure not to fry anything.

>Can you do Ohm's law and RC calculations?
Yes, they are simple equation.

>Can you program in C at all?
I have a bit more experience in python, but I can program simple stuff in C. I'm self taught tho. I went to school hoping to learn but I had the bad luck of having a teacher that sat on his laptop doing his own business instead of working.

>What does everyone think so far?
You are doing god's work japanon, from the little roadmap you mentioned you know what you are doing. You have no complaints from me.

# 75
>>3815
Thanks for the feedback.
>Eventually I'd like to see these classes move on to the Beagle Bone Blue, once you've finished everything you want to do with simpler, cheaper boards like the Nano.
That's a pretty cool board. Can't really compare it to the Nano, though. One is a multi-core SBC running a full-fledged operating system and the other is a low cost 8-bit microcontroller. We will do programming in C for SBCs and integrate it with the Nano later though. However, to keep costs down for everyone, I will probably be using the Orange Pi Zero - https://www.aliexpress.com/store/product/New-Orange-Pi-Zero-H2-Quad-Core-Open-source-development-board-beyond-Raspberry-Pi/1553371_32760774493.html Should be able to get it and an SD card and power supply for <20 USD. I have two here that I'm experimenting with. Can't say for certain yet though, it may be worth a couple dollars more to get one the orange pis with more features.

>Maybe there's a way to arrange things as a Beginner's class, and a Intermediate class?
We'll see. I'll refine stuff as we go and archive it for reference. I'd like to keep everyone at the same level and pace though, which is why I'm starting at the very basics. It's not comprehensive either so, if you've got the time, by all means experiment with your own programs and use other tutorials and books and stuff for independent study.

# 76
>>3816
So you've got a decent background then. Cool. Isn't it crazy what's out there these days? When I was in EE back in 2004, we had to assemble and solder our own dev boards with a fat 40-pin CDIP PIC micro and programmed in Basic. Now they got Arduino and Raspberry Pi kits for sale in the university book store. And the kind of sensors and shit you can get from China for pennies. If I had that stuff back then…

>I'm also worried about mechanical designs since that is where I have zero experience in.
I too have no real experience with mechanical design or fabrication. My last robot was a two-wheeled mobile type with all the parts made from plexiglass and angle aluminum, with a dremel and a drill press.

>>3819
Thanks for the feedback. That kit's fucking rad. 
>FPGAs
>beginners
I don't know. I doubt it. I don't think we'll be doing any kind of real-time digital signal processing that requires an FPGA. Dev boards aren't that cheap either (like 50+ USD last I looked). The SBCs out there are powerful enough for anything we're going to write, I would think. Hell, even an Atmega328p can run pose estimation algorithms on 6-axis IMU data in real time. I can really only see an FPGA being used from something like getting depth data from stereo cameras in real time and passing that to the main computer, or offloading something like a neural-net based voice synth from the main cpu, integrating a microphone array, etc. Fast, high-throughput audio/visual stuff.

# 77
==LESSON 3 - 8-BIT COUNTER AND DISPLAY==

This lesson we will finally be making a circuit on our breadboards. If you don't know how a breadboard works, have a quick read of this page https://learn.sparkfun.com/tutorials/how-to-use-a-breadboard/anatomy-of-a-breadboard for the basics. We're going to be sticking our Nano into one side like it was a DIP chip, and setting up a row of 8 LEDs next to it. I've attached both a terrible fritzing diagram and a photo of the circuit. The connections are simple. I bend the legs of my LEDs like in the pic with a pair of needle-nose pliers (nice for giving good, sharp bends to through-hole components) so they can be stuck in the DIP slot or on the power rails. On my board, I've got the negative legs stuck in the one ground rail and the resistors bend like a staple and inserted across the DIP slot. Make sure you get the polarity of the LEDs right. Look up how to tell which end is which if you aren't familiar. The wiring between the resistors and the Nano is hard to see but it goes like this: 

```cpp
Nano pin D8 (PB0) -> LED 1 resistor
Nano pin D9 (PB1) -> LED 2 resistor
Nano pin D10 (PB2) -> LED 3 resistor
Nano pin D11 (PB3) -> LED 4 resistor
Nano pin D12 (PB4) -> LED 5 resistor
Nano pin D5 (PD5) -> LED 6 resistor
Nano pin D6 (PD6) -> LED 7 resistor
Nano pin D7 (PD7) -> LED 8 resistor```

Don't forget to connect the Nano's GND pin (there are two of them, either works)to the breadboard ground or you'll have an open circuit and nothing will work. Take a minute to set that up. Now we have 8 LEDs lined up in a row, each one connected to its own digital I/O pin on the Nano. We'll use this as a simple display to show 8-bit values (0-255). Next post: the code.

# 78
==LESSON 3 CONTINUED - MAIN==

Let's start by making another folder: "03_count". In there, we're going to have the following five files: main.c, main.h, display.c, display.h, and of course, Makefile. Let's start with main.c and main.h. main.c:

```cpp
#include <avr/io.h>
#include <util/delay.h>
#include "main.h"
#include "display.h"

int main(void)
{
    display_setup(); // set up ports and pins for our display
    
    uint8_t count = 0x00; // initialize an unsigned 8-bit integer for our counter, set it to 0
    
    while (1) // infinite loop
    {
        display(count); // display the current value of count on our LEDs
        
        count++; // increment count by 1
        
        _delay_ms(500); // pause for half a second before looping back to beginning
    }
    
    return 0;
}```

main.h:

```cpp
int main(void);```

These should look familiar by now. Take a look at main.c. At the top, we have our usual includes. 'avr/io.h' lets us use AVR register names like DDRB, PORTC, etc. It also lets us use types like 'uint8_t' which is an unsigned 8-bit integer, or, an unsigned char. Check out this link for an intro to C types, their sizes in memory, and what values they can hold - https://intellipaat.com/tutorial/c-tutorial/c-data-types/ After the includes, we have our main function. Once in the main function, the first thing that's executed is a function we've written called "display_setup". The comment says what it does: initializes the Nano's ports to use the pins we've connected as digital outputs. Don't worry about the implementation just now. Next, we have the line "uint8_t count = 0x00;". What this does is create a new variable for us to use and sets it to an initial value of 0. I have written it in its hexidecimal notation of '0x00'. You can write it as uint8_t count = 0; or uint8_t count = 0b00000000; if you like; it's all the same to the compiler. Read a bit about binary, decimal, and hexadecimal number systems if you aren't familiar: https://www.embedded.fm/blog/2016/6/14/an-introduction-to-binary-and-hexadecimal https://learn.sparkfun.com/tutorials/hexadecimal/introduction Ok, so our setup is done. Let's enter the main loop then. First thing that does is display our value, "count". What's the value of that again? It should currently be 0. Zero in 8-bit binary is of course, "0000 0000" (space added for clarity). Writing a 0 to a digital pin will set the voltage on that pin to ground, or 0 volts. With the voltage being the same on each end of the 8 little circuits we've made (AVR pin -> resistor -> LED -> ground), no current will flow, and all of the LEDs will be dark. 
As the title of this lesson implies, we're not just trying to display "0" in binary, we want to count up from 0. That's what the next line does: "count++;" This is one way of incrementing in C. Other ways include writing "count += 1;" or "count = (count + 1);". It increases the value of count by 1. Next, we wait for half a second so that we can follow along with what is happening. Then it's back to the beginning of the loop. By looping like this indefinitely, you'll see the following take place: our value is 0, the LEDs are all off, pause, our value is now 1, the rightmost (LSB) LED is lit, the others are dark, pause, our value is 2, the second-to-right LED is lit, the rightmost is off now, pause, and so on.

Next: The LED implementation - display.c, display.h

# 79
Very silly question, are we powered using external supply (9V I believe) in most of these lessons? Because while skimming project tutorials for UNO most of them assume 5V USB supply, and using the external supply would mess up the logics.

# 80
Ah nevermind I see this being used (this is built into the Uno).

# 81
>>3824
>>3825
Actually, I'm still using just the USB programmer's power at the moment. If you supply power to the board by some other means, make sure that it works OK with your programming method. Some programmers will have a jumper on them that needs to be moved if they're going to supply power to the board or if an external source will. Some will also have a jumper to let you switch between 5V and 3.3V power and logic, make sure you got it on 5.

Lesson continuation in a few.

# 82
With our LEDs and 330 ohm resistors, each one will draw ~10 milliamps when turned on, for a total of about 80 mA. Each pin of the Atmega328p can supply up to 40 mA max, with a total of 200 mA for the whole chip (see datasheet chapter 32). A computer's USB 2.0 port will supply up to 500 mA max while a USB 3.0 port will do 900 mA. Typically USB programmers and USB-serial converters will supply 150-250 mA so we're alright for the time being. Always a good idea to check that your own setup is running in spec, though.

# 83
>>3826
>>3827
Ah ok, this confirmed some things, really appreciate it.  Will use proper power rails once we hit 20+ LEDs etc.

# 84
==LESSON 3 CONTINUED - display.c, display.h==

Let's start by adding the code to these two files. display.c:

```cpp
#include "display.h"

void display_setup(void)
{
    // set up the 8 output pins we're using and clear them
    
    DDRB |= PB_MASK; // set pins 0,1,2,3,4 of PORTB as output
    DDRD |= PD_MASK; // set pins 5,6,7 of PORTD as output

    PORTB &= ~(PB_MASK); // set PORTB pins 0,1,2,3,4 low (xxx0 0000)
    PORTD &= ~(PD_MASK); // set PORTD pins 5,6,7 low (000x xxxx)
}

void display(uint8_t num)
{
    // write the value of num to the display as a series of 8 bits
    
    PORTB = (num & PB_MASK); // (xxxx xxxx) & (0001 1111) = (000n nnnn)
    PORTD = (num & PD_MASK); // (xxxx xxxx) & (1110 0000) = (nnn0 0000)
}```

display.h:

```cpp
#include <avr/io.h>

#define PB_MASK 0x1F // 0001 1111
#define PD_MASK 0xE0 // 1110 0000

void display_setup(void);
void display(uint8_t num);```

This time, let's begin by taking a look at the header file first. On the first line of display.h, we've got "#include <avr/io.h>". Why include this in the header and not in display.c like is typical? Because in our function declarations

```cpp
void display_setup(void);
void display(uint8_t num);```

we need to use one of types provided to us by avr/io.h, "uint8_t". Not including this in the header gives us an error. As a bonus, though, because we included it here in display.h, we don't need to include it in display.c. If you remember how header files and includes work, you should be able to guess why: the contents of "avr/io.h" are copy-pasted into "display.h", which is then copy-pasted into "display.c". Let's take a look at this "#define" business. This is called macro declaration. The convention for macro names is all caps. This lets you know that they are not a variable that can be changed, they are constant expressions. Read more about this kind of C macro here - https://gcc.gnu.org/onlinedocs/cpp/Object-like-Macros.html#Object-like-Macros We use macros for simplicity: so we don't have to put "0x1F" or something in a hundred places in our code, then go back and change all of those if we need to use a different value. Please also note there are no equal signs in macro definitions, it just goes "#define NAME value".
>What is this shit anyway? PB_MASK = 0x1F?
These are called bitmasks. They let us do bitwise manipulation on only the bits specified, and not to all 8 in the byte. In this example it doesn't really matter, but if we were using the other pins for something else, it would interfere with those pins and fuck everything up. When in doubt, mask your bits when writing a byte to registers and ports. Let's look at the first of the two bitmasks, "PB_MASK". The name is short for "port B mask" and I just came up with it. It could be anything. Check out the value, what is it in binary? 0x1F translates to "0001 1111" in binary. If you know hex, you'll see why: 1 = 0001 and F = 1111. Take a look at display.c to see how we use these bitmasks.

PORTS. I/O pins on the AVR series chips are divided into groups of (usually) 8 pins, each given a letter. However, as some of the pins have alternate functions that may be in use, sometimes not all pins will be available to us to use. For instance, PORTB pins 6 and 7 are used for the inputs of the external crystal, and are not broken out for use on the Arduino Nano board. If you wanted to use those in your own board design, you would be limited to the Atmega's internal 1Mhz oscillator. Anyway, take a look at the pinout diagram. I wanted to use 8 I/O pins that were next to each other for convenience, so I picked the first 5 pins of PORTB (0, 1, 2, 3, and 4) and the last 3 pins of PORTD (5, 6, and 7). 
>Why didn't you just use all 8 pins from PORTD?
Because I want to use PD0 and PD1 (USART TX/RX pins) for something else next lesson. Let's set ours ports and pins up with our "display_setup" function. Here we are setting the values of two registers: DDRB and DDRD. These are Data Direction Registers. We write a value to them to set the pins of that port as either input or output. By writing our bitmasks to these registers, we set all the pins specified by 1s as output. So PB_MASK, which is 0001 1111 in binary, sets pins 0, 1, 2, 3, and 4, to 1 (HIGH, OUTPUT), and doesn't touch the other 3 pins. How so? With the "|=" operator. This means "or equals", or, "either your current value, or whatever value is being supplied. Read up on logical operators if you aren't familiar. Basically, if a pin's value is 0 or 1 and we do "pin |= 1", it will become a 1. Doing "pin |= 0" leaves it unchanged. We will be using this a lot.

Next: Port Data Registers

# 85
==LESSON 3 CONTINUED - display continued==

CORRECTION TO MAIN.C:

```cpp
#include "display.h"

void display_setup(void)
{
    // set up the 8 output pins we're using and clear them
    
    DDRB |= PB_MASK; // set pins 0,1,2,3,4 of PORTB as output
    DDRD |= PD_MASK; // set pins 5,6,7 of PORTD as output

    PORTB &= ~(PB_MASK); // set PORTB pins 0,1,2,3,4 low (xxx0 0000), x = unchanged
    PORTD &= ~(PD_MASK); // set PORTD pins 5,6,7 low (000x xxxx), x = unchanged
}

void display(uint8_t num)
{
    // write the value of num to the display as a series of 8 bits
    
    PORTB &= ~(PB_MASK); // clear our 5 bits in PORTB
    PORTD &= ~(PD_MASK); // clear our 3 bits in PORTD
    
    PORTB |= (num & PB_MASK); // (xxxx xxxx) & (0001 1111) = (000x xxxx)
    PORTD |= (num & PD_MASK); // (xxxx xxxx) & (1110 0000) = (xxx0 0000)
}```

I didn't follow my own advice about not touching the other bits. Anyway, we're still working with display_setup. Look at the next couple of lines:

```cpp
PORTB &= ~(PB_MASK); // set PORTB pins 0,1,2,3,4 low (xxx0 0000), x = unchanged
PORTD &= ~(PD_MASK); // set PORTD pins 5,6,7 low (000x xxxx), x = unchanged```

Lets look at this piece by piece. First, we have two more register names. These are the Port Data Registers for ports B and D. Writing to them lets us set the pins in those ports. If our pins were inputs, reading these registers would give up the values of those pins. We are using (at least some of) those pins as outputs right now, so we are writing to them (with the equals sign). Next we have this thing: "&=". This is an "and equals" operator. In other words, if something is currently 1, and we &= 1 it, it will remain a one. If it's currently a 0 it would remain a 0. This symbol, "~", is an inverse sign. we put that in front of our bitmasks to invert them. Thus, 0x1F (0001 1111) becomes 1110 0000. When we apply that with the "&=" operator to the value currently in PORTB, the first 5 bits (from right to left) will become 0s, the remaining 3 remain unchanged. This is to set all of our LEDs to off to start. It may not be necessary here, but it's always good practice to initial values of stuff you use so it's not in an unknown state at startup (which can be especially dangerous in robotics).

OK. So that sets up our ports and pins. It can be confusing but I hope everyone is still following along. Next we're going to look at the actual display function, "display". This time, our function requires a parameter to be passed to it when we use it. In other words, it needs to be given a number to display. You can see that in the first line:

```cpp
void display(uint8_t num)```

The "void" at the beginning is what the function returns, which in this case, is nothing (don't worry about this for now). The interesting bit is after the function name, in parentheses: "uint8_t num". What this says is that we need to give our function an 8-bit unsigned char every time we call it, and that we can access that value from inside the function with the variable name "num". Lets look at the function body itself. First, we clear the two data registers (only the bits we're using). This clears old data from them (last "frame", if you will). Then, we do a bitwise & with the number we're trying to show with the bitmask. So for the number 255, for example, which is 1111 1111 in binary, &'ing with our PORTB bitmask, 0001 1111, will give us a result of 0001 1111, which is then |='ed with the value currently in the PORTB data register, where only the 1s will affect it. Get it? Thus, writing our value to those pins. Same for PORTD.

Next - Makefile

# 86
==LESSON 3 END - whew==

Makefile for this lesson:

```cpp
# robowaifu learning project 03 - count

CC=avr-gcc
OBJCOPY=avr-objcopy

CFLAGS=-Os -Wall -DF_CPU=16000000UL -mmcu=atmega328p

ISP=usbtiny
BAUD=115200

EFUSE=0xFD
HFUSE=0xDA
LFUSE=0xFF

main.hex: main.elf
	${OBJCOPY} -O ihex -R .eeprom main.elf main.hex

main.elf: main.o display.o
	${CC} $(CFLAGS) -o main.elf main.o display.o
	
main.o: main.c
	${CC} $(CFLAGS) -c main.c -o main.o
	
display.o: display.c
	${CC} $(CFLAGS) -c display.c -o display.o

flash: main.hex
	avrdude -F -V -c ${ISP} -p ATMEGA328P -b ${BAUD} -U flash:w:main.hex
	
fuses:
	avrdude -F -V -c ${ISP} -p ATMEGA328P -b ${BAUD} -U efuse:w:${EFUSE}:m \
	-U hfuse:w:${HFUSE}:m -U lfuse:w:${LFUSE}:m  

clean:
	rm main.elf main.hex *.o```

Same as before, only we're building display.o instead of blink.o and stuff. Go ahead and do a "make flash" to see our binary counter in action. I tried to cover a lot of content in this lesson, so let me know if you have any questions, if you see any more mistakes, or if something isn't clear enough.

Next lesson: Talk to Me - serial communication

# 87
>>3830
Damn, fucked that up twice. This code I posted:

```cpp
#include "display.h"

void display_setup(void)
{
    // set up the 8 output pins we're using and clear them
    
    DDRB |= PB_MASK; // set pins 0,1,2,3,4 of PORTB as output
    DDRD |= PD_MASK; // set pins 5,6,7 of PORTD as output

    PORTB &= ~(PB_MASK); // set PORTB pins 0,1,2,3,4 low (xxx0 0000)
    PORTD &= ~(PD_MASK); // set PORTD pins 5,6,7 low (000x xxxx)
}

void display(uint8_t num)
{
    // write the value of num to the display as a series of 8 bits
    
    PORTB &= ~(PB_MASK); // clear our 5 bits in PORTB
    PORTD &= ~(PD_MASK); // clear our 3 bits in PORTD
    
    PORTB |= (num & PB_MASK); // (xxxx xxxx) & (0001 1111) = (000x xxxx)
    PORTD |= (num & PD_MASK); // (xxxx xxxx) & (1110 0000) = (xxx0 0000)
}```

is the fixed code for display.c, not main.c. My bad. Gotta hurry up and get a repository set up so I can just link there for the latest code.

# 88
>>3820
>We will do programming in C for SBCs and integrate it with the Nano later though.
That will be fine Sensei. As long as that's something we cover effectively I'm sure I should be able to adapt it to the BBBlue boards I intend to using in my robowaifu later.

>>3832
>Gotta hurry up and get a repository set up so I can just link there for the latest code.
~~GitHub~~SJWHub has become a wretched hive of politically-correct scum and villainy. I chose GitLab and thus far I really happy with it.
https://gitlab.com/users/sign_in#register-pane

# 89
How's everyone doing? Still with me? I'm finishing up the write-up for lesson 4: USART, strings, and pointers. Might have it up tonight.

# 90
Gitlab repository up with code at least, including Lesson 04's. Will put cleaned-up explanation text on there too when I can. Set as private for right now, let me know if you want access.

# 91
>>3834
>>3835
I'm still here and following along. I have Uni and that's taking up a lot of my focus, but be sure I'm here. Thank you and I look forward to the next lesson!

# 92
Hi Japanon, I finished all the lessons tonight, got my blinking counter going nicely. One question, why are the pins out of order? It seems like there are two groups of four, out of order.

>let me know a bit about you.
Software developer, generally pretty good with technology. I get pretty frustrated working with my hands though, bending the resistors to go into the breadboard was very frustrating to me. I wonder if having a low enough DEX could constitute some sort of disability.

>What direction would you like to see the curriculum go in?
The two projects I plan to attempt is moving eyes (with the goal of eye contact) and body warmth (see the thermal management thread for my thoughts on that). Body warmth could be done without any microcontrollers at all, but learning about electricity will still be useful for that project. Would like to know your thoughts on the matter. I'd like to see this thread work towards a pair of moving eyes. In particular I'd like to work with a stepper motor. Also, Iggy was investigating pressure sensors, so we could do some things with piezorestistors or capacitive touch sensors.

>What is your skill level with electronics?
Some knowledge, but little experience. Already learned a lot from this thread.

>Can you wire up a breadboard?
I did, although I found it frustrating. 

>Can you do Ohm's law and RC calculations?
In practice I'd probably use an online calculator. 

>Can you program in C at all?
Yes, although I'm learning a lot about makefiles from this thread.

>What does everyone think so far?
Thanks so much! Please keep going.

# 93
>>3837
Hi. Welcome back.
>One question, why are the pins out of order?
>It seems like there are two groups of four, out of order.
Can you clarify this? Is it not displaying for you properly? I suppose the pins are a bit out of order, that's just the way (my) Nano and breadboard are laid out. I've chosen to use two colors because we use the same setup in lesson 4 and it makes that output a little easier to see. Also because it's placed to the left of my PC, I have the Nano on the rightmost edge of the breadboard with the micro-usb connector facing right. The 8 LEDs are placed on the board in the remaining open space to the left. With the nature of how bytes and bits work, the first (least significant) bit is on the right and the last (most significant) bit is on the left. Thus the spaghetti. You can lay out your connections however you like, as long as the LED/resistor and board connectors are like so:

```cpp
Nano pin    AVR-C macro         Breadboard LED/resistor circuit
D8          PB0         ->      1 (rightmost)
D9          PB1         ->      2
D10         PB2         ->      3
D11         PB3         ->      4
D12         PB4         ->      5
D5          PD5         ->      6
D6          PD6         ->      7
D7          PD7         ->      8 (leftmost)```

Consult the pinout image of the Nano board in case yours is labeled differently. Let me know if that doesn't help. Post a photo of your setup if you still have issues.

> I get pretty frustrated working with my hands though, bending the resistors to go into the breadboard was very frustrating to me. I wonder if having a low enough DEX could constitute some sort of disability.
This is normal. I suggest using a pair of needle-nose pliers. One, to give you nice 90-degree bends so that your resistor leads look like  a '[' instead of a 'C'. They go in a lot easier that way. If the leads are thin or your breadboard super tight, or both, you can use the pliers to grab the lead and force it in. Works for me.

>In practice I'd probably use an online calculator.
Right. It's more about whether people know of them.

>moving eyes
You're going to have to be more specific. What kind of eyes are we talking here? Cameras? Non-functional doll eyes? Small OLED screens? I saw the thread with the moving eye rigs but it seems like the challenge there is the design and fabrication of the mechanical parts, versus programming for a couple of servos. I could be wrong though, let me know what you're trying to do.

> pressure sensors, piezoresistors or capacitive touch sensors
Will take a look at those.

# 94
>>3837
>got my blinking counter going nicely
Nevermind, looks like you do have it working. Gotta wake up fully before posting.

# 95
>>3838
>moving eyes
What I want is eyes that make eye contact with me, and possibly do cute things like shyly looking away and then back. It would work like the moving eye rigs you saw in the other thread, but there would be cameras installed inside the irises and an AI (CNN?) that learned to move the actuators such that the eyes pointed towards human eyes. (Pretty straight forward object recognition task.)

>pressure sensors, piezoresistors or capacitive touch sensors
We discussed this in another thread and talked about different options. I can't seem to find that thread right now though.

What is the ohms of the resistors you are using? Mine are blue and use the 5 band codes, so I had to learn how to read the code and I don't think I got it right. Using the color codes I guess 220 ohms, and that's what I used.

# 96
>>3838
Another thing that would be valuable to learn is communication between the board and the PC. I'd probably want a wireless connection, and I'd want the PC to be running python (so as to interface with tensorflow).

# 97
> '''< archive ends>'''

# 98
Are you still with us, OP? Your thread convinced me to read the K&R 2e book.

```cpp
#include <stdio.h>

/**
 * Print Fahrenheit-to-Celsius table using the formula:
 * C = (5/9) (F-32)
 * @code
 *   5      F-32
 * ----- x ------
 *   9       1
 * @endcode
 *
 * @return exit status, 0 = success
 */
main() {
  int lo = -20, hi = 130, step = 10;
  int fahr = lo, cent = 0;

  while (fahr < hi) {
    cent = 5 * (fahr - 32) / 9;  // see formula in function comment
    printf("%d\t%d\n", fahr, cent);
    fahr += step;
  }
}```

I hope you'll continue your class once I'm done with the book.

# 99
>tfw you find yourself innocently enough first just studying esoteric treatises, then presently realize you must now LARP as Thompson & Ritchie and only do your programming work using Vim, while trying to imagine what it must be like to craft UNIX & C using just an ancient 8K RAM minicomputer.
The power of autism is generally what changes the world tbh.

https://www.bell-labs.com/usr/dmr/www/chist.html

# 100
I'm pretty new to electronics and started messing with Arduinos a little lately. 

I noticed that the code here was pretty different from the usual things I write in Arduino IDE(no setup, loop, pinMode, etc.). Thought about asking about it but just now I saw someone say this in a 4chan/g/ thread
>Arduino is only useful as a quick prototyping tool and a programmer. The standard library is shit, you're much better off with just directly using the ATmega registers

Is that what you're doing here, OP?

# 101
>>14495
I don't think OP is with us lately Anon. While I can't personally speak with the same authority as he has on the topic, I'd suggest the 4chan advice is correct after a fashion. Certainly the Arduino IDE is both vital for a newcomer to get started and to learn with, yet in the end direct hardware programming is both more powerful and more flexible.
>tl;dr
It's a great place to start, but don't camp there?

# 102
>>14495



Arduino themselvs have a nice explanation on port manipulation vs digialWrite: https://www.arduino.cc/en/Reference/PortManipulation



As for setup()/loop(): They are kind of redundant, you can achieve largely the same functionality with

```cpp


int main() {

    // "setup" here

    while (1) {

        // "loop" here

    }

}

```



If you haven't already, spend some time familiarizing yourself with the bitwise operators in c++. They are used a lot in microcontroller programming.

