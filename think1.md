### 1.电商定向广告和搜索广告有怎样的区别，算法模型是否有差别
答：定向广告没有用户的动作行为作为参考。
搜索广告把用户输入的信息作为主要的参考信息。
算法模型上，定向广告更多的是考虑用户的隐性动作特征，比如说他的点击，搜索广告更多的考虑显性动作特征。

### 2.定向广告都有哪些常见的使用模型，包括Attention机制模型
答：定向广告的常模型：LR, MLR, DNN,DIN, DIEN, DSIN
其中DIN, DIEN, DSIN是基于Attention机制进行embedding.
### 3.DIN中的Attention机制思想和原理是怎样的
答：DIN中的Attetion是为了解决用户兴趣多样性，用户浏览过的相关商品对于预测帮助更大的问题。
它对用户行为进行embedding引入attention network,对每个兴趣表示赋予不同的权值。
### 4.DIEN相比于DIN有哪些创新
答：DIEN的出现是为了解决DIN的不足，主要是DIN把历史行为当做兴趣，没有考虑当时时刻的兴趣对下一个行为的影响。
DIEN引入AUGRU序列模型，对用户兴趣进化的过程进行建模，在 Embedding layer 和 Concatenate layer 之间加入了生成兴趣的 Interest Extractor Layer 和模拟兴趣演化的 Interest Evolving layer

#### 5.DSIN关于Session的洞察是怎样的，如何对Session兴趣进行表达
答：DSIN是为了解决DIEN中的不中，DIEN忽视了用户行为序列会话。
DSIN以每前后时间30min作为一个sesion，对用户的点击行为按照时间排序。
对每个Session再进行DSIN中的操作，可以做到并行。
#### 6.如果你来设计淘宝定向广告，会有哪些future work（即下一个阶段的idea）
答：Furture work有如下几个方面：
在冷启动的问题上，可以做到以user type为基础去给新用户进行推荐，做到千人10面。
是否能结合用户的更多的环境因素，进行推荐，比如用户的生活环境，工作环境等。

