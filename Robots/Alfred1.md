# 🤖 Alfred 1 — Mobile Robotics Learning Platform
**Platform:** Raspberry Pi 5 + TB6612FNG  
**Role:** Core learning rover for ROS 2 Jazzy  
**OS / Stack:** Ubuntu 24.04 + ROS 2 Jazzy  
**Communication:** Local ROS 2 nodes  
**Status:** In development

---

## 📘 Overview
Alfred 1 is the first fully custom, from-the-frame-up robot in the NOVAgrid ecosystem.  
Designed as a “learn-by-doing” platform, Alfred 1 is your stepping stone from robot hobbyist to robotics engineer.

Alfred 1 represents:

- a path to learn ROS 2  
- real robot navigation  
- a platform for computer vision  
- a testbed for sensors  
- and the mechanical precursor to Alfred 5  

He isn’t a toy or an RC car — he’s a **true robotics platform** built to teach real-world robotics challenges.

---

## 🔩 Hardware
| Component | Notes |
|----------|-------|
| **Raspberry Pi 5 + SSD** | Main compute unit |
| **RPLidar A1M8** | 360° environment scanning |
| **EMEET C960 1080p USB camera** | Front-facing RGB camera for basic vision & streaming |
| **TB6612FNG** | Motor driver |
| **JGA25-371 motors w/ encoders** | Precise differential drive |
| **LiFePO4 12.8V battery** | Main power source with onboard BMS |
| **5V buck converter (10A)** | Pi, sensors, peripherals |
| **Multiple HC-SR04 sensors** | Obstacle detection |
| **Custom aluminum frame (planned)** | CNC-cut for production-ready enclosure |

---

## 📡 Communication (ROS 2)
Alfred 1 uses ROS 2 Jazzy running directly on the Pi.

### ROS 2 Nodes (current and planned)
- `/scan` → LIDAR publisher  
- `/camera/image_raw` → camera topics  
- `/cmd_vel` → motor controller input  
- `/odom` → wheel odometry  
- `/ultrasonic` → HC-SR04 sensors  
- `/nav2` (future) → navigation stack  

---

## 🧠 Software Architecture
Three primary layers:

1. **Hardware Interface Layer** (motor, encoder, ultrasonic drivers)  
2. **ROS 2 Node Layer** (publishers/subscribers)  
3. **Navigation + Perception Layer** (SLAM, Nav2, CV)  

Future additions:

- custom Alfred API  
- higher-level state machine (behavior trees)  
- logging pipeline to NOVA  

---

## 🔮 Planned Upgrades
- Full Nav2 navigation  
- IMU integration  
- Autonomous mapping  
- Autonomous docking station  
- Custom PCB  
- CNC aluminum frame with logo cutouts

---

## 🗓 Development Roadmap
- **2025 Q4:** Motor control + encoder odometry  
- **2026 Q1:** LIDAR mapping + camera integration  
- **2026 Q2:** Nav2 testing  
- **2026 Q3:** Alfred API + behavior modes  

