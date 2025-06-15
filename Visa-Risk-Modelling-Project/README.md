# Visa Inc. Risk Modelling Project | Rolling Volatility Forecasting

This project simulates a real-world risk management workflow for Visa Inc., focused on estimating multi-step forward volatility and stress metrics to support dynamic risk reporting, attribution analysis, and pre-trade control environments.

## 🎯 Project Objective

To forecast 1–10 day forward volatility using AR-GARCH models and quantify risk through Value-at-Risk (VaR) and Expected Shortfall (ES) measures, supporting:

- Intraday exposure tracking
- Pricing validation
- Trade risk flags and stress attribution

## 🛠 Methodology

### 1. Volatility Forecasting
- **Model**: AR(1)-GARCH(1,1)
- **Library**: `arch`, `statsmodels`, `pandas`, `numpy`
- **Target**: Visa Inc. (V) stock daily returns
- **Data**: Refinitiv-sourced OHLC data
- **Output**: Multi-horizon volatility forecasts (1 to 10 days)

### 2. VaR & Expected Shortfall
- **Approach**: Parametric Gaussian distribution
- **Rolling Forecast**: Expanding-window re-estimation
- **Confidence Levels**: 95% and 99%
- **Metrics**:
  - Value-at-Risk (VaR)
  - Expected Shortfall (ES)
  - Realized loss comparison and exceedance tracking

### 3. Monte Carlo Simulation
- Used GARCH residuals to simulate future return paths
- Applied stochastic processes to assess tail risk
- Visualized expected return distribution under multiple regimes

## 📈 Key Results

- Generated rolling volatility forecasts over 1–10 day periods
- Computed daily 95% and 99% VaR & ES values for Visa
- Tracked exceedances (actual loss > VaR) to evaluate model reliability
- Visualized risk metrics with `matplotlib` and `plotly`

## 💡 Skills & Tools Demonstrated

- Time Series Modelling (AR-GARCH)
- Volatility attribution and stress testing
- Rolling forecasts and backtesting
- VaR/ES estimation and model exceedance tracking
- Python: `arch`, `pandas`, `statsmodels`, `matplotlib`, `plotly`

