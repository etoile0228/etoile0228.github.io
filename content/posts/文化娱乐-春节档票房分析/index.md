---
title: "春节档票房分析：从排片、地域和时段趋势理解档期竞争"
date: 2026-06-17T23:47:54+08:00
# weight: 1
# aliases: ["/first"]
categories: ["文化娱乐"]
tags: ["pyecharts", "春节档", "票房分析", "大屏"]
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

# 春节档票房分析：从排片、地域和时段趋势理解档期竞争

## 摘要

| 模块     | 内容                                                         |
| -------- | ------------------------------------------------------------ |
| 业务场景 | 文化娱乐                                                     |
| 数据来源 | 春节档票房详情、影片概览、三十日趋势、排片地域和院线分布数据。 |
| 分析方法 | 多表数据整合、pyecharts 大屏、趋势分析、院线和地域分布可视化。 |
| 结论先行 | 春节档票房高度依赖前几日排片和口碑扩散，趋势变化快。         |

本报告围绕“业务背景、分析目的、数据说明、分析思路、分析过程、核心结论和改进建议”展开，目标是用数据回答具体问题，并把分析结果转化为可执行的判断。

## 一、分析背景

春节档是电影市场最重要的竞争窗口，影片之间的差距不仅来自内容，也来自排片、地域覆盖、院线资源和口碑发酵。

## 二、分析目的

本次分析主要回答以下问题：

- 数据在时间、区域、类别或人群维度上呈现什么结构？
- 哪些图表最适合承载趋势、对比、分布和异常信息？
- 可视化结果如何帮助读者快速定位重点？

先明确分析目的，再开展数据处理和指标拆解，可以保证报告围绕问题展开，而不是简单罗列代码和图表。

## 三、数据来源与指标说明

| 项目           | 说明                                                         |
| -------------- | ------------------------------------------------------------ |
| 数据来源       | 春节档票房详情、影片概览、三十日趋势、排片地域和院线分布数据。 |
| 分析工具与方法 | 多表数据整合、pyecharts 大屏、趋势分析、院线和地域分布可视化。 |
| 重点分析指标   | 总量、占比、趋势、排名、区域分布、类别结构和异常变化。       |
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

- 先梳理展示对象和受众：判断这篇分析主要给业务、管理层还是面试官阅读。
- 根据问题选择图表：趋势看折线，结构看占比，对比看柱状图，空间分布看地图。
- 先用 pandas 聚合出清晰指标，再用可视化表达核心结论。
- 按照故事线组织图表顺序，避免图很多但结论分散。
- 每张图都配业务解释，让读者知道图表对应什么判断和行动。

## 五、数据处理过程

本项目的数据处理主要包括以下环节：

- 读取原始数据，检查字段类型、样本规模和基础统计信息。
- 处理缺失值、重复值、异常值或文本噪声，保证后续统计和建模结果可靠。
- 根据分析目标构造必要指标、标签或特征，并统一字段口径。
- 按业务维度进行分组、聚合、可视化或模型训练，为结论提供依据。

## 六、数据分析与结果

本部分按照“分析发现 -> 结果解读”的方式组织，重点说明数据体现出的现象及其业务含义。

### 1. 春节档票房高度依赖前几日排片和口碑扩散，趋势变化快。

结果解读：该发现是本项目最核心的结论之一，说明数据中存在值得关注的结构性特征。对应图表或模型结果应围绕这一判断展开，帮助读者理解结论来源。

### 2. 排片场次和票房贡献不一定完全匹配，上座率是判断资源效率的重要指标。

结果解读：该发现进一步解释了不同维度之间的差异。对业务决策而言，重点不只是看到差异，而是判断差异来自哪些对象、场景或指标。

### 3. 地域分布可以帮助片方识别强势市场和后续宣发重点。

结果解读：该发现可以作为后续优化策略或模型改进的依据。若用于真实业务，还需要结合成本、资源、实验结果或线上反馈继续验证。

## 七、结论

综合以上分析，可以得到以下结论：

- 春节档票房高度依赖前几日排片和口碑扩散，趋势变化快。
- 排片场次和票房贡献不一定完全匹配，上座率是判断资源效率的重要指标。
- 地域分布可以帮助片方识别强势市场和后续宣发重点。

## 八、建议

- 行动 1：片方应实时监控排片、上座率和口碑指标，动态调整宣发投放。
- 行动 2：影院应结合时段销售和观众结构优化黄金场分配。
- 行动 3：后续可加入社媒讨论量、评分和预售数据，构建票房预测模型。
- 跟进方式：为每条建议绑定一个可观察指标，后续按周或按月复盘效果。

建议部分应结合具体对象、执行动作和复盘指标，避免停留在泛泛的“加强管理”或“优化运营”。

## 九、局限性与改进方向

- 项目价值：把分散数据组织成趋势、结构、对比和空间分布，让管理者能快速识别重点对象和异常变化。
- 真实限制：票房、热度和评论数据受档期、宣发、排片、平台规则和口碑发酵影响，单一榜单不能完整解释内容表现。
- 业务风险：只追逐总票房或热度排名，可能忽略上座率、转化效率和长尾口碑，导致宣发资源配置失衡。
- 改进方向：将静态分析升级为可定期刷新的监控看板，并为异常指标设置阈值提醒。
- 改进方向：为关键图表补充下钻维度，使管理者能从总览进一步定位到地区、品类、用户或时间段。

## 附录：完整代码与输出结果

下面内容按原 notebook 的代码单元顺序整理。如果代码单元产生了文本输出或图片输出，也一并附在对应代码后面，便于复现完整分析过程。

### 代码单元 1

```python
import numpy as np
import pandas as pd
from collections import Counter
from pyecharts import options as opts
from pyecharts.charts import *
from pyecharts.commons.utils import JsCode
from pyecharts.globals import ThemeType
from pyecharts.components import Table
from pyecharts.options import ComponentTitleOpts
import datetime
```

### 代码单元 2

```python
data_haed = pd.read_excel(r"./春节档-电影票房表现概览.xlsx")
data_haed.head(1)
```

