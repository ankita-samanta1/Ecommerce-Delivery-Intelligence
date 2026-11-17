# E-Commerce Delivery Intelligence & Predictive Risk Analysis

## Project Overview

This project analyzes e-commerce delivery performance using SQL, Python, Machine Learning, and Power BI.

The objective is to understand delivery delays, identify operational patterns, evaluate machine learning models for late-delivery prediction, and analyze predicted delivery risks at the order level.

The project uses historical Brazilian e-commerce data from the Olist dataset (2016–2018).

## Business Objectives

- Analyze overall delivery performance.
- Identify late-delivery patterns across customer states and product categories.
- Understand customer review trends and negative feedback.
- Evaluate machine learning models for predicting late deliveries.
- Segment orders into predicted delivery-risk categories.
- Provide order-level risk insights to support business analysis.

## Tools & Technologies

- **SQL Server & SSMS:** Data storage, transformation, and analytical views.
- **Python:** Data cleaning, feature engineering, and machine learning.
- **Pandas & NumPy:** Data processing.
- **Scikit-learn:** Model evaluation and machine learning workflows.
- **XGBoost & LightGBM:** Predictive modelling.
- **Power BI:** Interactive dashboards and business intelligence.
- **DAX:** Measures and calculated columns.

## Machine Learning Models

Four classification models were evaluated:

1. Logistic Regression
2. Random Forest
3. XGBoost
4. LightGBM

### Model Evaluation Results

| Model | Accuracy | Precision | Recall | F1 Score | PR-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 82.84% | 6.15% | 27.45% | 10.05% | 0.0718 |
| Random Forest | 94.25% | 7.10% | 5.34% | 6.10% | 0.0722 |
| XGBoost | 96.36% | 19.57% | 1.34% | 2.50% | 0.1037 |
| LightGBM | 95.58% | 14.90% | 5.64% | 8.18% | 0.1019 |

**Important observation:** XGBoost achieved the highest PR-AUC, while Logistic Regression achieved the highest recall at the evaluated classification thresholds. No single model performed best across all evaluation metrics.

## Power BI Dashboard Pages

### 1. Executive Overview
- Delivery performance KPIs
- Delivery status distribution
- Monthly order trends
- Product category analysis
- State-wise delivery insights
- Monthly payment trends

### 2. Delivery Operations
- Payment method distribution
- Delivery status analysis
- Late orders by customer state
- Late delivery rate by state
- Order processing time by stage

### 3. Customer Experience
- Customer review KPIs
- Average review score by product category
- Negative review rate by category
- Customer type distribution
- Product category review summary

### 4. Predictive Model Evaluation
- Model accuracy, precision, recall, F1-score, and PR-AUC
- Model-wise error analysis
- Late-order detection versus missed orders
- Model performance trade-off analysis

### 5. Order-Level Risk Intelligence
- Predicted delivery-risk distribution
- Monthly predicted late-risk trend
- Actual late delivery rate by predicted risk category
- Actual delivery outcomes by predicted risk category
- High-risk order priority list

## Key Dataset & Evaluation Details

- Dataset: Brazilian Olist E-Commerce Dataset
- Historical period: 2016–2018
- Test dataset: 19,294 orders
- Actual late orders in test dataset: 674
- Actual late delivery rate in test dataset: 3.49%

## Risk Segmentation

Orders were grouped into three predicted risk categories using XGBoost late-risk probabilities:

- **High Risk:** Probability ≥ 50%
- **Medium Risk:** Probability ≥ 20% and below 50%
- **Low Risk:** Probability below 20%

These categories are exploratory segmentation thresholds and should not be interpreted as validated operational decision thresholds.

## Project Outcome

This project combines SQL-based analytics, Python-based machine learning, model evaluation, and interactive Power BI reporting to develop an end-to-end e-commerce delivery intelligence solution.

The analysis highlights delivery performance patterns, customer experience trends, model trade-offs, and order-level predicted risk.

---

**Project Category:** Data Analytics | Machine Learning | Business Intelligence

**Dataset:** Olist Brazilian E-Commerce Dataset
