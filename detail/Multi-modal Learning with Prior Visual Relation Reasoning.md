## Abstract  

In this work, we explore to model relations by contextual-sensitive embeddings based on human priori knowledge. We novelly propose a plug-and-play relation reasoning module injected with the relation embeddings to enhance image encoder. Specifically, we design upgraded Graph Convolutional Networks (GCN) to utilize the information of relation embeddings and relation directionality between objects for generating relation-aware image representations.

## Detail 

### 1 先用一个简单的网络产生场景图  

![捕获](./Multi-modalLearningwithPriorVisualRelationReasoning.assets/捕获.PNG)

###  2  Anisotropic Graph Convolution(AGConv) 

名字比较高大上，其实就是mutil-head的self-attention机制 

![2](Multi-modal Learning with Prior Visual Relation Reasoning.assets/2-1556350552688.PNG)

对应公式，$||$ 表示拼接，$h_{j}^{l}$表示第$j$个物体，$l$层的特征

![3](C:/Users/ww/Desktop/3.PNG)

![4](Multi-modal Learning with Prior Visual Relation Reasoning.assets/4.PNG)

### 3 类似于 Botton-up,top-down类似的结构进行VQA  

![5](Multi-modal Learning with Prior Visual Relation Reasoning.assets/5.PNG)

Cross-wise product的公式是： 

![6](Multi-modal Learning with Prior Visual Relation Reasoning.assets/6.PNG)

然后进行权重和，最后预测：

![7](Multi-modal Learning with Prior Visual Relation Reasoning.assets/7.PNG)

