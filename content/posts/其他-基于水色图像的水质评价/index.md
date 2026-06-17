---
title: "基于水色图像的水质评价：用图像特征和 SVM 做环境监测"
date: 2026-06-17T23:16:34+08:00
# weight: 1
# aliases: ["/first"]
categories: ["其他"]
tags: ["SVM", "图像特征", "环境监测", "机器学习"]
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

# 基于水色图像的水质评价：用图像特征和 SVM 做环境监测

## 摘要

| 模块     | 内容                                                         |
| -------- | ------------------------------------------------------------ |
| 业务场景 | 其他                                                         |
| 数据来源 | 水色图像及水质等级标签，包含图片样本、训练集和测试集。       |
| 分析方法 | 图像特征提取、训练测试划分、支持向量机分类、模型保存与预测。 |
| 结论先行 | 水色图像能提供直观信号，但会受到光照、拍摄角度、天气和设备差异影响。 |

本报告围绕“业务背景、分析目的、数据说明、分析思路、分析过程、核心结论和改进建议”展开，目标是用数据回答具体问题，并把分析结果转化为可执行的判断。

## 一、分析背景

水质监测通常依赖人工采样和实验室检测，成本高且频率有限。用图像辅助判断水质等级，可以作为低成本预警工具，服务河道巡检和环保监管。

## 二、分析目的

本次分析主要回答以下问题：

- 哪些变量或特征最可能影响目标结果？
- 模型能否稳定识别高风险、高价值或高需求样本？
- 模型输出应该如何转化为业务动作，而不是停留在准确率上？

先明确分析目的，再开展数据处理和指标拆解，可以保证报告围绕问题展开，而不是简单罗列代码和图表。

## 三、数据来源与指标说明

| 项目           | 说明                                                         |
| -------------- | ------------------------------------------------------------ |
| 数据来源       | 水色图像及水质等级标签，包含图片样本、训练集和测试集。       |
| 分析工具与方法 | 图像特征提取、训练测试划分、支持向量机分类、模型保存与预测。 |
| 重点分析指标   | 目标变量分布、特征变量、训练/测试集、准确率、召回率、精确率、AUC 或混淆矩阵。 |
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

- 先把业务目标转成可建模问题：明确预测对象、标签字段、样本粒度和模型输出的业务含义。
- 做数据检查和探索：查看缺失值、异常值、类别分布、关键变量分布，以及目标变量是否存在不平衡。
- 完成特征处理：对类别变量编码，对数值变量缩放或标准化，并根据业务含义保留可解释变量。
- 建立基准模型并比较效果：优先选择可解释模型作为 baseline，再根据数据复杂度尝试树模型或集成模型。
- 把模型指标翻译成业务动作：例如风控看召回和误报，营销看转化和 ROI，预测类问题看高峰期误差。

## 五、数据处理过程

本项目的数据处理主要包括以下环节：

- 读取原始数据，检查字段类型、样本规模和基础统计信息。
- 处理缺失值、重复值、异常值或文本噪声，保证后续统计和建模结果可靠。
- 根据分析目标构造必要指标、标签或特征，并统一字段口径。
- 按业务维度进行分组、聚合、可视化或模型训练，为结论提供依据。

## 六、数据分析与结果

本部分按照“分析发现 -> 结果解读”的方式组织，重点说明数据体现出的现象及其业务含义。

### 1. 水色图像能提供直观信号，但会受到光照、拍摄角度、天气和设备差异影响。

结果解读：该发现是本项目最核心的结论之一，说明数据中存在值得关注的结构性特征。对应图表或模型结果应围绕这一判断展开，帮助读者理解结论来源。

### 2. SVM 适合中小规模样本的分类任务，尤其在特征维度明确时能作为可靠基准模型。

结果解读：该发现进一步解释了不同维度之间的差异。对业务决策而言，重点不只是看到差异，而是判断差异来自哪些对象、场景或指标。

### 3. 环境监测模型的业务价值在于预警和筛查，而不是替代专业检测。

结果解读：该发现可以作为后续优化策略或模型改进的依据。若用于真实业务，还需要结合成本、资源、实验结果或线上反馈继续验证。

## 七、结论

综合以上分析，可以得到以下结论：

