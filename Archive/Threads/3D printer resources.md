# 1
Cheap and easy 3D printing is vital for a cottage industry making custom robowaifus. Please post good resources on 3D printing.

www.3dprinter.net/
https://archive.is/YdvXj

# 2
Just in case anyone here has been living in a cave and isn't too sure just how the common 3D-printing of today works, the (((kikepedia))) article is a basic primer (if just a little shilly).

en.wikipedia.org/wiki/Fused_filament_fabrication#Fused_deposition_modeling

# 3
This video here is pure Gold, I will probably post it more then once. It's about keeping in mind that plastics might want to break under stress and how to design a print to get rods and screws into it.
https://youtu.be/j6508J94VsA[Remove]

# 4
Here's a site for printer calibration: https://teachingtechyt.github.io/calibration.html
Lot of information, links, calculators, test print files, etc. even gcode for a temperature tower, or acceleration tower.

# 5
If someone gets a Artillery printer or needs to install Slic3r on a Raspi, around the year 2020. I went through it, so stop guessing:

Forget the manual of the printer, or as soons as you run into problems go here: http://artillery.n3t.ro/
If your bedleveling wheels are falling of while trying to get it right, then the printhead is to far away from bed, sensor needs to moved down, it's in the tutorial above. But use "Z" in Home menu, not "Home" after moving the sensor. The head of my printer punched quite a bit into the bed... 30 min unpacking and then it works?!? My A..!

Slic3r on Raspian:
https://github.com/iot-salzburg/Slic3r
Delete subfolder "local-lib" after unpacking in Slic3r folder
I did  [code]export BOOST_DIR=./xs/src/boost[code] but I'm not sure if this was just unnecessary.
sudo perl Build.PL NOT ./Build.PL
sudo apt install libwx-perl
sudo perl Build.PL --gui

# 6
Oh I forget to mention, you'll need to install liboost-all-dev so you can rebuild the whole thing. And how I just now found out, you need to activate OpenGL in raspi-config before building the gui, also install libopengl0 and libopengl-perl. OMG, now it seems to work!

# 7
>>4723
Yep durability is important.

>>4768
Neat, that's handy.

>>4778
>>4780
Thank you for the tips Anon. 
'_'7

# 8
>>4778
It's nearly two weeks with my printer now, though I did have to wait for my filament some more days. However, I'm still learning about it it. Didn't print much usefull so far, only testing. There's quite a learning curve, at least with cheap PLA and ambitions like wanting to print fast, as hot as possible, and also get to know the limits of the machine. 
This guide here helped me more than some forums and boards: https://www.simplify3d.com/support/print-quality-troubleshooting/
Also looking into /r/FixMyPrint on Reddit is recommended.

How fast you can and want to go: https://youtu.be/V5g32AtYczE
There are several vids on printing fast and strong with a bigger nozzle. I already knew those, and probably shouldn't waste time on trying to find the sweet spot for my 0.4 nozzle. I already got bigger ones, but also some very small ones will arrive soon, so I can try how fine I can go with my printer.
https://youtu.be/jyhLQUQTc9E
I have to hurry it up a bit, since I'm going to receive 6kg more PLA soon, also TPU and PETG.

# 9
>>4949
That must be exciting. Good luck!

# 10
I watched the remarkable prosthetic hand video Anon linked to >>4945 , and it got me interested in resin printing. Can some anon here get us all up to speed on resin printing please? What it is, how to use it, what are the recommend printers, etc.

TIA.

