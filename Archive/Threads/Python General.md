# 1
'''Python Resources general'''

Python is by far the most common scripting language for AI/Machine Learning/Deep Learning frameworks and libraries. Post info on using it effectively.

wiki.python.org/moin/BeginnersGuide
https://archive.is/v9PyD

On my Debian-based distro, here's how I set up Python, PIP, TensorFlow, and the Scikit-Learn stack for use with AI development:
[code]sudo apt-get install python python-pip python-dev
python -m pip install --upgrade pip
pip install --user tensorflow numpy scipy scikit-learn matplotlib ipython jupyter pandas sympy nose[/code]

LiClipse is a good Python IDE choice, and there are a number of others.
www.liclipse.com/download.html
https://archive.is/glcCm

# 2
Learn Python the Hard Way

learnpythonthehardway.org/book/
https://archive.is/Ah7jU

# 3
>Best online resource to learn Python? [closed] (StackOverflow)
stackoverflow.com/questions/70577/best-online-resource-to-learn-python
https://archive.is/rxB7U

Python Resources (UC Berkeley)
https://archive.is/qcd2R

docs.python-guide.org/en/latest/intro/learning/
https://archive.is/D3yge

# 4
Does the Python Anon have a recommendation for a good IDE for the language? The OP here has LiClipse, what is your recommendation? Linux ofc.

# 5
>>2428
Recently I've started using Spyder since it can show function argument tooltips for imported scripts without problems and has an interactive console with command history. It's also open-source.
>Spyder is a powerful scientific environment written in Python, for Python, and designed by and for scientists, engineers and data analysts. It offers a unique combination of the advanced editing, analysis, debugging, and profiling functionality of a comprehensive development tool with the data exploration, interactive execution, deep inspection, and beautiful visualization capabilities of a scientific package.
https://www.spyder-ide.org/

[code]sudo apt-get install spyder3[/code]

# 6
>>2429
Thanks Anon, got it. Looks good so far! :^)

BTW, I had to use Anaconda to install it, glad I did now.
[code]sudo conda install -c anaconda spyder[/code]

# 7
>>2435

# 8
I've been trying to find Tensorflow wheels with no AVX. I found one for Tensorflow 1.14.0 in Python 3.7 here: https://github.com/yaroslavvb/tensorflow-community-wheels/issues/135
But there still appears to be some AVX instructions in pywrap, tf2xla and libtensorflow_framework, similar to the problem I had with my build, which I found using this script: https://gitlab.com/kokubunji/cookbook/-/raw/master/check_avx.sh[code]find -L . -iname "*.so*" -exec check_avx.sh {} \; > avx.log[/code]
However, someone on the page said it worked for them. If anyone feels like testing it I'm leaving some instructions here on how to install it, including my attempt to build Tensorflow 2.3.1 for Python 3.8 with SSE4 and no AVX: https://anonfiles.com/ncG12cg2pb/tensorflow-2.3.1-cp38-cp38-linux_x86_64_whl

If your system's Python version is 3.8, you will have to build Python 3.7 from source to use the 1.14.0 wheel (or if your system is Python 3.7 and you want to use Tensorflow 2.3.1 by building Python 3.8). On Debian Buster to build Python you will need: ''zlib1g-dev libffi-dev libssl-dev libbz2-dev libncursesw5-dev libgdbm-dev liblzma-dev libsqlite3-dev tk-dev uuid-dev libreadline-dev''

To build Python 3.7.9 from source:[code]wget https://www.python.org/ftp/python/3.7.9/Python-3.7.9.tar.xz
tar -xvf Python-3.7.9.tar.xz
cd Python-3.7.9
./configure --enable-optimizations
make -j4[/code]Next install pip into it:[code]wget https://bootstrap.pypa.io/get-pip.py
./python get-pip.py[/code]
To install Tensorflow into this Python with pip:
[code]# use the path to wherever you downloaded the Tensorflow wheel
./python -m pip install -U -t Lib ../tensorflow-1.14.0-cp37-cp37m-linux_x86_64.whl[/code]Or from URL:[code]./python -m pip install -U -t Lib https://furas.pl/projects/tensorflow-no-avx/bin/tensorflow-1.14.0-cp37-cp37m-linux_x86_64.whl[/code]
Python source downloads: https://www.python.org/downloads/source/
Tensorflow community wheels: https://github.com/yaroslavvb/tensorflow-community-wheels/issues

