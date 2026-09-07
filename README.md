# Customer Churn Prediction & Retention Analytics

An end-to-end machine learning application that predicts customer churn probability and provides actionable retention recommendations through an interactive Flask web application.

## Live Demo

https://customer-churn-prediction-lj26.onrender.com/

## Project Overview

Customer churn is a major challenge for subscription-based businesses. Identifying customers who are likely to leave allows businesses to take proactive retention actions.

This project uses machine learning to predict whether a customer is likely to churn based on demographic, service, contract, and billing information.

The prediction system provides:

- Churn probability
- Customer risk level
- Prediction outcome
- Retention recommendations
- Interactive web-based dashboard

## Business Problem

The goal is to identify customers who are at a higher risk of churn so that businesses can proactively engage them with appropriate retention strategies.

## Solution

The project evaluates multiple machine learning classification models and selects the best-performing model based on ROC-AUC.

The selected model is integrated into a Flask web application where users can enter customer information and receive an instant churn prediction.

## Machine Learning Approach

### Models Evaluated

- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- XGBoost

### Data Preprocessing

- Removed customer ID
- Converted `TotalCharges` to numeric
- Handled missing values
- Standardized numerical features
- One-hot encoded categorical features
- Used stratified train-test splitting

### Evaluation Metrics

The models are evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

## Application Architecture

```text
Customer Input
      ↓
HTML / CSS / JavaScript
      ↓
Flask Application
      ↓
Saved ML Pipeline
      ↓
Churn Prediction
      ↓
Churn Probability
      ↓
Risk Level & Retention Recommendation