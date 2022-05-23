# 1
In the same spirit as the ''Embedded Programming Group Learning Thread 001'' >>367 , I'd like to start a thread for us all that is dedicated to helping /robowaifu/ get up to speed with the C++ programming language. The modern form of C++ isn't actually all that difficult to get started with, as we'll hopefully demonstrate here. We'll basically stick with the C++17 dialect of the language, since that's very widely available on compilers today.

There are a couple of books about the language of interest here, namely Bjarne Stroustrup's ''Programming -- Principles and Practice Using C++ (Second edition)'' https://stroustrup.com/programming.html , and ''A Tour of C++ (Second edition)'' https://stroustrup.com/tour2.html . The former is a thick textbook intended for college freshmen with no programming experience whatsoever, and the latter is a fairly thin book intended to get experienced developers up to speed quickly with modern C++. We'll use material from both ITT.

During the progress, I'll discuss a variety of other topics somewhat related to the language, like compiler optimizations, hardware constraints and behavior, and generally anything I think will be of interest to /robowaifu/. Some of this can be rather technical in nature, so just ask if something isn't quite clear to you. We'll be using an actual small embedded computer to do a lot of the development work on, so some of these other topics will kind of naturally flow from that approach to things.

We'll talk in particular about ''data structures and algorithms'' from the modern C++ perspective. There are whole families of problems in computer science that the language makes ridiculously simple today to perform effectively at an industrial scale, and we'll touch on a few of these in regards to creating robowaifus that are robust and reliable. 

>NOTES:
-Any meta thoughts or suggestions for the thread I'd suggest posting in our general /meta thread >>3108 , and I'll try to integrate them into this thread if I can do so effectively. 
-I'll likely (re)edit my posts here where I see places for improvement, etc. In accord with my general approach over the last few months, I'll also make a brief note as to the nature of the edit.
-The basic goal is to create a thread that can serve as a general reference to C++ for beginners, and to help flesh out the ''C++ tutorial section'' of the '''RDD''' >>3001 .

So, let's get started /robowaifu/.

# 2
What book would you recommend for someone who has had some previous programming experience before, but not necessarily with C++, Programming: Principles and Practice Using C++, or C++ Primer?  I've done some stuff in Python and Java, and I've wanted to learn C++, and those two are ones that I hear often for beginners.

# 3
>>4915
>''and the latter is a fairly thin book intended to get experienced developers up to speed quickly with modern C++. //
Tour++

# 4
>>4915
>>4916
seconding this, I'd really like to learn C++ as well.

# 5
>>4937
Thanks for the interest Anon. My schedule is in a bit of a ruckus atm. I'll try to update the thread on weekends. If you'd like to get ahead, then study the RaspberryPi 3, that will be the next topic. We'll be using it as the primary teaching platform ITT.

# 6
I decided that the process of getting the RaspberryPi boxes fully set up was detailed and involved enough, and only indirectly related to the main topic ITT, that it should be in it's own thread.
>>4969

