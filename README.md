# Real-Time Object Detection and Classification Using YOLOv8 and OpenCV
This project implements real-time object detection and classification using the YOLOv8 model with OpenCV. By leveraging a webcam or video feed, the system identifies and tracks various objects such as people, vehicles, and everyday items from the COCO dataset. Bounding boxes and confidence scores are dynamically displayed around detected objects, offering a robust and efficient solution for real-time visual recognition applications.

## Table of Contents
- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Dataset](#dataset)
- [Computer Vision](#computer-vision)
  - [Library Imports](#library-imports)
  - [Video Capture Initialization](#video-capture-initialization)
  - [Model Loading](#model-loading)
  - [Class Name Definition](#class-name-definition)
  - [Real-Time Video Processing Loop](#real-time-video-processing-loop)
  - [Detection Result Processing](#detection-result-processing)
  - [Bounding Box Drawing and Annotation](#bounding-box-drawing-and-annotation)
  - [Frame Display](#frame-display)

## Project Overview
The Real-Time Object Detection and Classification Using YOLOv8 and OpenCV project aims to develop an efficient and responsive system capable of detecting and classifying objects in real-time. The project utilizes the YOLOv8 (You Only Look Once) model, known for its speed and accuracy in object detection, alongside OpenCV for real-time video processing.

The system captures live video feed from a webcam or a pre-recorded video, processes each frame using the YOLOv8 model, and identifies objects such as people, vehicles, and various items from the COCO dataset. The detected objects are highlighted with bounding boxes and labeled with their corresponding class names and confidence scores, giving users visual feedback on the detection results.

This project can be adapted for various use cases, including security monitoring, traffic management, and automated inventory systems, where real-time object detection and classification are crucial. The design is modular, allowing for easy integration with other machine learning models or hardware systems, and offers a scalable solution for real-time visual recognition tasks.

## Problem Statement
In many industries, the need for real-time object detection and classification is critical for tasks such as surveillance, traffic monitoring, autonomous vehicles, and inventory management. Traditional methods often struggle to meet the required speed and accuracy for processing live video feeds while identifying multiple objects simultaneously. This limitation can lead to delayed responses, missed detections, or inefficient resource usage.

There is a demand for a solution that can quickly and accurately detect and classify objects in dynamic environments without sacrificing performance. The challenge lies in developing a system that can process live video streams in real-time, recognize various objects across different categories, and provide reliable feedback for informed decision-making in high-stakes applications.

## Dataset
The dataset used for this project is based on the COCO (Common Objects in Context) dataset, a widely used benchmark for object detection, segmentation, and captioning tasks. It contains over 80 object categories that are common in everyday life, such as people, vehicles, animals, and household items. The dataset provides labeled images with annotated bounding boxes for each object, allowing machine learning models to learn both the location and the class of each object within an image.

In this project, the YOLOv8 model has been pre-trained on the COCO dataset, enabling it to recognize and classify objects from 80 distinct categories in real-time. The dataset includes various types of objects like:

- People: person, backpack, handbag, suitcase
- Vehicles: bicycle, car, bus, truck, motorbike, train
- Animals: dog, cat, bird, horse, sheep, cow
- Household items: chair, sofa, dining table, laptop, book, clock
- Others: sports ball, skateboard, tennis racket, bottle, cup

The diverse set of categories allows the model to perform well in a variety of real-world environments, making it suitable for applications such as video surveillance, autonomous driving, and robotics. While the model is pre-trained, the system can be further fine-tuned on custom datasets for specialized object detection tasks.

## Computer Vision
### Library Imports
The code begins by importing the necessary libraries:
- **Ultralytics YOLO** for object detection.
- **OpenCV** for image and video processing.
- **cvzone** for enhanced drawing capabilities.
- **Math** for basic mathematical operations.
### Video Capture Initialization
The webcam is accessed using cv2.VideoCapture(0), and the resolution is set to 1280x720 pixels, preparing the system for live video processing.

### Model Loading
The YOLOv8 model is loaded from a specified path using pre-trained weights, enabling it to detect objects in video frames.

### Class Name Definition
A list of class names is defined, corresponding to the categories that the YOLO model can detect, such as people, vehicles, animals, and household items.

### Real-Time Video Processing Loop
An infinite loop is initiated to continuously read frames from the video feed. Each frame is processed by the YOLO model to perform object detection.

### Detection Result Processing
For each frame, the code retrieves bounding box coordinates and other detection information. It then calculates the dimensions of the bounding boxes and iterates through detected objects.

### Bounding Box Drawing and Annotation
Bounding boxes are drawn around detected objects using cvzone.cornerRect(). The code also calculates confidence scores for each detection and displays the class name along with the confidence score on the frame.

### Frame Display
Finally, the processed frame is displayed in a window using cv2.imshow(), and the program waits for a brief moment to allow for frame updates, keeping the display responsive.

This structured flow enables the system to effectively detect and classify objects in real-time, making it suitable for various applications such as surveillance, traffic monitoring, and autonomous systems.






