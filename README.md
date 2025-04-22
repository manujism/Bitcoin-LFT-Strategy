# Bitcoin-LFT-Strategy

# 📈 RSI Crossover Momentum Strategy (LFT)

This is a **mid-frequency trading strategy** developed for the **BTC/USDT** pair using [Freqtrade](https://www.freqtrade.io/). It leverages the **Relative Strength Index (RSI)** on the **1D (daily)** timeframe to capture bullish momentum and protect profits during downturns.

---

## 🔍 Overview

- **Entry:** Triggered when RSI shows a bullish breakout.
- **Exit:** Triggered when RSI momentum weakens.
- **Type:** Long-only, low-frequency, rule-based strategy.

---

## 📊 Indicators Used

- **RSI(14):** Momentum oscillator ranging between 0–100
  - **RSI > 60:** Strong bullish momentum
  - **RSI < 41:** Weak momentum or reversal signal

---

## 🟢 Entry Criteria


    (dataframe['rsi'] > 60) & (dataframe['rsi'].shift(1) <= 60)




🔴 Exit Criteria
(dataframe['rsi'] < 41) & (dataframe['rsi'].shift(1) >= 41)


🛡 Risk Management

  Stop Loss: 7%

  Leverage: 
  
  Shorting: Disabled
  
  Trade Direction: Long-only


✅ Advantages
Simplicity: Single momentum indicator

Low Frequency: Avoids overtrading

Easy to Optimize: Few parameters

🚀 Potential Enhancements
Add volatility filters (ATR, Bollinger Bands)

Include trend confirmation (e.g., EMA crossovers)

Adaptive RSI thresholds (percentiles or z-scores)

📈 Backtest Results (2018–2025)

Metric	Value
Initial Balance	1,000 USDT
Final Balance	34,058.85 USDT
Total Profit	+33,058.85 USDT
CAGR	65.95%
Avg. Daily Profit	1.30%
Avg. Profit/Trade	25.65%
Sharpe Ratio	0.47
Max Drawdown	40.38%
Win Rate	46.2% (12/26)
Profit Factor	3.65
Avg. Trade Duration	49 days
📌 Performance Metrics

KPI	Value
SQN	1.82
Calmar Ratio	0.71
Sortino Ratio	0.41
Expectancy	1,271.49 USDT
Trade Volume	65,159.93 USDT
Position Size	11,938.39 USDT
💡 Key Insights
📈 Outperformed BTC market returns (3,305.88% vs 686.96%)

⚠ Sub-50% win rate, but highly profitable due to large gains

🏃‍♂️ Cuts losses early, lets winners run

📉 Room to improve Sharpe and Sortino ratios



  


