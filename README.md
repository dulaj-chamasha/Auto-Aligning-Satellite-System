---

# 📡 Auto-Aligning Satellite System

![Platform](https://img.shields.io/badge/platform-Arduino%20UNO-blue?logo=arduino)
![Frequency](https://img.shields.io/badge/frequency-Ku%20Band%20(12--18%20GHz)-green)
![Communication](https://img.shields.io/badge/Signal-RF%20Detection%20%7C%20LNB-purple)
![Control](https://img.shields.io/badge/Control-Servo%20Motors%20%7C%20Dual%20Axis-orange)
![License](https://img.shields.io/badge/license-MIT-yellow.svg)

---

An **intelligent satellite dish alignment system** designed to eliminate manual positioning adjustments in satellite communication systems. 
Powered by **Arduino UNO** with automated RF signal strength detection and servo-controlled mechanical positioning.

---

## 📖 Overview

The **Auto-Aligning Satellite System** addresses critical challenges in satellite communication by:
* 🎯 **Automatically positioning dish antennas** for optimal signal reception without technician intervention
* 📶 **Detecting maximum RF signal strength** through intelligent circuit design
* 🔄 **Providing dual-axis control** for precise azimuth and elevation adjustments  
* ⚡ **Reducing service interruptions** and maintenance costs for satellite TV providers
* 🛰️ **Supporting Ku-band satellite communications** (12-18 GHz downconverted to 950-2150 MHz)

---

## 🛠️ Tech Stack

### 🔧 Input Components
* **RF Signal Detection Circuit** with BC548 transistors and 1N4007 diodes
* **LNB (Low Noise Block)** for signal downconversion and amplification
* **LDR Sensors** for positioning feedback control
* **Coaxial RG6U cables** (75Ω) for RF signal transmission

### 💡 Output & Control
* 🔴 **Status LEDs** (Red: Azimuth, Green: Elevation) for visual feedback
* ⚙️ **SG90 Servo Motors** for precise antenna positioning
* 📊 **Voltage measurement** proportional to signal strength
* 🎛️ **Arduino-based control system** for automation logic

### 🛰️ RF Processing
* 📡 **Ku-band reception** (12-18 GHz satellite transmission)
* 📻 **IF processing** (950-2150 MHz post-LNB downconversion)  
* 🔍 **Signal strength analysis** with threshold-based detection

---

## 🚀 Features

* 🎯 **Automated satellite tracking** eliminates manual dish alignment
* 📶 **Real-time RF signal monitoring** with precision voltage measurement
* 🔄 **Dual-axis servo control** for azimuth (0-360°) and elevation positioning
* ⚡ **Intelligent feedback system** using LED-LDR pairs for position locking
* 🛰️ **Geostationary satellite compatibility** with tested Intelsat 12 alignment
* 🔧 **Scalable design** supporting various dish antenna sizes

---

## 📂 Repository Structure

```bash
├── hardware/           # Circuit schematics and PCB designs
│   ├── rf_detector/    # Signal strength detection circuit
│   └── control_board/  # Arduino control system layout
├── firmware/           # Arduino IDE code and libraries
│   ├── main.ino       # Primary control algorithm
│   └── servo_control/ # Motor positioning functions
├── mechanical/         # CAD files and gear system designs
│   ├── solidworks/    # 3D models for antenna mounting
│   └── assembly/      # Mechanical component specifications
├── docs/              # Technical documentation and test results
│   ├── methodology/   # System design approach
│   └── validation/    # Performance testing data
└── README.md          # Project overview

```

## 📸 System Architecture

### Signal Processing Pipeline
```
Satellite (12-18 GHz) → Dish Antenna → LNB → RF Detection Circuit → Arduino Control → Servo Positioning
```

### Control Algorithm Flow
```
Initialize → Measure Signal → Threshold Check → Activate LEDs → LDR Feedback → Stop/Continue → Loop
```

---

## ⚙️ Technical Specifications

| Parameter | Value | Notes |
|-----------|--------|-------|
| **Input Frequency** | 12-18 GHz | Ku-band satellite transmission |
| **Processing Frequency** | 950-2150 MHz | Post-LNB downconversion |
| **Signal Threshold** | 2.2V (600 ADC) | Configurable trigger level |
| **Positioning Accuracy** | ±2° | Servo-controlled precision |
| **Response Time** | <2 seconds | Position adjustment speed |
| **Power Requirements** | 12V DC @ 2A | Maximum system consumption |

---

## 🧪 Testing & Validation

### Laboratory Results
* ✅ **Circuit functionality verified** using signal generators up to 25 MHz
* ✅ **Servo positioning accuracy** validated through mechanical testing
* ✅ **Control algorithm performance** measured with prototype system

### Field Testing
* 🛰️ **Successfully aligned with Intelsat 12** satellite
* 📶 **Maximum voltage differential detected** at optimal positioning (LOS)
* 🔄 **Automatic repositioning demonstrated** with environmental changes

---

## 🔧 Hardware Implementation

### RF Detection Circuit
* **Amplification**: BC548 transistor-based RF amplifier stage
* **Rectification**: 1N4007 diodes for AC-to-DC signal conversion
* **Filtering**: Capacitive noise reduction for clean signal measurement
* **Output**: Voltage proportional to received RF power

### Mechanical System  
* **Azimuth Control**: 360° horizontal rotation capability
* **Elevation Control**: Vertical positioning for satellite tracking
* **Gear Reduction**: High-precision positioning through mechanical advantage
* **Load Capacity**: Designed for standard residential dish antennas

---
## 🎯 Applications

* 🏠 **Residential Satellite TV** - Automatic alignment maintenance
* 🏢 **Commercial Systems** - Reduced service call requirements  
* 🗻 **Remote Installations** - Unmanned satellite communication stations
* 🚐 **Mobile Platforms** - RV and marine satellite systems
* 📡 **Telecommunications Infrastructure** - Network reliability improvement
  
---

## 📌 Future Enhancements

* 🏭 **Industrial motor integration** (KOTTO-36501, TSUKA TG-05) for full-scale deployment
* 🔌 **Optocoupler isolation** for enhanced signal integrity and noise reduction  
* 🌦️ **Weather compensation algorithms** for atmospheric attenuation correction
* 🌐 **IoT connectivity** for remote monitoring and diagnostic capabilities
* 🛰️ **Multi-satellite support** for dynamic satellite constellation tracking
* 📱 **Mobile app integration** for system configuration and status monitoring

---

## 📜 License

This project is licensed under the **MIT License** – open for educational and commercial use with proper attribution.

---

