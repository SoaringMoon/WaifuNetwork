# 1
Fully printed, it is quite the chonker.

Two heavy duty servos (110kg.cm torque or greater. 12 to 24 volt) in the shoulder.
Two 60kg.cm servos (DS5160SSG) in the bicep
Five 20kg.cm servos (PDI-6221MG) to move the forearm and fingers.
One micro-servo in the palm to drive the thumb.

# 2
Stupid question, what material did you print with? There are some nylon-based printing materials now that are apparently extremely strong, but also probably rather expensive.

# 3
>>6323
Very exciting progress Anon. I'm sure we'd all like to see some motion tests for her arm soon. This is for Sophie, correct?

>it is quite the chonker.
Heh, I'm sure she will lose some dieting. :^)

# 4
>>6325
I just used PLA (20% triangular infill for the hand and forearm, increasing to I think it was 30% in the elbow and 40% octohedral infill in the shoulder pieces) . Nylon filament is more expensive and prints considerably hotter if I remember correctly - this is just a prototype so I could do.without the higher electricity cost and potential strain on my 3D Printer. I decided against PLA mainly because of the warping and cracking issues. Honestly, PLA is  wonder-material for this sort of work! Cheap as chips, easy to work and surprisingly robust and reliable. I once left a PLA plant pot out in the garden for a year. Washed off the dirt and it was good as new!

# 5
>>6327
D'oh! I meant to write "I decided against ABS due to heat warping and cracking issues". Not PLA. PLA has never cracked on me once in hundreds of prints! (Slight elephants foot in taller prints but that's all).

# 6
>>6326
This arm has served as a test piece (first robot hand and arm I've ever constructed, so I learned quite a bit). The hand is already operational although the finger-stringing could do with some improvement (it's a bit arthritic at the moment XD). Just waiting to receive a heavy duty servo. I also have to run tests and get more familiar with my new benchtop power supply. Lots to do, but I must focus on electrical/fire safety first, then eventually I will be in a position to get the whole arm operational. After that, I plan to print out the lighter V2 arm which I am currently designing with Proto1 as a base. That will be the arm I upgrade Sophie with.

# 7
>>6329
>but I must focus on electrical/fire safety first, then eventually I will be in a position to get the whole arm operational.
Very wise! Please proceed with caution Anon. We look forward to your status reports.

# 8
Have finished making a lighter version of Ryan Gross's "Proto1 Humanoid Robot Arm". I call my heavily cut-down version the "Protolite".
Have uploaded to the usual repositories:

Googly Drive
https://drive.google.com/drive/folders/18MDF0BwI9tfg0EE4ELzV_8ogsR3MGyw1
MEGA
https://mega.nz/fm/InpynKDL

I want to try and make a light robot arm that can be used as a no-frills base for robowaifus. The Proto1 is built like a bodybuilder's arm, but I wanted something a lot more slender. Have kept the elbow and shoulder joints the same (mainly for strength reasons). But I have also uploaded all of the simplified .stl meshes which have about 90% less geometric density and are intended to be easier to make changes to - in case any other anons fancy a crack at redesigning one part or the whole arm.

# 9
>>6481
Correction, sorry. I have finished DESIGNING the Protolite v1. Now I just have to print it. Lots of things will go wrong. But at least I am at a stage where I have a design to test.

# 10
>>6481
>>6482
That's very good news to hear, thanks Anon! We hope the printing and other fabrication steps go very smoothly for you. Please keep us updated.

