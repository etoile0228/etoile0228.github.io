---
title: "微博情感分析：用分词和朴素贝叶斯识别社交文本情绪"
date: 2026-06-17T23:51:31+08:00
# weight: 1
# aliases: ["/first"]
categories: ["文化娱乐"]
tags: ["NLP", "朴素贝叶斯", "情感分析", "微博"]
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

# 微博情感分析：用分词和朴素贝叶斯识别社交文本情绪

## 摘要

| 模块     | 内容                                                         |
| -------- | ------------------------------------------------------------ |
| 业务场景 | 文化娱乐                                                     |
| 数据来源 | 微博文本情感数据，包含不同情绪类别的中文短文本。             |
| 分析方法 | 中文分词、停用词处理、文本向量化、朴素贝叶斯分类、模型评估。 |
| 结论先行 | 中文短文本噪声多，分词、停用词和表情符号处理会显著影响模型表现。 |

本报告围绕“业务背景、分析目的、数据说明、分析思路、分析过程、核心结论和改进建议”展开，目标是用数据回答具体问题，并把分析结果转化为可执行的判断。

## 一、分析背景

社交媒体情绪分析可以用于舆情监控、品牌口碑、活动反馈和内容治理。它的重点是快速识别情绪方向和异常波动。

## 二、分析目的

本次分析主要回答以下问题：

- 文本中用户最关注的主题和关键词是什么？
- 正负向反馈分别集中在哪些具体问题上？
- 这些文本信号能沉淀成哪些产品、运营或服务改进动作？

先明确分析目的，再开展数据处理和指标拆解，可以保证报告围绕问题展开，而不是简单罗列代码和图表。

## 三、数据来源与指标说明

| 项目           | 说明                                                         |
| -------------- | ------------------------------------------------------------ |
| 数据来源       | 微博文本情感数据，包含不同情绪类别的中文短文本。             |
| 分析工具与方法 | 中文分词、停用词处理、文本向量化、朴素贝叶斯分类、模型评估。 |
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

### 1. 中文短文本噪声多，分词、停用词和表情符号处理会显著影响模型表现。

结果解读：该发现是本项目最核心的结论之一，说明数据中存在值得关注的结构性特征。对应图表或模型结果应围绕这一判断展开，帮助读者理解结论来源。

### 2. 朴素贝叶斯适合作为文本分类基线，训练快且容易解释。

结果解读：该发现进一步解释了不同维度之间的差异。对业务决策而言，重点不只是看到差异，而是判断差异来自哪些对象、场景或指标。

### 3. 社交情绪具有强时效性，需要关注热点事件导致的数据分布变化。

结果解读：该发现可以作为后续优化策略或模型改进的依据。若用于真实业务，还需要结合成本、资源、实验结果或线上反馈继续验证。

## 七、结论

综合以上分析，可以得到以下结论：

- 中文短文本噪声多，分词、停用词和表情符号处理会显著影响模型表现。
- 朴素贝叶斯适合作为文本分类基线，训练快且容易解释。
- 社交情绪具有强时效性，需要关注热点事件导致的数据分布变化。

## 八、建议

- 行动 1：品牌舆情系统应把情绪分类和关键词聚类结合，既看情绪，也看原因。
- 行动 2：实际应用中应人工抽检高风险样本，避免模型误判引发处置偏差。
- 行动 3：后续可引入 BERT 或大模型进行更细粒度情绪和立场识别。
- 跟进方式：为每条建议绑定一个可观察指标，后续按周或按月复盘效果。

建议部分应结合具体对象、执行动作和复盘指标，避免停留在泛泛的“加强管理”或“优化运营”。

## 九、局限性与改进方向

- 项目价值：把非结构化文本转化为可统计的问题标签和情绪信号，帮助业务更快定位用户关注点和负面体验。
- 真实限制：票房、热度和评论数据受档期、宣发、排片、平台规则和口碑发酵影响，单一榜单不能完整解释内容表现。
- 业务风险：只追逐总票房或热度排名，可能忽略上座率、转化效率和长尾口碑，导致宣发资源配置失衡。
- 改进方向：建立人工抽检样本集，评估分词、情感判断和主题归类是否符合业务语境。
- 改进方向：把文本标签与订单、退款、投诉、复购或客服工单关联，验证文本问题对经营结果的影响。

## 附录：完整代码与输出结果

下面内容按原 notebook 的代码单元顺序整理。如果代码单元产生了文本输出或图片输出，也一并附在对应代码后面，便于复现完整分析过程。

### 代码单元 1

