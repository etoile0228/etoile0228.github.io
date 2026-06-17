---
title: "国产进口电影票房榜单分析：用大屏看影片表现和市场结构"
date: 2026-06-17T23:49:23+08:00
# weight: 1
# aliases: ["/first"]
categories: ["文化娱乐"]
tags: ["pyecharts", "票房", "大屏", "电影市场"]
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

# 国产进口电影票房榜单分析：用大屏看影片表现和市场结构

## 摘要

| 模块     | 内容                                                         |
| -------- | ------------------------------------------------------------ |
| 业务场景 | 文化娱乐                                                     |
| 数据来源 | 电影票房榜单、票房概览和时段趋势数据。                       |
| 分析方法 | Excel 数据读取、pyecharts 大屏、票房趋势、影片排行和结构对比。 |
| 结论先行 | 票房榜单能展示头部影片集中度，反映内容供给和宣发能力差异。   |

本报告围绕“业务背景、分析目的、数据说明、分析思路、分析过程、核心结论和改进建议”展开，目标是用数据回答具体问题，并把分析结果转化为可执行的判断。

## 一、分析背景

电影市场分析关注票房规模、排片效率、影片类型和观众热度。可视化大屏适合快速呈现市场格局和重点影片表现。

## 二、分析目的

本次分析主要回答以下问题：

- 数据在时间、区域、类别或人群维度上呈现什么结构？
- 哪些图表最适合承载趋势、对比、分布和异常信息？
- 可视化结果如何帮助读者快速定位重点？

先明确分析目的，再开展数据处理和指标拆解，可以保证报告围绕问题展开，而不是简单罗列代码和图表。

## 三、数据来源与指标说明

| 项目           | 说明                                                         |
| -------------- | ------------------------------------------------------------ |
| 数据来源       | 电影票房榜单、票房概览和时段趋势数据。                       |
| 分析工具与方法 | Excel 数据读取、pyecharts 大屏、票房趋势、影片排行和结构对比。 |
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

### 1. 票房榜单能展示头部影片集中度，反映内容供给和宣发能力差异。

结果解读：该发现是本项目最核心的结论之一，说明数据中存在值得关注的结构性特征。对应图表或模型结果应围绕这一判断展开，帮助读者理解结论来源。

### 2. 国产片和进口片的表现对比，需要结合档期、类型和排片资源解释。

结果解读：该发现进一步解释了不同维度之间的差异。对业务决策而言，重点不只是看到差异，而是判断差异来自哪些对象、场景或指标。

### 3. 票房趋势比单日排名更重要，可以判断影片后劲和口碑扩散。

结果解读：该发现可以作为后续优化策略或模型改进的依据。若用于真实业务，还需要结合成本、资源、实验结果或线上反馈继续验证。

## 七、结论

综合以上分析，可以得到以下结论：

- 票房榜单能展示头部影片集中度，反映内容供给和宣发能力差异。
- 国产片和进口片的表现对比，需要结合档期、类型和排片资源解释。
- 票房趋势比单日排名更重要，可以判断影片后劲和口碑扩散。

## 八、建议

- 行动 1：片方应关注首周走势和排片转化效率，及时调整宣发资源。
- 行动 2：影院可结合时段票房和上座率优化排片，而不是只追逐总榜排名。
- 行动 3：后续可加入豆瓣/猫眼评分和社媒热度，分析口碑对票房曲线的影响。
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
data = pd.read_excel("./票房榜.xlsx")
data.head(1)
```

**文本输出**

```text
榜单类别   电影        上映日期          票房  场均人次  平均票价  排名  EnMovieID
0   全部  长津湖  2021-09-30  5774075053    22    46   1     703496
```

### 代码单元 3

```python
data["年份"] = data["上映日期"].apply(lambda x: str(x.split("-")[0]))
```

### 代码单元 4

```python
data["票房"] = data["票房"].apply(lambda x: round(x/100000000, 2))
```

### 代码单元 5

```python
data = data.rename(columns={"票房":"票房/亿"})
```

### 代码单元 6

```python
data.head(1)
```

**文本输出**

```text
榜单类别   电影        上映日期   票房/亿  场均人次  平均票价  排名  EnMovieID    年份
0   全部  长津湖  2021-09-30  57.74    22    46   1     703496  2021
```

### 代码单元 7

```python
data_haed = pd.read_excel(r"./电影票房表现概览.xlsx")
data_haed.head(1)
```

**文本输出**

```text
EnMovieID  DBOMovieID  EFMTMovieID   电影                        英文电影名  \
0     703496       38846        36367  长津湖  The Battle at Lake Changjin   

               导演                  主演  GenreMainID 主要类型          作品类型  ...  \
