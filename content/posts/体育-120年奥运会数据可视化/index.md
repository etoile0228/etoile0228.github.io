---
title: "120 年奥运会数据可视化：用 Pyecharts 讲清国家、项目和运动员趋势"
date: 2026-06-17T23:45:34+08:00
# weight: 1
# aliases: ["/first"]
categories: ["体育"]
tags: ["pyecharts", "可视化", "体育数据", "数据故事"]
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

# 120 年奥运会数据可视化：用 Pyecharts 讲清国家、项目和运动员趋势

## 摘要

| 模块     | 内容                                                         |
| -------- | ------------------------------------------------------------ |
| 业务场景 | 体育                                                         |
| 数据来源 | 历届奥运会运动员参赛与奖牌数据，包含年份、国家、项目、运动员性别、身高体重和奖牌结果。 |
| 分析方法 | pandas 数据整理、Pyecharts 交互图表、时间序列趋势、地图和类别对比可视化。 |
| 结论先行 | 长周期体育数据适合用时间轴展示，不同国家的奖牌表现和参赛规模会随历史阶段变化。 |

本报告围绕“业务背景、分析目的、数据说明、分析思路、分析过程、核心结论和改进建议”展开，目标是用数据回答具体问题，并把分析结果转化为可执行的判断。

## 一、分析背景

体育数据可视化的价值在于把长期变化讲清楚，例如国家竞技实力迁移、女子项目参与度提升和项目结构变化。

## 二、分析目的

本次分析主要回答以下问题：

- 数据在时间、区域、类别或人群维度上呈现什么结构？
- 哪些图表最适合承载趋势、对比、分布和异常信息？
- 可视化结果如何帮助读者快速定位重点？

先明确分析目的，再开展数据处理和指标拆解，可以保证报告围绕问题展开，而不是简单罗列代码和图表。

## 三、数据来源与指标说明

| 项目           | 说明                                                         |
| -------------- | ------------------------------------------------------------ |
| 数据来源       | 历届奥运会运动员参赛与奖牌数据，包含年份、国家、项目、运动员性别、身高体重和奖牌结果。 |
| 分析工具与方法 | pandas 数据整理、Pyecharts 交互图表、时间序列趋势、地图和类别对比可视化。 |
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

### 1. 长周期体育数据适合用时间轴展示，不同国家的奖牌表现和参赛规模会随历史阶段变化。

结果解读：该发现是本项目最核心的结论之一，说明数据中存在值得关注的结构性特征。对应图表或模型结果应围绕这一判断展开，帮助读者理解结论来源。

### 2. 性别、项目和国家维度的交叉分析可以呈现体育公平性和项目发展趋势。

结果解读：该发现进一步解释了不同维度之间的差异。对业务决策而言，重点不只是看到差异，而是判断差异来自哪些对象、场景或指标。

### 3. 运动员身体特征与项目类型相关，但解释时需要避免把相关性误读为因果。

结果解读：该发现可以作为后续优化策略或模型改进的依据。若用于真实业务，还需要结合成本、资源、实验结果或线上反馈继续验证。

## 七、结论

综合以上分析，可以得到以下结论：

- 长周期体育数据适合用时间轴展示，不同国家的奖牌表现和参赛规模会随历史阶段变化。
- 性别、项目和国家维度的交叉分析可以呈现体育公平性和项目发展趋势。
- 运动员身体特征与项目类型相关，但解释时需要避免把相关性误读为因果。

## 八、建议

- 行动 1：做公开展示时应把图表组织成故事线：参赛规模、国家表现、项目结构、运动员画像。
- 行动 2：体育媒体可用该类分析支持赛前专题、国家队复盘和项目科普。
- 行动 3：后续可加入主办国效应、GDP/人口数据和训练投入，做跨领域解释。
- 跟进方式：为每条建议绑定一个可观察指标，后续按周或按月复盘效果。

建议部分应结合具体对象、执行动作和复盘指标，避免停留在泛泛的“加强管理”或“优化运营”。

## 九、局限性与改进方向

- 项目价值：把分散数据组织成趋势、结构、对比和空间分布，让管理者能快速识别重点对象和异常变化。
- 真实限制：历史体育数据跨越时间长，国家名称、项目设置和参赛规则变化会影响纵向比较。
- 业务风险：如果只比较奖牌数量，可能忽略参赛规模、项目结构和主办国效应，导致结论过于简单。
- 改进方向：将静态分析升级为可定期刷新的监控看板，并为异常指标设置阈值提醒。
- 改进方向：为关键图表补充下钻维度，使管理者能从总览进一步定位到地区、品类、用户或时间段。

## 附录：完整代码与输出结果

下面内容按原 notebook 的代码单元顺序整理。如果代码单元产生了文本输出或图片输出，也一并附在对应代码后面，便于复现完整分析过程。

### 代码单元 1

```python
import pandas as pd
import numpy as np
import pyecharts
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.commons.utils import JsCode
```

### 代码单元 2

```python
athlete_data = pd.read_csv('./athlete_events.csv')
noc_region = pd.read_csv('./noc_regions.csv')

# 关联代表国家
data = pd.merge(athlete_data, noc_region, on='NOC', how='left')
data.head()
```

**文本输出**

```text
ID                      Name Sex   Age  Height  Weight            Team  \
0   1                 A Dijiang   M  24.0   180.0    80.0           China   
1   2                  A Lamusi   M  23.0   170.0    60.0           China   
2   3       Gunnar Nielsen Aaby   M  24.0     NaN     NaN         Denmark   
3   4      Edgar Lindenau Aabye   M  34.0     NaN     NaN  Denmark/Sweden   
4   5  Christine Jacoba Aaftink   F  21.0   185.0    82.0     Netherlands   

   NOC        Games  Year  Season       City          Sport  \
0  CHN  1992 Summer  1992  Summer  Barcelona     Basketball   
1  CHN  2012 Summer  2012  Summer     London           Judo   
2  DEN  1920 Summer  1920  Summer  Antwerpen       Football   
3  DEN  1900 Summer  1900  Summer      Paris     Tug-Of-War   
4  NED  1988 Winter  1988  Winter    Calgary  Speed Skating   

                              Event Medal       region notes  
0       Basketball Men's Basketball   NaN        China   NaN  
1      Judo Men's Extra-Lightweight   NaN        China   NaN  
2           Football Men's Football   NaN      Denmark   NaN  
3       Tug-Of-War Men's Tug-Of-War  Gold      Denmark   NaN  
4  Speed Skating Women's 500 metres   NaN  Net
... 输出过长，博客中已截断
```

### 代码单元 3

```python
medal_data = data.groupby(['Year', 'Season', 'region',
                                        'Medal'])['Event'].nunique().reset_index()
medal_data.columns = ['Year', 'Season', 'region', 'Medal', 'Nums']
medal_data = medal_data.sort_values(by="Year" , ascending=True)
```

### 代码单元 4

```python
def medal_stat(year, season='Summer'):
    t_data = medal_data[(medal_data['Year'] <= year) & (medal_data['Season'] == season)]
    t_data = t_data.groupby(['region', 'Medal'])['Nums'].sum().reset_index()
    t_data = t_data.set_index(['region', 'Medal']).unstack().reset_index().fillna(0, inplace=False)
    t_data = sorted([(row['region'][0], int(row['Nums']['Gold']), int(row['Nums']['Silver']), int(row['Nums']['Bronze']))
                                for _, row in t_data.iterrows()], key=lambda x: x[1]+x[2]+x[3], reverse=True)[:20]
    return t_data
```

### 代码单元 5

