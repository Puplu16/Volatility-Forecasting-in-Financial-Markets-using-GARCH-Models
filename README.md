# Volatility Forecasting in Financial Markets using GARCH Models

A Quantitative Finance approach to modeling, forecasting, and applying time-varying volatility across multiple asset classes using the GARCH family of econometric models.

---

## 👥 Authors & Project Details
* **Samya Mukherjee** (B2430057)
* **Avirup Das** (B2430041)
* **Shubradip Bhattacharyya** (B2430062)
* **Date:** November 2025
* **Institution:** Ramakrishna Mission

---

## 📊 Project Overview
This project provides a robust empirical framework to analyze, model, and forecast financial market volatility. It investigates the stylized facts of financial assets (such as fat tails, asymmetry, and volatility clustering) and benchmarks multiple univariate GARCH specifications across diverse asset markets over a 7-year timeline (2018–2024).

### 🔒 Analyzed Asset Classes
The framework tracks four primary assets spanning traditional and modern global markets:
1. **S&P 500 Index (`^GSPC`)** – U.S. Equity Baseline
2. **EUR/USD Exchange Rate (`EURUSD=X`)** – Liquid Foreign Exchange
3. **Gold Futures (`GC=F`)** – Traditional Safe-Haven Commodity
4. **Bitcoin (`BTC-USD`)** – High-Volatility Cryptocurrency

---

## 🛠️ Computational Framework & Models
The technical pipeline was developed using Python's quantitative ecosystem (`arch`, `statsmodels`, `scipy`, `yfinance`, `pandas`, and `numpy`). 

Four statistical volatility structures were tested:
* **Standard GARCH(1,1)**: Symmetric volatility persistence baseline.
* **Exponential GARCH (EGARCH)**: Exponential modeling capturing asymmetric leverage responses.
* **Threshold GARCH (GJR-GARCH)**: Captures distinct variance shocks from negative vs. positive returns.
* **TARCH**: Threshold-based absolute shocks.

---

## 🔑 Key Empirical Findings

### 🏆 The Overall Champion Model
While in-sample criteria (AIC/BIC) preferred specific variations per asset, **EGARCH emerged as the ultimate out-of-sample performance champion** across metrics (RMSE & MAE) due to its exceptional ability to adapt to severe regime-switching environments and exponential shock responses.

### 📈 Asset Optimization Results
* **S&P 500**: Symmetric persistence is captured sufficiently by standard **GARCH(1,1)** under normal regimes.
* **EUR/USD**: Shows heavy threshold asymmetry; **TARCH/GJR-GARCH** structures strongly dominate breakouts.
* **Gold & Bitcoin**: Both exhibit structural asymmetric risk profiles best modeled via **EGARCH**.

---

## 💼 Financial Applications Implemented

### 1. Dynamic Portfolio Optimization
By substituting a static Markowitz matrix with a time-varying GARCH conditional covariance matrix ($\Sigma_t$), a 3-asset portfolio (Equities, Forex, Gold) was dynamically optimized using a minimum-variance strategy.
* **Static Portfolio Sharpe Ratio:** 0.3025
* **Dynamic GARCH Sharpe Ratio:** 0.5616
* **Performance Boost:** **+85.7% Improvement** in risk-adjusted performance.

### 2. Option Pricing (Black-Scholes Integration)
Integrating forward-looking GARCH forecasts instead of backward-looking historical volatility into European Call calculations showed material valuation impacts:
* For the **S&P 500**, GARCH predicted 1.439% higher upcoming risk premiums, leading to premium valuations **7.2% higher on average** compared to traditional metrics.

### 3. Market Regime Analysis
Assets were tested across **Low, Medium, and High Volatility regimes** calculated via 3-month rolling windows. High-volatility clusters accurately isolated the 2020 COVID-19 crash and the 2022 monetary transitions.


