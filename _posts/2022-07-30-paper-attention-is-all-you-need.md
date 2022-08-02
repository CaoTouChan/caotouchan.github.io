---
layout: post
read_time: true
show_date: true
title: "Transformer 模型结构解析"
date: 2022-07-30
description: ""
img: posts/20220730/transformer.jpg
tags: [NLP, artificial intelligence, transformer]
author: Alex Chan
mathjax: yes
toc: yes
---


# 缘起

Transformer 变得流行之前，深度学习的三大架构就是 MLP、 CNN、 RNN。其中，RNN 架构是当时的语言模型和机器翻译领域的主流。学界使用 RNN 和 encoder-decoder 结构来不断推动其发展。

但是这个路线有两个主要缺点：

1. 并行（parallelization）差：这是 RNN 架构无法避免的
2. 内存限制

注意力机制之后在 encoder-decoder 架构中被应用，但是依然没法脱离 RNN 的限制。

也有一些工作是使用 CNN 来替代 RNN 处理相关任务，但 CNN 很明显无法处理长序列。

Transformer 站在巨人肩膀上，使用几个技巧来提升模型性能，解决相关难题：

1. Averaging attention-weighted position
2. Multi-Head Attention
3. Self-attention
4. End-to-end memory network

模型效果也很惊艳：在 WMT 2014 英德翻译任务上达到了 28.4 BLEU，比现有的最佳结果（包括合奏）提高了 2 BLEU 以上。

# 模型结构

<center><img src='./assets/img/posts/20220730/transformer_model.jpg' ></center>


Transformer 是一个 encode-decoder 结构的模型，Encoder 一次看全整个序列，而 Decoder 则一次只能看到一个元素。

## Encoder 和 Decoder 堆叠

Encoder 是由 N （ 此处 N=6， 可调参 ）层模块组成，每层都有两个子层：

1. 多头自注意力（Multi-Head Attention）
2. 全连接 FFN （fully connected feed-forward network）

同时，在每两个子层之间，都会有一个 `Add & Norm` 子层，使用数学表示是 $LayerNorm(x + Sublayer(x))$ ，其代表：

1. Add：输入和多头自注意力子层输出的残差连接（residual connection）
2. Norm：此处使用的是 Layer Normalization。


之所以使用 Layer Normalization 而不使用 Batch Normalization 的原因是：

- 一则变长序列下 BN 抖动较大（BN 是对特征做正则，而 LN 是对样本做正则）；
- 二则test阶段 BN 在超长序列下可能失效 （BN 算完全局 $λ$ 和 $β$ 后再应用）

为了参差残差连接生效，模型中的所有子层以及嵌入层都会产生维度 $d_{model} = 512$ （可调参）的输出。

Decoder 总体上和 Encoder 没有太大区别，只是为了不 “泄露答案”，对于位置 i 的预测，只能看到比 i 小的序列。

## Attention

<center><img src='./assets/img/posts/20220730/attention.jpg' ></center>

Attention 实际上是把一个 query 通过和一组 key-value 对做映射后输出，其中的 query、key、value 都是向量。

Transformer 里边的是多个 Scaled Dot-Product Attention 进行组合后做输出。

### Scaled Dot-Product Attention

初始化三个权重矩阵 $W^Q$、$W^K$、$W^V$，分别和 $Embedding( input )$ 相乘，可以得到上图 Scaled Dot-Product Attention 中的 $Q$、$K$、$V$，通过一下运算可以得到输出：

<p style="text-align:center">
\(
    Attention(Q, K, V) = Softmax(\frac{QK^T}{√(d_k)})V
    \)
</p>

其中，$d_k$ 是 q、k、v 的维度 （默认 64，可调参）。

下图是 [The Illustrated Transformer](http://jalammar.github.io/illustrated-transformer/) 一个示意图：


<center><img src='./assets/img/posts/20220730/sample_attn.jpg' ></center>

### Muti-Head Attention

Muti-Head Attention 实际上就是拼接多个 Scaled Dot-Product Attention 的结果，然后和一个权重矩阵$W^O$相乘后输出：

<p style="text-align:center">
\(
MultiHead(Q,K,V) = Concat(head_1,...,head_h)W^O, \\
where \space head_i = Attention(QW_i^Q, KW_i^K, VW_i^V)
\)
</p>

下图是 [The Illustrated Transformer](http://jalammar.github.io/illustrated-transformer/) 一个示意图：

<center><img src='./assets/img/posts/20220730/multihead_attn.jpg' ></center>

## Position-wise Feed-Forward Networks

FFN 层由两个线性变换和 RELU 激活函数构成：

<p style="text-align:center">
\(
FFN(x) = max(0, xW_1 + b_1)W_2 + b_2
\)
</p>

## Positional Encoding

Transformer 和 RNN、CNN 之类的结构不同，其输入和序列无关，为了表征位置信息，模型 Encoder 和 Decoder 的底部都添加了 Positional Encoding —— 其与输入的 Embedding 具有同样的维度 ($d_{model}$)。 下图是 [The Illustrated Transformer](http://jalammar.github.io/illustrated-transformer/) 一个示意图（假设 $d_{model}=4$）：

<center><img src='./assets/img/posts/20220730/positional_encoding.png' ></center>

其计算方式是：

<p style="text-align:center">
\(
PE(pos, 2i) = sin(\frac{pos}{n^{2i/d_{model}}} ) \\ 
PE(pos, 2i+1) = cos(\frac{pos}{n^{2i/d_{model}}} ) 
\)
</p>

假设 $n = 100， d_{model} = 4$，那么 "I am" 的 Positional Encoding 为：

```
I : pos=0, 
    PE(0,0) = PE(0, 2*0) = sin(0) = 0.00
    PE(0,1) = PE(0, 2*0+1) = cos(0) = 1.00
    PE(0,2) = PE(0, 2*1) = sin(0) = 0.00
    PE(0,3) = PE(0, 2*1+1) = cos(0) = 1.00
am : pos=1, 
    PE(1,0) = PE(1, 2*0) = sin(1/1) = 0.84
    PE(1,1) = PE(1, 2*0+1) = cos(1/1) = 0.54
    PE(1,2) = PE(1, 2*1) = sin(1/10) = 0.10
    PE(1,3) = PE(1, 2*1+1) = cos(1/10) = 1.00
```

论文中的 $n = 10000， d_{model} = 512$。


# 参考

1. [Vaswani, Ashish, et al. "Attention is all you need." Advances in neural information processing systems 30 (2017).](https://arxiv.org/abs/1706.03762)

2. [The Illustrated Transformer](http://jalammar.github.io/illustrated-transformer/)

3. [Transformers Or as I like to call it Attention on Steroids. 💉💊](https://towardsdatascience.com/transformers-89034557de14)

4. [Transformer论文逐段精读](https://www.youtube.com/watch?v=nzqlFIcCSWQ&ab_channel=MuLi)

5. [The Annotated Transformer](http://nlp.seas.harvard.edu/2018/04/03/attention.html)

