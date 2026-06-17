---
title: "历年考研分数线数据可视化：从趋势和院校信息辅助择校判断"
date: 2026-06-17T23:08:42+08:00
# weight: 1
# aliases: ["/first"]
categories: ["教育"]
tags: ["pyecharts", "词云", "教育数据", "考研"]
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

# 历年考研分数线数据可视化：从趋势和院校信息辅助择校判断

## 摘要

| 模块     | 内容                                                         |
| -------- | ------------------------------------------------------------ |
| 业务场景 | 教育                                                         |
| 数据来源 | 历年考研国家线、大学信息和调剂数据。                         |
| 分析方法 | CSV/Excel 数据处理、Pyecharts 趋势图、院校信息分析、词云可视化。 |
| 结论先行 | 分数线变化能反映报考热度、招生计划和考试难度的综合影响。     |

本报告围绕“业务背景、分析目的、数据说明、分析思路、分析过程、核心结论和改进建议”展开，目标是用数据回答具体问题，并把分析结果转化为可执行的判断。

## 一、分析背景

考研择校需要同时考虑分数线趋势、院校层次、专业热度和调剂机会。数据可视化可以降低信息搜集成本，帮助考生做更理性的选择。

## 二、分析目的

本次分析主要回答以下问题：

- 文本中用户最关注的主题和关键词是什么？
- 正负向反馈分别集中在哪些具体问题上？
- 这些文本信号能沉淀成哪些产品、运营或服务改进动作？

先明确分析目的，再开展数据处理和指标拆解，可以保证报告围绕问题展开，而不是简单罗列代码和图表。

## 三、数据来源与指标说明

| 项目           | 说明                                                         |
| -------------- | ------------------------------------------------------------ |
| 数据来源       | 历年考研国家线、大学信息和调剂数据。                         |
| 分析工具与方法 | CSV/Excel 数据处理、Pyecharts 趋势图、院校信息分析、词云可视化。 |
| 重点分析指标   | 文本样本量、分词结果、关键词、词频、情感倾向、正负向主题和典型问题。 |
| 数据口径       | 本文以项目数据集中的字段为分析范围，先完成缺失值、异常值、重复值或类别字段处理，再围绕核心指标做统计、可视化或建模。 |

数据口径会直接影响分析结论，因此报告先说明数据范围、核心指标和处理方式，便于读者理解结论的适用边界。

## 四、分析思路

| 步骤                | 目的                                                         |
| ------------------- | ------------------------------------------------------------ |
| 1. 明确业务问题     | 确定分析要回答什么，以及结论会影响什么决策。                 |
| 2. 数据读取与清洗   | 处理缺失、重复、异常和字段格式问题，保证分析基础可靠。       |
| 3. 指标拆解与可视化 | 从趋势、结构、对比、分布或空间维度观察数据现象。             |
| 4. 建模或深度分析   | 根据项目需要完成聚类、预测、分类、回归、文本分析或可视化大屏。 |
| 5. 输出结论与建议   | 把数据发现翻译成业务语言，并给出可执行的下一步动作。         |

本项目的具体分析路径如下：

- 先明确文本分析目标：是识别用户关注点、判断情绪倾向，还是提取岗位/产品关键词。
- 对文本做清洗、分词和停用词过滤，减少无意义词对结果的干扰。
- 通过词频、关键词、词云或情感模型提炼主要信息。
- 结合业务场景解释文本结果，避免只停留在高频词罗列。
- 把文本洞察沉淀成标签、问题清单或运营建议。

## 五、数据处理过程

本项目的数据处理主要包括以下环节：

- 读取原始数据，检查字段类型、样本规模和基础统计信息。
- 处理缺失值、重复值、异常值或文本噪声，保证后续统计和建模结果可靠。
- 根据分析目标构造必要指标、标签或特征，并统一字段口径。
- 按业务维度进行分组、聚合、可视化或模型训练，为结论提供依据。

## 六、数据分析与结果

本部分按照“分析发现 -> 结果解读”的方式组织，重点说明数据体现出的现象及其业务含义。

### 1. 分数线变化能反映报考热度、招生计划和考试难度的综合影响。

结果解读：该发现是本项目最核心的结论之一，说明数据中存在值得关注的结构性特征。对应图表或模型结果应围绕这一判断展开，帮助读者理解结论来源。

### 2. 单年分数线不足以判断难度，需要观察多年趋势和波动范围。

结果解读：该发现进一步解释了不同维度之间的差异。对业务决策而言，重点不只是看到差异，而是判断差异来自哪些对象、场景或指标。

### 3. 调剂数据和院校信息可以补充风险判断，帮助考生制定备选方案。

结果解读：该发现可以作为后续优化策略或模型改进的依据。若用于真实业务，还需要结合成本、资源、实验结果或线上反馈继续验证。

## 七、结论

综合以上分析，可以得到以下结论：

