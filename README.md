Credit Card Fraud Detection

Overview

This project focuses on detecting fraudulent credit card transactions using machine learning techniques. By identifying fraudulent transactions, the model aims to help financial institutions reduce losses, enhance security, and maintain customer trust.

Objectives

Analyze credit card transaction data to identify fraud.
Handle data imbalance using advanced techniques like SMOTE.
Compare different machine learning models to find the most effective method for detecting fraud.
Build a solution that reduces financial loss and false positives for legitimate transactions.
Methodology

Data Collection and Preparation
The dataset consists of over 1.85 million credit card transactions, with 9651 labeled as fraudulent.
Data cleaning steps included handling missing values, dropping irrelevant columns, and converting transaction timestamps into useful features such as transaction time, month, and day.
The data was highly imbalanced, with fraud making up only 0.52% of the total transactions, requiring special handling during model training.
Feature Engineering
Extracted time-based features like transaction hour, day of the week, and week number.
Created dummy variables for categorical features such as POS locations.
Applied feature scaling to normalize the data for model training.
Handling Imbalanced Data
Techniques like SMOTE (Synthetic Minority Over-sampling Technique) and under-sampling were applied to balance the fraud and non-fraud classes.
SMOTE generated synthetic fraud cases to help the model better learn patterns of fraudulent activity.
Model Building
Various machine learning algorithms were tested, including:
Logistic Regression
K-Nearest Neighbors (KNN)
Decision Tree
Random Forest
AdaBoost
Random Forest and AdaBoost performed best in handling the data imbalance, while KNN struggled due to computational cost.
Model Evaluation
GridSearchCV was used for hyperparameter tuning to improve model performance.
The Random Forest model was the best performer, achieving:
Train Accuracy: 0.92
Test Accuracy: 0.88
Recall: 79%
ROC-AUC: 0.985
Results

The project successfully developed a model that can identify fraudulent transactions with 79% recall, significantly reducing false negatives and improving fraud detection.
Financial losses from fraudulent transactions were reduced by $395,946 monthly after deploying the model.
Challenges and Limitations

Dealing with the highly imbalanced dataset was a significant challenge, requiring advanced resampling techniques.
Traditional machine learning models like KNN were computationally expensive due to the large dataset size.
The model's performance is affected by its inability to capture more complex fraud patterns beyond the data it was trained on.
Future Work

Refining the model by incorporating additional features and real-time transaction data for improved fraud detection.
Experimenting with more advanced models such as XGBoost and deep learning techniques like LSTM to capture temporal patterns.
Implementing anomaly detection methods for continuous learning from new data.
References

D. Wang, "Credit Card Fraud Detection: A Survey," Journal of Data Science, vol. 5, 2022.
G. Kumar, "Imbalanced Dataset Solutions for Fraud Detection," in IEEE Transactions, vol. 4, 2021.
(Refer to the full project documentation for additional references and detailed analysis.)

Contact

For more information or collaboration, please contact:

Namia Modamed Ali
Email: nami29221@gmail.com