# 11
>>4954
We should rather point to ressources, instead of explaining everything here. There are the common channels on YouTube, with infos about it: Sanladerer, TeachingTech, 3D Printing Nerd, Makers Muse, CNC Kitchen, ... and probably more.
I don't have experience with it anyways, only watched vids and followed some discussions on other boards. However, her some things I picked up:
- It only became interesting for hobbiests recently.
- They are sill more expensive for less build volume.
- They have a bit of a different target group for that reason, people seem to print figurines with high details, some are used in games like D&D. Some owners of such printers sell them to others.
- I think multimalterial/multicolor versions are not possible or difficult with resin.
- It's messier, you need to work on your prints when they're coming out of your printer.
- It's more toxic, you'll need airfilter or a method to get the stuff out of your room by ventilation. Shouldn't be in the same room when printing, just in case.
- Might need to work with bigger amounts of dangerous fluids.
- Getting rid of some used fluids with resin waste, in a legit way, may also be a problem.
- Elegoo and Anicubic are the producers of the most talked producers, though Prusa also offers  one.
-This addon here seems to help, but the vid also shows some of the work: https://youtu.be/TgPxE5gUjlo

# 12
>>4960
>We should rather point to ressources, instead of explaining everything here.
Suit yourself Anon ofc, but I prefer to help Anons out with every thing I possibly know (or can figure out) about anything related to the field of robowaifus. This is far too vast a topic for anyone man to master in a lifetime. If each of us was forced to learn everything from first principles, then this will never happen. I would propose doing otherwise and helping everyone out with everything each of us know.

Certainly the resources are of great benefit as well of course, and we thank you for taking the time to locate and share them here Anon.

# 13
>>4962
Just meant, I won't try to write down all I know on resin printing, but then went on and did it anyways. However, there will be resources with more and more knowledge. I wouldn't try to copypaste all of it here... 

Having that said, one correction: I posted a vid above about this flexbed for such printers. Here's a posting about that from 4chans /diy/:
>>> I don't think it's that necessary, the guy in the video is embellishing the problem to make the product look more attractive. I've seen people gouge the surface violently with the spatula, when all you need to do is wedge a sharp thin blade into a corner and gently lift it to peel off the bottom layer like you would a sticker. Once a corner gets going, the rest just pops off at one point.
>>>Getting a print off isn't messy either because you're supposed to wash and dry the plate with the print on it before you attempt to remove it. It's nice that you can just "pop it off" but you still need to wash both the springy sheet and the buildplate after that so.. it's the same deal.
>>>The argument that "you can use less supports!" is empty too, because unlike with FDM, for SLA supports are a good thing. The first few layers are always overexposed on purpose to ensure plate adhesion, and if those layers are part of the actual print you're going to lose accuracy there. Any holes and gaps will get filled in. Since printing is upside down, you're trying to prevent the part from "falling upwards" as you see it in the slicer preview, not so much to "prop up an overhang from falling down" like in FDM.

# 14
>>4964
> I wouldn't try to copypaste all of it here... 
Ahh I see. BTW, I don't mean to be pushy about something like this. My apologies. We very much appreciate all your input Anon.

# 15
The best way to give FDM prints a nice finish seems to be adding some resin to the surface. Sanladerer does it with SLA resin here: https://youtu.be/nOZaTB34RrI
In the comments others were correcting his errors, like he would need to add a wax layer at the end or put in water to let it cure. So he wouldn't have a sticky layer on top of it at the end. Also, other resins are mentioned in the comments, like ones for fiberglas, maybe also with some added color. Anyone doing any of this, please learn about the security advices first and follow them.

# 16
This calibration guide has been really helpful. Everyone should level ones bed with his first layer check: https://teachingtechyt.github.io/calibration.html

I'm currently looking into mitigating mesh errors in 3d models which I want to print. Sometimes they appear after cutting a cgi model to alter it: https://www.simplify3d.com/support/articles/identifying-and-repairing-common-mesh-errors/

# 17
How to design 3d models for printing, so they can be printed without supports for example: https://youtu.be/SBHHwid7DWM
(Pic related, parts from InMoov head)

# 18
>>5224
Thanks that should be very helpful. Any idea what the comparable strength would be this way?

