# 1
Training AI and robowaifus requires immense amounts of data. It'd be useful to curate books and datasets to feed into our models or possibly build our own corpora to train on. The quality of data is really important. Garbage in is garbage out. The GPT2 pre-trained models for example are riddled with 'Advertisement' after paragraphs. Perhaps we can also discuss and share scripts for cleaning and preparing data here and anything else related to datasets.



To start here are some large datasets I've found useful for training chatbots:

>The Stanford Question Answering Dataset https://rajpurkar.github.io/SQuAD-explorer/

>Amazon QA http://jmcauley.ucsd.edu/data/amazon/qa/

>WikiText-103 https://blog.einstein.ai/the-wikitext-long-term-dependency-language-modeling-dataset/

>Arxiv Data from 24,000+ papers https://www.kaggle.com/neelshah18/arxivdataset

>NIPS papers https://www.kaggle.com/benhamner/nips-papers

>Frontiers in Neuroscience Journal Articles https://www.kaggle.com/markoarezina/frontiers-in-neuroscience-articles

>Ubuntu Dialogue Corpus https://www.kaggle.com/rtatman/ubuntu-dialogue-corpus

>4plebs.org data dump https://archive.org/details/4plebs-org-data-dump-2020-01

>The Movie Dialog Corpus https://www.kaggle.com/Cornell-University/movie-dialog-corpus

>Common Crawl https://commoncrawl.org/the-data/

# 2
>>2300
>digits
A propitious start. 

> Perhaps we can also discuss and share scripts for cleaning and preparing data here and anything else related to datasets.
I once wrote a crawler that walked through all the bibles published on Biblehub & Biblegateway, and then **~~stole~~** 'read' all their thousands and thousands of pages (ie, downloaded them all), then parsed every one of them out into JSON-like databases specific to each translation. Once completed this meant that I now had a way to directly correlate both the various translations to each other, but also with the original words in the extant manuscripts.

I say all this to simply point out that working with textual data is both important, and also complex for anything non-trivial. Many people just assume that dealing with text is both easy and simple, yet both assumptions are incorrect. There is a lot of work required to clean & normalize textual data for our robowaifus first, because as you said, GIGO.

High performance of the processing system seems pretty important to me, and so when I created the Biblebot software I wrote everything in standard C++ which could literally work through the entire processing load in just seconds once I had all the thousands of files downloaded locally. Slower methods such as Python would also suffice I imagine, but the basic need would remain: the data must be cleaned and normalized.

Further, I began to work on some graphical concepts to both display & refine the complex semantic and other interrelationships between words and phrases. This toolset hasn't materialized yet, but the ideas are basically valid I believe. The format for the interrelationships were based on Terry Halpin's Object Role Modeling, as specified in pic related.
>

I imagine that these experiences can at least be informative for this project, if not of some practical use. Good luck Anon.

# 3
>>2303
I just inadvertently discovered Dr. Halpin created a third book on the topic.
>
>Object-Role Modeling (ORM) is a fact-based approach to data modeling that expresses the information requirements of any business domain simply in terms of objects that play roles in relationships. All facts of interest are treated as instances of attribute-free structures known as fact types, where the relationship may be unary (e.g. Person smokes), binary (e.g. Person was born on Date), ternary (e.g. Customer bought Product on Date), or longer. Fact types facilitate natural expression, are easy to populate with examples for validation purposes, and have greater semantic stability than attribute-based structures such as those used in Entity Relationship Modeling (ER) or the Unified Modeling Language (UML).

>All relevant facts, constraints and derivation rules are expressed in controlled natural language sentences that are intelligible to users in the business domain being modeled. This allows ORM data models to be validated by business domain experts who are unfamiliar with ORM's graphical notation. For the data modeler, ORM's graphical notation covers a much wider range of constraints than can be expressed in industrial ER or UML class diagrams, and thus allows rich visualization of the underlying semantics.

>Suitable for both novices and experienced practitioners, this book covers the fundamentals of the ORM approach. Written in easy-to-understand language, it shows how to design an ORM model, illustrating each step with simple examples. Each chapter ends with a practical lab that discusses how to use the freeware NORMA tool to enter ORM models and use it to automatically generate verbalizations of the model and map it to a relational database.

# 4
>>2307
this book has a later companion workbook as well.
>

# 5
>>2303

I'm crawling and scraping the web at the moment for imageboard threads and arranging the replies into sequences to feed in for training. Fortunately it's only a few thousand threads for now and I can use BeautifulSoup in Python to process the pages, but filtering the posts and connecting them is something else. People link posts in crazy ways and reply to multiple posts at the same time, and there's empty posts, cross-thread and board links, spam, nonsense and copypasta. Separating the good data from the bad is really difficult. I'd like to be able to do sentiment analysis too and really focus in on what I'm looking to train on.



I'll have to check these books out and >>2251

When I make games I know how to structure everything but when it comes to processing text I have no idea what I'm doing and end up going full spaghetti and having no code to reuse afterwards.



What are some good libraries for parsing JSON and CSV in C/C++? Python isn't gonna cut it once I get to larger datasets. I know libxml2 for XML and just found MeTA Toolkit for text analysis but don't know if it's any good: https://meta-toolkit.org/

# 6
>>2309
>What are some good libraries for parsing JSON and CSV in C/C++?
I don't know about CSV, but I used jsoncpp when I wrote BUMP, such as it is. When I wrote the biblebot, I simply wrote the parsers by hand using just the C++ standard libraries such as string, iostream, vector, & map.

BeautifulSoup is amazing actually, and I'd advise you to at least ''try'' to use Python first before taking the plunge into Sepples. It's a beast.

# 7
>>2309
update: looks like the ACM book you linked from robowaifu u bread uses the meta-toolkit, so there's a nice convergence anon. might be worth looking into tbh.
>The Coursera course Text Retrieval and Search Engines uses MeTA in programming assignments available to thousands of students
>The Coursera course Text Mining and Analytics uses MeTA in its programming assignments as well
< An upcoming textbook Text Data Analysis and Management: A Practical Introduction to Text Mining and Information Retrieval showcases the MeTA toolkit with exercises and demos
>The UIUC course CS 410: Text Information Systems uses MeTA in some programming assignments
>The TIMAN Research Group from the UIUC Computer Science Department uses MeTA in their text mining research

# 8
Found this site full of anime subtitles:

https://kitsunekko.net/dirlist.php?dir=subtitles%2F

They're in ASS format and don't have speakers labeled but they'll save time transcribing dialog from anime. Soon we'll be the first in the world to talk with chatbots that imitate anime characters fairly well. What a time to be alive!



>>2310

I'm a big fan of Python but once shit starts getting coded in a big loop everything goes to shit fast even with libraries doing the heavy lifting. Processing these 2 million posts is gonna take awhile and it sure isn't gonna scale well to 200+ million. We're gonna need all the beasts we can tame if we're gonna ride our robowaifus to the stars.

# 9
>>2312
>We're gonna need all the beasts we can tame if we're gonna ride our robowaifus to the stars.
OK, fair enough. I was just trying to steer you onto a less painful course. But yes, I figured out a few years ago that if we want to actually create real, usable robowaifus then C++ was the only practical choice. I've been focused on it ever since.

