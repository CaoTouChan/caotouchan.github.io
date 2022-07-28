---
layout: post
read_time: true
show_date: true
title: "Transformer 系列大纲"
date: 2022-07-28
description: "In this series of articles we examine the details of how transformers work, and dive into the different kinds of transformers in different fields. "
img: posts/20220728/transformer.jpg
tags: [NLP, artificial intelligence, transformer]
author: Alex Chan
---

这段时间看了许多 Transformer 系列的文章，想着要不就用这个来作为我新博客的开篇吧。

自2017年以来，随着 Transformer 系列模型的发展，NLP（自然语言处理）、CV（计算机视觉）、RL（增强学习）、GANs 等领域都在探索其潜力。

系列文章会不断更新，本文为索引：

| 状态 | 领域                   | 年份   | 模型                   | 文章 | 原始论文                                                                                                                                                                                   | 简介                              |
|----|----------------------|------|----------------------|----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
|    | NLP                  | 2017 | Transformers         |    | [Attention Is All You Need](https://arxiv.org/abs/1706.03762)                                                                                                                          | 继MLP、CNN、RNN后的第四大类架构            |
|    | NLP                  | 2018 | GPT                  |    | [Improving Language Understanding by Generative Pre-Training](https://s3-us-west-2.amazonaws.com/openai-assets/research-covers/language-unsupervised/language_understanding_paper.pdf) | Pretrain w Transformer Decoder  |
|    | NLP                  | 2019 | GPT-2                |    | [Language Models are Unsupervised Multitask Learners](https://d4mucfpksywv.cloudfront.net/better-language-models/language_models_are_unsupervised_multitask_learners.pdf)              | Larger GPT                      |
|    | NLP                  | 2020 | GPT-3                |    | [Language Models are Few-Shot Learners](https://arxiv.org/abs/2005.14165)                                                                                                              | FSL 效果很棒                        |
|    | NLP                  | 2018 | Bert                 |    | [BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding](https://arxiv.org/abs/1810.04805)                                                                   | Transformer 模型屠榜 NLP            |
|    | NLP                  | 2021 | Codex                |    | [Codex](https://arxiv.org/pdf/2107.03374.pdf)                                                                                                                                          | 代替程序员？                          |
|    | CV                   | 2020 | ViT                  |    | [AN IMAGE IS WORTH 16X16 WORDS: TRANSFORMERS FOR IMAGE RECOGNITION AT SCALE](https://arxiv.org/pdf/2010.11929.pdf)                                                                     | Transformer 进入 CV               |
|    | CV                   | 2020 | DETR                 |    | [End-to-End Object Detection with Transformers](https://arxiv.org/pdf/2005.12872.pdf)                                                                                                  |                                 |
|    | CV                   | 2021 | CLIP                 |    | [CLIP: Connecting Text and Images](https://openai.com/blog/clip/)                                                                                                                      | 对比学习：图片 &文本                     |
|    | CV                   | 2021 | Swin Transformer     |    | [Swin Transformer: Hierarchical Vision Transformer using Shifted Windows](https://arxiv.org/pdf/2103.14030.pdf)                                                                        |                                 |
|    | CV                   | 2021 | MLP-Mixer            |    | [MLP-Mixer: An all-MLP Architecture for Vision](https://arxiv.org/pdf/2105.01601.pdf)                                                                                                  | MLP 替代自注意力                      |
|    | CV                   | 2021 | MAE                  |    | [Masked Autoencoders Are Scalable Vision Learners](https://arxiv.org/pdf/2111.06377.pdf)                                                                                               | BERT的CV版                        |
|    | RL                   | 2021 | Decision Transformer |    | [Decision Transformer: Reinforcement Learning via Sequence Modeling](https://arxiv.org/pdf/2106.01345.pdf)                                                                             |                                 |
|    | RL                   | 2021 |                      |    | [Pretrained Transformers As Universal Computation Engines](https://arxiv.org/pdf/2103.05247.pdf)                                                                                       |                                 |
|    | Scaling transformers | 2021 | Switch Transformers  |    | [Switch Transformers: Scaling to Trillion Parameter Models with Simple and Efficient Sparsity](https://arxiv.org/abs/2101.03961)                                                       |                                 |
|    | Scaling transformers | 2022 | ST-MoE               |    | [ST-MoE: Designing Stable and Transferable Sparse Expert Models](https://arxiv.org/abs/2202.08906)                                                                                     |