```python
year_list = sorted(list(set(medal_data['Year'].to_list())), reverse=True)

tl = Timeline(init_opts=opts.InitOpts(theme='dark', width='1000px', height='1000px'))
tl.add_schema(is_timeline_show=True,is_rewind_play=True, is_inverse=False,
             label_opts=opts.LabelOpts(is_show=False))

for year in year_list:
    t_data = medal_stat(year)[::-1]
    bar = (
        Bar(init_opts=opts.InitOpts())
            .add_xaxis([x[0] for x in t_data])
           .add_yaxis("铜牌🥉", [x[3] for x in t_data],
                        stack='stack1',
                        itemstyle_opts=opts.ItemStyleOpts(border_color='rgb(220,220,220)',color='rgb(218,165,32)'))
            .add_yaxis("银牌🥈", [x[2] for x in t_data],
                        stack='stack1',
                        itemstyle_opts=opts.ItemStyleOpts(border_color='rgb(220,220,220)',color='rgb(192,192,192)'))
            .add_yaxis("金牌🏅️", [x[1] for x in t_data],
                        stack='stack1',
                        itemstyle_opts=opts.ItemStyleOpts(border_color='rgb(220,220,220)',color='rgb(255,215,0)'))
            .set_series_opts(label_opts=opts.LabelOpts(is_show=True,
                                                       position='insideRight',
                                                       font_style='italic'),)
            .set_global_opts(
                title_opts=opts.TitleOpts(title="各国累计奖牌数（夏季奥运会）"),
                xaxis_opts=opts.AxisOpts(axislabel_opts=opts.LabelOpts(rotate=45)),
                legend_opts=opts.LegendOpts(is_show=True),
                graphic_opts=[opts.GraphicGroup(graphic_item=opts.GraphicItem(
                                                   rotation=JsCode("Math.PI / 4"),
                                                   bounding="raw",
                                                   right=110,
                                                   bottom=110,
                                                   z=100),
                                               children=[
                                                   opts.GraphicRect(
                                                       graphic_item=opts.GraphicItem(
                                                           left="center", top="center", z=100
                                                       ),
                                                       graphic_shape_opts=opts.GraphicShapeOpts(
                                                           width=400, height=50
                                                       ),
                                                       graphic_basicstyle_opts=opts.GraphicBasicStyleOpts(
                                                           fill="rgba(0,0,0,0.3)"
                                                       ),
                                                   ),
                                                   opts.GraphicText(
                                                       graphic_item=opts.GraphicItem(
                                                           left="center", top="center", z=100
                                                       ),
                                                       graphic_textstyle_opts=opts.GraphicTextStyleOpts(
                                                           text=year,
                                                           font="bold 26px Microsoft YaHei",
                                                           graphic_basicstyle_opts=opts.GraphicBasicStyleOpts(
                                                               fill="#fff"
                                                           ),
                                                       ),
                                                   ),
                                               ],
                                            )
                                    ],)
        .reversal_axis())
    tl.add(bar, year)

tl.render_notebook()
```

### 代码单元 6

```python
year_list = sorted(list(set(medal_data['Year'][medal_data.Season=='Winter'].to_list())), reverse=True)

tl = Timeline(init_opts=opts.InitOpts(theme='dark', width='1000px', height='1000px'))
tl.add_schema(is_timeline_show=True,is_rewind_play=True, is_inverse=False,
             label_opts=opts.LabelOpts(is_show=False))

for year in year_list:
    t_data = medal_stat(year, 'Winter')[::-1]
    bar = (
        Bar(init_opts=opts.InitOpts(theme='dark'))
            .add_xaxis([x[0] for x in t_data])
            .add_yaxis("铜牌🥉", [x[3] for x in t_data],
                        stack='stack1',
                        itemstyle_opts=opts.ItemStyleOpts(border_color='rgb(220,220,220)',color='rgb(218,165,32)'))
            .add_yaxis("银牌🥈", [x[2] for x in t_data],
                        stack='stack1',
                        itemstyle_opts=opts.ItemStyleOpts(border_color='rgb(220,220,220)',color='rgb(192,192,192)'))
            .add_yaxis("金牌🏅️", [x[1] for x in t_data],
                        stack='stack1',
                        itemstyle_opts=opts.ItemStyleOpts(border_color='rgb(220,220,220)',color='rgb(255,215,0)'))
            .set_series_opts(label_opts=opts.LabelOpts(is_show=True,
                                                       position='insideRight',
                                                       font_style='italic'),)
            .set_global_opts(
                title_opts=opts.TitleOpts(title="各国累计奖牌数（冬季奥运会）"),
                xaxis_opts=opts.AxisOpts(axislabel_opts=opts.LabelOpts(rotate=45)),
                legend_opts=opts.LegendOpts(is_show=True),
                graphic_opts=[opts.GraphicGroup(graphic_item=opts.GraphicItem(
                                                   rotation=JsCode("Math.PI / 4"),
                                                   bounding="raw",
                                                   right=110,
                                                   bottom=110,
                                                   z=100),
                                               children=[
                                                   opts.GraphicRect(
                                                       graphic_item=opts.GraphicItem(
                                                           left="center", top="center", z=100
                                                       ),
                                                       graphic_shape_opts=opts.GraphicShapeOpts(
                                                           width=400, height=50
                                                       ),
                                                       graphic_basicstyle_opts=opts.GraphicBasicStyleOpts(
                                                           fill="rgba(0,0,0,0.3)"
                                                       ),
                                                   ),
                                                   opts.GraphicText(
                                                       graphic_item=opts.GraphicItem(
                                                           left="center", top="center", z=100
                                                       ),
                                                       graphic_textstyle_opts=opts.GraphicTextStyleOpts(
                                                           text='截止{}'.format(year),
                                                           font="bold 26px Microsoft YaHei",
                                                           graphic_basicstyle_opts=opts.GraphicBasicStyleOpts(
                                                               fill="#fff"
                                                           ),
                                                       ),
                                                   ),
                                               ],
                                            )
                                    ],)
            .reversal_axis())
    tl.add(bar, year)

tl.render_notebook()
```

### 代码单元 7

```python
background_color_js = """new echarts.graphic.RadialGradient(0.5, 0.5, 1, [{
                                        offset: 0,
                                        color: '#696969'
                                    }, {
                                        offset: 1,
                                        color: '#000000'
                                    }])"""

tab = Tab()
temp = data[(data['Medal']=='Gold') & (data['Year']==2016) & (data['Season']=='Summer')]

event_medal = temp.groupby(['Sport'])['Event'].nunique().reset_index()
event_medal.columns = ['Sport', 'Nums']
event_medal = event_medal.sort_values(by="Nums" , ascending=False)

pie = (Pie(init_opts=opts.InitOpts(bg_color=JsCode(background_color_js), width='1000px', height='800px'))
       .add('金牌🏅️', [(row['Sport'], row['Nums']) for _, row in event_medal.iterrows()],
            radius=["30%", "75%"],
            rosetype="radius")
       .set_global_opts(title_opts=opts.TitleOpts(title="2016年夏季奥运会各项运动产生金牌占比",
                                                  pos_left="center",
                                                  title_textstyle_opts=opts.TextStyleOpts(color="white", font_size=20),     ),
                        legend_opts=opts.LegendOpts(is_show=False))
       .set_series_opts(label_opts=opts.LabelOpts(formatter="{b}: {d}%"),
                        tooltip_opts=opts.TooltipOpts(trigger="item", formatter="{a} <br/>{b}: {c} ({d}%)"),)
      )
tab.add(pie, '2016年夏奥会')

temp = data[(data['Medal']=='Gold') & (data['Year']==2014) & (data['Season']=='Winter')]

event_medal = temp.groupby(['Sport'])['Event'].nunique().reset_index()
event_medal.columns = ['Sport', 'Nums']
event_medal = event_medal.sort_values(by="Nums" , ascending=False)

pie = (Pie(init_opts=opts.InitOpts(bg_color=JsCode(background_color_js), width='1000px', height='800px'))
       .add('金牌🏅️', [(row['Sport'], row['Nums']) for _, row in event_medal.iterrows()],
            radius=["30%", "75%"],
            rosetype="radius")
       .set_global_opts(title_opts=opts.TitleOpts(title="2014年冬季奥运会各项运动产生金牌占比",
                                                  pos_left="center",
                                                  title_textstyle_opts=opts.TextStyleOpts(color="white", font_size=20),     ),
                        legend_opts=opts.LegendOpts(is_show=False))
       .set_series_opts(label_opts=opts.LabelOpts(formatter="{b}: {d}%"),
                        tooltip_opts=opts.TooltipOpts(trigger="item", formatter="{a} <br/>{b}: {c} ({d}%)"
        ),)
      )
tab.add(pie, '2014年冬奥会')
tab.render_notebook()
```