# 9
>>5747
Wow thanks for all the nice instructions and what must have been a metric ton of hard work to work through all this Anon. It gives me more confidence about Python tbh.

# 10
>>5748
It was more time consuming than anything. I also put up some instructions on how to build Tensorflow from source here: https://gitlab.com/kokubunji/cookbook/-/wikis/machine-learning/building-tensorflow-from-source

When I have some time I'll do PyTorch next. According to the Steam Hardware Survey only 78% of Steam users have CPUs that support AVX2 and 98% support SSE4. If we'll be creating virtual waifus in Godot, we'll need to deploy them with working AVX-free wheels.

# 11
>>5749
> only 78% of Steam users have CPUs that support AVX2 
I admire what you're doing. But tbh, for a moment I was wondering how many people would have a CPU without any AVX. You or someone else wrote Tensorflow needs any AVX, not AV2... The oldest processors with AVX came out 2011: https://en.m.wikipedia.org/wiki/Advanced_Vector_Extensions 
However, I think I get it, if there are some million CPUs which still could be used, at least for interference, it would be a waste to exclude them. Also, if future versions would require a newer version of AVX, then one could still drop back to the one without that requirement. 
Are there similar restrictions on old graphic cards?

# 12
>>5758
>I was wondering how many people would have a CPU without any AVX.
I'm certainly one of them, and I've been here on /robowaifu/ since it's very beginning (and even earlier haha)

# 13
>>5758
Tensorflow and PyTorch are built with SSE4.1 SSE4.2 AVX AVX2 FMA. You can find which instructions people have under Other Settings: https://store.steampowered.com/hwsurvey/Steam-Hardware-Software-Survey-Welcome-to-Steam AVX is 93.67%.

The official binaries of PyTorch 1.6.0 and Tensorflow 2.3.0 dropped support for my GPU (which only came out in January 2019). I'm probably gonna have a Frankenstein build of Linux in a few years just to keep my GPU working with the latest versions. In the meantime to get them to work I have to build the CUDA toolkit from source and then PyTorch and Tensorflow. For older hardware it'll be easier to just use older versions. There isn't a whole lot in the new version of PyTorch that's worth switching over anyway. The only problem is trying to maintain your system with all these out of date packages. Someone here almost wrecked his system just trying to downgrade from Python 3.8 to 3.7.

The way I envision going forward is people training PyTorch or Tensorflow models on the latest hardware and deploying the weights to be used or fine-tuned by mlpack models (or possibly other machine learning libraries) that can run on older hardware and embedded systems. In the future we'll likely have distributed computing groups working on training AI models, contributing our unused resources, including integrated GPUs running OpenCL, to improve AI for robowaifus.

# 14
>>5765
>The way I envision going forward is people training PyTorch or Tensorflow models on the latest hardware and deploying the weights to be used or fine-tuned by mlpack models (or possibly other machine learning libraries) that can run on older hardware and embedded systems. In the future we'll likely have distributed computing groups working on training AI models, contributing our unused resources, including integrated GPUs running OpenCL, to improve AI for robowaifus.
>/thread. 
This is a good vision for the future IMO. One that should deal with the practical realities of advanced AI in the future, while still carrying along everyone using inexpensive embedded robowaifu systems including new ones of the future. I also envision new frameworks & libraries beyond just those of PyTorch and Tensorflow . This distributed model should support those as well.

'''Robowaifu@Home''' when?

# 15
>>5767
Once robowaifus capture the public's attention, maybe can start a foundation that crowdfunds & maintains a good accelerator serverfarm, serving as the core linchpin for a robowaifu@home system?

