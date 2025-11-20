NOVAgrid – System Overview (v1.0)

Owner: AstroGear Labs (Eric)
Core Theme: Unified robotics + home automation ecosystem anchored around a central AI hub (NOVA), multiple robots (Alfred family, Oscar, Moe/Larry/Curly), and a distributed NOVAgrid sensor network.

1. Purpose

NOVAgrid is the umbrella architecture for:

All robots (indoor, outdoor, experimental)

The central AI brain (NOVA)

Home automation (Home Assistant)

Distributed IoT nodes (ESP/Arduino/Pico devices)

Dev workstations (Pedro, Jose)

The long-term goal is to create a cohesive, branded ecosystem where robots, sensors, and automation cooperate, rather than existing as separate one-off projects.

2. High-Level Layers

NOVAgrid is organized into four logical layers:

Core Compute Layer

Mobile Robotics Layer

IoT / Nodes Layer

Automation & Environment Layer

3. Core Compute Layer
3.1 NOVA – Central AI Hub

Hardware: Peladn Mini PC + 32" display

OS/Stack: Ubuntu + ROS 2 Jazzy + Piper TTS

Responsibilities:

Central ROS 2 master/coordination point

High-level planning, logging, visualization (rviz2)

Running core AI logic, map storage, multi-robot coordination

Provides TTS for robots and systems

Bridges to Home Assistant and NOVAgrid nodes

3.2 Pedro – Main Engineering Workstation

Hardware: Windows desktop

Role:

CAD (mechanical design, enclosures, frames)

KiCad PCB design

Documentation (plans, specs, PDFs)

Git/GitHub management

Video editing, media for AstroGear Labs

Note: No ROS2; Pedro is for design and dev, not runtime robotics.

3.3 Jose – Field Development Laptop

Hardware: Dell laptop

OS: Ubuntu + ROS 2 Jazzy

Role:

Mobile ROS2 dev and debugging

Live rviz2, teleop, and monitoring

Flashing firmware to Arduinos/ESPs

On-site diagnostics for Alfred 1, Alfred 5, Oscar, etc.

4. Automation & Environment Layer
4.1 Home Assistant

Hardware: Peladn bare-metal HA box

Role:

Manages home sensors (Zigbee, Wi-Fi, etc.)

Tracks energy, doors, motion, environmental data

Exposes data to NOVA/robots (future integrations)

Executes automations like alerts, TTS to speakers, etc.

Home Assistant + NOVA = environment-aware robots (robots react to the house, not just local sensors).

5. Mobile Robotics Layer
5.1 Alfred 1 – Small Development Rover

Hardware: Raspberry Pi 5 + SSD, JGA25-371 motors w/ encoders, TB6612FNG, LIDAR, camera

Stack: Ubuntu 24.04 + ROS 2 Jazzy

Role:

Primary learning and prototyping platform

Indoor navigation, mapping, and control experiments

Base for ROS 2 nodes, perception, and motion control

Portfolio robot showing “full stack” robotics capability

5.2 Alfred 5 – Indoor Butler Robot

Hardware: Raspberry Pi 5 + SSD, wheelchair motors, high-current drivers (IBT-2), LIDAR, camera

Role:

Indoor butler-style robot

Navigation in the home

Delivery/fetch tasks and eventual arm/hand integration

Main “hero” robot for AstroGear Labs

5.3 Moe – Mini Rover

Platform: Adafruit Feather, RC chassis

Role:

Lightweight, fun rover

Good for simple sensor experiments and demos

5.4 Larry – Rover 1

Platform: Pi Zero 2 W, micro-ROS

Role:

Low-power rover for experiments

Testing micro-ROS and small ROS nodes

5.5 Curly – Rover 2

Platform: Raspberry Pi 3B+

Role:

Mid-range rover for mapping and more capable experiments

5.6 Oscar – Zero-Turn Lawn Rover

Hardware: Raspberry Pi 5, hoverboard hub motors, BLDC drivers (VESC-type), rugged chassis

Role:

Outdoor autonomous mower

Zero-turn skid steer behavior

Obstacle detection via sensors/LIDAR

Long-term: GPS + safety layers for real cutting

6. IoT / NOVAgrid Nodes Layer
6.1 Skully – Animatronic Skull

Platform: Raspberry Pi 4

Stack: Rhasspy + Piper

Role:

Personality/voice node in NOVAgrid

Facial motion, LEDs, jaw movement

Local speech input/output

6.2 Arachno / Spyder – Camera Node

Platform: ESP32-CAM / M5Stack camera

Role:

Video stream and/or face detection

Sends events to Skully/NOVA

Controlled via MQTT/HTTP

6.3 NOVAgrid Sensor Nodes

Hardware: ESP32, ESP01, Raspberry Pi Picos, Arduinos, custom boards

Role:

Environmental sensors (temp, humidity, light, motion)

Power and current monitoring

Door and window status

Robot localization aids (beacons, tags)

Input to both Home Assistant and NOVA

7. Networking & Communication (High-Level)

Robots ↔ NOVA: ROS 2 over Wi-Fi/Ethernet

NOVA ↔ Home Assistant: API/Websocket/MQTT (future integration)

NOVA ↔ Skully / Spyder / Nodes: MQTT, HTTP, or custom lightweight protocols

Jose ↔ Robots/NOVA: SSH, rviz2 remote, ROS CLI tools

Pedro ↔ Everything: Git pulls, file shares, documentation sync

(A more detailed ROS2 topic/service/action map can be a v2 document.)

8. Build Priority / Roadmap (Short)

Alfred 1 – get it mechanically finished and moving under ROS2.

NOVA + Jose solid – stable ROS2 dev cycle, rviz2, teleop.

Home Assistant + a few NOVAgrid nodes – house data coming in.

Oscar basic platform – hoverboard drive working, remote control, then autonomy.

Alfred 5 framing + drive – wheelchair motors driving, base nav.

Skully + Spyder integrated with NOVA – personality + vision node.
