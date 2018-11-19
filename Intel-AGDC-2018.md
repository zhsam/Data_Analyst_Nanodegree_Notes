# AIDEVCON - Intel 人工智能大会
**Navee Rao- Intel 全球副总裁|人工智能事业部总经理**

## Part1- 工具
### 产品1： MKL DNN
**Intel 数据科学部主任 - 刘茵茵**

### 展示：百度
**百度 - Intel**
> 目前应用场景：

- 视觉
- 语言
- Deep CTR

> 语意匹配模型：文本建模

- BOW — CNN — GRNN — Matching Matrix

> 信息流 CTR 模型

- 小时级别，训练几亿数据，分布式、异步训练

> 下一步：

- 复杂模型部署，使用Intel MKL DN

### 产品2： nGraph
跨硬件的中间层
NervanaSystems/ngraph

### 展示：
**薛文哲 - 深度学习工程师**
跨硬件的灵活性
快速为图片变换场景

### 产品3： OpenVINO
推理速度：功耗：成本

## 应用介绍
### 医学影像
**汇医慧影 CEO- 柴象飞**

- 公司介绍

- 现有应用-乳腺癌
早期筛查 - 诊断 -

- 人工智能的三个金字塔
算法、算力、数据
快速使用AI赋能原有设备

- 未来展望
做宽做深
参与Intel AI智能实验室

- Vision for AI
AI赋能传统
从影像基础到疾病全管理+综合化决策

## Part2 - 硬件 Hardware


## Part3 - 社区 Community
Xeon - most of the data center runs on Xeon
CaseL Facebook

### 展示
**胡正-Midea视觉研究所长**
工业视觉检测

- how does AI help to do that?
Machine Vision System.
Different Angles - spend too much time for developing tools using traditional algorithms.
With AI, you'll be able to generate a trained model to.

- How does Intel AI help with that?
We want to utilize the computing power.

- Can you show some of the results?
中央空调的装配完整性检测。一台单相机，完成了检测。
不需要太多的打光等等，投资回报率特别高 (两个月)。
投诉 -- 罚款 (5000-10000)。
希望复制到其他地方，1.6M 投入这个应用。

- 关于AI的未来？
有些人会觉得AI会超越人，目前我们去训练AI，
到了一定阶段：让AI训练我们，例：下围棋，打网球。
你有更多的可能可以训练出更厉害的人，与AI共同进步。
希望一起合作，推广AI。

### 展示
ResNet
DLBoost - 10X faster than Xeon

### FPGA

### 展示：
Microsoft Azure


### Intel Movidius：VPU
Visual Processing CPU
Neural Compute Stick
http://intel.com/ncs

### 展示：

### Interl Nervana
### 展示：

### AI Builders Program
Incubate

### AI 应用
*腾讯高级硬件开发经理**
腾旭优图 - 计算机视觉产品落地

应用领域
- 安防- 亿级人脸库、毫秒级返回结果
- 工业-
- 医疗- 子宫癌
- 公益- 跨年龄段应用，匹配几年后的人脸 (防止600万人走失)
- 智慧零售：腾讯优Mall，提升营业额

硬件
- 优图盒子- Intel CPU+Myriad，本地进行 AI 预处理
- 腾讯优图 AI 摄影机- 实现基于人脸检测、跟踪

### Case：Ferrari Challenge
**Emile Chin-dickey Intel AI**
- Car detection: MobileNet, TensorFlow
- Classification: Identify individual driver, look at subtle differences
what happened if they change
Triditional: take 1000 photos of a car,
matching: Didn't require re-training

Frame by Frame Classification
Maintain the history of
Increase the Classification Confidence by time
-
End-to-end friend

### 开发者社区
开源工具+开发者社区
作为研究、应用、交流平台

- NLP架构：NLP architech
- RLCoach：RL Coach
- [神经网络Distiller(剪枝、量化)]('')

### MLPerf 项目
跨行业基准测试

### 长城修复方案

**南京大学-周智华**
Deep Learning - 机器学习使用深度神经网络
收到很多x，乘一个放大量，

ImageNet Winner：
- 2012: 8 layers
- 2015: 152 layers
- 2016: 1207 layers

误区：因为算力
2012前，不晓得怎么训练5层以上的模型
1- 计算单元可微
2- 算法进步，梯度不置于消失／离散

为什么要做到很深？
增加模型复制度，学习容量提高，学习能力可能提高

增加复杂度：
- 增加宽度：函数个数
- 增加深度：个数、迭代层数(更有效)

Sigmoid --> ReLu，解决

过你合是什么？

怎么防止过拟合？
决策树：剪枝
深度学习：早期停止

模型学习能力太强，当做一般规律：过拟合

缓解过拟合最有效的办法：更多的数据
3000万，过拟合风险降低

模型复杂度很重要，

浅层网络也可以用
一个影层，增加到无限神经元
为什么做不好？
1989年，一个隐含层，
可以以任意经度、复杂度

真正重要的：表示学习
以前：形状纹理描述图像，拿到原始对象，特徵工程(人)
Feature Learning / Representation Learning

表示学习最重要的是什么？逐层学习
至底往上：逐渐加工
不管浅层复杂度多高，始终做不到这一步

如果逐层处理很重要，决策树为什么不够好呢？
1-复杂度不够，最大深度 最多
2-使用最初使用特徵，没有用内部属性变换

Boosting?
1- 复杂度不够
2- 始终在原始空间上做事，没有做模型变换

做的深？
- 逐层加工
- 特徵内部变换

过拟合

数据量大下，复杂度小模型，学不进去
例：线性模型，1万样本 v.s. 1万万样本(学不进去)

帮助我们解决深度学习的
以前以为是原因，现在说反了
以前理解、解释，把因果弄反了

深度模型：(图片)
-
-
-
满足这三条因素，并非一定要靠神经网络

有没有必要考虑神经网络之外的模型?
神经网络的缺陷：
- 调参
同一个模型，不告诉你参数，无法重现这个模型
-
往往使用比实际更复杂的模型解决，训练过程中，逐渐简化他(shortcut, 权重二值化)

有没有可能自适应变化复杂度？很难做到

很多问题上 Kaggle数据分析比赛，
很多比赛获胜者是传统算法？为什么？

深度没有
离散、混合见磨
