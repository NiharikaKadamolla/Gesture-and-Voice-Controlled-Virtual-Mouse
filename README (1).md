# 🤖 PROTON - AI Voice & Gesture Assistant

> A smart desktop assistant that understands your commands and controls gesture recognition in real-time.

---

## 📌 About the Project

**PROTON** is an intelligent desktop assistant built to interact with users via a chat interface and launch advanced modules like **Gesture Recognition** using voice/text commands.

---

## 🖥️ Demo Screenshots

### 1. Welcome & Greeting
PROTON greets the user based on the time of day and personalizes the conversation by asking for the user's name.

![Welcome Screen](screenshots/1.jpeg)

---

### 2. Time, Date & Commands
PROTON can tell you the **current time**, **today's date**, and responds gracefully when a command is outside its scope.

![Time and Date](screenshots/2.jpeg)

---

### 3. Launching Gesture Recognition
Simply type `proton launch gesture recognition` and PROTON launches the Gesture Controller module instantly.

![Launch Gesture](screenshots/3.jpeg)

---

## 🖐️ Gesture Controller Module

The Gesture Controller uses **computer vision** to detect and track hand landmarks in real-time using your webcam.

### Open Palm Detection
Detects a fully open hand with all 21 landmarks mapped.

![Open Palm](screenshots/4.jpeg)

---

### ✌️ Peace / Victory Sign
Recognizes the two-finger gesture with precision tracking.

![Peace Sign](screenshots/5.jpeg)

---

### ☝️ Pointing Gesture
Tracks single-finger pointing in any direction.

![Pointing](screenshots/6.jpeg)

---

### 👌 OK Sign
Detects the thumb-index finger pinch gesture.

![OK Sign](screenshots/7.jpeg)

---

### 🤘 Custom Gesture
Supports custom and complex hand configurations.

![Custom Gesture](screenshots/8.jpeg)

---

## ✨ Features

- 🕐 **Real-time Clock** — Ask PROTON for the current time
- 📅 **Date Awareness** — Get today's date instantly
- 👋 **Personalized Greeting** — PROTON remembers your name
- 🖐️ **Gesture Recognition** — Launch hand tracking with a single command
- 🤖 **21-Point Hand Landmark Detection** — Powered by MediaPipe / OpenCV
- 💬 **Chat Interface** — Clean and intuitive dark-themed UI

---

## 🛠️ Tech Stack

| Component        | Technology           |
|-----------------|----------------------|
| Desktop UI       | Tkinter / PyQt       |
| Gesture Tracking | MediaPipe + OpenCV   |
| Voice/Chat Logic | Python               |
| Hand Landmarks   | MediaPipe Hands      |

---

## 🚀 Getting Started

### Prerequisites
```bash
pip install opencv-python mediapipe
```

### Run the Assistant
```bash
python proton.py
```

### Run Gesture Controller Only
```bash
python gesture_controller.py
```

---

## 💬 Supported Commands

| Command                              | Action                        |
|--------------------------------------|-------------------------------|
| `proton what is the time`            | Returns current time          |
| `proton what is the date`            | Returns today's date          |
| `proton launch gesture recognition`  | Opens Gesture Controller      |
| `proton bye`                         | Closes the assistant          |

---

## 📁 Project Structure

```
PROTON/
│
├── proton.py                 # Main assistant script
├── gesture_controller.py     # Gesture recognition module
├── screenshots/              # Demo images
│   ├── 1.jpeg
│   ├── 2.jpeg
│   └── ...
└── README.md
```

---

## 👩‍💻 Developed By

**Jyoti**  
Built with ❤️ using Python, OpenCV & MediaPipe

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