# 7
I mean it's a ''really'' '''big''' language. This stems from it's very wide generality of usage for 40 years. It serves in an almost unbelievably wide range of usage domains. So (especially) to help newcomers get off on the right foot, I'm going to guide everyone into setting themselves up with good documentation. Don't be concerned with understanding any of this ATP, it is simply to get you on the correct path for documentation from step one.

NOTE: I'll usually speak with the 'tutorial voice' ITT (ie, I'll give unqualified instructions). If you're an old hand at this--be patient. If you're a greenhorn, then I recommend simply following every step I give you. You'll then know you are on the same page as me. Almost all of these instructions ITT assume you are working along with us on the Raspberry Pi (either the real hardware or the virtual desktop).

So let's get started setting up your most important C++ bookmarks first.

# 8
>>4992
1. Open Chromium (display the bookmarks bar and bookmark all these.
2. Goto
https://en.cppreference.com/w/
3. Goto
https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines
  -click 'Turn ON syntax'
4. Goto
https://isocpp.org/get-started
5. Goto
http://www.cplusplus.com/
  -NOTE: Be aware this is nowhere near as authoritative cppreference is.

# 9
>>4993
Since it's an officially-recognized international standard, ISO C++ isn't ''defined'' by any of these sites, they are merely there to help professionals quickly get up to speed with information. The actual '''definition''' of the language is the actual standards document itself. While filled with an incredibly high degree of technical specificity (and therefore of little use to a beginner), I'll go ahead and add in a draft (ie, C++23 version) copy of it I rendered a few months ago:
>

If anyone wants instructions on creating your own up-to-the-minute copy of the document, just ask ITT.

# 10
I'm brand new to trying to learn C++. Like only a couple days in. A total baby when it comes to programming. Before this the most I've done is follow a tutorial to tweak a python script to get a Minecraft server going. 

I've been slowly going through this video to get the basics down. Any newbie like be shouldn't be afraid to learn at their own pace!

https://youtu.be/vLnPwxZdW4Y

This guy's simple examples and reiteration of concepts leading into other concepts helps the logic of C++ make sense. The development program he uses and recommends, Code::Blocks, is very helpful in the process of getting something to run. I'll link it here:

http://www.codeblocks.org/

I've gotten about an hour into the material and I'm making up my own little projects to help me understand each subject and the little ins-and-outs of C++. I've toyed around with variables to simulate a Pokémon battle and I'm messing around with user input prompts to customize a fake conversation. I know this is baby town for C++ and it's already super fascinating!

# 11
>>4995
That's good to hear Anon, thanks for sharing the cap and the link! Just let us know ITT if you have any questions as we go along. Having lots of different resources for learning is a good thing.

Mind telling us about the program you're working on? 
>and I'm making up my own little projects to help me understand each subject
Yes, that's a good approach for beginners. Lots and lots of small projects. This makes things easier to grasp as we go along.

# 12
I'm working on setting things up for our C++ class thread, and for those of you interested in participating in the thread I have a question:
-Would you rather I treat you like professionals who need to face the real-world complexity of building robowaifu software?
-Or would you prefer a simplistic approach where things are much easier to grasp?

The benefit of the first is that you'd be much more quickly able to create real robowaifu software (but the learning curve is steep for beginners).
The benefit of the second is that it would be more /comfy/ but you would take a long time until you were proficient enough to contribute here with software engineering?

Please let me know what you'd prefer.

# 13
>>5085
Anyone?

# 14
Alright, I plan to pursue a professionally-oriented, embedded developer approach to the class. This will be oriented towards using the best of C++ in modern embedded environments (such as robowaifus engineering) with plenty of '''C''' lore thrown in (just using best practices from C++ instead where feasible) to boot.

This will not really be a beginner's class therefore. I'd suggest the cplusplus.com tutorials for you guys.
http://cplusplus.com/doc/tutorial/

# 15
>>5085
I apologize for not responding. I feel like an ass because you've taken time out of your busy schedule to offer all of us FREE C++ training. since i am the only one who seems to be responding, i am requesting we do the 2nd one. I am the anon who said that i have some experience in HTML, Javascript, and CSS.

# 16
>>5143
Also two more things, Could Visual basic be used to code robowaifus or is it only exclusively used for web design and how much has C++ changed in the last 20 years? The last time my dad coded in C++ was around 20 years ago, mostly because he was a web designer and didn't really play around with C++.

# 17
>>5143
>to offer all of us FREE C++ training
Heh, I haven't really tried doing this before (training others) so I will have a lot to learn myself I'm sure. Best to be patient with each other, yea? :^)  Besides, I'm only looking after this on the weekends, so it's not too much of an impact really.

>i am requesting we do the 2nd one
I see then. Hmm, I definitely want to help anyone who wants to learn here. But it's kind of a juggling act to be able to address the needs of the beginner and the more experienced (without boring both at the same time haha). Let me give it some thought this week and I'll try to think through a good approach that might be helpful to everyone here.

>>5144
>how much has C++ changed in the last 20 years?
I'm not too sure, but I know that since 2011 the language has gone through a lot of changes and improvements. I'm guessing guys like your Dad might like the newer things if they took the time to learn them? 

Anyway, there's little doubt that it's one of the most important languages in the world for the demanding needs of engineering robowaifus, so it's a really good choice for us.

# 18
>>4993
1. Goto
https://releases.llvm.org/7.0.0/tools/clang/tools/extra/docs/clang-tidy/checks/list.html

We're going to be setting up and using both clang-tidy & clang-format on our RPi boxes, so you may as well begin now to familiarize yourself with them.

# 19
>>5146
>v7
Check that. Use this link instead, since RPi Buster has v9 in the repos:

1. Goto
https://releases.llvm.org/9.0.0/tools/clang/tools/extra/docs/clang-tidy/checks/list.html

# 20
First things first. Let's make sure we're all on the same page with our compilers. 
```cpp
g++ --version
clang++ --version```
If you worked your way through the RPi 'sepplesberry' setup thread >>4969, then you should see the same thing.
> #1

We'll be using C++17 for the most part, and these versions of our compilers both have good support for it. If you are on an older compiler, just let me know ITT and we'll try to devise alternatives that will work with C++11/14 for you. Don't use any old compiler that can't even support C++11.

>PROTIP:
''Writing software != typing text into an IDE and pressing the big green button.''

With our little RPi dev boxes, we are enjoying the real luxury of having an actually-usable GUI and a nice IDE directly on our embedded system. 

But in general you can't expect this. Software development for embedded is usually done on external dev boxes, then the cross-compiled binaries are pushed up to the target hardware over the wire to be able to use it (or indeed even to ''test'' it). Our current approach with our /comfy/ little RPi dev boxes makes things unusually convenient for us, but keep your eyes open to reality anon. Things won't always go this easy on us when building our robowaifus. :^)

While we'll consistently be using the C++ IDE ''Juci++'', it will also be a really good idea for you to learn at least the basics of using ''Vim''. This will allow you to edit files remotely on a small embedded machine via SSH. Some of those remote files ''could'' be software code files ofc:
> #2 #3

In fact, theoretically you don't even have to use an ''editor'' to write and compile software.
```cpp
echo "int main () {}" > foo.cpp
g++ foo.cpp```
> #4

Alright, let's get going with our C++ class, /robowaifu/.

# 21
Hey just to let you know there's at least another student keeping tabs on this, since you've been working hard documenting these lessons.  I could go either approach you suggested.  My experience with C++ is high school and college and hobbyist (with Arduino).  Though I have done some software development, I actually haven't used C++ in a professional setting.

# 22
>>5367
Oh hey there, welcome aboard. Sounds like you already have some development experience. You might like to skim through the Stroustrup book ''Tour++'' then to get up to date with modern C++. My impression is that most C++ training in an academic setting is rather dated.

This class will likely be rather slow-paced (off and on). Over time we will hopefully build up a decent tutorial guide for using C++ primarily in the context of embedded programming for robowaifu development. Please ask me questions (that goes for everyone ofc). Also, if there's a particular area of C++ you'd like me to address please let me know that as well.

# 23
Alright let's get started with the most basic 'Hello World' code to begin with. Select ''[RPi Menu] > Programming > juCi++'' to open your editor.
> #1

Choose ''File > New Project > C++'' . I suggest first creating a special work folder to keep all your project work for this thread in. Mine's simply called 'projects' .
> #2

Give the C++ project itself a name. Mine's simply 'cpp_class' .
> #3

juci will automatically create a project folder and set of starter files for you. We'll discuss each of these, but for now we're just interested in the one named ''main.cpp''. This is the minimal 'Hello World' program in C++ .
> #4

Choose ''Project > Compile and Run'' (ctrl+enter) . The IDE will build and run your program for you. Any console results will appear in the lower built-in terminal emulator.
> #5

That's it. You've gotten C++ running on your embedded computer. Next we'll break down ''functions''.

# 24
-Select all the code on line #1 and delete it.
-Select all the code on line #4 and delete it.
-Run the program (ctrl+enter)

You notice there was no 'Hello World!' output result in the terminal, but also that there wasn't any error messages either. So, the minimal valid C++ program is simply

```cpp
int main() { }```
> #1

This silly example is a do-nothing function that takes no arguments, and performs no actions. Now let's have a look at this (actually important) example function '''main()''' a little closer.

-From ''PPP2 §2.2 The classic first program''
>Every C++ program must have a function called main to tell it where to start executing. A function is basically a named sequence of instructions for the computer to execute in the order in which they are written. A function has four parts:
>• A return type, here '''int''' (meaning “integer”), which specifies what kind of result, if any, the function will return to whoever asked for it to be executed. The word int is a reserved word in C++ (a keyword), so int cannot be used as the name of anything else (see §A.3.1).
>• A name, here '''main'''.
>• A parameter list enclosed in parentheses (see §8.2 and §8.6), here '''()'''; in this case, the parameter list is empty.
>• A function body enclosed in a set of “curly braces,” '''{ }''', which lists the actions (called statements) that the function is to perform.
> #2

-From ''Tour++ §1.2.1 Hello World!''

>The minimal C++ program is
> ```cpp
int main() { }  // the minimal C++ program```
>This defines a function called main, which takes no arguments and does nothing.
>Curly braces, '''{ }''', express grouping in C++. Here, they indicate the start and end of the function body. The double slash, '''//''', begins a comment that extends to the end of the line. A comment is for the human reader; the compiler ignores comments.
>Every C++ program must have exactly one global function named '''main()'''. The program starts by executing that function. The '''int''' integer value returned by main(), if any, is the program’s return value to "the system." If no value is returned, the system will receive a value indicating successful completion. 
> #3

