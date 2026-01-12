📈 Market Overview, Risk & Volatility Regime Analysis — S&P 500  
*A practical demonstration of financial data analysis and risk evaluation using Python.*

---

## Overview
This project performs a quantitative market overview and risk analysis of the S&P 500 equity index using historical daily data.

The analysis focuses on **returns, volatility, drawdowns, and volatility regimes**, rather than price-only visualization.  
It demonstrates foundational quantitative finance skills expected of **junior quant, research, and financial data analyst roles**, with emphasis on **risk-aware market behavior**.

---

## Objectives
The analysis aims to:

- Study long-term return behavior of the S&P 500 across multiple market regimes  
- Quantify risk using volatility and drawdown-based measures  
- Analyze return distribution characteristics (skewness and kurtosis)  
- Evaluate risk-adjusted performance using standard financial metrics  
- Identify and compare **high-volatility vs low-volatility market regimes**

---

## Data
- **Instrument:** S&P 500 Index (^GSPC)  
- **Source:** Yahoo Finance (via `yfinance`)  
- **Frequency:** Daily  
- **Start Date:** 2015-01-01  
- **Prices:** Adjusted prices (dividends and splits accounted for using `auto_adjust=True`)  

---

## Methodology

### 1. Price & Trend Analysis
- Visualization of raw and log-transformed prices  
- Identification of long-term market behavior across multiple regimes  
- Log-prices used to highlight relative growth dynamics  

---

### 2. Return Computation
- Daily percentage returns computed from adjusted prices  
- Returns analyzed instead of prices due to:
  - Stationarity properties  
  - Direct relevance to risk measurement  
  - Alignment with quantitative strategy design  

---

### 3. Descriptive Statistics
Key statistical properties of returns are computed:

- Mean return  
- Volatility (standard deviation)  
- Skewness  
- Kurtosis (fat tails)  

These metrics help assess asymmetry and tail risk in equity returns.

---

### 4. Risk & Performance Metrics
Standard portfolio-level metrics are computed:

- Annualized return (252 trading days assumption)  
- Annualized volatility  
- Sharpe ratio (assuming zero risk-free rate for simplicity)  

These metrics are widely used in portfolio and strategy evaluation.

---

### 5. Drawdown Analysis
- Cumulative returns derived from daily returns  
- Drawdown series and **maximum drawdown** computed  
- Captures downside risk not visible through volatility alone  

---

### 6. Volatility Dynamics
- 30-day rolling annualized volatility  
- Used to observe:
  - Volatility clustering  
  - Regime persistence  
  - Risk regime transitions  

---

### 7. Volatility Regime Classification
- Market regimes classified into:
  - **High-volatility**
  - **Low-volatility**
- Median rolling volatility used as a robust, distribution-based threshold  

This simple regime classification provides meaningful risk context without complex modeling.

---

### 8. Regime-Based Analysis
- Return statistics compared across volatility regimes  
- Risk-adjusted behavior evaluated separately for each regime  
- Drawdowns analyzed conditionally on volatility state  

This highlights how market risk and return characteristics change under different volatility environments.

---

## Key Concepts Demonstrated
- Return stationarity vs price non-stationarity  
- Volatility as a proxy for market risk  
- Fat-tailed and asymmetric return distributions  
- Drawdowns as downside risk measures  
- Volatility clustering and regime persistence  
- Risk-adjusted performance across regimes  

---

## Results & Insights
- Equity returns exhibit clear volatility clustering and fat tails  
- High-volatility regimes are associated with:
  - Larger return dispersion  
  - Deeper and more persistent drawdowns  
  - Deterioration in risk-adjusted performance  
- Low-volatility regimes support more stable compounding  
- Even simple statistical tools can uncover meaningful market structure  

### Why This Project Matters
This project demonstrates how **basic statistical and time-series techniques** can extract meaningful risk insights from financial data — a foundational skill for **quantitative research, trading, and financial data roles**.

---

## Technologies Used
- Python  
- pandas  
- numpy  
- matplotlib  
- yfinance  

---

## Limitations
- Single-asset (index-level) analysis  
- No transaction costs or execution modeling  
- No predictive modeling or formal regime detection (e.g., HMM, GARCH)  

---

## Possible Extensions
- Multi-asset and cross-market regime comparison  
- Volatility regime detection using probabilistic models  
- Factor-based or signal-driven strategies  
- Backtesting systematic trading strategies  
- Value-at-Risk (VaR) and Expected Shortfall (ES) analysis  

---

## Author
**Harshith Gowda**  
MSc Data Science & Artificial Intelligence  
Aspiring Quantitative Analyst  

---

## Disclaimer
This project is for educational and research purposes only and does not constitute financial advice.
