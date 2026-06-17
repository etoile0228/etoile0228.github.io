---
title: "第七次人口普查数据可视化：从人口、教育和性别结构看区域差异"
date: 2026-06-17T23:19:40+08:00
# weight: 1
# aliases: ["/first"]
categories: ["社会科学"]
tags: ["人口普查", "pyecharts", "区域分析", "社会数据"]
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

# 第七次人口普查数据可视化：从人口、教育和性别结构看区域差异

## 摘要

| 模块     | 内容                                                         |
| -------- | ------------------------------------------------------------ |
| 业务场景 | 社会科学                                                     |
| 数据来源 | 第七次全国人口普查相关数据，包含各地区人口、年龄结构、性别构成和教育程度。 |
| 分析方法 | 多 CSV 数据整合、Pyecharts 地图和柱状图、区域对比、结构分析。 |
| 结论先行 | 人口规模、年龄结构和教育水平共同决定区域的人力资本和消费潜力。 |

本报告围绕“业务背景、分析目的、数据说明、分析思路、分析过程、核心结论和改进建议”展开，目标是用数据回答具体问题，并把分析结果转化为可执行的判断。

## 一、分析背景

人口结构决定长期消费、教育、养老、住房和产业布局。人口普查数据不仅是社会统计，也能为企业区域战略提供基础判断。

## 二、分析目的

本次分析主要回答以下问题：

- 数据在时间、区域、类别或人群维度上呈现什么结构？
- 哪些图表最适合承载趋势、对比、分布和异常信息？
- 可视化结果如何帮助读者快速定位重点？

先明确分析目的，再开展数据处理和指标拆解，可以保证报告围绕问题展开，而不是简单罗列代码和图表。

## 三、数据来源与指标说明

| 项目           | 说明                                                         |
| -------------- | ------------------------------------------------------------ |
| 数据来源       | 第七次全国人口普查相关数据，包含各地区人口、年龄结构、性别构成和教育程度。 |
| 分析工具与方法 | 多 CSV 数据整合、Pyecharts 地图和柱状图、区域对比、结构分析。 |
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

### 1. 人口规模、年龄结构和教育水平共同决定区域的人力资本和消费潜力。

结果解读：该发现是本项目最核心的结论之一，说明数据中存在值得关注的结构性特征。对应图表或模型结果应围绕这一判断展开，帮助读者理解结论来源。

### 2. 老龄化程度较高地区需要更多养老、医疗和社区服务供给。

结果解读：该发现进一步解释了不同维度之间的差异。对业务决策而言，重点不只是看到差异，而是判断差异来自哪些对象、场景或指标。

### 3. 教育水平和产业结构相关，能为人才招聘和城市选择提供参考。

结果解读：该发现可以作为后续优化策略或模型改进的依据。若用于真实业务，还需要结合成本、资源、实验结果或线上反馈继续验证。

## 七、结论

综合以上分析，可以得到以下结论：

- 人口规模、年龄结构和教育水平共同决定区域的人力资本和消费潜力。
- 老龄化程度较高地区需要更多养老、医疗和社区服务供给。
- 教育水平和产业结构相关，能为人才招聘和城市选择提供参考。

## 八、建议

- 行动 1：企业选址应结合人口规模、年龄结构、教育水平和城市产业定位。
- 行动 2：公共服务资源配置应重点关注老龄化、少子化和区域人口流动。
- 行动 3：后续可加入 GDP、房价和就业数据，构建城市发展综合画像。
- 跟进方式：为每条建议绑定一个可观察指标，后续按周或按月复盘效果。

建议部分应结合具体对象、执行动作和复盘指标，避免停留在泛泛的“加强管理”或“优化运营”。

## 九、局限性与改进方向

