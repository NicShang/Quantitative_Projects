# Max Drawdown Predictor (Cbus Super Portfolio Simulation)

This project simulates a Cbus Super Fund–style multi-asset portfolio and uses logistic regression to predict whether a drawdown greater than 5% will occur in the next 30 days. It combines ETF-based proxy modeling, NAV construction, and classification techniques to turn market features into actionable early warnings.

---

## Why I Built This Project

  Super funds like Cbus exist to preserve and grow capital over decades, not chase short-term alpha. Their portfolios must support members' retirement needs 20–30 years into the future, making drawdown risk management far more critical than tactical gains.
  
  I built this project to reflect that long-term, risk-conscious mindset. By replicating Cbus’s asset allocation with ETFs and applying logistic regression to predict forward-looking drawdowns, I aimed to simulate how pension risk teams can anticipate periods of elevated downside risk based on recent return and volatility behavior.
  
  This work helped me connect portfolio modeling with fiduciary duty, reinforcing the idea that in long-horizon investing, risk awareness, not return maximization, is what truly matters.

---

## Project Summary

- Simulates the “Growth (MySuper)” option of Cbus Super using publicly available ETF proxies.

- Constructs a historical NAV curve by weighting ETFs based on Cbus asset allocations.

- Labels each date based on whether the portfolio suffers a maximum drawdown > 5% in the next 20 days.

- Uses lagging features (e.g., 5-day return, 20-day volatility) to predict future drawdowns via logistic regression.

- Evaluates model performance using confusion matrix, classification report, ROC-AUC score, and curve.

---

## Key Results

- Model Type: Logistic Regression with class_weight=balanced

- Target: Will there be a max drawdown > 5% in next 20 days?

- Test Accuracy: 85%

- AUC Score: 0.99

- Recall for Drawdown Class (1): 100%

- Model demonstrates strong ability to identify upcoming drawdowns, albeit with some false positives.

---

## Tech Stack

- Python, JupyterLab

- pandas, NumPy, yfinance

- scikit-learn (Pipeline, LogisticRegression, metrics)

- plotly, matplotlib (for visualization)

---

## Data Source

- ETF prices via [Yahoo Finance](https://finance.yahoo.com)
- Portfolio weightings based on public [Cbus Super holdings (Dec 2024)](https://www.cbussuper.com.au/super/my-investment-options/cbus-investment-holdings)

