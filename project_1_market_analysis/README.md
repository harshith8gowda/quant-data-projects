📈 Market Overview & Risk Analysis — S&P 500
A practical demonstration of financial data analysis and risk evaluation using Python.

---

## Overview
This project performs a quantitative market overview and risk analysis of the S&P 500 equity index using historical daily data.

The analysis focuses on **returns, volatility, drawdowns, and risk-adjusted performance**, rather than price-only visualization.  
It demonstrates foundational quantitative finance skills expected of junior quant, research, and financial data analyst roles.

---

## Objectives
The analysis aims to:

- Study long-term return behavior of the S&P 500 across multiple market regimes  
- Quantify risk using volatility and drawdown-based measures  
- Analyze return distribution characteristics (skewness, kurtosis)  
- Compute standard risk-adjusted performance metrics used in practice  

---

## Data
- **Instrument:** S&P 500 Index (^GSPC)  
- **Source:** Yahoo Finance (via `yfinance`)  
- **Frequency:** Daily  
- **Start Date:** 2015-01-01  
- **Prices:** Adjusted prices (dividends and splits accounted for)

---

## Methodology

### 1. Price & Trend Analysis
- Visualization of raw and log-transformed prices  
- Identification of long-term market behavior across regimes  

### 2. Return Computation
- Daily percentage returns computed from adjusted prices  
- Returns analyzed instead of prices due to stationarity and risk relevance  

### 3. Descriptive Statistics
Key statistical properties of returns:
- Mean return  
- Volatility (standard deviation)  
- Skewness  
- Kurtosis (fat tails)  

These metrics provide insight into asymmetry and tail risk in equity returns.

### 4. Risk & Performance Metrics
- Annualized return  
- Annualized volatility  
- Sharpe ratio (assuming zero risk-free rate)  

Standard measures used in portfolio and strategy evaluation.

### 5. Drawdown Analysis
- Cumulative returns computed from daily returns  
- Maximum drawdown and drawdown series analyzed  

Drawdowns capture downside risk not visible through volatility alone.

### 6. Volatility Dynamics
- 30-day rolling annualized volatility  
- Used to observe volatility clustering and regime shifts  

---

## Key Concepts Demonstrated
- Return stationarity vs price non-stationarity  
- Volatility as a proxy for risk  
- Fat-tailed return distributions  
- Drawdowns as downside risk measures  
- Risk-adjusted performance evaluation  

---

## Results & Insights
- Equity returns exhibit volatility clustering and fat tails  
- Drawdowns reveal significant asymmetric downside risk  
- Risk-adjusted performance varies meaningfully across market regimes  
- Simple statistical tools already uncover meaningful market structure  

### Why This Project Matters
This project demonstrates how basic statistical techniques can extract meaningful risk insights from financial time series — a foundational skill for quantitative research and financial data roles.

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
- No transaction costs or strategy implementation  
- No predictive modeling or regime classification  

---

## Possible Extensions
- Multi-asset market comparison  
- Volatility-based regime detection  
- Factor-based or signal-driven strategies  
- Backtesting systematic trading strategies  
- Value-at-Risk (VaR) and Expected Shortfall (ES)  

---

## Author
**Harshith Gowda**  
MSc Data Science & Artificial Intelligence  
Aspiring Quantitative Analyst  

---

## Disclaimer
This project is for educational and research purposes only and does not constitute financial advice.
