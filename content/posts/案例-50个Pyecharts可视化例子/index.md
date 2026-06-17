---
title: "50 个 Pyecharts 可视化案例：沉淀可复用的数据表达模板"
date: 2026-06-18T00:22:40+08:00
# weight: 1
# aliases: ["/first"]
categories: ["案例"]
tags: ["pyecharts", "可视化模板", "图表设计", "可视化案例"]
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

# 50 个 Pyecharts 可视化案例：沉淀可复用的数据表达模板

## 摘要

| 模块     | 内容                                                         |
| -------- | ------------------------------------------------------------ |
| 业务场景 | 案例                                                         |
| 数据来源 | 多种示例数据和可视化图表配置。                               |
| 分析方法 | Pyecharts 柱状图、折线图、地图、饼图、组合图、大屏组件和主题配置。 |
| 结论先行 | 不同图表适合不同问题：趋势用折线，结构用饼图或堆叠图，空间分布用地图，对比用柱状图。 |

本报告围绕“业务背景、分析目的、数据说明、分析思路、分析过程、核心结论和改进建议”展开，目标是用数据回答具体问题，并把分析结果转化为可执行的判断。

## 一、分析背景

可视化能力不只是会画图，更重要的是能根据指标关系选择合适图表。这个案例库可以作为后续项目快速搭建看板的组件积累。

## 二、分析目的

本次分析主要回答以下问题：

- 数据在时间、区域、类别或人群维度上呈现什么结构？
- 哪些图表最适合承载趋势、对比、分布和异常信息？
- 可视化结果如何帮助读者快速定位重点？

先明确分析目的，再开展数据处理和指标拆解，可以保证报告围绕问题展开，而不是简单罗列代码和图表。

## 三、数据来源与指标说明

| 项目           | 说明                                                         |
| -------------- | ------------------------------------------------------------ |
| 数据来源       | 多种示例数据和可视化图表配置。                               |
| 分析工具与方法 | Pyecharts 柱状图、折线图、地图、饼图、组合图、大屏组件和主题配置。 |
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

### 1. 不同图表适合不同问题：趋势用折线，结构用饼图或堆叠图，空间分布用地图，对比用柱状图。

结果解读：该发现是本项目最核心的结论之一，说明数据中存在值得关注的结构性特征。对应图表或模型结果应围绕这一判断展开，帮助读者理解结论来源。

### 2. 可视化模板能提升项目交付效率，但必须服务业务问题，不能为了炫技而堆图。

结果解读：该发现进一步解释了不同维度之间的差异。对业务决策而言，重点不只是看到差异，而是判断差异来自哪些对象、场景或指标。

### 3. 交互式图表适合探索分析和汇报展示，静态图更适合定期报告和文章传播。

结果解读：该发现可以作为后续优化策略或模型改进的依据。若用于真实业务，还需要结合成本、资源、实验结果或线上反馈继续验证。

## 七、结论

综合以上分析，可以得到以下结论：

- 不同图表适合不同问题：趋势用折线，结构用饼图或堆叠图，空间分布用地图，对比用柱状图。
- 可视化模板能提升项目交付效率，但必须服务业务问题，不能为了炫技而堆图。
- 交互式图表适合探索分析和汇报展示，静态图更适合定期报告和文章传播。

## 八、建议

- 行动 1：建议把常用图表封装为函数，并统一配色、字体和标题规范。
- 行动 2：业务报告中每张图都应配一句结论，避免只展示图形而缺少解释。
- 行动 3：后续可整理为个人可视化组件库，提高项目复用度。
- 跟进方式：为每条建议绑定一个可观察指标，后续按周或按月复盘效果。

建议部分应结合具体对象、执行动作和复盘指标，避免停留在泛泛的“加强管理”或“优化运营”。

## 九、局限性与改进方向

- 项目价值：把分散数据组织成趋势、结构、对比和空间分布，让管理者能快速识别重点对象和异常变化。
- 真实限制：当前数据只覆盖项目样本范围，缺少线上业务闭环中的成本、反馈、人工审核和长期跟踪信息。
- 业务风险：如果把离线分析结论直接用于真实决策，可能因为数据时效、样本偏差或执行条件变化造成效果偏离。
- 改进方向：将静态分析升级为可定期刷新的监控看板，并为异常指标设置阈值提醒。
- 改进方向：为关键图表补充下钻维度，使管理者能从总览进一步定位到地区、品类、用户或时间段。

## 附录：完整代码与输出结果

下面内容按原 notebook 的代码单元顺序整理。如果代码单元产生了文本输出或图片输出，也一并附在对应代码后面，便于复现完整分析过程。

### 代码单元 1

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker

def bar_stack():
    bar = Bar(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))
    bar.add_xaxis(Faker.choose())
    # stack值一样的系列会堆叠在一起
    bar.add_yaxis('A', Faker.values(), stack='stack1')
    bar.add_yaxis('B', Faker.values(), stack='stack1')
    bar.add_yaxis('C', Faker.values(), stack='stack2')
    return bar

chart = bar_stack()
chart.render_notebook()
```

### 代码单元 2

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker

def bar_with_axis_off():
    bar = Bar(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))
    bar.add_xaxis(Faker.choose())
    bar.add_yaxis('', Faker.values())
    # 碰上类目标签过长的时候，可以选择关闭坐标轴，直接显示在图形中
    bar.set_series_opts(label_opts=opts.LabelOpts(position='insideLeft', formatter='{b}:{c}'))
    bar.set_global_opts(xaxis_opts=opts.AxisOpts(is_show=False),
                        yaxis_opts=opts.AxisOpts(is_show=False))
    bar.reversal_axis()
    return bar

chart = bar_with_axis_off()
chart.render_notebook()
```

### 代码单元 3

```
from pyecharts.charts import *
from pyecharts import options as opts
import random

x_data = list(range(2010, 2020))
y_data = [random.randint(20, 200) for _ in range(len(x_data))]

def bar_with_custom_axis_label():
    bar = Bar(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))
    bar.add_xaxis(x_data)
    bar.add_yaxis('', y_data)

    bar.set_global_opts(xaxis_opts=opts.AxisOpts(
        # 自定义坐标轴标签，在年份后加上`年`
        axislabel_opts=opts.LabelOpts(formatter='{value}年')))
    return bar

chart = bar_with_custom_axis_label()
chart.render_notebook()
```

### 代码单元 4

```
from pyecharts.charts import *
from pyecharts import options as opts
import random

x_data = [random.randint(0, 20) for _ in range(100)]
y_data = [random.randint(0, 50) for _ in range(100)]

def scatter_with_value_xaxis():
    scatter = Scatter(init_opts=opts.InitOpts(theme='light',
                                              width='1000px',
                                              height='600px'))
    scatter.add_xaxis(x_data)
    scatter.add_yaxis('', y_data)
    # X轴默认数据类型为离散数据，设置为数值型
    scatter.set_global_opts(xaxis_opts=opts.AxisOpts(type_="value"))
    return scatter

chart = scatter_with_value_xaxis()
chart.render_notebook()
```

### 代码单元 5

```
from pyecharts.charts import *
from pyecharts import options as opts
import random

x_data = ['香蕉', '梨子', '水蜜桃', '核桃', '西瓜', '苹果']
y_data_1 = [random.randint(10, 50) for _ in range(len(x_data))]
y_data_2 = [random.randint(100, 500) for _ in range(len(x_data))]

def bar_line_combine_with_two_axis():
    bar = Bar(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))
    bar.add_xaxis(x_data)
    # 添加一个Y轴
    bar.extend_axis(yaxis=opts.AxisOpts())
    bar.add_yaxis('左边Y轴', y_data_1, yaxis_index=0)

    line = Line(init_opts=opts.InitOpts(theme='light',
                                        width='1000px',
                                        height='600px'))
    line.add_xaxis(x_data)
    # 将line数据通过yaxis_index指向后添加的Y轴
    line.add_yaxis('右边Y轴', y_data_2, yaxis_index=1)

    bar.overlap(line)
    return bar

chart = bar_line_combine_with_two_axis()
chart.render_notebook()
```

