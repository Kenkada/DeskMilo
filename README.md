# 🤖 DeskMilo

> **Your expressive desktop AI companion that gives you eye contact, talks back, and helps you lock in.**

<p align="center">
  <img src="Assets/1.jpeg" alt="DeskMilo Hero Banner" width="450" style="border-radius: 10px;" />
</p>

<p align="center">
  <a href="https://www.python.org/downloads/"><img src="https://img.shields.io/badge/python-3.9+-blue.svg" alt="Python 3.9+"></a>
  <a href="#-bill-of-materials-bom"><img src="https://img.shields.io/badge/hardware-2--DOF%20Pan--Tilt-orange.svg" alt="Hardware: 2-DOF"></a>
</p>

---

## 🚀 What's New

### 🛠️ In v0.1 Prototype Release
- [ ] **Initial 2-DOF Rig Assembly:** Built pan-tilt head mechanism for smooth tracking.
- [ ] **Face Tracking V1:** Integrated OpenCV Haar cascade with deadzone smoothing to stop servo jitter.
- [ ] **Active Thermal Circuit:** Added transistor-switched 5V fan to keep the SBC chill during video stream processing.

---

## 📸 Media & Inspiration

> 🎬 **[Watch Inspiration Reel on Instagram](https://www.instagram.com/reel/Dchn35SNEEn/?stkn=cjRoMHJqa2syYXoy)**

| Front View | Side / Pan-Tilt Mechanism |
| :---: | :---: |
| <img src="Assets/2.jpeg" alt="Front View" width="260" /> | <img src="Assets/3.jpeg" alt="Mechanism" width="260" /> |

---

## ✨ Features

- 👀 **Active 2-DOF Face Tracking:** Uses computer vision to physically pan (left/right) and tilt (up/down) to track your face.
- 🗣️ **Voice & Audio Output:** Integrated speaker allows DeskMilo to greet you, speak task reminders, and play audio feedback.
- ❄️ **Active Thermal Cooling:** Monitored cooling fan ensures the onboard processor stays cool during continuous vision processing.
- 🌐 **Internet-Connected:** Ready to integrate with LLM APIs (OpenAI, Gemini, Ollama) for smart desktop assistance.

---

## 🛒 Bill of Materials (BOM)

| Item | Component | Qty | Approx Cost | Notes / Link |
| :---: | :--- | :---: | :---: | :--- |
| 1 | **Raspberry Pi 4B / Zero 2 W** | 1 | ~$35 - $55 | Brain of the robot |
| 2 | **MG90S / SG90 Micro Servos** | 2 | ~$5 | Pan (X-axis) and Tilt (Y-axis) |
| 3 | **2-DOF Pan-Tilt Bracket Kit** | 1 | ~$3 | Holds camera & tilt servo |
| 4 | **USB Web Camera or Pi Camera v2** | 1 | ~$10 - $15 | Face tracking & visual input |
| 5 | **5V 4010 DC Cooling Fan** | 1 | ~$2 | Keeps CPU cool |
| 6 | **Mini USB Speaker / I2S MAX98357A**| 1 | ~$5 - $8 | Audio & voice output |
| 7 | **2N2222 Transistor / MOSFET** | 1 | ~$0.50 | Fan switching circuit |
| 8 | **5V 3A Power Supply (USB-C)** | 1 | ~$8 | Stable power for Pi & servos |
| 9 | **3D Printed Enclosure & Base** | 1 set | ~$5 (filament) | [STL Files in /cad](./cad/) |

---

## 🔌 Hardware Wiring & Pinout

```text
[Raspberry Pi / Controller]
  ├── GPIO 18 (PWM)  ──>  Pan Servo Signal (Orange/Yellow wire)
  ├── GPIO 19 (PWM)  ──>  Tilt Servo Signal (Orange/Yellow wire)
  ├── GPIO 21        ──>  Fan Control via Transistor (Base)
  ├── USB Port 1     ──>  Camera
  ├── USB Port 2     ──>  Speaker
  └── 5V & GND       ──>  Power Rails (Use external 5V rail for servos if jitter occurs)