# 16
I'll put the code for going through this textfile here >>7907 into this thread, since I'm using Python3 for my work. It can be seen as some example here. I'm using Ipython3 as dev environment, which is sufficient here.
>33K line, reverse-sorted text file of word_post_counts (one count for a word per post, excluding dupes).
>https://files.catbox.moe/o38sax.txt
Little bit of criticism: The text file uses empty spaces between the counter and the term, and not always the same amount. A tab would have been better for parsing it, no big deal though. Also, after working on it for a bit I realized that the counting should happen later, also not a big deal since I got the data. In general the whole thing turned out to be more difficult than I thought at the beginning. 
[code]
import nltk
from nltk.corpus import stopwords
from nltk.stem import WordNetLemmatizer

file = open('/path/RobowaifuBoard/o38sax.txt', 'r')
data = file.read()
file.close()
  
parsed = data.split('\n')
parsed2 =  [term.split('   ') for term in parsed]

# just a peek into the data, list entry no 4223
parsed2[4223]
# returns: ['10', '  wholesome'] - LOL

# this removes the counter, only the term will be in the list
# we'll use the counter later, by making a dict out of the parsed2 data
tokens = [token[-1] for token in parsed2]

# removing some common words from the list 
clean_tokens = tokens[:]                                                                                                                                                             
sr = stopwords.words('english')                                                                                                                                      
for token in tokens:                         
    if token in stopwords.words('english'):                      
        clean_tokens.remove(token)

# the first line here is unnecessary, since the data was lower case already
# the second removes all non alphabetical characters from every entry
# this could be a problem with names, so mb keep the numbers or make a diff later?
# the { } makes it return a set, not a list, which means every double entry will be removed 
lower_tokens_set = {token.lower() for token in clean_tokens}
alpha_only_set = {''.join(c for c in string if c.isalpha()) for string in lower_tokens_set if len(string) > 3}

# this breaks down every KNOWN entry to it's simple grammatical form
# it uses the Wordnet corpus for that and again removes double entries
lemmatizer = WordNetLemmatizer()
lemmatized = {lemmatizer.lemmatize(token) for token in list(alpha_only_set)} 

len(lemmatized)
# will return 21016, which is still waaay to much, but at least a start.
[/code]

# 17
>>7911
I'm the author of that system. Give me an exact layout you'd prefer for your work and I can post a link to that ITT.

# 18
>>7913
I might add again that this is an optimization approach for millisecond-fast searches across all of /robowaifu/ . Our shitposting waifus will need something like that available to them. It doesn't represent a clear ordering (for example each word is only counted once per post). 

But by the same token, ''all'' the text is available as simple text (and I also fully parse that as well during the 2-3 second startup).

# 19
>>7913
Thanks, I'm working on other things as well and for now I should stop, so this isn't so urgent. But make it handing out the data as clean and homogeneous as possible is a always a good thing. Like keeping the distance between entries the same, or not having empty ones. However, not a big problem, I worked around it.  
- Having everything which starts with a big letter, but not at the beginning of a sentence might be worth filtering out.
- Also all tokens which consist only off upper case letters.
- Then returning all pairs or triplets of words might be great, though the file will be bigger then. Maybe this could help us to filter out common phrases. This might be more complicated as well, so are you really sure that there isn't already a library doing all of this?

>>7911
[code]
# cleaning empty string(s)
parsed2 = [token for token in parsed2 if token[0] is not '']

# putting all the terms with their counters in a dict, so I can call the counters (as an integer)
adict = {}
for token in parsed2:
    adict[token[-1].rstrip().lstrip()] = int(token[0])

adict['wholesome']
# will return 10
[/code]

# 20
>>7916
>so are you really sure that there isn't already a library doing all of this?
Haha, you tell me. I'm inventing this as I go along, but yea probably. All I know is that we need blazing fast performance and efficiency if we are to succeed at getting robowaifus working with older and smaller computers. But that's a far better approach than being dragged along by """TPTB""" with a hook in our jaws, unable to run even a modest algorithm w/o handing over a lot of gold for the latest in botnet hardware and loaded up with full-bloat pozzware.

Only our own software can be trusted. And if I had even the slightest chance of creating effective computers for our waifus, then you could be I would be learning how to create open-source ''hardware'' too.