### 代码单元 6

```
from pyecharts.charts import *
from pyecharts import options as opts
import random

x_data = ['香蕉', '梨子', '水蜜桃', '核桃', '西瓜', '苹果']
y_data_1 = [random.randint(10, 50) for _ in range(len(x_data))]
y_data_2 = [random.randint(100, 500) for _ in range(len(x_data))]

def bar_with_multiple_axis():
    bar = Bar(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))
    bar.add_xaxis(x_data)
    # 添加一个Y轴
    bar.extend_axis(yaxis=opts.AxisOpts())
    # 分别指定使用的Y轴
    bar.add_yaxis('左边Y轴', y_data_1, yaxis_index=0)
    bar.add_yaxis('右边Y轴', y_data_2, yaxis_index=1)
    return bar

chart = bar_with_multiple_axis()
chart.render_notebook()
```

### 代码单元 7

```
from pyecharts.charts import *
from pyecharts import options as opts
import random

x_data_1 = ["2020/10/{}".format(i + 1) for i in range(30)]
x_data_2 = ["2019/10/{}".format(i + 1) for i in range(30)]
y_data_1 = [random.randint(10, 50) for _ in range(30)]
y_data_2 = [random.randint(20, 60) for _ in range(30)]

def line_with_two_xaxis():
    line = Line(init_opts=opts.InitOpts(theme='light',
                                        width='1000px',
                                        height='600px'))
    line.add_xaxis(x_data_1)
    # 添加一个x轴
    line.extend_axis(xaxis_data=x_data_2, xaxis=opts.AxisOpts())
    line.add_yaxis('下面X轴', y_data_1)
    line.add_yaxis('上面X轴', y_data_2)
    return line

chart = line_with_two_xaxis()
chart.render_notebook()
```

### 代码单元 8

```
from pyecharts.charts import *
from pyecharts import options as opts
import random

ios_icon = 'path://M24.734 17.003c-0.040-4.053 3.305-5.996 3.454-6.093-1.88-2.751-4.808-3.127-5.851-3.171-2.492-0.252-4.862 1.467-6.127 1.467-1.261 0-3.213-1.43-5.28-1.392-2.716 0.040-5.221 1.579-6.619 4.012-2.822 4.897-0.723 12.151 2.028 16.123 1.344 1.944 2.947 4.127 5.051 4.049 2.026-0.081 2.793-1.311 5.242-1.311s3.138 1.311 5.283 1.271c2.18-0.041 3.562-1.981 4.897-3.931 1.543-2.255 2.179-4.439 2.216-4.551-0.048-0.022-4.252-1.632-4.294-6.473zM20.705 5.11c1.117-1.355 1.871-3.235 1.665-5.11-1.609 0.066-3.559 1.072-4.713 2.423-1.036 1.199-1.942 3.113-1.699 4.951 1.796 0.14 3.629-0.913 4.747-2.264z'
android_icon = 'path://M28 12c-1.1 0-2 0.9-2 2v8c0 1.1 0.9 2 2 2s2-0.9 2-2v-8c0-1.1-0.9-2-2-2zM4 12c-1.1 0-2 0.9-2 2v8c0 1.1 0.9 2 2 2s2-0.9 2-2v-8c0-1.1-0.9-2-2-2zM7 23c0 1.657 1.343 3 3 3v0 4c0 1.1 0.9 2 2 2s2-0.9 2-2v-4h4v4c0 1.1 0.9 2 2 2s2-0.9 2-2v-4c1.657 0 3-1.343 3-3v-11h-18v11zM24.944 10c-0.304-2.746-1.844-5.119-4.051-6.551l1.001-2.001c0.247-0.494 0.047-1.095-0.447-1.342s-1.095-0.047-1.342 0.447l-1.004 2.009-0.261-0.104c-0.893-0.297-1.848-0.458-2.84-0.458s-1.947 0.161-2.84 0.458l-0.261 0.104-1.004-2.009c-0.247-0.494-0.848-0.694-1.342-0.447s-0.694 0.848-0.447 1.342l1.001 2.001c-2.207 1.433-3.747 3.805-4.051 6.551v1h17.944v-1h-0.056zM13 8c-0.552 0-1-0.448-1-1s0.447-0.999 0.998-1c0.001 0 0.002 0 0.003 0s0.001-0 0.002-0c0.551 0.001 0.998 0.448 0.998 1s-0.448 1-1 1zM19 8c-0.552 0-1-0.448-1-1s0.446-0.999 0.998-1c0 0 0.001 0 0.002 0s0.002-0 0.003-0c0.551 0.001 0.998 0.448 0.998 1s-0.448 1-1 1z'

x_data = ["2020/7/{}".format(i + 1) for i in range(10)]

# 随机生成点数据
y_data_1 = [random.randint(10, 20) for i in range(len(x_data))]
y_data_2 = [random.randint(15, 25) for i in range(len(x_data))]

def bar_custom_legend_symbol():
    # 当前并不支持同一个图表针对不同的系列设置不同的icon
    # 方案是将多个系列的数据拆分到多个图表设置各自的icon，最后通过grid将图表组合起来
    ios_bar = Bar()
    ios_bar.add_xaxis(x_data)
    ios_bar.add_yaxis('IOS', y_data_1)
    ios_bar.set_global_opts(legend_opts=opts.LegendOpts(legend_icon=ios_icon,
                                                        pos_right='15%'))

    az_bar = Bar()
    az_bar.add_xaxis(x_data)
    az_bar.add_yaxis('Android', y_data_2)
    az_bar.set_global_opts(legend_opts=opts.LegendOpts(legend_icon=android_icon,
                                                       pos_right='5%'))

    # 将az_bar和ios_bar组合起来
    grid = Grid(init_opts=opts.InitOpts(theme='light',
                                        width='1000px',
                                        height='600px'))
    grid.add(ios_bar, is_control_axis_index=True, grid_opts=opts.GridOpts())
    grid.add(az_bar, is_control_axis_index=True, grid_opts=opts.GridOpts())
    return grid

chart = bar_custom_legend_symbol()
chart.render_notebook()
```

### 代码单元 9

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker

def bar_single_selected():
    bar = Bar(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))
    bar.add_xaxis(Faker.choose())
    bar.add_yaxis('A', Faker.values())
    bar.add_yaxis('B', Faker.values())
    # 设置图例选择模式为单选
    bar.set_global_opts(legend_opts=opts.LegendOpts(selected_mode='single'))
    return bar

chart = bar_single_selected()
chart.render_notebook()
```

### 代码单元 10

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker

def bar_with_default_selected_series():
    bar = Bar(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))
    bar.add_xaxis(Faker.choose())
    # 默认选中A C
    bar.add_yaxis('A', Faker.values(), is_selected=True)
    bar.add_yaxis('B', Faker.values(), is_selected=False)
    bar.add_yaxis('C', Faker.values(), is_selected=True)
    return bar

chart = bar_with_default_selected_series()
chart.render_notebook()
```

### 代码单元 11

```
from pyecharts.charts import *
from pyecharts import options as opts
import random

x_data = ["2020/10/{}".format(i + 1) for i in range(30)]

# 随机生成点数据
y_data = [random.randint(10, 20) for i in range(len(x_data))]

def bar_datazoom_inside():
    bar = Bar(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))
    bar.add_xaxis(x_data)
    bar.add_yaxis('', y_data)
    bar.set_global_opts(datazoom_opts=opts.DataZoomOpts(type_='inside',
                                                        range_start=50,   # 设置起止位置，50%-100%
                                                        range_end=100))
    return bar

chart = bar_datazoom_inside()
chart.render_notebook()
```

