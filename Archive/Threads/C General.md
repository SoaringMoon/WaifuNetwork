# 1
'''C++ Resources general'''

The C++ programming language is currently the primary AI-engine language in use.

isocpp.org/get-started
https://archive.is/hp4JR

stackoverflow.com/questions/388242/the-definitive-c-book-guide-and-list
https://archive.is/OHw9L

en.cppreference.com/w/
https://archive.is/gt73H

www.youtube.com/user/CppCon
https://archive.is/QGynC

''BTW if you're new to C++ and you're stuck on Windows (either you can't or won't upgrade to Linux) then you can at least incorporate a good, open shell into your system to begin with so you can follow along. Start at this link, and if you have any questions just ask ITT:''
www.msys2.org/
https://archive.fo/p3EUc

# 2
BTW, for anons who are interested in learning C++ but don't know where to start this book is literally the best (serious) beginner programming book in existence IMO. And it just so happens to use C++ as the basis to teach the art of programming. It has my highest recommendation for anyone new to programming.

http : //www.stroustrup.com/Programming/

# 3
I discovered this book a few months ago and bought a copy. I've been progressing through it as time allows. I'm now pretty much convinced that the new Ranges features coming up in C++20 will make programming functional in C++ both elegant and easy. Sample chapter:
https://livebook.manning.com/book/functional-programming-in-c-plus-plus/chapter-1/

A couple of reasons why functional is going to be important to us here on /robowaifu/ is that
1. The data structures are immutable (and basically optimized). This has huge implications for both run-time perf, and avoids metric shittons of potential complications for things like multithreading.
2. Composability. Functional approaches allow you to easily take a ''Generative'' or ''Metaprogramming'' approach to software development. Namely, you can pass an entire '''program''' into another program as an argument, and get an entirely new thing never seen before out the other end.

These things were always doable in C++ ofc, but the new features in C++20 will make the syntax clean, simple & elegant.

# 4
>>149
>and avoids metric shittons of potential complications for things like multithreading and ''security''*
ftfm.

Looks like Manning made ch7 available too.
https://livebook.manning.com/book/functional-programming-in-c-plus-plus/chapter-7/

# 5
Quick drop-in from Morgan Stanley where the C++ language creator Bjarne Stroustrup shills the language.
via isocpp.org

# 6
>>192
Do you dislike C++? If so, what are the problems you have with it?

>//-------------
==SFW board, keep it spoilered anon.==

# 7
>>193
No not really. It's a remarkable language, actually. It's biggest problem is that big. I mean yuge. That makes the learning curve to get to where you can do big projects with it pretty steep. There are a lot of easier languages to learn.

# 8
>>194
Right. I see. You basically have to be a master at it to use it properly. Do you feel that learning C++ is not worth the time?

# 9
>>195
Guess it depends on what you want to do actually. If you want to create a fancy webpage then JavaScript would be better and something like Python would be better for a webscraper or some kind of utility program like that. On the other hand from what this board seems like it's trying to do maybe C++ is just right who knows. I know it's going to be a lot of very hard work though, for sure.

# 10
>>196
Would programming a /robowaifu/ be best done using C++?

# 11
>>197
Maybe so.

# 12
There are two primary sources online, the actual standard itself, and cppreference .

While the C++ Committee isn't part of the ISO, like all other groups dealing with them they must literally give all their hard work over to these kikes if they want it to be adopted as an official international standard. So, the ''published'' standard itself is controlled by (((ISO))) and they want your sheqels. Lots of them (CHF198 for one pdf file!). Fucking jews man.

However, the C++ Foundation also actively maintains the ''draft'' of the standard (aka the 'working paper'), and that information is freely available via their site:
isocpp.org/std/the-standard
If you're autistic enough you can even compile your own pdf from the up-to-the-minute Latex sources:
github.com/cplusplus/draft

If you're not quite that /lit/, you can just use the online version maintained by one of the Committee members:
eel.is/c++draft/
Finally, you can also download his pdf version of the full draft standard as well:
github.com/timsong-cpp/cppwp

The above standard is, ofc, the final word in what is or isn't C++ .

But imo at least as important as the standard itself is the site cppreference.com . It addresses every feature of the language past and present--and even future. It's written by professionals (many of whom are on the Committee itself), for professionals. It's literally indispensable for a working C++ developer:

en.cppreference.com/w/
BTW, it's also the single best reference to the C language that's out there as well.

>tl;dr
The standard itself and cppreference are the only goto places for the C++ language definition, accept no substitutes.

# 13
>>214
>github.com/timsong-cpp/cppwp
I'm autistic enough that I didn't just want to post the latest draft right here, b/c it will quickly go out of date as the work progresses. I wanted anons to be able to find the authority itself.

But here's the latest from a little over a month ago atm.
>file related

# 14
For the anon**s** learning C++ right now, here's a little utility I just wrote so I thought I would post it here so you could have a look at some simple C++ code and ask me anything about it.

So, I wanted to be able to get a listing of all thread subjects on the board, ranked by reply count and then by image count. C++ has a perfect container type for databases of this sort, the multimap:
en.cppreference.com/w/cpp/container/multimap

I simply clean up the raw input file a little, then go through and save out the reply counts and image counts and thread subjects. Multimap automatically keeps everything sorted by the key ([reply_count, image_count] in this case), and then I just dump that container out in order into a new file.

Here's the code, study it and ask questions.

# 15
[code]#include <fstream>
#include <iostream>
#include <map>
#include <sstream>
#include <string>
#include <utility>
#include <vector>

// Returns true if all 3 tags are found inside the input line.
// ex. statline:    R: 5 / I: 2 / P: 1 [R] [G] [-]
bool is_stat_line(const std::string& line)
{
  bool p{false}, r{false}, i{false};
  const std::vector<std::string> tags{"P:", "R:", "I:"};

  for (const auto& e : tags) {
    auto find_tag_it = line.find(e);
    if (find_tag_it != std::string::npos) {  // we have a tag

      if (e == tags[0])  // page position
        p = true;
      if (e == tags[1])  // reply count
        r = true;
      if (e == tags[2])  // image count
        i = true;
    }
  }

  return (p && r && i);
}

// This function assumes we already have a verified valid statline via
// is_stat_line()
void load_rep_img(const std::string& stat_line,
                  std::pair<std::size_t, std::size_t>& rep_img)
{
  // load a vector with the individual elements from the stat_line
  std::stringstream ss{stat_line};
  std::vector<std::string> elems{};
  //
  std::string elem{};
  while (ss >> elem)
    elems.emplace_back(elem);

  // load the std::pair with stat values pulled from the vector
  bool have_r{false}, have_i{false};
  for (const auto& e : elems) {
    // if the flag is already set, then this next element will be the data value
    if (have_r) {
      rep_img.first = std::stoull(e);
      have_r = false;
    }
    else if (have_i) {
      rep_img.second = std::stoull(e);
      have_i = false;
    }

    // set the flags as needed
    if (e == "R:")
      have_r = true;
    //
    if (e == "I:")
      have_i = true;
  }
}

std::vector<std::string> load_lines(std::fstream& ifs)
{
  std::vector<std::string> lines{};
  std::string line{};

  // Store all non-blank lines in the order they come (compact the file)
  while (std::getline(ifs, line))
    if (!line.empty())
      lines.emplace_back(line);

  return lines;
}

// Clean the raw input textfile copypasted out from the board catalog via a
// browser. Ignore extraneous information, while saving out a list of thread
// subjects, ranked by post count, then by image count, ascending order.
int main()
{
  // file in
  const std::string infile{"catalog_raw"};
  std::fstream ifs(infile, ifs.in);
  if (!ifs.is_open()) {
    std::cerr << "failed to open input\n";
    return -1;
  }
  // Store only non-blank lines from the input file
  const std::vector<std::string> lines{load_lines(ifs)};

  // The target final container for writing file output from
  std::multimap<std::pair<std::size_t, std::size_t>, std::string> thread_map{};

  // Determine if a line is the statistics line for a thread. If it is, grab the
  // stats, then the NEXT line will be the thread subject line to store in the
  // multimap target.
  bool stat_found{false};
  std::pair<std::size_t, std::size_t> rep_img{};
  //
  for (const auto& e : lines) {

    if (stat_found) {  // we have the thread's subject line presently
                       // (during the subsequent iteration _after_ statline)
      // rep_img already loaded during the previous iteration.
      thread_map.emplace(rep_img, e);
      stat_found = false;
      continue;
    }

    stat_found = is_stat_line(e);

    if (stat_found)  // retain the stats for the next iteration
      load_rep_img(e, rep_img);
  }

  // file out
  const std::string outfile{"catalog_ranked"};
  std::fstream ofs(outfile, ofs.out);
  //
  for (const auto& e : thread_map)
    ofs << "[" << e.first.first << "] [" << e.first.second << "]"
        << "     " << e.second << '\n';
}

// TODO: Replace my clumsy hackery with a std::find_if() + lambda, and a
// std::transform(). When C++20 is out, convert the entire caller to
// functional code using the Ranges library.
[/code]

# 16
>>521
To use this code yourself on a board to get it's ranked thread subject list, follow these steps:

'''1.''' Get set up to compile C++ code ofc, since this is C++ code. The isocpp.org/get-started link ITT can help you if you've never done that before.
'''2.''' Open the catalog page of a board and '''ctrl+a''', then '''ctrl+c''' to copy all it's text to the system clipboard.
'''3.''' Open a plaintext editor, create a new file, then '''ctrl-v''' to paste the clipboard contents into that file.
'''4.''' Save the file to some directory where you can also save the file from the next step. Name it ''catalog_raw'', no extensions. The code expects to find this exact name.
'''5.''' Select all the code from the above post following the same copy+paste+save idiom, and create a file named ''rank_catalog.cpp''. Be sure to copy every single character.
'''6.''' Open the directory where you've saved these two files inside a terminal (command prompt) and enter this command:
[code]g++ rank_catalog.cpp -o rank_catalog -std=c++11[/code]
This will create an executable file named ''rank_catalog'' (on Wangblows it will be ''rank_catalog.exe'').
'''7.''' Execute the program.
[code]./rank_catalog[/code]
A new textfile will be generated for you named ''catalog_ranked''. Voilà, you now have a ranked copy of the board's threads. Repeat as desired for other catalogs (you don't have to go through the compiling process again, just save the ''catalog_raw'' file out again with the new data, then re-execute the program).

NOTE: This code will output the thread ''comment'' for a thread with no subject. It's a simple utility for my own purposes, and I didn't need to handle that corner case.

# 17
>>526
Heh, I just discovered this doesn't work properly on Wangblows, b/c it's a shitty OS that doesn't use line-endings properly like any decent OS would. I'll leave it to you filthy ''NSA_Botnet-OS''™ users to find the fix haha. (there is a simple one) **protip: save the ''raw_catalog'' textfile out differently, you mong**

# 18
Also, one other point. Some imageboards don't have all three of the "R:", "I:", and "P:" fields in the catalog list (as used here on julay and was the case with 8ch). This code will fail if they are not all three present. If this is the case for a board you'd like to get the ranked list from, then modify the '''bool is_stat_line(const std::string&)''' function to match your needs, recompile & re-execute.

[code]// Returns true if all 3 tags are found inside the input line.
// ex. statline:    R: 5 / I: 2 / P: 1 [R] [G] [-]
bool is_stat_line(const std::string& line)
{
  bool p{false}, r{false}, i{false};
  const std::vector<std::string> tags{"P:", "R:", "I:"};

  for (const auto& e : tags) {
    auto find_tag_it = line.find(e);
    if (find_tag_it != std::string::npos) {  // we have a tag

      if (e == tags[0])  // page position
        p = true;
      if (e == tags[1])  // reply count
        r = true;
      if (e == tags[2])  // image count
        i = true;
    }
  }

  return (p && r && i);  // <== start here, anon! :^)
}
[/code]

# 19
Q: ''What C++ editor/IDE do you recommend, Anon?''
A: I use juCi++ on the Debian derivative, Ubuntu. Big project management I just do inside the terminal, with tmux+Vim as my goto there.

gitlab.com/cppit/jucipp

[code]git clone --recursive https://gitlab.com/cppit/jucipp
mkdir jucipp/build
cd jucipp/build
cmake -DCMAKE_CXX_COMPILER=g++ ..
make
sudo make install
[/code]

# 20
StackOverflow is, in general, also the best resource for finding C++ questions that have already been asked by someone before.
stackoverflow.com/questions/tagged/c%2b%2b

Also, the CPP subreddit.
reddit.com/r/cpp/
**I know, I know**
**:^)**

Various members of the ISO C++ Standards Committee actively participate in both these places.

>>559
Also, here's one article on the (only vaguely related) topic of GUI systems.
insights.dice.com/2016/11/18/5-cross-platform-guis-for-c/
https://archive.is/dKD4f

# 21
If you are already up and going writing good C++ programs, you should probably take a look at Runtime-Compiled C++. This will could be highly useful for more or less interactively developing robowaifu software.
runtimecompiledcplusplus.blogspot.com/
https://archive.is/aJytC

Set it up on your box:
''Prereqs:'' (on my Debian deriv, see 'Getting-started-with-Runtime-Compiled-C-Plus-Plus.md' on the github's wiki for more details):
[code]sudo aptitude install libfreetype6-dev libx11-dev libgl1-mesa-dev libglu1-mesa-dev  libglfw-dev[/code]

'''Clone and build:'''
[code]git clone https://github.com/RuntimeCompiledCPlusPlus/RuntimeCompiledCPlusPlus.git
cd RuntimeCompiledCPlusPlus/Aurora
mkdir build && cd build && cmake .. && make[/code]

Now, you should be able to successfully play with the SimpleTest demo in the Examples directory. See the 'Demo-Tutorials.md' on the code wiki for more details.

>pics related. before, during, and after making a minor code change on the fly with the included demo game under RCCpp's example dir.

# 22
>>562
RCCpp's Vimeo:
vimeo.com/runtimecompiledcplusplus/videos
https://archive.is/3X8PA

# 23
CppCon 2017
www.youtube.com/playlist?list=PLHTh1InhhwT6bwIpRk0ZbCA0N2p1taxd6

# 24
CppCon 2018
www.youtube.com/playlist?list=PLHTh1InhhwT6V9RVdFRoCG_Pm5udDxG1c

# 25
Can you get a job writing C++? I just started learning to code because I need a job and it's all confusing.

# 26
>>573
You can indeed. Glassdoor has over 12,000 current openings for senior C++ devs.
https://www.glassdoor.com/Job/jobs.htm?suggestCount=0&suggestChosen=false&clickSource=searchBtn&typedKeyword=senior+software+engineer+c%2B%2B&sc.keyword=senior+software+engineer+c%2B%2B&locT=&locId=&jobType=

>I just started learning to code because I need a job
Unfortunately, C++ takes a long time to master b/c it's yuge. It has many qualities that make it great for designing and developing robowaifu systems, but ''"I'm going to quickly get a great job doing this shit!"'' isn't one of them.

You'd probably be better off going for some kind of web-stack developer if you're committed to a software career and you need income from that as quickly as possible anon.

# 27
>>574
Thanks heaps for the rundown, I'll work on webshit first.

# 28
>>578
nprb anon, good luck!

# 29
BTW, if you are here and you're very math-inclined, there is an excellent book on programming called ''Elements of Programming''. This year (2019) the Addison-Wesley publishers declined keeping it in print and reverted the rights back to the authors. They have made it freely available online, and also sell a paperback version now.
http://elementsofprogramming.com/
by Stepanov & McJones
It is one of the best books on programming in existence, period. It's up there with Knuth's ''TAOCP'' tomes in terms of its rigor, but it's much, much smaller and far more approachable, imo.
The book uses C++ to discuss the mathematical and logical basis of programming, in the manner of Euclid's ''The Elements'' treatise.

# 30
>>648
I feel like TAOCP is more like a bible or an encyclopedia you can search the information you need in. Or maybe I haven't read enough of it to appreciate the overall structure and internal logics of it.

# 31
>>649
that's probably a reasonable way to think about it anon. certainly the thousands and thousands of pages of the complete set (thus far) isn't just light reading heh.

# 32
I just discovered they have a C++ section. They've been pretty helpful to me in the past learning HTML & Python, so maybe this is helpful for someone too.
www.w3schools.com/cpp/default.asp

# 33
Well I finally took the plunge the other day and had a go at picking up Meson basics. I had been using CMake pretty consistently for a few years.

I must say that not only is it very straight forward to pick up and use Meson, but the Ninja build system is excellent. It's fast, and it's smart about managing big builds.

Eventually we'll have multi-million line codebases in our robowaifus. Having a build system like Ninja, and Meson's concise multi-language project management capabilities are convincing me already this is the way to go.

>pics related
Bjarne uses FLTK as a GUI framework for teaching in PPP2, but it can be a challenge to get it working correctly in a generalized way w/o resorting to FLTK's own build scripts. By using Meson, I was able to get it going with literally 3 simple lines in the .build file.

My example code is based on FLTK's basic sample:
www.fltk.org/doc-1.3/basics.html

Meson's official guide:
mesonbuild.com/Quick-guide.html

# 34
>>1057
Ehh, may as well post the code itself just in case.

> main.cpp
[code]#include <memory>
#include <string>

#include "muh_fltk.h"

int main(int argc, char** argv)
{
  using namespace std::literals;
  const std::string hi_str{"Hello, /robowaifu/!"s};

  auto window = std::make_unique<Fl_Window>(500, 180);
  auto box = std::make_unique<Fl_Box>(20, 40, 450, 100, hi_str.c_str());
  //
  box->box(up_box);
  box->labelfont(bold + italic);
  box->labelsize(36);
  box->labeltype(shadow_lbl);
  //
  window->end();
  window->show(argc, argv);

  return Fl::run();
}[/code]

> muh_fltk.h
[code]#pragma once

#include <FL/Fl.H>
#include <FL/Fl_Box.H>
#include <FL/Fl_Window.H>

// Let's end all the shouting, shall we? :^)
auto up_box = Fl_Boxtype::FL_UP_BOX;
auto shadow_lbl = Fl_Labeltype::_FL_SHADOW_LABEL;
auto bold = FL_BOLD;
auto italic = FL_ITALIC;[/code]

> meson.build
[code]project('test_fltk', 'cpp',
  default_options : 'cpp_std=c++14')

add_project_arguments('-Wall', '-Wextra', language: 'cpp')

# Get FLTK libraries
cxx = meson.get_compiler('cpp')
fltk_dep = cxx.find_library('fltk')

srcs = ['main.cpp', ]

exe = executable('test_fltk', srcs,
  dependencies : fltk_dep)

test('basic', exe)[/code]

# 35
>>1057
Lastly, here's the guy who created the Meson project talking about it during CppCon2018.

https://www.invidio.us/watch?v=SCZLnopmYBM

# 36
>>1057
>>1058
No good reason not to use concrete objects in this case, actually.

[code]#include <string>

#include "muh_fltk.h"

int main()
{
  using namespace std::literals;
  const std::string win_str{"/robowaifu/ fltk base test"s};
  const std::string hi_str{"Hello, /robowaifu/!"s};

  Fl_Window window{500, 180, win_str.c_str()};
  Fl_Box box{20, 40, 450, 100, hi_str.c_str()};
  //
  box.box(up_box);
  box.labelfont(bold + italic);
  box.labelsize(36);
  box.labeltype(shadow_lbl);
  //
  window.show();

  return Fl::run();
}[/code]

# 37
>>1070
1) Why use std::string when you are only using the const char * values?
2) Why this: [code]const std::string ...{"..."s};[/code]? You are;
a) Constructing a string via operator ""s
b) Constructing a string from the newly constructed string
3) Do not use something like "bold + italic". If you get used to this you will make mistakes. Use "bold | italic". You shouldn't be aliasing FLTK constants in the first place.

# 38
>>1058
because of the string literal operator ''s'' in this case keeps any problems from occurring using the slashes of '/robowaifu/' inside the string itself. otherwise i wouldn't bother. btw it works with ''any'' characters inside the string w/o worrying about side-effects, for example back-slashes (normally used for escapes ofc)
https://en.cppreference.com/w/cpp/string/basic_string/operator%22%22s

btw, if i know i have a c++17 compliant compiler on the system, then it's better to use a std::string_view instead.
https://en.cppreference.com/w/cpp/string/basic_string_view

