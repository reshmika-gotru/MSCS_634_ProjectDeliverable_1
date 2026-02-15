# MSCS_634_ProjectDeliverable_2 — Regression Modeling and Performance Evaluation
**Name:** Reshmika Gotru

## Dataset
**Name:** credit_risk_benchmark_dataset_cleaned.csv   
**Description:** This dataset contains credit-related attributes such as utilization, income, debt ratio, delinquency counts, and related risk indicators. The objective is to predict a continuous target value using regression.
# Engineering Features
Among the primary engineered features were:
To lessen skew, use log transforms (such as log_monthly_inc and log_debt_ratio).
Util_x_debt is the interaction term.
- Delinquency aggregates: late severity and late total
- Ratios: dep_per_open_credit 
# Models Built
1. **Linear Regression** (baseline)
2. **Ridge Regression** (L2 regularization)
3. **Lasso Regression** (L1 regularization)
Using GridSearchCV over a log-spaced alpha grid, Ridge and Lasso's hyperparameters were adjusted.
# Performance Evaluation
- **Metrics:** MSE, RMSE, MAE, R²
- **Cross-Validation:** 5-fold CV to assess generalization.
- **Results:** Ridge and Lasso outperformed Linear Regression, with Ridge slightly better in terms of RMSE and R².
## Visualizations
Generated plots:
- Cross-validated R² comparison across models
- Predicted vs Actual (best model)
- Residual distribution (best model)
## Challenges & Resolutions
- **Missing values:** addressed using imputation within pipelines.
- **Skewed variables:** reduced using log transforms.
- **Regularization sensitivity to scale:** fixed by applying StandardScaler.
# Conclusion
Regularization improved performance by reducing overfitting. Future work could explore more complex models (e.g., Random Forest, XGBoost) and additional feature engineering.