### 代码单元 8

```python
athlete = data.groupby(['Year', 'Season'])['Name'].nunique().reset_index()
athlete.columns = ['Year', 'Season', 'Nums']
athlete = athlete.sort_values(by="Year" , ascending=True)

x_list, y1_list, y2_list = [], [], []

for _, row in athlete.iterrows():
    x_list.append(str(row['Year']))
    if row['Season'] == 'Summer':
        y1_list.append(row['Nums'])
        y2_list.append(None)
    else:
        y2_list.append(row['Nums'])
        y1_list.append(None)

background_color_js = (
    "new echarts.graphic.LinearGradient(1, 1, 0, 0, "
    "[{offset: 0, color: '#008B8B'}, {offset: 1, color: '#FF6347'}], false)"
)

       
line = (
    Line(init_opts=opts.InitOpts(bg_color=JsCode(background_color_js), width='1000px', height='600px'))
    .add_xaxis(x_list)
    .add_yaxis("夏季奥运会",
        y1_list,
        is_smooth=True,
        is_connect_nones=True,
        symbol="circle",
        symbol_size=6,
        linestyle_opts=opts.LineStyleOpts(color="#fff"),
        label_opts=opts.LabelOpts(is_show=False, position="top", color="white"),
        itemstyle_opts=opts.ItemStyleOpts(
            color="green", border_color="#fff", border_width=3),
        tooltip_opts=opts.TooltipOpts(is_show=True))
    .add_yaxis("冬季季奥运会",
        y2_list,
        is_smooth=True,
        is_connect_nones=True,
        symbol="circle",
        symbol_size=6,
        linestyle_opts=opts.LineStyleOpts(color="#FF4500"),
        label_opts=opts.LabelOpts(is_show=False, position="top", color="white"),
        itemstyle_opts=opts.ItemStyleOpts(
            color="red", border_color="#fff", border_width=3),
        tooltip_opts=opts.TooltipOpts(is_show=True))
    .set_series_opts(
        markarea_opts=opts.MarkAreaOpts(
            label_opts=opts.LabelOpts(is_show=True, position="bottom", color="white"),
            data=[
                opts.MarkAreaItem(name="第一次世界大战", x=(1914, 1918)),
                opts.MarkAreaItem(name="第二次世界大战", x=(1939, 1945)),
            ]
        )
    )
    .set_global_opts(title_opts=opts.TitleOpts(title="历届奥运会参赛人数",
                                                pos_left="center",
                                                title_textstyle_opts=opts.TextStyleOpts(color="white", font_size=20),),
                     legend_opts=opts.LegendOpts(is_show=True, pos_top='5%',
                                                 textstyle_opts=opts.TextStyleOpts(color="white", font_size=12)),
                     xaxis_opts=opts.AxisOpts(type_="value",
                                                min_=1904,
                                                max_=2016,
                                                boundary_gap=False,
                                                axislabel_opts=opts.LabelOpts(margin=30, color="#ffffff63",
                                                                              formatter=JsCode("""function (value)
                                                                               {return value+'年';}""")),
                                                axisline_opts=opts.AxisLineOpts(is_show=False),
                                                axistick_opts=opts.AxisTickOpts(
                                                    is_show=True,
                                                    length=25,
                                                    linestyle_opts=opts.LineStyleOpts(color="#ffffff1f"),
                                                ),
                                                splitline_opts=opts.SplitLineOpts(
                                                    is_show=True, linestyle_opts=opts.LineStyleOpts(color="#ffffff1f")
                                                ),
                                            ),
                    yaxis_opts=opts.AxisOpts(
                                            type_="value",
                                            position="right",
                                            axislabel_opts=opts.LabelOpts(margin=20, color="#ffffff63"),
                                            axisline_opts=opts.AxisLineOpts(
                                                linestyle_opts=opts.LineStyleOpts(width=2, color="#fff")
                                            ),
                                            axistick_opts=opts.AxisTickOpts(
                                                is_show=True,
                                                length=15,
                                                linestyle_opts=opts.LineStyleOpts(color="#ffffff1f"),
                                            ),
                                            splitline_opts=opts.SplitLineOpts(
                                                is_show=True, linestyle_opts=opts.LineStyleOpts(color="#ffffff1f")
                                            ),
                                        ),)
)

line.render_notebook()
```

### 代码单元 9

```python
# 历年男性运动员人数
m_data = data[data.Sex=='M'].groupby(['Year', 'Season'])['Name'].nunique().reset_index()
m_data.columns = ['Year', 'Season', 'M-Nums']
m_data = m_data.sort_values(by="Year" , ascending=True)

# 历年女性运动员人数
f_data = data[data.Sex=='F'].groupby(['Year', 'Season'])['Name'].nunique().reset_index()
f_data.columns = ['Year', 'Season', 'F-Nums']
f_data = f_data.sort_values(by="Year" , ascending=True)

t_data = pd.merge(m_data, f_data, on=['Year', 'Season'])
t_data['F-rate'] = round(t_data['F-Nums'] / (t_data['F-Nums']  + t_data['M-Nums'] ), 4)

x_list, y1_list, y2_list = [], [], []

for _, row in t_data.iterrows():
    x_list.append(str(row['Year']))
    if row['Season'] == 'Summer':
        y1_list.append(row['F-rate'])
        y2_list.append(None)
    else:
        y2_list.append(row['F-rate'])
        y1_list.append(None)

background_color_js = (
    "new echarts.graphic.LinearGradient(0, 0, 0, 1, "
    "[{offset: 0, color: '#008B8B'}, {offset: 1, color: '#FF6347'}], false)"
)

       
line = (
    Line(init_opts=opts.InitOpts(bg_color=JsCode(background_color_js), width='1000px', height='600px'))
    .add_xaxis(x_list)
    .add_yaxis("夏季奥运会",
        y1_list,
        is_smooth=True,
        is_connect_nones=True,
        symbol="circle",
        symbol_size=6,
        linestyle_opts=opts.LineStyleOpts(color="#fff"),
        label_opts=opts.LabelOpts(is_show=False, position="top", color="white"),
        itemstyle_opts=opts.ItemStyleOpts(color="green", border_color="#fff", border_width=3),
        tooltip_opts=opts.TooltipOpts(is_show=True),)
    .add_yaxis("冬季季奥运会",
        y2_list,
        is_smooth=True,
        is_connect_nones=True,
        symbol="circle",
        symbol_size=6,
        linestyle_opts=opts.LineStyleOpts(color="#FF4500"),
        label_opts=opts.LabelOpts(is_show=False, position="top", color="white"),
        itemstyle_opts=opts.ItemStyleOpts(color="red", border_color="#fff", border_width=3),
        tooltip_opts=opts.TooltipOpts(is_show=True),)
    .set_series_opts(tooltip_opts=opts.TooltipOpts(trigger="item", formatter=JsCode("""function (params)
                                                                           {return params.data[0]+ '年: ' + Number(params.data[1])*100 +'%';}""")),)
    .set_global_opts(title_opts=opts.TitleOpts(title="历届奥运会参赛女性占比趋势",
                                                pos_left="center",
                                                title_textstyle_opts=opts.TextStyleOpts(color="white", font_size=20),),
                     legend_opts=opts.LegendOpts(is_show=True, pos_top='5%',
                                                 textstyle_opts=opts.TextStyleOpts(color="white", font_size=12)),
                     xaxis_opts=opts.AxisOpts(type_="value",
                                                min_=1904,
                                                max_=2016,
                                                boundary_gap=False,
                                                axislabel_opts=opts.LabelOpts(margin=30, color="#ffffff63",
                                                                              formatter=JsCode("""function (value)
                                                                               {return value+'年';}""")),
                                                axisline_opts=opts.AxisLineOpts(is_show=False),
                                                axistick_opts=opts.AxisTickOpts(
                                                    is_show=True,
                                                    length=25,
                                                    linestyle_opts=opts.LineStyleOpts(color="#ffffff1f"),
                                                ),
                                                splitline_opts=opts.SplitLineOpts(
                                                    is_show=True, linestyle_opts=opts.LineStyleOpts(color="#ffffff1f")
                                                ),
                                            ),
                    yaxis_opts=opts.AxisOpts(
                                            type_="value",
                                            position="right",
                                            axislabel_opts=opts.LabelOpts(margin=20, color="#ffffff63",
                                                                          formatter=JsCode("""function (value)
                                                                           {return Number(value *100)+'%';}""")),
                                            axisline_opts=opts.AxisLineOpts(
                                                linestyle_opts=opts.LineStyleOpts(width=2, color="#fff")
                                            ),
                                            axistick_opts=opts.AxisTickOpts(
                                                is_show=True,
                                                length=15,
                                                linestyle_opts=opts.LineStyleOpts(color="#ffffff1f"),
                                            ),
                                            splitline_opts=opts.SplitLineOpts(
                                                is_show=True, linestyle_opts=opts.LineStyleOpts(color="#ffffff1f")
                                            ),
                                        ),)
)

line.render_notebook()
```

