# 《统计学习方法》

> 以《统计学习方法》(李航)的内容为基础，综合了《机器学习》(周志华)、《机器学习基石》和《机器学习技法》(林轩田)等内容，并从零实现了部分算法的代码，同时也有相关模型在Scikit-Learn中的使用介绍。

## [第1章-统计学习方法概论](https://github.com/LobbyBoy-Dray/Statistical-Learning-LiHang/blob/master/%E7%AC%AC1%E7%AB%A0-%E7%BB%9F%E8%AE%A1%E5%AD%A6%E4%B9%A0%E6%96%B9%E6%B3%95%E6%A6%82%E8%AE%BA.ipynb) 

## [第2章-感知器](https://github.com/LobbyBoy-Dray/Statistical-Learning-LiHang/blob/master/%E7%AC%AC2%E7%AB%A0-%E6%84%9F%E7%9F%A5%E5%99%A8.ipynb)

## [第3章-k近邻法](https://github.com/LobbyBoy-Dray/Statistical-Learning-LiHang/blob/master/%E7%AC%AC3%E7%AB%A0-k%E8%BF%91%E9%82%BB%E6%B3%95.ipynb)

## [第4章-朴素贝叶斯法](https://github.com/LobbyBoy-Dray/Statistical-Learning-LiHang/blob/master/%E7%AC%AC4%E7%AB%A0-%E6%9C%B4%E7%B4%A0%E8%B4%9D%E5%8F%B6%E6%96%AF%E6%B3%95.ipynb)

## [第5章-决策树](https://github.com/LobbyBoy-Dray/Statistical-Learning-LiHang/blob/master/%E7%AC%AC5%E7%AB%A0-%E5%86%B3%E7%AD%96%E6%A0%91.ipynb)

## 第6章-Logistic回归&最大熵模型

## [第7章-支持向量机](https://github.com/LobbyBoy-Dray/Statistical-Learning-LiHang/blob/master/%E7%AC%AC7%E7%AB%A0-%E6%94%AF%E6%8C%81%E5%90%91%E9%87%8F%E6%9C%BA.ipynb)

一. 线性可分支持向量机与硬间隔最大化

* 从训练数据集线性可分的假设开始，引出支持向量机的概念——最大间隔的线性分类器；
* 定义了函数间隔与几何间隔，并推导出Hard-margin SVM的primal问题；
* 支持向量的含义：一部分位于边界上的点，决定着分离平面的位置；
* 推导对偶问题(Standard hard-margin SVM dual)，对支持向量的再理解；

二. 线性支持向量机与软间隔最大化

* 取消训练数据集线性可分的假设，对原Hard-margin的primal做出初步修正(林轩田)；
* 引入松弛变量，得到被标准的软间隔最大化的primal问题，即线性SVM；
* Soft-margin SVM dual的推导，重点关注KKT条件；
* 支持向量的再理解：Free SV和Bounded SV(林轩田)；
* Soft-margin primal经过变形，等价于合页损失函数+L2正则化；

三. 非线性支持向量机与核函数(林轩田)

* 使用核技巧的动机；
* Kernel Function = Non-linear transformation+Inner product；
* 多项式核与高斯核；
* 核函数的充要条件：Mercer's conditions，对称函数与半正定矩阵；

四. 序列最小最优化算法(SMO)

* 训练样本的容量非常大时，用QP程式解dual也很慢；
* 利用KKT条件，开发专门解决SVM二次规划的算法；
* SMO要解决的是Soft-margin svm dual：
  * 选择两个变量，一个是违反KKT条件最严重的那一个，另一个由约束条件自动确定；
  * 固定其他变量，解针对上述两个变量的子二次规划问题；
  * 直到所有alpha都满足KKT条件。