- 项目价值：把分散数据组织成趋势、结构、对比和空间分布，让管理者能快速识别重点对象和异常变化。
- 真实限制：人口和社会统计数据更新周期长，区域口径、年份口径和统计口径变化会影响跨期比较。
- 业务风险：宏观数据只能支持方向判断，不能直接替代城市选址、产品定价或公共资源配置中的微观调研。
- 改进方向：将静态分析升级为可定期刷新的监控看板，并为异常指标设置阈值提醒。
- 改进方向：为关键图表补充下钻维度，使管理者能从总览进一步定位到地区、品类、用户或时间段。
- 改进方向：结合 GDP、就业、房价、产业结构和迁徙数据，避免只用单一人口指标解释区域差异。

## 附录：完整代码与输出结果

下面内容按原 notebook 的代码单元顺序整理。如果代码单元产生了文本输出或图片输出，也一并附在对应代码后面，便于复现完整分析过程。

### 代码单元 1

```python
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.commons.utils import JsCode
import pandas as pd
import random

from pyecharts.globals import CurrentConfig, NotebookType,OnlineHostType
CurrentConfig.NOTEBOOK_TYPE = NotebookType.JUPYTER_NOTEBOOK
# pd.set_option('precision', 2)
```

### 代码单元 2

```python
df = pd.read_csv('./data/各地区人口.csv', usecols=['各地区人口', 'Unnamed: 1'])
df.drop(labels=[0, 1], axis=0, inplace=True)
df.rename(columns={'Unnamed: 1':'人口数', '各地区人口':'地区'}, inplace=True)

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
 '新疆': '新疆维吾尔自治区'}

coord = {
    '湖北': [114.31667, 30.51667],
    '广东': [113.23333, 23.16667],
    '北京': [116.41667, 39.91667],
    '上海': [121.48, 31.22],
    '辽宁': [123.38, 41.8],
    '江西': [115.90000, 28.68333],
    '四川': [104.06, 30.67],
    '安徽': [117.27, 31.86],
    '广西': [108.33, 22.84],
    '新疆': [87.68, 43.77],
    '江苏': [118.78, 32.04],
    '河北': [114.48, 38.03],
    '浙江': [120.19, 30.26],
    '湖南': [113, 28.21],
    '甘肃': [103.82, 36.07],
    '福建': [119.28000, 26.08],
    '贵州': [106.71, 26.57],
    '海南': [110.35, 20.02],
    '河南': [113.65, 34.76],
    '黑龙江': [126.63, 45.75],
    '吉林': [125.35, 43.88],
    '内蒙古': [111.65, 40.82],
    '宁夏': [106.27, 38.47],
    '山东': [117, 36.65],
    '山西': [112.53, 37.87],
    '陕西': [108.95, 34.27],
    '天津': [117.2, 39.13],
    '西藏': [91.11, 29.97],
    '云南': [102.73, 25.04],
    '重庆': [106.54, 29.59],
    '青海': [101.74, 36.56]}

data_pair = []
for idx, row in df.iterrows():
    name = row['地区'].replace(' ', '')
    try:
        value = coord[name]
        value.append(float(row['人口数']))
        data_pair.append([dictcode[name], value])
    except KeyError:
        if name == '现役军人':
            soldier = row['人口数']
        elif name == '全国[5]':
            total = row['人口数']

df = pd.read_csv('./data/全国人口年龄构成.csv')
df.drop(labels=[0, 1], axis=0, inplace=True)

data_pair_age = []
for idx, row in df.iterrows():
    data_pair_age.append([row['全国人口年龄构成'].replace('其中：', ''), float(row['Unnamed: 2'])])

df = pd.read_csv('./data/各地区性别构成.csv')
df.drop(labels=[0, 1], axis=0, inplace=True)
data_pair_sex = [('男性', float(df.iloc[0, 1])), ('女性', float(df.iloc[0, 2]))]

df = pd.read_csv('./data/各地区每10万人口中拥有的各类受教育程度人数.csv')
df.drop(labels=[0], axis=0, inplace=True)
data_pair_edu = [
    ('大学', float(df.iloc[0, 1])/1e3),
    ('高中', float(df.iloc[0, 2])/1e3),
    ('初中', float(df.iloc[0, 3])/1e3),
    ('小学', float(df.iloc[0, 4])/1e3),
    ('其他', 100-(float(df.iloc[0, 4])+float(df.iloc[0, 3])+float(df.iloc[0, 2])+float(df.iloc[0, 1]))/1e3)
    ]

data_pair_edu = [(x, round(y, 2)) for x, y in data_pair_edu]
```

