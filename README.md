# Chinese-Product-Review-Summary-Datasets
包括基于[懂车帝网站](https://www.dongchedi.com/)用户评论构建的Product-CSum数据集，以及基于公开ACSA数据集构建的Product-CSum-Cross数据集。

## Product-CSum
基于对懂车帝网站车友圈板块中不同车型的热门评论与精选评论进行标注得到。

**数据字段**
- Name：汽车名称
- Text：单条评论或多条评论（用‘|||’分隔）
- Summary_list：针对该text的归纳
- Summary_num：归纳数量

|        | Num. of text | Num. of Summary |
| ------ | ------------ | --------------- |
| 汽车(train)   | 1863         | 10313            |
| 汽车(test)   | 1800         | 1808            |

## Product-CSum-Cross

共包含化妆品、汽车、餐厅三个品类。其中，化妆品类别数据基于[之江杯2019-电商评论观点挖掘数据集](https://github.com/xmxoxo/Text-Opinion-Mining)进行标注，汽车类别数据基于[汽车行业用户观点主题及情感识别数据集](https://www.datafountain.cn/competitions/310/datasets)进行标注得到，餐厅类别数据基于ASAP数据集[<sup>1</sup>](#refer-anchor-1)进行标注得到。

**数据字段**

- Name：商品品类
- Text：单条评论或多条评论（用‘|||’分隔）
- Aspects：用gpt3.5-turbo对text抽取得到的“角度-极性-对应句子”
- Summary_list：针对该text的归纳
- Summary_num：归纳数量

**统计**

|        | Num. of text | Num. of Summary |
| ------ | ------------ | --------------- |
| 化妆品 | 1287         | 4786            |
| 汽车   | 1142         | 4969            |
| 餐厅   | 831          | 3530            |

## Reference
<div id="refer-anchor-1"></div>
- [1] Bu, J., Ren, L., Zheng, S., Yang, Y., Wang, J., Zhang, F. and Wu, W., 2021. ASAP: A chinese review dataset towards aspect category sentiment analysis and rating prediction. arXiv preprint arXiv:2103.06605.
