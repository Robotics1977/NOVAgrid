# 🤖 Oscar — Autonomous Lawnmower Rover
**Platform:** Raspberry Pi 5 + Wheelchair Motors  
**Role:** Outdoor autonomous mower  
**OS / Stack:** Ubuntu 24.04 + ROS 2 Jazzy  
**Communication:** ROS 2 + possible MQTT for sensor nodes  
**Status:** Planned

---

## 📘 Overview
Oscar is NOVAgrid’s heavy-duty outdoor rover built to autonomously mow or traverse yards.  
The concept merges:

- Wheelchair motors with wheels BLDC hub motors  
- a ruggedized Pi 5 compute unit  
- an enclosed electronics bay  
- long-range Wi-Fi or mesh network  

Oscar represents the outdoor robotics branch of NOVAgrid.

---

## 🔩 Hardware (Planned)
| Component | Notes |
|----------|-------|
| **Raspberry Pi 5** | Main computer |
| **Wheelchair motors** | Strong, efficient propulsion |
| **VESC or custom motor controller** | BLDC control |
| **GPS (RTK optional)** | Outdoor positioning |
| **Wheel encoders** | Odometry |
| **IMU** | Stability + filtering |
| **LIDAR** | Mapping & obstacle detection |
| **Battery pack 24–36V** | Long run time |
| **Metal frame** | Weather-resistant enclosure |

---

## 🧠 Software Architecture
- GPS + odometry fusion  
- Outdoor SLAM (cartographer or similar)  
- Perimeter mapping  
- Mowing patterns  
- Safety interlocks  
- Remote kill-switch  

---

## 🔮 Planned Features
- Blade engagement control  
- Perimeter wire compatibility (optional)  
- Docking station  
- Teleoperation mode  

---

## 🗓 Development Roadmap
- After Alfred 1 base frameworks  

---


