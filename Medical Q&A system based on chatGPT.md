# Medical Q&A system based on chatGPT

**This is a example from Bilbil website  <https://www.bilibili.com/video/BV1Hh4y137jb/?share_source=copy_web&vd_source=97728c4d5cab40e69919c88281c9e484>**

This is base on GPT-2 

GPT模型具体来说是一个transformer decoder。经典的transformer结构如下图所示，下图中左半部分是transformer encoder，它是一个双向的结构，既每一个单词既可以看到它前文信息又可以看到它后文信息；而下图右半部分是transformer decoder，它是一个单向(causal)的结构，既每一个单词只能看到它的前文信息但是看不到后文信息，这个功能可以通过mask来实现，将该单词后面位置的单词减掉一个极大的数就可以了。这里需注意下图中用红色框圈起来的部分，这部分仅是为了和transformer encoder做cross attention，由于GPT根本没有transformer encoder，红框部分自然没有存在的必要了，所以GPT每个transformer block的结构就是transformer decoder去掉红框后的部分。

The GPT model is specifically a transformer decoder, the classic transformer structure is shown in the following figure, the left half of the figure below is the transformer encoder, which is a bi-directional structure, each word can see both its preceding and following information; and the right half of the figure below is the transformer decoder, which is a uni-directional (causal) structure, each word can only see its preceding information but not the following information. transformer decoder, it is a unidirectional (causal) structure, that is, each word can only see the information before it but not after it, this function can be achieved through the mask, will be the word after the position of the word subtracted by a very large number of words can be. Here we need to pay attention to the part of the following figure circled in red, this part is only to do cross attention with the transformer encoder, because the GPT does not have a transformer encoder, the red part of the box naturally has no need to exist, so the GPT structure of each transformer block So the structure of each transformer block in GPT is the part of the transformer decoder after removing the red box.

<img width="380" alt="image" src="https://github.com/xinhaoyan/LLM/assets/111496997/7c1c69e4-1c72-4423-9fa6-226c8fe785da"> 

(From <https://zhuanlan.zhihu.com/p/619928985>)

<img width="808" alt="image" src="https://github.com/xinhaoyan/LLM/assets/111496997/7cfb9803-08c4-4bc3-b439-fbfd1ca28779">

<img width="888" alt="image" src="https://github.com/xinhaoyan/LLM/assets/111496997/c9fdc585-7c6d-47ff-9832-ceb891787b39">

有三条技术路线
Decoder： GPT
Encoder; bert
Decoder+ encoder: bart T5

Recommend Website: [Hugging Face]<https://huggingface.co/>


