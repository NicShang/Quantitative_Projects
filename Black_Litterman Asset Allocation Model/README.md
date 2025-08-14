# Black-Litterman Model Implementation

This project demonstrates a full implementation of the **Black-Litterman (BL) model** for portfolio optimization in Python.  
It integrates market equilibrium returns with investor views to produce posterior expected returns and an optimized asset allocation.

## Key Features
- **Data Preparation:** Import and clean historical price data for multiple assets.
- **Market Equilibrium Returns:** Calculate implied returns from market-capitalization weights using the reverse optimization approach.
- **Investor Views Integration:** Encode absolute and relative views into the BL model using the $P$ (pick) matrix and $Q$ (view returns) vector.
- **Posterior Estimation:** Apply Bayesian updating to combine equilibrium returns and investor views, yielding posterior means and covariances.
- **Portfolio Optimization:**  
  - Maximize the Sharpe ratio under constraints (no short selling, weight limits).  
  - Compare optimized BL portfolio vs. traditional mean-variance portfolio.
- **Visualization:** Plot efficient frontiers, weight distributions, and risk-return profiles.

## Skills & Tools
- **Python Libraries:** `numpy`, `pandas`, `cvxpy`, `matplotlib`
- **Quantitative Finance Concepts:** Mean-variance optimization, Bayesian statistics, market equilibrium, and investor view modeling
- **Practical Outcome:** A flexible framework for blending subjective insights with market data to improve portfolio allocation decisions.