### 代码单元 12

```
from pyecharts.charts import *
from pyecharts import options as opts
import random

x_data = ["2020/10/{}".format(i + 1) for i in range(30)]

# 随机生成点数据
y_data = [random.randint(10, 20) for i in range(len(x_data))]

def bar_with_datazoom_slider():
    bar = Bar(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))
    bar.add_xaxis(x_data)
    bar.add_yaxis('', y_data)
    bar.set_global_opts(datazoom_opts=opts.DataZoomOpts(range_start=50,   # 设置起止位置，50%-100%
                                                        range_end=100))
    return bar

chart = bar_with_datazoom_slider()
chart.render_notebook()
```

### 代码单元 13

```
from pyecharts.charts import *
from pyecharts import options as opts
import random

x_data = ["2020/10/{}".format(i + 1) for i in range(30)]

# 随机生成点数据
y_data = [random.randint(10, 20) for i in range(len(x_data))]

def bar_datazoom_both_way():
    bar = Bar(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))
    bar.add_xaxis(x_data)
    bar.add_yaxis('', y_data)
    # 通过list传入两个datazoom_opts
    bar.set_global_opts(datazoom_opts=[opts.DataZoomOpts(),
                                       opts.DataZoomOpts(type_='inside', range_start=50, range_end=100)])
    return bar

chart = bar_datazoom_both_way()
chart.render_notebook()
```

### 代码单元 14

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker

def bar_reverse_axis():
    bar = Bar(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))
    bar.add_xaxis(Faker.choose())
    bar.add_yaxis('A', Faker.values())
    bar.add_yaxis('B', Faker.values())
    # x,y轴翻转
    bar.reversal_axis()
    return bar

chart = bar_reverse_axis()
chart.render_notebook()
```

### 代码单元 15

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker

"""
更多动画效果可参见：https://echarts.apache.org/examples/zh/editor.html?c=line-easing
"""

def bar_with_animation():
    bar = Bar(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px',
                                      animation_opts=opts.AnimationOpts(animation_delay=1000,   # 动画延时
                                                                        animation_easing='bounceIn')
                                      )
              )
    bar.add_xaxis(Faker.choose())
    bar.add_yaxis('A', Faker.values())
    bar.add_yaxis('B', Faker.values())
    return bar

chart = bar_with_animation()
chart.render_notebook()
```

### 代码单元 16

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker

def bar_with_visualmap_color():
    bar = Bar(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))
    bar.add_xaxis(Faker.choose())
    bar.add_yaxis('A', Faker.values())
    bar.add_yaxis('B', Faker.values())
    # 设置视觉组件，默认通过颜色映射数据，数值范围为0-100，可通过min_和max_进行自定义
    bar.set_global_opts(visualmap_opts=opts.VisualMapOpts())
    return bar

chart = bar_with_visualmap_color()
chart.render_notebook()
```

### 代码单元 17

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker
from pyecharts.commons.utils import JsCode

color_js = """
            new echarts.graphic.LinearGradient(
                                0,
                                1,
                                0,
                                0,
                                [{offset: 0, color: '#008B8B'},
                                 {offset: 1, color: '#FF6347'}],
                                false)
           """

def bar_with_linear_gradient_color():
    bar = Bar(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))
    bar.add_xaxis(Faker.choose())
    bar.add_yaxis('', Faker.values(),
                  # 使用JsCode执行渐变色代码
                  itemstyle_opts=opts.ItemStyleOpts(color=JsCode(color_js)))

    return bar

chart = bar_with_linear_gradient_color()
chart.render_notebook()
```

### 代码单元 18

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker
from pyecharts.commons.utils import JsCode

color_js = """new echarts.graphic.RadialGradient(
                    0.4, 0.3, 1,
                    [{offset: 0,
                      color: '#F8F8FF'},
                     {offset: 1,
                      color: '#00BFFF'}
                      ])"""

def scatter_with_radial_gradient_color():
    scatter = Scatter(init_opts=opts.InitOpts(theme='light',
                                              width='1000px',
                                              height='600px'))
    scatter.add_xaxis(Faker.choose())

    scatter.add_yaxis("", Faker.values(),
                      symbol_size=50,
                      # 渐变配色
                      itemstyle_opts=opts.ItemStyleOpts(color=JsCode(color_js)))
    return scatter

chart = scatter_with_radial_gradient_color()
chart.render_notebook()
```

### 代码单元 19

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker

def bar_with_custom_splitline():
    bar = Bar(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))
    bar.add_xaxis(Faker.choose())
    bar.add_yaxis('A', Faker.values())
    bar.add_yaxis('B', Faker.values())
    # 设置分割线
    bar.set_global_opts(yaxis_opts=opts.AxisOpts(
        splitline_opts=opts.SplitLineOpts(is_show=True,
                                          linestyle_opts=opts.LineStyleOpts(type_='dotted'))))
    return bar

chart = bar_with_custom_splitline()
chart.render_notebook()
```

### 代码单元 20

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker

def bar_with_custom_splitarea():
    bar = Bar(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))
    bar.add_xaxis(Faker.choose())
    bar.add_yaxis('A', Faker.values())
    bar.add_yaxis('B', Faker.values())
    # 设置分割区域
    bar.set_global_opts(yaxis_opts=opts.AxisOpts(
        splitarea_opts=opts.SplitAreaOpts(is_show=True,
                                          areastyle_opts=opts.AreaStyleOpts(opacity=1))))
    return bar

chart = bar_with_custom_splitarea()
chart.render_notebook()
```

### 代码单元 21

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker

def bar_with_dict_config():
    bar = Bar(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))
    bar.add_xaxis(Faker.choose())
    bar.add_yaxis('', Faker.values())
    # 通过字典配置itemstyle
    bar.set_series_opts(itemstyle_opts=dict(color='#008B8B', opacity=0.8))
    return bar

chart = bar_with_dict_config()
chart.render_notebook()
```

### 代码单元 22

```
from pyecharts.charts import *
from pyecharts import options as opts
import random

x_data = ["2020/10/{}".format(i + 1) for i in range(30)]

# 随机生成点数据
y_data = [i + random.randint(10, 20) for i in range(len(x_data))]

def line_with_area():
    line = Line(init_opts=opts.InitOpts(theme='light',
                                        width='1000px',
                                        height='600px'))
    line.add_xaxis(x_data)
    line.add_yaxis('', y_data)
    # opacity 默认为0，即透明
    line.set_series_opts(areastyle_opts=opts.AreaStyleOpts(opacity=0.5))

    return line

chart = line_with_area()
chart.render_notebook()
```

### 代码单元 23

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker

def line_stack_area():
    line = Line(init_opts=opts.InitOpts(theme='light',
                                        width='1000px',
                                        height='600px'))
    line.add_xaxis(Faker.choose())
    line.add_yaxis('A',
                   Faker.values(),
                   stack='stack')
    line.add_yaxis('B',
                   Faker.values(),
                   stack='stack')
    line.add_yaxis('C',
                   Faker.values(),
                   stack='stack')
    # opacity 默认为0，即透明
    line.set_series_opts(areastyle_opts=opts.AreaStyleOpts(opacity=0.5))

    return line

chart = line_stack_area()
chart.render_notebook()
```

### 代码单元 24

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker

def line_with_custom_linestyle():
    line = Line(init_opts=opts.InitOpts(theme='light',
                                        width='1000px',
                                        height='600px'))
    line.add_xaxis(Faker.choose())
    line.add_yaxis('样式1',
                   Faker.values(),
                   linestyle_opts=opts.LineStyleOpts(width=5,
                                                     curve=0,
                                                     opacity=0.7,
                                                     type_='solid',
                                                     color='red')
                   )
    line.add_yaxis('样式2',
                   Faker.values(),
                   linestyle_opts=opts.LineStyleOpts(width=3,
                                                     curve=0.5,
                                                     opacity=0.9,
                                                     type_='dashed',
                                                     color='yellow')
                   )
    line.add_yaxis('样式3',
                   Faker.values(),
                   linestyle_opts=opts.LineStyleOpts(width=1,
                                                     curve=1,
                                                     opacity=0.5,
                                                     type_='dotted',
                                                     color='green')
                   )
    return line

chart = line_with_custom_linestyle()
chart.render_notebook()
```

