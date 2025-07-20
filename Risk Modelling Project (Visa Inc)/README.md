# Risk Modelling Project | Rolling Volatility Forecasting (Basel-Aligned)

This project simulates a forward-looking volatility and risk diagnostics pipeline aligned with Basel III/FRTB requirements. It supports market risk capital computation through internal models by generating dynamic Value-at-Risk (VaR) and Expected Shortfall (ES) forecasts, scenario-based stress diagnostics, and backtestable outputs suitable for regulatory validation.

---

## Objective

To generate 1–10 day ahead volatility forecasts using AR-GARCH family models, enabling rolling VaR/ES estimation and stress diagnostics in line with Basel market risk capital frameworks. The pipeline is designed to:

- Provide forward-looking VaR/ES metrics for internal capital modeling
- Trigger early-warning signals for market volatility regime shifts
- Support scenario-based stress testing under adverse market events
- Enable exposure monitoring and breach tracking for limit governance
- Generate outputs compatible with backtesting and P&L attribution validation tests

---

## Methodology

### 1. Volatility Forecasting

- **Model**: AR(6)-GARCH(3,7)
- **Libraries**: `arch`, `statsmodels`, `pandas`, `numpy`
- **Data**: Daily OHLC equity returns from Refinitiv (or equivalent sources)
- **Output**: Basel-compliant rolling VaR/ES forecasts (1–10 day horizons, 97.5% ES)

### 2. Stress Simulation & Attribution

- Simulated 5,000 Monte Carlo paths using GARCH residuals to assess downside risk
- Identified threshold exceedance zones and regime shifts across confidence levels
- Structured outputs into reporting-ready dashboards for scenario-based capital stress testing

### 3. Model Validation (Basel-aligned)

- Performed statistical validation using:
  - **Jarque-Bera test** for distributional assumptions
  - **Ljung-Box test** for autocorrelation structure
- Designed for use in internal model validation (backtesting, coverage ratio evaluation)
- Supports diagnostic tracking under Basel’s P&L Attribution and Risk Factor Eligibility Tests (FRTB)

### 4. Deliverables

- Fully automated Python pipeline for volatility prediction and market risk diagnostics
- Modular architecture for:
  - Risk capital estimation
  - Internal model governance
  - Exposure and limit breach tracking
  - Regulatory stress test simulation

---

## Business & Regulatory Relevance

This project mirrors Basel III / FRTB workflows for internal model approval of market risk capital under the Internal Models Approach (IMA). It provides a blueprint for implementing:

- Rolling VaR/ES estimation under FRTB (97.5% ES, 1-day horizon)
- Scenario-based stress testing and breach detection
- Model validation tools compatible with regulatory backtesting frameworks
- Risk signal transformation for dashboards and board-level consumption

It highlights how quantitative pipelines can produce regulatory-aligned, explainable outputs that aid both internal oversight and external compliance in risk-sensitive environments.