**文本输出**

```text
EntMovieID  DBOMovieID  EFMTMovieID       电影  \
0      709649       39085        40910  长津湖之水门桥   

                            英文电影名          导演                     主演  \
0  The Battle At Lake Changjin II  陈凯歌/徐克/林超贤  吴京/易烊千玺/朱亚文/李晨/韩东君/胡军   

   GenreMainID 主要类型       作品类型  ...     累计场次      累计人次   第一天观看人次  \
0           27   战争  战争/历史/主旋律  ...  1161376  52062562  11142376   

           首映票房          首周票房         首周末票房   猫眼想看人数  淘票票想看人数  猫眼评分  豆瓣评分  
0  6.384868e+08  2.530065e+09  9.807439e+08  1155811  1144344   9.6   7.2  

[1 rows x 31 columns]
```

### 代码单元 3

```python
data_haed["首映票房"] = data_haed["首映票房"].apply(lambda x: round(x/100000000, 2))
data_haed["首周票房"] = data_haed["首周票房"].apply(lambda x: round(x/100000000, 2))
data_haed["首周末票房"] = data_haed["首周末票房"].apply(lambda x: round(x/100000000, 2))

data_haed = data_haed.rename(columns={"首映票房": "首映票房/亿", "首周票房": "首周票房/亿", "首周末票房": "首周末票房/亿"})
```

### 代码单元 4

```python
data_haed.info()
```

**文本输出**

```text
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 10 entries, 0 to 9
Data columns (total 31 columns):
 #   Column       Non-Null Count  Dtype  
---  ------       --------------  -----  
 0   EntMovieID   10 non-null     int64  
 1   DBOMovieID   10 non-null     int64  
 2   EFMTMovieID  10 non-null     int64  
 3   电影           10 non-null     object 
 4   英文电影名        10 non-null     object 
 5   导演           10 non-null     object 
 6   主演           10 non-null     object 
 7   GenreMainID  10 non-null     int64  
 8   主要类型         10 non-null     object 
 9   作品类型         10 non-null     object 
 10  地区           10 non-null     object 
 11  电影时长         7 non-null      object 
 12  电影版本         10 non-null     object 
 13  点映日期         10 non-null     object 
 14  最晚结束日期       10 non-null     object 
 15  最新上映天数       10 non-null     int64  
 16  正式上映日期       10 non-null     object 
 17  数据截止日期       10 non-null     object 
 18  点映天数         10 non-null     int64  
 19  点映票房         10 non-null     float64
 20  累计票房         10 non-null     float64
 21  累计场次         10 non-null     int64  
 22  累计人次         10 non-null     int64  
 23  第一天观看人次      10 non-null     int64  
 24  首
... 输出过长，博客中已截断
```

### 代码单元 5

```python
data_haed = data_haed.drop(labels=["EntMovieID","DBOMovieID","EFMTMovieID","GenreMainID"],axis=1)
```

### 代码单元 6

```python
colums = list(data_haed)
print(colums)
```

**文本输出**

```text
['电影', '英文电影名', '导演', '主演', '主要类型', '作品类型', '地区', '电影时长', '电影版本', '点映日期', '最晚结束日期', '最新上映天数', '正式上映日期', '数据截止日期', '点映天数', '点映票房', '累计票房', '累计场次', '累计人次', '第一天观看人次', '首映票房/亿', '首周票房/亿', '首周末票房/亿', '猫眼想看人数', '淘票票想看人数', '猫眼评分', '豆瓣评分']
```

### 代码单元 7

```python
headers = colums
rows_all = data_haed[colums].apply(lambda x: list(x), axis=1).values.tolist()

table_all = Table()
attributes = {"class": "fl-table", "style": "margin: 0 auto"}  # 居中显示
table_all.add(headers, rows_all, attributes)
table_all.set_global_opts(
    title_opts=ComponentTitleOpts(title=f"春节档-电影详情数据概览", subtitle="（上下左右移动表格）")
)
table_all.render_notebook()
```

### 代码单元 8

```python
data_movie_time = pd.read_excel(r"./春节档-电影票房三十日时段详情.xls")
```

### 代码单元 9

```python
data_movie_time["当前票房/万"] = data_movie_time["当前票房/万"].apply(lambda x: round(x/10000000, 2))
data_movie_time["当前场次"] = data_movie_time["当前场次"].apply(lambda x: round(x/10000, 2))
data_movie_time["当前人次/万"] = data_movie_time["当前人次/万"].apply(lambda x: round(x/1000000, 2))
 
data_movie_time = data_movie_time.rename(columns={"当前票房/万": "当前票房/千万", "当前场次": "当前场次/万", "当前人次/万": "当前人次/百万"})
data_movie_time = data_movie_time[data_movie_time['日期']<='2022-02-07']
data_movie_time.head(2)
```

**文本输出**

```text
电影  EnMovieID  DBOMovieID          日期 星期  当前票房/千万  当前场次/万  当前人次/百万  \
0  长津湖之水门桥     709649       39085  2022-02-01  二    63.85   14.94    11.14   
1  长津湖之水门桥     709649       39085  2022-02-02  三    47.16   16.31     8.52   

    票房占比    黄金场票房/万  黄金场场次    黄金场人次  黄金场票房占比  黄金场场次占比  黄金场人次占比  
0  44.07  152743012  30348  2566593       24       20       23  
1  44.93  116514075  33048  2058020       25       20       24
```

### 代码单元 10

```python
data_movie_time['电影'].value_counts()
```

**文本输出**

```text
带你去见我妈          30
汪汪队立大功大电影       25
长津湖之水门桥          7
这个杀手不太冷静         7
奇迹·笨小孩           7
狙击手              7
熊出没·重返地球         7
四海               7
喜羊羊与灰太狼之筐出未来     7
小虎墩大英雄           7
Name: 电影, dtype: int64
```

### 代码单元 11

```python
movie_chang = data_movie_time[data_movie_time["电影"] == "长津湖之水门桥"]
```

### 代码单元 12

