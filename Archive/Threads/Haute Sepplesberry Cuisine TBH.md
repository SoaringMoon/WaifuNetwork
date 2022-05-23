# 1
Good morning /robowaifu/. For today's cooking-lesson class, we'll be baking up some delicious Sepplesberry Pies. First we prepare some crispy and light Pi crusts and get them just right, then we'll load them up with tons and tonnes of succulent and Juci Sepplesberrys. We'll also mix in lots of other tasty goodness then pop them into the oven and after a couple hours, ''voilà!'' delightful Sepplesberry Pies.

>tl;dr
'''ITT we mek C++ dev boxes from RaspberryPi computers'''
>''C++ development main thread'' >>4895

Embedded processors and integrated systems programming naturally go hand-in-hand for /robowaifu/. The RaspberryPi and C++ are natural baseline choices for each of these categories. At this point in time they are both popular concerns with large communities behind them, and each bring objective benefits for us as robowaifu technicians. For the Pis they are quite powerful relatively speaking, and inexpensive as well. For C++ it has great performance and other characteristics when used correctly, with generic abstraction mechanisms second to none.

In an attempt to dovetail the two areas we're going to be going through setting up Raspberry Pis as little computers for learning the C++ programming language on. This should help every anon on /robowaifu/ that follows along to be on the same basic page for both embedded and programming. Once we're finished each of you will have your own little development exploration box you can literally carry around in your pocket. It will be self-contained, independent, and won't interfere with your other computing/vidya platforms. It will offer you a convenient way to begin controlling embedded hardware directly on the same machine that you write software for it on. 

This is a pretty compelling scenario IMO, and should serve us all as a good base from which we can branch out and grow from there. Working with other hardware and software will flow naturally from this project, and will give each of us a common experience from which we can build together and keep moving forward.

So let's get started /robowaifu/.

# 2
Okay, I'm to busy with other stuff, but curious: What are you going to do with it exactly? ROS? Control of motors?

# 3
>>4973
>In an attempt to dovetail the two areas we're going to be going through setting up Raspberry Pis as little computers for learning the C++ programming language on.

>ROS? Control of motors?
ROS is definitely not in the plan for these little boxes, but stepper control is definitely on the list.

# 4
Nice, really appreciate it.



Btw some other boards like Nvidia Jetson Nano, when I bought it they gave a disk image to download that's pretty much complete.  I haven't booted it since before the pandemic and I don't remember if the disk image already had Tensorflow pre-installed, but basically they enroll you in a couple of courses that are free with the purchase, it seems that there are already a couple of built-in AI functionality which you access through JupyterLab.



Of course, they want you to be beholden to their system.



Perhaps later on with this R Pi-based system we can have a shareable disk image that will contain the essentials.

# 5
>>4982
>Of course, they want you to be beholden to their system.
Jen-Hsun Huang needs a new black leather jacket bro!

>Perhaps later on with this R Pi-based system we can have a shareable disk image that will contain the essentials.
Very good idea Anon. Definitely on the ''TODO:'' list now. :^)

# 6
>'''Help! I want to learn too, but I don't have an RPi board yet.'''
==Nprb Fam, /robowaifu/ has you covered.==

Raspberry Pi offers a desktop spin of their platform. Since we'll have a standardized platform here, we'll be able to set them up identically and you can follow along with everyone who has their boards already. However, later on we'll be controlling the actual GPIO hardware pins themselves with C++, so you'll need to arrange to get yourself an RPi board by that point in time ofc (as well as a couple of inexpensive servos, etc.)

The spin comes as a bootable ISO image that you install as a virtual machine on your normal computer. You should be using a (real, non-VM) Linux along with all of us as your base machine to do this. I'll be demonstrating setting up the RPi Desktop image running under QEMU/KVM, on the Arch Linux derivative Manjaro. If you're still on Windows or macOS, then you can just use VirtualBox to do the setup.

First things first, go and grab a copy of 3GB image ''2020-02-12-rpd-x86-buster.iso'' from
www.raspberrypi.org/downloads/raspberry-pi-desktop/
and we'll get started.

# 7
To setup QEMU, etc., on your Manjaro Linux machine just follow the instructions on this wiki page:
https://wiki.manjaro.org/index.php?title=Virt-manager

Namely, enter:

```cpp
sudo pacman -S virt-manager qemu vde2 ebtables dnsmasq bridge-utils openbsd-netcat```
then run libvirt:

```cpp
sudo systemctl enable libvirtd.service
sudo systemctl start libvirtd.service```
That will get you up and running with QEMU and the Virtual Machine Manager front-end.

# 8
1. You can find the Virtual Machine Manager under Manjaro's System menu.
2. Double-click the ''User session'' item to connect.
3. Click the '+' to create a new virtual machine.
4. Choose Local install media.
5. Browse local to the downloaded ISO image.

# 9
1. Enter Debian 10 in the 'Choose the operating system' field.
2. Just click-through steps 3 & 4, then enter ''RPi_Desktop'' in the 'Name' field.
3. Use the arrow key and arrow-down to 'Graphical Install' .
  -NOTE: Left-ctrl + Left-alt will give you back the mouse cursor.
4. Resize the window by ''View > Resize to VM'', and click 'Continue' .
5. Choose 'Guided - use entire disk' .

# 10
1. Continue
2. Continue
3. Continue
4. Choose 'Yes' 
5. Go grab some coffee or tea. :^)

# 11
1. Choose 'Yes'
2. Choose '/dev/vda'
3. Continue
4. Just let it reboot into 'Debian GNU/Linux' **or as I’ve recently taken to calling it, GNU plus Linux :^)**
5. Resize the window again ''View > Resize to VM'' . 

Congrats Anon! You have Raspberry Pi up and running on your machine w/o having to have the embedded board.

# 12
An additional alternative (that we'll specifically be using later on when we no longer need/want a GUI on the target hardware) is to use the raspi-lite setup to run under QEMU:

```cpp
Raspbian Lite zip-archive: https://downloads.raspberrypi.org/raspbian_lite/images/raspbian_lite-2020-02-14/2020-02-13-raspbian-buster-lite.zip
Kernel image: https://github.com/dhruvvyas90/qemu-rpi-kernel/blob/master/kernel-qemu-5.4.51-buster
Device tree blob: https://github.com/dhruvvyas90/qemu-rpi-kernel/blob/master/versatile-pb-buster-5.4.51.dtb```

# 13
'''Time for the real hardware, Anon.'''

Alright, we're going to go ahead and set up the real RaspberryPi hardware for our C++ Learning Project now. I looked around in my pile of gear and found an older RPi device. It's an RPi 2b v1.1, copyright 2014. This is a 900Mhz device, 4 cores, with 1GB of RAM. If we can manage our little programming class project successfully on this older hardware, then we can surely do it on your newer Raspberry Pi of today, Anon. :^)

I'm planning to work with this hardware headless (no monitor), attached directly via Ethernet to my main box. The main box will be providing network access for the RPi hardware through the ''Shared to other computers'' method via it's Ethernet port out to the RPi. I'll be using a separate, inexpensive (~ US$20.00 ) keyboard with a built-in touchpad to run the RPi (just until we get the VNC server set up properly). This keyboard provides a mouse+keyboard dongle that we'll plug into one of the RPi's USB ports.

I'll be using an 8GB MicroSD card to hold the RPi system. A larger one would be fine, but it'd be best if you don't try to use a smaller one.
> #1
Insert it into it's adapter (as needed) and put it into your main box
> #2

Let's go ahead and download the ~2.5GB zip file we'll be using for our real hardware image, saving it onto our main box.
https://www.raspberrypi.org/downloads/raspberry-pi-os/
We'll use the '...with desktop and recommended softfware' version.
> #3
Then cd into it's download directory from the terminal shell.

Now that we have the file downloaded, we can write it out to our MicroSD card using the linux command ''dd''.
IMPORTANT: Figure out ahead of time ''exactly'' what the name of the MicroSD device is on your system.
https://www.raspberrypi.org/documentation/installation/installing-images/linux.md