So actually, this is both the most important function in one sense, and the 4-part template for every C++ function. Maybe not that silly (for teaching at least) :^)

# 25
>>5422
-Choose ''Edit > Undo'' 3 times to get the original hello world code back.
-Between the ''#include <iostream>'' and ''int main() {'' add this code:
```cpp
void baz() {
  std::cout << "baz()\n";
}

void bar() {
  std::cout << "bar()\n";
}

void foo() {
  std::cout << "foo()\n";
}```

-Below the ''  std::cout << "Hello World!\n";'' inside main() add this code:
```cpp
  foo();
  bar();
  baz();```
  
-Now run the program (ctrl+enter)
> #1

Recall from ''PPP2 §2.2'' 
>''A function is basically a named sequence of instructions for the computer to execute in the order in which they are written.''

The point of this simple exercise is to show you that each of the 3 new functions were each executed from ''main()'', in the order they were called inside main(). Try scrambling around the ordering of the 4 statements inside main()'s function body to confirm for yourself they execute in whatever order you write them.
> #2

# 26
>>5423
Now let's rearrange things just a bit to demonstrate chaining function calls together.

-Cut the ''bar();'' code from main(), and paste it in the bottom of the ''foo()'' function body.
-Cut the ''baz();'' code from main(), and paste it in the bottom of the ''bar()'' function body.
-Add a new statement at the bottom of the ''main()'' function body.
```cpp
  std::cout << "Back from 3 functions, now exiting.\n";```

Run the program.
> #1

The takeaway here is that the single statement ''foo();'' inside main() triggered a cascade of calls to the other three functions, and main() got control back afterwards then exited. Notice, again, these all ''execute[d] in the order in which they are written.''
-first main() called foo()
-next foo() called bar()
-next bar() called baz()
-finally main() regained control after the chained calls finished. The program then exited when main() completed.

>===
-''minor prose edit''
-''s/two/three''

# 27
Functions form the heart of software development. Unlike the silly ''foo() bar() baz()'' canonical examples, functions are actually named meaningfully in real code. For example:
```cpp
bool waifu_stand()```
and
```cpp
bool waifu_sit()```
are pretty recognizable at a glance, simply by their function name. 

Don't worry if it's a little confusing for now, it will make a lot more sense to you as we go along Anon. We'll be talking about functions very often.

Well, I think that's enough for now, see you next time.

Cheers.

# 28
When you write computer software, you use variables to hold information inside the computer. Variables have both a ''name'' and a ''type''. For example, the statement:
```cpp
const int over_9000{9001};```
tells C++ to set up an object inside the computer's memory named 'over_9000' . It's interpreted as the ''integer'' variable type by C++, and pre-loaded with the constant (unchanging) value '9001'.

There are effectively just four fundamental (that is, directly ''built-in'' to the language) types in C++ :
• int      - a whole number such as ''0'', ''-1'', or ''9001''
• bool   - a Boolean which can only be ''true'' or ''false''
• char   - a single character such as ''R'' or ''w''
• float   - a number with a decimal part such as ''0.0'', ''-1.1'', or ''9001.1009''

There's also a 'fake type'
• void   - a type placeholder meaning simply ''nothing''

>''Tour++ §1.4 Types, Variables, and Arithmetic'' 
> Every name and every expression has a type that determines the operations that may be performed on it. For example, the declaration
> '''int inch;'''
> specifies that ''inch'' is of type ''int''; that is, inch is an integer variable.
> #1

In general, these are the basic types you need to memorize (and master) first. Once you fully understand these types and how to use them effectively, then you should be able to learn the more sophisticated types available in C++ with relative ease. Focus on the basics first, then everything else should fall into place for you afterwards.

Here's a little more technical information about types and objects. Just try to make sense of things, but don't worry about it if it doesn't entirely make sense to you for now. You'll eventually get it all organically as we go along.
>''PPP2 §3.8 Types and objects'' 
> #2

>===
''minor accent change''
''swap 'interpreted' clause''
''replace hyphens w/ bullets in list''
''minor (but numerous) prose edits''

# 29
==daily reminder==
you must type code in yourself to learn it tbh.

