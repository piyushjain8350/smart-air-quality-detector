# smart-air-quality-detector
A smart indoor air quality monitoring system using Arduino UNO, MQ sensor, DHT11, LCD, relay, fan, and buzzer. Displays IAQ status (Good–Unhealthy) on LCD and activates fan or buzzer automatically.
# 🏠 Indoor Air Quality Monitor (Arduino UNO)

A smart **Indoor Air Quality (IAQ) Monitoring System** built using Arduino UNO, MQ gas sensor, DHT11 temperature/humidity sensor, 16x2 LCD, relay-controlled fan, and buzzer alert system.

---

## 🚀 Features
- Monitors air quality using **MQ gas sensor**
- Displays real-time **IAQ category** on LCD (Good, Moderate, Unhealthy, etc.)
- Shows **temperature** and **humidity** using DHT11
- Activates **fan** automatically when air quality becomes unhealthy
- Triggers **buzzer** at very unhealthy air quality levels
- Uses **moving average** for stable readings
- Warm-up calibration for accurate baseline sensing

---

## 🧩 Components Used
| Component | Description |
|------------|--------------|
| Arduino UNO | Main controller |
| MQ-135 / MQ-2 sensor | Air quality sensor |
| DHT11 | Temperature and humidity sensor |
| 16x2 LCD | Display module |
| 5V Relay Module | Controls external fan |
| DC Fan | Simulates air purifier |
| Buzzer | Audio alert for poor air quality |
| Jumper Wires + Breadboard | Circuit connections |

---

## ⚙️ Circuit Overview
- MQ Sensor → `A0`
- DHT11 → Digital Pin `2`
- Relay Module → Pin `5`
- Buzzer → Pin `6`
- LCD (4-bit mode) → Pins `7, 8, 9, 10, 11, 12`

---

## 🧠 Working Principle
1. The MQ sensor measures air quality levels (gases like CO, NH₃, smoke).
2. After a warm-up period, a **baseline** is established.
3. The system classifies the air into categories:
   - `Good`
   - `Moderate`
   - `Unhealthy for Sensitive Groups`
   - `Unhealthy`
   - `Very Unhealthy`
4. The fan turns ON at “Unhealthy” and buzzer sounds at “Very Unhealthy”.
5. The LCD continuously displays IAQ, temperature, and humidity.

---

## 🧰 Libraries Used
- `DHT.h`
- `LiquidCrystal.h`

Install via Arduino IDE → *Sketch* → *Include Library* → *Manage Libraries...*

---

## 🔧 Future Enhancements
- Add Wi-Fi module (ESP8266/ESP32) for IoT integration
- Log data to cloud dashboard
- Add CO₂ / PM2.5 sensors for higher accuracy
- Display AQI graph via web interface

---

## 📜 Author
**Piyush Jain**  
💡 Arduino | IoT | Embedded Systems Enthusiast  
🔗 [LinkedIn] *(https://www.linkedin.com/in/piyushjain8350/)*

---
### 🪶 License
This project is open source under the **MIT License**.