```python
line = Line(
    init_opts=opts.InitOpts(
        theme='light',
        width='1000px',
        height='600px')
)

line.add_xaxis(
    movie_chang["日期"].tolist()
)

colums = ["当前票房/千万", "当前人次/百万", "当前场次/万"]
for i in range(3):

    line.add_yaxis(
        colums[i],
        movie_chang[colums[i]],
        is_symbol_show=False,
        is_smooth=True,
        is_selected=True,
        areastyle_opts=opts.AreaStyleOpts(opacity=0.5),
        label_opts=opts.LabelOpts(is_show=False),
        z=100,
        linestyle_opts={
                "normal": {
                    "shadowColor": 'rgba(0, 0, 0, .5)',
                    "shadowBlur": 0,
                    "shadowOffsetY": 1,
                    "shadowOffsetX": 1,
                },
            },
    )

line.set_global_opts(
    xaxis_opts=opts.AxisOpts(
        boundary_gap=False,
        axislabel_opts=opts.LabelOpts(margin=30, color="black"),
        axistick_opts=opts.AxisTickOpts(is_show=False),),
    yaxis_opts=opts.AxisOpts(
        name='',
        axisline_opts=opts.AxisLineOpts(is_show=True),
        axistick_opts=opts.AxisTickOpts(is_show=False),
        splitline_opts=opts.SplitLineOpts(
            is_show=True,
            linestyle_opts=opts.LineStyleOpts(color='#483D8B'))
    ),
    tooltip_opts=opts.TooltipOpts(
        is_show=True, trigger='axis', axis_pointer_type='cross'),
    title_opts=opts.TitleOpts(title="长津湖上映后一周电影票房表现",# 标题
                            title_textstyle_opts=opts.TextStyleOpts(font_size=18), #主标题字体大小
                            subtitle="2022-02-01~2022-02-07", # 次坐标轴
                            pos_left='center'),# 标题位置
    legend_opts=opts.LegendOpts(
                                is_show=True,
                                pos_top=45,
                                orient="horizontal"
                                                ),  # 不显示图例

    graphic_opts=[
                opts.GraphicGroup(
                            graphic_item=opts.GraphicItem(id_='1',left="center", top="center", z=-1),
                            children=[
                                    opts.GraphicImage(graphic_item=opts.GraphicItem(id_="logo",
                                                                                    left='center',
                                                                                    z=-1),
                                                      graphic_imagestyle_opts=opts.GraphicImageStyleOpts(
                                        # 设置背景图片
                                        #image="https://img2.baidu.com/it/u=3979355417,3562690433&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=388",
                                        width=1000,
                                        height=600,
                                        opacity=0.5,)
                                    )
                                ]
                                )
                                ]
)

line.set_series_opts(
   
    markarea_opts=opts.MarkAreaOpts(
        is_silent=True,
        label_opts=opts.LabelOpts(position='bottom', color='#000000'),
        itemstyle_opts=opts.ItemStyleOpts(color='#1E90FF', opacity=0.2),
        data=[
            opts.MarkAreaItem(name="正式上映\n春节档", x=("2022-02-01", "2022-02-02")),
            # opts.MarkAreaItem(name="高峰期", x=("2021-10-05", "2021-10-07")),
            # opts.MarkAreaItem(name="第三周\n小高峰", x=("2021-10-15", "2021-10-17")),
        ]
    ),
)
line.set_colors(colors=['#80FFA5', '#00DDFF', '#FF0087'])
line.render_notebook()
```

### 代码单元 13

```python
# 读入数据
data = pd.read_excel(r"./春节档-票房详情.xlsx")
data.head(5)
```

**文本输出**

```text
日期            票房   票房环比      场次  场次环比        人次   人次环比  场均人次  平均票价  \
0  2022-02-07  5.216625e+08 -32.03  426462 -6.80  10938703 -29.49    26    48   
1  2022-02-06  7.674549e+08 -10.91  457564 -4.49  15514640  -9.52    34    49   
2  2022-02-05  8.613918e+08  -3.28  479079 -1.77  17146416  -1.40    36    50   
3  2022-02-04  8.906360e+08 -12.62  487703 -3.61  17390306  -9.49    36    51   
4  2022-02-03  1.019280e+09  -4.10  505980 -3.14  19214740  -1.60    38    53   

                当日票房冠军          服务费  
0  长津湖之水门桥￥19074万 占37%  48125189.04  
1  长津湖之水门桥￥28841万 占38%  57248675.54  
2  长津湖之水门桥￥33388万 占39%  68692473.25  
3  长津湖之水门桥￥35846万 占40%  74792791.97  
4  长津湖之水门桥￥43921万 占43%  91251155.02
```

### 代码单元 14

```python
def tranform_data(x):
    x = round(x / 10000, 2)
    return x

data['票房/(万)'] = data['票房'].apply(lambda x: tranform_data(x))
```

### 代码单元 15

```python
data['票房/(万)'] = data['票房'].apply(lambda x: tranform_data(x))
data_7 = data[data["日期"] >= "2022-02-01"]
```

### 代码单元 16