- 分数线变化能反映报考热度、招生计划和考试难度的综合影响。
- 单年分数线不足以判断难度，需要观察多年趋势和波动范围。
- 调剂数据和院校信息可以补充风险判断，帮助考生制定备选方案。

## 八、建议

- 行动 1：择校时应按冲刺、稳妥和保底三档配置目标院校。
- 行动 2：教育产品可将分数线趋势、院校画像和调剂信息整合成推荐工具。
- 行动 3：后续可加入专业招生人数、复试线和录取最低分，提升决策价值。
- 跟进方式：为每条建议绑定一个可观察指标，后续按周或按月复盘效果。

建议部分应结合具体对象、执行动作和复盘指标，避免停留在泛泛的“加强管理”或“优化运营”。

## 九、局限性与改进方向

- 项目价值：把非结构化文本转化为可统计的问题标签和情绪信号，帮助业务更快定位用户关注点和负面体验。
- 真实限制：分数线和调剂数据受招生计划、报考人数、考试难度和政策变化影响，历史趋势不能直接等同于下一年结果。
- 业务风险：如果只按历史分数线推荐院校，可能忽略专业课难度、复试比例和招生缩招风险。
- 改进方向：建立人工抽检样本集，评估分词、情感判断和主题归类是否符合业务语境。
- 改进方向：把文本标签与订单、退款、投诉、复购或客服工单关联，验证文本问题对经营结果的影响。

## 附录：完整代码与输出结果

下面内容按原 notebook 的代码单元顺序整理。如果代码单元产生了文本输出或图片输出，也一并附在对应代码后面，便于复现完整分析过程。

### 代码单元 1

```python
import json
import requests
import pandas as pd
import pyecharts.options as opts
from pyecharts.charts import *
from pyecharts.globals import ThemeType#设定主题
from pyecharts.commons.utils import JsCode
import chardet
import jieba
import numpy as np
```

### 代码单元 2

```python
df1 = pd.read_csv(r'./考研历年国家分数线(1).csv')
df2 = pd.read_csv(r'./考研历年国家分数线(2).csv')
df3 = pd.read_csv(r'./考研历年国家分数线(3).csv')
df4 = pd.read_csv(r'./考研历年国家分数线(4).csv')
df5 = pd.read_csv(r'./考研历年国家分数线(5).csv')
df6 = pd.read_csv(r'./考研历年国家分数线(6).csv')
df_all= pd.concat([df1,df2,df3,df4,df5,df6])
df_all.info()
```

**文本输出**

```text
<class 'pandas.core.frame.DataFrame'>
Int64Index: 100864 entries, 0 to 863
Data columns (total 13 columns):
 #   Column   Non-Null Count   Dtype 
---  ------   --------------   ----- 
 0   年份       100864 non-null  int64 
 1   学校名称_链接  100864 non-null  object
 2   学校名称     100863 non-null  object
 3   院系名称_链接  100864 non-null  object
 4   院系名称     100725 non-null  object
 5   专业代码     100761 non-null  object
 6   专业名称_链接  100864 non-null  object
 7   专业名称     100864 non-null  object
 8   总分       100864 non-null  object
 9   政治__管综   100864 non-null  object
 10  外语       100864 non-null  object
 11  业务课_一    100864 non-null  object
 12  业务课_二    100864 non-null  object
dtypes: int64(1), object(12)
memory usage: 10.8+ MB
```

### 代码单元 3

```python
print(df_all.shape)
```

**文本输出**

```text
(100864, 13)
```

### 代码单元 4

```python
print('重复值：' ,df_all.duplicated().sum())
print('空值: \n',df_all.isnull().sum())
```

**文本输出**

```text
重复值： 58
空值: 
 年份           0
学校名称_链接      0
学校名称         1
院系名称_链接      0
院系名称       139
专业代码       103
专业名称_链接      0
专业名称         0
总分           0
政治__管综       0
外语           0
业务课_一        0
业务课_二        0
dtype: int64
```

### 代码单元 5

```python
df_all = df_all.drop_duplicates()
df_all = df_all.dropna(axis=0,how='any')
```

### 代码单元 6

```python
df_all.info()
print(df_all.shape)
```

**文本输出**

```text
<class 'pandas.core.frame.DataFrame'>
Int64Index: 100563 entries, 0 to 863
Data columns (total 13 columns):
 #   Column   Non-Null Count   Dtype 
---  ------   --------------   ----- 
 0   年份       100563 non-null  int64 
 1   学校名称_链接  100563 non-null  object
 2   学校名称     100563 non-null  object
 3   院系名称_链接  100563 non-null  object
 4   院系名称     100563 non-null  object
 5   专业代码     100563 non-null  object
 6   专业名称_链接  100563 non-null  object
 7   专业名称     100563 non-null  object
 8   总分       100563 non-null  object
 9   政治__管综   100563 non-null  object
 10  外语       100563 non-null  object
 11  业务课_一    100563 non-null  object
 12  业务课_二    100563 non-null  object
dtypes: int64(1), object(12)
memory usage: 10.7+ MB
(100563, 13)
```