An alternative to the instructions in the above link is just to use GParted to determine the MicroSD device name. Since we're going to use GParted later on with the actual RPi system, we'll go ahead and use that:
> #4
-It's also convenient enough to just unmount the device directly inside GParted as needed.
> #5

# 14
>>5165
As mentioned, we'll use '''dd''' to write the downloaded image out to the MicroSD disk.
https://tldp.org/LDP/abs/html/extmisc.html

 I'm going to combine unzip and write in one Bash statement, so in my specific case, the command is:
```cpp
unzip -p 2020-08-20-raspios-buster-armhf-full.zip | sudo dd of=/dev/mmcblk0 bs=4M conv=fsync```
> #1
In a few minutes the image should be written out to the device.
> #2

Checking again with GParted, we see you now have a fat32 ''/boot'' partition, and an ext4 ''/rootfs'' partition. 
> #3
Because of a setting with the bootloader (in regards to the next step), let's go ahead and move ''/rootfs'' to the end of the drive space. This will take several minutes to finish.
> #4

There is an unallocated block of 668MB, so we may as well go ahead and create a swap file there.
> #5

>===
''-'/rootfs' instead''
''-add code-block''

# 15
>>5166
Turn swapon.
> #1

Unmount the partitions, and eject the MicroSD card from your main box, then insert it into the RPi hardware drive slot (from the bottom side of the board).
> #2

Connect the Ethernet cable, HDMI video cable, mouse+keyboard dongle, and then power it up. Once it boots up, click the ''Cancel'' button on the initial 'Welcome to Raspberry Pi' dialog that first pops up. We'll deal with updates a little later.
> #3

# 16
>>5167
Alright that's it for today class. If you've followed along successfully, congrats. You've begun a journey into embedded computing. :^) We'll continue on with the RPi preliminaries soon. As always, if you get stuck or have any questions just ask ITT.

Cheers

# 17
Alright, there are a couple of things to get set up on the main box as well so we can work with our SepplesberryPi w/o having to use either a monitor, keyboard, or mouse connected to it. We'll connect it directly to our main box with an Ethernet cable for it's networking. IIRC, I think W*ndows calls this ''Internet Connection Sharing'', but ofc we'll be using Linux instead. 

So, I use the WiFi for my main box's Internet access. This leaves the Ethernet wired port available. And it's this port we'll set up for the RPi to get out to the network with. You configure the settings on your main box to ''bridge'' the two connections (and this will also provide DHCP settings for any incoming clients connecting through the Ethernet port). For the RPi, you don't have to do anything special, it just werks.

BTW, YMMV. This setup is workable for my specific situation. You may want to connect yours straight into your router, or across the WiFi, etc. Just make sure you can figure out what it's IP address is afterwards b/c you'll need it for the other step. 

Then, we'll use VNC to control our RPi remotely. The RPi has the VNC server software already installed, but we'll need to install the viewer software on our main box. Once everything's set up, you'll no longer need to use those other peripherals to work on your RPi dev box.

Go ahead and plug the two boxes together with the Ethernet cable in between.

On your main machine, choose 'Advanced Network Configuration'.
> #1

Select the Ethernet connection, then click the little gear for 'Edit the selected connection'.
> #2

Choose ''IPv4 Settings > Method > Shared to other computers'' then save.
> #3

That should be all that's needed. Power cycle your RPi and it should now have an IP address given to it by your main box, and should be able to get out to the Internet as normal also. If things don't quite work for you at first, you might check the ip addresses on your main box with ''ifconfig'', and also try pinging some known-good domain to make sure there's not any issues with the main box itself. As always, you can ask questions ITT.

# 18
>>5214
On the RPi, we see scrot is already installed by default, and that we have only 408 MB free on the drive. We'll free some space up before we're done.

Let's go ahead and set up VNC then we'll no longer need the physical keyboard+mouse, nor the HDMI monitor attached to our RPi hardware.

Select ''[RPi Menu] > Preferences > Raspberry Pi Configuration''
> #1

Enable ''SSH'' & ''VNC''.
> #2

Now check your IP address under the ''VNC Server'' applet, you'll need this address for the viewer on your main box.
> #3

# 19
>>5216
Alright, that's got the VNC server running on the RPi sorted, now let's get the client up on our main box. I'm just going to use the Pamac graphical software installer tool for it.
> #1

Start the viewer software and then enter the IP address from the RPi you got in the previous step. The client software will warn you this is an unrecognized server, click 'Continue' .
> #2

Congrats Anon, you're now jacked in:
> #3

# 20
>>5257
Alright, now that we have everything working for us to remote into the RPi, I'm going to go headless with mine. After powering the RPi box down, I'm unplugging the keyboard, mouse, and HDMI monitor connection. I'm ''also'' going to unplug the Ethernet cable, b/c in my final setup, I'll be moving the RPi to the server room and connecting it directly into my internal router. I'll still use my main box to run it remotely by using it's new IP address.

In your case, you can feel free to continue using your 'Shared to other computers' connection, and that way if you don't have a router handy your RPi can run that way.

So, once I moved the RPi and got the new IP address to use for a new VNC client connection, I see this:
> #1

Other than the obvious security warning, you notice that the screen dimensions have also gotten much smaller (they previously auto-adjusted to the HDMI monitor I had plugged in for the initial RPi setup).

Click 'OK', then select ''Select [RPi Menu] > Preferences > Raspberry Pi Configuration > Change Password''
> #2

While we're in here, we may as well go ahead and fix the display too. ''Display > Set Resolution'' 1280x720 will be good enough in my case.
> #3

Now drag the dialog up as far as you can, to just be able to see the 'OK' button hiding at the bottom...
> #4

...and click it to reboot, enter your new password, and see the new changes. Change your ''[RPi Menu] > Preferences > Appearance Settings > Picture'' to something better and click OK.
> #5

There, that's better! :^)

# 21
As mentioned, we'll free some space up on our RPis. We should also update them as well. Ever have to juggle apps on your phone's limited space? This is a little like that. Also, if anyone has good advice here on this general topic of system/storage cleanup, please speak up here ITT. :^)

So, on my RPi, I'm going to purge unused locales and LibreOffice.

In a terminal, run

```cpp
sudo apt-get install localepurge```
then select 'OK'
> #1

Since ''en_GB.UTF-8'' is already selected (by default), just go ahead and select 'OK' again to purge everything. Select 'Yes' when asked about the dpkg setting.

Then we can remove the locale files themselves:

```cpp
sudo rm -rf /usr/share/locale```
> #2

That will free a few hundred meg. Let's purge LibreOffice to free more:

```cpp
sudo apt-get remove --purge libreoffice*
sudo apt-get clean
sudo apt-get autoremove```

So, altogether that gives us a little more than a gig free.
> #3

==UPDATE==
>Read the full post before proceeding Anon...

That should be enough room, so let's go ahead and upgrade everything now: (this will take a good while, probably around 60 minutes. start htop in another terminal tab if you'd like to watch over the system during this period)
```cpp
sudo apt-get update && sudo apt-get upgrade```

-Update: Turns out, 1.1GB ''wasn't'' enough to upgrade Wolfram along with everything else (no space left on device error). :/
> #4

I planned on removing it and other software on my RPi anyway (since it's not about learning C++) so I'll go ahead and remove it and other programs to free up even more room, and we'll try again.

# 22
>>5264
Alright, I'm going to go ahead and remove several of the programming systems to free up room, in particular Wolfram is quite large for our small system. Pick and choose your own choices for deletion, ofc. (In particular, if you've never programmed before, I'd recommend looking at Scratch as well as taking our C++ class).
```cpp
sudo apt-get remove --purge wolfram*
sudo apt-get remove --purge bluej*
sudo apt-get remove --purge thonny*
sudo apt-get remove --purge greenfoot*```

Then, do another autoremove to pick up stragglers:
```cpp
sudo apt-get clean
sudo apt-get autoremove```

That gives us over 3 gigs free now. 
> #1

==NOTE:== If you didn't run this from the previous post b/c you saw the update about the issue with wolfram, then you should run this now:
```cpp
sudo apt-get update && sudo apt-get upgrade```

Remember, that swap partition on the drive from before? Let's go ahead and activate it now. I'll use GParted installed right on the RPi itself this time.
```cpp
sudo apt-get install gparted```

After installation, you can find it in ''[RPi Menu] > System Tools > GParted''

Highlite the 668MB partition and choose 'Swapon'
> #2

You can quickly check that you have the 768M swap now with htop
> #3

Alright, that gives us plenty of room for our next steps, setting up a powerful C++ tooling system on our RPi box. We'll do that next.

>===
>''-removed Scratch from the deletion list, since there was enough room for it after all''
>''-added note about running upgrade''

# 23
Alright first things first, we'll set up the prerequisites for my favorite open-source C++ IDE on Linux.
https://gitlab.com/cppit/jucipp
> #1

```cpp
sudo apt-get install libclang-dev liblldb-dev || sudo apt-get install libclang-6.0-dev liblldb-6.0-dev || sudo apt-get install libclang-4.0-dev liblldb-4.0-dev || sudo apt-get install libclang-3.8-dev liblldb-3.8-dev
sudo apt-get install universal-ctags || sudo apt-get install exuberant-ctags
sudo apt-get install git cmake make g++ clang-format pkg-config libboost-filesystem-dev libboost-serialization-dev libgtksourceviewmm-3.0-dev aspell-en libaspell-dev libgit2-dev
```

We can go ahead and install Mesonbuild as well.
```cpp
sudo apt-get install meson```

Now, let's pull the repo, then build and install juCi++ itself. (this will take a good long while (~30min) to finish during the ''make'' step, you might want an htop tab open again. also, ensure your big swapfile is on, you might just need it! :^) 
```cpp
git clone --recursive https://gitlab.com/cppit/jucipp
mkdir jucipp/build
cd jucipp/build
cmake -DCMAKE_CXX_COMPILER=g++ ..
make -j2
sudo make install```

The installed executable name is simply ''juci''
> #2

Use mousepad editor to edit the ~/.juci/config/config.json file with these edits:
```cpp
"variant": "dark"```
and
```cpp
"style": "juci-dark-blue"```
and
```cpp
"font": "Noto Sans Mono 16"```
> #3

Then restart and you should have a nice dark theme. Create a simple C++ project, then ''Project > Compile and Run''
> #4 #5

You should see why I appreciate this simple-looking IDE soon I imagine. 

Well, I think that's more than enough for today's class, and a good stopping point. So we'll pick up with the rest of the tooling setup next time (we're almost there). 

Cheers.

# 24
>>5270
'''Quick update'''
I noticed afterwards looking at #4 & #5 that the source font ''wasn't'' monospaced. Checking further, sure enough Noto Sans Mono font was missing (probably wiped during the LibreOffice purge). So we'll go ahead and grab all those fonts again.

-On the RPi box, start Chromium and go to:
https://www.google.com/get/noto/
filter for ''Noto Sans Mono'' and then download the zip file
> #1

-Extract the fonts out
> #2

-Then start a terminal and enter
```cpp
cd /usr/share/fonts/truetype/noto```

```cpp
sudo cp /home/pi/Downloads/NotoSansMono*.ttf .```

```cpp
sudo chmod 644 *.ttf```

```cpp
ls -lah```
> #3

-Now restart juci and confirm the source editor pane is in fact now using the Noto Sans Mono font
> #4

Sorry about that little oversight class. :^)

# 25
>>5289
''Additional minor update''
Looking at the screen capture from this post, I wasn't too pleased with the font rendering inside the editor. I managed a minor improvement for it by setting the '' [RPi Menu] > Preferences > Appearance Settings > Defaults'' to the 'For medium screens:' selection.
> #1

# 26
I'm also going to turn on the 80-char indicator, and add a shortcut keys for ''Zen mode'' to juci.

Use mousepad editor to edit the ~/.juci/config/config.json file with these edits:
```cpp
"show_right_margin": true```

```cpp
"window_toggle_zen_mode": "<primary><alt>z"```

Here's the zen mode activated:
> #2

Even more simple focus with juci ''F-11'''d
> #3

