# Rotation Equivariant Siamese Networks for Tracking

Deepak K. Gupta, Devanshu Arya, Efstratios Gavves. 阿姆斯特丹大学； [pdf](https://arxiv.org/abs/2012.13078) [github](https://github.com/dkgupta90/re-siamnet) 

旋转是跟踪任务中长期流行但还未解决且难度很高的挑战，当前基于深度学习的跟踪器使用regular CNNs难以应对目标旋转问题。作者提出rotation-equivariant Siamese networks来解决跟踪中目标的旋转挑战。

PS：regular CNNs能够解决平移不变性，作者要解决的是旋转不变性

SiamNets：

* 能够用一种无监督的方式估计目标的朝向变化 -> 促进在2D pose estimation任务中的使用
* 通过对两帧之间朝向变化的限制，对跟踪施加额外的运动约束
* 使用到的方法：group-equivariant convolutional layers comprising steerable filter

