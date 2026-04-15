# Trader Performance vs Market Sentiment Analysis

## Overview

This project analyzes how market sentiment (Fear/Greed) impacts trader behavior and performance using Hyperliquid trading data.

The goal is to identify patterns that can help design better trading strategies based on market conditions.

---

## Datasets Used

1. **Fear & Greed Index**

   * Contains daily sentiment classification (Fear, Greed, Neutral)

2. **Historical Trader Data**

   * Includes trade-level details such as account, price, size, side, and PnL

---

## Data Preparation

* Cleaned missing values and removed duplicates
* Converted timestamps into date format
* Merged both datasets on date
* Created key metrics:

  * Daily PnL
  * Trade count
  * Trader-level aggregation

---

## Analysis Performed

### 1. PnL vs Sentiment

* Compared average trader profitability across Fear, Greed, and Neutral periods
* Found that **Fear periods show higher average PnL**

---

### 2. Trader Behavior

* Analyzed trade frequency and activity
* Observed differences in behavior across sentiment conditions

---

### 3. Trader Segmentation (Clustering)

* Used KMeans clustering based on:

  * Total PnL
  * Trade count
* Identified different trader types:

  * High activity, low profit (overtraders)
  * Low activity, high profit (efficient traders)
  * High activity, high profit (skilled traders)

---

## Key Insight: The Fear Premium

* Traders tend to perform better during Fear periods (~345 avg PnL vs ~157 in Greed)
* This suggests that market panic may create profitable opportunities

---

## Strategy Recommendations

* Reduce aggressive trading during Greed periods
* Focus on selective, high-quality trades during Fear periods
* Avoid excessive trading, as higher activity does not guarantee higher profit

---

## Conclusion

Market sentiment plays a significant role in both trader behavior and performance.
Using sentiment-aware strategies can improve decision-making and trading outcomes.

---

## How to Run

1. Open the notebook (`.ipynb`)
2. Run all cells step by step
3. Ensure required libraries are installed:

   * pandas
   * numpy
   * matplotlib
   * seaborn
   * scikit-learn

---

## Author

Farhan
