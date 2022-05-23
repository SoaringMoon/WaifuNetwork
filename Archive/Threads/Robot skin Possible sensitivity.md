# 1
The Anki VECTOR has a skin-like touch sensor on it, could we incorporate it into our robogirls?

# 2
>>242
You can make a capacitive touch sensor pretty easily

Like if there's 2 conductive surfaces and when they move closer together or further apart the charge potential between them changes

# 3
Wish I had money to experiment with this stuff. It'd go well with silicone skin covering it, but how would we incorporate it into the hands and face? How flexible are piezoelectric film sensors?

hoshistar81.jp/skin/nonlinear/nonlinear.html
hoshistar81.jp/skin/cellbridge/cellbridge.html
hoshistar81.jp/skin/robotskin/robotskin.html

# 4
You can make a touch sensor using foil and a 1+ megaohm resistor.  If the skin is thin enough the capacitance can be detected even without touching the foil.

drive.google.com/file/d/0BzI1z5n4uz3GeFZMbEdwX1ZmT3M/view

I remember eons ago I even made one without a microcontroller, I don't remember the setup though, using a 555 timer.

# 5
However we have to do it, this is important at the very least for **sex with** our robowaifus, and is probably also very important for her when she's doing things like cleaning the dishes, cooking, or other mundane tasks that require both judgement in action, as well as sensitivity in manipulation. I imagine there are literally 1'001 activities where at least sensitive touchpads of various sizes and shapes, strategically placed around the robowaifu's body, will be of essence.

A way must be found to do this guys, effectively and cheaply. It needs to be mass-producible.

# 6
>>675
You could just have a sheet of silicone with various touch receptors all over it. Now, making pain receptors? That, I have no clue.

# 7
>>675
ANOTHER IDEA: we could just steal a harmony unit, skin it, and reverse engineer the technology they use to make the skin, so we can make something like Jenny the Robot with flexible skin in the right spots.

# 8
>>677
Dude, Harmony skin is just silicone, it's not rocket science, however it's a laborious process.

www.smooth-on.com/

Not to mention the material costs.  Sex dolls tend to be handmade, that's why you end up paying 500+ for 10 pounds of silicone.

# 9
>>673
>How flexible are piezoelectric film sensors?
pretty dang flexible, they're thin films.

# 10
>>672
>>674
This. Or dot her skin with diffuse infrared sensors which can not only help her navigate, but also measure your body heat and pulse.

# 11
>>675
So, I've noticed that a lot of the Uncanny Valley thing mainly stems from how most sex dolls lack any kind of facial muscles. They're mainly just rubber or silicone wrapped around a skeleton. The guy that made the Shinobu Simulator, managed to work-out some of the uncanny valley to the models by implementing "muscle groups," to the face of the character. Now, since we're working with something physical rather than something digital, why not give a robot artificial muscles for facial expressions? It would look a lot nicer and probably smoother in its movements.

Or, maybe if someone could recreate neurons, then you could hook up said neurons to both the skeleton and the muscles for a robot. Then you have them end inside the artificial skin. Make sure some of the ends are sensors with a feed-back to the computer and there you go. A Robot that can feel things. Bonus points if you can have internal heat that is generated to vent through the skin and muscles. The ONLY thing I would find hard to replicate would be those fake neurons. Unless, someone made a vat-grown clone-thing?
**Sorry for the rant, its just my two cents on everything** **Yes, its all easier said than done**

# 12
>>864
Yes, facial animation is a big challenge to overcome the Uncanny Valley and make our robowaifus charming anon--even if they are intentionally designed to be less realistic looking (especially in the beginning years of production).

>The guy that made the Shinobu Simulator, managed to work-out some of the uncanny valley to the models by implementing "muscle groups," to the face of the character.
Using 'Blendshapes' or 'Morph targets' is a commonplace approach to facial animation. IIRC the VivaDev guy said he is a professional in the industry doing it as a side hobby.

>why not give a robot artificial muscles for facial expressions?
Cost. One of the reasons for having robotic-looking robowaifus in the beginning is ease of engineering and cost reduction.