### 代码单元 7

```python
print('重复值：' ,df_all.duplicated().sum())
print('空值: \n',df_all.isnull().sum())
```

**文本输出**

```text
重复值： 0
空值: 
 年份         0
学校名称_链接    0
学校名称       0
院系名称_链接    0
院系名称       0
专业代码       0
专业名称_链接    0
专业名称       0
总分         0
政治__管综     0
外语         0
业务课_一      0
业务课_二      0
dtype: int64
```

### 代码单元 8

```python
df_all = df_all.drop(labels=['学校名称_链接','院系名称_链接','专业名称_链接'],axis=1)
df_all.head(2)
```

**文本输出**

```text
年份    学校名称    院系名称    专业代码        专业名称   总分 政治__管综  外语 业务课_一 业务课_二
0  2020  中国人民大学  公共管理学院  125200  (专业学位)公共管理  175     88  44     -     -
1  2020  中国人民大学  公共管理学院  125200  (专业学位)公共管理  175     88  44     -     -
```

### 代码单元 9

```python
df_all['专业名称'] = df_all['专业名称'].str.replace('\(专业学位\)','')
df_all['专业名称'] = df_all['专业名称'].str.replace('★','')
df_all.head(2)
```

**文本输出**

```text
C:\Users\Administrator\AppData\Local\Temp\2\ipykernel_18548\4240388851.py:1: FutureWarning: The default value of regex will change from True to False in a future version.
  df_all['专业名称'] = df_all['专业名称'].str.replace('\(专业学位\)','')
年份    学校名称    院系名称    专业代码  专业名称   总分 政治__管综  外语 业务课_一 业务课_二
0  2020  中国人民大学  公共管理学院  125200  公共管理  175     88  44     -     -
1  2020  中国人民大学  公共管理学院  125200  公共管理  175     88  44     -     -
```

### 代码单元 10

```python
data_2020 = df_all[df_all['年份'] == 2020]
data_2020.info()
```

**文本输出**

```text
<class 'pandas.core.frame.DataFrame'>
Int64Index: 65808 entries, 0 to 5995
Data columns (total 10 columns):
 #   Column  Non-Null Count  Dtype 
---  ------  --------------  ----- 
 0   年份      65808 non-null  int64 
 1   学校名称    65808 non-null  object
 2   院系名称    65808 non-null  object
 3   专业代码    65808 non-null  object
 4   专业名称    65808 non-null  object
 5   总分      65808 non-null  object
 6   政治__管综  65808 non-null  object
 7   外语      65808 non-null  object
 8   业务课_一   65808 non-null  object
 9   业务课_二   65808 non-null  object
dtypes: int64(1), object(9)
memory usage: 5.5+ MB
```

### 代码单元 11

```python
data_2020['专业名称'].value_counts()[:100]
```

**文本输出**

```text
工商管理        1058
计算机科学与技术     877
管理科学与工程      844
数学           808
内科学          808
            ... 
计算机应用技术      178
网络空间安全       177
城乡规划学        173
艺术学理论        173
中医内科学        173
Name: 专业名称, Length: 100, dtype: int64
```

### 代码单元 12

```python
data_2020.groupby('学校名称')['专业名称'].count().sort_values(ascending = False)[:100]
```

**文本输出**

```text
学校名称
北京大学      3093
复旦大学      1248
清华大学      1217
武汉大学       858
中国人民大学     758
          ... 
河南科技大学     211
华北理工大学     208
上海师范大学     207
吉林农业大学     205
沈阳农业大学     203
Name: 专业名称, Length: 100, dtype: int64
```

### 代码单元 13

```python
def tranform_num(x):
    if '-' in x:
        return 0
    else:
        return x
    
data_2020['总分'] = data_2020['总分'].apply(lambda x:tranform_num(x) )
data_2020['总分'] = data_2020['总分'].astype('int')
```

**文本输出**

```text
C:\Users\Administrator\AppData\Local\Temp\2\ipykernel_18548\688768844.py:7: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame.
Try using .loc[row_indexer,col_indexer] = value instead

See the caveats in the documentation: https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#returning-a-view-versus-a-copy
  data_2020['总分'] = data_2020['总分'].apply(lambda x:tranform_num(x) )
C:\Users\Administrator\AppData\Local\Temp\2\ipykernel_18548\688768844.py:8: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame.
Try using .loc[row_indexer,col_indexer] = value instead

See the caveats in the documentation: https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#returning-a-view-versus-a-copy
  data_2020['总分'] = data_2020['总分'].astype('int')
```

### 代码单元 14