# 30
>>5438
>'''Daily reminder''' literally ''everything'' inside our computer's systems are simply ''1'''s and ''0'''s (plus timing signals).
This simple truth presents a big challenge for the forerunner men of Computer Science; namely, ''How do we represent an arbitrary human-readable 'number' in an entirely general way, using only synchronized high voltages and low voltages?''.

The basic number type ''Integers'' are probably the most important computer object type out there. '''C''' and '''C++''' both have quite sophisticated notions of the integer type built right in. Based DMR is based **as are all the giants on whose shoulders he stood on**.

And, since they are simplistic numbers, ints should also support the basic arithmetic operations such as ''add & subtract'', ''multiply & divide''.

How does this work, practically speaking?

# 31
>>5347
I hope this isn't too old, I just dusted off an Rpi 3B+ which I haven't touched in almost 2 years, was too lazy to update everything so just did the dependencies.  I figured at some point I will want to reinstall a fresh image anyway but in the meantime I'm following along fine.

pi@raspberrypi:~ $ g++ --version
g++ (Raspbian 6.3.0-18+rpi1+deb9u1) 6.3.0 20170516
Copyright (C) 2016 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

pi@raspberrypi:~ $ clang++ --version
clang version 6.0.1-10+rpi1~bpo9~rpt1 (tags/RELEASE_601/final)
Target: armv6-unknown-linux-gnueabihf
Thread model: posix
InstalledDir: /usr/bin

# 32
>>5463
Hey there, welcome. No that should be OK for much of what we're doing. I can probably devise reasonable alternatives for C++14 (your compilers) for things. If something's not working for you please let me know ITT and I'll try to address it for you.

# 33
>'''mlpack''' advanced C++ AI library xpost
>>5730

# 34
An anon mentioned we should start learning testing early (>>5741) so that we're doing things correctly from the beginning. This is good advice and we're going to go ahead and set up a simple project to begin our testing experiments. If you haven't already done so, follow the instructions in this post >>6517 to get ''Catch2'' set up on your machine.

Open Juci and create a new project ''waifu_say''
> #1

We're going to play around with a simplistic mapping of sayings our waifu can say to us, and also begin doing basic testing on it.

-As always, delete the default ''.clang-format'' file that Juci automatically creates in our project directories. This will ensure that the clang-format system picks up and uses our own, better, .clang-format file we have already created in our home directories.
-Copy the two ''amalgamated'' files from the Catch2 local repo into our project directory:
```cpp
cd ~/_prj/waifu_say/
cp ~/_repo/Catch2/extras/*amalgamated.* .```
> #2

We'll be using these two files to perform testing on our software. Let's create a new ''test.cpp'' file and #include that new header file first thing.
```cpp
#include "catch_amalgamated.hpp"```
> #3

Open the ''meson.build'' file and make these two changes:
-Change the C++ standard flag to ''-std=c++2a''
-Add a new executable for the project to build named ''test_say'' and add both the test.cpp & catch .cpp files as it's sources
```cpp
executable('test_say', ['test.cpp', 'catch_amalgamated.cpp'])```
> #4

Go ahead and build now (ctrl+enter). If everything went well, you should see that Juci compiled ''two'' executables for the project this time, ''waifu_say'' & ''test_say''. Note: the very first time compiling with this new header takes a good while b/c raisins. It will go along faster afterwards.
> #5

# 35
>>6519
The author of Catch2 recorded a talk a couple months ago about using ''Test-Driven Design'' for C++
https://www.youtube.com/watch?v=N2gTxeIHMP0
I'd recommend you make the hour or so to watch this talk. We'll be loosely adopting his approach to drive the design of our simple waifu_say class.

Open the ''test.cpp'' file and add a new blank test case:
```cpp
TEST_CASE("Just like make robowaifu") {}```

The test case's description is just a free-form string. It's generally important to name these test cases meaningfully, but we'll just go ahead with this memetic version for now. :^)
Build it. If all went well, you should see some results from Catch2 in the Juci terminal emulator:
```cpp
===============================================================================
test cases: 1 | 1 passed
assertions: - none -

~/_prj/waifu_say/build/test_say returned: 0```

Since Catch2 provides nice coloration, we'll generally be running our tests in terminal shell instead:
```cpp
build/test_say```
> #1

Now let's add a C++ std::map with a few strings that represent things our waifu might say to us into test.cpp:
```cpp
#include <cstdint>
#include <map>
#include <string>

const std::map<uint32_t, std::string> sayings{
    {1, "I love you Oniichan!"},
    {2, "Did you have a hard day Oniichan?"},
    {3, "Oniichan, do your best!"},
    {4, "Poor Oniichan, please get some rest."},
};```
> #2

Let's create our first failing test by adding a (non-existent) ''Robowaifu'' class variable into our test:
```cpp
Robowaifu waifu```

Build it and see that we have our first failing test.
> #3

As Phil Nash mentioned, our ''compiler'' is actually part of our testing system.

Let's get this test to pass by adding an empty Robowaifu class & building again:
> #4

>===
-''add slides link from Phil Nash talk:''
https://levelofindirection.com/refs/tdcpp.html

# 36
>>6520
OK, now let's write our first test assertion ( a ''REQUIRE()'' in Catch2 ). We'd like our waifu simply to ''say'' things to us, so we'll just type that out, using one of the key numbers from std::map ''sayings'':
```cpp
REQUIRE(waifu.say(1));```

Building that gives us our next failing test:
> #1

Ofc, the ''Robowaifu'' class has no function named ''say()'' yet. So let's add that public member function to the class and try again:
```cpp
 public:
  std::string say(uint32_t say_num) const {}```

Building that gives us a lengthy error-spew. Scrolling up, we find the pertinent bit as the first error in the output:
```cpp
In file included from ../test.cpp:5:
../test.cpp: In function ‘void ____C_A_T_C_H____T_E_S_T____0()’:
../catch_amalgamated.hpp:5229:54: error: no match for ‘operator!’ (operand type is ‘std::__cxx11::string’ {aka ‘std::__cxx11::basic_string<char>’})
     } while( (void)0, (false) && static_cast<bool>( !!(__VA_ARGS__) ) )
                                                      ^~~~~~~~~~~~~~```
>protip: Always search for the ''first'' error in a spew. This is usually the culprit.
> #2

The problem is ''' error: no match for ‘operator!' ''' . Wat does this mean? :^)
The problem is that the REQUIRES() is a binary test and needs two parts. We've only given it the first half, but not the second. Basically, we have to provide the string for it to compare the argument ''waifu.say(1)'' against.

OK, let's fix that:
```cpp
REQUIRE(waifu.say(1) == "I love you Oniichan!");```
> #3

Welp trying again and it looks like we're still red (failing). 
```cpp
-------------------------------------------------------------------------------
Just like make robowaifu
-------------------------------------------------------------------------------
../test.cpp:19
...............................................................................

../test.cpp:22: FAILED:
  REQUIRE( waifu.say(1) == "I love you Oniichan!" )
with expansion:
  "" == "I love you Oniichan!"

===============================================================================
test cases: 1 | 1 failed
assertions: 1 | 1 failed```

What now? Looking at the the 'with expansion' section gives us the clue:
```cpp
with expansion:
  "" == "I love you Oniichan!"```
> #4

The first part of the equation is just an empty string "".  Looking at the function body of Robowaifu::say(), we see that we aren't actually returning anything yet. Let's add just enough to make this latest test pass:
```cpp
std::string say(uint32_t say_num) const { return "I love you Oniichan!"; }```
Build and run it now:
```cpp
build/test_say -s``` 
(note the ' -s ' flag. it will show us successful tests too)
> #5

OK, we're back to green again.

# 37
>>6522
Alright, let try a second test assertion now to get to the next failing test:
```cpp
REQUIRE(waifu.say(2) == "Did you have a hard day Oniichan?");```
> #1

We can see we have one pass and one fail from our two assertions. Ofc, the return value from Robowaifu::say() simply returns the correct response for the first item in ''sayings''. Let's use the same (limited) approach to 'fix' the second assertion's failure:
```cpp
  std::string say(uint32_t say_num) const {
    return "Did you have a hard day Oniichan?";
  }```
Re-running the build shows all we've done by this is simply swap the errors for one another ''(note: I reversed the ''REQUIRE()''s inside the test case b/c of an early abort issue with the current devel version)''. This helps us with understanding two things.
A) We need a better approach to our 'solution'.
B) By leaving ''previous'' tests in place, they act as regression-test checks to let us quickly see if any new code breaks something that used to work. In this case it does ofc (the previous ''say()'' output).

So, how to make this work correctly? Juci itself can help us out here. Scrolling up a bit in our code and hovering our mouse over the yellow-squiggles underneath the 'say_num' parameter, we see that the IDE is providing us with the info that say_num is an unused parameter. This is a clue for us: we aren't even referencing the std::map containing our sayings collection, from inside our Robowaifu class yet!
> #2

A C++ std::map provides us with generic containers of pair items. In this specific case, we have a number of strings representing sayings, and they are indexed by the unsigned integer key. 
```cpp
const std::map<uint32_t, std::string> sayings{
    {1, "I love you Oniichan!"},
    {2, "Did you have a hard day Oniichan?"},
    {3, "Oniichan, do your best!"},
    {4, "Poor Oniichan, please get some rest."},
};```