```python
bar = (
    Bar(init_opts=opts.InitOpts(
        theme='light',
        width='980px',
        height='500px'
    ))  # 设置图表大小
        .add_xaxis(xaxis_data=data_7['日期'].tolist())  # x轴
        .add_yaxis(
        series_name="场次",  # 柱形图系列名称
        y_axis=data_7['场次'].tolist(),  # 数据
        label_opts=opts.LabelOpts(is_show=False, position='top', formatter="{c}"),  # 显示数据标签
        itemstyle_opts=opts.AreaStyleOpts(
            opacity=0.8,
            color=JsCode("""
                            new echarts.graphic.LinearGradient(
                            0, 0, 0, 1,
                            [{offset: 0, color: 'rgba(30,144,255)'},
                             {offset: 1, color: 'rgba(30,144,255,0.5)'}],
                              false)
                            """)
        )
    )
        .add_yaxis(
        series_name="人次",  # 柱形图系列名称
        y_axis=data_7['人次'].tolist(),  # 数据
        label_opts=opts.LabelOpts(is_show=False, position='top', formatter="{c}"),  # 显示数据标签
        itemstyle_opts=opts.AreaStyleOpts(
            opacity=0.8,
            color=JsCode("""
                             new echarts.graphic.LinearGradient(
                                           0, 0, 0, 1,
                                           [{offset: 0, color: '#ed556a'},
                                            {offset: 1, color: '#ee3f4d'}],
                                           false)
                           """)
        )
    )

        .extend_axis(  # 设置次坐标轴
        yaxis=opts.AxisOpts(
            name="",  # 次坐标轴名称
            type_="value",  # 次坐标手类型
            min_=-4000,  # 最小值
            max_=200000,  # 最大值
            is_show=False,  # 是否显示
            axisline_opts=opts.AxisLineOpts(is_show=False,  # y轴线不显示
                                            linestyle_opts=opts.LineStyleOpts(color='#00ca95')),  # 设置线颜色, 字体颜色也变
            axistick_opts=opts.AxisTickOpts(is_show=False),  # 刻度线不显示
            axislabel_opts=opts.LabelOpts(formatter="{value}"),  # 次坐标轴数据显示格式
        )
    )

        .set_global_opts(title_opts=opts.TitleOpts(title="2022年春节电影票房大盘",  # 标题
                                                   title_textstyle_opts=opts.TextStyleOpts(font_size=20),  # 主标题字体大小
                                                   subtitle="2022-02-01~2022-02-07",  # 次坐标轴
                                                   pos_left='center'),  # 标题位置
                         legend_opts=opts.LegendOpts(
                             is_show=True,
                             pos_top=50,
                             orient="horizontal"
                         ),  # 不显示图例
                         tooltip_opts=opts.TooltipOpts(
                             trigger="axis",
                             axis_pointer_type="shadow"
                         ),  # 提示框
                         xaxis_opts=opts.AxisOpts(name='',
                                                  type_='category',
                                                  axislabel_opts=opts.LabelOpts(rotate=360),
                                                  ),
                         yaxis_opts=opts.AxisOpts(type_="value",  # y轴类型
                                                  is_show=False,
                                                  # max_=5000000,
                                                  name='',  # y轴名称
                                                  name_location='middle',  # y轴名称位置
                                                  name_gap=70,  # y轴名称距离轴线距离
                                                  axistick_opts=opts.AxisTickOpts(is_show=False),  # 刻度线
                                                  axisline_opts=opts.AxisLineOpts(is_show=True),  # y轴线
                                                  splitline_opts=opts.SplitLineOpts(is_show=True),  # y轴网格线
                                                  axislabel_opts=opts.LabelOpts(formatter="{value}")),  # 轴标签显示方式
                         )
)

line = (
    Line()
        .add_xaxis(xaxis_data=data_7['日期'].tolist())  # x轴
        .add_yaxis(
        series_name="票房/(万)",  # 名称
        yaxis_index=1,  # 次坐标
        is_smooth=True,  # 线条样式  , 是否设置成圆滑曲线
        y_axis=data_7['票房/(万)'].tolist(),
        itemstyle_opts={
            "normal": {
                "color": JsCode(
                    """new echarts.graphic.LinearGradient(0, 0, 0, 1, [{
                                        offset: 0,
                                        color: '#2486b9'
                                    }, {
                                        offset: 1,
                                        color: '#FF00FF'
                                    }], false)""", ),
                "opacity": 0.7,
                "barBorderRadius": [45, 45, 45, 45],
                "shadowColor": 'rgb(0, 160, 221)',
            }},
        linestyle_opts={
            'normal': {
                'width': 4,
                'shadowColor': 'rgba(0, 0, 0, 0.5)',
                'shadowBlur': 5,
                'shadowOffsetY': 10,
                'shadowOffsetX': 10,
                'curve': 0.7,
                'color': '#2486b9'
            }
        },
        label_opts=opts.LabelOpts(is_show=False),  # 显示数据标签
    )
)

bar.overlap(line)  # 图表组合
bar.render_notebook()
```

### 代码单元 17

```python
data = pd.read_excel(r'./春节档-电影票房表现概览.xlsx')

data["累计票房"] = data["累计票房"].apply(lambda x: round(x / 10000000, 2))
data["累计场次"] = data["累计场次"].apply(lambda x: round(x / 10000, 2))
data["累计人次"] = data["累计人次"].apply(lambda x: round(x / 1000000, 2))

data = data.rename(columns={"累计票房": "累计票房/千万", "累计场次": "累计场次/万", "累计人次": "累计人次/百万"})
data = data[data['正式上映日期'] == '2022-02-01']
data.head(1)
```

**文本输出**

```text
EntMovieID  DBOMovieID  EFMTMovieID       电影  \
0      709649       39085        40910  长津湖之水门桥   

                            英文电影名          导演                     主演  \
0  The Battle At Lake Changjin II  陈凯歌/徐克/林超贤  吴京/易烊千玺/朱亚文/李晨/韩东君/胡军   

   GenreMainID 主要类型       作品类型  ...  累计场次/万 累计人次/百万   第一天观看人次          首映票房  \
0           27   战争  战争/历史/主旋律  ...  116.14   52.06  11142376  6.384868e+08   

           首周票房         首周末票房   猫眼想看人数  淘票票想看人数  猫眼评分  豆瓣评分  
0  2.530065e+09  9.807439e+08  1155811  1144344   9.6   7.2  

[1 rows x 31 columns]
```

### 代码单元 18

```python
movies = data['电影'].tolist()
movies
```

**文本输出**

```text
['长津湖之水门桥',
 '这个杀手不太冷静',
 '奇迹·笨小孩',
 '狙击手',
 '熊出没·重返地球',
 '四海',
 '喜羊羊与灰太狼之筐出未来',
 '小虎墩大英雄']
```

### 代码单元 19

