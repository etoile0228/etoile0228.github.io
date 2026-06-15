---
title: "My 1st post"
date: 2026-06-15T19:10:19+08:00
# weight: 1
# aliases: ["/first"]
categories: ["first"]
tags: ["first"]
author: "Etoile"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Desc Text."
canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: true # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/<path_to_repo>/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

## 项目概览

- 项目领域：电商
- 技术关键词：母婴电商, 用户分析, pyecharts, 消费行为
- 项目简介：母婴消费有很强的生命周期属性，宝宝年龄、家庭阶段和品类需求密切相关。理解用户所处阶段，比单纯推荐热销商品更重要。

## 学习目标

- 练习从业务背景出发提出可分析的问题，而不是只运行代码。
- 熟悉 用户与交易表关联、消费频次分析、品类分析、pyecharts 可视化。
- 通过图表、指标和模型结果总结业务现象，并形成自己的理解。
- 将 notebook、图表和代码整理成可复盘、可展示的作品。

## 数据与方法

- 数据概况：天池母婴消费样本数据，包含用户、婴儿信息、商品类别和交易记录。
- 技术路线：用户与交易表关联、消费频次分析、品类分析、pyecharts 可视化。

## 分析过程与思路

- 先梳理展示对象和受众：判断这篇分析主要给业务、管理层还是面试官阅读。
- 根据问题选择图表：趋势看折线，结构看占比，对比看柱状图，空间分布看地图。
- 先用 pandas 聚合出清晰指标，再用可视化表达核心结论。
- 按照故事线组织图表顺序，避免图很多但结论分散。
- 每张图都配业务解释，让读者知道图表对应什么判断和行动。

## 核心发现

- 母婴用户的需求随宝宝成长快速变化，纸尿裤、喂养、玩具和服饰的购买节奏不同。
- 用户复购价值高，但信任成本也高，商品质量和售后体验会影响长期留存。
- 品类交叉购买可以帮助识别家庭阶段，并用于下一阶段商品推荐。

## 我的业务理解

这个项目的重点不是单纯把数据做成图，而是借助数据理解一个具体场景。整理文章时，我把代码执行过程、图表输出和业务解释放在同一篇文章里，方便以后回看自己当时的分析路径，也能作为个人数据分析作品集的一部分展示。

## 业务建议

- 平台可按宝宝月龄构建生命周期运营脚本，提前推送下一阶段刚需商品。
- 对高频刚需品类可设计订阅购或周期购，提高复购稳定性。
- 后续可引入 RFM、优惠敏感度和商品评价，构建更完整的母婴用户分层。

## 项目复盘

- 亮点：项目不是单纯展示代码，而是从业务问题出发，能体现分析链路完整性。
- 不足：部分数据来自公开或学习数据集，缺少真实业务中的成本、实验和线上反馈。
- 优化：可以把 notebook 拆成数据清洗、特征工程、建模评估和可视化脚本，并补充 README、环境依赖和图表截图。

## 完整分析代码与输出图片

下面内容按原 notebook 的代码单元顺序整理。代码完整保留；如果 notebook 输出中包含 PNG 图表，也会导出为图片并嵌入文章。为了保证文章前半部分更适合阅读，完整代码默认放在折叠区。

<details>
<summary>展开查看完整 notebook 代码和输出图片</summary>


### 代码单元 1

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import pyecharts.charts as pyc
import pyecharts.options as opts
import warnings
from datetime import datetime
warnings.filterwarnings("ignore")
plt.rcParams['font.sans-serif'] = ['Microsoft YaHei']
plt.rcParams['axes.unicode_minus'] = False
# 作图的字体默认设置
fontdict = {'fontsize': 15,
            'horizontalalignment': 'center'}
