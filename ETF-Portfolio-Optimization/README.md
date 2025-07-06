# ETF Portfolio Optimization | Mandate-Constrained Allocation Engine

This project builds a systematic asset allocation pipeline tailored for institutional ETF portfolios, designed to align with long-horizon return mandates (e.g., CPI+6%) and regulatory-style constraints. It offers robust performance simulation, intuitive visualization, and a reusable codebase supporting strategic portfolio design and communication.

## Objective

To construct a transparent and reusable optimization engine that:

- Meets predefined mandate objectives (e.g., CPI+6% real return)
- Embeds policy constraints (e.g., ≥65% core, ≤15% satellite)
- Enables quantitative justification of portfolio construction decisions  
- Supports scenario testing for stress-aware investment planning

## Methodology

- **Languages/Libraries**: Python (`pandas`, `numpy`, `scipy`, `plotly`)
- **Modeling Features**:
  - Log-transformed ETF price returns with missing data handling
  - Modular portfolio optimizer (Sharpe-maximizing under constraints)
  - Monte Carlo simulation (5,000 randomized portfolios) for stress testing
- **Visualization Tools**:
  - Efficient frontier, optimal allocation zones, drawdown diagnostics
  - Interactive charts (Plotly) for stakeholder reporting

## Business Value

This project mirrors the decision workflow of superannuation funds, wealth managers, and institutional consultants, offering:

- **Mandate-Driven Allocation Support**: Empowers investment teams to validate whether proposed ETF portfolios satisfy real-return targets under regulatory or client-imposed constraints  
- **Risk-Aware Scenario Planning**: Enables simulation-based understanding of downside exposure under various market regimes  
- **Clear Stakeholder Communication**: Provides intuitive visual outputs (efficient frontier, allocation diagnostics) that bridge technical optimization with practical decision-making  
- **Reusable Architecture**: The Python-based framework is modular and scalable, supporting different asset sets, client mandates, or strategy overlays with minimal changes  

This solution provides not only analytical rigor but also improves communication between quantitative analysts, portfolio managers, and non-technical stakeholders—making it suitable for real-world advisory, asset allocation, or investment committee settings.
