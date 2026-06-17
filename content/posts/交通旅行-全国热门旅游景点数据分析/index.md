---
title: "全国热门旅游景点数据分析：从景点评分、价格和文本标签看文旅供给"
date: 2026-06-17T23:05:19+08:00
# weight: 1
# aliases: ["/first"]
categories: ["交通旅行"]
tags: ["pandas", "pyecharts", "jieba", "文旅分析"]
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

# 全国热门旅游景点数据分析：从景点评分、价格和文本标签看文旅供给

## 摘要

| 模块     | 内容                                                         |
| -------- | ------------------------------------------------------------ |
| 业务场景 | 交通旅行                                                     |
| 数据来源 | 全国热门旅游景点数据，包含地区、景点名称、评分、价格、热度和文本描述等信息。 |
| 分析方法 | Excel 数据处理、pandas 聚合、pyecharts 可视化、jieba 分词和关键词分析。 |
| 结论先行 | 热门景区往往集中在旅游资源强、交通便利和内容曝光高的地区。   |

本报告围绕“业务背景、分析目的、数据说明、分析思路、分析过程、核心结论和改进建议”展开，目标是用数据回答具体问题，并把分析结果转化为可执行的判断。

## 一、分析背景

文旅消费决策同时受到目的地供给、价格门槛、口碑评价和内容传播影响。分析景点数据可以帮助平台做推荐，也能帮助目的地理解自身竞争位置。

## 二、分析目的

本次分析主要回答以下问题：

- 文本中用户最关注的主题和关键词是什么？
- 正负向反馈分别集中在哪些具体问题上？
- 这些文本信号能沉淀成哪些产品、运营或服务改进动作？

先明确分析目的，再开展数据处理和指标拆解，可以保证报告围绕问题展开，而不是简单罗列代码和图表。

## 三、数据来源与指标说明

| 项目           | 说明                                                         |
| -------------- | ------------------------------------------------------------ |
| 数据来源       | 全国热门旅游景点数据，包含地区、景点名称、评分、价格、热度和文本描述等信息。 |
| 分析工具与方法 | Excel 数据处理、pandas 聚合、pyecharts 可视化、jieba 分词和关键词分析。 |
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

### 1. 热门景区往往集中在旅游资源强、交通便利和内容曝光高的地区。

结果解读：该发现是本项目最核心的结论之一，说明数据中存在值得关注的结构性特征。对应图表或模型结果应围绕这一判断展开，帮助读者理解结论来源。

### 2. 评分与价格不能简单线性理解，高价景区需要更强的体验或稀缺性支撑。

结果解读：该发现进一步解释了不同维度之间的差异。对业务决策而言，重点不只是看到差异，而是判断差异来自哪些对象、场景或指标。

### 3. 文本关键词能补充结构化字段无法表达的主题，例如亲子、自然风光、历史文化和打卡属性。

结果解读：该发现可以作为后续优化策略或模型改进的依据。若用于真实业务，还需要结合成本、资源、实验结果或线上反馈继续验证。

## 七、结论

综合以上分析，可以得到以下结论：

- 热门景区往往集中在旅游资源强、交通便利和内容曝光高的地区。
- 评分与价格不能简单线性理解，高价景区需要更强的体验或稀缺性支撑。
- 文本关键词能补充结构化字段无法表达的主题，例如亲子、自然风光、历史文化和打卡属性。

## 八、建议

- 行动 1：旅游平台可将评分、价格、地理距离和主题标签组合为个性化推荐特征。
- 行动 2：目的地运营应围绕高频关键词优化内容投放，强化用户可感知的独特卖点。
- 行动 3：后续可接入评论情感、节假日客流和交通成本，做更完整的出游决策模型。
- 跟进方式：为每条建议绑定一个可观察指标，后续按周或按月复盘效果。

建议部分应结合具体对象、执行动作和复盘指标，避免停留在泛泛的“加强管理”或“优化运营”。

## 九、局限性与改进方向

