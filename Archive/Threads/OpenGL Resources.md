# 1
Good VR is one important interim goal for a fully-realized RoboWaifu, and it's also much easier to visualize an algorithm graphically at a glance than 'trying to second-guess a mathematical function'. OpenGL is by far the most portable approach to graphics atm.

>"This is an excellent site for starting with OpenGL from scratch. It covers from very introductory topics all the way to advanced topics like Deferred Shading. Liberal usage of accompanying images and code. Strongly recommended."

learnopengl.com/
https://archive.is/BAJ0e

Plus the two books related, but learnopengl.com is particularly well-suited for beginners.

www.openglsuperbible.com/
https://archive.is/NvdZQ

opengl-redbook.com/
https://archive.is/xPxml

www.opengl.org
https://archive.fo/EZA0p

# 2
Nominally geared for beginners, although I consider it very difficult to fit something this complex into a single video–even one over 3 hrs in length! Presented live at SIGGRAPH '13.

www.youtube.com/watch?v=6-9XFm7XAT8&index=6&list=PLUPhVMQuDB_aWSKj7L_-3Ot_nxBze_YMy
https://archive.is/J0YXd

https://www.invidio.us/watch?v=6-9XFm7XAT8

# 3
open.gl/transformations
https://archive.is/wV8ak

# 4
I think I'll take a shot at creating an OGL generator to take away some of the burden of dealing with the graphics and scene complexity as a learning exercise.

If it goes well, then I might try my hand at extending it to a full environment builder for the simulator idea in this thread.
>>155

# 5
>>683
Well it was surprisingly difficult, but I finally managed to get a system set up where I can make a simple OpenGL window with a spinning triangle. I got it working after switching to Manjaro (ARCH) Linux, and 'm using GLFW + GLAD. I had to install GLFW from the software manager, and I had cloned and built both GLFW and GLAD from github. I generated the GLAD files specific for my machine with the command:

```cpp
python main.py --generator c --no-loader --out-path output```

, and then copied the two include directories into /usr/include/ and the glad.c file into my project directory (as per the GLAD instructions). I used the code example from here:

www.glfw.org/docs/latest/quick.html

The image is a capp of the simple OpenGL window result.

Here's the simplest blank window code (w/o animation) that I managed to get working:

```cpp
// based on code at:
// http://www.glfw.org/docs/latest/quick.html

#include <glad/glad.h>  // NOTE: must be #include'd before glfw3.h

#include <GLFW/glfw3.h>
#include <iostream>

//------------------------------------------------------------------------------

static void key_callback(
    GLFWwindow* window, int key, int scancode, int action, int mods)
{
  if (key == GLFW_KEY_ESCAPE && action == GLFW_PRESS)
    glfwSetWindowShouldClose(window, GLFW_TRUE);
}

//------------------------------------------------------------------------------

int main()
{
  if (!glfwInit()) {
    std::cerr << "Failed to init OpenGL\n";
    return -1;
  }

  GLFWwindow* window = glfwCreateWindow(
      640, 480, "Even simpler example", nullptr, nullptr);
  if (!window) {
    std::cerr << "Failed to create a window\n";
    glfwTerminate();
    return -1;
  }

  glfwSetKeyCallback(window, key_callback);
  glfwMakeContextCurrent(window);

  // NOTE: Leaving this directive out causes a failure with a return code 139 on
  // my box
  if (!gladLoadGLLoader((GLADloadproc)glfwGetProcAddress)) {
    std::cerr << "Failed to initialize GLAD\n";

    glfwDestroyWindow(window);  // NOTE: Are these needed here?
    glfwTerminate();            //

    return -1;
  }

  glfwSwapInterval(1);
  while (!glfwWindowShouldClose(window)) {
    // DESIGN: Any rendering code would go here:

    glfwSwapBuffers(window);
    glfwPollEvents();
  }

  glfwDestroyWindow(window);
  glfwTerminate();
}```

Here's my basic CMakeLists.txt file to go with that code:

```cpp
cmake_minimum_required(VERSION 2.8)

project(simple)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++14 -Wall -Wextra -Wno-unused-parameter")

add_executable(simple main.cpp glad.c)

find_package(PkgConfig REQUIRED)
pkg_search_module(GLFW REQUIRED glfw3)
target_link_libraries(simple ${GLFW_LIBRARIES} )```

