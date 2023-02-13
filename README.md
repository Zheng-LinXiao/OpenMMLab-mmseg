# OpenMMLab-mmseg-basic
## 使用环境
win10 + cuda11.3 +pytorch1.10.0
环境安装链接：https://github.com/open-mmlab/mmsegmentation/blob/master/docs/en/get_started.md#installation
## 数据准备
组织病理切片小鼠肾小球：https://zihao-openmmlab.obs.cn-east-3.myhuaweicloud.com/20230130-mmseg/dataset/Glomeruli-dataset.zip
数据集组织结构：
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
# 训练
训练脚本
```bash
python tools/train.py pspnet_r50-d8_512x1024_40k_glomeruli.py --work-dir work/pspnet
```
# 结果
+------+-------+-------+
| aAcc |  mIoU |  mAcc |
+------+-------+-------+
| 99.6 | 90.32 | 94.91 |
+------+-------+-------+
# 训练pth
链接：https://pan.baidu.com/s/1W4IdlIdrA_--EUyRlXLc7g?pwd=ao5b 
提取码：ao5b
