# 🦾 GPS 미지원 환경을 위한 실시간 센서 융합형 실내 위치 추정 솔루션

> ### A real-time disaster rescue robot for GPS-denied environments using multi-sensor data fusion ### 
> *(LiDAR, IMU, Wheel Encoder, Camera, Temperature/Humidity)*  

---

## 🔗 Links    
- 📄 **Paper:** “*Real-Time Disaster Rescue Robot for GPS-Denied Environments Using Multi-Sensor Data Fusion*,”  
  *Korea Information Technology Society, Nov. 2025*  

---

## 🧩 Background  

Modern disaster environments often block GPS signals (e.g., tunnels, basements, or dense urban areas).  
This project proposes a **multi-sensor fusion robot system** capable of real-time localization, mapping, and autonomous navigation in such GPS-denied environments.  

### 🎯 Key Objectives  
- 🛰️ Replace unreliable GPS data with **LiDAR–IMU–Odometry fusion (LIO)**  
- ⚙️ Perform **real-time SLAM** and **path planning** on a **Linux-based ROS2 system**  
- ☁️ Provide **cloud-based monitoring** through **MongoDB Atlas** and **Node-RED**  
- 🧠 Detect environmental hazards with **YOLOv5** and onboard cameras  

---

## ⚙️ Environment Setup  

| **Category** | **Details** |
|---------------|-------------|
| **OS** | Ubuntu 20.04 LTS |
| **Framework** | ROS2 Foxy, Navigation2, Cartographer |
| **Base Package** | Referenced the [STELLA_N2CAM_PI_X4PRO_ROS2_v2.0](https://github.com/ntrexlab/STELLA_N2CAM_PI_X4PRO_ROS2_v2.0) ROS2 package by NtrexLab
| **Programming** | Python 3, C++ |
| **Hardware** | Raspberry Pi 4, Stella N2 Robot |
| **Sensors** | LiDAR (YDLidar X4PRO), IMU (MW-AHRSv2U), Wheel Encoder, GPS (EZ-0048), Temp/Humidity Sensor |
| **Database / Monitoring** | MongoDB Atlas, Node-RED |
| **AI Model** | YOLOv5 (custom trained for obstacle detection) |

---

## 🧠 System Architecture  

### 🧩 System Overview  
<img width="972" alt="System Architecture" src="https://github.com/user-attachments/assets/5227d894-40b7-4a96-a4eb-fbb972524345" />

### ⚙️ Hardware  
<img width="959" alt="Hardware Diagram" src="https://github.com/user-attachments/assets/eaf8da6a-4658-474c-819f-b097c7bb600d" />

### 💻 Software  
<img width="1337" alt="Software Diagram" src="https://github.com/user-attachments/assets/82e0d6e4-ddb8-4f9d-bc54-49870729c32b" />

### ☁️ Node-RED Pipeline  
<img width="1893" alt="Node-RED Diagram" src="https://github.com/user-attachments/assets/62a25a0c-25c0-43c5-ba43-f65bd10baf42" />

---

## 🧩 Built With  

- **ROS2 (Foxy)** – SLAM, Navigation, and real-time sensor fusion  
- **Cartographer** – LiDAR-Inertial SLAM implementation  
- **YOLOv5** – Real-time object detection for hazard identification  
- **MongoDB Atlas** – Cloud data storage for live sensor updates  
- **Node-RED Dashboard** – Web-based real-time monitoring  
- **Raspberry Pi 4 + Stella N2** – Embedded control and execution platform  

---

## 🤖 Robot Platform & Test Track  

### 🧠 Customized Robot System  
The robot platform was built using **Raspberry Pi 4**, **YDLidar X4PRO**, **MW-AHRSv2U IMU**, and **a custom chassis** for modular expansion.  
It integrates multiple sensors for real-time localization, mapping, and obstacle detection in disaster-like indoor environments.  

<img src="https://github.com/user-attachments/assets/a8fa8789-a0e9-48c7-bced-dc42487dbaaf" width="600" alt="Customized Robot" />

---

### 🧭 Indoor Test Track  
To evaluate SLAM accuracy and navigation performance, a custom indoor track was designed to simulate **GPS-denied environments** such as tunnels and corridors.  
Obstacles were randomly placed to test dynamic path planning and YOLO-based hazard detection.  


<img src="https://github.com/user-attachments/assets/de58f297-f8d9-410e-862e-6fb62ddbb3e1" width="700" alt="Robot Track" />


---

## 📊 Results  

### 🛰️ End-to-end monitoring pipeline from robot → cloud → web in GPS-denied indoor environments  
<img width="1694" alt="Web Dashboard" src="https://github.com/user-attachments/assets/0c4860cf-5545-40ec-9fa9-354de3e2eee7" />

**Web Dashboard Features:**  
The web dashboard (built with **Node-RED** and **MongoDB Atlas**) provides a real-time visualization of all robot states and sensor data, enabling remote monitoring and control.  

- **SLAM Mapping:** Real-time 2D map generation via LiDAR–IMU–Odometry fusion  
- **Trajectory Tracking:** Displays robot path, orientation (roll/pitch/yaw), and cumulative distance  
- **Object Detection:** YOLOv5-based real-time obstacle and hazard visualization through live camera feed  
- **Sensor Data Monitoring:** Live values for LiDAR range, IMU angular velocity, acceleration, GPS status, and temperature/humidity  
- **Alert System:** Visual warning when an obstacle is detected within 30 cm of the robot  
- **Cloud Synchronization:** Latest sensor data automatically updated to MongoDB in real time  
- **Indoor/Outdoor Detection:** GPS status indicator switches between indoor/outdoor based on signal availability  


🎥 **Result Video:** [YouTube Link](https://youtu.be/2Iq2_ShP6eY?si=E3-j7cPRBcZmXgdn)

---

## 🏆 Award  
***Honorable Mention (KAIT Hanium Dream-Up ICT Competition 2025)***

---