0  陈凯歌/徐克/林超贤/徐正阳  吴京/易烊千玺/段奕宏/朱亚文/李晨           12   剧情  剧情/战争/历史/主旋律  ...   

      累计场次       累计人次  第一天观看人次          首映票房          首周票房         首周末票房  \
0  5716231  124478494  4249441  2.051913e+08  1.527661e+09  1.322469e+09   

      猫眼想看人数    淘票票想看人数  猫眼评分  豆瓣评分  
0  1012616.0  1042773.0   9.5   7.4  

[1 rows x 31 columns]
```

### 代码单元 8

```python
data_haed_all = data.merge(data_haed, how="left", on=['EnMovieID'])

data_haed_all["首映票房"] = data_haed_all["首映票房"].apply(lambda x: round(x/100000000, 2))
data_haed_all["首周票房"] = data_haed_all["首周票房"].apply(lambda x: round(x/100000000, 2))
data_haed_all["首周末票房"] = data_haed_all["首周末票房"].apply(lambda x: round(x/100000000, 2))

data_haed_all = data_haed_all.rename(columns={"电影_x": "电影", "首映票房": "首映票房/亿", "首周票房": "首周票房/亿", "首周末票房": "首周末票房/亿"})
```

### 代码单元 9

```python
data_haed_all.info()
```

**文本输出**

```text
<class 'pandas.core.frame.DataFrame'>
Int64Index: 150 entries, 0 to 149
Data columns (total 39 columns):
 #   Column       Non-Null Count  Dtype  
---  ------       --------------  -----  
 0   榜单类别         150 non-null    object 
 1   电影           150 non-null    object 
 2   上映日期         150 non-null    object 
 3   票房/亿         150 non-null    float64
 4   场均人次         150 non-null    int64  
 5   平均票价         150 non-null    int64  
 6   排名           150 non-null    int64  
 7   EnMovieID    150 non-null    int64  
 8   年份           150 non-null    object 
 9   DBOMovieID   150 non-null    int64  
 10  EFMTMovieID  150 non-null    int64  
 11  电影_y         150 non-null    object 
 12  英文电影名        150 non-null    object 
 13  导演           150 non-null    object 
 14  主演           139 non-null    object 
 15  GenreMainID  150 non-null    int64  
 16  主要类型         150 non-null    object 
 17  作品类型         150 non-null    object 
 18  地区           150 non-null    object 
 19  电影时长         146 non-null    object 
 20  电影版本         150 non-null    object 
 21  点映日期         150 non-null    object 
 22  最晚结束日期       150 non-null    object 
 23  最新上映天数       150 non-null    int64  
 24
... 输出过长，博客中已截断
```

### 代码单元 10

```python
data_haed_all = data_haed_all.drop(labels=["EnMovieID","DBOMovieID","EFMTMovieID","电影_y","GenreMainID"],axis=1)
```

### 代码单元 11

```python
colums = list(data_haed_all)
print(colums)
```

**文本输出**

```text
['榜单类别', '电影', '上映日期', '票房/亿', '场均人次', '平均票价', '排名', '年份', '英文电影名', '导演', '主演', '主要类型', '作品类型', '地区', '电影时长', '电影版本', '点映日期', '最晚结束日期', '最新上映天数', '正式上映日期', '数据截止日期', '点映天数', '点映票房', '累计票房', '累计场次', '累计人次', '第一天观看人次', '首映票房/亿', '首周票房/亿', '首周末票房/亿', '猫眼想看人数', '淘票票想看人数', '猫眼评分', '豆瓣评分']
```

### 代码单元 12

```python
data_all = data_haed_all[data_haed_all["榜单类别"] == "全部"]
data_china = data_haed_all[data_haed_all["榜单类别"] == "国产"]
data_foreign = data_haed_all[data_haed_all["榜单类别"] == "进口"]

data_cat = [data_all, data_china, data_foreign]
cat = ["全部", "国产","进口"]
```

### 代码单元 13

```python
headers = colums
rows_all = data_all[data_all["榜单类别"] == "全部"][colums].apply(lambda x: list(x), axis=1).values.tolist()

table_all = Table()
attributes = {"class": "fl-table", "style": "margin: 0 auto"}  # 居中显示
table_all.add(headers, rows_all, attributes)
table_all.set_global_opts(
    title_opts=ComponentTitleOpts(title=f"榜单类别 - 全部 - TOP50", subtitle="全部是包括国产、进口\n （上下左右移动表格）")
)
# 渲染时间较长
table_all.render_notebook()
```

### 代码单元 14

```python
tab = Tab()

