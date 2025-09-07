# 🎨 Color Detection with OpenCV & Arduino

A computer vision and embedded systems project that integrates **OpenCV (Python)** with an **Arduino UNO** to detect colors in real-time and trigger hardware responses (LEDs + buzzer). This project demonstrates the synergy between software-based image processing and hardware-based feedback systems.

---

## 📌 Project Overview

- Uses a webcam to detect specific colors in the environment.  
- Converts **BGR → HSV color space** for robust color detection.  
- Handles special cases (like red hue wrap-around in HSV).  
- Communicates with Arduino via **pyFirmata** over serial.  
- Activates:
  - **LED1 (Pin 3)**
  - **LED2 (Pin 7)**
  - **Buzzer (Pin 11)**  

---

## 🛠️ Requirements

### 🔹 Software
- Python 3.8+  
- Libraries:  
  ```bash
  pip install opencv-python numpy pyfirmata

### 🔹 Hardware
- Arduino UNO (or compatible board)  
- USB cable for Arduino ↔ PC communication  
- Breadboard & jumper wires  
- **Components used:**  
  - 2 × LEDs (with ~220Ω resistors)  
  - 1 × Buzzer  


## ⚙️ Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/color-detection-arduino.git
   cd color-detection-arduino

   
### Connect Arduino hardware

- LED1 → Pin 3

- LED2 → Pin 7

- Buzzer → Pin 11

- Common ground (GND) to breadboard

### Run the Python script
  
  ```bash
    - python color_detection.py
   ```



## How It Works

  - Camera Capture → Webcam captures live video frames.

  - Color Processing → Frames are converted from BGR to HSV.

  - Masking → A color range is applied to isolate target colors.

### Arduino Control →

   - Detected color triggers Arduino pins via pyFirmata.

   - Example: Detecting red → LED1 ON + buzzer ON.


## 📂 Project Structure

   - ├── color_detection.py   # Main Python script
   - ├── README.md            # Documentation
   - ├── requirements.txt     # Dependencies
   - └── /images              # Example screenshots (optional)



## 🚀 Future Improvements

   - Add more colors with individual hardware responses.

   - Integrate with ESP32/ESP8266 for IoT-based color alerts.

   - Store detected color logs with timestamps.

   - Add a GUI (PyQt/Tkinter) for dynamic color range selection.

# 👨‍💻 Author

- **Ahmed Gwely**  
- Passionate about Computer Vision, Embedded Systems, and AI-driven IoT.  
- 🌐 [LinkedIn Profile](https://www.linkedin.com/in/ahmed-gwely-2589611b0/)  


