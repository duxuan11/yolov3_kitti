## YOLOV3：You Only Look Once目标检测模型在Pytorch当中的实现
---

 

## 目录
1. [文件下载 Download](#文件下载)
2. [预测步骤 How2predict](#预测步骤)
3. [训练步骤 How2train](#训练步骤)

## 文件下载
训练所需的yolo_weights.pth可以在百度云下载。  
链接: https://pan.baidu.com/s/1ncREw6Na9ycZptdxiVMApw   
提取码: appk
kitti
只需要下载Download left color images of object data set (12 GB)和对应的标签Download training labels of object data set (5 MB)即可。

## 预测步骤
### a、使用预训练权重
1. 下载完库后解压，在百度网盘下载yolo_weights.pth，放入model_data，运行predict.py，输入  
2. 也可以使用自己的训练权重 但注意修改yolo.py里的model_path
```python
img/street.jpg
```
2. 在predict.py里面进行设置可以进行fps测试和video视频检测。  
```
1. 运行predict.py，输入  
```python
img/street.jpg
```
2. 在predict.py里面进行设置可以进行fps测试和video视频检测。  

## 训练步骤
1. 本文使用VOC格式进行训练。  
2. 训练前将标签文件放在VOCdevkit文件夹下的VOC2007文件夹下的Annotation中。  
3. 训练前将图片文件放在VOCdevkit文件夹下的VOC2007文件夹下的JPEGImages中。  
4. 在训练前利用voc2yolo3.py文件生成对应的txt。  
5. 再运行根目录下的voc_annotation.py，运行前需要将classes改成你自己的classes。**注意不要使用中文标签，文件夹中不要有空格！**   

8. **修改train.py里面的num_classes，使其为要检测的类的个数**。   
9. 运行train.py即可开始训练。

