# Reddit Stock Sentiment: Tech & Semiconductor Data 📈💬

[![Dataset Status](https://img.shields.io/badge/Dataset-Complete-brightgreen.svg)](#)
[![License: CC0 1.0](https://img.shields.io/badge/License-CC0--1.0-yellow.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
[![Domain](https://img.shields.io/badge/Domain-NLP%20%7C%20Finance-blue.svg)](#)
[![Python](https://img.shields.io/badge/Language-Python-informational.svg)](#)

<p align="center">
  <img src="Neon Sentiment Semi-Analyzer Dashboard.png" alt="Reddit Stock Sentiment Cover Image" width="100%" style="border-radius: 20px; box-shadow: 0 4px 12px rgba(0, 225, 255, 0.3);">
</p>

## Overview
Welcome to the comprehensive Reddit sentiment dataset covering top global tech and semiconductor stocks—specifically **ASML**, **Micron (MU)**, **SanDisk (SNDK)**, and **Western Digital (WDC)**. Spanning a 14-month capture window (**January 2025 – February 2026**), this dataset links **1,988 primary post submissions** directly to **37,031 user comments** across major financial subreddits.

Whether you're developing financial NLP models (FinBERT, RoBERTa), analyzing retail trading volume dynamics, or backtesting sentiment-driven alpha strategies, this dataset provides a structured, high-signal foundation for your research.

---

## 📊 Dataset Highlights
- **Coverage**: 39,019 total records across 14 consecutive months
- **Target Tickers**: ASML, MU (Micron), SNDK (SanDisk), WDC (Western Digital)
- **Subreddit Sources**: `r/wallstreetbets`, `r/stocks`, `r/valueinvesting`, `r/investing`, `r/Semiconductors`, `r/options`, `r/StockMarket`, `r/SecurityAnalysis`, `r/TheRaceTo10Million`
- **Data Architecture**: Structured relational pair (`posts_stocks.csv` linked to `comments_stocks.csv` via `post_id`)
- **Data Cleanliness**: Standardized schemas with complete timestamping and engagement metrics

---

## 📁 Data Structure

### 1. Primary Posts (`posts_stocks.csv`)
Contains **1,988 primary Reddit post submissions** gathered from key financial subreddits. Each record captures the complete post headline, full body text, author username, creation timestamp, net upvote score, comment count, and its designated semiconductor equity ticker tag.

| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| **post_id** | String | Unique alphanumeric submission identifier (e.g., `1nvjksh`) |
| **subreddit** | String | Subreddit community name (e.g., `wallstreetbets`, `stocks`) |
| **stock_ticker** | String | Target equity ticker symbol (`ASML`, `MU`, `SNDK`, `WDC`) |
| **title** | String | Headline text of the main post |
| **body** | String | Raw text body content (retains `[removed]` / `[deleted]` flags) |
| **author** | String | Reddit username of the author |
| **created_utc** | String / Timestamp | UTC timestamp of post creation (`YYYY-MM-DD HH:MM:SS`) |
| **score** | Integer | Net total score (upvotes minus downvotes) |
| **upvote_ratio** | Float | Ratio of upvotes relative to total votes cast |
| **num_comments** | Integer | Total comment count attached to the thread |
| **url** | String | Embedded external link or image URL |
| **permalink** | String | Direct relative web path on Reddit |

### 2. User Comments (`comments_stocks.csv`)
Comprises **37,031 individual user comments** directly nested under the semiconductor stock discussion threads. It provides granular conversational text data alongside comment-level upvote scores, timestamps, and thread identifiers.

| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| **comment_id** | String | Unique identifier for the individual comment (e.g., `nquqx7i`) |
| **post_id** | String | Foreign key linking comment back to `posts_stocks.csv` |
| **subreddit** | String | Subreddit community where comment was posted |
| **stock_ticker** | String | Target equity ticker symbol associated with thread |
| **body** | String | Full text of the comment response |
| **author** | String | Reddit username of the commenter |
| **created_utc** | String / Timestamp | UTC timestamp when comment was submitted (`YYYY-MM-DD HH:MM:SS`) |
| **score** | Integer | Net upvotes accumulated by the comment |
| **permalink** | String | Direct URL path to the specific comment |

---

## 💡 Potential Use Cases

1. **Financial Sentiment Analysis**: Train FinBERT, RoBERTa, or custom Transformer models to classify text into Bullish, Bearish, or Neutral sentiment categories.
2. **Sentiment vs. Equity Price Movements**: Align thread engagement spikes and score patterns with daily price volatility, volume runs, and earnings events for $ASML, $MU, $SNDK, and $WDC.
3. **Retail Trader Behavioral Dynamics**: Compare discussion tone and risk appetite between retail speculation (`r/wallstreetbets`) and fundamental valuation discussions (`r/valueinvesting`, `r/SecurityAnalysis`).
4. **Conversational LLM Fine-Tuning**: Benchmark open-source language models on domain-specific financial acronyms, slang, and sentiment extraction.

---

## 📌 Provenance & Acknowledgements

- **Sources**: Raw public text extracted directly from open financial subreddits via public API endpoints. Original community threads are available at [Reddit](https://www.reddit.com/).
- **Collection Methodology**: Data was gathered via continuous scraping scripts filtering target tickers (`ASML`, `MU`, `Micron`, `SNDK`, `SanDisk`, `WDC`, `Western Digital`) across target subreddits between Jan 2025 and Feb 2026. Submissions and comment trees were extracted, normalized, and exported directly into structured CSV formats.

---

## ⭐ Support & Feedback

If you find this dataset valuable for your NLP research, quantitative modeling, or analytics projects, please consider **Upvoting** 👍 this dataset on Kaggle and starring the project! 

Feel free to open a Discussion topic or share your analysis notebooks!

---

## ⚠️ Disclaimer
*This dataset is provided for educational, academic, and research purposes only. It does not constitute financial, investment, or trading advice.*