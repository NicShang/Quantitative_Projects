# Super Fund Portfolio Risk Modelling | Drawdown Forecasting & VaR Analysis

This project simulates a real-world risk advisory scenario for institutional clients like superannuation funds. It integrates portfolio-level drawdown forecasting and multi-method Value-at-Risk (VaR) estimation to support capital preservation, fiduciary oversight, and risk-aware portfolio management.

---

## Objective

To build a forward-looking risk monitoring pipeline capable of:

- Forecasting high-risk drawdown periods (>5% in 20 days) using statistical classifiers
- Quantifying tail risks via Parametric, Historical, and Monte Carlo VaR
- Benchmarking portfolio-level risks against single ETF exposures
- Supporting timely de-risking decisions with explainable, production-structured analytics

---

## Methodology

### 1. Data Pipeline
- Pulled historical daily prices of 7 ETFs across equity, fixed income, property, infrastructure, and cash sectors using `yfinance`
- Constructed NAV-based portfolio return series with normalized weights
- Engineered lagged features: momentum, moving averages, return volatility

### 2. Drawdown Risk Forecasting
- Defined binary risk flag if 20-day return < -5%
- Trained logistic regression classifier
- Achieved **100% sensitivity** and **AUC = 0.98** on test set, capturing all major drawdown events
- Structured for early-warning alerts under fiduciary priorities

### 3. VaR & Expected Shortfall (ES)
- Implemented 3 methods: 
  - **Parametric VaR** (Variance-Covariance)
  - **Historical Simulation**
  - **Monte Carlo VaR** (Simulated paths from return distributions)
- Evaluated ES to reflect tail severity
- Compared diversified portfolio metrics to single-asset (e.g., IVV) profiles

### 4. Reporting Outputs
- Visualized VaR & ES metrics with bar plots for stakeholder interpretation
- Supported transparency and control framework alignment

---

## Business Value

- Enables **early intervention** during periods of elevated drawdown risk—critical for member protection in super funds
- Demonstrates benefits of **portfolio diversification** over single ETF exposure
- Provides explainable **risk metrics** (VaR, ES) to align with **governance** and **reporting standards**
- Readily extendable to real-world super funds, family offices, or institutional advisory contexts

---

## Tools & Libraries
- Python, Pandas, Scikit-learn, Matplotlib
- Logistic Regression, Simulation, VaR Theory
- Modular functions & classes for reuse in custom reporting pipelines

---

## Reusability & Deployment
- Built with a modular, production-aware design (custom classes + clean output structure)
- Easily adaptable for scenario variation (e.g., different ETFs, lookback periods, confidence levels)