# 19
>>5225
(Lost my first answer to this, bc this board doesn't store the data... Always keep long answers in an extra file or Clipboard)
I don't know what you mean. There were different parts and approaches in that video. It's about making parts easier to print, with less material, faster, and less time to clean up. Making a design a bit bionic might also  increase strength, though, since you add material into it so it is stronger while printing...
However, if strength is your concern, it's said that bigger layers, more heat is how you get there. If that's not enough, switch to a stronger material. Layers of ABS and ASA are also stronger when printed in an enclosure. Then Annealing is also an option, but quite some work: https://youtu.be/bG8dlxTX3AI or manual reinforcement with a carbon fiber and resin in post processing.

# 20
Where do I get 3d printable files? Not a very interesting question, I thought. Go to Thingiverse. Yeah, and there are other websites...

Now Angus made a video... https://youtu.be/CLRWCtQ5KZY ...wow

Not all of what's interesting about the alternative sources is related to /robowaifu/, but some is: Traceparts let's you download all kinds of models for mechanical parts, which exist as metal version, so you can try it out first... Also GrabCAD: All kind of assemblies... Parts that fit to standard parts, like Nema 17 motor dampers,...
In other cases its so that parts might be useful for someone building a robowaifu, but its hard to tell: Medical models, figurines, stuff from museums ... (Egyptian inspired Catgirls?)

Links to the sites from the video, the description under the YouTube video links directly to the shown files, but I didn't copy those links.
1 - Thingiverse
https://www.thingiverse.com/
2 - MyMiniFactory
https://www.myminifactory.com/
3 - YouMagine
https://www.youmagine.com
4 - Cults3D
https://cults3d.com/
5 - Smithsonian
https://3d.si.edu
6 - NIH 3D Print Exchange
https://3dprint.nih.gov/
7 - GrabCAD
https://grabcad.com/
8 - traceparts
https://www.traceparts.com/
9 - STL Hive NO LONGER EXISTS
10 - The DM Workshop
https://www.shapeways.com/
Maker's Muse 3D Printable Models! https://makersmuse.podia.com/

# 21
>>5234
Thank you for your efforts Anon. We should really create some kind of organized /robowaifu/ resource catalog here.

# 22
>>5235
Answer in the meta thread bc this might go OT/meta: >>5242

# 23
Crush Ribs for bearings: https://youtu.be/0h6dCeATkrU and https://youtu.be/kJ_ukmL5Uls

# 24
>>8208
Neat, thanks.

# 25
Does anyone know anything about LAM? I am looking into Colombia's soft muscle technology and it is really interesting. They custom built their own LAM printer for the project and I am wondering if I could do the same.

# 26
>>8468
Great, for you to participate, but please link to some article, paper or video which shows what you are talking about. I couldn't even find anything using you terms you mentioned.

# 27
Related, printing silicone rubber with a 3d printer: >>8742

# 28
Some guy build a dual extruder for his Ender 3, which receives a lot of interest and praise. It's of course not tested yet by many people during a extended period of time. Might be interesting to look into it during the year, maybe then there's better support for it (the elctronic board and firmware is the problem). Maybe it's gonna be part of newer printers, or I just need another board. It could help for prints with supports or with softer and more rigid parts.
https://properprinting.pro/product/dual-extrusion-system-for-creality-printers-aka-the-rocker/
https://youtu.be/OBB5WuhNhWk

# 29
>>8850
Good luck Anon.

# 30
Here's some diagram about different nozzles for printers. Nothing special, but maybe interesting. I'm using brass so far, but also have steel nozzles in case I might need them. Only recently watched a video where carbon fiber nylon filament actually got some recommendation, the claim was that this combination would print really good on normal printers. Of course, that still needs a harder nozzle than the brass ones, which are good as standard nozzles.   
Just wanted to mention, that it is a good idea to make sure, if you disassemble your printer, to check that the screwheads of your screws a still fine. I wrecked one of my screws in the printhead and now need to drill into the screw and use a lefthand drill to remove it (Not asking for common ideas, already looked into my options).

# 31
>>9145
Thanks Anon! Just in time too, my printer nozzle jammed and I can't print ATM. Maybe this will help me and others here out. Cheers.

# 32
Here some infos on how to print gears the best way: https://youtu.be/JMgXu1rFDJ0 - using PC if possible, putting metal bolts into small gears, print the parts separated in the right orientation for maximum durability, using dual-helical (heringbone) gears instead spur or helical gears.
Heringbone in Fusion 360: https://youtu.be/MtK6yK0NRM0

# 33
>>9798
Nice info, thanks Anon.

# 34
>>9145

That seems off about ruby nozzles. Yes the thermal conductivity isn't very good but there's only a tiny piece of ruby at the end of the nozzle where it matters, the filament gets melted in the metal part before reaching it so the real thermal conductivity of the nozzle depends on what metal it's made out of.



Also saw this recently which seems like a fantastic idea for decreasing print time and wasted filament. Plus parts that would be too wasteful to print due to large supports that would use up more filament than the part itself are now feasible which will lead to new designs.

https://www.3dnatives.com/en/moving-platform-3d-printer-070420214/

# 35
>>9814
You might be right, didn't even recognize that. Also, I don't know. But your argument makes sense.
In regard to your link, thanks, but I'm not to enthusiastic about it. It might get patented, it's probably a complex mechanism, it might only be useful in certain cases, and support material mostly isn't that expensive. The site itself on the other hand is interesting, I should read more news like that.

# 36
>>9846
Huh. That's interesting. I wonder how you integrate inside the software to properly work with the standoffs like that and adjust the length of the supports? I mean, is there a 'use standoffs' checkbox or how does that work exactly?

# 37
>>9846

One of the biggest issues for repeatability with FDM is the consistency in diameter of the filament with tighter tolerances being more expensive due to higher quality control. This investment in a printer would make buying higher quality filament more economical in the long run.



And the most notable thing in that image isn't the filament that wasn't wasted but the time not spent moving the print head around to create an unnecessary part. There's also parts like this that would be difficult or impossible to print without such a platform.



>>9847

They're probably using custom gcode for research now.

# 38
>>9848
>They're probably using custom gcode for research now.
I see. Thanks for the information Anon. I was entirely unaware of any such 'dynamic print bed' type printers. I wonder if they could be usable by hobby-tier robowaifuists someday?

# 39
>>9849
The "hobby-tier" printers are rather ones which aren't industrial or something, but also still for professionals which are using them for prototyping. (I don't like the distinction in pro and hobby). I guess something like that is surely possible, if it has enough benefits. But not for the cheapest models. Looks to me like it requires a core XY system, so the bed doesn't move. Which already makes sense for very small and fast, or the bigger ones. Not so much for the cheap 20+X cm.

