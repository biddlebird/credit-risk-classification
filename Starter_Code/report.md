## Overview of the Analysis

In this analysis, the objective was to develop a machine learning model to assess loan risk by classifying loans as either "healthy" (`0`) or "high-risk" (`1`). The financial data contained loan-related variables, and the goal was to predict the risk category of each loan to help financial institutions identify potentially risky loans before approving them.

The target variable for the analysis was binary, with two labels:
- `0` representing "healthy loans"
- `1` representing "high-risk loans"

Using `value_counts`, we observed an imbalance between classes, with healthy loans (`0`) being far more prevalent than high-risk loans (`1`). This imbalance posed challenges for model accuracy and recall, especially for the minority class (`1`).

The machine learning process involved the following steps:
1. **Data Preparation:** Loading and inspecting the dataset, separating features (`X`) and target (`y`), and splitting the data into training and testing sets.
2. **Model Selection:** Logistic Regression was chosen as a straightforward yet powerful model for binary classification.
3. **Model Training:** We instantiated and trained the Logistic Regression model using the training data.
4. **Model Evaluation:** After making predictions on the test set, we evaluated model performance using metrics such as accuracy, precision, recall, and the F1-score.

## Results

- **Machine Learning Model 1: Logistic Regression**
   - **Accuracy:** 99%
   - **Precision for `0` (healthy loan):** 1.00
   - **Recall for `0` (healthy loan):** 0.99
   - **Precision for `1` (high-risk loan):** 0.84
   - **Recall for `1` (high-risk loan):** 0.94
   - **F1-Score for `1` (high-risk loan):** 0.89

## Summary

The Logistic Regression model performed best in terms of accuracy and balance between precision and recall. This model achieved an overall accuracy of 99% and handled the class imbalance fairly well. It demonstrated strong predictive ability for healthy loans, with near-perfect precision and recall. Although precision was slightly lower for high-risk loans, recall was still high at 0.94, meaning the model was effective at identifying most high-risk loans, a crucial factor when assessing loan risk.

In this scenario, recall for high-risk loans (`1`) is more critical, as failing to identify these could result in significant financial losses. Therefore, the Logistic Regression model is recommended for this application, as it provides a balanced approach that prioritizes correctly identifying high-risk loans while maintaining accuracy for healthy loans.