```python
bar_china = (
    Bar(init_opts=opts.InitOpts(width="1200px", height="600px", theme='light'))  # 设置图表大小
        .add_xaxis(xaxis_data=data['电影'].tolist())  # x轴
        .add_yaxis(
        series_name="累计票房/千万",  # 柱形图系列名称
        stack='stack1',
        y_axis=data['累计票房/千万'].tolist(),  # 数据
        label_opts=opts.LabelOpts(is_show=False, position='top', formatter="{c} /千万"),  # 显示数据标签
        itemstyle_opts={
            "normal": {
                "color": JsCode("""new echarts.graphic.LinearGradient(0, 0, 0, 1, [{
                    offset: 0,
                    color: '#126bae'
                }, {
                    offset: 1,
                    color: '#619ac3'
                }], false)""", ),
                "opacity": 0.8,
                #                 "barBorderRadius": [20, 20, 0, 0],
                'shadowBlur': 4,
                'shadowColor': 'rgba(0, 0, 0, 0.3)',
                'shadowOffsetX': 5,
                'shadowOffsetY': 5,
                'borderColor': 'rgb(220,220,220)',
                'borderWidth': 1
            }}
    )
        .add_yaxis(
        series_name="累计人次/百万",  # 柱形图系列名称
        stack='stack1',
        y_axis=data['累计人次/百万'].tolist(),  # 数据
        label_opts=opts.LabelOpts(is_show=False, position='top', formatter="{c} /百万"),  # 显示数据标签
        itemstyle_opts={
            "normal": {
                "color": JsCode("""new echarts.graphic.LinearGradient(0, 0, 0, 1, [{
                    offset: 0,
                    color: '#ea7293'
                }, {
                    offset: 1,
                    color: '#ec8aa4'
                }], false)""", ),
                "opacity": 0.8,
                #                 "barBorderRadius": [20, 20, 0, 0],
                'shadowBlur': 4,
                'shadowColor': 'rgba(0, 0, 0, 0.3)',
                'shadowOffsetX': 5,
                'shadowOffsetY': 5,
                'borderColor': 'rgb(220,220,220)',
                'borderWidth': 1
            }}
    )

        .add_yaxis(
        series_name="累计场次/万",  # 柱形图系列名称
        stack='stack1',
        y_axis=data['累计场次/万'].tolist(),  # 数据
        label_opts=opts.LabelOpts(is_show=False, position='top', formatter="{c} /万"),  # 显示数据标签
        itemstyle_opts={
            "normal": {
                "color": JsCode("""new echarts.graphic.LinearGradient(0, 0, 0, 1, [{
                    offset: 0,
                    color: '#9eccab'
                }, {
                    offset: 1,
                    color: '#a4cab6'
                }], false)""", ),
                "opacity": 0.8,
                #                 "barBorderRadius": [20, 20, 0, 0],
                'shadowBlur': 4,
                'shadowColor': 'rgba(0, 0, 0, 0.3)',
                'shadowOffsetX': 5,
                'shadowOffsetY': 5,
                'borderColor': 'rgb(220,220,220)',
                'borderWidth': 1
            }}
    )

        .reversal_axis()
        # .set_series_opts(label_opts=opts.LabelOpts(position="right"))
        .set_global_opts(title_opts=opts.TitleOpts(title="春节档上映电影票房表现概览",  # 标题
                                                   title_textstyle_opts=opts.TextStyleOpts(font_size=20),  # 主标题字体大小
                                                   subtitle="",  # 次坐标轴
                                                   pos_left='center'),  # 标题位置
                         legend_opts=opts.LegendOpts(
                             is_show=True,
                             pos_top=30,
                             orient="horizontal"
                         ),  # 不显示图例
                         tooltip_opts=opts.TooltipOpts(
                             trigger="axis",
                             axis_pointer_type="shadow"
                         ),  # 提示框
                         yaxis_opts=opts.AxisOpts(name='',
                                                  type_='category',
                                                  #    axislabel_opts=opts.LabelOpts(rotate=30),
                                                  ),
                         xaxis_opts=opts.AxisOpts(type_="value",  # y轴类型
                                                  #   max_=5000000,
                                                  name='',  # y轴名称
                                                  name_location='middle',  # y轴名称位置
                                                  name_gap=70,  # y轴名称距离轴线距离
                                                  axistick_opts=opts.AxisTickOpts(is_show=False),  # 刻度线
                                                  axisline_opts=opts.AxisLineOpts(is_show=False),  # y轴线
                                                  splitline_opts=opts.SplitLineOpts(is_show=True),  # y轴网格线
                                                  axislabel_opts=opts.LabelOpts(formatter="{value}")),  # 轴标签显示方式
                         # datazoom_opts=opts.DataZoomOpts(is_zoom_lock=False,
                         #                                 orient="vertical")
                         )
)
bar_china.render_notebook()
```

### 代码单元 20

```python
data_move_diyu = pd.read_excel(r'./春节档-排片地域分布（场次）-top10影片.xlsx')
data_move_diyu.head(5)
```

**文本输出**

```text
日期    城市               电影     场次
0  2022-02-07  一线城市           CLevel      1
1  2022-02-07  一线城市        CityLevel   一线城市
2  2022-02-07  一线城市   709649|长津湖之水门桥  11802
3  2022-02-07  一线城市  708179|这个杀手不太冷静   9828
4  2022-02-07  一线城市    706338|奇迹·笨小孩   6181
```

### 代码单元 21

```python
data_move_diyu = data_move_diyu.drop(data_move_diyu[(data_move_diyu['电影'] == "CLevel") | (data_move_diyu['电影'] == "CityLevel")].index)
data_move_diyu["电影"] = data_move_diyu["电影"].apply(lambda x: x.split("|")[-1])
data_move_diyu.head(5)
```

**文本输出**

```text
日期    城市        电影     场次
2  2022-02-07  一线城市   长津湖之水门桥  11802
3  2022-02-07  一线城市  这个杀手不太冷静   9828
4  2022-02-07  一线城市    奇迹·笨小孩   6181
5  2022-02-07  一线城市       狙击手   5781
6  2022-02-07  一线城市  熊出没·重返地球   3034
```

### 代码单元 22