Sure, I can set up sliding window datasets of the texts. I figured that 3, 5, and 7 word sequences might be useful as a modest beginning. I guess I can probably generate all 3 sets in roughly two or three seconds now, but we'd have to see. I'll need to finish getting this system knocked into shape over the next week or so and then I'll have a look at your idea Anon.

# 21
>>7917
>then you could ''bet''*

# 22
>>7916
I still need to work on this. I need to filter out the tokens with quotation marks and add together the counters if some term appears twice. Terms with "/" need do be handled as a special case, because "/robowaifu/" isn't the same than robowaifu, and "alogs/robowaifu" can't become "alogsrobowaifu". For the search on topics this might not be relevant, though. Since dicts seem to not allow special chars in their keys, I might need to handle these entries in separate.

# 23
>>7919
Hey there, since it's trivial enough to do for me now, I went ahead and created a plain text file for you of every post on robowaifu (as of a few minutes ago, so you can even find your post there). I have a rudimentary approach to cleaning up the text just a bit before inserting it into the data containers so it's not an ''exact'' match to the posts. But, you might find it useful and I hope you can.

Cheers Anon.
https://files.catbox.moe/e37qds.7z

# 24
>>7922
Thanks, that's great. Except that you now filter out all non alphabetical characters? A reference to the board like "/robowaifu/" becomes "robowaifu" now, which is like a mentioning of a robowaifu. Cleaning these extra chars out should probably done later, before counting singular words, but some then still need to be a special case. Only when used as key for a dict "/" can't be in there. Some if the quotes are also being used to show that terms belong together, like a name of a movie. Such things should be able to be filtered out and stored into a extras list or file.

# 25
>>7923
Heh, in a word:
'''Yes.'''

We have two different agendas going on here: A) atm, mine is to create a search system that responds much faster than human perception, and to provide reasonably plausible links for the user to use in pursuing further information. For example, an AI such as B) your project that's trying to pin down exact semantic meanings, etc.

Think of my tool as one that ''your'' tool can use as a front-end to quickly locate research material to use. For that material, you have the full JSON files to parse exactly as you see fit ofc.

# 26
>>7923
Hey Anon, so as a Christmas present to you I created another version of the all_posts.txt file that '''doesn't''' have much in the way of filtering at all. I hope it can be of some help to you. Good luck with your project.

online text:
https://files.catbox.moe/h6jp5n.txt
zip you can download:
https://files.catbox.moe/ub266f.7z

Merry Christmas!

# 27
>>7937
Thanks. I'm just trying occasionally if and how we can use this to find the most interesting terms on the board and per posting, so that the index thread can be, at least in part, created automatically.

# 28
>>7916

[code]
# cleaning the space from the terms in the entry
parsed3 = [(token[0], token[-1].lstrip().rstrip()) for token in parsed2]
# also everything which is not a letter or number
parsed4 = [(token[0], ''.join(c for c in token[-1] if c.isalpha() or c.isnumeric())) for token in parsed3]

# creating a dict, counting the counters of entries together which appear twice due cleaning
better_dict = {}
keys = []
for token in parsed4:
    keys = (better_dict.keys())
    if token[-1] in keys:
        better_dict[token[-1]] = better_dict[token[-1]] + int(token[0])
    else:
        better_dict[token[-1]] = int(token[0])

#Test
better_dict['wholesome']

[/code]

# 29
[code]
from nltk.stem import PorterStemmer    
stemmer = PorterStemmer()

# finding all the terms lemmatizing didn't
# if the simple form is already in the set "lemmatized_longerthan3" then the longer one can be removed. First step is to have a list or set with those.
stemmeable = {token for token in lemmatized_longerthan3 if stemmer.stem(token) in lemmatized_longerthan3 and token != stemmer.stem(token)}
# Then the one is substracted from the other. Which kills around 3000 terms.
longerthan3 = list(set(lemmatized_longerthan3) - stemmeable)

# For a side to side peak into it, uncomment the following lines: 
# comp = [(token, stemmer.stem(token)) for token in stemmeable]
# comp[42]

