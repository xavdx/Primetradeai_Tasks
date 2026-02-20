# Trader Performance vs Market Sentiment Analysis

## Objective:
This project analyzes how Bitcoin market sentiment (Fear/Greed Index) relates to trader behavior and performance on Hyperliquid. The goal is to identify sentiment-driven patterns that can inform smarter trading strategies.

## Environment: 
Developed in Google Colab (Python 3.x). Fully compatible with standard Jupyter Notebook environments.
---

## Methodology:

### 1. Data Preparation
- Loaded Fear/Greed Index dataset and Hyperliquid trader dataset.
- Documented row counts, missing values, and duplicates.
- Converted timestamps to daily format.
- Merged datasets on date to align trades with sentiment classification.
- Created key metrics:
  - Daily PnL per account
  - Win rate
  - Average trade size (USD)
  - Number of trades per day
  - Long/Short ratio
  - Trader-level aggregates for segmentation

---

### 2. Analysis

We evaluated:

- Performance differences between Fear vs Greed regimes
- Behavioral shifts across sentiment
- Trader segmentation:
  - Frequent vs Infrequent traders
  - Consistent vs Volatile traders
  - High vs Low exposure traders

---

## Key Insights:

1. **Regime-Level Profitability Shift**  
   Fear regimes exhibit higher average daily profitability, while Greed regimes show larger extreme drawdowns.

2. **Risk Asymmetry in Greed**  
   Win rates are slightly higher during Greed, but tail-risk and volatility reduce aggregate profitability.

3. **Frequency-Sentiment Interaction**  
   Frequent traders outperform during Fear, while infrequent traders perform better during Greed.

4. **Exposure Amplifies Sentiment Effects**  
   High-exposure traders significantly amplify returns during Greed regimes but are also more exposed to tail risk.

---

## Strategy Recommendations:

### Strategy 1- Regime-Adaptive Frequency
Increase trading activity during Fear regimes; reduce overtrading during Greed unless strategy is momentum-based.

### Strategy 2- Dynamic Exposure Scaling
Scale exposure cautiously during Greed due to amplified tail risk. Allow structured exposure during Fear where volatility-driven opportunity is higher.

---

## How to Run:

1. Clone the repository: git clone https://github.com/xavdx/Primetradeai_Tasks.git


2. Install dependencies:

pip install -r requirements.txt


3. Open the notebook:

jupyter notebook Primetradeai_Anshav_Desai.ipynb.ipynb


---

## Reproducibility:

All analysis steps are documented inside the notebook, including:
- Data cleaning
- Feature engineering
- Segmentation logic
- Visualization
- Insight derivation




# Executive Summary:

## Methodology

This analysis investigates how Bitcoin market sentiment (Fear/Greed Index) interacts with trader behavior and profitability on Hyperliquid.

The workflow consisted of:

1. **Data Preparation**
   - Loaded sentiment and trade datasets.
   - Checked row counts, missing values, and duplicates.
   - Converted timestamps to daily format.
   - Merged datasets on date to align each trade with daily sentiment.
   - Created key metrics:
     - Daily PnL per account
     - Win rate
     - Average trade size (USD)
     - Trade frequency
     - Long/Short ratio
     - Trader-level aggregates for segmentation

2. **Behavioral Segmentation**
   Traders were segmented into:
   - Frequent vs Infrequent
   - Consistent vs Volatile
   - High vs Low Exposure

3. **Regime Comparison**
   Performance and behavior were compared across Fear, Greed, and Neutral sentiment regimes using aggregated statistics and visualizations.

---

## Key Insights

1. **Sentiment Regimes Affect Aggregate Profitability**
   Fear regimes exhibit higher average daily profitability, while Greed regimes show larger extreme drawdowns, indicating stronger tail risk during optimistic markets.

2. **Risk Asymmetry in Greed**
   Win rates are slightly higher during Greed; however, aggregate profitability is lower due to volatility and large downside extremes. This suggests overconfidence-driven risk amplification.

3. **Frequency-Sentiment Interaction**
   Frequent traders outperform during Fear regimes, whereas infrequent traders perform better during Greed regimes. Market conditions affect trader archetypes differently.

4. **Exposure Amplifies Sentiment Effects**
   High-exposure traders generate substantially larger returns, particularly during Greed regimes. However, this also increases sensitivity to drawdowns.

---

## Strategy Recommendations

**1. Regime-Adaptive Trading Frequency**
Increase trading activity during Fear regimes to capitalize on volatility-driven opportunities. Reduce overtrading during Greed unless using momentum-aligned strategies.

**2. Dynamic Exposure Scaling**
Scale exposure cautiously during Greed regimes due to amplified tail risk. Allow structured exposure during Fear where aggregate opportunity appears stronger.

---

This analysis demonstrates that sentiment-aware trading adjustments can materially impact performance outcomes. Market regimes do not affect all trader types uniformly, highlighting the importance of behavioral segmentation in strategy design.
