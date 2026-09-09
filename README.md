# 🏦 Loan Default Prediction System

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/pandas-data%20analysis-orange.svg)](https://pandas.pydata.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-machine%20learning-yellow.svg)](https://scikit-learn.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

An industry-grade machine learning project aimed at assessing and predicting borrower credit risk (`loan_status`). By analyzing comprehensive demographic details, employment history, credit scores, and financial metrics, this project builds robust predictive models to automate lending decisions and mitigate financial default risks.

---

## 📊 Dataset Overview

The dataset (`14.csv`) comprises **45,000 records** and **14 features** detailing applicant profiles and loan characteristics:

* **Target Variable:** 
  * `loan_status`: Binary classification target (`0` = Non-default / Fully Paid, `1` = Default).
* **Numerical Features (9):**
  * `person_age`, `person_income`, `person_emp_exp`, `loan_amnt`, `loan_int_rate`, `loan_percent_income`, `cb_person_cred_hist_length`, `credit_score`, `loan_status`.
* **Categorical Features (5):**
  * `person_gender`, `person_education`, `person_home_ownership`, `loan_intent`, `previous_loan_defaults_on_file`.

### **Class Distribution Analysis:**
* **Non-Defaults (`0`):** 35,000 records (~77.78%)
* **Defaults (`1`):** 10,000 records (~22.22%)
* *Note:* The dataset exhibits class imbalance, requiring appropriate handling (e.g., class weighting, SMOTE, or evaluation using Precision, Recall, and ROC-AUC).

---

## 🗂️ Repository Directory Structure

```text
loan-default-prediction-ml/
│
├── data/
│   └── 14.csv                    # Cleaned dataset used for training & analysis
│
├── notebooks/
│   └── loan_default_analysis.ipynb # Interactive Jupyter Notebook with end-to-end workflow
│
├── reports/
│   └── project_report.pdf        # Detailed documentation and analytical report
│
├── src/                          # Modular source code (optional scripts)
│   ├── data_preprocessing.py
│   └── train_model.py
│
├── .gitignore                    # Files to ignore (e.g., venv, checkpoints)
├── LICENSE                       # MIT License
└── README.md                     # Project documentation

🛠️ Key Workflow & Methodology
Exploratory Data Analysis (EDA):

Inspected data types, missing values, and statistical summaries using pandas.

Evaluated feature distributions and correlation matrices.

Visualized class distribution imbalances using matplotlib and seaborn.

Data Preprocessing & Feature Engineering:

Handled categorical encoding (One-Hot / Label Encoding).

Feature scaling for numerical variables.

Addressed class imbalance for reliable model training.

Model Training & Evaluation:

Trained baseline and advanced classification models (Logistic Regression, Random Forest, Gradient Boosting).

Evaluated performance using metrics suited for imbalanced data (Precision, Recall, F1-Score, and ROC-AUC).

🚀 Getting Started & Installation
1. Clone the Repository
Bash
git clone [https://github.com/your-username/loan-default-prediction-ml.git](https://github.com/your-username/loan-default-prediction-ml.git)
cd loan-default-prediction-ml
2. Create a Virtual Environment
Bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
3. Install Dependencies
Bash
pip install -r requirements.txt
⚙️ Usage
Jupyter Notebook: Launch Jupyter to explore the step-by-step pipeline:

Bash
jupyter notebook notebooks/loan_default_analysis.ipynb
Google Colab: Alternatively, upload 14.csv and the .ipynb notebook to Google Colab and execute cells sequentially after mounting Google Drive.