- 水色图像能提供直观信号，但会受到光照、拍摄角度、天气和设备差异影响。
- SVM 适合中小规模样本的分类任务，尤其在特征维度明确时能作为可靠基准模型。
- 环境监测模型的业务价值在于预警和筛查，而不是替代专业检测。

## 八、建议

- 行动 1：实际部署应统一采集设备和拍摄条件，降低非水质因素带来的误差。
- 行动 2：建议把模型输出设计为风险等级和复检建议，而不是单一结论。
- 行动 3：后续可扩展到深度学习图像分类，并结合地理位置、时间和历史水质数据。
- 跟进方式：为每条建议绑定一个可观察指标，后续按周或按月复盘效果。

建议部分应结合具体对象、执行动作和复盘指标，避免停留在泛泛的“加强管理”或“优化运营”。

## 九、局限性与改进方向

- 项目价值：用可量化模型辅助判断关键结果，减少只依赖经验决策带来的不稳定性。
- 真实限制：当前数据只覆盖项目样本范围，缺少线上业务闭环中的成本、反馈、人工审核和长期跟踪信息。
- 业务风险：如果把离线分析结论直接用于真实决策，可能因为数据时效、样本偏差或执行条件变化造成效果偏离。
- 改进方向：按时间切分训练集和验证集，增加线上/线下指标对齐，避免随机切分高估模型效果。
- 改进方向：补充模型监控，包括数据漂移、预测分布、召回率、误报率和业务转化效果。

## 附录：完整代码与输出结果

下面内容按原 notebook 的代码单元顺序整理。如果代码单元产生了文本输出或图片输出，也一并附在对应代码后面，便于复现完整分析过程。

### 代码单元 1

```python
import numpy as np
import pandas as pd
from sklearn import preprocessing
from PIL import Image
import os

def PicManage(path,i):
    pic = Image.open(path)
    pic.c_x, pic.c_y = (int(i/2) for i in pic.size)
    box = (pic.c_x-50, pic.c_y-50, pic.c_x+50, pic.c_y+50)
    #从图片中提取中心100*100的子矩形
    region = pic.crop(box)
    
    #切分RGB
    r, g, b = np.split(np.array(region), 3, axis = 2)
    
    #计算一阶矩
    r_m1 = np.mean(r)
    g_m1 = np.mean(g)
    b_m1 = np.mean(b)
    
    #二阶矩
    r_m2 = np.std(r)
    g_m2 = np.std(g)
    b_m2 = np.std(b)
    
    #三阶矩
    r_m3 = np.mean(abs(r - r.mean())**3)**(1/3)
    g_m3 = np.mean(abs(g - g.mean())**3)**(1/3)
    b_m3 = np.mean(abs(b - b.mean())**3)**(1/3)
    
    #将数据标准化，区间在[-1,1]
    typ = np.array([i])
    arr = np.array([r_m1,g_m1,b_m1,r_m2,g_m2,b_m2,r_m3,g_m3,b_m3])
    #df = pd.DataFrame(preprocessing.minmax_scale(arr,feature_range=(-1,1))).T
    df = pd.DataFrame(arr).T
    dn = pd.DataFrame(typ).T
    return df,dn

result = []
type_result = []
for i in os.listdir('./data/images'):
    if i.endswith('.jpg'):
        df,dn = PicManage('./data/images/'+i,int(i[0]))
        result.append(df)
        type_result.append(dn)
        
data = pd.concat(result)
typ = pd.concat(type_result)
data = pd.DataFrame(preprocessing.normalize(data,norm='l2'))
data['type'] = typ.values
data.to_excel('./data/picData.xlsx',index = False)
```

### 代码单元 2

```python
data
```

**文本输出**

