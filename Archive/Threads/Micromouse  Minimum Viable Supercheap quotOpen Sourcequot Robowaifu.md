# 1
To keep this board just alive, I will chronicle my development of my first waifu-type bot.  In the Fluffytail thread I realized I projected too far ahead with final character designs and 3D models, when I hadn't even completed a single decent robot at the thread's creation.  Now that I have experience making the basic robots I feel confident enough to tackle this next challenge.  Besides, before I make a catgirl I better make a mousegirl first.

If for any reason 8ch goes down, I will start a Twitter account and will follow the you-know-who's of Japanese robowaifu twitterati which have been posted before, I'm just not into a social media mood right now because of all the virtue signalling.

'''Why Micromouse?'''

It is small and mechanically simple, while at the same time it has very precise movements which give the illusion of intelligence.  I want to make a tabletop pet similar to Anki Cosmo or Vector.  I was originally going to try to make a walking Rachnera quadruped but it's more complex with walking robots having to factor maximum weight.  With a micromouse the only constraints are length and width to be able to fit into and traverse a maze.

'''Minimum Viable Product Robowaifu?'''

This is just going to be a basic pet that runs around erratically, makes beeping noises and lights up some blushing LEDs.  It's going to be pretty tall, not your typically low profile micromouse, and to make it a waifu it will merely have a cardboard cutout of an anime character propped up on top of the chassis.  An infrared sensor will be placed on the head to determine whether a hand is simulating a headpat.  It will have multiple modes so that it can behave like a typical micromouse as well as turn into a waifu.

'''Supercheap Opensource?'''

Unlike University / Competition-grade micromice that you see from Japan/Taiwan, this is just going to barely qualify.  The parts total should cost no more than US $50, with no single module costing more than $4.  Many parts are from grab bags or off-the-shelf consumeables with negligible cost, assuming you have stockpiled enough electronics.  The skill level required to make this will be high school electronics; you only need to know how to solder safely and make 3D prints.  There's no custom PCBs or machined aluminum, but at the same time I'll try my best to not have this thing look like an amateur contraption.  I intend to post everything, all the STL designs for all the parts, all the code, so that anyone reading this can make his own and most likely improve upon it.  I really liked the Group Learning Thread, but this time I'll keep it in simple Windows Arduino IDE since some AVR-speak (e.g. hexadecimal fuse-setting) is a bit confusing and I don't recommend for total noobs.

Next post will be initial parts and design considerations.

# 2
Bump to save.

# 3
>>26
>Japanese robowaifu twitterati 

these guys anon?
https://twitter.com/Spri_ta
https://twitter.com/Ramphastos3

>I want to make a tabletop pet 
This has been a popular idea going back at least several years. Good luck anon, but $50 seems too low. I'd shoot for US$100 as the bar if I were you tbh.

# 4
>>3553
Yup those guys, once I have made visible progress I'll try my best at "notice me senpai" efforts.

Most entry level robot kits are in the $60-$80 range, and I consider them slightly superior to the sloppy robots I have made so far, but yeah in that range.

Also, I've been enjoying this autistic show, and been thinking this robot would be very easy to make, it's just an 8-DOF quadruped with a cylindrical shell, a wagging appendage and an LCD screen that pops up.  That'll be for next time.

# 5
>>3555
>I've been enjoying this autistic show

Kek, I watched ep 8 after seeing your post. Sure, I think cute animu roombas would be a good project goal. I think the new Jetson Nano >>4632 would probably have enough general-purpose & AI hardware power to drive it to where with the right programming it could even act semi-intelligent. cf, the nano jetbot could even serve as a core of a roombawaifu.

https://github.com/NVIDIA-AI-IOT/jetbot

And regardless of the hardware, I think it's a reasonably good design idea anon.

# 6
>>3555
Kemurikusa is a personal favorite this season. If you're thinking of making Shiro, this mechanism would allow for simplification of both walking mechanism and control.
https://www.robotshop.com/community/robots/show/octobot-spider-robot

Rin a cute

# 7
Ah, that looks pretty stable thanks, less electronics overhead is always a good thing.

Alright, I got the core parts list, hold off on buying anything if you don't already have it, I need to design the chassis first and test out the fit.  Writing this out first actually helps me cement my design process.

The overall design will be 7cm wide by 9cm long with the axle line around 5cm from the front.  This is because in a standard micromouse maze, the useable cell area is 16.8cm wide but if you want the mouse to run diagonally the clearance is only 11cm.  For testing I plan to build an 8x8 micromouse maze (pictured) which is only 1/4 the size but has the core features, namely:
- start at one of the corners, clockwise orientation
- center four squares is the finish line, there is more than 1 way to reach it
- a wall-hugging algorithm will NOT work as the mouse will miss the opening, instead it should seek to reach the center.

For the parts list, here are my reasonings for the following:

1.) Can't get any more basic than an Arduino Pro Mini (A Nano will work too, but I already have CP2102 / FTDI and no bootloader install necessary).  We're not going to be doing complex math nor driving a TFT display that needs high refresh, so an ARM MCU – much less a full Linux board  – would be overkill.

2.) size of the board is limited only to how good you are spacing components and soldering.

3.) 20c or cheapest motors in the world

4.-6.) There's a big local Tamiya scene so 4wd parts are affordable, this is better than rubber-banded rollers.  You can use all four wheels instead of adding a caster wheel if you're willing to add the other gears, but once again, I'm purposefully going el-cheapo to prove the point that there's a real low barrier of entry to creating a machine that exhibits some waifu-like behaviors.  The pivot of rotation is also directly at the axle lines instead of some midpoint.

7. I'll forego LiPo and the necessary battery management, discrete batteries it is for now.

8. L298N is way more flexible and TB6612FNG is insanely good, however L9110s requires less pinouts and will work for micro sized projects that don't need high current.

9. I found a module that already packages 4 infrared sensor-receiver pairs so this should save some effort having to roll your own.  The additional TCRT5000s are for detecting closer distances such as table edges.

10. LCDs are terrible with Arduino (better use STM32 and faster chips), but LEDs are just perfect, and the 8x8 display is really bargain priced and perfect at displaying the mapping of the 8x8 test maze in real time.  I add plenty of discrete LEDs to place near the key sensor points so I can monitor the triggers and confirm if they align with the arduino's programming, I'm sure the built-in modules have their own status LEDs though so this is more for my own OCD.

11. Of course we want it ("her") to beep-beep, plus it seems to become standard for micromice to give audible response to mode changes.

12. I'll be using a binary code to switch between the mode changes, which are:

0 0 : pet mode free drive
0 1 : maze mode wallhug
1 0 : maze mode exploring
1 1 : maze mode speedrun

The pushbutton and one of the infrared sensors will alternate as standby activate / hold triggers.

The double pole slide switches will be used to change the sensor outputs going into the arduino since there are not enough pins – the table edge sensors won't be needed during maze modes.

Next will be the design of the chassis, might take a bit but will post when done.