# 39
>>1072
>Use "bold | italic". You shouldn't be aliasing FLTK constants in the first place.
actually '+' is the correct operator here, not '|', and the aliasing serves my purposes in this case as I indicated in the comment.

# 40
>>1072
BTW, there's an even more powerful string literal idiom for C++11, though clumsier:

[code]const std::string bar{R"foo(!@@#@$#%$^&%&^%*&%?????////<<<|||)foo"};[/code]

https://en.cppreference.com/w/cpp/language/string_literal

# 41
>>1074
Well I'll eat crow, that's the weirdest API for setting flags on a font that I've ever seen.
>>1075
Not sure how this is useful here. You can just do
[code]
const char foo[] = "My program";
[/code]
and now you don't even need to use .c_str(). No need to add an extra constructor call to your program startup.

# 42
>>1076
>>1076
FLTK is pretty different but it's actually a great choice for an almost universal GUI framework. I think Bjarne made a good choice of it for PPP.

>const char foo[] = "My program";
ehh, fair enough. but

[code]const char foo[] = "Hello, \robowaifu\!";[/code]
would sure create trouble.

And besides, this is C++, not C. Raw pointers should be strictly avoided inside user code in current_year. Keep them inside library code. And quite frankly, std::string is amazing IMO.

# 43
>>1078
[code]const char foo[] = "Hello, \\robowaifu\\!";[/code]
There.
>Raw pointers should be strictly avoided inside user code in current_year.
Please get rid of this mindset. Raw pointers will never truly go away since they're a part of your hardware's memory model. Jumping through hoops and incurring performance costs to avoid raw pointers will just cause you more trouble in the future. I'm not saying "oh use raw pointers for everything STL bad", but there are some situations where having a raw pointer doesn't hurt whatsoever.
>And quite frankly, std::string is amazing IMO.
It's just a struct holding a char*, a length and a capacity. It has its own place. You don't need to run std::basic_string<char>::basic_string(stdd::basic_string<char>) for every string you create, especially since you only care about the char* '''in this context'''.

# 44
>>1079
mine's prettier. :^)
"make programming enjoyable" is a fundamental design goal of C++. 

>please get rid of this
no thanks. i programmed in C for two years before learning C++. i'll stick with the latter. i'm well aware of the need for raw pointers but as i said, keep them in library code where they rightfully belong. 

std::string is doing much more than just that tbh. RAII is so fundamental the the C++ Tao that i'll never go back. i'll literally go out of my way to write extensive library code first just so the effort of writing large codebases becomes much easier and more reliable.

# 45
>>1080
"Make programming enjoyable" is a fundamental design goal of C++? Funny, whenever I write code in C++ I feel like I am pulling out my nails one by one.
>no thanks.
Oh well, carry on then. Good luck.

# 46
>>1081
kek. OK I misquoted.
>"...'''more''' enjoyable." :^)

Heh, I understand. Like other large languages it takes time and effort to master. IMO it's time & effort well-spent. There are no perfect languages, but if you're going to create ginormous systems like robowaifus will be, then C++ is literally the best language in the world to use for it. That's why I'm here, actually.