```

### 代码单元 2

```python
baby = pd.read_csv("./(sample)sam_tianchi_mum_baby.csv")
trade = pd.read_csv("./(sample)sam_tianchi_mum_baby_trade_history.csv")
```

### 代码单元 3

```python
baby.head()
```

**文本输出**

```text
user_id  birthday  gender
0      2757  20130311       1
1    415971  20121111       0
2   1372572  20120130       1
3  10339332  20110910       0
4  10642245  20130213       0
```

### 代码单元 4

```python
trade.head()
```

**文本输出**

```text
user_id   auction_id    cat_id      cat1  \
0  786295544  41098319944  50014866  50022520   
1  532110457  17916191097  50011993        28   
2  249013725  21896936223  50012461  50014815   
3  917056007  12515996043  50018831  50014815   
4  444069173  20487688075  50013636  50008168   

                                            property  buy_mount       day  
0  21458:86755362;13023209:3593274;10984217:21985...          2  20140919  
1  21458:11399317;1628862:3251296;21475:137325;16...          1  20131011  
2  21458:30992;1628665:92012;1628665:3233938;1628...          1  20131011  
3  21458:15841995;21956:3494076;27000458:59723383...          2  20141023  
4  21458:30992;13658074:3323064;1628665:3233941;1...          1  20141103
```

### 代码单元 5

```python
baby.info()
```

**文本输出**

```text
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 953 entries, 0 to 952
Data columns (total 3 columns):
 #   Column    Non-Null Count  Dtype
---  ------    --------------  -----
 0   user_id   953 non-null    int64
 1   birthday  953 non-null    int64
 2   gender    953 non-null    int64
dtypes: int64(3)
memory usage: 22.5 KB
```

### 代码单元 6

```python
trade.info()
```

**文本输出**

```text
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 29971 entries, 0 to 29970
Data columns (total 7 columns):
 #   Column      Non-Null Count  Dtype 
---  ------      --------------  ----- 
 0   user_id     29971 non-null  int64 
 1   auction_id  29971 non-null  int64 
 2   cat_id      29971 non-null  int64 
 3   cat1        29971 non-null  int64 
 4   property    29827 non-null  object
 5   buy_mount   29971 non-null  int64 
 6   day         29971 non-null  int64 
dtypes: int64(6), object(1)
memory usage: 1.6+ MB
```

### 代码单元 7

```python
trade.buy_mount.describe()
```

**文本输出**

```text
count    29971.000000
mean         2.544126
std         63.986879
min          1.000000
25%          1.000000
50%          1.000000
75%          1.000000
max      10000.000000
Name: buy_mount, dtype: float64
```

### 代码单元 8

```python
quantity = trade.buy_mount.value_counts().sort_index()
plt.figure(figsize=(10, 8))
sns.scatterplot(x=quantity.index, y=quantity.values, alpha=0.3)
plt.title("单个订单购买量分布", fontdict=fontdict)
plt.ylabel("订单数", fontdict=fontdict)
plt.xlabel("购买量", fontdict=fontdict)
plt.show()
```

**图表输出 1**

![图表输出 15-1](./C:/mnt/c/Users/T1ng/Desktop/python数据分析/电商-母婴市场消费数据分析-约350行（pyecharts可视化、数据分析）/images/cell-015-output-01.png)

### 代码单元 9

```python
# 保留buy_mount[0,195]以内的记录
trade = trade[(trade.buy_mount >= 1) & (trade.buy_mount <= 195)]
# 列重命名
trade.rename({"auction_id": "item_id"}, axis=1, inplace=True)
# 先将property暂且取出放在一边，后续再分析
property = trade.property
trade.drop('property', axis=1, inplace=True)
# 日期类型转换
baby['birthday'] = pd.to_datetime(baby.birthday.astype('str'))
trade['day'] = pd.to_datetime(trade.day.astype('str'))
```

### 代码单元 10

```python
# 本次统计数据的时间范围是2012/7/2-2015/2/5
trade.day.describe()
```

**文本输出**

```text
count                   29942
unique                    949
top       2014-11-11 00:00:00
freq                      454
first     2012-07-02 00:00:00
last      2015-02-05 00:00:00
Name: day, dtype: object
```

### 代码单元 11

```python
count_cat1 = trade.cat1.nunique()
count_cat = trade.cat_id.nunique()
count_item = trade.item_id.nunique()
sales_volume = trade.buy_mount.sum()
count_user = trade.user_id.nunique()
print("商品类目数：", count_cat1)
print("商品类别数：", count_cat)
print("商品数：", count_item)
print("总销量：", sales_volume)
print("用户数", count_user)
```

**文本输出**

```text
商品类目数： 6
商品类别数： 662
商品数： 28394
总销量： 49973
用户数 29915
```

### 代码单元 12

```python
# 根据年月查看销量趋势
# 根据年分组
year_item = trade[['item_id', 'buy_mount', 'day']].groupby(by=trade.day.dt.year)[
    'buy_mount'].sum()
