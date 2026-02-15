# Project Deliverable 3 in MSCS 634: Classification, Clustering, and Association Rule Mining

## Overview
This project applies classification, clustering, and association rule mining to a cleaned dataset to extract predictive and descriptive insights.

## Classification
- Models built: Decision Tree, KNN.
- Hyperparameter tuning: GridSearchCV used to tune KNN (n_neighbors, weights).
- Evaluation: Confusion matrix, ROC curve (AUC), Accuracy, and F1 score.
- Key result: The tuned KNN achieved the best balance of predictive performance (highest F1 and strong ROC-AUC).

## Clustering
- Model: K-Means with standardized features.
- Visualization: PCA 2D scatter plot.
- Group interpretation: Cluster profiles were summarized using feature averages to describe distinct risk/behavior groups.

## Association Rule Mining (FP-Growth)
- Approach: Numeric features were binned to create transaction-like items.
- FP-Growth mined frequent itemsets; association_rules generated rules.
- Strong rules were filtered using confidence and lift.

## Practical Relevance
- Classification supports risk prediction and decision automation.
- Clustering enables customer segmentation (targeted interventions/policies).
- Association rules reveal interpretable co-occurrence patterns for proactive risk strategies.

## Challenges & Fixes
- Imbalanced classes: Used F1 score and ROC-AUC (not accuracy alone) and stratified split.
- Scaling sensitivity: Applied StandardScaler for SVM/KNN and clustering.
- Association rule format: Converted numeric data into bins to enable transaction mining.
