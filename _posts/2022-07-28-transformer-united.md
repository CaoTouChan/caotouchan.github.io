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
mathjax: yes
toc: yes
---
这段时间看了许多 Transformer 系列的文章，想着要不就用这个来作为我新博客的开篇吧。

自2017年以来，随着 Transformer 系列模型的发展，NLP（自然语言处理）、CV（计算机视觉）、RL（增强学习）、GANs 等领域都在探索其潜力。

系列文章会不断更新，本文为索引：

# NLP

## ✅ Transformer 
- [Vaswani, Ashish, et al. "Attention is all you need." Advances in neural information processing systems 30 (2017).](https://arxiv.org/abs/1706.03762)[![citation](https://img.shields.io/badge/dynamic/json?label=citation&query=citationCount&url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F204e3073870fae3d05bcbc2f6a8e263d9b72e776%3Ffields%3DcitationCount)](https://www.semanticscholar.org/paper/Attention-is-All-you-Need-Vaswani-Shazeer/204e3073870fae3d05bcbc2f6a8e263d9b72e776)
- [Transformer : 继 MLP、CNN、RNN 后的第四大类架构](./paper-attention-is-all-you-need)

## 💤 GPT 
- [Radford, Alec, et al. "Improving language understanding by generative pre-training." (2018).](https://s3-us-west-2.amazonaws.com/openai-assets/research-covers/language-unsupervised/language_understanding_paper.pdf)[![citation](https://img.shields.io/badge/dynamic/json?label=citation&query=citationCount&url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Fcd18800a0fe0b668a1cc19f2ec95b5003d0a5035%3Ffields%3DcitationCount)](https://www.semanticscholar.org/paper/Improving-Language-Understanding-by-Generative-Radford-Narasimhan/cd18800a0fe0b668a1cc19f2ec95b5003d0a5035) 

## 💤 GPT-2
- [Radford, Alec, et al. "Language models are unsupervised multitask learners." OpenAI blog 1.8 (2019): 9.](https://d4mucfpksywv.cloudfront.net/better-language-models/language_models_are_unsupervised_multitask_learners.pdf)[![citation](https://img.shields.io/badge/dynamic/json?label=citation&query=citationCount&url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F9405cc0d6169988371b2755e573cc28650d14dfe%3Ffields%3DcitationCount)](https://www.semanticscholar.org/paper/Language-Models-are-Unsupervised-Multitask-Learners-Radford-Wu/9405cc0d6169988371b2755e573cc28650d14dfe)

## 💤 GPT-3
- [Brown, Tom, et al. "Language models are few-shot learners." Advances in neural information processing systems 33 (2020): 1877-19](https://arxiv.org/abs/2005.14165)[![citation](https://img.shields.io/badge/dynamic/json?label=citation&query=citationCount&url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F6b85b63579a916f705a8e10a49bd8d849d91b1fc%3Ffields%3DcitationCount)](https://www.semanticscholar.org/paper/Language-Models-are-Few-Shot-Learners-Brown-Mann/6b85b63579a916f705a8e10a49bd8d849d91b1fc) 

## 💤 BERT
- [Devlin, Jacob, et al. "Bert: Pre-training of deep bidirectional transformers for language understanding." arXiv preprint arXiv:1810.04805 (2018).](https://arxiv.org/abs/1810.04805)[![citation](https://img.shields.io/badge/dynamic/json?label=citation&query=citationCount&url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Fdf2b0e26d0599ce3e70df8a9da02e51594e0e992%3Ffields%3DcitationCount)](https://www.semanticscholar.org/paper/BERT%3A-Pre-training-of-Deep-Bidirectional-for-Devlin-Chang/df2b0e26d0599ce3e70df8a9da02e51594e0e992)

## 💤 Codex
- [Chen, Mark, et al. "Evaluating large language models trained on code." arXiv preprint arXiv:2107.03374 (2021).](https://arxiv.org/pdf/2107.03374.pdf)[![citation](https://img.shields.io/badge/dynamic/json?label=citation&query=citationCount&url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Facbdbf49f9bc3f151b93d9ca9a06009f4f6eb269%3Ffields%3DcitationCount)](https://www.semanticscholar.org/paper/Evaluating-Large-Language-Models-Trained-on-Code-Chen-Tworek/acbdbf49f9bc3f151b93d9ca9a06009f4f6eb269)

# CV

## 💤 ViT 
- [Dosovitskiy, Alexey, et al. "An image is worth 16x16 words: Transformers for image recognition at scale." arXiv preprint arXiv:2010.11929 (2020).](https://arxiv.org/pdf/2010.11929.pdf)[![citation](https://img.shields.io/badge/dynamic/json?label=citation&query=citationCount&url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F7b15fa1b8d413fbe14ef7a97f651f47f5aff3903%3Ffields%3DcitationCount)](https://www.semanticscholar.org/paper/An-Image-is-Worth-16x16-Words%3A-Transformers-for-at-Dosovitskiy-Beyer/7b15fa1b8d413fbe14ef7a97f651f47f5aff3903)

## 💤 DETR
- [Carion, Nicolas, et al. "End-to-end object detection with transformers." European conference on computer vision. Springer, Cham, 2020.](https://arxiv.org/pdf/2005.12872.pdf)[![citation](https://img.shields.io/badge/dynamic/json?label=citation&query=citationCount&url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F962dc29fdc3fbdc5930a10aba114050b82fe5a3e%3Ffields%3DcitationCount)](https://www.semanticscholar.org/paper/End-to-End-Object-Detection-with-Transformers-Carion-Massa/962dc29fdc3fbdc5930a10aba114050b82fe5a3e)

## 💤 CLIP
- [Radford, Alec, et al. "Learning transferable visual models from natural language supervision." International Conference on Machine Learning. PMLR, 2021.](https://openai.com/blog/clip/)[![citation](https://img.shields.io/badge/dynamic/json?label=citation&query=citationCount&url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F6f870f7f02a8c59c3e23f407f3ef00dd1dcf8fc4%3Ffields%3DcitationCount)](https://www.semanticscholar.org/paper/Learning-Transferable-Visual-Models-From-Natural-Radford-Kim/6f870f7f02a8c59c3e23f407f3ef00dd1dcf8fc4)

## 💤 Swin Transformer
- [Swin Transformer: Hierarchical Vision Transformer using Shifted Windows](https://arxiv.org/pdf/2103.14030.pdf)[![citation](https://img.shields.io/badge/dynamic/json?label=citation&query=citationCount&url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Fc8b25fab5608c3e033d34b4483ec47e68ba109b7%3Ffields%3DcitationCount)](https://www.semanticscholar.org/paper/Swin-Transformer%3A-Hierarchical-Vision-Transformer-Liu-Lin/c8b25fab5608c3e033d34b4483ec47e68ba109b7)

## 💤 MLP-Mixer
- [Tolstikhin, Ilya O., et al. "Mlp-mixer: An all-mlp architecture for vision." Advances in Neural Information Processing Systems 34 (2021): 24261-24272.](https://arxiv.org/pdf/2105.01601.pdf)[![citation](https://img.shields.io/badge/dynamic/json?label=citation&query=citationCount&url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F2def61f556f9a5576ace08911496b7c7e4f970a4%3Ffields%3DcitationCount)](https://www.semanticscholar.org/paper/MLP-Mixer%3A-An-all-MLP-Architecture-for-Vision-Tolstikhin-Houlsby/2def61f556f9a5576ace08911496b7c7e4f970a4)

## 💤 MAE
- [He, Kaiming, et al. "Masked autoencoders are scalable vision learners." Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition. 2022.](https://arxiv.org/pdf/2111.06377.pdf) [![citation](https://img.shields.io/badge/dynamic/json?label=citation&query=citationCount&url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Fc1962a8cf364595ed2838a097e9aa7cd159d3118%3Ffields%3DcitationCount)](https://www.semanticscholar.org/paper/Masked-Autoencoders-Are-Scalable-Vision-Learners-He-Chen/c1962a8cf364595ed2838a097e9aa7cd159d3118)

## 💤 DALL·E 2
- [Ramesh, Aditya, et al. "Hierarchical text-conditional image generation with clip latents." arXiv preprint arXiv:2204.06125 (2022).](https://arxiv.org/abs/2204.06125)[![citation](https://img.shields.io/badge/dynamic/json?label=citation&query=citationCount&url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Fc57293882b2561e1ba03017902df9fc2f289dea2%3Ffields%3DcitationCount)](https://www.semanticscholar.org/paper/Hierarchical-Text-Conditional-Image-Generation-with-Ramesh-Dhariwal/c57293882b2561e1ba03017902df9fc2f289dea2)

# RL

## 💤 Decision Transformer
- [Chen, Lili, et al. "Decision transformer: Reinforcement learning via sequence modeling." Advances in neural information processing systems 34 (2021): 15084-15097.](https://arxiv.org/pdf/2106.01345.pdf)[![citation](https://img.shields.io/badge/dynamic/json?label=citation&query=citationCount&url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Fc1ad5f9b32d80f1c65d67894e5b8c2fdf0ae4500%3Ffields%3DcitationCount)](https://www.semanticscholar.org/paper/Decision-Transformer%3A-Reinforcement-Learning-via-Chen-Lu/c1ad5f9b32d80f1c65d67894e5b8c2fdf0ae4500)

## 💤 Universal Computation Engines
- [Lu, Kevin, et al. "Pretrained transformers as universal computation engines." arXiv preprint arXiv:2103.05247 (2021).](https://arxiv.org/pdf/2103.05247.pdf)[![citation](https://img.shields.io/badge/dynamic/json?label=citation&query=citationCount&url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F3544650f12a05cf4ed3bf2f7e22fc5c02fcabf50%3Ffields%3DcitationCount)](https://www.semanticscholar.org/paper/Pretrained-Transformers-as-Universal-Computation-Lu-Grover/3544650f12a05cf4ed3bf2f7e22fc5c02fcabf50)


# Scaling transformers

## 💤 Switch Transformers
- [Fedus, William, Barret Zoph, and Noam Shazeer. "Switch transformers: Scaling to trillion parameter models with simple and efficient sparsity." (2021).](https://arxiv.org/abs/2101.03961)[![citation](https://img.shields.io/badge/dynamic/json?label=citation&query=citationCount&url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2Ffdacf2a732f55befdc410ea927091cad3b791f13%3Ffields%3DcitationCount)](https://www.semanticscholar.org/paper/Switch-Transformers%3A-Scaling-to-Trillion-Parameter-Fedus-Zoph/fdacf2a732f55befdc410ea927091cad3b791f13)

## 💤 ST-MoE
- [Zoph, Barret et al. “ST-MoE: Designing Stable and Transferable Sparse Expert Models.” (2022).](https://arxiv.org/abs/2202.08906)[![citation](https://img.shields.io/badge/dynamic/json?label=citation&query=citationCount&url=https%3A%2F%2Fapi.semanticscholar.org%2Fgraph%2Fv1%2Fpaper%2F1bc9865ebf52b59abac7f5ee4456ff2ac37fcff3%3Ffields%3DcitationCount)](https://www.semanticscholar.org/paper/ST-MoE%3A-Designing-Stable-and-Transferable-Sparse-Zoph-Bello/1bc9865ebf52b59abac7f5ee4456ff2ac37fcff3)