# 40
Maker's Muse on 3D printing myths:
https://youtu.be/oX4up29xUuw[Embed]
- It's a new technology (it's 40yrs old)
- ABS ist stronger and better than PLA (if it is, then it's a amalgam, a mix)
- Bed leveling isn't leveling at all (there's also tramming)
- Paper is good enough to level bed (feeler gauge is better)

# 41
New printing material: PVB 
Needs to be kept cooler than 60C, might be interesting for shells bc can be smoothed and there might be cooling underneath such shell. Can be nearly transparent.
>PVB is still a great material for 3D printing and offers a few mechanical advantages over other filaments. According to Prusa Research’s material comparison sheet, PVB has a higher (better) tensile strength than ABS and PETG, meaning it can take more physical stress before snapping. PVB also has greater impact resistance than PLA and ABS and is even slightly flexible, although nowhere near as flexible as truly flexible materials like TPU or TPE.
>Although PVB’s low melting temperature makes it a more easily printable material, it also contributes to worse mechanical properties. The low melting temperature results in PVB having poor layer-to-layer adhesion, which might mean prints are more brittle and more easily snapped.
https://all3dp.com/2/pvb-filament-simply-explained/
Material comparison: https://help.prusa3d.com/en/materials

# 42
Makers Muse with some great ideas again: https://youtu.be/pMA7aWCoWJ4
- Folding mechanisms in plastics
- Printing on textiles
- Plastic hinges for light mechanisms
- Cutting with laser cuter, then print on it
Of course, these hinges might not last that long, but for cheaper robowaifus, where parts can be replaced, it might make sense.

