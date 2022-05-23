# 1
Robowaifus will need power to run, and since they will be mobile this means a mobile power system too. ITT post info on batteries and other mobility capable power systems.

# 2
This university research project aims to make recharging your power system as quick as refilling a tank of special electrolytes. While it's aimed at the automotive industry, maybe it will have importance to the robowaifu industry as well.

https://www.invidio.us/watch?v=yNZkbt928oA

# 3
>>786
While being an overall cool advancement, I don't think robowaifu's will really need fast charging capabilities. After all what else would she be doing while "asleep"

# 4
>>787
In the sixth ''Chobits'' episode, 'Chii Weakens' charging you're robowaifu (ie, getting Chii's master Hideki to learn that he even needs to) is the topic, and when the landlady (secretly Chii's mom) finally begins charging her up for Hideki, the implication is that she's charging up super fast. But then again, she's a super robowaifu, so maybe that's expected.

As to 'what else would she be doing' [at night], I may hear the sound of /clang/ing off in the distance heh. Sometimes she just might need a quick recharge tbh.

# 5
How about a bio-reactor that used microbes to generate energy? Bonus: you could have dinner with your waifu.

# 6
>>790
That's an interesting idea anon. Have any info links?

>Bonus: you could have dinner with your waifu.
Leld. 
>inb4 robowaifu farting ala the Bicentennial Man scene

# 7
Samsung claims this tech will charge 5x faster, and store 45% more energy per volume.
>In theory, a battery based on the “graphene ball” material requires only 12 minutes to fully charge. Additionally, the battery can maintain a highly stable 60 degree Celsius temperature, with stable battery temperatures particularly key for electric vehicles.

news.samsung.com/global/samsung-develops-battery-material-with-5x-faster-charging-speed

# 8
Hey guys, I've taken the plunge into learning how to use 18650 lithium ion batteries, they are world standard 3.7V rechargeable batteries used in cellphones and Teslas (which use thousands of them).  I arrived at this decision since a casual browse of online shopping sites revealed more hits of 18650 battery holders and charge protection circuits than C battery cells, which I was going to originally use. C sized nickel cadmium batteries in particular are hard to find.

I also discovered the ESP32 is a 3.3V chip and can be powered by a single 18650 (in fact there's a version that comes with a battery holder and OLED built in), and two 18650 in series can provide sufficient voltage to the regulator powering the other type of Arduino boards.

Note that these batteries are particular and will be damaged if overcharged or undercharged, hence the necessary (but dirt cheap) protection circuits, picture is a one-cell 1A USB-powered one and a two-celled one that I'll have to somehow hook up to a 9V charger with enough amperage.  In the meantime I can charge each individually via USB and I'll put a hardware battery level indicator in my waifubot.

# 9
>>793
Forgot to mention the newer version of the TP4056 03962A has OUT + - which you can connect to a load already, since not only does it have overcharge protection (i.e. the older versions) but also undercharge protection.

# 10
>>793
>>794
>I also discovered the ESP32 is a 3.3V chip and can be powered by a single 18650
I was just looking into this too recently. While possible, like you say, it seems most people recommend going up to 2S to get 7.4~6V over the discharge cycle, then using a 90+ efficiency switching regulator to bring it down to the 3.3V you need, plus another for 5V or 6V for motors or whatnot.  The problem with a 1S direct connection isn't so much the low end of the cycle apparently, the 2.6~3.0V or whatever your particular board cuts off at, but rather the top end, 4.2~3.7V when charging/fully charged. Toasty.

Glad to finally see some non-theoretical battery discussion too, I'm working on my own battery pack and charging setup right now. Want to get the waifu hardware organized and off of my prototyping/research desk. Thinking either 2S2P or 2S3P. Pic related. Basically the same as yours. Same deal with the charger, I've got a 9V 1.3A charger here that's hopefully up the task. The product description says it wants 8.4V but I can regulate down to that.
links:

www.banggood.com/2S-7_4V-8A-Peak-Current-15A-18650-Lithium-Battery-Protection-Board-With-Over-Charge-Protection-p-1259709.html?

www.instructables.com/id/DIY-Professional-18650-Battery-Pack/

# 11
So it looks like it will be 2SxP for sure for me then. Turns out the Orange Pi Zero cannot be powered with a regulated 3.3V supply via the 3.3V pins. Apparently those only exist to supply 100mA or so to peripheral sensors and whatnot. So now I've got the amusing situation of the 3.3V Pi and a 3.3V Arduino pro mini clone being powered with 5V (through the RAW pin on the mini). The 2 red FTDI boards have the 3.3V jumper in place too. Now I just got to get everything on a board with double sided tape or something, and the wires routed so I don't fry something with a loose 5V lead.

# 12
>>791

en.m.wikipedia.org/wiki/Biobattery

en.m.wikipedia.org/wiki/Microbial_fuel_cell

# 13
I see your standard lithium batteries being chosen, very practical. We also see some theoretical discussion, very interesting. Fuel cells may be worth looking into if you want an option that doesn't require plugging in your partner. I wonder what options will be most cost efficient, but certainly your partner if using lithium batteries can't be more costly to charge than an electric car. There is the matter of energy density however. Will there be room within your partner for sufficient energy packs to run them for a day? You may also want to make your system hot-swappable in case she starts running low on energy during a late evening out. 

It may be worth it to study the power systems used for artificial hearts.

# 14
>>798
My first response for technical problems like this has always been, "how did biology solve it?" 
In this case, it kind of didn't. Sleep isn't a charging cycle, as much as it is a cleaning time. Spend the less-productive night hours squirreled away, healing your body and indexing the day's memories and such. What people actually do to get their energy is eat and digest, and humans only store enough energy for about three days of actually doing things. When someone eats, they are getting all the energy from the storage of whatever they are eating. That's why you eat your own body weight in food in about a month, but it's split into a pound or two three times a day: the thing you're eating also didn't solve the energy storage problem, and you use energy almost as fast as you get it if you're an active person. It's like that all the way down to the plant level, when they use the sun's energy to turn ground-minerals into chemicals they can use.
Considering that billions of years of evolution managed to get energy storage for three days of activity, the best option probably is to have some form of on-site power generator and a steady supply of fuel, as it is much easier to generate power than store it. The reliance on fossil fuels is because they have something like 40 times the energy per kilogram of current batteries. Those biobatteries that >>797 mentioned show great potential if they can be miniaturized to fit inside of a torso.

As for artificial hearts, those work via "inductive coupling" - basically, if you have two conductors set up right, you can wirelessly transfer energy short distances, as in, a few feet at most. The transmission speed decreases very drastically with range. The heart is connected to one of the conductor (along with a rechargeable battery), while outside of the body is a much bigger battery connected to the other conductor. The rechargeable battery inside has only about half an hour of charge, almost all energy goes nonstop from the external battery to the heart. Inductive coupling can be used to transfer energy without breaking the skin, but doesn't have the flexibility to be much better than regular charging in terms of range, and takes up a lot more space, since a bigger conductor means faster power transfer at a much less efficient trade than bigger charging cables.

# 15
>>799
Any refinement possible on your '3-day energy storage based on evolution' model to account for motivated humans being able to go 40 days w/o food?

>inductive coupling
what if we made a wireless-charging futon for our robowaifus to sleep on overnights?

# 16
>>799
Could use some variety of flow battery if we're looking for in ingestion based model. Your waifu would require input of material in order to keep running however adding this new material would be quick and depending on volume could be rather convenient. As well I find the idea of my waifu having to "eat/drink" in a fashion like a live person to be appealing in some manner.

# 17
>>801
>As well I find the idea of my waifu having to "eat/drink" in a fashion like a live person to be appealing in some manner.
There's a social appeal to eating together with friends and loved ones anon. Watch the scene with K and Joi in ''Bladerunner 2049'' and imagine instead that she was eating holographic food along with him. It becomes more charming to my thinking.

# 18
Here a long article about types of batteries: https://batteryuniversity.com/learn/article/types_of_lithium_ion
Website itself is worth bookmarking: https://batteryuniversity.com/

Some video about some of the types (incomplete): https://youtu.be/LqgP16JQ24I 
Lithium-Ceramic: https://youtu.be/kJXRyWQgOY4
BMS diy: https://youtu.be/rT-1gvkFj60
LTO safety: https://youtu.be/XsrRDZxEFQE

# 19
>>4391
Excellent. Also, I appreciate the fact you took the time to post in the correct thread. Finding anything after the fact (especially weeks/months later) in off-topic threads can be like the proverbial needle in a haystack. Now, I can find this info from the catalog any day I please.

# 20
>related xpost
>>4385
>>4386

# 21
>related crossposts (>>10664, >>10666)

# 22
>related xpost (>>10663)

# 23
>related xpost (>>10729)

# 24
Hydrogen is promoted by some Anons but it's worse than good batteries in terms of conversion efficiency, and much worse in terms of convenience and expense (at least in the scale of a single robowaifu's on-board power systems).

But if you're interested in it, here's an interesting post on the topic.
https://www.forbes.com/sites/quora/2018/05/08/what-are-the-pros-and-cons-of-using-hydrogen-to-generate-electricity/

# 25
I've been developing and building a direct ethanol/methanol fuel cell. Not specifically for this application, but it would work good I think.

# 26
>>14265
Cool. From the scratch or with some kit? If it's your own design, will you publish it on some website or will you make it into a product? How is the patent situation actually? These girls a few years ago got threatended with legal action if they try to make a product out of theirs. 
Just looked into it for a moment, some of such fuel cells are available for sale. Nice, good to know, but if at all then I'll need it in maybe two or three years or so. If anything, this will be some additional gimmick to a high-end luxury robowaifu, since these current commercial development kits seem to cost 1800$ while providing 400mW at less than a volt, lol. https://www.fuelcellstore.com/dmfc-flex-stak

# 27
>>14267
Okay, but this looks much more promising: https://youtu.be/s4T3Oj9w0dk - 50W, 12-24V, needs a bit more than a liter fuel per hour. It's still too big, but not that much to make me loose hope.
This guy here also made a small direct ethanol fuel cell. His video is in Italian, but he comments in English as well and seems to know about different options how to get there. He has more explainer videos up. 
Personally, I just hope for some product in form of a kit. As I wrote above, I'll only need that in two years or so.

# 28
I don't know much about fuel cells and I'm not going to pretend that I do, but I realized that one idea I've been thinking about might produce oxygen and hydrogen mixed together with other potentially flammable gases. Rather than flaming-burps or trying to fit a small gas engine in there, is there a way I could use it with a fuel cell, or is burning it my only option?

# 29
>>14273
Your idea and question is rather vague. What other gases? Just look up what kinds of fuel cells exist. However, don't try to do everything differently. Don't try to reinvent the wheel. We are only a few guys here. We don't need to invent everything which we might use, let others do that, for other use cases. We only need to find out about it, and then adjust it to our use case if necessary. 
Batteries will be fine for many use cases. Lightweight waifus won't need much energy. Wheels reduce the amount of power needed to move around. External vehicles are another solution. Heavier waifus might be plugged in, after moving from one place to another. This heavier model will most likely have water and alcohol inside for heat distribution and cleaning, this is why a direct ethanol fuel cell might make sense.

# 30
>>14273


Anything that has an emission will damage you or your robowaifu.

Ethanol fuel emissions are still poisonous unlike what the retards from earlier claim. They are essentially telling anons that they should let their car engine run while in their living space.

# 31
>>14279
>Ethanol fuel emissions are still poisonous
There are not gaseous emissions with a direct ethanol fuel cell. The water involved becomes more acidic, if I recall it correctly. So, it's not like a car engine.
>>14296
Fascinating. My uncalled advice is, to find something more helpful to work on. It seems to be complex, messy and inefficient.

# 32
>>14296
>>14301
Lol. I (quite appropriately, I might add) will be moving your posts into shitposting-central soon. The topic of human (or other biological) digestion systems is certainly an issue to be addressed by the men thinking about this topic, and contributing into our biological thread. Certainly, there are many complex topics that necessarily come up when one decides to ''intentionally'' introduce biology into a robowaifu system.

And the general topic of management of microbiological **infestations** presence on/within our robowaifus is something serious that needs to be addressed by very smart men here as well. Obviously her master's sanitation will be an issue for a robowaifu, and perhaps you'd be able to contribute to the protocols involved with reigning-in issues there?

But, plainly, these posts indicates you'll be far more comfortable discussing this topic generally & specifically from within the warm, comforting environs of our mini-/b/, well-suited to this topic in general. Maybe from there you can explain effectively for us all what the directors who created these humorous mangos/animus that involve the purely-non-living robowaifus drinking/eating were thinking? :^)

# 33
>>14302
The only reason I even brought it up was because of >>14277 asking what other gases would be involved because I was curious about burning gases for power. I already mentioned the electrolysis creating hydrogen and oxygen, regular humid air, hydrogen chloride, carbon monoxide, and presumably methane. I explained the process I was thinking about because genuinely don't know what other gases might be produced.

If I did go through with this, I have some ideas of burning the gas to produce heat, and converting the heat into power. (another reason for the circulatory system) If there's any ideas for a more direct method of getting power, I'd like to hear it.

# 34
>>14304
yes, the infamous holzgas generator 
this was popular in vehicles back in the 40s due to war rationing 
you can find it mentioned in the nuremburg trials as this was (((their))) official story for decades before they abandoned that story and went with the insecticide zyklon b after people forgot what delousing was

# 35
>>14305
Or just a regular modern catalytic converter. I already assumed that the guy who wanted to make an ethanol fuel cell was also going to use a catalyst to deal with the carbon monoxide and other fumes, so I didn't think what I was saying was that weird.

# 36
>>14304
Heh, I'm simply joking about the topic itself--as portrayed by your posts. Very /b/-tropic.
>If there's any ideas for a more direct method of getting power, I'd like to hear it.
I would suggest that not only are electro-mechanical systems based on electrical motors significantly more efficient at delivering Watts directly where they are needed, but direct cabling for electricity straight into the robowaifu is a ''pretty direct'' method of getting direct current directly into the system.

This form of directly getting power into a robot is still fairly commonplace in robo-prototyping labs. Our direct goal ofc, is to directly place direct-current batteries directly near our direct-current electrical motors, afaict.
**:^)**

