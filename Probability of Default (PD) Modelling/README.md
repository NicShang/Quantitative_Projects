# Intensity-based Probability of Default (PD) Modelling

This project applies **credit risk modelling techniques** learned during the CQF program to build a Probability of Default (PD) model. The focus is on **intensity-based approaches**, which model default as a stochastic process rather than a single balance-sheet event. This method is consistent with practices in risk management frameworks such as **IFRS 9** and **Basel**.

---

## Project Overview
The project simulates client credit data with financial drivers and applies an **intensity-based Poisson model** to estimate default probabilities. The model is calibrated using **maximum likelihood estimation (MLE)** and evaluated with **ROC/AUC metrics** to assess discriminatory power.  

The workflow mirrors tasks in credit risk teams:
- Data simulation and cleaning
- Model parameter estimation
- Performance evaluation with statistical metrics
- Regulatory-style reporting outputs

---

## Methodology

### 1. Data Simulation
- Generated synthetic client data with key financial drivers such as leverage (X1) and income growth (X2).
- Defined observation horizons and simulated default events using **exponential survival distributions**.

### 2. Model Construction
- Built a **Poisson Intensity PD Model** where  
  λ = exp(Xβ), linking financial features to default intensity.
- Defined the negative log-likelihood function for parameter estimation.

### 3. Parameter Estimation
- Used **maximum likelihood estimation (MLE)** to fit model parameters β.
- Ensured convergence and interpretability of coefficients.

### 4. Model Evaluation
- Assessed model discriminatory power using **ROC curves** and **AUC scores**.
- Interpreted outputs in the context of credit risk monitoring and early warning indicators.

---

## Key Results
- Successfully simulated default events across varying horizons.  
- Estimated intensity parameters that reflect sensitivity to leverage and income growth.  
- Achieved strong ROC/AUC results, showing the model can distinguish between defaulting and non-defaulting clients.  

---

## Transferable Value
This project demonstrates:
- Practical ability to **design and implement PD models** relevant to risk management.  
- Strong foundation in **mathematical statistics, maximum likelihood estimation, and survival analysis**.  
- Experience in **model monitoring, validation, and regulatory alignment**.  
- Clear applicability to **developing, validating, and maintaining credit risk models (PD, LGD, EAD)** in line with industry standards.  

---

## Technical Stack
- **Python**: Data simulation, modelling, and evaluation  
- **NumPy / Pandas**: Data handling  
- **SciPy**: Parameter optimization  
- **Matplotlib / scikit-learn**: ROC/AUC evaluation and visualization  

---

## Next Steps
- Extend the framework to **Loss Given Default (LGD)** and **Exposure at Default (EAD)** modelling.  
- Incorporate **stress testing scenarios** to assess model robustness under adverse conditions.  
- Explore migration to **cloud-based environments** for scalability and integration with production workflows.  

