# Siamese based tracker

### feature extractor

* DSiam 采用online learning modules 解决目标表观变化和背景抑制转换，来改进特征表示
* SA-Siam 分别训练语义分支和表观分支，在测试阶段进行联合（相辅相成）
* RASNet 引入空间和通道attention来提高深度模型的判别能力
* GCT 采用时空GCN进行目标建模

### similarity matching



### tracking head

1. SiamFC, cross-correlation-layer
2. SiamRPN，up-channel cross-correlation-layer. 添加两个分支，one classification branch for background-foreground classification of anchors, one regression branch for proposal refinement
3. 

