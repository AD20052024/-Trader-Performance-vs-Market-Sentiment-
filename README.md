# -Trader-Performance-vs-Market-Sentiment-
# Trader Performance vs Market Sentiment Analysis

## Overview
This project analyzes how Bitcoin market sentiment (Fear vs Greed) influences trader behavior and performance on the Hyperliquid trading platform.

By combining market sentiment data with historical trading data, the goal is to identify patterns in:

- trader profitability
- trading activity
- position sizes
- long vs short bias

The analysis aims to uncover insights that can help design better trading strategies and risk management rules.

---

## Datasets

Two datasets were used for this analysis.

### 1. Bitcoin Market Sentiment Dataset
Contains daily sentiment classification of the Bitcoin market.

Columns include:
- date
- value
- classification (Fear / Greed)

This dataset represents overall market sentiment conditions.

### 2. Historical Trader Data (Hyperliquid)
Contains detailed trading activity data.

Key columns include:
- Account
- Symbol
- Execution Price
- Size USD
- Side
- Closed PnL
- Timestamp

This dataset represents individual trader behavior and performance.

---

## Methodology

The analysis was performed using Python (Pandas, Matplotlib, Seaborn) in a Jupyter/Google Colab notebook.

The workflow included the following steps:

### 1. Data Loading
Both datasets were loaded and inspected to understand their structure and column information.

### 2. Data Cleaning
Basic data quality checks were performed:
- dataset size inspection
- missing value checks
- duplicate record detection

### 3. Data Alignment
Since the datasets used different time formats, timestamps were converted to a daily date format.

The datasets were then merged on the date column to associate each trade with the corresponding market sentiment.

### 4. Feature Engineering
Additional features were created to support the analysis:
- win_trade to indicate profitable trades
- trade exposure indicators
- trader segmentation variables

### 5. Metrics Calculation
Several performance and behavioral metrics were computed:
- daily PnL per trader
- win rate
- average trade size
- leverage / risk exposure distribution
- number of trades per day
- long vs short trade ratio

### 6. Visualization
Data visualizations were used to identify patterns between market sentiment and trading behavior.

Charts included:
- PnL distribution across Fear vs Greed markets
- trading activity comparison
- trade size distribution
- leverage / risk exposure patterns

### 7. Trader Segmentation
Traders were segmented into behavioral groups:
- frequent vs infrequent traders
- high vs low trade size traders
- consistent vs inconsistent traders

This segmentation helped identify differences in trading patterns and performance stability.

---

## Key Insights

### 1. Market Sentiment Influences Trader Behavior
Trader activity and position sizes tend to increase during Greed market conditions, indicating higher market confidence.

### 2. Trading Activity Changes with Market Conditions
The number of trades generally increases during Greed periods, while traders appear more cautious during Fear periods.

### 3. Risk Exposure Varies with Sentiment
Traders tend to take larger position sizes during Greed sentiment, reflecting increased risk-taking behavior.

### 4. Performance Stability Differs Between Traders
Segment analysis shows that consistent traders exhibit more stable performance, while inconsistent traders experience higher volatility in returns.

---

## Strategy Recommendations

### Strategy 1 — Risk Reduction During Fear Markets
When market sentiment indicates Fear:
- reduce position sizes
- limit leverage exposure
- focus on fewer high-confidence trades

This helps reduce drawdowns during volatile market conditions.

### Strategy 2 — Controlled Opportunity During Greed Markets
When sentiment indicates Greed:
- increase trade participation moderately
- take advantage of market momentum
- maintain strict risk management rules

This allows traders to benefit from favorable market conditions while managing risk.

### Strategy 3 — Focus on Consistent Risk Management
Traders should prioritize consistent position sizing and disciplined risk management rather than high-risk trades.

Stable strategies often lead to more consistent long-term performance.

---

## How to Run the Project

### Requirements
Python libraries used:

- pandas
- matplotlib
- seaborn

Install them using:

pip install pandas matplotlib seaborn

### Running the Notebook

1. Clone the repository

git clone <repo-link>

2. Open the notebook

Trader_Sentiment_Analysis.ipynb

3. Run all cells to reproduce the analysis and visualizations.

---

## Project Structure

trader-sentiment-analysis  
│  
├── Trader_Sentiment_Analysis.ipynb  
├── README.md  
├── charts/  
└── data/  

---

## Conclusion

This analysis demonstrates that market sentiment significantly influences trader behavior and risk-taking patterns.

By incorporating sentiment-aware strategies, traders can improve risk management and trading performance.
