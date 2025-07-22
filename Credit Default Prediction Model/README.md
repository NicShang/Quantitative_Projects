# Credit Default Risk Modeling using Poisson Intensity Approach

## 1. Project Background

This project simulates how a credit model validation team within a bank estimates and verifies the probability of default (PD) for borrowers. It is inspired by the responsibilities of the Credit Model Validation role at Commonwealth Bank of Australia (CBA), with a focus on independent modeling, validation, and result interpretation.

## 2. Why This Approach

Under frameworks such as IRB, IFRS9, and stress testing, banks are required to develop sound and explainable PD models. The Poisson intensity model provides a mathematically grounded method to model default events over time. Its structure allows for continuous-time default modeling and offers strong interpretability, which aligns well with regulatory expectations and validation standards.

## 3. Data Simulation

To support the modeling process, we generate a synthetic dataset that includes:
- X1 and X2 as borrower-specific features
- T as the time-to-event or loan survival time
- event as the observed default outcome, where 1 indicates a default and 0 indicates survival

## 4. Modeling Approach

We use a Poisson process to model the arrival of a default event. The model assumes that the default intensity lambda is an exponential function of borrower features. Specifically, we define lambda as exp(X * beta), where beta is a parameter vector. The survival function is given by S(t) = exp(-lambda * t), and the probability of default is calculated as 1 minus the survival probability. We estimate the model parameters by minimizing the negative log-likelihood function using maximum likelihood estimation.

## 5. Model Validation

To evaluate the model performance, we use three standard metrics:
- ROC curve and AUC score to assess the model’s ability to distinguish between default and non-default cases
- KS statistic to measure the separation between good and bad borrowers
- Binning chart to compare the predicted scores with actual default rates across score buckets

## 6. Visualization and Key Findings

The AUC score is approximately 0.68, which indicates moderate predictive power. The KS value reaches around 0.25, suggesting the model is able to distinguish between defaulters and non-defaulters to a reasonable extent. The binning chart shows that the actual default rate increases with the predicted score, which confirms that the model captures the correct directional relationship between credit risk and score.

## 7. Future Improvements

Several enhancements can be made to strengthen the model:
- Incorporate additional borrower-level features such as credit history and external ratings
- Extend the model to allow time-varying intensity functions, such as in Cox proportional hazards models
- Introduce macroeconomic variables to support stress testing scenarios
- Split the data into training and testing sets to assess generalization and stability
- Package the code into a reusable module and add SQL integration for deployment in production environments

This project demonstrates a solid understanding of credit risk modeling, strong Python implementation skills, and the ability to validate and communicate model performance. It reflects the core competencies required for credit model validation roles in modern banking environments.
