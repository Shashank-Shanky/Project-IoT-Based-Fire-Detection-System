# Project-IoT-Based-Fire Detection System using ESP32 and Blynk



### 🔥 Fire Detection System using ESP32 and Blynk

**Developed by: Shashank**

---

#### 📋 Project Overview

This project is a fire detection and alert system that uses an ESP32 microcontroller, a flame sensor, buzzer, and LEDs. The system connects to the Blynk IoT platform to send real-time notifications and updates through a mobile application.

---

#### 🛠️ Features

* Detects presence of fire using a flame sensor.
* Sends real-time alerts via the **Blynk** mobile app.
* Activates a **buzzer** and turns on a **red LED** when fire is detected.
* Displays fire detection status using **green/red LEDs**.
* Blynk **virtual LED** shows fire alert on app.
* Logs event using `Blynk.logEvent()`.

---

#### 🔗 Blynk Configuration

```cpp
#define BLYNK_TEMPLATE_ID "TMPL39krsjNT-"
#define BLYNK_TEMPLATE_NAME "Fire Detection"
#define BLYNK_AUTH_TOKEN "tU8gZPgZL7vGC2IO3F6H15M-keaih-2J"
```

#### 📶 WiFi Credentials

```cpp
char ssid[] = "Wokwi-GUEST"; // Enter your WiFi/Hotspot name
char pass[] = "";            // Enter your WiFi/Hotspot password
```

---

#### 🧰 Hardware Components

* ESP32 Development Board
* Flame Sensor
* Buzzer
* Red LED (Pin 14)
* Green LED (Pin 12)
* Jumper Wires
* Breadboard

---

#### 🔌 Pin Configuration

| Component    | ESP32 Pin |
| ------------ | --------- |
| Flame Sensor | D23       |
| Green LED    | D12       |
| Red LED      | D14       |
| Buzzer       | D13       |

---

#### 📱 Blynk App Setup

1. Create a new Blynk project.
2. Add a **LED Widget** on **Virtual Pin V1**.
3. Enable **Event Logging** for fire alert notifications (`fire_alert`).
4. Use the credentials above to connect ESP32 to Blynk.

---

#### 🧠 How It Works

* Continuously reads input from the **flame sensor**.
* If fire is detected (`LOW` signal):

  * Logs an event to Blynk.
  * Turns ON the **red LED** and **buzzer**.
  * Turns OFF the **green LED**.
* If no fire:

  * Turns OFF red LED and buzzer.
  * Turns ON green LED.
* The system updates the Blynk app in real time.

---

#### 💻 Libraries Used

* `WiFi.h`
* `WiFiClient.h`
* `BlynkSimpleEsp32.h`

---




