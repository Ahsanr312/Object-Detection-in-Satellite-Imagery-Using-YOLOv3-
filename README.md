# Object-Detection-in-Satellite-Imagery-Using-YOLOv3
This repository provides the experimentation of Object Detection in Satellite Imagery using YOLOv3.
A simple laptop (windows, linux or mac) is all you need for this project, as we will be using Google Colab for training and testing purpose. 

### Original Repository: https://github.com/AlexeyAB/darknet

### Yolov3 Paper: https://arxiv.org/abs/1804.02767

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
  - Upload "Train_YOLOv3.ipynb" file to the same yolov3 folder on google drive by first downloading it.
  - After successful upload, right click on the "Train_YOLOv3.ipynb" file and select open with -> Google Colaboratory. The file will opened in the colab.
  - Next, we need to choose GPU for our training. To do so, click on "Edit" and select "Notebook settings" and then choose "GPU" under Hardware accelerator option. 
  - Press "save" and you are good to go.
  - Now run each cell one by one and wait for the first cell to complete the execution. (You can run all cells together by clicking "Runtime" and then selecting "Run all" but I recommend run one cell at a time and check the output and play around)
  - This notebook is created for training YOLOv3 for only one object. But you can do it for as much objects as you desire by changing some parameters.
  
#### 3. Important Training Steps/Parameters:
- 