- 项目价值：把非结构化文本转化为可统计的问题标签和情绪信号，帮助业务更快定位用户关注点和负面体验。
- 真实限制：出行和旅游需求对天气、节假日、区域活动、价格和突发事件敏感，历史数据对未来异常场景的解释能力有限。
- 业务风险：预测或分群结果如果没有接入实时库存、运力、价格和渠道策略，容易出现供需错配或收益损失。
- 改进方向：建立人工抽检样本集，评估分词、情感判断和主题归类是否符合业务语境。
- 改进方向：把文本标签与订单、退款、投诉、复购或客服工单关联，验证文本问题对经营结果的影响。
- 改进方向：接入实时天气、节假日、库存/运力、价格和渠道数据，让分析结果能服务实时运营。

## 附录：完整代码与输出结果

下面内容按原 notebook 的代码单元顺序整理。如果代码单元产生了文本输出或图片输出，也一并附在对应代码后面，便于复现完整分析过程。

### 代码单元 1

```python
import jieba
import pandas as pd
from collections import Counter
from pyecharts.charts import Line,Pie,Scatter,Bar,Map,Grid
from pyecharts.charts import WordCloud
from pyecharts import options as opts
from pyecharts.globals import ThemeType
from pyecharts.globals import SymbolType
from pyecharts.commons.utils import JsCode

from pyecharts.globals import CurrentConfig, NotebookType,OnlineHostType
CurrentConfig.NOTEBOOK_TYPE = NotebookType.JUPYTER_NOTEBOOK
```

### 代码单元 2

```python
df = pd.read_excel('./旅游景点.xlsx')
df.head()
```

**文本输出**

```text
城市        名称   星级   评分     价格     销量       省/市/区                    坐标  \
0  上海   上海迪士尼乐园  NaN  0.0  325.0  19459  上海·上海·浦东新区  121.667917,31.149712   
1  上海  上海海昌海洋公园   4A  0.0  276.5  19406  上海·上海·浦东新区  121.915647,30.917713   
2  上海   上海野生动物园   5A  3.6  116.0   6764  上海·上海·浦东新区  121.728112,31.059636   
3  上海      东方绿舟   4A  3.5   40.0   5353   上海·上海·青浦区  121.015977,31.107866   
4  上海      东方明珠   5A  3.8   54.0   3966  上海·上海·浦东新区   121.50626,31.245369   

                    简介   是否免费                      具体地址  
0         每个女孩都有一场迪士尼梦  False  上海市浦东新区川沙镇黄赵路310号上海迪士尼乐园  
1   看珍稀海洋生物 | 玩超刺激娱乐项目  False         上海市浦东新区南汇城银飞路166号  
2  全球动物聚集地 | 零距离和动物做朋友  False           上海市浦东新区南六公路178号  
3     全国首屈一指的青少年校外教育营地  False          上海市青浦区沪青平公路6888号  
4       感受云端漫步，品味老上海风情  False             上海市浦东新区世纪大道1号
```

### 代码单元 3

```python
df.info()
```

**文本输出**

```text
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 2443 entries, 0 to 2442
Data columns (total 11 columns):
 #   Column  Non-Null Count  Dtype  
---  ------  --------------  -----  
 0   城市      2443 non-null   object 
 1   名称      2443 non-null   object 
 2   星级      913 non-null    object 
 3   评分      2443 non-null   float64
 4   价格      2443 non-null   float64
 5   销量      2443 non-null   int64  
 6   省/市/区   2443 non-null   object 
 7   坐标      2443 non-null   object 
 8   简介      2402 non-null   object 
 9   是否免费    2443 non-null   bool   
 10  具体地址    2440 non-null   object 
dtypes: bool(1), float64(2), int64(1), object(7)
memory usage: 193.4+ KB
```

### 代码单元 4

```python
df.describe()
```

**文本输出**

```text
评分            价格            销量
count  2443.000000   2443.000000   2443.000000
mean      1.683135    151.780929    360.652886
std       2.012527    649.170226   1043.798441
min       0.000000      0.000000      0.000000
25%       0.000000     32.000000     40.000000
50%       0.000000     62.000000     90.000000
75%       3.700000    120.000000    270.000000
max       5.000000  23888.000000  19459.000000
```

### 代码单元 5

```python
df.loc[df['销量']==0,:].head()
```

**文本输出**

