#### Thinking1	XGBoost与GBDT的区别是什么？
- XGboost跟GBDT 都是基于决策树的集成模型, 使用损失函数的负梯度作为残差近似值进行迭代.
- XGboost是在GBDT的基础上, 损失函数加上了正则(泰勒展开, 二阶导), 比GBDT(只用了一阶泰勒)有更强的泛化能力, 能够更有效地防止过拟合.
- XGboost采用了分bucket的方式, 采用了'贪心算法', 对只在边界上的特征作为节点的候选, 性能优于GBDT
- XGBoost采用基于特征计算的并行, 将特征排序后以block的形式储存在内存中, 在后面可以复用. 在进行节点分列时,使用多线程并行方式进行特征的增益计算, 并选择增益最大的特征作为分割节点. 
- XGboost也有缺点, 就是参数过多, 调参比较复杂, 不是和处理超高纬特征数据


#### Thinking2	举一个你之前做过的预测例子（用的什么模型，解决什么问题，比如我用LR模型，对员工离职进行了预测，效果如何... 请分享到课程微信群中）


#### Thinking3	请你思考，在你的工作中，需要构建哪些特征（比如用户画像，item特征...），这些特征都包括哪些维度（鼓励分享到微信群中，进行交流）

- T2 与 T3 一并回答.
- 使用过LR模型对违约用户进行是否违约进行预测, 以便解决在用户申请贷款时能够识别用户未来是否会违约, 对于模型的评估采用AUC分数. AUC效果0.7左右, 中等水平.主要是在用户特征工程上还有很大的提升空间.
- 用户的特征, 分了几大类别: 1)用户基础属性(年龄, 性别, 婚姻状况, 住址, 工作, 学历等), 2) 用户历史借贷行为(借贷次数, 借贷产品, 违约次数, 最大逾期天数等), 3) 用户使用app行为和设备信息(登录时间, 设备, 登录ip, 等app操作数据) , 4) 衍生数据(在2 和3的基础上, 计算的统计数据, 如申请前1,3,7,30的借款行为)
- 特征非常多, 通常使用开源toad包先对特征进行筛选(缺失率, 相关性, iv值), 最终入模的特征不超过20个.这里的iv值是指特征对目标的信息值, iv值越高, 该特征对目标的区分度越高.
- 关于特征的评估, 除了iv值, 也使用过XGBoost的特征重要性, 以及SHAP值.