# 11
I have considered getting a CNC machine for a while now which would really open a lot of doors for me in designing and fabricating parts out of stronger materials. Upfront cost would be worse (and I'd want something quality) but the durability would be especially helpful especially with things like joints. If I ever get one I'll take pictures of it and cut parts with design advice from anons.

Good luck on your work anon, hoping to see more news drop from you, it's inspiring.

# 12
Actually it might be more cost effective for me to build a CNC machine and I have not considered that possibility until now. Might be more in the spirit of this board as well, as buying a CNC machine might be too out of reach for many anons. Obviously, work with 3D printing is still extremely valuable and should not be stopped. Good luck and godspeed.

# 13
>>6325
Nylon isn't that expensive, but it's harder to print. The printer should have an enclosure, and maybe even an heater insinde. That makes the printer more expensive. Same for Polycarbonate, which would probably even work better.
However, this would most likely the better route compared to using a CNC machine to build metal parts. 

>>6323
>>6481
Well done, progress much appreciated.

# 14
>>6495
Nylon is not much more expensive than PLA, but when I said nylon-based I meant the ones that mix in other materials like carbon fiber for strength. Just checked price on one website and the material is about twice the price of PLA. I'm not sure how it would hold up against metal for smaller parts that need high durability but it's worth a try. I have heavily considered getting a CNC machine so if I actually owned one, I personally can't see not using it. Obviously it wouldn't be used for everything, but I can see a lot of value in metal joints. %%Not trying to break my waifu's legs during sex after all.%%

# 15
>>6496
In my experience so far, the main failure point in this kind of cheaply manufactured robot is the servo horns. Very difficult if not impossible to make functional servo horns out of PLA for anything above micro servos (I have tried and after a few dozen movements, the metal servo output shaft always wears the gripping teeth of the PLA servo horn away, which means that the output shaft just rotates inside the servo horn and the joint won't move) This is a common problem with cheap, plastic robot parts. It even happened to a cheap factory-made Arduino robot arm that I purchased. Most standard strength (20kg.cm to 60kg.cm) servos come with ABS plastic servo horns. As long as you don't exceed the carrying weight that the motor is designed for, these should be fine. But if you want long-lasting shoulder or hip joints, it's gotta be metal servohorns all the way...

Also, I think a problem that I am going to encounter making a robot arm out of PLA is heat deformation of the biopolymer closest to the larger servomotors when they get hot. I haven't encountered this problem yet, but if it happens, I plan to widen the boxes which contain each servo motor and insulate the base and sides with small blocks of wood. This will hopefully mean that the servo motors can heat up without melting the very parts that hold them!

# 16
>>6500
Thanks for the good advice about the servo horns Anon.

>and insulate the base and sides with small blocks of wood.
I wonder if some kind of sheet aluminum (spun aluminum is best) might be a better heat dissipation choice? After all, you don't really want to insulate the servo motors either, but rather draw heat off. Probably some kinds of ideas in the ''Robowaifu Thermal Management'' thread >>234 could help.

# 17
>>6501
Interesting. Thanks, anon! I may just leave vent holes over any servo areas that get especially hot...as long as the arm structure remains strong enough not to snap. Plus this has the added benefit of reducing weight and material use even further. We'll see...

# 18
>>6500
Considering CNC is also used heavily for making wood parts I was wondering if there would be any use for wood as a material in building.
>>6501
Copper would conduct heat better. This would also be interesting for discussion about using the heat generated from batteries, processors, any and all electronics in order to warm the robowaifu up. %%After all you'd especially want the pussy to be warm, so conserving at least some of this heat and reusing it would be smart%%

# 19
>>6508
Like all engineering, everything's a trade-off. While copper would undoubtedly be a better thermal conductor than normal aluminum, it's also notably heavier/weaker. And ''spun''-aluminum is already pretty remarkable in it's cooling abilities as is.
>This would also be interesting for discussion about using the heat generated from batteries, processors, any and all electronics in order to warm the robowaifu up.
Yep. It's already being discussed in some depth in >>234 .

# 20
>>6508
If your robowaifu is going to have moving legs then creating a warm vag may be simpler than expected. After all, two of the largest servos or stepper motors will have to be located within the pelvic area, and these motors soon warm up after about 15 minutes of operating under load. I have a NEMA17 at the front of my 3D printer and it gets toasty warm just from moving the buildplate back and forth.

# 21
Significant breakthrough! The 180kg.cm high-torque servo motor is now operational. Posting guide here to show how I got it working. 

I realized that this kind of complicated looking electronic hardware is a BIG turnoff to a lot of people who are trying to make a large robot. Most instructions online either had parts missing and were written in Chinglish or videos by a couple of Indians whom I could barely understand.

Fuck that. I just wanted it to work ASAP. So without further ado:

Hardware Used:

High Torque (180kg.cm) Servo Motor DC12 Volt to 24 Volt with steel gearing.
£30 ($39.58) each at time of writing.

Elegoo MEGA2560 R3 (Arduino MEGA2560 Clone) about £13 ($17.15) at time of writing. You can get cheaper ones but MAKE SURE THAT YOURS COMES WITH A USB CABLE! 
(You don't actually need a power adaptor because the benchtop PSU will be providing the electricity, but it's a good idea to make sure that a plug is also included so that you can use your microcontroller for other applications as well).

The power plug I got with mine was an Elegoo brand AC-DC adaptor
Input:100-240 Volts AC 
Output: 9 Volts - 1 Amp DC
The data cable was a blue type A to type B USB 2.0 cable.
The type A end goes in your computer's USB port, 
The type B end fits into the socket on your Arduino/Elegoo Mega.

Eventek KPS3010D DC 0-30 Volt 0-10 Amp Benchtop Variable Power Supply 
Mine cost £75.99 ($100) and included a power cord and two sets of crocodile clips.

Jumper wires - male to female 
You can get over 100 of these for about £5-6 ($6-8) off Amazon. 
Male to male ones are often included in the pack as well.
You'll only need a couple of jumper wires to connect one high-torque servo, but of course robowaifus include many circuits and servo motors so a pack of 100+ is useful!

Standard Household Electrical Cable  
A 2m extension lead costs about £5-6 ($6-8) or you can get 10m of cabling for about £11 ($14.50).

I used a craft knife and metal snips to strip the outer cable wall off and get a couple of 30cm (1ft) lengths of power and neutral cable. 

I then used a wire stripper to strip about half a centimeter of covering from each end
and wound the exposed copper filaments into a tight helix between my fingers.
These wires can then be connected between your PSU and the positive and negative screw terminals on your high-torque servo motor (see wiring diagram).
 
I know these benchtop power supplies expect you to attach a black negative cable and a red positive power cable but in the U.K. the power cable (positive) is brown and the negative cable is blue.

Wiring (also see circuit diagram)

Negative terminal on PSU ----> Negative screw terminal on servo motor
Positive terminal on PSU ----> Positive screw terminal on servo motor

GND on servo motor ---->GND on Arduino MEGA
PWM on servo motor ---->PWM Pin 9 on Arduino MEGA

Once your high-torque servo motor is connected to the ArduinoMEGA and PSU, 
load up ArduinoIDE and make sure that you have selected the correct microcontroller from the

Tools> Board:> ArduinoAVR Boards menu 
(in this case ArduinoMEGA or MEGA2560).

Then make sure that serial port is operational by checking 

Tools> Port:>"COM X" 

For example, mine was set to COM3. 

If you have problems here you'll need to open Device Manager and troubleshoot it.
Ports (COM & LPT) is just below Portable Devices. If you can't see any Ports (COM & LPT) option, press 

View> Show hidden devices 

and it should appear.

Once your board and port are set, you should copy and paste the following code into Arduino IDE. This is the "Sweep" servo example sketch.

```cpp

/* Sweep
 by BARRAGAN <http://barraganstudio.com>
 This example code is in the public domain.

 modified 8 Nov 2013
 by Scott Fitzgerald
 http://www.arduino.cc/en/Tutorial/Sweep
*/

#include <Servo.h>

Servo myservo;  // create servo object to control a servo
// twelve servo objects can be created on most boards

int pos = 0;    // variable to store the servo position

void setup() {
  myservo.attach(9);  // attaches the servo on pin 9 to the servo object
}

void loop() {
  for (pos = 0; pos <= 180; pos += 1) { // goes from 0 degrees to 180 degrees
    // in steps of 1 degree
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
  for (pos = 180; pos >= 0; pos -= 1) { // goes from 180 degrees to 0 degrees
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
}
```

Then press the Upload button.

As soon as the code uploads successfully to your ArduinoMEGA, then the high-torque servo
shaft should repeatedly move between 0 and 180 degrees.

Thats it. Functional high-torque servo!

# 22
>>6729
Freakin' awesome. Thanks alot Anon. This has been a long term concern for me for our robowaifu's shoulder and hip joints. All the hard work for your careful post appreciated! :^)

# 23
>>6730
A pleasure! 

Now I just have to get more than one high-powered servo working. It should be fairly easy. Pretty sure I can screw another motor directly into the PSU's front terminals. For more, I'll probably need a breadboard or some kind of splitting device so that several more connections can be made to further motors. Whatever I try, I must keep exposed conductors to a minimum. More high-torque motors will draw more current of course, but this kind of experimentation is exactly what a benchtop power supply is made for. 

(BTW, my high-torque servo came with a servo wire and a 10K potentiometer, but you can get this working without having to use either of them.)

# 24
>>6731
It was easy to get two running. That's enough to move one shoulder in the Protolite arm. Any more is gonna require some careful wire splicing. The 60kg.cm servos and 25kg.cm servos I have already operated because they can just run off a couple of Arduinos with servo shields like most hobby electronics. Just gonna leave this very short side-by-side comparison of the code here.

# 25
>>6734
Good news Anon, grats. I imagine with your careful attention to weight reduction for her arms this dual-arrangement should be good enough to go on with. Well-commented code btw. :^)

