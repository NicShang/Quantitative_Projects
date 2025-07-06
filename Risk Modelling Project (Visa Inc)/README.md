# Risk Modelling Project | Rolling Volatility Forecasting

This project simulates a forward-looking volatility monitoring pipeline designed to support dynamic risk diagnostics, stress-tested scenario reporting, and signal attribution in portfolio oversight and capital planning.

## Objective
To forecast short-term market volatility (1–10 days ahead) using AR-GARCH family models and generate actionable risk metrics, including Value-at-Risk (VaR) and Expected Shortfall (ES), supporting:

- Early-warning alerts for shifting market conditions
- Scenario-based stress reporting
- Exposure and threshold tracking in capital management frameworks

## Methodology

### 1. Volatility Forecasting
- **Model**: AR(6)-GARCH(3,7)
- **Libraries**: arch, statsmodels, pandas, numpy
- **Target**: Daily returns from Refinitiv-sourced OHLC equity data
- **Output**: Rolling VaR/ES estimates, 1–10 day multi-step volatility forecasts

### 2. Stress Simulation & Attribution
- Simulated 5,000 Monte Carlo paths from GARCH residuals to evaluate downside risk under stressed regimes
- Identified high-volatility clusters using exceedance tracking across confidence thresholds
- Structured outputs into reporting-ready format for scenario-based dashboards

### 3. Model Validation
- Performed diagnostic checks including Jarque-Bera and Ljung-Box tests
- Validated distribution fit and autocorrelation behavior to ensure model robustness

### 4. Deliverables
- Fully automated Python pipeline for volatility forecasting and risk diagnostics
- Structured for modular reuse in capital planning, stress testing, and exposure management environments

## Business Relevance
This project mirrors real-world workflows in financial risk advisory and reporting, offering practical implementation examples of how quantitative models can enhance portfolio oversight and inform decision-making under uncertainty. It highlights how technical outputs can be translated into clear, usable insights for non-technical stakeholders.
