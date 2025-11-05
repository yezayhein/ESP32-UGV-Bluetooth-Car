# ESP32-UGV-Bluetooth-Car
ESP32 Bluetooth-controlled car using the Dabble app’s GamePad module. Control forward, reverse, left, and right movements via smartphone Bluetooth. Features PWM speed control for smooth motor operation. Ideal for robotics and IoT beginners.
# 🚙 ESP32 Bluetooth Controlled UGV

This project is a **4-wheel unmanned ground vehicle (UGV)** controlled via **Bluetooth** using the [Dabble app](https://thestempedia.com/product/dabble/).  
It runs on **ESP32** and an **L298N motor driver**.

---

## 🧠 Features
- 4-wheel drive (left/right motor pairs)
- Controlled with Dabble GamePad (Bluetooth)
- PWM motor speed control using ESP32 `ledcWrite()`
- Easy to expand (ultrasonic, sensors, Wi-Fi, etc.)

---

## ⚙️ Hardware Used
| Component | Quantity | Description |
|------------|-----------|-------------|
| ESP32 DevKit | 1 | Main controller |
| L298N Motor Driver | 1 | Dual H-Bridge |
| DC Motors | 4 | 6V–12V geared motors |
| Battery | 1 | 7.4V or 12V |
| Dabble App | 1 | Bluetooth controller (Android/iOS) |

---

## 🔌 Pin Configuration

| ESP32 Pin | L298N Pin | Function |
|------------|------------|-----------|
| 33 | ENA | Right PWM |
| 14 | IN1 | Right direction 1 |
| 12 | IN2 | Right direction 2 |
| 25 | ENB | Left PWM |
| 26 | IN3 | Left direction 1 |
| 27 | IN4 | Left direction 2 |

> ⚠️ Note: GPIO12 is a boot-sensitive pin.  
> If ESP32 fails to start, change it to GPIO13.

---

## 📱 Dabble App Setup
1. Install **Dabble** from Play Store / App Store.  
2. Open **GamePad module**.  
3. Pair your ESP32 (Bluetooth name: `MyBluetoothCar`).  
4. Control movement using:
   - ⬆️ Up → Forward  
   - ⬇️ Down → Backward  
   - ⬅️ Left → Turn Left  
   - ➡️ Right → Turn Right  

---

## 🧩 Libraries Required
- **DabbleESP32**  
  Install via Arduino IDE Library Manager:  
  `Sketch → Include Library → Manage Libraries → Search "DabbleESP32"`

---

## 🧱 Wiring Diagram (to add)
You can include a diagram later inside `/images`.

---

## 📜 License
This project is licensed under the **MIT License** — free for personal and educational use.
