# 😴 Drowsiness Detection System

A real-time driver drowsiness detection system using Python, OpenCV, and Dlib. This project detects when a driver is becoming drowsy by analyzing eye movements using Eye Aspect Ratio (EAR), and plays an alert if drowsiness is detected.

---

## 🚗 Project Overview

Drowsiness while driving is a major cause of road accidents. This project helps prevent such accidents by:

- Monitoring the driver’s eye movement through a webcam
- Using facial landmarks to detect eye openness
- Calculating Eye Aspect Ratio (EAR)
- Playing a loud alarm if the eyes remain closed for too long

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

The system uses Dlib’s 68-point facial landmark predictor to locate both eyes. Then it calculates the Eye Aspect Ratio (EAR) as follows:

```python
def eye_aspect_ratio(eye):
	A = distance.euclidean(eye[1], eye[5])
	B = distance.euclidean(eye[2], eye[4])
	C = distance.euclidean(eye[0], eye[3])
	return (A + B) / (2.0 * C)
