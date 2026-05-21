# Market Sentiment vs Trader Performance

## Overview
This project analyzes the relationship between Bitcoin market sentiment and trader performance using historical trading data from Hyperliquid and the Bitcoin Fear & Greed Index.

The goal of this analysis is to identify how market emotions such as Fear and Greed influence trader profitability, leverage usage, trading activity, and overall trading behavior.

---

## Datasets Used

### 1. Bitcoin Fear & Greed Index Dataset
Contains:
- Date
- Market Sentiment Classification (Fear/Greed)

Dataset Link:  
https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf/view?usp=sharing

---

### 2. Hyperliquid Historical Trader Dataset
Contains:
- Account
- Symbol
- Execution Price
- Trade Size
- Side
- Time
- Closed Profit & Loss (closedPnL)
- Leverage
- Event Information

Dataset Link:  
https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing

---

## Project Objectives

- Analyze trader behavior under Fear and Greed market conditions
- Compare profitability across market sentiments
- Study leverage usage patterns
- Identify high-performing traders
- Visualize trading trends and sentiment impact
- Generate actionable insights for smarter trading strategies

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab

Optional:
- Plotly
- Streamlit

---

## Project Workflow

### 1. Data Collection
- Imported historical trader dataset
- Imported Bitcoin Fear & Greed Index dataset

### 2. Data Cleaning
- Removed missing values
- Converted timestamps to datetime format
- Extracted date information
- Checked duplicates and inconsistencies

### 3. Data Merging
Merged both datasets using the date column to associate each trade with market sentiment.

### 4. Exploratory Data Analysis (EDA)
Performed:
- Profitability analysis
- Leverage analysis
- Trade volume analysis
- Win rate analysis
- Correlation analysis

### 5. Visualization
Created:
- Bar charts
- Boxplots
- Heatmaps
- Profit distribution graphs

---

## Key Insights

- Traders tend to use higher leverage during Greed periods.
- Trading activity increases during Greed markets.
- Fear periods show more cautious trading behavior.
- High leverage often leads to larger losses during volatile conditions.
- A small number of traders contribute to a major portion of overall profits.

---

## Sample Analysis

### Average Profit by Sentiment

```python
merged_df.groupby('Classification')['closedPnL'].mean()
```

### Win Rate Calculation

```python
merged_df['win'] = merged_df['closedPnL'] > 0

win_rate = merged_df.groupby(
    'Classification'
)['win'].mean()
```

---

## Project Structure

```bash
market-sentiment-vs-trader-performance/
│
├── data/
│   ├── historical_data.csv
│   └── fear_greed_index.csv
│
├── notebook/
│   └── market_sentiment_vs_trader_performance.ipynb
│
├── report/
│   └── final_report.pdf
│
├── images/
│   └── charts.png
│
├── README.md
```

---

## How to Run the Project

### Open Google Colab

Upload:
- historical_data.csv
- fear_greed_index.csv
- market_sentiment_vs_trader_performance.ipynb

Install required libraries if needed:

```python
pip install pandas numpy matplotlib seaborn
```

Run all notebook cells to perform:
- Data cleaning
- Data merging
- Exploratory Data Analysis
- Visualization
- Insight generation

---

## Future Improvements

- Build a Streamlit dashboard
- Add machine learning models for trade prediction
- Include real-time crypto market data
- Perform advanced time-series analysis
- Add technical indicators like RSI and MACD

---

## Conclusion

This project demonstrates how market sentiment influences trader behavior and trading performance in cryptocurrency markets. By combining sentiment analysis with trading data analytics, valuable insights can be generated for risk management and strategy optimization.

---

## Author

Bumandla Rajashekar  
B.Tech CSE (AI & ML)  
Python | Data Science | Machine Learning | Web Development
