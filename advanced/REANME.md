# OpenMMLab-mmseg-advanced
## 使用环境
win10 + cuda11.3 +pytorch1.10.0
## 数据准备
数据集PascalVOCDataset + Aug
<br>
生成AUG步骤：
<br>1、下载SBD,SBD官网：http://home.bharathh.info/pubs/codes/SBD/download.html
<br>2、将SBD解压后将dataset放进去vocaug（这个文件夹自己创建一下）
<br>3、在mmseg中python tools/convert_datasets/voc_aug.py data/VOCdevkit data/VOCdevkit/VOCaug --nproc 8运行
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
VOC数据集训练
```bash
python tools/train.py pspnet_r50-d8_512x512_20k_voc12.py --work-dir work/voc
```
<br>VOC数据集增强+Aug训练
```bash
python tools/train.py pspnet_r50-d8_512x512_20k_voc12aug.py --work-dir work/voc_aug
```
## 结果
### Voc数据集训练结果
|  aAcc  |   mIoU  |   mAcc  |
| :----: | :-----: | :-----: |
|  91.38 |  64.33  |  77.73  |
### Voc + Aug数据集训练结果
|  aAcc  |   mIoU  |   mAcc  |
| :----: | :-----: | :-----: |
|  87.69 |  58.09  |  81.11  |
## 训练pth和log
<br>Voc数据集训练结果Pth
<br>20230213_194659.log<br>
链接：https://pan.baidu.com/s/1p9SGjS0yeNCzOqZf5Fdizw?pwd=h0ll 
提取码：h0ll
<br>Voc+aug数据集训练结果Pth
<br>20230213_220527.log
<br>
链接：https://pan.baidu.com/s/1nuABQIK_5RAVA7K3UDCFFA?pwd=b6in 
提取码：b6in
