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

Leverage: None

Shorting: Disabled

Trade Direction: Long-only


