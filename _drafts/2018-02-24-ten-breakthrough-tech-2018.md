---
layout: post
title:  "2018突破性技术top10: (1)对抗神经网络"
date:   2018-02-24 20:37:00 +0800
if_home: True
tags: ['report', 'machine learning']
author: "LIU Wang-Sheng"
---

> 近日，MIT technology review 评选了2018突破性技术top10，其中伊恩.“好人”(Ian Goodfellow)的对抗神经网络不出意外地入选。虽然目前对抗神经网络并未被广泛地使用，但是可以预见到，一旦这个技术被商业化，将极大地改变（但愿往好的方向）我们的生活。

# 神经网络的“决斗”
现在，训练好的神经网络已经具有极强的预测和识别能力，很多方面超越人类。但是所有神经网络必须基于实际世界中采集的数据进行训练，整个产生数据的过程费时费力。那么可不可以让网络自己产生数据呢？脑洞大开的Ian在一次酒吧学术讨论中提出对抗神经网络（Generative adversarial network,GAN）。想到当时Ian还是在读博士生，不禁让人汗颜。

基本思路是对同一个数据集训练两个神经网络。第一个网络是生成器，用来对已有图片添加扰动来生成更多新的图片；第二个是判别器，来鉴别一张图片是真实世界中采集的还是由生成器生成的。两个网络进行决斗，最终使生成器生成的图片不能被判别器识别。

这个技术让人细思极恐。之前说到神经网络的图片识别能力很多方面已经超越人类，如果生成器生成的“机器”图片能糊弄判别器，那就意味着完全能骗过人类的眼睛。除了图片，GAN还可以用到视频、语音等其他领域。某种程度上，神经网络具备一定的想象力，拥有了创造的能力。

# 见招拆招
这节详细简要介绍GAN的训练过程，详细版本可以参考Ian在NIPS2016上的[tutorial](https://arxiv.org/pdf/1701.00160.pdf)。

# GAN就在我们身边
识别不了

# 一个示例



<!-- more -->