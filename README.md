# Raspberry-Object-Detection

## Guidelines
* This repository contains python script for the object detection on Raspberry Pi in real time using OpenCV. 
* It uses a already trained [MobileNet](https://arxiv.org/abs/1704.04861) Architecture stored as Caffe Model. 
* This model uses Single Shot Detection([SSD](https://arxiv.org/abs/1512.02325)) algorithm for prediction.
* Look for the architecture detail [here](https://github.com/GopiKishan14/Raspberry-Object-Detection/blob/master/MobileNetSSD_deploy.prototxt.txt)
* This [code](https://github.com/GopiKishan14/Raspberry-Object-Detection/blob/master/pi_object_detection.py) stores the input images in a queue and output the predictions along with box in queue.
* This [code](https://github.com/GopiKishan14/Raspberry-Object-Detection/blob/master/real_time_object_detection.py) runs on real time videostream to output the prediction as well as bounding box across it.
* Above codes can be directly run on raspberry pi having packages [imutils](https://pypi.org/project/imutils/) and [cv2](https://pypi.org/project/opencv-python/)
* To Install, run
```
pip install imutils
pip install opencv-python
```
* USAGE, To run the videostream, clone the repo and in working directory, run
```
python real_time_object_detection.py --prototxt MobileNetSSD_deploy.prototxt.txt --model MobileNetSSD_deploy.caffemodel
```
Note : Press 'q' to stop the videostream.


## Abstract Code WalkThrough :
### Overviewing real_time_object_detection.py

* Importing packages

![image](https://user-images.githubusercontent.com/32811229/80908634-07b54e00-8d3f-11ea-9ddb-b553f04ba80a.png)

* Creating the argument parser for the python script
![image](https://user-images.githubusercontent.com/32811229/80908719-cf623f80-8d3f-11ea-9ce2-c21dd53b5e71.png)

* Initializing the list of class labels MobileNet SSD was trained to detect, then generate a set of bounding box colors for each class.

![image](https://user-images.githubusercontent.com/32811229/80908757-2d8f2280-8d40-11ea-92a5-40403ec84015.png)

* Load the model and initialize the video stream.

![image](https://user-images.githubusercontent.com/32811229/80908774-57e0e000-8d40-11ea-916e-96373273c93b.png)

* For each frame, obtain the detections and predictions.

![image](https://user-images.githubusercontent.com/32811229/80908793-7ba42600-8d40-11ea-85d8-1f4aab2304de.png)


* For each detection, if prediction is above confidence (self-defined), draw the bounding box over it.

![image](https://user-images.githubusercontent.com/32811229/80908812-9d051200-8d40-11ea-897d-69385cca2291.png)

* Shows the output frame with break condition key "q". On Break condition, it destroys all the windows.

![image](https://user-images.githubusercontent.com/32811229/80908821-bf972b00-8d40-11ea-8733-a00f8244de93.png)


## Learning Resources
### For Learning basics of Raspberry PI 
[![Tutorial](http://img.youtube.com/vi/RpseX2ylEuw/0.jpg)](https://www.youtube.com/playlist?list=PLQVvvaa0QuDesV8WWHLLXW_avmTzHmJLv "Visit sentdex")