### 代码单元 10

```python
temp = data[(data['Medal']=='Gold')]

athlete = temp.groupby(['Name'])['Medal'].count().reset_index()
athlete.columns = ['Name', 'Nums']
athlete = athlete.sort_values(by="Nums" , ascending=True)

background_color_js = (
    "new echarts.graphic.LinearGradient(0, 0, 1, 1, "
    "[{offset: 0, color: '#008B8B'}, {offset: 1, color: '#FF6347'}], false)"
)

pb = (
    PictorialBar(init_opts=opts.InitOpts(bg_color=JsCode(background_color_js), width='1000px', height='800px'))
    .add_xaxis([x.replace(' ','\n') for x in athlete['Name'].tail(10).tolist()])
    .add_yaxis(
        "",
        athlete['Nums'].tail(10).tolist(),
        label_opts=opts.LabelOpts(is_show=False),
        symbol_size=25,
        symbol_repeat='fixed',
        symbol_offset=[0, 0],
        is_symbol_clip=True,
        symbol='image://https://cdn.kesci.com/upload/image/q8f8otrlfc.png')
    .reversal_axis()
    .set_global_opts(
        title_opts=opts.TitleOpts(title="获得金牌数量最多的运动员", pos_left='center',
                                  title_textstyle_opts=opts.TextStyleOpts(color="white", font_size=20),),
        xaxis_opts=opts.AxisOpts(is_show=False,),
        yaxis_opts=opts.AxisOpts(
            axistick_opts=opts.AxisTickOpts(is_show=False),
            axisline_opts=opts.AxisLineOpts(
                linestyle_opts=opts.LineStyleOpts(opacity=0)
            ),
        ),
    ))

pb.render_notebook()
```

### 代码单元 11

```python
total_athlete = len(set(data['Name']))
medal_athlete = len(set(data['Name'][data['Medal'].isin(['Gold', 'Silver', 'Bronze'])]))
gold_athlete = len(set(data['Name'][data['Medal']=='Gold']))

l1 = Liquid(init_opts=opts.InitOpts(theme='dark', width='1000px', height='800px'))
l1.add("获得奖牌", [medal_athlete/total_athlete],
            center=["70%", "50%"],
            label_opts=opts.LabelOpts(font_size=50,
                formatter=JsCode(
                    """function (param) {
                            return (Math.floor(param.value * 10000) / 100) + '%';
                        }"""),
                position="inside",
            ))
l1.set_global_opts(title_opts=opts.TitleOpts(title="获得过奖牌比例", pos_left='62%', pos_top='8%'))
l1.set_series_opts(tooltip_opts=opts.TooltipOpts(is_show=False))

l2 = Liquid(init_opts=opts.InitOpts(theme='dark', width='1000px', height='800px'))
l2.add("获得金牌",
        [gold_athlete/total_athlete],
        center=["25%", "50%"],
        label_opts=opts.LabelOpts(font_size=50,
            formatter=JsCode(
                """function (param) {
                        return (Math.floor(param.value * 10000) / 100) + '%';
                    }"""),
            position="inside",
        ),)
l2.set_global_opts(title_opts=opts.TitleOpts(title="获得过金牌比例", pos_left='17%', pos_top='8%'))
l2.set_series_opts(tooltip_opts=opts.TooltipOpts(is_show=False))

grid = Grid().add(l1, grid_opts=opts.GridOpts()).add(l2, grid_opts=opts.GridOpts())
grid.render_notebook()
```

### 代码单元 12

```python
tool_js = """function (param) {return param.data[2] +'<br/>'
            +'平均体重： '+Number(param.data[0]).toFixed(2)+' kg<br/>'
            +'平均身高： '+Number(param.data[1]).toFixed(2)+' cm<br/>'
            +'平均年龄： '+Number(param.data[3]).toFixed(2);}"""

background_color_js = (
    "new echarts.graphic.LinearGradient(1, 0, 0, 1, "
    "[{offset: 0, color: '#008B8B'}, {offset: 1, color: '#FF6347'}], false)"
)

temp_data = data[data['Sex']=='M'].groupby(['Sport'])['Age', 'Height', 'Weight'].mean().reset_index().dropna(how='any')

scatter = (Scatter(init_opts=opts.InitOpts(bg_color=JsCode(background_color_js), width='1000px', height='600px'))
           .add_xaxis(temp_data['Weight'].tolist())
           .add_yaxis("男性", [[row['Height'], row['Sport'], row['Age']] for _, row in temp_data.iterrows()],
                      # 渐变效果实现部分
                      color=JsCode("""new echarts.graphic.RadialGradient(0.4, 0.3, 1, [{
                                        offset: 0,
                                        color: 'rgb(129, 227, 238)'
                                    }, {
                                        offset: 1,
                                        color: 'rgb(25, 183, 207)'
                                    }])"""))
           .set_series_opts(label_opts=opts.LabelOpts(is_show=False))
           .set_global_opts(
               title_opts=opts.TitleOpts(title="各项目运动员平均升高体重年龄",pos_left="center",
                                         title_textstyle_opts=opts.TextStyleOpts(color="white", font_size=20)),
               legend_opts=opts.LegendOpts(is_show=True, pos_top='5%',
                                           textstyle_opts=opts.TextStyleOpts(color="white", font_size=12)),
               tooltip_opts = opts.TooltipOpts(formatter=JsCode(tool_js)),
               xaxis_opts=opts.AxisOpts(
                   name='体重/kg',
                   # 设置坐标轴为数值类型
                   type_="value",
                   is_scale=True,
                   # 显示分割线
                   axislabel_opts=opts.LabelOpts(margin=30, color="white"),
                   axisline_opts=opts.AxisLineOpts(is_show=True, linestyle_opts=opts.LineStyleOpts(color="#ffffff1f")),
                   axistick_opts=opts.AxisTickOpts(is_show=True, length=25,
                                                   linestyle_opts=opts.LineStyleOpts(color="#ffffff1f")),
                   splitline_opts=opts.SplitLineOpts(is_show=True, linestyle_opts=opts.LineStyleOpts(color="#ffffff1f")
                                                )),
               yaxis_opts=opts.AxisOpts(
                   name='身高/cm',
                   # 设置坐标轴为数值类型
                   type_="value",
                   # 默认为False表示起始为0
                   is_scale=True,
                   axislabel_opts=opts.LabelOpts(margin=30, color="white"),
                   axisline_opts=opts.AxisLineOpts(is_show=True, linestyle_opts=opts.LineStyleOpts(color="#ffffff1f")),
                   axistick_opts=opts.AxisTickOpts(is_show=True, length=25,
                                                   linestyle_opts=opts.LineStyleOpts(color="#ffffff1f")),
                   splitline_opts=opts.SplitLineOpts(is_show=True, linestyle_opts=opts.LineStyleOpts(color="#ffffff1f")
                                                )),
               visualmap_opts=opts.VisualMapOpts(is_show=False, type_='size', range_size=[5,50], min_=10, max_=40)
    ))

temp_data = data[data['Sex']=='F'].groupby(['Sport'])['Age', 'Height', 'Weight'].mean().reset_index().dropna(how='any')
    
scatter1 = (Scatter()
           .add_xaxis(temp_data['Weight'].tolist())
           .add_yaxis("女性", [[row['Height'], row['Sport'], row['Age']] for _, row in temp_data.iterrows()],
                     itemstyle_opts=opts.ItemStyleOpts(
                         color=JsCode("""new echarts.graphic.RadialGradient(0.4, 0.3, 1, [{
                                        offset: 0,
                                        color: 'rgb(251, 118, 123)'
                                    }, {
                                        offset: 1,
                                        color: 'rgb(204, 46, 72)'
                                    }])""")))
           .set_series_opts(label_opts=opts.LabelOpts(is_show=False))
        )
scatter.overlap(scatter1)
scatter.render_notebook()
```