# 8
Alright, I was surprised thing thing started to look more like the front end of a race car.  As such you might want to change the front sensor LEDs to white/yellow and the rear LEDs to red for added effect.  The anime cardboard cutout will be slotted at the back in between the back panel and the battery pack, with a hole that can be used for fastening (it's used more for the motor driver attached to the back).

It's bigger than planned… 9cm wide and more than 12cm long, but I think it can go diagonals.  The toy motors will make it very slow, but the same size fits the Tamiya atomic motors, and if you pump 5V into them, yeah.

The "canopy" is the 8x8 dot matrix display module, when you pop it open, you can gain access to the main board to insert the Arduino pro mini into the female header pins soldered onto the perfboard.  Speaking of perboards, you can fit 3 – yes, three – 5cm x 7cm boards as these will be the ones providing rigidity to the chassis.  You don't need all 3, only two or even one will suffice if you manage to fit all the components onto the board, which is severely lacking in space since the mounts are resting on top of it so only the center and extreme sides are clear.   Me, I'll try to use 2 - the board housing the pro mini on top, and a board with the edge sensors / LEDs attached from below.  Otherwise, they make a nice sandwich.  A four-channel infrared module can even be squished in, just make sure to insulate them with plastic sheets or electrical tape.  Oh, and the step down buck module (the green tiny kind) will generate some heat, so find a central space within the sandwich to fasten and insulate.

I've attached the raw blend file.  I have yet to separate each component such as right and left parts into their own stl files with proper printing orientation.  The battery holder and caster can be ignored if you have a sealed battery pack or the actual metal ball unit respectively, otherwise they're just makeshift components.  The next two weeks will be dedicated to test prints.

Rename mainchassis.pdf to .blend

>missing filename:
mainchassis.pdf

# 9
I need to rework the motor mounts since they're too loose and wobbly.  The motors must be braced really tight while at the same time allow for adjustment.  In the meantime the other stl files are included in the "pdf", rename to zip and extract.

I'm still an amateur but I hope posting step by step will help someone else's design process, most of the robots I've encountered online are "here's my robot, here's my final code" which is overwhelming for me since I learn the best when I start with a blank program.

>missing filename:
individualstlszip.pdf

# 10
>>3560
Pretty nice design anon.

# 11
Sounds interesting, keep us updated man.

# 12
More pics of the final assembly before it gets 1000X messier with all the electronic components and wiring.

As shown, there is space for 2X 18650 LiPo batteries (although I plan to save my rechargeables for the future walking robots that need more power/less weight).

One 4X IR module has been installed, with 2 sets at the front bumper set an an angle, and 2 sets at the rear sides (to detect when a wall has been passed so it can turn left/right).  I plan to add 4 more IR sets, but be soldered to the perfboard instead.  The ready-made set saved me some soldering but takes up too much space.  At the rear the IR main module and the motor driver are screwed together… this is where the main cardboard cutout will be secured – it will need one mounting hole.

Majority of the holes are for M2 screws, although a few (the motor mounts and the caster mounts) can fit M3 or 1/8" screws.

At the bottom I managed to fit in a second perfboard, unfortunately I didn't have enough M2 screws of the right size so it's more of a compromise.  If you have right length screws you may even have enough space to squeeze in the IR module in between the two perfboards.

# 13
Ah forgot the motormounts, here they are (rename to zip then extract).  I tried making alternate mounts that are far more sturdier so can't snap easily, however I had a hard time finding out how to secure them so I reverted to the original design mounts.  You can use cable ties if necessary (pic is of the unused revised mount).

Next will be determining pinouts and physical components placement, I guess I should test them out on breadboard first.

>missing filename:
motormounts.pdf

# 14
>>3563
>>3564
Nice, compact design anon. I understand it better now that I can see the motors mounted 90' with screw gears. I like that your approach allows you to easily swap out different power sources. Do you have the ability to trim all the wiring to fit precisely? It would look nice if everything tucked in very tidily, and that skill and approach will only become more important as your robots become larger/more complex.

Good job!

# 15
>>3565
Thanks man, well thus far I started with dupont jumpers with isolated custom circuitry. In this case since it's a pro mini meant to be embedded everything will be soldered so the connections will be cut to fit. If ever I do reach the point of having no real estate for electronics I'll have to pony up for custom PCBs eventually.

# 16
Right now I'm running test sketches and finding whether it is better to read analog values or digital values depending on the infrared module used.  The TCRT5000 has surprisingly far detect distance (10cm) even though it won't be enough to slam an LED until 2cm.  The line tracker premade modules are already output-slammed, so while we can use digital inputs their triggering can be adjusted by potentiometer.

I've learned to test everything out on breadboard first, as I've made costly mistakes before of soldering some circuits I was absolutely sure would work.  Once on breadboard I can migrate components of the circuit to perfboard and test each module until everything works on the soldered board.  I'm still adjusting resistor values so once finalized I'll post the final circuit and some test arduino sketches.

Once all the sensors are on chassis, I'll have to build the maze walls and line them up straight on each side and make sure the robot can run straight down, with the motor driver adjusting whenever its veering left or right, kinda like a line follower but more like wall-sides follower.

>missing filename:
 breadboarding.webm

# 17
>>3567
>output-slammed
more info on this?

>I've learned to test everything out on breadboard first
haha good idea.

Looks interesting anon. Please keep us up to date on your progress!

# 18
>>3568
output slammed by LM393 or LM339 comparator so the signal can be properly pulled as close as possible to Vcc or ground to give a proper digital signal and also enough to drive status LEDs.

Now I don't know whether it's my soldering, but I've tested on two different pro minis and inputs A5 and A7 seem to be susceptible to oscillation when there's comparator load on the other inputs.  Though I haven't tried on a Nano yet (the whole point of the Pro Mini is that it's smaller and doesn't need bootloader).  I'll also try taking out all comparators and feeding all infrareds directly as analog inputs as levels 0 through 1023.  Comparators are needed to drive the status LEDs so I won't have my Christmas lights, but this time I'll prioritize functionality and ease of wiring.

# 19
>>3569
>All that analog circuitry

Have you tried something like this yet? The sensor half of your IR LED thing there is a phototransistor, meaning that the current flow through it increases with received light intensity. Reading the voltage before the phototransistor will give you a usable distance reading. The circuit in my image should give you 5V at 10+ cm (no bounced light) and the voltage drop of the phototransistor at full intensity (~0.7V or so, you'll have to experiment with distance and reflectivity to get the minimum distance) with a more or less linear scale with distance between those two. However, your reading will likely be overwhelmed with background noise. To eliminate that, apparently it's common practice to pulse the LED, on for T ms, off for T ms. You read the analog voltage during the off phase, which is all background noise, and subtract that from the reading you take during the on phase to get the true distance. Accuracy increases with smaller T. If you're not moving fast, the ambient IR shouldn't change enough to warrant more than 50 pps or so. Also, you have a microcontroller. If you want an LED to flash at a certain distance or timing, program it. You shouldn't need to fuss with analog comparators for something like this. 

I like what you're doing and wish I had the free time now to do the same. Keep us posted.

# 20
>>3570
I hadn't thought of pulsing the IR LED, thanks for the suggestion!  I noticed the TCRT5000 modules use pulldown resistors instead (active high) compared to the regular sized infrared pairs with pullup resistors (active low), but they should work either way.

I had used a variant of the circuit I posted to process the photoresistor voltage divider for the edge detectors for one of my sumobots. I could have just fed the voltage divider directly as analog input but I was lacking pins at the time and needed to make sure the signals were all processed so all the microcontroller had to do was make a decision.  I have 8 IR pairs, I don't need all working at the same time so I'll use SPDT switches to not go over the pin count.

# 21
Very useful information I found attached (it's a "real" pdf lol, no need for renaming).

They have two pulses for the diagonal IR, a second power pulse will make it detect whether the mouse can move diagonally to save time.  Awesome.

I am seriously contemplating using stepper motors since they are accurate and highly recommended.  Competition micromice apparently use the full suite high speed DC motors + encoders + PID.  I was originally using DC motors without encoders, just winging it hence the additional side IRs to keep equidistant between two walls.  We'll see, a mark II design that fits the larger steppers might be in the works if I find lots of trouble here.

# 22
>>3571
You have 8 pairs of IR LEDs/sensors, and not enough pins to drive/read them, so you want to disable some with a switch? Have you considered a shift register like the good old 595? Only needs 3 GPIO pins and no passive components to drive 8 outputs. Can be bit-banged in a handful of lines of code. You may be able to drive the LEDs directly from the 595 outputs if you don't exceed the total package current limit. Otherwise, go with a darlington transistor array on the low side of your LEDs.

See this page for an intro if you're interested: https://lastminuteengineers.com/74hc595-shift-register-arduino-tutorial/

# 23
>>3573
Also would need 74HC165 parallel-to-serial.

Analog inputs can't be multiplexed, so all the IR voltages go straight to A0-A7.  I think I'll switch back from pro mini to nano since it's just slightly more convenient.  Stayed up until 5am rethinking my pinouts, finally arrived here:
[code]ATMEGA328P PINOUT:				MICROMOUSE SIGNAL:

A0						IRleftside				
A1						IRleftdiag	
A2						IRheadpat
A3						IRcenter
A4 						IRrightdiag	
A5 						IRrightside
A6 (analog only)				IRedgeleft
A7 (analog only)				IRedgeright			
D0 (RX keep load-free for serial.begin)	  	unconnected	
D1 (TX keep load-free for serial.begin)		unconnected	 
D2						LATCH // for 74HC595 IR pulse selector
D3 PWM						buzzer // sound	
D4						IB1 // motor driver
D5 PWM						IA1 // motor driver pwm
D6 PWM						IA2 // motor driver pwm
D7						IB2 // motor driver
D8						CS // for MAX7219 LED displays (daisy-chained 8x8 to 8x7seg)
D9 PWM					        LOAD // for 74HC165 digital input selector
D10 PWM						ENABLE // for 74HC165
D11 PWM						DOUT // Output lines to MAX7219 and 74HC195						
D12						DIN // Input lines from 74HC165						
D13						CLK // clock lines to all serial devices


74HC165 inputs:

In7
In6
In5
In4
In3
In2
In1
In0 

In2-In0 (3 bits) - main modes

000 = debug mode (motors off)
001 = wallhug right
010 = wallhug left
011 = wallstraight
100 = line following
101 = erratic pet mode
110 = maze explore mode
111 = maze speedrun mode

In5-In3 (3 bits) - test/display/serial monitor A7 to A0 IR voltage inputs

In7, In6 (2 separate bits) - pushbutton inputs (activate mode, deactivate/standby mode (stores current data))[/code]

# 24
>>3574
I'll admit the 595 was half-baked, but you get the idea. Port expanders and multiplexers are cheap and easy, so don't limit yourself by something like microcontroller pin counts.

Anyway, there's nothing I hate more than internet queers who only want to critique and nitpick others without doing anything themselves, so I've decided to make one of these myself, both to learn something new and to maybe help out Flip anon here if possible. I went down to Tokyo yesterday to check out the Aitendo store in Akihabara. I use their site a lot, just never been to the store (shipping is less than the cost of the trains 1-way). I grabbed a whole bunch of parts including: TM1637 LED controllers (Chinese garbage), PCF8574 I2C 8-pin port expanders (god-tier), PCF8591T 8-bit 4-channel I2C ADCs (working nicely), NY9M005A MOSFET single-motor bidirectional drivers (not tested yet), a TB6612FNG dual motor driver module (not tested yet), a dozen IR LED/Phototransistor modules, plus a ton of SOP/SOIC to DIP adapter boards, connectors, and power-related stuff. I'm aiming for roughly the same size and functionality of the other anon. I've got the major pieces up and running already, so I'll follow up with some schematics and code when I can. Currently powered by an 18650 li-ion raised to 6.5V (for motors) with a switching boost regulator, then dropped to 3.3V for the electronics with an AMS1117 linear regulator. Microcontroller is a 3.3V pro mini at 8Mhz.

# 25
>>3574
I wanted to test the pulsed IR LED background noise elimination scheme that I had read about and posted in this thread earlier, so I made a simple test circuit and wrote a quick test program for it. Circuit is as pic related. I am pulsing the IR LED using a GPIO with an NPN transistor on the low side. I am reading the phototransistor sensor by measuring the voltage across a 300K ohm resistor, again, on the low side. This gives me an easy to work with 0-max voltage reading, with higher readings being closer. The code section for that is here:
[code]// read background noise
adc_read_noise = PCF8591_read(PCF8591_ADDR, 0x01);

// turn on IR LED
PORTB |= (1 << PB0); // PB0 HIGH

_delay_us(200); // allow LED to stabilize

// get distance reading
adc_read_real = PCF8591_read(PCF8591_ADDR, 0x01);

// turn off IR LED
PORTB &= ~(1 << PB0); // PB0 LOW

// subtract noise
if (adc_read_noise > adc_read_real) // subtraction would cause an underflow
{
    adc_read_real = 0;
}
else
{
    adc_read_real -= adc_read_noise;
}[/code]
The code to interface with the ADC is as follows. I'm doing a two-read average just because power of two averaging is computationally lightweight, disregarding the fact that it's 16 bits.
[code]uint8_t PCF8591_read(uint8_t address, uint8_t control)
{
    uint16_t value; // I2C read result
    
    i2c_start((address << 1) | I2C_WRITE); // start I2C in write mode
    
    i2c_write(control); // select ADC pin

    i2c_rep_start((address << 1) | I2C_READ); // start I2C again in read mode
    
    i2c_readAck(); // read from ADC once, discard result
    
    value = i2c_readAck(); // read from ADC
    
    value += i2c_readNak(); // read from ADC again, add to result
    
    i2c_stop(); // stop and release bus
    
    return (uint8_t)(value >> 1); // return average of two reads
}[/code]
It works pretty well. I'm getting a solid ~0 reading with nothing in front of the sensor, and I'm detecting a piece of white paper reliably at up to ~14cm. ADC reading is 1-2 at 14cm and 230-231 at 1cm, giving me ~0.56 LSB per mm, which is more precision than I need given the inherent noise and inaccuracy of the system.

# 26
Went ahead and ordered some more parts for my build. Should be here in a week or so. I decided to go with the same motor driver module. The ones I had bought apparently have a voltage max of ~5.5 and I need at least 6, preferably 6.5-7. I haven't even tried the Toshiba chip yet but I want to be able to hand solder everything, so I don't want to go below 1.27 pitch if I can help it. I also got a few ball bearing casters. The layout will be wheels in the front, caster in the back. That should keep it from getting hung up on rug edges or cables on the floor. The wheels are roughly the same size, 34mm with 3mm D-shaft holes. The plan is to prototype with a chassis cut from 5mm coated foam board, then using a printed circuit board for the chassis when the design is settled.

# 27
Awesome, glad to see another real-world perspective on this.  These sizes can barely be made into robowaifus, with cardboard or maybe at most papercraft stuck on top, but after this I plan to tackle the balancebot with a stuffed anime doll like pic related.

My main dilemma right now is whether and how to add optical rotational encoding to the wheels, with just DC motors I need to know how many rotations they made to estimate how many squares in the maze the robot has traversed.  With my setup there's barely space for an encoder wheel but maybe I can paint the gears with black and white stripes and thus have the drive gears double as encoders.

>>3578
> I decided to go with the same motor driver module. The ones I had bought apparently have a voltage max of ~5.5 and I need at least 6, preferably 6.5-7.
I picked the L9110S because they were the cheapest and worked okay when I used them previously, with minimal operational pincount, the main issue with the L9110S is the VCC is the same for motor and logic, so you'll need to isolate them to prevent the motor VCC from potentially back-frying the microcontroller:

https://www.electroschematics.com/13797/l9110-motor-driver-primer/

The yellow TT motors and the generic toy motors will actually be quite fast at 5V, the micro metal gear motors like you ordered come in either 6V or 12V.  Since you have the TB6612FNG I'd go with that.

# 28
>>3577
>given the inherent noise and inaccuracy of the system
Push it one step further by implementing lock-in amplifier on the MCU.

>A lock-in amplifier is a type of amplifier that can extract a signal with a known carrier wave from an extremely noisy environment. Depending on the dynamic reserve of the instrument, signals up to 1 million times smaller than noise components, potentially fairly close by in frequency, can still be reliably detected.
It's probably a massive overkill, but if you happen to need more precision/distance you could try using this method. A bit of DSP magic can do wonders.

# 29
I like where this thread is going tbh.

# 30
>>3579
Thanks for the heads up about the L9110S module. I had looked over the datasheet, and it looks like the inputs are as you'd expect from your average H-bridge driver, one-way only. The issue is likely just with that module, where some dumb shit decided to pull the inputs up instead of down. So depending on your setup, yeah you may see motor voltage on your microcontroller outputs. I don't see any mention of braking in the datasheet, so setting the inputs HIGH-HIGH and LOW-LOW should both stop current to the motors, per the truth table. When mine get here, I'll desolder the resistors on one and pull the inputs down at the microcontroller side. That is if I don't just pop the ICs off and breadboard them with DIP adapters. Pic related is a module I found somewhere without pull-ups.

By the way, would you mind telling me what voltage drop are you getting across the driver IC? Supply voltage minus the voltage measured across the motor. I'm trying to figure out if the switches in this thing are MOSFET or BJT. BJT drivers like the L298 will drop 1.5V-5V as heat, MOSFETs as little as 1-2 supposedly. My allegedly-MOSFET NY9M005A here is dropping 2.4V free spinning and ~4V stalled.

# 31
Forgot pic, NY9M005A on breadboard. Added a 470uF cap on VCC for power filtering as well as a standard 0.1uF for decoupling. Same 0.1uF cap across the motor leads for spark noise.

# 32
>>3582
.97V to 1.48V.  I don' have a proper LCD multimeter though, just an LED voltmeter which is a load by itself.

# 33
I'm currently still waiting for more parts to arrive, I decided to might as well make my setup as robust as can be.

I need to make a custom implementation of pic related that will fit my chassis.  The way they work is described here.

https://www.brainy-bits.com/speed-sensor-with-arduino/

I'm going to be using the sensor just to measure distance traveled, for the rotation speed control I'll just let the wall-avoidance nature of the bot take care of it moving somewhat straight.  I also dislike the fact they're interrupting just to count up, I'm thinking of using a discrete binary or decade counter and only interrupt at bigger intervals, say when one rotation is completed or one maze square has been traversed (~18cm).

The kit disc encoders have 20 slits, I don't need that much, I only really need 10 so one rotation = 10 clicks.  Instead of holes I was thinking of a decagon with alternate black and white strips so the infrared pair would just point at the rim and read the reflection.  This can be easily 3d printed or even made of cardboard.

Since the diameter of my wheel is around 3cm, one rotation would be pi x 3cm or around 9.4cm, so almost two rotations or 19-20 clicks would make the robot move one maze square.

Of course all this will be moot if I had just gone with the more precise predictable movements of stepper motors, which is what I'll use for a second robot that will have the added ability to draw by having a servo that can raise and lower a pen.

# 34
>>3585
>that will have the added ability to draw by having a servo that can raise and lower a pen.
That sounds cool. It reminds me of the scene in the classroom where the guy has the little moebot Sumomo write out the memory prices on paper.

# 35
I'm seriously considering using two Arduinos now, in I2C configuration:

https://www.arduino.cc/en/Tutorial/MasterReader

- I need to cut down on circuitry whether analog or digital  (I need to save my Megas for my planned legged robots 16+ pwms for servos).
- Instead of going shift by one byte (using shift registers), then read/right the next set, which wastes clock cycles, have both read/write at the same time, and compare notes later.
- The slave will continuously poll the microsensors and motor drivers so the master can concentrate on the macro sensing and big behaviors.  
-I will be making robots that can be controlled via a universal 2.4Ghz remote control eventually, where the transmitter/receiver controller modules are pro minis, so this will be a stepping stone to that ability.  I can start to formulate standard serial commands which can also be sent via bluetooth, etc.

Gonna rethink the pinouts again.

>>3577
>ADC reading is 1-2 at 14cm and 230-231 at 1cm

I'm using active low so it starts usually 800-900 and goes to 0-200.  Discovered the prebuilt modules only output 500-600, that's barely a logic high, no wonder they had to add comparators. Guess I'll have to stick with the discrete IR pairs.

>>3586
Aye, the program for a drawbot already exist (there's a project called Mirobot), I will just make it cute.

# 36
>>3587
>I need to save my Megas for my planned legged robots 16+ pwms for servos
>for my planned legged robots 16+ pwms for servos
>16+ pwms for servos
can you elaborate this?

# 37
>>3588
Robots like ]]4643

typically have 15-22 servos, the Servo library supports up to 12 motors on most Arduino boards and 48 on the Arduino Mega. (Turns out RC "PWM" is different from "real PWM", so can be faked on other pins via software.).  It's just a precaution, I also got separate 16-channel servo controllers just in case.

# 38
>>3589
I think I understand. So this is some type of channel on the micro-controller's output pins, and the number is simply the count of them.

# 39
>>3587
Turns out I wasn't reading the voltage drop correctly. If I measure from VCC to motor+ and from motor- to GND, I get about 0.8V dropped at each, which is more in line with what I expected from a MOSFET motor driver. I guess back EMF is what's causing the voltage to appear lower than the ~3.4 it should be.

>Arduinos
>Megas
>pro minis

Wew. It's Thursday night, I have a 4-day weekend, my work project's PCB is at the fab, and I'm not sober enough to constructively criticize anyone so have these pics instead. It's a SOP-8 flashing socket on a DIP adapter, some assembly required. Set me back maybe 5USD.

# 40
>>3591
That's neat. I'm assuming you can program the chip using that little socket? Have a good weekend anon.

# 41
>>3592
>I'm assuming you can program the chip using that little socket?
Sure. You still need a programmer though, like the USBtinyISP that I use. The socket just lets you breadboard a surface-mount chip without soldering it. I use them to flash firmware to microcontrollers before soldering them onto boards. I just wanted to demonstrate that you don't need SOP to DIP adapters and a lot of soldering to use surface mount chips in your designs. I say that because most everything available in DIP package these days is ancient, and expensive to boot. Even 1.27mm pitch SOP /SOIC is getting rare.

# 42
>>3591
cute

>>3596
Noticed that too, electronics was my first hobby as a kid, little did I know that I would be using blue resistors and packaging like pic related.  Most of the DIP chips I have had their markings rubbed off already due to old age.

I took the plunge and got analog multiplexers (https://playground.arduino.cc/Learning/4051/) octal flip-flop latches, and decade counters, will see which works best, despite professing I need to lower pin count, I still have a hard on for hardware solutions.

# 43
>>3597
>I still have a hard on for hardware solutions.
kekd a little tbh

# 44
My motors and other parts aren't here yet, so let's talk infrared a little more. The IR LED/phototransistor pair units I have are TCRT5000 from Vishay. I went over the datasheet and attached the most relevant bits here. First one is the absolute maximum specs for the IR LED portion. Take note of the maximum current allowed indicated by "forward surge current": 3 whole Amperes. Awesome. Caveat: for 10 microseconds max. Just like with a camera's flash, if I want to maximize range, I need to push as much power through the LED as I can get away with, for just as long as I need to.

How long do I need to have it on though? I need the IR LED on for as long as it takes to read the result from the I2C ADC. Using the 16-bit timer Timer 1 with no prescaler (simple time measuring for intervals under 8.2ms with an 8Mhz AVR, 4.1ms with a 16Mhz), I got the following results:

[code]single ADC read:	~515 microseconds
2-read average:	~606 microseconds
4-read average:	~794 microseconds[/code]

That's actually pretty long, damn. So I can have the LED on with 3 Amps flowing through it for 10 microseconds. Assuming a linear relationship between current and time, having the LED on 51x longer should mean that if I reduce the current to 1/51th of 3A, I should be good. In other words, ~59 milliamperes. But wait, the datasheet says the max continuous current is 60mA. Pulsing for 515us with a low duty cycle, say, once every 20ms, should let us go higher than 60mA, somewhere between 60mA and 3A. I guess the relationship isn't actually linear. I would guess I could go as high as 150~200mA for 500us. By the way, the earlier ranging tests were done at ~64mA pulsed. The code for this time test is as follows:

[code]// Timer 1 setup
TCCR1B = (1 << CS10);   // no prescaler
TCNT1 = 0x00; // set timer1 counter initial value to 0

while (1)
{
    _delay_ms(100);
        
    TCNT1 = 0x00; // set timer1 counter initial value to 0
        
    // read backgroud noise
    adc_read_noise = PCF8591_read(PCF8591_ADDR, 0x01);
        
    elapsed = TCNT1; // number of counts
                     // 1 / F_CPU * count = elapsed time in seconds
        
    PORTB |= (1 << PB0); // turn on IR LED
        
    TCNT1 = 0x00; // reset timer1 counter
        
    // get distance reading
    adc_read_real = PCF8591_read(PCF8591_ADDR, 0x01);
        
    elapsed += TCNT1;
        
    PORTB &= ~(1 << PB0); // turn off IR LED
        
    // subtract noise
    if (adc_read_noise > adc_read_real) // subtraction would cause an underflow
    {
        adc_read_real = 0;
    }
    else
    {
        adc_read_real -= adc_read_noise;
    }
        
    send_string("elapsed count: ");
    sprintf(word_buffer, "%d", (elapsed >> 1)); // divide by two
    send_string(word_buffer);
    send_string("\n\r");
        
    send_string("ADC value: ");
    sprintf(byte_buffer, "%d", adc_read_real);
    send_string(byte_buffer);
    send_string("\n\r");
}[/code]

A more sophisticated approach would start a timer, start the I2C transaction, have an interrupt trigger after 300us, turn on the LED in the interrupt handler and disable the timer, then get the reading from the ADC, potentially reducing your on-time to ~200us. But I digress. So how to switch 100-200mA per LED anyway? AVR GPIOs aren't going to want to do that. The PCF8574 won't sink more than 50mA per output, and 100mA at a time total. Enter the P-channel MOSFET. Available in tiny SOT and dual-channel SOP-8 packages, and with near infinite gate resistance, the PCF8574 can drive them to saturation at 3.3V with ease. Schematic related is what the circuit for 2 IR LED/phototransistor pairs would look like, and what I'll likely end up doing.

# 45
>>3599
Cool. I think I mostly followed that. Do you have a couple of burner circuits you can push to failure to get an idea of just how far you can go before you get into trouble. Destructive testing?

# 46
>>3600
It's all burner circuits for now. I've got plenty of sensors. I switched to using the ADC on the Atmega for right now. At 125,000 samples per second (8Mhz / 64 prescaler), I'm able to have the IR LED on for as little as ~120 microseconds. Current setup is like pic related, until I can borrow some mosfets from work. The transistors I have are your dime-a-dozen NPN types rated at 150mA so I suppose they would actually be the first to go. That said, I'm getting a max range of about 14cm with a 22ohm resistor on the LED (~64mA), and about 21cm with 2, 22ohm resistors in parallel (~128mA). Still doing a bit of experimentation though. The max distance and especially linearity changes a lot with the values of R7 and R10, oddly enough, as well as the value of C6. I can't quite put a pattern to it yet. I'm switching in mosfets though, so I won't be doing anything more with this for now.

# 47
>>3601
>I can't quite put a pattern to it yet
Interesting. My guess as an amateur is that you're exposing some temporally-unspecified behavior in the IR diode, maybe a cascade of some quantum tunneling effect or other. But you would know about these things far better than I would.

# 48
Apparently the grab bag of generic 940nm IR I ordered had the receivers with the short lead/long leads and flat ends switched up, this stumped me for the longest time.  Initial tests show they behave almost similar to the TCRT5000s (they're also 3mm), I can probably switch them in and save the latter for the special occasions, especially when I do need that plastic housing.

Since I'll be using multiple MCUs and multiplexing, I'll be adding more IR measurement vectors to the design. Since I'll be pulsing them I can group pulse the ones that point in opposite directions together, for example, to save on clock cycles, as long as they're far enough apart not to cause interference with each other's readings.

>>3601
Note that the micromouse will be surrounded by walls only 1-5cm away, unless it is looking into a long corridor or diagonal.  For longer distance obstacle avoidance I have ordered Sharp rangefinders and Time of Flight chips, but won't be deployed here.

# 49
Another good research paper, explains how each IR pair can be used for navigation.

I currently have 5 IR pairs for positioning, I will make it 6 like in the paper.  Two front IRs are for detecting protruding walls especially during diagonal runs.  The previous micromouse paper I posted only had 4 IR pairs but they were using precise stepper motors so perhaps don't need to keep center-positioning the mouse in between two walls.

# 50
>>3604
thanks anon.

# 51
Major changes to the chassis…

I have no idea what I was thinking making a front-engined design, perhaps I was thinking about pulling power with the structure also pulling the motor gears together.  So much wasted space on the perfboard.

Anyways, because I decided to go dual-microcontroller, I will need much more space for electronics.  The previous aerodynamic design is gone, instead there is more space to stack electronics.  Thankfully, I can just reuse the revised thicker motor mounts (after trimming the bottom holding arm to allow the main gear to rotate – see closeup pics), they are mounted from the rear in a mid-engined fashion.  The LED displays and the waifu cardboard cutout will be placed last, they will mount on the top layer after all the other electronics have been stacked.

Also gone are the ready made IR modules, they just won't do honestly, especially after the technique Nippon-anon showed us regarding pulsing IR arrays.  They were hard-soldered and couldn't be pulsed, and the receivers can't sink that much current hence the extraneous comparator circuit.  I will be using discrete IR pairs instead, soldered directly to the perfboards but bent and sticking as far out as possible.

As for the wheels, I've changed to Tamiya 5-spoke wheels so they can function as some form of encoder.  They're slightly smaller than the previous wheels so I used a flat rubber band to expand the diameter by 2mm to fit the tire properly. I'll have an infrared LED shine outward from underneath the axle and have a receiver arch over the wheel on the other side.    I noticed infrared can pass through the thin plastic gears but gets blocked by cardboard.  So I'll need to apply some cardboard masks to the insides of the wheel spokes.  My previous attempt in creating a 10 spoke than 5-spoke combo encoder wheel failed, they were just too wobbly.  If you have to make a 3D-printed wheel, it has to be at least 5cm diameter, plus anything round is really brittle, 3D prints work best on square block shapes.

I'll be adopting the dual microcontroller design in the future, it just makes sense… the slave MCU will read and cycle through all sensors, and the master MCU will interrupt, get the current readings, and make decisions.  Previously with one microcontroller I was having trouble with the timings since it took too long to take readings when the MCU should be making a decision at the same time, and it was hard to switch between the modes.

# 52
>>3606
It's fun watching the progression Philippines-anon. Keep up the good work.

>I'll be adopting the dual microcontroller design in the future, it just makes sense…
Good thinking. I'm guessing that several controller chips, of various classes, will be needed for any larger robowaifu designs.

# 53
Is this is an okay idea…

I'd like to be able to see the value of the reading from the infrared receivers even without a serial monitor hooked up, ideally simultaneously.  That way while debugging I can manually place the micromouse in the maze and have an instant view of all the infrared readings.

So I was thinking of using RGB LEDs, only the green and red colors.  If the distance is far it'll be green.  As an obstacle gets closer it becomes yellow (green + red) and at point blank it becomes full red.  I'd like to map the 0 through 1023 analog infrared readings into 0 through 255 PWM to power the LEDs.  Initially, for 6 IR pairs, I thought I'd need 12 PWM pins to power the green and red pins of the 6 RGB LEDs.  While the green value is PWM, the red value will be 255-PWM or the inverse duty cycle.  But then I thought of using an inverter, I made a scribble with two options… A.) using a transistor  B.) using a comparator.

# 54
>>3608
You don't even need a transistor for this. All you have to do is pic related. When output is HIGH bottom diode is on and when output is LOW top diode is on. Make sure that your MCU pin can sink/source required current limited by resistor (it probably can but check to be sure).

# 55
>>3609
Nvm. I missed common anode part. This wouldn't work. Transistor solution it is then.

# 56
>>3609
>>3610
It would be great to have it that simple though.

# 57
>>3611
Hold my waifu. Pic related should work theoretically if forward voltage of green is greater than that of red LED (it should be because of different band gap). I don't have common anode RGB LED to test this circuit but it's worth trying.

# 58
>>3612
>posts wrong image

# 59
>>3613
Neat, thanks anon.

# 60
>>3613
Ah, will try this method as well this week, thanks!

# 61
Just sharing a really awesome micromouse, its like an F1 racer (while mine is a knockoff jeepney with anime decals by comparison.)

https://twitter.com/Haido_Ele/status/1125663948492001282

Looks like it is allowed for the mouse to start its run with its back flush against the wall, this does simplify things (just measure distance between axle and rear to determine distance of axle from maze cell center and go from there)

# 62
>>3616
Pretty sweet looking tbh.

# 63
Started soldering, I don't have enough breadboard space for everything so I'll construct module by module.  First up is a 2cm x 8cm perfboard for the 6 IR pairs mounted on top of the bumper, it will mount using the female header connected to L-shaped pins at the front edge of the mainboard.   They all are all active low activation (pullup resistors), 150 ohms for the transmitter, 10K for the receiver.  My soldering is shit, but so far its tested and functions well.  Form follows function.

Q:  Why are you using tiny 3mm instead of 5mm IR LEDs?

A:   Because I bought a ton of them, and I will use them for the bottom sensors as well.  This isn't just a micromouse, but its a pet that can detect tabletop edges, as well as have a line-following mode.  With one generic IR model used, the expected electrical behavior is uniform across the board and I can more easily identify threshold values that apply to all sensors.  These particular units are 940nm and behave similarly to the TCRT5000.

Next up would be the bottom-facing IR pairs, then the RGB LED "shield" to give visual feedback to the sensors.

# 64
>>3618
I look forward to seeing a webm of them in action anon! Good job. Did you use anon's suggestion above after all yet?
>>3615

# 65
>>3619
>>3613
Confirmed, it works if you manually ground the red pin.  However if you use the output of a phototransistor the green doesn't budge at all.

Now when using the output of a micro it does switch, however it doesn't "steal" all of the current away from the green LED, so it ends up a slight orange.

I also tested the transistor circuit and it works quite well, the red is very red which means its a full switch.

Appreciate your inputs.

>missing filename:
orangey.mp4

# 66
>>3620
Thanks for the video. It's fun to watch everyone's progress.
>however it doesn't "steal" all of the current away from the green LED, so it ends up a slight orange.
hmm. anyway to inexpensively shunt the power away until it's above the proper threshold do you think anon?

# 67
^^^
The transistor solution worked, so I'm using that.

Anyways, fucking flip government has always been one of the biggest virtue-signalling hypocrites around (think of New Zealand), prostitution and porn are technically illegal and yet the cuntry is known for hookers and visiting pornhub the longest.  Yeah we tend to fall into (((their))) plans but I actually wish for our birthrate to plummet so there will be more resources for other races who aren't such a plague on the world.
Anyways, if this browsing inconvenience gets sjws off our boards the better I guess.

The bottom sensor module is complete, it's 3/8 of a 5cm x 7cm perfboard that fastens to the bottom of the front bumper.  Its spacing is good enough for black electrical tape, initial tests show its decent enough at detecting the black tape against a wooden floor background for line following (like the orihime robots in the Time of Eve inspired robot cafe in Japan). I will use this module to have the micromouse patrol my apartment.

# 68
>>3622
Glad to hear you found a good solution. Looking forward to seeing a working prototype mousing it's way around your place.

>like the orihime robots in the Time of Eve inspired robot cafe in Japan
Yea, I'm going to need some reference on this anon. For research purposes ofc. :^)

p.s. glad you found a way around their bullshit anon.

# 69
>>3602
>My guess as an amateur is that you're exposing some temporally-unspecified behavior in the IR diode, maybe a cascade of some quantum tunneling effect or other.
Nah. The problem was twofold. For one, I did not have enough voltage drop across the resistor to properly control the IR LED, where tiny changes in the supply voltage would cause relatively large changes in the current through the diode, and in the ADC result. 3.3V supply - 1.2V LED drop - 0.7V transistor drop = only 1.4V. For more on this phenomenon, look up why you can't use blue or white LEDs with a 3.3V supply. Anyway, this is another significant noise factor with this setup. Unwanted variations in the ADC signal voltage as well as variations in the ADC reference voltage is one noise source, but unwanted fluctuations in the LED supply voltage and current is another, likely more overlooked one. I have moved to a separate linear-regulated 5V supply for the LEDs for now. Still experimenting with that and MOSFETs. Driving the gate of a P-channel MOSFET with an NPN transistor is showing promise for now.

The second issue I was having was just loose and shitty breadboard connections. Major fluctuations all across the board depending on which way a pin was leaning or what hole it was in, or if I used one dupont cable to connect two breadboard grounds versus two, big pain in the ass. Got around it somewhat by mocking up on some perfboard, but that's proving harder to experiment with. Going to make up a PCB. At least that way it's easy to desolder and change component values, while giving me solid connections and a proper ground plane.

# 70
>>3604
Nice read.

>>3606
I agree that any complex robotic system will require a number of processors. This is already the case, in fact, as most all digital sensors will incorporate a microcontroller internally to convert to do ADC, timing, SPI/I2C communication, calibration, etc. This is something that you and I should keep in mind going forward. Rather than a flat, multi-MCU setup where processor 0 handles functions A, B, and C, and processor 1 handles D and E, each function of the robot should have it's own processor, and communicate with the "main" processor by a standard protocol (I2C or SPI, etc.). This will keep the system modular, allowing you to change implementation of say, the motor control, without having to change your high-level motor control code significantly. This will also extend the life and usability of the platform by allowing you to swap in different microcontrollers for high-level control, like ESP32, STM32, etc. with no changes to the underlying sensor and drive systems.

# 71
>>3608
Get yourself a couple of UART to bluetooth breakouts. 
https://www.banggood.com/HC-05-Wireless-Bluetooth-Serial-Transceiver-Module-Slave-And-Master-p-908621.html 
One on the Atmega UART and another connected to a USB-serial cable to your PC. Should be plug-and-play.

# 72
So my parts finally came in yesterday, and I took a few hours to whip a little something up. Just a quick mockup to see something in motion. The body is 5mm hard foam board 120mm x 60mm. Wheels are 34mm diameter. Battery is a 2000mAh Li-ion I had lying around. Everything is held on with 2-sided tape. Works fine. 

Some observations:
The supposed 160RPM speed of the motors is a good baseline for this size robot and wheel diameter. Full speed is fairly satisfying while not fast enough to be dangerous, cause wheel slip, etc.

The pull-ups on the L9110 motor driver board are weak enough to not give me any problems even with a 3.3V micro and 6.5V motor voltage.

There is a high-pitched, audible noise coming from the motor controller or motors when driven with 3906.25Hz PWM (8Mhz clock / 8 prescale / 256 counts). A good PWM frequency for brushed DC motors is apparently in the 10-50Khz range. A 16Mhz 5V Atmega would give me 7812.5Hz at the same settings. Eliminating the prescaler gave me 31250hz PWM and no noise, so I'm sticking with that for now. A 16Mhz Atmega would be double that frequency, with likely huge power losses in the MOSFETs. Flip anon, I'm interested in your PWM frequency and timer setup if you wouldn't mind filling me in with how you're doing that. I am using both of the 8-bit timers, Timer0 and Timer2, using the 4 output compare registers, OCR0A, OCR0B, OCR2A, OCR2B to control left PWM forward, left PWM reverse, right PWM forward, and right PWM reverse.

>missing filename:
output.webm

# 73
>>3625
Good architectural design approach.

# 74
>>3623
Thanks man,

https://www.invidio.us/watch?v=7HB6xLe2f3U

>>3624
>>For more on this phenomenon, look up why you can't use blue or white LEDs with a 3.3V supply. 
I actually spent a whole day researching why people hated blue LEDs since they've been overused in most consumer electronics since they were too dazzling.  As lighting, white LEDs are just phosphor-coated blue LEDs and blamed with not giving enough near infrared natural light.

I think I might just go old-school with red LEDs for my waifus especially as I start to use 3.3V circuits and have no nearby high power rails to connect to.  They will look like evil succubi, but at least they won't disrupt your sleep unlike blue colors.

>>3625
Right now I'm maximizing real estate and minimizing pin counts, but definitely for the larger robots I'll break out the functionality.

>>3626
I have those, I'm saving them for larger robots that can be remote controlled via bluetooth serial.  I admit I also want an excuse to use RGB LEDs.  Color-blind people apparently hate them, so any final waifu models will probably use discrete indicators.

>>3627
Cool!

In one of my sumobots, I was using Timer0 (16 MHz / 64 default / 256 = 976.5625Hz) via pins 5 and 6.  It was not a conscious decision, they were the available digital pins I was left with.  The motor module gave off a slight buzz but wasn't annoying.

Some more progress pics… the main board can now fit two pro minis back to back, with one pin spacing gap in between.  They will communicate via i2c. Thankfully I only need 18 out of the 24 pins (9 pins per side per arduino) so just had the side with extra pins jutting out.  I should have bought 10 pin female headers but ended up using 15 + 5 per side with one of them trimmed otherwise they won't be flush.

I'm also creating an output "shield" which will house all the RGB LED outputs as well as pass on the SPI lines to the matrix displays.  I've decided to have the power in come in through the shield also.  There's barely any space left on the mainboard.

Next up are the rear board (for housing the pushbutton when the mouse backs up against the wall, and the power source for the motors), and another undercarriage module for the rotary encoders.

# 75
>>3627
Very nice to see your little moebot in action anon. It looks like it's very agile and quick! Glad to hear you found a good solution for both power and finicky connections.

>>3629
>https://www.invidio.us/watch?v=7HB6xLe2f3U
Cool af tbh. I wonder if one of us **or ''all'' of us together?** manages to make a business of this one day that we can hire women to drive some types of waifubots like this.

>They will look like evil succubi, but at least they won't disrupt your sleep unlike blue colors.
kekd.

I like the layout and design of your shield anon.

# 76
Dual Supply Power module that goes to the back (I'll have to redesign the rear end fixture of the chassis).

It has a linear 7805 that will power the microprocessor circuit (they say it gives less noise so ideal for analog-digital conversion), and also a buck converter / step-down switching power supply which will be used for the motors.

At the back are some debug switches and the main interrupt pushbutton which will tell the robot to start/stop measurements from its position with its back against the maze wall.  It's a mouse click pushbutton switch so I'll need to design the big clicking plate that will push it.

Currently working on the main outputs module, and then a logic board (which OR's and AND's some of the logic to feed into the limited pins of the arduinos), and then I'll post the schematic of each board and how they fit together when done.  The way the boards are split up is in case I mess up and decide to redo some functionality, I only need to discard one board and the rest will still be usable.

# 77
>>3631
Looking good.

>It has a linear 7805 that will power the microprocessor circuit (they say it gives less noise so ideal for analog-digital conversion),
It does. You have the right idea. 

>and also a buck converter / step-down switching power supply which will be used for the motors.
Stepping down, eh? What is your supply voltage? I'm using a boost converter to step up the 3-4.2 from a 1S LiPo to 7.5V for my motors. I get about 1.4V drop across the motor drivers. The video I posted earlier was at 6.5V. I have a little bit more headroom now at 7.5. Pic related is a power supply module I sent off to the board house Saturday. The size and layout is just trying to be compact for now, I'll work in into the robot later. It features a micro usb port for charging, will charge a 1S LiPo at ~490mA, has a switch to cut wall power and switch to battery, a boost converter to provide 7.5V for the motors, followed by a linear regulator for 3.3V for the logic. Total power is 2A. Not much in the way of headroom, but good enough for now. 40mm x 30mm, M3 mounting holes. Power and charge indicator LEDs. All solid capacitors, no tantalums. Total of 20 boards. May make extras if they work out and anyone was interested. Motor voltage is adjustable with 1 resistor and the linear regulator can be 1.8V, 2.5V, 2.8V, 3.3V, 5V, whatever.

# 78
It's nice to see you guy's progress. Thanks for the pics and descriptions.

>>3631
That's a good idea to add debug switches anon.

>>3632
Looks like a nice design anon, pretty compact. Any idea of the mass?

# 79
>>3632
I'm using plain AA or AAA batteries to make 9V, got kinda used to it.  AA's have more throughput than the shit-tier LiPos at the hardware store (1200mAh) .I have some 2S battery protection circuits (for 7.4V), I got some step ups too but don't plan to use it except for the smallest of projects.

That is really cool that you have custom PCBs to be manufactured, and surface mount components too, wooo.  I can't believe I still managed to get 74HCXX series and 74LSXX logic gates in DIP format, they were probably rotting in some warehouse for 20-30 years.  When it comes time to make my own custom PCBs, they'll be for DIP spacing for my own sanity, also I'm planning to unify a common waifu architecture first.  For example just have one common torso but can attach to a bipedal base (becomes a wrestler), a hexapod base (becomes a crawler / spider robot), a tracked chassis (becomes a land drone FPV camera scouter) or differential wheels (becomes a shop assistant / Pepper clone).  This micromouse is essentially the tech prototype for a future shop assistant waifu that navigates larger "mazes" such as department store aisles but using longer range lidar/ultrasonic/time of flight sensors.

# 80
>>3634
Ah, gotcha. 

>That is really cool that you have custom PCBs to be manufactured, and surface mount components too, wooo.
Thanks. I wouldn't say manufactured though, I still have to do all the assembly myself, which is easier than it looks. If you look close enough you'll see there's plenty of pad around every component. I hand-solder these sizes at work everyday. No special tools, either: forceps, normal soldering iron tip, regular old solder. You get a feel for it pretty quick. It's actually through-hole that gives me a hard time these days, especially when a lead is connected to two ground planes and refuses to heat up. I'll do a thread one of these days about how I do a design from start to finish, maybe a breakout for a lesser-known micro like the Attiny841/441 or something.

# 81
Have either of you guys read ''The Door into Summer'' by Robert A. Heinlein? I believe you'd both appreciate it. :^)

>>3634
>also I'm planning to unify a common waifu architecture first
This seems like a really good idea.

>>3635
> I'll do a thread one of these days about how I do a design from start to finish, maybe a breakout for a lesser-known micro like the Attiny841/441 or something.
That would be great!

# 82
>>3636
Not yet, will do, thanks for the recommend!

# 83
Remind me to use the services of a PCB etching service in the future.  It's going to be 3 months and this robots only slowly taking shape because of the sheer soldering I have to do.

New updates…
-added buzzer in the extra space on the power supply board
-finished RGB LED indicator board.  For some reason one of the LEDs has a bluish tint even though there is no connection at all to any of the blue leads.  Egh, whatever.

The gazillions of transistors you see include not just the visible LED driving ones here but the drivers for the Infrareds as well.  I labeled them B1 (base1), B2, B3, B4 etc. and C1 (collector1), C2, C3, C4, etc. The MCU signal goes to the base signals (through resistor), while the IR leads which are active low connect through to the collectors.  There still aren't enough for all the IR LED pairs, so they will drive them two at a time, ideally pairs that point in opposite directions.

# 84
>>3638
Looking good. Have you nailed down the circuit for your IR LEDs/phototransistors yet? I've been kicking around a few different patterns (NPN transistor, P-channel MOSFET, N-channel MOSFET), and various resistor values for the receiving side, but noise and loose connections are making it hard to see whether I'm improving it or not. I'd like to hear what you're using. I need to get a design in place so I can move onto the movement and object avoidance logic. 

Pic related is the power supply PCB I posted before. It charges and discharges just fine. No more occasional microcontroller restarts when changing both motor directions quickly. I'm able to set the motor supply voltage to 6.6, 7.0, or 7.5 volts with the value of resistors I ordered with it. Running at 7.5V right now for testing. The charge LEDs are not working as they should because I followed some design on the internet, and didn't look closely enough at the reference materials. Oh well. It's already fixed, along with the layout being tightened up overall. Also fixed up the power loops around the buck regulator, they were bad before, but nearly ideal now. I'll get pics up when I finish the silkscreen. Will reorder when I do the sensor or motor boards, combining shipping makes it like 5 USD for 5 (x4) boards shipped.

# 85
>>3639
I'm so used to painting and 3D programs that circuit design software seems counterintuitive to me, so handdrawn it is.

Top portion is general format for IR sensor boards (there's more than one, this is the main one).  All active low driven, both for transmit and receive.

Bottom portion is essentially
>>3608
but with 470 ohm resistors since I don't consume too much current.  Depending on the pwm frequency that is mapped to the infrared receiver's DAC value, the LED glows from green to red.

The extra transistors are for driving the infrared transmitters (or groups of them at a time).

I have tested them piecemeal, but I'm not yet done with all of them, still soldering some more.  I've slowed down a bit because of life issues.  I'm currently sorting my way through the headpat circuits, which is basically some crazy contraption made from interrupts through AND/OR gates and transistor S-R latches. (since I exhausted the gpios of both pro minis and cannot get another MCU due to lack of space).  I'm basically reusing the pins for the infrared transmitter drivers (B1 through B4 etc) to drive the interrupts when two or more of them go logic high (since in conventional operation they only cycle one at a time).

# 86
>>3640
Gotcha. I was more wondering if your resistor values and such were set in stone yet. I'm still dragging my feet on an IR sensor PCB. Going to stick with the TCRT5000 and n-channel MOSFETs for now. I've got the resistor values and such more-or-less figured out, it's just the physical arrangement giving me problems, how to make a compact board with an I2C interface, that I can arrange in a variety of positions and directions. I whipped up one board already, but it's a little over-engineered for a first prototype. It's getting binned and a simpler one made up today.

Alright. I'm now facing a bit of feature-creep with my bot here. The more I work on it, the more I learn, the more ICs I come across and want to try out, the more the scope keeps expanding and, I'll never finish at this rate. I'll make a PCB, it'll have some little bug with it that I want to fix, and since I'm scrapping the traces and layout I might as well optimize the layout, and add this IC, and this feature, and two more of these… ad infinitum. So I'm going to go ahead and do something I should have done a long time ago, lay out the detailed design goals for this project.

What it is:
1. Autonomous floor-dwelling "micro mouse" style robot.

The goals:
1. Further my robotics education.
2. Allow me to make modules that can be reused or expanded on for other projects.

What it will do:
1. Explore it's environment autonomously.
2. Be rechargeable.
3. Send telemetry back to a base station.

How it will do it:
Exploration
1. Environmental sensing and obstacle avoidance using horizontally-arranged ranging sensors, in all likelihood simple IR LED/phototransistor pairs.
2. Random movement in a planar environment (my living room/kitchen since there are ~4cm step-ups leading to the rest of the apartment)
3. If possible, produce a heat map of the room by combining crude wheel odometry with sensor readings over time. If it produces something even vaguely box-shaped, I'll be impressed.
4. The motor driver ICs will be from Texas Instruments DRV88xx line for high performance, likely DRV8871.

Recharging
1. The battery will be a flat, 3.7V lithium polymer type between 1000 and 2000mAh.
2. A physical switch will change modes between charging and running.
3. Charging will be done through a standard 5V micro-USB phone charger providing at a minimum ~450-500mA.

Telemetry
1. The reported data will include: current motor PWM value, motor current and voltage (= power), detected obstacle direction and distance.
2. Communication will be done with Bluetooth low energy, 4.1 or 4.2.
3. The robot will use a surface-mount module, the receiver will be an ESP32 connected to a PC by UART or connected via wifi and sockets.
4. Position tracking and room mapping will be handled by the receiving PC, most likely an Orange Pi Zero.

General/Other
1. Chassis will be 1.6mm FR4 printed circuit board, under 10cm x 10cm.
2. Drive system is 2 6V "N20" gear motors in differential drive configuration with a bearing in the rear for balance.
3. Subsumption architecture using Attiny841 as I2C slaves to control all sub-systems (motors, current sensors, IR sensors).
4. "Main" MCU will be an AVR micro of some variety, focusing on communication (with sensors, motors, and base station).

And that's it for version 1. Deciding all this and writing it down will allow me to produce SOMETHING in the short-term that I can use and evaluate on the whole. It gives me a completed physical object that I can appreciate, as well as a defining line between version 1 and version 2, version 2 giving me a place to put all of the ideas in my head for the time being. Ideas like automatic wireless inductive charging with battery level monitoring, 7.4V or higher battery pack with balancing, absolute wheel odometry, LIDAR, larger size/different wheel configuration, on-board higher-level processing via SBC or 32-bit MCU, etc.

# 87
>>3641
Those are pretty cool goals for a first roamer bot.  In my case it's just going to be standalone, no remote communications (that's for future intermediate bots).

Finally finished all the custom modules, they were tested individually so next would be testing them all together hooked up to the dual Pro Minis on a breadboard.  If it goes well then I can proceed to hardwire the mainboard.  I should really go for custom PCBs next time.

# 88
>>26
This is awesome. Good stuff!

# 89
>>3642
that's pretty impressive work anon.

