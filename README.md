<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a0a1a,40:1a1a3e,70:2d2d6b,100:0a0a1a&height=200&section=header&text=AirMouse&fontSize=72&fontColor=ffffff&fontAlignY=38&fontStyle=bold&desc=Control%20Your%20Computer%20Without%20Touching%20It&descSize=17&descAlignY=62&descColor=818cf8" width="100%"/>

<br/>

<p align="center">
  <img src="https://img.shields.io/badge/MediaPipe-Hand%20Tracking-FF6B35?style=for-the-badge&logo=google&logoColor=white"/>
  <img src="https://img.shields.io/badge/OpenCV-Real--Time%20Vision-5C3317?style=for-the-badge&logo=opencv&logoColor=white"/>
  <img src="https://img.shields.io/badge/PyAutoGUI-Mouse%20Control-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Input-Webcam-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/Landmarks-21%20Hand%20Points-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Output-Real--Time%20Mouse%20Control-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Phases-2%20(Build%20%2B%20Tune)-purple?style=flat-square"/>
</p>

<br/>

> **AirMouse** is a touchless computer control system that uses MediaPipe's 21-point 3D hand landmark detection and OpenCV to track hand gestures through a standard webcam and translate them into real-time mouse movements, clicks, and scrolling — no hardware required beyond your camera.

</div>

---

## 🧠 How It Works

```
Webcam Frame
     │
     ▼
MediaPipe Hands
  Detects 21 3D landmarks per hand (wrist, knuckles, fingertips)
     │
     ▼
Landmark Analysis
  Index fingertip position  → cursor coordinates
  Thumb + index pinch       → left click
  Finger distance tracking  → scroll detection
     │
     ▼
NumPy Coordinate Smoothing
  Exponential averaging reduces jitter
  Maps hand frame → screen resolution
     │
     ▼
PyAutoGUI
  Moves cursor to mapped position
  Fires click / scroll events
```

---

## ✨ Features

| Gesture | Action |
|---|---|
| ☝️ Index finger move | Move cursor |
| 🤏 Thumb + index pinch | Left click |
| ✌️ Two-finger gesture | Scroll |
| 🖐️ Open palm | Pause tracking |

---

## ⚙️ Two-Phase Development

**Phase 1 — Core Implementation** (`Phase 1 (Code)/`)
Basic hand detection, landmark extraction, cursor mapping, and click detection. Gets the system working end to end.

**Phase 2 — Tuning** (`Phase 2 (Tuning)/`)
Smoothing algorithms, gesture sensitivity calibration, dead zone implementation to prevent cursor jitter, and multi-gesture refinement.

---

## 🚀 Quickstart

```bash
git clone https://github.com/mahmedmajeedai/AI-virtual-mouse-using-hand-gesture.git
cd AI-virtual-mouse-using-hand-gesture
pip install opencv-python mediapipe pyautogui numpy
python "Phase 2 (Tuning)/main.py"
```

Allow webcam access when prompted. Hold your hand in view of the camera and start controlling.

---

## 🛠️ Tech Stack

| Library | Role |
|---|---|
| `mediapipe` | 21-point 3D hand landmark detection in real time |
| `opencv-python` | Webcam capture, frame display, visual overlay |
| `pyautogui` | Programmatic mouse movement and click simulation |
| `numpy` | Coordinate smoothing and screen space mapping |

---

## 🌍 Applications

| Domain | Use Case |
|---|---|
| 🏥 **Healthcare** | Touchless interaction with shared clinical devices |
| ♿ **Accessibility** | Alternative input for users with mobility limitations |
| 🎤 **Presentations** | Slide control without a physical clicker |
| 🧪 **HCI Research** | Gesture-based interface experimentation |

---

## ⚠️ Requirements

- Python 3.7 or higher
- A working webcam (built-in or USB)
- Adequate lighting for hand detection

---

<div align="center">

**Built by [Muhammad Ahmed Majeed](https://github.com/mahmedmajeedai)**

*Touchless human-computer interaction via computer vision*

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2d2d6b,50:1a1a3e,100:0a0a1a&height=80&section=footer" width="100%"/>

</div>
