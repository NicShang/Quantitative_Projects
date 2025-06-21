## Project Overview: Super Fund Portfolio Risk Modeling
This project simulates a realistic investment scenario for superannuation funds like Cbus Super Fund, by constructing a diversified ETF-based portfolio comprising:

  Australian equities (VAS.AX)
  
  International developed equities (IVV)
  
  Fixed income (VAF.AX)
  
  Property (VNQ)
  
  Infrastructure (IFRA)
  
  Cash equivalents (AAA.AX)
  
  Emerging markets (IEM.AX)

The goal is to quantify tail risks of this portfolio under a 95% confidence level, using multiple Value at Risk (VaR) methodologies.

## Methodology & Technical Stack
1） Data Acquisition & Processing

    Historical daily prices are sourced using yfinance for 7 representative ETFs.
    
    The portfolio Net Asset Value (NAV) is constructed using normalized price weights.
    
    Daily log returns are computed for risk estimation.

2） VaR Model Construction

    VaR logic is encapsulated using Pydantic-based data models and custom Python classes.

3） Three VaR methods are implemented:
      
    Parametric VaR (based on mean-variance assumptions)
      
    Historical VaR (non-parametric percentile estimation)
      
    Monte Carlo VaR (based on simulated return distributions)

    Expected Shortfall (CVaR) is also computed to evaluate average loss beyond VaR.

4） Visualization

    A bar chart is created using matplotlib to intuitively compare the four risk metrics side-by-side.

--

## Business Value & Use Case
- Demonstrates a transparent and explainable risk modeling framework, applicable to pension fund risk teams.

- Enables daily tail risk monitoring of multi-asset portfolios for better risk budgeting and asset allocation decisions.

- Scalable to real-world use cases such as:

    Rebalancing triggers
    
    Compliance and reporting workflows
    
    Stress testing and downside risk analytics

- Highlights technical proficiency in:

    Python programming
    
    Financial risk theory (VaR, CVaR)
    
    Business-aware modeling suited for quantitative roles like Deloitte QFS.