# 各年季度销量情况
year_quarter_item = trade[['item_id', 'buy_mount', 'day']].groupby(by=[trade.day.dt.year, trade.day.dt.quarter])[
    'buy_mount'].sum()
# 根据年月分组
year_month_item = trade[['item_id', 'buy_mount', 'day']].groupby(
    by=[trade.day.dt.year, trade.day.dt.month])['buy_mount'].sum()
```

### 代码单元 13

```python
# 各年销量情况
plt.figure(figsize=(10, 5))
sns.barplot(x=year_item.index, y=year_item.values)
plt.title("年销量趋势", fontdict=fontdict)
plt.xlabel("年份", fontdict=fontdict)
plt.ylabel("销量", fontdict=fontdict)
plt.show()
```

**图表输出 1**

![图表输出 23-1](./C:/mnt/c/Users/T1ng/Desktop/python数据分析/电商-母婴市场消费数据分析-约350行（pyecharts可视化、数据分析）/images/cell-023-output-01.png)

### 代码单元 14

```python
index_list = year_quarter_item.index.tolist()
index_list = ['-'.join([str(x[0]),str(x[1])]) for x in index_list]
index_list
```

**文本输出**

```text
['2012-3',
 '2012-4',
 '2013-1',
 '2013-2',
 '2013-3',
 '2013-4',
 '2014-1',
 '2014-2',
 '2014-3',
 '2014-4',
 '2015-1']
```

### 代码单元 15

```python
# 各季度销售情况
plt.figure(figsize=(10, 5))
sns.barplot(x=index_list, y=year_quarter_item.values)
plt.title("季度销量趋势", fontdict=fontdict)
plt.xlabel("(年,季度)", fontdict=fontdict)
plt.ylabel("销量", fontdict=fontdict)
plt.show()
```

**图表输出 1**

![图表输出 26-1](./C:/mnt/c/Users/T1ng/Desktop/python数据分析/电商-母婴市场消费数据分析-约350行（pyecharts可视化、数据分析）/images/cell-026-output-01.png)

### 代码单元 16

```python
# 各月份销量情况
x = [str(x[0])+"/"+str(x[1]) for x in year_month_item.index]
y = [int(x) for x in year_month_item.values]
p  =pyc.Bar().add_xaxis(xaxis_data=x
                    ).add_yaxis(series_name="销量", y_axis=y,
                        markpoint_opts=opts.MarkPointOpts(data=[opts.MarkPointItem(coord=[x[4], y[4]], value=y[4]),
                        opts.MarkPointItem(coord=[x[10], y[10]], value=y[10]),
                    opts.MarkPointItem(coord=[x[16], y[16]], value=y[16]),
                    opts.MarkPointItem(coord=[x[22], y[22]], value=y[22]), opts.MarkPointItem(coord=[x[28], y[28]], value=y[28])])
                    ).set_series_opts(label_opts=opts.LabelOpts(is_show=False)
                ).set_global_opts(title_opts=opts.TitleOpts(title="月销量趋势", subtitle="2012/7-2015/2的销量趋势图"), toolbox_opts=opts.ToolboxOpts())