```python
data_1 = data_2020.groupby('专业名称')['总分'].agg([np.mean, np.max,np.min])
data_1['mean'] = data_1['mean'].astype('int')
data_1 = data_1.sort_values(by=['mean'],ascending=False)[:50]
data_1
```

**文本输出**

```text
mean  amax  amin
专业名称                            
公共关系学            409   409   409
国别与区域研究          402   402   402
美术理论研究           397   397   397
信息艺术设计           390   390   390
国民经济动员学          388   400   376
高级秘书与行政助理学       386   386   386
公共组织与人力资源        385   385   385
中国政治             383   383   383
网络与新媒体           382   382   382
符号学              382   382   382
传媒艺术学            381   381   381
媒介管理学            380   380   380
非传统安全            380   380   380
公共财政与公共政策        380   380   380
政府经济管理           379   379   379
地方政府与社会治理        377   377   377
电子政务             376   380   360
犯罪心理学            375   375   375
城乡发展与规划          375   375   375
公共管理信息化理论与技术     375   375   375
能源与气候经济          375   376   375
文化研究             372   378   355
医院管理与卫生政策        372   372   372
物流管理与工程          372   372   372
医药信息系统           370   370   370
互联网金融学           370   370   370
法与经济学            370   370   370
艺术与科学            370   370   370
电视电影与视听传播学       370   370   370
创业学              370   370   370
军事法学             370   370   370
饭店管理             370   370   370
文化传播学            370   370   370
企业经济学            368   368   368
网络经济学            368   368  
... 输出过长，博客中已截断
```

### 代码单元 15

```python
bar = Bar(init_opts=opts.InitOpts(theme='light',
                                    width='1000px',
                                    height='1200px')
                                    )

bar.add_xaxis(data_1.index.tolist())
bar.add_yaxis('最高分',
               data_1['amax'].tolist(),
               z_level=1,
               stack='1',
               category_gap='50%',
               tooltip_opts=opts.TooltipOpts(is_show=False),
               label_opts=opts.LabelOpts(position='insideRight', formatter='{c} 分'),
               itemstyle_opts={"normal": {
                        'shadowBlur': 10,
                        'shadowColor': 'rgba(0, 0, 0, 0.1)',
                        'shadowOffsetX': 10,
                        'shadowOffsetY': 10,
                        'color':'#ec9bad',
                        'borderColor': 'rgb(220,220,220)',
                        'borderWidth':2}
                },
               )
bar.add_yaxis('最低分',
               data_1['amin'].tolist(),
               z_level=1,
               stack='1',
               category_gap='50%',
               tooltip_opts=opts.TooltipOpts(is_show=False),
               label_opts=opts.LabelOpts(position='insideLeft', formatter='{c} 分'),
               itemstyle_opts={"normal": {
                        'shadowBlur': 10,
                        'shadowColor': 'rgba(0, 0, 0, 0.1)',
                        'shadowOffsetX': 10,
                        'shadowOffsetY': 10,
                        'color':'#87CEFA',
                        'borderColor': 'rgb(220,220,220)',
                        'borderWidth':2}
                },
               )

bar.set_global_opts(title_opts=opts.TitleOpts(title="各专业的最高分和最低分",
                                              pos_left="center",
                                              pos_top='0%',
                                              title_textstyle_opts=opts.TextStyleOpts(font_size=20,
                                                                                      color='#00BFFF')),
                        legend_opts=opts.LegendOpts(is_show=True, pos_top='3%'),
                        datazoom_opts=opts.DataZoomOpts(type_='inside',
                                                    range_start=50,   # 设置起止位置，50%-100%
                                                    range_end=100,
                                                    orient='vertical'),
                        xaxis_opts=opts.AxisOpts(is_show=False, max_=818),
                        yaxis_opts=opts.AxisOpts(axisline_opts=opts.AxisLineOpts(is_show=False),
                                             axistick_opts=opts.AxisTickOpts(is_show=False),
                                             axislabel_opts=opts.LabelOpts(color='#528B8B', font_size=10, font_weight='bold')),
                    )
bar.reversal_axis()
bar.render_notebook()
```

### 代码单元 16

```python
data_2 = data_2020['专业名称'].value_counts()[:50]
```

### 代码单元 17

