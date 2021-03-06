# 基于交替方向乘子法的分布式优化和统计学习
这个是对 Stephen Boyd 教授2011年发表的关于ADMM的文章的中文翻译和Python实现。本人才疏学浅，有不足之处请各位指正！仅供学术交流之用。随缘更新～

英文原文链接：[https://web.stanford.edu/~boyd/papers/pdf/admm_distr_stats.pdf]

## 摘要
目前许多在统计和机器学习领域的问题可以落实到凸优化的框架里。由于现代数据集的规模和复杂度的爆炸式增长，通过大量特征和训练样本来解决问题的需求日益凸显。因此，通过去中心化的方式收集或者存储这些数据集和使用分布式的方法去解决问题，是必要的，或者至少是非常需要的。在这篇综述中，我们认为交替方向乘子法 (ADMM) 适合于解决分布式凸优化，特别是用于解决统计、机器学习和其它相关领域里的大规模问题。ADMM 在1970年代得到了发展，其起源于1950年代，并且它与许多其它算法相同或者接近，比如说：对偶上升法、乘子法、Douglas–Rachford 分裂法、Spingarn偏逆法、Dykstra交替推理法、针对L_1问题的Bregman迭代算法、近邻法等。在简要的介绍了ADMM的理论和发展历程后，我们讨论它在统计和机器学习领域的广泛应用，包括LASSO、稀疏逻辑回归、基追踪、协方差选择、SVM等。我们也讨论了分布式优化在非凸情形和性能提升方面的应用，包括分布式MPI、Hadoop和MapReduce的应用细节。

## 简介


