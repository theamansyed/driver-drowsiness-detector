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

def eye_aspect_ratio(eye):
	A = distance.euclidean(eye[1], eye[5])
	B = distance.euclidean(eye[2], eye[4])
	C = distance.euclidean(eye[0], eye[3])
	return (A + B) / (2.0 * C)

- If EAR < 0.25 for more than 20 consecutive frames, it assumes the driver is drowsy.
- It plays a warning alarm using pygame.mixer.

---

## 🔊 Alarm Feature

The alarm is triggered using music.wav and pygame.mixer when drowsiness is detected.  
It helps wake the driver instantly through sound and visual warnings.

---

## 📁 Project Structure

drowsiness-detection/
├── Drowsiness_Detection.py  
├── music.wav  
├── models/  
│   └── shape_predictor_68_face_landmarks.dat (⚠️ Download separately)  
├── assets/  
│   ├── eye1.jpg  
│   ├── eye2.png  
│   └── eye3.jpg  
├── README.md  

---

## 📥 Required Model File

⚠️ IMPORTANT: The model file is NOT included in this repository because it exceeds GitHub’s file size limit.

👉 Download the model from Google Drive here:  
https://drive.google.com/file/d/1zks9BYF0uJe-15oi-JJjLSLVdsBw9JAq/view?usp=sharing

After downloading, place the file inside the following folder:
models/shape_predictor_68_face_landmarks.dat

---

## 🛠️ How to Run

Step 1: Install Dependencies
pip install opencv-python dlib scipy pygame imutils

Step 2: Run the Script
python Drowsiness_Detection.py

Make sure your webcam is connected.

---

## 🎮 Controls

- Press Q to quit the application

---

## 📈 Future Improvements

- Add GUI interface with Tkinter or PyQt
- Deploy on Raspberry Pi or embedded systems
- Mobile version
- Emergency contact alert integration

---

## 👨‍💻 Author

Syed Mahammad Aman
Solo-developed and presented at a college expo.

---

## ⭐ Support

If this helped you, leave a ⭐ on the repo!
