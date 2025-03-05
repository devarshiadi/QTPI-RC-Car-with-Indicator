# 🚗 QTPI RC Car with Indicator

## 📌 Overview
This project is built using the **QTPI Robotic Kit** and **Code2Play** (similar to MIT Innovator). It allows users to control an RC car using a mobile app with Bluetooth connectivity. The car includes movement controls and LED indicators for directions.

## 🛠 Features
- **Bluetooth Connectivity**: Connects to the RC car via Bluetooth.
- **Directional Control**: Move Forward, Backward, Left, and Right.
- **Indicator Lights**: RGB lights turn red to indicate turns.
- **Drag-and-Drop Programming**: Built using a block-based logic system.

## 📑 Installation & Setup
1. **Install the App**
   - Download and install the APK file: `RC_CAR_WITH_INDICATOR.apk`
   - Ensure Bluetooth is enabled on your device.

2. **Modify or Customize the App**
   - Import `RC_CAR_WITH_INDICATOR.aia` into MIT App Inventor or Code2Play.
   - Modify UI components and logic blocks as needed.

## 🎨 Project Presentation (PPT)
[📌 Click here to view the PPT](https://www.canva.com/design/DAGg1rjSozg/7wej1OpXyx5-GteqUhogdw/edit?utm_content=DAGg1rjSozg&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)

## 📖 Coding Logic
### **1️⃣ Connecting to the RC Car**
- **Before Picking Bluetooth Device:**
  - `when CONNECT.BeforePicking DO`
  - Set `CONNECT.Elements` to `BluetoothClient1.AddressAndNames`
- **After Picking Bluetooth Device:**
  - Use `if-then-else` to check connection success
  - Show notification: "Connected" or "Failed to Connect"

### **2️⃣ Movement Controls**
- **Forward:**
  - `when FORWARD.TouchDown DO`
  - `RIGHT_MOTOR.Rotate(150, True)`, `LEFT_MOTOR.Rotate(150, True)`
  - `when FORWARD.TouchUp DO` → Set motor speed to `0`
- **Backward:**
  - Same as Forward but `Direction = False`
- **Left & Right Turns:**
  - Left: `LEFT_MOTOR.Rotate(150, False)`, `RIGHT_MOTOR.Rotate(150, True)`, `LEFT_RGB.Red = 255`
  - Right: `LEFT_MOTOR.Rotate(150, True)`, `RIGHT_MOTOR.Rotate(150, False)`, `RIGHT_RGB.Red = 255`
  - On `TouchUp`, set motor speed to `0` and turn off RGB lights

### **3️⃣ Exit Application**
- `when Screen1.BackPressed DO`
- `Close Application`

## 🔗 Resources
- **[MIT App Inventor](https://appinventor.mit.edu/)**
- **[QTPI Robotics](https://www.qtpi.in/)**
- **[Code2play Inventor](https://www.stemdesi.in/)

---
💡 *Feel free to modify the code and experiment with different motor speeds and RGB light effects!* 🚀

