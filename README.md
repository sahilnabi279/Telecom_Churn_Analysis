# Telecom Customer Churn Analysis

An end-to-end machine learning project that analyzes telecom customer data and predicts customer churn to support proactive retention strategies.

## Project Overview
Customer churn can reduce recurring revenue and customer lifetime value. This project combines two customer datasets, explores churn patterns, preprocesses the data, trains and evaluates multiple classification models, and generates churn-risk scores and retention recommendations.

## Dataset
- 100,000 customer records
- Client.csv: customer/household attributes
- Record.csv: customer records and churn-related attributes
- Target: `churn` (0 = retained, 1 = churn)


## Workflow
1. Load and inspect data
2. Merge datasets using `Customer_ID`
3. Explore churn distribution, missingness, and feature relationships
4. Impute missing values (median for numeric, most frequent for categorical)
5. One-hot encode categorical variables and scale numeric variables
6. Stratified 80/20 train-test split
7. Compare Logistic Regression, Random Forest, and Extra Trees
8. Generate risk scores, feature importance, retention recommendations, and illustrative business scenarios

## Results
- **Best model:** Random Forest
- **Accuracy:** 0.62
- **Precision:** 0.61
- **Recall:** 0.66
- **F1-score:** 0.63
- **ROC-AUC:** 0.67
- **High-risk customers identified:** 3,107

These metrics indicate useful predictive signal, while also leaving room for improvement through feature engineering, threshold optimization, and further model tuning.

## Repository Structure
```
data/               
notebooks/             # Analysis notebook
models/                # Saved model pipeline
outputs/
  charts/              # Visualizations
  results/             # CSV reports, risk lists, and summaries
```

## Setup
Use Python 3.12 recommended.

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
```


## Notes
- The business-impact scenarios are illustrative and depend on assumptions; they are not profit estimates.
- Customer-level risk outputs may contain sensitive information. Avoid sharing them publicly unless the data is anonymized and authorized.
- Dataset churn proportion should not automatically be interpreted as the real-world telecom churn rate.

## Author
Sahil Nabi