Simple I know, but hey we all have to start somewhere yea? Now I'll begin trying to figure out how to manage creating, saving and loading geometry data on the disk files from inside the code. That should let me start exploring how to create and display environment and object geometries to use in my OpenGL windows. Once that's basically working, I could then start thinking about things like better shaders, etc. But on my old notebook machine right now I only have OpenGL v 2.1 (an Intel Mobile 4 series integrated graphics controller) so I don't expect to do anything remarkable atm. OTOH, this also means my stuff should be compatible w/ basically everyone's graphics setup if it becomes something I package up sometime.

Also, now that I have a reasonably usable OpenGL dev box I've begun working through this book:

learnopengl.com/

# 6
>>684
>(as per the GLAD instructions)
Actually, check that. I got the command instruction from the GLFW site instead.

www.glfw.org/docs/latest/context_guide.html#context_glext_auto

# 7
Modern computer graphics recommendation thread on HN.

news.ycombinator.com/item?id=14652936

# 8
Here's a WordPress w/ lots of D3D **shudder** and OGL stuff.

fgiesen.wordpress.com/2011/07/09/a-trip-through-the-graphics-pipeline-2011-index/

# 9
Some srsly great shaders can be found here if you dig around.

www.shadertoy.com/

# 10
The Cinder library now has official support for Ubuntu Linux and Raspberry Pi 2 & 3 as of version 0.9.1
libcinder.org/download

I consider this the best general purpose library I've ever seen for the Creative Coding field for C++ devs. I've gotten it successfully built on Ubuntu and I'll be playing around with it a bit for various experiments related to visualizing my facial animation code. The results should be runnable on Windows, Linux, and Mac.

libcinder.org/gallery

# 11
>>684
So, I made this post a couple of years ago now, and I thought I'd do another one like it since I understand things a little more now and can probably explain it just a bit better (or maybe not heh). The next couple of posts are all about how I just made a simple (but working) OpenGL sample program on a fresh install of Manjaro Linux using the GLAD/GLFW sample code.

# 12
>>1723
First, I'll install GLAD. The repo is at: 
https://github.com/Dav1dde/glad
but I'll install it using pip (as per the recommendation). First I need to make sure pip is installed, either pacman or the Pamac gui can be used. Install 'python-pip' from the official ''extra'' repo.
>1

-Then I install the latest GLAD version directly from the repo
```cpp
sudo pip install --upgrade git+https://github.com/dav1dde/glad.git#egg=glad```
>2

-Now I'll generate OpenGL C-loader files using GLAD. Since the ''learnopengl.com'' book focuses on the OpenGL 3.3 core (for good reasons), I'll specify that in particular.
```cpp
python glad --generator=c --out-path=GL --api="gl=3.3" --profile=core```
-This will create 3 files in 3 different subdirectories under GL/. 
```cpp
tree GL```
>3

-I'll copy the two include directories into the /usr/include/ directory for access by my own OpenGL code.
```cpp
sudo cp -r GL/include/* /usr/include/
```

-I can confirm the new directories are in place now.
```cpp
ls /usr/include/ | grep -e KHR -e glad
```
>4

-The third file is under the GL/src directory, and is named 'glad.c' . It should be a little under 9'000 lines long. I'll copy this file into whatever directory where my own source code is located for each of my projects. 

It defines all the C-declarations describing the OpenGL 3.3 core spec, and makes sure they are all loaded properly for the program. Have a good look at the file, and you'll see that this is why I use the GLAD generator; b/c it saves metric shittons of time, effort, and fubar grief when dealing with OpenGL.
>5

# 13
>>1723
-Next, I'll install GLFW, and be sure to use the X11 version. I'll add the documents too. Here's the GLFW site.
https://www.glfw.org/docs/latest/build_guide.html
I'll just use Pamac.
> 1, 2

-Now I'll create a simple test project, just using the one provided with the glad repo. Using my favorite editor Juci, I'll create a new C++ project, delete the default main.cpp file and copy the ''glad.c'' & ''hellowindow2.cpp'' files into the project directory.
>3, 4