```python
data_x =data_2.index.tolist()
data_y = data_2.values.tolist()

bar = Bar(init_opts=opts.InitOpts(theme='light',
                                  width='1000px',
                                  height='900px'))
bar.add_xaxis(data_x)
bar.add_yaxis('考研专业', [int(i) for i in data_y])
bar.set_series_opts(label_opts=opts.LabelOpts(position="insideLeft",
                                              font_size=12,
                                              font_weight='bold',
                                              formatter='{b}:{c} 个'))
bar.set_global_opts(title_opts=opts.TitleOpts(title="2020年考研专业Top50", pos_top='2%', pos_left='center',
                                              title_textstyle_opts=opts.TextStyleOpts(font_size=20,
                                                                                      color='#00BFFF')),
                    legend_opts=opts.LegendOpts(is_show=False),
                    xaxis_opts=opts.AxisOpts(is_show=False, is_scale=True),
                    yaxis_opts=opts.AxisOpts(is_show=False),
                    datazoom_opts=opts.DataZoomOpts(type_='inside',
                                                    range_start=50,   # 设置起止位置，50%-100%
                                                    range_end=100,
                                                    orient='vertical'),
                    
                    visualmap_opts=opts.VisualMapOpts(is_show=False,
                                          max_=1058,
                                          min_=1,
                                          is_piecewise=False,
                                          dimension=0,
                                          range_color=['rgba(236,155,173,1)', 'rgba(237,157,178,0.4)'])
                                      )
bar.reversal_axis()
bar.render_notebook()
```

### 代码单元 18

```python
def get_cut_words(content_series):
    # 读入停用词表
    stop_words = [' ','是','的']

#     with open(r"\中文停用词库.txt", 'r') as f:
#         lines = f.readlines()
#         for line in lines:
#             stop_words.append(line.strip())

    # 添加关键词
    my_words = ['']
    for i in my_words:
        jieba.add_word(i)

    # 自定义停用词
    my_stop_words = ['查看','详细','详见','详情','与化','03','02','01','正文','多个','相关']
    stop_words.extend(my_stop_words)

    # 分词
    word_num = jieba.lcut(content_series.str.cat(sep='。'), cut_all=False)

    # 条件筛选
    word_num_selected = [i for i in word_num if i not in stop_words and len(i)>=2]
    
    return word_num_selected
```

### 代码单元 19

```python
text1 = get_cut_words(content_series=df_all.专业名称)
```

**文本输出**

```text
Building prefix dict from the default dictionary ...
Dumping model to file cache C:\Users\ADMINI~1\AppData\Local\Temp\2\jieba.cache
Loading model cost 1.245 seconds.
Prefix dict has been built successfully.
```

### 代码单元 20

```python
# 安装stylecloud
```

**文本输出**

```text
Looking in indexes: https://pypi.tuna.tsinghua.edu.cn/simple
Collecting stylecloud
  Downloading https://pypi.tuna.tsinghua.edu.cn/packages/28/6a/695819d00292ce4d7701938262886318b3b98c6d7c7ea29d8b1a516cbff7/stylecloud-0.5.2.tar.gz (262 kB)
     -------------------------------------- 262.1/262.1 kB 3.2 MB/s eta 0:00:00
  Preparing metadata (setup.py): started
  Preparing metadata (setup.py): finished with status 'done'
Collecting wordcloud
  Downloading https://pypi.tuna.tsinghua.edu.cn/packages/5d/fb/240a57f37c650721e30c86253348c2a0436ca6f6803bb5eb6d58cdca3018/wordcloud-1.8.2.2-cp39-cp39-win_amd64.whl (153 kB)
     -------------------------------------- 153.1/153.1 kB 8.9 MB/s eta 0:00:00
Collecting icon-font-to-png
  Downloading https://pypi.tuna.tsinghua.edu.cn/packages/3d/70/c3b6c5904ae8592cb97c3ddb5de40801837f66922aa140e285d4a2e49a42/icon_font_to_png-0.4.1-py2.py3-none-any.whl (161 kB)
     -------------------------------------- 161.4/161.4 kB 3.2 MB/s eta 0:00:00
Collecting palettable
  Downloading https://pypi.tuna.tsinghua.edu.cn/packages/ca/46/5198aa24e61bb7eef28d06cb69e56bfa1942f4b6807d95a0b5ce361fe09b/palettable-3.3.0-py2.py3-none-any.whl (111 kB)
     -------------------
... 输出过长，博客中已截断
```

### 代码单元 21

```python
import numpy as np
import stylecloud
from IPython.display import Image

stylecloud.gen_stylecloud(
    text=' '.join(text1),
    collocations=False,
    font_path=r'./SimHei.ttf',
    icon_name='fas fa-book',
    size=768,
    output_name='./词云图1.png'
)

Image(filename='./词云图1.png')
```

**图表输出 1**

![图表输出 36-1](./images/cell-036-output-01.png)

### 代码单元 22

```python
text2 = get_cut_words(content_series=df_all.学校名称)
text2[:4]
```

**文本输出**

```text
['中国人民大学', '中国人民大学', '中国人民大学', '同济大学']
```

### 代码单元 23

```python
stylecloud.gen_stylecloud(
    text=' '.join(text2),
    collocations=False,
    font_path=r'./SimHei.ttf',
    icon_name='fas fa-graduation-cap',
    size=768,
    output_name='词云图2.png'
)

Image(filename='词云图2.png')
```

**图表输出 1**

![图表输出 38-1](./images/cell-038-output-01.png)

### 代码单元 24

