# OpenMMLab-mmseg-basic
## 使用环境
win10 + cuda11.3 +pytorch1.10.0
<br>环境安装链接：https://github.com/open-mmlab/mmsegmentation/blob/master/docs/en/get_started.md#installation
## 数据准备
组织病理切片小鼠肾小球：https://zihao-openmmlab.obs.cn-east-3.myhuaweicloud.com/20230130-mmseg/dataset/Glomeruli-dataset.zip
<br>数据集组织结构：
```shell
mmseg
├── data
│   ├── glomeruli
│   │   ├── splits
│   │   │    ├──train.txt
│   │   │    └──val.txt
│   │   ├── masks
└   └   └── images
```
## 训练
训练脚本
```bash
python tools/train.py pspnet_r50-d8_512x1024_40k_glomeruli.py --work-dir work/pspnet
```
## 结果
|  aAcc  |   mIoU  |   mAcc  |
| :----: | :-----: | :-----: |
|  99.6  |  90.32  |  94.91  |
## 训练pth
链接：https://pan.baidu.com/s/1W4IdlIdrA_--EUyRlXLc7g?pwd=ao5b 
提取码：ao5b

<br>
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
│   │   ├── VOC2007
│   │   ├── VOC2012
└   └   └── VOCcode
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