### 代码单元 25

```
from pyecharts.charts import *
from pyecharts import options as opts
import random

line_style = {
    'normal': {
        'width': 4,  # 设置线宽
        'shadowColor': 'rgba(155, 18, 184, .3)',  # 阴影颜色
        'shadowBlur': 10,  # 阴影大小
        'shadowOffsetY': 10,  # Y轴方向阴影偏移
        'shadowOffsetX': 10,  # x轴方向阴影偏移
        'curve': 0.5  # 线弯曲程度，1表示不弯曲
    }
}

x_data = ["2020/10/{}".format(i + 1) for i in range(30)]

# 随机生成点数据
y_data_1 = [i + random.randint(10, 20) for i in range(len(x_data))]
y_data_2 = [i + random.randint(15, 25) for i in range(len(x_data))]

def line_with_shadow():
    line = Line(init_opts=opts.InitOpts(theme='light',
                                        width='1000px',
                                        height='600px'))
    line.add_xaxis(x_data)
    line.add_yaxis("Android",
                   y_data_1,
                   is_symbol_show=False,
                   is_smooth=True,
                   # 传入线风格参数
                   linestyle_opts=line_style)
    line.add_yaxis("IOS",
                   y_data_2,
                   is_symbol_show=False,
                   is_smooth=True,
                   # 传入线风格参数
                   linestyle_opts=line_style)
    line.set_global_opts(title_opts=opts.TitleOpts(title="终端日活趋势"))
    return line

chart = line_with_shadow()
chart.render_notebook()
```

### 代码单元 26

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker

def line_with_smooth_connect():
    line = Line(init_opts=opts.InitOpts(theme='light',
                                        width='1000px',
                                        height='600px'))
    line.add_xaxis(Faker.choose())
    # 设置is_smooth=True来平滑曲线
    line.add_yaxis('平滑曲线', Faker.values(), is_smooth=True)
    line.add_yaxis('直线', Faker.values(), is_smooth=False)

    return line

chart = line_with_smooth_connect()
chart.render_notebook()
```

### 代码单元 27

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker

def bar_with_guide_line():
    bar = Bar(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))
    bar.add_xaxis(Faker.choose())
    bar.add_yaxis('A', Faker.values())
    bar.add_yaxis('B', Faker.values())
    # 设置标记线
    bar.set_series_opts(
        markline_opts=opts.MarkLineOpts(
            data=[
                opts.MarkLineItem(type_="min", name="最小值"),
                opts.MarkLineItem(type_="max", name="最大值"),
                opts.MarkLineItem(type_="average", name="平均值"),
            ]
        )
    )

    return bar

chart = bar_with_guide_line()
chart.render_notebook()
```

### 代码单元 28

```
from pyecharts.charts import *
from pyecharts import options as opts
import random

x_data = ["2020/10/{}".format(i + 1) for i in range(30)]

# 随机生成点数据
y_data = [i + random.randint(10, 20) for i in range(len(x_data))]

def line_with_custom_mark_point():
    line = Line(init_opts=opts.InitOpts(theme='light',
                                        width='1000px',
                                        height='600px'))
    line.add_xaxis(x_data)
    line.add_yaxis('', y_data)
    # 自定义标记点
    line.set_series_opts(
        markpoint_opts=opts.MarkPointOpts(
            data=[opts.MarkPointItem(name="自定义标记点", coord=[x_data[2], y_data[2]], value=y_data[2])]
        )
    )

    return line

chart = line_with_custom_mark_point()
chart.render_notebook()
```

### 代码单元 29

```
from pyecharts.charts import *
from pyecharts import options as opts
import random

x_data = ["2020/10/{}".format(i + 1) for i in range(30)]

# 随机生成点数据
y_data = [i + random.randint(10, 20) for i in range(len(x_data))]

def line_with_mark_area():
    line = Line(init_opts=opts.InitOpts(theme='light',
                                        width='1000px',
                                        height='600px'))
    line.add_xaxis(x_data)
    line.add_yaxis('', y_data)
    # 设置标记区域
    line.set_series_opts(
        markarea_opts=opts.MarkAreaOpts(
            data=[
                opts.MarkAreaItem(name="黄金周", x=("2020/10/1", "2020/10/8"))
            ]
        )
    )

    return line

chart = line_with_mark_area()
chart.render_notebook()
```

### 代码单元 30

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.commons.utils import JsCode

x_data = ['Apple', 'Huawei', 'Xiaomi', 'Oppo', 'Vivo', 'Meizu']
y_data = [0.98, 0.89, 0.92, 1.07, 0.81, 1.23]

js = """function (param) {return param.name +':'+ Math.floor(param.value[1])+'%';}"""

def line_with_per_show():
    line = Line(init_opts=opts.InitOpts(theme='light',
                                        width='1000px',
                                        height='600px'))
    line.add_xaxis(x_data)
    # 传入数据时先乘以100
    line.add_yaxis('', [round(v * 100, 0) for v in y_data])
    # 执行js代码让%显示
    line.set_series_opts(label_opts=opts.LabelOpts(is_show=True,
                                                   formatter=JsCode(js)))

    return line

chart = line_with_per_show()
chart.render_notebook()
```

### 代码单元 31

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker

def pictorialbar_with_custom_symbol():
    pictorialbar = PictorialBar(init_opts=opts.InitOpts(theme='light',
                                                        width='1000px',
                                                        height='600px'))
    pictorialbar.add_xaxis(Faker.choose())
    pictorialbar.add_yaxis('A',
                           Faker.values(),
                           symbol_size=20,
                           # 自定义图形
                           symbol='path://M100,0 L41.22,180.90 L195.10,69.09 L4.89,69.09 L158.77,180.90 z',
                           symbol_repeat="fixed",
                           is_symbol_clip=True
                           )

    return pictorialbar

chart = pictorialbar_with_custom_symbol()
chart.render_notebook()
```

### 代码单元 32

```
from pyecharts.charts import *
from pyecharts import options as opts

ios_icon = 'path://M24.734 17.003c-0.040-4.053 3.305-5.996 3.454-6.093-1.88-2.751-4.808-3.127-5.851-3.171-2.492-0.252-4.862 1.467-6.127 1.467-1.261 0-3.213-1.43-5.28-1.392-2.716 0.040-5.221 1.579-6.619 4.012-2.822 4.897-0.723 12.151 2.028 16.123 1.344 1.944 2.947 4.127 5.051 4.049 2.026-0.081 2.793-1.311 5.242-1.311s3.138 1.311 5.283 1.271c2.18-0.041 3.562-1.981 4.897-3.931 1.543-2.255 2.179-4.439 2.216-4.551-0.048-0.022-4.252-1.632-4.294-6.473zM20.705 5.11c1.117-1.355 1.871-3.235 1.665-5.11-1.609 0.066-3.559 1.072-4.713 2.423-1.036 1.199-1.942 3.113-1.699 4.951 1.796 0.14 3.629-0.913 4.747-2.264z'

def liquid_with_custom_shape():
    liquid = Liquid(init_opts=opts.InitOpts(theme='light',
                                            width='1000px',
                                            height='600px'))
    liquid.add('', [0.4, 0.5], shape=ios_icon)

    return liquid

chart = liquid_with_custom_shape()
chart.render_notebook()
```

### 代码单元 33