BTW I'm building the prereqs for MeTA rn on my box, I'm gonna give it a go, since I already have Text processing textbook you mentioned.

# 10
>>2313
>prereqs
```cpp
Arch Linux Build Guide
Arch Linux consistently has the most up to date packages due to its rolling release setup, so it’s often the easiest platform to get set up on.

To install the dependencies, run the following commands.

sudo pacman -Sy
sudo pacman -S clang cmake git icu libc++ make jemalloc zlib
Once the dependencies are all installed, you should be ready to build. Run the following commands to get started:

# clone the project
git clone https://github.com/meta-toolkit/meta.git
cd meta/

# set up submodules
git submodule update --init --recursive

# set up a build directory
mkdir build
cd build
cp ../config.toml .

# configure and build the project
CXX=clang++ cmake ../ -DCMAKE_BUILD_TYPE=Release
make
You can now test the system by running the following command:

./unit-test --reporter=spec
If everything passes, congratulations! MeTA seems to be working on your system.```
https://meta-toolkit.org/setup-guide.html#arch-linux-build-guide

# 11
>>2313

Yeah, it's pretty much unavoidable once we get to microcontrollers.



>>2314

For some reason it wouldn't download this file (the server kept returning an empty response) but I found a mirror for it and dropped it into ./deps/icu-58.2/

https://ftp.osuosl.org/pub/blfs/conglomeration/icu/icu4c-58_2-src.tgz



Then it wouldn't build on Debian because it couldn't find xlocale.h but I found a fix:

# from the build directory

sed -i 's/xlocale/locale/' deps/icu-58.2/src/ExternalICU/source/i18n/digitlst.cpp

https://github.com/meta-toolkit/meta/issues/195



Then it wouldn't build with Debian's default g++-8 because it needs g++-7

rm CMakeCache.txt

CXX=g++-7 cmake ../ -DCMAKE_BUILD_TYPE=Release



Then everything built with all tests passed.

# 12
>>2317
>Yeah, it's pretty much unavoidable once we get to microcontrollers.
Actually, we'll probably need to wrap C-code in libraries for C++ use for much of that particular use case. I meant for the things C++ brings to the table. Namely great abstraction & generic programming while still being 99% the performance of hand-coded assembler. And it's ability to do this while still providing very good concurrency and parallelism is a mix that simply can't be beat. And trust me, we'll need every ounce of that power before we're finished rolling out the first prototypes.