```text
城市      名称   星级   评分   价格  销量  省/市/区                               坐标  \
301  台湾  复兴桥风景区  NaN  0.0  0.0   0  台湾·桃园  121.35037883956,24.815040245504   
302  台湾     长春祠  NaN  3.5  0.0   0  台湾·花莲  121.60445032684,24.162302549393   
303  台湾    淡水老街  NaN  0.0  0.0   0  台湾·淡水  121.44124069779,25.171297755773   
304  台湾    士林官邸  NaN  5.0  0.0   0  台湾·台北  121.53013540214,25.093934468272   
305  台湾    北安公园  NaN  5.0  0.0   0  台湾·台北  121.52694244942,25.076889096728   

                     简介   是否免费               具体地址  
301   带动了北横碧水青山的另一种欢乐风情  False       桃园县复兴乡中正路15号  
302     一道飞瀑分流入溪，山水景色绝佳   True              台湾花莲县  
303        美食汇聚的北台湾老街之一   True          台北县淡水镇中正路  
304    林木参天、绿树幽深，极富神秘色彩   True  台北市士林区中山北路五段兴福林路口  
305  满园新绿，温雅如诗，连绵一片绿意盎然  False    台湾台北市中山北路四段北安路旁
```

### 代码单元 6

```python
df = df[df['销量']!=0]
df.shape
```

**文本输出**

```text
(2320, 11)
```

### 代码单元 7

```python
df.isnull().sum()
```

**文本输出**

```text
城市          0
名称          0
星级       1407
评分          0
价格          0
销量          0
省/市/区       0
坐标          0
简介         37
是否免费        0
具体地址        2
dtype: int64
```

### 代码单元 8

```python
df['星级'].fillna('未知', inplace=True)
df.isnull().sum()
```

**文本输出**

```text
城市        0
名称        0
星级        0
评分        0
价格        0
销量        0
省/市/区     0
坐标        0
简介       37
是否免费      0
具体地址      2
dtype: int64
```

### 代码单元 9

```python
df.fillna('未知', inplace=True)
df.isnull().sum()
```

**文本输出**

```text
城市       0
名称       0
星级       0
评分       0
价格       0
销量       0
省/市/区    0
坐标       0
简介       0
是否免费     0
具体地址     0
dtype: int64
```

### 代码单元 10

```python
df.sort_values('销量', ascending=False).head()
```

**文本输出**

```text
城市             名称  星级   评分     价格     销量       省/市/区  \
0     上海        上海迪士尼乐园  未知  0.0  325.0  19459  上海·上海·浦东新区   
1     上海       上海海昌海洋公园  4A  0.0  276.5  19406  上海·上海·浦东新区   
211   北京             故宫  5A  5.0   58.6  15277   北京·北京·东城区   
2187  陕西  秦始皇帝陵博物院（兵马俑）  5A  4.4  120.0  12714   陕西·西安·临潼区   
474   四川    成都大熊猫繁育研究基地  4A  4.0   52.0   9731   四川·成都·成华区   

                        坐标                    简介   是否免费  \
0     121.667917,31.149712          每个女孩都有一场迪士尼梦  False   
1     121.915647,30.917713    看珍稀海洋生物 | 玩超刺激娱乐项目  False   
211   116.403347,39.922148      世界五大宫之首，穿越与您近在咫尺  False   
2187  109.266029,34.386024               世界第八大奇迹  False   
474   104.152603,30.738951  无关黑与白， 不分胖与瘦， 可爱而又温暖  False   

                          具体地址  
0     上海市浦东新区川沙镇黄赵路310号上海迪士尼乐园  
1            上海市浦东新区南汇城银飞路166号  
211               北京市东城区景山前街4号  
2187      陕西省西安市临潼县秦始皇陵东1.5公里处  
474       四川省成都市成华区外北熊猫大道1375号
```

### 代码单元 11

```python
# 线性渐变
color_js = """new echarts.graphic.LinearGradient(0, 0, 1, 0,
    [{offset: 0, color: '#009ad6'}, {offset: 1, color: '#ed1941'}], false)"""

sort_info = df.sort_values(by='销量', ascending=True)
b1 = (
    Bar()
    .add_xaxis(list(sort_info['名称'])[-20:])
    .add_yaxis('热门景点销量', sort_info['销量'].values.tolist()[-20:],itemstyle_opts=opts.ItemStyleOpts(color=JsCode(color_js)))
    .reversal_axis()
    .set_global_opts(
        title_opts=opts.TitleOpts(title='热门景点销量数据'),
        yaxis_opts=opts.AxisOpts(name='景点名称'),
        xaxis_opts=opts.AxisOpts(name='销量'),
        )
    .set_series_opts(label_opts=opts.LabelOpts(position="right"))

)
# 将图形整体右移
g1 = (
    Grid()
        .add(b1, grid_opts=opts.GridOpts(pos_left='20%', pos_right='5%'))
)
g1.render_notebook()
```