```
from pyecharts.charts import *
from pyecharts import options as opts
import datetime

# 美国covid确诊数据
data = [(datetime.datetime(2020, 1, 21, 0, 0), 1), (datetime.datetime(2020, 1, 22, 0, 0), 1),
        (datetime.datetime(2020, 1, 23, 0, 0), 1), (datetime.datetime(2020, 1, 24, 0, 0), 2),
        (datetime.datetime(2020, 1, 25, 0, 0), 2), (datetime.datetime(2020, 1, 26, 0, 0), 5),
        (datetime.datetime(2020, 1, 27, 0, 0), 5), (datetime.datetime(2020, 1, 28, 0, 0), 5),
        (datetime.datetime(2020, 1, 29, 0, 0), 5), (datetime.datetime(2020, 1, 30, 0, 0), 5),
        (datetime.datetime(2020, 1, 31, 0, 0), 7), (datetime.datetime(2020, 2, 1, 0, 0), 8),
        (datetime.datetime(2020, 2, 2, 0, 0), 8), (datetime.datetime(2020, 2, 3, 0, 0), 11),
        (datetime.datetime(2020, 2, 4, 0, 0), 11), (datetime.datetime(2020, 2, 5, 0, 0), 11),
        (datetime.datetime(2020, 2, 6, 0, 0), 11), (datetime.datetime(2020, 2, 7, 0, 0), 11),
        (datetime.datetime(2020, 2, 8, 0, 0), 11), (datetime.datetime(2020, 2, 9, 0, 0), 11),
        (datetime.datetime(2020, 2, 10, 0, 0), 11), (datetime.datetime(2020, 2, 11, 0, 0), 12),
        (datetime.datetime(2020, 2, 12, 0, 0), 12), (datetime.datetime(2020, 2, 13, 0, 0), 13),
        (datetime.datetime(2020, 2, 14, 0, 0), 13), (datetime.datetime(2020, 2, 15, 0, 0), 13),
        (datetime.datetime(2020, 2, 16, 0, 0), 13), (datetime.datetime(2020, 2, 17, 0, 0), 13),
        (datetime.datetime(2020, 2, 18, 0, 0), 13), (datetime.datetime(2020, 2, 19, 0, 0), 13),
        (datetime.datetime(2020, 2, 20, 0, 0), 13), (datetime.datetime(2020, 2, 21, 0, 0), 15),
        (datetime.datetime(2020, 2, 22, 0, 0), 15), (datetime.datetime(2020, 2, 23, 0, 0), 15),
        (datetime.datetime(2020, 2, 24, 0, 0), 15), (datetime.datetime(2020, 2, 25, 0, 0), 15),
        (datetime.datetime(2020, 2, 26, 0, 0), 15), (datetime.datetime(2020, 2, 27, 0, 0), 16),
        (datetime.datetime(2020, 2, 28, 0, 0), 16), (datetime.datetime(2020, 2, 29, 0, 0), 24),
        (datetime.datetime(2020, 3, 1, 0, 0), 30), (datetime.datetime(2020, 3, 2, 0, 0), 53),
        (datetime.datetime(2020, 3, 3, 0, 0), 73), (datetime.datetime(2020, 3, 4, 0, 0), 104),
        (datetime.datetime(2020, 3, 5, 0, 0), 174), (datetime.datetime(2020, 3, 6, 0, 0), 222),
        (datetime.datetime(2020, 3, 7, 0, 0), 337), (datetime.datetime(2020, 3, 8, 0, 0), 451),
        (datetime.datetime(2020, 3, 9, 0, 0), 519), (datetime.datetime(2020, 3, 10, 0, 0), 711),
        (datetime.datetime(2020, 3, 11, 0, 0), 1109), (datetime.datetime(2020, 3, 12, 0, 0), 1561),
        (datetime.datetime(2020, 3, 13, 0, 0), 2157), (datetime.datetime(2020, 3, 14, 0, 0), 2870),
        (datetime.datetime(2020, 3, 15, 0, 0), 2968), (datetime.datetime(2020, 3, 16, 0, 0), 4360),
        (datetime.datetime(2020, 3, 17, 0, 0), 6141), (datetime.datetime(2020, 3, 18, 0, 0), 8914),
        (datetime.datetime(2020, 3, 19, 0, 0), 14153), (datetime.datetime(2020, 3, 20, 0, 0), 19479),
        (datetime.datetime(2020, 3, 21, 0, 0), 25818), (datetime.datetime(2020, 3, 22, 0, 0), 33756),
        (datetime.datetime(2020, 3, 23, 0, 0), 43845), (datetime.datetime(2020, 3, 24, 0, 0), 54108),
        (datetime.datetime(2020, 3, 25, 0, 0), 66044), (datetime.datetime(2020, 3, 26, 0, 0), 84080),
        (datetime.datetime(2020, 3, 27, 0, 0), 102254), (datetime.datetime(2020, 3, 28, 0, 0), 122054),
        (datetime.datetime(2020, 3, 29, 0, 0), 141194), (datetime.datetime(2020, 3, 30, 0, 0), 162690),
        (datetime.datetime(2020, 3, 31, 0, 0), 188701), (datetime.datetime(2020, 4, 1, 0, 0), 214194),
        (datetime.datetime(2020, 4, 2, 0, 0), 244593), (datetime.datetime(2020, 4, 3, 0, 0), 276535),
        (datetime.datetime(2020, 4, 4, 0, 0), 309699), (datetime.datetime(2020, 4, 5, 0, 0), 337573),
        (datetime.datetime(2020, 4, 6, 0, 0), 367210), (datetime.datetime(2020, 4, 7, 0, 0), 397992),
        (datetime.datetime(2020, 4, 8, 0, 0), 429686), (datetime.datetime(2020, 4, 9, 0, 0), 464442),
        (datetime.datetime(2020, 4, 10, 0, 0), 497943), (datetime.datetime(2020, 4, 11, 0, 0), 527958),
        (datetime.datetime(2020, 4, 12, 0, 0), 556517), (datetime.datetime(2020, 4, 13, 0, 0), 581810),
        (datetime.datetime(2020, 4, 14, 0, 0), 608845), (datetime.datetime(2020, 4, 15, 0, 0), 637974),
        (datetime.datetime(2020, 4, 16, 0, 0), 669272), (datetime.datetime(2020, 4, 17, 0, 0), 701996),
        (datetime.datetime(2020, 4, 18, 0, 0), 730317), (datetime.datetime(2020, 4, 19, 0, 0), 756375),
        (datetime.datetime(2020, 4, 20, 0, 0), 783716), (datetime.datetime(2020, 4, 21, 0, 0), 809213),
        (datetime.datetime(2020, 4, 22, 0, 0), 837414), (datetime.datetime(2020, 4, 23, 0, 0), 871617),
        (datetime.datetime(2020, 4, 24, 0, 0), 907908), (datetime.datetime(2020, 4, 25, 0, 0), 940829),
        (datetime.datetime(2020, 4, 26, 0, 0), 968517), (datetime.datetime(2020, 4, 27, 0, 0), 990993),
        (datetime.datetime(2020, 4, 28, 0, 0), 1015518), (datetime.datetime(2020, 4, 29, 0, 0), 1042926),
        (datetime.datetime(2020, 4, 30, 0, 0), 1072667)]

def calendar_custom_cell():
    calendar = Calendar(init_opts=opts.InitOpts(theme='light',
                                                width='1000px',
                                                height='600px'))
    calendar.add('确证人数',
                 yaxis_data=data,
                 label_opts=opts.LabelOpts(is_show=True),
                 calendar_opts=opts.CalendarOpts(
                     # 日历位置
                     pos_top='10%',
                     pos_left='10%',
                     # 日期范围
                     range_=['2020-01-21', '2020-04-30'],
                     # 日历单元格尺寸
                     cell_size=50,
                     # 年月日标签样式设置
                     yearlabel_opts=opts.CalendarYearLabelOpts(margin=40,
                                                               label_font_size=20,
                                                               label_color='rgba(130,134,112,0.8)'),
                     daylabel_opts=opts.CalendarDayLabelOpts(label_color='#778633', label_font_weight='bold'),
                     monthlabel_opts=opts.CalendarMonthLabelOpts(label_color='#778633', label_font_weight='bold')
                 )
                 )
    # 设置视觉组件
    calendar.set_global_opts(visualmap_opts=opts.VisualMapOpts(
        max_=1000000,
        is_piecewise=True,
        pieces=[{"min": 1000000},
                {"min": 10000, "max": 1000000},
                {"min": 100, "max": 10000},
                {"max": 100}],
        range_color=["#CCD3D9", "#E6B6C2", "#D4587A", "#DC364C"]
    ))
    return calendar

chart = calendar_custom_cell()
chart.render_notebook()
```

