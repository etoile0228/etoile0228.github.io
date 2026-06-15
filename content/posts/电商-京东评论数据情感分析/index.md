---
title: "电商-京东评论数据情感分析"
date: 2026-06-15T19:07:29+08:00
# weight: 1
# aliases: ["/first"]
categories: ["电商"]
tags: ["评论","情感"]
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
- 技术关键词：NLP, jieba, 情感分析, 词云
- 项目简介：评论文本是电商平台最直接的用户反馈。相比只看评分，文本分析能定位用户满意和不满的具体原因，帮助商品运营、客服和供应链优化。

## 学习目标

- 练习从业务背景出发提出可分析的问题，而不是只运行代码。
- 熟悉 中文分词、停用词处理、关键词提取、情感倾向分析、词云可视化。
- 通过图表、指标和模型结果总结业务现象，并形成自己的理解。
- 将 notebook、图表和代码整理成可复盘、可展示的作品。

## 数据与方法

- 数据概况：京东商品评论数据，包含评论文本和相关评价信息。
- 技术路线：中文分词、停用词处理、关键词提取、情感倾向分析、词云可视化。

## 分析过程与思路

- 先明确文本分析目标：是识别用户关注点、判断情绪倾向，还是提取岗位/产品关键词。
- 对文本做清洗、分词和停用词过滤，减少无意义词对结果的干扰。
- 通过词频、关键词、词云或情感模型提炼主要信息。
- 结合业务场景解释文本结果，避免只停留在高频词罗列。
- 把文本洞察沉淀成标签、问题清单或运营建议。

## 核心发现

- 高频词可以快速呈现用户关注点，例如价格、物流、包装、质量和售后。
- 负面评论词云更适合用于问题发现，因为它能聚焦影响购买决策的痛点。
- 情感分析要结合业务语境，部分词在不同品类中含义不同，不能只依赖通用词典。

## 我的业务理解

这个项目的重点不是单纯把数据做成图，而是借助数据理解一个具体场景。整理文章时，我把代码执行过程、图表输出和业务解释放在同一篇文章里，方便以后回看自己当时的分析路径，也能作为个人数据分析作品集的一部分展示。

## 业务建议

- 运营侧应把负面关键词沉淀为问题标签，并追踪问题出现频率的变化。
- 商品详情页可强化正向高频卖点，客服和供应链则优先处理负向高频问题。
- 后续可使用监督学习或大模型做方面级情感分析，细分到物流、价格、质量和服务。

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
import pandas as pd
data = pd.read_csv('./京东评论数据.csv')
data.head(2)
```

**文本输出**

```text
sku_id                                   _id item_name   comment_id  \
0  7534113  03b51aa9-2b5e-41c3-a40b-343164a1d23a   comment  11801751173   
1  7534113  03b51aa9-2b5e-41c3-a40b-343164a1d23a   comment  11525358140   

                                             content        creation_time  \
0                                 还可以刷脸解锁，帮朋友买的，她很满意  2018-08-13 12:24:59   
1  第一次买vivo，真心不错，1498的机子，没想到照相很清晰，性价比很高，买值了，还送了小音...  2018-05-27 17:49:17   

   reply_count  score  useful_vote_count  useless_vote_count  ...  \
0            0      5                  0                   0  ...   
1            7      5                 19                   0  ...   

   user_province  nickname user_level_name user_client  user_client_show  \
0            NaN     k***0          PLUS会员           2     来自京东iPhone客户端   
1            NaN     呢***呐          PLUS会员           4    来自京东Android客户端   

  is_mobile  days       reference_time after_days  after_user_comment  
0       1.0   4.0  2018-08-09 13:38:15        0.0          NO_MESSAGE  
1       1.0   5.0  2018-05-22 09:32:37        0.0          NO_MESSAGE  