# 27
>>5292
>>5291
I also noticed that I could further improve the font rendering in the editor if I changed the font in the gtk_theme section as well:
```cpp
"font": "Arial 16"```
> #1

To my eye, it seems to crispen up the entire window's fonts for some reason.
> #2

# 28
OK, let's finish setting up the tooling for our SepplesberryPi machines, and then we can move on with the beginnings of our C++ class instead of all this **boring** sysadmin-type stuff! :^)

Let's go ahead and install a package manager called synaptic onto our RPis first:
```cpp
sudo apt-get install synaptic```

Once it's installed, you can find it under ''[RPi Menu] > Preferences > Synaptic Package Manager''
> #1

It's a convenient tool for getting quick insights into package's installation status, etc. For example, let's search for the llvm-toolchain tool ''clang-format'':
> #2

You can see that ''clang-format-7'' has been installed already, but we actually want the newer version 9 instead. So, we can use synaptic to remove the old version and install the new version in it's place.
-Select the two installed versions (ctrl+click), then right-click and choose ''Mark for Complete Removal''.
> #3

-Then select ''clang-format-9'', right-click and ''Mark for installation''
-Click 'Apply' (it's the little paper airplane icon)
Once everything's completed you should see this:
> #4

clang-format version 9 is installed now. But we still need to set up a symlink for the new version so we can use just the shortcut name ''clang-format'' w/o having to pay attention to the version number. First out of curiosity, we can see what's listed for the tool now:
```cpp
ls -lah /usr/bin | grep 'clang-format'```
and see it's a symlink: ''clang-format-9 -> ../lib/llvm-9/bin/clang-format''

Now let's create a new one for the shortcut term:
```cpp
sudo ln -sf /usr/bin/clang-format-9 /usr/bin/clang-format```

Now we can check the version with the short name and see everything's updated for the new version now:
> #5

# 29
>>5309
OK, now let's basically repeat the entire process to setup another powerful llvm-toolchain tool, ''clang-tidy''.

-Search 'clang-tidy' in Synaptic:
> #1

-Mark ''clang-tidy-9'' for installation and accept the additional changes:
> #2

-Apply the changes. Let's see what version is installed on the system now, from the terminal:
```cpp
ls -lah /usr/bin | grep 'clang-tidy'```
> #3

-Let's create the shortcut name symlink and check the version number as well.
```cpp
sudo ln -sf /usr/bin/clang-tidy-9 /usr/bin/clang-tidy```

```cpp
clang-tidy --version```
> #4

# 30
>>5310
Alright, let's finish up installs for now by adding a few useful utilities, and the amazing text editor ''Vim'' into the mix.

```cpp
sudo apt-get install iftop nethogs tmux vim```
> #1

If you're new to Vim, be sure to try the vimtutor 30minute tutorial first, Anon!
```cpp
vimtutor```
> #2

# 31
Alright, let's create a couple of config files and we should be all set for C++ class this weekend.

Clang-tidy is a powerful linting tool that helps uncover buggy code. Don't leave home without it. :^)
https://releases.llvm.org/9.0.0/tools/clang/tools/extra/docs/clang-tidy/index.html

Let's use it to create an initial config file, which we can then tweak. We'll create both files in our ''pi'' home directory.
```cpp
cd```
then
```cpp
clang-tidy --format-style=chromium --dump-config > .clang-tidy```

Let's have a look inside the file that was created.
```cpp
mousepad .clang-tidy```
> #1

You don't have to understand ''any'' of this atp, and the only thing we're interested in for now is the very first key value in the file: ''Checks''
'''Checks:          'clang-diagnostic-*,clang-analyzer-*'''''

We're going to add several entries in addition to the two there now. The easiest way for you to do this will simply be to hilight the whole line #2, then copy+paste all this text over top of it:
```cpp
Checks:          'clang-diagnostic-*,
clang-analyzer-*,
modernize-*,
-modernize-use-trailing-return-type,
cppcoreguidelines-*,
-cppcoreguidelines-avoid-magic-numbers,
bugprone-*,
readability-*,
-readability-magic-numbers,
cert-*,
misc-*,
performance-*,
hicpp-*'```

So, if you've done it right, then your .clang-tidy file will now look like this.
> #2
Be sure to save it.

>===

The other important tool we need a config file for is clang-format. It's a remarkable tool to always keep the C++ software code files you (or others) create looking consistent, and formatted properly.
https://releases.llvm.org/9.0.0/tools/clang/docs/ClangFormat.html

Creating a config file for it is similar to clang-tidy. Enter this in the terminal:
```cpp
clang-format -style=chromium -dump-config > .clang-format```
> #3

and we'll just leave that one as is for now (but feel free to look inside it ofc).

# 32
Well, believe it or not
==we're finally done==
**>implying**

Heh, at least that should be enough for us to go on with for now. :^)

