# Person_Car_Detection-Eagle-View-Assignment-
The goal of this task is to train a model that can localize and classify each instance of person and car as accurately as possible.


Introduction

Object Detection is a prominent Computer-Vision problem that comes with its own unique facets and difficulty. In this mini-project, an attempt is made to incorporate the popular YOLO v3 object detection model to localize and classify person and cars in a real world image.


Overview and Key parameters

•	Model Name : You only look once (YOLO v3) 
•	Dataset : Subset of Open Images with cars and person images.
•	Annotation provided : COCO JSON
•	Annotation used : YOLO darknet format
•	Training set : 300 image
•	Images resolution : 416x416
•	Programming language : Python
•	Main Packages used :  Tensorflow, Numpy


Model Description

Prior work on object detection repurposes classifiers to perform detection.  Instead, we frame object detection as a regression problem to spatially separated bounding boxes and associated class probabilities. A single neural network predicts bounding boxes and class probabilities directly from full images  in  one  evaluation.   Since the whole  detection pipeline is a single network, it can be optimized end-to-end directly on detection performance.



![image](https://user-images.githubusercontent.com/60094794/137641271-6e85a2c7-f936-4d7b-afda-c8d0a2edfd65.png)


               
               
               
Characteristics :

•	Fastest Object detection algorithm
•	30FPS minimum image processing rate
•	MAP ~ 55-60% on COCO test dev


False Positives

1.	Statues vs Silhouettes :
Images that contain statues of a person figure are practically indistinguishable from an actual person ,from a computer’s point of view. Even if we are able train the model to differentiate a statue and an actual person, still a dark silhouette of a person and a bronze statue will look exactly the same. This case extends to sign boards with person figures too.
2.	Large two wheelers and small trucks:
The actual boundary of defining a car is tested in this problem. A four-wheeler within a definite size range and shape type can be broadly called a car. But, large touring bikes (eg : Honda Goldwing) and small pickup trucks often end up being classified as a car, due to their comparable resemblance with appearance of a car. 
3.	Picture in Picture:
This is a classic false positive case. Many images have images inside itself. Picture of a wall poster with paintings of cars and person figures most often go on to get  detected and classified.



Conclusion 

The following conclusions were inferred.
1.	YOLO algorithm works very well in the task of Object detection. 
2.	Relatively simpler two category problem makes the result even more accurate.
3.	Image augmentation was done by adding noise and rotation, making the model even more powerful.
4.	The task gives us two deep insights into defining a particular object under a category. 
a.	No clear and cent percent specific definition of a particular object can be define.
b.	False positives are inevitable even when categories have very little or no similarity.



