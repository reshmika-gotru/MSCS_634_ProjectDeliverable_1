# Project Deliverable 1 in MSCS 634: Data Collection, Cleaning, and Exploration# Summary of the Dataset
- Dataset: Benchmark Credit Risk Dataset
16,714 records
Characteristics: 11
- Goal (for further modeling): dlq_2yrs (binary)

# Justification for Dataset Selection:
The Credit Risk Benchmark Dataset from Kaggle was selected for this data mining project. It contains 150,000 borrower records with 11 attributes, meeting and exceeding the project requirements for size and feature count. The dataset includes a binary target variable indicating default status and features such as income, debt ratio, age, and delinquency history. It presents realistic data quality challenges including missing values (20% in MonthlyIncome), outliers (values 96/98 in delinquency features), and class imbalance (6.7% default rate). These characteristics support all four project phases: data cleaning (Deliverable 1), classification modeling (Deliverable 2), clustering and association mining (Deliverable 3), and business insights for lending decisions (Deliverable 4). The dataset thus provides an ideal foundation for applying the data mining concepts and techniques covered in this course

# Important Actions Taken:
1. The dataset was loaded and its structure (data kinds, shape) examined.
2. Verified duplication and missing values.
3. Duplicates were eliminated.
4. Converted monthly_inc = 0 to missing and imputed, treating dubious values.
5. By capping specific columns, noisy extreme outliers were found and dealt with.
6. Conducted EDA using target comparisons, correlation heatmaps, boxplots, and distributions.

# Important Takeaways:
The distribution of target classes is rather balanced.
Extreme outliers can be found in rev_util and debt_ratio; cleansing increases stability.
Variables pertaining to late payments seem to be very important in forecasting dlq_2 years.

# Difficulties & Solutions:
The problem: Distributions were skewed by extreme outliers.
  Winsorization or capping at the first and 99th percentiles is the solution.
The problem was that monthly_inc had zeros, which probably indicated missing data.
  The median was used to impute the zeros once they were converted to NaN.