```python
data_move_diyu = data_move_diyu.fillna(0)
data_move_diyu['场次'] = data_move_diyu['场次'].astype(int)
```

### 代码单元 23

```python
one_city = data_move_diyu[(data_move_diyu['城市'] == '一线城市')]
two_city = data_move_diyu[(data_move_diyu['城市'] == '二线城市')]
three_city = data_move_diyu[(data_move_diyu['城市'] == '三线城市')]
four_city = data_move_diyu[(data_move_diyu['城市'] == '四线城市')]
five_city = data_move_diyu[(data_move_diyu['城市'] == '五线城市')]
one_city.head(5)
```

**文本输出**

```text
日期    城市        电影     场次
2  2022-02-07  一线城市   长津湖之水门桥  11802
3  2022-02-07  一线城市  这个杀手不太冷静   9828
4  2022-02-07  一线城市    奇迹·笨小孩   6181
5  2022-02-07  一线城市       狙击手   5781
6  2022-02-07  一线城市  熊出没·重返地球   3034
```

### 代码单元 24

```python
one_city_movie = one_city.groupby('电影')['场次'].sum().reset_index().sort_values('场次', ascending=False).reset_index(
            drop=True)[:10]
one_city_movie = one_city_movie.rename(columns = {'场次': '一线城市场次'})
two_city_movie = two_city.groupby('电影')['场次'].sum().reset_index().sort_values('场次', ascending=False).reset_index(
            drop=True)
two_city_movie = two_city_movie.rename(columns = {'场次': '二线城市场次'})
three_city_movie = three_city.groupby('电影')['场次'].sum().reset_index().sort_values('场次', ascending=False).reset_index(
            drop=True)
three_city_movie = three_city_movie.rename(columns = {'场次': '三线城市场次'})
four_city_movie = four_city.groupby('电影')['场次'].sum().reset_index().sort_values('场次', ascending=False).reset_index(
            drop=True)
four_city_movie = four_city_movie.rename(columns = {'场次': '四线城市场次'})
five_city_movie = five_city.groupby('电影')['场次'].sum().reset_index().sort_values('场次', ascending=False).reset_index(
            drop=True)
five_city_movie = five_city_movie.rename(columns = {'场次': '五线城市场次'})

move_top_10 = one_city_movie.merge(two_city_movie, how='left', on='电影').fillna(0)
move_top_10 = move_top_10.merge(three_city_movie, how='left', on='电影').fillna(0)
move_top_10 = move_top_10.merge(four_city_movie, how='left', on='电影').fillna(0)
move_top_10 = move_top_10.merge(five_city_movie, how='left', on='电影').fillna(0)
move_top_10
```

**文本输出**

```text
电影  一线城市场次  二线城市场次  三线城市场次  四线城市场次  五线城市场次
0       长津湖之水门桥  102185  358793  240544  222869  113999
1      这个杀手不太冷静   68584  250606  174082  161984   79804
2        奇迹·笨小孩   49719  177363  117773  115099   58419
3            四海   36326  115744   78934   75835   38944
4           狙击手   35058  106896   61403   52186   30055
5      熊出没·重返地球   25687  107346   83216   74974   37094
6  喜羊羊与灰太狼之筐出未来    9746   35138   24441   22786   11680
7        小虎墩大英雄    4361   14250    8826    9003    5254
8     汪汪队立大功大电影    1142    2926     881     370     101
9     好想去你的世界爱你     499    2035    1087    1015     476
```

### 代码单元 25

```python
paipian_top = pd.read_excel(r'./春节档-排片统计（场次）-top10影片.xlsx')
paipian_top.head(5)
```

**文本输出**

```text
日期        电影      场次     占比
0  2022-02-07   长津湖之水门桥  127296  29.85
1  2022-02-07  这个杀手不太冷静  106724  25.03
2  2022-02-07    奇迹·笨小孩   65424  15.34
3  2022-02-07       狙击手   46466  10.90
4  2022-02-07  熊出没·重返地球   42144   9.88
```

### 代码单元 26

```python
paipian_top.groupby('电影')['场次'].sum()
```

**文本输出**

```text
电影
喜羊羊与灰太狼之筐出未来     103791
四海               345783
奇迹·笨小孩           518373
好想去你的世界爱你          5112
小虎墩大英雄            41694
带你去见我妈              150
汪汪队立大功大电影          5420
熊出没·重返地球         328317
狙击手              285598
独家头条                 97
这个杀手不太冷静         735060
长津湖之水门桥         1038390
魔法满屋                220
魔法精灵                158
Name: 场次, dtype: int64
```

### 代码单元 27

