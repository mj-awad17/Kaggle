# 📈 Financial Market Trends (2021–2023) 🚀

[![Dataset Status](https://img.shields.io/badge/Dataset-Complete-brightgreen.svg)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Domain](https://img.shields.io/badge/Domain-Finance%20%7C%20Time--Series-blue.svg)](#)
[![Format](https://img.shields.io/badge/Format-CSV-orange.svg)](#)
[![Python](https://img.shields.io/badge/Made%20with-Python-informational.svg)](#)

<p align="center">
  <a href="#-dataset-overview">Overview</a> •
  <a href="#-file-structure">Files</a> •
  <a href="#-data-dictionary">Data Dictionary</a> •
  <a href="#-what-you-can-do-with-this-dataset">Use Cases</a> •
  <a href="#-quick-start">Quick Start</a>
</p>

---

## 📊 Dataset Overview

This repository hosts the **Financial Market Trends (2021–2023)** dataset—a structured, daily record of financial market observations spanning **January 2021 through September 2023**. 

Designed for quantitative analysts, data scientists, and financial researchers, this dataset captures essential macroeconomic indicators, trading volumes, volatility measurements, and structural market event flags. It provides a clean benchmark for studying post-pandemic economic fluctuations, regulatory shifts, and market recovery trajectories.

---

## 📁 File Structure

```text
├── financial_market_trend_2021-to-2023.csv   # Primary daily financial dataset
└── README.md                                 # Project documentation

```

* **`financial_market_trend_2021-to-2023.csv`**: Contains daily records of benchmark market prices, trading activity, interest rates, volatility scores, and binary classifications for regulatory changes and market recovery phases.

---

## 📋 Data Dictionary

| Column Name | Data Type | Description |
| --- | --- | --- |
| `Date` | `Date (YYYY-MM-DD)` | Calendar date of the recorded trading session. |
| `Market Price ($)` | `Float` | Benchmark market price in USD. |
| `Recovery Index` | `Float` | Normalized index tracking localized market recovery momentum. |
| `Trading Volume` | `Float / Integer` | Total volume of assets traded during the session. |
| `Volatility Index` | `Float` | Metric quantifying the magnitude of price variation and market risk. |
| `Interest Rate (%)` | `Float` | Prevailing benchmark interest rate percentage for the period. |
| `Regulatory Change` | `Binary (0 / 1)` | Flag denoting a major regulatory shift (`1` = Yes, `0` = No). |
| `Market Recovery` | `Binary (0 / 1)` | Target flag indicating whether the market entered a recovery phase (`1` = Yes, `0` = No). |

---

## 🧠 What You Can Do With This Dataset

Data analysts and data scientists can leverage this dataset across several exploratory, statistical, and machine learning workflows:

* **📈 Time-Series Forecasting:** Build ARIMA, Prophet, or LSTM/Transformer models to forecast future `Market Price ($)` and `Volatility Index` movements based on historical lags.
* **🎯 Binary Classification:** Train classification models (Logistic Regression, Random Forest, XGBoost) to predict `Market Recovery` (`0` vs. `1`) using macroeconomic features like `Interest Rate (%)` and `Trading Volume`.
* **📉 Event-Study & Impact Analysis:** Analyze how sudden spikes in `Regulatory Change` or shifts in `Interest Rate (%)` impact short-term market volatility and trading liquidity.
* **🔍 Exploratory Data Analysis (EDA) & Dashboards:** Create interactive Power BI, Tableau, or Plotly dashboards visualizing multi-year correlation matrices, drawdown periods, and recovery cycles.
* **⚙️ Feature Engineering Practice:** Derive rolling moving averages (7-day, 30-day), RSI indicators, volatility-adjusted returns, and lag features to boost predictive accuracy.

---

## 🚀 Quick Start

Load and inspect the dataset directly in Python using `pandas`:

```python
import pandas as pd

# Load the dataset
df = pd.read_csv("financial_market_trend_2021-to-2023.csv", parse_dates=["Date"])

# Sort chronologically and preview
df = df.sort_values("Date").reset_index(drop=True)
print(df.head())
print(df.info())

```

---

## 🤝 Contributing & Feedback

Contributions, notebooks, and exploratory analyses using this dataset are always welcome! Feel free to open an issue or submit a pull request with your findings or feature-engineering scripts.

---

## ⭐ Support This Repository

If you find this dataset helpful for your research, portfolio projects, or machine learning experiments, **please consider giving this repository a star ⭐** at the top right! Your support helps other data enthusiasts discover the project and encourages future dataset releases.
