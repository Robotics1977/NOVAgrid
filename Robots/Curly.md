# 🤖 Curly — Rover 2
**Platform:** Raspberry Pi 3B+  
**Role:** Larger, heavier NKOK rover  
**OS / Stack:** ROS 2 Humble/Iron  
**Communication:** Full ROS 2 network  
**Status:** Planned

---

## 📘 Overview
Curly is the larger sibling to Larry, built on the same RC chassis family but with more power, more onboard compute, and room for expansions.

He is your mid-tier rover for small indoor or outdoor tasks.

---

## 🔩 Hardware (Planned)
| Component | Notes |
|----------|-------|
| **Raspberry Pi 3B+** | Bigger compute than Larry |
| RC chassis | Larger NKOK model |
| Motor driver | TB6612 or similar |
| Camera module | Optional CV tests |
| Ultrasonic sensors | Basic obstacle detection |
| LiPo battery | Power |

---

## 🧠 Software Architecture
- ROS 2 base nodes  
- Optional Nav2 Lite  
- Camera streaming  
- Remote control via teleop  

---

## 🔮 Planned Features
- Mapping via 2D lidar (optional)  
- Mini manipulator (optional)  
- MQTT telemetry  

---


