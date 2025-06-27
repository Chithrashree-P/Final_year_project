# 🥛 Milk Quality Analysis - Final Year Project

Welcome to the **Milk Quality Analysis** project! This system uses multiple sensors to collect real-time data on milk quality and displays it on a web interface using a local XAMPP server.

---

## 📌 Project Overview

This project integrates hardware sensors, a local server, and a web dashboard to evaluate milk quality in real-time.

### ✅ Components Used

- **Sensors**:
  - 🧪 *pH Sensor*: Measures acidity/alkalinity.
  - 🎨 *Colour Sensor*: Detects milk discoloration.
  - 🌡️ *Temperature Sensor*: Monitors milk temperature.
  - 💨 *Gas Sensor*: Detects spoilage gases like ammonia.
  - 📏 *Ultrasonic Sensor*: Measures milk volume.

- **Microcontroller**:
  - ESP32 (or ESP8266)

- **Software Stack**:
  - **Arduino IDE** – Upload code to ESP32.
  - **XAMPP** – PHP, Apache, and MySQL server.
  - **MySQL** – Stores the sensor data.
  - **PHP + HTML/CSS** – Frontend web interface.

---

## 📁 Project Directory Structure



---

## ⚙️ System Requirements

### 🔧 Hardware:
- ESP32 microcontroller
- pH Sensor
- Colour Sensor
- Gas Sensor
- Ultrasonic Sensor
- Temperature Sensor

### 💻 Software:
- XAMPP (Apache, MySQL, PHP)
- Arduino IDE
- Web browser (Chrome, Firefox, etc.)

---

## 🚀 Setup Instructions

### 1. Install XAMPP
- Download from: [https://www.apachefriends.org](https://www.apachefriends.org)
- Install and start **Apache** and **MySQL** via the XAMPP control panel.

### 2. Set Up the Database
- Open: `http://localhost/phpmyadmin`
- Create a database named: `milk_quality_db`
- Import `milk_quality_db.sql` from the `database/` folder.

### 3. Upload Sensor Code
- Connect sensors to ESP32.
- Open Arduino IDE.
- Upload `sensors.ino` from the `sensors_code/` directory.
- Ensure ESP32 sends HTTP POST/GET requests to XAMPP server.

### 4. Deploy Web Interface
- Copy the `web_code/` contents to the `htdocs/` folder in XAMPP.
- Access it at: `http://localhost/`

### 5. Start Monitoring
- Power on the ESP32 and sensors.
- The system starts sending data to the database.
- The web page will display real-time milk quality data.

---

## 📊 How It Works

1. **Data Collection**:
   - Sensors collect data continuously.
   - ESP32 sends data to a local server via HTTP.

2. **Data Storage**:
   - XAMPP’s MySQL stores data in the `milk_quality` table.

3. **Visualization**:
   - PHP & MySQL display values on the dashboard.
   - Quality is evaluated (e.g., pH < 6.5 → Spoiled Milk).

---

## 🛠️ Troubleshooting

| Issue | Solution |
|-------|----------|
| **XAMPP not running** | Start Apache and MySQL in control panel. |
| **Database connection errors** | Check credentials in `web_code/config.php`. Confirm DB name is `milk_quality_db`. |
| **No data on the webpage** | Confirm ESP32 is correctly sending data to your local server IP. |

---

## 📬 Contact

For queries or support, feel free to reach out:

📧 **Email**: [pchitrashree@gmail.com](mailto:pchitrashree@gmail.com)

---

## ⚠️ Disclaimer

> This project is for **educational and research** purposes only. It is not validated or certified for commercial or industrial use.

---

### 🙏 Thank You for Using This Project!
