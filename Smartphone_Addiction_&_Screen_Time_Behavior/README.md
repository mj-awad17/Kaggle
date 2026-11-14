# 📱 Smartphone Addiction & Digital Behavior Dataset

<p align="center">
  <strong>Understanding Smartphone Usage Patterns, Digital Dependency, and Their Impact on Everyday Life</strong>
</p>

<p align="center">
  <a href="https://github.com/YOUR_USERNAME/YOUR_REPOSITORY">
    <img src="https://img.shields.io/badge/⭐_Star_This_Repository-Support_The_Project-yellow?style=for-the-badge" alt="Star Repository"/>
  </a>
  <a href="YOUR_DATASET_LINK">
    <img src="https://img.shields.io/badge/📊-Explore_Dataset-blue?style=for-the-badge" alt="Explore Dataset"/>
  </a>
  <a href="https://github.com/YOUR_USERNAME/YOUR_REPOSITORY/fork">
    <img src="https://img.shields.io/badge/🍴-Fork_Repository-success?style=for-the-badge" alt="Fork Repository"/>
  </a>
</p>

<p align="center">
  <img src="Children Surrounded by Digital Holograms.png" alt="Smartphone Addiction Dataset Banner" width="100%"/>
</p>

## 📌 Overview

Smartphones have become an essential part of modern life, influencing how people communicate, study, work, entertain themselves, and interact with the digital world.

However, excessive smartphone usage may be associated with various behavioral and lifestyle challenges, including sleep disruption, reduced productivity, stress, and difficulties maintaining a healthy digital balance.

The **Smartphone Addiction & Digital Behavior Dataset** is designed to support the exploration of smartphone usage patterns and their potential relationship with digital dependency.

This dataset provides demographic information, daily smartphone usage statistics, social media engagement, gaming behavior, sleep patterns, notification frequency, application interaction frequency, and self-reported lifestyle indicators.

It offers opportunities for researchers, students, data analysts, and machine learning enthusiasts to investigate digital behavior through data-driven approaches.

## 📊 Dataset Information

| Property | Details |
|---|---|
| Dataset Name | Smartphone Addiction & Digital Behavior |
| Total Records | 691,369 |
| Total Original Columns | 14 |
| Data Format | Excel (.csv) |
| Data Category | Behavioral & Lifestyle Data |
| Target Variable | `addicted_label` |
| Machine Learning Type | Classification |
| Primary Application | Data Analysis & Predictive Modeling |

## 📂 Dataset Features

The dataset contains 14 original attributes covering demographic, behavioral, and lifestyle-related information.

| No. | Column Name | Description |
|---|---|---|
| 1 | `id` | Unique identifier assigned to each dataset record. |
| 2 | `age` | Age of the individual in years. |
| 3 | `daily_screen_time_hours` | Total daily smartphone screen time, measured in hours. |
| 4 | `social_media_hours` | Daily time spent using social media applications. |
| 5 | `gaming_hours` | Daily time spent playing mobile games. |
| 6 | `work_study_hours` | Time dedicated to work or study activities. |
| 7 | `sleep_hours` | Recorded sleeping duration in hours. |
| 8 | `notifications_per_day` | Number of smartphone notifications received daily. |
| 9 | `app_opens_per_day` | Number of times smartphone applications are opened daily. |
| 10 | `weekend_screen_time` | Smartphone screen time recorded for weekends. |
| 11 | `gender` | Gender category recorded for the individual. |
| 12 | `stress_level` | Self-reported stress category. |
| 13 | `academic_work_impact` | Indicates whether smartphone usage has an impact on academic or professional activities. |
| 14 | `addicted_label` | Binary target variable representing the recorded smartphone addiction classification. |

## 🎯 Target Variable

The dataset includes a target column:

**`addicted_label`**

This variable can be used to develop binary classification models that investigate smartphone addiction patterns.

| Value | Description |
|---|---|
| 0 | Negative class |
| 1 | Positive class |

*The precise operational definition of these labels should be confirmed using the dataset's original labeling methodology.*

## 🔍 Potential Research Questions

This dataset can help explore several interesting research questions:

- Does increased daily screen time have an association with smartphone addiction?
- Is excessive social media consumption associated with digital dependency?
- How do smartphone usage patterns relate to sleeping habits?
- Does notification frequency influence smartphone checking behavior?
- Is there a relationship between stress levels and smartphone dependency?
- How does smartphone usage affect academic and professional productivity?
- Are smartphone addiction patterns different across age groups?
- Does gaming behavior contribute to differences in smartphone usage patterns?