### 代码单元 34

```
from pyecharts.charts import *
from pyecharts import options as opts
import datetime

# 美国covid确诊数据
data = [(datetime.datetime(2020, 1, 21, 0, 0), 1), (datetime.datetime(2020, 1, 22, 0, 0), 1),
        (datetime.datetime(2020, 1, 23, 0, 0), 1), (datetime.datetime(2020, 1, 24, 0, 0), 2),
        (datetime.datetime(2020, 1, 25, 0, 0), 2), (datetime.datetime(2020, 1, 26, 0, 0), 5),
        (datetime.datetime(2020, 1, 27, 0, 0), 5), (datetime.datetime(2020, 1, 28, 0, 0), 5),
        (datetime.datetime(2020, 1, 29, 0, 0), 5), (datetime.datetime(2020, 1, 30, 0, 0), 5),
        (datetime.datetime(2020, 1, 31, 0, 0), 7), (datetime.datetime(2020, 2, 1, 0, 0), 8),
        (datetime.datetime(2020, 2, 2, 0, 0), 8), (datetime.datetime(2020, 2, 3, 0, 0), 11),
        (datetime.datetime(2020, 2, 4, 0, 0), 11), (datetime.datetime(2020, 2, 5, 0, 0), 11),
        (datetime.datetime(2020, 2, 6, 0, 0), 11), (datetime.datetime(2020, 2, 7, 0, 0), 11),
        (datetime.datetime(2020, 2, 8, 0, 0), 11), (datetime.datetime(2020, 2, 9, 0, 0), 11),
        (datetime.datetime(2020, 2, 10, 0, 0), 11), (datetime.datetime(2020, 2, 11, 0, 0), 12),
        (datetime.datetime(2020, 2, 12, 0, 0), 12), (datetime.datetime(2020, 2, 13, 0, 0), 13),
        (datetime.datetime(2020, 2, 14, 0, 0), 13), (datetime.datetime(2020, 2, 15, 0, 0), 13),
        (datetime.datetime(2020, 2, 16, 0, 0), 13), (datetime.datetime(2020, 2, 17, 0, 0), 13),
        (datetime.datetime(2020, 2, 18, 0, 0), 13), (datetime.datetime(2020, 2, 19, 0, 0), 13),
        (datetime.datetime(2020, 2, 20, 0, 0), 13), (datetime.datetime(2020, 2, 21, 0, 0), 15),
        (datetime.datetime(2020, 2, 22, 0, 0), 15), (datetime.datetime(2020, 2, 23, 0, 0), 15),
        (datetime.datetime(2020, 2, 24, 0, 0), 15), (datetime.datetime(2020, 2, 25, 0, 0), 15),
        (datetime.datetime(2020, 2, 26, 0, 0), 15), (datetime.datetime(2020, 2, 27, 0, 0), 16),
        (datetime.datetime(2020, 2, 28, 0, 0), 16), (datetime.datetime(2020, 2, 29, 0, 0), 24),
        (datetime.datetime(2020, 3, 1, 0, 0), 30), (datetime.datetime(2020, 3, 2, 0, 0), 53),
        (datetime.datetime(2020, 3, 3, 0, 0), 73), (datetime.datetime(2020, 3, 4, 0, 0), 104),
        (datetime.datetime(2020, 3, 5, 0, 0), 174), (datetime.datetime(2020, 3, 6, 0, 0), 222),
        (datetime.datetime(2020, 3, 7, 0, 0), 337), (datetime.datetime(2020, 3, 8, 0, 0), 451),
        (datetime.datetime(2020, 3, 9, 0, 0), 519), (datetime.datetime(2020, 3, 10, 0, 0), 711),
        (datetime.datetime(2020, 3, 11, 0, 0), 1109), (datetime.datetime(2020, 3, 12, 0, 0), 1561),
        (datetime.datetime(2020, 3, 13, 0, 0), 2157), (datetime.datetime(2020, 3, 14, 0, 0), 2870),
        (datetime.datetime(2020, 3, 15, 0, 0), 2968), (datetime.datetime(2020, 3, 16, 0, 0), 4360),
        (datetime.datetime(2020, 3, 17, 0, 0), 6141), (datetime.datetime(2020, 3, 18, 0, 0), 8914),
        (datetime.datetime(2020, 3, 19, 0, 0), 14153), (datetime.datetime(2020, 3, 20, 0, 0), 19479),
        (datetime.datetime(2020, 3, 21, 0, 0), 25818), (datetime.datetime(2020, 3, 22, 0, 0), 33756),
        (datetime.datetime(2020, 3, 23, 0, 0), 43845), (datetime.datetime(2020, 3, 24, 0, 0), 54108),
        (datetime.datetime(2020, 3, 25, 0, 0), 66044), (datetime.datetime(2020, 3, 26, 0, 0), 84080),
        (datetime.datetime(2020, 3, 27, 0, 0), 102254), (datetime.datetime(2020, 3, 28, 0, 0), 122054),
        (datetime.datetime(2020, 3, 29, 0, 0), 141194), (datetime.datetime(2020, 3, 30, 0, 0), 162690),
        (datetime.datetime(2020, 3, 31, 0, 0), 188701), (datetime.datetime(2020, 4, 1, 0, 0), 214194),
        (datetime.datetime(2020, 4, 2, 0, 0), 244593), (datetime.datetime(2020, 4, 3, 0, 0), 276535),
        (datetime.datetime(2020, 4, 4, 0, 0), 309699), (datetime.datetime(2020, 4, 5, 0, 0), 337573),
        (datetime.datetime(2020, 4, 6, 0, 0), 367210), (datetime.datetime(2020, 4, 7, 0, 0), 397992),
        (datetime.datetime(2020, 4, 8, 0, 0), 429686), (datetime.datetime(2020, 4, 9, 0, 0), 464442),
        (datetime.datetime(2020, 4, 10, 0, 0), 497943), (datetime.datetime(2020, 4, 11, 0, 0), 527958),
        (datetime.datetime(2020, 4, 12, 0, 0), 556517), (datetime.datetime(2020, 4, 13, 0, 0), 581810),
        (datetime.datetime(2020, 4, 14, 0, 0), 608845), (datetime.datetime(2020, 4, 15, 0, 0), 637974),
        (datetime.datetime(2020, 4, 16, 0, 0), 669272), (datetime.datetime(2020, 4, 17, 0, 0), 701996),
        (datetime.datetime(2020, 4, 18, 0, 0), 730317), (datetime.datetime(2020, 4, 19, 0, 0), 756375),
        (datetime.datetime(2020, 4, 20, 0, 0), 783716), (datetime.datetime(2020, 4, 21, 0, 0), 809213),
        (datetime.datetime(2020, 4, 22, 0, 0), 837414), (datetime.datetime(2020, 4, 23, 0, 0), 871617),
        (datetime.datetime(2020, 4, 24, 0, 0), 907908), (datetime.datetime(2020, 4, 25, 0, 0), 940829),
        (datetime.datetime(2020, 4, 26, 0, 0), 968517), (datetime.datetime(2020, 4, 27, 0, 0), 990993),
        (datetime.datetime(2020, 4, 28, 0, 0), 1015518), (datetime.datetime(2020, 4, 29, 0, 0), 1042926),
        (datetime.datetime(2020, 4, 30, 0, 0), 1072667)]

def calendar_in_Chinese():
    calendar = Calendar(init_opts=opts.InitOpts(theme='light',
                                                width='1000px',
                                                height='600px'))
    calendar.add('确诊人数',
                 yaxis_data=data,
                 label_opts=opts.LabelOpts(is_show=True),
                 calendar_opts=opts.CalendarOpts(
                     # 日期范围
                     range_=['2020-01-21', '2020-04-30'],
                     # 日历单元格尺寸
                     cell_size=50,
                     # 年月日标签样式设置
                     # 星期和月份设置为中文显示，默认是英文
                     yearlabel_opts=opts.CalendarYearLabelOpts(margin=50),
                     daylabel_opts=opts.CalendarDayLabelOpts(name_map='cn'),
                     monthlabel_opts=opts.CalendarMonthLabelOpts(name_map='cn')
                 )
                 )
    # 设置视觉组件
    calendar.set_global_opts(visualmap_opts=opts.VisualMapOpts(
        max_=1000000,
        is_piecewise=True,
        pieces=[{"min": 1000000},
                {"min": 10000, "max": 1000000},
                {"min": 100, "max": 10000},
                {"max": 100}],
        range_color=["#CCD3D9", "#E6B6C2", "#D4587A", "#DC364C"]
    ))
    return calendar

chart = calendar_in_Chinese()
chart.render_notebook()
```

