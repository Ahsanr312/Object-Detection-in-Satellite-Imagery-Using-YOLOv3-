# Object-Detection-in-Satellite-Imagery-Using-YOLOv3-
This repository provides the experimentation of Object Detection in Satellite Imagery using YOLOv3.
A simple laptop (windows, linux or mac) is all you need for this project, as we will be using Google Colab for training and testing purpose.

### Original Repository: https://github.com/AlexeyAB/darknet

### Paper Yolo v3: https://arxiv.org/abs/1804.02767

### About Darknet framework: http://pjreddie.com/darknet/

### Dataset: Will be shared on request {ahsanr4@gmail.com}

### STEPS TO FOLLOW:

#### 1. Dataset Preparation 
- An image dataset is a folder containing images of our target object for which we want to train YOLOv3. There must be a minimum of 100 images that contains the target object. For example I have trained YOLOv3 to recognize Jets, so I have made a dataset comprising of 402 images while each image contains atleast one Jet.
- Secondly, we need object location in each image that is exactly where the object/objects are located in each images. For this purpose, we need to label each image from our training dataset. An external software will be used for image labeling, that is, "LabelImg". You can download it for Windows/Linux from https://tzutalin.github.io/labelImg/ 
- LabelImg Usage:
  - I am Ahsan