```python
bar_diyu = (
    Bar(init_opts=opts.InitOpts(width="1200px", height="600px", theme='light')) # 设置图表大小
    .add_xaxis(xaxis_data=move_top_10['电影'].tolist())  # x轴
    .add_yaxis(
        series_name="一线城市",  #柱形图系列名称
        stack='stack1',
        y_axis=move_top_10['一线城市场次'].tolist(), # 数据
        label_opts=opts.LabelOpts(is_show=False,position='top',formatter="{c}"), # 显示数据标签
        itemstyle_opts=opts.ItemStyleOpts(color="#8e97e2",opacity=0.8),     # 柱形图颜色及透明度
        )
    .add_yaxis(
        series_name="二线城市",  #柱形图系列名称
        stack='stack1',
        y_axis=move_top_10['二线城市场次'].tolist(), # 数据
        label_opts=opts.LabelOpts(is_show=False,position='top',formatter="{c}"), # 显示数据标签
        itemstyle_opts=opts.ItemStyleOpts(color="#ed9b9b",opacity=0.8),     # 柱形图颜色及透明度
        )
    .add_yaxis(
        series_name="三线城市",  #柱形图系列名称
        stack='stack1',
        y_axis=move_top_10['三线城市场次'].tolist(), # 数据
        label_opts=opts.LabelOpts(is_show=False,position='top',formatter="{c}"), # 显示数据标签
        itemstyle_opts=opts.ItemStyleOpts(color="#4fc0cc",opacity=0.8),     # 柱形图颜色及透明度
        )
    .add_yaxis(
        series_name="四线城市",  #柱形图系列名称
        stack='stack1',
        y_axis=move_top_10['四线城市场次'].tolist(), # 数据
        label_opts=opts.LabelOpts(is_show=False,position='top',formatter="{c}"), # 显示数据标签
        itemstyle_opts=opts.ItemStyleOpts(color="#f7ce8f",opacity=0.8),     # 柱形图颜色及透明度
        )
    .add_yaxis(
        series_name="五线城市",  #柱形图系列名称
        stack='stack1',
        y_axis=move_top_10['五线城市场次'].tolist(), # 数据
        label_opts=opts.LabelOpts(is_show=False,position='top',formatter="{c}"), # 显示数据标签
        itemstyle_opts=opts.ItemStyleOpts(color="#7fa7c1",opacity=0.8),     # 柱形图颜色及透明度
        )
    .reversal_axis()
    # .set_series_opts(label_opts=opts.LabelOpts(position="right"))
    .set_global_opts(title_opts=[
            dict(
                text='春节档 - 排片地域分布（累计场次）',
                left='left',
                textStyle=dict(
                    color='#000',
                    fontSize=20)),
            dict(
                text='春节档 - 排片统计（累计场次）',
                left='60%',
                top='10%',
                textStyle=dict(
                    color='#000',
                    fontSize=16)),
        ],
                    legend_opts=opts.LegendOpts(
                                             is_show=False,),  # 不显示图例
                    tooltip_opts=opts.TooltipOpts(
                                             trigger="axis",
                                             axis_pointer_type="shadow"
                                             ),# 提示框
                    yaxis_opts=opts.AxisOpts(name='',
                                            type_='category',
                                            #    axislabel_opts=opts.LabelOpts(rotate=30),
                                               ),
                     xaxis_opts=opts.AxisOpts(type_="value", # y轴类型
                                            #   max_=5000000,
                                              name='', # y轴名称
                                              name_location='middle', # y轴名称位置
                                              name_gap=70,  # y轴名称距离轴线距离
                                              axistick_opts=opts.AxisTickOpts(is_show=False),   # 刻度线
                                              axisline_opts=opts.AxisLineOpts(is_show=False),   # y轴线
                                              splitline_opts=opts.SplitLineOpts(is_show=True),   # y轴网格线
                                              axislabel_opts=opts.LabelOpts(formatter="{value}")), # 轴标签显示方式
                                               )
)
pie = (Pie(init_opts=opts.InitOpts(theme='light'))
    .add('', [list(z) for z in zip(paipian_top.groupby('电影')['场次'].sum().index.tolist(),
        paipian_top.groupby('电影')['场次'].sum().values.tolist())],radius=['45','100'],center=['70%','40%'])
    .set_series_opts(label_opts=opts.LabelOpts(formatter='{b}：{c}  {d}%'))
    .set_global_opts(legend_opts=opts.LegendOpts(is_show=False))
    )
bar_diyu.overlap(pie)
bar_diyu.render_notebook()
```

### 代码单元 28