With a map, you can ''find()'' the key, and retrieve the value, pretty much the way a database works. So, next we'll refactor our ''Robowaifu::say()'' member function to use the ''say_num'' parameter and retrieve the correct text string with it.

https://en.cppreference.com/w/cpp/container/map/find

# 38
>>6524
In Modern C++ (17 or greater), an ''if()'' logical test can have two sections; the initializer, and the conditional. This is similar to the way a ''for()'' loop works. If you read the cppreference.com link to map::find() posted above, then you saw that an ''iterator'' is the return type from the find() function. Iterators are kind of like C-pointers for C++, and you use similar syntax for dereferencing them for example. 

Further, a std::map item has two named parts, 'first' and 'second'. First is the key, and second is the value.

Combining all these facts together, and we can write a search test to see if the ''say_num'' parameter was actually found within our map:
```cpp
  std::string say(uint32_t say_num) const {
    if (auto search = sayings.find(say_num); search != sayings.end())
      return search->second;
  }```
This is saying to the system, "Look for this key number. If you find it in the std::map, return true". This is the correct behavior we're looking for ofc.

Re-running our system now shows us that, sure enough, we're back to green.
> #1

Great! We're done right? Well wait, what's this yellow squiggle and warning message?
> #2

Apparently our function has a problem still. Turns out we're only handling behavior for the valid case. What happens if we pass an ''invalid'' number into waifu.say() ? For example, since we currently have only 4 sayings in our map (numbered 1 - 4), what happens if we 'inadvertently' pass in a number not in that range?
```cpp
REQUIRE(waifu.say(9'001) == "Foobar9000");```
> #3

The failing test shows us what our new say() code does with an invalid input key number:
```cpp
with expansion:
  "" == "Foobar9000"```
  
Similar to earlier in our code, the function just returns an empty string. Instead of simply returning ''nothing'' from our function with an invalid input, what if we improved it a little by at least indicating that our waifu doesn't understand the saying number we asked for from her.
```cpp
  std::string say(uint32_t say_num) const {
    if (auto search = sayings.find(say_num); search != sayings.end())
      return search->second;

    return "I don't understand Oniichan...";
  }```
  
Ah, that got rid of the squiggles too. Now our waifu is telling us if she doesn't understand what we just asked for.
> #4

But we're still failing that final test. Sometimes the ''tests themselves'' are the problem. Let's change the invalid, bogus one to use the '''!=''' operator instead and re-run:
```cpp
REQUIRE(waifu.say(9'001) != "Foobar9000");```
> #5

So, seems like we're back to all green and we have a system that will properly look up a valid key and return the correct text to us, and provide a helpful message when we pass in an invalid one (and not break the system). Seems like we're making good progress with our Robowaifu class so far and our tests.

# 39
OK class, I think that's plenty to take in for this time. Hopefully you picked up on some of the basics of unit testing, and driving our C++ code designs with tests. It can guide us into the correct behavior in our systems without us having to figure everything out perfectly in advance.

Next time, we'll expand on ''waifu_say'' project to start associating an anon's '''inputs''' with the desired waifu outputs, and then refactor out our class into it's own header and begin using it independently of the test harness.

Till then, cheers!

# 40
>>6528
Since it may be a bit before I come back with more, I figured I'll go ahead and temporarily post the 3 file's current-state contents, just in case any anons following along are getting stuck.

>main.cpp
```cpp
#include <iostream>

int main() {
  std::cout << "Hello World! \n";
}```

>test.cpp
```cpp
#include <cstdint>
#include <map>
#include <string>

#include "catch_amalgamated.hpp"

const std::map<uint32_t, std::string> sayings{
    {1, "I love you Oniichan!"},
    {2, "Did you have a hard day Oniichan?"},
    {3, "Oniichan, do your best!"},
    {4, "Poor Oniichan, please get some rest."},
};

class Robowaifu {
 public:
  std::string say(uint32_t say_num) const {
    if (auto search = sayings.find(say_num); search != sayings.end())
      return search->second;

    return "I don't understand Oniichan...";
  }
};

TEST_CASE("Just like make robowaifu") {
  Robowaifu waifu;

  REQUIRE(waifu.say(2) == "Did you have a hard day Oniichan?");
  REQUIRE(waifu.say(1) == "I love you Oniichan!");

  REQUIRE(waifu.say(9'001) != "Foobar9000");
}```

>meson.build
```cpp
project('waifu_say', 'cpp')

add_project_arguments('-std=c++2a', '-Wall', '-Wextra', language: 'cpp')

executable('waifu_say', 'main.cpp')
executable('test_say', ['test.cpp', 'catch_amalgamated.cpp'])```

>===
-''fixed operator!=()''

# 41
Just a random anon here, sharing a tidbit of inner workings of computers. 
For those who skipped high school, for our purposes any number to the power of 0 is 1. Mathematicians argue over that, but it doesn't matter to us right now.
An easy way to understand the bit representation of unsigned integers is to know this compact definition, which is rarely peddled around:

Bits are numbered starting from 0, every bit's value is 2 to the power of its number.


This also helps with a fun little detail, to have the machine give you the value of a specific bit, you merely have to shift the number 1 left by the bit's number.
>1 << 0;
Returns 1.
>1 << 8;
Returns 256.

# 42
>>6531
Thanks for the tip Anon. There's a guy Bean Eater who created a simple 8-bit computer from scratch using breadboards and commonly-available ICs. In a couple of the videos about the ALU & A/B registers he deals with one's- and two's-complement number representations.

Playlist is linked here >>1554

# 43
>>6531
>>6532
I might also add there's a great little book that addresses all sorts of interesting things going on inside computers. ''But How Do It Know?''
>>4660

Hopefully, we'll integrate some of it's contents ITT in addition to the two primary books by Stroustrup already being used.

