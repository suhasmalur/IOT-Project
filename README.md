# 🚀 IoT Attendance System with RFID

<div align="center">

# 📡 Smart Attendance Tracking System

### Using ESP8266, RFID & Google Sheets

![ESP8266](https://img.shields.io/badge/ESP8266-NodeMCU-blue?style=for-the-badge)
![RFID](https://img.shields.io/badge/RFID-MFRC522-green?style=for-the-badge)
![IoT](https://img.shields.io/badge/IoT-Attendance%20System-orange?style=for-the-badge)
![Arduino](https://img.shields.io/badge/Arduino-IDE-teal?style=for-the-badge)
![Google Sheets](https://img.shields.io/badge/Cloud-Google%20Sheets-success?style=for-the-badge)

### ⚡ Real-Time | Contactless | Automated | Cloud Enabled

</div>

---

## 📖 Overview

Traditional attendance systems are time-consuming, prone to human errors, and vulnerable to proxy attendance.

This project introduces an **IoT-Based Smart Attendance System** that uses RFID technology and cloud integration to automate attendance recording.

When a user scans an RFID card:

✅ Identity is verified instantly

✅ Attendance is recorded automatically

✅ Timestamp is generated

✅ Data is stored in Google Sheets

✅ LCD displays confirmation

✅ Buzzer provides feedback

The entire process is completed within a few seconds and can be monitored remotely.

---

# 🎯 Features

✨ Contactless Attendance Marking

✨ RFID-Based Authentication

✨ Real-Time Cloud Logging

✨ Google Sheets Integration

✨ Wi-Fi Connectivity

✨ LCD Display Feedback

✨ Buzzer Notifications

✨ Low-Cost Deployment

✨ Paperless Attendance Management

✨ Easy Scalability

---

# 🏗️ System Architecture

```text
+------------+
| RFID Card  |
+------------+
       |
       v
+----------------+
| MFRC522 Reader |
+----------------+
       |
       v
+----------------+
| ESP8266        |
| NodeMCU        |
+----------------+
       |
      WiFi
       |
       v
+----------------------+
| Google Apps Script   |
+----------------------+
       |
       v
+----------------------+
| Google Sheets        |
+----------------------+

       |
       +----> LCD Display
       |
       +----> Buzzer
```

---

# 🔥 Working Flow

```text
Power ON
   ↓
Connect to WiFi
   ↓
Initialize RFID Reader
   ↓
Wait For Card
   ↓
Read RFID Data
   ↓
Validate User
   ↓
Send Data To Cloud
   ↓
Store In Google Sheets
   ↓
Display Success Message
```

---

# 🛠️ Hardware Components

| Component | Quantity |
|------------|----------|
| ESP8266 NodeMCU | 1 |
| MFRC522 RFID Reader | 1 |
| RFID Cards/Tags | Multiple |
| 16x2 I2C LCD Display | 1 |
| Active Buzzer | 1 |
| Breadboard | 1 |
| Jumper Wires | As Required |
| USB Cable | 1 |

---

# 💻 Software Requirements

### IDE

- Arduino IDE

### Cloud Services

- Google Sheets
- Google Apps Script

### Programming Language

- C++

---

# 📚 Required Libraries

Install the following libraries from Arduino Library Manager:

```cpp
ESP8266WiFi
ESP8266HTTPClient
WiFiClientSecureBearSSL
MFRC522
SPI
LiquidCrystal_I2C
```

---

# 🔌 Circuit Connections

## RFID MFRC522 → ESP8266

| RFID Pin | ESP8266 Pin |
|-----------|------------|
| SDA | D4 |
| SCK | D5 |
| MOSI | D7 |
| MISO | D6 |
| RST | D3 |
| GND | GND |
| 3.3V | 3.3V |

---

## LCD I2C → ESP8266

| LCD Pin | ESP8266 Pin |
|----------|------------|
| SDA | D2 |
| SCL | D1 |
| VCC | 5V |
| GND | GND |

---

## Buzzer → ESP8266

| Buzzer Pin | ESP8266 Pin |
|------------|------------|
| Positive | D8 |
| Negative | GND |

---

# 🚀 How To Run

## 1️⃣ Clone Repository

```bash
git clone https://github.com/YOUR_USERNAME/IOT-Project.git
```

Move inside project folder

```bash
cd IOT-Project
```

---

## 2️⃣ Open Arduino IDE

Open the project file

```text
attendance_system.ino
```

---

## 3️⃣ Install Libraries

Arduino IDE

```text
Sketch
 └── Include Library
      └── Manage Libraries
```

Install:

```text
MFRC522
LiquidCrystal_I2C
ESP8266WiFi
ESP8266HTTPClient
```

---

## 4️⃣ Configure WiFi

Replace with your credentials:

```cpp
const char* ssid = "YOUR_WIFI_NAME";
const char* password = "YOUR_WIFI_PASSWORD";
```

---

## 5️⃣ Configure Google Apps Script URL

```cpp
String GOOGLE_SCRIPT_URL =
"https://script.google.com/macros/s/YOUR_SCRIPT_ID/exec";
```

---

## 6️⃣ Select Board

```text
Tools
 └── Board
      └── NodeMCU 1.0 (ESP-12E Module)
```

---

## 7️⃣ Upload Code

Click Upload Button

```text
✔ Compiling
✔ Uploading
✔ Done
```

---

## 8️⃣ Start Attendance Logging

Bring RFID card near reader.

Attendance will be stored automatically.

🎉 Done!

---

# 📂 Project Structure

```text
IOT-Project
│
├── README.md
├── attendance_system.ino
├── images
│   ├── setup.jpg
│   ├── rfid.jpg
│   ├── lcd.jpg
│   └── nodemcu.jpg
│
├── docs
│   └── Project_Report.pdf
│
└── circuit_diagram.png
```

---

# 📊 Example Attendance Record

| Name | Date | Time |
|--------|----------|----------|
| Suhas M Alur | 14-06-2026 | 09:30:25 |
| Student 1 | 14-06-2026 | 09:31:08 |
| Student 2 | 14-06-2026 | 09:32:44 |

---

# 📸 Screenshots

## 📷 Project Setup

```markdown
![Project Setup](images/setup.jpg)
```

---

## 📷 RFID Reader

```markdown
![RFID Reader](images/rfid.jpg)
```

---

## 📷 LCD Display

```markdown
![LCD Display](images/lcd.jpg)
```

---

## 📷 NodeMCU ESP8266

```markdown
![ESP8266](images/nodemcu.jpg)
```

---

# 🔐 Advantages

✅ Eliminates Proxy Attendance

✅ Fast Attendance Logging

✅ Real-Time Data Access

✅ Cloud-Based Storage

✅ Easy Management

✅ Accurate Timestamping

✅ User Friendly

✅ Cost Effective

---

# ⚠️ Limitations

❌ Requires Wi-Fi Connection

❌ No Offline Data Storage

❌ No Biometric Authentication

❌ No Admin Dashboard

---

# 🚀 Future Enhancements

### 👆 Fingerprint Authentication

Integrate biometric verification.

---

### 😀 Face Recognition

Use camera modules for facial recognition.

---

### 📱 Mobile Application

Attendance monitoring through Android/iOS app.

---

### ☁️ Firebase Integration

Replace Google Sheets with Firebase Database.

---

### 📊 Analytics Dashboard

Generate attendance reports and insights.

---

### 💾 Offline Data Storage

Store attendance locally during network outages.

---

### 🔔 Email/SMS Notifications

Notify administrators automatically.

---


# 🏆 Project Highlights

🏅 Real-Time Attendance Logging

🏅 Cloud-Based Data Storage

🏅 RFID Authentication

🏅 IoT Integration

🏅 Contactless Operation

🏅 Low-Cost Implementation

---

# ⭐ Support

If you found this project useful:

⭐ Star this repository

🍴 Fork this repository

📢 Share with friends

💻 Contribute to the project

---


### "Transforming Attendance Management Through IoT"

⭐ Star This Repository If You Like It ⭐

</div>