-Here's the contents of the new CMakeLists.txt file:
```cpp
cmake_minimum_required(VERSION 2.8)

project(muh_ogl_test)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++1z -Wall -Wextra -Wno-unused-parameter")

add_executable(muh_ogl_test hellowindow2.cpp glad.c)

find_package(glfw3 3.3 REQUIRED)
target_link_libraries(muh_ogl_test glfw dl)
	```
-Now, just pressing Ctrl+Return in Juci saves, builds and runs the OpenGL sample.
>5

-Or, build and run from the terminal:
```cpp
g++ hellowindow2.cpp glad.c -lglfw -ldl && ./a.out
```
-I made a zip for you to look at.
https://files.catbox.moe/s54kmo.gz

Hope that helps anon. Cheers.

# 14
>>1725
Oops, I forgot to mention the 'clone the GLAD git repo first before installing it with pip' between the 'install pip' and 'install glad' steps.
```cpp
git clone https://github.com/Dav1dde/glad.git```
Apologies.

# 15
>>1727
Double-duh. Actually I guess it's more about running the generator locally, rather than installing it. So, needed just before the generation step actually. Hmm, I suppose you could use the DLd repo from the pip install step too. IDK if you can direct that download to somewhere other than ''/tmp/'' with pip.

# 16
>>1725
I guess to complete the circle I should go ahead and post a copy of the newer code as well. I also plan to wrap all this mess in a clean and simple-to-use ''muh_gl.h'' file later.

```cpp
#include <cstdlib>
#include <iostream>
#include <string>

// GLAD
#include <glad/glad.h>  // NOTE: #include before glfw

// GLFW
#include <GLFW/glfw3.h>

//------------------------------------------------------------------------------

using std::cerr;
using std::cout;
using std::exit;
using std::string;

//------------------------------------------------------------------------------

static void err_cb(int, const char*);
static void key_cb(GLFWwindow* window, int key, int scancode, int action,
                   int mode);

//------------------------------------------------------------------------------

int main()
{
  cout << "Starting GLFW context init, OpenGL 3.3 core..." << std::endl;

  const GLuint w{800}, h{600};
  const string title{"Muh /robowaifu/ Simulator Title"};

  // Init GLFW (& OGL)
  glfwSetErrorCallback(err_cb);
  if (!glfwInit()) {  // Attempt OGL init
    cerr << "\nFailed to init GLFW/OGL\n";
    exit(-1);
  }
  else {  // Set all the required options for GLFW
    glfwWindowHint(GLFW_CONTEXT_VERSION_MAJOR, 3);
    glfwWindowHint(GLFW_CONTEXT_VERSION_MINOR, 3);
    glfwWindowHint(GLFW_OPENGL_PROFILE, GLFW_OPENGL_CORE_PROFILE);
    glfwWindowHint(GLFW_RESIZABLE, GL_FALSE);
  }

  // Setup the window
  auto win{glfwCreateWindow(w, h, title.c_str(), nullptr, nullptr)};
  if (!win) {  // Failed
    cerr << "\nFailed to create OGL window\n";
    glfwTerminate();
    exit(-1);
  }
  else {  // Attempt configs
    glfwMakeContextCurrent(win);
    if (!gladLoadGLLoader(GLADloadproc(glfwGetProcAddress))) {
      cerr << "\nFailed to get the OGL context process address\n";
      glfwDestroyWindow(win);
      glfwTerminate();
      exit(-1);
    }
    else {
      glfwSetKeyCallback(win, key_cb);
      glViewport(0, 0, w, h);
    }
  }

  cout << "GLFW Initialization complete, begin game loop..." << std::endl;
  //-------------------
  // Game Loop
  //
  while (!glfwWindowShouldClose(win)) {
    glfwPollEvents();

    // Just clear the buffer for now
    glClearColor(0.2f, 0.3f, 0.3f, 1.0f);
    glClear(GL_COLOR_BUFFER_BIT);

    glfwSwapBuffers(win);
  }
  //
  //-------------------
  cout << "Clean exit from game loop, cleaning up GLFW..." << std::endl;

  // Clean up
  glfwDestroyWindow(win);
  glfwTerminate();
}

//------------------------------------------------------------------------------

void err_cb(int err, const char* desc)
{
  cerr << '\n' << err << " error: '" << desc << "'\n";
}

//------------------------------------------------------------------------------

void key_cb(GLFWwindow* win, int key, int scancode, int action, int mode)
{
  if (action == GLFW_PRESS) {
    cout << "GLFW key code: " << key << " pressed." << std::endl;
    if (key == GLFW_KEY_ESCAPE) glfwSetWindowShouldClose(win, GL_TRUE);
  }
}
```

