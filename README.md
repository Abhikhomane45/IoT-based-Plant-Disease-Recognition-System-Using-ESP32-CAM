# 🌱 IoT-Based Plant Disease Recognition System Using ESP32-CAM

![Project Banner](https://img.shields.io/badge/IoT-Smart%20Agriculture-green) ![Language](https://img.shields.io/badge/Language-C%2B%2B%20%26%20PHP-blue) ![Python](https://img.shields.io/badge/Python-TensorFlow-yellow)

---

## 📝 Project Overview

The **IoT-Based Plant Disease Recognition System** is designed to help **farmers, gardeners, and researchers** detect plant diseases early. It combines **IoT hardware**, **web technologies**, and **AI-based image analysis** to automate plant health monitoring.

**Core Components**:

- **ESP32-CAM**: Captures real-time images of plant leaves.  
- **XAMPP Server (PHP/Apache)**: Stores images and hosts a web dashboard.  
- **Python AI Model (TensorFlow/Keras)**: Classifies plant diseases automatically.  
- **Web Dashboard**: Displays uploaded images and disease results interactively.

---

## ⚡ Features

- Real-time leaf image capture with ESP32-CAM  
- Automatic image upload to local server using PHP  
- AI-based disease recognition via Python models  
- Interactive dashboard for monitoring plant health  
- Low-cost, scalable, and easy to deploy  

---

## 🏗️ System Architecture

### Components:

| Component        | Function |
|-----------------|---------|
| ESP32-CAM        | Captures high-resolution images of plant leaves |
| OV2640 Camera    | 2MP camera integrated with ESP32-CAM |
| XAMPP Server     | Receives images and hosts PHP web interface |
| Python AI Model  | Predicts disease type using ML models |
| Web Dashboard    | Displays images and disease analysis |

### Workflow:

1. ESP32-CAM captures leaf images.  
2. Images uploaded to `upload.php` on XAMPP server.  
3. Python script `analyze.py` predicts plant disease.  
4. Dashboard `index.php` displays results.

---

## 💻 Hardware Requirements

| Component | Description |
|-----------|-------------|
| ESP32-CAM | Wi-Fi + Bluetooth microcontroller with OV2640 camera |
| OV2640 Camera | 2MP camera for capturing leaf images |
| FTDI Programmer | USB-to-Serial interface for programming ESP32-CAM |
| I2C 16x2 LCD Display | Optional display for status messages |
| Power Supply | 5V, 2A USB or battery supply |

---

## 🛠️ Software Requirements

- Arduino IDE (for ESP32-CAM programming)  
- Python 3.x  
- TensorFlow / TensorFlow Lite  
- OpenCV (for image preprocessing)  
- Arduino Libraries:
  - `ESPAsyncWebServer`
  - `WiFi.h`
  - `Wire.h` and `LiquidCrystal_I2C.h` (for LCD display)

---

## ⚙️ Installation & Setup

### 1️⃣ Hardware Setup
1. Connect ESP32-CAM to FTDI programmer:
   - TX → ESP32 RX (U0R, GPIO3)
   - RX → ESP32 TX (U0T, GPIO1)
   - GND → GND
   - VCC → 5V
   - IO0 → GND (for programming mode)
2. Connect I2C LCD (optional):
   - SDA → GPIO15
   - SCL → GPIO14
   - VCC → 5V
   - GND → GND
3. Power the system with 5V supply.

### 2️⃣ XAMPP Server Setup
1. Install [XAMPP](https://www.apachefriends.org/index.html) and start **Apache**.  
2. Place project folder inside `htdocs`.  
3. Create `uploads/` folder with write permissions for storing images.

### 3️⃣ ESP32-CAM Software Setup
1. Install ESP32 board in Arduino IDE.  
2. Install required libraries (`ESPAsyncWebServer`, `WiFi`, `LiquidCrystal_I2C`).  
3. Configure Wi-Fi credentials and server URL in ESP32-CAM code:

##cpp
const char* ssid = "YourWiFiSSID";
const char* password = "YourWiFiPassword";
const char* serverUrl = "http://<Your-PC-IP>/esp32-cam/upload.php";



## 👥 Project Team
- **Abhijeet Khomane** – Hardware & Software Integration  
- **Shubham Gavade** – Software & AI Implementation  
- **Purva Patil** – Documentation & Testing  

---

## 📌 Acknowledgements
We sincerely thank our project guide, for their valuable guidance and support throughout this project. We also extend our gratitude to the Department of Electronics & Computer Engineering, **P.E.S’s Modern College of Engineering**, for providing the resources and environment necessary to complete this work. Special thanks to the open-source communities, online tutorials, and research papers that assisted in understanding IoT, ESP32-CAM, and machine learning concepts.

---

## 🌟 Notes
- This project is intended for **educational and research purposes**.  
- Proper safety should be observed while handling electronic components.  
- Contributions, suggestions, and improvements are welcome.

---

## 📫 Contact
- **Email:** abhikhomane123@gmail.com  
- **LinkedIn:** [https://www.linkedin.com/in/abhijeet-khomane-08a202275](https://www.linkedin.com/in/abhijeet-khomane-08a202275)  
- **GitHub:** [https://github.com/Abhikhomane45](https://github.com/Abhikhomane45)

---

© 2025 IoT-Based Plant Disease Recognition System Team. All rights reserved.

