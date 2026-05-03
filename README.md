                                                        ESP32 Smart Home

ESP32 Sentinel: Local-First Smart HomeA high-performance, private home automation hub powered by the ESP32. This system hosts a responsive web dashboard directly from the microcontroller—no cloud, no apps, and no external servers required. 

🚀 Key Features
. Asynchronous Web Server: Supports multiple client connections simultaneously without lag.  
. Zero-Cloud Privacy: All data stays on the device; hosts its own Wi-Fi Access Point.  
. Event-Driven Alerts: Real-time triggers for gas leaks (MQ-2) and proximity detection (HC-SR04).  
. Multi-Zone Monitoring: Independent climate and security tracking for Living Room, Bedroom, and Kitchen.  
. Persistent Memory: Saves alarm thresholds and light states during power cycles using NVS.


🛠️ Hardware Stack
This project utilizes an ESP32-WROOM-32 as the central MCU for logic and AP hosting. Environmental monitoring is handled by three DHT22 sensors for high-accuracy temperature and humidity tracking. For security and safety, the system includes three HC-SR04 sensors for proximity detection and an MQ-2 sensor for gas and smoke detection. Local alerts are managed via an Active Buzzer and LED indicators.  

🔧 Core Pinout (Optimized)
Sensors (DHT): GPIO 4, 5, 18  Distance (Trig/Echo): GPIO 12/14, 27/35, 25/33  Analog Gas (ADC1): GPIO 34  Indicators (LEDs/Buzzer): GPIO 19, 23, 15, 26  

📥 Quick Start
Clone this repo.  Install ESPAsyncWebServer and DHT sensor libraries.  Flash the firmware using PlatformIO or Arduino IDE.  Connect to the "ESP32-Sentinel" Wi-Fi and visit [http://192.168.4.1](http://192.168.4.1).  

Note: Use a voltage divider on HC-SR04 Echo pins to protect the ESP32 from 5V logic.  