p.render_notebook()
```

### 代码单元 17

```python
def quarterData(trade: pd.DataFrame, low: tuple, high: tuple) -> list:
    """
    输入日期型字符串,返回日期范围内的销量和用户量
    """
    from datetime import datetime
    low = datetime.strptime(low, "%Y/%m/%d")
    high = datetime.strptime(high, "%Y/%m/%d")
    trade_low = trade[(trade.day >= datetime(low.year, low.month, low.day)) & (
        trade.day <= datetime(high.year, high.month, high.day))]
    group_low = trade_low[['buy_mount', 'day', 'user_id']].groupby(
        by=[trade_low.day.dt.month, trade_low.day.dt.day])
    mount = group_low.buy_mount.sum()
    user = group_low.user_id.nunique()

    return [mount, user]
```

### 代码单元 18

```python
def lineMountUser(mount, user, title):
    """
    输入销量和用户量数据以及标题，生成折线图
    """
    plot = pyc.Line().add_xaxis(xaxis_data=[str(x[0])+"/"+str(x[1]) for x in mount.index]
                                ).add_yaxis(series_name="销量", y_axis=[int(x) for x in mount.values], markline_opts=opts.MarkLineOpts(data=[opts.MarkLineItem(name='当月销量均值', type_="average")])
                                            ).add_yaxis(series_name="用户量", y_axis=[int(x) for x in user.values], markline_opts=opts.MarkLineOpts(data=[opts.MarkLineItem(name='当月用户量量均值', type_="average")])
                                                        ).set_series_opts(label_opts=opts.LabelOpts(is_show=False)
                                                                          ).set_global_opts(title_opts=opts.TitleOpts(title=title), toolbox_opts=opts.ToolboxOpts(), tooltip_opts=opts.TooltipOpts(trigger='axis')
                                                                                            ).render_notebook()
    return plot
```

### 代码单元 19

```python
mount_2013_1_quarter = quarterData(trade, "2013/1/1", "2013/3/31")[0]
mount_2014_1_quarter = quarterData(trade, "2014/1/1", "2014/3/31")[0]
user_2013_1_quarter = quarterData(trade, "2013/1/1", "2013/3/31")[1]
user_2014_1_quarter = quarterData(trade, "2014/1/1", "2014/3/31")[1]
```

### 代码单元 20

```python
lineMountUser(mount_2013_1_quarter, user_2013_1_quarter, "2013年第一季度销量")
```

### 代码单元 21

```python
lineMountUser(mount_2014_1_quarter, user_2014_1_quarter, "2014年第一季度销量")
```

### 代码单元 22

```python
mount_2012_4_quarter, user_2012_4_quarter = quarterData(
    trade, "2012/10/1", "2012/12/31")
mount_2013_4_quarter, user_2013_4_quarter = quarterData(
    trade, "2013/10/1", "2013/12/31")
mount_2014_4_quarter, user_2014_4_quarter = quarterData(
    trade, "2014/10/1", "2014/12/31")
```

### 代码单元 23

```python
lineMountUser(mount_2012_4_quarter, user_2012_4_quarter, "2012年第四季度销量")
```

### 代码单元 24

```python
lineMountUser(mount_2013_4_quarter, user_2013_4_quarter, "2013年第四季度销量")
```

### 代码单元 25

```python
lineMountUser(mount_2014_4_quarter, user_2014_4_quarter, "2014年第四季度销量")
```

### 代码单元 26

```python
# trade = pd.merge(left=trade, right=baby, how='left',
#                       on='user_id', suffixes=("_trade", "_baby"))
```

### 代码单元 27

```python
# 由于数据不完整，所以我们只计算2013年和2014年的复购率
repurchase_data_2013 = trade[(trade.day >= datetime(
    2013, 1, 1)) & (trade.day <= datetime(2013, 12, 31))]
repurchase_data_2014 = trade[(trade.day >= datetime(
    2014, 1, 1)) & (trade.day <= datetime(2014, 12, 31))]
```

### 代码单元 28

```python
# 根据月和userid分组
group_2013 = repurchase_data_2013.groupby(
    by=[repurchase_data_2013.day.dt.month, 'user_id'])
group_2014 = repurchase_data_2014.groupby(
    by=[repurchase_data_2014.day.dt.month, 'user_id'])
