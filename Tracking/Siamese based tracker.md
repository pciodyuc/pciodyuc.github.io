# Siamese based tracker

### feature extractor

* DSiam 采用online learning modules 解决目标表观变化和背景抑制转换，来改进特征表示
* SA-Siam 分别训练语义分支和表观分支，在测试阶段进行联合（相辅相成）
* RASNet 引入空间和通道attention来提高深度模型的判别能力
* GCT 采用时空GCN进行目标建模
* DaSiamRPN 设计了一个distractor-aware module 来实现incremental learning，并得到更具判别性的特征来应对semantic distractors
* SiamRPN++ 和 SiamDW 设计使用更深的网络来改进跟踪性能

### similarity matching



### tracking head

1. SiamFC, ==cross-correlation-layer==
2. SiamRPN，==up-channel cross-correlation-layer==. 添加两个分支，one classification branch for background-foreground classification of anchors, one regression branch for proposal refinement
3. SiamRPN++， ==Depth-wise cross correlation (DW-Xcorr)==, a channel-by-channel correlation operation, 解决两个分支参数不平衡问题，使得训练过程更稳定，以及信息联合更有效？
4. PG-Net，==PG-correlation==， 传统cross-correlation operation 带来much backgroun information, 这可能会淹没目标特征，造成对相似distractors敏感，提出了pixel-to-global matching method来抑制背景的干扰， 依旧使用fixed-scale cropped region as the template feature
5. SiamGAT, 提出target-aware graph attention tracker, 从target template到search region有效的信息传播，[笔记](..\Tracking\papers\Graph-Attention-Tracking.md)
6. 

### 数据不平衡

* C-RPN 级联RPNs的序列，容易的负样本在早期阶段被过滤掉，hard samples are preserved across stages

### 基于RPN

缺点：对anchor的超参敏感

* SiamRPN
* SiamRPN++ 和 SiamDW
* C-RPN

### anchor-free（消除anchor的负面影响）

* SiamFC++
* SiamCAR
* SiamBAN
* Ocean

### Online

* Ocean 使用一个online-updating module 来动态适应跟踪器