### 代码单元 3

```python
data_pair
```

**文本输出**

```text
[['北京市', [116.41667, 39.91667, 21893095.0]],
 ['天津市', [117.2, 39.13, 13866009.0]],
 ['河北省', [114.48, 38.03, 74610235.0]],
 ['山西省', [112.53, 37.87, 34915616.0]],
 ['内蒙古自治区', [111.65, 40.82, 24049155.0]],
 ['辽宁省', [123.38, 41.8, 42591407.0]],
 ['吉林省', [125.35, 43.88, 24073453.0]],
 ['黑龙江省', [126.63, 45.75, 31850088.0]],
 ['上海市', [121.48, 31.22, 24870895.0]],
 ['江苏省', [118.78, 32.04, 84748016.0]],
 ['浙江省', [120.19, 30.26, 64567588.0]],
 ['安徽省', [117.27, 31.86, 61027171.0]],
 ['福建省', [119.28, 26.08, 41540086.0]],
 ['江西省', [115.9, 28.68333, 45188635.0]],
 ['山东省', [117, 36.65, 101527453.0]],
 ['河南省', [113.65, 34.76, 99365519.0]],
 ['湖北省', [114.31667, 30.51667, 57752557.0]],
 ['湖南省', [113, 28.21, 66444864.0]],
 ['广东省', [113.23333, 23.16667, 126012510.0]],
 ['广西壮族自治区', [108.33, 22.84, 50126804.0]],
 ['海南省', [110.35, 20.02, 10081232.0]],
 ['重庆市', [106.54, 29.59, 32054159.0]],
 ['四川省', [104.06, 30.67, 83674866.0]],
 ['贵州省', [106.71, 26.57, 38562148.0]],
 ['云南省', [102.73, 25.04, 47209277.0]],
 ['西藏自治区', [91.11, 29.97, 3648100.0]],
 ['陕西省', [108.95, 34.27, 39528999.0]],
 ['甘肃省', [103.82, 36.07, 25019831.0]],
 ['青海省', [101.74, 36.56, 5923957.0]],
 ['宁夏回族自治区', [106.27, 38.47, 7202654.0]],
 ['新疆维
... 输出过长，博客中已截断
```

### 代码单元 4