>needing to downgrade the compiler
hmm. that's a surprise. good job figuring things out anon. btw i'd recommend you set up an Arch box (manjaro is a good choice for simplicity's sake) if you want to stay on the current edge of things.

# 13
>Datasets
>There are several public datasets that we’ve converted to the line_corpus format:

```cpp
20newsgroups, 
https://meta-toolkit.org/data/20newsgroups.tar.gz
originally from here.
http://qwone.com/~jason/20Newsgroups/


IMDB Large Movie Review Dataset,
https://meta-toolkit.org/data/imdb.tar.gz
originally from here.
http://ai.stanford.edu/~amaas/data/sentiment/


Any libsvm-formatted dataset can be used to create a forward_index.
http://www.csie.ntu.edu.tw/~cjlin/libsvmtools/datasets/```

>sauce:
https://meta-toolkit.org/overview-tutorial.html

# 14
word stemming tool used in meta-tools
https://snowballstem.org/
https://github.com/snowballstem

# 15
>>2320
located the 'official' sepples version, quite a bit simpler too tbh.
https://github.com/smassung/porter2_stemmer

# 16
here's meta-toolkit's discourse for support, etc.
https://forum.meta-toolkit.org/

# 17
>>2312
>Soon we'll be the first in the world to talk with chatbots that imitate anime characters fairly well.

# 18
```cpp
Alphabetical list of part-of-speech tags used in the Penn Treebank Project:
Number
Tag
Description
1.	CC	Coordinating conjunction
2.	CD	Cardinal number
3.	DT	Determiner
4.	EX	Existential there
5.	FW	Foreign word
6.	IN	Preposition or subordinating conjunction
7.	JJ	Adjective
8.	JJR	Adjective, comparative
9.	JJS	Adjective, superlative
10.	LS	List item marker
11.	MD	Modal
12.	NN	Noun, singular or mass
13.	NNS	Noun, plural
14.	NNP	Proper noun, singular
15.	NNPS	Proper noun, plural
16.	PDT	Predeterminer
17.	POS	Possessive ending
18.	PRP	Personal pronoun
19.	PRP$	Possessive pronoun
20.	RB	Adverb
21.	RBR	Adverb, comparative
22.	RBS	Adverb, superlative
23.	RP	Particle
24.	SYM	Symbol
25.	TO	to
26.	UH	Interjection
27.	VB	Verb, base form
28.	VBD	Verb, past tense
29.	VBG	Verb, gerund or present participle
30.	VBN	Verb, past participle
31.	VBP	Verb, non-3rd person singular present
32.	VBZ	Verb, 3rd person singular present
33.	WDT	Wh-determiner
34.	WP	Wh-pronoun
35.	WP$	Possessive wh-pronoun
36.	WRB	Wh-adverb```

>sauce
https://www.ling.upenn.edu/courses/Fall_2003/ling001/penn_treebank_pos.html

# 19
>>2327

# 20
>>2327
>>2328
Semantic treebanks

>Abstract Meaning Representation (AMR)  https://amr.isi.edu/
>DeepBank project	http://moin.delph-in.net/DeepBank
>Geoquery	https://www.cs.utexas.edu/users/ml/geo.html
>Groningen Meaning Bank	https://gmb.let.rug.nl/
>RoboCup Corpus	https://www.cs.utexas.edu/~ml/wasp/
>Universal Conceptual Cognitive Annotation (UCCA)	https://universalconceptualcognitiveannotation.github.io/
>FrameNet	https://framenet.icsi.berkeley.edu/fndrupal/
>PropBank	http://verbs.colorado.edu/~mpalmer/projects/ace.html

>sauce
https://en.wikipedia.org/wiki/Treebank

# 21
>>2317
-I also had an issue with this dependency, namely the version. On my Arch box, the current pacman-installed ICU is ~v65, but the meta-toolkit's cmake config insists on an exact (lower) version.

-For Arch the fix is easy, in the cloned meta-toolkit repo's dir
  meta/deps/meta-cmake/
open the file FindOrBuildICU.cmake in a simple text editor

replace line #34 with:
  if (BUILD_STATIC_ICU OR NOT ICU_VERSION OR NOT ICU_VERSION VERSION_GREATER_EQUAL "${FindOrBuildICU_VERSION}")
  
(ie, use 'VERSION_GREATER_EQUAL' instead of 'VERSION_EQUAL')

-That's it, just change that one statement. The cmake command does the right thing and everything builds and tests successfully afterwards.

-One other thing, I'd recommend using the 'develop' branch instead of the 'master' branch of the repo as it somewhat accomodates the C++17 standard. From the repo dir:

git fetch
git checkout develop
git submodule update --init --recursive

>---

BTW, I think this is the latest release version of the ICU code:
https://github.com/unicode-org/icu/releases/download/release-66-1/icu4c-66_1-src.tgz

# 22
Noice, I installed Calibre and found it can convert epub to txt easy:

''ebook-convert input.epub output.txt''

They only need a tiny bit of editing to clean up for training.



>>2333

And thanks, I'm looking at src/tools/profile.cpp at the moment trying to figure out how to use MeTA. To start I'd like to discard shitposts then remove stop words and analyze the word frequency to get an idea of the content of posts being collected. It seems like I have to create an index first to perform searches, although perhaps I can just use the word counts. Then I'd like to filter them by content, probably by exporting the data to do some semi-supervised learning on good and bad post examples until it can figure out the filtering automatically.

# 23
>>2338
I don't know much about the tool yet, but I think they cover some of the basics here
https://meta-toolkit.org/profile-tutorial.html

thanks for the tip about calibre, i didn't know that.

# 24
Idea: it might be possible to build a system that can scrape dialog from manga for use in training chatbots. It'd be an interesting project since it would also need to be able to predict some of the context and who is speaking. It makes me wonder what other massive data resources could be tapped into with adequate tools.

# 25
>>2450
Certainly there is a mountain of content in mango Anon, it would be great to figure it out.
>that scene
Kek. The Madhouse animu did a really good job with that one.

# 26
>>2450
subtitle files, visual novels, light/web novel translations.
Visual novels are particularly good because if you make a scrapper for a commonly used engine (like  renpy) you can access dialog from thousands of games. Also, associating lines with characters, context and even emotions should be easy to do by using the displayed artwork as a reference.

# 27
>>2464
>should be easy to do by using the displayed artwork as a reference.
can you define 'easy to do' anon? how would the process work. what algorithm would work, for example?

# 28
>>2465

It's ez, just invent the singularity :^)



LSTMs are good at this sort of stuff where it needs to detect cute anime girls and flick a switch that stays on for long periods of time, although I'm not really sure what someone would do with a visual novel reading bot besides endlessly generating choose your own adventures like AI Dungeon. That'd be pretty crazy with a good voice synth. If anon knows some tricks for easy image recognition, please share.

# 29
>>2300

pdftotext that comes with poppler-utils can be used to convert PDFs. For some reason ebook-convert doesn't work on my system for PDFs. pdftotext has some problems though spacing paragraphs and converting math symbols properly. Cleaning up a 500-page machine learning textbook is a bitch but I know it will be worth it. I'll post it here once it's complete.



It would be extremely useful if we could build a model that can construct questions for any given sentence. Then format everything it reads into a Q&A and train chatbots on that. Like this:

<Q: What would help us collect an insane amount of chatbot training data?

>A: It would be extremely useful if we could build a model that can construct questions for any given sentence.



It would get really good at answering technical questions on any topic trained on, plus be able to intuit technical things not found in any of the training data. It'd be like having a group of researchers in your pocket you can query any time and make Google look like ancient dinosaur technology.

# 30
>>2472
> I'll post it here once it's complete.
Please do Anon.
>It would be extremely useful if we could build a model that can construct questions for any given sentence. 
That's a great idea. It's something I wish I could do well tbh.
>and make Google look like ancient dinosaur technology.
This brings up the question of industrial espionage. Ofc (((interests))) will stop at nothing to succeed. If you could literally make Jewgle then you would be the focus of much attention.

# 31
>>2467
>It's ez, just invent the singularity :^)
You. I like the way you think Anon.

# 32
>>2465
oh, I wasn't thinking of using AI to recognize characters, but to parse the game data files directly. In renpy a dialog commands look like this:
```cpp

define e = Character("Eileen", image="eileen")

label start:
    show eileen mad
    e "I'm a little upset at you."
    e happy "But it's just a passing thing."
```

# 33
>>2478
Interesting syntax.

# 34
Found an archive of an old anime transcript website. This thing is a goldmine:

https://www.dropbox.com/s/lmqa9hnciu1fbav/animetranscripts_backup_jul_2018.7z?dl=0



Mining the transcripts into text format is gonna take a bit of work but it'll be an excellent dataset for people to bootstrap their chatbots on.

# 35
>>2585
Thanks Anon, grabbing a copy now.

# 36
Some chatbot datasets from the ParlAI team that created >>3190



>PersonaChat http://convai.io/ '''Paper''': https://arxiv.org/pdf/1801.07243

>DailyDialog '''Website''': https://web.archive.org/web/20190917200842/yanran.li/dailydialog (defunct site, dataset archived here: https://files.catbox.moe/kr936x.zip) '''Paper''': https://arxiv.org/abs/1710.03957

>Wizard of Wikipedia '''Paper''': https://openreview.net/forum?id=r1l73iRqKm

>Empathetic Dialogues '''Paper''': https://arxiv.org/abs/1811.00207

>SQuAD '''Website''': https://rajpurkar.github.io/SQuAD-explorer/

>MS MARCO '''Website''': http://www.msmarco.org/

>QuAC '''Website''': https://www.aclweb.org/anthology/D18-1241

>HotpotQA '''GitHub''': https://hotpotqa.github.io/

>QACNN & QADailyMail '''Paper''': https://arxiv.org/abs/1506.03340

>CBT '''Paper''': https://arxiv.org/abs/1511.02301

>BookTest '''Paper''': https://arxiv.org/abs/1610.00956

>bAbI Dialogue tasks '''Paper''': https://arxiv.org/abs/1605.07683

>Ubuntu Dialogue '''Paper''': https://arxiv.org/abs/1506.08909

>OpenSubtitles '''Website''': http://opus.lingfil.uu.se/OpenSubtitles.php

>Image Chat '''Paper''': https://arxiv.org/abs/1811.00945

>VQA '''Website''': http://visualqa.org/

>VisDial '''Paper''': https://arxiv.org/abs/1611.08669

>CLEVR '''Website''': http://cs.stanford.edu/people/jcjohns/clevr/



To download these datasets setup ParlAI:

https://github.com/facebookresearch/ParlAI#installing-parlai

Then do with the dataset's appropriate task name:

```cpp
python examples/display_data.py --task TASKNAME --datatype train```

See the complete list of datasets and their task names here: https://github.com/facebookresearch/ParlAI/blob/master/parlai/tasks/task_list.py

Example to download ConvAI2:

```cpp
python examples/display_data.py --task convai2 --datatype train```

# 37
>>3195
Thanks, Anon!

# 38
>>3195
>Example to download ConvAI2:
```cpp
python examples/display_data.py --task convai2 --datatype train
Illegal instruction (core dumped)```
==Why Does Python Hate Me!?== 
**:^)**

# 39
>>3200

How else do you expect software to run and package maintainers to maintain code when tech conferences clap roaringly when it's said calling connectors male and female is not inclusive because it implies that an outie is male and an innie is female?



The download files for a task can be found in its folder at ParlAI/parlai/tasks/''TASKNAME''/build.py

# 40
>>3202

(((redhat)))

# 41
>>3202
Haha, good point. But in fact **(of course)** the issue is all on my end. If Kokubunji says it works, you can believe it works. I just screwed the pooch in the Python Plane of AI dubs is all. :^)