# 26
Nice work as always

# 27
>>6496
Okay, if you wanted some CNC anyways it's another thing. I just think plastics is quite durable, also one can use standard metal parts for reinforcement. I personally think about building a CNC mill for cutting metal sheets. This shouldn't need to much power. These parts could then be separated from each other with layers out of other materials, and so the metal layers could be used to transport electricity for power and communication while adding strength.

>>6729
How big are these motors? And where exactly do you want to put them? Maybe you wrote that already and I overlooked it.

# 28
>>6777
They're 9.55cm long and 6.5cm wide. Two of them are needed in each shoulder so that it can move in x,y,z. They are common and cheap, but heavy (each one weighs 530g) and noisy. But I don't really care about the noise.

# 29
>>6797
Okay, thanks. That's not small but also not that huge. So she might be able to lift 4kg using both arms, which is sufficient. Noise might later be mitigated using quarz sand or other material, noise cancellation or some sound overlay.

# 30
This kind of servomotor can be purchased upto a torque of 380kg.cm. It obviously costs more, and Ryan Gross recommends servos rated at 110kg.cm+ for the full-size Proto1 arm, so this 180kg.cm is probably overkill but they were on offer so I went for it. I'll probably use a couple of 380s eventually. However these very strong motors are used to drive the wheels on 1:1 scale RC cars. So I if I make a programming error my robowaifu may inadvertantly crush me to death. Maybe I can become the first recorded case of death by robo-snu-snu?