I may redo this entire thread one day from the lessons I learned creating it to make it more straightforward and easier to work through. My apologies for it being the mess that it is try to do better next time.

Anyways, onward!!
>>4895

# 33
>>5313
Thanks anon, this should save me a bit more money in my robowaifu endeavors, btw is it possible to implement this into a raspberry pi tower?

# 34
>>5320
nprb, y/w. 
>RPi tower
if i understand you correctly, then yes. there are numerous examples of RPi Beowulf clusters out there. our ''Robowaifu-OS & Robowaifu-Brain(cluster)'' thread talks about it.
>>201

# 35
Not too surprisingly, I forgot at least one step, namely we need short name symlinks for the clang compilers and debugger. from the terminal:
```cpp
sudo ln -sf /usr/bin/clang-9 /usr/bin/clang
sudo ln -sf /usr/bin/clang++-9 /usr/bin/clang++
sudo ln -sf /usr/bin/lldb-9 /usr/bin/lldb```

Now we can check the versions:
> #1

# 36
>>5270
One thing I didn't go over for when it's needed, is how to update a local git repo and rebuild/reinstall it (whenever the source repo is updated with new software for example). Switch into the same local repo and git pull:
```cpp
cd jucipp
git pull```

Since this is a repo with submodules, you should update those as well for good measure:
```cpp
git submodule update --init --recursive
git submodule foreach --recursive git fetch
git submodule foreach git merge origin master```

Then do the typical cmake/make dance again:
```cpp
cd build
cmake -DCMAKE_CXX_COMPILER=g++ -DCMAKE_BUILD_TYPE=Release ..
make -j2
sudo make install```

And actually, since we switched the llvm-toolchain dev libraries over to version 9 earlier, you should go ahead and rebuild your juci IDE anyway since it depends on those libs.

>===
-''add release mode to cmake cmd''

# 37
BTW, I'd suggest you regularly update your system yourself. My impression is that the Raspberry Pi Foundation's approach to this is a bit lax.

```cpp
sudo apt-get update && sudo apt-get upgrade```

# 38
>>5313
Thanks mate, great tutorial!
Apologies, I only just had a look at it. I picked a some things that I'll take away, like VNC and the juci IDE. Have you used Code Blocks? That's the one I use for C development (the subleq assembler) at the moment. Not sure how the two compare, but I'll give it a go later.
C++ is definitely attractive, as long as I can optimise it sufficiently. Having namespaces would be REALLY nice XD
Thanks again anon!

# 39
>>5426
Sure thing, you're welcome mate.

>Have you used Code Blocks?
Yes, I've both used it, and it's available in the RPi (Buster) repos at v17. Give it a try on the RPi if you'd like (I'd suggest trying Geany first though).

Juci++ does a much better job of supporting the llvm/clang toolchain directly, which IMO is basically indispensable ATP. It also directly supports both CMake and the more modern Meson build systems, again, an indispensable item on the checklist. Plus for my tastes, I much prefer the simplified interface for the IDE the guys have chosen to implement for it. It's not perfect, but it's definitely my favorite IDE for writing C or C++ code on Linux with.

I think we'll pretty much show that modern C++ brings a lot of benefits to the table for embedded development.

# 40
>>5427
>Juci++ does a much better job of supporting the llvm/clang toolchain directly, which IMO is basically indispensable ATP. It also directly supports both CMake and the more modern Meson build systems, again, an indispensable item on the checklist. Plus for my tastes, I much prefer the simplified interface for the IDE the guys have chosen to implement for it. It's not perfect, but it's definitely my favorite IDE for writing C or C++ code on Linux with.
Sure, no you definitely sold juci for me ;)
>I think we'll pretty much show that modern C++ brings a lot of benefits to the table for embedded development.
Actually watched a lecture by this training company (duolos) on embedded c++, and saw some really good features, some of which C seems to have taken.
Definitely replacing preprocessor directives with constants and inline functions will save time and hassle as the compiler can help you.
Not sure about the iostreams though, seems to be very (and perhaps too much for embedded) complex. 
Basically one needs to write it much more carefully than on a general computer, as I can see memory requirements become very large.

# 41
>>5430
>Not sure about the iostreams though, seems to be very (and perhaps too much for embedded) complex. 
I get you on that. But one of the great features about C++ streams is they are both type-aware and type-safe. They also have quite sophisticated transformations built right it. But yes, not all embedded devices will afford us the luxury of the SBC-class machines, and for them, avoiding the use of streams makes sense. One '''very''' nice thing about C++ from the very beginning is the principle ''You don't pay for what you don't use'' ( the zero-overhead principle https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines#inaims-aims ).

# 42
>>5432
*very* interesting....thanks anon.
Now you made me want to read the c++ books damn it XD

# 43
>>5434
Haha, no need to rush Anon. I expect the C++ learning thread will go on for at least one year, Lord willing. I think you'll pick it up rather organically if you follow along with us (at least that's one of my goals in doing it). Take your time.

# 44
OK, Anon very graciously offered to make the effort to port his amazing ''WaifuSynth'' & ''Clipchan'' projects over to ''mlpack'' so anons can use them on older/smaller hardware, and to be freed from Big Tech stranglehold on our robowaifus.
>>5718
>In a few months I'll definitely see if I can port Spleeter and WaifuSynth to mlpack. That would completely disentangle ourselves from Facebook and Google and be a huge step forward to keeping AI open.

So, in an effort to both encourage him in this big undertaking, and to make a simple validation of the basic idea on our little RPi boxes, let's install mlpack and create the basic ''Nearest Neighbor'' 'hello world' test project for it.

-Open synaptic & search 'mlpack'. Mark all 4 items that show up for installation. You can examine all the things with the 'Show Details' button.
> #1 #2

-Visit ''mlpack.org'' and you'll see they have the basic example right on the front page. We'll use this as copypasta for our own project.
> #3

-Fire up Juci and create a project. I'm naming mine 'mlpack_test'
> #4

-Delete the .clang-format file from the project, so it uses our better one in our home directory.

-Open the ''CMakeLists.txt'' file and make these three changes:
  -change -std=c++1y to -std=c++17
  -add -fopenmp flag
  -add mlpack target_link_libraries line
> #5

# 45
>>5730
Be sure your swapfile is on anon, you'll need it heh! :^)
> #1

Replace the basic ''main.cpp'' code with the example code from mlpack.org, and build (ctrl+enter). This will take a while b/c raisins, and you'll get a number of 'parameter passing changed in GCC 7.1' alerts. You can gnore them. 

If all went well, you should see pic related.
> #2

```cpp
Nearest neighbor of point 0 is point 3 and the distance is 0.449757.
Nearest neighbor of point 1 is point 2 and the distance is 0.918409.
Nearest neighbor of point 2 is point 1 and the distance is 0.918409.
Nearest neighbor of point 3 is point 0 and the distance is 0.449757.```
We can see these outputs precisely match the test values on their website. Congrats Anon, you now have the power of AI in your hands on your SepplesberryPi! :^)

>===
-''add 'ctrl+enter' note''
-''minor prose edit''

