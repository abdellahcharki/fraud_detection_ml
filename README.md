# Fraud Detection Project – Probabilistic Machine Learning

This repository contains a **probabilistic machine learning project** for detecting fraudulent transactions using Bayesian and frequentist approaches.

---

## 🚀 Project Goal

Fraud detection is a classic case of **imbalanced classification**. Our goal:

✅ Predict whether a transaction is fraudulent  
✅ Compare different probabilistic models  
✅ Quantify uncertainty and interpret model coefficients

We explore:
- Logistic Regression (Frequentist)
- Naive Bayes
- Bayesian Logistic Regression (PyMC)
- Model comparison and uncertainty evaluation

---

## 📂 Folder Structure

root/
│
├── data/
│    ├── Fraud.csv
│    └── processed_fraud.csv
│
├── notebooks/
│    ├── 01_Data_Exploration_Preprocessing.ipynb
│    ├── 02_Frequentist_Logistic_Regression.ipynb
│    ├── 03_Naive_Bayes_Classification.ipynb
│    ├── 04_Logistic_Regression_Bayesian.ipynb
│    └── 05_Final_Model_Comparison.ipynb
│
├── README.md
└── requirements.txt


## 🗂️ Dataset

We use a synthetic fraud detection dataset:

- File: `data/Fraud.csv`
- Features include:
  - Transaction type
  - Amount
  - Origin and destination balance changes
- Target:
  - `isFraud` = 1 → fraudulent
  - `isFraud` = 0 → normal transaction
- Highly imbalanced → very few fraudulent transactions

---


### 02_Frequentist_Logistic_Regression.ipynb

- Tests different penalties:
  - L1
  - L2
  - Elastic Net
- Uses class-weight balancing
- Plots ROC & Precision-Recall curves
- Prints metrics for easy comparison

---

### 03_Naive_Bayes_Classification.ipynb

- Fits a Gaussian Naive Bayes model
- Prints metrics:
  - ROC AUC
  - Precision / Recall
- Plots ROC and PR curves

---

### 04_Logistic_Regression_Bayesian.ipynb

- Implements Bayesian logistic regression in PyMC
- Samples posterior distributions of:
  - Intercept
  - Coefficients
- Visualizes uncertainty using trace plots and summaries

---

### 05_Final_Model_Comparison.ipynb

- Compares:
  - Frequentist logistic regression
  - Naive Bayes
  - Bayesian logistic regression
- Prints ROC AUC and classification reports
- Plots curves for all models side by side

---


## 🤝 Credits

- Developed for the course **Probabilistic Machine Learning** (SoSe 2025)
- Dataset inspired by fraud detection problem settings