# 31
>>6886
>Maybe I can become the first recorded case of death by robo-snu-snu?
leld

# 32
Well, the Protolite hand is very nearly finished. The only problem I'm having is with that little blue micro servo that is supposed to flex the thumb left and right. I was stupid and bought a small pack of what are very probably counterfeit TowerPro micro servos from some Chinese supplier on Amazon. They make excellent finger-burners, but are otherwise useless. Gonna be more careful who I get them from next time!

# 33
>>7004
Wow, that's quite an improvement you've made there Anon. If you keep going on like this, you apparently will come up with a state-of-the-art robowaifu arm/hand design. Go, go, go! :^)
>finger-burners
I'm unfamiliar with that concept?

# 34
>>7006
LOL I noticed that while the rest of my servos operated normally, these would just heat up where the 555 timer is. One of them even melted through the external casing. So to prevent them getting too hot, I hold a finger over the bottom every time I test them. Hence the "finger burner". This happens even at just 5V so not sure what the problem is. Just a helluva lot of resistance and heat coming from somewhere in the servo driver circuit. Gears move okay when checked manually.

# 35
Great work, and thanks for sharing.
I looked up the servos in the forearm: http://www.jx-servo.com/en/Product/STANDARD/SD/555.html
Did you or the original creator consider to put them in a line, so the arm would be thinner and longer? Is there a reason not to do that? They are circa 4x2x4 cm, so five would be 20 cm, which is a bit much, but four would fit that way.

Also, how much will the fingers then be able to hold and lift? How is it calculated, considering they're connected to strings? Seem to be quite strong...

# 36
>>7011
My pleasure anon! The original creator (Ryan Gross) positioned the forearm servos like that because the next part up the arm is another 20kg.cm servo which connects to the back of the forearm case (effectively the wrist is above the forearm rather than below). 

You could change it so that the 4 servos are all in a line, but you need a gap between each servo for the mounting tabs+wires. By all means download the Protolite arm from Sophie's file repository and experiment with the .f3d file in Fusion360, but I reckon you'll end up with overly long forearms. TBH I am still working on shortening and downscaling the joints because the rest of the arm is still too long for the size of my robowaifu. She's only a little lady, but then that makes her parts easier and cheaper to prototype.

# 37
>>7023
Oh yeah. The hands can definitely hold light things like cups, a comb, a toothbrush etc. I have to find some rubber pads for her palm and I'm going to squeeze silicone caulk on the inside of the fingers to make the hand more grippy. Then hopefully she will be able to hold heavier things such as my socket wrench. The "ligament" material is BZS monofilament 40lb (18.4kg) clear fishing line. It is very strong, stronger than the ligaments in my own fingers. 
So it's just the weakness of PLA biopolymer coupled with the relatively small size and torque rating of the forearm servos that limit grip strength. If you were to 3D Print the forearm in ABS or Nylon and maybe scale it up 20% or so, you could definitely fit more powerful servos in. Then your robowaifu would have an iron grip!

