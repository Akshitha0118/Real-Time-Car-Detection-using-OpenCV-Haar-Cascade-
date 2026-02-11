# 🚗 Real-Time Car Detection using OpenCV (Haar Cascade)
## 📌 Project Overview

This project implements real-time car detection from video using OpenCV and a Haar Cascade Classifier.

The system processes each frame of a video, detects cars, and draws bounding boxes around them.

## It demonstrates the fundamentals of:

Computer Vision

Object Detection

Haar Cascade Classifiers

Video Processing with OpenCV

## 🎯 Features

✅ Real-time car detection
✅ Haar Cascade-based object detection
✅ Frame-by-frame video processing
✅ Bounding box visualization
✅ Error handling for file paths

## 🛠️ Technologies Used

Python 🐍

OpenCV

Haar Cascade XML Classifier

Video Processing

## 📂 Project Structure
Car-Detection-OpenCV/
│
├── haarcascade_car.xml
├── car_detection.py
├── sample_video.mp4
└── README.md

## ⚙️ How It Works
### 1️⃣ Import Required Libraries
import cv2
import time

### 2️⃣ Load Haar Cascade Classifier
car_classifier = cv2.CascadeClassifier(car_classifier_path)


Loads the pre-trained Haar cascade model

Checks if the file path is correct

### 3️⃣ Load Video File
cap = cv2.VideoCapture(video_path)


Opens the video file

Validates if the video is successfully loaded

### 4️⃣ Frame Processing Loop

For every frame:

Convert frame to grayscale

Detect cars using detectMultiScale()

Draw bounding boxes

Display the processed frame

cars = car_classifier.detectMultiScale(
    gray,
    scaleFactor=1.1,
    minNeighbors=3,
    minSize=(30, 30)
)

### 5️⃣ Exit Condition

Press Enter key to stop detection:

if cv2.waitKey(1) == 13:

## 🧠 Key Concepts Used
🔹 Haar Cascade Classifier

A machine learning-based approach where:

Positive images (cars) and negative images are used

Features are extracted

A cascade function is trained to detect objects

🔹 Grayscale Conversion

Improves detection speed and performance:

gray = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)

## 🚀 How to Run the Project
Step 1: Install Dependencies
pip install opencv-python

Step 2: Download Haar Cascade XML

Make sure you have:

haarcascade_car.xml

Step 3: Update File Paths

Update:

car_classifier_path = "your_path/haarcascade_car.xml"
video_path = "your_path/video.mp4"

Step 4: Run the Script
python car_detection.py

## 📊 Detection Parameters Explained
Parameter	Purpose
scaleFactor	Controls image scaling
minNeighbors	Reduces false positives
minSize	Minimum object size
## ⚠️ Challenges Faced

Incorrect file paths

Haar cascade loading errors

Frame capture issues

False positives in detection

Video playback speed issues