# The Lancaster stemmer takes even some more out, I think it's good to have both results to work with. For now I substract both from the data.
from nltk.stem.lancaster import LancasterStemmer
st = LancasterStemmer()
lancastered = {token for token in lemmatized_longerthan3 if st.stem(token) in lemmatized_longerthan3 and token != st.stem(token)}
longerthan3 = list(set(lemmatized_longerthan3) - lancastered)
[/code]

We are down to only around 17k terms now. Huraay. Next, I'll try to use a list with the most common terms in English to get rid of those. If that doesn't bring down the number a lot, this whole approach failed. We currently have more than 7k terms appearing only once and 1.5k terms appearing more than 20 times. Looking into these lists, I can't see any pattern emerging.

# 30
Found a PyTorch implementation of PCGrad: https://github.com/WeiChengTseng/Pytorch-PCGrad
Based on the paper Gradient Surgery for Multi-Task Learning: https://arxiv.org/pdf/2001.06782.pdf

PCGrad fixes conflicts between two gradients that are causing learning interference to ensure when combined they move towards the optimal loss instead of a random direction. It performs best with a high learning rate, which is particularly interesting to training with extremely large batch sizes since higher learning rates can be used in those circumstances to improve training efficiency. PCGrad greatly enhances both accuracy and data efficiency and also works with reinforcement learning.

I'm not sure how compatible it is with gradient accumulation. It seems no one has reported results on that yet, but I'll do some tests find out.

It's also fairly simple to implement. Implementing this in mlpack should be a piece of cake and could enable older hardware to outperform what a modern desktop can do today without PCGrad. Of course one with PCGrad would still rip older hardware to shreds but I think it's cool this might enable older hardware to be able to train voice synthesis models and such, given they have enough memory to hold the model.

The official Tensorflow implementation is also available here: https://github.com/tianheyu927/PCGrad

# 31
Python will soon have switch statements, resulting in even more readeable code. Some comment say this resembles finite-state machines and will also increase the quality of the code.
https://hackaday.com/2021/04/02/python-will-soon-support-switch-statements/

# 32
>>9476
>match

That looks really nice. I hope C++ will adopt something like that soon. They have occasionally demonstrated a willingness to step outside the beaten path of diehard C fanatics and do something a lot better. Full regex pattern matching for the switch() statement in C++ would be a very, very powerful mechanism indeed. Typically I don't consider Python's typeless variable paradigm an advantage -- quite the opposite, in fact. However this '''match''' qualifies in my mind as an exception to that rule.

Thanks Python-Anon! :^)

# 33
>>9476
This will be immensely useful for scripting symbolic AI. Using elif statement trains or dictionaries for switch cases is a train wreck.

>>9478
Python has had typing annotations since 3.5 and they've generally become standard practice because debugging without them is a nightmare.
[code]def greeting(name: str) -> str:
    return 'Hello ' + name[/code]
The Python runtime doesn't enforce these types but they can be checked with the IDE or other tools like mypy before running.
[code]python -m pip install --user mypy
mypy test.py && python test.py[/code]
Jupyter notebooks can also be checked using nbqa with mypy:
[code]python -m pip install --user nbqa
nbqa mypy notebook.ipynb[/code]
Another useful package for Jupyter notebooks is nbconvert which can convert them to Python scripts and HTML.
[code]python -m pip install --user nbconvert
jupyter nbconvert --to script notebook.ipynb
jupyter nbconvert --to html notebook.ipynb[/code]

# 34
>>9484
>typing annotations
I see. I didn't realize any of that. Thanks for the detailed explanation, Anon!

# 35
any nontrivial materials for learning llvmlite? I want to write compiler for metatrader-like language, means programs that not get run once sequentially, but certain parts of program run every "tick" (meaning every time price changes) and all is conditional on price change. 
Most examples are hello world languages, i am not sure how to begin writing standard library for my hello world language that will support what i want

# 36
>>9558
>any nontrivial materials for learning llvmlite?
You can hardly get more 'nontrivial ' for learning some code than, well, the ''code itself'', Anon.
https://github.com/numba/llvmlite

