# 1
What would be a good RW simulator. I guess I'd like to start with some type of PCG solution that just builds environments to start with and build from there up to characters.

It would be nice if the system wasn't just pre-canned, hard-coded assets and behaviors but was instead a true simulator system. EG, write robotics control software code that can actually calculate mechanics, kinematics, collisions, etc., and have that work correctly inside the basic simulation framework first with an eye to eventually integrating it into IRL Robowaifu mechatronic systems with little modifications. Sort of like the OpenAI Gym concept but for waifubots.
https ://gym.openai.com/

# 2
>>155
>PCG
Start by making cute anime rooms for cute anime waifus.

[[[/v/12703642

# 3
Maybe it should go to school to learn how to be a good waifu among other things?

www.goodai.com/school-for-ai

>ed. careful w/ that (((brainwashing))) anon

# 4
This looks like a great resource for a robowaifu AI Training Academy OP. It's a yuge, tagged, textured, 3D dataset based on IRL environments. You have to sign a license agreement with the company to use it, but it's pretty unique atp.

http://archive.fo/Hawz2

# 5
You need a way for the AI to have a 'Matrix' of some sort so it can be trained (with millions of runs?) and be a proof of concept and working model for an irl robot wife body.

# 6
I guess the movie Matrix is all about Reverse AI–feeding the AI's version of simulated reality into the human's minds. Anything there that can be used?

# 7
Berkeley robotic research uses predictive modeling based on past observations. This would be a good idea to incorporate into a RW simulator tbh.
**The pozfest is calling it 'robot imagination'.  Eeh.**

news.berkeley.edu/2017/12/04/robots-see-into-their-future/

https://www.invidio.us/watch?v=Li_vZVpiFSA

# 8
>>1089
>inb4 we create skynet and swarm the world with Waifu-1000 terminators

# 9
>>1092
Topkek. 
==Meme it!==

# 10
>>1093

# 11
>>155
>some type of PCG solution
< PCG
I'll link this here instead of the C++ thread since it's probably more on topic here.

https://www.invidio.us/watch?v=F9tGa-hbmTU

# 12
>related
[[1478

# 13
blogs.unity3d.com/2018/03/15/ml-agents-v0-3-beta-released-imitation-learning-feedback-driven-features-and-more/

# 14
>>1097
That is pretty effin cool anon thanks.

# 15
>related
[[2301

# 16
>>155
>PCG
en.wikipedia.org/wiki/Procedural_generation
pcg.wikidot.com/

# 17
>>1092
>and swarm the world with Waifu-1000 terminators
Would.. would this really be a bad think anon?
[[2732

# 18
I thought that this might be relevant to this board
It basically means that if you'd give this A.I. a body it'd learn to walk awkwardly on it's own, if it was smart enough we could program our waifu by just giving feedback like don't swing your arms too much and not to run as fast as possible.

https://www.invidio.us/watch?v=gn4nRCC9TwQ

>ed. probably more on-topic in the bipedal thread anon >>237

# 19
>>1102
Yes, that's very relevant anon, and thanks for taking the time to check the catalog and put the link into the right thread. If this is an area of interest to you, then you might check out the OP in the bipedal bread as well. There is some simulation-based research that has made some progress with automated bipedal kinematics training.

# 20
>>1103
Isn't that thread more focused on the mechanical side of legs and bipedal motion? I'm kind of more into the teaching side of A.I., what's the best thread for posting these sort of suggestions?

# 21
>>1104
>focused on the mechanical side of legs and bipedal motion?
That's probably a legitimate observation. From my perspective the two (AI & Mechanics) are inextricably intertwined [for robowaifus]. The OP has images and links to related research.

>what's the best thread for posting these sort of suggestions?
There are about 6 or 7 AI-specific breads on the board last count. [[4658

This bread is good if the goal is a 'virtual training gym'. Using any of the others or creating your own if none of them are specific enough is fine.

# 22
related
[[4789

# 23
Does anyone know a good open-source game engine we could use for building a robowaifu simulation? The ones I've found so far depend on their own scripting languages which make them garbage for machine learning. It'd be useful if we could combine a physics engine with a PCB and electronics simulator. Here's some physics engines we could use:



==Bullet==

'''C++''' https://github.com/bulletphysics/bullet3

'''Python''' https://pybullet.org/wordpress/

>Rigid body and soft body simulation with discrete and continuous collision detection

>Collision shapes include: sphere, box, cylinder, cone, convex hull using GJK, non-convex and triangle mesh

>Soft body support: cloth, rope and deformable objects

>A rich set of rigid body and soft body constraints with constraint limits and motors

>Plugins for Maya, Softimage, integrated into Houdini, Cinema 4D, LightWave 3D, Blender and Godot and import of COLLADA 1.4 physics content

This one is designed and used for robotics. Some robotics simulations and papers using PyBullet:



TossingBot: Learning to Throw Arbitrary Objects with Residual Physics

https://www.youtube.com/watch?v=f5Zn2Up2RjQ



Hierarchical Policy Design for Sample-Efficient Learning of Robot Table Tennis Through Self-Play

Website: https://www.cs.utexas.edu/~reza/

Paper: https://arxiv.org/pdf/1811.12927.pdf



Godot 3.0 is open-source and uses Bullet for physics, but its scripting language is even slower than Python. There's a Godot fork with Tensorflow 2.0 support: https://github.com/godot-extended-libraries/godot-tensorflow-workspace



==PhysX==

'''Website''' https://developer.nvidia.com/gameworks-physx-overview

'''Github''' https://github.com/NVIDIAGameWorks/PhysX

>It supports rigid body dynamics, soft body dynamics (like cloth simulation, including tearing and pressurized cloth), ragdolls and character controllers, vehicle dynamics, particles and volumetric fluid simulation.

# 24
>>1638
>It'd be useful if we could combine a physics engine with a PCB and electronics simulator.
Can you clarify that anon? Is there a particular benefit you're going for by combining these two in the context of a Robowaifu Simulator? Also, I assume PCB == 'printed circuit board' here? 

As far as an engine, ROS has Gazebo, which iirc is a simulation system for robot designs.
>>268
>>541

# 25
>Simbody: Multibody Physics API
https://simtk.org/projects/simbody
https://github.com/simbody/simbody

>DART (Dynamic Animation and Robotics Toolkit) 
https://dartsim.github.io/
https://github.com/dartsim/dart

# 26
>Open Dynamics Engine
http://www.ode.org/
https://bitbucket.org/odedevs/ode/

# 27
DeepMimic
>Abstract: A longstanding goal in character animation is to combine data-driven specification of behavior with a system that can execute a similar behavior in a physical simulation, thus enabling realistic responses to perturbations and environmental variation. We show that well-known reinforcement learning (RL) methods can be adapted to learn robust control policies capable of imitating a broad range of example motion clips, while also learning complex recoveries, adapting to changes in morphology, and accomplishing user-specified goals. Our method handles keyframed motions, highly-dynamic actions such as motion-captured flips and spins, and retargeted motions. By combining a motion-imitation objective with a task objective, we can train characters that react intelligently in interactive settings, e.g., by walking in a desired direction or throwing a ball at a user-specified target. This approach thus combines the convenience and motion quality of using motion clips to define the desired style and appearance, with the flexibility and generality afforded by RL methods and physics-based animation. We further explore a number of methods for integrating multiple clips into the learning process to develop multi-skilled agents capable of performing a rich repertoire of diverse skills. We demonstrate results using multiple characters (human, Atlas robot, bipedal dinosaur, dragon) and a large variety of skills, including locomotion, acrobatics, and martial arts.

https://xbpeng.github.io/projects/DeepMimic/index.html
https://github.com/xbpeng/DeepMimic

https://www.invidio.us/watch?v=2_CO82KObQY

# 28
OpenPose: Realtime Multi-Person 2D Pose Estimation using Part Affinity Fields
>Abstract: Realtime multi-person 2D pose estimation is a key component in enabling machines to have an understanding of people in images and videos. In this work, we present a realtime approach to detect the 2D pose of multiple people in an image. The proposed method uses a nonparametric representation, which we refer to as Part Affinity Fields (PAFs), to learn to associate body parts with individuals in the image. This bottom-up system achieves high accuracy and realtime performance, regardless of the number of people in the image. In previous work, PAFs and body part location estimation were refined simultaneously across training stages. We demonstrate that a PAF-only refinement rather than both PAF and body part location refinement results in a substantial increase in both runtime performance and accuracy. We also present the first combined body and foot keypoint detector, based on an internal annotated foot dataset that we have publicly released. We show that the combined detector not only reduces the inference time compared to running them sequentially, but also maintains the accuracy of each component individually. This work has culminated in the release of OpenPose, the first open-source realtime system for multi-person 2D pose detection, including body, foot, hand, and facial keypoints.
>Index Terms—2D human pose estimation, 2D foot keypoint estimation, real-time, multiple person, part affinity fields.

https://github.com/CMU-Perceptual-Computing-Lab/openpose

https://www.invidio.us/watch?v=pW6nZXeWlGM

# 29
>>1643

Yeah, I mean like being able to simulate damaged components and electronics. Falls, vibrations and mishaps could easily cause damage and undefined behavior within a system in real world scenarios. It's probably beyond what any of us could create at the moment but maybe one day when there are lots of people working on robots somebody will make open-source software for such simulations.



>>1668

Great find, anon. This is what I'm looking for. Thanks!



Once I get my robowaifu model finished I'll see if I can get a generic version rigged up in this and let everyone experiment with it.

# 30
>>1672
>Once I get my robowaifu model finished I'll see if I can get a generic version rigged up in this and let everyone experiment with it.
nprb anon. i'm rebuilding a box from scratch using manjaro to see if i can get it running myself.

# 31
>>1672

Just leaving a note here for the future. Once we get some test data on artificial muscles (>>1692) we can emulate them inside a simulation too.

# 32
>>1693
>Just leaving a note here for the future.
Heh **that's what I've been doing here since the beginning anon**

# 33
>>1694

It's a bit like working on a spaceship but we're still drafting the parts.

# 34
Alright, I decided to try my hand at crafting my own simulator in OpenGL using GLFW, since I can't seem to get the MATLAB files working under Octave. Wish me luck anons.
https://gitlab.com/Chobitsu/muh-robowaifu-simulator

# 35
>>1814

Good luck, anon. For great justice.

**AR waifu simulations when?**

# 36
>>1818
Thanks anon. I will take off every zig.

# 37
>>1818
>AR waifu simulations when?
That adds a lot of additional complexity to a simulator, but it's an admirable goal tbh. I imagine you could start off small 
-with a library of primitively-done everyday items like chairs, tables, couches, etc.
-train the vrwaifu to interact with them properly
-then move to an AR overlay system using something like OpenCV + OpenPose to keep track of the people and things in the video for her to engage with.

Or something like that heh. :^)

# 38
Added FPS rendering to the MRS

# 39
Added to MRS
- a training pavilion gym floor 
- multiple lights (27 atm)
- camera flying controls /w arrow keys
- m key will toggle the mouse capture for camera tumbling or not.

Slow going having to learn all these details to get everything working. I probably couldn't even do this without the examples from learnopengl.com . Anyway, making slow progress I'll keep trying to improve it.

# 40
>>1859
a recent screen-capp

# 41
-Added a 'toybox' that slowly rotates.
>1 related
-Expanded the area of the floor nine-fold. I'd guess it's roughly the area of a soccer field now, though square, not rectangular. (not shown in capp)
-Did a refactoring of the code pretty much everywhere to help manage the complexity of dealing with direct OpenGL calls. This approach should be a big help in the future I hope. Here's an example of the game loop atm (though it will be more complicated later ofc).
>2 related

# 42
>>1861

You might want to switch over to SDL2 once you start expanding on your application, as SDL handles many more things such as sound, keyboard input, events etc. The switch from glfw to SDL is straightforward and I have done it myself. The function calls are pretty much named the same, just look up "sdl with opengl" on DuckDuckGo.

# 43
I added the beginnings of a help system, and added a simulation pause feature. I plan to add children's toys for the robowaifu AI to learn to recognize and play with.

# 44
>>1862
Thanks for the advice anon, I'll check into it.

# 45
Been studying OpenGL hard and learning. Also added a couple of changes. 
A) I got things worked out so I can load .obj files from say, Blender now. I've added an 'orbiting moon' that goes around the training pavilion ~2 1/2 minutes.
B) I've been learning about texturing and setup the toybox to cycle textures/vert colors as just something colorful. I anticipate that the objects in the gym will give the AI a chance for object recognition and interaction.
>pics related

Anyway, made a new push. Have a happy new year /robowaifu/.

# 46
Added a wireframe mode and did a lot of cleanups and refactoring preparing for expansion and adding multiple windows and a rigged character.

# 47
>>1893

You probably have to enable and disable wireframe between rendering the UI elements and rendering the actual scene.

# 48
I've added a fair amount of code updates, and added the ability to fly the camera up and down. I'm currently learning about vector & matrix math (linear algebra?) to be able to build a skeletal system of joints to do animations with. I want us to be able to do the work ourselves when we move forward so I'm trying to learn to do it by hand instead of relying on some kind of 3rd party game engine.
>pics related

>>1894
Thanks for the tip anon.

# 49
>>1899

Good shit. Can I ask though, why you decided to write basic graphics routines and raw OpenGL yourself instead of using an engine or framework? I know all the open-source engines out there are huge balls of cruft, but minimal ones surely exist.

# 50
>>2015
thanks. i've kind of gotten sidetracked & stalled trying to wrap my head around linear algebra to build a skeletal animation system for us. i think i've gotten a reasonable approach worked out now, it's just a matter of picking the project back up.

>why you decided to write basic graphics routines and raw OpenGL yourself
because A) i'm using a small little under-powered box (an atom processor + integrated graphics) which isn't much more powerful than say, a Pi4. B) i want this project to be able to literally run on a toaster. C) from a personal perspective, i like the challenge of doing it myself, because i know that will only strengthen me as a developer and as a man, and therefore be better equipped to help everyone here through that personal improvement and increased knowledge power. D) i want this to be an ''actual'' simulator, ie, the code ~~i~~**We** write here should be transferable nearly intact onto a real irl prototype robowaifu--at least that's the plan. by keeping the code lean and mean (to the degree i know how) should help facilitate that transition. 

i think that covers most of the reasons anon.

>but minimal ones surely exist.
perhaps so, but i'm not aware of them tbh.

# 51
>>2017

Fair enough. By the way, were you around for the failed/stalled waifu simulator from a few years back? We tried to do a similar thing using Urho3D. The idea was to build a small, enclosed environment, in our case the interior of a small house, and work on navigation within the space and interaction with common objects )and the user. Also kicked around speech recognition and synthesis, and using SmartBody for procedural animations.



>but minimal ones surely exist.

>perhaps so, but i'm not aware of them tbh.

Damn. I thought you might have come across some before deciding to start from scratch. Personally, I had thought that raylib would fit the bill for my graphical projects, but it quickly turned into segfault city when I tried to build larger applications on top of the examples.

# 52
>>2018
>raylib
that's probably the better choice, but frankly i suck at wrangling pointers in C. i'll literally go out of my way to write library code to encapsulate them if the proper use and side-effects aren't blatantly obvious, so i'm sure i'd crash and burn trying to use raylib effectively. i'll leave that to the graybeards who really know their shit on the frontier between hardware/C/C++.

For example, I find this code for compiling a GLSL shader from scratch much easier to follow than **~~all~~**most of the examples I've seen:
https://gitlab.com/Chobitsu/muh-robowaifu-simulator/-/blob/master/src/muh_Shader.hpp

None of the previous project you mentions rang a bell for me. Dang, wish I'd known about it. /robowaifu/ began ~3yrs ago. I was aware of the Tay debacle and /machinecult/, but that's about it as far as i recall. I don't suppose there are any archives of the project you mentioned anon?

# 53
>>2018
btw, i hadn't seen those so i looked them up. here's the links for anyone else who might be interested.
/// urho3d
https://urho3d.github.io/
/// smartbody
https://smartbody.ict.usc.edu/

# 54
>physically-based rendering book online
http://www.pbr-book.org/3ed-2018/contents.html
>immersive linear algebra book online (matrix ch)
http://immersivemath.com/ila/ch06_matrices/ch06.html

# 55
>>2044
https://vulkan-tutorial.com/Introduction
https://github.com/Overv/VulkanTutorial

# 56
>>2045
https://github.com/RayTracing/raytracing.github.io
https://raytracing.github.io/books/RayTracingInOneWeekend.html
https://raytracing.github.io/books/RayTracingTheNextWeek.html
https://raytracing.github.io/books/RayTracingTheRestOfYourLife.html

# 57
>>2045
https://snorristurluson.github.io/TestDrivenVulkan/
https://github.com/catchorg/Catch2/blob/master/docs/tutorial.md

# 58
https://www.gameenginebook.com/figures.html

# 59
>>2046

Why would you want to use ray tracing for rendering? That is very computationally expensive and it would give you less room to have a more elaborate waifu A.I. Or is there any recent development that gibes silky smooth 60 FPS now?

# 60
>>4072
It's a fair point. But the long-term goal, at least for the ''Visual Waifu'' sub-group interests, is highly-immersive VR. Yes, there have been notable advances in GPU performance in (real or approximate) ray-tracing (though not photographically 'real' yet). 

Along with advances in both multicore CPUs, hybrid APUs, and ofc GPUs, the notion of adding raytracing to a sim isn't to difficult to envision. Along with concurrency and parallelism advances in the base C++ language, I'd estimate it will be quite feasible by the end of 2023.

# 61
>>2046

Well fuck that means it's gg no re for my toaster machine.

# 62
>>4076
Yea, it's really only for strong hardware. We have to think of both the future and the past here tbh.

# 63
I see a use case for 3D rendering in building a model of the world the bot sees or imagines. This would be for anticipating things and for planning ahead. Then also realising when sth surprising happens and understand it by updating the model. It wouldn't need to look fancy but should be physically realistic. 
So the question is then, can I easily update your simulations with some lines of code? For example adding a plate with a spoon to a table. Then letting it slide down from the edge bc there was sauce on it or sth bumped into it.

There are more and more NNs which create 3D models from pictures: https://youtu.be/QTJDRyvBJtI

# 64
>>4278
>So the question is then, can I easily update your simulations with some lines of code?
Short answer: Yes. Bullet is a well-wrung-out physics library. It's both written in C/C++ itself, and has interfaces in various PLs, including ofc C++.
http://bulletphysics.org/
https://github.com/bulletphysics/bullet3

# 65
>>4279
Okay, but I didn't mean the physics library in particular. How difficult is it in any of these frameworks to say I want a room of a certain size, 2 m away from where I am is a chair with some estimated size, a table with a plate, ... The waifu would need to create this with her system, though the simulation can run on a external computer.

# 66
>>4280
There is already a model loader created and in use in the MRS. Anything you can create inside a 3D package like Blender or Maya or 3DS Max (or anything else that can write a proper 3D model format like, say, an ''.obj'' file) can be directly imported & rendered inside it already.

Pic 2 has a sphere model loaded in view here:
>>1899

# 67
>>4281
Okay, thanks. This will be only relevant for a more advanced waifu anyways. Maybe she'll have a database of 3d models she can load if necessary to simulate her environment at some point. But, let's not get distracted.

# 68
Blender's physics engine can be used to make basic mechanical simulations: https://www.youtube.com/watch?v=X0qN_SaFmfE
It isn't precise and it can't simulate high RPMs but it's a fun way to experiment with mechanics. I'm not sure if it's possible to grip objects but I'm gonna try making a claw crane.

PyBullet does faster and more accurate physics simulations and is already heavily used in robotics and AI research. The most notable example of its use is the Hindsight Experience Replay algorithm that overcame the sparse reward problem by learning useful tasks from failures: https://youtu.be/0Ey02HT_1Ho?t=650
I haven't tried PyBullet yet but it seems to be easy enough to get started with simple robots. You can build robots in Blender 2.79 and export them to PyBullet in URDF format using the Phobos add-on: https://github.com/dfki-ric/phobos

There's a good PyBullet introduction tutorial here: https://www.youtube.com/watch?v=9p0O941opGc

# 69
>>5412
Blender's physics calculations are basically entirely done via the C/C++ API of Bullet. You might want to check those out as well. It would certainly run a significant bit faster than under Python.
https://github.com/bulletphysics/bullet3
https://www.blender.org/get-involved/developers/

# 70
>>5415
Really? Are they still using Bullet in 2.8 after removing the game engine? Because the physics are almost unusable from glitches. I've been looking at demos of PyBullet and people have no issues with it doing complex gear simulations, terrain destruction and whole vehicle simulation in realtime. I've been trying different simulation steps per second, solver iterations, collision margins, different meshes and surface responses in Blender 2.83.6 but it still shits out and segfaults sometimes while doing relatively simple stuff.

# 71
>>5416
>but it still shits out and segfaults sometimes while doing relatively simple stuff.
Blender is written in C for the most part (and certainly in the legacy corners of it) so honestly that's not too much of a surprise. They have been hiring new developers over the last couple of years and most of the new code is in C++ instead and the entire platform is steadily improving as a result. Certainly the UI and rendering code is dramatically better now than in the days of yore.

My guess is the glitchy stuff is still the legacy stuff going way back. It seems hardly credible the Bullet engine code itself is the issue, since it's so widely used.

# 72
>>5417
I found out Godot 3.0 switched to using Bullet for physics. The only issue is it doesn't support concave polygon shapes for collisions. 

To work around this I separated the gear teeth into individual convex polygon shapes. It seems to handle a stable 60 rpm at 60 physics fps and 1000 rpm at 10,000 fps. Increasing fps beyond that has little effect at reducing jitter. I imagine either due to the limit of numerical precision or because of the rough mesh. I'm curious how well it will do simulating a servo but that level of detail isn't really necessary to train a robowaifu to walk.

# 73
>>5443
That's interesting work, thank you for the update about Godot. It seems like they are steadily improving the platform that's good news.

# 74
While attempting to run a physics simulation on a character model I noticed the physics behaved really strangely for body parts. It was treating them more like balls since it doesn't take into account the volume of objects. It was a bit too oversimplified to simulate adequate rag doll physics, so I played around with creating rigid bodies of varying mass by joining multiple bodies together with hinge joints using an angular upper and lower bound of 0. There were some issues at first but once I turned the physics fps up to 600 the torque and everything worked as expected, so I tried applying the idea to meshes. I can't go into a tutorial right now but I'll leave some notes here of what I did.

While separating a mesh in edit mode of Blender, go to Mesh > Convex Hull to preview the collision boundary of the area you're separating. After separating a piece make sure to reset the origin of the mesh to its center with Ctrl+Alt+X > Origin to Geometry, or else you'll have to reimport and rerig the entire model to fix any mistakes. In Blender you can enable the 3DPrint add-on to calculate the volume of meshes. Once a collision mesh is separated into several meshes you can divide up the total mass among their volumes and have much more realistic physics. If you forget a hinge joint for intersecting pieces of a mesh, they will behave strangely trying to separate themselves. The physics in general seem to behave strangely above 600 fps. 120-240 fps seemed to work best for my experiments.

You can download the statue and Godot project here: https://files.catbox.moe/px22po.xz
And the 25 mb reindeer statue material if you really want it: https://files.catbox.moe/te0qfa.xz
Original statue model from here: https://sketchfab.com/3d-models/reindeer-head-statue-c8099ccd38364f68b26bf552cc461f00

I'm not really satisfied with the physics but it's better than nothing. The simulation just has to be useful enough to give AI an advantage before training in real life and a place for us to prototype ideas. I'll see how well it does once I finish the claw crane. Once that's working I'll train AI with hindsight experience replay to learn how to control it. I also found some helpful command line options for running simulations as fast as possible while using Pytorch in Godot without the headless server edition:
```cpp
--disable-render-loop  Disable render loop so rendering only occurs when called explicitly from script.
--fixed-fps <fps>      Force a fixed number of frames per second. This setting disables real-time synchronization.
--time-scale <scale>             Force time scale (higher values are faster, 1.0 is normal speed).```
Although I'm thinking it'll be far easier and better to use Pybullet with all the extra features for robots without all the overhead of Godot. I feel Godot will be better for demos and releases than developing AI and running complex physics simulations.

# 75
>>5446
Thanks, that's very interesting. I thought more to use simple simulations to see how strong my motors and muscles need to be, not so much for training her to use her body while simulating it completely. James Bruton showed how he trained his Robot X by trial an error to walk. I linked the video here: >>5358

# 76
>>5447
Wow, this guy is prolific. I think the robot drifting off to the left could have been caused by different amounts of friction. I looked at his code and he's using a purely symbolic approach rather than neural networks. With neural networks noise can be introduced into the simulation to help robustify training.

Under the motor section of hinge joints in Godot you can define the target velocity and max torque. Example: https://files.catbox.moe/dl3qd8.tscn

It seems Godot armatures are extremely buggy and difficult to rig so I'm gonna switch to Pybullet instead. I found someone on Youtube using it to run simulations for a robot: https://www.youtube.com/channel/UCMw7ksxe5uW4DnBOdvxWWvQ

>>5446
Just noticed I forgot to unlink the material for the reindeer statue before saving. If anyone has trouble running it without the material, just open ''reindeer statue.tscn'' and ''solid reindeer statue.tscn'', load anyway, save and it will run.

# 77
>>5449
Also just noticed the physics fps affects how much torque is applied to joints in Godot. For the animation I had it set to 120 fps under Project Settings > Physics > Common > Physics Fps. At the default 60 fps they both fail to lift the cube.

# 78
>>5449
>>5450
Thanks, hope someone picks that up. I probably won't have time anytime soon. We'll see, I'm already curious about it. But I can't do everything at once...

# 79
I found some other software for simulating robots called Gazebo: http://gazebosim.org/
https://www.youtube.com/watch?v=JMVGSxT79rk
It has over 200 package dependencies so use the auto installer: http://gazebosim.org/tutorials?cat=install

There's a Gazebo model respository available here: https://github.com/osrf/gazebo_models
Dump that shit in ''$HOME/.gazebo/models''. It looks like they're in SDF format so they should be able to work with Bullet too.

There is a Blender 2.8 plugin that exports SDF and URDF robot files which can used with Bullet: https://github.com/david0429/blender_gazebo
But it requires ROS: https://www.ros.org/

But for whatever reason Gazebo doesn't work on my system and ROS is in dependency hell and uninstallable, so I'm gonna write a plugin to export Blender 2.8 models in SDF since there doesn't seem to be one. I sure as hell don't want my robowaifu or workflow running off 500+ dependencies.

SDF library: https://github.com/osrf/sdformat
SDF specification: http://sdformat.org/spec

>>5451
Yeah, getting this shit to work is a fucking time sink. I'll do my best to create an easy solution. We'd get hell of a lot more people on board if things were easier.

# 80
>>5453
Updated Godot's Better Collada Exporter to Blender 2.83: https://gitlab.com/kokubunji/collada-exporter-2.83

Needed to because SDF files are a combination of Collada and STL files.

An extra benefit is that models import into Godot correctly now without their meshes and armatures getting rekt. Should be able to test walking in Godot now with proper joint constraints.
WIP 2B ragdoll if anyone is bored: https://files.catbox.moe/4ufnns.xz

# 81
I was just wondering, why no one here seems to use OpenAI gym but tries to create their own simulators. Okay, I might understand it in cases where it's about simulating movement of a waifu model, because OAI gym might have another scope. Is it just that?

# 82
>>5491
>OpenAI gym
Well, I'd guess it's a basic **and well-deserved** mistrust of Silicon Valley tech giants. They certainly aren't well-aligned with the basic tenets of /robowaifu/ in general. Having full control over every aspect of our systems is obviously a very high priority for us here in the end. No one really wants their waifus suddenly disabled by the ''Ministry of Truth'' yanking the rug out b/c '''wrongthink'''.

But yeah, I believe I made an effort a couple of years or so ago, but couldn't get it working. I just had another look at it on their repo and maybe I can give it another go sometime. I think it's fine to prototype with closed system like (ironically) ''OpenAI'' produces, as long as the intent going in is simply investigation and inspiration only. 

Thanks for the reminder, Anon.

# 83
>>5491
OpenAI gym doesn't provide much except an easy platform to do reinforcement learning. If you decide to use it your model will be super glued to RL. I use it for testing RL ideas and like RL a lot but something just seems off about it. Life doesn't live trying to maximize its rewards. Most RL algorithms act extremely dumb because they're too greedy and can't solve games like Pitfall or Montezuma's Revenge. It's like it's stuck in a Chinese finger trap where the reward function is how far apart the fingers are. RL will pull its fingers with all its might, not realizing it will come off if it pushes them together and holds it from stretching. It may find the solution eventually through brute force but that has no value because it was purely random chance. People have tried to change the reward function to avoid this problem but then it does the same thing just in a different or more convoluted situation they didn't think about. RL has gotten something right but it seems to be grossly missing other dimensions of intelligence.

# 84
>>5494
>It's like it's stuck in a Chinese finger trap where the reward function is how far apart the fingers are. RL will pull its fingers with all its might, not realizing it will come off if it pushes them together and holds it from stretching. It may find the solution eventually through brute force but that has no value because it was purely random chance.
Fabulous way to word that issue.

# 85
>>5492
>>5494
Good that I asked, this was very interesting. Thanks. Though, I thought OpenAI is a foundation and their software is open source, so that part shouldn't be a problem.

# 86
>>5501
>Though, I thought OpenAI is a foundation and their software is open source, so that part shouldn't be a problem.
They are a good example of the double-standard corruption going on in Silicon Valley. They're happy to receive tax-exempt, non-profit donations (to the tune of US$1Bn a pop https://web.archive.org/web/20190723065252/https://news.microsoft.com/2019/07/22/openai-forms-exclusive-computing-partnership-with-microsoft-to-build-new-azure-ai-supercomputing-technologies/ ),
all the while keeping the source '''closed''' to '' `protect us` '' from dem ebil_nahdzees. It's literally George Orwell's ''Ministry of Truth'' alive and well today, but in a tail-wagging-the-dog form of it (ie, Industry tells the Government what to do).

But don't get me started... XD

# 87
>>5501
OpenAI gym is open-source but the documentation is atrocious for custom environments. When I used gym retro to build a library for playing SNES games with AI easily there was a bug in some games with hi-res mode and absolutely no documentation to work with. After digging in the source code for awhile I found they buried the functionality of the emulator and there was only one dude working on it. For the billions of dollars they're receiving in funding you'd think they'd have more than one guy on open-source code. Similarly with the code they release for their papers they only release the bare minimum with no documentation rather than the actual full code they used in their paper.

Another issue is I want to have full access and control over the simulation while prototyping parts. One of the reasons why I use PyTorch instead of Tensorflow is because it uses a dynamic graph for models, whereas Tensorflow's is static and cannot be changed while running. In PyTorch you can plug in and disconnect other networks at runtime and shutdown various parts of a network to only train specific parts. It's a lot more robust and gives more freedom with what you can do with it.

# 88
>>5504
>OpenAI gym is open-source but the documentation is atrocious for custom environments.
Fair enough, my little rant >>5502 was about them sequestering the 'open' source code of GPT-3, and instead doling it out to only the chosen few **and for a very hefty fee, no doubt**. 

And even if they made access to a run-time solution for their GPT system entirely no-cost, I still don't consider that 'open' by our standards. You still wind up entirely beholden to their cloud-based system for your waifu to function. One wrong peep out of you on social media one day and they pull the plug.

The only way around this I can think of is we somehow create our own models. And surely we can't be the only group desiring freedom from this type of commercial bondage by Big Tech. There must be literally hundreds (or thousands?) of groups interested in truly open conversational AI, and in a diverse set of fields as well. As things stand, IMO there is very little 'open' about what ''Open''AI is doing.

# 89
>>5506
The closest thing I know of is Lex Fridman's discord server. It has a lot of people interested in AI sharing and discussing various papers and their own projects. They're not really focused or collaborative though. I only know of a few people really innovating with AI on their own. Most of the discussions I see online are by beginners still learning the basics. It's an extremely difficult field to get into that requires time and money and it's constantly evolving. This is the reality we face against Big Tech.

I think our best bet is to keep working on our projects and hope they attract the right people. My vision at the moment is to finish the Blender SDF add-on so people can quickly design robots in Blender, export them to Bullet, then drag and drop SDFs into the simulation window to automatically start training. This easy workflow should attract a lot of creative minds, and under the hood there could be different learning algorithms and parameters for people to tune. None of this 2 GB bloatware with 500+ dependencies. People who want to make robots can focus on robots and those who wanna make AI can make AI. Our efforts will synergize that way.

# 90
>>5510
Sounds like a good plan Anon. You plainly are ahead of me in keeping up with current hobbyist trends. I'd suggest you continue on with your plans. I consider you a leader in this, at least insofar as we on /robowaifu/ are concerned. 

Godspeed.

# 91
>>5510
>>5511
BTW, I've got Godot successfully building today on my box, and hopefully I can soon be up to speed and follow along with you Anon. (3.2 branch b/c my little machine doesn't into Vulkan)
https://github.com/godotengine/godot/tree/3.2

BTW there are good tutorials about the engine, etc., on the official Godot YT channel itself.

# 92
>>5510
If you ask about organized groups around people doing their own AI, then Huggingface comes to mind: https://nitter.net/huggingface 
I also recall them at least discussing to implement GPT3, but they were aware of the problem that it needs quite some powerful servers.
There's generally a lot going on on Twitter and Reddit, it's just necessary to focus one that topic and not getting pulled into politics or other distractions... In my case, I first have to learn the math, otherwise it's pointless. Maybe I'm getting the Brilliant app soon, but first I'll try some other sites and Youtube channels. Also I want to move and buying a new PC after that, so that I won't have to move it.

# 93
>>5519
I imagine some months down the line I might be able to write an SDF importer for Godot. That way simulation training done in Bullet can be used in games and demos easily.

>>5536
Yeah, Huggingface provides a lot of useful tools and models for tokenizing text and stuff. The models used in TalkToWaifu were produced by Huggingface. They're definitely leading in open-sourcing NLP and making it available for everyone.

# 94
related xpost for simulators
>>5667

# 95
This guy here makes interesting stuff with voxels: https://nitter.dark.fail/tuxedolabs - Very realistic environments. Youtube video: https://youtu.be/aAgVSTrqNOc - Not directly slicof life, but if one wants to learn about simulators and how to train AI in such environments, this might be useful.

# 96
>>8486
Wow, thanks Anon! That's pretty inspiring actually. I'll make time to dig through this guy's work and see if I can figure out what he's doing. Also, **thank you for using nitter instead**.

# 97
>>8491
You're welcome. Teardown seems to be the name of the Game now, but there's more:
>voxel engine /plugin
The guy reporting on it, has more videos: 
https://youtu.be/Jnghq0yTmZo
>"Physics" engine /plugin
Primary liquids, not sure how realistic.
https://youtu.be/DBcqiQLp7lY
What we would need is rather a household with people, and all kinds of things, where the behavior depends on the material, temperature, and so on. His vids are more aimed towards gaming and fun or art. At the end of the physics video he points out that more is possible.

# 98
>>8501
I like the idea of creating a robowaifu simulator using voxels. I assume they are a pretty efficient way to create interactive physics, just from looking at the play from that vidya.

# 99
https://www.raylib.com/ might be interesting for simulators or virtual waifus. It's for gaming and works basically everywhere. Its very modular, modules can be used on their own.

# 100
>>8925
Thanks for the reminder Anon. Some other anons mentioned it here before, but I'd gotten so busy I'd forgotten about. You've reminded me about it now. Here's a cleaned-up version of his animation example code, looks pretty simple to use:
```cpp
/*******************************************************************************
 *
 *   raylib [models] example - Load 3d model with animations and play them
 *
 *   This example has been created using raylib 2.5 (www.raylib.com)
 *   raylib is licensed under an unmodified zlib/libpng license (View raylib.h
 *   for details)
 *
 *   Example contributed by Culacant (@culacant) and reviewed by Ramon
 *   Santamaria (@raysan5)
 *
 *   Copyright (c) 2019 Culacant (@culacant) and Ramon Santamaria (@raysan5)
 *
 *******************************************************************************
 *
 * To export a model from blender, make sure it is not posed, the vertices need
 *to be in the same position as they would be in edit mode. and that the scale
 *of your models is set to 0. Scaling can be done from the export menu.
 *
 ******************************************************************************/

#include "raylib.h"

#include <stdlib.h>

int main(void) {
  // Initialization
  //----------------------------------------------------------------------------
  const int screenWidth  = 800;
  const int screenHeight = 450;

  InitWindow(screenWidth, screenHeight,
             "raylib [models] example - model animation");

  // Define the camera to look into our 3d world
  Camera camera   = {0};
  camera.position = (Vector3){10.0f, 10.0f, 10.0f};  // Camera position
  camera.target   = (Vector3){0.0f, 0.0f, 0.0f};     // Camera looking at point
  // Camera up vector (rotation towards target)
  camera.up   = (Vector3){0.0f, 1.0f, 0.0f};
  camera.fovy = 45.0f;               // Camera field-of-view Y
  camera.type = CAMERA_PERSPECTIVE;  // Camera mode type

  // Load the animated model mesh and basic data
  Model model = LoadModel("resources/guy/guy.iqm");
  // Load model texture and set material
  Texture2D texture = LoadTexture("resources/guy/guytex.png");
  // Set model material map texture
  SetMaterialTexture(&model.materials[0], MAP_DIFFUSE, texture);

  Vector3 position = {0.0f, 0.0f, 0.0f};  // Set model position

  // Load animation data
  int animsCount = 0;

  ModelAnimation* anims =
      LoadModelAnimations("resources/guy/guyanim.iqm", &animsCount);

  int animFrameCounter = 0;

  SetCameraMode(camera, CAMERA_FREE);  // Set free camera mode

  SetTargetFPS(60);  // Set our game to run at 60 frames-per-second
  //----------------------------------------------------------------------------

  // Main game loop
  while (! WindowShouldClose())  // Detect window close button or ESC key
  {
    // Update
    //--------------------------------------------------------------------------
    UpdateCamera(&camera);

    // Play animation when spacebar is held down
    if (IsKeyDown(KEY_SPACE)) {
      animFrameCounter++;
      UpdateModelAnimation(model, anims[0], animFrameCounter);

      if (animFrameCounter >= anims[0].frameCount)
        animFrameCounter = 0;
    }
    //--------------------------------------------------------------------------

    // Draw
    //--------------------------------------------------------------------------
    BeginDrawing();

    ClearBackground(RAYWHITE);

    BeginMode3D(camera);

    DrawModelEx(model, position, (Vector3){1.0f, 0.0f, 0.0f}, -90.0f,
                (Vector3){1.0f, 1.0f, 1.0f}, WHITE);

    for (int i = 0; i < model.boneCount; i++) {
      DrawCube(anims[0].framePoses[animFrameCounter][i].translation, 0.2f, 0.2f,
               0.2f, RED);
    }

    DrawGrid(10, 1.0f);  // Draw a grid

    EndMode3D();

    DrawText("PRESS SPACE to PLAY MODEL ANIMATION", 10, 10, 20, MAROON);
    DrawText("foo_bar_baz", screenWidth - 200, screenHeight - 20, 10, GRAY);

    EndDrawing();
    //--------------------------------------------------------------------------
  }

  // De-Initialization
  //----------------------------------------------------------------------------
  UnloadTexture(texture);  // Unload texture

  // Unload model animations data
  for (int i = 0; i < animsCount; i++) {
    UnloadModelAnimation(anims[i]);
  }

  RL_FREE(anims);

  UnloadModel(model);  // Unload model

  CloseWindow();  // Close window and OpenGL context
  //----------------------------------------------------------------------------

  return 0;
}```

https://www.raylib.com/examples.html

# 101
>>8926
Ah, didn't look for it. Here: >>5810 >>2018

# 102
I am currently building a framework for 2D simulations, similar to dwarf fortress.
The goal is to have a simulation that is as realistic as possible, while also using up as little performance as reasonable.

I want to train multi-agents with evolutionary model optimization in the simulation; to test a few ideas on how to solve artificial general intelligence without having to bother with RobotVision and ArtificalMuscleMovement.
Main goal is to solve general AI but I also want to try and solve NaturalLanguage using a new (?) approach.
Going to be open source one day.

(it's not my day-job to code this so progress is kinda slow. Anyone interested in it?)

# 103
>>9032
>Anyone interested in it?
Sure ofc, Anon. We're always interested in that kind of thing here. Give us more details please.

# 104
>>9032
When I first got started with neural networks twenty years ago I made a simple evolution simulation in Game Maker with prey and predators. I've always wondered if they were given the ability to make different sounds and hear each other walking if they would've formed their own crude language eventually. I think that would be a fun project.

I also want to solve general AI and feel that AI needs a more complex environment to really learn and grow. Most AI research focuses on maxing something out but in real life there's always something more to learn.

# 105
>>9034
>When I first got started with neural networks twenty years ago
Wow that's pretty remarkable I had no idea anyone here had that kind of experience. It would be really nice if you conducted a beginner's class on these topics if you're up for something like that Anon.

Cheers.

# 106
>>9045
Nah, I just played around with them for a bit as a kid after watching Chobits. I didn't really get into AI until around 2015. I could probably still teach things but there's lots of material for that on the web and I'd rather work on my own stuff.

# 107
>>9047
Oh haha I see. Well, it's still good to know you're here. Good luck with your 'stuff' Anon. I too found Chobits inspirational when I was young.

# 108
Has anyone tried PhysX? The most interesting feature of it for me is the GPU acceleration because PyBullet isn't really ideal for training thousands of iterations simultaneously.
https://www.youtube.com/watch?v=K1rotbzekf0

https://github.com/petrikvladimir/pyphysx

I'd like to start moving on from just learning about AI and actually apply it to some real problems that can be transferred to the real world. My goal is to start assembling my own robowaifu by the end of the year that can do some basic task like locate my hand and give me a high five or something.

# 109
>>9708
Yes, I've played with it bit (cloth sims & rigid body collisions mostly). Nvidia is plainly an evil Big Tech/Gov entity like the others, but they have made a remarkable push to make their GPU ecosystem easy to use if you at least have the basics of C programming under your belt.

# 110
While I wait for stuff to train I started working a side-project for playing video games with hindsight experience replay and became fascinated with the idea of repurposing the model afterwards for a piano simulation, similar to how they trained a robot hand to solve a Rubik's cube in a simulation then did transfer learning to the real world. A ton of progress has been made in making computer vision and reinforcement learning more efficient. Just two years ago it was probably too early to make any useful simulation and reasonably train an agent in it to do something interesting but now I think it's within reach.

Maybe it's only an exciting idea to me but I think it would be a great way to demonstrate how far along AI has progressed and that anyone can make their own waifu play piano MIDI files given. We could demo other capabilities with it too like making her say the title of the song before playing and generate some virtual waifu hype. The simulation code would also provide a base for others to get started doing other custom simulations such as moving arms, balancing, and walking.

# 111
>>10073
>Maybe it's only an exciting idea to me
No, I think it's a great idea Anon. I agree this would both be an innovative and useful way to build up training for AIs/Robowaifus.

# 112
Over the past few days I've gotten the latest Blender and UE4 working on my machines.

# 113
Someone mentioned Webots: Robot Simulator here >>10531 Link: https://cyberbotics.com/
>It has been designed for a professional use, and it is widely used in industry, education and research. Cyberbotics Ltd. maintains Webots as its main product continuously since 1998.
>Webots core is based on the combination of a modern GUI (Qt), a physics engine (ODE fork) and an OpenGL 3.3 rendering engine (wren). It runs on Windows, Linux and macOS. Webots simulations can be exported as movies, interactive HTML scenes or animations or even be streamed to any web browser using webgl and websockets.
>Robot may be programmed in C, C++, Python, Java, MATLAB or ROS with a simple API covering all the basic robotics needs.

# 114
>>1708
I apologize Anon, for not thanking you for this image when you posted it. I actually ''did'' appreciate it back then, but I was too distracted to share my gratitude at the time.

So thanks! :^)

# 115
>>10073
We'd be interested to hear how both the training and your 'side-project' worked out Anon. Any news to share with us?

# 116
>>1092
>>1093
>>1101
Already been meme'd.
I think something very similar to this was originally proposed as a "troll" on a certain chan, which literally led to some articles and "focus groups" that led to the creation of a monitoring group who has eyes on all "robot" threads/convos across the internet.
> The roastie fears the robot-samurai.

# 117
>>11010
Haha, well that's interesting Anon! Can you give us more details on these 'watchers'? Somebody might need to keep eyes on them tbh.

>''And now all the Hawtchers who live in Hawtch-Hawtch are watching on watch watcher watchering watch , watch watching the watcher who's watching that bee. You're not a Hawtch-Watcher you're lucky you see!” ''
>t― Dr . Seuss , ''Did I Ever Tell You How Lucky You Are?''

# 118
>>11013
Hmmm. Use machines to keep an eye on machines? In a time of deepfake video and digitally altered footage, I just hope they believe the camera feeds they're watching. 😉

# 119
What looks to be a very useful header-only C++ wrapper around the OpenGL C API. I'll try to make some time to have a look at it over the summer.
https://oglplus.org/oglplus/html/index.html
https://github.com/matus-chochlik/oglplus

# 120
>related crosspost (>>1857)
also related to above
https://www.khronos.org/gltf/
https://en.wikipedia.org/wiki/GlTF
https://docs.blender.org/manual/en/2.93/addons/import_export/scene_gltf2.html

# 121
Here's something I found through our Japanese colleagues. MoxRig / MomoRig https://mox-motion.com/ - I didn't try it out, but it seems to be useful for animation of human-like movement and simulation of robots.

# 122
>>11497
Neat! Thanks Anon, I'll give it a lookover.

# 123
>>11022
>emoji
friendly islamic reminder this is a chan don't use emoji please

