# Visa Inc. Risk Modelling – Volatility Forecasting & Risk-Based Capital Estimation

This project implements a risk modelling framework focused on volatility forecasting and regulatory capital estimation for Visa Inc., simulating a Basel-aligned Value-at-Risk (VaR) and Expected Shortfall (ES) evaluation process. The analysis demonstrates readiness to assess market risk using advanced statistical tools and aligns with industry expectations for model governance and stress testing.

## Project Objectives

- Forecast Visa Inc. stock return volatility using time series models (e.g. GARCH)
- Estimate Value-at-Risk (VaR) and Expected Shortfall (ES) under different methods
- Evaluate model robustness using backtesting and visual diagnostics
- Explore implications under Basel regulatory frameworks (Basel II.5/III)

## Key Features

### Volatility Forecasting
- Implemented GARCH family models to capture time-varying volatility in Visa stock returns.
- Used AIC and diagnostic tests to compare model fit and select the best-performing model.

### VaR & ES Estimation
- Estimated 1-day 99% VaR and Expected Shortfall using:
  - Historical simulation
  - Parametric normal assumption
  - Fitted GARCH model with student-t distribution
- Highlighted model sensitivity to tail behavior and volatility clustering.

### Model Validation & Backtesting
- Conducted rolling-window backtests to evaluate VaR breaches.
- Plotted violation ratios and exception flags to assess model reliability over time.

## Basel Compliance Relevance

This project aligns with **Basel Committee on Banking Supervision (BCBS)** standards in the following ways:

- **Value-at-Risk**: Modeled both historical and parametric VaR, in line with Basel II.5 internal models approach (IMA) requirements.
- **Expected Shortfall (ES)**: Demonstrated Basel III-compliant tail risk measurement to replace VaR as the primary capital requirement metric.
- **Backtesting**: Used exception counting and coverage tests to support model accuracy and regulatory validation.

## Business Value

- **Risk Capital Adequacy**: Provides a prototype system to evaluate risk capital charges for financial institutions holding equity exposure.
- **Stress Testing Readiness**: Supports scenario-based testing under volatile market conditions and economic downturns.
- **Audit & Governance**: Builds transparent and interpretable outputs, aiding internal model validation and external audit reviews.
