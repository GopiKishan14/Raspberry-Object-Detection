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
* USAGE, To run the videostream
```
python real_time_object_detection.py --prototxt MobileNetSSD_deploy.prototxt.txt --model MobileNetSSD_deploy.caffemodel
```
Note : Press 'q' to stop the videostream.


## Abstract Code WalkThrough :


* Importing

![image](https://user-images.githubusercontent.com/32811229/80908634-07b54e00-8d3f-11ea-9ddb-b553f04ba80a.png)

* Creating the argument parser for the python script
![image](https://user-images.githubusercontent.com/32811229/80908719-cf623f80-8d3f-11ea-9ce2-c21dd53b5e71.png)

* a

![image](https://user-images.githubusercontent.com/32811229/80908757-2d8f2280-8d40-11ea-92a5-40403ec84015.png)

* b
![image](https://user-images.githubusercontent.com/32811229/80908774-57e0e000-8d40-11ea-916e-96373273c93b.png)

* c

![image](https://user-images.githubusercontent.com/32811229/80908793-7ba42600-8d40-11ea-85d8-1f4aab2304de.png)


* d

![image](https://user-images.githubusercontent.com/32811229/80908812-9d051200-8d40-11ea-897d-69385cca2291.png)

* e

![image](https://user-images.githubusercontent.com/32811229/80908821-bf972b00-8d40-11ea-8733-a00f8244de93.png)

