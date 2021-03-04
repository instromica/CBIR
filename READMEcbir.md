# 基于内容的图像检索系统

## 项目描述

> - **特征提取**：采用VGG16网络进行特征提取(使用keras预训练的网络)
> - **索引构建**: 采用线性索引和kd树实现

**The Oxford Buildings Dataset测评结果**

|  mAP  | average time |     
| 0.806 |    1.08s     |



## 开发环境

python 3.7

tensorflow 1.14.0

keras 2.2.5

## 其他必须安装的库

numpy 1.16.4

h5py 2.8.0

matplotlib 3.0.2

## 目录说明:

├─ dataset  
├─ groundtruth  
├─ models  
├─ src  
│─ calmAP.py  
│─ vgg16.py      
│─ index,py      
│─ kdtree.py    
│─ query.py    
│─ searchpic.py  
│─ GUI.py



## 数据集准备

### oxbuild_images

下载链接[oxbuild_image](https://www.robots.ox.ac.uk/~vgg/data/oxbuildings/)

文件组织形式如下


oxbuild_images 
|_ all_souls000000.jpg  
|_ ...  
|_ worcester_000198.jpg  


### caltech256图像数据库

文件组织形式如下

database  
|_ 0001_0001.jpg  
|_ ...  
|_ 257_0827.jpg  





## 运行系统

1. 在windows 10 系统上运行GUI.py

2. 选定要检索的图片

3. 选定要检索的数据集

4. 点击检索按钮即可展示检索结果




### 返回前十张图

运行程序后会返回前十张图的图片名和相似度得分，以及搜索所耗的时间


### 计算AP与mAP


运行cal_mAP文件，即可返回在oxbuild_images数据集上计算得到的mAP


mAP = 0.806060606060606059