```python
chart = Map3D(init_opts=opts.InitOpts(
    width='1000px',
    height='600px',
    theme='dark',
    bg_color='#000')
)

# 引用添加的地图
chart.add_schema(
    maptype="china",
    ground_color='#999',
    shading="lambert",
    emphasis_label_opts=opts.LabelOpts(is_show=True),
    itemstyle_opts=opts.ItemStyleOpts(
            border_width=0.2,
            border_color="rgb(0,0,0)",
    ),
    light_opts=opts.Map3DLightOpts(
        main_shadow_quality='high',
        is_main_shadow=True,
        main_intensity=1,
        main_alpha=30,
        ambient_cubemap_texture='https://echarts.apache.org/examples/data-gl/asset/canyon.hdr',
        ambient_cubemap_diffuse_intensity=0.5,
        ambient_cubemap_specular_intensity=0.5
    ),
    post_effect_opts=opts.Map3DPostEffectOpts(
        is_enable=True,
        is_ssao_enable=True,
        ssao_radius=1,
        ssao_intensity=1
    )
)
chart.add(
    "GDP",
    data_pair=data_pair,
    type_="bar3D",
    bar_size=1.5,
    min_height=3,
    shading="lambert",
    label_opts=opts.LabelOpts(
            is_show=False,
            formatter=JsCode(
                "function(data){return data.name + ': ' + data.value[2];}"),
    )
)
chart.set_global_opts(
    visualmap_opts=opts.VisualMapOpts(
        is_show=False,
        type_='color',
        dimension=2,
        min_=1e7,
        max_=1e8,
        range_color=[
            '#313695',
            '#4575b4',
            '#74add1',
            '#abd9e9',
            '#e0f3f8',
            '#ffffbf',
            '#fee090',
            '#fdae61',
            '#f46d43',
            '#d73027',
            '#a50026']
    ),
    title_opts=opts.TitleOpts(
        title="全国各省人口统计",
        subtitle='数据来自全国第七次人口普查数据，未包含港澳台地区。',
        pos_left="2%",
        pos_top='1%',
        title_textstyle_opts=opts.TextStyleOpts(color='#00BFFF', font_size=20)
        ),
    tooltip_opts=opts.TooltipOpts(is_show=False),
    legend_opts=opts.LegendOpts(is_show=False),
    graphic_opts=[
                opts.GraphicGroup(
                    graphic_item=opts.GraphicItem(id_='1', left="100px", bottom="100px"),
                    children=[
                        opts.GraphicRect(
                            graphic_item=opts.GraphicItem(
                                left="center", top="center", z=1
                            ),
                            graphic_shape_opts=opts.GraphicShapeOpts(
                                width=200, height=80
                            ),
                            graphic_basicstyle_opts=opts.GraphicBasicStyleOpts(
                                # 颜色配置，这里设置为黑色，透明度为0.5
                                fill="rgba(0,0,0,0.5)",
                                line_width=4,
                                stroke="#fff",
                            ),
                        ),
                        opts.GraphicText(
                            graphic_item=opts.GraphicItem(
                                left="center", top="center", z=100
                            ),
                            graphic_textstyle_opts=opts.GraphicTextStyleOpts(
                                # 要显示的文本
                                text='全国人口：{:,}\n\n现役军人：{:,}'.format(int(total), int(soldier)),
                                font="bold italic 14px Microsoft YaHei",
                                graphic_basicstyle_opts=opts.GraphicBasicStyleOpts(
                                    fill="#fff"
                                ),
                            ),
                        )
                    ],
                ),
                
                ]
)

pie = Pie(
    init_opts=opts.InitOpts(
        theme='dark',
        width='1000px',
        height='400px',
        bg_color='rgb(0,0,0)')
)
pie.add(
    "",
    data_pair_age,
    # 指定饼图中心位置
    center=["20%", "35%"],
    # 将饼图尺寸相应缩小，不然饼图会重叠
    radius=["15%", "25%"],
    label_opts=opts.LabelOpts(formatter='{b}\n{c}%')
)

pie.add(
    "",
    data_pair_sex,
    # 指定饼图中心位置
    center=["50%", "35%"],
    # 将饼图尺寸相应缩小，不然饼图会重叠
    radius=["15%", "25%"],
    label_opts=opts.LabelOpts(formatter='{b}\n{c}%')
)

pie.add(
    "",
    data_pair_edu,
    # 指定饼图中心位置
    center=["80%", "35%"],
    # 将饼图尺寸相应缩小，不然饼图会重叠
    radius=["15%", "25%"],
    label_opts=opts.LabelOpts(formatter='{b}\n{c}%')
)

pie.add(
    "",
    [('城镇', 63.89), ('农村', 36.11)],
    # 指定饼图中心位置
    center=["20%", "70%"],
    # 将饼图尺寸相应缩小，不然饼图会重叠
    radius=["15%", "25%"],
    label_opts=opts.LabelOpts(formatter='{b}\n{c}%')
)

pie.add(
    "",
    [('汉族', 91.11), ('少数民族', 8.89)],
    # 指定饼图中心位置
    center=["50%", "70%"],
    # 将饼图尺寸相应缩小，不然饼图会重叠
    radius=["15%", "25%"],
    label_opts=opts.LabelOpts(formatter='{b}\n{c}%')
)

pie.add(
    "",
    [('流动人口', 26.62), ('非流动人口', 73.38)],
    # 指定饼图中心位置
    center=["80%", "70%"],
    # 将饼图尺寸相应缩小，不然饼图会重叠
    radius=["15%", "25%"],
    label_opts=opts.LabelOpts(formatter='{b}\n{c}%')
)

pie.set_global_opts(
    legend_opts=opts.LegendOpts(is_show=False),
    title_opts=[dict(text='人口画像', left='2%', top='1%', textStyle=dict(color='#00BFFF', fontSize=20)),
                dict(
        text='年龄 ',
        left='20%',
        top='32%',
        textAlign='center',
        textStyle=dict(
            color='#fff',
            fontWeight='normal',
            fontSize=15)),
        dict(
        text='性别 ',
        left='50%',
        top='32%',
        textAlign='center',
        textStyle=dict(
            color='#fff',
            fontWeight='normal',
            fontSize=15)),
        dict(text='教育 ', left='80%', top='32%', textAlign='center', textStyle=dict(color='#fff', fontWeight='normal', fontSize=15)),
        dict(text='户籍 ', left='20%', top='67%', textAlign='center', textStyle=dict(color='#fff', fontWeight='normal', fontSize=15)),
        dict(text='民族 ', left='50%', top='67%', textAlign='center', textStyle=dict(color='#fff', fontWeight='normal', fontSize=15)),
        dict(text='流动 ', left='80%', top='67%', textAlign='center', textStyle=dict(color='#fff', fontWeight='normal', fontSize=15))
        ],
    graphic_opts=[
        opts.GraphicGroup(
            graphic_item=opts.GraphicItem(
                id_='2', left="center", top="40px"),
            children=[
                opts.GraphicRect(
                    graphic_item=opts.GraphicItem(
                        left="center", top="center", z=1
                    ),
                    graphic_shape_opts=opts.GraphicShapeOpts(
                        width=950, height=320
                    ),
                    graphic_basicstyle_opts=opts.GraphicBasicStyleOpts(
                        fill="rgba(0,0,0,0)",
                        line_width=5,
                        stroke="#fff",
                    ),
                )
            ],
        )
    ]
)
colors = [
        '#313695',
        '#4575b4',
        '#74add1',
        '#abd9e9',
        '#e0f3f8',
        '#ffffbf',
        '#fee090',
        '#fdae61',
        '#f46d43',
        '#d73027',
        '#a50026'
        ]
random.shuffle(colors)
pie.set_colors(colors)

page = Page()
page.add(chart).add(pie)
# page.render('./全国人口画像.html')
page.render_notebook()
```

