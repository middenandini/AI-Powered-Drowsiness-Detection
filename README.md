
# AI-Powered Real-Time Drowsiness Detection and Auto-Braking System

An intelligent automotive safety system that bridges computer vision software with an embedded hardware mechanism to prevent accidents caused by driver fatigue.

## ⚙️ How It Works (System Logic)
The working principle of the system is based on an integrated feedback loop between a computer vision-based software module and a hardware-controlled safety mechanism:

1. **Facial Tracking (Python):** The system processes video frames in real-time using OpenCV and Haar Cascade models to track facial landmarks, detect eye states, and monitor yawning frequency.
2. **Signal Transmission:** When prolonged eye closure or continuous yawning is detected, the Python script triggers an immediate local audio alert (`alarm.wav`) and initiates serial communication to send a trigger signal to a connected microcontroller.
3. **Automatic Braking (Arduino):** The hardware firmware processes this signal to engage a safety feedback loop, activating a hardware buzzer and driving a **DC motor** to simulate an automatic vehicle braking action.

## 🛠️ Tech Stack & Components
- **Software:** Python, OpenCV, Haar Cascade Face Detection, Serial Communication (PySerial)
- **Hardware:** Arduino Microcontroller, Camera Module, DC Motor (Braking Control), Buzzer Alarm

## 📂 Repository Contents
- `drowsiness_yawn.py` / `drowsiness_yawn with Voice.py` - Core applications handling real-time camera tracking and fatigue detection logic.
- `haarcascade_frontalface_default.xml` - Pre-trained model used for rapid facial feature detection.
- `Requirements.txt` - Project dependencies for easy local environment configuration.
- *(Note: Hardware-side Arduino .ino firmware files are hosted locally and will be synchronized shortly).*
