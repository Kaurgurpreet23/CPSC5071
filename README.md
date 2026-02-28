# Predicting Employee Attrition

## Overview

This project analyzes employee attrition by integrating traditional HR factors with remote productivity metrics. The objective is to evaluate whether productivity-related variables add predictive value beyond workplace factors.

---

## Datasets

### Employee Attrition Dataset (Kaggle)

Source: [Employee Attrition and Factors – Kaggle](https://www.kaggle.com/datasets/thedevastator/employee-attrition-and-factors)

Includes HR variables such as:
- Attrition (target variable)
- MonthlyIncome
- JobSatisfaction
- WorkLifeBalance
- OverTime
- YearsAtCompany
- JobLevel


### Remote Worker Productivity Dataset (Kaggle)

Source: [Remote Worker Productivity Dataset – Kaggle](https://www.kaggle.com/datasets/ziya07/remote-worker-productivity-dataset)

Includes:
- productivity_score
- average_daily_work_hours
- task_completion_rate
- late_task_ratio
- focus_time_minutes
- experience_years
---

## Data Integration

The two datasets do not share a common employee identifier.

Productivity metrics were aggregated by `experience_years` and merged with the attrition dataset using:

`TotalWorkingYears ↔ experience_years`

A LEFT JOIN was applied to retain all employee records.

---

## Key Findings

- Overtime, JobSatisfaction, MonthlyIncome, JobLevel, and YearsAtCompany show strong relationships with attrition.
- Productivity metrics show weaker direct correlation but may contribute in predictive modeling.
- The dataset is imbalanced, with more employees staying than leaving.

---

## Modeling

- Logistic Regression (baseline model)
- Random Forest (comparison model)

Evaluation metrics:
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

---

## Tools

- Python
- Pandas
- Scikit-learn
- Seaborn
- SQLite

---

## Authors

**Badamgarav Battushig**  
**Gurpreet Kaur**