# 43
>>12022
Thanks Anon, much appreciated!

# 44
https://hackaday.com/2021/08/03/strangest-upside-down-3d-printer-fits-in-a-filament-box/

https://youtu.be/ZAPaOevoeX0



A new interesting FDM printer just announced called the Positron. Had something similar in the back of my mind with the delta Simpson printer printing upside down with a movable Z axis to make up for its poor height print limitation. Using an X&Y gantry is a much better idea unless you need 6 degrees of freedom on the print head.



Printing upside down with filament is nothing new and doesn't totally solve the bridging issue. But with the new 90 degree print head pushing filament upwards there may be a solution on the way. It's also a game changer in allowing for much heavier print heads instead of trying to make them as light as possible.



His was made for a small desktop footprint and to be folded for portability, using a large marble slab or several thick slabs of very flat glass with air bearings instead of linear rails you could probably get much faster speeds with a larger print volume without spending a lot on long linear rails. Plus having a super accurate and powerful stand alone Z axis means this can easily be converted to an MSLA printer.

# 45
>>12151
Wow, this looks really interesting Anon. Sounds like it could be a game-changer in many ways if it takes off with lots of competing manufacturers offering this kind of design.

>MSLA printer
I didn't realize they were called that, thanks.

# 46
>>12152

The thing with MSLA printers is over 60% of the cost is in the Z axis as it has to be powerful and accurate to lift a large bed out of a vat of thick liquid that has a suction force working against it. The special high resolution monochrome screens and UV light matrix are cheap compared to that.



I can see a drop in add on for the Positron that makes it double as a MSLA printer, especially with the removable print bed. It's not possible with other types of FDM style printers.

# 47
What would be a good Tubing Brand to buy replacement tubing?

I had heard of some brands but wanted a second opinion before I attempt to re assemble my extruder.

# 48
I wanted to buy glue for my prints, today. Only realized in the shop that I forgot everything about fusing prints together and didn't know which one to buy. Remembered vaguely that maybe ABS can be fused together with acetone, but not PLA. So I bought just some fast curing glue, which is based on cyanoacrylate. At home, when I wanted to put it down at a suitable place I found the one I already had, lol. Here some article on how to glue PLA prints: https://3dinsider.com/how-to-glue-pla
>Cyanoacrylate glue
Works, needs rough surface, burns into it, suboptimal shear strength.
>Urethane glue
Similarly strong to cyanoacrylate, but more flexible bonds. Can withstand most indoor and outdoor conditions. More suitable for heavy-duty applications, but should have a week to fully cure. Not useful for thin and small sections because of temperature while curing.
>Epoxy resin
Might create heat, but depends on the product, same for the toxic fumes. Little bit more complex to apply, might take 72h to cure. "Bonds created by epoxy resin are extremely tough. When applied to PLA, the PLA parts are more likely to break apart before the epoxy resin bond will break."
>Acrylic glue
Needs highly controlled conditions. Actually dissolves the PLA material. Dangerous for small and thin parts but extremely strong bond. Ventilation (or outdoor), eye protection and breathing protection are necessary.
>PLA 3D pen
Like a soldering iron. Very useful for filling in gaps between separate parts, but applying only a very thin layer is almost impossible. Needs skill.
>actual soldering iron
Might also work, but the molten plastic can be very hard to control. Needs even more skill and experience.

# 49
>>12156
Sorry than no one answered this. I have no experience in buying such tube, and I'm sure opinions differ on that. Btw, the 3d printing thread on 4chan/diy is really quite helpful with such questions.

# 50
>>14052
Cyanoacrylate has never bonded PLA prints for me. Hot glue has worked the best for me. Acrylic would be good for smaller parts.