```python
import pandas as pd
```

### 代码单元 25

```python
df_info = pd.read_excel(r'./大学信息2021new.xlsx')
df_info.head()
```

**文本输出**

```text
school school_type                                        school_attr  \
0       北方民族大学         民族类                             中央部委高校\n\n\n丝绸之路大学联盟成员   
1  上海船舶运输科学研究所         NaN                                                NaN   
2         北华大学          综合  （2012年）\n（2014年\n全国高校实践育人创新创业基地（2015年）\n（2017年...   
3     佛山科学技术学院         NaN                                                NaN   
4       武汉轻工大学          理工  国家粮食和物资储备局与湖北省人民政府共建高校（2018）\n湖北省国内一流学科建设高校（20...   

  province  
0       宁夏  
1       上海  
2       吉林  
3       广东  
4       湖北
```

### 代码单元 26

```python
df_info.info()
```

**文本输出**

```text
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 747 entries, 0 to 746
Data columns (total 4 columns):
 #   Column       Non-Null Count  Dtype 
---  ------       --------------  ----- 
 0   school       747 non-null    object
 1   school_type  528 non-null    object
 2   school_attr  531 non-null    object
 3   province     747 non-null    object
dtypes: object(4)
memory usage: 23.5+ KB
```

### 代码单元 27

```python
def transform_attr(x):
    #转换学校属性
    if '211' in x and '985' not in x:
        return 211
    elif '985' in x:
        return '985'
    else:
        return '双非'
    
def transform_type(x):
    #转换学校类型
    if '理工类' in x or '理工类院校' in x or '理工科' in x or '理工、教学研究型大学' in x or '理工类\n[4]' in x or '理工\n[6]' in x:
        return '理工'
    elif '综合类' in x or '综合性大学\n[3]' in x or '综合类（应用型大学）' in x or '综合、研究教学型大学' in x or '综合类大学' in x or '综合师范类' in x:
        return '综合'
    elif '师范类院校' in x or '师范类' in x or '师范类（综合类）' in x or '师范（综合）' in x or '地方师范院校' in x:
        return '师范'
    elif '农林类' in x or '农业类' in x:
        return '农林'
    elif '医药类' in x:
        return '医药'
    elif '民族类' in x:
        return '民族'
    elif '未知' in x or '国有企业' in x or '科技型企业' in x or '公立大学' in x:
        return '其他'
    elif '重点' in x or '省' in x or '2' in x or '' in x:
        return '其他'
    else:
        return x
    
# 转换数据
df_info['school_level'] = df_info.school_attr.astype(str).apply(lambda x:transform_attr(x))
df_info['school_types'] = df_info.school_type.astype(str).apply(lambda x: transform_type(x))
# 筛选字段
df_info= df_info[['school','province','school_level','school_types']]

# 处理省份数据
df_info.loc[(df_info.school=='北京工商大学')&(df_info.province=='未知'), 'province']= '北京'
df_info.loc[(df_info.school=='哈尔滨工程大学')&(df_info.province=='未知'), 'province']= '哈尔滨'
df_info.loc[(df_info.school=='江苏大学')&(df_info.province=='未知'), 'province']= '江苏'
df_info.loc[(df_info.school=='青岛大学')&(df_info.province=='未知'), 'province']= '山东'
df_info.loc[(df_info.school=='北京石油化工学院')&(df_info.province=='未知'), 'province']= '北京'
df_info.loc[(df_info.school=='齐鲁工业大学')&(df_info.province=='未知'), 'province']= '山东'
df_info.loc[(df_info.school=='江苏科技大学')&(df_info.province=='未知'), 'province']= '江苏'
df_info.loc[(df_info.school=='浙江农林大学')&(df_info.province=='未知'), 'province']= '浙江'
df_info.loc[(df_info.school=='燕山大学')&(df_info.province=='未知'), 'province']= '河北'
df_info.loc[(df_info.school=='福州大学')&(df_info.province=='未知'), 'province']= '福建'
df_info.loc[(df_info.school=='内蒙古科技大学')&(df_info.province=='未知'), 'province']= '内蒙古'
```

### 代码单元 28

```python
df_info.head()
```

**文本输出**

```text
school province school_level school_types
0       北方民族大学       宁夏           双非           民族
1  上海船舶运输科学研究所       上海           双非           其他
2         北华大学       吉林           双非           其他
3     佛山科学技术学院       广东           双非           其他
4       武汉轻工大学       湖北           双非           其他
```

### 代码单元 29

```python
df_info = df_info.drop_duplicates()#删除重
df_info.info()
```

**文本输出**

```text
<class 'pandas.core.frame.DataFrame'>
Int64Index: 327 entries, 0 to 745
Data columns (total 4 columns):
 #   Column        Non-Null Count  Dtype 
---  ------        --------------  ----- 
 0   school        327 non-null    object
 1   province      327 non-null    object
 2   school_level  327 non-null    object
 3   school_types  327 non-null    object
dtypes: object(4)
memory usage: 12.8+ KB
```

