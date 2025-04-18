# Clinical Trial Enrollment Duration Prediction

This project focuses on predicting the enrollment duration of clinical trials using machine learning models. Accurate prediction of enrollment time can significantly reduce delays in clinical trials, optimize patient recruitment, and improve overall trial efficiency.

---

## Project Overview

Clinical trials often face delays due to inefficient enrollment planning, which impacts drug development timelines and costs. This project uses data from ClinicalTrials.gov, including structured and unstructured features, to build predictive models that estimate how long patient enrollment will take in interventional studies.

---

## Data Collection & Preprocessing

- **Data Source:** ClinicalTrials.gov dataset focusing on interventional studies.
- **Features:** Study phases, interventions, enrollment numbers, conditions, age groups, and primary outcomes.
- **Handling Missing Values:** 
  - Categorical variables filled with 'Unknown'.
  - Numerical variables filled with median values to avoid outlier distortion.
- **Encoding:** One-hot encoding for categorical variables.
- **Feature Engineering:** Log transformation applied to enrollment numbers to normalize skewed data.
- **Data Split:** 80% training, 20% testing.

---

## Models Used

- **Linear Regression:** Baseline model.
- **Random Forest Regressor:** Handles non-linear relationships and provides feature importance.
- **Gradient Boosting Regressor:** Balances bias-variance trade-offs for improved accuracy.

Hyperparameters were optimized using GridSearchCV, and SHAP values were used for model explainability.

---

## Model Performance

| Metric          | Random Forest | Gradient Boosting | Linear Regression |
|-----------------|---------------|-------------------|-------------------|
| RMSE            | 0.0022        | 0.0117            | 1.19              |
| MAE             | 0.00029       | -                 | -                 |
| R² Score        | 0.99999       | -                 | 0.13              |
| Adjusted R²     | 0.99999       | -                 | -                 |
| SMAPE           | 0.0030        | 0.1478            | -                 |

Random Forest outperformed all models, showing near-perfect accuracy and minimal prediction bias.

---

## Key Features Impacting Enrollment Duration

- **Enrollment Numbers:** Most influential predictor; larger trials take longer.
- **Study Phases:** Phase 3 and 4 trials have longer durations.
- **Age Group:** Trials involving older adults tend to have longer enrollment.
- **Interventions:** Complex trials with multiple interventions require more time.
- **Conditions:** Certain diseases require specialized patient selection, affecting enrollment speed.

---

## Explainability

SHAP (SHapley Additive exPlanations) was used to interpret model predictions, helping identify how each feature contributes to enrollment duration. This transparency supports clinical trial planners in refining recruitment strategies.

---

## Challenges & Future Work

- **Challenges:**
  - Dataset imbalance with underrepresented conditions/phases.
  - Missing external factors like geographic location and investigator experience.
  - Trade-off between model complexity and explainability.

- **Future Enhancements:**
  - Expand dataset to include global clinical trials.
  - Incorporate additional features such as trial location.
  - Deploy model as a real-time decision support tool for clinical research organizations and pharmaceutical companies.

---

## Business & Clinical Relevance

- Optimizes study design and feasibility assessments.
- Enhances resource allocation and patient recruitment strategies.
- Supports faster regulatory approvals by reducing trial delays.
- Potential to scale into a clinical decision support system for biotech firms and regulatory agencies.

---

## References & Sources

- ClinicalTrials.gov dataset
- SHAP explainability framework
- Research articles on clinical trial enrollment and design impacts

---

Feel free to explore the code and data to reproduce the results or extend the model for other clinical trial datasets.

Citations:
[1] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/64706810/faf19ba5-7586-4e2c-af57-65017219ac24/ps2_final_PPT.pdf

---
Answer from Perplexity: https://www.perplexity.ai/search/go-through-attachment-and-tell-6ZDFsrVVRbWXg9Fij3iyIg?utm_source=copy_output
