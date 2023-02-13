# OpenMMLab-mmseg-advanced
## 使用环境
win10 + cuda11.3 +pytorch1.10.0
## 数据准备
数据集PascalVOCDataset
<br>数据集组织结构：
```shell
mmseg
├── data
│   ├── VOCdevkit
│   │   ├── VOC2012
│   │   │    ├──Annotations
│   │   │    ├──ImageSets
│   │   │    ├──JPEGImages
│   │   │    ├──SegmentationClass
│   │   │    ├──SegmentationObject
│   │   │    └──SegmentationClassAug
│   │   ├── VOC2007
└   └   └── VOCaug
```
## 训练
训练脚本
```bash
python tools/train.py pspnet_r50-d8_512x512_20k_voc12.py --work-dir work/voc
```
## 结果
|  aAcc  |   mIoU  |   mAcc  |
| :----: | :-----: | :-----: |
|  91.38 |  64.33  |  77.73  |

## 训练pth
链接：https://pan.baidu.com/s/1p9SGjS0yeNCzOqZf5Fdizw?pwd=h0ll 
提取码：h0ll
