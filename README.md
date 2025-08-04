# Pairs Trading Strategy Using Cointegration

This project implements a **market-neutral pairs trading strategy** using Python. It identifies statistically cointegrated stock pairs and generates trading signals based on the spread's z-score. The strategy is backtested on historical stock data, and key performance metrics such as Sharpe Ratio, Max Drawdown, and Cumulative Returns are evaluated.

---

## Overview

Pairs trading is a market-neutral strategy that involves identifying two historically correlated assets. When the price relationship between the pair deviates significantly from the mean, the strategy takes a long position in the underperforming asset and a short position in the outperforming asset, expecting mean reversion.

---

## Methodology

1. **Data Collection**  
   - Historical stock data is downloaded using the `yfinance` API.
   - Example pair: Coca-Cola (`KO`) and PepsiCo (`PEP`).

2. **Cointegration Analysis**  
   - The Engle-Granger two-step method is used to test for cointegration.
   - Linear regression is applied to model the spread between the two stocks.

3. **Signal Generation**  
   - Z-score of the spread is calculated.
   - Entry/Exit thresholds are based on standard deviations from the mean.

4. **Backtesting**  
   - Simulated trades based on generated signals.
   - Daily portfolio returns are computed and visualized.

5. **Performance Evaluation**  
   - Sharpe Ratio  
   - Maximum Drawdown  
   - Cumulative Returns

---

## Tools & Libraries

- Python 3.8+
- `pandas`, `numpy`, `matplotlib`, `seaborn` – data manipulation & plotting  
- `yfinance` – historical stock data  
- `statsmodels` – cointegration & regression  
- `scikit-learn` *(optional)* – clustering or dimensionality reduction  
- `QuantStats` *(optional)* – advanced performance analysis

---

## Getting Started

### Prerequisites
Install the required libraries using pip:
```bash
pip install yfinance pandas numpy matplotlib seaborn statsmodels
