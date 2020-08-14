# Analysis-and-prediction-of-hotel-bookings-dataset

Hotel bookings dataset 来源于( https://www.kaggle.com/jessemostipak/hotel-booking-demand )。该数据最初摘自Nuno Antonio，Ana Almeida和Luis Nunes为2019年2月第22卷的数据简介撰写的酒店预订需求数据集( https://www.sciencedirect.com/science/article/pii/S2352340918315191 )。现已由 Thomas Mock 和 Antoine Bichat 在2020年2月11日下载清理并发布(https://github.com/rfordatascience/tidytuesday/blob/master/data/2020/2020-02-11/readme.md)。

该数据集具体包含两个不同酒店（度假酒店和城市酒店）在预订到达日期之前的数据，其中包括一家度假酒店和一家城市酒店。具体变量包括诸如预订的时间、停留时间、成人、儿童或婴儿的数量以及可用停车位的数量等信息，总计36个。

本项目的工作主要为两个部分，第一是基于该数据集进行探索性数据分析（EDA），进而挖掘出数据集包含的一些潜在信息；第二是基于因变量（is_canceled）建立一个有效的模型来预测客人是否真的会来，为酒店具体营业计划的制定提供一些支撑。


## 1.探索性数据分析

对数据集以及相关变量的具体分析，我希望能够解决以下问题：

 - 客人来自哪里，其年龄组成是怎么样的？
 
 - 客人平均预订多少时间，具体分布？
 
 - 通过meal分析客人对于服务的需求？
 
 - 一年中房价如何变化，客人每晚为一间客房支付多少费用？
 
 - 一年中哪个月最忙，或者哪个时间段最忙？
 
 - 人们在酒店平均停留多长时间，两个酒店各自的平均停留时长？
 
 - 预订的取消主要来自于哪个时间段，哪个酒店的取消情况更少？
 
 - 客人预订的入住时间主要是周几？
 
 - 客户提出的特殊要求的数量对取消预订的影响？
 
 - 来自公司的预订有多少，哪家公司是高质量客户（订单多且取消少）

首先，我们需要载入数据集并看一下其具体的大小以及是否需要补缺。

### 1.1 数据预处理



看起来需要对孩子、国家、代理机构和公司进行补充缺失值  

此外，根据Nuno Antonio等对该数据的[补充说明](https://www.sciencedirect.com/science/article/pii/S2352340918315191)，我们可以得知meal变量中的属性Undefined和SC均指无餐套餐。

