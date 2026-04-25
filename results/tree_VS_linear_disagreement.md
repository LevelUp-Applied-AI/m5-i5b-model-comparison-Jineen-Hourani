# Tree vs. Linear Disagreement Analysis

## Sample Details

- **Test-set index:** 4060
- **True label:** 0
- **RF predicted P(churn=1):** 0.5998
- **LR predicted P(churn=1):** 0.1700
- **Probability difference:** 0.4299

## Feature Values

- **tenure:** 36.0
- **monthly_charges:** 20.0
- **total_charges:** 1077.33
- **num_support_calls:** 2.0
- **senior_citizen:** 0.0
- **has_partner:** 0.0
- **has_dependents:** 0.0
- **contract_months:** 1.0

## Structural Explanation

> "The Random Forest predicted a high churn probability (0.60) compared to the Logistic Regression (0.17). This disagreement likely stems from the tree model capturing a **non-linear interaction** between a short contract (`contract_months: 1.0`) and moderate `tenure` (36 months). While the linear model sees 36 months of tenure as a strong negative signal for churn (weighted by a fixed coefficient), the Random Forest identifies that even long-term customers are at high risk if they are currently on a month-to-month contract."