```

### 代码单元 29

```python
repurchase_data_2013.groupby(
    by=[repurchase_data_2013.day.dt.month, 'user_id']).size()[[1]].sum()
```

**文本输出**

```text
628
```

### 代码单元 30

```python
def cmonthPurchaseRate(data):
    """
    导入根据月和userid分组数据
    """
    rate = []
    for i in range(1, 13):
        cmonth_bought_user = data.size()[[i]].sum()
        cmonth_repurchase_user = (data.size()[[i]] > 1).sum()
        rate.append(round(cmonth_repurchase_user/cmonth_bought_user, 4))
    return rate
```

### 代码单元 31

```python
purchase_rate_month_2013 = cmonthPurchaseRate(group_2013)
purchase_rate_month_2014 = cmonthPurchaseRate(group_2014)
```

### 代码单元 32

```python
pyc.Line().add_xaxis(xaxis_data=[x for x in range(1, 13)]
                     ).add_yaxis(
    series_name='2013年当月复购率', y_axis=purchase_rate_month_2013
).add_yaxis(series_name='2014年当月复购率', y_axis=purchase_rate_month_2014
            ).set_series_opts(label_opts=opts.LabelOpts(is_show=False)).set_global_opts(title_opts=opts.TitleOpts(title="当月复购率变化趋势", subtitle="2013年及2014年月复购率变化趋势"), toolbox_opts=opts.ToolboxOpts(), tooltip_opts=opts.TooltipOpts(is_show=True, trigger='axis')).render_notebook()
```

### 代码单元 33

```python
# 产品大类复购率
# 根据产品大类分组，然后循环大类进行索引求出每个大类的复购率
t = trade.groupby(by=['cat1', 'user_id']).size()
purchase_dict={}
for i in trade.cat1.unique():
    c = t.loc[i].value_counts()
    purchase_dict[i]=((c.sum()-c[:1])/c[:1]).values[0].round(4)
plt.figure(figsize=(10,6))
sns.barplot(x=list(purchase_dict.keys()),y=list(purchase_dict.values()))
plt.title("各大类复购率",fontdict=fontdict)
plt.show()
```

**图表输出 1**

![图表输出 51-1](./C:/mnt/c/Users/T1ng/Desktop/python数据分析/电商-母婴市场消费数据分析-约350行（pyecharts可视化、数据分析）/images/cell-051-output-01.png)

### 代码单元 34

```python
# 商品大类销售情况
cat = trade.groupby("cat1")['buy_mount'].sum()
sns.barplot(x=cat.index, y=cat.values)
plt.title("商品大类销售情况")
plt.xlabel("商品大类")
plt.show()
```

**图表输出 1**

![图表输出 54-1](./C:/mnt/c/Users/T1ng/Desktop/python数据分析/电商-母婴市场消费数据分析-约350行（pyecharts可视化、数据分析）/images/cell-054-output-01.png)

### 代码单元 35

```python
# 人均大类购买情况
cat_aver_user = (trade.groupby("cat1")['buy_mount'].sum(
) / trade.groupby("cat1")['user_id'].count()).sort_values(ascending=False)
sns.barplot(x=cat_aver_user.index, y=cat_aver_user.values)
plt.title("商品大类人均购买情况")
plt.xlabel("商品大类")
plt.show()
```

**图表输出 1**

![图表输出 55-1](./C:/mnt/c/Users/T1ng/Desktop/python数据分析/电商-母婴市场消费数据分析-约350行（pyecharts可视化、数据分析）/images/cell-055-output-01.png)

### 代码单元 36

```python
# 大类下子类别数量
cat_count = trade.groupby("cat1")['cat_id'].count()
sns.barplot(x=cat_count.index, y=cat_count.values)
plt.title("商品大类的子类数量")
plt.xlabel("商品大类")
plt.show()
```

**图表输出 1**

![图表输出 56-1](./C:/mnt/c/Users/T1ng/Desktop/python数据分析/电商-母婴市场消费数据分析-约350行（pyecharts可视化、数据分析）/images/cell-056-output-01.png)

</details>