**文本输出**

```text
C:\Users\Administrator\AppData\Local\Temp\2\ipykernel_17528\2327063722.py:12: FutureWarning: Indexing with multiple keys (implicitly converted to a tuple of keys) will be deprecated, use a list instead.
  temp_data = data[data['Sex']=='M'].groupby(['Sport'])['Age', 'Height', 'Weight'].mean().reset_index().dropna(how='any')
C:\Users\Administrator\AppData\Local\Temp\2\ipykernel_17528\2327063722.py:59: FutureWarning: Indexing with multiple keys (implicitly converted to a tuple of keys) will be deprecated, use a list instead.
  temp_data = data[data['Sex']=='F'].groupby(['Sport'])['Age', 'Height', 'Weight'].mean().reset_index().dropna(how='any')
```

### 代码单元 13

```python
CN_data = data[data.region=='China']
CN_data.head()
```

**文本输出**

```text
ID           Name Sex   Age  Height  Weight   Team  NOC        Games  \
0        1      A Dijiang   M  24.0   180.0    80.0  China  CHN  1992 Summer   
1        2       A Lamusi   M  23.0   170.0    60.0  China  CHN  2012 Summer   
1072   602  Abudoureheman   M  22.0   182.0    75.0  China  CHN  2000 Summer   
2611  1463      Ai Linuer   M  25.0   160.0    62.0  China  CHN  2004 Summer   
2612  1464      Ai Yanhan   F  14.0   168.0    54.0  China  CHN  2016 Summer   

      Year  Season            City       Sport  \
0     1992  Summer       Barcelona  Basketball   
1     2012  Summer          London        Judo   
1072  2000  Summer          Sydney      Boxing   
2611  2004  Summer          Athina   Wrestling   
2612  2016  Summer  Rio de Janeiro    Swimming   

                                         Event Medal region notes  
0                  Basketball Men's Basketball   NaN  China   NaN  
1                 Judo Men's Extra-Lightweight   NaN  China   NaN  
1072                 Boxing Men's Middleweight   NaN  China   NaN  
2611  Wrestling Men's Lightweight, Greco-Roman   NaN  China   NaN  
2612     Swimming Women's 200 metres Freestyle   NaN  China   NaN
```

### 代码单元 14

```python
background_color_js = (
    "new echarts.graphic.LinearGradient(1, 0, 0, 1, "
    "[{offset: 0, color: '#008B8B'}, {offset: 1, color: '#FF6347'}], false)"
)

athlete = CN_data.groupby(['Year', 'Season'])['Name'].nunique().reset_index()
athlete.columns = ['Year', 'Season', 'Nums']
athlete = athlete.sort_values(by="Year" , ascending=False)

        
s_bar = (
        Bar(init_opts=opts.InitOpts(theme='dark', width='1000px', height='300px'))
        .add_xaxis([row['Year'] for _, row in athlete[athlete.Season=='Summer'].iterrows()])
        .add_yaxis("参赛人数", [row['Nums'] for _, row in athlete[athlete.Season=='Summer'].iterrows()],
                  category_gap='40%',
                  itemstyle_opts=opts.ItemStyleOpts(
                                border_color='rgb(220,220,220)',
                                color=JsCode("""new echarts.graphic.LinearGradient(0, 0, 0, 1,
                                             [{
                                                 offset: 1,
                                                 color: '#00BFFF'
                                             }, {
                                                 offset: 0,
                                                 color: '#32CD32'
                                             }])""")))
        .set_series_opts(label_opts=opts.LabelOpts(is_show=True,
                                                position='top',
                                                font_style='italic'))
        .set_global_opts(
            title_opts=opts.TitleOpts(title="中国历年奥运会参赛人数-夏奥会", pos_left='center'),
            xaxis_opts=opts.AxisOpts(axislabel_opts=opts.LabelOpts(rotate=45)),
            legend_opts=opts.LegendOpts(is_show=False),
            yaxis_opts=opts.AxisOpts(axislabel_opts=opts.LabelOpts(margin=20, color="#ffffff63")),
            graphic_opts=[
            opts.GraphicImage(
                graphic_item=opts.GraphicItem(
                    id_="logo", right=0, top=0, z=-10, bounding="raw", origin=[75, 75]
                ),
                graphic_imagestyle_opts=opts.GraphicImageStyleOpts(
                    image="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1586619952245&di=981a36305048f93eec791980acc99cf7&imgtype=0&src=http%3A%2F%2Fimg5.mtime.cn%2Fmg%2F2017%2F01%2F06%2F172210.42721559.jpg",
                    width=1000,
                    height=600,
                    opacity=0.6,),
            )
        ],)
        )

        
w_bar = (
        Bar(init_opts=opts.InitOpts(theme='dark',width='1000px', height='300px'))
        .add_xaxis([row['Year'] for _, row in athlete[athlete.Season=='Winter'].iterrows()])
        .add_yaxis("参赛人数", [row['Nums'] for _, row in athlete[athlete.Season=='Winter'].iterrows()],
                  category_gap='50%',
                  itemstyle_opts=opts.ItemStyleOpts(
                                border_color='rgb(220,220,220)',
                                color=JsCode("""new echarts.graphic.LinearGradient(0, 0, 0, 1,
                                             [{
                                                 offset: 1,
                                                 color: '#00BFFF'
                                             }, {
                                                 offset: 0.8,
                                                 color: '#FFC0CB'
                                             }, {
                                                 offset: 0,
                                                 color: '#40E0D0'
                                             }])""")))
        .set_series_opts(label_opts=opts.LabelOpts(is_show=True,
                                                position='top',
                                                font_style='italic'))
        .set_global_opts(
            title_opts=opts.TitleOpts(title="中国历年奥运会参赛人数-冬奥会", pos_left='center'),
            xaxis_opts=opts.AxisOpts(axislabel_opts=opts.LabelOpts(rotate=45)),
            legend_opts=opts.LegendOpts(is_show=False),
            yaxis_opts=opts.AxisOpts(axislabel_opts=opts.LabelOpts(margin=20, color="#ffffff63")),
            graphic_opts=[
            opts.GraphicImage(
                graphic_item=opts.GraphicItem(
                    id_="logo", right=0, top=-300, z=-10, bounding="raw", origin=[75, 75]
                ),
                graphic_imagestyle_opts=opts.GraphicImageStyleOpts(
                    image="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1586619952245&di=981a36305048f93eec791980acc99cf7&imgtype=0&src=http%3A%2F%2Fimg5.mtime.cn%2Fmg%2F2017%2F01%2F06%2F172210.42721559.jpg",
                    width=1000,
                    height=600,
                    opacity=0.6,),
            )
        ],)
        )

page = (
    Page()
    .add(s_bar,)
    .add(w_bar,)
)
page.render_notebook()
```

### 代码单元 15