>//------------------------------
edit: added an over-abundance of diagnostic output.

# 17
Obviously not OpenGL, but this seems like it might be of interest for onboard robowaifu graphical displays. ANSI C immediate-mode graphical toolkit.

github.com/Immediate-Mode-UI/Nuklear

# 18
>>1731
>I also plan to wrap all this mess in a clean and simple-to-use muh_gl.h file later.
Done. Here's the what the same code looks like now:
```cpp
#include <cstdlib>
#include <iostream>

#include "muh_gl.h"

using std::cerr;
using std::cout;
using std::exit;

//------------------------------------------------------------------------------

int main()
{
  cout << "Starting GLFW context init, OpenGL 3.3 core..." << std::endl;
  if (!muh_gl::init_glfw()) exit(-1);
  auto win{muh_gl::init_win()};

  cout << "GLFW Initialization complete, begin game loop..." << std::endl;
  //-------------------
  // Game Loop
  //
  while (!glfwWindowShouldClose(win)) {
    glfwPollEvents();

    // Just clear the buffer with a background color for now
    glClearColor(0.2f, 0.3f, 0.3f, 1.0f);
    glClear(GL_COLOR_BUFFER_BIT);

    glfwSwapBuffers(win);
  }
  //-------------------
  cout << "Clean exit from game loop, cleaning up GLFW..." << std::endl;

  // Clean up
  glfwDestroyWindow(win);
  glfwTerminate();
}
```

# 19
==TBH SMH FAM==
I just want to establish firmly here and now, that I'm the originator of this clever literary device, in fact of course.

```cpp
// Say Hi to the MRS. Anon,
// Muh Robowaifu Simulator.
//=========================
//

#include <iostream>

#include "muh_gl.h"

using std::cout;

//------------------------------------------------------------------------------

int main()
{
  const int w{800}, h{600};
  auto win{muh_gl::init_win(w, h, "Muh Robowaifu Simulator")};

  cout << "GLFW init successful, begin game loop..." << std::endl;
  //-------------------
  // Game Loop
  //
  while (!glfwWindowShouldClose(win)) {
    glfwPollEvents();

    // Just clear the buffer with a background color for now
    glClearColor(0.2f, 0.3f, 0.3f, 1.0f);
    glClear(GL_COLOR_BUFFER_BIT);

    glfwSwapBuffers(win);
  }
  //-------------------
  cout << "Clean exit from game loop, cleaning up GLFW...\n";

  // Clean up
  glfwDestroyWindow(win);
  glfwTerminate();
}

// Copyright (2019)
// License (MIT)  https://opensource.org/licenses/MIT
```
**:^)**

# 20
Went ahead and created a public repo for this work.
>>1814

# 21
Well, it was kind of convoluted to work out all the details, but I've managed to add quality TTF text rendering to the MRS.

# 22
>>1815
BTW, I removed GLAD as an external dependency. There's an option to create all-local files, so I moved MRS to that approach. It means anons don't have to deal with GLAD now.

# 23
Added a ''void rndr_tick(Shader txt_shdr, const unsigned fps_tick)'' function to ensure the MRS was really getting an honest 60fps (it is). However, occasionally I'd notice a little artifact that made me think that tearing was happening even though I set the swap interval to 1:
```cpp
glfwSwapInterval(1);  // 1 should prevent tearing```

Now I'm not so sure it's actually tearing;
A) It only infrequently occurred
B) It is likely limited to only the fast-transitioning digit at the end, afaict.

This makes me think it's actually not tearing, but rather the screen capp program I'm using (Shutter) is simply 'snapping' the image right at the instant a digit is being redrawn. I'd welcome insight if anyone knows more about this stuff.
>pic related

# 24
>>1848
Unrelated: Does the system redraw ''from the bottom-up''? For some reason I thought the drawing happened from the upper-left corner down, but apparently not. Given that the coordinate origin for the system starts in the lower-left corner (similar to a Cartesian system) I guess that makes sense. Live and learn.

