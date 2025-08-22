# Telecom Customer Churn Prediction

## Project Overview
This project, completed as part of the **Estarta Internship**, focuses on predicting **customer churn** for a telecom company using machine learning.  
The goal is to help telecom providers identify customers at risk of leaving and improve service retention.

## Dataset
The dataset is publicly available from the **CrowdAnalytix Community** churn prediction competition.  
It contains **3,333 customer records** with 20 features, including usage patterns, service plans, and customer support interactions.  
The target variable is **`Churn`**.

## Data Quality and Preparation
- Checked for **missing values** and **duplicates**.  
- Retained outliers in numerical features (valid customer behavior).  
- Analyzed **correlation** among numerical features to reduce redundancy.  
- Encoded categorical features (`International plan`, `Voice mail plan`).  
- Converted target variable `Churn` to numeric.  
- Split data into **training (80%)** and **testing (20%)** sets.  
- Applied **target encoding** on `State` after splitting to avoid data leakage.  
- Standardized numerical features using **scaling**.  
- Applied **SMOTE oversampling** on the training set to balance churn vs. non-churn classes.  

## Feature Analysis
- Performed **Chi-square test** for categorical features (e.g., `State`).  
- Calculated **information gain** for numerical features.  
- Evaluated **feature importance** using **XGBoost**.  

## Modeling
Three models were trained and evaluated:  
1. **Logistic Regression**  
2. **Decision Tree**  
3. **XGBoost**  

Model performance was assessed using:  
- Confusion matrix  
- Precision, Recall, F1-score  
- ROC-AUC  

## Key Findings
- **XGBoost** achieved the highest performance:  
  - Accuracy: **93.40%**  
  - ROC-AUC: **0.9109**  
- Most important features:  
  - Customer service calls  
  - Total day charge  
  - Service plan indicators  

## Files in the Repository
- **`churn_prediction.ipynb`** – Jupyter Notebook with preprocessing, feature analysis, modeling, and results.  
- **`Customer Churn Prediction in the Telecom Industry - Report.pdf`** – Project report summarizing methodology, findings, and conclusions.  
