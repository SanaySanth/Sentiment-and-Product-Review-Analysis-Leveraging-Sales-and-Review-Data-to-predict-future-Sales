# Sentiment and Product Review Analysis: Leveraging Sales and Review Data to Predict Future Sales

This repository contains an end-to-end time series and sentiment analysis pipeline that combines **historical sales data** and **customer review sentiment** to **forecast future sales** at multiple granularities (overall, by brand, by car series, fuel type, and city).

The project uses:

- **Text sentiment analysis** on product reviews  
- **Time series forecasting** using **ARIMA** and **SARIMA**  
- Rich **visualizations** (rolling means, heatmaps, boxplots, etc.) to interpret trends and seasonality

---

## 🧱 Project Overview

### Objectives

1. **Clean and preprocess** raw automotive sales and review data.
2. Perform **EDA (Exploratory Data Analysis)** to understand distributions, trends and seasonality.
3. Compute **sentiment scores** from textual reviews.
4. Aggregate data to **monthly time series** for:
   - Overall sales
   - Brand-level and series-level sales
   - Brand-level and series-level sentiment
   - Fuel-type-wise and city-wise sales
   - Average fuel consumption
5. Use **ARIMA** and **SARIMA** models to forecast **future sales and sentiment**:
   - SARIMA for series with clear **yearly seasonality** (most sales & sentiment series).
   - ARIMA for **non-seasonal** series (e.g., average fuel consumption).
6. Generate **plots and reports** to support business decisions like inventory planning, pricing and marketing.

---

## 📂 Repository Structure

> Note: Names are based on the notebooks you provided.

```text
.
├── ba-preprocess.ipynb          # Data loading, cleaning, preprocessing
├── eda-ba.ipynb                 # Exploratory Data Analysis (EDA)
├── sentimental-analysis.ipynb   # Text cleaning & sentiment scoring for reviews
├── arima-3para.ipynb            # Global & segment-level forecasting (price, fuel, city, overall, fuel consumption)
├── arima2-brand-series.ipynb    # Brand-wise & series-wise sales + sentiment forecasting
├── forecast_outputs/            # Generated plots, CSVs, and JSON summary files
└── README.md                    # Project documentation (this file)
