📉 Mean Reversion Strategy Backtest — S&P 500  
*A systematic trading strategy implemented and evaluated using Python.*

---

## Overview
This project implements and backtests a **simple mean reversion trading strategy** on the S&P 500 equity index using historical daily data.

The goal is not to maximize returns, but to **demonstrate systematic strategy design, backtesting discipline, and risk-aware evaluation**, which are essential skills for quantitative trading and research roles.

---

## Strategy Intuition
Mean reversion strategies are based on the idea that asset prices tend to revert toward a rolling average after extreme deviations.

This strategy:
- Buys the index after statistically significant downward deviations  
- Exits positions once prices revert toward the mean  

---

## Data
- **Instrument:** S&P 500 Index (^GSPC)  
- **Source:** Yahoo Finance (via `yfinance`)  
- **Frequency:** Daily  
- **Start Date:** 2015-01-01  
- **Prices:** Adjusted prices (`auto_adjust=True`)  

---

## Signal Construction

### Z-Score Signal
- Rolling window: **20 trading days**
- Z-score measures deviation from rolling mean in standard deviation units

\[
Z_t = \frac{P_t - \mu_t}{\sigma_t}
\]

---

## Trading Rules
- **Long Entry:** Z-score < -1  
- **Exit:** Z-score > 0  
- **Positioning:** Long-only  
- **Execution:** Signals shifted by one day to avoid lookahead bias  

---

## Backtesting Methodology
- Daily strategy returns computed from lagged positions  
- Cumulative performance compared against buy-and-hold benchmark  
- No leverage applied  

---

## Performance Metrics
The following metrics are evaluated:

- Annualized return  
- Annualized volatility  
- Sharpe ratio (zero risk-free rate assumption)  
- Maximum drawdown  

---

## Results (Summary)
- The strategy exhibits **lower volatility and smaller drawdowns** than the market  
- Risk-adjusted performance is positive but **inferior to buy-and-hold**  
- Strategy behaves defensively during volatile market conditions  

This is expected behavior for a simple mean reversion strategy applied to a broad equity index.

---

## When the Strategy Fails
Mean reversion strategies tend to underperform during:
- Strong trending markets  
- Structural regime shifts  
- Prolonged high-volatility environments  

Understanding failure modes is essential for robust strategy design.

---

## Limitations
- No transaction costs or slippage modeling  
- Fixed parameter choices (window, thresholds)  
- Long-only strategy  
- No regime or volatility filter  

---

## Possible Extensions
- Volatility or regime-aware filtering  
- Dynamic position sizing  
- Parameter sensitivity analysis  
- Walk-forward validation  
- Combination with trend-following strategies  

---

## Technologies Used
- Python  
- pandas  
- numpy  
- matplotlib  
- yfinance  

---

## Author
**Harshith Gowda**  
MSc Data Science & Artificial Intelligence  
Aspiring Quantitative Analyst  

---

## Disclaimer
This project is for educational and research purposes only and does not constitute financial advice.
