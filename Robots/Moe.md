🤖 Moe — Mini Rover

Platform: Adafruit Feather ESP32 + Music Maker FeatherWing
Role: Mini rover with audio capability
OS / Stack: Arduino (C++)
Communication: MQTT
Status: In development

📘 Overview

Moe is a compact rover powered by an ESP32-based Adafruit Feather board and the Adafruit Music Maker FeatherWing, making him the only robot in NOVAgrid with built-in sound playback.

He is designed for:

lightweight autonomous experiments

MQTT communication with NOVA

testing small-scale sensor integration

robot "personality" behaviors through audio

Moe represents the smallest but most expressive mobile robot in the NOVAgrid ecosystem.

🔩 Hardware
Core Components
Component	Notes
Adafruit Feather ESP32	Primary controller
Music Maker FeatherWing	REQUIRED — audio playback module
Motor driver	L298N / TB6612FNG (TBD)
Ultrasonic sensor	HC-SR04, primary obstacle sensing
Mini RC chassis	2-wheel drivetrain
Battery	TBD
📡 Communication (MQTT)

Moe uses MQTT over Wi-Fi to connect to NOVA.

MQTT Topics — Publish
Topic	Payload
moe/status	online / offline / battery / error
moe/distance	ultrasonic readings
MQTT Topics — Subscribe
Topic	Command
moe/cmd/move	forward, stop, (later: left/right/back)
moe/cmd/sound	play sound name / sound ID
moe/cmd/reboot	ESP32 software reboot
🧠 Firmware Architecture (Arduino)

The firmware runs in layers:

Wi-Fi setup

MQTT connect and keepalive

Ultrasonic sensor loop

Motor control loop

Sound handler for Music Maker module

Command dispatcher for incoming MQTT messages

A minimal structure:

void loop() {
    handleMQTT();
    readSensors();
    publishStatus();
}


(A full firmware folder can be added later.)

🔮 Planned Upgrades

Add IMU for better motion tracking

Add OTA updates via ArduinoOTA

Add bump sensors

Add "personality mode" using random sound triggers

Add LED indicators

🗓 Development Roadmap

2025 Q4: Basic MQTT communication

2026 Q1: Motor control + audio playback

2026 Q2: Test autonomy behaviors

2026 Q3: Integration with NOVA dashboard