# 46
>>5731
>main.cpp
```cpp
// This is an interactive demo, so feel free to change the code and click the
// 'Run' button.

// This simple program uses the mlpack::neighbor::NeighborSearch object
// to find the nearest neighbor of each point in a dataset using the L1 metric,
// and then print the index of the neighbor and the distance of it to stdout.

#include <mlpack/core.hpp>
#include <mlpack/methods/neighbor_search/neighbor_search.hpp>

using namespace mlpack;
using namespace mlpack::neighbor;  // NeighborSearch and NearestNeighborSort
using namespace mlpack::metric;    // ManhattanDistance

int main() {
  // Load the data from data.csv (hard-coded).  Use CLI for simple command-line
  // parameter handling.
  arma::mat data(
      "0.339406815,0.843176636,0.472701471; \
       0.212587646,0.351174901,0.81056695;  \
       0.160147626,0.255047893,0.04072469;  \
       0.564535197,0.943435462,0.597070812");
  data = data.t();

  // Use templates to specify that we want a NeighborSearch object which uses
  // the Manhattan distance.
  NeighborSearch<NearestNeighborSort, ManhattanDistance> nn(data);

  // Create the object we will store the nearest neighbors in.
  arma::Mat<size_t> neighbors;
  arma::mat distances;  // We need to store the distance too.

  // Compute the neighbors.
  nn.Search(1, neighbors, distances);

  // Write each neighbor and distance using Log.
  for (size_t i = 0; i < neighbors.n_elem; ++i) {
    std::cout << "Nearest neighbor of point " << i << " is point "
              << neighbors[i] << " and the distance is " << distances[i] << "."
              << std::endl;
  }

  return 0;
}```

>CMakeLists.txt
```cpp
cmake_minimum_required(VERSION 2.8)

project(mlpack_test)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++17 -Wall -Wextra -fopenmp")

add_executable(mlpack_test main.cpp)

target_link_libraries(mlpack_test mlpack)```

# 47
==Alert==
There's a 0-day software exploit that's been discovered regarding the FreeType library.
>>6004


Your RPi machines are vulnerable to this, so please follow the instructions Anon generously provided in that post (download the zip, unzip, cd into that directory, &tc). Just change the last confirmation command to this instead as your filename is different on your RPis:
```cpp
ldd /usr/lib/chromium-browser/chromium-browser | grep freetype```

# 48
>>6009
BTW, as already mentioned ITT, but worth mentioning again here, you ought to regularly keep your RPis updated manually, as they aren't very good at keeping themselves up to date currently.
```cpp
sudo apt-get update && sudo apt-get upgrade```

# 49
We're going to be using FLTK as our GUI/Widget toolkit for our classwork. Visit https://www.fltk.org/ and click the ''Download'' link.
> #1
We'll be building the v1.3.5 directly from source:
https://www.fltk.org/pub/fltk/1.3.5/fltk-1.3.5-source.tar.bz2
> #2
Extract it then cd into it's directory on the terminal.
> #3

Enter these commands in order:
```cpp
./configure
make -j3
sudo make install```
> #4

OK, you're all set. The library is installed, and so is a GUI designer tool called ''FLUID''. You can start reading the docs and examples now to get ahead of the class.
https://www.fltk.org/pub/fltk/1.3.5/fltk-1.3.5-docs-pdf.tar.gz
/usr/local/share/doc/fltk

>'''FAQ'''
==Why FLTK?==
-A) It's incredibly lightweight/fast. This means in can run on practically everything, including processors significantly smaller than our RPi.
-B) It's actually quite a simple programming model, and one that's been wrung out for over 3 decades now on a very wide array of hardware.
> #5

>''"But it looks wonky. WAHHH!11 I want my iPh*ne interface."''
'''Be a man, Anon. Our robowaifus will need lightweight GUIs.''' 
**:^)**

# 50
>>6307
'''Oh Brother'''
So, I decided to port a little sample app from my main box over to the new RPi FLTK install and only discovered ''afterwards'' there's an apparent driver incompatibility on the RPi itself with the 1.3.5 code.

Sorry about that oversight class.



So, just start Synaptic, search ''FLTK'', then mark ''libfltk1.3-dev'' for installation, and this will install the older 1.3.4-9 version and prerequisites:
> #

# 51
Start Juci and create a new project, using Meson as your build system. We'll overwrite it's default files in just a minute.

Open ''[RPi Menu] > Programming > FLUID'' to open the graphical designer and play around with it. Here's a quick sample from it I whipped up inside ''FLUID''. Click the 'Function', then 'Window', then 'Button' and tweak everything the way you want.
> #1

Choose ''Edit > Project Settings" in FLUID and change the header and code file extensions to '.hpp' and '.cpp' respectively.
> #2

Then choose ''File > Write Code...'' in the FLUID interface, and save the files out the designer created for you. Do this into the same project directory you created above in Juci.
> #3

Here are all the modification to my 4 files for this example:
>main.cpp
```cpp
#include <iostream>

#include "fluid_test.hpp"

int main() {
  std::cout << "Hello World!\n";

  auto foo = make_window();
  foo->show();

  return Fl::run();
}```

>fluid_test.hpp
```cpp
// generated by Fast Light User Interface Designer (fluid) version 1.0305

#ifndef fluid_test_hpp
#define fluid_test_hpp
#include <FL/Fl.H>
#include <FL/Fl_Double_Window.H>
#include <FL/Fl_Button.H>
Fl_Double_Window* make_window();
#endif```

>fluid_test.cpp
```cpp
// generated by Fast Light User Interface Designer (fluid) version 1.0305

#include "fluid_test.hpp"

Fl_Double_Window* make_window() {
  Fl_Double_Window* w;
  { Fl_Double_Window* o = new Fl_Double_Window(805, 505);
    w = o; if (w) {/* empty */}
    { Fl_Button* o = new Fl_Button(50, 150, 705, 145, "Hello /robowaifu/ !");
      o->box(FL_SHADOW_BOX);
      o->labelfont(11);
      o->labelsize(64);
    } // Fl_Button* o
    o->end();
  } // Fl_Double_Window* o
  return w;
}```

>meson.build
```cpp
project('fltk_test', 'cpp')

add_project_arguments('-std=c++2a', '-Wall', '-Wextra', language: 'cpp')

cxx = meson.get_compiler('cpp')
fltk_dep = cxx.find_library('fltk')

executable('fltk_test', ['main.cpp', 'fluid_test.cpp'],
           dependencies : fltk_dep )```
> #4

Build it (ctrl+enter)
> #5

Grats, you're now haxoring GUI apps for your robowaifu Anon. Now that you've done all the legwork, you can thereafter quickly change things around inside FLUID, write the code out, then rebuild everything in Juci. It will take just seconds to tweak things around for you now.

If you get stuck, just do what I did and make sure you have the same 4 files in your Juci project directory, and that they contain the same code from above (and that you named the files just like mine). As always asks questions ITT if you need to.

# 52
>>6310
Oops, intended to post this cap here.
>

# 53
>>6313
> using Meson as your build system
Another oops. I just realized I haven't gone over doing that ITT yet, but in another thread.
>>5990

Apologies about that. Meson in general is much easier to use than CMake--especially for a library like FLTK.

