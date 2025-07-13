# 😴 Drowsiness Detection System

A real-time driver drowsiness detection system using Python, OpenCV, and Dlib. This project uses facial landmark detection and Eye Aspect Ratio (EAR) to monitor a driver’s alertness and trigger an alarm if signs of drowsiness are detected.

---

## 🚗 Project Overview

Drowsiness while driving is a major cause of road accidents. This project helps detect signs of fatigue in drivers and provides an alert to prevent potential mishaps.

It works by:
- Monitoring the driver’s eye movement through a webcam
- Calculating Eye Aspect Ratio (EAR)
- Triggering an alarm if the eyes remain closed for too long

---

## 🧠 Technologies Used

- Python
- OpenCV
- Dlib
- Scipy
- Imutils
- Pygame

---

## 🧪 How It Works

The system uses Dlib’s 68-point facial landmark detector to find the driver’s eyes. It then calculates the Eye Aspect Ratio (EAR):

```python
def eye_aspect_ratio(eye):
	A = distance.euclidean(eye[1], eye[5])
	B = distance.euclidean(eye[2], eye[4])
	C = distance.euclidean(eye[0], eye[3])
	return (A + B) / (2.0 * C)
