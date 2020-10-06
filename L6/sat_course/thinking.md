### Thinking1	什么是近似最近邻查找，常用的方法有哪些
- 最近邻查找Nearest Neighbor分为 KNN (查找离目标数据最近的k个数据项) 和 ANN( 近似最近邻居检索); 相对KNN, ANN是指在牺牲可接受范围内的经度的情况下提高检索效率. 处理大规模数据时可以采用
- 常用方法: 
    - MinHash 最小哈希值 , 进行降维
    - LSH 局部敏感哈希, 进行分桶,通过索引方式查找
    - MinHashLSHForest : 与MinHash+ LSH相似, 把数据结构按照树的结构存储
    - MinHashLSHEnsemble: 大的集合会导致并集过大, jaccard过小, MinHashLSHEnsemble对大集合进行惩罚,通过containment的化简方式.并集只取集合本身. 


### Thinking2	为什么两个集合的minhash值相同的概率等于这两个集合的Jaccard相似度
- Jaccard相似度的计算公式是交比并(IOU), 分子是交集的数量, 分母是并集的数量
- 两个集合的minhash值, 是指对两个集合相等的概率, 这个概率是等同于两列的值都为1 除以 两列至少有一个值等于1, 公式近似于同于交集比并集.
- minHash值主要用于降维, 在维度相差比较多的情况下, 信息会有损失, 所以两个值的minHash值并不一定等同于Jaccard相似度, 只是一个近似度.




### Thinking3	SimHash在计算文档相似度的作用是怎样的？
- SimHash是LSH的一种, 通过SimHash算法得到每篇文档的指纹, 并计算两两文档之间的汉明距离
- 对汉明距离小于3的文档, 曾两篇文档的相似度比较高.通常适用于长文本


### Thinking4	为什么YouTube采用期望观看时间作为评估指标
- 主要是从商业的角度考虑, Youtube是视频公司, 盈利模式是通过在播放视频时插入广告. 
- 用户观看时间越长, 可插播广告的时间就越长.