# 44
So the silly test ''REQUIRE(waifu.say(9'001) != "Foobar9000");'' was really just an artifact of the way we grew the code, and isn't really relevant for a proper test. We've already provided for a reasonable result from our class' member function on an invalid input ''"I don't understand Oniichan..."'', so time for a minor refactoring of the test itself.
```cpp
REQUIRE(waifu.say(9'001) == "I don't understand Oniichan...");```
> #1

Recall from Phil Nash's ''Test Driven C++'' talk linked above that there are 3 steps in the primary TDD loop:
-Red
-Green
-Refactor
> #2

Even tests may need refactoring themselves, as we saw above. But we're not done just yet. We have two passing tests about valid inputs (#2 & #1), but we don't really want to try testing every.single.input. Not only would that be a fool's errand, but it doesn't really help us to ''drive the design'', and that's what we're really after here. 

What might be a better approach is to provide a valid input, and then check for both the positive result, and then confirm it's inverse; 'not a negative' result. To put it another way, let's also make sure we don't get a "I don't understand Oniichan..." when we give a valid input. This may seem silly at first, but once code grows big and things begin to change around this approach (testing the positive and negative) can help us smoke out regression bugs we might introduce.

Let's remove one of the redundant positives, and replace it with the 'not a negative' test instead.
```cpp
  REQUIRE(waifu.say(1) == "I love you Oniichan!");
  REQUIRE(waifu.say(1) != "I don't understand Oniichan...");```
OK, that passes and we now can be fairly sure that if we give a valid input, we'll get a valid output.
> #3 #4

# 45
>>6922
OK, now that we've wrung our simple Robowaifu class with it's sole member function out a bit, let's lift both it and the ''sayings'' std::map out into their own files, and we can begin using them outside our test system.

Create two new files in our project 'Robowaifu.hpp' & 'sayings.hpp', (''File > New File''). Cut & paste the Robowaifu class into it's own file, and the sayings std::map into it's own file. You'll also need to add the appropriate C++ library includes for each file as well. Eg:
```cpp
#include <cstdint>
#include <map>
#include <string>```
> #1 #2

Since we've moved the sayings std::map off into it's own file, we'll need to include it into the Robowaifu.hpp file so the class itself can find the sayings data.
```cpp
#include "sayings.hpp"```
> #3

The test file now just contains the test (as we'd like), but we need to add an #include for the new Robowaifu.hpp file so the test can find the new location of the class itself.
```cpp
#include "Robowaifu.hpp"```
> #4

Now let's switch over to ''main.cpp'', the program itself, and after including the Robowaifu.hpp once again, and instantiating a Robowaifu object, we'll try testing the valid sayings and a couple of invalid ones. Everything seems to be working so far:
> #5

Alright, we've lifted our class out of the test itself and begun using it 'in production'. Next we'll start working on anon's ''inputs'', and you'll start seeing why we are using code numbers to index into the possible waifu sayings to us.

Cheers.

# 46
>>7066

# 47
Because I am a programming brainlet, I'm trying my hand at some C. The first exercise is a bugger, and my brain was like "Duurrr Fahrenheit to Celsius then Celsius to Fahrenheit then Fahrenus to Celsyheit and Fahrycels to Heityfahr?"

However, once they introduce the 'for' statement I began to realise that this stuff has a lot of potential. Sure, it took me four hours to figure out how to code two temperature conversion charts, but once they are done, just changing a couple of numbers lets you convert between any temperature in those units! Also, the whole calc can be reversed by only changing three characters. 

At first I was like -_-
But then I was like O_0

# 48
>>10301
Congratulations, Anon. You've opened up a whole new world. You can create entire universes out of your dreams now if you just keep moving forward.

Programming with serious intent at the level of C is easily one of the most creative things you can do as a human being IMO. And C++ is unironically even ''better''!

This isn't a C class ''per se'' but it's pretty likely I can help you out with things if you get stuck. Just give me a shout.

# 49
>>10302
Will do OP, thanks! I'd heard that learning C is best before starting on C++, so I'll just keep on plodding. After all, if your waifu speaks Thai or Russian, then it's best to learn those languages. And if your waifu speaks C/C++...

# 50
'''Bjarne's Big Blue Birb Book;'''
==Wakey-Wakey Exercises== edition

So, since the ~~PPP2~~ '''''B5''''' textbook is literally the best textbook for freshmen learning to do serious programming, it's featured ITT ofc. :^)

Unfortunately, Bjarne has since moved on from teaching and the GUI chapters of the textbook have kind of been languishing since FLTK's API has improved and left novices with some incompatibilities difficult to resolve. For other reasons (..., >>12933) I myself needed to crack open the books and pick these chapters back up. 

I discovered the issue, and so accordingly I'm aiming to fix it so that any Anons here on /robowaifu/ wanting to actually learn to do GUI work from ~~PPP2~~ '''B5''' can do so relatively easily. Bjarne even mentioned on his site that basically 'pull requests are welcome', and so it's not inconceivable I may eventually turn this into a big patch that could show up in the book's support code eventually. **That would be cool! :^)**

Anyway, after a little initial efforts here it is Anon. I plan to eventually keep adding to it until all 5 of the GUI chapters have been completed here.

>chapter.12.3.cpp
```cpp
// The B5 Project
// ==============
// Bjarne's Big Blue Birb Book; Wakey-Wakey Exercises edition  (aka PPP2)

// Filename: book_code/ch12/chapter.12.3.cpp
// ~begins on B5 p 415

//
// This is example code from Chapter 12.3 "A first example" of
// "Programming -- Principles and Practice Using C++" by Bjarne Stroustrup
//

#include "Graph.h"          // get access to our graphics library facilities
#include "Simple_window.h"  // get access to our window library

//------------------------------------------------------------------------------

int main() {
  using namespace Graph_lib;  // our graphics facilities are in Graph_lib

  // Point tl(100, 100);  // to become top left  corner of window
  // Simple_window win(tl, 600, 400, "Canvas");  // make a simple window

  Simple_window win(600, 400, "Canvas");  // make a simple window

  Polygon poly;  // make a shape (a polygon)

  poly.add(Point(300, 200));  // add a point
  poly.add(Point(350, 100));  // add another point  
  poly.add(Point(400, 200));  // add a third point

  poly.set_color(Color::red);  // adjust properties of poly

  win.attach(poly);  // connect poly to the window

  win.wait_for_button();  // give control to the display engine
}

//------------------------------------------------------------------------------

// -Note: The examples and library code here are all the authorship of Bjarne
// Stroustrup. We make no pretensions to being anything other than 'Software
// Repair Technicians', who are simply helping to bring the code 'up to speed'
// and 'into usability' for today. In essence; we're basically just editing the
// code slightly for better compatibility with more modern FLTK versions.
// -For any other contributions we've made in 'packaging-up' the code into our
// unified approach, our standard MIT (Expat) licensing model applies as usual.

// -book sauce:
// https://stroustrup.com/programming.html

// Copyright (2021)
// License MIT (Expat) https://opensource.org/licenses/MIT```
>B5_project-0.1.tar.xz.sha256sum
```cpp
ba6ea168d8e3da248b8c96605eac008ac711611c9e333a7108e381835c0f5ba8 *B5_project-0.1.tar.xz```
''as always, just rename the .pdf extension to .7z then extract files. build instructions are in readme.txt .''
>backup drop onto catbox
https://files.catbox.moe/wffny3.7z

# 51
>>13062
So, I meant to go ahead and do all of Chapter 12's examples before pushing a new version number here, but there were already quite a few changes with just the 4 additional example files that I decided it might be easier to take in at a smaller set of incremental changes. 

Note: I have an unresolved bug where color selections are taking the new color assignments before drawing to the window canvas'. Not sure yet where it's breaking, but I plan to address the issue after I finish posting all of Chapter 12 here first. So, hopefully it will be fixed before we begin Chapter 13 next. :^)

Cheers.

>version_log snippet
```cpp
210913 - v0.1a
---------------
-add '[B5]' tag comments in example codes, to mark our edits/changes
-add chapter.12.7.3-2.cpp
-add public move() function to Shape
-add 'Shape(initializer_list<Point> lst)' ctor to Shape
-add Lines, Text, Axis, Font classes to Graph.h
-#include <initializer_list> in Graph.h
-add chapter.12.7.3-1.cpp
-add chapter.12.7.2.cpp
-add debug comment in 12.3 main()
-add FLTK default screen, Simple_window max dims tests
-minor cleanup of Point
-rm book_srcs_all.cpp from ./book_code/
-add chapter.12.7.1.cpp
-add standard file header to meson.build, test_basic_sanity.cpp, doctest.h
-patch dated command example provided in version.log
-various minor comment & javadoc edits```
>B5_project-0.1a.tar.xz.sha256sum
```cpp
1cf0b08048a8e6151b716dd9d967f9f1d433eebb0bc72ce810ecba7383ab2ab1 *B5_project-0.1a.tar.xz```
''as always, just rename the .pdf extension to .7z then extract files. build instructions are in readme.txt .''
>leaving a dropping in the catbox
https://files.catbox.moe/f96zhn.7z

# 52
>>13106
>are ''not'' taking the new color*
derp

# 53
Alright, so I suppose I may just try to adopt a general standard of making a push here for every 4 new example code files added. The learning curve should be getting a little easier by now if you're following along (even though the code is getting longer, less new ideas).

The cool Function added in for graphing a sine wave is nice. If you examine the definition code in Graph.cpp for implementing the function drawing, you'll see it's really pretty straightforward IMO. No fancy maths needed on your part, the '''std::sin''' function does all that for you already.

>version.log snippet
```cpp
210913 - v0.1b
---------------
-add chapter.12.7.6-1.cpp
-begin debugging line color issue (behavior changed w/ Rectangle)
-add Rectangle struct to Graph.h
-add chapter.12.7.6.cpp
-add chapter.12.7.5.cpp
-add Function struct to Graph.h
-add chapter.12.7.4.cpp
-add Window label re-assignment test
-add standard file header to test_all.cpp
-various minor comment, javadoc, & formatting edits/cleanups```
>B5_project-0.1b.tar.xz.sha256sum
```cpp
6f5f69fa882b8cb39db03a41f2a6299114590377275c1b13e4c1c049350a71e4 *B5_project-0.1b.tar.xz```
''as always, just rename the .pdf extension to .7z then extract files. build instructions are in readme.txt .''
>just leaving a fresh dropping in the catbox :^)
https://files.catbox.moe/d3ub7c.7z

# 54
Well, thankfully I seemed to have gotten ahead of the game a little bit and found the basic line color issue (it was in the Shape class). So hopefully that's sorted, but I'll continue looking into it further. So, hopefully it looks like there need be any real timeout break between Ch12 & Ch13 postings here?

>version.log snippet
```cpp
210914 - v0.1c
---------------
-add Text label re-assignment test
-need Graph_lib namespace specifier for Font details 
-add chapter.12.7.8-2.cpp
-add chapter.12.7.8-1.cpp
-(tentative) apparently found the basic drawing color issue? (others may remain)
-add + change access level for some member functions in Shape
-add chapter.12.7.7.cpp
-patch East-const in error()
-add chapter.12.7.6-2.cpp
-various minor comment, javadoc, & formatting edits/cleanups```
>B5_project-0.1c.tar.xz.sha256sum
```cpp
602c141c7baf0f4566e494ddb5cd0ae117583795bfabb02c8e6665c2389d631c *B5_project-0.1c.tar.xz```
''as always, just rename the .pdf extension to .7z then extract files. build instructions are in readme.txt .''
>the making of the droppings into the catboxes :^)
https://files.catbox.moe/ma3p1s.7z

# 55
>>13131
>there ''needn't'' be *

# 56
Alright we've come to the end of Chapter 12 with this post, and so I'm going to just leave it at the 3 example files. It was a fair bit of work getting Image, etc. working actually. I'm only showing 2 window capps b/c the ''chapter.12.7.9-2.cpp'' example turned up some kind of bug that crashes the program if an image display is moved off-screen. Therefore to bypass, I just avoid the issue (moving image) which basically would leave us with an exact duplicate of the 9-1 image so w/e.

It's probably due to some change in FLTK's API during the intervening timeframe I'd guess just offhand. And quite frankly, I'm concerned that it could turn into a real tar-baby for me, so I'm going to shelve running it down to the ground for now. Since I've been making steady progress thus far, I'd like to avoid any potential 'morasses in evil swamps' just yet. :^) Hopefully I'll be surprised in the end and it will be just a simple fix, possibly only a masking operation beforehand or something.
> #2

I also had a go at a couple of the utility functions related to Images display. I think they'll prove workable over time.
> #3

So anyway, it's good to get to the end of this first chapter in the GUI section of the textbook. Unsurprisingly, there's a nice learning curve to get over with all the new concepts, etc., and hopefully things are already getting easier for you as you work along with us Anon. Cheers.

>version.log snippet
```cpp
210915 - v0.1d
---------------
-add Ellipse major/minor axes test
-#include <cmath> in Graph.h
-add Circle, Ellipse, Mark to Graph.h/.cpp
-add chapter.12.7.10.cpp
-debug moving image offscreen
-add chapter.12.7.9-2.cpp
-refactor get_encoding(), can_open() utilities
-#include <fstream>, <cstdlib> in Graph.cpp
-add Image, Suffix, and some support utilities to Graph.h/.cpp
-add FLTK images library support in meson.build
-add 2 image resources to ./assets/
-add ./assets/ directory
-add chapter.12.7.9-1.cpp
-various minor comment, javadoc, & formatting edits/cleanups```
>B5_project-0.1d.tar.xz.sha256sum
```cpp
fac5b79b783052a178bf0a1691735609737fc30bbdf92bf75c0be1113a7ed13b *B5_project-0.1d.tar.xz```
''as always, just rename the .pdf extension to .7z then extract files. build instructions are in readme.txt .''
>having of the droppings into the catboxes is much better than of being into the streets :^)
https://files.catbox.moe/fy4bp7.7z

# 57
So let's get started with '''B5''' chapter 13 right Anon? I think for the chapter openers now on, I'll just use 3 example files so I can post the chapter's overview page from the book for each one. Seems like a good idea since Bjarne himself has already put in a lot of effort to clearly state the chapter's intentions. I'm highly unlikely to be able to improve on that tbh.
> #1

I'm skipping the first window's capp, since basically it's almost identical visually to the second one (this is intentional, he was making a point about two different classes '''Line''' & '''Lines'''). 

As for 'versioning' the files, I'm simply planning to add a tick number one for each chapter. No real reason to do anything more complicated here, since this is really just a progress dump and version numbers are only being used to mark time with.

>verson.log snippet
```cpp
210915 - v0.2
---------------
-add chapter.13.4.cpp
-add chapter.13.3-2.cpp
-add chapter.13.3-1.cpp
-add Line to Graph.h
-add chapter.13.2.cpp
-add ./book_code/ch13 directory
-patch East-const in various functions
-minor logic consolidation in get_encoding()
-add (overlooked) standard file footer to chapter.12.7.10.cpp
-various minor comment, javadoc, & formatting edits/cleanups```
>B5_project-0.2.tar.xz.sha256sum
```cpp
d44054ad59bcadab4beaf4e542406e1e551e2617ec17db0d4e04706248020972 *B5_project-0.2.tar.xz```
''as always, just rename the .pdf extension to .7z then extract files. build instructions are in readme.txt .''
>i'll probably just drop '''''(sic!)''''' making all the bad poo jokes. :^)
https://files.catbox.moe/1nik6f.7z

# 58
So, nothing much to add here news-wise. Everything's going smooth as silk for now pretty much Anon.

Hope you are understanding the concept of the classes' designs, and how we're intentionally keeping FLTK "at arm's distance" for our own Graphics/GUI system being engineered here. This is a good thing, and actually makes it pretty easy ('''read:''' relatively inexpensive) to switch out back ends later on for a better-fitting one, etc., if needs be. This approach to systems abstraction brings lots of flexibility to the table for us both as software and systems engineers.

Anyway, here's the next 4 example files from the set.

>version.log snippet
```cpp
210916 - v0.2a
---------------
-add chapter.13.6.cpp
-add chapter.13.5-3.cpp
-add chapter.13.5-2.cpp
-add chapter.13.5-1.cpp
-add Ellipse visibility set/read testing
-add Ellipse color set/read testing
-various minor comment, javadoc, & formatting edits/cleanups```
>B5_project-0.2a.tar.xz.sha256sum
```cpp
9e14254bf7064783fffafb5af45945675df0855624170a0c92e0f8d957abced5 *B5_project-0.2a.tar.xz```
''as always, just rename the .pdf extension to .7z then extract files. build instructions are in readme.txt .''
>catbox backup file:
https://files.catbox.moe/ms1dlc.7z

# 59
So, I got nothing Anon **except to say that this puts us halfway through Chapter 13  :^)**. Here's the next 4 example files from the set. 

>version.log snippet
```cpp
210916 - v0.2b
---------------
-add Rectangle fill color set/read testing
-add chapter.13.9-1.cpp
-add chapter.13.8-2.cpp
-add chapter.13.8-1.cpp
-add chapter.13.7.cpp
-patch overlooked 'ch13' dir for the g++ build instructions in meson.build
-various minor comment, javadoc, & formatting edits/cleanups```
>B5_project-0.2b.tar.xz.sha256sum
```cpp
197c9dfe2c4c80efb77d5bd0ffbb464f0976a90d8051a4a61daede1aaf9d2e96 *B5_project-0.2b.tar.xz```
''as always, just rename the .pdf extension to .7z then extract files. build instructions are in readme.txt .''
>catbox backup file:
https://files.catbox.moe/zk1jx2.7z

# 60
The 13.10-1 example doesn't actually create any graphics display, so I'll skip ahead to the 13.10-2 example instead on the final one for this go. I kind of like that one too since it shows how easy it is to create a palette of colors on-screen.

>version.log snippet
```cpp
210917 - v0.2c
---------------
-add Line line style set/read testing
-add as_int() member function to Line_style
-add chapter.13.10-2.cpp
-add Vector_ref to Graph.h
-add chapter.13.10-1.cpp
-add chapter.13.9-4.cpp
-add chapter.13.9-3.cpp
-add chapter.13.9-2.cpp
-patch the (misguided) window re-labeling done in chapter.13.8-1.cpp
-various minor comment, javadoc, & formatting edits/cleanups```
>B5_project-0.2c.tar.xz.sha256sum
```cpp
45d1b5b21a7b542effdd633017eec431e62e986298e24242f73f91aa5bacaf42 *B5_project-0.2c.tar.xz```
''as always, just rename the .pdf extension to .7z then extract files. build instructions are in readme.txt .''
>catbox backup file:
https://files.catbox.moe/l7hdf0.7z

# 61
Don't think things could really have gone any smoother on this one. I never had to even look at the library code itself once, just packaged up the 4 examples for us. Just one more post to go with this chapter.

>version.log snippet
```cpp
210918 - v0.2d
---------------
--add chapter.13.13.cpp
--add chapter.13.13.cpp
--add chapter.13.12.cpp
--add chapter.13.11.cpp
-various minor comment, javadoc, & formatting edits/cleanups```
>B5_project-0.2d.tar.xz.sha256sum
```cpp
5fbcf1808049e7723ab681b288e645de7c17b882abe471d0b6ef0e12dd2b9824 *B5_project-0.2d.tar.xz```
''as always, just rename the .pdf extension to .7z then extract files. build instructions are in readme.txt .''
>catbox seems to be down for me atm so no backup this time
n/a

# 62
>>13294
>catbox seems to be down for me atm so no backup this time
It came back up.
https://files.catbox.moe/ty7nqu.7z

# 63
OK another one ticked off the list! :^) Things went pretty smoothly overall,  except I realized that I had neglected to add an argument to the FLTK script call for the g++ lads. Patched up that little oversight, sorry Anons. This chapter has 24 example files, so about half again as large as Chapter 12 was.

So, the main graphic image in the last example (Hurricane Rita track) covers up the 'Next' button for the window, but it's actually still there. Just click on it's normal spot and the window will close normally. There are only 3 examples for this go, so images are a little shy on the count for this post.

>version.log snippet
```cpp
210918 - v0.2e
---------------
-add Font size set/read testing
-patch missing '--use-images' arg in g++ build instructions in meson.build
-add 2 image resources to ./assets/
-add chapter.13.17.cpp
-add chapter.13.16.cpp
-add chapter.13.15.cpp
-various minor comment, javadoc, & formatting edits/cleanups```
>B5_project-0.2e.tar.xz.sha256sum
```cpp
6bd5c25d6ed996a86561e28deb0d54be37f3b8078ed574e80aec128d9e055a78 *B5_project-0.2e.tar.xz```
''as always, just rename the .pdf extension to .7z then extract files. build instructions are in readme.txt .''
>catbox backup file:
https://files.catbox.moe/a4h1dr.7z

