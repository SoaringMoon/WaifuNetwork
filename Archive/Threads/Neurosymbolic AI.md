# 1
I stumbled upon a couple videos critiquing "Deep Learning" as inefficient, fragile, opaque, and narrow [1]. It claims Deep Learning requires too much data, yet it performs poorly trying to extrapolate from training set, and how it arrives to its conclusions are opaque, so it's not immediately obvious why it breaks in certain cases, and all that learned information cannot be transfered between domains easily. They then put forth "Neurosymbolic AI" as the solution to DL's ails and next step of AI, along with NS-VQA as an impressive example at the end [2]. What does /robowaifu/ think about Neurosymbolic AI (NeSy)?

NeSy is any approach that combines neural networks with symbolic AI techniques to take advantage of both their strengths. One example is the Neuro-Symbolic Dynamic Reasoning (NS-DR) applied on the CLEVRER dataset [3], which cascades information from neural networks into a symbolic executor. Another example is for symbolic mathematics [4], which "significantly outperforms Wolfram Mathematica" in speed and accuracy.

The promise or goal is that NeSy will bring about several benefits:
1. Out-of-distribution generalization
2. Interpretability
3. Reduced size of training data
4. Transferability
5. Reasoning
I brought it up because points 3 and 5, and to a lesser degree 4, are very relevant for the purpose of making a robot waifu's AI. Do you believe these promises are real? Or do you think it's an over-hyped meme some academics made to distract us from Deep Learning? I'm split between believing these promises are real and this being academics trying to make "Neurosymbolic AI" a new buzzword. [5] tries to put forth a taxonomy of NeSy AIs. It labels [4] as an example of NeSy since it parses math expressions into symbolic trees, but [4] refers to itself as Deep Learning, not neurosymbolic or even symbolic. Ditto with AlphaGo and self-driving car AI. And the NS-DR example was beaten by DeepMind's end-to-end neural network Aloe [6], and overwhelmingly so when answering CLEVRER's counterfactuals. A study reviewed how well NeSy implementations met their goals based on their paper, but their answer was inconclusive [7].

It's also annoying looking for articles on this topic because there's like five ways to write the term (Neurosymbolic, Neuro Symbolic, Neuro-Symbolic, Neural Symbolic, Neural-Symbolic).

>References
[1] MIT 6.S191 (2020): Neurosymbolic AI. <https://www.youtube.com/watch?v=4PuuziOgSU4>
[2] Neural-Symbolic VQA: Disentangling Reasoning from Vision and Language Understanding. <http://nsvqa.csail.mit.edu/>
[3] CLEVRER: CoLlision Events for Video REpresentation and Reasoning. <http://clevrer.csail.mit.edu/>
[4] Deep Learning for Mathematics <https://arxiv.org/abs/1912.01412> (article: <https://www.quantamagazine.org/symbolic-mathematics-finally-yields-to-neural-networks-20200520/>)
[5] The Third AI Summer. Part III. <https://youtu.be/_cQITY0SPiw?t=1745>
[6] Attention over learned object embeddings enables complex visual reasoning. <https://arxiv.org/abs/2012.08508> (article: <https://venturebeat.com/2020/12/21/deepmind-researchers-claim-neural-networks-can-outperform-neurosymbolic-models-on-visual-tasks/>)
[7] Is Neuro-Symbolic AI Meeting its Promise in Natural Language Processing? A Structured Review. <https://arxiv.org/abs/2202.12205>

>Further Reading
Neurosymbolic AI: The 3rd Wave. <https://arxiv.org/abs/2012.05876>
Neuro-Symbolic AI Archives. <https://mitibmwatsonailab.mit.edu/category/neuro-symbolic-ai/>

# 2
>>16217
I think such critique is outdated. The impressive results of NS-VQA have been beaten by full deep learning approaches like MDETR.[1] It would be a bit ironic to call deep learning fragile and narrow and then proceed to write specific functions that only handle a certain type of data that the training set just happens to be a small subset of and call it generalization. Sure it can handle 'out-of-distribution' examples with respect to the training set, but give it a truly out-of-distribution dataset with respect to the functions and these handwritten methods will fail completely.