```text
0         1         2         3         4         5         6  \
0    0.694584  0.648002  0.300866  0.016948  0.019283  0.049012  0.019829   
1    0.724619  0.644356  0.241090  0.017369  0.012551  0.015402  0.019654   
2    0.684701  0.654157  0.320038  0.009824  0.008021  0.013856  0.011670   
3    0.674509  0.679098  0.288470  0.009039  0.006791  0.012106  0.010517   
4    0.675955  0.677012  0.289796  0.008533  0.007435  0.013893  0.010055   
..        ...       ...       ...       ...       ...       ...       ...   
198  0.560942  0.804839  0.184335  0.027689  0.023188  0.015606  0.032190   
199  0.618554  0.736411  0.269419  0.019033  0.014666  0.021957  0.022124   
200  0.624337  0.729070  0.276431  0.017316  0.012111  0.022299  0.020220   
201  0.620825  0.736037  0.265352  0.018336  0.013935  0.021965  0.021619   
202  0.651614  0.648433  0.391345  0.014332  0.013291  0.019667  0.016500   

            7         8  type  
0    0.022430  0.056295     1  
1    0.014343  0.017885     1  
2    0.009515  0.016106     1  
3    0.008115  0.014070     1  
4    0.008754  0.016116     1  
..        ...       ...   ...  
198  0.026074  0.018299     5  
199  0.017318  0.025589     5  
... 输出过长，博客中已截断
```

### 代码单元 3

```python
print(data.shape)
```

**文本输出**

```text
(203, 11)
```

### 代码单元 4

```python
import pandas as pd

# datapath = './data/picData.xlsx'
# data = pd.read_excel(datapath)
# print(data.columns)
# data1 = data[[0, 1, 2, 3, 4, 5, 6, 7, 8]]
# data1 = data1.values
# data2 = data[['type']]
# data2 = data2.values

datapath = './data/moment.csv'
data = pd.read_csv(datapath,encoding='gbk')
print(data.columns)
data1 = data[['R通道一阶矩', 'G通道一阶矩', 'B通道一阶矩', 'R通道二阶矩', 'G通道二阶矩', 'B通道二阶矩',
       'R通道三阶矩', 'G通道三阶矩', 'B通道三阶矩']]
data1 = data1.values
data2 = data[['类别']]
data2 = data2.values
```

**文本输出**

```text
Index(['类别', '序号', 'R通道一阶矩', 'G通道一阶矩', 'B通道一阶矩', 'R通道二阶矩', 'G通道二阶矩', 'B通道二阶矩',
       'R通道三阶矩', 'G通道三阶矩', 'B通道三阶矩'],
      dtype='object')
```

### 代码单元 5

```python
#划分训练集和测试集
#cross_validation 在sklearn0.20中改为model_selection
from sklearn.model_selection  import train_test_split
train, test, train_target, test_target = train_test_split(data1,data2,test_size=0.2)
train_target = train_target.astype(int)
test_target = test_target.astype(int)

#构建SVM模型
from sklearn import svm
model = svm.SVC()
model.fit(train*30,train_target)
```

**文本输出**

```text
c:\users\administrator\envs\jupytervir\lib\site-packages\sklearn\utils\validation.py:63: DataConversionWarning: A column-vector y was passed when a 1d array was expected. Please change the shape of y to (n_samples, ), for example using ravel().
  return f(*args, **kwargs)
SVC()
```

### 代码单元 6

```python
#混淆矩阵
from sklearn import metrics

cm_train = metrics.confusion_matrix(train_target, model.predict(train*30))
# 分类准确率
train_accuracy = metrics.accuracy_score(train_target,model.predict(train*30))
print("train accuracy: %f"% train_accuracy) # 0.777778

tr = pd.DataFrame(cm_train,index = range(1,6),columns = range(1,6)).to_excel('./data/train.xlsx')
```

**文本输出**

```text
train accuracy: 0.777778
```

### 代码单元 7

```python
#保存模型
# from sklearn.externals import joblib 旧版 scikit-learn==0.20.3
import joblib
joblib.dump(model,'svcmodel.pkl')
```

**文本输出**

```text
['svcmodel.pkl']
```

### 代码单元 8

```python
#加载模型
model = joblib.load('svcmodel.pkl')
#混淆矩阵
cm_test = metrics.confusion_matrix(test_target, model.predict(test*30))
# 分类准确率
test_accuracy = metrics.accuracy_score(test_target,model.predict(test*30))
print("test accuracy: %f"% test_accuracy) #0.756098

te = pd.DataFrame(cm_test,index = range(1,6),columns = range(1,6)).to_excel('./data/test.xlsx')
```

**文本输出**

```
test accuracy: 0.756098
```

