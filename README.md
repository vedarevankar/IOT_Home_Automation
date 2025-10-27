# 🏠 SmartHome IoT Suite

<div align="center">

![Project Status](https://img.shields.io/badge/Status-Complete-success?style=for-the-badge)
![Build](https://img.shields.io/badge/Build-Passing-brightgreen?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Arduino-00979D?style=for-the-badge&logo=arduino&logoColor=white)
![IoT](https://img.shields.io/badge/IoT-Blynk-23C48E?style=for-the-badge&logo=blynk&logoColor=white)

**A comprehensive IoT-powered home automation system with intelligent sensors, real-time monitoring, and seamless control.**

[Features](#-features) • [Hardware](#-hardware-requirements) • [Installation](#-installation) • [Usage](#-usage) • [Dashboard](#-dashboard)

</div>

---

## 🌟 Features

### 🌙 **Smart Garden Lights**
- **Automated illumination** using LDR (Light Dependent Resistor) sensor
- Intelligent dusk-to-dawn operation
- Energy-efficient lighting control
- Real-time light intensity monitoring

### 🌡️ **Temperature Management**
- Automated climate control system
- Real-time temperature sensing and display
- Configurable threshold-based conditioning
- Live temperature graphs and analytics

### 💧 **Serial Tank Automation**
- Intelligent water level monitoring
- Automated pump control with safety protocols
- Customizable fill/drain sequences
- Status indicators and alerts

### 📊 **Unified Dashboard**
- Beautiful, intuitive Blynk interface
- Real-time sensor data visualization
- Remote control from anywhere
- Historical data logging
- Push notifications for critical events

---

## 🛠️ Hardware Requirements

| Component | Purpose |
|-----------|---------|
| **Arduino Uno** | Main microcontroller |
| **LDR Sensor** | Light intensity detection |
| **Temperature Sensor** | Environmental monitoring (DHT11/DHT22) |
| **Relay Module** | Device switching control |
| **Water Level Sensor** | Tank monitoring |
| **ESP8266/ESP32** | WiFi connectivity (if using Arduino Uno) |
| **LED Indicators** | Status visualization |
| **Jumper Wires** | Circuit connections |

---

## 💻 Software Stack

```
┌─────────────────────────────────────┐
│     Arduino IDE                     │
│  - Core programming environment     │
│  - Libraries: Blynk, Sensors        │
└─────────────────────────────────────┘
              │
              ▼
┌─────────────────────────────────────┐
│   PicsimLab Simulator               │
│  - Hardware simulation              │
│  - Circuit testing & validation     │
└─────────────────────────────────────┘
              │
              ▼
┌─────────────────────────────────────┐
│   Null Emulator                     │
│  - Bridge between IDE & simulator   │
│  - Serial communication             │
└─────────────────────────────────────┘
              │
              ▼
┌─────────────────────────────────────┐
│   Blynk IoT Platform                │
│  - Cloud dashboard                  │
│  - Mobile app control               │
│  - Data analytics                   │
└─────────────────────────────────────┘
```

---

## 📦 Installation

### 1️⃣ **Clone the Repository**
```bash
git clone https://github.com/yourusername/SmartHome-IoT-Suite.git
cd SmartHome-IoT-Suite
```

### 2️⃣ **Install Arduino IDE**
- Download from [arduino.cc](https://www.arduino.cc/en/software)
- Install required libraries:
  - Blynk Library
  - DHT Sensor Library
  - ESP8266WiFi (if applicable)

### 3️⃣ **Setup Blynk**
- Install Blynk app on your smartphone
- Create a new project
- Note your **Auth Token**
- Configure widgets as per dashboard setup

### 4️⃣ **Configure Simulation Environment**
- Install [PicsimLab](https://github.com/lcgamboa/picsimlab)
- Install Null Emulator for serial bridging
- Connect simulator to Arduino IDE

### 5️⃣ **Upload Code**
- Update WiFi credentials and Blynk Auth Token in the code
- Select correct board (Arduino Uno)
- Upload the sketch

---

## 🚀 Usage

### **Quick Start**

1. **Power on** the Arduino system
2. **Connect** to WiFi (watch for connection LED indicator)
3. **Open** Blynk app on your phone
4. **Monitor** real-time sensor data on the dashboard
5. **Control** devices remotely with a tap

### **System Modes**

| Mode | Description | Trigger |
|------|-------------|---------|
| **AUTO** | Fully automated based on sensors | Default |
| **MANUAL** | User-controlled via dashboard | Toggle switch |
| **SCHEDULE** | Time-based automation | Set in Blynk |

---

## 📱 Dashboard

The Blynk dashboard provides:

- 📊 **Real-time Graphs**: Temperature trends, light levels
- 🎛️ **Control Switches**: Manual override for all devices
- 📈 **Analytics**: Historical data and patterns
- 🔔 **Notifications**: Alerts for temperature thresholds, tank levels
- 📍 **Status Indicators**: Connection status, sensor health

---

## 🎯 Project Components

### Garden Lights Module
```cpp
// Automated light control based on ambient brightness
if (lightLevel < THRESHOLD) {
  digitalWrite(GARDEN_LIGHTS, HIGH);
}
```

### Temperature Conditioning
```cpp
// Climate control based on temperature readings
if (temperature > MAX_TEMP) {
  digitalWrite(COOLING_SYSTEM, HIGH);
}
```

### Tank Automation
```cpp
// Water level management with safety checks
if (waterLevel < MIN_LEVEL && !isPumping) {
  startPump();
}
```

---

## 🌈 Future Enhancements

- [ ] Voice control integration (Alexa/Google Home)
- [ ] Machine learning for predictive automation
- [ ] Solar panel monitoring
- [ ] Energy consumption tracking
- [ ] Multi-zone temperature control
- [ ] Mobile app with custom UI

---

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Veda Revankar**

- GitHub: [@vedarevankar](https://github.com/vedarevankar)
- LinkedIn: [Veda Revankar](https://linkedin.com/in/vedarevankar)

---

<div align="center">

**⭐ Star this repository if you find it helpful!**

Made with ❤️ and Arduino

</div>