[2 rows x 21 columns]
```

### 代码单元 2

```python
data.describe()
```

**文本输出**

```text
sku_id    comment_id  reply_count        score  \
count  3.637000e+03  3.637000e+03  3637.000000  3637.000000   
mean   7.936312e+09  1.161979e+10     6.291724     4.880946   
std    1.165137e+10  2.520618e+08    41.624571     0.591341   
min    1.592994e+06  1.045844e+10     0.000000     1.000000   
25%    5.920651e+06  1.155459e+10     0.000000     5.000000   
50%    7.651903e+06  1.174154e+10     0.000000     5.000000   
75%    2.034912e+10  1.178850e+10     1.000000     5.000000   
max    3.032369e+10  1.180889e+10  1355.000000     5.000000   

       useful_vote_count  useless_vote_count  user_level_id  user_province  \
count        3637.000000              3637.0    3637.000000            0.0   
mean           13.532307                 0.0      75.692329            NaN   
std            72.564442                 0.0      21.125683            NaN   
min             0.000000                 0.0      50.000000            NaN   
25%             0.000000                 0.0      61.000000            NaN   
50%             0.000000                 0.0      62.000000            NaN   
75%             2.000000                 0.0     105.000000            NaN   
max          2318.000
... 输出过长，博客中已截断
```

### 代码单元 3

```python
#取出sku_id','content'字段
data1 = data[['sku_id','content']]
data1.head(10)
```

**文本输出**

```text
sku_id                                            content
0  7534113                                 还可以刷脸解锁，帮朋友买的，她很满意
1  7534113  第一次买vivo，真心不错，1498的机子，没想到照相很清晰，性价比很高，买值了，还送了小音...
2  7534113                                         手机好用快递送的快。
3  8240587  手机收到。外观设计很好！美观大方。我喜欢！一直使用华为手机。从荣耀七，荣耀八，荣耀九。反正一...
4  5942439                  收到了，挺好的，声音大，电池大，好用发货速度快，非常满意，好好好。
5  5089275  本来觉得双十一还会便宜的，想不到和11月初的价格差不多，想想还是感觉入手了，早买早享受。我的...
6  7081550  没有真正意义上的窄边框，不过已经不错了，手机流畅，另外还有51G空间可用，同时试了下近距拍摄...
7  5663902                       幻夜黑颜色很漂亮，2.5D屏幕，圆润。2K屏很清晰，惊艳
8  7283905  特地用了一段时间才来评价，这手机值得这个价钱，打游戏还行，就是电池很不耐用，摄像头也很突出，...
9  5001213  机器没得说，价格也合理，虽说仍有不足，但还是比较满意的，首发就抢到了，暂时发现的不足就是扬声...
```

### 代码单元 4

```python
#安装snownlp包
```

**文本输出**

```text
Looking in indexes: https://pypi.tuna.tsinghua.edu.cn/simple
Collecting snownlp
  Downloading https://pypi.tuna.tsinghua.edu.cn/packages/3d/b3/37567686662100d3bce62d3b0f2adec18ab4b9ff2b61abd7a61c39343c1d/snownlp-0.12.3.tar.gz (37.6 MB)
     ---------------------------------------- 37.6/37.6 MB 3.1 MB/s eta 0:00:00
  Preparing metadata (setup.py): started
  Preparing metadata (setup.py): finished with status 'done'
Building wheels for collected packages: snownlp
  Building wheel for snownlp (setup.py): started
  Building wheel for snownlp (setup.py): finished with status 'done'
  Created wheel for snownlp: filename=snownlp-0.12.3-py3-none-any.whl size=37760953 sha256=400f03511ccda3443b1a0c80aa51754ac9840c0a2e37c47eadb04472268b8d67
  Stored in directory: c:\users\administrator\appdata\local\pip\cache\wheels\e3\39\48\6bf6f2fdb44ab1aeb2bbbc27b79941ff05d39d181fdaad0fb5