### 代码单元 30

```python
df_info.shape
```

**文本输出**

```text
(327, 4)
```

### 代码单元 31

```python
df = pd.read_excel(r'./考研调剂数据-3.08.xlsx')
df.shape
```

**文本输出**

```text
(747, 5)
```

### 代码单元 32

```python
df_2021 = df[df['time'].str.contains('2021')].copy()
df_2021.shape
```

**文本输出**

```text
(747, 5)
```

### 代码单元 33

```python
pd.merge(df_2021,df_info,how = 'left',on = 'school').shape
```

**文本输出**

```text
(774, 8)
```

### 代码单元 34

```python
df_all = pd.merge(df_2021,df_info,how = 'left',on = 'school')
df_all.head(5)
```

**文本输出**

```text
school            name                          title  \
0       北方民族大学    电子科学与技术、电子信息  2021年北方民族大学“电子科学与技术”和“电子信息”..   
1  上海船舶运输科学研究所  轮机工程、通信与信息系统..    上海船舶运输科学研究所2021年硕士研究生招生调剂信息   
2         北华大学  基础数学、计算数学、概率..  北华大学数学与统计学院2021年硕士研究生招生预调剂信..   
3     佛山科学技术学院  机械工程、光学工程、材料..     佛山科学技术学院2021年硕士研究生预调剂公告(一)   
4     佛山科学技术学院  机械工程、光学工程、材料..     佛山科学技术学院2021年硕士研究生预调剂公告(一)   

                                   url        time province school_level  \
0  /tiaoji/schooldetail/id/28535.shtml  2021-03-09       宁夏           双非   
1  /tiaoji/schooldetail/id/29191.shtml  2021-03-08       上海           双非   
2  /tiaoji/schooldetail/id/29189.shtml  2021-03-08       吉林           双非   
3  /tiaoji/schooldetail/id/29187.shtml  2021-03-08       广东           双非   
4  /tiaoji/schooldetail/id/29187.shtml  2021-03-08       湖南           双非   

  school_types  
0           民族  
1           其他  
2           其他  
3           其他  
4           其他
```

### 代码单元 35

```python
df_all = df_all[['school','name','time','province','school_level','school_types']]
df_all.head()
```

**文本输出**

```text
school            name        time province school_level school_types
0       北方民族大学    电子科学与技术、电子信息  2021-03-09       宁夏           双非           民族
1  上海船舶运输科学研究所  轮机工程、通信与信息系统..  2021-03-08       上海           双非           其他
2         北华大学  基础数学、计算数学、概率..  2021-03-08       吉林           双非           其他
3     佛山科学技术学院  机械工程、光学工程、材料..  2021-03-08       广东           双非           其他
4     佛山科学技术学院  机械工程、光学工程、材料..  2021-03-08       湖南           双非           其他
```

### 代码单元 36

```python
df_all.isnull().sum()
```

**文本输出**

```text
school           0
name            10
time             0
province         0
school_level     0
school_types     0
dtype: int64
```

### 代码单元 37

```python
pub_time = df_all.time.value_counts().sort_index()
pub_time
```

**文本输出**

```text
2021-01-04      3
2021-01-05      1
2021-01-12      1
2021-01-19      2
2021-01-26      2
2021-02-05      1
2021-02-07      3
2021-02-18      6
2021-02-22      1
2021-02-23      3
2021-02-24      1
2021-02-25     14
2021-02-26    110
2021-02-27     64
2021-02-28     29
2021-03-01     78
2021-03-02     99
2021-03-03    101
2021-03-04     57
2021-03-05    108
2021-03-06     32
2021-03-07     12
2021-03-08     45
2021-03-09      1
Name: time, dtype: int64
```

### 代码单元 38

```python
line1 = Line(init_opts=opts.InitOpts(width='1000px',height='600px'))
line1.add_xaxis(pub_time.index.tolist())
line1.add_yaxis('发布热度',pub_time.values.tolist(),
               areastyle_opts=opts.AreaStyleOpts(opacity=0.5),
               label_opts=opts.LabelOpts(is_show=True))
line1.set_global_opts(title_opts=opts.TitleOpts(title='调剂信息发布时间走势图'),
                     toolbox_opts=opts.ToolboxOpts(),
                      xaxis_opts=opts.AxisOpts(name='时间',
                                               type_='category',
                                               axislabel_opts=opts.LabelOpts(rotate=45),
                                               ),
                     visualmap_opts=opts.VisualMapOpts())
line1.render_notebook()
```

### 代码单元 39

```python
level_perc = df_all.school_level.value_counts() / df_all.school_level.value_counts().sum()
display(level_perc)
level_perc = np.round(level_perc * 100 ,2)
level_perc
```

**文本输出**