```python
t2 = Timeline(init_opts=opts.InitOpts(width="1200px", height="600px", theme='light'))
t2.add_schema(is_auto_play=True, is_loop_play=True, is_timeline_show=False, play_interval=1000)

for d in range(1,7):  # 指定多个月份
    
    one_city_movie = data_move_diyu[(data_move_diyu['城市'] == '一线城市') & (data_move_diyu['日期'] == f"2022-02-0{d}")]
    two_city_movie = data_move_diyu[(data_move_diyu['城市'] == '二线城市') & (data_move_diyu['日期'] == f"2022-02-0{d}")]
    three_city_movi = data_move_diyu[(data_move_diyu['城市'] == '三线城市') & (data_move_diyu['日期'] == f"2022-02-0{d}")]
    four_city_movi = data_move_diyu[(data_move_diyu['城市'] == '四线城市') & (data_move_diyu['日期'] == f"2022-02-0{d}")]
    five_city_movi = data_move_diyu[(data_move_diyu['城市'] == '五线城市') & (data_move_diyu['日期'] == f"2022-02-0{d}")]

    one_city_movie = one_city_movie.rename(columns = {'场次': '一线城市场次'})
    two_city_movie = two_city_movie.rename(columns = {'场次': '二线城市场次'})
    three_city_movie = three_city_movie.rename(columns = {'场次': '三线城市场次'})
    four_city_movie = four_city_movie.rename(columns = {'场次': '四线城市场次'})
    five_city_movie = five_city_movie.rename(columns = {'场次': '五线城市场次'})

    move_top_10 = one_city_movie.merge(two_city_movie, how='left', on='电影').fillna(0)
    move_top_10 = move_top_10.merge(three_city_movie, how='left', on='电影').fillna(0)
    move_top_10 = move_top_10.merge(four_city_movie, how='left', on='电影').fillna(0)
    move_top_10 = move_top_10.merge(five_city_movie, how='left', on='电影').fillna(0)

    move_top_10 = move_top_10.rename(columns={"日期_x": "日期", "城市_x": "城市"})

    paipian = paipian_top[(paipian_top['日期'] == f"2022-02-0{d}")][:10]

    bar_diyu_pie = (
    Bar(init_opts=opts.InitOpts(width="1200px", height="600px")) # 设置图表大小
        .add_xaxis(xaxis_data=move_top_10['电影'].tolist())  # x轴
        .add_yaxis(
                series_name="一线城市",  #柱形图系列名称
                stack='stack1',
                y_axis=move_top_10['一线城市场次'].tolist(), # 数据
                label_opts=opts.LabelOpts(is_show=False,position='top',formatter="{c}"), # 显示数据标签
                itemstyle_opts=opts.ItemStyleOpts(color="#8e97e2",opacity=0.8),     # 柱形图颜色及透明度
                )
        .add_yaxis(
                series_name="二线城市",  #柱形图系列名称
                stack='stack1',
                y_axis=move_top_10['二线城市场次'].tolist(), # 数据
                label_opts=opts.LabelOpts(is_show=False,position='top',formatter="{c}"), # 显示数据标签
                itemstyle_opts=opts.ItemStyleOpts(color="#ed9b9b",opacity=0.8),     # 柱形图颜色及透明度
                )
        .add_yaxis(
                series_name="三线城市",  #柱形图系列名称
                stack='stack1',
                y_axis=move_top_10['三线城市场次'].tolist(), # 数据
                label_opts=opts.LabelOpts(is_show=False,position='top',formatter="{c}"), # 显示数据标签
                itemstyle_opts=opts.ItemStyleOpts(color="#4fc0cc",opacity=0.8),     # 柱形图颜色及透明度
                )
        .add_yaxis(
                series_name="四线城市",  #柱形图系列名称
                stack='stack1',
                y_axis=move_top_10['四线城市场次'].tolist(), # 数据
                label_opts=opts.LabelOpts(is_show=False,position='top',formatter="{c}"), # 显示数据标签
                itemstyle_opts=opts.ItemStyleOpts(color="#f7ce8f",opacity=0.8),     # 柱形图颜色及透明度
                )
        .add_yaxis(
                series_name="五线城市",  #柱形图系列名称
                stack='stack1',
                y_axis=move_top_10['五线城市场次'].tolist(), # 数据
                label_opts=opts.LabelOpts(is_show=False,position='top',formatter="{c}"), # 显示数据标签
                itemstyle_opts=opts.ItemStyleOpts(color="#7fa7c1",opacity=0.8),     # 柱形图颜色及透明度
                )
        .reversal_axis()
        # .set_series_opts(label_opts=opts.LabelOpts(position="right"))
        .set_global_opts(title_opts=[
                dict(
                        text=f'2022-02-0{d} - 排片地域分布（场次）- 春节档',
                        left='left',
                        textStyle=dict(
                        color='#000',
                        fontSize=20)),
                dict(
                        text=f'2022-02-0{d} - 排片统计（场次）- 春节档',
                        left='60%',
                        top='10%',
                        textStyle=dict(
                        color='#000',
                        fontSize=16)),
                ],
                        legend_opts=opts.LegendOpts(
                                                is_show=False,),  # 不显示图例
                        tooltip_opts=opts.TooltipOpts(
                                                trigger="axis",
                                                axis_pointer_type="shadow"
                                                ),# 提示框
                        yaxis_opts=opts.AxisOpts(name='',
                                                type_='category',
                                                #    axislabel_opts=opts.LabelOpts(rotate=30),
                                                ),
                        xaxis_opts=opts.AxisOpts(type_="value", # y轴类型
                                                #   max_=5000000,
                                                name='', # y轴名称
                                                name_location='middle', # y轴名称位置
                                                name_gap=70,  # y轴名称距离轴线距离
                                                axistick_opts=opts.AxisTickOpts(is_show=False),   # 刻度线
                                                axisline_opts=opts.AxisLineOpts(is_show=False),   # y轴线
                                                splitline_opts=opts.SplitLineOpts(is_show=True),   # y轴网格线
                                                axislabel_opts=opts.LabelOpts(formatter="{value}")), # 轴标签显示方式
                                                )
        )
    pie = (Pie(init_opts=opts.InitOpts(theme='light'))
        .add('', [list(z) for z in zip(paipian['电影'].tolist(),
                paipian['场次'].tolist())],radius=['45','100'],center=['70%','40%'])
        .set_series_opts(label_opts=opts.LabelOpts(formatter='{b}：{c}  {d}%'))
        .set_global_opts(legend_opts=opts.LegendOpts(is_show=False))
        )
    bar_diyu_pie.overlap(pie)
    t2.add(bar_diyu_pie,'{}'.format(d))
t2.render_notebook()
```

### 代码单元 29

```python
from pyecharts.charts import Page
page = Page(layout=Page.DraggablePageLayout, page_title="大屏展示")

page.add(
   line,bar,bar_china,bar_diyu,t2)
# 先保存到test.html 然后打开，拖拽图片自定义布局， 之后记得点击左上角“save config”对布局文件进行保存。
# 会生成一个chart_config.json的文件，这其中包含了每个图表ID对应的布局位置
page.render('test.html')
```

**文本输出**

```text
'C:\\myproject\\cx_xiangmu\\Python数据分析\\上架\\2301-Python数据分析与可视化项目\\文化娱乐-春节档票房分析（Pyecharts大屏可视化）\\test.html'
```

### 代码单元 30

```python
# 然后运行下面这行代码。保存布局好的的仪表盘文件。
page.save_resize_html('test.html', cfg_file='chart_config.json', dest='大屏展示1.html')
```

**文本输出**

```
'<!DOCTYPE html>\n<html>\n<head>\n    <meta charset="UTF-8">\n    <title>大屏展示</title>\n            <script type="text/javascript" src="https://assets.pyecharts.org/assets/v5/echarts.min.js"></script>\n        <script type="text/javascript" src="https://assets.pyecharts.org/assets/v5/jquery.min.js"></script>\n        <script type="text/javascript" src="https://assets.pyecharts.org/assets/v5/jquery-ui.min.js"></script>\n        <script type="text/javascript" src="https://assets.pyecharts.org/assets/v5/ResizeSensor.js"></script>\n\n            <link rel="stylesheet"  href="https://assets.pyecharts.org/assets/v5/jquery-ui.css">\n\n</head>\n<body >\n    <style>.box {  } </style>\n        \n    <div class="box">\n                <div id="77044a02c6074383a62ce927c7fe70ca" class="chart-container" style="position: absolute; width: 1000.5px; height: 603.5px; top: 27.24609375px; left: 1242.98828125px;"></div>\n    <script>\n        var chart_77044a02c6074383a62ce927c7fe70ca = echarts.init(\n            document.getElementById(\'77044a02c6074383a62ce927c7fe70ca\'), \'light\', {renderer: \'canvas\'});\n        var option_77044a02c6074383a62ce927c7fe70ca = {\n    "animation": true,\n    "animati
... 输出过长
```

