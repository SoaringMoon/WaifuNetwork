# 1
#fairybot #vocaloid
![[Pasted image 20220522122847.png]]
![[Pasted image 20220522122853.png]]
![[Pasted image 20220522122908.png]]
![[Pasted image 20220522122914.png]]

Height; 15cm  
Type; Vocaloid  
  
I'm making it in as natural looking way as I can, this means a bone structure and a similar layout of the electronics and components as with a living humanoid  
  
This is a prototype version that I'm working on, I might change things later and make modifications or adjustments to the design or components

The brain circuit is a MSP430 Ultra-Low Power MCU  
eZ430-F2013 Development tool  
  
The target board is removable and works by itself (given that it has electric power to operate)  
  
I could insert more than one potentially and wire them together for more functionality  
  
Its small enough that it fits (its about 2cm wide and 2cm long circuit board)  
  
plugs in with usb and can be programmed with C programming language to control  
  
8 inputs/outputs (which can be further linked to give more inputs/outputs)

![[Mini Lapis Old Thread 02.png]]
![[Mini Lapis Old Thread 03.png]]
![[Mini Lapis Old Thread 04.png]]
![[Mini Lapis Old Thread 05.png]]
![[Mini Lapis Old Thread 06.png]]
![[Mini Lapis Old Thread 07.png]]
![[Mini Lapis Old Thread 08.png]]
![[Mini Lapis Old Thread 09.png]]
![[Mini Lapis Old Thread 10.png]]
![[Mini Lapis Old Thread 11.png]]
![[Mini Lapis Old Thread 12.png]]
![[Mini Lapis Old Thread 13.png]]
![[Mini Lapis Old Thread 14.png]]
![[Mini Lapis Old Thread 15.png]]
![[Mini Lapis Old Thread 16.png]]

# 2
![[Mini Lapis Breadboard 01.png]]
![[Mini Lapis Breadboard 02.png]]

There was more to the thread but I'm not sure where those parts are right now.  

Here are some 2018 pics I posted before

I ended up putting the parts for the mini Lapis into a box so I wouldn't lose the parts, its all still there so I can work on it again but I need to figure out some details with it first, like how to properly do the actuators

![[Mini Lapis 01.png]]
![[Mini Laps 02.png]]
![[Mini Lapis 03.png]]

The joints for the elbows work, the chest was fixed and I was working on spine segments  
  
There was a vid showing the elbow moving but I don't know what happened to the vid

# 3
I tested some circuits like seen in #2 but other than that not much has happened with this project for a while for a number of reasons, but I'll report progress when able

# 4
Hi /hover/ welcome back, I'm glad you found us again. Thanks for the archive pics, etc. I'll eventually restore the rest of the thread, this OP was originally just a placeholder (as with all the threads here). I probably have everything but the pdfs and webms if any were in your thread.  
  
BTW, we owe you a debt of gratitude OP. You really established the _Fairybot_ class of robowaifu for everyone, so thanks. These will be very important in the future when this tech really takes off.

# 5
I could use this as my new thread then  
I have a bunch of tiny neodymium magnets I could experiment with making electromagnet actuators out of, but ideally it would be better to pair them with nickel-cobalt magnets to make electropermanent magnet actuators

# 6
Right now there's these two options;  

[https://hackaday.com/2018/04/17/diy-magnetic-actuator-illustrated-and-demonstrated/](https://hackaday.com/2018/04/17/diy-magnetic-actuator-illustrated-and-demonstrated/)  

[https://hackaday.com/2018/08/25/better-motion-through-electrostatic-actuators/](https://hackaday.com/2018/08/25/better-motion-through-electrostatic-actuators/)  

Static electricity seems to use too high voltage for actuators tho so that might be tricky to get working, which is why magnetic actuators are next in line

# 7
Great, sounds good then. I found this link via your first link. Seems interesting and potentially pertinent.  
  
hackaday.com/2017/02/10/a-micro-rc-plane-builder-shares-his-tricks/

# 8
#shagrug_motor #magnet
shagrug motor seems to use single magnet with a hole in it, with the wire wound directly onto the magnet (and small frame)  

I don't have such small magnets with holes in them and trying to saw or drill a neodymium magnet doesn't really work (they're too hard)  

It takes a while to wind a coil by hand and it helps to have some kinda support frame  

The landing gears seem to use a special wire, haven't looked into that much but its interesting

# 9
#3d_printing #arms #bones #project 
I was looking at the arm again, there's an issue with it getting stuck, it can be seen near the end of the vid in ==post==

The string gets stuck between the "bones" I thought a solution might be to have the thread got through another insulator tubing on the other side but its tricky to get it to align in the right spot  
I've been arduino coding another project and thought of using the MSP for it, but I could get another MSP. Sometimes when working on other projects one finds solutions to the project one was stuck on before.  

I'm still thinking about what the best way way is for making an actuator frame without 3d printing it

# 10
actually, i believe that probably is the right solution anon. find some thin Teflon tubing, but and adhere a tiny little guide-ring from it, and i bet that will take care of the issue for you.  

# 11
![[Pasted image 20220522124207.png]]

I already threaded the thread through red insulator tubing (its from a small red wire)  
I'm thinking now that it could maybe be glued in place with superglue or something, need to think more about how to best go about this  

The MSP430 processor on the dev board seen in ==post== I have access to some of them but only know the location of this one for now, the other ones are seemingly missing I should practice coding more on this one first anyway  

I don't have access to a 3d printer for now, the city fab lab doesn't seem to have open hours anymore, but bizzare thing is they do have them out in the country in smaller towns, I'm pretty sure all the fab labs have 3d printers  

Fab lab works a bit like a library for tools except they're heavy tools so you just use them at the fab lab (these kinda labs are all over the world now)  

Also might be kinda tricky to 3d draw the parts properly but I might do that later actually, this one could be more of a prototype

# 12
#teflon #fusion360
Teflon is explicitly designed to stay slippery. You might have better success using it over plastic insulation.  

ah got it. i plan to eventually repopulate the threads here, including the electronics learning class one.  

cool. i've never been to one yet tbh. expensive?  

There's the Fusion 360 product anon, and Blender too ofc, whenever you feel inclined to design a reproducible system others can create as well.  
  
Good luck.

# 13
This insulation actually works surprisingly well like the video shows ==post==

Booking at a specific time probably costs, but I'm not sure how much and its kinda irrelevant for me right now anyway since I don't have money to spare  
But it used to have open hours here for the public on specific days, I'm not sure if they have those open days since the schedule doesn't show it, but it still reads on the front page that they do, I'll have to check on that better later  
  
I actually happened to get lucky the other day and got a bunch of 3d printing filament for free  
  
Funnily when I started out making models for 3d printing I used sketchup

# 14 
#fusion360 #autodesk
Fusion360 can get as detailed as they come. The Autodesk and cloud lock-in aren't to my tastes however. I think I'll stick with Ton & Blender.