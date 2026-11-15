# 🇵🇰 Pakistan Petrol Prices (2013–2026)

### Historical Weekly Petrol Prices Across 17 Major Cities of Pakistan

<p align="center">
  <a href="https://psopk.com/fuel-prices/pol/archives">
    <img src="https://img.shields.io/badge/Data%20Source-Pakistan%20State%20Oil-blue?style=for-the-badge" alt="Data Source"/>
  </a>
  <a href="https://www.kaggle.com/mjwad17/datasets">
    <img src="https://img.shields.io/badge/Platform-Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white" alt="Kaggle"/>
  </a>
  <a href="https://github.com/mjwad17/Kaggle">
    <img src="https://img.shields.io/badge/⭐%20Star%20Repository-GitHub-black?style=for-the-badge&logo=github" alt="Star Repository"/>
  </a>
</p>

---

## 📌 Overview

The **Pakistan Petrol Prices (2013–2026)** dataset provides historical weekly petrol price information across 17 major cities of Pakistan, together with a national-level price indicator.

The dataset covers approximately 13 years of historical records, from January 2013 to March 2026, making it a useful resource for understanding long-term fuel price movements and geographical differences in petrol prices.

All petrol prices are represented in Pakistani Rupees (PKR).

This dataset is designed for data analysts, researchers, students, economists, and machine learning enthusiasts interested in exploring Pakistan's historical fuel price trends.

## 📊 Dataset Highlights

- **Time Period:** January 2013 – March 2026
- **Total Observations:** 626 weekly records
- **Geographical Coverage:** 17 major Pakistani cities
- **Additional Indicator:** Pakistan national-level price
- **Reporting Frequency:** Weekly
- **Currency:** Pakistani Rupee (PKR)
- **File Format:** CSV
- **Total Features:** 19 columns

## 📁 Dataset Structure

The dataset contains one CSV file:

| File Name | Description |
|---|---|
| `Petrol Price.csv` | Historical weekly petrol prices across 17 Pakistani cities and the national price indicator. |

## 🗺️ Geographical Coverage

The dataset includes petrol price information for the following locations:

1. Islamabad
2. Rawalpindi
3. Gujranwala
4. Sialkot
5. Lahore
6. Faisalabad
7. Sargodha
8. Multan
9. Bahawalpur
10. Karachi
11. Hyderabad
12. Sukkur
13. Larkana
14. Peshawar
15. Bannu
16. Quetta
17. Khuzdar

An additional `Pakistan` column represents the national-level petrol price indicator.

## 📋 Column Descriptions

| Column | Description |
|---|---|
| Period End | Ending date of the weekly reporting period. |
| Islamabad | Petrol price in Islamabad (PKR). |
| Rawalpindi | Petrol price in Rawalpindi (PKR). |
| Gujranwala | Petrol price in Gujranwala (PKR). |
| Sialkot | Petrol price in Sialkot (PKR). |
| Lahore | Petrol price in Lahore (PKR). |
| Faisalabad | Petrol price in Faisalabad (PKR). |
| Sargodha | Petrol price in Sargodha (PKR). |
| Multan | Petrol price in Multan (PKR). |
| Bahawalpur | Petrol price in Bahawalpur (PKR). |
| Karachi | Petrol price in Karachi (PKR). |
| Hyderabad | Petrol price in Hyderabad (PKR). |
| Sukkur | Petrol price in Sukkur (PKR). |
| Larkana | Petrol price in Larkana (PKR). |
| Peshawar | Petrol price in Peshawar (PKR). |
| Bannu | Petrol price in Bannu (PKR). |
| Quetta | Petrol price in Quetta (PKR). |
| Khuzdar | Petrol price in Khuzdar (PKR). |
| Pakistan | National-level petrol price indicator (PKR). |

## 🔍 Potential Applications

This dataset can be used for several analytical and research purposes:

### 1. Exploratory Data Analysis (EDA)
- Analyze historical petrol price movements.
- Identify periods of significant price increases and decreases.
- Explore price distributions across different cities.

### 2. Regional Price Comparison
- Compare petrol prices between major Pakistani cities.
- Identify geographical price differences.
- Investigate regional pricing patterns.

