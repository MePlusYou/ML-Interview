# ML-Interview
机器学习面试问题总结
2018年准备找工作了，决心总结一下，问题都是网上的资源和自己面试遇到的。
## 什么是boosting tree
## GBDT
GBDT(Gradient Boosting Decision Tree) 又叫 MART（Multiple Additive Regression Tree)，是一种迭代的决策树算法，该算法由多棵决策树组成，所有树的结论累加起来做最终答案。它在被提出之初就和SVM一起被认为是泛化能力较强的算法。

## L1和L2正则为何可以减弱over-fitting?
目标函数 = loss + 正则
loss = 0 过拟合
## L1和L2正则有什么区别
相同点：都用于避免过拟合

不同点：
L1可以让一部分特征的系数缩小到0，从而间接实现特征选择。所以L1适用于特征之间有关联的情况。

L2让所有特征的系数都缩小，但是不会减为0，它会使优化求解稳定快速。所以L2适用于特征之间没有关联的情况

## KNN和LR有什么本质区别
## 怎么理解Dropout
## 为什么random forest具有特征选择的功能
## random forest有哪些重要的参数？
## DNN为什么功能强大，说说你的理解
## SVM的损失函数是什么？怎么理解
2分类SVM等于Hinge损失 + L2正则化。

## 介绍下Maxout
## 项目中over-fitting了，你怎么办
1. regularization：L2用的最多，L1也有用的。
2. dropout：一大利器。
3. early stop：结合cross validation使用。
4. cross validation：当数据量较小的时候，应该是用来减轻 overfitting 最好的方式了吧。
5. 当然，尽可能的扩大 training dataset 才是王道。
6. 在训练之前记得 shuffle 一下数据集，一般是每次训练一个 epoch（就是把 training dataset 训练了一遍）后就 shuffle 一次，但是对于较大的数据集可以只 shuffle 一次，虽然这样会使得训练在第二个 epoch 就变得 biased，但是带来的好处可以 overcome 这种缺陷。

作者：小华仔
链接：https://www.zhihu.com/question/26898675/answer/151101888
来源：知乎
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
## 详细说一个你知道的优化算法(Adam等)
## 项目(比赛）怎么做的模型的ensemble
https://www.leiphone.com/news/201710/YoMbUNqRlasrpgle.html

常见的Ensemble方法有Bagging、Boosting、Stacking、Blending。
1.6.1 Bagging

Bagging是将多个模型（基学习器）的预测结果简单地加权平均或者投票。Bagging的好处在于可以并行地训练基学习器，其中Random Forest就用到了Bagging的思想。

1.6.2 Boosting

Boosting的思想有点像知错能改，每训练一个基学习器，是为了弥补上一个基学习器所犯的错误。其中著名的算法有AdaBoost，Gradient Boost。Gradient Boost Tree就用到了这种思想。

1.6.3 Stacking

Stacking是用新的模型（次学习器）去学习怎么组合那些基学习器，它的思想源自于Stacked Generalization（http://www.machine-learning.martinsewell.com/ensembles/stacking/Wolpert1992.pdf）这篇论文。如果把Bagging看作是多个基分类器的线性组合，那么Stacking就是多个基分类器的非线性组合。Stacking可以很灵活，它可以将学习器一层一层地堆砌起来，形成一个网状的结构，如下图：

1.6.4 Blending

Blending与Stacking很类似，它们的区别可以参考这里（https://mlwave.com/kaggle-ensembling-guide/）

## stacking是什么？需要注意哪些问题
## 了解哪些online learning的算法
## 如何解决样本不均衡的问题
## fasterRCNN中的ROIPooling是如何实现的
## 如何进行特征的选择
## 如何进行模型的选择
## 什么是梯度消失？怎么解决
## 常用的有哪些损失函数
## XX用户画像挖掘怎么做的feature engineering?
## 假设一个5*5的filter与图像卷积，如何降低计算量？
## 做过模型压缩吗？介绍下
## 什么是residual learning？说说你的理解
## residual learning所说的residual和GBDT中的residual有什么区别？
## FFM和FTRL有过了解吗？
## 你对现在Deep Learning的发展和遇到的问题有什么看法？