# 37
>>9484
>Python has had typing annotations since 3.5
Starting with 3.9 this here seems to be interesting: 
>Type annotations for a tensor's shape, dtype, names, ...
>Bye-bye bugs! Say hello to enforced, clear documentation of your code.
>If (like me) you find yourself littering your code with comments like # x has shape (batch, hidden_state) or statements like assert x.shape == y.shape , just to keep track of what shape everything is, then this is for you.
https://github.com/patrick-kidger/torchtyping

# 38
>>9673
Great find, anon. This is incredibly useful. I had no idea about typeguard either that does run-time type checking.

# 39
>>9673
Thanks, Anon. Much appreciated.

# 40
Here's a thread on Reddit about a problem with random in Numpy and PyTorch: https://www.reddit.com/r/MachineLearning/comments/mocpgj/p_using_pytorch_numpy_a_bug_that_plagues - It's about setting seeds in the data loader when using Numpy's random number generator. A lot of people got it wrong and 100k+ tested projects on Github, 95% got it wrong. It's not a bug, but easy to overlook.

# 41
>>9950
Surprising something like that could go unnoticed so long. C++'s standard library has a generator that uses hardware entropy device if available (almost always is in past 10 years). I wonder if Python provides something similar.

# 42
>The secrets module is used for generating cryptographically strong random numbers suitable for managing data such as passwords, account authentication, security tokens, and related secrets.
>In particular, secrets should be used in preference to the default pseudo-random number generator in the random module, which is designed for modelling and simulation, not security or cryptography.
https://docs.python.org/3/library/secrets.html

# 43
Here are 70+ Python coding projects, to learn Python or getting better at it. Some also strike me as useful for any home assistant. https://www.theinsaneapp.com/2021/06/list-of-python-projects-with-source-code-and-tutorials.html

# 44
>>10810
Thanks anon, this is good stuff! That one about age and gender detection with computer vision looks especially useful.

# 45
I'm actually working on a sentiment analysis neural network with TensorFlow, but it's actually pretty bad because I can't find a proper dataset to train it. Has anyone ever found something that could prove useful in the future?

# 46
>>10893
There's a 'dataset' thread Anon, maybe you can find something useful there? (>>2300)

# 47
Neat! I went for months (at least a year maybe?) despondent, angry & frustrated with Python because it's freakin hard to get anything to work with it. I even made my system entirely unusable one time trying do a downgrade (had to nuke my whole box and start over).