headers = colums

rows_china = data_china[colums].apply(lambda x: list(x), axis=1).values.tolist()

rows_foreign = data_foreign[colums].apply(lambda x: list(x), axis=1).values.tolist()

attributes = {"class": "fl-table", "style": "margin: 0 auto"}  # 居中显示

table_china = Table()
attributes = {"class": "fl-table", "style": "margin: 0 auto"}  # 居中显示
table_china.add(headers, rows_china, attributes)
table_china.set_global_opts(
    title_opts=ComponentTitleOpts(title=f"榜单类别 - 国产 - TOP50", subtitle="")
)

table_foreign = Table()
attributes = {"class": "fl-table", "style": "margin: 0 auto"}  # 居中显示
table_foreign.add(headers, rows_foreign, attributes)
table_foreign.set_global_opts(
    title_opts=ComponentTitleOpts(title=f"榜单类别 - 进口 - TOP50", subtitle="")
)

table = Table()
table.add([], [], attributes)
table.set_global_opts(
    title_opts=ComponentTitleOpts(title="键盘左右键移动视图查看", subtitle="")
)

tab.add(table_china, "国产")
tab.add(table_foreign, "进口")
tab.add(table, "点击预览")

tab.render_notebook()
```

### 代码单元 15

```python
# from pyecharts.globals import CurrentConfig, NotebookType
# CurrentConfig.NOTEBOOK_TYPE = NotebookType.JUPYTER_NOTEBOOK
```

### 代码单元 16

```python
line_max = max(max(data_all['场均人次'].tolist()), max(data_all['平均票价'].tolist()))

bar_max = max(data_all['票房/亿'].tolist())

bar_all = (
    Bar(init_opts=opts.InitOpts(width="1000px", height="600px",theme='light'))  # 设置图表大小
        .add_xaxis(xaxis_data=data_all['电影'].tolist())  # x轴
        .add_yaxis(
        series_name="票房/亿",  # 柱形图系列名称
        y_axis=data_all['票房/亿'].tolist(),  # 数据
        label_opts=opts.LabelOpts(is_show=False, position='top', formatter="{c}/亿"),  # 显示数据标签
        itemstyle_opts={
            "normal": {
                "color": JsCode("""new echarts.graphic.LinearGradient(0, 0, 0, 1, [{
                    offset: 0,
                    color: '#ee3f4d'
                }, {
                    offset: 1,
                    color: '#eea2a4'
                }], false)""", ),
                "opacity": 0.8,
#                 "barBorderRadius": [20, 20, 0, 0],
                'shadowBlur': 8,
                'shadowColor': 'rgba(0, 0, 0, 0.4)',
                'shadowOffsetX': 10,
                'shadowOffsetY': 10,
                'borderColor': 'rgb(220,220,220)',
                'borderWidth': 1
            }}
    )
        .extend_axis(  # 设置次坐标轴
        yaxis=opts.AxisOpts(
            name="",  # 次坐标轴名称
            type_="value",  # 次坐标手类型
            min_=-2 * line_max,  # 最小值
            max_=2 * line_max,  # 最大值
            is_show=False,  # 是否显示
            axisline_opts=opts.AxisLineOpts(is_show=False,  # y轴线不显示
                                            linestyle_opts=opts.LineStyleOpts(color='#2486b9')),  # 设置线颜色, 字体颜色也变
            axistick_opts=opts.AxisTickOpts(is_show=False),  # 刻度线不显示
            axislabel_opts=opts.LabelOpts(formatter="{value}"),  # 次坐标轴数据显示格式
        )
    )

        .set_global_opts(title_opts=opts.TitleOpts(title="电影票房 - top50",  # 标题
                                                   title_textstyle_opts=opts.TextStyleOpts(font_size=20),  # 主标题字体大小
                                                   subtitle="国产/进口",  # 次坐标轴
                                                   pos_left='center',
                                                   pos_top='0.8%'),  # 标题位置
                         legend_opts=opts.LegendOpts(is_show=True,
                                                     pos_top=50,
                                                     orient="horizontal",
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
                                                  max_=bar_max,
                                                  name='票房/亿',  # y轴名称
                                                  name_location='middle',  # y轴名称位置
                                                  name_gap=70,  # y轴名称距离轴线距离
                                                  axistick_opts=opts.AxisTickOpts(is_show=False),  # 刻度线
                                                  axisline_opts=opts.AxisLineOpts(is_show=False),  # y轴线
                                                  splitline_opts=opts.SplitLineOpts(is_show=True),  # y轴网格线
                                                  axislabel_opts=opts.LabelOpts(formatter="{value}"),
                                                  ),  # 轴标签显示方式
                         datazoom_opts=opts.DataZoomOpts(is_zoom_lock=False)
                         )
)

