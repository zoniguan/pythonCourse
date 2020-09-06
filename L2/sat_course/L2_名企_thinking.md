## L2-2 Thinking  
  
### Thinking 1 : MVC框架指的是什么

 
全称Model View Controller, 是用一种业务逻辑\数据\界面显示分离的方法组织代码. 将业务逻辑聚集到一个部件里面，在改进和个性化定制界面及用户交互的同时，不需要重新编写业务逻辑. 比如一批统计数据可以分别用柱状图、饼图来表示。C存在的目的则是确保M和V的同步，一旦M改变，V应该同步更.
 

### Thinking 2 : 基于Python的可视化技术都有哪些，你使用过哪些

- 可视化技术有matlabplot, seaborn, grphviz, echarts, pyecharts, Flash等
- 使用过matlabplot 和seaborn
- 主要用于以下几种情况
    - 数据EDA时快速看到数据的分布情况(柱状图),变量关系(散点图)
    - 对时间序列数据多用线形图看趋势
    - 也用于机器学习时对模型进行可视化效果(如聚类通过绘制轮廓系数值,选择最优k值)