### 3. Time-Series Analysis
- Study long-term petrol price trends.
- Identify seasonal or recurring patterns.
- Examine historical price fluctuations.

### 4. Machine Learning & Forecasting
- Develop petrol price prediction models.
- Experiment with time-series forecasting techniques.
- Compare forecasting approaches such as ARIMA, Prophet, and LSTM.

### 5. Economic Research
- Explore historical fuel price movements.
- Support research into transportation and energy economics.
- Investigate relationships between petrol prices and broader economic indicators using additional datasets.

## 🛠️ Getting Started

You can load and explore this dataset using Python and Pandas.

### Requirements

```bash
pip install pandas numpy matplotlib seaborn
```

### Load the Dataset

```python
import pandas as pd

# Load dataset
df = pd.read_csv("Petrol Price.csv")

# Display first five rows
print(df.head())

# Dataset information
print(df.info())
```

### Data Preparation

The original file contains a metadata row indicating the reporting frequency (`Weekly`) and currency (`PKR`). Remove this row before numerical analysis.

```python
# Remove metadata row
df = df.iloc[1:].copy()

# Convert date column
df["Period End"] = pd.to_datetime(
    df["Period End"],
    format="%d-%b-%y"
)

# Convert petrol price columns to numeric
price_columns = df.columns.drop("Period End")

df[price_columns] = df[price_columns].apply(
    pd.to_numeric,
    errors="coerce"
)

# Sort chronologically
df = df.sort_values("Period End").reset_index(drop=True)

print(df.head())
print(df.info())
```

### Visualize Petrol Price Trends

```python
import matplotlib.pyplot as plt

plt.figure(figsize=(14, 6))

plt.plot(
    df["Period End"],
    df["Pakistan"],
    label="Pakistan",
    linewidth=2
)

plt.title("Historical Petrol Prices in Pakistan (2013–2026)")
plt.xlabel("Year")
plt.ylabel("Petrol Price (PKR)")
plt.legend()
plt.grid(alpha=0.3)

plt.tight_layout()
plt.show()
```

## 📚 Data Source

The dataset is based on historical petrol price information published by **Pakistan State Oil (PSO)**.

Official Source:

https://psopk.com/fuel-prices/pol/archives

Pakistan State Oil provides historical POL price archive information that serves as the primary source for this dataset.

## ⚙️ Collection Methodology

Historical petrol price information was obtained from Pakistan State Oil's official POL price archives and organized into a structured CSV file.

The records are arranged by weekly reporting period, with separate columns representing petrol prices across 17 major cities and an additional Pakistan-level price indicator.

The dataset covers historical records from January 2013 through March 2026. Prices are expressed in PKR.

The original file includes a metadata row identifying the reporting frequency and currency. Users should account for this row when preparing the dataset for numerical analysis.

## ⚠️ Important Notes

- The dataset represents historical records and does not provide live petrol prices.
- The latest observation in this version is dated **5 March 2026**.
- Prices are expressed in Pakistani Rupees (PKR).
- The first data row after the column headers contains metadata rather than an actual observation.
- The `Pakistan` column is retained as a national-level indicator and should not automatically be interpreted as a calculated average of the city prices.
- Always refer to the original PSO archive for source verification and updated information.

## 🎯 Who Can Benefit From This Dataset?

This dataset is suitable for:

- Data Science and Machine Learning students.
- Data Analysts and Business Analysts.
- Economic and Financial Researchers.
- University Students and Academic Researchers.
- Time-Series Forecasting Enthusiasts.
- Anyone interested in Pakistan's energy and fuel market.

## ⭐ Support the Project

If you find this dataset useful for your research, analysis, or machine learning projects, please consider giving this repository a ⭐ **Star** on GitHub.

Your support encourages further data collection, documentation, and contributions to open data projects.

**Explore. Analyze. Learn. Share.**

## 📜 Disclaimer

This dataset is provided for educational, analytical, and research purposes. The underlying information is attributed to Pakistan State Oil (PSO). Please consult the official PSO website for authoritative and updated petrol pricing information.

This repository is an independent data project and is not officially affiliated with or endorsed by Pakistan State Oil.

---

**Made for the Data Science Community 🇵🇰**

If you use this dataset in your project, please acknowledge the original source: Pakistan State Oil (PSO).