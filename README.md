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

```plaintext
fraud-detection-project/
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
```

## 🗂️ Dataset

We use a synthetic fraud detection dataset:
⚠️ **Important:** The original fraud detection dataset used in this project is large and not included in this repository to keep the repo size manageable.

Download the dataset file:

    - File name: `Fraud.csv`
    - [🔗 Download Link](https://your-download-link-here.com/Fraud.csv)

Each row in the dataset represents a single transaction, with the following columns:

- **step** → Represents a unit of time where **1 step = 1 hour**
- **type** → Type of online transaction (e.g. TRANSFER, CASH_OUT)
- **amount** → The amount of the transaction
- **nameOrig** → Customer initiating the transaction
- **oldbalanceOrg** → Customer's balance before the transaction
- **newbalanceOrig** → Customer's balance after the transaction
- **nameDest** → Recipient of the transaction
- **oldbalanceDest** → Initial balance of the recipient before the transaction
- **newbalanceDest** → New balance of the recipient after the transaction
- **isFraud** → Target variable:
    - `1` → Fraudulent transaction
    - `0` → Legitimate transaction

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