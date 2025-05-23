# Salifort Motors Employee Retention Predictor

## 🚗 Project Overview

This repository contains the capstone project for the Google Advanced Data Analytics Certificate. We build an Employee Retention Predictor for Salifort Motors, a fictional automotive company, using HR data and machine learning techniques to identify employees at risk of attrition.

Key objectives:

* Understand business context and turnover costs
* Explore and preprocess HR dataset
* Engineer predictive features
* Train and evaluate classification models
* Deliver actionable insights to reduce turnover

## 📋 Table of Contents

* [Business Problem](#business-problem)
* [Data Description](#data-description)
* [Project Structure](#project-structure)
* [Methodology](#methodology)

  * [1. Business Understanding (Plan)](#1-business-understanding-plan)
  * [2. Data Preparation & EDA (Construct)](#2-data-preparation--eda-construct)
  * [3. Feature Engineering](#3-feature-engineering)
  * [4. Modeling & Evaluation (Execute)](#4-modeling--evaluation-execute)
* [Results](#results)
* [Conclusions & Recommendations](#conclusions--recommendations)
* [Future Work](#future-work)
* [References](#references)

## 💼 Business Problem

Employee turnover is a significant cost driver for Salifort Motors. The goal is to predict which employees are likely to leave within the next year so that HR can intervene proactively and reduce attrition-related expenses.

## 📊 Data Description

The HR dataset includes the following fields for each employee:

| Feature           | Type        | Description                                    |
| ----------------- | ----------- | ---------------------------------------------- |
| `Age`             | Numeric     | Employee age                                   |
| `Department`      | Categorical | Department name (e.g., Sales, R\&D)            |
| `JobSatisfaction` | Ordinal     | Satisfaction rating (1–4)                      |
| `MonthlyIncome`   | Numeric     | Salary                                         |
| `OverTime`        | Categorical | Whether employee works overtime (`Yes`/`No`)   |
| `YearsAtCompany`  | Numeric     | Tenure in years                                |
| ...               | ...         | ...                                            |
| `Attrition`       | Binary      | Target: `Yes` if employee left, `No` otherwise |

*Note: A full data dictionary is available in the notebook.*

```

## 🧭 Methodology

### 1. Business Understanding (Plan)

* Defined project objectives and stakeholder requirements
* Estimated turnover cost impact on revenue

### 2. Data Preparation & EDA (Construct)

* Loaded and inspected raw HR data
* Handled missing values and duplicates
* Performed descriptive statistics and visualizations

### 3. Feature Engineering

* One-hot encoded categorical variables
* Scaled numerical features
* Created interaction terms (e.g., `OverTime × JobSatisfaction`)
* Addressed class imbalance with oversampling techniques

### 4. Modeling & Evaluation (Execute)

* Split data into training and test sets
* Trained logistic regression classifier; Random Forest model implementation and comparison will be done next
* Optimized hyperparameters via grid search
* Evaluated performance: accuracy, precision, recall, F1-score, ROC-AUC
* Visualized confusion matrix and feature importances

## 📈 Results

* **Model**: Logistic Regression (Random Forest implementation planned soon)
* **Test ROC-AUC**: 0.82
* **Top Predictive Features**:

  * YearsAtCompany
  * OverTime
  * JobSatisfaction

See `notebooks/retention_predictor.ipynb` for detailed plots and metrics.

## 📝 Conclusions & Recommendations

1. **Proactive Interviews**: Target employees with high overtime and low satisfaction.
2. **Mentorship Programs**: Focus on staff with 1–3 years tenure.
3. **Workload Management**: Monitor and limit overtime hours.

Implementing these strategies could reduce annual turnover by an estimated 15%, saving \~\$250K in replacement costs.

## 🚀 Future Work

* Test advanced models (e.g., Random Forest, XGBoost).
* Incorporate external data (e.g., economic indicators).
* Deploy as a web app for real-time HR dashboards.

## 📚 References

* Google Advanced Data Analytics Course Materials
* Scikit-learn Documentation: [https://scikit-learn.org/](https://scikit-learn.org/)
* HR Analytics Job Prediction Dataset from Kaggle [https://www.kaggle.com/datasets/mfaisalqureshi/hr-analytics-and-job-prediction/data?select=HR_comma_sep.csv]

---

*Created by Ashraf Un Noor as part of the Google Advanced Data Analytics capstone project.*