Successfully built snownlp
Installing collected packages: snownlp
Successfully installed snownlp-0.12.3
[notice] A new release of pip available: 22.3.1 -> 23.0
[notice] To update, run: python.exe -m pip install --upgrade pip
```

### 代码单元 5

```python
from snownlp import SnowNLP
data1['emotion'] = data1['content'].apply(lambda x:SnowNLP(x).sentiments)
data1.head(10)
```

**文本输出**

```text
C:\Users\Administrator\AppData\Local\Temp\2\ipykernel_14348\3076741958.py:2: SettingWithCopyWarning: 
A value is trying to be set on a copy of a slice from a DataFrame.
Try using .loc[row_indexer,col_indexer] = value instead

See the caveats in the documentation: https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#returning-a-view-versus-a-copy
  data1['emotion'] = data1['content'].apply(lambda x:SnowNLP(x).sentiments)
sku_id                                            content   emotion
0  7534113                                 还可以刷脸解锁，帮朋友买的，她很满意  0.470635
1  7534113  第一次买vivo，真心不错，1498的机子，没想到照相很清晰，性价比很高，买值了，还送了小音...  0.999999
2  7534113                                         手机好用快递送的快。  0.561609
3  8240587  手机收到。外观设计很好！美观大方。我喜欢！一直使用华为手机。从荣耀七，荣耀八，荣耀九。反正一...  0.868183
4  5942439                  收到了，挺好的，声音大，电池大，好用发货速度快，非常满意，好好好。  0.983088
5  5089275  本来觉得双十一还会便宜的，想不到和11月初的价格差不多，想想还是感觉入手了，早买早享受。我的...  0.984574
6  7081550  没有真正意义上的窄边框，不过已经不错了，手机流畅，另外还有51G空间可用，同时试了下近距拍摄...  0.956682
7  5663902                       幻夜黑颜色很漂亮，2.5D屏幕，圆润。2K屏很清晰，惊艳  0.999839
8  7283905  特地用了一段时间才来评价，这手机值得这个价钱，打游戏还行，就是电池很不耐用，摄像头也很突出，...  0.996540
9  5001213  机器没得说，价格也合理，虽说仍有不足，但还是比较满意的，首发就
... 输出过长，博客中已截断
```

### 代码单元 6

```python
data1.describe()
```

**文本输出**

```text
sku_id      emotion
count  3.637000e+03  3637.000000
mean   7.936312e+09     0.746161
std    1.165137e+10     0.354481
min    1.592994e+06     0.000000
25%    5.920651e+06     0.562240
50%    7.651903e+06     0.962449
75%    2.034912e+10     0.999123
max    3.032369e+10     1.000000
```

### 代码单元 7

```python
#情感分直方图
import matplotlib.pyplot as plt
import numpy as np

plt.rcParams['font.sans-serif']=['SimHei']
plt.rcParams['axes.unicode_minus'] = False

bins=np.arange(0,1.1,0.1)
plt.hist(data1['emotion'],bins,color='#4F94CD',alpha=0.9)
plt.xlim(0,1)
plt.xlabel('情感分')
plt.ylabel('数量')
plt.title('情感分直方图')

plt.show()
```

**图表输出 1**

![图表输出 16-1](./images/cell-016-output-01.png)

### 代码单元 8

```python
from wordcloud import WordCloud
import jieba
w = WordCloud()
text = ''
for s in data['content']:
    text += s
data_cut = ' '.join(jieba.lcut(text))

w = WordCloud(font_path="./SimHei.ttf",
                      stopwords=['的','我','了','是','和','都','就','用'],  # 去掉停用词
                      #max_words=100,
                      width=2000,
                      height=1200).generate(data_cut)
# 保存词云
w.to_file('词云图.png')
# 显示词云文件
plt.imshow(w)
plt.axis("off")
plt.show()
```

**文本输出**

```text
Building prefix dict from the default dictionary ...
Loading model from cache C:\Users\ADMINI~1\AppData\Local\Temp\2\jieba.cache
Loading model cost 1.096 seconds.
Prefix dict has been built successfully.
```

**图表输出 1**

![图表输出 19-1](./images/cell-019-output-02.png)

### 代码单元 9

```python
#关键词top10
from jieba import analyse
key_words = jieba.analyse.extract_tags(sentence=text, topK=10, withWeight=True, allowPOS=())
key_words
```

**文本输出**

```text
[('手机', 0.20904023041744998),
 ('不错', 0.10491967558213072),
 ('京东', 0.09431019624843097),
 ('屏幕', 0.054966423247022445),
 ('华为', 0.05061411737589104),
 ('小米', 0.04731076382922812),
 ('拍照', 0.04647606302614274),
 ('非常', 0.044200923839597485),
 ('手感', 0.04270424332006433),
 ('感觉', 0.040063432512755605)]
