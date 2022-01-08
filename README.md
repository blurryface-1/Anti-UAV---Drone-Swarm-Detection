# Building a Custom Anti-UAV Object Detection Model using YOLOv5 

<p align="center">
  <a>
    <img src="https://www.embention.com/wp-content/uploads/2019/06/greg-rakozy-S-8ntPEsSwo-unsplash-1024x387.jpg.webp" alt="Logo" width="1020" height="400">
  </a>
<br />
</p>

This repo let's you train a custom image detector using the state-of-the-art <a href ="https://github.com/ultralytics/yolov5">YOLOv5</a> computer vision algorithm. The detector will be trained on a dataset of images of drones. This model will be able to detect drones in the images and videos in almost real-time.
<br>

## Introduction:

Unmanned Ariel Vehicles (UAVs) have a wide range of uses and are definitely one of the fastest-growing technologies in the world right now. UAVs have become very accessible to the masses over the recent years. However, the negligent and malevolent use of UAVs can pose a significant risk. Drone technology today poses a threat to the governments, companies, and the general public since they have been used for espionage and military strikes in the past.

Drones can be employed for a variety of attacks due to their ease of control. As a result, there is a dire necessity for preventive countermeasures.

This repo presents a viable drone detection system based on YOLOv5 that uses drone images captured under varied lighting and weather circumstances to detect drones swarms. 
<br><br>

## Pipeline Overview:

To build and test your YOLO object detection algorithm follow the below steps:

1. <b>Image Annotation </b>
   - Download the [dataset](https://app.roboflow.com/ds/GCfAhcDsm5?key=M3f5GiSxHE) of images of drones. The dataset consists of drones in various environmental and lighting conditions.
   - Label the images using any image annotation tool.
   - Annotate the images.

2. <b>Training </b>
   - Download pre-trained weights.
   - Train your custom YOLO model on annotated images 

3. <b>Inference </b>
   - Detect objects in new images and videos.
   - 

<br>

## Getting Started


### Google Colab  <a href="" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

With Google Colab, you can skip most of the set up steps and start training your own model right away. 

<br>

## About The Project

This drone detection system uses YOLOv5 which is a family of object detection architectures and we have trained the model on Drone Dataset.

### Architecture: The Image depicts flowchart for YOLO Architecture.

<br>
  <p align="center">
  <a>
    <img src="https://i.ibb.co/MgwYh3v/unknown.png" alt="Logo" width="720" height="300">
  </a>
    <br>
​    


* YOLO an acronym for 'You only look once', is an object detection algorithm that divides images into a grid system. Each cell in the grid is responsible for detecting objects within itself.

* The YOLO algorithm considers the positions of bounding boxes and the likelihood of a class as a regression problem to guess by looking at them once on video content or images.  

* After dividing the input photos by a `SxS` grid, it estimates the locations of bounding boxes that encompass annotated entities. To calculate the confidence score, the anchor boxes that overlap the bounding boxes, guess the objects' class probabilities, location of object centers, and bounding box dimensions. 

* The confidence score is based on whether the objects are present in the bounding boxes, as well as how much of the relevant class is reflected. Following equation can be used to compute it.
  `
  $$
  C = P(class) ☓ IoU
  $$
  `
  where C refers to the confidence score and IoU (Intersection over Union) 

* IoU is the value obtained by dividing the size of the intersection between the correct-answers box and the prediction box by the size of the union, which refers to the degree of overlap. Therefore, IoU is 0 if there is no intersection and 1 if they entirely overlap.

<br>

![img](https://miro.medium.com/max/2000/1*HW82Bdszqwii0-H4K1mcXg.png)

<br>

### Data:

The learning data was established by attaching labels, x-coordinates, y-coordinates, width, and height values to all the images obtained by the splitting the frames of the videos from the [Anti-UAV dataset](). On average, each RGB video returned 1000 frames. Images were later chosen to make the dataset more diverse and precise given the presence of numerous similar frames. A learning data of 2,485 photos was generated from the entire collection of images obtained. From the learning data, 2,244 images were used for training and the rest 241 images were used for validation. As hyperparameters for training, the batch size and subdivision values were all set to 8, and the epoch number was set to 80. 
<br/>

<br>

### Performance:

<p align="center">
  <a>
    <img src="https://i.ibb.co/JRkW3TJ/results.png" alt="Logo" width="1080" height="500">
  </a>
<br />
The final model was observed to have a precision of 99.1% and a recall of 97.5% on the test data.


<br>

## Outputs:

<p align="center">
<a><img src="https://i.ibb.co/Rj30GWG/Screenshot-2021-11-22-044919.png" alt="Logo" width="1080" height="600"></a>
<br/>
