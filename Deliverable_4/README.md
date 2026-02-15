# Credit Risk Intelligence: End-to-End Data Mining for Delinquency Prediction

## Dataset Summary
- **Dataset:** Credit Risk Benchmark Dataset  
- **Size:** ~150,000 records with 11 key attributes  
- **Focus:** Credit behavior, repayment history, utilization, debt burden, and delinquency risk  
- **Data challenges:** Missing values (notably income/dependents), outliers/noise, and class imbalance in the delinquency target  

## Project Steps
1. **Data Loading and Inspection**
   - Imported data, checked schema, and reviewed shape/types.
2. **Data Quality Checks**
   - Identified missing values, duplicate rows, and suspicious/invalid values.
3. **Data Cleaning and Preprocessing**
   - Removed duplicates, treated zero-income values, imputed missing values, and capped outliers.
4. **Exploratory Data Analysis (EDA)**
   - Examined distributions, boxplots, correlation heatmap, and class distribution.
5. **Regression Modeling**
   - Built and compared Linear Regression, Ridge, and Lasso with scaling and engineered features on a continuous burden-score target.
6. **Classification Modeling**
   - Trained Decision Tree and KNN; tuned KNN with GridSearchCV; evaluated using F1, confusion matrix, and ROC-AUC.
7. **Clustering**
   - Applied K-Means to identify borrower segments and profiled cluster characteristics.
8. **Association Rule Mining**
   - Used Apriori on binned transaction-style features to discover frequent patterns and high-lift rules.

## Deliverable Alignment
- **Deliverable 1:** Data quality assessment, cleaning, outlier handling, and EDA.
- **Deliverable 2:** Feature engineering and regularized regression benchmarking.
- **Deliverable 3:** Classification, K-Means clustering, and Apriori-based association rule mining.
- **Deliverable 4 (this README):** Consolidated end-to-end insights and recommendations.

## Major Findings
- Delinquency-related features (`late_30_59`, `late_60_89`, `late_90`) are among the strongest predictors of risk.
- Financial stress indicators (`debt_ratio`, `rev_util`, income-derived features) provide high predictive signal.
- Cleaning + feature engineering + scaling/regularization improved model stability and performance.
- Tuned models outperformed baseline versions, and unsupervised methods revealed meaningful risk segments and behavior patterns.

## Future Improvements and Considerations
- **Model expansion:** Compare current methods with ensemble models (for example, Random Forest, XGBoost, LightGBM) and calibration techniques for risk probability quality.
- **Imbalance handling:** Evaluate SMOTE, class weights, and threshold tuning to improve minority-class recall without sacrificing precision.
- **Feature enrichment:** Add temporal behavior trends, bureau-derived variables, and interaction features that better capture borrower risk dynamics.
- **Robust validation:** Include nested cross-validation, stability checks across random seeds, and segment-level validation to confirm generalization.
- **Interpretability and governance:** Add SHAP-based explainability, bias/fairness checks, and model-monitoring rules for drift and performance decay.
- **Deployment readiness:** Design a repeatable training/inference pipeline with versioning, scheduled retraining, and automated reporting for business stakeholders.