line_all = (
    Line()
        .add_xaxis(xaxis_data=data_all['电影'].tolist())  # x轴
        .add_yaxis(
        series_name="场均人次",  # 名称
        yaxis_index=1,  # 次坐标
        is_smooth=True,  # 线条样式  , 是否设置成圆滑曲线
        y_axis=data_all['场均人次'].tolist(),
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
                'width': 3,
                'shadowColor': 'rgba(0, 0, 0, 0.5)',
                'shadowBlur': 5,
                'shadowOffsetY': 10,
                'shadowOffsetX': 10,
                'curve': 0.5,
                'color': '#2486b9'
            }
        },
        label_opts=opts.LabelOpts(is_show=False),  # 显示数据标签
    )
    
    .add_yaxis(
        series_name="平均票价",  # 名称
        yaxis_index=1,  # 次坐标
        is_smooth=True,  # 线条样式  , 是否设置成圆滑曲线
        y_axis=data_all['平均票价'].tolist(),
        itemstyle_opts={
            "normal": {
                "color": JsCode(
                    """new echarts.graphic.LinearGradient(0, 0, 0, 1, [{
                                        offset: 0,
                                        color: '#1a6840'
                                    }, {
                                        offset: 1,
                                        color: '#66c18c'
                                    }], false)""", ),
                "opacity": 0.7,
                "barBorderRadius": [45, 45, 45, 45],
                "shadowColor": 'rgb(0, 160, 221)',
            }},
        linestyle_opts={
            'normal': {
                'width': 3,
                'shadowColor': 'rgba(0, 0, 0, 0.5)',
                'shadowBlur': 5,
                'shadowOffsetY': 10,
                'shadowOffsetX': 10,
                'curve': 0.5,
                'color': '#66c18c'
            }
        },
        label_opts=opts.LabelOpts(is_show=False),  # 显示数据标签
    )
)
bar_all.overlap(line_all)  # 图表组合

