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
## 🛒 Bill of Materials (BOM) — Discrete Circuitry & Fabrication

| Item | Component & Spec | Qty | Cost | Engineering Purpose |
| :---: | :--- | :---: | :---: | :--- |
| 1 | **Raspberry Pi 4B (4GB RAM)** | 1 | $55 | Primary embedded computing & vision host |
| 2 | **SanDisk 64GB Extreme A2 MicroSD Card** | 1 | $14 | Linux OS, OpenCV binaries, and model weights |
| 3 | **Custom Carrier PCB Fabrication (JLCPCB)** | 5 pcs | $16 | 2-layer custom motherboard + SMD solder stencil |
| 4 | **PCA9685PW 16-Ch PWM Driver IC + Passives** | 1 | $6 | Discrete I2C servo controller chip & decoupling |
| 5 | **MP1584EN DC-DC Buck Step-Down Circuit** | 1 set | $7 | IC, 4.7µH power inductor, Schottky diode & caps |
| 6 | **MAX98357A I2S DAC Audio Amp IC + Filters** | 1 | $5 | Discrete I2S Class-D amplifier IC & ferrite beads |
| 7 | **INMP441 Omnidirectional MEMS Mic IC** | 1 | $4 | Surface-mount digital microphone transducer |
| 8 | **Power Filter Array (1000µF Caps, TVS Diodes, MOSFETs)** | 1 set | $6 | Peak servo surge suppression & brownout protection |
| 9 | **SMD Passives & Connector Pack (0805, Headers, JST)** | 1 set | $8 | Resistor/capacitor reels, screw terminals, headers |
| 10 | **MG90S Metal-Gear Micro Servos** | 2 | $8 | Raw 2-DOF pan/tilt actuators |
| 11 | **Raspberry Pi Camera Module v2 (IMX219 8MP)** | 1 | $18 | Bare camera sensor & FPC ribbon |
| 12 | **0.96" Bare I2C OLED Glass Panels (SSD1306)** | 2 | $10 | Bare display panels for expressive digital eyes |
| 13 | **4Ω 3W 28mm Slim Audio Speaker Transducer** | 1 | $4 | Bare speaker driver for voice feedback |
| 14 | **5V 4010 DC Brushless Fan & Aluminium Heatsinks** | 1 | $5 | Active thermal management package |
| 15 | **5V 4A Regulated USB-C Power Adapter** | 1 | $13 | Continuous power delivery for system + servos |
| 16 | **Mechanical Hardware (PLA Filament, M2/M3 Heat-Set Inserts)** | 1 set | $15 | Custom 3D chassis, joints & threaded brass inserts |
| **Σ** | **Total Estimated Budget** | — | **$194** |  |
---


