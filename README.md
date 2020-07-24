# 简介

基于 https://github.com/tensorboy/pytorch_Realtime_Multi-Person_Pose_Estimation 仓库添加的一种方法。

## 主要工作

在原先VGG+PAF的基础上修改，使用在关键点检测方面表现优异的HRNet进行backbone的替换，实现了HRNet+PAF的实时人体姿态估计。

训练入口：./train/train_hrnet.py

模型实现：./lib/network/rtpose_hrnet.py

## 模型性能

资源不足问题导致训练超慢（虽然后续关键点以及PAF分支从6层叠加删减至2层）~

之前在租的服务器上跑了几十轮：

VGG+PAF mAP为0.36

HRNet+PAF mAP为0.43

目前瞅着还算说得过去~~~