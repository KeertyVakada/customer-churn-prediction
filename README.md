# Customer Churn Prediction & Retention Analytics

An end-to-end machine learning application that predicts customer churn probability and provides actionable retention recommendations through an interactive Flask web application.

## Live Demo

https://customer-churn-prediction-lj26.onrender.com/

## Project Overview

Customer churn is a major challenge for subscription-based businesses. Identifying customers who are likely to leave enables organizations to take proactive retention actions and reduce potential revenue loss.

This project builds an end-to-end customer churn prediction system using machine learning. The application analyzes customer demographic, service, contract, and billing information to estimate the likelihood of churn.

The trained machine learning pipeline is integrated into a Flask web application that provides an interactive interface for generating individual customer predictions.

### Key Features

- Customer churn prediction
- Churn probability score
- Customer risk classification
- Retention recommendations
- Interactive web dashboard
- Production deployment using Flask and Gunicorn
- Publicly accessible live application

---

## Business Problem

Customer retention is an important business objective for subscription-based companies.

The goal of this project is to identify customers who are at a higher risk of churn so that businesses can proactively engage them with appropriate retention strategies.

Instead of waiting for customers to leave, the prediction system helps identify potential churn risk in advance and provides actionable recommendations.

---

## Solution

The project follows an end-to-end machine learning workflow:

1. Load and preprocess customer data
2. Clean numerical and categorical features
3. Build preprocessing pipelines
4. Train multiple classification models
5. Evaluate model performance using multiple metrics
6. Select the best-performing model based on ROC-AUC
7. Save the complete preprocessing and model pipeline
8. Integrate the trained pipeline with a Flask application
9. Generate real-time customer churn predictions
10. Provide churn probability, risk level, and retention recommendations

---

## Machine Learning Approach

### Models Evaluated

The following classification models were evaluated:

- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- XGBoost

### Data Preprocessing

The preprocessing pipeline includes:

- Removed `customerID`
- Converted `TotalCharges` to numeric
- Handled missing values using imputation
- Standardized numerical features
- One-hot encoded categorical features
- Used stratified train-test splitting
- Used `handle_unknown="ignore"` for categorical features

### Evaluation Metrics

Model performance is evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

The best-performing pipeline is selected based on ROC-AUC and saved as `model.pkl`.

---

## Project Structure

```text
customer-churn-prediction/
│
├── app.py
├── train_model.py
├── model.pkl
├── requirements.txt
├── README.md
├── .gitignore
│
├── WA_Fn-UseC_-Telco-Customer-Churn.csv
│
├── templates/
│   ├── index.html
│   └── result.html
│
├── static/
│   ├── css/
│   │   └── style.css
│   │
│   └── js/
│       └── script.js
│
└── screenshots/
    ├── dashboard.png
    └── prediction.png