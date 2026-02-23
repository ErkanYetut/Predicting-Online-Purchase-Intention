# Predicting-Online-Purchase-Intention

E-commerce has transformed the retail landscape
by providing unparalleled convenience and accessibility. However, low conversion rates remain a persistent challenge, driven
by complex customer behaviors that are difficult to interpret
in digital environments. 

This repository contains the implementation of a machine learning pipeline for predicting whether a user session on an e-commerce website will result in a purchase.

The project conducts a comparative empirical analysis of multiple classification models and focuses on proper preprocessing and evaluation for imbalanced datasets.

📄 Detailed report: [Project Report (PDF)](report/Erkan_Yetut_Online_Purchase_Intention_Report.pdf)

---

## Dataset
The study uses the **Online Shoppers Purchasing Intention Dataset** (UCI Machine Learning Repository).  
The dataset consists of 12,330 user sessions with 18 numerical and categorical features describing user behavior (page visits, session duration, bounce rate, exit rate, visitor type, etc.).

The target variable is a binary label indicating whether the session resulted in a transaction.

---

## Methodology

The modeling pipeline includes:

- Data preprocessing and exploratory analysis
- One-hot encoding for categorical variables
- Robust scaling for numerical features
- Handling class imbalance using **SMOTE**
- Feature selection using **Random Forest importance**
- Train–test split and cross-validation

We compared the following models:

- Logistic Regression
- Random Forest
- Support Vector Machine (RBF kernel)
- Stacking Ensemble
- XGBoost

---

## Evaluation

Since the dataset is highly imbalanced, accuracy was not used as the primary metric.  
Models were evaluated using:

- F1-Score
- Matthews Correlation Coefficient (MCC)
- ROC-AUC
- PR-AUC

---

## Results

XGBoost achieved the best performance:

- F1-Score: 0.8956  
- MCC: 0.5988  
- ROC-AUC: 0.9283  

The results show that **data preprocessing and proper evaluation metrics had a larger impact than the choice of algorithm itself**.

---

## How to Run

1. Clone the repository
2. Install requirements
3. Run the notebook



## Research Report

The full project report describing the methodology, experiments, and results can be accessed here:

[📄 View Project Report](report/Erkan_Yetut_Online_Purchase_Intention_Report.pdf)




## Summary
Predicting online shoppers’ purchase intentions is critical for addressing these challenges and improving conversion rates. This study focuses on the widely used
dataset introduced by Sakar et al., which reflects the imbalanced
nature of purchase intention data. To address this imbalance,
we employed the Synthetic Minority Oversampling Technique
(SMOTE) to enhance model training. Various machine learning
models, including Logistic Regression, Random Forest, Stacking,
and XGBoost, were compared using metrics such as F1-Score,
Matthews Correlation Coefficient (MCC), auROC, and auPR.
Our results demonstrate that XGBoost outperforms other
models, achieving an F1-Score of 0.8956, MCC of 0.5988,
and auROC of 0.9283. The combination of feature selection
and SMOTE significantly improved classification performance,
underscoring the critical role of preprocessing in e-commerce
prediction tasks. By leveraging ensemble methods and advanced
evaluation metrics, this study highlights the potential of machine
learning in building robust predictive models to analyze customer
behavior and improve e-commerce platform performance.
