# UnPark – Parkinson’s Mobility Assistant

UnPark is an **AI-powered wearable device** designed to assist individuals with Parkinson’s Disease who experience **Freezing of Gait (FOG)**. Built for the **McMaster MedSprint Hackathon** (March 2025), this project bridges AI, wearable devices, and healthcare. The system detects freezing episodes using an **ankle-mounted accelerometer**, then provides real-time **vibrational cues** to help restore movement.

The solution combines hardware and software, featuring a **Raspberry Pi**, real-time Flask server, and an iOS companion app built with **Swift** and **Firebase** integration.

---
## 🔍 Explore

🎥 [Demo](https://www.youtube.com/watch?v=U3_JdsC1bM8&ab_channel=YashPanchal)      
📄 [Slideshow Presentation](Unpark-MedSprint_Pitch.pptx)

---

## 🧠 Key Features

- **Real-time Freeze Detection** using motion and derivative-based analysis with 95% accuracy
- **Instant Haptic Cueing** via vibration motor to unfreeze motion
- **SocketIO Integration** for real-time data transmission over Wi-Fi
- **iOS App Support** for episode logging, analytics, and clinical sharing
- **Customizable Sensitivity** to minimize false positives

---

## 🔧 Hardware Components

- Raspberry Pi 4
- MPU6050 Accelerometer Module
- Vibration Motor Module
- Battery Pack (portable use)
- Ankle Strap Mounting Assembly

---

## 🧪 Software Stack

- `Python`
- `Flask` + `Flask-SocketIO`
- `eventlet`
- `Swift` (iOS)
- `Firebase` (for data storage & sync)
- `mpu6050` Python sensor library

---

## ⚙️ How It Works

1. The ankle-mounted device reads 3D accelerometer data continuously.
2. An algorithm detects abnormal stillness patterns with low motion and derivative thresholds.
3. Upon a freeze detection, a haptic cue (vibration) is triggered.
4. Freeze events are sent in real-time via SocketIO to a local Flask server.
5. The iOS app logs events, visualizes trends, and enables clinical sharing.

---

## 🚀 Getting Started (Raspberry Pi Code)

### 1. Clone this repository:

```bash
git clone https://github.com/yashp1932/UnPark-Parkinsons-Mobility-Assistant.git
cd UnPark-Parkinsons-Mobility-Assistant
```
### 2. Install Python Dependencies
```bash
pip install -r requirements.txt
```
### 3. Run the Script
```bash
python freeze_detection.py
```
---
## 📱 iOS App
The iOS app (built in Swift) listens for freeze events from the Raspberry Pi over the same Wi-Fi network.

Features:
- Real-time freeze alerts
- Cloud-based logging via Firebase
- Trend graphs and analytics
- Shareable clinical reports

**Note: The app repo is hosted separately and available upon request.**

---
## 📈 Results
- Achieved **95% detection accuracy** in controlled testing
- Delivered **sub-100ms** response time for haptic feedback
- Enabled **real-time event syncing** between hardware and mobile app
- Successfully demonstrated at the McMaster MedSprint Hackathon 2025

---




