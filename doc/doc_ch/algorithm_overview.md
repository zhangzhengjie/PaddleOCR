<a name="算法介绍"></a>
## 算法介绍
本文给出了PaddleOCR已支持的文本检测算法和文本识别算法列表，以及每个算法在**英文公开数据集**上的模型和指标，主要用于算法简介和算法性能对比，更多包括中文在内的其他数据集上的模型请参考[PP-OCR v1.1 系列模型下载](./models_list.md)。

- [1.文本检测算法](#文本检测算法)
- [2.文本识别算法](#文本识别算法)

<a name="文本检测算法"></a>
### 1.文本检测算法

PaddleOCR开源的文本检测算法列表：
- [x]  DB([paper](https://arxiv.org/abs/1911.08947))（ppocr推荐）
- [x]  EAST([paper](https://arxiv.org/abs/1704.03155))
- [x]  SAST([paper](https://arxiv.org/abs/1908.05498))

在ICDAR2015文本检测公开数据集上，算法效果如下：

|模型|骨干网络|precision|recall|Hmean|下载链接|
|-|-|-|-|-|-|
|EAST|ResNet50_vd||||[敬请期待]()|
|EAST|MobileNetV3||||[敬请期待]()|
|DB|ResNet50_vd||||[敬请期待]()|
|DB|MobileNetV3||||[敬请期待]()|
|SAST|ResNet50_vd||||[敬请期待]()|

在Total-text文本检测公开数据集上，算法效果如下：

|模型|骨干网络|precision|recall|Hmean|下载链接|
|-|-|-|-|-|-|
|SAST|ResNet50_vd||||[敬请期待]()|

**说明：** SAST模型训练额外加入了icdar2013、icdar2017、COCO-Text、ArT等公开数据集进行调优。PaddleOCR用到的经过整理格式的英文公开数据集下载：[百度云地址](https://pan.baidu.com/s/12cPnZcVuV1zn5DOd4mqjVw) (提取码: 2bpi)

PaddleOCR文本检测算法的训练和使用请参考文档教程中[模型训练/评估中的文本检测部分](./detection.md)。


<a name="文本识别算法"></a>
### 2.文本识别算法

PaddleOCR开源的文本识别算法列表：
- [x]  CRNN([paper](https://arxiv.org/abs/1507.05717))（ppocr推荐）
- [x]  Rosetta([paper](https://arxiv.org/abs/1910.05085))
- [x]  STAR-Net([paper](http://www.bmva.org/bmvc/2016/papers/paper043/index.html))
- [x]  RARE([paper](https://arxiv.org/abs/1603.03915v1))
- [x]  SRN([paper](https://arxiv.org/abs/2003.12294))

参考[DTRB](https://arxiv.org/abs/1904.01906)文字识别训练和评估流程，使用MJSynth和SynthText两个文字识别数据集训练，在IIIT, SVT, IC03, IC13, IC15, SVTP, CUTE数据集上进行评估，算法效果如下：

|模型|骨干网络|Avg Accuracy|模型存储命名|下载链接|
|-|-|-|-|-|
|Rosetta|Resnet34_vd||rec_r34_vd_none_none_ctc|[敬请期待]()|
|Rosetta|MobileNetV3||rec_mv3_none_none_ctc|[敬请期待]()|
|CRNN|Resnet34_vd||rec_r34_vd_none_bilstm_ctc|[敬请期待]()|
|CRNN|MobileNetV3||rec_mv3_none_bilstm_ctc|[敬请期待]()|
|STAR-Net|Resnet34_vd||rec_r34_vd_tps_bilstm_ctc|[敬请期待]()|
|STAR-Net|MobileNetV3||rec_mv3_tps_bilstm_ctc|[敬请期待]()|


PaddleOCR文本识别算法的训练和使用请参考文档教程中[模型训练/评估中的文本识别部分](./recognition.md)。