```python
background_color_js = (
    "new echarts.graphic.LinearGradient(1, 0, 0, 1, "
    "[{offset: 0, color: '#008B8B'}, {offset: 1, color: '#FF6347'}], false)"
)

CN_medals = CN_data.groupby(['Year', 'Season', 'Medal'])['Event'].nunique().reset_index()
CN_medals.columns = ['Year', 'Season', 'Medal', 'Nums']
CN_medals = CN_medals.sort_values(by="Year" , ascending=False)

        
s_bar = (
        Bar(init_opts=opts.InitOpts(theme='dark', width='1000px', height='300px'))
        .add_xaxis(sorted(list(set([row['Year'] for _, row in CN_medals[CN_medals.Season=='Summer'].iterrows()])), reverse=True))
        .add_yaxis("金牌", [row['Nums'] for _, row in CN_medals[(CN_medals.Season=='Summer') & (CN_medals.Medal=='Gold')].iterrows()],
                  category_gap='20%',
                  itemstyle_opts=opts.ItemStyleOpts(
                                border_color='rgb(220,220,220)',
                                color=JsCode("""new echarts.graphic.LinearGradient(0, 0, 0, 1,
                                             [{
                                                 offset: 0,
                                                 color: '#FFD700'
                                             }, {
                                                 offset: 1,
                                                 color: '#FFFFF0'
                                             }])""")))
        .add_yaxis("银牌", [row['Nums'] for _, row in CN_medals[(CN_medals.Season=='Summer') & (CN_medals.Medal=='Silver')].iterrows()],
                  category_gap='20%',
                  itemstyle_opts=opts.ItemStyleOpts(
                                border_color='rgb(220,220,220)',
                                color=JsCode("""new echarts.graphic.LinearGradient(0, 0, 0, 1,
                                             [{
                                                 offset: 0,
                                                 color: '#C0C0C0'
                                             }, {
                                                 offset: 1,
                                                 color: '#FFFFF0'
                                             }])""")))
        .add_yaxis("铜牌", [row['Nums'] for _, row in CN_medals[(CN_medals.Season=='Summer') & (CN_medals.Medal=='Bronze')].iterrows()],
                  category_gap='20%',
                  itemstyle_opts=opts.ItemStyleOpts(
                                border_color='rgb(220,220,220)',
                                color=JsCode("""new echarts.graphic.LinearGradient(0, 0, 0, 1,
                                             [{
                                                 offset: 0,
                                                 color: '#DAA520'
                                             }, {
                                                 offset: 1,
                                                 color: '#FFFFF0'
                                             }])""")))
        .set_series_opts(label_opts=opts.LabelOpts(is_show=True,
                                                position='top',
                                                font_style='italic'))
        .set_global_opts(
            title_opts=opts.TitleOpts(title="中国历年奥运会获得奖牌数数-夏奥会", pos_left='center'),
            xaxis_opts=opts.AxisOpts(axislabel_opts=opts.LabelOpts(rotate=45)),
            legend_opts=opts.LegendOpts(is_show=False),
            yaxis_opts=opts.AxisOpts(axislabel_opts=opts.LabelOpts(margin=20, color="#ffffff63")),
            graphic_opts=[
            opts.GraphicImage(
                graphic_item=opts.GraphicItem(
                    id_="logo", right=0, top=0, z=-10, bounding="raw", origin=[75, 75]
                ),
                graphic_imagestyle_opts=opts.GraphicImageStyleOpts(
                    image="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1586619952245&di=981a36305048f93eec791980acc99cf7&imgtype=0&src=http%3A%2F%2Fimg5.mtime.cn%2Fmg%2F2017%2F01%2F06%2F172210.42721559.jpg",
                    width=1000,
                    height=600,
                    opacity=0.6,),
            )
        ],)
        )

        
w_bar = (
        Bar(init_opts=opts.InitOpts(theme='dark', width='1000px', height='300px'))
        .add_xaxis(sorted(list(set([row['Year'] for _, row in CN_medals[CN_medals.Season=='Winter'].iterrows()])), reverse=True))
        .add_yaxis("金牌", [row['Nums'] for _, row in CN_medals[(CN_medals.Season=='Winter') & (CN_medals.Medal=='Gold')].iterrows()],
                  category_gap='20%',
                  itemstyle_opts=opts.ItemStyleOpts(
                                border_color='rgb(220,220,220)',
                                color=JsCode("""new echarts.graphic.LinearGradient(0, 0, 0, 1,
                                             [{
                                                 offset: 0,
                                                 color: '#FFD700'
                                             }, {
                                                 offset: 1,
                                                 color: '#FFFFF0'
                                             }])""")))
        .add_yaxis("银牌", [row['Nums'] for _, row in CN_medals[(CN_medals.Season=='Winter') & (CN_medals.Medal=='Silver')].iterrows()],
                  category_gap='20%',
                  itemstyle_opts=opts.ItemStyleOpts(
                                border_color='rgb(220,220,220)',
                                color=JsCode("""new echarts.graphic.LinearGradient(0, 0, 0, 1,
                                             [{
                                                 offset: 0,
                                                 color: '#C0C0C0'
                                             }, {
                                                 offset: 1,
                                                 color: '#FFFFF0'
                                             }])""")))
        .add_yaxis("铜牌", [row['Nums'] for _, row in CN_medals[(CN_medals.Season=='Winter') & (CN_medals.Medal=='Bronze')].iterrows()],
                  category_gap='20%',
                  itemstyle_opts=opts.ItemStyleOpts(
                                border_color='rgb(220,220,220)',
                                color=JsCode("""new echarts.graphic.LinearGradient(0, 0, 0, 1,
                                             [{
                                                 offset: 0,
                                                 color: '#DAA520'
                                             }, {
                                                 offset: 1,
                                                 color: '#FFFFF0'
                                             }])""")))
        .set_series_opts(label_opts=opts.LabelOpts(is_show=True,
                                                position='top',
                                                font_style='italic'))
        .set_global_opts(
            title_opts=opts.TitleOpts(title="中国历年奥运会获得奖牌数-冬奥会", pos_left='center'),
            xaxis_opts=opts.AxisOpts(axislabel_opts=opts.LabelOpts(rotate=45)),
            legend_opts=opts.LegendOpts(is_show=False),
            yaxis_opts=opts.AxisOpts(axislabel_opts=opts.LabelOpts(margin=20, color="#ffffff63")),
            graphic_opts=[
            opts.GraphicImage(
                graphic_item=opts.GraphicItem(
                    id_="logo", right=0, top=-300, z=-10, bounding="raw", origin=[75, 75]
                ),
                graphic_imagestyle_opts=opts.GraphicImageStyleOpts(
                    image="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1586619952245&di=981a36305048f93eec791980acc99cf7&imgtype=0&src=http%3A%2F%2Fimg5.mtime.cn%2Fmg%2F2017%2F01%2F06%2F172210.42721559.jpg",
                    width=1000,
                    height=600,
                    opacity=0.6,),
            )
        ],)
        )

page = (
    Page()
    .add(s_bar,)
    .add(w_bar,)
)
page.render_notebook()
```

### 代码单元 16

```python
background_color_js = (
    "new echarts.graphic.LinearGradient(1, 0, 0, 1, "
    "[{offset: 0.5, color: '#FFC0CB'}, {offset: 1, color: '#F0FFFF'}, {offset: 0, color: '#EE82EE'}], false)"
)

CN_events = CN_data[CN_data.Medal=='Gold'].groupby(['Year', 'Sport'])['Event'].nunique().reset_index()
CN_events = CN_events.groupby(['Sport'])['Event'].sum().reset_index()
CN_events.columns = ['Sport', 'Nums']

data_pair = [(row['Sport'], row['Nums']) for _, row in CN_events.iterrows()]

wc = (WordCloud(init_opts=opts.InitOpts(bg_color=JsCode(background_color_js), width='1000px', height='600px'))
     .add("", data_pair,word_size_range=[30, 80])
     .set_global_opts(title_opts=opts.TitleOpts(title="中国获得过金牌运动项目",pos_left="center",
                                         title_textstyle_opts=opts.TextStyleOpts(color="white", font_size=20)))
)

wc.render_notebook()
```

### 代码单元 17

```python
USA_data = data[data.region=='USA']
USA_data.head()
```

**文本输出**

