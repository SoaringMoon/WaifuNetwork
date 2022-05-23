# 1
https://wenlong.page/language-planner/

https://github.com/huangwl18/language-planner



Can world knowledge learned by large language models (LLMs) be used to act in interactive environments? In this paper, we investigate the possibility of grounding high-level tasks, expressed in natural language (e.g. "make breakfast"), to a chosen set of actionable steps (e.g. "open fridge"). While prior work focused on learning from explicit step-by-step examples of how to act, we surprisingly find that if pre-trained LMs are large enough and prompted appropriately, they can effectively decompose high-level tasks into low-level plans without any further training. However, the plans produced naively by LLMs often cannot map precisely to admissible actions. We propose a procedure that conditions on existing demonstrations and semantically translates the plans to admissible actions. Our evaluation in the recent VirtualHome environment shows that the resulting method substantially improves executability over the LLM baseline. The conducted human evaluation reveals a trade-off between executability and correctness but shows a promising sign towards extracting actionable knowledge from language models.



I think it's worth a whole thread. 

If not, move it to the appropriate section.

# 2
Update in this topic, this time by DeepMind. 

https://www.youtube.com/watch?v=L9kA8nSJdYw

Slowly, they realize what we all think about, yet only in virtual spaces.

# 3
>>16197

>Human: show me how you polish the baluster

>Robowaifu: say no more goshujin-sama



There was a really interesting paper recently on context-aware language models that can do planning and achieve better than human performance on a flight-booking task, using a model the same size as GPT-2 small: https://sea-snell.github.io/CALM_LM_site/

It shows a lot of promise for using a Monte Carlo tree search for doing planning with language models, since it only takes 5 dialog generation attempts with the new method to outdo human performance without doing a tree search at all.



Also a huge breakthrough in zero-shot multi-modal learning has been made that completely blows CLIP and SotA specialized models to pieces by using a simple to understand contrastive and captioning loss (CoCa) that can leverage existing models: https://arxiv.org/pdf/2205.01917.pdf

This is going to be huge for embodied agents. It's a lot like the similarity measure used between sentence embeddings produced by the RoBERTa model in OP's paper to ensure the translated generated instructions are executable, except it does it between images and sentences.



And there's another paper worth mentioning doing transfer learning from a language model trained on Wikipedia to an RL agent (on continuous control and games) that outperforms training from scratch: https://arxiv.org/pdf/2201.12122.pdf



It seems we're headed towards a leap forward soon with goal-oriented embodied agents using language models.