bar_all.render_notebook()
```

### 代码单元 17

```python
tab_rank = Tab()
for i in range(1,3):
    line_max = max(max(data_cat[i]['场均人次'].tolist()), max(data_cat[i]['平均票价'].tolist()))

    bar_max = max(data_cat[i]['票房/亿'].tolist())

    bar1 = (
        Bar(init_opts=opts.InitOpts(width="1000px", height="600px",theme='light'))  # 设置图表大小
            .add_xaxis(xaxis_data=data_cat[i]['电影'].tolist())  # x轴
            .add_yaxis(
            series_name="票房/亿",  # 柱形图系列名称
            y_axis=data_cat[i]['票房/亿'].tolist(),  # 数据
            label_opts=opts.LabelOpts(is_show=False, position='top', formatter="{c}/亿"),  # 显示数据标签
            itemstyle_opts={
                "normal": {
                    "color": JsCode("""new echarts.graphic.LinearGradient(0, 0, 0, 1, [{
                        offset: 0,
                        color: '#ee3f4d'
                    }, {
                        offset: 1,
                        color: '#eea2a4'
                    }], false)""", ),
                    "opacity": 0.8,
    #                 "barBorderRadius": [20, 20, 0, 0],
                    "shadowColor": 'rgb(0, 160, 221)',
                }}
        )
            .extend_axis(  # 设置次坐标轴
            yaxis=opts.AxisOpts(
                name="",  # 次坐标轴名称
                type_="value",  # 次坐标手类型
                min_=-2 * line_max,  # 最小值
                max_=2 * line_max,  # 最大值
                is_show=False,  # 是否显示
                axisline_opts=opts.AxisLineOpts(is_show=False,  # y轴线不显示
                                                linestyle_opts=opts.LineStyleOpts(color='#2486b9')),  # 设置线颜色, 字体颜色也变
                axistick_opts=opts.AxisTickOpts(is_show=False),  # 刻度线不显示
                axislabel_opts=opts.LabelOpts(formatter="{value}"),  # 次坐标轴数据显示格式
            )
        )

            .set_global_opts(title_opts=opts.TitleOpts(title=f"{cat[i]}电影票房 - top50",  # 标题
                                                    title_textstyle_opts=opts.TextStyleOpts(font_size=20),  # 主标题字体大小
                                                    subtitle="",  # 次坐标轴
                                                    pos_left='center',
                                                    pos_top='0.8%'),  # 标题位置
                            legend_opts=opts.LegendOpts(is_show=True,
                                                        pos_top=35,
                                                        orient="horizontal",
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
                                                    max_=bar_max,
                                                    name='票房/亿',  # y轴名称
                                                    name_location='middle',  # y轴名称位置
                                                    name_gap=70,  # y轴名称距离轴线距离
                                                    axistick_opts=opts.AxisTickOpts(is_show=False),  # 刻度线
                                                    axisline_opts=opts.AxisLineOpts(is_show=False),  # y轴线
                                                    splitline_opts=opts.SplitLineOpts(is_show=True),  # y轴网格线
                                                    axislabel_opts=opts.LabelOpts(formatter="{value}"),
                                                    ),  # 轴标签显示方式
                            datazoom_opts=opts.DataZoomOpts(is_zoom_lock=False)
                            )
    )

    line1 = (
        Line()
            .add_xaxis(xaxis_data=data_cat[i]['电影'].tolist())  # x轴
            .add_yaxis(
            series_name="场均人次",  # 名称
            yaxis_index=1,  # 次坐标
            is_smooth=True,  # 线条样式  , 是否设置成圆滑曲线
            y_axis=data_cat[i]['场均人次'].tolist(),
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
                    'width': 3,
                    'shadowColor': 'rgba(0, 0, 0, 0.5)',
                    'shadowBlur': 5,
                    'shadowOffsetY': 10,
                    'shadowOffsetX': 10,
                    'curve': 0.5,
                    'color': '#2486b9'
                }
            },
            label_opts=opts.LabelOpts(is_show=False),  # 显示数据标签
        )
        
        .add_yaxis(
            series_name="平均票价",  # 名称
            yaxis_index=1,  # 次坐标
            is_smooth=True,  # 线条样式  , 是否设置成圆滑曲线
            y_axis=data_cat[i]['平均票价'].tolist(),
            itemstyle_opts={
                "normal": {
                    "color": JsCode(
                        """new echarts.graphic.LinearGradient(0, 0, 0, 1, [{
                                            offset: 0,
                                            color: '#1a6840'
                                        }, {
                                            offset: 1,
                                            color: '#66c18c'
                                        }], false)""", ),
                    "opacity": 0.7,
                    "barBorderRadius": [45, 45, 45, 45],
                    "shadowColor": 'rgb(0, 160, 221)',
                }},
            linestyle_opts={
                'normal': {
                    'width': 3,
                    'shadowColor': 'rgba(0, 0, 0, 0.5)',
                    'shadowBlur': 5,
                    'shadowOffsetY': 10,
                    'shadowOffsetX': 10,
                    'curve': 0.5,
                    'color': '#66c18c'
                }
            },
            label_opts=opts.LabelOpts(is_show=False),  # 显示数据标签
        )
    )
    bar1.overlap(line1)  # 图表组合
    tab_rank.add(bar1, cat[i])
tab_rank.add(table, "点击预览")
tab_rank.render_notebook()
```

### 代码单元 18

```python
data_china_year = data_china["年份"].value_counts()
data_foreigna_year = data_foreign["年份"].value_counts()
```

### 代码单元 19

```python
tags_china = []
tag_china = data_china['作品类型'].tolist()
for t in tag_china:
    try:
        for i in t.split('/'):
            tags_china.append(i)
    except:
        continue
tags_china_pair = []
for key, value in Counter(tags_china).items():
    tags_china_pair.append([key, value])

print(tags_china_pair)
```

**文本输出**

```text
[['剧情', 18], ['战争', 5], ['历史', 3], ['主旋律', 11], ['动作', 20], ['喜剧', 24], ['亲情', 2], ['动画', 2], ['玄幻', 1], ['科幻', 3], ['冒险', 6], ['悬疑', 4], ['侦探', 1], ['犯罪', 7], ['爱情', 8], ['怀旧', 2], ['灾难', 2], ['奇幻', 7], ['运动', 1], ['抢险', 1], ['惊悚', 1], ['青春', 2], ['家庭', 1], ['公路', 2]]
```

### 代码单元 20

```python
tags_foreign = []
tag_foreign = data_foreign['作品类型'].tolist()
for t in tag_foreign:
    try:
        for i in t.split('/'):
            tags_foreign.append(i)
    except:
        continue