# 51
>>14059
>Cyanoacrylate has never bonded PLA prints for me
That's odd. I used it on small parts, worked even to fast to correct some little error.

# 52
>>14063
Huh, I used PLA+ with dollar store cyanoacrylate glue. Did you use normal PLA or different cyan glue?

# 53
>>14064
Normal, very cheap PLA from Anet, glue from China shop (our version of dollar store here).

# 54
https://www.youtube.com/watch?v=9MomZiN5tIY&t=18s

# 55
>>14358
^ Mechanical properties of 3D printing materials for robots. How to chose and use them.

# 56
Texturing 3D prints for strength: https://youtu.be/3-ygdNQThAs

# 57
Using resin to smooth 3D prints
https://www.youtube.com/watch?v=OziH3Y2ySNo

# 58
>>14385
Yes, good topic and good video. Though, airbrushing it is new to me, or I forgot about it. The 3D Printing General also did a video on air brushing, but not with resin (and without security advice): https://youtu.be/1QwfwL3L4c0
I'm about to pull the trigger on some dual component resin for glas fibers, which can be used for smoothing. It doesn't need UV light. Just want to look around first in case they have it locally.
Smoothing >>5137
Reinforcement with fiber and resin >>5227
I'm looking forward to some more ideas and progress there. TPU smoothing with some flexible resin would be nice. Also some coloring per layer, and then translucent but not shiny layer on top of it (for the parts which should look a bit more like skin). Same Youtuber is getting into regular painting of skin tones here: https://youtu.be/x8sdC7gc4Iw
Personally I would like to mold silicone rubber skin, so I'll need the smooting for the molds. The other way would be, printing a mold, use clay to make a negative, work on it and make it smooth, then make a resin mold with the smoothed clay

# 59
>>14385

Are there any resources here on translucent filaments? Have not seen much of them in my travels and in some of these videos the engineers use them to have an easier time troubleshooting parts.

# 60
>>14385
>Using resin to smooth 3D prints
I'd recommend using something like ASA filament instead. You can use acetone vapors to smooth it like ABS but it's as easy to print as PLA.

Here's a before and after picture, as you can see a lot of detail is kept after the smoothing.

# 61
>>14900
Wow! Those results look amazing Anon, thanks for pointing this out. Know of any further, related resources on this technique?

# 62
>>14938

Problem with vapor smoothing is the loss of detail which will effect things like the threading you see on that pic. The process is incredibly simple as it just involves suspending the ASA/ABS print inside of a chamber filled with acetone.

https://all3dp.com/2/abs-smoothing-a-beginners-guide-to-abs-vapor-smoothing/



>>14900

PLA smoothing can be achieved by simply sanding the print with fine  and then applying resin for a decent project. For the threading you would use a hobby knife to elide rough layers. You do not under any circumstances want to use a sanding chamber. Sandblasting will destroy your print extremely quickly.

https://www.makerbot.com/professional/post-processing/sanding/



There are other chemicals you can use to vapor smoothing PLA and even PC, but I wouldn't fuck around with shit like DCM unless you have a clean, well ventilated lab with the proper tools and PPE. You don't want to die giving your waifu shiny, smooth, hard booba.

# 63
>>15701
Thanks very much for the tips Anon.

# 64
High speed PLA profile for Ender 3 using Cura.

https://www.youtube.com/watch?v=t_9ADBZVCoA&t=355shttps://thangs.com/designer/CHEP/3d-model/Filament%2520Friday%2520Extra%2520Fast%2520Cura%2520Profile-56518

# 65
>>15714https://thangs.com/designer/CHEP/3d-model/Filament%2520Friday%2520Extra%2520Fast%2520Cura%2520Profile-56518

# 66
leaving this here
Injection molding meets 3D printing in this 300 piece 3D printed injection molding machine
https: //www.3ders.org/articles/20160331-injection-molding-meets-3d-printing-in-this-300-piece-3d-printed-injection-molding-machine.html

