# 🏐 Volleyball Smart Sensors & Biometrics Dataset

[![Dataset Status](https://img.shields.io/badge/Dataset-Complete-brightgreen.svg)](#)
[![License: CC0 1.0](https://img.shields.io/badge/License-CC0--1.0-yellow.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
[![Domain](https://img.shields.io/badge/Domain-Sports%20Analytics%20%7C%20IoT-blue.svg)](#)
[![Data Type](https://img.shields.io/badge/Type-Synthetic-orange.svg)](#)

Welcome to the **Volleyball Smart Sensors & Biometrics Dataset** repository! 🚀 This dataset provides 1,462 synthetically generated telemetry records, physiological measurements, and performance tracking metrics across 25 players and 10 structured training sessions.

<!-- ---

## 📌 Subtitle
> *Simulated IMU telemetry, biomechanics & player performance logs*

--- -->

## 📖 Description & Context

### 💡 Context
Modern sports analytics relies heavily on inertial measurement units (IMUs), biometric monitors, and computer vision feedback loops to quantify athletic performance. Volleyball is a fast-paced sport requiring explosive movements, precise mechanics, and quick reaction times. 

Real-world athletic sensor data is often proprietary or restricted due to privacy concerns. This dataset provides a clean, standardized telemetry environment mimicking wearable sensors and biometric devices used during professional volleyball training drills.

### 🎯 Inspiration
This repository empowers data scientists, machine learning engineers, and sports analysts to:
- 🔮 **Predict performance ratings and movement execution quality** based on sensor dynamics.
- 🎯 **Classify volleyball movement types** (`Serve`, `Spike`, `Block`, `Dig`) using multi-axis accelerometer and gyroscope telemetry.
- 📈 **Model impact kinematics** such as landing forces, jump heights, and ball contact velocities against player fatigue metrics.

<!-- ---

## 🏷️ Tags
`synthetic-data` • `sports` • `tabular` • `time-series` • `classification` • `regression` • `biometrics`

--- -->

## 📁 File Structure

| File Name | Description |
| :--- | :--- |
| 📄 `volleyball_training_data.csv` | Contains 1,462 synthetic movement records, body orientations, telemetry metrics, movement labels, and AI-assisted coaching tips. |


## 🔬 Feature Dictionary (Column Descriptors)

### 👤 Player & Session Identifiers
- 🆔 `player_id`: Unique identifier for each simulated athlete (`P001`–`P025`).
- 📌 `session_id`: Identifier for the training session block (`S001`–`S010`).
- 🕒 `timestamp`: Programmatically generated date and time for each recorded sample.

### 🫀 Biometrics & Physiological State
- ❤️ `heart_rate_bpm`: Real-time simulated heart rate in beats per minute (BPM).
- 🌡️ `skin_temp_c`: Simulated skin temperature in degrees Celsius (°C).

### ⚡ Wearable Sensor Telemetry (IMU)
- 📐 `accel_x` / `accel_y` / `accel_z`: Tri-axial accelerometer readings on X, Y, and Z axes ($g$).
- 🔄 `gyro_x` / `gyro_y` / `gyro_z`: Gyroscope angular velocity around X, Y, and Z axes (°/s).

### 🏃 Kinematics & Execution Metrics
- 🦶 `foot_placement_angle_deg`: Angle of foot placement relative to the baseline (degrees).
- 🦾 `swing_angle_deg`: Arm swing angle execution during spike or serve mechanics (degrees).
- 🚀 `jump_height_cm`: Vertical jump elevation achieved during the action (centimeters).
- 🏐 `movement_label`: Categorical movement type performed (`Serve`, `Spike`, `Block`, `Dig`).

### 💥 Impact & Ball Interaction
- ⚡ `ball_impact_velocity_kmh`: Speed of the ball upon striking/contact (km/h).
- ⏱️ `ball_contact_time_ms`: Duration of hand-to-ball impact contact (milliseconds).
- 📉 `landing_force_g`: Peak vertical g-force experienced upon landing.
- ⚡ `reaction_latency_ms`: Response time to incoming play stimulus (milliseconds).

### 🎯 Coaching & Performance Feedback
- ⭐ `feedback_score`: Normalized performance evaluation score ($0.80$ to $1.00$).
- 💡 `recommended_adjustment`: Rule-based coaching advice generated for technique correction.


## 🏗️ Provenance

### 📍 Sources
This is a purely synthetic dataset generated programmatically using statistical distributions and rule-based logic designed to mirror professional volleyball wearable sensor outputs (IMU telemetry, chest-strap heart rate monitors, and motion capture systems).

### ⚙️ Collection Methodology
The data was synthetically generated via a custom simulation script configured to model 25 distinct player profiles across 10 training sessions. Telemetry values (accelerometer, gyroscope, biometrics) were sampled from controlled probabilistic distributions, while movement labels, impact velocities, and coaching recommendations were programmatically mapped to simulate realistic athletic training drills and performance variance.


## 🌟 Call to Action & Community Encouragement

Whether you are a **student**, **data analyst**, **machine learning engineer**, or **sports tech researcher**, this dataset offers a rich playground for exploration! 🎨✨

Here are a few ways you can dive in:
1. **EDA & Visualizations**: Build dashboards comparing jump heights and landing forces across different position movements.
2. **Predictive Modeling**: Train regression models to estimate `feedback_score` or predict `landing_force_g`.
3. **Multi-Class Classification**: Build classifiers to identify action types (`Serve`, `Spike`, `Block`, `Dig`) using pure accelerometer/gyroscope signals.

> 🤝 **Show Your Support!**  
> If you find this dataset helpful for your projects, learning journey, or research, please consider giving this repository a ⭐ **Star** on GitHub and sharing your notebooks and insights with the community! Happy coding and modeling! 🚀🎉