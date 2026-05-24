# 🖱️ Gesture Controlled Virtual Mouse

A real-time hand gesture recognition system that lets you control your computer's mouse using hand movements captured through a webcam — no physical mouse needed. Built with Python, OpenCV, and MediaPipe.

---

## 📌 Table of Contents
- [About the Project](#about-the-project)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Limitations](#limitations)
- [Future Improvements](#future-improvements)

---

## 📖 About the Project

This project uses computer vision and machine learning to detect hand landmarks in real time and map them to mouse actions. It also includes **Proton**, a voice assistant that can launch gesture recognition on command and perform tasks like opening browsers, searching Wikipedia, and more.

---

## ✨ Features

- 🖱️ Control mouse cursor using index finger movement
- 👆 Left click by pinching index finger and thumb
- 📜 Scroll using two fingers
- 🔊 Control system volume using pinch gesture
- 🎤 Voice assistant (Proton) with gesture launch support
- 💬 Chrome-based chat UI for Proton interaction

---

## 🛠️ Tech Stack

| Library | Purpose |
|---|---|
| OpenCV | Webcam capture and video display |
| MediaPipe | Real-time hand landmark detection |
| PyAutoGUI | Mouse movement and click control |
| pycaw | Windows system volume control |
| SpeechRecognition | Voice command recognition |
| pyttsx3 | Text-to-speech for Proton replies |
| eel | Chrome-based chat UI for Proton |
| wikipedia | Wikipedia search via Proton |
| pywin32 | Windows system-level integration |

---

## 🚀 Getting Started

### Prerequisites
- Windows 10/11
- Anaconda Distribution ([Download here](https://www.anaconda.com/products/individual))
- Google Chrome (required for Proton UI)
- Webcam and Microphone

### Installation

**Step 1 — Clone the repository:**
```bash
git clone https://github.com/xenon-19/Gesture-Controlled-Virtual-Mouse.git
```

**Step 2 — Create conda environment:**
```bash
conda create --name gest python=3.9
conda activate gest
```

**Step 3 — Install dependencies:**
```bash
pip install -r requirements.txt
```

**Step 4 — Install additional packages:**
```bash
conda install PyAudio
conda install pywin32
pip install opencv-contrib-python
pip install mediapipe==0.10.5
pip install pycaw
pip install protobuf
pip install wikipedia
pip install eel
pip install SpeechRecognition pyttsx3
```

**Step 5 — Navigate to src folder:**
```bash
cd Gesture-Controlled-Virtual-Mouse\src
```

---

## 🎮 Usage

### Running Gesture Recognition only:
1. Uncomment the last 2 lines in `Gesture_Controller.py`:
```python
gc1 = GestureController()
gc1.start()
```
2. Run:
```bash
python Gesture_Controller.py
```

### Running Proton Voice Assistant (with Gesture support):
1. Make sure the last 2 lines in `Gesture_Controller.py` are **commented out**
2. Run:
```bash
python Proton.py
```
3. Say **"Proton Launch Gesture Recognition"** to activate gesture control

### Quick Launch (Windows .bat file):
Create a file `run_proton.bat` on your Desktop:
```bat
@echo off
call C:\Users\YourName\anaconda3\Scripts\activate.bat gest
cd C:\Users\YourName\Gesture-Controlled-Virtual-Mouse\src
python Proton.py
```

---

## 🖐️ Gesture Controls

| Gesture | Action |
|---|---|
| Index finger up, move hand | Move cursor |
| Pinch index + thumb | Left click |
| Two fingers up/down | Scroll |
| Pinch spread/close | Volume control |

---

## 🎤 Proton Voice Commands

| Say | Action |
|---|---|
| "Proton Launch Gesture Recognition" | Starts gesture control |
| "Proton open Chrome" | Opens Chrome browser |
| "Proton what time is it" | Tells current time |
| "Proton search Wikipedia for ..." | Wikipedia search |
| "Proton exit" | Closes Proton |

---

## ⚠️ Limitations

- Windows only (due to pycaw and pywin32 dependencies)
- Sensitive to lighting conditions — works best in well-lit rooms
- Cursor may jitter due to hand tremors (no smoothing applied)
- Limited gesture vocabulary
- Arm fatigue during extended use
- Requires Google Chrome for Proton UI

---

## 🔮 Future Improvements

- Add smoothing algorithm (EMA) to reduce cursor jitter
- Train a custom gesture classifier for more gestures
- Port to Linux and macOS using cross-platform libraries
- Multi-hand support for richer interactions
- Visual feedback overlay for confirmed gestures

---

## 📋 Notes

- Use `mediapipe==0.10.5` specifically — newer versions removed the `mp.solutions` API this project depends on
- Always activate the `gest` conda environment before running
- Press **Enter** on the webcam window to close it cleanly

---

## 🙏 Acknowledgements

- [MediaPipe by Google](https://mediapipe.dev/)
- [OpenCV](https://opencv.org/)
- Original project by [xenon-19](https://github.com/xenon-19/Gesture-Controlled-Virtual-Mouse)
