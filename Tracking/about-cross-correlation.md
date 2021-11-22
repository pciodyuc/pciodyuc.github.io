PG-Net: Pixel to Global Matching Network for Visual Tracking 
* ECCV2020

- - 动机：siamese-based      tracker中使用了similarity matching （cross correlation），该方法无法抑制背景信息 surpress the      influence of background，因此得到的解决不精确

  - 解决方案：replace the cross      correlation with Pixel to Global matching correlation (PG-corr)

  - - reduce the match region by       decomposing the template feature into spatial and channel kernels with       size of 1 × 1

 

Transformer Tracking CVPR2021

- - 动机：Cross correlation      太简单，只是个局部线性匹配器，且没有利用global context（容易陷入局部最优），丢失了语义信息

  - 解决方案：使用Transformer-like      fusion，该部分包括

  - - Ego-context augment module       based on self-attention
    - Cross-feature augment module       based on cross-attention

  - 50 fps