tags_foreign_pair = []
for key, value in Counter(tags_foreign).items():
    tags_foreign_pair.append([key, value])
```

### 代码单元 21

```python
pie = (
    Pie(init_opts=opts.InitOpts(width="1000px", height="900px", theme='light'))
        .add('国产年份', [list(z) for z in zip(data_china_year.index.tolist(),
                                       data_china_year.values.tolist())],
             radius=['55', '100'],
             center=['33%', '30%']
             )
        .add('进口', [list(z) for z in zip(data_foreigna_year.index.tolist(),
                                       data_foreigna_year.values.tolist())],
             radius=['55', '100'],
             center=['75%', '30%'])
        .add('国产电影标签', tags_china_pair,
             radius=['55', '100'],
             center=['33%', '80%']
             )
        .add('进口电影标签', tags_foreign_pair,
             radius=['55', '100'],
             center=['75%', '80%']
             )
        .set_series_opts(
            label_opts=opts.LabelOpts(formatter="{b}: {c}", font_size=14),
            tooltip_opts=opts.TooltipOpts(trigger="item", formatter="{a} <br/>{b}: {c} ({d}%)"),
            itemstyle_opts={"normal": {
                                        'shadowBlur': 2,
                                        "borderColor": '#87CEFA',
                                        "borderWidth": 3,
                                        'shadowColor': '#87CEFA',
                                        'opacity': 1
                                    }
                           })
        .set_global_opts(
            legend_opts=opts.LegendOpts(is_show=False, pos_top='5%'),
            title_opts=[
                dict(
                    text=f'国产-进口上榜 - TOP50 - 详情分布',
                    left='center',
                    top='1%',
                    textStyle=dict(
                        color='#000',
                        fontSize=24)),
                dict(
                    text=f'国产分布',
                    left='28%',
                    top='10%',
                    textStyle=dict(
                        color='#999999',
                        fontSize=18)),
                dict(
                    text=f'进口分布',
                    left='70%',
                    top='10%',
                    textStyle=dict(
                        color='#999999',
                        fontSize=18)),
                dict(
                    text=f'国产电影标签',
                    left='28%',
                    top='55%',
                    textStyle=dict(
                        color='#999999',
                        fontSize=18)),
                dict(
                    text=f'进口电影标签',
                    left='70%',
                    top='55%',
                    textStyle=dict(
                        color='#999999',
                        fontSize=18)),
            ],
            )
)
pie.render_notebook()
```

### 代码单元 22

```python
bar_china = (
    Bar(init_opts=opts.InitOpts(width="1200px", height="600px", theme='light')) # 设置图表大小
    .add_xaxis(xaxis_data=data_china['电影'].tolist())  # x轴
    .add_yaxis(
        series_name="首映票房/亿",  #柱形图系列名称
        stack='stack1',
        y_axis=data_china['首映票房/亿'].tolist(), # 数据
        label_opts=opts.LabelOpts(is_show=False,position='top',formatter="{c} 亿"), # 显示数据标签
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
        series_name="首周票房/亿",  #柱形图系列名称
        stack='stack1',
        y_axis=data_china['首周票房/亿'].tolist(), # 数据
        label_opts=opts.LabelOpts(is_show=False,position='top',formatter="{c} 亿"), # 显示数据标签
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
        series_name="首周末票房/亿",  #柱形图系列名称
        stack='stack1',
        y_axis=data_china['首周末票房/亿'].tolist(), # 数据
        label_opts=opts.LabelOpts(is_show=False,position='top',formatter="{c} 亿"), # 显示数据标签
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
    .set_global_opts(title_opts=opts.TitleOpts(title="国产电影上映首周票房表现 -Top50",# 标题
                                               title_textstyle_opts=opts.TextStyleOpts(font_size=20), #主标题字体大小
                                               subtitle="", # 次坐标轴
                                               pos_left='center'),# 标题位置
                    legend_opts=opts.LegendOpts(
                                             is_show=True,
                                             pos_top=30,
                                             orient="horizontal"
                                                             ),  # 不显示图例
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
                     datazoom_opts=opts.DataZoomOpts(is_zoom_lock=False,
                                                    orient="vertical")
                                               )
)
bar_china.render_notebook()
```

### 代码单元 23

```python
bar_foreign = (
    Bar(init_opts=opts.InitOpts(width="1200px", height="600px", theme='light')) # 设置图表大小
    .add_xaxis(xaxis_data=data_foreign['电影'].tolist())  # x轴
    .add_yaxis(
        series_name="首映票房/亿",  #柱形图系列名称
        stack='stack1',
        y_axis=data_foreign['首映票房/亿'].tolist(), # 数据
        label_opts=opts.LabelOpts(is_show=False,position='top',formatter="{c} 亿"), # 显示数据标签
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
        series_name="首周票房/亿",  #柱形图系列名称
        stack='stack1',
        y_axis=data_foreign['首周票房/亿'].tolist(), # 数据
        label_opts=opts.LabelOpts(is_show=False,position='top',formatter="{c} 亿"), # 显示数据标签
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
        series_name="首周末票房/亿",  #柱形图系列名称
        stack='stack1',
        y_axis=data_foreign['首周末票房/亿'].tolist(), # 数据
        label_opts=opts.LabelOpts(is_show=False,position='top',formatter="{c} 亿"), # 显示数据标签
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
    .set_global_opts(title_opts=opts.TitleOpts(title="进口电影上映首周票房表现 -Top50",# 标题
                                               title_textstyle_opts=opts.TextStyleOpts(font_size=20), #主标题字体大小
                                               subtitle="", # 次坐标轴
                                               pos_left='center'),# 标题位置
                    legend_opts=opts.LegendOpts(
                                             is_show=True,
                                             pos_top=30,
                                             orient="horizontal"
                                                             ),  # 不显示图例
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
                     datazoom_opts=opts.DataZoomOpts(is_zoom_lock=False,
                                                    orient="vertical")
                                               )
)
bar_foreign.render_notebook()
```

### 代码单元 24

```python
data_movie_time = pd.read_excel(r"./电影票房三十日时段详情.xlsx")
```

### 代码单元 25

```python
data_movie_time["当前票房"] = data_movie_time["当前票房"].apply(lambda x: round(x/10000000, 2))
data_movie_time["当前场次"] = data_movie_time["当前场次"].apply(lambda x: round(x/10000, 2))
data_movie_time["当前人次"] = data_movie_time["当前人次"].apply(lambda x: round(x/1000000, 2))
 
data_movie_time = data_movie_time.rename(columns={"当前票房": "当前票房/千万", "当前场次": "当前场次/万", "当前人次": "当前人次/百万"})
data_movie_time.head(2)
```

**文本输出**

```text
电影  EnMovieID  DBOMovieID          日期 星期  当前票房/千万  当前场次/万  当前人次/百万   票房占比  \
0  长津湖     703496       38846  2021-09-30  四    20.52   16.47     4.25  72.67   
1  长津湖     703496       38846  2021-10-01  五    41.08   15.33     8.37  65.17   

       黄金场票房  黄金场场次    黄金场人次  黄金场票房占比  黄金场场次占比  黄金场人次占比  
0   60450589  33889  1257242       29       21       30  
1  108748583  34326  2194202       26       22       26
```

### 代码单元 26

```python
movie_chang = data_movie_time[data_movie_time["电影"] == "长津湖"]
```

### 代码单元 27

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
    title_opts=opts.TitleOpts(title="长津湖上映后三十日电影票房表现",# 标题
                            title_textstyle_opts=opts.TextStyleOpts(font_size=18), #主标题字体大小
                            subtitle="2021-09-30~2021-10-30", # 次坐标轴
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
                                        image="https://img2.baidu.com/it/u=3979355417,3562690433&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=388",
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
            opts.MarkAreaItem(name="正式上映\n国庆档", x=("2021-09-30", "2021-10-01")),
            opts.MarkAreaItem(name="高峰期", x=("2021-10-05", "2021-10-07")),
            opts.MarkAreaItem(name="第三周\n小高峰", x=("2021-10-15", "2021-10-17")),
        ]
    ),
)
line.set_colors(colors=['#80FFA5', '#00DDFF', '#FF0087'])
line.render_notebook()
```

### 代码单元 28

```python
chart = Gauge(
)
chart.add(
    "",
    [("猫眼评分", 9.5)],
    max_=10,
    start_angle=200,
    end_angle=-20,
    pointer=opts.GaugePointerOpts(
        is_show=True
    ),
    itemstyle_opts=opts.ItemStyleOpts(
        color='rgba(50, 163, 107, 0.3)'
    ),
    detail_label_opts=opts.GaugeDetailOpts(
        border_radius=8,
        offset_center=[0, '15%'],
        font_size=50,
        font_weight='bolder',
        formatter='{value}',
    ),
    axisline_opts=opts.AxisLineOpts(
        is_show=True,
        linestyle_opts=opts.LineStyleOpts(
            width=30,
            color=[(0.8, "#67e0e3"), (0.98, "#D4587A"), (1, "#67e0e3")]
        )
    ),
    title_label_opts=opts.GaugeTitleOpts(
        color='rgba(217, 48, 118, 0.9)',
        offset_center=[0, '-35%'],
        font_size=20,
        font_weight='bolder',
    )
)

chart.set_global_opts(
    title_opts=opts.TitleOpts(
        title="长津湖",
        pos_right='0%',
        pos_bottom='30%',
        title_textstyle_opts=opts.TextStyleOpts(
            color='rgba(217, 48, 118, 0.1)',
            font_size=80
        )
    ),
)
chart.render_notebook()
```

### 代码单元 29

```python
chart_1 = Gauge(
    # init_opts=opts.InitOpts(
    #     width='500px',
    #     height='500px'
    # )
)
chart_1.add(
    "",
    [("豆瓣评分", 7.4)],
    max_=10,
    start_angle=200,
    end_angle=-20,
    pointer=opts.GaugePointerOpts(
        is_show=True
    ),
    itemstyle_opts=opts.ItemStyleOpts(
        color='rgba(50, 163, 107, 0.3)'
    ),
    detail_label_opts=opts.GaugeDetailOpts(
        border_radius=8,
        offset_center=[0, '15%'],
        font_size=50,
        font_weight='bolder',
        formatter='{value}',
    ),
    axisline_opts=opts.AxisLineOpts(
        is_show=True,
        linestyle_opts=opts.LineStyleOpts(
            width=30,
            color=[(0.7, "#37a2da"), (0.8, "#D4587A"), (1, "#37a2da")]
        )
    ),
    title_label_opts=opts.GaugeTitleOpts(
        color='rgba(217, 48, 118, 0.9)',
        offset_center=[0, '-35%'],
        font_size=20,
        font_weight='bolder',
    )
)
 
chart_1.set_global_opts(
    title_opts=opts.TitleOpts(
        title="长津湖",
        pos_right='0%',
        pos_bottom='30%',
        title_textstyle_opts=opts.TextStyleOpts(
            color='rgba(217, 48, 118, 0.1)',
            font_size=80
        )
    ),
)
chart_1.render_notebook()
```

### 代码单元 30

```python
from pyecharts.charts import Page
page = Page(layout=Page.DraggablePageLayout, page_title="大屏展示")

page.add(
    bar_all,pie,bar_china,bar_foreign,line,chart,chart_1)
# 先保存到test.html 然后打开，拖拽图片自定义布局， 之后记得点击左上角“save config”对布局文件进行保存。
# 会生成一个chart_config.json的文件，这其中包含了每个图表ID对应的布局位置
page.render('test.html')
```

**文本输出**

```text
'C:\\myproject\\cx_xiangmu\\Python数据分析\\上架\\2301-Python数据分析与可视化项目\\文化娱乐-国产进口电影票房榜单分析（Pyecharts大屏可视化）\\test.html'
```

### 代码单元 31

```python
# 然后运行下面这行代码。保存布局好的的仪表盘文件。
page.save_resize_html('test.html', cfg_file='chart_config.json', dest='大屏展示1.html')
```

**文本输出**

```
'<!DOCTYPE html>\n<html>\n<head>\n    <meta charset="UTF-8">\n    <title>大屏展示</title>\n            <script type="text/javascript" src="https://assets.pyecharts.org/assets/v5/echarts.min.js"></script>\n        <script type="text/javascript" src="https://assets.pyecharts.org/assets/v5/jquery.min.js"></script>\n        <script type="text/javascript" src="https://assets.pyecharts.org/assets/v5/jquery-ui.min.js"></script>\n        <script type="text/javascript" src="https://assets.pyecharts.org/assets/v5/ResizeSensor.js"></script>\n\n            <link rel="stylesheet"  href="https://assets.pyecharts.org/assets/v5/jquery-ui.css">\n\n</head>\n<body >\n    <style>.box {  } </style>\n        \n    <div class="box">\n                <div id="8ade7d4ad5014434b43b25976f4fc145" class="chart-container" style="position: absolute; width: 995px; height: 602px; top: 25.666667938232422px; left: 165px;"></div>\n    <script>\n        var chart_8ade7d4ad5014434b43b25976f4fc145 = echarts.init(\n            document.getElementById(\'8ade7d4ad5014434b43b25976f4fc145\'), \'light\', {renderer: \'canvas\'});\n        var option_8ade7d4ad5014434b43b25976f4fc145 = {\n    "animation": true,\n    "animationThresh
... 输出过长
```