# 47
>>521
Ehh, I just realized that the final file out segment of this code would be semantically more sensible using C++17's structured binding feature. So, rather than using obtuse terms like ''e.first.second'' etc, the output stream can use more specific ones like ''img'' & ''subj''. The final types within the stream are unchanged from the original ('''size_t, size_t, & string'''), only now they have more suggestive variable naming.

[code]// file out
const std::string outfile{"catalog_ranked"};
std::fstream ofs(outfile, ofs.out);
//
for (const auto& e : thread_map) {
  const auto [rep, img]{e.first};
  const auto& subj{e.second};

  ofs << "[" << rep << "] [" << img << "]"
      << "     " << subj << '\n';
}[/code]

https://en.cppreference.com/w/cpp/language/structured_binding

# 48
>>1072
>>1076
>>1079
>>1081
BTW, thanks anon. I appreciate the input, it's welcome anytime.

# 49
Ehh, I just realized I overlooked mentioning the C++ Core Guidelines. It's a group effort on the part of top C++ developers to coalesce the language around a set of core principles the language is remarkably good at, and to move away from the legacy language issues (primarily still there to ensure compatibility with C) that have been troublesome in the past.

While led by several top ISO C++ Committee members (founded by Bjarne himself as well as the committee Chair Herb Sutter), it is a non-sanctioned **pirate ''ARRRGH, Matey!''** organization. It is actively maintained and has now become a strong influence guiding the future of C++, as the founders intended. Think of it as an agile way for the ''Good Guys''™ to skirt the bureaucratic Committee members.

Here's an example guideline related to the incredibly important computer science topic of '''RAII''':
github.com/isocpp/CppCoreGuidelines/blob/master/CppCoreGuidelines.md#Re-raii

# 50
>>1270
BTW, there's a nicely rendered view of the guidelines available.
isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines

# 51
>using c++

# 52
>>1281
>not using c++

# 53
>>1281
>>1282
>not using BASIC

# 54
>>1281
>>1282
>>1333
plebeians all of you.

# 55
>>1281
>>1282
>>1333
>>1334
>not using brainfuck

# 56
>>1335
Touché. Not sure how effective that would be at creating masterful, monster powerful robowaifus though anon.

# 57
>>1335
>>1337 **LEET**
What exactly is brainfuck?

# 58
>>1338
>What exactly is brainfuck?
A meme.

# 59
>>1339
>A meme.
Oh, thanks for clearing that up.

# 60
>>1338
>ikr mr. 1337++
brainfuck is le ebin LEETHAXXORZ programming **maymay** language.

hello_brainfuck.bf
[code]++++++++++[>+++++++>++++++++++>+++>+<<<<-]>++.>+.+++++++..+++.>++.<<+++++++++++++++.>.+++.------.--------.>+.>.[/code]

# 61
OK, there's a thread begun about the ArchBot Imageboard Migration Tool up on fatchan now.
https://fatpeople.lol/tech/thread/76.html

# 62
>>1342
Are we moving to fatchan? I am confused.

# 63
>>1343
No ofc not (well, as long as julay stays up). Why do you ask anon?
>t.Chobitsu

# 64
>>1344
I misinterpreted the original statement when I saw the word "migration". Sorry about that. Thanks for clearing things up.

# 65
>>1345
The tool itself is intended to support board migrations eventually, so yeah. But no that doesn't mean ''we'' are migrating atm. I'm basically creating this tool to help the masses of BOs migrate ''their'' boards off of 8kun and onto a better **bunker** site somewhere else. The first step ofc is to be able to grab a full copy of the original board in a hurry, and that's what this phase of the tool does. 

No worries, thanks for asking anon. I didn't realize I was generating confusion.

# 66
>>1342
I'm curious why you posted that on the /tech/ board over there when the one here has some activity.

https://julay.world/tech/

# 67
>>1347
Because the site Admin Tom there is awesome. He understands what /tech/ is actually about.

# 68
This is my first post at /robowaifu/, although i have been lurking since long before the falling of 8ch.
being a c++ programmer myself, i followed your example and tried meson (and also fltk, which is much more simple and effective than any other gui library i have seen so far).
compared with autotools, meson is not only faster, but incredibly less painful to work with.
all of this being said, the small program i made to try to use those tools is a simple text editor operated through keyboard shortcuts. it's aim is to be something like microsoft's notepad, with a focus on minimalism, customization and ease of use. i will be adding new features these days. the repository of the project https://gitlab.com/schinopsis/shlnot
i have also been tinkering with nlp, and will be posting in the AI thread once i get something that works

# 69
>>1397
Hi anon glad to hear the example worked out for you. One of the chief obstacles we have to overcome is managing a tremendous amount of complexity and dynamic activity all going on simultaneously--the vast majority of which has a hard real-time or near real-time performance constraint. Coffee languages won't do it. Neither in my opinion will C. We have to be able to build systems with both great performance and great abstraction. Otherwise we'll never succeed as a small team. C++ is quite literally the perfect language to build robowaifu software in.

 Yeah, I think FLTK may not have that native look, but the '''FAST''' in ''Fast Light ToolKit'' certainly is well-named. It will serve us well imo. Yeah, Meson is pretty great. I'm frankly a little angry with myself for not picking it up earlier it would have made many things simpler haha.

Interesting little project thanks for sharing it anon. I'll clone it and have a look. A good editor is obviously an important item for any projects we'd do here that need a lot of keyboard input. The little project I've been working on will need some kind of graphical text editor soon tbh.

Yes, AI and especially NLP will be pretty vital to differentiating a robowaifu from just some kind of sexbot. Conversation and companionship are primary goals right? Looking forward to your posts.

Glad to meet you anon, welcome aboard.

# 70
>>1397
pretty sweet anon. i love the little 'micro-breadcrumbs' in the file browser. ever think about having VIM shortcuts? that would turn this into a great little editor imo.

# 71
OK, so here's the newest version of the imageboard tool. It's called ''BUMP'' now. For any of you guys following along, please let me know if you find any issues with it etc.
Cheers

https://files.catbox.moe/akc819.zip

# 72
-removed libstdc++ dependency
-fully integrated functions inside the classes, no ''archbot.h'' file now
-slightly faster performance now when checking on thread bumps

https://files.catbox.moe/zlugd0.xz

# 73
-Reworked data containers to pure vectors
  -a bit faster, and much simpler code now
-Added version into config file
-Consolidated Page class to hold data
-Simplified JSON management
[code]5ac6c8e3faa99c294e92c4b5f385c7306ea5b6c5b8f369c6322d3e022b2c9034 BUMP-0.1c.tar.xz[/code]
https://files.catbox.moe/tuutsb.xz

# 74
-Added basic HTTP error reporting for catalog.json input

[code]be0c406f005c5b4ceaee3c449ec824ceabb3f83e87210893c078bb08406f3dd7 BUMP-0.1d.tar.xz[/code]
https://files.catbox.moe/fmht9v.xz

# 75
Have an important new release today.
[code]191106 - v0.2
-------------
-add a .sites.config file to map differing JSON schemas, to allow diff. IB s/w;
  -supports lynxchan
  -supports jschan (new)
  -supports vichan/openib (new)
  -direct archival support now included for:
      julay.world
      prolikewoah.com
      fatpeople.lol
      anon.cafe
      christchannel.xyz
      late.city
      sportschan.org
      floridachan.com
      erischan.org
      vch.moe
      8kun.net
      jthnx5wyvjvzsxtu.onion
      
-more resilient in the face of network errors
-add use of OP's comment as thread directory name if subject field is blank
-extend thread directory ID pad suffix to adapt to higher post ID numbers
-add download progress message scroll
-add a file 404 record for a failed download attempt (skips re-attempting later)

1edee477f9de708d73b8c0555a0eaba7c91d7e437b114e209b6501c4f427112d BUMP-0.2.tar.xz
https://files.catbox.moe/1g4lqu.xz[/code]

# 76
>>1460
Add useragent to tool, and patched minor bug.
[code]191106 - v0.2a
--------------
-patch '<="bump_v0.2"' bug
-add bump useragent

dc09d8f6ec38f5e4d020eaf3d187fa8404d21944c23427f914a8bb820d51848a BUMP-0.2a.tar.xz
https://files.catbox.moe/9xfs89.xz[/code]

# 77
>>1460
>>1461
Hey, this is Robi. Wanna help me add support for different imageboards on https://gitgud.io/rb/MultiScraper ? I am trying to also add support for importing scraped threads.

# 78
>>1462
Oh hey there Robi. Sorry I missed this. Sure, but I'm not much of a dev outside of C++ tbh. If you think that would work then I'm your guy.

# 79
>>1462
Hey Robi, question. I've never run an IB before (or even installed one). Do you think I'll need an install of Lynxchan running to help out with this project?

# 80
[code]191115 - v0.2b
--------------
-direct archival support now included for:
    endchan.net
    8kun.us

-add notification for new thread discovery
-add apostrophe handling in filenames
-patch bug with filename extension handling    
-patch minor bug causing unnecessary rechecking of un-bumped threads
-add 'file empty' record similar to file 404 record (skips re-attempting later)
-add minor optimization when force-rechecking a thread's files
-extend DL timeout to 90 secs to better accommodate endchan's large filesizes
-add special check for MongoDB crash
-add thread's ID prefix to the 'file_404s.json' file
-add 'deleted' file download bypass
-patch minor bug w/ force re-checking of threads

https://files.catbox.moe/0y7z6j.xz
0b43b392ea2b69de1bb7d83c1c4714e473763629060c7f05f5dde4bd32a1dfa1 BUMP-0.2b.tar.xz[/code]

Since this is taking me longer to get the duplicate file management in place, I'll just put it off until a v0.2c release and go ahead and put what I have out there now, since endchan.net is now included and there's a couple of bugfixes that help alleviate some nuisance. Cheers.

# 81
[code]191121 - v0.2c
--------------
-direct archival support now included for:
    lainchan.org
    arisuchan.jp
    8kun.top

-add timeout error code 9001 - interim step towards better error correction
-extend DL timeout out to 120sec to pick up even longer downloads (good for TOR)
-add space handling in filenames
-make minor output message adjustments
-add somewhat better validation of 'catalog.json' files
-add facility for cleanly re-acquiring any accidentally deleted thread folders
f76855c247ea4243f5e3fb98b52a1ebdd4759e86d815de148e7d77f9d6e96495 BUMP-0.2c.tar.xz
https://files.catbox.moe/bvccj0.xz[/code]

Alright, I've decided to go ahead and make another subrelease earlier since 8kun.top seems to be working atm. I'll be doing a pretty significant revamping of the Page class' data management, so I'll hold off on the dupe files handling until then.

# 82
>>1523
Hmm, looks like that was a bit premature. Apparently VanwaTech's system allows browsers OK for 8kun.top, but is rejecting BUMP--probably all types of bots. Might need to play around with the useragent, oh well. 

Sorry if I got anyone's hopes up **what I get for not testing heh** (it still works fine with 8kun's onion service jthnx5wyvjvzsxtu.onion, use torify).

# 83
Someone complained that they were interested in the software, but they were confused how to get everything set up to build BUMP. I created a INSTALL file for Ubuntu that I hope helps. If anything's unclear or you experience some difficulty with these instructions, I'd appreciate knowing about it, thanks. I'll include this file when I make the next release.

>Install.txt
[code]Here are detailed setup instructions for BUMP from a clean install of Ubuntu 19.10:

1. Execute this command from a terminal:
  sudo apt-get install meson ninja-build libcurl4-openssl-dev libfltk1.3-dev libjsoncpp-dev

-this will get you set up with required developer libraries

2. Clone and build juci++ (instructions located at):
  https://gitlab.com/cppit/jucipp/blob/master/docs/install.md#debianlinux-mintubuntu

-installing this will get you set up with the basic latest dev environment and other rereqs, 
not to mention being a powerful little FOSS C & C++ IDE.

3. Clone and build curlpp:
  git clone https://github.com/JosephP91/curlcpp.git
  cd curlcpp/ && mkdir build && cd build
  cmake .. && make
  sudo make install

4. May as well use Juci to build BUMP software since you have Juci now. From the directory 
where you extracted the (inside) BUMP archive, run this from the terminal:
  juci .

5. Inside Juci, compile and run the BUMP code:
  Project > Compile and Run (Ctrl+Return)

-you should see an error about 'program argument error' from BUMP. These can be added under:
  Project > Set Run Arguments
(for example):
  bump julay.world ck

You should be all set to archive literally any board for every site included in the .sites.config 
file. BUMP is pretty smart about figuring out what needs to be updated in future runs and only grabs 
what's changed. Also, it will probably be easier to just run BUMP from the terminal afterwards tbh.[/code]

# 84
BTW there's a new /robowaifu/-oriented C++ & OpenGL project begun in the RW Simulator thread (just in case any C++ anons here missed it).
>>1814

# 85
I've been working on learning functional C++ code here's a simple example of the idea.

[code]int main()
{
  vector<int> ints{0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
  auto even = [](int i) { return 0 == i % 2; };
  auto square = [](int i) { return i * i; };

  for (int i : ints | filter(even) | transform(square)) {
    cout << i << ' ';
  }

  cout << '\n';
}[/code]

this outputs:
[code]0 4 16 36 64 100[/code]

I really like this style of coding and I'm really glad ranges is finally in C++20.
https://en.cppreference.com/w/cpp/ranges
Until GCC 9.3 arrives, I'm just using Eric Niebler's library for now.

code:
https://privatebin.net/?e15accfb31d0132c#EW58fwas6hHJdr8AA8qgQuPHV18hbmtTJr1NZNJRZbim

# 86
heh for some reason private bin ditched the includes:
[code]#include <iostream>
#include <vector>

using std::cout;
using std::vector;

#include <range/v3/view/filter.hpp>
#include <range/v3/view/transform.hpp>

using namespace ranges;
using views::filter;
using views::transform;[/code]

# 87
>>1945
here's another toy example that demonstrates ranges lazy-evaluation:
[code]// lazyEvaluation.cpp
#include <cstdio>
#include <tuple>

#include <range/v3/all.hpp>
using namespace ranges;

decltype(auto) pairs(const char* foo)
{
  return views::zip_with([](int c, auto i) { return std::make_pair(c, i); },
                         views::c_str(foo), views::ints(0, unreachable));
}

int main()
{
  for (const auto [c, i] : pairs("ROBOWAIFU")) {
    printf("(%c,%i) ", c, i);
  }

  printf("\n\n");
}[/code]

outputs:
[code](R,0) (O,1) (B,2) (O,3) (W,4) (A,5) (I,6) (F,7) (U,8)[/code]

the '''views::ints(0, unreachable)''' call is an iota-view from zero to infinity, but because of lazy evaluation it only returns the proper numbers of elements.

# 88
The C++20 standard was finalized last month. I think it addresses a couple of key features that have long been missing, modules & coroutines. Modules are a fundamental game-changer for the entire C culture IMO. Coroutines have been done using C++ in one form or another for decades but always as some type of custom solution. Having them in the standard itself will help dismantle proprietary-only approaches, and will certainly improve concurrency in general. Personally, ranges are the biggest change to my own programming style so far, but it's not really something fundamental like modules, but rather more of a sophistication layered on top of Stepanov's breakthroughs.

https://isocpp.org//blog/2020/02/bjarne-stroustrup-on-cpp20s-significance

https://invidio.us/watch?v=03BtQljH2oA

# 89
>>1994
>The C++20 standard was finalized last month
A significant number of committee members post on the r/cpp subreddit  **i know, w/e :^)**
I rendered a pdf of the page discussing the Prague meeting.
old.reddit.com/r/cpp/comments/f47x4o/202002_prague_iso_c_committee_trip_report_c20_is/

there are also a number of important discussions going on in the working groups that will have a future impact in AI/ML & embedded using the standard C++ library, and therefore are important for the future of robowaifus. EG:
http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2020/p1708r2.pdf
http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2020/p2072r0.pdf
http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2020/p1709r2.pdf

cheers.

# 90
>>1999
meant to add this link on the ''deterministic exceptions in c++'' proposal. this need is a significant issue in the real-time kernel of a robowaifu, and will be a huge boon if adopted in the standard.
https://www.research.ed.ac.uk/portal/files/78829292/low_cost_deterministic_C_exceptions_for_embedded_systems.pdf

# 91
>>1994
Here's a pretty nice item about C++20 ranges. I learned a few things.
https://hannes.hauswedell.net/post/2019/11/30/range_intro/

# 92
https://github.com/fffaraz/awesome-cpp

# 93
https://cpp-taskflow.github.io/cpp-taskflow/index.html
https://github.com/cpp-taskflow/cpp-taskflow

# 94
>>2024
>main.cpp

[code]#include <taskflow/taskflow.hpp>  // Cpp-Taskflow is header-only

int main()
{
  tf::Executor executor;
  tf::Taskflow taskflow;
  auto [A, B, C, D] = taskflow.emplace(
      []() { std::cout << "TaskA\n"; },  //  task dependency graph
      []() { std::cout << "TaskB\n"; },  //
      []() { std::cout << "TaskC\n"; },  //          +---+
      []() { std::cout << "TaskD\n"; }   //    +---->| B |-----+
  );                                     //    |     +---+     |
                                         //  +---+           +-v-+
  A.precede(B);  // A runs before B      //  | A |           | D |
  A.precede(C);  // A runs before C      //  +---+           +-^-+
  B.precede(D);  // B runs before D      //    |     +---+     |
  C.precede(D);  // C runs before D      //    +---->| C |-----+
                                         //          +---+
  executor.run(taskflow).wait();
  return 0;
}[/code]

> meson.build

[code]project('taskflow', 'cpp')

add_project_arguments('-std=c++2a', '-Wall', '-Wextra', language: 'cpp')

cxx = meson.get_compiler('cpp')
thrd_dep = cxx.find_library('pthread')

executable('taskflow', 'main.cpp', dependencies : thrd_dep)[/code]

>outputs

[code]TaskA
TaskC
TaskB
TaskD[/code]

# 95
>>2027

# 96
https://gitlab.com/libeigen/eigen

# 97
Intel has sponsored the book now, so it's free for anyone interested in TBB (also opensauce now).

https://link.springer.com/book/10.1007%2F978-1-4842-4398-5
https://github.com/oneapi-src/oneTBB

# 98
>>2028
BTW, for anyone who's never dabbled into the incredibly complex world of concurrency and parallelization, this model's approach is remarkable in it's ease of use & resiliency. i haven't had a chance to profile anything with it just yet, but according to the published numbers in their paper, it's also notably higher performance than the two major parallelization/concurrency frameworks OpenMP & TBB.

# 99
>>2020
Once we get into a large system of complex dynamics and having to sort out in realtime lots and lots of signal needles inside noise haystacks, I may look into this libraries performance as an optimization.
https://github.com/orlp/pdqsort

# 100
>>2120

# 101
Another curated list of C++ libraries. The location itself of the list adds a fair measure of credence to the legitimacy of the selections.
https://en.cppreference.com/w/cpp/links/libs

# 102
>>215
I realized I hadn't posted an updated a copy here since C++20 was voted in. So, I just personally rendered the typeset from the official TeX draft sources themselves https://github.com/cplusplus/draft , so this is literally as current atm as anywhere else. Read it right here on /robowaifu/ first **nerds**! :^) 
>Working Draft, Standard for Programming Language C++, 2020-05-15, 1'834pp

# 103
[code]C++

Several C++20 features have been implemented:
  P1668R1, Permitting Unevaluated inline-assembly in constexpr Functions
  P1161R3, Deprecate a[b,c]
  P0848R3, Conditionally Trivial Special Member Functions
  P1091R3, Extending structured bindings
  P1143R2, Adding the constinit keyword
  P1152R4, Deprecating volatile
  P0388R4, Permit conversions to arrays of unknown bound
  P0784R7, constexpr new
  Concepts, including P0734R0, P0857R0, P1084R2, P1141R2, P0848R3, P1616R1, P1452R2
  P1301R4, [[nodiscard("with reason")]]
  P1814R0, class template argument deduction for alias templates
  P1816R0, class template argument deduction for aggregates
  P0960R3, Parenthesized initialization of aggregates
  P1331R2, Allow trivial default initialization in constexpr contexts
  P1327R1, Allowing dynamic_cast and polymorphic typeid in constexpr contexts
  P0912R5, Coroutines (requires -fcoroutines)

Several C++ Defect Reports have been resolved, e.g.:
  DR 1560, lvalue-to-rvalue conversion in ?:
  DR 1813, __is_standard_layout for a class with repeated bases
  DR 2094, volatile scalars are trivially copyable,
  DR 2096, constraints on literal unions
  DR 2413, typename in conversion-function-ids
  DR 2352, Similar types and reference binding
  DR 1601, Promotion of enumeration with fixed underlying type
  DR 330, Qualification conversions and pointers to arrays of pointers
  DR 1307, Overload resolution based on size of array initializer-list
  DR 1710, Missing template keyword in class-or-decltype
  
New warnings:
  -Wmismatched-tags, disabled by default, warns about declarations of structs, classes, and class templates and their specializations with a class-key that does not match either the definition or the first declaration if no definition is provided. The option is provided to ease portability to Windows-based compilers.
  -Wredundant-tags, disabled by default, warns about redundant class-key and enum-key in contexts where the key can be eliminated without causing an syntactic ambiguity.
  
G++ can now detect modifying constant objects in constexpr evaluation (which is undefined behavior).

G++ no longer emits bogus -Wsign-conversion warnings with explicit casts.

Narrowing is now detected in more contexts (e.g., case values).

Memory consumption of the compiler has been reduced in constexpr evaluation.

The noexcept-specifier is now properly treated as a complete-class context as per [class.mem].

The attribute deprecated can now be used on namespaces too.

The ABI of passing and returning certain C++ classes by value changed on several targets in GCC 10, including AArch64, ARM, PowerPC ELFv2, S/390 and Itanium. These changes affect classes with a zero-sized subobject (an empty base class, or data member with the [[no_unique_address]] attribute) where all other non-static data members have the same type (this is called a "homogeneous aggregate" in some ABI specifications, or if there is only one such member, a "single element"). In -std=c++17 and -std=c++20 modes, classes with an empty base class were not considered to have a single element or to be a homogeneous aggregate, and so could be passed differently (in the wrong registers or at the wrong stack address). This could make code compiled with -std=c++17 and -std=c++14 ABI incompatible. This has been corrected and the empty bases are ignored in those ABI decisions, so functions compiled with -std=c++14 and -std=c++17 are now ABI compatible again. Example: struct empty {}; struct S : empty { float f; }; void f(S);. Similarly, in classes containing non-static data members with empty class types using the C++20 [[no_unique_address]] attribute, those members weren't ignored in the ABI argument passing decisions as they should be. Both of these ABI changes are now diagnosed with -Wpsabi.[/code]

# 104
>>3187
forgot sauce.
https://gcc.gnu.org/gcc-10/changes.html

# 105
>>3187
I neglected to list the improvments in libstdc++
[code]Runtime Library (libstdc++)

Improved experimental C++2a support, including:
  Library concepts in <concepts> and <iterator>.
  Constrained algorithms in <ranges>, <algorithm>, and <memory> (thanks to Patrick Palka).
  New algorithms shift_left and shift_right (thanks to Patrick Palka).
  std::span (thanks to JeanHeyd Meneide).
  Three-way comparisons in <compare> and throughout the library.
  Constexpr support in <algorithm> and elsewhere (thanks to Edward Smith-Rowland).
  <stop_token> and std::jthread (thanks to Thomas Rodgers).
  std::atomic_ref and std::atomic<floating point>.
  Integer comparison functions (cmp_equal, cmp_less etc.).
  std::ssize, std::to_array.
  std::construct_at, std::destroy, constexpr std::allocator.
  Mathematical constants in <numbers>.
Support for RDSEED in std::random_device.
Reduced header dependencies, leading to faster compilation for some code.[/code]

# 106
>>3187
>>3188
>>3248
https://gcc.gnu.org/onlinedocs/libstdc++/manual/status.html#status.iso.2020

# 107
Codeplay has a Community Edition of their SYCL (single-source heterogeneous computing--ie, run your standard C++ code directly on GPUs) implementation. SYCL is an open standard controlled by Khronos.
https://developer.codeplay.com/home/
https://www.khronos.org/sycl/

# 108
>>3286
Example raytracer built using this setup.
https://www.codeplay.com/portal/05-19-20-ray-tracing-in-a-weekend-with-sycl-basic-sphere-tracing

# 109
>>3286
>SYCL
>related
https://github.com/codeplaysoftware/syclacademy

https://www.invidio.us/watch?v=1RqdVEDY5vg&t=1s

# 110
>>3248
I finally installed GCC10.1 today and this now works right out of the box:

>muh_ranges.cpp
[code]#include <iostream>
#include <ranges>
#include <vector>

using std::views::filter;
using std::views::transform;

int main() {
  std::vector ints{0, 1, 2, 3, 4, 5};

  auto even = [](int i) {
    return 0 == i % 2;
  };

  auto square = [](int i) {
    return i * i;
  };

  for (int i : ints | filter(even) | transform(square)) {
    std::cout << i << ' ';
  }

  std::cout << std::endl;
}[/code]

>outputs:
[code]0 4 16[/code]

All that needs to be done with your build file to enable this  is simply to specify C++20 as the standard:

>meson.build
[code]project('muh_ranges_tst', 'cpp')

add_project_arguments('-std=c++20', '-Wall', '-Wextra', language: 'cpp')

executable('muh_ranges_tst', 'muh_ranges.cpp')[/code]

This has been a long wait and I'm pretty stoked tbh. While there are a '''lot''' of other improvements to C++20, ranges was the biggest one for me personally. This will literally change all my future C++ code for the better. Give it a couple more standard revs and it will probably be easier to read in most cases than even Python.

# 111
>>3688

# 112
>>3682
The dream is alive. :^)

# 113
>>3682
>>3693
I just found out you can integrate the ranges piping directly on the primary argument for the ''for_each()'' algo:

[code]#include <algorithm>
#include <iostream>
#include <ranges>
#include <vector>

using std::ranges::for_each;
using std::ranges::sort;
using std::views::filter;
using std::views::transform;

auto print = [](const auto e) {
  std::cout << e << ' ';
};

auto even = [](const int i) {
  return 0 == i % 2;
};

auto square = [](const auto i) {
  return i * i;
};

int main() {
  std::vector ints{5, 7, 4, 2, 8, 6, 1, 9, 0, 3};

  sort(ints);
  for_each(ints | filter(even) | transform(square), print);

  std::cout << std::endl;
}[/code]

>outputs:
[code]0 4 16 36 64[/code]

# 114
Any professional C++ developers who have needed to solve determinate template specialization (at compile-time ofc), or have had to wade through 100+ long error messages in the past will appreciate C++20 concepts. You can use any of the builtin concepts, create your own, and also compose them:

>muh_constraints.cpp
[code]// https://en.cppreference.com/w/cpp/language/constraints
#include <concepts>
#include <iostream>
#include <type_traits>

using uint = unsigned;

template <class T>
concept Integral = std::is_integral<T>::value;

template <class T>
concept SignedIntegral = Integral<T> && std::is_signed<T>::value;

template <class T>
concept UnsignedIntegral = Integral<T> && ! SignedIntegral<T>;

// constrained C++20 function template
template <SignedIntegral T>
void z(T) {
  std::cout << "signed\n";
}

// constrained C++20 function template
template <UnsignedIntegral T>
void z(T) {
  std::cout << "unsigned\n";
}

int main() {
  z(1);
  z(uint(1));

  std::cout << std::endl;
}[/code]

>outputs:
[code]signed
unsigned[/code]

# 115
Normal functions and template functions can effectively be equivalent now in C++20. Consider a trivial GCD example.

Though calculating a greatest common divisor can be tedious and error-prone for the non-maths types **like me**, the standard library provides a GCD function, but it's on you the programmer to ensure the arguments passed to it satisfy specific constraints beforehand, or the code is either undefined or ill-formed. Tn the past this maybe meant writing verbose tests and perhaps specializing template code, but with C++20 concepts, you can now combine constraints (such as Integral) with the ''auto'' keyword, and get template functions directly by just writing normal functions.

This is a big step towards true unification of generic programming and standard programming. In the history of the language until now, these have generally been pretty distinct. Note the remark in the std::gcd, and how it's satisfied by the ''Integral'' constraint we created.

>gcd_foo.cpp
[code]/*https://en.cppreference.com/w/cpp/numeric/gcd
Computes the greatest common divisor of the integers m and n.

Remarks
If either M or N is not an integer type, or if either is (possibly
cv-qualified) bool, the program is ill-formed.
*/

#include <iostream>
#include <numeric>
#include <type_traits>

// C++20 concept
template <typename T>
concept Integral = std::is_integral<T>::value;

using std::cout;

// C++20 constrained (normal) function
Integral auto muh_gcd(Integral auto m, Integral auto n) {
  return std::gcd(m, n);
}

int main() {
  cout << "gcd(1,0): " << muh_gcd(1, 0) << '\n';
  cout << "gcd(-100,100): " << muh_gcd(-100, 100) << '\n';
  cout << "gcd(10,100): " << muh_gcd(10, 100) << '\n';
  cout << "gcd(1071, 462): " << muh_gcd(1071, 462) << '\n';

  // ill-formed, and will be caught at compile-time with muh_gcd()
  // cout << "gcd(3.14,6.28): " << muh_gcd(3.14, 6.28) << '\n';
  // cout << "gcd(true,false): " << muh_gcd(true, false) << '\n';

  cout << std::endl;
}[/code]

>outputs:
[code]gcd(1,0): 1
gcd(-100,100): 100
gcd(10,100): 10
gcd(1071, 462): 21[/code]

# 116
>>3712
Again note, this is all generated template code in the end. These calls are ''pre-computed as constants at compile-time''. '''No runtime costs'''. Multiply that by billions of items, and the value of normal_functions==generic_functions starts to come into focus.

# 117
Note that when using C++20 concepts, the C++ compiler will still properly select functions from the candidates just as normal. Consider an overload to add two parameters:

[code]#include <iostream>
#include <string>
#include <type_traits>

template <typename T>
concept Arithmetic = std::is_arithmetic<T>::value;

using std::cout;

// C++20 constrained function
Arithmetic auto muh_add(Arithmetic auto A, Arithmetic auto B) {
  cout << "Arithmetic\t";
  return A + B;
}

// C++17 generic function
auto muh_add(auto A, auto B) {
  cout << "auto\t\t";
  return A + B;
}

int main() {
  cout << "muh_add(6, 5): " << muh_add(6, 5) << '\n';         // ints
  cout << "muh_add(5.5, 5): " << muh_add(5.5, 5) << '\n';     // doubles
  
  std::string foo{"robo"}, bar{"waifu"};
  cout << "muh_add(foo, bar): " << muh_add(foo, bar)<< '\n';  // strings
  
  cout << std::endl;
}[/code]

>outputs
[code]muh_add(6, 5): Arithmetic	11
muh_add(5.5, 5): Arithmetic	10.5
muh_add(foo, bar): auto		robowaifu[/code]

Of the 3 calls to muh_add(), for the first two the compiler chooses the Arithmetic constrained function (and each type uses the overloaded operator '+'). For the last one the compiler correctly determines that a std::string is ''not'' an Arithmetic type and finds the second, generic candidate. This function uses the overloaded operator '+' as well for concatenating the two strings.

# 118
>>3704
>>3712
>>3717
BTW, if any Anons want to dabble around with concepts, be aware these examples are merely expository-only, and not intended for production. Basically, don't roll-your-own when you don't have to. Even when you do, you should be composing the new concepts out of the official standard library ones. 
(see this list https://en.cppreference.com/w/cpp/concepts )

For example, there is already a ''std::integral'' concept in the C++20 standard.
https://en.cppreference.com/w/cpp/concepts/integral

# 119
==Curated C++ Performance List==
Maintained by Bartłomiej Filipek, whose no slouch in this domain himself.
https://github.com/fenbf/AwesomePerfCpp

# 120
Bjarne just released a mini-synopsis of C++ over the last ~15yrs. 168p.

>By 2006, C++ had been in widespread industrial use for 20 years. It contained parts that had survived unchanged since introduced into C in the early 1970s as well as features that were novel in the early 2000s. From 2006 to 2020, the C++ developer community grew from about 3 million to about 4.5 million. It was a period where new programming models emerged, hardware architectures evolved, new application domains gained massive importance, and quite a few well-financed and professionally marketed languages fought for dominance. How did C++ ś an older language without serious commercial backing ś manage to thrive in the face of all that?
>This paper focuses on the major changes to the ISO C++ standard for the 2011, 2014, 2017, and 2020 revisions. The standard library is about 3/4 of the C++20 standard, but this paper’s primary focus is on language features and the programming techniques they support. The paper contains long lists of features documenting the growth of C++. Significant technical points are discussed and illustrated with short code fragments. In addition, it presents some failed proposals and the discussions that led to their failure. It offers a perspective on the bewildering flow of facts and features across the years. The emphasis is on the ideas, people, and processes that shaped the language.
>Themes include efforts to preserve the essence of C++ through evolutionary changes, to simplify its use, to improve support for generic programming, to better support compile-time programming, to extend support for concurrency and parallel programming, and to maintain stable support for decades’ old code.
>The ISO C++ standard evolves through a consensus process. Inevitably, there is competition among proposals and clashes (usually polite ones) over direction, design philosophies, and principles. The committee is now larger and more active than ever, with as many as 250 people turning up to week-long meetings three times a year and many more taking part electronically. We try (not always successfully) to mitigate the effects of design by committee, bureaucratic paralysis, and excessive enthusiasm for a variety of language fashions.
>Specific language-technical topics include the memory model, concurrency and parallelism, compile-time computation, move-semantics, exceptions, lambda expressions, and modules. Designing a mechanism for specifying a template’s requirements on its arguments that is sufficiently flexible and precise yet doesn’t impose run-time costs turned out to be hard. The repeated attempts to design łconceptsž to do that have their roots back in the 1980s and touch upon many key design issues for C++ and for generic programming.
>The description is based on personal participation in the key events and design decisions, backed by the thousands of papers and hundreds of meeting minutes in the ISO C++ standards committee’s archives.

==>---==
Actually, this looks to be an addition to ACM's next HOPL, which is an important and relatively rare (the next HOPL will be only the 4th in the ACM's 70+ years) event. If so, and if I'm not entirely mistaken, then that puts Bjarne into the sole unique club of having 3 entries in HOPL. Along with his Turing Award that marks quite a legacy for his career.

# 121
>>3855
>Actually, this looks to be an addition to ACM's next HOPL, which is an important and relatively rare (the next HOPL will be only the 4th in the ACM's 70+ years) event. If so, and if I'm not entirely mistaken, then that puts Bjarne into the sole unique club of having 3 entries in HOPL. Along with his Turing Award that marks quite a legacy for his career.
Both now confirmed.

>''"...With this paper, C++ becomes the first and only language to be presented three times at HOPL and I become the first and only person to present three times. HOPL happens every 15 years. The other papers are now accessible as the Proceedings of the ACM on Programming Languages, Volume 4, Issue HOPL, June 2020: https://dl.acm.org/toc/pacmpl/"''

http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2020/p2184r0.pdf

# 122
>>4116
final edit here.
>

# 123
How are you supposed to run this on a microcontroller inside a robots head?

# 124
>>4123
Hey Anon, so we're kind of divided as a group about where to place the compute resources for a robowaifu. Some of us think we should keep the sensitive SBCs inside a shielded little 'breadbox' ''inside'' the robowaifu's chest to keep it safe from RF interference and physical shock/damage. Others of us think the biomemetic approach is best and want to put the SBCs inside the head. The little microcontrollers can (and will) be distributed around the robowaifu's body generally near where they are needed, and all networked together.

Just fyi, we have a thread about these devices.
>>16
>Single board computers & micro-controllers

# 125
>>648
Not sure why I didn't just post the book itself.

# 126
C++20 ranges has a nice & clean calling convention for binary_search() now:
[code]binary_search(haystack, needle)[/code]
Be sure to sort your container first ofc, or it's undefined behavior. Here's a trivial usage example:

[code]#include <algorithm>
#include <iostream>
#include <vector>

using std::cout;
using std::vector;

using std::ranges::binary_search;
using std::ranges::sort;

int main() {
  vector haystack{3, 5, 9, 4, 1};
  sort(haystack);

  vector needles{1, 2, 3};
  for (const auto needle : needles) {
    cout << "Searching for " << needle << '\n';

    if (binary_search(haystack, needle))
      cout << "Found " << needle << '\n';
    else
      cout << "no dice!\n";
  }
}[/code]

# 127
C++ finally added designated initializers, which makes the arguments self-documenting ''at the caller site''. This is a big help in code-reasoning, especially if a specific ctor has a long list of parameters. I(t also allows the args to be passed in any order I believe).
[code]// https://en.cppreference.com/w/cpp/language/aggregate_initialization
// sauce: https://caiorss.github.io/C-Cpp-Notes/Libraries-and-featuresCPP17.html

#include <iostream>
#include <string>

struct Point2D
{
  float x;
  float y;

  friend std::ostream& operator<<(std::ostream& os, Point2D const& p) {
    return os << "Point{x = " << p.x << ", y = " << p.y << "} "
              << std::endl;
  }
};

class Product
{
public:
  Product(int id, std::string name, double price)
      : m_id(id)
      , m_name(name)
      , m_price(price) {}

  int         id() const { return m_id; }
  double      price() const { return m_price; }
  std::string name() const { return m_name; }

private:
  int         m_id;
  std::string m_name;
  double      m_price;
};

int main() {
  std::cout << std::boolalpha;

  Point2D p1{.x = 2.5f, .y = -10.20f};
  std::cout << "p1 => " << p1;

  Point2D p2 = {.x = -12.55f, .y = -3.5f};
  std::cout << "p2 => " << p2;

  auto p3 = Point2D{.x = -10.55f, .y = 13.5f};
  std::cout << "p3 => " << p3 << '\n';

  Product prod{.id = 200, .name = "Colombian coffee", .price = 100.56};
  std::cout << "Product => id = " << prod.id() << ", name = " << prod.name()
            << ", price = " << prod.price() << '\n';
}[/code]

>outputs
[code]p1 => Point{x = 2.5, y = -10.2} 
p2 => Point{x = -12.55, y = -3.5} 
p3 => Point{x = -10.55, y = 13.5} 

Product => id = 200, name = Colombian coffee, price = 100.56[/code]

# 128
>>4402
> I(t also allows the args to be passed in any order I believe).
Update: tested and no, apparently. The arguments have to be passed in the same order as the ctor parameters as always. Wouldn't surprise me if this is relaxed in a future version of the standard, however.

# 129
I was investigating C++17 std::apply, and found this overly-clever but very useful code for enumerating complex tuples directly to an ostream.

[code]// https://en.cppreference.com/w/cpp/utility/apply
// tuple ostream operator<< example using std::apply

#include <iostream>
#include <tuple>
#include <utility>

template <typename... Ts>
std::ostream& operator<<(std::ostream& os, std::tuple<Ts...> const& the_tuple) {
  std::apply(
      [&os](Ts const&... tuple_args) {
        os << '[';

        // This is too clever, actually (but the use-case is worth it tbh)
        std::size_t n{0};
        ((os << tuple_args << (++n != sizeof...(Ts) ? ", " : "")), ...);

        os << ']';
      },
      the_tuple);
  return os;
}

int main() {
  std::tuple myTuple{25, "Hello", 9.31f, 'c'};
  std::cout << myTuple << '\n';
}[/code]

>outputs
[code][25, Hello, 9.31, c][/code]

# 130
For experienced developers, I'd like some advice if you wouldn't mind. I'm working on ideas for the C++ Group Learning Thread >>4895. As any of you who are experienced know, one of the biggest headaches of a large codebase is tracking down bugs.

One of the greatest things since sliced bread for this area is clang-tidy and it's numerous checks.
https://releases.llvm.org/10.0.0/tools/clang/tools/extra/docs/clang-tidy/checks/list.html

So, my request is basically advice on how to go about easing newcomers into this topic w/o overwhelming them. My favorite open-sauce editor already directly supports both clang-tidy & clang-format, as well as the modern build systems of cmake and meson. So the tool isn't the issue, it's the integration of these ideas for the beginners in a way that helps them appreciate why they need to follow the guidance of these tools (after all, much of what they have experienced so far is bad advice).

Thoughts?

# 131
Well, the conversation about ''mlpack'' in the Speech Synthesis general >>5718 led me eventually to discover through this blogpost
https://shrit.me/blog/gsoc_week_9/
a couple of different libraries that nicely fulfill a couple of needs I've recognized in my own code.
-CLI11, for standard and flexible command line argument parsing.
https://github.com/CLIUtils/CLI11
and
-Cereal, for object serialization (out to disk for example).
https://github.com/USCiLab/cereal

My approaches to these problems have thus far been too bulky/convoluted. Hopefully these two projects will help me with that.
>''Thank you for reading my blog. Please be sure to upboat and like.''
**:^)**

# 132
>>5059
Keeping it simple I guess. Nobody is going to use something unless it saves them some trouble.

From my experience teaching, people are mostly blindly trying things to get to their goal, so I focus on making the process easy and enjoyable for them as possible without doing their thinking for them. People pay more attention when they feel like they're figuring out something on their own than following instructions, and when they make a mistake I just point out the consequences of what they're doing and let them decide if they want those consequences or not. People can only take things one step at a time. All you can really do is make sure they have what they need to keep heading in the right direction. You might know something extremely useful for them to do in a hundred steps but if they're walking in the wrong direction it becomes irrelevant.

As for tracking down bugs the most revolutionary thing for me as a beginner was writing automated tests for functions used more than once. Once I saw that editing a function could introduce bugs into other seldom used areas of a program, no one needed to tell me to write tests because they saved me a lot of time debugging. So when teaching something I find it most helpful to think about why something is useful and create a simple concrete example that other people will immediately realize the benefit of doing themselves, while considering the different goals they might have.

# 133
>>5741
Thanks Anon, great advice. This is more or less my first time trying to teach so I have a lot to learn. Thanks for the advice about testing. Makes good sense hearing it in that light. I planned to introduce some practical approaches a few months down the road, but I'll probably move that forward a bit now.

ATM, I'm juggling with how much of an internal hardware model to push. Obviously this is complex topical domain, and hardware knowledge will be fundamental to successful robowaifu devs, but again, how to impart that w/o being overwhelming to beginners is the challenge for me.

Keeping it simple is always a good idea. **Not sure how good I am at that yet haha**

# 134
>>5739
Progress report: Seems like I have CLI11 working in a basic 'Hello World' way. I can't really imagine a cleaner way to deal with argument parsing in C++ honestly.

>main.cpp
[code]#include <cstdlib>
#include <iostream>

#include "include/rw_utils.hpp"

int main(int argc, char** argv) {
  if (auto bad_args = do_arg_parse(argc, argv))
    std::exit(bad_args);

  std::cout << "Hello World\n";

  return 0;
}[/code]

>rw_utils.hpp
[code]#pragma once

#include "include/CLI11.hpp"

int do_arg_parse(int argc, char** argv) {
  CLI::App app{"This is Bumpmaster. Here we master the bumps..."};

  std::string filename = "default";
  app.add_option("-f,--file", filename, "A help string");

  try {
    app.parse(argc, argv);
  } catch (const CLI::ParseError& e) {
    return app.exit(e);
  }

  return 0;
}[/code]

First, just copy the latest CLI11.hpp file from https://github.com/CLIUtils/CLI11/releases into an 'include' project directory, and you should be good to go.

# 135
>>6063
>Update:
I neglected the fact that using ''--help'' still executed the program (it shouldn't). Doing a little research led me to the requirement to clutter up your main() function with all the arg parsing code to stop this. I'm not willing to write software in that way, no thanks.

Looking around a little further, I found you could create custom handling for the help flag. It's a bit hacky, but it lets me keep my main() clean and keep the complexity hidden--as it should be in maintainable code.
>

>rw_utils.hpp
[code]#pragma once

#include "CLI11.hpp"

static CLI::App app{"This is Bumpmaster. Here we master the bumps..."};
bool have_help{false};
int p{0};

int handle_args(int argc, char** argv) {
  app.add_option("-p", p, "Parameter");

  // Disable default help handler
  // https://github.com/CLIUtils/CLI11/blob/master/examples/modhelp.cpp
  app.set_help_flag();
  // Add custom flag that activates help
  auto help = app.add_flag("-h,--help", "Request help");

  try {
    app.parse(argc, argv);

    if (*help) {
      have_help = true;
      throw CLI::CallForHelp();
    }

  } catch (const CLI::ParseError& e) {
    return app.exit(e);
  }

  return 0;
}

// Wrapper for dealing w/ arg errors + help
void parse_args(int argc, char** argv) {
  if (auto err = handle_args(argc, argv)) {  // non-zero == args error state
    std::exit(err);
  } else if (have_help) {
    std::exit(0);
  }
}[/code]

# 136
>>6063
Is there a place to find libraries like these? One of the reasons I don't use C++ much is because it's difficult for me to find useful libraries like this.

# 137
>>6088
>Is there a place to find libraries like these?
OFC. You came to the right place! :^)

But seriously, yes there are many, many libraries out there (of varying quality). Part of growth as a developer is a result of dabbling with lots of different and deciding for yourself between the good, the bad, and the ugly.  Here's a small collection to get you started on your way Anon:

>'''awesome-cpp'''
>''"A curated list of awesome C++ (or C) frameworks, libraries, resources, and shiny things. Inspired by awesome-... stuff."''
https://github.com/fffaraz/awesome-cpp

>'''AwesomePerfCpp'''
>''"A curated list of awesome C/C++ performance optimization resources: talks, articles, books, libraries, tools, sites, blogs. Inspired by awesome."''
https://github.com/fenbf/AwesomePerfCpp

>'''A list of open source C++ libraries'''
>''"The objective of this page is to build a comprehensive list of open source C++ libraries, so that when one needs an implementation of particular functionality, one needn't to waste time searching on web"''
https://en.cppreference.com/w/cpp/links/libs

Be sure to post results of your experimentations ITT. Cheers.

# 138
>>6063
>>6077
I have some other things calling me atm, but I wanted to leave my current working example for my proof-of-concept for using this library. It's working enough to go on with for now, certainly an improvement from my original approach:

>main.cpp
[code]#include <iostream>

#include "include/rw_cli_args.hpp"

using rw::filename;
using rw::p;

int main(int argc, char** argv) {
  rw::parse_args(argc, argv);

  std::cout << "Hello World\n";

  if (p)
    std::cout << "Have '-p' arg: " << p << '\n';
  if (!filename.empty())
    std::cout << "Have '-filename' arg: " << filename << '\n';

  return 0;
}[/code]

>rw_cli_args.hpp
[code]#pragma once

#include <cstdlib>
#include <string>

#include "CLI11.hpp"

namespace robowaifu {

// This is the single, and overall CLI App object for parsing program arguments
CLI::App app{"This is /robowaifu/'s Bumpmaster. Here we master the BUMPs :^)"};

// Optional variables possibly assigned to by command-line arguments
int p{0};
std::string filename{""};

// Simple flag to track if the help flag was passed in
bool have_help{false};

// Configure for, and parse, any command-line arguments
int handle_args(int argc, char** argv) {
  app.add_option("-p", p, "Parameter param");
  app.add_option("-f, --file", filename, "A help string");

  // Disable the default help handler and add a custom flag for activating help
  // https://github.com/CLIUtils/CLI11/blob/master/examples/modhelp.cpp
  app.set_help_flag();
  auto help = app.add_flag("-h, --help", "Request help");

  try {
    app.parse(argc, argv);

    if (*help) {                 // Special block just for the custom help flag
      have_help = true;          // used by parse_args() below
      throw CLI::CallForHelp();  // caught immediately below, returns a '0' exit
    }
  } catch (const CLI::ParseError& e) {
    return app.exit(e);
  }

  return 0;
}

// Wrapper to unify correct program exit on either arg errors or the help flag
void parse_args(int argc, char** argv) {
  if (auto bad_arg = handle_args(argc, argv)) {  // non-zero ret == error state
    std::exit(bad_arg);
  } else if (have_help) {  // simple hack to prevent program execution on --help
    std::exit(0);
  }

  // DESIGN: This would probably be a good place to emplace CLI option pointers
  // into a general-purpose std::vector<Option*> (if CLI doesn't already provide
  // something like this) and pass it back to caller. Possibly a better approach
  // than keeping 'global' vars scattered all over inside this namespace as now.
  // -Using a vector instead would allow us to efficiently manage an unlimited
  // number of arguments passed into our program once they are parsed, It would
  // be a simple handle to them all, easily usable from anywhere in our code.

  // ...
}

}  // namespace robowaifu

namespace rw = robowaifu;  // shorthand namespace alias[/code]

# 139
>>6089
Thanks, this is gonna be a huge help for making usable applications with mlpack.

# 140
>>6104
y/w
>this is gonna be a huge help for making usable applications with mlpack.
i'll be very interested to see what you'll come up with anon. thanks to /robowaifu// i too am exploring how to use mlpack.

# 141
Much as I appreciate FLTK, it's ancient C heritage can result in some butt-ugly code for things like creating menus. In an attempt to ameliorate some of the pain in writing GUI code for our robowaifus that can run on the smallest potato, I'm starting a little side-project to wrap calls with simpler C++ ones.

>main.cpp
[code]#include <array>

#include "Window.hpp"

using muh_window::Menu;
using muh_window::Menu_item;
using muh_window::Window;

auto setup_items() {
  std::array<Menu_item, 4> items{"File", "Edit", "Tools", "Help"};

  // DESIGN: configure all menu items (callbacks, etc) here...

  return items;
}

int main() {
  const auto win_title{"/robowaifu/ fltk base window/menu test"};
  const int win_width{500};
  const int win_height{180};
  const int menu_height{25};

  Window window{win_width, win_height, win_title};

  Menu menu{win_width, menu_height};
  menu.menu(setup_items().data());

  // window.end();
  // DESIGN: any add'l non-FLTK setup code would go here...

  window.show();
  return Fl::run();
}[/code]

>Window.hpp
[code]#pragma once

#include <FL/Fl.H>
#include <FL/Fl_Double_Window.H>
#include <FL/Fl_Menu_Bar.H>

namespace muh_window {

struct Point {
  Point(const int x, const int y) : x{x}, y{y} {}
  int x{0}, y{0};
};

struct Rect {
  Rect(const Point ul_origin, const int w, const int h)
      : ul_origin{ul_origin}, w{w}, h{h} {}

  Point ul_origin;
  int w{100}, h{100};
};

class Window : public Fl_Double_Window {
 public:
  Window() : Fl_Double_Window{0, 0, 100, 100, ""} {}
  Window(const Rect& rect, const char* title)
      : Fl_Double_Window{rect.ul_origin.x, rect.ul_origin.y, rect.w, rect.h,
                         title} {}
  Window(const int w, const int h, const char* title)
      : Fl_Double_Window{w, h, title} {}
};

// DESIGN: Use Fluid and see what it defines a menu as, then inherit/setup that
class Menu : public Fl_Menu_Bar {
 public:
  Menu(const Rect& rect)
      : Fl_Menu_Bar{rect.ul_origin.x, rect.ul_origin.y, rect.w, rect.h} {}

  Menu(const int x, const int y, const int w, const int h)
      : Fl_Menu_Bar{x, y, w, h} {}

  Menu(const int w, const int h) : Menu{0, 0, w, h} {}
};

class Menu_item : public Fl_Menu_Item {
 public:
  Menu_item(const char* label, const uchar fnt_sz)
      // struct Fl_Menu_Item {
      //  const char*   text;     // label()
      //  ulong         shortcut_;
      //  Fl_Callback*  callback_;
      //  void*         user_data_;
      //  int           flags;
      //  uchar         labeltype_;
      //  uchar         labelfont_;
      //  uchar         labelsize_;
      //  uchar         labelcolor_;
      // };
      : Fl_Menu_Item{label, 0, 0, 0, 0, (uchar)FL_NORMAL_LABEL, 0, fnt_sz, 0} {}

  Menu_item(const char* label) : Menu_item{label, 18} {}
};

};  // namespace muh_window[/code]

>meson.build
[code]project('fltk_simple', 'cpp')

add_project_arguments('-std=c++20', '-Wall', '-Wextra', language: 'cpp')

cxx = meson.get_compiler('cpp')
fltk_dep = cxx.find_library('fltk')

executable('fltk_simple', 'main.cpp', dependencies : fltk_dep)[/code]

I personally consider functions like
[code]auto setup_items() {
  std::array<Menu_item, 4> items{"File", "Edit", "Tools", "Help"};

  // DESIGN: configure all menu items (callbacks, etc) here...

  return items;
}[/code]

and statements at the caller:
[code]menu.menu(setup_items().data());[/code]
much cleaner and easier to reason about than typical FLTK examples.

# 142
>>6860
You probably need to compile this code in Release mode (-O3) for this work correctly. Inside Juci, you can tell Mesonbuild to do this by ''Project > Run Command'', then entering this external code to instruct meson to use release mode:
[code]cd build && meson configure --buildtype=release && cd ..[/code]

# 143
I needed to create a subject-sorted list of the threads on /robowaifu/ for our new topical index thread  >>7254 . I felt like it might be a good idea to show others how I used C++ to create that text file just in case anyone else is exploring cataloguing our board and wants to use it since this same basic approach can be used to process literally any of the text anywhere on this board -- not just thread IDs and subjects. If you get stuck AMA ITT.

>'''Instructions:'''
-''prerequisites:'' You'll need both the ''meson'' build system, and the ''jsoncpp'' developer library installed on your system. (You can get by w/o meson ofc, but if you know this already then you don't need any instructions from ''me'' heh).

Create a project directory for this C++20 code, create these two files (''main.cpp'' & ''meson.build'') there and copypasta these two code blocks into them. Then extract a copy of the threads JSON archive (current version is https://files.catbox.moe/e1fbkn.7z , latest version can be found linked in that thread's OP >>7143) into a subdirectory '''all_jsons''' located inside the project directory. 

Configure the project (open a terminal and issue ''meson build'' inside the project directory) then build it (issue ''cd build/ && meson compile''), and run it (''cd .. && build/rw_json_prj''). You'll get a new sorted text file '''id_subjs.txt''' of all the threads, with each data element being extracted from it's own JSON file located in the ''all_jsons'' directory.

>main.cpp
[code]#include <algorithm>
#include <cstdint>
#include <exception>
#include <filesystem>
#include <fstream>
#include <iomanip>
#include <iostream>
#include <regex>
#include <string>
#include <utility>
#include <vector>

#include <json/json.h>

namespace fs   = std::filesystem;
using dir_iter = fs::directory_iterator;

using std::cout;
using std::ifstream;
using std::left;
using std::ofstream;
using std::pair;
using std::regex;
using std::regex_replace;
using std::setw;
using std::string;
using std::unexpected;
using std::vector;
using std::ranges::sort;

//------------------------------------------------------------------------------
// Take a raw json source and parse it into a json db
//
template <typename T>
Json::Value parse_json(T& json_src) {
  Json::Reader reader{};
  Json::Value  json_dat{};
  reader.parse(json_src, json_dat);
  return json_dat;
}

//------------------------------------------------------------------------------
// Validate filepath then return the file's full JSON parse
//
Json::Value get_jsonfile_dat(const fs::path& filepath) {
  if (fs::exists(filepath) && fs::is_regular_file(filepath)) {
    ifstream jsonfile{filepath.string()};
    return parse_json(jsonfile);
  } else {
    throw(unexpected);
  }
}

//------------------------------------------------------------------------------
// Return a copy of in, replacing each bad substring with with a single
// good character
//
std::string repl_w_char(const std::string& in,
                        const std::string& bad,
                        const char         good) {
  const regex  bad_match{bad};
  const string good_ch{good};

  return regex_replace(in, bad_match, good_ch);
}

//------------------------------------------------------------------------------
// Return a copy of s, cleaning various bad text it may contain
//
std::string clean_str(const std::string& s) {
  string res{s};
  // Handle individual JSON string-to-char replacements
  res = repl_w_char(res, "'", '\'');
  res = repl_w_char(res, """, '"');

  return res;
}

//------------------------------------------------------------------------------
// Program entry-point
//
int main() {
  const fs::path                 jsons_dir{"./all_jsons/"};
  vector<pair<uint32_t, string>> id_subjs{};

  // load container from all JSON files in directory
  for (const auto& jsonfile : dir_iter{jsons_dir}) {
    auto json = get_jsonfile_dat(jsonfile);
    id_subjs.emplace_back(
        pair{json["threadId"].asUInt(), clean_str(json["subject"].asString())});
  }

  // sort container, defining our own custom sort criteria
  sort(id_subjs, [](auto a, auto b) {
    auto [id_a, subj_a]{a};
    auto [id_b, subj_b]{b};

    // return id_a < id_b;   // sort by id, or...
    return subj_a < subj_b;  // sort by subject
  });

  // stream the now-sorted container's contents out to file
  ofstream ofs{"id_subjs.txt"};
  for (const auto& [id, subj] : id_subjs) {
    ofs << ">>" << left << setw(7) << id << subj << '\n';
  }

  cout << "directory entry count: " << id_subjs.size() << '\n';
}[/code]

>meson.build
[code]project('rw_json_prj', 'cpp')

add_project_arguments('-std=c++20', '-Wall', '-Wextra',
                      '-Wno-deprecated-declarations',
                      language: 'cpp')

cxx=meson.get_compiler('cpp')
jsondep=cxx.find_library('jsoncpp')

executable('rw_json_prj', 'main.cpp', dependencies : jsondep)[/code]

>''compiled w/ g++ 10.2.0 and jsoncpp 1.9.4-1''

>===
-''minor OP prose edit''
-''minor comment edit''
-''rename get_jsonfile_dat() and jsonfile for clarity''
-''add std usings for function readability''
-''pluralize container name''
-''simply subdirectory name in post text''
-''update JSON archive link''
-''add build instructions in OP''

# 144
>>7268
>Discussion
The sort statement (lines 104-111) forms the core. Here we write a custom C++ lambda function that extracts out both parts of a pair of elements from the container, then simply returns a straightforward comparison between the two. Right now this code is defaulting to sorting ascending by subject, but either of the other three possibilities on this container are also straightforward, and I also provided one of those commented out.

>core sorting statement:
[code]  // sort container, defining our own custom sort criteria
  sort(id_subjs, [](auto a, auto b) {
    auto [id_a, subj_a]{a};
    auto [id_b, subj_b]{b};

    // return id_a < id_b;   // sort by id, or...
    return subj_a < subj_b;  // sort by subject
  });[/code]

Since we're only capturing these two JSON fields into our container ATM, that pretty much constitutes most of what we can do. But the JSON files themselves provide literally all the fields the Lynxchan imageboard software uses to manage the thread's posts. Any (or all) of these can be extracted with this same direct approach and then used to process the system any way you can contrive.

>std::pair of ID & subject being captured into the vector containing them all:
[code]  const fs::path                 jsons_dir{"./all_jsons/"};
  vector<pair<uint32_t, string>> id_subjs{};

  // load container from all JSON files in directory
  for (const auto& jsonfile : dir_iter{jsons_dir}) {
    auto json = get_jsonfile_dat(jsonfile);
    id_subjs.emplace_back(
        pair{json["threadId"].asUInt(), clean_str(json["subject"].asString())});
  }[/code]

Here's a pretty-print of the OP and some post data from thread #1 ''Robowaifu References'' ' JSON. As you can see there are quite a few fields there, and you can modify the above code and the vector to use any or all of them for processing. Again, right now we're only capturing the ''threadId'' & ''subject'' fields into a std::pair, but you can swap that out using a std::tuple instead and free-form the data however you'd like.

>pretty-print snippet:
[code]{
	"signedRole": null,
	"id": null,
	"name": "Anonymous",
	"email": null,
	"boardUri": "robowaifu",
	"threadId": 1,
	"subject": "Robowaifu references",
	"markdown": "My favorite robowaifu is Chii. I'd like to see yours.",
	"message": "My favorite robowaifu is Chii. I'd like to see yours.",
	"creation": "2019-09-09T00:09:49.229Z",
	"locked": false,
	"archived": false,
	"pinned": false,
	"cyclic": true,
	"autoSage": false,
	"files": [{
		"originalName": "0704220907690_000_db11d79641c31f1fdfbd6d39323e7bbb7b1f8bf11f24c14b1f531bc76711f363.jpg",
		"path": "/.media/db11d79641c31f1fdfbd6d39323e7bbb7b1f8bf11f24c14b1f531bc76711f363.jpg",
		"thumb": "/.media/t_db11d79641c31f1fdfbd6d39323e7bbb7b1f8bf11f24c14b1f531bc76711f363",
		"mime": "image/jpeg",
		"size": 419112,
		"width": 1136,
		"height": 1700
	}],
	"posts": [{
		"name": "Robowaifu Technician",
		"signedRole": null,
		"email": null,
		"id": null,
		"subject": null,
		"markdown": "<a class=\"quoteLink\" href=\"/robowaifu/res/1.html#1\">>>1</a>\r<br>My robowaifu is 2b. It's nice to see /robowaifu/ back again. I also really like the automaton from MGE",
		"message": ">>1\r\nMy robowaifu is 2b. It's nice to see /robowaifu/ back again. I also really like the automaton from MGE",
		"postId": 24,
		"creation": "2019-09-09T06:21:31.362Z",
		"files": [{
			"originalName": "0216d3245db2eb77f56addf7f3ec18ad8f7aebd815d0775f337333cbd3da71b6.jpg",
			"path": "/.media/0216d3245db2eb77f56addf7f3ec18ad8f7aebd815d0775f337333cbd3da71b6.jpg",
			"thumb": "/spoiler.png",
			"mime": "image/jpeg",
			"size": 1609514,
			"width": 1755,
			"height": 3307
		}, {
			"originalName": "Bridal_Automaton.jpg",
			"path": "/.media/85709b1ebef9d3ba20099ee263c5c27eca62b7a1453f321866ed9ef43a3e5040.jpg",
			"thumb": "/spoiler.png",
			"mime": "image/jpeg",
			"size": 2202496,
			"width": 2000,
			"height": 2500
		}, {
			"originalName": "Automaton2b.png",
			"path": "/.media/8be218e68a8f161faee9d6de7fa289bf02df1ccd072a5fc033f315769ef528d6.png",
			"thumb": "/spoiler.png",
			"mime": "image/png",
			"size": 211713,
			"width": 682,
			"height": 999
		}]
	}, {[/code]

>===
-''add std::tuple clarification''

# 145
>>7268
Rather than throwing an exception, I decided that simply returning an empty JSON parse was a better approach. A user of the code will realize their mistake quickly enough if they investigate, and this approach is more robust.

[code]//------------------------------------------------------------------------------
// Validate filepath then return the file's JSON parse
//
Json::Value get_jsonfile_dat(const fs::path& filepath) {
  if (fs::exists(filepath) && fs::is_regular_file(filepath)) {
    ifstream jsonfile{filepath.string()};
    return parse_json(jsonfile);
  } else
    return Json::Value{};
}[/code]

# 146
>>7268
Lol, Lynxchan pls. Looks like the page rendering is 'helping' us again, and actually converting text in the code. Here's what the source code actually looks like, and you'll need to edit it accordingly in your own software:
>

# 147
Decided to be a good little boy and add some Javadoc comments to those utility functions, since now that I think about it we can probably be lift them out in some form or other into a new utility header file to serve in other contexts. (Like a rewrite of ''BUMP'' or some kind of an Internet-scraping frontend for our waifus). My Javadoc is still beginner-tier I imagine, pull requests welcome.

[code]/**-----------------------------------------------------------------------------
 @brief    Take a raw JSON source and parse it into a Json db
 @param    json_src [IN] The raw input JSON source
 @returns  The Json data after parsing
*/
template <typename T>
Json::Value parse_json(T& json_src) {
  Json::Reader reader{};
  Json::Value  json_dat{};
  reader.parse(json_src, json_dat);
  return json_dat;
}

/**-----------------------------------------------------------------------------
 @brief    Validate 'filepath' then return the file's JSON parse
 @param    filepath [IN] The input filesystem path
 @returns  The Json data after parsing
*/
Json::Value get_jsonfile_dat(const fs::path& filepath) {
  if (fs::exists(filepath) && fs::is_regular_file(filepath)) {
    ifstream jsonfile{filepath.string()};
    return parse_json(jsonfile);
  } else
    return Json::Value{};
}

/**-----------------------------------------------------------------------------
 @brief    Return a copy of 'in', replacing each bad substring with a single
 good character
 @param    in [IN] The input source string
 @param    bad [IN] The bad search pattern
 @param    good [IN] The good replacement char
 @returns  The now-cleaned string copy
*/
std::string repl_w_char(const std::string& in,
                        const std::string& bad,
                        const char         good) {
  const regex  search{bad};
  const string replace{good};

  return regex_replace(in, search, replace);
}

/**-----------------------------------------------------------------------------
 @brief    Return a copy of 'in', cleaning various bad JSON text it may contain
 @param    in [IN] The input string to clean
 @returns  The now-cleaned string copy
*/
std::string clean_str(const std::string& in) {
  string res{in};
  // Handle individual JSON string-to-char replacements
  res = repl_w_char(res, "&apos;", '\'');
  res = repl_w_char(res, "&quot;", '"');

  return res;
}[/code]

# 148
>>7508
OK, I've begun the process of providing a well commented set of text utilities in C++ we can use for multiple projects here on /robowaifu/. This set will grow over time I'm sure, but this seems a good set to begin with for now.

>rw_text_utils.hpp
[code]#pragma once

#include <filesystem>
#include <fstream>
#include <iterator>
#include <regex>
#include <string>
#include <utility>

#include <json/json.h>

namespace fs = std::filesystem;

using std::begin;
using std::cend;
using std::ifstream;
using std::make_pair;
using std::regex;
using std::regex_replace;
using std::string;

namespace rw {

/**-----------------------------------------------------------------------------
 @brief    Take a raw JSON source and parse it into a Json db
 @param    json_src [IN] The raw input JSON source
 @returns  The Json data after parsing
*/
template <typename T>
Json::Value parse_json(T& json_src) {
  Json::Reader reader{};
  Json::Value  json_dat{};
  reader.parse(json_src, json_dat);
  return json_dat;
}

/**-----------------------------------------------------------------------------
 @brief    Validate 'filepath' then return the file's Json parse
 @param    filepath [IN] The input filesystem path
 @returns  The Json data after parsing
*/
Json::Value get_jsonfile_dat(const fs::path& filepath) {
  if (fs::exists(filepath) && fs::is_regular_file(filepath)) {
    ifstream jsonfile{filepath.string()};
    return parse_json(jsonfile);
  } else
    return Json::Value{};
}

/**-----------------------------------------------------------------------------
 @brief    Return a copy of 'in', replacing each bad substring with a single
 good character
 @param    in [IN] The input source string
 @param    bad [IN] The bad search pattern string
 @param    good [IN] The good replacement char
 @returns  The now-cleaned string copy
*/
std::string repl_w_char(const std::string& in,
                        const std::string& bad,
                        const char         good) {
  const regex  search{bad};
  const string replace{good};
  return regex_replace(in, search, replace);
}

/**-----------------------------------------------------------------------------
 @brief    Return a copy of 'in', cleaning various bad JSON text it may contain
 @param    in [IN] The input string to clean
 @returns  The now-cleaned string copy
*/
std::string clean_str(const std::string& in) {
  string res{in};
  // Handle individual JSON string-to-char replacements
  res = repl_w_char(res, "&apos;", '\'');
  res = repl_w_char(res, "&quot;", '"');
  return res;
}

/**-----------------------------------------------------------------------------
 @brief    Split 'in' string into a pair, dividing on the final 'delim' char
 @param    in [IN] The input string to split
 @param    delim [IN] The delimiter char to divide upon
 @returns  The now-split string pair
*/
std::pair<std::string, std::string> split_str(const std::string& in,
                                              const char         delim) {
  const auto str_end{string::npos};  // note: this works in both directions

  if (const auto split_pos{in.rfind(delim)};  // Search reverse for final delim
      split_pos != str_end) {                 // Delimeter found
    const string front{in.substr(0, split_pos)};
    const string back{in.substr(split_pos + 1, str_end)};
    return make_pair(front, back);
  } else
    return make_pair(in, "");  // Delimeter not found
}

/**-----------------------------------------------------------------------------
 @brief    split_str() wrapper that defaults using a '.' delimiter char
 @param    in [IN] The input string to split
 @returns  The now-split string pair
*/
std::pair<std::string, std::string> split_str_dot(const std::string& in) {
  return split_str(in, '.');
}

/**-----------------------------------------------------------------------------
 @brief    split_str() wrapper that defaults using a '/' delimiter char
 @param    in [IN] The input string to split
 @returns  The now-split string pair
*/
std::pair<std::string, std::string> split_str_slash(const std::string& in) {
  return split_str(in, '/');
}

/**-----------------------------------------------------------------------------
 @brief    Consolidate 'in_out' string in-place, paring contiguous chars 'c'
 down to just one 'c' per contiguous sequence
 @param    in_out [IN/OUT] The string to pare down
 @param    c [IN] The char to consolidate
*/
void rm_dupes(std::string& in_out, const char c) {
  char prev{'\0'};

  for (auto it{begin(in_out)}; it != cend(in_out); ++it) {
    if ((prev == *it) && (c == *it)) {  // Have a dupe,
      in_out.erase(it);                 // remove it,
      --it;                             // now back up to adjust for next check
    } else
      prev = *it;
  }
}

/**-----------------------------------------------------------------------------
 @brief    Return a copy of string 'in', removing each single leading and
 trailing char 'c', if present
 @param    in [IN] The input string to trim
 @param    c [IN] The target char to trim from string
 @returns  The now-trimmed string copy
*/
std::string trim_chars(const std::string& in, const char c) {
  string res{in};

  if (res[0] == c)
    res = res.substr(1, res.size());  // Remove a single leading char c

  if (res[res.size() - 1] == c)
    res = res.substr(0, (res.size() - 1));  // Remove a single trailing char c

  return res;
}

}  // namespace rw[/code]

# 149
>>7534
Sounds great. This is especially for the data from the board? So people can work with the downloaded data? If so, what would help people  that haven't learned C++ yet the most, might be a way to use these functions from the shell/commandline. Just an idea, maybe it's better to learn the language a bit...

# 150
>>7538
Yes, I'm doing this atm to deal with our new Library thread, but yes it can be used for many different things to do with our robowaifus inside or out. C++ is the high-performance language of choice I'm targeting us for running robowaifu software on small, inexpensive onboard computers. 

Yes, I'll add simple instructions ITT for it's use when I get the new software written this weekend Anon.

# 151
>>7538
>maybe it's better to learn the language a bit...
Added some index links for C++ Anon, maybe they can help you get started.
>>7184

# 152
>>7538
>This is especially for the data from the board? So people can work with the downloaded data?
Anon, I know I implied I'd be ready with this utility by this weekend but I'm going to have to push that back until at least next weekend instead. Currently you can only search for individual words, not phrases, and has a few other things to work out. On a positive note, it's pretty fast so far and I think it will be that way when it's working correctly.

My apologies for the delay.

# 153
>>7598
Hey, I'm not the one pushing for the index thread being done as fast as possible. It would be great, but if it takes more time, then this is it. My own code takes more time than anticipated as well, sometimes just because I'm getting to angry and need to take a break.

# 154
>>7602
Haha, fair enough then. Give me a month or two and I should have a decent TUI or FLTK GUI for the thing w/ live local downloading of board JSONs in place. Cheers.

# 155
added post linking to the CLI search tool outputs.
[code]time to parse local /robowaifu/ JSON data:  5209ms
unique word@post count:  31669

(q to quit) enter search terms: ambulatory

   THREAD SUBJECT                      POST LINK
Actuators for waifu movement!   ->  https://alogs.theГунтretort.com/robowaifu/res/406.html#7102
Work on my Elfdroid Sophie      ->  https://alogs.theГунтretort.com/robowaifu/res/4787.html#7502

 search for terms:  'ambulatory'
   took:  24us , 2  results

(q to quit) enter search terms: organelles

   THREAD SUBJECT                      POST LINK
Can Robowaifus Experience Love  ->  https://alogs.theГунтretort.com/robowaifu/res/14.html#3912
   "                            ->  https://alogs.theГунтretort.com/robowaifu/res/14.html#3914
   "                            ->  https://alogs.theГунтretort.com/robowaifu/res/14.html#3915
   "                            ->  https://alogs.theГунтretort.com/robowaifu/res/14.html#3921

 search for terms:  'organelles'
   took:  15us , 4  results

(q to quit) enter search terms: delicious

   THREAD SUBJECT                      POST LINK
Waifus in society               ->  https://alogs.theГунтretort.com/robowaifu/res/106.html#4148
RoboWaifuBanners                ->  https://alogs.theГунтretort.com/robowaifu/res/252.html#6704
Fluffytail 800 dev thread       ->  https://alogs.theГунтretort.com/robowaifu/res/364.html#6194
Waifu Robotics Project Dump     ->  https://alogs.theГунтretort.com/robowaifu/res/366.html#3440
Robowaifu Propaganda and Recru  ->  https://alogs.theГунтretort.com/robowaifu/res/2705.html#2708
Haute Sepplesberry Cuisine TBH  ->  https://alogs.theГунтretort.com/robowaifu/res/4969.html#4969

 search for terms:  'delicious'
   took:  26us , 6  results

(q to quit) enter search terms: q[/code]

# 156
>>7616
>yfw links are corrupted
==FUUUUU==
Kek, Robi you bastard. :^)
>

# 157
>>7616
Oh, this looks really promising, now I'm getting tempted to try it myself.

# 158
>>7626
Sure, let me add multi-word searches and I'll post the progress so far ITT. Maybe in the next day or three. You need a copy of the /robowaifu/ threads JSON archive as well (available in the OP of our Library thread), so I'll make a current one and push it up to catbox for you as well. It's quite fast atm let's hope it stays that way heh.

# 159
>>7626
OK Anon, just wanted to let you know things are coming along nicely now and I have multi-word phrase searching going. It's not parsing things perfectly just yet as you can see
>

but the term-intersection functionality is locating your exact post regardless. I'd say you can expect me to post this code before the weekend. I may actually put the full setup for this utility code into the Sepplesberry thread instead of ITT though, so it can serve as a teaching project for the C++ class.
>>4969

Cheers.

# 160
>>7644
BTW, the results are still instantaneous, humanly-speaking and that was a high priority for all this to me. After all, we can't have our shitposting waifus having lags while reading the bantz! :^)

# 161
Neat. Thanks to Anon over in the basement  , I found out about this high-performance computing site news site
https://insidehpc.com/
where I found out that LLVM/Intel have new DPC++ library SYCL extensions out.
https://github.com/intel/llvm/tree/sycl/sycl/doc/extensions

>tl;dr
One day soon we'll be able to run our robowaifus effectively on mere ''Potato-Pi's'' Anon! :^)

# 162
OK, to any anons who are interested in 'robowaifu-JSON-indexing' tool I've been working on, I intended to have a post of the code here this weekend but afk-life has kept me from knocking it into good shape yet. So, I'll plan to try again ''next'' weekend, my apologies for any inconvenience Anon.

# 163
>>7626
OK, I have it parsing correctly now, and I decided that it would be more helpful to everyone if we had the terms sorted ''by occurrence'' across the board, rather than alphabetically. The timing is now more accurate as well.

I still haven't implemented exact (ie, inside quotes) searching yet, and there's a lot of clean up to do now. So I'm going to hold off for at least another week, but since next weekend will be Christmas, I'll probably manage it during a weekday following. But things are coming along.
>

# 164
Feeling pretty stoked. Scratched my head and finally managed to get parallel (multi-core) JSON file parsing working, and along with some other code cleanups I basically managed to cut the startup time of the program in half. Feels much snappier starting now. It's chewing through the 135 files (~10MB) and parsing every post and every word in about 2.5 seconds now, and that's on my old potato. Probably would do even better on a good box.
>

# 165
>>7904
>parallel (multi-core) JSON file parsing working

>muh_code_snippet:
[code]/**-----------------------------------------------------------------------------
 @brief    load the word-counting map 'io_w_pt' in parallel from each JSON file
 located inside the 'all_jsons' directory
 @param    io_w_pt [IN/OUT] The word-counting map to load
*/
void ld_map(map<string, set_pair_ints>& io_w_pt) {
  //
  // lambda to perform the JSON file parsing into the map
  auto parse_json_file{[&io_w_pt](auto& filepath) {
    const auto thread =
        rw::get_jsonfile_dat(filepath);  // each filepath == 1 imageboard thread

    const uint32_t thrd_id{thread["threadId"].asUInt()};
    const auto     thrd_subj = thread["subject"].asString();

    // store this thread's subject off into the global var container
    thrd_subjs[thrd_id] = rw::clean_str(thrd_subj);

    // OP's subject+message text
    clean_store_words(io_w_pt,
                      string{thrd_subj + ' ' + thread["message"].asString()},
                      thrd_id, thrd_id);

    // each reply post's subject+message text
    for (const auto& post : thread["posts"])
      clean_store_words(
          io_w_pt,
          string{post["subject"].asString() + ' ' + post["message"].asString()},
          post["postId"].asUInt(), thrd_id);
  }};

  // first, read in all JSON file paths from the directory
  vector<file_path> paths{};
  for (const auto& jsonfile : dir_iter{jsons_dir})
    paths.push_back(jsonfile);

  // then run filepath processing in parallel, using the lambda above
  for_each(par_unseq, cbegin(paths), cend(paths), parse_json_file);
}[/code]

Not too pretty, compared to some pre-canned functions in another language, but it suits myself well enough for now. In my experience, you usually have to deal with more complexity if you want more performance/efficiency so yea.

>===
-''minor code edit for readability''

# 166
>>7904
>updated JSON archive of the board
https://files.catbox.moe/3n02er.7z

# 167
>>7904
>It's chewing through the 135 files (~10MB) and parsing every post and every word in about 2.5 seconds now, and that's on my old potato.
BTW, during that two and a half seconds, it's also generating this 33K line, reverse-sorted text file of word_post_counts (one count for a word per post, excluding dupes).
https://files.catbox.moe/o38sax.txt

# 168
>>7906
Blimey. Still didn't find they time to look into the program but I download the and backup the results at least.

>>7907
Okay, that's fast. How flexible is it, if you want to do something slightly different, like searching for every pair of two words?
>o38sax.txt
I'm looking through the list, if it can be used for filtering out the relevant terms in a reasonable amount of time. If I recall correctly there's already a search available, so we could find the postings with these terms then and get their ID  numbers?

# 169
>>7908
>How flexible is it, if you want to do something slightly different, like searching for every pair of two words?
Since I'm writing it myself from scratch using nothing standard C++ & the jsoncpp library, it's as flexible as we can dream up how to make it. Yes, we could do any number of permutations of 'sliding window' views into the posts, if I take your meaning Anon.

# 170
Update: I have exact term matching working for the search tool now. Eg, here's a 'hello world' search:
>

There are 8 posts with all those words, and in that exact order (ORDERED), and 2 posts with all those words, but ''not'' in that exact order  (UN-ORDERED).

So, things are coming along. I have to chase down a random crash (probably have to reel in the multi-core just a bit), and some clean up. Then I should be able to set it all up on a RaspberryPi and test it there. If all goes well, I'll create a step-by-step tutorial for building it and using it on your own RPis, and then eventually use the whole project as a set of non-trivial lessons on using Modern C++ correctly on a small-scale (it's about 1'000 lines of code).

Cheers.

# 171
>>7921
>I have to chase down a random crash (probably have to reel in the multi-core just a bit)
In accord w/
>>2701
>Confessional
I'll reveal the crashing bug  I finally found. But I'm still unsure just how to fix it yet (other than just not using parallelism for that op).

>fubar.cpp
[code]//----------------------------------

void clean_store_words(map<string, set_pair_ints>& io_w_pt,
                       const std::string&          in,
                       const uint32_t              post,
                       const uint32_t              thrd) {
  string temp{in};
  scrub_chars(temp);
  rw::rm_dupes(temp, '\'');

  // parse each message into a vector<string>
  stringstream   message{temp};
  vector<string> words{};

  while (message >> temp) {  // '>>' stream operator parses on whitespace here
    scrub_string(temp);

    if (temp != "")
      words.push_back(temp);
  }

  string cleaned_msg{};

  // DEBUG: making this normal seems to have stopped the crashing.
  // test.
  // -UD: went 10 times straight w/o crashing. Will try bringing the others back
  // 'online'.
  // -UD2: 10 more times crash-free w/ others @ par_unseq. Seems OK now,
  // apparently this was the problem. Wonder what was happening?
  for_each(cbegin(words), cend(words), [&](const auto& word) {
    // for_each(par_unseq, cbegin(words), cend(words), [&](const auto& word) {
    io_w_pt[word].insert(make_pair(post, thrd));

    cleaned_msg += word + ' ';  // DEBUG: i wonder if the string concat could
    // be part of the crashing issue w/ par ops?
    // -test.
    // -UD: Yes, this appears to be the fundamental issue.
    //   -how to solve? exact-matching won't w/o this insertion into container.
    //     -some kind of atomic op?
    //
  });

  // insert the cleaned message into the global (for exact-matches)
  all_msgs[post] = cleaned_msg;
}[/code]

# 172
>>7928
>Merry Christmas /robowaifu/ .
Thanks, for the program. At least , I intent to look into it soon. Merry Christmas as well.

# 173
>>7929
Heh, sorry I fixed some typos and added another first build step. Cheers.

# 174
Alright, I've decided that the search tool is good enough at a basic level to go ahead and provide it as a download before Christmas. I've decided to name it ''waifusearch''. It's not packed or anything yet, so you'll have to build it yourself from codefiles using a C++ compiler. You can download and unzip this somewhere:
https://files.catbox.moe/ptpzgm.7z
[code]def73cb9eafed554363cadb6685e072575d5b1322b409dc96de9352d4f945647 waifusearch-0.1.tar.xz[/code]

BTW, I provided the current /robowaifu/ JSON files inside this archive as well. They are located inside the 'all_jsons' subdirectory. And the program will be expecting them to be there, even if you overwrite them all with newer versions provided from the ''Library'' thread in the future.

==Notes==

'''Dependencies'''
-The software has a dependency on the jsoncpp library, and I also use the meson build system. You'll need both if you follow my build instructions below.
-This is a multi-core enabled program. I use GCC to compile with, and they apparently use Intel's TBB to supply the underlying task queue system for g++ to provide the standard C++17 parallel execution policies.
>tl;dr
You'll also need to install the TBB dependency. All of these should be available from your package manager, and that's definitely the recommended approach here. But just in case, here's the source locations if not.
-''Meson''
https://github.com/mesonbuild/meson
-''JsonCpp''
https://github.com/open-source-parsers/jsoncpp
-''Threading Building Blocks''
https://github.com/oneapi-src/oneTBB

'''Building'''
-Initialize the project as a mesonbuild one. From the code directory:
[code]meson build[/code]
-Be sure to tell meson to use release mode before building the project. From the code directory:
[code]cd build && meson configure --buildtype=release && cd ..[/code]
-Either build from Juci, or you can just build w/ meson from the terminal instead. From the code directory:
[code]cd build && meson compile && cd ..[/code]

'''Running'''
-Execute the waifusearch program. From the code directory:
[code]build/waifusearch[/code]
-You should see something like this appear ('hello world' search example given):
[code]time to process local /robowaifu/ JSON data:  2322 ms

(q to quit)  enter search phrase:  hello world

                   ORDERED:
                   ========
    THREAD SUBJECT                      POST LINK
C++ General                       -> https://alogs.theГунтretort.com/robowaifu/res/12.html#6063     @ch: ~66
   "                              -> https://alogs.theГунтretort.com/robowaifu/res/12.html#6095     @ch: ~391
Selecting a Programming Language  -> https://alogs.theГунтretort.com/robowaifu/res/128.html#134     @ch: ~1102
Robowaifu-OS & Robowaifu-Brain(c  -> https://alogs.theГунтretort.com/robowaifu/res/201.html#208     @ch: ~75
Modern C++ Group Learning Thread  -> https://alogs.theГунтretort.com/robowaifu/res/4895.html#5422   @ch: ~150
   "                              -> https://alogs.theГунтretort.com/robowaifu/res/4895.html#5423   @ch: ~64
   "                              -> https://alogs.theГунтretort.com/robowaifu/res/4895.html#6529   @ch: ~242
Haute Sepplesberry Cuisine TBH    -> https://alogs.theГунтretort.com/robowaifu/res/4969.html#6313   @ch: ~772

                   UN-ORDERED:
                   ===========
    THREAD SUBJECT                      POST LINK
Robowaifu fiction to promote the  -> https://alogs.theГунтretort.com/robowaifu/res/29.html#50       
/robowaifu/ Embassy Thread        -> https://alogs.theГунтretort.com/robowaifu/res/2823.html#5158   

  full search took:  225 us
' hello world '  [8 : 2] = 10 results

(q to quit)  enter search phrase:  [/code]
-If so, you're all set (ignore the Гунт-abused links in this post, the real ones from the program work). You should be able to search across /robowaifu/'s posts quickly. Once you find a result you're interested in, just right-click over the post link and choose 'Copy Link Address' then paste into your browser.
>note: the program will also auto-generate two files, ''all_posts.txt'' & ''word_post_counts.txt'' when you run it. Feel free to look into them for search ideas or whatever you'd like.

I hope it's helpful enough for now Anon. Eventually, we'll expand it out to work across any imageboard that ''Bumpmaster'' supports. Cheers, and I hope you all have a Merry Christmas /robowaifu/ .

# 175
OK for ''waifusearch'', today added character trimming into the text parsing to properly handle bold and italic text in posts. Also, began a proper version log as well:
>version.log
[code]// waifusearch, the lightning IB searcher
// ======================================
// -This software is designed to search an imageboard's text fast

201226 - v0.1a
--------------
-add proper char trimming to address bold and italics text in posts
-add board_nm string, and output_files flag, user global vars
-add version log, and various comments to meson.build

201224 - v0.1
-------------
-initial release

NOTES:
-Currently, waifusearch only supports Lynxchan-based JSON files.[/code]
https://files.catbox.moe/sw058v.7z
[code]90db32390fc2eb18e567548af9381088d421cbd7c5ee88805e8510464098013d waifusearch-0.1a.tar.xz[/code]

Cheers, /robowaifu/ .

# 176
OK, I've done some needed housekeeping to clean up redundant processing and make maintenance easier in the future. No real performance differences, this is mostly just to ensure all text processing is uniform and help developers.

>version.log
[code]201228 - v0.1b
--------------
-refactor to remove redundant code, simplify & unify text processing
-add vec_pair_s_vpi alias[/code]

https://files.catbox.moe/pfn2tu.7z
[code]eaa25db2a04caf480ca76bd7d4c92c29f62774b4e6e1251154e834a0fb9ddb8f waifusearch-0.1b.tar.xz[/code]

# 177
For ''waifusearch'', today I added some timing breakdown details to the output. There are four distinct phases this tool goes through to optimize the speed of searching across the entire collection of words here, and each of these are detailed both as a percentage of the whole, and as raw microseconds.
>
I can now easily test any perf optimizations in different sections, as well as have a better feel for the underlying behavior. For example, I suspected it before but now have numeric data that the first phase (sea) needs front-loading the first time through. BTW, there is a user-global flag you can use to turn this display off if you'd like (as well as other vars):
[code]const bool        show_timing{true};[/code]
I'm probably pretty close now to the planned functionality I wanted for the tool at this early stage. If anyone has any suggestions, questions, or requests about it then feel free to let me know ITT.

>version.log
[code]201229 - v0.1c
--------------
-add display of timing breakdown details
-add disp_unfounds() function and outputs
-add percent_str() function to rw_text_utils.hpp
-rename alias' to better align w/ cppcoreguidelines (NL.5)
-minor function re-ordering[/code]

https://files.catbox.moe/dj7vr5.7z
[code]a19eb6fc377422734944cb2344c82ee996dce77be35e9ade66f104fbcbfcb602 waifusearch-0.1c.tar.xz[/code]

# 178
Alright, I added parallelization to the loop inside x, the costliest part of the system time-wise.
[code]void locate_terms(const Map_words_2_posts&        w_tp,
                  const std::vector<std::string>& terms) {
  const auto bgn_loc = clk_time.now();

  const uint32_t    pad_len{27};
  Map_words_2_posts uniques{};
  Vec_words_2_posts vw_vtp_valids{};

  // attempt a term locate inside the w_tp & copy it if found
  for_each(par_unseq, cbegin(terms), cend(terms), [&](const auto& term) {
    try {
      uniques[term] = w_tp.at(term);
    } catch (const out_of_range& e) {
      unfounds.emplace_back(rw::make_pad_str(term, pad_len));  // global
    }
  });

  cp_map_2_vec(uniques, vw_vtp_valids);
  sort_counts(vw_vtp_valids);  // sort terms by post counts, low to high

  time_spans.emplace_back(clk_time.now() - bgn_loc);  // time_spans[1]: loc

  if (show_terms)
    disp_terms(vw_vtp_valids, pad_len);

  if (! vw_vtp_valids.empty())
    find_intersects(vw_vtp_valids);
}[/code]

It doesn't bring too much to the table for very short (1 or 2 word) searches b/c setup overhead, but for searches that are sentence-length or longer it basically cuts the time by a quarter to a half (roughly speaking) on my box. 
>

I decided to go ahead and push a new rev on the same day since it's a fairly nice advance for ''waifusearch''. Should've done this refactor a bit sooner heh. :^)

https://files.catbox.moe/7k95kq.7z
[code]a82f71469d2db60834e12a03e76621201732afa1ff1547554d62e868f29447c5 waifusearch-0.1d.tar.xz[/code]
Cheers.

>===
-''edit sorting terms comment''

# 179
>>7966
>to the loop inside ''locate_terms()'' *
lol

# 180
Alright, to wrap things up for the time being for ''waifusearch'', I've broken down the timings a bit further in the costliest region to get more details. I've also added a bit of a safety check for the file writes which is probably a good idea in a multi-threaded context. I completed the javadoc comments for each function such as they are. I think I've worked out all the kinks as far as I can tell at this point. We'll go ahead and add a link to this tool in the OP of the ''Library'' thread as well now for anyone interested in research here.

Sometime next year I'll probably make time to get this building on the Raspberry Pi, so any Anons following along with that project can use waifusearch on their boxes at will. As things allow, eventually I'll integrate all this into the ''Bumpmaster'' project to search across the entire collections of boards an anon might have **I currently keep around 60 or so boards archived with ''BUMP''**. I also have a plan to create a small course around this tool in the ''C++ Learning Thread''. Having a specific project to learn from will probably be a beneficial thing for all concerned. And this utility is in fact doing a few interesting things that will be helpful for anyone in the class to know about in detail.

That aside, the ultimate goal here ofc is to lay a foundation for our waifus to have a good search system to retrieve any textual information generally speaking, and not just to shitpost along with us. But little-by-little. And who really knows? This may very well turn out to be the year of the robowaifu for us all or at least additional good progress on that timeline. Here's hoping! :^) BTW, I thought it would be fun to adopt ''Sumomo'' as the official mascot of the project, in honor of the many times she served in doing searches!

[code]201231 - v0.1e
--------------
-add add'l timing sections for copy and sort operations
-add write_file_ready() to rw_text_utils.hpp
-add std::accumulate in disp_timing()
-for locate_terms(), wrap processing after loop in sanity check block
-add have_results flaq & test
-add javadoc comments for functions
-minor function re-ordering[/code]

https://files.catbox.moe/uc4uit.7z
[code]7c13ced53ed67e5d21e7cdd9456a57d2f2922f13643b91a8abd80f612ef49477 waifusearch-0.1e.tar.xz[/code]

Cheers, and I hope you all have a very Happy New Year /robowaifu/ . Godspeed to us all this year. :^)

# 181
>>7975
Thanks. This all sounds great. Didn't really use it yet, because I tried to get another software done to the end of the year but it turned out to take more time and I dropped out for a while doing other stuff like sorting data.
>building on the Raspberry Pi
Thanks, I was looking into it. I think "Threading Building Blocks" would need to come from Github, while jsoncpp and meson are available in Raspian repo.
> adopt Sumomo as the official mascot of the project
Great idea, she's great.
 > Happy New Year /robowaifu/
Thanks again. I'm sure we will have a good year, and I wish everyone the same.

# 182
>>7999
>Thanks, I was looking into it. I think "Threading Building Blocks" would need to come from Github, while jsoncpp and meson are available in Raspian repo.
Welp, I have good news and bad news Anon. First the good news; TBB is included already in the Raspian repo:
>

If you search Synaptic for ''TBB'', you'll see
>''libtbb-dev''
>''parallelism library for C++ - development files''

Now the bad news; GCC8 ''doesn't actually support'' the C++17 parallelism execution policies. Only version 9 (and later) does. My apologies, I wasn't aware and ATM only g++8 is on the RPi.

Now, for the '''other''' good news... **:^)**
I __was__ able to get ''waifusearch'' working on the RaspberryPi despite that (though it runs more slowly):
>

There are a number of changes I needed to make to pull it off, so it will take me a bit to get things cleaned up and to explore anything I can improve upon with it. I'll try to package up a new revision by this weekend (possibly a RPi-specific one) and post it ITT.

Stay tuned Anon.

# 183
>>7999
>>8017
I went ahead and did a full tutorial of the build process in the ''Sepplesberry'' thread for everyone, Anon.
>>8026

Cheers.

# 184
Implemented an easy to use named-timer mechanism today. A container is maintained system-wide for all timings, and whenever a Timer object is created it begins timing automatically, and when it goes out of scope or is explicitly stopped it calculates the difference and stores that into the system container.
>Timer.hpp
[code]#pragma once

#include <chrono>
#include <string>
#include <utility>
#include <vector>

namespace rw {

// alias'
using Clock   = std::chrono::steady_clock;
using Time_pt = std::chrono::time_point<Clock>;

// globals
static std::vector<std::pair<std::string, Time_pt>> named_timings{};

// usings
using std::make_pair;
using std::move;
using std::string;

class Timer {
 public:
  Timer(const std::string& timer_name)
      : name{move(timer_name)}, start{Clock::now()} {}
  ~Timer() {
    if (! have_stop)
      stop();
  }

  void stop() {
    named_timings.emplace_back(make_pair(move(name), (Clock::now() - start)));
    have_stop = true;
  }

 private:
  const string  name;
  const Time_pt start;
  bool          have_stop{false};
};

}  // namespace rw[/code]
Using it is quite simple, and you can rely on the stop() function, or simply let it fall through and RAII will do the trick. Here's an example of both ways:
>snippet.cpp
[code]void foo() {
  Timer t{"foo"};
  sleep_for(Sec{1});
}

int main() {
  Timer t{"main"};
  cout << "Hello World!\n";
  t.stop();

  foo();

  if (disp_timings)
    // rw::disp_timings();
    rw::disp_us_timings();
}[/code]
Note how clean and simple the RAII form is when appropriate. I'll probably use this all over my general-purpose code now as a form of perma-profiling since the perf impact is practically nil and iterating the ''named_timings'' container is strictly a standard approach.

Example output from above snippet:
[code]Hello World!
main timer took: 74 us
foo timer took: 1000231 us[/code]

# 185
OK, so I've made a few developer-oriented improvements to ''waifusearch'', nothing that really changes it's usage but makes the code a little cleaner internally. I've integrated my nifty little 'fire-and-forget' named timer class into the tool, and also changed the timings display to make it a bit more readable (raw microseconds and percentage-of-total numbers are now grouped together with the timer name itself). 
>

I also added a flag to the ''meson.build'' that should stop the annoying notes coming up from GCC when you build on the RaspberryPi. The comments in that file have been tweaked a little for the RPi as well.
>version.log
[code]210112 - v0.1g
--------------
-add Timer.hpp for cleaner automated timings
-move to disp_pct_timings() using new Timer class
-move user-configurable globals to user_flags.hpp
-simplify parallel execution guard macros
-move to std::copy algorithm in assemble_words()
-relocate assemble_words() to rw_text_utils.hpp
-add build comments for RPi version to meson.build
-add '-Wno-psabi' project arg to meson.build
-minor code-consistency cleanups[/code]
https://files.catbox.moe/dlijqn.7z
[code]189aea5e788b4d163f918407a03052633a9cc6b3e33460688efbee9c06972128 waifusearch-0.1g.tar.xz[/code]
I hope you're doing well so far this year, /robowaifu/ . Cheers.

# 186
OK, I've finally gotten around to adding command-line parsing to waifusearch. This will make it far more convenient to change it's behavior a little. For example, switching between outputting in-board crosslinks, or full hyperlinks.
>

>version.log
[code]210115 - v0.1h
--------------
-add command-line arguments parsing
-patch minor RPi using bug[/code]
No other improvements included with this version, but the benefit of having program arguments is more than valuable enough to make a special push just for that.

https://files.catbox.moe/bkflel.7z
[code]312a27a8cbb86e0b8f808fda0c36695fefc91c73ed7c870b6a21384f8752914b waifusearch-0.1h.tar.xz[/code]
Cheers.

# 187
>>8103
>the archive of /robowaifu/ thread JSONs is available for researchers
>latest revision 210120:
https://files.catbox.moe/0qyvy6.7z

Just in case the place is deplatformed, here's today's version. It may be a while before I do anything else with waifusearch (beginning to mostly work on Bumpmaster instead now) so if you have anything else in it you'd like to see I'd say ask me about it soon while the code is still fresh in my mind. 

So, the latest versions of the JSON archives should be posted occasionally in the Library thread's OP.

Cheers.

# 188
OK, so I made a couple of small display improvements and patched a minor bug related to unfound terms display.

>version.log
[code]210126 - v0.1i
--------------
-show unfound terms early in the results display
-strip unfound terms from the final search phrase display
-add clean_unfounds() wrapper
-add squash_n_trim() func to rw_text_utils.hpp
-rename trim_lr() func in rw_text_utils.hpp
-rename rm_substrings() func in rw_text_utils.hpp
-remove unnecessary short-circuits in find_intersects()
-patch minor display bug with unfound terms[/code]
https://files.catbox.moe/yuq4z3.7z
[code]3b7a5d7a8ff662c448a1f71d57fb6d82f170019806ddd7fe958343edce29d280 waifusearch-0.1i.tar.xz[/code]

# 189
>>8293
Thanks, I hope I can make it to try it out today.

# 190
>>8297
>software building instructions >>7933
>RaspberryPi building instructions >>8026
The RPi instructions are probably a little more hand-holding and basically apply to any Linux box. Just ask ITT if you get stuck Anon.

# 191
Comments from inside the file ''meson.build'' :
[code]# ===
# DEPENDENCIES:  jsoncpp, mesonbuild (and other than on RaspberryPi), tbb
# You should install these from your distro's package manager if possible.
#
# As of this date in 2021, these are the sources of the 3 external dependencies;
#
# -JsonCpp
# https://github.com/open-source-parsers/jsoncpp
# -Threading Building Blocks
# https://github.com/oneapi-src/oneTBB
# -Mesonbuild (optional, but recommended)
# https://github.com/mesonbuild/meson

# ===
# BUILDING WITH MESON (from the code directory):
# -Initialize the project as a mesonbuild one.
#    meson build
# -note: This step is needed only once, or again after a version change.
#
# -Build, Execute.
#    cd build && ninja && cd .. 
#    build/waifusearch

# https://mesonbuild.com/Reference-manual.html

# ===
# BUILDING WITH g++ (from the code directory):
# -Build, Execute.
#    g++ main.cpp -std=c++20 -O3 -ljsoncpp -ltbb -o waifusearch
#        -(or on RPi):
#        g++ main.cpp -std=c++2a -O3 -ljsoncpp -lstdc++fs -o waifusearch
#    ./waifusearch

# -With either build approach, only the final execution step is
#  needed anytime thereafter.[/code]

# 192
Made a minor usage change where hyperlinks are now the default (change this with the '-y' flag) . My original thinking on this was looking towards the future when waifusearch will be fully integrated with the upcoming Bumpmaster imageboard system. But until then while this tool is still just a simple CLI-based search, it's more useful to present hyperlinks in the terminal instead I think. Other than that, made some minor display cosmetics and one small, proactive code modification.

>version.log
[code]210128 - v0.1j
--------------
-rename 'make_crosslinks' to 'make_hyperlinks' (hyperlinks are now the default)
-move clean_unfounds() earlier in processing chain (avoiding a potential bug)
-only display 'ORDERED' header if both types are present
-similarly, only segregate counts if 'UNORDERED' results are present
-minor javadoc edits[/code]
https://files.catbox.moe/52t4ku.7z
[code]224c28818ed61406419550c08f4bd25544838950eddb28a4ec1bfac60b876448 waifusearch-0.1j.tar.xz[/code]
Should have the build file squared this time, cheers.

# 193
>>8337
Your work is much appreciated. I'm only looking into it now, though, for various reasons. One is, that I wanted to find a way to check CPP code for dangerous commands, before using something I downloaded from a anonymous source from the web. Also, maybe understanding a bit of it. I'm using cppcheck now, and got some errors:

[code]Checking .../waifusearch-0.1j/rw_text_utils.hpp ...
/waifusearch-0.1j/rw_text_utils.hpp:27:0: error: failed to evaluate #if condition, division/modulo by zero [preprocessorErrorDirective]
#if __has_include(<jsoncpp/json/json.h>)  // RPi's version[/code] Maybe it works nevertheless, but cppchecks stops checking the file with that error in it.

I think this stuff here is unimportant or just warnings about what a file does: [spoiler][code].../waifusearch/waifusearch-0.1j/CLI11.hpp:7109:0: error: Exception thrown in function declared not to throw exceptions. [throwInNoexceptFunction]
        for(const App_p &com : subcommands_) {
^
Checking ... /waifusearch/waifusearch-0.1j/rw_cli_args.hpp: CLI11_HAS_FILESYSTEM;__has_include...
Checking ... waifusearch/waifusearch-0.1j/rw_cli_args.hpp: CLI11_HAS_FILESYSTEM;__has_include;_GLIBCXX_RELEASE;__cpp_lib_filesystem...
Checking .../waifusearch/waifusearch-0.1j/rw_cli_args.hpp: CLI11_HAS_FILESYSTEM;__has_include;__GLIBCXX__;__cpp_lib_filesystem...
Checking .../waifusearch/waifusearch-0.1j/rw_cli_args.hpp: CLI11_HAS_FILESYSTEM;__has_include;__MAC_OS_X_VERSION_MIN_REQUIRED...
Checking .../waifusearch/waifusearch-0.1j/rw_cli_args.hpp: CLI11_HAS_FILESYSTEM;__has_include;__cpp_lib_filesystem...
Checking .../waifusearch/waifusearch-0.1j/rw_cli_args.hpp: _HAS_STATIC_RTTI;__GXX_RTTI;__cpp_rtti...
Checking .../waifusearch/waifusearch-0.1j/rw_cli_args.hpp: _MSC_VER...
Checking .../waifusearch/waifusearch-0.1j/rw_cli_args.hpp: _WIN32...
Checking .../waifusearch/waifusearch-0.1j/rw_cli_args.hpp: __CUDACC__...
Checking .../waifusearch/waifusearch-0.1j/rw_cli_args.hpp: __GNUC__...
[/code][/spoiler]

# 194
>>8387
That's fine, it's a good idea actually. The first one is failing because cppcheck isn't properly evaluating the non-standard GCC macro ''__has_include''
https://gcc.gnu.org/onlinedocs/cpp/_005f_005fhas_005finclude.html

Not too surprising, but it should be checking pretty common compiler vendor macros like that.

The second one is probably a minor bug on the part of the CLI11 library writer. It's pretty irrelevant in this case, and in particular that quite simplistic way I'm using the library to just check the command argument and then set the global user flags. These are OK Anon.

>Also, maybe understanding a bit of it. 
I wrote this software myself, so ask away if you ever have any questions Anon. BTW, I'll be doing some new work on waifusearch to add ''Boolean logical operators'' into the search capabilities. This will obviously be helpful improvement. Starting with '''OR''' today.

# 195
>>8390
I tried this, after reading the link. I probably did something wrong. It didn't work.
[code]
#if defined __has_include &&  if __has_include(<jsoncpp/json/json.h>)  // RPi's version
#  include <jsoncpp/json/json.h>
#  else
#  include <json/json.h>
#endif
[/code]

# 196
>>8549
If you want to perform the defined test first, then use this:
[code]#if defined __has_include
#if __has_include(<jsoncpp/json/json.h>)  // RPi's version
#include <jsoncpp/json/json.h>
#else
#include <json/json.h>
#endif
#endif[/code]
BTW, if you aren't building for the RPi, then you don't need any of this. Just include the JsonCpp header from it's normal location:
[code]#include <json/json.h>[/code]
Let me know how it goes if you get stuck Anon.

# 197
>>8552
Oh, I just needed to comment it out, then it worked. Also, I only installed the dev version libjsoncpp after doing this check. I had the wrong one. 

Finally I installed it, and it's great. Didn't even know till I installed it, that it only searches the downloaded json. No problem, just a surprise. I'll look into Bump next.

# 198
>>8554
>Didn't even know till I installed it, that it only searches the downloaded json. No problem, just a surprise. 
Yeah, one of my long-term design goals is to lay a foundation for text processing for our robowaifus that will work 
A) At lightning speed. 
B) Directly on-board mobile, tiny processors (ie RPi & other SBCs). 

These are basically interrelated concerns in a sense and means both a local copy of data, and also basically necessitates a compiled-code solution in either Assembler, C, or C++ . I chose C++ for what I hope are (or at the least ''will be'') apparent reasons to everyone in the end.

>I'll look into Bump next.
I actually am working on the next version (I'm that author as well) and intend to integrate ''waifusearch'' directly into the tool so anyone can search across whole libraries of shitposting in a flash. Ostensibly it's because it will be a nice feature to have in Bumpmaster. But in fact, it's to lay a groundwork for the AI in our waifus to be able to gain context quickly from ad-hoc, ad-lib, de-facto slanguage posts from Anons in English. And to do it very fast on minimal hardware.

After all, I want my waifu to be able to shitpost the bantz with me right? :^)

# 199
>>8556
>waifus to be able to gain context quickly from ad-hoc, ad-lib, de-facto slanguage posts from Anons
Yeah, that's gonna be awesome.

# 200
>>8556
What I'm missing in BUMP-2d are building instructions. I don't know what kinf of libcurl library it needs, and don't want to try all of them out.

# 201
>>8560
It's still going to take a lot of work Anon, but yes it will be. The techniques I'm trying to master in ''waifusearch'' are basically only just prep work. 'Assistants to the Chief', as it were. The real heavy-lifting will come from libraries like mlpack & Armadillo. And even that is just the 'sharp tools for the Carpenter'. It will take the teamwork of multiple anons willing to learn & use compiled languages well enough, and some with a good understanding of the mathematical basis of ML, to join in the team and begin contributing. Hey, Lewis & Clark didn't actually build the railways out to the West themselves! They simply blazed a trail for others to follow across.

>tl;dr
It will go faster if you and others crack the books, and join in Anon. :^)

>>8562
Any reasonably current version of the dependencies, including dev libcurl, should all work. Sorry about the lack of adequate build instructions Anon. It's roughly equivalent to those of waifusearch, since it also uses mesonbuild. If you can wait a week or so, I'll try to assemble an interim release for you where I correct this and I'll link it here. It won't really be a new version ''per se'', but it should at least have clearer build instructions for it. The new system is called ''Bumpmaster'', and will be a good bit more powerful. But it probably won't be till late spring/early summer when I can give it more focus that the first version will be released.

# 202
>>8565
I don't really need it anytime soon, just FYI:
At first it seems like it's that line in meson.build, what cases the error:
>curl_dep = cxx.find_library('curl')
I have libcurlpp-dev and libcurl4 installed.
It returns: "meson.build:21:0: ERROR: C++ library 'curl' not found" but if I comment the line above out, then it just uses the next line to case an error. 
[code]Version: 0.52.1
Source dir: /.../BUMP-02d/BUMP-0.2d
Build dir: /.../BUMP-02d
Build type: native build
Project name: BUMP
Project version: 0.2d
C++ compiler for the host machine: c++ (gcc 8.3.0 "c++ (Raspbian 8.3.0-6+rpi1) 8.3.0")
C++ linker for the host machine: GNU ld.bfd 2.31.1
Host machine cpu family: arm
Host machine cpu: armv7l
[/code]

# 203
>>8576
OK, I'll do my best to make sure that BUMP builds and runs on the RaspPi first before I push the next version Anon. (I created BUMP before I thought of having C++ classes on /robowaifu/ .)

# 204
Another suggestion, which would probably be easy to implement: It would be great if Waifusearch could be called directly in the shell with some search string and would then write the result to stout. I think this is necessary to call it from other programs as well, and then work with the result in that program which is calling Waifusearch.

# 205
>>8620
Good suggestion, thanks. I understand that would be a better fit with the Unix Philosphy. I simply wanted to do a boatload of different searches when I first got it working and so I did a 'search loop' instead of the more normal approach.
[code]/**-----------------------------------------------------------------------------
 @brief    Front end to search-loop the word@post map 'w_tp' for user's query
 terms.

 @param    w_tp [IN] The word/thread+post map to search through.
*/
void do_search(Map_words_2_posts& w_tp) { //... [/code]
It should be rather straightforward to make the system run in a single-shot mode instead. When I make time, I'll add a flag, probably -s with a string argument to it that should work. R/n I'm working on all the weird edge cases in doing simple Boolean ORs. I should have that ready by this weekend I think, and then I promised Anon to have a go at getting BUMP working on RPi.

Once those are out of the way I'll add your flag so it can be scripted, etc., and I'm planning to go ''full-CAS'' with /robowaifu/ text searching at some point after that so we can really spell out exactly what kinds of things to look for for our waifus.

I should probably just skip that whole ordeal and go with the regex library, but a) I want to understand it more deeply first before I just give over >>8568, and b) it's just possible that I may be able to eventually turn this system into a fully-distributed system than can run searches concurrently across many machines at once. If we can pull ''that'' off here, then chewing through various large corpora at high speed should be a snap for our waifus.

# 206
>>8622
>and I'm planning to go full-CAS 
I just checked and was surprised to see so many different ''CAS'', so I'll be explicit:
https://en.wikipedia.org/wiki/Computer_algebra_system

I mean I want us to be able to ask our waifus for detailed searches that might look something like this in the underlying C++ code's execution path:
[code]waifusearch> (Chii OR Sumomo) AND Hideki NOT (Hibiya OR Yumi) AND School[/code]
Probably not a great example off the top of my head but you should get the picture. A long way from a NLP front-end, but eventually that front-end would need to produce something like the above to run through a lot of data. Since that's actually a useful enough feature (and simpler!) I'll try to get that underlying part working very fast, first.

# 207
>>8622
> I'll add a flag, probably -s with a string argument
Yeah, this is the way. :)
>go with the regex library
If it was just for some search engine, then there's also Elastic Search. Don't know much about it, but it seems to be good. However, the interesting thing about your project might be that it is so small that it might fit into a small app for a phone or tablet. I already mentioned BUMP  somewhere a while ago, to people which might be interested in building something like the Omnichan app.
>I want to understand it more deeply first before 
Yeah I understand, and won't criticize that notion. Just keep in mind that building on already existing stuff might let you build more powerful things faster.
>full-CAS 
This looks very useful.

# 208
>>8624
>However, the interesting thing about your project might be that it is so small that it might fit into a small app for a phone or tablet.
Exactly. My target platform is low-end SBCs like the RPi, actually. I want our robowaifus to be able to interact with us verbally in realtime ''totally disconnected from other computing resources'' in a fast and energy-efficient way.

Onboard, compact data sources, and efficient, compiled code (or even critical sections of actual machine code) are the only way to pull that off. This software would easily run 100 times over in a modern phone.

>protip:
**waifusearch> Omnichan app**
**:^)**

# 209
OK so here's the new version of waifusearch. We've moved up a point level. We now support using a Boolean OR to separate different (but usually related) phrases together into the same search. This is definitely the largest modification yet to the code. Basically not only to support using Boolean OR for now, but also to refactor the architecture to support more sophisticated CAS (computer algebra system) type operations on the searches in the future. 

Also, performing a one-shot search is also supported now using the '''-s''' flag, combined with a string argument containing the search text. Please note, this isn't very performant ATM because the code has been designed to process the JSON text into an efficiently-traversed memory structure, and then repeatedly using that same structure over and over. Performing a one-shot means (for now) always ''re-doing'' that front-loading each time. In the future, I plan to serialize this already-processed data out to a disk file. That would then provide the ability to read that file back directly into the waifusearch memory structures instead of recreating them from scratch each time. But for now -- while it actually works -- doing a one-shot isn't anywhere near as responsive as normal searches are.

>version.log
[code]210220 - v0.2a
--------------
-refactoring to support Boolean operators 'OR' , '|' , in search specification
-add one-shot search capability, suited to scripting waifusearch
-add search phrase/words to listing output
-use 'waifusearch' prompt instead
-add disp_offsets user flag
-add search_once user arg
-add do_Boolean_ops() func
-add map_phrase_groups() func
-add match_phrases() func
-add search_n_tag() func
-add sep_search_phrases() func
-ren ld_phrase_map() func
-add cp_sort_disp() func
-add parse_to_csv() func in rw_text_utils.hpp
-add trunc_pad_str() wrapper in rw_text_utils.hpp
-add rw_gen_utils.hpp header
-add Vec_phrase_grps alias
-add multi-threading memory fencing
-remove redundant unfounds.clear() operation[/code]
https://files.catbox.moe/kiasfm.7z
[code]5e0360c493892863a1741c4143a8e9c7320eccaf722a7c026fe9cbe082318687 waifusearch-0.2a.tar.xz[/code]

# 210
>>8678
Here's an example usage of the new Boolean OR feature:
[code]build/waifusearch -y false -t true -e true
time to process local /robowaifu/ JSON data:  3017 ms

waifusearch>  hello world | foo bar
 term:  foo                          count:  15
 term:  bar                          count:  18
 term:  hello                        count:  63
 term:  world                        count:  309
# terms found:  4

                  ORDERED:
                  ========
   THREAD SUBJECT                      POST LINK
C++ General                        >>3717    foo bar
   "                               >>6063    hello world
   "                               >>6095      " 
   "                               >>7921      " 
   "                               >>7933      " 
   "                               >>8057      " 
Selecting a Programming Language   >>134       " 
Robowaifu-OS & Robowaifu-Brain(c   >>208       " 
Modern C++ Group Learning Thread   >>5420      " 
   "                               >>5422      " 
   "                               >>5423    hello world, foo bar
   "                               >>5425    foo bar
   "                               >>6529    hello world
Haute Sepplesberry Cuisine TBH     >>5730      " 
   "                               >>6313      " 

                  UN-ORDERED:
                  ===========
   THREAD SUBJECT                      POST LINK
C++ General                        >>1075    (foo, bar)
Robowaifu fiction to promote the   >>50      (hello, world)
/robowaifu/ Embassy Thread         >>5158      " 
Modern C++ Group Learning Thread   >>5424    (foo, bar)

' hello world | foo bar '  [15 : 4] = 19 results
--------------------------------------------------------------------------------
 total:    sea:74     loc:238    ldm:33     dbo:19     snt:86     mch:22     us
 472 us       :16        :50        : 7        : 4        :18        : 5     %
--------------------------------------------------------------------------------[/code]

Note how when the two phrases both appear inside the same post, then both phrases also appear at the end of the result. Here's an example where two ''exact matches'' both appear inside the same post:
[code]>>5423    hello world, foo bar[/code]
Whenever all words in a phrase appear in a post, but they aren't in the exact order specified in the search, then the words of the phrases will appear as CSVs inside parenthesis:
[code]C++ General                        >>1075    (foo, bar)
Robowaifu fiction to promote the   >>50      (hello, world)[/code]

# 211
>>8678
Wow, that's great. Seems to be some big leap forward. 
>Performing a one-shot means (for now) always re-doing that front-loading each time
Yes, that's always a problem. I ran into the same problem with my chatbot and graph parsing. The alternative to storing it, would be to let the parsing be done in a program which runs in a daemon mode, while the search part can be called by another program.

# 212
>>8688
>daemon
Yes, I considered exactly that as the solution for **a good bit** later when we're actually implementing such a tool in a production runtime for our robowaifus. 

And as you basically indicated, I imagine there are entire classes of types of solutions that would require multiple, cooperating components for their systems to function correctly.

For example, when we adopt a Neuromorphic response strategy for our robowaifu's 'nerve & muscle' sense/response cycles, we'll need to adopt both a real-time tiny kernel directly into the sensor hardware to provide for instantaneous responses. This will enable her to have self-defense for thing like avoiding dangerous, hot or sharp objects for example -- same as the designs we ''bios'' enjoy having. 

OTOH, within a short time-frame (say 5ms), there may also be the need her to have the ability for higher-order functions to kick in to direct her to go on in and proceed -- even in the face of danger. Again (but in a little different, 'human being' way) ''same as we people do''.

To my thinking this simple example spells out one of the many design-separation boundaries between static & one-shot/repetition processing that will be needed for effective Robowaifu Systems Engineering design strategy & engineering approaches.

# 213
Updated ''BUMP'' to work with the RPi, but the instructions for building & running should work similarly for other Linux distros.
>>8769

# 214
>>8562
>>8576
I meant to have this for you sooner Anon.
>>8769

# 215
I'm not sure where to post this, I made a C++ imageboard some time ago. it lacks some important features and I'm not developing it anymore, but I thought it might be useful or interesting to someone: gitlab.com/schinopsis/cxxchan

# 216
>>8823
Thanks I'll have a look Anon.

# 217
>>8823
Apologies, but I wasn't able to see the repo. Looks like Gitlab is forcing Tor users to log in now before you can even see a repo. 
>

This is of course a very bad development on their part if true. I'll be looking to move my little repo off there if this turns out to be the case. Any chance you can zip the repo into a flattened version
https://stackoverflow.com/questions/4506758/flatten-old-history-in-git
and then just post it onto catbox.moe ?

# 218
>>8830
my fault, it was set as private by default

# 219
>>8835
Ah I see, grabbed a clone and I'll give it a look. Eventually, the ''Bumpmaster'' project should basically be a high-performance, standalone on- and off-line imageboard program. It will be written mostly (if not entirely) in C++ (with some C dependencies on well-established libraries like cURL).

# 220
Video interview with Bjarne Stroustrup in March. This lockdown racket scheme has visibly taken a toll on him this past year. :/
https://www.youtube.com/watch?v=8aIqIBmNJyM

# 221
So I finally installed waifusearch v0.2a. It worked, but I got some error messages:
[code]g++ main.cpp -std=c++2a -O3 -ljsoncpp -lstdc++fs -o waifusearch

In file included from /usr/include/c++/8/vector:69,
                 from /usr/include/c++/8/bits/fs_path.h:37,
                 from /usr/include/c++/8/filesystem:37,
                 from main.cpp:12:
/usr/include/c++/8/bits/vector.tcc: In member function \u2018void std::vector<_Tp, _Alloc>::_M_realloc_insert(std::vector<_Tp, _Alloc>::iterator, _Args&& ...) [with _Args = {std::pair<std::chrono::duration<long long int, std::ratio<1, 1000000000> >, std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> > >}; _Tp = std::pair<std::chrono::time_point<std::chrono::_V2::steady_clock, std::chrono::duration<long long int, std::ratio<1, 1000000000> > >, std::__cxx11::basic_string<char> >; _Alloc = std::allocator<std::pair<std::chrono::time_point<std::chrono::_V2::steady_clock, std::chrono::duration<long long int, std::ratio<1, 1000000000> > >, std::__cxx11::basic_string<char> > >]\u2019:
/usr/include/c++/8/bits/vector.tcc:413:7: note: parameter passing for argument of type \u2018std::vector<std::pair<std::chrono::time_point<std::chrono::_V2::steady_clock, std::chrono::duration<long long int, std::ratio<1, 1000000000> > >, std::__cxx11::basic_string<char> > >::iterator\u2019 {aka \u2018__gnu_cxx::__normal_iterator<std::pair<std::chrono::time_point<std::chrono::_V2::steady_clock, std::chrono::duration<long long int, std::ratio<1, 1000000000> > >, std::__cxx11::basic_string<char> >*, std::vector<std::pair<std::chrono::time_point<std::chrono::_V2::steady_clock, std::chrono::duration<long long int, std::ratio<1, 1000000000> > >, std::__cxx11::basic_string<char> > > >\u2019} changed in GCC 7.1
       vector<_Tp, _Alloc>::
       ^~~~~~~~~~~~~~~~~~~
/usr/include/c++/8/bits/vector.tcc: In member function \u2018void rw::Timer::stop()\u2019:
/usr/include/c++/8/bits/vector.tcc:109:4: note: parameter passing for argument of type \u2018__gnu_cxx::__normal_iterator<std::pair<std::chrono::time_point<std::chrono::_V2::steady_clock, std::chrono::duration<long long int, std::ratio<1, 1000000000> > >, std::__cxx11::basic_string<char> >*, std::vector<std::pair<std::chrono::time_point<std::chrono::_V2::steady_clock, std::chrono::duration<long long int, std::ratio<1, 1000000000> > >, std::__cxx11::basic_string<char> > > >\u2019 changed in GCC 7.1
    _M_realloc_insert(end(), std::forward<_Args>(__args)...);
    ^~~~~~~~~~~~~~~~~
[/code]

# 222
>>10484
Hmm. Thanks for letting us know Anon. So, when you say 
>''It worked''
do you mean you were able to successfully, build, run, and search with it? Something else?

BTW, would you double-check your ''meson.build'' file, you should see a line like this:
[code]add_project_arguments('-Wno-deprecated-declarations', '-Wno-psabi',
                      language: 'cpp')[/code]
The ''no-psabi'' warning directive should have disable that warning.

# 223
>>10485
>g++ main.cpp -std=c++2a -O3 -ljsoncpp -lstdc++fs -o waifusearch
Ahh, that must be it. Apologies, I neglected to add that directive to the comment on line #61. It should read:
[code]#        g++ main.cpp -std=c++2a -O3 -ljsoncpp -lstdc++fs -Wno-psabi -o waifusearch[/code]

I've amended that comment line and it will be in the next version of the tool. Try rebuilding with that command instead and let me know how it goes please.

# 224
>>10487
I might rebuild it tonight, if I don't forget it before going to bed. It works anyways, I mean searching and all. No errors so far.

# 225
>>10489
> It works anyways, I mean searching and all. No errors so far.
You're fine then, that was just an odd warning that the GCC devs added for that version of the compiler -- which they apparently later dropped in newer versions (thankfully). 

Also, I'd advise you to grab the latest version of the JSON archives to update it with. I'll try to start generating those on a more frequent basis.

# 226
Microcontroller-oriented C++ blogpost.
>'''A C++ (subset?) for small micro-controllers'''
http://www.voti.nl/blog/?p=114

# 227
>>8678
Feature request: Sometimes I wonder if a link, or more specifically a YouTube video, has already been posted. I think Waifusearch doesn't find that right now. If that's easy to change, it might be worth considering, same for files.

# 228
>>10791
Noted. Actually, it ''will'' return any part of the YT video link, eg, the hash of it. But ofc that's not particularly useful by itself. The other part ofc is if the poster actually mentioned the name of the video in his post.

I went through and found at least 400 YT videos have been linked here on /robowaifu/. I'm currently working on ''Bumpmaster'' atm, but I've given some thought to creating some kind of video link scraper that will auto-generate proper youtube-dl links.

Maybe we should have a set of crosslinks on our library thread for something like this Anon? After all, it's why the thread was created in the first place to help everyone locate anything posted here.

# 229
>>10791
>same for files.
Apologies, I missed that. Yes, that's a pretty easy addition and I had already planned to incorporate that soon. Be aware, it would only be a filename search, not some type of AI-context analysis relying on huge globohomo cloud datacenters. So, if an anon posted a well-named file, you might get lucky that way. OTOH, if it's just a SHA or other type of hash name, then probably not so much.

One feature I want to add into ''Bumpmaster'' is crowd-sourced tagging of posts & other content, including images. We potentially could conceivably even tap into the work the Hydra community has done in this area.

# 230
>>10794 >>10795
Sounds all very good, thanks. I probably could get all inks out of the json archives and also download them this way, including the description.

# 231
>>10809
Yep, and there are a few of them here too:
[code]waifusearch>  youtube OR youtu.be
.  .  .
' youtube | youtu be '  =  476 results

waifusearch>  [/code]

# 232
>>10812
Yeah, if it's possible to build on Waifusearch, it's probably better to do it that way.

# 233
just leaving this here for future reference.
https://github.com/adobe-fonts/source-code-pro

# 234
New talk by ''Sean Parent''
https://www.youtube.com/watch?v=NO5wHzI_oug

Turns out, he's finished all the talks for his book, and is now just doing the writing. Also, he's starting the '''STLab''' at Adobe back up, and ''David Abrahams'' will be joining him there. This is great news ofc. 

We probably will get a very polished implementation of an efficient, scalable & robust ''continuations library'' out of this collaboration. This is great news for /robowaifu/ and should make things like anon's ''IPCNet'' (>>2418) and anon's ''RPCS'' (>>11018) doable on very lightweight hardware, and relatively quite simple to write the underlying 'fabric' software itself.

# 235
What would be the fastest way to do matrix multiplication in C++? With compiler optimizations, profiling and everything. I wanna implement a transformer with raw, absolute speed. No fluff or usable code, just pathological maximum efficiency, running on a Raspberry Pi 4B.

The matrix operations in the self-attention layers will also be a key part to optimize:
[code]# query: (batch_size, query_length, heads, heads_dim)
# key: (batch_size, key_length, heads, heads_dim)
# energy: (batch_size, heads, query_length, key_length)
energy = einsum("nqhd,nkhd->nhqk", (query, key))[/code]

[code]# attention: (batch_size, heads, query_length, key_length)
# value: (batch_size, value_length, heads, head_dim)
# out: (batch_size, query_length, heads, head_dim)
out = einsum("nhqk,nvhd->nqhd", (attention, value)).view(batch_size, query_len, self.heads * self.head_dim)[/code]
Einsum is just a way to describe multiplying and adding matrices and transposing axes. How can these three things be done most efficiently?

# 236
>>12422
>The real heavy-lifting will come from libraries like mlpack & Armadillo (>>8565)
You won't be able to outperform the pure-template libraries of Armadillo lad. And since you're interested in doing this type maths for ML work, you may as well ride with mlpack to utilize it with. Besides, we already have AI researchers here working with both, so you'll be right at home with it, /robowaifu/ speaking.
https://mlpack.org/
http://arma.sourceforge.net/

# 237
>>12422
>>12424
If you just want to cut to the chase, this lad has already hatched together a tensor contraction algorithm you can tinker around with for starters.
https://github.com/romeric/Fastor

I'm sure you'll have your hands full getting all this to work well on wee hardware like the RPi, but of course that's a serious and fundamental goal for the ''Model A'' robowaifu prototyping stage, so go to it you madlad! :^)

# 238
>>12425
>I'm sure you'll have your hands full getting all this to work well on wee hardware like the RPi
I've been doing some tests and the RPi is roughly 1/10th the speed of my PC. Full-attention layers are probably out of the question but it should be able to handle linear attention. Fastor looks amazing. I hadn't heard of this.

>>12424
Armadillo might have some issues with it: https://romanpoya.medium.com/a-look-at-the-performance-of-expression-templates-in-c-eigen-vs-blaze-vs-fastor-vs-armadillo-vs-2474ed38d982
But I don't think the norm function is needed for inferencing, only clipping the gradient during training. I'll test them both and see which is faster.

# 239
>related crosspost (>>12439)

# 240
Do the C++ anons here have this channel on their radar? Dave's garage: https://youtu.be/B9DouAlkZlc

# 241
>>12739
Thanks for the heads-up Anon, but something titled >'' 'New!  Stupid C++ Tricks - Most Dangerous C Functions (E02)' ''
doesn't sound like something I'm really interested in spending the bandwidth to download. Mind spelling out why you linked that particular one, is there something I'm missing?

So-called 'C-with-classes' that so many C developers are prone to is absolutely the worst of both worlds and something no self-respecting C++ developer, nor the same for C developers would give two pennies for. Standard, straight modern C++ is superior in every way imaginable from the professional software engineer's perspective, and teaching newcomers ''circa mid 1980's'' software techniques is something only worthless college """professors""" who never slung a line of professional code in their lives would think of ~~abusing~~ doing tbh.

# 242
I still can't use Bump to reliably backup the forum. Even if a delete a whole subfolder from the folder with threads, and the catalog json+html it do recognize that something is missing. It doesn't remember failed downloads of pictures or files, so it won't try again.
Before that it looked good, it updated some thread and downloaded all the old pictures with it. I don't know why. This would at least helpd a little.

# 243
>>13034
Hey Anon, sorry you're having trouble with BUMP.
I'd suggest you try this command (note the 2 separate, extra '1' at the end):
[code]build/bump alogs.theГунтretort.com robowaifu 1 1[/code]

That should hopefully rebuild the special ''.archbot.config'' file for you, walk all the threads and all your local directories, and patch up anything missing. I added the two 'undocumented' flags to the program to deal with just such issues.

Let me know if you still have issues, I'm usually around the board every few days like today.

# 244
>>13064
>that Гунтed link
==AUUUUUUGH ROBI U BASTARD==
Got me again. :^)

# 245
>>8823
How do I install/run this?

# 246
>>13537
[code]
meson build
meson -C ninja
cp cxxchanConfig.example.json cxxchanConfig.json
cp config.example.json config.json
build/cxxchan
[/code]
then uncomment the 0.0.0.0:80 listener in the config.json file, and you should be able to access localhost/sys/login in your browser

*depending on your gcc version you might have to edit some const c-string declarations (const char* -> constexpr char*, constexpr char x[] -> constexpr char* x)

# 247
>>14626
ninja -C build*

# 248
>>8823
God, what the fuck is wrong with whoever wrote that library you used?

In libcaptcha.c:
[code]void makegif(unsigned char im[70*200], unsigned char gif[gifsize]) {
 	// tag ; widthxheight ; GCT:0:0:7 ; bgcolor + aspect // GCT
 	// Image Separator // left x top // widthxheight // Flags
	// LZW code size
	memcpy(gif,"GIF89a" "\xc8\0\x46\0" "\x83" "\0\0"
		"\x00\x00\x00"
		"\x10\x10\x10"
		"\x20\x20\x20"
		"\x30\x30\x30"
		"\x40\x40\x40"
		"\x50\x50\x50"
		"\x60\x60\x60"
		"\x70\x70\x70"
		"\x80\x80\x80"
		"\x90\x90\x90"
		"\xa0\xa0\xa0"
		"\xb0\xb0\xb0"
		"\xc0\xc0\xc0"
		"\xd0\xd0\xd0"
		"\xe0\xe0\xe0"
		"\xff\xff\xff"
		"," "\0\0\0\0" "\xc8\0\x46\0" "\0" "\x04",13+48+10+1);

	int x,y;
	unsigned char *i=im;
	unsigned char *p=gif+13+48+10+1;
	for(y=0;y<70;y++) {
		*p++=250; // Data length 5*50=250
		for(x=0;x<50;x++)
		{
			unsigned char a=i[0]>>4,b=i[1]>>4,c=i[2]>>4,d=i[3]>>4;

			p[0]=16|(a<<5);			// bbb10000
			p[1]=(a>>3)|64|(b<<7);	// b10000xb
			p[2]=b>>1;			// 0000xbbb
			p[3]=1|(c<<1);		// 00xbbbb1
			p[4]=4|(d<<3);		// xbbbb100
			i+=4;
			p+=5;
		}
	}

 	// Data length // End of LZW (b10001) // Terminator // GIF End
	memcpy(gif+gifsize-4,"\x01" "\x11" "\x00" ";",4);
}[/code]
He could've assigned that huge-ass string at the start to an array with a nice name like "header" and memcpy()ed the array, as well as taken its size with the sizeof operator instead of calculating it by hand. After making that mistake, he then goes and copypastes his complicated length calculation when initializing the variable *p, and makes the same mistake all over again at the bottom of the function.
It's literally the first function in that file I read and a first impression like this usually means the entire program is rotten. 

He also got his MAX macro wrong.
[code]#define MAX(x,y) ((x>y)?(x):(y))[/code]
Notice how (x>y) doesn't parenthesize x and y.

Just skimming further down I see memmove() used for no reason at the end of the filter() function (its source and destination don't overlap, the source is an auto array, the destination is one of the function's parameters).
I also see a load of repeated small read() calls that would've been better done with readv() and which have no error checking inside captcha().
Then there's also the buttload of globals which in all likelihood are global for no reason, of which Clang says lt4 and lt6 aren't used.

t. C programmer who wouldn't touch C++ even at gunpoint.

# 249
>>14738
Thanks for the constructive critique Anon, it's appreciated. Yes, memory-management is a very tricky issue, and one that few in life master. I strongly prefer to figure something like this out 'one time only', then encapsulate it all behind a simple-to-use interface I can stumble through successfully during a bleary eyed 3AM coding session.

>t. C programmer who wouldn't touch C++ even at gunpoint.
Kek. BTW, would you like to write robowaifu software with us here? I can tell you (well in advance) that we'll be needing many, many device drivers for our robowaifu's electronics & hardware systems. Literally hundreds of different drivers to adopt to our HALs. C programming will obviously play a very strong role in the devising of all these.

It's certainly a man-sized task, and your help would be welcome if you'd care to assist us with it. We certainly have a big, big collection of things to do on our plate, and this will be a vital one.

Cheers.

# 250
>>14738

>t. C programmer who wouldn't touch C++ even at gunpoint.

Nice bait. Though its true that the majority of his globals are unnecessary and should be creatable in an array function as needed to take advantage of C++’s dynamic memory allocation. 

Optimization is truly a dark art these days.

# 251
>>14743
The constants that make up those globals have to be somewhere in memory, using a C++ feature for them won't improve anything. If anything it might create an undesirable situation where some memory is allocated and then the values are unnecessarily copied into the memory when the values could be used directly from where they already are in memory at the start of the program.

They should be inside a function that calls the functions that need them, and then passed on as arguments. The compiler will place them in some region of memory and they won't be copied around if the compiler can prove they're never written to or if you explicitly give them static storage duration.

The issue with the globals is semantics. Computers do what we tell them to do. 
That C programmer told the compiler he needs a number in a specific place that can be read and written in any way possible by anyone and that he wants the latest state of the number every time he uses it, when what he actually wants is a number that is always known and always the same and that will only ever be recalled in the current source file, gifsize should've been an enum which is what provides these semantics. Heck, thanks to POSIX the compiler doesn't even know if those globals will be executed, because POSIX has functions for making a place in memory executable.
There is no such thing as self documenting code, but there is code about which there is less to know. One has to look at the entire program to tell if the global gifsize is modified and then find out why and when, even if it's const qualified, because const variables can be modified in C (and probably C++). If at least it had internal linkage, you'd know its only uses were in that ~240LoC file, and suddenly it's also easier to put faith in the "const" qualifier.
The semantics of globals prohibit compiler optimizations. Inside a linkable library or without LTO, the compiler is forced to assume that the broadest set of operations is performed on the globals, as all it knows is that code other than the code it can see has read/write/execute access to them, and because of that gifsize & its friends can't resolve into immediates in assembly and the operations performed on them can't be resolved at compile time or anything like that, they have to be a place in memory that the processor has to fetch with a pointer and every single operation on them has limited range of possible optimizations. This isn't so much of a premature optimization as it is a nice little side effect of just getting the semantics right, correct code is both easier to understand and faster.

# 252
>>14758
Naicu insights, Anon. Thanks!
>correct code is both easier to understand and faster.
Lol, you clearly saved the best bit for last. :^)

I would go further and add that the closer you fashion a solution in code to one that a domain expert themselves immediately recognize as good one, then the more likely it is to be efficient in both time and space after compilation.

I hope you help us all with the drivers Anon. We'll probably start with the Arduino Nano (which is amply documented already) and move out from there. Cheers.

# 253
>>14759
Sure. But I haven't done drivers. Never touched an Arduino either.

# 254
>>14765
Neat! That's good to hear Anon. Welcome aboard!
>But I haven't done drivers. 
It'll be easy. You just need to devise a standardized way to talk to the device's pins. As you might imagine, pin numbers can be all over the place, and may also require small amounts of preamble ceremony beforehand. We just need to turn that into easy to remember interfaces, standard across all the devices we'll use in our robowaifus. 

I'd suggest you have a look at Derek Molloy's videos for a starter Anon.
https://www.youtube.com/c/DerekMolloyatDCU/playlists

>Never touched an Arduino either.
You might want to pick up a handful then, they're quite inexpensive (for the power they bring). Here's but one of hundreds of possible sources, 3 for ~ US$ 20
www.amazon.com/REXQualis-Board-ATmega328P-Compatible-Arduino/dp/B07WK4VG58

>===
-''fix missing greenquote''

# 255
>>14738
kek, feel free to email the libcaptcha author (kefeer@brokestream.com). that library has some problems indeed, I noticed that various things were wrong when I used it for the ib, I even felt tempted to rewrite it entirely, or at least partly, or at the very least fix the compiler warnings, but got scared by the copyright notice (points 1 and 2 in particular). and didn't want to waste time writing my own.

I ended up doing things like avoiding the gifSize "constant" entirely and the declare my own ("constexpr int gifSize = 17646"; constexpr is a C++ specifier for expressions that are known at compile time). to avoid some of the semantic problems that you mention.

you're wrong about the internal linking tho. g++ uses internal linking by default for symbols marked as "const" (and static, obviously). I never #include the libcaptcha.c file, so the compiler would throw an error (even before linking) if I tried to use those symbols anyway.

the C++ part (my code) is even worse. from the hard-coded queries to the obscure orm (which needs it's own compiler to generate implementation files), blocking queries everywhere, and non-threadsafe globals in a multi-threading context. it nonetheless work. I might try to write something better in zig or C++ in the distant future

# 256
>>14826
>blocking queries everywhere, and non-threadsafe globals in a multi-threading context.
We'd certainly be interested in seeing solutions to these issues Anon. BTW, do you know of Apple's ''libdispatch'' ?

