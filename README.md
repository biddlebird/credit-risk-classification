# Loan Risk Prediction using Logistic Regression

## Overview

This project aims to classify loans as either "healthy" (low risk) or "high-risk" (high default likelihood) using a machine learning model, specifically a logistic regression classifier. The primary objective is to help financial institutions make informed decisions by predicting the likelihood of loan default based on historical data.

## Table of Contents

- [Project Structure](#project-structure)
- [Data Description](#data-description)
- [Analysis Process](#analysis-process)
- [Results](#results)
- [Dependencies](#dependencies)
- [How to Run](#how-to-run)

## Project Structure

```
Loan-Risk-Prediction/
│
├── Starter_Code/
│   ├── Resources/
│   │   └── lending_data.csv        # The CSV data file containing loan information
│   └── loan_risk_prediction.ipynb  # Jupyter Notebook with code and analysis
│
├── README.md                       # Project overview and instructions
└── results/                        # Folder for storing outputs (optional)
    ├── model_performance.png       # Visualization of model results
    └── report.txt                  # Classification report output
```

## Data Description

The dataset includes financial information on individual loans, and each record is labeled to indicate whether a loan is high-risk (`1`) or healthy (`0`). The data has multiple columns that may represent factors like income, debt-to-income ratio, credit score, and more.

- **Target Variable (`y`)**: Indicates the risk category of each loan (`0` for healthy, `1` for high-risk).
- **Feature Variables (`X`)**: Financial and demographic attributes that contribute to loan risk.

The target variable is slightly imbalanced, with more instances of healthy loans than high-risk ones.

## Analysis Process

1. **Data Loading and Preparation**:
   - Load data into a Pandas DataFrame.
   - Separate the target (`y`) and feature variables (`X`).

2. **Model Selection**:
   - Logistic Regression was chosen for this binary classification task.

3. **Model Training**:
   - Split the data into training and test sets (80/20 split).
   - Train the Logistic Regression model on the training data.

4. **Model Evaluation**:
   - Generate predictions on the test set.
   - Evaluate using accuracy, precision, recall, and F1-score.
   - Analyze the confusion matrix and classification report for detailed performance.

## Results

The Logistic Regression model performed with an accuracy of 99%. Below are key metrics from the classification report:

| Metric       | Healthy Loans (0) | High-Risk Loans (1) |
|--------------|--------------------|----------------------|
| Precision    | 1.00               | 0.84                |
| Recall       | 0.99               | 0.94                |
| F1-Score     | 1.00               | 0.89                |

### Summary

The model performed well across both classes. Given the importance of predicting high-risk loans accurately, the high recall of 0.94 for the `1` class (high-risk) makes this model a strong candidate for loan risk assessment.

## Dependencies

- Python 3.x
- Pandas
- Scikit-learn
- Jupyter Notebook

## How to Run

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd Loan-Risk-Prediction
   ```

2. Open the Jupyter Notebook:
   ```bash
   jupyter notebook Starter_Code/loan_risk_prediction.ipynb
   ```

3. Run the cells in the notebook to perform data loading, model training, and evaluation.
