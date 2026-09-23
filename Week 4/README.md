# Power BI Week 4 – Exploratory Data Analysis (EDA)

## 📊 Overview

This project focuses on Exploratory Data Analysis (EDA) using Power BI with stock market data. The dashboard uses DAX measures, moving averages, interactive visualizations, slicers, dynamic metric selection, and a custom tooltip to analyze stock price and trading volume trends.

## 🎯 Objectives

- Calculate 20-day and 50-day Simple Moving Averages (SMA)
- Analyze trading volume trends
- Create a Moving Average Crossover Signal
- Build an interactive stock price trend visualization
- Analyze trading volume and identify volume spikes
- Implement date-based slicers
- Create a dynamic stock price metric selector
- Design a custom tooltip for detailed stock information

## 🛠️ Tools & Technologies

- Power BI Desktop
- DAX
- Stock Market Dataset
- Interactive Power BI Visualizations

## 📈 Key Features

### 1. Simple Moving Averages
Created 20-day and 50-day Volume SMA measures using DAX to analyze short-term and longer-term trading volume trends.

### 2. Moving Average Crossover
Created a Moving Average Crossover Signal to compare the 20-day and 50-day SMAs and display Bullish or Bearish conditions.

### 3. Interactive Price Trend
Created an interactive line chart displaying stock price and moving averages over time. A zoom slider was also enabled for easier timeline analysis.

### 4. Trading Volume Analysis
Created a trading volume visualization using Trading Volume, Volume 20 SMA, and Volume Spike Highlight to identify periods of increased trading activity.

### 5. Timeline Slicers
Implemented:
- Date Range Slicer
- Relative Date Slicer

These allow the dashboard to be filtered according to the required time period.

### 6. Dynamic Metric Selector
Created a Field Parameter containing:
- Open Price
- High Price
- Low Price
- Close Price

This allows users to dynamically switch between different stock price measures.

### 7. Custom Tooltip
Created a `Stock_Tooltip` page to display detailed information when hovering over the main chart, including:
- Open Price
- High Price
- Low Price
- Close Price
- Trading Volume
- Daily Return %

## 📂 Files

- `WEEK 4 Report.pdf` – Assignment report and screenshots
- `week 4 powerbi eda.pbix` – Power BI project exported as pdf

## 📌 Outcome

The completed dashboard provides an interactive view of stock price and trading volume trends using DAX calculations, moving averages, dynamic filters, field parameters, and custom tooltips.
