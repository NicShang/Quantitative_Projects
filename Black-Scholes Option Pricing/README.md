# Black-Scholes Option Pricing | Quantitative Finance Project

This project implements the **Black-Scholes-Merton model** to price European call and put options. It provides a hands-on demonstration of derivatives pricing using Python and interactive visualizations to build intuition around option mechanics.

---

## Project Objectives
- Apply the Black-Scholes formula to value European call and put options.
- Analyze how key inputs (stock price, volatility, time to maturity, interest rate) affect option pricing.
- Visualize payoffs, time value decay, and option value surfaces under different market conditions.

---

## Tools & Libraries
- `NumPy` – vectorized calculations
- `SciPy.stats.norm` – cumulative distribution function
- `Matplotlib` – static and dynamic payoff visualization
- `IPyWidgets` – sliders for live scenario adjustments

---

## Core Functions
- Closed-form Black-Scholes pricing functions:
  - `black_scholes_call_price()`
  - `black_scholes_put_price()`
- Plotting utilities for:
  - Payoff diagrams (long/short calls & puts)
  - Time value vs. intrinsic value
  - Value surfaces over a range of prices and maturities

---

## Key Features
- Interactive widgets for real-time exploration of pricing mechanics
- Time-decay illustration for both intrinsic and extrinsic value
- Clear modular code structure for reuse in other models (e.g., binomial trees, greeks)