```text
ID             Name Sex   Age  Height  Weight           Team  NOC  \
10   6  Per Knut Aaland   M  31.0   188.0    75.0  United States  USA   
11   6  Per Knut Aaland   M  31.0   188.0    75.0  United States  USA   
12   6  Per Knut Aaland   M  31.0   188.0    75.0  United States  USA   
13   6  Per Knut Aaland   M  31.0   188.0    75.0  United States  USA   
14   6  Per Knut Aaland   M  33.0   188.0    75.0  United States  USA   

          Games  Year  Season         City                 Sport  \
10  1992 Winter  1992  Winter  Albertville  Cross Country Skiing   
11  1992 Winter  1992  Winter  Albertville  Cross Country Skiing   
12  1992 Winter  1992  Winter  Albertville  Cross Country Skiing   
13  1992 Winter  1992  Winter  Albertville  Cross Country Skiing   
14  1994 Winter  1994  Winter  Lillehammer  Cross Country Skiing   

                                                Event Medal region notes  
10           Cross Country Skiing Men's 10 kilometres   NaN    USA   NaN  
11           Cross Country Skiing Men's 50 kilometres   NaN    USA   NaN  
12  Cross Country Skiing Men's 10/15 kilometres Pu...   NaN    USA   NaN  
13  Cross Country Skiing Men's 4 x 10 kilometres R...   
... 输出过长，博客中已截断
```

### 代码单元 18

```python
background_color_js = (
    "new echarts.graphic.LinearGradient(1, 0, 0, 1, "
    "[{offset: 0, color: '#008B8B'}, {offset: 1, color: '#FF6347'}], false)"
)

athlete = USA_data.groupby(['Year', 'Season'])['Name'].nunique().reset_index()
athlete.columns = ['Year', 'Season', 'Nums']
athlete = athlete.sort_values(by="Year" , ascending=False)

        
s_bar = (
        Bar(init_opts=opts.InitOpts(theme='dark', width='1000px', height='300px'))
        .add_xaxis([row['Year'] for _, row in athlete[athlete.Season=='Summer'].iterrows()])
        .add_yaxis("参赛人数", [row['Nums'] for _, row in athlete[athlete.Season=='Summer'].iterrows()],
                  category_gap='40%',
                  itemstyle_opts=opts.ItemStyleOpts(
                                border_color='rgb(220,220,220)',
                                color=JsCode("""new echarts.graphic.LinearGradient(0, 0, 0, 1,
                                             [{
                                                 offset: 1,
                                                 color: '#00BFFF'
                                             }, {
                                                 offset: 0,
                                                 color: '#32CD32'
                                             }])""")))
        .set_series_opts(label_opts=opts.LabelOpts(is_show=True,
                                                position='top',
                                                font_style='italic'))
        .set_global_opts(
            title_opts=opts.TitleOpts(title="美国历年奥运会参赛人数-夏奥会", pos_left='center'),
            xaxis_opts=opts.AxisOpts(axislabel_opts=opts.LabelOpts(rotate=45)),
            legend_opts=opts.LegendOpts(is_show=False),
            yaxis_opts=opts.AxisOpts(axislabel_opts=opts.LabelOpts(margin=20, color="#ffffff63")),
            graphic_opts=[
            opts.GraphicImage(
                graphic_item=opts.GraphicItem(
                    id_="logo", right=0, top=0, z=-10, bounding="raw", origin=[75, 75]
                ),
                graphic_imagestyle_opts=opts.GraphicImageStyleOpts(
                    image="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1586619952245&di=981a36305048f93eec791980acc99cf7&imgtype=0&src=http%3A%2F%2Fimg5.mtime.cn%2Fmg%2F2017%2F01%2F06%2F172210.42721559.jpg",
                    width=1000,
                    height=600,
                    opacity=0.6,),
            )
        ],)
        )

        
w_bar = (
        Bar(init_opts=opts.InitOpts(theme='dark',width='1000px', height='300px'))
        .add_xaxis([row['Year'] for _, row in athlete[athlete.Season=='Winter'].iterrows()])
        .add_yaxis("参赛人数", [row['Nums'] for _, row in athlete[athlete.Season=='Winter'].iterrows()],
                  category_gap='50%',
                  itemstyle_opts=opts.ItemStyleOpts(
                                border_color='rgb(220,220,220)',
                                color=JsCode("""new echarts.graphic.LinearGradient(0, 0, 0, 1,
                                             [{
                                                 offset: 1,
                                                 color: '#00BFFF'
                                             }, {
                                                 offset: 0.8,
                                                 color: '#FFC0CB'
                                             }, {
                                                 offset: 0,
                                                 color: '#40E0D0'
                                             }])""")))
        .set_series_opts(label_opts=opts.LabelOpts(is_show=True,
                                                position='top',
                                                font_style='italic'))
        .set_global_opts(
            title_opts=opts.TitleOpts(title="美国历年奥运会参赛人数-冬奥会", pos_left='center'),
            xaxis_opts=opts.AxisOpts(axislabel_opts=opts.LabelOpts(rotate=45)),
            legend_opts=opts.LegendOpts(is_show=False),
            yaxis_opts=opts.AxisOpts(axislabel_opts=opts.LabelOpts(margin=20, color="#ffffff63")),
            graphic_opts=[
            opts.GraphicImage(
                graphic_item=opts.GraphicItem(
                    id_="logo", right=0, top=-300, z=-10, bounding="raw", origin=[75, 75]
                ),
                graphic_imagestyle_opts=opts.GraphicImageStyleOpts(
                    image="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1586619952245&di=981a36305048f93eec791980acc99cf7&imgtype=0&src=http%3A%2F%2Fimg5.mtime.cn%2Fmg%2F2017%2F01%2F06%2F172210.42721559.jpg",
                    width=1000,
                    height=600,
                    opacity=0.6,),
            )
        ],)
        )

page = (
    Page()
    .add(s_bar,)
    .add(w_bar,)
)
page.render_notebook()
```

### 代码单元 19