# 37
>>14302
This whole recent discussion seem to be based on BS. This questionable claim >>14265 starting it, was never fleshed out. - That's already suspicious - Then this seems to be trolling by acting to be stupid or new: >>14273 and >>14279 - And here >>14305 we're back to the Nazis. 
I made the more productive postings here, and still wouldn't care if the whole discussion would get moved over into the Basement. The biology thread doesn't deserve this nonsense. Discussion on digestion as an option would be fine, but it's a very awkward and special way to go, unless you want to live in a dark rainforest and having your waifu eating plants and animals. Based on that, discusions on that topic should imo generally getting cut down to the more serious appearing postings.

# 38
>>14307
I already made the only contribution I have to make on the subject of energy storage here >>5080 and I'm not sure if I mentioned it elsewhere, but I once saw a low-resolution concept digital camera that used solar cells.

As far as long-term power storage goes, you can't really get much better than generic lead-acid when they're used right.

# 39
>>791

This is going to be hilarious in application but it is entirely possible to turn used vegetable oil, rapeseed oil and canola oil into diesel fuel. I'm not sure how that'd work outside of a combustion engine but if we're talking about fuel from food that's the closest I can think of next to giving them a natural "septic tank" style stomach that comes complete with a micro biome and some sort of way to extract the energy out of it like a real stomach.

# 40
>>14320
>it is entirely possible to turn used vegetable oil, rapeseed oil and canola oil into diesel fuel
Those things are also flammable entirely on their own, we typically don't use them as fuel because they're not as energy dense. I think it makes more sense to try to use them as they are to produce energy than to take up more space with a microbrewery to convert them to another fuel.

# 41
>>14320
>Plant oil
>some sort of way to extract the energy out of it
Please just stop. There's nothing to improve or resolve here. Otherwise, buy some lab equipment on Ebay and go to work, or at least provide some idea how this is going to work and a reason why it is better than the existing alternatives

