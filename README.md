# GPT-Arabic
This simple GPT implementation uses a decoder-only transformer to generate Arabic poems. This implementation is inspired by Let's Build GPT: From Scratch by Andrej Karpathy.
# DataSet
Poem Comprehensive Dataset: The Arabic dataset is scraped mainly from الموسوعة الشعرية and الديوان. After merging both, the total number of verses is 1,831,770 poetic verses[1].
# Archeticure
We used the decoder only of the transformer structure declared in the paper "Attention is All You Need paper"[2], while the full structure (Encoder and decoder) is mainly used for machine translation, we only need
the decoder to build GPT. 
# Further work
To specify the GPT for specific tasks we need to fine-tune the model, I recommend reading the paper "Language Models are Few-Shot Learners"[3] and OPENAI blog[4]for more details and an efficient approach to achieve it.
# suggested exercises:
Suggested exercises:
- EX1: The n-dimensional tensor mastery challenge: Combine the `Head` and `MultiHeadAttention` into one class that processes all the heads in parallel, treating the heads as another batch dimension (answer is in nanoGPT).
- EX2: Train the GPT on your own dataset of choice! What other data could be fun to blabber on about? (A fun advanced suggestion if you like: train a GPT to do addition of two numbers, i.e. a+b=c. You may find it helpful to predict the digits of c in reverse order, as the typical addition algorithm (that you're hoping it learns) would proceed right to left too. You may want to modify the data loader to simply serve random problems and skip the generation of train.bin, val.bin. You may want to mask out the loss at the input positions of a+b that just specify the problem using y=-1 in the targets (see CrossEntropyLoss ignore_index). Does your Transformer learn to add? Once you have this, swole doge project: build a calculator clone in GPT, for all of +-*/. Not an easy problem. You may need Chain of Thought traces.)
- EX3: Find a dataset that is very large, so large that you can't see a gap between train and val loss. Pretrain the transformer on this data, then initialize with that model and finetune it on tiny shakespeare with a smaller number of steps and lower learning rate. Can you obtain a lower validation loss by the use of pretraining?
- EX4: Read some transformer papers and implement one additional feature or change that people seem to use. Does it improve the performance of your GPT?

# References
1- Poem Comprehensive Dataset https://hci-lab.github.io/LearningMetersPoems/
2- - Attention is All You Need paper: https://arxiv.org/abs/1706.03762
3- OpenAI GPT-3 paper: https://arxiv.org/abs/2005.14165 
4- OpenAI ChatGPT blog post: https://openai.com/blog/chatgpt/