# 54
>>6310
>>6314
__Update__: I began to have a suspicion that possibly it was the ''prerequisites'' that were the issue rather than the version of FLTK source code (which frankly made no sense in this context. it's very well-done code). 

I went back into the source extract and reran the build/install cycle, then re-tested my little sample app in Juci. Sure enough, everything works fine now. I'm not really sure why the ''./configure'' step didn't pick up any issues but w/e.

So, you can use latest version of FLTK source after all. Just go back into the extract directory and enter the same 3 commands as before:
```cpp
./configure
make -j3
sudo make install```
> #1

Inside Juci choose ''Project > Recreate Build'' (this will nuke the previous meson build directory contents)
> #2

Then build. Your GUI applications should now be using the static 1.3.5 version of the FLTK library.
> #3

I suspect the issue was something wonky with the original RPi X11 lib before the install via Synaptic.

# 55
>>6307
>/usr/local/share/doc/fltk

There are some nice demo programs in the examples folder there. For example, there's one called ''curves.cxx'' which demos Bézier curves and slider widgets. 
> 
Since I'm interested in creating a node-graph GUI to represent robowaifu knowledge-trees, this is a topic I'm interested in currently. If you'd like to test this (or any other examples from that folder) on your own, one way is to create a new .cpp file in your project directory, copypasta the code from the original in the examples into that new project file, 
> #1
and add an additional executable in mesonbuild for the new file
> #2

>curve.cpp
```cpp
//
// "$Id$"
//
// Curve test program for the Fast Light Tool Kit (FLTK).
//
// Copyright 1998-2015 by Bill Spitzak and others.
//
// This library is free software. Distribution and use rights are outlined in
// the file "COPYING" which should have been included with this file.  If this
// file is missing or damaged, see the license at:
//
//     http://www.fltk.org/COPYING.php
//
// Please report all bugs and problems on the following page:
//
//     http://www.fltk.org/str.php
//

#include <FL/Fl.H>
#include <FL/Fl_Double_Window.H>
#include <FL/Fl_Hor_Value_Slider.H>
#include <FL/Fl_Toggle_Button.H>
#include <FL/fl_draw.H>

double args[9] = {20, 20, 50, 200, 100, 20, 200, 200, 0};
const char* name[9] = {"X0", "Y0", "X1", "Y1",    "X2",
                       "Y2", "X3", "Y3", "rotate"};

int points;

class Drawing : public Fl_Widget {
  void draw() {
    fl_push_clip(x(), y(), w(), h());
    fl_color(FL_DARK3);
    fl_rectf(x(), y(), w(), h());
    fl_push_matrix();
    if (args[8]) {
      fl_translate(x() + w() / 2.0, y() + h() / 2.0);
      fl_rotate(args[8]);
      fl_translate(-(x() + w() / 2.0), -(y() + h() / 2.0));
    }
    fl_translate(x(), y());
    if (!points) {
      fl_color(FL_WHITE);
      fl_begin_complex_polygon();
      fl_curve(args[0], args[1], args[2], args[3], args[4], args[5], args[6],
               args[7]);
      fl_end_complex_polygon();
    }
    fl_color(FL_BLACK);
    fl_begin_line();
    fl_vertex(args[0], args[1]);
    fl_vertex(args[2], args[3]);
    fl_vertex(args[4], args[5]);
    fl_vertex(args[6], args[7]);
    fl_end_line();
    fl_color(points ? FL_WHITE : FL_RED);
    points ? fl_begin_points() : fl_begin_line();
    fl_curve(args[0], args[1], args[2], args[3], args[4], args[5], args[6],
             args[7]);
    points ? fl_end_points() : fl_end_line();
    fl_pop_matrix();
    fl_pop_clip();
  }

 public:
  Drawing(int X, int Y, int W, int H) : Fl_Widget(X, Y, W, H) {}
};

Drawing* d;

void points_cb(Fl_Widget* o, void*) {
  points = ((Fl_Toggle_Button*)o)->value();
  d->redraw();
}

void slider_cb(Fl_Widget* o, void* v) {
  Fl_Slider* s = (Fl_Slider*)o;
  args[fl_intptr_t(v)] = s->value();
  d->redraw();
}

int main(int argc, char** argv) {
  Fl_Double_Window window(300, 555);
  Drawing drawing(10, 10, 280, 280);
  d = &drawing;

  int y = 300;
  for (int n = 0; n < 9; n++) {
    Fl_Slider* s = new Fl_Hor_Value_Slider(50, y, 240, 25, name[n]);
    y += 25;
    s->minimum(0);
    s->maximum(280);
    if (n == 8)
      s->maximum(360);
    s->step(1);
    s->value(args[n]);
    s->align(FL_ALIGN_LEFT);
    s->callback(slider_cb, (void*)(fl_intptr_t)n);
  }
  Fl_Toggle_Button but(50, y, 50, 25, "points");
  but.callback(points_cb);

  window.end();
  window.show(argc, argv);
  return Fl::run();
}

//
// End of "$Id$".
//```

>meson.build
```cpp
project('fltk_test', 'cpp')

add_project_arguments('-std=c++2a', '-Wall', '-Wextra', language: 'cpp')

cxx = meson.get_compiler('cpp')
fltk_dep = cxx.find_library('fltk')

executable('fltk_test', ['main.cpp', 'fluid_test.cpp'], dependencies : fltk_dep )
executable('curve_test', 'curve.cpp', dependencies : fltk_dep )```

Then select the ''curve.cpp'' tab in Juci, and build (ctrl+enter). 
> #3

Play around with all the settings (and even the code in the file. I find it fun to watch the way the curves change and interact.

# 56
OK, we're going to set up a C++ testing framework on our RaspberryPis now.

There are a number of these frameworks out there for C++, but Catch2 is the simplest one to use for this language, and one of the most powerful ones as well. It's really well thought out tbh.

Go to https://github.com/catchorg/Catch2 and have a look around the repository. When you're ready, go ahead and clone the repo locally:
```cpp
cd _repo
git clone https://github.com/catchorg/Catch2.git```
> #1

There are two files we'll be using for our projects to enable testing. They are named ''catch_amalgamated.hpp'' & ''catch_amalgamated.cpp'' and located in the Catch2/extras/ directory:
> #2

That's about it. You'll be copying these two files into each of your project's directories and using them from there.

# 57
OK, so there's a search utility that's been created for us and it works with the JSON files archives of /robowaifu/. We'll get that set up to work on our RaspberryPis too. First, download this file:
https://files.catbox.moe/tmu6qr.7z

Open ''File Manager'', then drag the downloaded zip from above over from the desktop and into a project parent folder. In my case that's /home/pi/_prj/
> #1

Right-click on the file and choose ''Extract Here''. This will extract two separate files, the original code files archive, and a SHA256 sum file you can verify it's integrity with. Now open a terminal and change directories to where the files are. Execute this command now:
```cpp
sha256sum -c waifusearch-0.1f.tar.xz.sha256sum```
If everything's OK, you'll get this response:
```cpp
waifusearch-0.1f.tar.xz: OK```
Now you know the original archive is untampered with, you can extract it too now. You'll get a new directory named ''waifusearch-0.1f'', and you can delete the archive and checksum files anytime now.
> #2

We need to install a new build dependency on your RPi machine first before proceeding (ofc we presume you've already followed along with us ITT for everything else needed here). Start Synaptic ''([RPi Menu] > Preferences > Synaptic Package Manager)'', and search for 'jsoncpp' . You'll see a result named '''libjsoncpp-dev library for reading and writing JSON for C++ (devel files)'''. Right-click it and choose ''Mark for Installation'' then choose 'Apply' (the little paper airplane). Alright, now you're all set to build ''waifusearch'':
> #3

Go to the terminal and cd into the new directory. From there issue the command:
```cpp
meson build```
This will configure the new project as a ''Mesonbuild'' one, and configure it properly from the already-included ''meson.build'' file. During this configuration, Meson creates a new build directory for you. In this case it's named 'build' (after the named parameter argument ''build'' that you passed).
> #4

Fire up Juci, open the new project folder ''File > Open Folder'', and build the code (ctrl+shift+enter). After about a minute or so, you should see a successful message at the bottom of Juci's embedded terminal emulator (you can ignore all the notes from the old g++ version):
```cpp
[2/2] Linking target waifusearch.```
> #5

OK, you're all set. ''waifusearch'' is built and you're ready to use it from your RPi. We'll cover some examples in the next post.

# 58
>>8026
Now go back into the terminal and make sure you're cd'd into the ''waifusearch-0.1f'' directory. From there, issue this command to run the new executable you just built in the previous post:
```cpp
build/waifusearch```
In a few seconds, you'll see the search prompt. Now, just type in any words you want to look for on /robowaifu/ . For example, here's the search for the phrase 'clone the repo locally':
> #1

This gives us two results. The first one, under the ''ORDERED'' category, is from a post just a couple up ITT. BTW, 'ordered' just means that exact set of words in your search phrase were found ''& in that exact __order__''. The second result, under the ''UN-ORDERED'' category, includes all those words too, just not in that exact order. It's all the way over in the /meta2 thread. 

You probably already noticed that waifusearch defaults to showing ''crosslinks'' in it's results list. This is so it will be easy for you to copypasta these results here onto /robowaifu/ , and have them work directly for everyone else automatically (for example, there is a search for 'Sophie' posted in the ''Library'' thread >>7997).

You can change this to instead show full hyperlink URIs, which you personally can then copypasta into your browser instead.

To do this (just for now) you have to change a single flag inside the codefile ''main.cpp'' and rebuild the program to switch modes. Quit ''waifusearch'' (the letter 'q' to quit), go back into Juci, open the main.cpp file and scroll down until you find the variable named ''make_crosslinks'' (~L48) , and change it from being 'true' to 'false'
Build again (and again, you'll see the '[2/2' linking success message when it's completed).
> #2

Then return to the terminal and rerun the program, and now waifusearch will show you the hyperlinks in it's results instead.
> #3

In the future, the plan is to provide several arguments to change the behavior of waifusearch, and the the crosslinks/hyperlinks setting will be one of them. Well, I hope you managed to successfully get the search tool set up on your RaspberryPi Anon. If you find anything interesting using it, be sure to post it somewhere in a good thread for us!

BTW, the OP of the ''Library'' thread will occasionally have new updated JSON archives available. If you see a new one sometime, you can download it, then extract the resulting JSON out into the ''all_jsons'' subdirectory of your project directory. This will update waifusearch's information. Simply restart the program afterwards and you'll be on the the latest data using that new archive.

There are a lot of other potential plans for the tool in the future, but this should be enough for you to go on with for now Anon. Please ask me any questions or let me know if you have any issues with the program ITT, thanks.

Cheers /robowaifu/ RPi Anons.

# 59
>>8027
>example waifusearch for 'Chobits Chii' , to demonstrate copypasta'ing searches here on /robowaifu/ (use codeblocks for good formatting Anon):
```cpp
 search:  Chobits Chii

                  ORDERED:
                  ========
   THREAD SUBJECT                      POST LINK
Early Business Ideas               >>3148    @ch: ~170

                  UN-ORDERED:
                  ===========
   THREAD SUBJECT                      POST LINK
(Robo)Waifu personality thread     >>468     
   "                               >>2056    
Batteries & Power                  >>788     
Electronics General                >>843     
Speech Synthesis general           >>5530    
   "                               >>5532    
Robowaifu Propaganda and Recruit   >>2792    

' chobits chii '  [1 : 7] = 8 results```

# 60
>>8026
OK I've pushed a new version up to catbox, v0.1g
''waifusearch'' searching tool (latest version) >>8063

# 61
>>8064
==AUGGGGH.== :^)
'''Quick hotfix: '''

For some reason at the last minute I failed to add a using statement that keeps this version from building on the RPi. In the file ''main.cpp'', add this using for duration_cast:
```cpp
using std::chrono::duration_cast;```
>
Then you can build. My apologies RPi bros, this little patch will be in the next rev.

# 62
>>8065
New push today. Includes the little using fix, but also includes CLI argument parsing **finally :^)**
>>8103

# 63
'''waifusearch v0.1j''' >>8337

# 64
OK, some Anons wanted to set up ''BUMP'' for downloading /robowaifu/ and some other boards. One thing I neglected before when I originally wrote it was to support building it on the RaspberryPi. I've fixed that now. Note: Many boards are at least 1GB in size when downloaded. Lots of pics, video, pdf files, etc. For example, /robowaifu/ is currently ~2.3GB in size.
>tl;dr 
Make sure you have either plenty of storage on your basic RPi MicroSD, or use a big pendrive in a USB port for downloading the board data onto.

1. We're presuming you're already following along ITT and have set up your RPi for building C++ code, building and running waifusearch, etc. While none of these things are necessary to building and running BUMP, these instructions presume you have. So if you still have unmet dependencies, etc., b/c you're only setting up this program, then you'll need to look up higher ITT to find the instructions, etc. Nothing too complicated. And ofc, some things will be different if you're running on a different flavor of Linux. YMMV, but as long as you can meet the basic dependencies then you should be good to go.

2. That being said there are two additional required dependencies, and one optional dependency. The first two are the developer libcurl library straight from the RPi's repo. The second is the curlcpp library which you'll need to download from their SJWhub repo and build/install it locally. The last, optional, one is torsocks just in case you want to hide your power level on your local network/ISP, etc. **You '''are''' hiding your power level concerning anything you do online (particularly on IBs), aren't you Anon? :^)**. It also comes from the RPi's official repos.

3. I'd say you should go ahead and update/upgrade your RPi install first things first Anon. This can help make sure you have everything on your system patched first. Open a terminal and run an upgrade from the repos. (You should probably be doing this regularly, btw.)
```cpp
sudo apt-get update && sudo apt-get upgrade```
4. Let's go ahead and set up libcurl (I'll also add torsocks for myself). Open Synaptic and search 'libcurl' , and mark ''libcurl4-openssl-dev'' for installation.
> #1 #2 #3

5. Clone the curlcpp repo locally.
```cpp
git clone https://github.com/JosephP91/curlcpp.git```
> #4
-Build/install it with the CMake/Make dance.
```cpp
cd curlcpp/ && mkdir build && cd build
cmake -DCMAKE_BUILD_TYPE=Release ..
make -j2
sudo make install```
> #5

# 65
>>8769
1. Alright, now we can go ahead and download the updated BUMP software for today. You should check the signature of the archive file first, then again extract the codefiles themselves somewhere. I keep my software work in a ''_prj'' directory off my home dir. But (as mentioned above) if you need to use a different drive to store files onto, then I'd recommend you extract (or move) BUMP onto that same drive somewhere since BUMP stores all it's downloads inside it's own directory. 
>note: I plan to change that requirement for ''Bumpmaster'', to allow better flexibility for storage, etc., but for now just put the codefiles on your intended storage drive.

>version.log
```cpp
210301 - v0.2e
--------------
-add support for building on RaspberryPi
-add build notes inside meson.build file
-add AlogSpace onion to .sites.config
-various minor comment cleanups```
https://files.catbox.moe/kigqqd.7z
```cpp
49f53c2658c50e00a56d20d0e7299809eccae67d1ac7329cfe1891dfd45e67a8 BUMP-0.2e.tar.xz```
2. Open a terminal in the extract directory and tell mesonbuild to configure this project:
```cpp
meson build```
> #1
-Now you can build it.
```cpp
cd build && ninja && cd ..```
> #2

3. OK, you're all set. BUMP is now built and ready to download any board from any site listed in it's ''.sites.config'' file. So to start off with, let's download AlogSpace '''/ck/''' (since why not?) I'm going to access the hidden service via torsocks on my machine.
```cpp
torsocks -i build/bump bhlnasxdkbaoxf4gtpbhavref7l2j3bwooes77hqcacxztkindztzrad.onion ck```
> #3
>Note: If you aren't using BUMP over Tor, then you can just use the normal address and omit the ''torsocks -i'' prefix from the command. ie, ''build/bump alogs.theГунтretort.com ck''

4. Once everything's finished downloading you can run it again, and BUMP is smart enough after the initial big dump to download only the new stuff that's changed since your ''last'' download. For example, re-running the previous command indicates nothing's changed yet:
> #4

5. If you want to download other boards using BUMP -- /robowaifu/, say :^) -- then simply use the correct ''sitename boardname'' suffix to the terminal command. For example:
```cpp
torsocks -i build/bump bhlnasxdkbaoxf4gtpbhavref7l2j3bwooes77hqcacxztkindztzrad.onion robowaifu```
> #5

Hope that's got it all worked out for you Anon. As always, just ask ITT if you get stuck anywhere. Cheers.

>===
-''add latest version.log entry''

# 66
>>8769
Thank, just build it. The ... behind the cmake command should be ../ for the path, following your instructions.

# 67
>>8772
Great, well done. Building worked.
For the sake of completing the turorial, in case you make a textfile out of it: In point 2/> #1. One needs to create a build folder again, go into it, then use meson < path>, then call ninja. Obvious for experinced users, but I needed a moment to try stuff out.
Also the .sites.config file needs to be copied into the build folder to work. Actually, it needs to be in the current working dir. Calling Bump from a folder /Backups/ requires the file to be in that folder.

Testing it after building... Sorry, it failed. You might have choosen the naive approach when it comes to downloading files. It assumes if it started the download, that it worked? My backup of the board has 10.9 MB and it tells me that's all when restarting it. My connection very shacky, so it skipped a lot.

# 68
>>8863
Hmm. If you'd care to, maybe you can try again from scratch (w/o DL'ing again ofc) and take captures of the terminal at each step? 

The steps in '''2.'''
```cpp
meson build```
```cpp
cd build && ninja && cd ..```
are explicitly crafted that way in particular.

The 'meson build' command will call the build system ''mesonbuild'' and instruct it to both create a subdirectory named 'build', and also to configure it as a proper build directory for the project. You could just as easily call 'meson foo' and it would still work just as well, but 'build' is the canonical folder name.

The following three-step command is also specific:
-'cd build' changes directories down into the new mesonbuild-created directory.
-'ninja' calls the ninja build program (which needs to be run inside the mesonbuild's project build directory). When it completes, it will leave a new, compiled executable in that directory named '''bump'''.
-'cd ..' jumps back up to the project directory after the build, which is where the program expects to run from.

Which brings us to the step '''3.''' executing the program. The command (just as an example):
```cpp
build/bump anon.cafe comfy```
also has three parts, all of them important:
-'build/bump' tells the shell to look down into the 'build' directory and find an executable there named 'bump'. The BUMP program itself, however, expects to be called from the directory you're currently in (the project directory) again b/c of the hard-coded directory layouts. Thus the ''directory/program'' form of the command.
-'anon.cafe' is the site name BUMP will lookup online, and use it to find the board's contents, which in this example is:
-'comfy'

I realize this can all be a little confusing at first, but once you've run the program a few times, it becomes 2nd-nature. I have a big script I call from my crontab which downloads ~50 boards now, basically automatically.

So yeah, I'd suggest you start over perhaps, and capp screens of each step along the way and then post those here (in order) if you have issues again. Cheers.

# 69
>>8872
One more thing:
==YOU ONLY HAVE TO BUILD THE PROGRAM ONCE!==

It just dawned on me that newcomers might think they have to do all this every.single.time. heh. :^) 

After the program has been built (once), thereafter you just call it like any other, passing the specific ''sitename'' ''boardname'' arguments for each board you might want to archive. (The currently-supported sires are listed inside the ''version.log'' file.)

# 70
>>8872
Ah, I didn't know the meson build would create the dir. I tend to just look vaguely at things. I also overlooked that the line with the two ampersands were a legit Linux command line, despite doing this myself every day. Lol.
I'm calling Bump from some dir where I want the backups to be, not from the dir of Bump itself.
I don't know what the best way would be to solve the not downloaded file problem. On one hand I'm glad that you might even not have a library that reads files from the disk in you project, but checking if a file would be there, might make the most sense that way.

# 71
>>8877
>I'm calling Bump from some dir where I want the backups to be, not from the dir of Bump itself.

No, that's perfectly OK, but in that case I would simply copy the build compiled executable from the build directory to wherever you want to run it from in that case. There's no reason the BUMP executable has to reside in any particular directory.

>I don't know what the best way would be to solve the not downloaded file problem. On one hand I'm glad that you might even not have a library that reads files from the disk in you project, but checking if a file would be there, might make the most sense that way.
Please share the message or a screen capp.

# 72
>>8878
>in that case I would simply copy ''or symlink'' the build compiled executable*

# 73
>>8878
Ah, now I see the problem. We misunderstood each other. I meant the .sites.config file needs to be in the folder where I'm calling Bump from. It seem not to look in the build folder, or wherever it resides but in CWD.

# 74
>>8882
Ah that's true. I'd suggest you copy both .sites.config (holds all the site configuration data in a JSON) + the bump executable into whatever folder you want to store the data in. Then it will be:
>from whatever data directory:
```cpp
./bump anon.cafe comfy```
or whichever ''sitename boardname'' (like robowaifu).

Apologies about the confusion. Hopefully the new approach for ''Bumpmaster'' will be simpler to use in the future.

>===
-''edit example command''

# 75
>>8883
No problem, no apologies required, I'm glad to have it. Just wanted to mention it, in case someone runs into the same problem and also as a bug report.

# 76
>>5270
==Update==
The developers of Juci have made a big update that now takes advantage of ccache to speed up the compilation process if parts of a project have already done. I recommend you install ccache under ''Synaptic''
>
and also follow the steps to update Juci and rebuild it.  >>5346

# 77
>>8863
I renamed a file named .archbot.config to make it downloading the files again. It might only redownload the catalog.json anyways. Need to do more testing. Can't really imagine that this Curl library cant be given some attribute to not redownload files which have the same name and size (maybe hashsum).

# 78
>>9376
So, by doing this renaming you're basically telling BUMP to reconstruct the entire archive from scratch. This is because the program explicitly checks this .archbot.config file (named in honor of the very earliest version of the tool '''''Arch'''ive '''Bot''''' >>610) to find this archive's configuration setup. If it can't find that exact filename, it presumes this is a new archive that anon is setting up. Note: However, since this is ''not'' a new setup, it simply redownloads & rechecks all the JSON files from the board (potentially downloading any new files that haven't been yet) during this 'new setup' process, overwriting the previous JSONs (& simply reusing the already-created, custom-named thread directories within the archive's directory tree). 

Rather than going to all the trouble of doing this, if you want to re-download all the JSONs you can instead simply pass an 'undocumented' flag '''1''' at the end of the statement to do this:
```cpp
build/bump anon.cafe comfy 1```
This ''force_recheck'' flag tells BUMP to redownload & recheck all the board's thread's JSON files.

Note: The '''catalog.json''' is the single file that will __always__ be downloaded with every invocation of BUMP, since it contains all the information needed that tells the program which (if any) threads have been, well, ''BUMPed''. :^)

As far as your other comment about checking the status of a file before attempting to download, yes. Both HTTP/2 & cURL both support this type of tag in the header (however a website may or may not provide it). I simply hadn't gotten around to addressing it since the algorithm already did all the required 'update-needed' checks by simply using the board's catalog JSON file itself. CBA to change it ATP, but it's something I'm likely the adopt in the new ''Bumpmaster'' program instead.

>tl;dr
Just put a '1' on the end of the command if you need a re-check, Anon.

# 79
>>9382
>Just put a '1' on the end of the command if you need a re-check, Anon.
Okay, I'll try that. It's not urgent, if there are others using the program to make a backup of the board. I can wait. 
Another thing: Which files would I need to copy into Waifusearch, to use the updated jsons for search. I know you're planning to join these anyways, just wondering if I can do it manually or with a small script on my own. Again, I'm not trying to urge anything here. Not that important.

# 80
>>9396
>Which files would I need to copy into Waifusearch, to use the updated jsons for search.
Well, here's my crappy shell script I use for it.
>cp_jsons.sh
```cpp
#!/usr/bin/env bash
unalias cp
cd /home/johnny/_prj/BUMP-0.2e/
torify -i build/bump alogs.theГунтretort.com robowaifu 
cd alogs.theГунтretort.com/robowaifu/
find threads/ -iname '*.json' -exec cp -f -t all_jsons/ {} + 
rm all_jsons/*_file_404s.json 
rm all_jsons/7143.json 
rm all_jsons/273.json  
cp -f all_jsons/* /home/johnny/_prj/waifusearch/all_jsons/ 
cd ..
```
>tl;dr
''All of them'' (well except the library/archive threads).

>===
-''add Bash env specifier''

# 81
>>9399
Note: I should add, I created an ''all_jsons'' subdirectory under the BUMP robowaifu archive directory once I had written Waifusearch, for just this purpose. It's not part of the base BUMP directory creation process, so you'll need to do it manually beforehand prior to running a script like this ofc.

>===
-''minor prose edit''

# 82
>>9396
>Okay, I'll try that. It's not urgent, if there are others using the program to make a backup of the board. I can wait. 
I'm not aware of anyone but myself doing so ATM. I've been presuming that you yourself were doing so Anon. It would certainly be good to have several of us doing so. Just in case something happened both simultaneously to the AlogSpace and to one of us as well...it could spell the end of /robowaifu/ if no one else was there to step up with a recovery.

'''Again, as mentioned before here, if this ever happens, then one of you approach the Administration of our two bunker sites with the backups and request a full restoration of the board there.'''

==Robowaifus are an idea whose time has come. A little thing like leftists and glowniggers trying to end this board isn't going to stop it now!== :^)

