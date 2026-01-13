# SECB3203 25261 — Programming for Bioinformatics  
## Diabetes Risk Prediction using Machine Learning (Classification)

**Course:** SECB3203 Programming for Bioinformatics  
**Semester:** 2025/2026  
**Project Type:** Supervised Machine Learning (Binary Classification)

### Group Members
- **IRDINA SOFIA BINTI ROHAIDI - A24CS0253**
- **RAJA NUR ALLEA DEWI MAHSURI BINTI RAJA MOHD YUSRI - A24CS0294**  
- **NURZULAIKHA BINTI MOHD ISA - A24CS0291**  
---

## Overview
Diabetes is a major global health issue that can lead to severe complications such as cardiovascular disease, kidney failure, nerve damage, and vision impairment.  
This project applies supervised machine learning models to predict **diabetes risk** using health indicator data.

**Goal:** Predict whether an individual is **Low Risk (0)** or **High Risk (1)** for diabetes.

---

## Dataset
- **Source:** Diabetes Health Indicators Dataset (Kaggle)
- **Records:** 70,692 (5050 split)
- **Target Variable:** `Diabetes_binary`  
  - `0` = Low risk / No diabetes  
  - `1` = High risk / Diabetes  

> Note: Dataset is based on health indicators, not lab glucose tests.

---

## Features Used
The project uses selected health indicators such as:
- BMI
- High Blood Pressure (HighBP)
- High Cholesterol (HighChol)
- General Health (GenHlth)
- Physical Health (PhysHlth)
- Mental Health (MentHlth)
- Physical Activity (PhysActivity)
- Age
- Difficulty Walking (DiffWalk)

---

## Methods & Workflow
### 1) Data Preprocessing
- Load dataset
- Select relevant features
- Check missing values
- (Optional) BMI outlier handling

### 2) Exploratory Data Analysis (EDA)
- Descriptive statistics
- Correlation analysis (Pearson)
- ANOVA test for feature significance
- Visualization: correlation heatmap

### 3) Model Development
**Baseline Model**
- Decision Tree

**Improved Model**
- Gradient Boosting (ensemble boosting)

**Other comparison models**
- Logistic Regression (L2 / Ridge regularization)
- Random Forest
- AdaBoost

### 4) Model Evaluation
- Metrics: Accuracy, Precision, Recall, F1-score, ROC-AUC
- Confusion Matrix for each model
- ROC Curve comparison

### 5) Testing & Validation (Progress 5)
- Overfitting vs underfitting (train vs test comparison)
- Ridge concept: L2 regularization in Logistic Regression
- Grid Search (hyperparameter tuning)
- Model refinement (final tuned model evaluation)

---

## Results Summary (Test Set)
The results were sorted by **F1-score** (higher is better).

| Model | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|------|---------:|----------:|-------:|---------:|--------:|
| **Gradient Boosting** | 0.7542 | 0.7336 | 0.7983 | **0.7646** | **0.8297** |
| Logistic Regression (L2) | 0.7473 | 0.7381 | 0.7666 | 0.7521 | 0.8250 |
| AdaBoost | 0.7448 | 0.7346 | 0.7666 | 0.7502 | 0.8223 |
| Random Forest | 0.7349 | 0.7183 | 0.7728 | 0.7446 | 0.8120 |
| Decision Tree (Baseline) | 0.6500 | 0.6525 | 0.6417 | 0.6470 | 0.6503 |

**Best model:** Gradient Boosting  
Reason: Highest F1-score and ROC-AUC, with strong recall (better at detecting high-risk individuals).