### 代码单元 35

```
from pyecharts.charts import *
from pyecharts import options as opts

def geo_add_custom_coordinate():
    geo = Geo(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))
    # 添加自定义坐标点
    geo.add_coordinate('x', 116.397428, 39.90923)
    geo.add_coordinate('y', 112.398615, 29.91659)

    geo.add_schema(maptype="china")
    geo.add("", [('x', 1), ('y', 2)])

    return geo

chart = geo_add_custom_coordinate()
chart.render_notebook()
```

### 代码单元 36

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.datasets import register_url
import ssl

def geo_foreign_country():
    # 添加其他国家的地图
    # noinspection PyBroadException
    try:
        register_url("https://echarts-maps.github.io/echarts-countries-js/")
    except Exception:
        ssl._create_default_https_context = ssl._create_unverified_context
        register_url("https://echarts-maps.github.io/echarts-countries-js/")

    geo = Geo(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))

    geo.add_schema(maptype="美国")

    return geo

chart = geo_foreign_country()
chart.render_notebook()
```

### 代码单元 37

```
from pyecharts.charts import *
from pyecharts import options as opts

def geo_effect_scatter():
    geo = Geo(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))

    geo.add_schema(maptype="china")

    geo.add("",
            [("广州", 150), ("北京", 70), ("长沙", 64), ("上海", 74),  ("厦门", 63)],
            # 涟漪效果散点图
            type_='effectScatter')

    return geo

chart = geo_effect_scatter()
chart.render_notebook()
```

### 代码单元 38

```
from pyecharts.charts import *
from pyecharts import options as opts

def geo_heatmap():
    geo = Geo(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))

    geo.add_schema(maptype="china")

    geo.add("",
            [("广州", 150), ("北京", 70), ("深圳", 64), ("上海", 74),  ("杭州", 63)],
            type_='heatmap')
    # 热点图必须配置visualmap_opts
    geo.set_global_opts(visualmap_opts=opts.VisualMapOpts())
    return geo

chart = geo_heatmap()
chart.render_notebook()
```

### 代码单元 39

```
from pyecharts.charts import *
from pyecharts import options as opts

def geo_lines():
    geo = Geo(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))

    geo.add_schema(maptype="china")

    geo.add("广州出发",
            # 数据格式（from， to）
            [("广州", "上海"), ("广州", "北京"), ("广州", "西宁"), ("广州", "重庆")],
            type_='lines')
    geo.add("成都出发",
            # 数据格式（from， to）
            [("成都", '长沙'), ("成都", "武汉"), ("成都", "长春"), ("成都", "南京")],
            type_='lines')

    return geo

chart = geo_lines()
chart.render_notebook()
```

### 代码单元 40

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker

def pie_custom_radius():
    pie = Pie(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))
    pie.add("",
            [list(z) for z in zip(Faker.choose(), Faker.values())],
            # 设置半径范围，0%-100%
            radius=["40%", "75%"])

    return pie

chart = pie_custom_radius()
chart.render_notebook()
```

### 代码单元 41

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker

def pie_with_custom_label():
    pie = Pie(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='600px'))
    pie.add("", [list(z) for z in zip(Faker.choose(), Faker.values())])
    pie.set_series_opts(
        # 自定义数据标签
        label_opts=opts.LabelOpts(position='top',
                                  color='red',
                                  font_family='Arial',
                                  font_size=12,
                                  font_style='italic',
                                  interval=1,
                                  formatter='{b}:{d}%'
                                  )
    )

    return pie

chart = pie_with_custom_label()
chart.render_notebook()
```

### 代码单元 42

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker

def pie_multiple():
    pie = Pie(init_opts=opts.InitOpts(theme='light',
                                      width='1000px',
                                      height='800px'))
    pie.add("",
            [list(z) for z in zip(Faker.choose(), Faker.values())],
            radius=["20%", "50%"],
            center=["25%", "50%"])
    # 添加多个饼图
    pie.add("",
            [list(z) for z in zip(Faker.choose(), Faker.values())],
            radius=["20%", "50%"],
            center=["75%", "50%"])

    return pie

chart = pie_multiple()
chart.render_notebook()
```

### 代码单元 43

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker

def scatter_with_visualmap_size():
    scatter = Scatter(init_opts=opts.InitOpts(theme='light',
                                              width='1000px',
                                              height='600px'))
    scatter.add_xaxis(Faker.choose())
    scatter.add_yaxis('', Faker.values())
    # 设置视觉组件
    scatter.set_global_opts(visualmap_opts=opts.VisualMapOpts(type_='size'))
    return scatter

chart = scatter_with_visualmap_size()
chart.render_notebook()
```

### 代码单元 44

```
from pyecharts.charts import *
from pyecharts import options as opts
import random

x_data = [random.randint(0, 100) for _ in range(30)]
y_data = [(random.randint(0, 100), random.randint(0, 100), random.randint(0, 100)) for _ in range(30)]

def scatter_with_visualmap_color_size():
    scatter = Scatter(init_opts=opts.InitOpts(theme='light',
                                              width='1000px',
                                              height='600px'))
    scatter.add_xaxis(x_data)
    scatter.add_yaxis('', y_data)
    # 多个映射维度通过list形式传入
    # dimension指定数据维度
    scatter.set_global_opts(visualmap_opts=[opts.VisualMapOpts(is_show=True, type_='size', dimension=2, pos_top='20%'),
                                            opts.VisualMapOpts(is_show=True, type_='color', dimension=3,  pos_top='60%')
                                            ],
                            xaxis_opts=opts.AxisOpts(type_="value"))
    return scatter

chart = scatter_with_visualmap_color_size()
chart.render_notebook()
```

### 代码单元 45

```
from pyecharts.charts import *
from pyecharts import options as opts
import random

x_data = [random.randint(0, 100) for _ in range(30)]
y_data = [(random.randint(0, 100), random.randint(0, 100), random.randint(0, 100), random.randint(0, 100))
          for _ in range(30)]