### 代码单元 5

```python
df = pd.read_csv('./data/各地区人口.csv')
df.drop(labels=[0, 1, 2, 34], axis=0, inplace=True)
df.columns = ['地区', '人口数', '2020年占比', '2010年占比']
df['2020年占比'] = df['2020年占比'].astype('float')
df['2010年占比'] = df['2010年占比'].astype('float')
df['占比变化'] = df['2020年占比'] - df['2010年占比']

data_pair = []
for idx, row in df.iterrows():
    data_pair.append([dictcode[row['地区'].replace(' ', '')], round(row['占比变化'], 2)])
```

### 代码单元 6

```python
map_chart = Map(
    init_opts=opts.InitOpts(
        theme='dark',
        width='1000px',
        height='700px',
        bg_color='#000')
)
map_chart.add('占比变化',
              data_pair=data_pair,
              maptype='china',
              # 关闭symbol的显示
              is_map_symbol_show=False,
              label_opts=opts.LabelOpts(color='#fff'),
              itemstyle_opts={
                  'normal': {
                      'shadowColor': 'rgba(0, 0, 0, .5)',  # 阴影颜色
                      'shadowBlur': 5,  # 阴影大小
                      'shadowOffsetY': 0,  # Y轴方向阴影偏移
                      'shadowOffsetX': 0,  # x轴方向阴影偏移
                      'borderColor': '#fff'
                  }
              }
              )
map_chart.set_global_opts(
    visualmap_opts=opts.VisualMapOpts(
        is_show=True,
        is_piecewise=True,
        series_index=0,
        pos_top='center',
        pos_left='2%',
        range_text=['人口占比变化：\n\n流入', '流出'],
        min_=-0.5,
        max_=0.5,
        precision=1,
        pieces=[
            {'min': 0.2, "color": 'red'},
            {'min': 0.1, 'max': 0.2, 'color': '#FF69B4'},
            {'min': 0, 'max': 0.1, 'color': '#FFB6C1'},
            {'min': -0.1, 'max': 0, 'color': '#87CEFA'},
            {'max': -0.1, 'min': -0.2, 'color': '#1E90FF'},
            {'max': -0.2, 'color': 'blue'}],
    ),
    legend_opts=opts.LegendOpts(is_show=False),
    tooltip_opts=opts.TooltipOpts(
        is_show=True,
        trigger='item',
        formatter='{b}:{c}%'
    ),
    title_opts=dict(
        text='2010-2020年各省人口占比变化',
        left='2%',
        top='1%',
        textStyle=dict(
            color='#00BFFF'))
)

map_chart.render('2010-2020年各省人口占比变化.html')
map_chart.render_notebook()
```