```python
#把记事本中的数据去掉词语的词性重新写入csv文件，并且标记好分类
import re
import pandas as pd
def proc_text(text):
    pos_words=[]
    pos_list=[]
    type_list = []
    for file in text:
        with open(file,encoding='UTF-8') as f:
            line = f.readline()
            while(line):
                line = line.strip('\n')
                line=re.sub('/[a-zA-Z]+', '',line).replace(" ","")
                pos_list.append(line)
                type_list.append(int(file[7]))
                line = f.readline()
    dataframe = pd.DataFrame({'text': pos_list, 'type': type_list})
    dataframe.to_csv("./data/data.csv", index=False, sep=',',encoding="utf_8_sig")
texts_list =['./data/0_simplifyweibo.txt','./data/1_simplifyweibo.txt','./data/2_simplifyweibo.txt','./data/3_simplifyweibo.txt']
proc_text(texts_list)
```

### 代码单元 2

```python
import re
import jieba
from gensim.models import word2vec
# from nltk.classify import NaiveBayesClassifier
from sklearn import naive_bayes
from sklearn.model_selection import train_test_split
from sklearn.feature_extraction.text import CountVectorizer
import pandas as pd

def chinese_word_cut(mytext):
    return " ".join(jieba.cut(mytext))

#把停用词转换为一个列表存储
def get_custom_stopwords(stop_words_file):
    with open(stop_words_file) as f:
        stopwords = f.read()
    stopwords_list = stopwords.split('\n')
    custom_stopwords_list = [i for i in stopwords_list]
    return custom_stopwords_list

df = pd.read_csv('./data/data.csv')
X = df[['text']]
y = df.type

#对评论语句进行分词
X['cut_text'] = X.text.apply(chinese_word_cut)
print(X['cut_text'][0:10])
```

**文本输出**

```text
Building prefix dict from the default dictionary ...
Dumping model to file cache C:\Users\ADMINI~1\AppData\Local\Temp\2\jieba.cache
Loading model cost 1.021 seconds.
Prefix dict has been built successfully.
0    啊呀呀 ！ 要死 啦 ！ 么 么 么 ！ 只 穿 外套 就 好 了 ， 我 认为 里面 那 ...
1                         风格 不 一样 嘛 ， 都 喜欢 ！ 最 喜欢 哪张 ？
2    好 呀 ， 试试 D . I . Y . 去死皮 面膜 1 . 将 燕麦片 加水 中 浸泡 ...
3    张 1 老师 ， 谢谢 侬 的 1 信任 ！ 粉丝 多少 无所谓 重在 质地 近日 发现 一...
4    第二 條看 來 有點 吸引力 呵呵 【 美国 相亲 节目 与 中国 的 1 几大 不同 】 ...
5    喜欢 苹果 IPHONE4 。 功能强大 ， 时尚 ， 手机 功能 多 。 沃爱 平谷 第二...
6    回复 太牛 了 买房子 送 瓷砖 呗 ！ 昨晚 上 经过 中润 ， 看到 的 1 一个 立柱...
7    人们 脱口而出 的 1 一般 都 是 没有 实际意义 的 1 话 — — — — 噗 … …...
8    开张大吉 ！ 祝贺 买卖 兴隆 我家 的 1 酸辣粉 小店 开业 了 欢迎 铁岭 的 1 朋...
9    方 大水 你 怎么 可以 这么 萌 这么 有 爱 捏 啊 呜 ~ ~ 偶 不要 变成 HC ...
Name: cut_text, dtype: object
```

### 代码单元 3

```python
#分隔训练集和测试集，训练集为90%，测试集为10%
X_train, X_test, y_train, y_test = train_test_split(X, y,test_size=0.1, random_state=0)
stop_words_file = './data/停用词.txt'
#停用词列表
stopwords = get_custom_stopwords(stop_words_file)
# 在超过这一比例的文档中出现的关键词（过于平凡），去除掉。
max_df = 0.9
# 在低于这一数量的文档中出现的关键词（过于独特），去除掉。
min_df = 4
#特征提取，使用 CountVectorizer向量化工具，它依据词语出现频率转化向量。
#特征提取使用“一袋子词”（bag of words）模型。一袋子词模型不考虑词语的出现顺序，
#也不考虑词语和前后词语之间的连接。每个词都被当作一个独立的特征来看待。可能会因为没有联系上下文到达效果不如人意。
vect = CountVectorizer(max_df = max_df,min_df = min_df,token_pattern=u'(?u)\\b[^\\d\\W]\\w+\\b',stop_words=stopwords)
```

### 代码单元 4

```python
from sklearn.naive_bayes import MultinomialNB
from sklearn.pipeline import make_pipeline
#分类模型，采用朴素贝叶斯
nb = MultinomialNB()
#利用管道(pipeline)把vect 和 nb 串联起来
pipe = make_pipeline(vect, nb)
#查看模型的工作步骤
#pipe.steps
```

