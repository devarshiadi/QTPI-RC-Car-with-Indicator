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
- **[Code2play Inventor](https://www.stemdesi.in/)**

---
💡 *Feel free to modify the code and experiment with different motor speeds and RGB light effects!* 🚀

# ❓ Frequently Asked Questions (FAQ) - QTPI RC Car

## 1️⃣ **What is the QTPI RC Car project?**
The QTPI RC Car is a Bluetooth-controlled robotic car built using the QTPI robotic kit and programmed with a drag-and-drop block-based interface. It allows users to control movement and indicator lights via a mobile app.

## 2️⃣ **How do I connect the app to the RC car?**
- Ensure Bluetooth is enabled on your mobile device.
- Click on **CONNECT** in the app.
- Select the appropriate Bluetooth device from the list.
- If the connection is successful, a "Connected" notification will appear.

## 3️⃣ **What are the movement controls?**
- **Forward:** Moves the car ahead.
- **Backward:** Moves the car in reverse.
- **Left:** Turns the car left while lighting up the left indicator.
- **Right:** Turns the car right while lighting up the right indicator.
- Releasing any button stops the movement.

## 4️⃣ **What do the RGB lights indicate?**
- **Left Turn:** Left RGB light turns red.
- **Right Turn:** Right RGB light turns red.
- **No movement:** Both RGB lights remain off.

## 5️⃣ **How do I modify the app?**
- Open `RC_CAR_WITH_INDICATOR.aia` in MIT App Inventor or Code2Play.
- Adjust UI components and logic blocks as per your requirements.
- Recompile and deploy the modified version.

## 6️⃣ **What happens if the app fails to connect?**
- Ensure the RC car is powered on and within Bluetooth range.
- Restart Bluetooth on your mobile device.
- Try reconnecting using the **CONNECT** button in the app.
- If the issue persists, restart the RC car and try again.

## 7️⃣ **How do I close the application?**
- Press the **Back Button** on your mobile device.
- The app will prompt to exit or close automatically.

## 8️⃣ **Can I customize the motor speed?**
Yes, in the block-based code editor, modify the **Rotate Speed** values for `RIGHT_MOTOR` and `LEFT_MOTOR` to adjust speed levels.

## 9️⃣ **Where can I find the source files?**
- `RC_CAR_WITH_INDICATOR.apk` (Installable app)
- `RC_CAR_WITH_INDICATOR.aia` (Editable source file)



