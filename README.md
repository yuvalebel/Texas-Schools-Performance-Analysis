# 🎓 Texas Schools Performance Analysis

**Final Project | Advanced Topics in Machine Learning & Data Mining**  
*Ariel University*

---

##  AI Acknowledgment

> **Note:** This project, including all code logic, data processing pipelines, and documentation, was developed and co-authored with the assistance of **Google Gemini AI**.  
> We utilized AI as a specialized research and coding partner to optimize model performance, handle complex data cleaning, and structure our analysis.

---

##  Project Overview

This repository contains the **final project** for the *Advanced Topics in Machine Learning & Data Mining* course at **Ariel University**.

The research focuses on predicting and analyzing **school accountability ratings (A–F)** in **Texas**, using a comprehensive **multi-source educational and socio-economic dataset**.

Our primary objective was to move beyond simple classification and develop a **diagnostic framework** capable of identifying schools that are **underperforming relative to their available socio-economic resources**. This approach aims to generate **actionable insights** for educational policy and school-level management.

---

##  Machine Learning Pipeline

### 1️. Classification (Supervised Learning)

We conducted a comparative study of **six machine learning models** to identify the most robust predictor of school accountability ratings:

- **Logistic Regression** *(Baseline)*
- **Decision Tree**
- **Random Forest**  *(Best Performing Model)*
- **Support Vector Machine (SVM)**
- **k-Nearest Neighbors (k-NN)**
- **XGBoost** *(Advanced Gradient Boosting)*

**Model Optimization & Evaluation:**
- Hyperparameter tuning using **GridSearchCV**
- Evaluation metrics:
  - **F1-Weighted** – to address class imbalance
  - **Mean Absolute Error (MAE)** – to reflect the *ordinal* nature of A–F school ratings

---

### 2️. Unsupervised Learning & Diagnostics

To complement the supervised models, we applied unsupervised techniques for deeper diagnostic insights:

#### 🔹 K-Means Clustering
- Schools were segmented into **three distinct socio-economic "Resource Profiles"**
- Key clustering features:
  - % of Gifted Students
  - % of At-Risk Students
  - Social Vulnerability Index (SVI)

#### 🔹 Dimensionality Reduction (PCA)
- **Principal Component Analysis (PCA)** was used to:
  - Visualize cluster separation
  - Examine explained variance

#### 🔹 Anomaly Detection
- Developed a rule-based logic to identify **"Negative Outliers"**:
  - Schools with **high resources (Cluster 1)**
  - Yet receiving **low ratings (D/F)**
- These cases may indicate **localized management or operational issues**, rather than resource constraints

---

##  Repository Structure

```
├── data/
│   └── Master_Dataset.csv          # Original and preprocessed datasets
│
├── notebooks/
│   └── School_ML.ipynb              # Main Jupyter Notebook with full ML pipeline
│
├── figures/
│   ├── feature_importance.png
│   ├── pca_clusters.png
│   └── heatmaps.png                 # Visual analysis outputs
│
├── requirements.txt                 # Environment dependencies
└── README.md                        # Project documentation
```

---

##  Key Findings

- **Feature Importance:**
  - The percentage of **Gifted Students** and the **Social Vulnerability Index (SVI)** emerged as stronger predictors of school success than direct financial metrics.

- **Educational Resilience:**
  - Schools with **high bilingual education investment** frequently *outperformed expectations*, achieving higher ratings despite elevated vulnerability scores.

- **Policy Insight:**
  - Resource availability alone does not guarantee academic success—**how resources are utilized** plays a critical role.

---

##  Authors

- **Yuval Lebel**  
- **Adir Cohen**

---

##  Notes

- This project is intended for **academic and research purposes**.
- All analyses comply with the dataset's public availability and ethical research standards.

.
