# 1
Hello Anons, wanted to share some info and perhaps make you think about what you should compute with.

==x86/amd64==
-Proprietary ISA (Instruction Set Architecture)
This means to get enough low-level detail requires signing non disclosure agreements (NDA).
Even then, they might not disclose all the available commands (see Breaking x86 video below).
If you cannot trust what the processor is doing, then no open-source software will make it any more trustworthy.

-Complexity
Common instruction sets come with hundreds (over a 1000 for x86) instructions.
Breaking x86 instruction set
https://www.hooktube.com/watch?v=KrksBdWcZgQ
Hardware backdoor x86 (not for all processor models)
https://www.hooktube.com/watch?v=_eSAF_qT_FY
The more complex the system, the more bugs (in hardware and software).
Intel had plenty of bugs that were discovered post release, for example the Pentium floating point division: https://en.wikipedia.org/wiki/Pentium_FDIV_bug).
Interestingly, the x86 assembly instructions are actually decoded to a sequence of RISC instructions to be used by the internal cores of the CPU.
https://stackoverflow.com/questions/5806589/why-does-intel-hide-internal-risc-core-in-their-processors

-Security/Backdoors
Intel has its Management Engine, which provides full access to CPU, RAM(?), control via network.
Advertised for sysadmins, but present on consumer hardware.
https://www.hooktube.com/watch?v=3CQUNd3oKBM
Intel ME Cleaner - Tool for disabling and pruning  Intel ME from BIOS/UEFI firmware.
https://github.com/corna/me_cleaner
AMD Platform Security Processor (PSP)
Similar to Intel ME, based on an ARM core.
Video below shows how bios can be analysed.
Looks to be somewhat tamer compared to Intel ME, however this may have changed.
Dissecting AMD PSP:
https://www.hooktube.com/watch?v=IW2YsxSj6zE

Speaking to an experienced programmer, he told me the main reason why x86 is the main desktop/PC architecture, is that it allows compiling C almost directly to assembly. This is not the case as for ARM ISAs or RISC V.
I guess from a certain perspective, if you had an architecture with enough instructions to better support C (such as array operations) then it might have a chance at competing with x86.

==ARM==
Proprietary ISA, several versions available, current is v8.
There are licensing fees for use in custom ASICs, don't know how much the documentation covers the internals.
The are many Single Board Computers (SBC) using an ARM-based.
They are probably a better option compared to an x86 system security wise, however the underlying arch is still unknown.

==RISC V==
Reduced Instruction Set Computing V
I was once an excited ''consoomer'' for RISC V, until I heard about a libre project designing a system-on-chip (SoC) that struggled to get the necessary amendments to the standard (for graphics) put through. Here's a snippet from the project lead:
>if you were not associated directly with UC Berkeley, you were basically not welcome. Caveat: if you signed the NDA-like agreement which conflicts directly with, for example, the Debian Charter and the whole purpose of libre licenses, then you got a "voice" and you got access to the closed and secretive RISC-V resources and mailing lists.
https://www.crowdsupply.com/libre-risc-v/m-class/updates/nlnet-grants-approved-power-isa-under-consideration

