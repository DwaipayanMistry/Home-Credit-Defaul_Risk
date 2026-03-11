# Credit Risk Prediction — Home Credit Default Risk

## Overview

This project analyzes borrower financial data to identify key factors influencing **loan default risk** and builds a machine learning model to predict the probability of default.

Using the **Home Credit Default Risk** dataset, the project performs exploratory data analysis, feature engineering, and predictive modeling to understand borrower behavior and develop a credit risk prediction pipeline.

The goal is to demonstrate how **data analytics and machine learning can support financial institutions in improving credit risk assessment and reducing potential losses.**

---

## Problem Statement

Financial institutions must evaluate the risk associated with lending money to borrowers. Poor risk assessment can lead to significant financial losses due to loan defaults.

This project aims to:

- Analyze borrower demographics and financial characteristics
- Identify key indicators of default risk
- Engineer predictive features from multiple data sources
- Train a machine learning model to estimate default probability

---

## Dataset

Dataset used: **Home Credit Default Risk (Kaggle)**

Main datasets used:

| Dataset               | Description                               |
| --------------------- | ----------------------------------------- |
| application_train     | Borrower application information          |
| bureau                | Credit history from external institutions |
| previous_application  | Previous loan applications                |
| installments_payments | Installment payment history               |

These datasets contain demographic, financial, and behavioral information about borrowers.

---

## Project Structure

```
credit-risk-analysis
│
├── notebooks
│   ├── eda_analysis.ipynb
│   └── predictive_modeling.ipynb
│
├── data
│   └── dataset files
│
├── figures
│   └── visualization outputs
│
└── README.md
```

---

## Exploratory Data Analysis

The EDA focuses on identifying patterns related to borrower risk.

Key analyses include:

- Age and employment stability
- Income and credit distribution
- Loan burden metrics
- External credit scores
- Payment behavior analysis
- Credit exposure indicators
- Correlation analysis

These analyses help uncover relationships between borrower characteristics and default probability.

---

## Feature Engineering

Several financial risk indicators were created to improve predictive performance.

Examples:

- AGE
- EMPLOYMENT_YEARS
- CREDIT_INCOME_RATIO
- ANNUITY_INCOME_RATIO
- CREDIT_GOODS_RATIO
- EXT_SOURCE_MEAN
- MEAN_PAYMENT_DELAY
- BUREAU_LOAN_COUNT

These features capture borrower financial capacity, credit history, and repayment behavior.

---

## Predictive Modeling

A **LightGBM classifier** was trained to predict loan default probability.

Model pipeline:

1. Data preprocessing
2. Feature engineering
3. Train-validation split
4. LightGBM model training
5. Model evaluation using ROC-AUC
6. Feature importance analysis

LightGBM is well suited for tabular financial datasets and is widely used in credit risk modeling.

---

## Model Evaluation

The model is evaluated using **ROC-AUC**, which measures the model's ability to distinguish between defaulters and non-defaulters.

Feature importance analysis reveals the most influential predictors of default risk.

Typical key drivers include:

- External credit scores
- Credit-to-income ratio
- Loan payment burden
- Borrower age
- Employment stability

---

## Key Insights

Important findings from the analysis include:

- External credit scores are the strongest predictors of default risk.
- Borrowers with higher credit-to-income ratios face greater financial pressure.
- Higher annuity-to-income ratios indicate increased repayment burden.
- Late installment payments are associated with higher default probability.
- Default risk results from the interaction of demographics, financial capacity, and repayment behavior.

---

## Technologies Used

Python
Pandas
NumPy
Scikit-learn
LightGBM
Matplotlib
Seaborn

These tools were used for data processing, analysis, and machine learning modeling.

---

## How to Run the Project

1. Clone the repository

```
git clone <repository-url>
```

2. Install dependencies

```
pip install pandas numpy scikit-learn lightgbm matplotlib seaborn
```

3. Download the dataset from Kaggle and place it in the project directory.
4. Run the notebooks:

- eda_analysis.ipynb
- predictive_modeling.ipynb

---

## Business Impact

This project demonstrates how machine learning can support **credit risk assessment** in financial institutions.

Potential applications include:

- Improving credit scoring models
- Identifying high-risk borrowers
- Reducing loan default losses
- Supporting data-driven lending decisions

---

## Future Improvements

Possible extensions include:

- Hyperparameter tuning
- Cross-validation
- Advanced feature engineering
- Model comparison (XGBoost, CatBoost)
- Model explainability using SHAP

---

## Author

Dwaipayan Mistry