def scatter_with_visualmap_color_size_opacity():
    scatter = Scatter(init_opts=opts.InitOpts(theme='light',
                                              width='1000px',
                                              height='600px'))
    scatter.add_xaxis(x_data)
    scatter.add_yaxis('', y_data)
    # 多个映射维度通过list形式传入
    # dimension制定数据维度
    scatter.set_global_opts(visualmap_opts=[opts.VisualMapOpts(is_show=True, type_='size', dimension=2, pos_top='10%'),
                                            opts.VisualMapOpts(is_show=True, type_='color', dimension=3, pos_top='40%'),
                                            opts.VisualMapOpts(is_show=True, type_='opacity', dimension=4,
                                                               # VisualMapOpt中对于range_opacity没给默认值，需要自行设定
                                                               range_opacity=[0.2, 1], pos_top='70%')],
                            xaxis_opts=opts.AxisOpts(type_="value"))
    return scatter

chart = scatter_with_visualmap_color_size_opacity()
chart.render_notebook()
```

### 代码单元 46

```
from pyecharts.charts import *
from pyecharts import options as opts
import random

x_data = [random.randint(0, 100) for _ in range(30)]
y_data = [(random.randint(0, 100), random.randint(0, 100), random.randint(0, 100)) for _ in range(30)]

def scatter_with_custom_bgColor():
    scatter = Scatter(
        init_opts=opts.InitOpts(theme='light',
                                width='1000px',
                                height='600px',
                                # 自定义背景颜色
                                bg_color='#008B8B'))
    scatter.add_xaxis(x_data)
    scatter.add_yaxis('', y_data)
    # 多个映射维度通过list形式传入
    # dimension制定数据维度
    scatter.set_global_opts(visualmap_opts=[opts.VisualMapOpts(is_show=True, type_='size', dimension=2),
                                            opts.VisualMapOpts(is_show=True, type_='color', dimension=3)],
                            xaxis_opts=opts.AxisOpts(type_="value"))
    return scatter

chart = scatter_with_custom_bgColor()
chart.render_notebook()
```

### 代码单元 47

```
from pyecharts.charts import *
from pyecharts import options as opts
import random

text = """
I used to rule the world
Seas would rise when I gave the word
Now in the morning I sleep alone
Sweep the streets I used to own
I used to roll the dice
Feel the fear in my enemy eyes
Listen as the crowd would sing
Now the old king is dead
Long live the king
One minute I held the key
Next the walls were closed on me
And I discovered that my castles stand
Upon pillars of salt and pillars of sand
I hear Jerusalem bells are ringing
Roman Cavalry choirs are singing
Be my mirror my sword and shield
My missionaries in a foreign field
For some reason I can't explain
Once you go there was never
Never an honest word
That was when I ruled the world
"""

word_list = set(text.split(' '))

words = [(word, random.randint(1, 100)) for word in word_list]

def wordcloud_custom_word_size():
    wordcloud = WordCloud(init_opts=opts.InitOpts(theme='light',
                                                  width='1000px',
                                                  height='600px'))
    wordcloud.add('',
                  words,
                  # 设置字体大小范围
                  word_size_range=[10, 50])

    return wordcloud

chart = wordcloud_custom_word_size()
chart.render_notebook()
```

### 代码单元 48

```
from pyecharts.charts import *
from pyecharts import options as opts

data = [('广东', 10430),
        ('山东', 9579),
        ('河南', 9402),
        ('四川', 8041),
        ('江苏', 7866),
        ('河北', 7185),
        ('湖南', 6568),
        ('安徽', 5950),
        ('湖北', 5724),
        ('浙江', 5442),
        ('广西', 4603),
        ('云南', 4597),
        ('江西', 4457),
        ('辽宁', 4375),
        ('黑龙江', 3831),
        ('陕西', 3733),
        ('山西', 3571),
        ('福建', 3552),
        ('贵州', 3477),
        ('重庆', 2884),
        ('吉林', 2746),
        ('甘肃省', 2557),
        ('内蒙古', 2471),
        ('台湾', 2316),
        ('上海', 2301),
        ('新疆', 2181),
        ('北京', 1961),
        ('天津', 1294),
        ('海南', 867),
        ('香港', 710),
        ('宁夏', 630),
        ('青海', 562),
        ('西藏', 300),
        ('澳门', 55)]

def map_with_viusalmap():
    map_chart = Map(init_opts=opts.InitOpts(theme='light',
                                            width='1000px',
                                            height='600px'))
    map_chart.add('人口（万人）',
                  data_pair=data,
                  maptype='china',
                  # 关闭symbol的显示
                  is_map_symbol_show=False)

    map_chart.set_global_opts(visualmap_opts=opts.VisualMapOpts(
        max_=10430,  # visualmap默认映射数据范围是【0，100】，需调整
        is_piecewise=True,
        range_color=["#CCD3D9", "#E6B6C2", "#D4587A", "#DC364C"]
    ))
    return map_chart

chart = map_with_viusalmap()
chart.render_notebook()
```

### 代码单元 49

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker

def page_simple_layout():
    # 图表1
    bar_1 = Bar(init_opts=opts.InitOpts(theme='light',
                                        width='500px',
                                        height='300px'))
    bar_1.add_xaxis(Faker.choose())
    bar_1.add_yaxis('A', Faker.values())
    bar_1.add_yaxis('B', Faker.values())

    # 图表2
    bar_2 = Bar(init_opts=opts.InitOpts(theme='light',
                                        width='500px',
                                        height='300px'))
    bar_2.add_xaxis(Faker.choose())
    bar_2.add_yaxis('A', Faker.values())
    # x,y轴翻转
    bar_2.reversal_axis()

    # 图表3
    line = Line(init_opts=opts.InitOpts(theme='light',
                                        width='500px',
                                        height='300px'))
    line.add_xaxis(Faker.choose())
    line.add_yaxis('A', Faker.values())
    line.add_yaxis('B', Faker.values())

    # 图表4
    pie = Pie(init_opts=opts.InitOpts(theme='light',
                                      width='500px',
                                      height='300px'))
    pie.add("",
            [list(z) for z in zip(Faker.choose(), Faker.values())],
            radius=["40%", "75%"])

    page = Page(layout=Page.SimplePageLayout)
    # 需要自行调整每个 chart 的 height/width，布局会因为页面大小而不同
    page.add(bar_1, bar_2, line, pie)

    return page

chart = page_simple_layout()
chart.render_notebook()
```

### 代码单元 50

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker

def tab_with_multiple_chart():
    # 图表1
    bar = Bar()
    bar.add_xaxis(Faker.choose())
    bar.add_yaxis("商家A", Faker.values())
    bar.add_yaxis("商家B", Faker.values())

    # 图表2
    line = Line()
    line.add_xaxis(Faker.choose())
    line.add_yaxis("商家A", Faker.values())
    line.add_yaxis("商家B", Faker.values())

    # 先通过Grid将图表1和图表2组合起来
    grid = Grid()
    grid.add(bar, grid_opts=opts.GridOpts(pos_bottom="60%"))
    grid.add(line, grid_opts=opts.GridOpts(pos_top="60%"))

    # 再将Grid添加到Tab
    tab = Tab()
    tab.add(grid, '示例')

    return tab

chart = tab_with_multiple_chart()
chart.render_notebook()
```

### 代码单元 51

```
from pyecharts.charts import *
from pyecharts import options as opts
from pyecharts.faker import Faker

def timeline_auto_play():
    timeline = Timeline(init_opts=opts.InitOpts(theme='light',
                                                width='1000px',
                                                height='600px'))
    timeline.add_schema(is_auto_play=True,  # 自动播放
                        is_loop_play=True  # 循环播放
                        )
    for year in range(2000, 2020):
        bar = Bar()
        bar.add_xaxis(['香蕉', '梨子', '水蜜桃', '核桃', '西瓜', '苹果', '菠萝'])
        bar.add_yaxis('A', Faker.values())
        bar.add_yaxis('B', Faker.values())
        timeline.add(bar, '{}年'.format(year))
    return timeline

chart = timeline_auto_play()
chart.render_notebook()
```