This was my "red pill" if you will, that like the development Linux kernel, it's predominantly focused on working towards the interests of corporations as opposed to smaller developer groups.
The ISA itself is available to study ( https://riscv.org/specifications/ ) and the main issue technically speaking is that the base instructions aren't long enough to deal with, say a 64 bit address/number directly, thus requiring extensions. The ISA has had quite a few extensions since its inception.

==Alternatives==
-POWER ISA originally designed by IBM. Later open-sourced. 
https://openpowerfoundation.org/?resource_lib=power-isa-version-3-0
One implementation is by Raptor, using Power9 ISA. Comparable to x86 desktops, very expensive.
https://www.raptorcs.com/

-Older architectures which have been reverse engineered, or materials eventually released.
Such ISAs can be implemented inside a Field Programmable Gate Array (FPGA) for systems designed to give the user more control.
Here's a project based on the commodore '''65''' in an FPGA, project called MEGA65
https://github.com/MEGA65
https://www.hooktube.com/watch?v=KuNB4ocZDXA
The points by the chap are pretty good, and one of the main takeaways is:

'''Separate''' your computing environments.

Your most important, trusted code runs on a small, fully verified CPU.
While any application that requires high performance or proprietary CPU/system, runs independently without access to the trusted system
For example if you were to design a secure phone, the main system could run on a trusted FPGA core (''if you trust the FPGA of course''), and when service is required, the trusted core controls whether the cellular modem is enabled.
Unfortunately, greater integration leads to high chance of security breaches and botnets, so more modular design is necessary for security.

-Libre-SoC, a system-on-chip currently in development.
Supposedly will be the first open SoC with open source graphics.
Graphics seem to be the main issue in preventing fully libre computing hardware.
What I mean is dedicated graphics, not software rendering.
https://libre-soc.org/

==Ultra RISC / OISC?==
One Instruction Set Computing 
It may seem crazy, but there are individual CPU instructions that are Turing-complete, and hence an architecture built around this instruction can execute any finite problem (with enough RAM and time).
One example is the MOV instruction, which can move data between memory and CPU registers.
A C compiler for x86 has been written to compile your code down to just MOV instructions.
https://github.com/xoreaxeaxeax/movfuscator
The MOV-only on x86 is more of a toy than practical, however there's potential to making a simple processing core in hardware, and by having many of these cores (8+) in a multi-processor system one could achieve better performance.

One of the architectures I'm working on is the Subtract and Jump If Less Than Or Equal To Zero (SUBLEQ), as it is also Turing-complete and someone has already written an OS for it here:
http://gerigeri.uw.hu/DawnOS/index.html
The plan is to make small scale version of the CPU before going for full Dawn OS compliance (256MiB is A LOT of memory for an FPGA dev board XD)
That's about as much as I'll say for now, as I would like to spend more time developing. Don't expect it to replace your PC, however as an embedded system it'll have a shot.


==What do I use?==
Both my desktop and laptop have Intel processors, one Sandybridge, the other Nehalem. Have not disabled the ME, however planning to give it a test when I have more time.
I use Arch and Debian (better compatibility with tools like yosys), but I intend to move Systemd-less system, potentially Gentoo, OpenBSD or FreeBSD.
I tried Artix, however I couldn't get some things working, and their wiki isn't nearly as detailed.
So if I want to learn about another init system, I may as well start from an OS that comes with it out of the box.

==What are your options?==
-Use either intel or AMD, but '''CHECK'' if there's support for disabling the ME or PSP. ME cleaner even works on fairly recent generations of hardware: https://github.com/corna/me_cleaner/wiki/me_cleaner-status
-Use older CPUs. CPU before ME/PSP (or earlier versions where it can be disabled) is probably the easiest.
-Use a lightweight OS. Most POSIX compliant OSs can be configured to be lightweight and hence make using older hardware realistic. The most demanding uses are compilation of programs and video playback, so those will be harder to do.
-Limit network connectivity on machines that you're concerned about. If it can't call back home then it can't leak your data eh? XD (Hehe, there are other ways for hackers to do it... Air Hopper: https://www.hooktube.com/watch?v=2OzTWiGl1rM)
-Aim to use libre hardware, as it gives you more control over hardware. Example: https://github.com/OLIMEX

Thanks for reading Anons.
(Just to let you know I'm definitely '''NOT''' an expert on CPU arch's, I just want a system that's not a botnet XD)

# 2
Great OP. Look forward to seeing this thread develop over time. Thanks Anon.

> I just want a system that's not a botnet XD
So do we all. I don't see that ''any'' commercial processor affords us the security we require. Even if we manage to successfully firewall our robowaifu sufficiently to **(probably)** ensure ''privacy'', it's of little use if some backdoor killswitch or 0-day can be used against them. We  need truly open & peer-reviewed hardware. So do many other industries ofc, but our needs seem particularly acute, at least up there with the medical devices field.

# 3
>No Elbrus
>No Baikal
lame tbh

# 4
>>4512
Hardly helpful. Care to expand your point here, friend?

# 5
>>4514
Yes comrade I shall extrapolate my point in bullet points. 
1) domestical producion
3) not owned by wectern company
4. it can run doom 3 at reasonable FPS
7] free of U.S. influence
that was my exlaining of as to why russian cpu;s are a very good to use instead of AM,D and Intel both which  are not real cpus as they limit severaly the freedom of using the desktop to its full potential as they both own vastly superior technology (but not to russian new instructions sets) which are not sold to customer in fear of retalation.
extrapolate your option.

# 6
>>4512
>>4515
Эльбрус (Elbrus) is a an x86 compatible processor family (though it also has its own ISA). These processors are designed in Russia and used by the internal services there. Never had my hands on one, and certainly for a wide dissemination, not the best choice :P
Large die, likely produced in small batches, so expensive.

# 7
>>4515
Kek. Fine then, komrade. Try to remember we're an engineering board, not /b/. We need details here, lots of details. :^)

>>4516
Yeah, I kind of expected that. What our goal is ultimately is cheaply-producible kits & kit accessories, that Anons the world over can source in their home locations. Anything with restricted access is a no-starter in general.

Since this needs to be brought up I'll go ahead and ask it:
==Which is riskier to Anon's robowaiufus;==
'''Murrican botnet'''
>or
'''Bugmen botnet'''
?
Seems to me these are the most likely sources of compute resources for Anons the world over.

That is, which in /robowaifu/'s opinions poses the greatest risk of our beloved robowaifus being murdered remotely via backdoored, remotable kill-switches built into the dies?

# 8
>>4520
Both, so any chip produced by any company may have been tampered with.
A way of reducing risk of "bot-ing" can be to isolate complex systems, and have them be controlled by simpler systems. Perhaps not as crazy as making a processor entirely out of discrete logic gates, but perhaps a processor so simple, there's not much you could botnet into it.
Of course we need to '''define what a botnet is''', because for a RAM chip, could you have a botnet? If it only talks to the cpu, then perhaps the most damage someone could do is force it reset/wipe at an unexpected moment?

# 9
>>4521
Hmm, good questions. I guess I should start by saying I'm less concerned about recoverable attacks (ie, wiping the RAM or storage), as those can be restored. My chief concern is intentional bricking of the components via remote kill-switch capability.

And yes, that's a good scheme to use simpler chips as it's obviously going to be easier for feds (of either country) to coerce manufacturers to slip in insidious systems onto the chips w/o general detection the more complex the device is.

>'''define what a botnet is'''
==I know it when I see it...== ;)
I think most of us basically mean the notion that the globohomo industrial-state utilizing or incorporating systems for surveillance and control into other systems. Think George Orwell's ''1984'' for a milder example of the idea.

What do other anons here think it means? **We're sort of inventing this as we go along r/n heh.**

# 10
>>4523
System-on-Chip containing external interfaces such as:
-LAN Ethernet 802.3
-WLAN 802.11 (all variants)
-BT, Wireless PANs (802.15...)
-Serial interfaces (need some other way to transfer data via internet)
could be prime targets for botnetting.

Any SoC will likely have a common bus, thus enabling memory access from any internal block (however you '''MUST''' be able to bypass memory protection which is usually present on these kinds of chips).

By avoiding "jack-of-all-trades" chips (but sacrificing cost, area, power) you are less likely to be botnetted. Certainly avoid chips with integrated network interfaces, and perhaps use dedicated network chips, which could be powered down separately.

Another thing I just thought of; say you have an I2C sensor that in the datasheet might have 130 registers you could write to for configuration (it's a big sensor XD). If we were to assume minimum number of bits were used to address these registers, then 8 bits would be needed. 8 bits would give 256 possible addresses, and so the manufacturer could throw in some extra internal/debug configuration registers.
When you write a driver for the master that will control such a sensor, you should ensure your program never tries to access unmentioned locations to prevent accidental triggering of hidden features.

A little contrived example, but hopefully gets the gist across, putting in an undocumented feature isn't hard.

# 11
>>4529
Good points I'm sure. Mind just making simple recommendations for those of us who ''aren't'' EEs Anon? From my own limited perspective, you just eliminated 100% of possibilities for me. Obviously that's an untenable situation.

The C PL is notorious for having a propensity for security holes, and unfortunately most software for small devices is written in exactly this worst security-language of all. :/

# 12
>>4531
Let's see...
For projects where need small amount of processing (such as motor control, keypad detection, driving small displays etc.), go for a microcontroller without wireless connectivity. If your project requires internet access, really think about whether you actually need it. For any internet project you should consider your routers settings (whether traffic from any unused ports is allowed) and block as much as possible. 
Unfortunately I've only really used AVR (arduino) and a few ARM Cortex M0 based micros (STM32F0, mbed).
I'm just starting to get to the point of understanding how C PL works, so I'm much more positive towards it. There are controllers that support micro python if you are interested in trying a higher level language.

For something a bit beefier, I've used a Raspberry Pi (RPi 3) and RPi Zero. The zero you could buy without wifi, and so use it as an air-gapped system. Raspberry Pi foundation releases schematics for their boards, but if you're buying new, some of Olimex's boards might be more interesting. If you have the option to buy an SBC without wifi, but then plug in a usb dongle, that will be a little bit more secure. In terms of embedded computing you're stuck with ARM...though there is SiFive and their RISC V based boards. FPGA dev boards (like TinyFPGA BX) are a good option if you want to try an architecture other than ARM. Some boards are even supported by Arduino IDE.

Because I still have a whole bunch of boards and chips since my blue pill uni days, I'll be using those. However if I get new micros, trying a different architecture like the Z80 might be useful for experience.

# 13
>>4533
Alright thanks for the advice Anon. I hope these alternatives to commodity SBCs become much cheaper in the near future.

# 14
>>4506
>Speaking to an experienced programmer, he told me the main reason why x86 is the main desktop/PC architecture, is that it allows compiling C almost directly to assembly. This is not the case as for ARM ISAs or RISC V.
Bullshit. I mean, this might have been true in 1980s or something, but these days C compilers are very complicated and advanced shit, they can solve the issue of having a different instruction set. All android and iphones are running fine on ARM. Amazon and a few other companies have ARM servers. It looks like apple is going to sell ARM desktops for real now.
The problem is compatibility. If you have a program compiled to x86, it won't run on ARM. You need to recompile (and maybe change a few things, depending on how much low-level mockery is in it) your programs to ARM. In open source world it's not a big deal, raspberry pi and the likes are doing fine, but on windows, where 99% of the software is closed source propertiary garbage? It's not going to happen. And it's not going to help that m$ did everything they could to lock down the ARM version of windows as much as possible (do they still exists btw?).
An alternative is going the apple way, and provide a built-in x86 emulator to run non-ported software on ARM, but of course it'll lower your performance, and other than apple nobody bothered to really create a high performace x86 emulator on ARM (qemu is a joke, m$ didn't even try).

Also an example from plan9:
http://catb.org/~esr/writings/taoup/html/plan9.html
>it looks like Plan 9 failed simply because it fell short of being a compelling enough improvement on Unix to displace its ancestor. Compared to Plan 9, Unix creaks and clanks and has obvious rust spots, but it gets the job done well enough to hold its position.
The same is true with x86 and arm, If it works and already exists, have working software for everything, people won't ditch it for something marginally better, just to start over from the beginning again. Either intel/amd would need to do some huge fuckup or ARM do some miracle.
But now that nvidia purchased ARM, it's dead anyway.

# 15
Negating the press-release-pandering, what is the most likely outcome of the takeover?

nvidianews.nvidia.com/news/nvidia-to-acquire-arm-for-40-billion-creating-worlds-premier-computing-company-for-the-age-of-ai
https://web.archive.org/web/20200913233530/nvidianews.nvidia.com/news/nvidia-to-acquire-arm-for-40-billion-creating-worlds-premier-computing-company-for-the-age-of-ai

-What would be the best possible outcome for /robowaifu/ in this situation? 
-What alternatives will we have if Nvidia locks down all new systems in future to not function w/o supplying your GlobohomoNetID? 
-Will they be able to sabotage older ARM machines or will they be limited to just their new designs?

# 16
>>6454
>What would be the best possible outcome for /robowaifu/ in this situation?
Knowing nvidia, probably nothing good. They will likely won't kill it like 3dfx/voodoo, because they don't have their own cpu, but expect as much fuckery as possible from them. Like they already cripple double calculation performance in "consumer" GPUs.
>What alternatives will we have if Nvidia locks down all new systems in future to not function w/o supplying your GlobohomoNetID?
Any other cpu from the >>4506 list? (which is all shit)
>Will they be able to sabotage older ARM machines or will they be limited to just their new designs?
Old machines are safe, unless there's some yet unknown backdoor in them that can be triggered remotely. **ARM TrustZone is pretty much a black-box with lots of vulnerabilities so avoid it if possible**. As far as I can tell, current ARM manufactures can use their old licenses to produce old designs, so ARM won't disappear overnight, but if they want to produce newer revisions, they'll have to bend to nvidia's whim.

# 17
>One implementation is by Raptor, using Power9 ISA. Comparable to x86 desktops, very expensive.
For people familiar with the Power ISA those Raptor computers are an incredible bargain compared to their previously attempted POWER8 computer. The price on their TL2WK2 model started at under $5k back in 2018. The same model today is over $7k. By the end of next year it'll probably be around $10k. If the rumors are true about POWER10 being impossible to use in a libre computing platform because of PCIe 5 I wouldn't be surprised if this model sells for $15k or more in a few years.
https://web.archive.org/web/20180510191631/https://secure.raptorcs.com/content/TL2WK2/purchase.html
https://secure.raptorcs.com/content/TL2WK2/purchase.html

The PowerPC Notebook project is aiming for a 1000+ euro price point using a SoC from 2012 and that's a good deal compared to the earlier Power based A-Eon Amigas. I'm seriously considering getting the board as I've been following this project closely for years now and have been a ppc GNU/Linux user for over a decade.
http://powerpc-notebook.org/

You really need to know what you're getting involved with before jumping into this ISA. IBM owns RedHat from which the Fedora distro is created and ppc64le isn't even treated as a primary platform there as hardly anyone uses it. Desktop support for Power has been in a state of decay ever since Apple switched over to x86 making affordable Power based computers difficult to find and it's probably going to stay that way.

When it comes to embedded use sure IBM released two of their older chip designs to the public recently but it'll cost tens of millions to fabricate it, just getting it to the modern Power ISA standard and as something useful in a SBC would take a year or two of full time work. As long the z series mainframe CPUs keep coming out that's what IBM will use to create the new Power ISA standards. The whole open aspect of this ISA is just a make-work marketing move without any real backing behind it.

If you look at the OpenPower foundation's members most of the big names there that could have done something with it(Altema, Xilinx, Mellanox) have all been gobbled up by other ISA manufacturers. There's no real future for it outside of high performance computing. And so far it's the best the libre computing world has at the moment.

# 18
==MIPS==
What about MIPS? rms was known for using the MIPS-based Lemote Yeelong netbooks because it supported entirely free operating systems with no binary blobs. Looks like a few Linux distros and BSDs ave support for it, though Debian support, which is what I use, has fallen behind. Maybe a good time for me to learn Gentoo.

It seems like a pretty mature ISA. It's been around since 1985 so patents have expired on some older models. The N64, PS1, PS2, and PSP all used MIPS. It is still used in embedded systems and supercomputers, and is one of the commonly studied architectures in universities, yet there's not a lot of use on consumer PCs or servers so they should be relatively free from that sort of privacy infringing pozz we want to avoid. The Loongson CPU that Lemote uses has models as recent 2019.

If anyone has experience or insight on MIPS please share, I'm a newbie to this low level stuff.

# 19
>>6623
Was thinking of buying a GnuBee NAS device which is MIPS powered and the only current device I know of that's supported and in relatively common use by the GNU/Linux community.

MIPS is fine and if you're looking for a SBC to screw around with it the Creator Ci20/Ci40 board is pretty decent and it's also the only board on elinux.org/Main_Page#Hardware_Pages that isn't ARM or x86 based. The problem with MIPS is it's unlikely to see use in consumer products outside of the Asian market and it's only popular there because it's very cheap to license. Instead of making x86 or ARM chips they do emulation combined with MIPS which results in the MIPS software ecosystem remaining stagnant outside of embedded use.

Also in >>6467 I meant Altera instead of Atmel(misspelled as Altema), mixed up the two. Intel killed that company just as AMD is going to kill Xilinx and Nvidia will destroy Mellanox. All of the commotion we've been seeing in the CPU world relates to patents that expired or are set to expire soon.

# 20
>>6454
>Kim Jong il acquired Arm
I never had access to a Arm based processor before, but thinking how all that damn hardware producers are getting more monopolized with less choice available for the customer to purchase makes the future look pretty grim. Is there any news regarding between relationship of Nvidia and Intel or something? Because it makes me wonder why it took Nvidia so long to buy up a processor company.

# 21
>>6640
>Kim Jong il
Kek. Took me a minute to get that one.
>relationship
Well, they both sued each other about a decade or so ago. Not sure what the outcome of that was. But as you correctly observed the trend is for companies to gobble one another up. What's a bitter lawsuit and rivalry when the boards can each bank billions by consolidating? JK, I have no idea tbh Anon.

# 22
Someone posted this in the general engineering thread >>6338 related to some RISC/Arduino development board: https://www.youtube.com/watch?v=HNwWQ9zGT-8

# 23
>>6852
kek. that's faggot's condescending, jaded speech pattern is grating af.

# 24
>>4506
>Speaking to an experienced programmer, he told me the main reason why x86 is the main desktop/PC architecture, is that it allows compiling C almost directly to assembly. This is not the case as for ARM ISAs or RISC V.
The reason x86 is the main desktop/PC architecture is because the IBM PC won the 80s and became too big to fall. It became so big that IBM got cucked out of their own market when they tried to close it up and assert control, and that's a good thing.

# 25
>>6623
MIPS has one of the highest quality assemblies ever, but the company behind it went bankrupt in 2010. The reason it's popular in universities is exactly because of its extreme simplicity and beauty, it's perfect as a first assembly.
They liberated some recent versions and some old versions have expired patents, there's not even a point for that RISC-V shit anymore when MIPS is so much better and also free.

I'm not sure anyone will keep developing MIPS openly though, although MIPS hardware is still manufactured all over. Currently its ubiquity in some corners of the market (routers for instance) and relatively recent death means operating systems still have good support for MIPS, but there's nothing to say it will last.
I had a really good MIPS router called "Linksys WRT160N v3" but a really bad thunderstorm killed it, I miss it.

# 26
>>6856
>I had a really good MIPS router called "Linksys WRT160N v3" but a really bad thunderstorm killed it, I miss it.
==F==

I hope your implicit prediction that MIPS is dead and gone now turns out to be wrong tbh.

# 27
>>6858
He's probably right. The EOMA68 libre computing project looked into using MIPS but decided against it when they realized how little support it has outside of embedded.

>1.2ghz MIPS, with performance being somewhat lacking. The only decent OSes left for it are Debian, but the Libre variants were abandoned years ago due to lack of available MIPS32 hardware.
https://www.crowdsupply.com/eoma68/micro-desktop/updates/picking-a-processor

Also another option for libre computing that's been picking up steam recently is using FPGAs to run your own custom ISA. It's a very expensive proposition but is currently in development for secure computing;
https://www.bunniestudios.com/blog/?p=5971
It's been successfully used for classic console emulation with the MiSTer project. In a few years a 3-400mhz CPU done entirely in an FPGA for under $100 might be a thing.

# 28
>>7092

# 29
Good news: Chinese companies pushing Android on RiscV to be more independent from USA. This might help the RiscV development and adoption: https://github.com/T-head-Semi/aosp-riscv

# 30
>>8285
I consider Android itself highly dubious, given who develops it. But I can definitely appreciate the development of RISC-V into a sizable alternative ISA hardware platform. Thanks Anon.

# 31
I just found this;
https://www.extremetech.com/extreme/319318-robomorphic-computing-robot-response-times

Custom configurations may be superior and can be templated and improved upon to create new and better systems for robotics hardware for improved adaptability and faster responses

# 32
>>8315
One of the precepts Carver Mead's, et al, ''Neuromorphic Computing'' entails is driving the intelligence of a system further and further out to it's periphery. The closer the response evaluation systems get to the 'borders' of a system, the more biology-like it becomes, and also the more efficient. So, while in the case of robowaifus we can store the significant majority of the computing hardware itself tucked safely away inside a hardened breadbox in the robowaifu's chest, yet logically-speaking it would serve us well I think to follow Carver's lead on this topic.

If we can offload much of the sense/response cycle from a 'central' core general-purpose computing system tasked with higher-order decision making and oversight, and onto specialized hardware such as these types of tuned FPGAs, then we could more evenly distribute the computing loads (with an improvement in thermal/electrical efficiency btw). And as the article suggests we'd also improve response times due to latency issues through a whole chain of comms, etc., that would otherwise be required.

Also,
<"...Improving robot reaction times could allow them to operate effectively in emergency situations where quick responses are required."
>that opening image
Exactly what kind of 'emergency situations' are they implying here?
>**'''''SHUT IT DOWN!'''''**

# 33
nano/g had a post today re the RISC-V chip being 'verified' by OneSpin about a month ago.

>"OneSpin Contributes to the OpenHW Ecosystem to Achieve Processor Integrity for the CORE-V CVE4 Open-Source RISC-V Cores"
>"Automated formal solution detects bugs not found by simulation yielding high-quality of results and fast verification signoff:
www.design-reuse.com/news/49125/onespin-openhw-core-v-cve4-open-source-risc-v-processor-integrity.html

aHR0cDovL25hbm9jaGFucXpheXR3bHlkeWtiZzVueGtneWp4azN6c3JjdHh1b3hkbWJ4NWpiaDJ5ZHlwcmlkLm9uaW9uL2cvNDkwOCNwb3N0MzY0MDgK

# 34
>>8287
>I consider Android itself highly dubious
I concur. The worst thing are the proprietary driver. Lot's of hardware just doesn't work on bare linux, but runs on Android. It's almost a joke that we have incredibly beefy SoCs inside our phones, but can barely do much actual work with them.

# 35
>>8321
Yeah, sounds like something we should keep in mind. Object detection based on touch or slipping could be detected in the arms and lower legs. There also are already cam+sbc combos mentioned in the section for computer vision. 

>>8323
Aren't these drivers from the producers of the hardware? This is not an Android issue. Android can run on open source hardware, for all I know. Android itself is open source, but without the Google apps, and the name. So companies can build their own versions, without Google apps and they need to name it differently.
Anyways, my posting wasn't about Android but RISC-V lifting of. There will be more powerful processors coming and there will be better free  software libraries to support the RISC-V part of such chips.

# 36
>>8325
Replicant is an example of an alternative Android version funded by the FSF that removes the non-free code and built in Google telemetry. That project made headlines awhile back for finding a backdoor in one of the devices they were attempting to liberate
https://www.fsf.org/blogs/community/replicant-developers-find-and-close-samsung-galaxy-backdoor

Hardly anyone uses it it because of the few devices that can run it some of the functionality doesn't work unless you install non-free drivers which defeats the purpose. It's a huge issue when it comes to the GPU as it does software based rendering which is very inefficient. Only very recently due to new work being done on the Lima drivers for the Mali GPU may it be reasonable to use on ARM hardware that's almost a decade old. But we're still not there yet.
https://redmine.replicant.us/projects/replicant/wiki/DeviceStatus#Replicant-60

Having an open ISA running a permissively licensed OS is fine but when the hardware to use it requires a proprietary and signed bootloader or important parts of the SoC can't run without proprietary firmware that makes it unsuitable for a secure system. That's the road the RISC-V ecosystem is headed down.

# 37
>>8327
> That's the road the RISC-V ecosystem is headed down.
This is utterly negative. This was obviously going to happen. However, I think RISC-V itself will improve and there will be more competition. Some companies are more for open drivers than others. In other cases reverse engineering will solve the problem. Then there will be more and more old hardware designs becoming released as open source or the patents run out. And of course some company, university or foundation could create some CPU design and release it as a free hardware design.

# 38
>>8327
Thanks for the info I didn't know about the Replicant platform Anon.
>That's the road the RISC-V ecosystem is headed down.
I presume you mean a secure system? Or am I misinterpreting your meaning?

# 39
>>8315
After actually reading that article and not just the headline, it turned out to be very interesting.
>compute-bound kernels, such as calculating the gradient of rigid body dynamics, take 30 to 90 percent of the available runtime processing power in emerging nonlinear Model Predictive Control (MPC) systems
>The researchers report that implementing their proposed structure in an FPGA as opposed to a CPU or GPU reduces latency by 8x to 86x and improves response rates by an overall 1.9x – 2.9x when the FPGA is deployed as a co-processor.

# 40
Yeah, maybe I misunderstood him and he meant it's going well. Here's an interview with somebody working on RISC-V: https://youtu.be/lXdx0X2WHfY

# 41
>>8341
One of the most important things about non-proprietary standardization is longevity. For example, regardless of whatever else may happen in the software development industry's space, in 50 years C++ will still be a real thing, and you will still be able to compile your code then. This is simply b/c it's an open (and in this case international) standard. This is one important reason I stress C & C++ here, because they will stay around for us over the long haul.

RISC-V seems to bring this same kind of benefit to the table for processor hardware, as this guy brings out in the interview.

Thanks Anon, interesting. Please drop more here if you think of any on-topics.

# 42
FreeBSD on RISC-V talk
https://linuxreviews.org/FreeBSD_Fridays:_Introduction_to_RISC-V_on_FreeBSD

# 43
>>6467
The reason why relatively affordable and owner controlled POWER10 hardware won't be available has to do with the new OMI standard not PCIe 5
>In the future, even your RAM will have firmware; and the subject of POWER10 blobs
https://www.devever.net/~hl/omi
As that page explains this is very a different situation than with the controller boards on hard drives or SSDs having locked down proprietary firmware.

Saw this coming down the pipe for awhile(and has already been an issue with DDR4 on some SoC as mentioned in the footnotes in the link above) but I thought it would be a major issue in specialized NVMe drives for gaming or other niche tasks first. The only realistic solution for a FLOSS OS in a world where RAM is locked down is to have the entire OS only run in the cache on the CPU. Which isn't as crazy as it sounds considering how quickly it's growing.
https://www.nextplatform.com/2020/01/16/cache-is-king/

These issues always surface in high performance computing environments as they are the first to adopt new standards so by the middle of this decade it might be a more pressing issue that gets more attention. Heck I remember first reading about x86-64 CPUs that had blown fuses to only work with specific motherboards from servethehome.com
https://www.servethehome.com/amd-psb-vendor-locks-epyc-cpus-for-enhanced-security-at-a-cost/2/

# 44
An anon over in the R&D thread made a post >>8548 that led me indirectly to this.
https://web.archive.org/web/20180205224807/https://spectrum.ieee.org/tech-talk/computing/hardware/lowbudget-chip-design-how-hard-is-it

# 45
>"We are now using white designed but East Asian built cpus, because corporate cancer has devoured our fabs, and are likely to soon be using Chinese designed CPUs. People are starting to use the Exynos SoC, which is a Samsung design built in a Samsung fab for a Samsung built and designed CPU, and the Media Tec chips, which are designed and built in Taiwan. If I was building a home security system today, it would be running on Taiwanese designed and built CPUs and SoCs.

Don't know what this guy's blog is all about yet, but this quote most definitely caught my eye insofar as our computing concerns here on /robowaifu/ go.

https://blog.reaction.la/war/where-we-go-from-here/

# 46
We are definitely going to need some kind of ''Robowaifu Security General'', etc. But until we do, this thread probably is a better place than most to simply dump (at least somewhat) pertinent information, I suppose. Like many other domains we need to focus on, this one is most definitely multi-variate and ~~impossible~~ tough to pin down to a single topic.

https://en.wikipedia.org/wiki/Schnorr_signature

https://medium.com/bitbees/what-the-heck-is-schnorr-52ef5dba289f

https://medium.com/digitalassetresearch/schnorr-signatures-the-inevitability-of-privacy-in-bitcoin-b2f45a1f7287

# 47
>>9236
https://en.wikipedia.org/wiki/Lightning_Network

# 48
>>9237
https://medium.com/dataseries/triple-entry-accounting-system-a-revolution-with-blockchain-768f4d8cabd8

# 49
>>9238
https://academy.binance.com/en/articles/blockchain-scalability-sidechains-and-payment-channels

# 50
>>6629
>Intel killed that company just as AMD is going to kill Xilinx and Nvidia will destroy Mellanox.
smh
At least I hope Lattice will remain, the open-source tool chain is great to have (project IceStorm).

# 51
>>10930
>At least I hope Lattice will remain, the open-source tool chain is great to have (project IceStorm).
Sounds interesting Anon. Can you share more about it here?

# 52
>>10934
>Sounds interesting Anon. Can you share more about it here?
For as long as FPGAs (Field Programmable Gate Arrays) existed, the vendor software used to convert the Hardware Description Language (HDL) like Verilog/VHDL to logic netlist, place-and-route, and bitstream generation has been proprietary (Xilinx Vivado, Altera Quartus etc.). This meant that any open designs could only be open at the HDL level, and the rest had to be generated by the user. Even the top-level HDL files were sometimes proprietary as they were generated by vendor tools.

This changed when some very clever people reverse-engineered Lattice's iCE40 FPGAs. From there, open-source tools were written to support netlist generation, place-and-route, and bitstream generation. These tools are not only open, they run faster and can be used on an embedded computer (such as Olimex or Banana Pi). The latter point was considered unspeakable (vendor tools typically take +5GB of space and the RAM usage would be fairly high). This projects kicked off further development and research into other FPGAs. Of all the things I've heard in open-source, this is probably the most impressive.

At the moment the Yosys project (umbrella group) supports several FPGA architectures (ordered highest to lowest in terms of number of resources and capability):
-Xilinx 7 series
-Lattice ECP5 series
-Lattice iCE40 series

See the docs for more info:
https://symbiflow.readthedocs.io/en/latest/toolchain-desc/yosys.html

What does this mean for us?

Well, we can instantiate any processor architecture (MIPS, Z80, 6502, etc.) and design customised digital processing block or peripherals. Perhaps you need a 50-channel motor control module directly hooked up to a CPU running at 100MHz? No problem!

With these tools timing analysis can also be done, resource utilisation checked etc.

If you want to get started, TinyFPGA series of boards are not a bad choice. I have the BX model, and using it was straightforward on Debian Linux. (Also supports other OSs as well of course).

# 53
>>10936
Wow, that's much more interesting than I expected. Thanks for taking the time to spell out the details for us.
>Perhaps you need a 50-channel motor control module directly hooked up to a CPU running at 100MHz? No problem!
More like ''500'' channels, so maybe we need a wee little cluster of these CPUs? :^)

# 54
>>10938
>Thanks for taking the time to spell out the details for us.
There's something fun about turning history into a tale like that. Probably sticks in your head better too :P

>More like 500 channels, so maybe we need a wee little cluster of these CPUs? :^)
Now you're just being greedy XD
Although the EC5 and Xilinx 7 series might actually be able to handle that many (you'll be limited by the IC package more than anything...)

# 55
>>10941
>history into a tale
You know, I've thought that we should find someone who's interested in documenting the rise of the robowaifu age at the hand of a small band of anonymous men on the Internet. Should be a good read if done well.

>Now you're just being greedy XD
Heh, maybe. :^)
>Head, incl. eyes, lids, brows, mouth, jaw, tongue, nostrils, throat (w/ potentially cooling water consumption controls/valving) >50+ channels
>Neck+shoulders+chest, incl. head rotation/leaning, 'breathing', arm-rotation controls, shoulder girdle, ~50 channels (2 arms)
>Arm, incl. add'l shoulder, elbows, wrists, fingers, thumb, all finger knuckles, palm (50 channels per arm)
>Central torso/Pelvis, incl. spinal column rotation/leaning, pelvic girdle control, hips w/ rotations, ~50 channels
>Leg, incl. add'l hip, knee, ankle, ball of foot, toe flexion, ~50 channels (2 legs)
>Various power charging/control systems ?
>Various cooling systems ?
>Various computing power control/conditioning systems ?
>Add'l various kinematic/positional systems ?
>Visual analysis systems ?
>Hearing analysis systems ?
>Speech control systems ?
>Communications & control systems ?

and last, but certainly not least
>Literally hundreds of sensors of varied types, spread over the whole body (haptics, thermal, electrical, RF, pressure, kinematic)

It's quite possible that in the end, 500 is an ''under''estimate! :^)

> (you'll be limited by the IC package more than anything...)
Yes, agreed. I've already gotten some design approaches that encompass hundreds of connectors in a compact volume, pretty much lifted directly from industrial controls approaches.

# 56
>>10942
I was thinking of a distributed topology, where across the whole body there are low-level controllers that deal with sensors/actuators on an individual level, while communicating with a central (beefy) processor that's running the main OS. Something like a CAN bus in cars (although I can't speak for CAN as I haven't used it yet).

In that case, you won't need 100s of outputs on a single FPGA, but perhaps limited to about a 100 at most. Of course the difficulting of micro-managing movement arises.

But surely as the brain doesn't fully manage our bodies (the spine and other parts help out), so should the robo-waifu main system should delegate tasks?

Imagine a command protocol where instead of telling the leg to move to a specific set of coordinates, the main computer provides required tolerances (i.e. "appendage within 20 cm radius of torso" or "leg must distribute 35% of the overall weight" etc.) and the leg controller (MCU or FPGA etc.) actually does the system analysis to get the leg there. With greater tolerances, the solution can be achieved faster, and so rapid motions are either less precise, or preparation is required beforehand (the robowaifu gets into a running position and the actual run is a simple progression)

# 57
>>10942
>>10944
Also just had a thought. The local appendage controllers can be provided with a time duration for specific tolerances, thus allowing some level of autonomy.
The main controller would only update on a variable basis (depending on the complexity of the action) and only respond in real-time when an interrupt is received from the local controller saying that the appendage is outside the given tolerances. Perhaps like TCP (when a packet drops), the frequency at which main controller sends commands sharply increases when the appendage is outside tolerable range, and decreases proportionally to the rate of change of the deviation from tolerances.

# 58
>>10944
>>10945
(Another anon) Yeah, that sounds more like what I want, though others here want a central bread box in the chest with everything inside.

# 59
>>10944
>>10945
Yes. I've thought long and hard about these kinds of issues myself. Honestly, I think we probably need a new thread here that targets these kinds of topics. Something like "Robowaifu Motion Control Systems", or "Robowaifu Distributed Control Network" or something like that.

Ideas?

# 60
>>10947
>Ideas?
Hehehe, yes :)
Currently writing it, 1114 words so far. I'll try to make a basic diagram too.

I'll create a new thread for it; does "Robowaifu System Overview" sound alright?

# 61
>>11011
Sure. I'd say that sounds good, but you might want to tuck a 'control' in there somewhere in the subject. Seems to be a central idea on the topic. I'm sure your writing will guide you to a good name Anon.

# 62
>>10944
I've actually had this kind of idea rattling around in my head for a while and never bothered committing it to text.
I think what is the most likely feasible way to orchestrate a robowaifu "brain", for lack of a workable AGI, is to have specialized 'skill' AIs that handle specific tasks, rather than breaking it down by hardware subsystems.

For example, a 'locomotion' skill would need to incorporate both the legs and arms in order to keep balance and also provide a natural-seeming stride. Your 'chatbot' AI could be kept insulated from all the other skills so it only has to keep track of information relevant to its skill, rather than everything needing models for everything. This also serves to help break up AI development into a task manageable by a collection of random anons. It also means individual skill data can be crowd-sourced, so in theory all the AIs would learn from each-other. Group learning probably only really makes sense for 'non-personality' AIs, tasks that objectively have a way to be performed well (walking, driving) rather than subjective tasks (speech, decision-making, artistic-type tasks).

These specialized skills would somehow need to co-operate. Perhaps something like treating hardware parts as a 'lockable' resource so two skills don't try to use the legs and once and end up with your robot falling over. It'd make doing something like grabbing something fluidly as they walk by a nightmare and probably force them to do something like "go to position in front of object" > "stop" > "grab" > "proceed to next position" but it's better than the alternative.

We'd then have to train some sort of 'taskmaster' AI to handle behavior, taking inputs and outputs from these discrete 'skill' AIs and making behavior decisions based on them. I think that's a more manageable task that having one mega-AI that does everything, especially considering that hypothetical mega-AI would have to make the same decisions.

This has kind of been a ramble, but I'm interested to see what everyone else thinks about this idea of 'consciousness architecture'

# 63
>>11098
Good ideas Anon. The program separation as you mentioned is a goal we should strive for (at least at this point).

Have a look at the thread I made on RPCS (>>11018) as you may find it more relevant for the what you've mentioned. I'll be expanding what I wrote into a doc, and software architecture will be included (at least enough for the programmers to get going).

>'consciousness architecture'
This morning I was thinking about how the robowaifu software platform might work.
As the base, only the lowest level functions will be present (sensor check, calibration etc.). From there, you (the user) can load 'modules' that provide functionality and make the robowaifu's behaviour increasingly complex.
Even better if we could come up with an API that could be a long term standard, so that you could compare 'alpha' stage chatbot robowaifu all the way through to the latest and greatest masterchef/scuba-diving/prankster of a waifu.

# 64
>>11099
Yeah, that thread does seem more relevant. It might be more valuable to move this discussion there for later reference, since it seems to fall under the umbrella of 'control systems'

# 65
>>11098
I don't know what you mean by a workable AI. You seem to have this ideal of some completely from the scratch self learning system which you call AI. 
That aside, your thoughts are quite similar to mine. Same goes for >>11099. Though, I don't really see any problems with it. We should have subsystems, running on different hardware and communicate with each other. Of course, the software for it could be shared with others, since it doesn't contain private information.

# 66
>>11112
I meant workable "AGI" or "Artificial General Intelligence", which is different than the types of AI we have today. It could also be termed "strong AI", and has the ability to learn, on its own, any task a human can.

At present, what we have is "weak AI", which is generally an AI that is trained on and capable of performing one specific task (For example, image classification, driving, generating text, etc.). As a 'strong AI' is likely decades out (if not further, outside of any of our natural lifetimes), my idea is to combine multiple "weak AIs" into a whole, with a 'supervisor' AI that is tasked with figuring out the right response to a situation. It would still be unable to learn a new skill on its own and would require human aid to do so. However I believe it would, with enough single-task AIs, be able to be interacted with in a convincing enough manner for you to forget that fact.

This approach's most difficult part is still at the top, as a machine learning program to figure out the right thing to do still straddles the line between "weak" an d "strong" AI, but it has the benefits of some of the work already being done, being compartmentalized enough to be divided into sub-tasks, and also means we don't have to solve the harder problem of making software that can learn an entirely new skill.

# 67
>>11127
If it's like a human then it's AGI. Doesn't matter how it's designed inside. It should be made of different parts, including regular programs. Which also debunks the problem of some rampant super AGI, especially out of the blue.

# 68
Even though the primary topic for this post is about a secure OS implementation, I'm going to drop it ITT since it also relates to RISC-V hardware.
https://microkerneldude.wordpress.com/2021/05/05/sel4-on-risc-v-verified-to-binary-code/
https://sel4.systems/

# 69
A mad lad made a 1000 transistor silicon chip in his garage.
https://www.youtube.com/watch?v=IS5ycm7VfXg

>My chip is a simple 10×10 array of transistors to test, characterize, and tweak the process but this is a huge step closer to more advanced DIY computer chips. The Intel 4004 has 2,200 transistors and I’ve now made 1,200 on the same piece of silicon.
http://sam.zeloof.xyz/second-ic/

# 70
>>12421
This is really cool, thank you very much Anon! :^)
>related
http://sam.zeloof.xyz/maskless-photolithography/
http://sam.zeloof.xyz/developing-patterning-process-for-homemade-microelectronics/
http://sam.zeloof.xyz/category/semiconductor/

He clearly knows what he's doing, but he's using quite primitive techniques relatively-speaking. Obviously that's a prerequisite under these circumstances, but it's getting the job done after all. Seems like he's having some process contamination issues going (unsurprisingly tbh). But the size of the fab final assembly should mean he can fit it all into a homemade clean containment glovebox, so there's that.

My instinct is that you should be able to get this to a MC68000-tier machine process w/o any significant changes to the photolithography mechanism designs, apart from the steppers.

# 71
I haven't really thought much about security other than simply not giving it any sort of internet connectivity. I had thought about giving it some wireless connectivity, but only because of the limitations of fitting a PC inside of a space roughly the size and shape of a human skull and torso. I was thinking of a completely offline server with wireless transceiver and another transceiver inside the skull, with a signal only strong enough to maintain a signal within my own property.

# 72
>>4506
Going to necro this thread.
Does anyone use a librebooted thinkpad for their development? How is it? I'm getting one for backdoor-less work.

Second pic unrelated.

# 73
>>6858
MIPS back on the menu?  Restructure in 2021. 

https://www.mips.com/about/

# 74
>>14745
https://www.eejournal.com/article/wait-what-mips-becomes-risc-v/
I can't seem to find an official announcement but the article is linked by RISC-V's website: https://riscv.org/news/2021/03/wait-what-mips-becomes-risc-v-classic-cpu-company-exits-bankruptcy-throws-in-the-towel-jim-turley-electronics-engineering-journal/

# 75
>>13155
Please contribute ideas into the ''Sumomo Project'' thread Anon (>>14409) We're designing solutions that are intended to deal directly with issues such as this. Your feedback there would be appreciated!

>>13757
>Going to necro this thread.
Lol, we don't have such a thing as necro'ing here on /robowaifu/, Anon. We keep subjects on-topic to the extent feasible. Your's is in the right place afaict. I wish I had info for you, but I've never gotten my own Thinkpad yet. I know it's a popular topic though, so I imagine it's locatable info. Please share here again with anything you uncover Anon!

>>14745
>>14764
This would be welcome if true Anon. Have any >tl;dr for us a month passed?

