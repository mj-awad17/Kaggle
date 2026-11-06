<<<<<<< HEAD
# Basketball Injury & Biomechanical Dataset

[![Kaggle Dataset](https://img.shields.io/badge/Kaggle-Dataset-blue?style=for-the-badge&logo=kaggle)](https://www.kaggle.com/datasets/mjwad17)
[![Topic](https://img.shields.io/badge/Domain-Sports%20Analytics%20%26%20Healthcare-green?style=for-the-badge)](#)
<!-- [![License](https://img.shields.io/badge/License-CC%20BY%204.0-orange?style=for-the-badge)](https://creativecommons.org/licenses/by/4.0/) -->

<p align="center">
  <img src="thumbnail_for_Basketball_Injury_Analytics_._In_the_cent-0.jpg" alt="PSEB AI Engineering Bootcamp Banner" width="100%" style="border-radius: 10px; box-shadow: 0 4px 8px rgb(46, 253, 0);">
</p>

## 📌 Dataset Overview

**Title:** Basketball Injury & Biomechanical Dataset  
**Subtitle:** Analyze player kinematics, rehab efficiency, and injury recurrence risks.

Sports injury prevention and physical rehabilitation are critical components of modern high-performance athletics. In basketball, explosive dynamic movements—such as jumping, rapid deceleration, and sharp directional cutting—place immense physical strain on the musculoskeletal system. 

This dataset provides a comprehensive collection of **206 player records**, detailing physical profiles, biomechanical measurement indicators during movements, specific injury diagnoses, environmental circumstances, and subsequent rehabilitation program outcomes.

---

## 💡 Key Features & Metrics

The dataset captures multi-dimensional attributes divided into key domains:

* **Player Demographics:** Age, Height ($cm$), Weight ($kg$), and Player Position (`Guard`, `Forward`, `Center`).
* **Medical Profile:** Injury Type (e.g., `ACL Tear`, `Ankle Sprain`, `Hamstring Strain`), Severity Level (`Mild`, `Moderate`, `Severe`), Date of Injury, and Historical Injury Count.
* **Biomechanical Indicators:** High-frequency movement tracking data including:
  * Knee joint flexion angle ($\text{knee\_angle\_deg}$)
  * Ankle dorsiflexion angle ($\text{ankle\_flexion\_deg}$)
  * Vertical jump height ($\text{jump\_height\_cm}$)
  * Dynamic movement speed ($\text{speed\_m\_s}$)
  * Neuromuscular reaction time ($\text{reaction\_time\_ms}$)
* **Rehabilitation Tracking:** Specific rehabilitation protocols, recovery duration ($\text{weeks}$), continuous recovery efficiency scores ($0.0$ to $1.0$), and binary recurrence outcomes ($0$ or $1$).



## 🚀 Recommended Tasks & Analytics Ideas

1. **Injury Recurrence Prediction (Binary Classification):**
   * Build ML models (e.g., XGBoost, LightGBM, Random Forest) to predict whether an injury will recur ($\text{Injury\_Recurrence} = 1$) using joint kinematics and rehab duration.

2. **Rehabilitation Efficiency Optimization (Regression):**
   * Predict the continuous variable $\text{Rehabilitation\_Efficiency\_Score}$ based on player physical parameters and chosen therapy programs.

3. **Biomechanics Clustering & Risk Stratification:**
   * Apply unsupervised techniques (K-Means, Hierarchical Clustering) on joint angles and reaction speeds to categorize players into distinct movement profile risk tiers.

4. **Exploratory Data Analysis (EDA):**
   * Investigate correlations between dynamic parameters (e.g., jump height vs. knee flexion angle) across different playing positions.


## 📁 File Structure

| File Name | Format | Dimensions | Description |
| :--- | :--- | :--- | :--- |
| `basketball_injury_biomechanical_dataset.csv` | CSV | 206 rows $\times$ 19 columns | Main tabular dataset containing player physical attributes, kinematics, injury records, and rehabilitation outcomes. |



## 📊 Data Dictionary / Column Descriptions

| Column Name | Data Type | Range / Values | Description |
| :--- | :--- | :--- | :--- |
| `Player_ID` | Integer | $1 - 206$ | Unique identifier for each player record. |
| `Age` | Integer | $18 - 34$ years | Player's age at the time of assessment. |
| `Height_cm` | Integer | $167 - 209\text{ cm}$ | Player height measured in centimeters. |
| `Weight_kg` | Integer | $70 - 109\text{ kg}$ | Player body weight measured in kilograms. |
| `Position` | String | `Guard`, `Forward`, `Center` | Player's primary court position. |
| `Injury_Type` | String | `ACL Tear`, `Ankle Sprain`, etc. | Diagnosis of the primary recorded injury. |
| `Injury_Severity` | String | `Mild`, `Moderate`, `Severe` | Clinical rating of injury severity. |
| `Rehabilitation_Program` | String | `Physiotherapy`, `Strength Training`, etc. | Protocol applied during recovery. |
| `Rehabilitation_Time_weeks` | Integer | $2 - 11\text{ weeks}$ | Total duration of the rehabilitation period. |
| `Injury_Recurrence` | Binary | $0$ (No), $1$ (Yes) | Indicator if the injury reoccurred post-recovery. |
| `Previous_Injuries_Count` | Integer | $0 - 10$ | Total prior documented sports injuries. |
| `Environmental_Condition` | String | `Indoor`, `Outdoor`, `Cold`, etc. | Playing environment context during injury. |
| `Date_of_Injury` | Date | `MM/DD/YYYY` | Date the injury was sustained. |
| `Rehabilitation_Efficiency_Score` | Float | $0.0 - 1.0$ | Normalized index of rehabilitation recovery success. |
| `knee_angle_deg` | Float | $0.0^\circ - 100.0^\circ$ | Measured biomechanical knee joint flex angle. |
| `jump_height_cm` | Float | Continuous | Maximum vertical jump achieved during testing. |
| `ankle_flexion_deg` | Float | $0.0^\circ - 100.0^\circ$ | Measured ankle dorsiflexion angle. |
| `speed_m_s` | Float | Continuous | Peak movement speed captured during dynamic tests ($m/s$). |
| `reaction_time_ms` | Float | Continuous | Measured neuromuscular reaction time ($ms$). |

---

<!-- ## 🌐 Provenance & Metadata

* **Data Collection Method:** Synthesized and modeled based on clinical patterns in sports medicine, wearable biomechanical sensor metrics, and basketball player injury tracking logs.
* **Cleaning & Preprocessing:** Sanitized for missing data, standard feature naming formats applied, and numeric scales regularized.
* **License:** Creative Commons Attribution 4.0 International ([CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)).

--- -->

<!-- ## 🎨 Cover Image Prompt

If you need to generate a cover image or thumbnail for your Kaggle dataset page, use this prompt:

> **Prompt:** *A high-tech digital illustration of a basketball player in mid-jump on a dark court, featuring holographic biomechanical skeleton overlays, joint angle vectors, motion tracking heatmaps around the knees and ankles, futuristic neon blue and glowing orange data nodes, highly detailed, 4k resolution, cinematic lighting, sleek sports analytics dashboard aesthetic.* -->
=======
>>>>>>> 385d9e10cb4d467240084483fcda1e92e4cab427
