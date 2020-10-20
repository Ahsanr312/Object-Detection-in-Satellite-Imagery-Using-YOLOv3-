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
  - Run LabelImg then click on "Open Dir" and choose the folder where the training dataset is located.
  - For "Change save dir", choose the same training dataset folder.
  - Then select saving format which by default is "PascalVOC" click to change it to "YOLO" format.
  - For labeling the object, click "Create RectBox" and select the area where the target object is located. Then add the label by giving object name (which in our case is Jet).
  - Then click on "Save" which will generate a .txt for the respective image. Do this for the complete training dataset.
  - Finally, rename this training dataset folder to "images" and compress to get images.zip

#### 2. Training online using Google Colab
- Google Colab will be used for the training of YOLOv3. It provides a free service as well as a pro service that can be only used when you pay for it. In our case the free service provided is sufficient enough to train YOLOv3 on our custom dataset. The only disadvantage that I noted is that one can only use it for 12 hours in a single go, after that you will be disconnected and the files will deleted. Though, this problem is solved with help of the falgs in training time. YOLOv3 while training saves weights so even the training is interrupted we can resume training from last saved weights.
- Set up google drive:
  - Log in to your google account and go to google drive.
  - Create a folder, by naming it "yolov3" and upload the images.zip that we prepared earlier to yolov3 folder.
- Set up google colab:
  - Upload "Train_YoloV3"
 
Go on google colab and log in with the same account you used to log in on google drive.
Upload this file “Train_YoloV3.ipynb”
n.b. You can get this file by clicking on “Click here to download the Source code” at the beginning of the post.
Then we need to enable the GPU. So click on “Edit”.