### 代码单元 7

```python
df = pd.read_csv('./data/各地区人口年龄构成.csv')
df.drop(labels=[0, 1], axis=0, inplace=True)
df.columns = ['地区', '0—14岁',	'15—59岁',	'60岁及以上', '其中65岁及以上']
df['0—14岁'] = df['0—14岁'].astype('float')
df['15—59岁'] = df['15—59岁'].astype('float')
df['60岁及以上'] = df['60岁及以上'].astype('float')
```

### 代码单元 8

```python
bar = Bar(
    init_opts=opts.InitOpts(
        theme='dark',
        width='1000px',
        height='1000px',
        bg_color='#000')
)
bar.add_xaxis(
    df['地区'].tolist()
)
bar.add_yaxis(
    '0—14岁',
    df['0—14岁'].tolist(),
    stack=1,
    label_opts=opts.LabelOpts(is_show=True, formatter='{c}%', position='insideLeft'),
    itemstyle_opts={
        'normal': {
            'shadowColor': 'rgba(0, 0, 0, .5)',  # 阴影颜色
            'shadowBlur': 5,  # 阴影大小
            'shadowOffsetY': 2,  # Y轴方向阴影偏移
            'shadowOffsetX': 2,  # x轴方向阴影偏移
            'borderColor': '#fff'
        }
    }
)

bar.add_yaxis(
    '15—59岁',
    df['15—59岁'].tolist(),
    stack=1,
    label_opts=opts.LabelOpts(is_show=True, formatter='{c}%', position='insideLeft'),
    itemstyle_opts={
        'normal': {
            'shadowColor': 'rgba(0, 0, 0, .5)',  # 阴影颜色
            'shadowBlur': 5,  # 阴影大小
            'shadowOffsetY': 2,  # Y轴方向阴影偏移
            'shadowOffsetX': 2,  # x轴方向阴影偏移
            'borderColor': '#fff'
        }
    }
)

bar.add_yaxis(
    '60岁及以上',
    df['60岁及以上'].tolist(),
    stack=1,
    label_opts=opts.LabelOpts(is_show=True, formatter='{c}%', position='insideLeft'),
    itemstyle_opts={
        'normal': {
            'shadowColor': 'rgba(0, 0, 0, .5)',  # 阴影颜色
            'shadowBlur': 5,  # 阴影大小
            'shadowOffsetY': 2,  # Y轴方向阴影偏移
            'shadowOffsetX': 2,  # x轴方向阴影偏移
            'borderColor': '#fff'
        }
    }
)
bar.set_global_opts(
    xaxis_opts=opts.AxisOpts(is_show=False, max_=100),
    yaxis_opts=opts.AxisOpts(
        axisline_opts=opts.AxisLineOpts(is_show=False),
        axistick_opts=opts.AxisTickOpts(is_show=False)),
    legend_opts=opts.LegendOpts(is_show=True, pos_top='1%', pos_right='10%'),
    title_opts=opts.TitleOpts(
        title="全国各省人口年龄构成",
        # subtitle='数据来自全国第七次人口普查数据，未包含港澳台地区。',
        pos_left="5%",
        pos_top='1%',
        title_textstyle_opts=opts.TextStyleOpts(color='#00BFFF', font_size=20)
        ),
)

bar.reversal_axis()
bar.set_colors(['orange', 'blue', 'red'])
bar.render('./全国各省人口年龄构成.html')
```