A lot of deep learning approaches these days can learn entire new classes of data from as few as 10-100 examples. ADAPET[2] learns difficult language understanding tasks from only 32 examples. RCE[3] can learn from a single success state example of a finished task. DINO[4] can learn to identify objects from no labelled examples at all. CLIP[5] and CoCa[6] are examples of deep learning generalizing to datasets they were never trained on, including adversarial datasets, and outperforming specialized models, and this is just stuff off the top of my head. Someone ought to give DALL-E 2 the prompt "a school bus that is an ostrich" and put that meme to rest.

That said, neurosymbolic AI has its place though and I've been using it lately to solve problems that aren't easily solvable with deep learning alone. There are times when using a discrete algorithm saves development time or outperforms existing deep learning approaches. I don't really think of what I'm doing as neurosymbolic AI either. Stepping away from matrix multiplications for a bit doesn't suddenly solve all your problems and become something entirely different from deep learning. You have to be really careful actually because often a simpler deep learning approach will outperform a more clever seeming neurosymbolic one, which is clearly evident in the progression of AlphaGo to AlphaZero to MuZero. From my experience it hasn't really delivered much on the promises you listed, except maybe point 2 and 5. I wouldn't think of it as something good or bad though. It's just another tool and it's what you do with that tool what counts.

There was a good paper on how to do supervised training on classical algorithms. Basically you can teach a neural network to do a lot of what symbolic AI can do, even complicated algorithms like 3D rendering, finding the shortest path or a sorting algorithm. I think it shows we've barely scratched the surface of what neural networks are capable of doing.
https://www.youtube.com/watch?v=01ENzpkjOCE
https://arxiv.org/pdf/2110.05651.pdf

>Links
1. https://arxiv.org/abs/2104.12763
2. https://arxiv.org/abs/2103.11955
3. https://arxiv.org/abs/2103.12656
4. https://arxiv.org/abs/2104.14294
5. https://arxiv.org/abs/2103.00020
6. https://arxiv.org/abs/2205.01917

# 3
Idling around the Interwebz today[a], I found myself reading the ''Chinese Room Argument'' article on the ''IEP''[b], I came across the editor's contention in the article the notion that "mind is everywhere" is an "absurd consequence".
>''"Searle also insists the systems reply would have the absurd consequence that “mind is everywhere.” For instance, “there is a level of description at which my stomach does information processing” there being “nothing to prevent [describers] from treating the input and output of my digestive organs as information if they so desire.” "''[1],[2]

I found that supposed-refutation of this concept vaguely humorous on a personal level. As a devout Christian Believer, I would very strongly assert that indeed, ''Mind'' __is__ everywhere. Always has been, always will be. To wit: The Holy Spirit ''sees and knows everything, everywhere''. As ''King David'' wrote:
>7  Where can I go to escape Your Spirit?
>     Where can I flee from Your presence?
>8  If I ascend to the heavens, You are there;
>      if I make my bed in Sheol, You are there.
>9  If I rise on the wings of the dawn,
>      if I settle by the farthest sea,
>10 even there Your hand will guide me;
>      Your right hand will hold me fast.[3]

However, I definitely agree with the authors in their writing that 
>''"it's just ridiculous"''
to assert 
>''" “that while [the] person doesn’t understand Chinese, somehow the conjunction of that person and bits of paper might” ".''[1],[2] 

We robowaifuists face a '''mighty''' set of challenges & conundrums in our ''Herculean'' quest for great robowaifus with great robowaifu 'minds'. As with the human biological systems, I would admonish all of us here to closely investigate the human ''soul'' (and soul-accessories) in this frontiersman-tier adventure before us! :^)

'''==='''

1. https://iep.utm.edu/chinese-room-argument/
2. Searle, John. 1980a. “Minds, Brains, and Programs.” ''Behavioral and Brain Sciences'' 3, 417-424.
3. https://biblehub.com/bsb/psalms/139.htm

a.  related shitposts:
     http://tew7tfz7dvv4tsom45z2wseql7kwfxnc77btftzssaskdw22oa5ckbqd.onion/valis/res/2530.html#2530
b. ''Internet Encyclopedia of Philosophy'' (maintained by the ''University of Tennessee at Martin'')

>===
-''minor fmt, prose edit''

