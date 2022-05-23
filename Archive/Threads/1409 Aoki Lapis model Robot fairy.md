# 1
Height; 15cm
Type; Vocaloid

I'm making it in as natural looking way as I can, this means a bone structure and a similar layout of the electronics and components as with a living humanoid

This is a prototype version that I'm working on, I might change things later and make modifications or adjustments to the design or components

# 2
The brain circuit is a MSP430 Ultra-Low Power MCU
eZ430-F2013 Development tool

The target board is removable and works by itself (given that it has electric power to operate)

I could insert more than one potentially and wire them together for more functionality

Its small enough that it fits (its about 2cm wide and 2cm long circuit board)

plugs in with usb and can be programmed with C programming language to control

8 inputs/outputs (which can be further linked to give more inputs/outputs)

# 3
>>266

>> 267

/hover/ BO here, I just found out this board's on here, I see you have the first part of my thread

Stand by, I'll post what I found of the rest of the thread that I archived in the form of pics for now

# 4
>>979

# 5
>>980

# 6
There was more to the thread but I'm not sure where those parts are right now.

Here are some 2018 pics I posted before

# 7
I ended up putting the parts for the mini Lapis into a box so I wouldn't lose the parts, its all still there so I can work on it again but I need to figure out some details with it first, like how to properly do the actuators

# 8
The joints for the elbows work, the chest was fixed and I was working on spine segments



There was a vid showing the elbow moving but I don't know what happened to the vid

# 9
I have this reference model in a digital 3d program which shows what she looks like from all angles

# 10
I tested some circuits like seen in >>982 but other than that not much has happened with this project for a while for a number of reasons, but I'll report progress when able

# 11
>>979
>/hover/ BO here, I just found out this board's on here, I see you have the first part of my thread
Hi /hover/ welcome back, I'm glad you found us again. Thanks for the archive pics, etc. I'll eventually restore the rest of the thread, this OP was originally just a placeholder (as with all the threads here). I probably have everything but the pdfs and webms if any were in your thread.

BTW, we owe you a debt of gratitude OP. You really established the ''Fairybot'' class of robowaifu for everyone, so thanks. These will be very important in the future when this tech really takes off.

# 12
>>993

I could use this as my new thread then

I have a bunch of tiny neodymium magnets I could experiment with making electromagnet actuators out of, but ideally it would be better to pair them with nickel-cobalt magnets to make electropermanent magnet actuators

# 13
>>1001

Right now there's these two options;

https://hackaday.com/2018/04/17/diy-magnetic-actuator-illustrated-and-demonstrated/

https://hackaday.com/2018/08/25/better-motion-through-electrostatic-actuators/

Static electricity seems to use too high voltage for actuators tho so that might be tricky to get working, which is why magnetic actuators are next in line

# 14
>>985

I just found the video

# 15
>>1001
>>1002
Great, sounds good then. I found this link via your first link. Seems interesting and potentially pertinent.

hackaday.com/2017/02/10/a-micro-rc-plane-builder-shares-his-tricks/

>>1004
Great. Please repost any other video files you have, as I have none.

# 16
>>1005

shagrug motor seems to use single magnet with a hole in it, with the wire wound directly onto the magnet (and small frame)

I don't have such small magnets with holes in them and trying to saw or drill a neodymium magnet doesn't really work (they're too hard)

It takes a while to wind a coil by hand and it helps to have some kinda support frame

The landing gears seem to use a special wire, haven't looked into that much but its interesting

# 17
>>1009
Please keep us updated on your progress when you can /hover/.

# 18
>>1011

I was looking at the arm again, there's an issue with it getting stuck, it can be seen near the end of the vid in >>1004

The string gets stuck between the "bones" I thought a solution might be to have the thread got through another insulator tubing on the other side but its tricky to get it to align in the right spot

I've been arduino coding another project and thought of using the MSP for it, but I could get another MSP. Sometimes when working on other projects one finds solutions to the project one was stuck on before.

I'm still thinking about what the best way way is for making an actuator frame without 3d printing it

# 19
>>1034
>I thought a solution might be to have the thread got through another insulator tubing on the other side but its tricky to get it to align in the right spot
actually, i believe that probably is the right solution anon. find some thin Teflon tubing, but and adhere a tiny little guide-ring from it, and i bet that will take care of the issue for you.

>MSP
sauce?

>without 3d printing it
no printer yet?

# 20
>>1035
> cut and adhere*

# 21
>>1035

I already threaded the thread through red insulator tubing (its from a small red wire)

I'm thinking now that it could maybe be glued in place with superglue or something, need to think more about how to best go about this

>MSP

The MSP430 processor on the dev board seen in >>267 I have access to some of them but only know the location of this one for now, the other ones are seemingly missing I should practice coding more on this one first anyway

>no printer yet?

I don't have access to a 3d printer for now, the city fab lab doesn't seem to have open hours anymore, but bizzare thing is they do have them out in the country in smaller towns, I'm pretty sure all the fab labs have 3d printers

Fab lab works a bit like a library for tools except they're heavy tools so you just use them at the fab lab (these kinda labs are all over the world now)

Also might be kinda tricky to 3d draw the parts properly but I might do that later actually, this one could be more of a prototype

# 22
>>1037
Teflon is explicitly designed to stay slippery. You might have better success using it over plastic insulation.

>MSP430
ah got it. i plan to eventually repopulate the threads here, including the electronics learning class one.

>Fab lab
cool. i've never been to one yet tbh. expensive?

>Also might be kinda tricky to 3d draw the parts properly but I might do that later actually
There's the Fusion 360 product anon, and Blender too ofc, whenever you feel inclined to design a reproducible system others can create as well.

Good luck.

# 23
>>1038

This insulation actually works surprisingly well like the video shows >>1004



Booking at a specific time probably costs, but I'm not sure how much and its kinda irrelevant for me right now anyway since I don't have money to spare

But it used to have open hours here for the public on specific days, I'm not sure if they have those open days since the schedule doesn't show it, but it still reads on the front page that they do, I'll have to check on that better later



I actually happened to get lucky the other day and got a bunch of 3d printing filament for free



Funnily when I started out making models for 3d printing I used sketchup

# 24
>>1039
>I actually happened to get lucky the other day and got a bunch of 3d printing filament for free
very nice, gratz.

>Funnily when I started out making models for 3d printing I used sketchup
cool, cool. how was it?

# 25
>>1042

It worked out fine, I would prefer to use something else for detail work tho

# 26
>>1047
Fusion360 can get as detailed as they come. The (((Autodesk))) and (((cloud))) lock-in aren't to my tastes however. I think I'll stick with Ton & Blender.