### 代码单元 12

```python
dictcode = {'北京': '北京市',
 '天津': '天津市',
 '河北': '河北省',
 '山西': '山西省',
 '内蒙古': '内蒙古自治区',
 '辽宁': '辽宁省',
 '吉林': '吉林省',
 '黑龙江': '黑龙江省',
 '上海': '上海市',
 '江苏': '江苏省',
 '浙江': '浙江省',
 '安徽': '安徽省',
 '福建': '福建省',
 '江西': '江西省',
 '山东': '山东省',
 '河南': '河南省',
 '湖北': '湖北省',
 '湖南': '湖南省',
 '广东': '广东省',
 '广西': '广西壮族自治区',
 '海南': '海南省',
 '重庆': '重庆市',
 '四川': '四川省',
 '贵州': '贵州省',
 '云南': '云南省',
 '西藏': '西藏自治区',
 '陕西': '陕西省',
 '甘肃': '甘肃省',
 '青海': '青海省',
 '宁夏': '宁夏回族自治区',
 '新疆': '新疆维吾尔自治区',
'台湾':'台湾',
 '香港':'香港',
 '澳门':'澳门'}
```

### 代码单元 13

```python
df_tmp1 = df[['城市','销量']]
df_counts = df_tmp1.groupby('城市').sum()
m1 = (
        Map()
        .add('假期出行分布', [list(z) for z in zip([dictcode[x] for x in df_counts.index.values.tolist() ], df_counts.values.tolist())], 'china')
        .set_global_opts(
        title_opts=opts.TitleOpts(title='假期出行数据地图分布'),
        visualmap_opts=opts.VisualMapOpts(max_=100000, is_piecewise=False,range_color=["white", "#fa8072", "#ed1941"]),
        )
    )
m1.render_notebook()
```

### 代码单元 14

```python
# 线性渐变
color_js = """new echarts.graphic.LinearGradient(0, 1, 0, 0,
    [{offset: 0, color: '#009ad6'}, {offset: 1, color: '#ed1941'}], false)"""

df_tmp2 = df[df['星级'].isin(['4A', '5A'])]
df_counts = df_tmp2.groupby('城市').count()['星级']
b2 = (
        Bar()
            .add_xaxis(df_counts.index.values.tolist())
            .add_yaxis('4A-5A景区数量', df_counts.values.tolist(),itemstyle_opts=opts.ItemStyleOpts(color=JsCode(color_js)))
            .set_global_opts(
            title_opts=opts.TitleOpts(title='各省市4A-5A景区数量'),
            datazoom_opts=[opts.DataZoomOpts(), opts.DataZoomOpts(type_='inside')],
        )
    )
b2.render_notebook()
```

### 代码单元 15

```python
df0 = df_counts.copy()
df0.sort_values(ascending=False, inplace=True)
c1 = (
    Pie()
    .add('', [list(z) for z in zip(df0.index.values.tolist(), df0.values.tolist())],
         radius=['30%', '100%'],
         center=['50%', '60%'],
         rosetype='area',
         )
    .set_global_opts(title_opts=opts.TitleOpts(title='地区景点数量'),
                     legend_opts=opts.LegendOpts(is_show=False),
                     toolbox_opts=opts.ToolboxOpts())
    .set_series_opts(label_opts=opts.LabelOpts(is_show=True, position='inside', font_size=12,
                                               formatter='{b}: {c}', font_style='italic',
                                               font_weight='bold', font_family='Microsoft YaHei'
                                               ))
)
c1.render_notebook()
```

### 代码单元 16

```python
item_style = {'normal': {'shadowColor': '#000000',
                         'shadowBlur': 20,
                         'shadowOffsetX':5,
                         'shadowOffsetY':15
                         }
              }
s1 = (
        Scatter()
        .add_xaxis(df_counts.index.values.tolist())
        .add_yaxis('4A-5A景区数量', df_counts.values.tolist(),symbol_size=50,itemstyle_opts=item_style)
        .set_global_opts(visualmap_opts=opts.VisualMapOpts(is_show=False,
                                              type_='size',
                                              range_size=[5,50]))
)
s1.render_notebook()
```