```

### 代码单元 10

```python
#计算积极评论与消极评论各自的数目
pos = 0
neg = 0
for i in data1['emotion']:
    if i >= 0.5:
        pos += 1
    else:
        neg += 1
print('积极评论，消极评论数目分别为：',pos,neg)
```

**文本输出**

```text
积极评论，消极评论数目分别为： 2791 846
```

### 代码单元 11

```python
# 积极评论占比
import matplotlib.pyplot as plt

plt.rcParams['font.sans-serif']=['SimHei']
plt.rcParams['axes.unicode_minus'] = False

pie_labels='postive','negative'
plt.pie([pos,neg],labels=pie_labels,autopct='%1.1f%%',shadow=True)

plt.show()
```

**图表输出 1**

![图表输出 26-1](./images/cell-026-output-01.png)

### 代码单元 12

```python
#获取消极评论数据
data2=data1[data1['emotion']<0.5]
data2.head(10)
```

**文本输出**

```text
sku_id                                            content   emotion
0   7534113                                 还可以刷脸解锁，帮朋友买的，她很满意  0.470635
13  5942439                       收到货，声音很大，功能也多，适合老人用，就是重量有点重，  0.461794
17  7283905  27号下的单，今天收到1星期内，坐标河南商丘，手机是武汉仓过来的。充电头是5V2A的 不支持...  0.001627
18  5001213  今天刚收到！\n看到京东的快递包装盒，我内心是一群奔腾而过的！几千块钱的物品包装，没有防压提...  0.495955
22  5942439                         用着目前还可以，就是不知道可以用多久。希望久一些吧。  0.239150
32  5001213  第一批抢到，两天后才收到，机器没一代惊艳，边框略粗，全面屏？解决了通话，回归正常手机行列！！...  0.444317
35  8240587  总体来说，颜值非常高，很好看，虽然说是后置指纹，但是后背看起来还是挺不错的。用起来整体体验还...  0.000012
44  3901175  手机还可以，就刚开始把卡放进去的时候不显示卡，过了第二天才显示出来，耳机也没有，还有就是怎么...  0.005839
48  7534113          像素不行，反正买都买了用都用了总体来说还行吧不讨厌也不喜欢一般般，暂时没有什么问题  0.499447
51  5089275  总之还是挺好的，挺不错、虽然没有什么优惠吧，抢了个神券还不能用！！！也是用的上了第三个苹果、...  0.457264
```

### 代码单元 13

```python
#消极评论词云图
text2 = ''
for s in data2['content']:
    text2 += s
data_cut2 = ' '.join(jieba.lcut(text2))
w.generate(data_cut2)
image = w.to_file('消极评论词云.png')

# 显示词云文件
plt.imshow(w)
plt.axis("off")
plt.show()
```

**图表输出 1**

![图表输出 29-1](./images/cell-029-output-01.png)

### 代码单元 14

```python
#消极评论关键词top10
key_words = jieba.analyse.extract_tags(sentence=text2, topK=10, withWeight=True, allowPOS=())
key_words
```

**文本输出**

```text
[('手机', 0.19237764869875004),
 ('京东', 0.08930157104159077),
 ('未填写', 0.08087213276666493),
 ('评价', 0.06602737843353074),
 ('屏幕', 0.05285184715212572),
 ('快递', 0.050103021155518554),
 ('用户', 0.05005720904465942),
 ('充电', 0.04605195695403029),
 ('收到', 0.038929704221495554),
 ('没有', 0.03758001077768642)]
```

</details>