## 🧹 Data Preparation & Quality Considerations

Before conducting statistical analysis or building machine learning models, some data preparation steps may be necessary.

Recommended preprocessing:

1. **Missing Value Treatment:** Identify and appropriately handle missing observations.
2. **Data Type Validation:** Ensure numerical columns contain valid numerical values.
3. **Outlier Detection:** Investigate unusual observations in screen time, sleep duration, and other numerical variables.
4. **Categorical Encoding:** Encode categorical variables such as gender and stress level when required.
5. **Feature Scaling:** Apply appropriate scaling techniques for models that require normalized numerical features.
6. **Class Distribution Analysis:** Examine the distribution of `addicted_label`.
7. **Train-Test Split:** Separate training and testing data before model development.

Some initial records contain missing values and invalid entries, so the dataset should not be assumed to be completely clean.

## 🤖 Machine Learning Applications

The dataset can be used for different machine learning experiments, including:

| Algorithm | Potential Application |
|---|---|
| Logistic Regression | Baseline addiction classification |
| Decision Tree | Understanding behavioral decision patterns |
| Random Forest | Predicting addiction categories |
| XGBoost | Advanced classification |
| Support Vector Machine | Classification experiments |
| K-Nearest Neighbors | Similarity-based classification |

**Important:** Model performance should be evaluated using appropriate metrics such as accuracy, precision, recall, F1-score, and ROC-AUC.

## 📈 Data Visualization Opportunities

The dataset also provides opportunities to create interactive dashboards and analytical reports.

Suggested visualizations:

- Daily Screen Time Distribution
- Smartphone Addiction by Age Group
- Social Media vs. Gaming Usage
- Sleep Duration and Screen Time Relationship
- Stress Level vs. Addiction Classification
- Notifications and Application Opening Frequency
- Academic and Work Impact Analysis
- Addiction Class Distribution

These visualizations can be developed using Python, Matplotlib, Seaborn, Plotly, or Power BI.

## 🛠️ Tools & Technologies

The following technologies can be used to explore and analyze the dataset:

- **Python:** Data analysis and machine learning.
- **Pandas:** Data manipulation and preprocessing.
- **NumPy:** Numerical operations.
- **Matplotlib & Seaborn:** Statistical visualization.
- **Scikit-learn:** Machine learning experiments.
- **Power BI:** Interactive dashboard development.
- **Jupyter Notebook:** Exploratory data analysis.

## 🚀 Getting Started

You can begin exploring the dataset using Python.

```python
import pandas as pd

# Load the dataset
df = pd.read_excel("Smartphone Addiction.xlsx")

# Display dataset dimensions
print("Dataset Shape:", df.shape)

# Preview records
print(df.head())

# Inspect data types and missing values
print(df.info())

# Generate descriptive statistics
print(df.describe(include="all"))

# Check missing values
print(df.isnull().sum())
```

## ⚠️ Important Notes

- The dataset contains behavioral and lifestyle-related information.
- Statistical associations should not automatically be interpreted as causal relationships.
- The addiction classification should not be treated as a clinical diagnosis.
- Missing values, invalid entries, and unusual observations should be investigated before analysis.
- Any additional survey-based or engineered features should be clearly distinguished from the original dataset attributes.
- Machine learning results should be interpreted with appropriate attention to data quality, class imbalance, and potential bias.

## 🌍 Who Can Use This Dataset?

This dataset may be useful for:

- Data Science Students
- Machine Learning Enthusiasts
- Academic Researchers
- Behavioral Data Analysts
- Digital Wellness Researchers
- Data Visualization Developers
- Predictive Modeling Projects

## 🤝 Contributions & Community

Contributions, suggestions, improvements, and new analytical approaches are welcome!

If you find this dataset useful for your research, academic projects, dashboards, or machine learning experiments, consider contributing to its development.

You can contribute by:

- Suggesting additional research questions.
- Developing new visualization techniques.
- Exploring machine learning algorithms.
- Improving data preprocessing methods.
- Sharing interesting analytical findings.

## ⭐ Support This Project

If you find this dataset interesting or useful, please consider giving this repository a **STAR ⭐**!

Your support helps increase the project's visibility, encourages further development, and motivates the community to explore digital behavior and smartphone addiction through data science.

**Found this dataset useful? Don't forget to ⭐ Star the repository and share it with fellow data science enthusiasts!**

---

<p align="center">
  <strong>📱 Explore Digital Behavior. Discover Patterns. Build Insights.</strong>
</p>

<p align="center">
  Made for the Data Science & Machine Learning Community ❤️
</p>