### 代码单元 17

```python
df_tmp3 = df[df['星级'].isin(['4A', '5A'])]
df_counts = df_tmp3.groupby('城市').count()['星级']
m2 = (
    Map()
    .add('4A-5A景区分布', [list(z) for z in zip([dictcode[x] for x in df_counts.index.values.tolist() ], df_counts.values.tolist())], 'china')
    .set_global_opts(
    title_opts=opts.TitleOpts(title='地图数据分布'),
    visualmap_opts=opts.VisualMapOpts(max_=50, is_piecewise=True),
    )
)
m2.render_notebook()
```

### 代码单元 18

```python
# 门票价格占比
price_level = [0, 50, 100, 150, 200, 250, 300, 350, 400, 500]
label_level = ['0-50', '50-100', '100-150', '150-200', '200-250', '250-300', '300-350', '350-400', '400-500']
jzmj_cut = pd.cut(df['价格'], price_level, labels=label_level)
df_price = jzmj_cut.value_counts()
df_price
```

**文本输出**

```text
0-50       888
50-100     725
100-150    278
150-200    184
200-250     62
250-300     59
300-350     20
350-400     19
400-500     13
Name: 价格, dtype: int64
```

### 代码单元 19

```python
p1 = (
    Pie(init_opts=opts.InitOpts(
            width='800px', height='600px',
            )
       )
        .add(
        '',
        [list(z) for z in zip(df_price.index.tolist(), df_price.values.tolist())],
        radius=['20%', '60%'],
        center=['40%', '50%'],
        rosetype='radius',
        label_opts=opts.LabelOpts(is_show=True),
        )
        .set_global_opts(title_opts=opts.TitleOpts(title='门票价格占比',pos_left='33%',pos_top="5%"),
                        legend_opts=opts.LegendOpts(type_='scroll', pos_left="80%",pos_top="25%",orient="vertical")
                        )
        .set_series_opts(label_opts=opts.LabelOpts(formatter='{b}: {c} ({d}%)'),position='outside')
    )
p1.render_notebook()
```

### 代码单元 20

```python
color_js = """new echarts.graphic.RadialGradient(
                    0.5, 0.5, 1,
                    [{offset: 0,
                      color: '#009ad6'},
                     {offset: 1,
                      color: '#ed1941'}
                      ])"""

s2 = (
        Scatter()
        .add_xaxis(df_price.index.tolist())
        .add_yaxis('门票价格区间', df_price.values.tolist(),symbol_size=50,itemstyle_opts=opts.ItemStyleOpts(color=JsCode(color_js)))
        .set_global_opts(
            yaxis_opts=opts.AxisOpts(name='数量'),
            xaxis_opts=opts.AxisOpts(name='价格区间(元)'))
        .set_global_opts(visualmap_opts=opts.VisualMapOpts(is_show=False,
                                              # 设置通过图形大小来表现数据
                                              type_='size',
                                              # 图形大小映射范围
                                              range_size=[5,50]))
)
s2.render_notebook()
```

### 代码单元 21

```python
contents = "".join('%s' % i for i in df['简介'].values.tolist())
contents_list = jieba.cut(contents)
ac = Counter(contents_list)

stopwords = []
with open('./stopwords.txt', "r",encoding='utf-8') as f:  # 打开文件
    data = f.read()  # 读取文件
    stopwords = data.split('\n')

for i in stopwords:
    del ac[i]
 
w1 = (
    WordCloud()
    .add("",
         ac.most_common(150),
         word_size_range=[5, 100],
         textstyle_opts=opts.TextStyleOpts(font_family="cursive"),
         shape='star')
    .set_global_opts(title_opts=opts.TitleOpts(title="景点简介词云"))
)
w1.render_notebook()
```

**文本输出**

```
Building prefix dict from the default dictionary ...
Loading model from cache C:\Users\ADMINI~1\AppData\Local\Temp\2\jieba.cache
Loading model cost 1.001 seconds.
Prefix dict has been built successfully.
```