I ''like'' that term '''Master''', think I'll use that someday...

>>3203
They're a real mixed-bag IMO. Some talented & good, some absolute evil & pure diversity.

# 42
>>2312
If someone ever needs to convert Japanese subtitles into romaji you can do so with Ichiran:
Web API: http://ichi.moe/
Source: https://github.com/tshatrov/ichiran

# 43
>>5533
possibly-related xpost
>>5532

# 44
Found someone who gathered 2B's voice files already: https://drive.google.com/open?id=1sm5lhG9fzxtu2GH10oXHsdOO9SeJQfyW
Spreadsheet of lines: https://drive.google.com/open?id=1x2Y-STrvg2Iq90zKL6zV1WMCkTcKoOI2

Also a dump of all of Nier's sound files: https://mega.nz/file/GVJCTbTR#BXCIUkkwu7INniWTH3brkklw7JrozkRGyvxC9LFLxZE
https://drive.google.com/open?id=0Bxz6TQ9R9H8ydXpraFZHajdnRWM

Preparing the data now for training. Will post the results in the speech synthesis thread when it's done.
>>199

# 45
>>5620
Excellent find Anon. I'm sure 2B will be a very popular waifu for anons.

# 46
>>3202

>Python joins movement to dump offensive master, slave terms.

If managing forked version wasn't such a mess then I would change master to moonman and slave to nigger, fuck you SJW eternal butthurt faggots.

# 47
Well surprise, surprise. Even ''Google'' thinks it might be a good idea to __reduce__ the power consumption required to do AI inferencing.
ai.googleblog.com/2018/04/introducing-cvpr-2018-on-device-visual.html
https://web.archive.org/web/20180520081050/https://ai.googleblog.com/2018/04/introducing-cvpr-2018-on-device-visual.html

>found via Product-Key paper linked by anon here:
>>6631

>pardon the intrusion OP. I realize this is probably off-topic somewhat, but I couldn't locate a better thread to put it. seemed at least vaguely related.

# 48
>>2585
Finished cleaning most of the anime transcripts data: https://anonfiles.com/D1V1U3p6p8/anime-transcripts.tar_xz (15 MB uncompressed)

The combine.py script will combine them all into one text file for finetuning GPT-2 or training your own model. Now our waifus can be filled with the spirit of anime.

# 49
>>6737

Thanks man, you did a good work.

# 50
>>6737
>'''502 Bad Gateway'''
I've tried probably 7 times across tor and vpns. Anonfiles hates me right now apparently. Any chance you could also post them up to catbox or another anon file server?

# 51
>>6739
Sure thing: https://files.catbox.moe/mgbmfj.xz
I've been having similar problems with Anonfiles. Usually it fixes itself after an hour.

# 52
>>6737
Damn, thanks a lot. Can you also give me instructions to fine-tune GPT2 or train my own model? I would prefer fine-tuning since I don't have a powerful machine right now.

# 53
>>6744
Excellent, thanks alot. Wow, that's a lot of anime dialog! :^)

# 54
>>6746
For now there is https://gitlab.com/kokubunji/TalkToGPT2#training but GPT2 requires at least 12 GB to train with a block size of 180.

I'm working on a modified GPT2 model that can train with only 6 GB of memory and hopefully outperform the original GPT2 model. I'm also updating TalkToWaifu to support other models besides GPT2, particularly people's own custom models.

# 55
>>6788
>I'm working on a modified GPT2 model that can train with only 6 GB of memory and hopefully outperform the original GPT2 model. I'm also updating TalkToWaifu to support other models besides GPT2, particularly people's own custom models.
Godspeed.

# 56
>>6788
It seems transformers changed their code so those training instructions are outdated.

# 57
Seems to me it might be possible you can uncover some hidden treasures here OP.
https://archiveteam.org/

# 58
>>7084
>quotes articles on missing data that no longer exist and archive.org is down
Kek'd. Is there a way to access their archives without the warrior app?

# 59
>>7099
Please find out and let us know Anon. Suggesting something far, far better would ofc be even more welcome aye? :^)

# 60
Open Source chatbots on github contain some data, which might also be useful for training other systems. Example: https://github.com/pandorabots/rosie/tree/master/lib/maps but maybe more importantly all the AIML files in such chatbots contain possible conversations: 
https://github.com/pandorabots/rosie/tree/master/lib
https://github.com/pandorabots/Free-AIML