Your notion about artificial neurons is indeed quite far-fetched atm, imo. Ofc, we plan to simulate these functions using regular wiring and more commonplace engeneering sensors.

>Bonus points if you can have internal heat that is generated to vent through the skin and muscles.
Trust me, we'll have all the 'bonus' points we can handle. Dissipating heat effectively will be a major Systems Engineering challenge to begin with anon.
>>234 

No apologies, thanks for the input anon. Yes, it's easier said than done, but ''someone'' has to say it all, right? :^)

>also
sauce on the stretchy light thing?

# 13
>>865

zmescience.com/research/technology/stretchable-artificial-skin-423/

# 14
>>925
thanks mate, bookmarked.

# 15
>tfw robowaifus will have full-haptic sensing vaginas with precision women don't even have
https://www.youtube.com/watch?v=LWC3if29T-I
The future cannot come soon enough

# 16
>>1623
That's pretty exciting anon. Looks like robowaifu skin may eventually exceed even my hopes for it.

# 17
This is bit of a strange project but it has an interesting idea of using light to detect deformations in silicone gel skin to get tactile feedback.
https://bair.berkeley.edu/blog/2020/05/14/omnitact/
https://arxiv.org/pdf/2003.06965.pdf

# 18
>>3648
That is interesting Anon. At least ''one'' of my robowaifus I want to be able to glow-in-the-dark **'''NO NOT A CIANIGGER HAHA'''** and having glowy fingertips would be breddy cool tbh. What kind of hardward costs do you think we could get something like this down to?

# 19
>>3649
About $15 for two 640x480 cameras and the LEDs.

# 20
>>3655
Hmm, about $300 for just the fingers and toes? Pretty expensive. I guess that will have to wait for better models. :^)

# 21
>>3656
Sensors will be one very important factor which will make a difference in price. This is unavoidable, let alone for the extra work. All these signals will also need to be handled by microcontrollers and then by the AI. I personally will go for the expensive model, but build it on my own. Even if they will cost 10-15k it's still worth it.

# 22
>>4284
Yes, that's one of the great things about '''DIY''' Robot Wives. Individual garage labs can do prototyping (which is always more expensive than production after tooling costs regardless) without rigid regard for pressures like schedules and budgets. It can become a work of love.

>Even if they will cost 10-15k it's still worth it.
**Actually, high-end robowaifus will probably cost about as much as high-end cars do. We can probably help that a bit, but you can bet Teslawaifu, Googlewaifu, Facebookwaifu, et al, will squeeze it for all they can get away with.**

# 23
I was going to mention this in the Robot Vision General thread, but I figure I'd resurrect this thread instead. I remembered seeing that someone made a proof-of-concept camera out of solar cells, but I can't find it anymore. It was greyscale, very low resolution and probably had a lousy refresh rate, but it was a functioning digital camera. I loved this idea because if it's improved enough you've got a digital camera that generates power instead of consuming it.

Then I remembered this post: >>3648 where light is used to detect deformation in skin for touch sensing. I had no interest in flexible solar panels before, but what if there were a flexible solar panel acting as a camera beneath a layer of skin to create a sense of touch? When it's not being touched or covered, the body is passively absorbing light and trickle-charging the battery. The LEDs could be visible if you really want, or they could be infrared (panels with good infrared sensitivity are better in winter) and give the body a similar thermal image to a real human body and be warm to the touch. And some self-warming holes when you feel her from the inside. ;)

# 24
>>13235
I've often thought about the notion that at the very least we should add trickle-charging to various parts of our robowaifu's outer shell designs. Can't really think through some of the issues. But, I would be off-topic here since it's a Power issue. Your pic made me think of it. Sauce on that BTW?

# 25
>>13240
>But, I would be off-topic here since it's a Power issue.
I didn't really mean for it to be about power as much as about trying to create a passive-energy sense of touch using flexible materials.

>Your pic made me think of it. Sauce on that BTW?
I just did an image search for flexible solar panels, but it's: https://www.ecowatch.com/best-flexible-solar-panels-2654431234.html

# 26
>>13280
Thanks Anon.

