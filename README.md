# 🎙️ Voice Controlled Home Automation with Arduino (Offline)

An **offline voice-controlled home automation system** using **Arduino Uno** and the **VC-02 AI Voice Recognition Module**, designed to control household appliances such as lights and fans using predefined voice commands—without any internet dependency.

This project is especially beneficial for **elderly and disabled individuals**, offering privacy, fast response time, and reliability in low-connectivity environments.

---

## 📌 Features

- 🔊 Offline voice recognition (no internet required)
- ⚡ Fast response time (< 1 second)
- 🔐 Privacy-preserving (local processing)
- 🧠 Supports pre-trained English voice commands
- 🏠 Controls real appliances using relay modules
- ♿ Accessibility-focused design
- 💡 Scalable for more devices

---

## 🛠️ Hardware Components

- Arduino Uno  
- VC-02 Offline Voice Recognition Module  
- Relay Module  
- LED  
- Fan / AC Load  
- Jumper Wires  
- Power Supply  

---

## 🧩 Software & Libraries

- Arduino IDE  
- SoftwareSerial Library  
- UART Serial Communication (9600 baud)

---

## ⚙️ System Architecture

### Working Principle

The system operates in **three main stages**:

#### 1. Voice Command Recognition
- The VC-02 module listens for predefined voice commands.
- Upon recognition, it generates a corresponding hexadecimal code via UART.

#### 2. Hexadecimal Code Mapping
Each command maps to a fixed hexadecimal value:

| Voice Action | Hex Code |
|-------------|----------|
| LED ON | AA11 |
| LED OFF | AA00 |
| FAN ON | A190 |
| FAN OFF | A145 |

#### 3. Device Control Logic
- Arduino reads serial data using `SoftwareSerial`
- Hex codes are matched using conditional logic
- Corresponding GPIO pins are toggled to control relays and appliances

---

## 🔌 Hardware Connections

### VC-02 → Arduino Uno

| VC-02 Pin | Arduino Pin | Description |
|---------|------------|------------|
| TX | D2 | Sends command data |
| RX | D3 | Receives optional data |
| VCC | 5V | Power supply |
| GND | GND | Common ground |

### Output Devices

| Device | Arduino Pin | Function |
|------|------------|----------|
| LED (via resistor) | D8 | LED ON/OFF |
| Relay Signal | D9 | Fan / AC Load control |
| Relay VCC/GND | 5V / GND | Relay power |

---

## 🧪 Testing & Simulation

- Circuit simulated using **Proteus**
- Serial output verified via Arduino Serial Monitor
- Reliable command recognition under varied environments
- Consistent real-time control without network latency

---

## 📊 Results & Observations

- Accurate recognition of trained voice commands
- Stable UART communication
- Reliable GPIO triggering
- Fast and consistent response
- Successful real-time control of appliances

---

## 🚀 Applications

### 🏠 Smart Home Automation
- Voice-based control of lights, fans, and appliances
- Improves comfort and energy efficiency

### ♿ Accessibility Solutions
- Enables independence for elderly and disabled users
- Reduces need for physical interaction with switches

### 🌐 Offline Control Systems
- Works in rural or low-connectivity areas
- Ideal for privacy-sensitive and industrial environments

---

## ⚠️ Limitations

- Initial voice training required
- Hardware failure may affect usability
- Limited scalability with basic `if-else` logic
- No internal device state tracking

---

## 🔮 Future Enhancements

- Control of more appliances (ACs, RGB LEDs, smart locks)
- Mobile app integration (Bluetooth / WiFi)
- Voice feedback confirmation
- Smart security system integration
- Energy monitoring per device
- Scalable command handling (switch-case / mapping)

---

## 👩‍💻 Authors

- **Isha Roy** (220102042)  
- **Nitish Kumar Singh** (220102067)  

Department of Electronics and Electrical Engineering  
Indian Institute of Technology Guwahati  

---

## 📚 References

1. Arduino UNO R3 Datasheet  
2. Arduino Official Documentation  
3. VC-02 Voice Recognition Module Manual (AI Thinker)  
4. SparkFun – UART Communication  
5. Instructables – Arduino Voice Automation Projects  

---

⭐ If you find this project useful, feel free to star the repository!