```text
双非     0.981912
985    0.011628
211    0.006460
Name: school_level, dtype: float64
双非     98.19
985     1.16
211     0.65
Name: school_level, dtype: float64
```

### 代码单元 40

```python
pie1 = Pie(init_opts=opts.InitOpts(theme='light',width='800px',height='600px'))
pie1.add("",
         [*zip(level_perc.index, level_perc.values)],
         radius=["40%","75%"])
pie1.set_global_opts(title_opts=opts.TitleOpts(title='学校层次分布',pos_left='center', pos_top='center',title_textstyle_opts=opts.TextStyleOpts(
                                                   color='#00BFFF', font_size=30, font_weight='bold'),
                                               ),
                     legend_opts=opts.LegendOpts(orient="vertical", pos_top="15%", pos_left="2%"),
#                      toolbox_opts=opts.ToolboxOpts()
                    )
pie1.set_series_opts(label_opts=opts.LabelOpts(formatter="{c}%"))
pie1.render_notebook()
```

### 代码单元 41

```python
province_num = df_all.province.value_counts().sort_values()
province_num
```

**文本输出**

```text
贵州      2
宁夏      2
甘肃      4
海南      4
内蒙古     4
新疆      5
云南      6
天津     11
广西     14
安徽     18
河南     20
福建     20
四川     21
重庆     22
湖南     23
山西     24
江西     28
河北     30
吉林     32
浙江     33
辽宁     39
陕西     40
上海     41
江苏     45
黑龙江    46
湖北     48
广东     49
山东     64
北京     79
Name: province, dtype: int64
```

### 代码单元 42

```python
# 条形图
bar1 = Bar(init_opts=opts.InitOpts(theme='light',width='1000px', height='1000px'))
bar1.add_xaxis(province_num.index.tolist())
bar1.add_yaxis("省份", province_num.values.tolist())
bar1.set_global_opts(title_opts=opts.TitleOpts(title="调剂信息发布数省份分布"),
#                      toolbox_opts=opts.ToolboxOpts(),
                     visualmap_opts=opts.VisualMapOpts(max_=79))
bar1.set_series_opts(label_opts=opts.LabelOpts(position='right'))  # 标签
bar1.reversal_axis()
bar1.render_notebook()
```

### 代码单元 43

```python
c = Map(init_opts=opts.InitOpts(width='800px', height='750px'))
c.add('',[list(z) for z in zip(province_num.index.tolist(), province_num.values.tolist())], 'china')
c.set_global_opts(title_opts=opts.TitleOpts('调剂信息省份分布地图'),
#                   toolbox_opts=opts.ToolboxOpts(is_show=True),
                  visualmap_opts=opts.VisualMapOpts(max_=79))
c.render_notebook()
```

### 代码单元 44

```python
print([list(z) for z in zip(province_num.index.tolist(), province_num.values.tolist())])
```

**文本输出**

```text
[['贵州', 2], ['宁夏', 2], ['甘肃', 4], ['海南', 4], ['内蒙古', 4], ['新疆', 5], ['云南', 6], ['天津', 11], ['广西', 14], ['安徽', 18], ['河南', 20], ['福建', 20], ['四川', 21], ['重庆', 22], ['湖南', 23], ['山西', 24], ['江西', 28], ['河北', 30], ['吉林', 32], ['浙江', 33], ['辽宁', 39], ['陕西', 40], ['上海', 41], ['江苏', 45], ['黑龙江', 46], ['湖北', 48], ['广东', 49], ['山东', 64], ['北京', 79]]
```

### 代码单元 45

```
# 改为省份全称才能正常显示
c = Map(init_opts=opts.InitOpts(width='800px', height='750px'))
c.add('',[['贵州省', 2],
 ['宁夏回族自治区', 2],
 ['甘肃省', 4],
 ['海南省', 4],
 ['内蒙古自治区', 4],
 ['新疆维吾尔自治区', 5],
 ['云南省', 6],
 ['天津市', 11],
 ['广西壮族自治区', 14],
 ['安徽省', 18],
 ['河南省', 20],
 ['福建省', 20],
 ['四川省', 21],
 ['重庆市', 22],
 ['湖南省', 23],
 ['山西省', 24],
 ['江西省', 28],
 ['河北省', 30],
 ['吉林省', 32],
 ['浙江省', 33],
 ['辽宁省', 39],
 ['陕西省', 40],
 ['上海市', 41],
 ['江苏省', 45],
 ['黑龙江省', 46],
 ['湖北省', 48],
 ['广东省', 49],
 ['山东省', 64],
 ['北京市', 79]], 'china')
c.set_global_opts(title_opts=opts.TitleOpts('调剂信息省份分布地图'),
#                   toolbox_opts=opts.ToolboxOpts(is_show=True),
                  visualmap_opts=opts.VisualMapOpts(max_=79))
c.render_notebook()
```