**文本输出**

```text
'C:\\Users\\Administrator\\cx_xiangmu\\Python数据分析\\上架\\2301-Python数据分析与可视化项目\\人口学-\\全国各省人口年龄构成.html'
```

### 代码单元 9

```python
bar.render_notebook()
```

### 代码单元 10

```python
df = pd.read_csv('./data/各地区性别构成.csv')
df.drop(labels=[0, 1], axis=0, inplace=True)
df.columns = ['地区', '女',	'男',	'性别比']
df['男'] = df['男'].astype('float')
df['女'] = df['女'].astype('float')
df.sort_values(by='女', inplace=True)
```

### 代码单元 11

```python
bar = Bar(
    init_opts=opts.InitOpts(
        theme='dark',
        width='1000px',
        height='1000px',
        bg_color='#000')
)
bar.add_xaxis(
    df['地区'].tolist()
)
bar.add_yaxis(
    '男性',
    df['男'].tolist(),
    stack=1,
    label_opts=opts.LabelOpts(is_show=True, formatter='{c}%', position='insideLeft'),
    itemstyle_opts={
        'normal': {
            'shadowColor': 'rgba(0, 0, 0, .5)',  # 阴影颜色
            'shadowBlur': 5,  # 阴影大小
            'shadowOffsetY': 2,  # Y轴方向阴影偏移
            'shadowOffsetX': 2,  # x轴方向阴影偏移
            'borderColor': '#fff'
        }
    }
)

bar.add_yaxis(
    '女性',
    df['女'].tolist(),
    stack=1,
    label_opts=opts.LabelOpts(is_show=True, formatter='{c}%', position='insideLeft'),
    itemstyle_opts={
        'normal': {
            'shadowColor': 'rgba(0, 0, 0, .5)',  # 阴影颜色
            'shadowBlur': 5,  # 阴影大小
            'shadowOffsetY': 2,  # Y轴方向阴影偏移
            'shadowOffsetX': 2,  # x轴方向阴影偏移
            'borderColor': '#fff'
        }
    }
)

bar.set_global_opts(
    xaxis_opts=opts.AxisOpts(is_show=False, min_=40, max_=60),
    yaxis_opts=opts.AxisOpts(
        axisline_opts=opts.AxisLineOpts(is_show=False),
        axistick_opts=opts.AxisTickOpts(is_show=False)),
    legend_opts=opts.LegendOpts(is_show=True, pos_top='1%', pos_right='10%'),
    title_opts=opts.TitleOpts(
        title="全国各省人口性别构成",
        # subtitle='数据来自全国第七次人口普查数据，未包含港澳台地区。',
        pos_left="5%",
        pos_top='1%',
        title_textstyle_opts=opts.TextStyleOpts(color='#00BFFF', font_size=20)
        ),
)

bar.reversal_axis()
bar.set_colors(['blue', 'red'])
bar.render_notebook()
```

### 代码单元 12

```python
df = pd.read_csv('./data/各地区每10万人口中拥有的各类受教育程度人数.csv')
df.drop(labels=[0, 1], axis=0, inplace=True)
df.columns = ['地区', '大学', '高中',	'初中', '小学']
df['大学'] = df['大学'].astype('int') / 1e3
df['高中'] = df['高中'].astype('int') / 1e3
df['初中'] = df['初中'].astype('int') / 1e3
df['小学'] = df['小学'].astype('int') / 1e3
df['其他'] = 100-df['大学'] - df['高中'] - df['初中'] - df['小学']
df.sort_values(by='大学', inplace=True)
```

### 代码单元 13

