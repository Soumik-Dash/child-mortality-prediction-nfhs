# child-mortality-prediction-nfhs
# Predicting Child Mortality in India: A Study Based on NFHS Data

This repository contains the complete implementation of a machine learning project that predicts child mortality outcomes using socio-demographic and health-related data from the **National Family Health Survey (NFHS)**. The project applies a range of classification models and interprets the results using explainable AI techniques.

---

## 🎯 Objective

The goal of this project is to classify whether a child will survive or not based on variables such as:
- Maternal age
- Total children ever born
- Birth order
- Education level
- Wealth index
- Place of residence
- Religion, caste, and contraceptive method
- Marital status, and more

This analysis aims to inform policy and healthcare interventions by identifying key determinants of child mortality in India.

---

## 📊 Dataset

- **Source**: [National Family Health Survey (NFHS)](https://dhsprogram.com)
- **Description**: A nationally representative survey collecting population, health, and nutrition indicators in India.
- **Target Variable**: Binary classification — `1` for death, `0` for alive.

> ⚠️ Note: Due to data privacy policies, raw data is not uploaded. Only a cleaned and anonymized version is used for modeling.

---

## 🧪 Methodology

- **Data Preprocessing**
  - Missing value imputation
  - Label Encoding (ordinal features) and One-Hot Encoding (nominal features)
  - Feature scaling using Standardization
  - SMOTE for handling class imbalance

- **Models Implemented**
  - Logistic Regression
  - K-Nearest Neighbors (KNN)
  - Support Vector Machine (SVM)
  - Random Forest Classifier
  - Gradient Boosting Classifier
  - XGBoost Classifier

- **Evaluation Metrics**
  - Accuracy
  - Precision
  - Recall
  - F1 Score
  - ROC-AUC
  - Confusion Matrix

- **Model Interpretation**
  - Feature Importance from Tree Models
  - SHAP (SHapley Additive Explanations) for local and global interpretability

---

## 📈 Results

| Model              | Accuracy | ROC-AUC | F1 Score |
|-------------------|----------|---------|----------|
| Logistic Regression | 67.38%   | 69.03%  | Moderate |
| KNN                | 82.61%   | 61.68%  | Low      |
| SVM                | 67.54%   | 69.36%  | Moderate |
| Random Forest      | 91.22%   | 72.82%  | High     |
| Gradient Boosting  | 83.18%   | 76.15%  | Good     |
| **XGBoost**        | **92.93%** | **75.75%** | **Best**   |

### 🔍 Top Features (from XGBoost + SHAP)
- `total_children_ever_born`
- `mother_age`
- `birth_order`
- `preceding_birth_interval`
- `education_level`
- `wealth_index`
- `place_of_residence`
- `caste`

---
