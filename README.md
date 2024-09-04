# Credit Card Fraud Detection

## Overview
This project focuses on detecting fraudulent credit card transactions using machine learning techniques. The goal is to identify fraudulent transactions and help financial institutions reduce losses, enhance security, and maintain customer trust.

## Objectives
- Analyze credit card transaction data to identify fraudulent transactions.
- Handle data imbalance using techniques like SMOTE.
- Compare various machine learning models for effective fraud detection.
- Build a solution to reduce financial losses and false positives.

## Methodology

### 1. Data Collection and Preparation
- **Dataset**: 1.85 million credit card transactions, with 9651 labeled as fraudulent.
- **Data Cleaning**: Handled missing values, dropped irrelevant columns, and converted timestamps into useful features such as transaction time, day, and month.
- **Imbalance**: Fraud accounts for only 0.52% of the dataset, requiring specialized techniques to balance the dataset during model training.

### 2. Feature Engineering
- Extracted time-based features like hour, day of the week, and week number.
- Created dummy variables for categorical data (e.g., POS locations).
- Applied feature scaling for normalization.

### 3. Handling Imbalanced Data
- **SMOTE (Synthetic Minority Over-sampling Technique)** was applied to balance the classes by generating synthetic fraud cases.
- Under-sampling was used to reduce the number of non-fraud cases.

### 4. Model Building
- Models used:
  - **Logistic Regression**
  - **K-Nearest Neighbors (KNN)**
  - **Decision Tree**
  - **Random Forest**
  - **AdaBoost**
- **Random Forest** and **AdaBoost** models performed the best, especially when handling imbalanced data.

### 5. Model Evaluation
- **GridSearchCV** was used for hyperparameter tuning.
- The **Random Forest** model achieved the best performance with:
  - **Train Accuracy**: 92%
  - **Test Accuracy**: 88%
  - **Recall**: 79%
  - **ROC-AUC**: 0.985

## Results
- The model successfully detected 79% of fraudulent transactions, reducing false negatives.
- Financial losses from fraudulent transactions were reduced by **$395,946** per month after deploying the model.

## Challenges and Limitations
- Dealing with the highly imbalanced dataset required advanced resampling techniques.
- Computationally expensive models like KNN were not feasible due to the large dataset size.
- The model's performance may be limited when generalizing to new, unseen fraud patterns beyond the training data.

## Future Work
- Improve the model by incorporating additional features and real-time transaction data for better fraud detection.
- Explore more advanced techniques such as **XGBoost** and **deep learning models** to capture more complex fraud patterns.
- Implement anomaly detection methods for continuous learning from new data.

## Technologies Used
- **Python**
- **Pandas**, **NumPy** for data manipulation
- **Matplotlib**, **Seaborn** for data visualization
- **Scikit-learn** for machine learning models and evaluation metrics
- **Imbalanced-learn** (SMOTE) for handling data imbalance

## Installation and Setup
To run this project locally, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/username/credit-card-fraud-detection.git
