# Multi-Robot Search and Rescue Using Deep Image Processing, SLAM, AMCL, and Optimized Communication

This repository contains the code, models, and documentation for the thesis titled:

**"Optimizing Multi-Robot Collaboration Using Deep Image Processing and Communication Protocols for Search and Rescue Operations"**

## 📖 Overview

This research proposes a modular, scalable system for autonomous multi-robot search and rescue (SAR) operations in disaster environments. The system leverages:

- **Deep Learning** (for real-time victim and obstacle detection using CNNs)
- **SLAM (Simultaneous Localization and Mapping)** (for environment mapping)
- **AMCL (Adaptive Monte Carlo Localization)** (for robust robot localization)
- **Optimized Communication Protocols** (for efficient, real-time data sharing)
- **Multi-Robot Coordination** (for distributed task allocation and path planning)

## 🎯 Objectives

- Enable real-time visual detection of victims/obstacles via CNN-based processing.
- Share only mission-critical information to reduce bandwidth usage.
- Improve localization and mapping in GPS-denied environments using SLAM and AMCL.
- Maximize area coverage and minimize redundancy in multi-robot navigation.

## 🧠 Key Skills & Technologies

| Skill/Tech                      | Application                                      |
|-------------------------------|--------------------------------------------------|
| Python & ROS (Robot Operating System) | Robot programming and middleware integration      |
| OpenCV                         | Image acquisition and preprocessing              |
| TensorFlow / PyTorch           | Deep learning-based victim detection (CNN)       |
| GMapping / Cartographer SLAM   | 2D SLAM implementation for dynamic environments  |
| AMCL (ROS Package)             | Particle filter-based robot localization         |
| MQTT / ROS2 DDS                | Lightweight, efficient robot-to-robot communication |
| Multi-threading / Async I/O    | Real-time data handling and synchronization      |
| A* / Dijkstra / RRT            | Path planning and obstacle avoidance algorithms  |
| Gazebo / RViz                  | Simulation and visualization                     |
| Git                            | Version control and collaboration                |

## 🧪 System Architecture

```plaintext
+------------------+     Image Feed     +------------------+
|   Robot Camera   | -----------------> |   CNN Detector   |
+------------------+                    +------------------+
                                                |
                                        Detected Info (Victims, Obstacles)
                                                |
                              +-----------------v------------------+
                              | Communication Manager (ROS/MQTT)   |
                              +-----------------+------------------+
                                                |
                          +---------------------v----------------------+
                          | Task Allocator & Multi-Robot Coordinator  |
                          +---------------------+----------------------+
                                                |
                           +--------------------v-------------------+
                           | SLAM + AMCL Based Localization & Map   |
                           +----------------------------------------+
