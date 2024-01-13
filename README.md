# GPT-Arabic
This simple GPT implementation uses a decoder-only transformer to generate Arabic poems. This implementation is inspired by Let's Build GPT: From Scratch by Andrej Karpathy.
# DataSet
Poem Comprehensive Dataset: The Arabic dataset is scraped mainly from الموسوعة الشعرية and الديوان. After merging both, the total number of verses is 1,831,770 poetic verses[1].
# Archeticure
We used the decoder only of the transformer structure declared in the paper "Attention is All You Need paper"[2], while the full structure (Encoder and decoder) is mainly used for machine translation, we only need
the decoder to build GPT. 
# Further work
To specify the GPT for specific tasks we need to fine-tune the model, I recommend reading the paper "Language Models are Few-Shot Learners"[3] and OPENAI blog[4]for more details and an efficient approach to achieve it.

# References
1- Poem Comprehensive Dataset https://hci-lab.github.io/LearningMetersPoems/
2- - Attention is All You Need paper: https://arxiv.org/abs/1706.03762
3- OpenAI GPT-3 paper: https://arxiv.org/abs/2005.14165 
4- OpenAI ChatGPT blog post: https://openai.com/blog/chatgpt/
