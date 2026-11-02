# Customer Churn Prediction: Telco Customers

**Final Data Science Capstone Project (Task 6)** | Arifa Begum R | YuvaIntern Data Engineer Internship

## Problem
A telecom company loses about 26.5% of its customers (1,869 of 7,043). This project finds out who is likely to leave, why, and what the company should do about it.

## Dataset
Telco Customer Churn (Kaggle, user *blastchar*): 7,043 customers, 21 columns covering demographics, services, contract, billing and the target `Churn`.
File: `WA_Fn-UseC_-Telco-Customer-Churn.csv`

## What the notebook does
1. Problem statement and objectives
2. Data cleaning (fixed `TotalCharges`, which was stored as text, 11 blank rows with tenure 0)
3. Exploratory data analysis (contract, tenure, charges, services, demographics)
4. Correlation analysis and removal of duplicated information
5. Feature engineering and 80/20 stratified train/test split
6. Modeling: Logistic Regression and Random Forest
7. Interpretation (feature importance, odds ratios) and 5-fold cross-validation
8. Business value of retention
9. Recommendations, limitations and future scope, conclusion

## Key results
| Model | Accuracy | Precision | Recall | F1 | ROC-AUC |
|---|---|---|---|---|---|
| Logistic Regression | 0.742 | 0.509 | 0.775 | 0.614 | 0.839 |
| Random Forest | 0.749 | 0.518 | 0.791 | 0.626 | 0.840 |

- Baseline "nobody churns" accuracy is 0.735, so accuracy alone is misleading; recall and ROC-AUC are used.
- Cross-validated ROC-AUC: 0.843 (Logistic Regression), 0.844 (Random Forest).
- Main drivers: month-to-month contract (42.7% churn), first year of tenure (47.4%), Fiber optic internet (41.9%), electronic check payment (45.3%).
- Churn costs about 1.67M a year in revenue;
