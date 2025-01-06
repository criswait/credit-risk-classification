# Credit Risk Analysis Report

## Overview of the Analysis
This analysis aimed to evaluate the performance of a machine learning model in predicting credit risk. The goal was to build a model capable of accurately identifying borrowers likely to default on loans (high-risk loans) versus those likely to repay their loans (healthy loans). By leveraging historical lending data, this analysis provides insights that can be used to enhance decision-making processes in credit risk assessment.

The dataset used for this analysis contains financial information about borrowers, such as: 
- Loan size
- Interest rate
- Borrower income
- Debt-to-income ratio
- Number of accounts
- Derogatory marks
- Total debt

The target variable, loan_status, indicates whether a loan is healthy (0) or high-risk (1). The dataset was highly imbalanced, with the majority of loans being healthy.

## Machine Learning Process
1. Data Preparation:
     - The dataset was split into features (X) and labels (y).
     - Training and testing datasets were created using an 80/20 split.
  
2. Model Selection:
     - A logistic regression model was chosen as the baseline algorithm due to its simplicity and effectiveness in binary classification tasks.

3. Model Training and Prediction:
     - The logistic regression model was trained on the training dataset (X_train, y_train).
  
4. Model Evaluation:
     - The performance of the model was evaluated using a confusion matrix and classification report, focusing on accuracy, precision, recall, and F1-scores.
  
## Results
Logistic Regression Model:
- Accuracy: 99%
- Precision:
     - Class 0 (Healthy Loans): 1.00
     - Class 1 (High-Risk Loans): 0.86

- Recall:
     - Class 0 (Healthy Loans): 1.00
     - Class 1 (High-Risk Loans): 0.91

- F1-Score:
     - Class 0 (Healthy Loans): 1.00
     - Class 1 (High-Risk Loans): 0.88
 
## Summary
The logistic regression model demonstrated strong performance, particularly for predicting healthy loans (0), achieving perfect precision, recall, and F1-score. It also performed well in predicting high-risk loans (1), with a recall of 91% and an F1-score of 0.88. This indicates that the model successfully identifies the majority of high-risk loans while maintaining a low rate of false positives.

## Recommendation
The logistic regression model is suitable for deployment in this context of credit risk analysis. However, improvements can be made to address the imbalance in the dataset better and further enhance the prediction of high-risk loans. Techniques such as oversampling the minority class or using class weights could be explored to improve the precision for high-risk loans.

Given the financial implications of misclassifying high-risk loans, prioritizing recall for class 1 is critical to minimize missed defaults. Therefore, the current model provides a solid baseline but should be fine-tuned for optimal performance in real-world applications.