I tried for the 1'000th time it seems to get Spyder installed and running, and '''this''' time, have actually made some forward progress!
>

I discovered this one stupid Python trick yesterday:
[code]pip3 list --outdated --format=freeze | grep -v '^\-e' | cut -d = -f 1 | xargs -n1 pip3 install -U[/code]
Now I expect all the bitches will be clamoring for my attention now of course. 

I had to re-run and re-run it, but finally after maybe a dozen times, enough of the system was upgraded sufficiently to actually bring the IDE up.

Now if I can only figure out a way to ''downgrade'' the three libraries in the warning dialog, I can actually apply myself to learning Python soon. I'm not hopeful even now though, and I'm terribly gunshy after all my previous unsuccessful efforts getting Python dependencies sorted out.

# 48
>>11584
>'''Update:'''
Well whadya know? I seemed to find a way that a) didn't destroy my machine in the process (always important!), and b) got rid of the error warning in Spyder.
[code]pip uninstall jedi
pip install --upgrade jedi==0.17.2

pip uninstall parso
pip install --upgrade parso==0.7.0

pip uninstall pyls_spyder
pip install --upgrade pyls_spyder==0.3.2[/code]
>

It came from a LUA site, of all places.
code.luasoftware.com/tutorials/python/python-pip-downgrade-package/

# 49
>>11584
You probably should use virtual environments: https://realpython.com/python-virtual-environments-a-primer/

# 50
>>11589
>'''Update-update'''
Turns out, the __exact__ reason I wanted an IDE (rather than just a Python console) ''doesn't work on my machine'' even after downgrade-patching the lib dependencies.
>

I tried restarting several times, but didn't help. I noticed the IDE had a little message at the bottom 'LSP Python restarting' with a little orbiting icon. Finally the orbit stopped and the message changed to
>
maybe it's related to code-completion not working, etc.

I don't '''want''' to hate Python, I really don't. **It's simply impossible not to do, of course. D:<**
>pic related

# 51
>>11591
There seems to be an Anaconda installer, did anyone try that one? https://anaconda.org/anaconda/spyder
Spyder really looks promising. Most machine learning scientists and engineers seem to use Jupyter notebooks, though. In case you didn't know.
These two config frameworks were also mentioned, for managing configuration of ML projects without the notebooks: https://medium.com/pytorch/hydra-a-fresh-look-at-configuration-for-machine-learning-projects-50583186b710
https://github.com/toml-lang/toml

# 52
>>11591
What OS or distro are you using?

Also:
[code]python --version
pip --version
python -m pip --version
pip show torch tensorflow spyder
uname -a[/code]
>>11592
Jupyter notebooks are great for experimenting but not so much for writing libraries. Personally I write most of my code in Mousepad that only has syntax highlighting and only touch Spyder when I'm writing clean code for other people to use.

# 53
Sentdex created an open-source Python code transformer model like Github Copilot. It has only been trained 2 epoches so it's not great but it's interesting and fun to play around with. I feel it's gonna be important to stay on top of these developments to keep up with AI-accelerated productivity so I made an easy-to-use GUI to inference these models (just press Control+Tab to generate.)

GottaPyFast: https://gitlab.com/robowaifudev/gottapyfast/

Sentdex Demo: https://www.youtube.com/watch?v=1PMECYArtuk
Sentdex Model: https://huggingface.co/Sentdex/GPyT

How to use the model:
[code]from transformers import AutoTokenizer, AutoModelWithLMHead

# set device to cuda if you have a GPU
device = "cpu"
tokenizer = AutoTokenizer.from_pretrained("Sentdex/GPyT")
model = AutoModelWithLMHead.from_pretrained("Sentdex/GPyT").to(device)

def generate(model, query, max_length=100, top_p=0.9, temperature=1.0, do_sample=True):
    newlinechar = "<N>"
    query = query.replace("\n", newlinechar)
    tokenized = tokenizer.encode(query, return_tensors="pt").to(model.device)
    response = model.generate(tokenized, max_length=max_length, do_sample=do_sample, top_p=top_p, temperature=temperature).to(model.device)
    decoded = tokenizer.decode(response[0])
    return decoded.replace("<N>","\n")

print(generate(model, "import torch", max_length=256, top_p=0.95, temperature=1.0))[/code]

# 54
Trying to package PyTorch and Transformers for Windows is a nightmare. I put together some notes here on how to get it to work:
https://gitlab.com/robowaifudev/cookbook/-/wikis/python/pyinstaller

I think using MLPack would be much more practical. PyTorch takes up a massive 3.1 GB which is completely unnecessary. Another option could be to rewrite the GPT2 transformer model to use NumPy instead which is only 5.4 MB. I'll look more into this later.

# 55
>>11683
Thanks for all your hard work here Anon. I apologize to you and everyone else here for being such a pussified faggot about Python. I recognize it's important to all of us, or else I wouldn't even consider picking it up.

Please look into mlPack ''sooner'' rather than later if you at all can. It's probably our only real hope for doing waifu AI on a shoestring budget hardware-wise.

# 56
>>11684
MLPack's documentation is really lacking, especially for newer features and seems to be missing essential features. I'd I have to sit down with it for 3-6 months to get transformers and text-to-speech models working in it.

I'm looking into using Chainer which is built on top of NumPy and quite popular in Japan. A basic application with Chainer packaged with PyInstaller compresses down to 14 MB. On top of that there's already lots of ML models implemented in it.

I think if I roll out some waifu tech with Chainer to garner interest we could get some more help to build things in MLPack, which will be particularly useful for embedded systems and actual physical robowaifu.

# 57
>>11688
Migration guide from PyTorch to Chainer
https://chainer.github.io/migration-guide/

