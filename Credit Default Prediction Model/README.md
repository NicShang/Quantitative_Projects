# Credit Default Risk Modeling using Poisson Intensity Approach

## 1. Project Background

This project simulates how a credit model validation team within a bank estimates and verifies the probability of default (PD) for borrowers. It is inspired by the responsibilities of the Credit Model Validation role at Commonwealth Bank of Australia (CBA), with a focus on independent modeling, validation, and result interpretation.

## 2. Why This Approach

Under frameworks such as IRB, IFRS9, and stress testing, banks are required to develop sound and explainable PD models. The Poisson intensity model provides a mathematically grounded method to model default events over time. Its structure allows for continuous-time default modeling and offers strong interpretability, which aligns well with regulatory expectations and validation standards.

## 3. Data Simulation

To support the modeling process, we generate a synthetic dataset that includes:
- `X1` and `X2` as borrower-specific features
- `T` as the time-to-event or loan survival time
- `event` as the observed default outcome, where 1 indicates a default and 0 indicates survival

## 4. Modeling Approach

I use a Poisson process to model the arrival of a default event. The model assumes that the default intensity λ (lambda) is an exponential function of borrower features. Specifically, I define:

λ = exp(Xβ)
S(t) = exp(-λ * t)
PD = 1 - S(t)

where `β` is the parameter vector to be estimated. The model is trained by minimizing the negative log-likelihood using maximum likelihood estimation.

## 5. Model Validation

To evaluate the model’s performance, we implemented the following validation metrics from scratch:
- **ROC curve** and **AUC score** to assess classification power
- **Kolmogorov-Smirnov (KS) statistic** to measure the separation between default and non-default populations
- **Binning chart** to visually assess score calibration and monotonicity

## 6. Stress Testing: Impact of Macroeconomic Shocks

To evaluate model robustness under macroeconomic uncertainty, we introduced interest rate (`X3`) as a proxy stress factor. Using historical RBA cash rate data:
- We randomly sampled interest rates from the historical time series and added them as a new feature `X3`
- The Poisson model was retrained using the new feature set `X1`, `X2`, and `X3`
- Predicted PDs were then analyzed against `X3` to simulate how rising interest rates might impact default probabilities

The result showed a **clear negative relationship** between interest rate levels and predicted PDs. A linear regression trend line over the scatter plot revealed that higher interest rates were associated with lower PDs in the simulated environment, consistent with reduced credit availability or risk-based selection effects.

Interactive visualization was also built using **Plotly**, allowing stakeholders to explore the sensitivity analysis dynamically.

## 7. Future Improvements

Several enhancements can be made to strengthen the model:
- Incorporate additional borrower-level features such as credit history and external ratings
- Extend the model to allow time-varying intensity functions, such as in Cox proportional hazards models
- Introduce macroeconomic scenarios more rigorously, including stress shocks from GDP, unemployment, and inflation
- Split the data into training and testing sets to assess generalization and model stability
- Package the code into a reusable module and add SQL integration for deployment in production environments

---

This project demonstrates a solid understanding of credit risk modeling, strong Python implementation skills, and the ability to validate and communicate model performance. It reflects the core competencies required for credit model validation roles in modern banking environments.