```python
background_color_js = (
    "new echarts.graphic.LinearGradient(1, 0, 0, 1, "
    "[{offset: 0, color: '#008B8B'}, {offset: 1, color: '#FF6347'}], false)"
)

medals = USA_data.groupby(['Year', 'Season', 'Medal'])['Event'].nunique().reset_index()
medals.columns = ['Year', 'Season', 'Medal', 'Nums']
medals = medals.sort_values(by="Year" , ascending=False)

        
s_bar = (
        Bar(init_opts=opts.InitOpts(theme='dark', width='1000px', height='300px'))
        .add_xaxis(sorted(list(set([row['Year'] for _, row in medals[medals.Season=='Summer'].iterrows()])), reverse=True))
        .add_yaxis("金牌", [row['Nums'] for _, row in medals[(medals.Season=='Summer') & (medals.Medal=='Gold')].iterrows()],
                  category_gap='20%',
                  itemstyle_opts=opts.ItemStyleOpts(
                                border_color='rgb(220,220,220)',
                                color=JsCode("""new echarts.graphic.LinearGradient(0, 0, 0, 1,
                                             [{
                                                 offset: 0,
                                                 color: '#FFD700'
                                             }, {
                                                 offset: 1,
                                                 color: '#FFFFF0'
                                             }])""")))
        .add_yaxis("银牌", [row['Nums'] for _, row in medals[(medals.Season=='Summer') & (medals.Medal=='Silver')].iterrows()],
                  category_gap='20%',
                  itemstyle_opts=opts.ItemStyleOpts(
                                border_color='rgb(220,220,220)',
                                color=JsCode("""new echarts.graphic.LinearGradient(0, 0, 0, 1,
                                             [{
                                                 offset: 0,
                                                 color: '#C0C0C0'
                                             }, {
                                                 offset: 1,
                                                 color: '#FFFFF0'
                                             }])""")))
        .add_yaxis("铜牌", [row['Nums'] for _, row in medals[(medals.Season=='Summer') & (medals.Medal=='Bronze')].iterrows()],
                  category_gap='20%',
                  itemstyle_opts=opts.ItemStyleOpts(
                                border_color='rgb(220,220,220)',
                                color=JsCode("""new echarts.graphic.LinearGradient(0, 0, 0, 1,
                                             [{
                                                 offset: 0,
                                                 color: '#DAA520'
                                             }, {
                                                 offset: 1,
                                                 color: '#FFFFF0'
                                             }])""")))
        .set_series_opts(label_opts=opts.LabelOpts(is_show=True,
                                                position='top',
                                                font_style='italic'))
        .set_global_opts(
            title_opts=opts.TitleOpts(title="美国历年奥运会获得奖牌数数-夏奥会", pos_left='center'),
            xaxis_opts=opts.AxisOpts(axislabel_opts=opts.LabelOpts(rotate=45)),
            legend_opts=opts.LegendOpts(is_show=False),
            yaxis_opts=opts.AxisOpts(axislabel_opts=opts.LabelOpts(margin=20, color="#ffffff63")),
            graphic_opts=[
            opts.GraphicImage(
                graphic_item=opts.GraphicItem(
                    id_="logo", right=0, top=0, z=-10, bounding="raw", origin=[75, 75]
                ),
                graphic_imagestyle_opts=opts.GraphicImageStyleOpts(
                    image="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1586619952245&di=981a36305048f93eec791980acc99cf7&imgtype=0&src=http%3A%2F%2Fimg5.mtime.cn%2Fmg%2F2017%2F01%2F06%2F172210.42721559.jpg",
                    width=1000,
                    height=600,
                    opacity=0.6,),
            )
        ],)
        )

        
w_bar = (
        Bar(init_opts=opts.InitOpts(theme='dark', width='1000px', height='300px'))
        .add_xaxis(sorted(list(set([row['Year'] for _, row in medals[medals.Season=='Winter'].iterrows()])), reverse=True))
        .add_yaxis("金牌", [row['Nums'] for _, row in medals[(medals.Season=='Winter') & (medals.Medal=='Gold')].iterrows()],
                  category_gap='20%',
                  itemstyle_opts=opts.ItemStyleOpts(
                                border_color='rgb(220,220,220)',
                                color=JsCode("""new echarts.graphic.LinearGradient(0, 0, 0, 1,
                                             [{
                                                 offset: 0,
                                                 color: '#FFD700'
                                             }, {
                                                 offset: 1,
                                                 color: '#FFFFF0'
                                             }])""")))
        .add_yaxis("银牌", [row['Nums'] for _, row in medals[(medals.Season=='Winter') & (medals.Medal=='Silver')].iterrows()],
                  category_gap='20%',
                  itemstyle_opts=opts.ItemStyleOpts(
                                border_color='rgb(220,220,220)',
                                color=JsCode("""new echarts.graphic.LinearGradient(0, 0, 0, 1,
                                             [{
                                                 offset: 0,
                                                 color: '#C0C0C0'
                                             }, {
                                                 offset: 1,
                                                 color: '#FFFFF0'
                                             }])""")))
        .add_yaxis("铜牌", [row['Nums'] for _, row in medals[(medals.Season=='Winter') & (medals.Medal=='Bronze')].iterrows()],
                  category_gap='20%',
                  itemstyle_opts=opts.ItemStyleOpts(
                                border_color='rgb(220,220,220)',
                                color=JsCode("""new echarts.graphic.LinearGradient(0, 0, 0, 1,
                                             [{
                                                 offset: 0,
                                                 color: '#DAA520'
                                             }, {
                                                 offset: 1,
                                                 color: '#FFFFF0'
                                             }])""")))
        .set_series_opts(label_opts=opts.LabelOpts(is_show=True,
                                                position='top',
                                                font_style='italic'))
        .set_global_opts(
            title_opts=opts.TitleOpts(title="美国历年奥运会获得奖牌数-冬奥会", pos_left='center'),
            xaxis_opts=opts.AxisOpts(axislabel_opts=opts.LabelOpts(rotate=45)),
            legend_opts=opts.LegendOpts(is_show=False),
            yaxis_opts=opts.AxisOpts(axislabel_opts=opts.LabelOpts(margin=20, color="#ffffff63")),
            graphic_opts=[
            opts.GraphicImage(
                graphic_item=opts.GraphicItem(
                    id_="logo", right=0, top=-300, z=-10, bounding="raw", origin=[75, 75]
                ),
                graphic_imagestyle_opts=opts.GraphicImageStyleOpts(
                    image="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1586619952245&di=981a36305048f93eec791980acc99cf7&imgtype=0&src=http%3A%2F%2Fimg5.mtime.cn%2Fmg%2F2017%2F01%2F06%2F172210.42721559.jpg",
                    width=1000,
                    height=600,
                    opacity=0.6,),
            )
        ],)
        )

page = (
    Page()
    .add(s_bar,)
    .add(w_bar,)
)
page.render_notebook()
```

### 代码单元 20

```python
background_color_js = (
    "new echarts.graphic.LinearGradient(1, 0, 0, 1, "
    "[{offset: 0.5, color: '#FFC0CB'}, {offset: 1, color: '#F0FFFF'}, {offset: 0, color: '#EE82EE'}], false)"
)

events = USA_data[USA_data.Medal=='Gold'].groupby(['Year', 'Sport'])['Event'].nunique().reset_index()
events = events.groupby(['Sport'])['Event'].sum().reset_index()
events.columns = ['Sport', 'Nums']

data_pair = [(row['Sport'], row['Nums']) for _, row in events.iterrows()]

wc = (WordCloud(init_opts=opts.InitOpts(bg_color=JsCode(background_color_js), width='1000px', height='600px'))
     .add("", data_pair,word_size_range=[30, 80])
     .set_global_opts(title_opts=opts.TitleOpts(title="美国获得过金牌运动项目",pos_left="center",
                                         title_textstyle_opts=opts.TextStyleOpts(color="white", font_size=20)))
)

wc.render_notebook()
```

### 代码单元 21

```
f1 = lambda x:max(x['Event']) / sum(x['Event'])
f2 = lambda x: x.sort_values('Event', ascending=False).head(1)

t_data = data[(data.Medal=='Gold') & (data.Year>=2000) &(data.Season=='Summer')].groupby(['Year', 'Sport', 'region'])['Event'].nunique().reset_index()
t_data = t_data.groupby(['Sport', 'region'])['Event'].sum().reset_index()
t1 = t_data.groupby(['Sport']).apply(f2).reset_index(drop=True)
t2 = t_data.groupby(['Sport'])['Event'].sum().reset_index()
t_data = pd.merge(t1, t2, on='Sport', how='inner')
t_data['gold_rate'] = t_data.Event_x/ t_data.Event_y
t_data = t_data.sort_values('gold_rate', ascending=False).reset_index(drop=True)

t_data = t_data[(t_data.gold_rate>=0.5) & (t_data.Event_y>=10)]

background_color_js = (
    "new echarts.graphic.LinearGradient(1, 0, 0, 1, "
    "[{offset: 0, color: '#008B8B'}, {offset: 1, color: '#FF6347'}], false)"
)

fn = """
    function(params) {
        if(params.name == '其他国家')
            return '\\n\\n\\n' + params.name + ' : ' + params.value ;
        return params.seriesName+ '\\n' + params.name + ' : ' + params.value;
    }
    """

def new_label_opts():
    return opts.LabelOpts(formatter=JsCode(fn), position="center")

pie = Pie(init_opts=opts.InitOpts(theme='dark', width='1000px', height='1000px'))
idx = 0

for _, row in t_data.iterrows():
    
    if idx % 2 == 0:
        x = 30
        y = int(idx/2) * 22 + 18
    else:
        x = 70
        y = int(idx/2) * 22 + 18
    idx += 1
    pos_x = str(x)+'%'
    pos_y = str(y)+'%'
    pie.add(
            row['Sport'],
            [[row['region'], row['Event_x']], ['其他国家', row['Event_y']-row['Event_x']]],
            center=[pos_x, pos_y],
            radius=[70, 100],
            label_opts=new_label_opts(),)
    
pie.set_global_opts(
        title_opts=opts.TitleOpts(title="被单个国家统治的项目",
                                  subtitle='统计周期：2000年悉尼奥运会起',
                                  pos_left="center",
                                  title_textstyle_opts=opts.TextStyleOpts(color="white", font_size=20)),
        legend_opts=opts.LegendOpts(is_show=False),
    )

pie.render_notebook()
```

