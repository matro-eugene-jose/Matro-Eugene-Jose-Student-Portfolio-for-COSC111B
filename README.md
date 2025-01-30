# **Laboratory Activity 2**  

### **Description**  
This project utilizes an Arduino to create a smooth, sequential LED illumination effect using Pulse Width Modulation (PWM). Each LED gradually brightens before transitioning to the next, producing a visually appealing fading effect.  

### **Components Used**  
- **Arduino Uno** (or a compatible board)  
- **5 LEDs**  
- **5 Resistors** (220Ω recommended)  
- **Jumper wires**  
- **Breadboard**  

### **Wiring Instructions**  
- Connect the LEDs to the appropriate digital pins:  
  - For an **Arduino Uno R3**, use pins **11, 10, 9, 6, and 5**.  
  - If using a different Arduino model, use pins **12, 11, 10, 9, and 8** instead.  
- Each LED should be connected in series with a current-limiting resistor to prevent excessive current flow.  

### **Code Explanation**  
1. **Pin Setup:**  
   - An array named `ledPins[]` holds the pin numbers assigned to the LEDs.  
   - The `setup()` function configures these pins as outputs.  

2. **LED Brightness Control (loop function):**  
   - The program gradually increases each LED's brightness from 0 to 255 using the `analogWrite()` function.  
   - The `map()` function helps adjust brightness values for smoother transitions.  
   - A short delay of **30ms** ensures a smooth, gradual fade-in effect.  
   - Once an LED reaches full brightness, the next LED begins its transition after a **200ms** pause.  

### **How to Use**  
1. Upload the code to your Arduino board using the **Arduino IDE**.  
2. Observe the LEDs lighting up sequentially with a smooth fading effect.  
3. Adjust the `ledPins[]` array if using a different Arduino model to match the correct pins.  


# **Laboratory Activity 3**  

### **Description**  
This Arduino-based project simulates a fire detection system using a flame sensor. The system continuously monitors for fire and activates an alert mechanism—such as an LED or buzzer—when a flame is detected.  

### **Components Used**  
- **Arduino Uno** (or a compatible board)  
- **Flame Sensor**  
- **LED** (for visual alert)  
- **Buzzer** (for audible alert)  
- **Jumper wires**  
- **Breadboard**  

### **Wiring Instructions**  
- Connect the **flame sensor** output to a designated digital pin on the Arduino.  
- Attach an **LED** to another digital pin to function as a visual indicator.  
- Connect a **buzzer** to a separate digital pin to emit an audible alarm.  
- Ensure all components share a common ground and proper power connections.  

### **Code Explanation**  
1. **Sensor Initialization:**  
   - The flame sensor is assigned to an input pin on the Arduino.  
   - The LED and buzzer are set as output devices within the `setup()` function.  

2. **Fire Detection Logic:**  
   - The `loop()` function continuously reads input from the flame sensor.  
   - If a fire is detected, the LED lights up, and the buzzer sounds an alert.  
   - If no fire is detected, both the LED and buzzer remain off.  
   - A short delay is used to ensure stable sensor readings.  

### **How to Use**  
1. Upload the code to your Arduino board using the **Arduino IDE**.  
2. Bring a small, controlled flame (such as a lighter) near the flame sensor to test its detection capability.  
3. When fire is detected, the LED should illuminate, and the buzzer should activate.  
4. If necessary, adjust the sensor's sensitivity for more accurate readings.  

### **Safety Precautions**  
- Avoid prolonged exposure of the sensor to extreme heat.  
- Double-check all wiring to prevent electrical hazards.  
- Keep flammable materials at a safe distance when testing with an open flame.  

