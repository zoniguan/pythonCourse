Thinking1	今天讲解了时间序列预测的两种方式，实际上在数据库内建时间属性后，可以产生时序数据库，请思考什么是时序数据库？为什么时间序列数据成为增长最快的数据类型之一
- 时序数据是基于时间的一系列的数据。在有时间的坐标中将这些数据点连成线，往过去看可以做成多纬度报表，揭示其趋势性、规律性、异常性；往未来看可以做大数据分析，机器学习，实现预测和预警; 在互联网,物联网兴起的推动下, 时间序列数据的应用和场景激增, 所以时间序列数据成为增长最快的数据类型之一.
- 时序数据库就是存放时序数据的数据库，并且需要支持时序数据的快速写入、持久化、多纬度的聚合查询等基本功能, 在时序数据写入/查询/数据压缩方面有巨大的优势，能够解决许多用户痛点.



Thinking2	BCG Matrix（波士顿矩阵）四象限分别代表什么？不同象限，有怎样的数据决策
- 四象限代表: 
    - 明星类产品, 即销售增长和市场占有率都高的产品群
    - 瘦狗类产品, 即销售增长和市场占有率都低的产品群
    - 问题类产品, 即销售增长高,市场占有率低的产品群
    - 金牛类产品, 即销售增长低,市场占有率高的产品群
- 数据决策
    - 对于明星类产品, 需要加大投资力度, 来支持产品的快速发展, 如扩大市场规模, 加强竞争地位
    - 对于金牛类产品, 已经进入成熟期, 增长率低,无需加大投资. 反而尽量压缩这类产品的投资, 尽快回收资金, 作为明星产品的后盾. 但如果企业只有一个金牛类产品, 还是比较脆弱, 如果市场情况发生变化导致份额降低, 金牛类产品有可能会转变为瘦狗类产品.
    - 对于问题类产品, 销售高但占有率低, 证明市场销售商存在一定的问题, 需要对问题类产品进行改进, 需要引入选择性投资战略. 
    - 对于瘦狗类产品,属于衰退型产品, 无法为企业带来收益, 应该采取撤退战略. 并将资源向其他类产品转移. 