# 61
Little heads-up: Some activists and NYT are going after libraries with faces bc China build a detector for Turks to look atter what they're doing. The issue is, threre are databases with images that contain pictures of human faces which are available to download. However, a lot of these images were harvested from sites like Flickr. As I already mentioned somewhere here on the board, the data which has been use can be extracted from neuronal networks. So now, people want their pictures removed, because "face detection is racist" or whatever.
My intention isn't debating this, but raise awareness that these free datasets might not be available at some point or being shrinked down. I think in another case they took one from the net  because "bigotted labels" and such stuff. So it's crucial to backup and share them in other ways (though not necessarily only between us here). 
Link (I realized, I don't know a good mirror site anymore): -www.nytimes.com/2021/01/31/technology/facial-recognition-photo-tool.html

>===
-rm hotlinking to NYT

# 62
>>8417
That reminds me of that quote, "whoever controls the data controls the future"

# 63
>>8417
It's a reasonable point, and certainly anyone that's already heavily invested in facial recognition has probably already amassed a large collection. 'Activists' generally are useless women and trannies, reduced to nothing more than harshly worded posts on twatter (at least as long as the Rule of Law held in the US, which obvs. is no longer the case). However it's plainly true that more and more data of __'''all'''__ types is being memory-holed everywhere at the behest of """TPTB""". So the basic point that's always been true still stands now:
==Save EVERYTHING==

But honestly, most people are quite vain and I think there will be little shortage of facial images fodder for AI systems to use. And additionally, I think we already have plenty available for general needs we might have here on /robowaifu/.

# 64
>>8425
Yes, the history (((revisionists))) are hard at work as usual. Thankfully, ~~**information**~~books today can't be so easily burned.

>"However it's plainly true that more and more data of all types is being memory-holed everywhere at the behest of """TPTB""". So the basic point that's always been true still stands now:
>"Save EVERYTHING

# 65
Here are two datasets from eleuther.ai, which tries to replicate GPT-3, therefore language oriented:
>The Pile is an 825 GiB diverse, open source language modelling dataset consisting of data from 22 high quality sources. It is useful for both training and benchmarking large language models.
>In our evaluations, models trained on the Pile show moderate improvements in traditional language modeling benchmarks, along with significant improvements on Pile BPB (our benchmarking measure).
https://pile.eleuther.ai/

>Why is the Pile a good training set?
>Recent work has shown that especially for large models, diversity in data sources improves general cross-domain knowledge of the model, as well as downstream generalization capability. In our evaluations, not only do models trained on the Pile show moderate improvements in traditional language modeling benchmarks, they also show significant improvements on Pile BPB.

>Why is the Pile a good benchmark?
>To score well on Pile BPB (bits per byte), a model must be able to understand many disparate domains including books, github repositories, webpages, chat logs, and medical, physics, math, computer science, and philosophy papers. Pile BPB is a measure of world knowledge and reasoning ability in these domains, making it a robust benchmark of general, cross-domain text modeling ability for large language models.

>OpenWebText2 is a dataset inspired by WebText, created by scraping URLs extracted from Reddit submissions up until April 2020 with a minimum score of 3 as a proxy for quality.
>It features content from multiple languages, document metadata, multiple dataset versions, and open source replication code.
>17,103,059 documents
>65.86 GB uncompressed text
>28 GB compressed including text and metadata
https://eleuther.ai/projects/open-web-text2/

# 66
seems interesting.
>
https://the-eye.eu/public/AI/

# 67
>>2303
>related xpost
>>8773

# 68
>Danbooru2020: A Large-Scale Crowdsourced and Tagged Anime Illustration Dataset
>Danbooru2020 is a large-scale anime image database with 4.2m+ images annotated with 130m+ tags; it can be useful for machine learning purposes such as image recognition and generation. https://www.gwern.net/Danbooru2020

# 69
Found a really useful tool, pdf2txt.py, for converting PDFs into text, particularly research papers: https://github.com/euske/pdfminer
It's used by this project to turn Arxiv into a dataset but I don't have 1 TB to mirror 1.5 million papers :^) https://github.com/mattbierbaum/arxiv-public-datasets
But it works a lot better than ebook-convert and performs best with the -V option to fix fragmented text. Just need a script to unwrap the text and clean it up.

Once I finish my script I'll create a dataset of the 800 or so papers I have saved. There's a lot of great curated information in there focused around solving robowaifu AI. Hopefully it will be useful for training AI research assistants and mentors. I've already gotten a ton of great ideas and learned some things I didn't know about just by discussing stuff with the standard GPT2-medium model and using some prompt engineering. Being able to finally train on Arxiv papers and get meaningful answers to specific questions will be amazing. I imagine tutorials will become a thing of the past once we can create AIs to answer questions around a given topic.

# 70
>>9240
>but I don't have 1 TB to mirror 1.5 million papers
I do. I'll look at it and see what I can do.

# 71
>>9240
So, give me some idea which of the 3 scripts you'd like to use Anon?
```cpp
The scripts in bin will then create any of the three subdirectories:

$ARXIV_DATA/tarpdfs   # raw pdf files from Amazon AWS bucket
$ARXIV_DATA/fulltext  # .txt from raw .pdf
$ARXIV_DATA/output    # co-citation network, parsed author strings, etc```
>

# 72
>>9240
I decided to go with fulltext and, unsurprisingly, Python broke on me. **WHY DOES PYTHON HATE ME SO LOL? :^)** 
Apparently you have to have some kind of account for authorization or something.

# 73
>>9246
The fulltext but it's not much use to me if I can't train my models on them. I'll probably get a couple new hard drives soon. Arxiv does provide a public API though for grabbing papers: https://arxiv.org/help/api/

I don't have the resources to train on all 1.5 million anyway. Training on a GB of text takes about a day on my machine. It would be more useful to have a web crawler that goes through all the citations of selected papers and downloads ones it can find and also any papers matching specific keywords. Arxiv citations are pretty easy to scrape from the fulltext papers.

# 74
>>6737
I've fixed some errors in the generated anime transcripts. There was a common issue with two characters speaking on the same line and some genius using lowercase Ls for Is. Having fixed that and included the missing files, there's 20% more data now and a validation and test set.

Text files for training: https://files.catbox.moe/b5d37o.xz
Raw data and scripts to rebuild transcripts: https://files.catbox.moe/mpx203.xz

Also transcribed an hour of Dorothy Haze's dialog from VA-11 Hall-A: https://files.catbox.moe/x0f3g5.xz

# 75
>>9408
Awesome. Thank you Anon, good work. Just think of what must be millions of man-hours of focused effort that have gone into our favorite Animus. Much of that effort was pre-production effort in the Story Depts. The script can be said to be a crystallization of all this human effort focused on creating scenarios & characters pleasing to males.

So in effect, what you've put into our hands represents the consolidation of millions of hours of devoted efforts of extraordinarily hard-working artists from Japan. All of which is now ready to go ''back to work'' creating ever.more.devoted. robowaifus for all of us.

I'd call that an important gift!

# 76
I prepared the Cornell Movie-Dialog Corpus into a text file for training with <|endoftext|> tokens between conversations: https://files.catbox.moe/pvi2ef.xz
Website: https://www.cs.cornell.edu/~cristian/Cornell_Movie-Dialogs_Corpus.html

If I messed something up or the file is taken down the Python script to regenerate it:
```cpp

import json
lines = open("movie_lines.txt", "rb").read().decode("utf-8", errors='ignore').strip().split("\n")
line_db = {}
for line in lines:
    line = line.split(" +++$+++ ")
    line_db[line[0]] = (line[3], line[4])
conversations = open("movie_conversations.txt", "rb").read().decode("utf-8", errors='ignore').strip().split("\n")
for line in conversations:
    conversation_lines = json.loads(line.split(" +++$+++ ")[3].replace("'", '"'))
    for line in conversation_lines:
        speaker, text = line_db[line]
        print(f"{speaker.title()}: {text}")
    print("<|endoftext|>")
```

# 77
>>9500
Thanks, got it. Especially appreciate you showing us how it's done, too!

# 78
Anyone here able to run GPT-2 on their GPU and wanna help build a dataset?

I've made a script for creating data to train a reward model by using GPT-2 to generate conversations between two random characters (bot-to-bot). Basically all you have to do is pick the best responses it generates until reaching the max token length and it starts generating another conversation. You can also write in your own responses if the generation is particularly bad or stuck.

# 79
>>9503
Looks like an interesting project. Might even turn out to be a rudimentary beginning to anon's ''Robowaifu@home'' idea (>>8958), in that we start sharing our own efforts onto a common dataset. Do you have any plans to redistribute the results openly for everyone's benefit back here Anon?

Also, this vaguely reminds me in a fashion of anon's 
>replacing rewards with examples
post (>>9438 and following). I wonder if you might be able to kind of integrate that sort of approach into your project?

# 80
>>9512
The dataset will be maintained on GitLab. I think that's the easiest way for both contributing data and getting updates, and people can fork it to make different versions if they wish.

The recursive classification algorithm is similar to temporal difference learning and needs time steps. I can see this algorithm being useful for completing tasks in a conversation but I don't think this dataset will be much help to it since there aren't any tasks being solved, unless the end result of conversations are reformulated into tasks somehow. Recursive classification still needs another paper or two to develop it into solving multiple tasks and ones it has never seen before in training for unsupervised learning.

There are other ways though to make this dataset useful beyond a human feedback reward model. MuZero's dynamics model that predicts the next state given an action and the current state could be modified into seeking a goal state rather than trying to win in a board game. Given enough processing power and hindsight experience replay (HER) to learn from mistakes it might be able to learn how to lead a conversation to a target state. The recursive classification algorithm's results aren't quite as impressive as HER which can learn multiple different tasks, and there has been a significant improvement to HER by combining it with expectation maximization: https://arxiv.org/abs/2006.07549

# 81
>>9517
OK, count me in if I can manage to run it with you. My best box has an i7 in it. It's for school, but I can probably set up a dual-boot for it. Is Ubuntu good enough, distro-wise (Python versions, etc., etc., etc.) ? I would appreciate detailed, tutorial-style setup, operation, and results pushes, etc., if you would please.

I would recommend you consider sort of approaching this effort the way the ''Foldit'' guys did (>>9028). Namely, fashion it sort of like a game that anons can 'play' . The fundamental premise seems to lend itself to this paradigm, and we're more likely to see ongoing participation by only vaguely interested anons that way IMO.

This also sounds like it's a project that likely should have it's own thread to me. That way the long chain of (entirely unrelated) dialogue about development doesn't detract from this dataset thread which seems more like it should be a 'library archive' type thread to me.

# 82
>>9520
>and we're more likely to see ongoing participation by only vaguely interested anons that way IMO.
Also, on this same general tack, what about the idea of setting up a server online and letting many, many anons 'play' along with the waifu this way. After all in this scenario, it's not the raw horsepower and number-crunching that is the valuable thing. Rather obtaining the human-reasoning needed to assess and score the reasonableness of any particular output is the valuable bit. There's a lot more that could be said, but we should probably hold off on it until you make a decision about a new project thread or not.

# 83
>>9520
I don't recommend running GPT-2 on a CPU because it's so slow. As the conversation gets longer it will take over half a minute to generate responses even with just the small model and a fast CPU. If there was already a crude T5 chat model it'd be a different story, but until then an Nvidia GPU with at least 3 GB and CUDA 7.0 is needed or Google Colab.

The code should be able to run on Linux, Windows or Mac just fine. I recommend using Python 3.8 or 3.7 with Pytorch 1.8.x and CUDA 11.1. CUDA installation will depend on your platform. I'm not familiar with other distros but on Debian Linux buster-backports provides CUDA 11.1. Older cards from 2018 or earlier should be fine with just CUDA 10.2 which PyTorch also supports.

Make sure when installing Python on Windows to check 'Add Python 3.x to PATH', otherwise Python won't run from the terminal.
Then get PyTorch: https://pytorch.org/get-started/locally/ (It's easiest to install with pip)

Once Python and PyTorch are installed, install the transformers library from a terminal with:

```cpp
python -m pip install --user transformers```
This should be all you need.

>>9523
If I had the money for a server I'd rent a GPU instance, train it on extra data and have it done in a few hours. The motivation of this dataset is to train the model with as little compute as possible. I just need a little help for now to push it into a usable state so it can be used instead of GPT-2. T5 takes less than half a second on the CPU to generate a response. That'd make it much more approachable for anons to participate without expensive hardware. The validation perplexity is at 25 now so there's hope.

Another idea I have is to train the reward model with sentences taken from other samples in the dataset but that don't match the conversation, or by discriminating its own generated responses as a GAN. I think the former would help it learn more sensible replies. A GAN might be too unstable to train.

I'll make a thread for it later so these posts can be moved there.

# 84
>>9526
Alright. I'll try to set up a dual-boot before the upcoming weekend is out. Debian, is it Anon?

>The validation perplexity is at 25 now so there's hope.
Good news. Please keep us up to date Anon. It would be absolutely marvelous to be able to run a reasonably responsive and competent chatbot on embedded hardware today.

And I would say there's no need to make a new thread unless you yourself deem it reasonable.

# 85
>>9569
Yeah, personally I prefer it because they supported my ancient Pentium 4 for nearly two decades but it tends to lag behind in updates because of this support for older systems. It took over a year to even use the full capabilities of my GPU I bought 2 years ago. Mint and Ubuntu are the easiest to install and use and tend to have more recent updates if you don't need that long-term stability.

The chat model has been slowly inching forward but slowed to a crawl. I've been playing around with different hyperparameters but no luck. I think it has bottomed out unless I start doing 2-hour optimizer steps with a ridiculous amount of gradient accumulation steps. The validation set perplexity is at 20 now which isn't bad but not quite good enough either. Once I start throwing other training tasks at it though there should be further gains and we might be able to skip GPT-2 completely.

Ideally about 10 GB of data is needed for training but I only have 40 MB of high-quality chat data so the only option right now is to train on other data. I've written a Wikipedia and Stack Exchange scraper to soak up a ton of data, just need to process it into tasks and train.

It all hinges on the reward model working well really. Without a working reward model, creating this dataset won't make a big difference without a team of novelists to crank out a 100 books worth of data.

# 86
>>9575
>but I only have 40 MB of high-quality chat data
What data do you need? Could you use extracted dialogs from subtitles?

# 87
>>9595
>Could you use extracted dialogs from subtitles?
I think he's already doing that Anon:
>>9408

# 88
>>9600
Ah, I see, but limited to the source of a single waifu. Finding ways how she would say something and then change other dialogs automatically with a script might help to create more data.

# 89
>>9595
Any data that can be formulated into a query and response can be used. At the moment I'm using subtitles from anime and movies with character names but I could potentially use ones without names and just predict the next sentence or line. Some of what it learns on other data and tasks will transfer to learning chat dialog.

I could train it on a variety of other tasks like reversing the order of words in a sentence, labeling parts of speech, translation, determining whether recipes are highly rated or not, or go Jeopardy mode and predict the query from a response. The only limit of what you can teach a text-to-text transformer is what you can fit into text, your processing power, and the amount of data you have.

The question is what would be the best data to train on? I have a very tiny amount of compute and can't test a hundred different things. It's not obvious what skills are necessary to comprehend a sentence either and what tasks will improve those skills. Basketball training drills for instance don't look anything like basketball but they significantly improve someone's performance.

# 90
>>9603
Well, one thing I have is a metric boatload of raw JSONs of shitposting for roughly a year and a half or so. Probably 60+ boards if I dug around. Now this is, again, ''shitposting'', so YMMV. But many of these are deterministically post/response.

I could imagine automatically going through it all, finding the many thousands of post/reply pairs and then maybe getting a human involved in check that it is in fact a query/response pair?

I've never yet tried to go through and pull all the JSON out from all these archives in their entirety yet, but I do it for /robowaifu/ here generally a few times a week. So, shouldn't be too difficult to pull those and push the archive file to catbox.

# 91
v>>9605
BTW, I've already gotten a  fairly well wrung-out mechanism for parsing the raw JSON into individual posts written (''BUMP'', ''Waifusearch''), so it might be wisdom if you can clearly specify how you'd like the data parsed out, and I could do a lot of preprocessing data-massaging in advance for you, instead of just giving you a big dump of un-processed raw JSON files.

# 92
>>9607
Also BTW, if you haven't ever done so yet, you can examine exactly what the JSON I'm speaking of looks like for yourself Anon. For example:
http://bhlnasxdkbaoxf4gtpbhavref7l2j3bwooes77hqcacxztkindztzrad.onion/robowaifu/res/2300.json
https://alogs.theГунтretort.com/robowaifu/res/2300.json

(Just replace the domain w/ the proper AlogSpace URI if you don't use Tor)

# 93
>>9603

That post reminded me that there's a fan-run website about the gameshow Jeopardy. Their archive got over 400000 clue-question pairs: https://j-archive.com/



I think the more funny and intelligent the quiz show is, the less useful it is for building basic understanding. The gold standard of entertaining quiz games is You Don't Know Jack IMHO. That stuff is too witty and punny to easily build anything faintly resembling common sense from that. The questions from YDKJ are too fragile, by that I mean slightly changing the wording is likely to completely screw with their meaning. Jeopardy isn't quite like that. Still, something more dull and easy than Jeopardy would be better. Maybe some ROMs from quiz games ''aimed at children'' have good boring common-sense stuff in plain text.

# 94
>>9671
Yeah, it just becomes a database lookup at that point. But I speculate it can learn some useful information on reversing common queries and responses. Like "I'm fine" is usually a response to "How are you?" We take this prior knowledge for granted but unless a model learns this it will fail to make any connection. An interesting future research project might be having the model generate its own tasks to learn and explore looking at data in new ways unsupervised.

'''Update to''' >>9503
The past few days I've tried a dozen different experiments to use the hidden state of the T5 encoder to discern whether a response matched a query in comparison to a response taken from another random query. Nothing was able to learn anything, which is kinda depressing because that might mean it might not do well later with a recurrent network modulating the hidden states. I'm not really sure why this is but I suspect because the T5 was pretrained for 100 GPU years or whatever amount of time on text-to-text and trying to train it to be used a completely different way with a pitiful GPU in a few hours is not happening.

So I started feeding those queries and responses into the T5 model asking if the response makes sense to the query, and to output labels yes or no. Surprisingly it had no struggle learning this way and the responses are becoming much more sensible, even though it's only capable of discerning the right answer 70% of the time so far. In the state it's in it might even be usable in place of GPT-2 for generating a chat dataset, although the quality still has a long way to go. The first image shown is a conversation generated by picking from 3 responses by T5-chat as Dorothy and entering my own input for Jill, and the second image T5-chat as Haruhi.

With this working now the chat dataset project can be used to train T5-chat so I'll be making a thread for it once everything is ready to go.

# 95
>>9671
>Maybe some ROMs from quiz games aimed at children have good boring common-sense stuff in plain text.
Yeah, we're dealing with some odd juxtapositions in our endeavors here, and this is a fundamental one tbh. IMO, the only reasonable hope we have ATM of AI communications that will stand up for hours of engagement are ones that are necessarily 'dumbed down' to a child's level. (BTW, even that is already vastly beyond any of the animals, so a rather notable achievement). However, we also plainly want to be able to engage with our waifus as well, ''adults''.

A bit of a conundrum for now I'd say.

>sage for off-topic

# 96
>>9678
>chats
lol.

Well sounds like you made a nice breakthrough by using a wonderfully simplistic 'trick'. That's encouraging. No doubt eventually we'll all be able to tick off 100GPU-years of compute on our 'smart' watches in a few years, but for now this is by far our best kind of approach very likely. That is, ''finding clever approaches that get right to the heart of the problem''.

# 97
I just mentioned Chatterbot somewhere else, here's the corpus. URL might not work, since the dumb jokes of the forum software: https://github.com/Гунтhercox/chatterbot-corpus - this link here https://chatterbot.readthedocs.io/en/stable/corpus.html might be better anyways, since it comes with some explanations.

# 98
>>9753
>conversations:
>have you read the communist
>yes, marx had made some interesting observations.
>stock market
>you can never really predict the stock market.
>stock market
>my lawyer said i shouldn't give stock tips online.
>stock market
>mutual funds might be better unless you are wealthy.
>stock market
>i'm not sure an individual alone can really beat the market.
>56 KB
Top-tier conversation quality

# 99
>>9765
I gave an answer on how to handle this. But, I put it in the thread about chatbots here >>9780

# 100
Not sure if this is the right thread OP, just let me know and I can delete it if not. On this video (>>10463), the author promotes ''Weights and Biases'' papers page. It now redirects to a community page that seems like it might be interesting to the ML practitioners here on /robowaifu/.

# 101
Some archives of 4chan posts from 2008-2015

SQL Database: https://archive.org/download/archive-moe-database-201506

Files: https://archive.org/details/@archivemoe



Penfifteen Archive from 2004-2008: https://archive.org/details/studionyami-com_penfifteen-2012-03-05

And moar post archives: https://wiki.archiveteam.org/index.php/4chan



I'm working on some dataset generating scripts for finetuning language models, including image-post pairs for multimodal training >>11731



It'll take a few months to download and process all the data. My plan is to compress the images to 384x384 webp files so each dataset isn't 200+ GB per board (/v/ is over 2 TB). SqueezeNet's input size is 227, AlexNet is 256 and VGG is 224, so I think that is sufficient and leaves room for data augmentation. If someone has the hardware to train StyleGAN2 at 512 or 1024, I'm sure they can download the archives and regenerate the dataset with the scripts. I'll release the image datasets and each board separately so people can pick what they want.



Also if anyone wants to help I'll post the scripts when they're ready.

# 102
>>11778
Bandwidth is a real issue for me currently. I'll try to help out later.
>4chan posts from 2008-2015
Nice. Pretty classic era tbh.

# 103
>>11778
>My plan is to compress the images to 384x384 webp files so each dataset isn't 200+ GB per board (/v/ is over 2 TB).
Good thinking. How are you planning to situate each selection frame for each image Anon? Seems quite impractical to do by hand, yet there's a need for accurate placement/pre-scaling to capture the vital essence of each image, humanly-speaking.

# 104
>>11782

It took me three days just to download the database, 57.5 GB compressed.



>>11889

I will be resizing the largest dimension down to 384 or smallest dimension up to 256. That way models can select any 256x256 crop of that, perhaps using a spatial transformer network to position the crop. However, GIFs and Webms will pose a significant challenge. I will skip those for now.

# 105
Wake the fuck up robofucker, we got an imageboard to burn: https://files.catbox.moe/6pslbq.xz



These are /robowaifu/ posts up to July 2021 containing a post chain for each post. The script to regenerate it from the json files is included. The chains have been shuffled to avoid repetitions that would throw transformers into seizures. Now there's no excuse not to have a shitposting waifu while wasting time talking about making a robowaifu. Pray to God she motivates you into actually working.

# 106
>>12044
>It took me three days just to download the database, 57.5 GB compressed.
Lel. Please go easy on us assistants, and try to figure out how to slice that up into MUCH smaller parts so we can help you out here, Anon. Think ''push the compute load out to the edges of the network, not saturate the wireline''! :^)

This is an exciting project idea, I sure hope you can pull it off. It should revolutionize the whole 'fun with waifus' paradigm!

# 107
>>12051
LOL. That was fast Anon, thanks!

# 108
>>12052

I can handle the database processing. The issue is the images. They're split up into 10 GB tar files which can be extracted with:

```cpp
cpio -D output_path -ivd -H tar < images.tar.ab```

However, some of the files will be lost doing it this way, since they're one tar file split into multiple.

# 109
==Raiders of the Lost Kek==

3.5 years of /pol/ posts, June 2016 - November 2019 (in JSON format)

Paper: https://deepai.org/publication/raiders-of-the-lost-kek-3-5-years-of-augmented-4chan-posts-from-the-politically-incorrect-board



Download: https://zenodo.org/record/3606810

```cpp
sudo apt-get install zstd

unzstd pol_0616-1119_labeled.tar.zst

tar -xvf pol_0616-1119_labeled.tar```

# 110
>>12194
LOL. I'm shocked they published this publicly. Seems likely it's not earning them any brownie points that way? Regardless, better get it while you still can Anon.
==Save.Everything.==

# 111
>>12194
Interesting project Anon. Vaguely curious about how much did they

'''Raiders of the Lost Kek:'''
''3.5 Years of Augmented 4chan Posts from the Politically Incorrect Board''
>abstract
>''This paper presents a dataset with over 3.3M threads and 134.5M posts from the Politically Incorrect board (/pol/) of the imageboard forum 4chan, posted over a period of almost 3.5 years (June 2016-November 2019). To the best of our knowledge, this represents the largest publicly available 4chan dataset, providing the community with an archive of posts that have been permanently deleted from 4chan and are otherwise inaccessible. We augment the data with a set of additional labels, including toxicity scores and the named entities mentioned in each post. We also present a statistical analysis of the dataset, providing an overview of what researchers interested in using it can expect, as well as a simple content analysis, shedding light on the most prominent discussion topics, the most popular entities mentioned, and the toxicity level of each post. Overall, we are confident that our work will motivate and assist researchers in studying and understanding 4chan, as well as its role on the greater Web. For instance, we hope this dataset may be used for cross-platform studies of social media, as well as being useful for other types of research like natural language processing. Finally, our dataset can assist qualitative work focusing on in-depth case studies of specific narratives, events, or social theories.''

# 112
For speech recognition, Mozilla has the voice "Common Voice" corpus with multiple languages, if anyone is interested.  English alone is over 2,000 hours of spoken phrases, about 65gb.  The other languages I looked at were around 20gb each, but it varies.  You can also add to the project yourself by recording or verifying phrases.

https://commonvoice.mozilla.org/en

# 113
>>14321
Thanks, that might be useful. I wonder if we can also use subtitle files with their related shows and movies.

# 114
>>14325
waifusearch clipchan

# 115
>>14326
Lol, how could I forget. Blackout, because of insufficient sleep.

# 116
>Wikipedia-based Image Text (WIT) Dataset is a large multimodal multilingual dataset. WIT is composed of a curated set of 37.6 million entity rich image-text examples with 11.5 million unique images across 108 Wikipedia languages. Its size enables WIT to be used as a pretraining dataset for multimodal machine learning models.

This is going to be an extremely important dataset towards blessing language models with sight. After training on this dataset it should be possible to train with human feedback to produce more detailed descriptions for improving the model's visio-linguistic understanding. Other modalities could be explored from there like problem solving from images, critiquing artwork, playing games, watching videos, webcam interaction, automated web search, and a lot more. It'll open up a lot of possibilities.



Website: https://github.com/google-research-datasets/wit

Download: https://github.com/google-research-datasets/wit/blob/main/DATA.md

# 117
>>15365
>This is going to be an extremely important dataset towards blessing language models with sight. 
Sounds like a real breakthrough may be around the corner Anon. Please keep us all up to date on things with this.

# 118
Some incredibly based independent researchers put together an image-text-pair dataset to open-source OpenAI's work so people can replicate DALL-E and do other multi-modal research.



Dataset: https://laion.ai/laion-400-open-dataset/

Direct download: https://www.kaggle.com/datasets/romainbeaumont/laion400m (50 GB total, or can be downloaded in 1.8 GB parts according to necessity or hardware limits)

Paper: https://arxiv.org/pdf/2111.02114.pdf

Tool to search the dataset by text or image: https://rom1504.github.io/clip-retrieval/



To use the dataset you need something that can read parquet files. I recommend fastparquet which uses a minimal amount of memory.

```cpp
# python -m pip install fastparquet

from fastparquet import ParquetFile

DATA_PATH = "part-00000-5b54c5d5-bbcf-484d-a2ce-0d6f73df1a36-c000.snappy.parquet"

pf = ParquetFile(DATA_PATH)

row_group_iter = iter(pf.iter_row_groups()) # each row group has about 1M rows

row_group = next(row_group_iter)

row_iter = row_group.iterrows()

i, row = next(row_iter)

row[1], row[2] # ( image_url, text )

row.keys() # ( 'SAMPLE_ID', 'URL', 'TEXT', 'HEIGHT', 'WIDTH', 'LICENSE', 'NSFW', 'similarity' )```

Or you can use img2dataset which will download the images locally and resize them: https://github.com/rom1504/img2dataset



The quality of the dataset isn't exactly as spectacular as >>15365 but probably as good as you can get from a raw scrape of the internet and it has a much larger breadth of content.

There's also LAION-5B but it's so massive it's beyond our capabilities to really use right now: https://laion.ai/laion-5b-a-new-era-of-open-large-scale-multi-modal-datasets/

# 119
>>15834

>chobits hentai pictures wallpaper chobits

# 120
>>15834
>Some incredibly based independent researchers put together an image-text-pair dataset to open-source OpenAI's work so people can replicate DALL-E and do other multi-modal research.
That is very exciting Anon. Thanks for the heads-up!

# 121
>>15834
>Or you can use img2dataset which will download the images locally and resize them: https://github.com/rom1504/img2dataset

I just wonder if we can somehow capitalize on something at least vaguely similar to the approach that Nvidia is using for it's proprietary DLSS ?
https://en.wikipedia.org/wiki/Deep_learning_super_sampling

Basically, have an image analysis pipeline that does the vast bulk of it's work at lower resolution for higher 'frame' rates, and then does a DL, ''Waifu2x''-style upscaling near the latter end of the pipe?

# 122
>>15851

For image generation certainly, but for image analysis not so much. However, a lot of work has gone into finding optimal models with neural architecture search. And EfficientNetv2 for example starts training at a lower resolution with weak data augmentation then gradually increases the resolution and difficulty to minimize the amount of compute needed to train it. That last bit of high resolution training is unavoidable though if you want to extract useful information from it.

https://arxiv.org/pdf/2104.00298.pdf



>>15835

Kek, I think they said 1% of the dataset is NSFW and it's only labelled so by image content.



I have an idea though to create a reward model for good image labels and then use it to filter out the poorly captioned images. Finetuning on cleaner data should fix a lot of the weirdness CompVis/latent-diffusion generates and improve CLIP.



Another possibility might be using the reward model to generate superhuman quality captions for images. In the human feedback paper the 1B parameter model generated summaries were preferred 60% of the time compared to the actual human summarizes and 70% with the 6B model.

https://openai.com/blog/learning-to-summarize-with-human-feedback/



To go even further beyond, it might be possible to generate these superhuman captions, score them, finetune the reward model on the new ones, and train the caption generator to make even better captions in an iterative loop to create extremely high quality datasets that would require 10 million man-hours to make by hand.

