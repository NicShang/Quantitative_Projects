# 🧠 Drawdown Risk Classifier for Superannuation Portfolios

This project simulates a diversified superannuation (pension) portfolio inspired by Cbus Super’s publicly disclosed asset allocations. The aim is to construct a predictive framework to classify periods where the portfolio is at risk of experiencing a significant drawdown (e.g., >10% within 20 trading days).

---

## 🔍 Why NAV, not just volatility?

While volatility (standard deviation) is a common risk metric, it fails to capture **cumulative losses, sustained downtrends, and tail events**. In real-world portfolio oversight—especially for retirement funds—risk is not about daily noise but whether the portfolio enters a **prolonged drawdown**.

> 📈 This project constructs the **portfolio-level NAV series** as the foundation for evaluating drawdowns, stress regimes, and tail-risk exceedance—something volatility alone cannot detect.

---

## 📦 Project Overview

- ✅ Simulate multi-asset super fund portfolio NAV using ETF proxies (VAS.AX, IVV, VAF, VNQ, IFRA, IEM, AAA)
- ✅ Generate future 20-day rolling drawdown as the basis for classification
- ✅ Create engineered features (5-day return, 20-day return, 20-day volatility)
- ✅ Train logistic regression and gradient boosting models to predict drawdown events
- ✅ Evaluate classification performance (precision, recall, ROC-AUC)

---

## 🧰 Tools & Techniques

- `Python`, `pandas`, `yfinance`, `scikit-learn`, `plotly`
- Portfolio NAV construction
- Labeling regime risk via rolling max drawdown
- Logistic Regression / XGBoost classification
- Model explainability (planned: SHAP)

---

## 🧩 Key Insight

> Portfolio NAV is the foundation of risk truth in long-horizon investing.  
> This project demonstrates how downside-aware models can complement volatility models by **anticipating actual portfolio stress**, not just noise.

---

## 📊 Example Output (in progress)

- Simulated NAV curve  
- 20-day future drawdown curve  
- Predicted probability of entering drawdown zone  
- Classification report (confusion matrix, ROC)

---

## 📁 Data Source

- ETF prices via [Yahoo Finance](https://finance.yahoo.com)
- Portfolio weightings based on public [Cbus Super holdings (Dec 2024)](https://www.cbussuper.com.au/super/my-investment-options/cbus-investment-holdings)

---

## ✍️ Author

Nic Shang — aspiring quant/data analyst with focus on investment risk modelling.  
Studying CQF with focus on GARCH, simulation-based risk, and portfolio construction.

---

*This project is built for learning purposes and does not reflect any actual recommendation or investment advice.*
