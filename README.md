# VEHICLE-RECOGNITION-SYSTEM
Engineered a comprehensive vehicle recognition system, encompassing license plate detection and recognition, car counting in images using OpenCV, video frame analysis for car counting. 

## Abstract

In today's tech-driven world, vehicle recognition systems are indispensable. This project, utilizing OpenCV and Python libraries like Keras and Tesseract, offers efficient vehicle counting and license plate detection functionalities. Despite challenges in accurately detecting vehicles of varying sizes, the system demonstrates commendable performance and versatility. From traffic logging to automated license plate and entry time registration, its applications are diverse and impactful. 

## Introduction

Vehicle recognition systems capture the license plates of moving vehicles using a camera, quickly scan various character information on the license plate based on image processing, and generate data. This mainly works on machine learning.License plate detection is identifying the part of the car that is predicted to be the number plate.This technology applies in many areas. On roads, it is used to identify the cars that are breaking the traffic rules.Vehicle detecting and counting have a significant influence in numerous systemthat helps to regulate and control traffic in urban areas.Object detection is a fascinating field in computer vision. It goes to a whole new level when we’re dealing with video data. The complexity rises up a notch, but so do the rewards.

## LICENSE PLATE DETECTION AND RECOGNITION


**Methodology**

The process involves three key steps:

Image Capture: Input is provided by capturing an image of the car containing the license plate.
Image Processing: The captured image undergoes processing to identify and isolate the license plate region.
Number Plate Recognition: Extracting the alphanumeric values from the detected license plate region.


**Results**

Upon successful execution, the program displays the recognized license plate number.

## COUNTING CARS IN IMAGE USING OPENCV


The traffic issue is a significant issue occurring in numerous urban areas in theworld. There are numerous significant reasons for the traffic issue. The quantity of
individuals moving into a metropolitan region has developed generously,prompting an emotional expansion in the quantity of vehicles. 

**Methodology**

1. Libraries used OpenCV, NumPy, Cvlib, Matplotlib, Keras and Tensorflow
2. Read an image from storage.
im = cv2.imread('traffic-jam-getty.jpg')

3. Perform object detection on the image and label about the detected
objects.
bbox, label, conf = cv.detect_common_objects(im)
output_image = draw_bbox(im, bbox, label, conf)

4. Display the image with a bounding box.
plt.imshow(output_image)
plt.show()

5. Count the number of cars in the image and print it.
print('Number of cars in the image is ' + str(label.count('car')))


**Results**

When the program has run successfully, the number of vehicles in image is printed.


## COUNTING CARS THROUGH VIDEO FRAMES

Our objective is to capture the coordinates of the moving object and highlight that object in the video.

**Methodology**

1. OpenCV is an image processing library. It is designed to solve computervision problems. OpenCV is a C/C++ library that is extended in Python.
NumPy library is used to support multi-dimensional arrays, matrices, etc.,in the Python programming language. It is an open-source numerical Python library.
import cv2
import numpy as np

2. cap=cv2.VideoCapture('video.mp4’) reads a video file. Define variables:
min_width_rect=80 min_height_rect=80 count_line_position=550

3. algo = cv2.bgsegm. createBackgroundSubtractorMOG () function carriesout the background subtraction operation.
4. Create a function
def center handle(x,y,w,h) x1=int(w/2) 
y1=int(h/2) cx=x+x1 cy=y+y1 return cx,cy

5. We will now convert the image into grayscale.
grey=cv2.cvtColor(frame1, cv2.COLORBGR2GRAY)

6. Next, we will apply Gaussian Blur to remove the noise from theimage. Gaussian blur is one of the techniques of image processing. It iswidely used in graphics designing too for reducing the noise and smoothing the image so that for further pre-processing, it will generate better output.
blur=cv2.GaussianBlur(grey,(3,3,),5)
img_sub-algo. apply(blur)

7. We will dilate the image. Dilation is one of the morphological techniques where we try to fill the pixels with the element, also known as kernels, to
fill the missing parts of the images whenever needed.
dilat=cv2.dilate(img_sub, np.ones((5,5)))

8. Now we will perform a Morphology transformation with the kernel. Here we are using a morphology-Ex technique that tells the function on which
image processing operations need to be done. To implement the morphology-Ex method using OpenCV we will be using the get structuring element method.
kernel=cv2.StructuringElement(cv2.MORPH_ELLIPSE,(5,5))

9. cv2.findContours() function find Contours, cv2.boundingRect(array) function calculates the up-right bounding rectangle of a point set or non-zero pixels of the gray-scale image.
cv2.imshow() shows the output image in a new opencv window.
cv2.waitKey(0) keeps the window open until any key is pressed.

**Results**

When the program has run successfully, the number of vehicles in video frame is printed.

## CAR SPEED DETECTION USING IR SENSOR AND ARDUINO

A simple automatic detection of speed of a vehicle is designed in Arduino Car Speed Detector project, where you can place the system in one place and view the results instantly without any human intervention.

**Methodology**

The working of the Arduino based car speed detector project is very simple. Arduino continuously reads the inputs from the IR Sensors. When a car moving
in front of the setup reaches the first sensor, Arduino becomes alert and capture a time stamp the moment the car leaves the first IR Sensor. Another time stamp is recorded when the car reaches the second IR Sensor. Millis() function of Arduino used for capturing the time stamps. Arduino then calculates the velocity by assuming the particular distance between the two IR Sensor and displays the result.

**Results**

When the program has run successfully, the speed of the vehicle is printed.


## REAL WORLD APPLICATIONS


1. Parking:
a. Automated license number and entry time registration.
b. Easy free parking spaces detection.
c. Finds the total number of vehicles parked.
d. Analyzes the total number of empty spaces.
e. Locate a particular vehicle using its license plate number.
f. Automated bill generation at exit points.

2. Toll Plaza: a. Now a days there is a huge rush at the toll plazas in order to pay thetoll tax. On any toll plaza the vehicle has to stop for paying the toll amount. Hence, we are trying to develop a system that would pay the toll amount automatically and reduce the rush at the toll plaza. Camera is used to capture number plate of vehicle.
b. Our system is able to count the total number of vehicles that are passing through the toll plazas. By doing automation of toll plaza, we can have the solution over money loss at toll plaza by reducing the man power required for collection of money and also can reduce the traffic at toll plazas which indirectly resulting in the reduction of time at toll plaza.

3. Maintaining records:  It is challenging for some individuals to record all the vehicles with them because the cars are passing by in real-time, this application can be very well-versed to attain the time-saving quality and be automated.

4. Traffic surveillance control:  As this application can be planted anywhere as it only requires a camera or some wires (for connectivity) hence if the
traffic is high at someplace, then from that area, an officer can monitor it and forward the information to next toll officer so that they could be prepared beforehand.

5. Helps traffic police:  A vehicle detection and counting system could be beneficial for the traffic police because everything they can monitor from one place only likes how many vehicles have crossed this toll and which vehicle.

## Conclusion

Now we can conclude that in many aspects it works efficiently but now it is the project we need to implement it to the real world appication so that it can be beneficial for all mankind. Hence we can use opencv for the counting of the number of the vehicles on the roads. We have used some image recognition libraries in the detection of the license plate in the system. In this way this is efficient, reliable, portable and easy technology based solution for the traffic surveillance.
