# ETF Portfolio Optimization | Finance Capstone Project

This project mirrors many operational workflows seen in real-world investment operations—such as compliance monitoring, mandate interpretation, and systematic trade implementation—making it directly relevant for middle-office and investment operations roles.
   
    ## Key Components
        - This project simulates a $5 million ETF portfolio construction for an assertive-risk client using a core-satellite 
        investment strategy, as part of the final capstone at the University of Sydney.
        
        - The objective was to design a portfolio of ASX-listed ETFs that meets the investor’s return target of CPI + 6%, 
        while complying with constraints on:
        
            Strategic Asset Allocation (SAA)
            
            Tactical Asset Allocation (TAA)
            
            Minimum/maximum ETF weights
            
            Core-satellite split (65–85% core, 15–35% satellite)

    ## Technical Highlights
        Portfolio Optimization: Implemented in Python using NumPy, Pandas, and SciPy.optimize.minimize, enforcing real-world investment 
        rules (e.g. total weight = 100%, individual bounds, core ≥ 65%).
        
        Risk-Adjusted Allocation: Maximized Sharpe ratio and simulated risk-return space using Monte Carlo simulation.
        
        Constraint Handling: Encoded portfolio eligibility criteria (e.g., max 10% per satellite ETF) into optimizer via SLSQP constraints.
        
        Efficient Frontier Visualization: Plotted expected return vs volatility with Sharpe color scaling via Plotly.


# Visa Inc. Risk Modelling Project

This project was developed as part of a university financial time series course. The goal was to assess portfolio risk and volatility for Visa Inc. using AR-GARCH modeling, Monte Carlo simulation, and VaR/Expected Shortfall forecasting.

    ## Key Components
    - 📊 AR-GARCH volatility modeling using `arch` and `statsmodels`
    - 🎯 VaR and Expected Shortfall calculations across 1-, 10-, and 22-day horizons
    - 🧠 Python automation pipeline with traceable risk metric generation
    - 📈 Market data pre-processing from historical Visa Inc. stock prices
    
    ## Skills Demonstrated
    - Time series forecasting under real-world pressure
    - Translating volatility into actionable risk insights
    - Presenting risk metrics to simulated "hedge fund stakeholders"


# Black-Scholes Option Pricing (CQF Coursework)

This project implements a closed-form Black-Scholes-Merton model for pricing European call and put options using Python. The model was developed as part of my CQF (Certificate in Quantitative Finance) learning journey, focusing on applying derivatives pricing theory in a practical, code-driven environment.

      ## 🔍 Key Features
      
      - Closed-form valuation of European call and put options
      - Adjustable parameters: spot price, strike price, risk-free rate, volatility, and time to maturity
      - Built using core libraries: `NumPy`, `SciPy`, and `Matplotlib`

      ## 🧠 Learning Objectives
      
      - Understand the theoretical basis of the Black-Scholes model
      - Translate financial theory into executable Python code
      - Explore the sensitivity of option prices to key input variables


