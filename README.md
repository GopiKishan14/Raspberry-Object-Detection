# Raspberry-Object-Detection

## Guidelines
* This repository contains python script for the object detection on Raspberry Pi in real time using OpenCV. 
* It uses a already trained [MobileNet](https://arxiv.org/abs/1704.04861) Architecture stored as Caffe Model. 
* This model uses Single Shot Detection([SSD](https://arxiv.org/abs/1512.02325)) algorithm for prediction.
* Look for the architecture detail at [here](https://github.com/GopiKishan14/Raspberry-Object-Detection/blob/master/MobileNetSSD_deploy.prototxt.txt)
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
