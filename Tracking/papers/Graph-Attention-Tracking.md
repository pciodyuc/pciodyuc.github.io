# **Graph Attention Tracking**. 

* Dongyan Guo, Yanyan Shao, Ying Cui, Zhenhua Wang, Liyan Zhang, ==Chunhua Shen==.

* 浙江工业大学；南京航空航天大学；

* 阿德莱德大学. 

* [pdf](https://arxiv.org/abs/2011.11204) [github](https://github.com/ohhhyeahhh/SiamGAT)

Siamese-based trackers 通过convolutional feature cross-correlation进行相似性学习，其中target feature region需要预先固定，所以这种cross-correlation方法有以下缺点：

1. 保存有很多不利的（adverse）背景信息
2. 丢失了大量前景信息
3. 目标被作为一个整体，当目标产生较大的旋转、姿势变化以及遭遇严重遮挡时，这种global matching是不鲁棒的
4. global matching 极大的忽略了目标结构和层级信息

作者提出target-aware Siamese graph attention network来解决以上信息：

1. 使用target-aware area selection mechanism固定不同目标的大小和表观比，从而替代pre-fixed region cropping

2. 学习part-level relations
   1. 通过a complete bipartite graph构建目标和搜索区域part-to-part 的对应关系
   2. 使用graph attention mechanism将target信息从template传播给search region