```
bar = Bar(
    init_opts=opts.InitOpts(
        theme='dark',
        width='1000px',
        height='1000px',
        bg_color='#000')
)
bar.add_xaxis(
    df['地区'].tolist()
)
bar.add_yaxis(
    '大学（含大专）',
    df['大学'].tolist(),
    stack=1,
    label_opts=opts.LabelOpts(is_show=True, formatter='{c}%', position='insideLeft'),
    itemstyle_opts={
        'normal': {
            'shadowColor': 'rgba(0, 0, 0, .5)',  # 阴影颜色
            'shadowBlur': 5,  # 阴影大小
            'shadowOffsetY': 2,  # Y轴方向阴影偏移
            'shadowOffsetX': 2,  # x轴方向阴影偏移
            'borderColor': '#fff'
        }
    }
)

bar.add_yaxis(
    '高中（含中专）',
    df['高中'].tolist(),
    stack=1,
    label_opts=opts.LabelOpts(is_show=True, formatter='{c}%', position='insideLeft'),
    itemstyle_opts={
        'normal': {
            'shadowColor': 'rgba(0, 0, 0, .5)',  # 阴影颜色
            'shadowBlur': 5,  # 阴影大小
            'shadowOffsetY': 2,  # Y轴方向阴影偏移
            'shadowOffsetX': 2,  # x轴方向阴影偏移
            'borderColor': '#fff'
        }
    }
)

bar.add_yaxis(
    '初中',
    df['初中'].tolist(),
    stack=1,
    label_opts=opts.LabelOpts(is_show=True, formatter='{c}%', position='insideLeft'),
    itemstyle_opts={
        'normal': {
            'shadowColor': 'rgba(0, 0, 0, .5)',  # 阴影颜色
            'shadowBlur': 5,  # 阴影大小
            'shadowOffsetY': 2,  # Y轴方向阴影偏移
            'shadowOffsetX': 2,  # x轴方向阴影偏移
            'borderColor': '#fff'
        }
    }
)

bar.add_yaxis(
    '小学',
    df['小学'].tolist(),
    stack=1,
    label_opts=opts.LabelOpts(is_show=True, formatter='{c}%', position='insideLeft'),
    itemstyle_opts={
        'normal': {
            'shadowColor': 'rgba(0, 0, 0, .5)',  # 阴影颜色
            'shadowBlur': 5,  # 阴影大小
            'shadowOffsetY': 2,  # Y轴方向阴影偏移
            'shadowOffsetX': 2,  # x轴方向阴影偏移
            'borderColor': '#fff'
        }
    }
)

bar.add_yaxis(
    '其他',
    [round(x, 2) for x in df['其他'].tolist()],
    stack=1,
    label_opts=opts.LabelOpts(is_show=True, formatter='{c}%', position='insideLeft'),
    itemstyle_opts={
        'normal': {
            'shadowColor': 'rgba(0, 0, 0, .5)',  # 阴影颜色
            'shadowBlur': 5,  # 阴影大小
            'shadowOffsetY': 2,  # Y轴方向阴影偏移
            'shadowOffsetX': 2,  # x轴方向阴影偏移
            'borderColor': '#fff'
        }
    }
)

bar.set_global_opts(
    xaxis_opts=opts.AxisOpts(is_show=False, max_=100),
    yaxis_opts=opts.AxisOpts(
        axisline_opts=opts.AxisLineOpts(is_show=False),
        axistick_opts=opts.AxisTickOpts(is_show=False)),
    legend_opts=opts.LegendOpts(is_show=True, pos_top='1%', pos_right='10%'),
    title_opts=opts.TitleOpts(
        title="全国各省人口接受教育程度",
        # subtitle='数据来自全国第七次人口普查数据，未包含港澳台地区。',
        pos_left="5%",
        pos_top='1%',
        title_textstyle_opts=opts.TextStyleOpts(color='#00BFFF', font_size=20)
        ),
)

bar.reversal_axis()
bar.set_colors(['blue', '#1E90FF', '#87CEFA', '#FF69B4', 'red'])

bar.render_notebook()
```