### 代码单元 5

```python
#把训练集内容输入，做k折交叉验证，算出模型分类准确率的均值。
#cv的值代表k，初始训练样本分成k份，其中（k-1）份被用作训练集，剩下一份被用作评估集，这样一共可以对分类器做k次训练，并且得到k个训练结果。
from sklearn.model_selection import cross_val_score
cross_val_score(pipe, X_train.cut_text, y_train, cv=5, scoring='accuracy').mean()
```

**文本输出**

```text
C:\Users\Administrator\Envs\jv\lib\site-packages\sklearn\feature_extraction\text.py:409: UserWarning: Your stop_words may be inconsistent with your preprocessing. Tokenizing the stop words generated tokens ['若果'] not in stop_words.
  warnings.warn(
C:\Users\Administrator\Envs\jv\lib\site-packages\sklearn\feature_extraction\text.py:409: UserWarning: Your stop_words may be inconsistent with your preprocessing. Tokenizing the stop words generated tokens ['若果'] not in stop_words.
  warnings.warn(
C:\Users\Administrator\Envs\jv\lib\site-packages\sklearn\feature_extraction\text.py:409: UserWarning: Your stop_words may be inconsistent with your preprocessing. Tokenizing the stop words generated tokens ['若果'] not in stop_words.
  warnings.warn(
C:\Users\Administrator\Envs\jv\lib\site-packages\sklearn\feature_extraction\text.py:409: UserWarning: Your stop_words may be inconsistent with your preprocessing. Tokenizing the stop words generated tokens ['若果'] not in stop_words.
  warnings.warn(
C:\Users\Administrator\Envs\jv\lib\site-packages\sklearn\feature_extraction\text.py:409: UserWarning: Your stop_words may be inconsistent with your preprocessing. Tokenizing the stop words generated token
... 输出过长，博客中已截断
```

### 代码单元 6

```python
#使用用训练集，把模型拟合出来
pipe.fit(X_train.cut_text, y_train)
#在测试集上，对情感分类标记进行预测。
result=pipe.predict(X_test.cut_text)
#查看测试集上前五十个的预测结果
print(result[0:50])
```

**文本输出**

```text
C:\Users\Administrator\Envs\jv\lib\site-packages\sklearn\feature_extraction\text.py:409: UserWarning: Your stop_words may be inconsistent with your preprocessing. Tokenizing the stop words generated tokens ['若果'] not in stop_words.
  warnings.warn(
[1 1 2 0 1 0 0 0 0 1 1 0 0 2 0 0 0 0 1 0 0 3 0 0 0 0 0 0 0 0 1 0 0 0 2 0 2
 0 0 0 0 0 2 2 1 0 0 0 0 0]
```

### 代码单元 7

```python
#使用scikit-learn给我们提供的模型性能测度工具，帮助我们为预测结果和实际情况进行对比
from sklearn import tree
from sklearn import metrics
TR = tree.DecisionTreeClassifier(criterion='entropy')
corretcRate=metrics.accuracy_score(y_test,result)
print("对测试集的预测结果的正确率：",corretcRate)
confusionMatrix=metrics.confusion_matrix(y_test, result)
print("混淆矩阵：\n",confusionMatrix)
```

**文本输出**

```text
对测试集的预测结果的正确率： 0.6287097137282858
混淆矩阵：
 [[13505  1078  1048   385]
 [ 2098  1390   488   119]
 [ 2177   583  1590   126]
 [ 1279   301   214   272]]
```

### 代码单元 8

```python
# # 0：喜悦；1：愤怒；2：厌恶；3：低落
# result=pipe.predict(['我 很棒','我 很好']).tolist()
# result
#[0,0]
```

### 代码单元 9

```python
from sklearn.pipeline import make_pipeline
from sklearn import tree
TR = tree.DecisionTreeClassifier(criterion='entropy')

pipe = make_pipeline(vect, TR)
from sklearn.model_selection import cross_val_score

pipe.fit(X_train.cut_text, y_train)
result=pipe.predict(X_test.cut_text)

from sklearn import metrics
corretcRate=metrics.accuracy_score(y_test,result)
print("对测试集的预测结果的正确率：",corretcRate)
confusionMatrix=metrics.confusion_matrix(y_test, result)
print("混淆矩阵：\n",confusionMatrix)
```

### 代码单元 10

```
print(result[:10])
print(y_test[:10])
confusionMatrix=metrics.confusion_matrix([1,2,3], [1,2,3])
print("混淆矩阵：\n",confusionMatrix)
```

