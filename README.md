# Bank Customer Churn Analytics

Predicting customer churn for a retail bank using classification models, with a focus on identifying the key drivers behind customer exit.

## Overview

This was a team project (3 members) completed as part of my M.S. Business Analytics coursework at ASU's W.P. Carey School of Business. My focus within the project was data cleaning, exploratory analysis, and model evaluation.

**Dataset:** [Bank Customer Churn](https://www.kaggle.com/datasets/radheshyamkollipara/bank-customer-churn) (Kaggle) — 10,000 customer records.

## Approach

1. **Data cleaning** — dropped non-predictive identifier columns, encoded categorical features (Gender, Card Type)
2. **EDA** — correlation analysis, class distribution, outlier checks via boxplots, age distribution
3. **Model selection** — used LazyPredict to screen candidate models before deeper tuning
4. **Modeling** — tuned and evaluated three classifiers via grid search with cross-validation:
   - AdaBoost
   - K-Nearest Neighbors
   - Random Forest
5. **Evaluation** — held out 15% of the data (stratified by class) to test final model performance

## Results

| Model | Accuracy | AUC | F1 |
|---|---|---|---|
| **Random Forest** | **85.3%** | 82.4% | 52.5% |
| AdaBoost | 83.1% | 82.5% | 49.3% |
| KNN | 69.9% | 51.5% | 21.6% |

Random Forest and AdaBoost performed comparably well; KNN performed close to random guessing (AUC ≈ 0.51).

**Key finding:** Age was the most important predictor of churn — older customers were significantly more likely to exit.

## Tools

Python, pandas, scikit-learn, LazyPredict, seaborn, plotly

## Note

This repository contains my individual code contribution to a group project. Team member names have been omitted from this repo for privacy.
