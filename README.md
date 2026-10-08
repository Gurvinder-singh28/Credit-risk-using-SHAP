💳 Credit Risk Prediction using XGBoost & SHAP

An end-to-end Explainable Machine Learning application that predicts credit default risk using XGBoost and explains model predictions using SHAP (SHapley Additive exPlanations).

The project goes beyond simply predicting loan risk by providing an interpretable ML workflow and a deployed FastAPI REST API for real-time predictions.

🚀 Live Demo

👉 "Try the Live Application" (https://credit-risk-using-shap-c6ru.onrender.com/)

📂 GitHub Repository

👉 "View Source Code" (https://github.com/Gurvinder-singh28/Credit-risk-using-SHAP)

---

📌 Project Overview

Credit-risk assessment is an important Machine Learning application in financial services.

This project uses applicant and loan-related information to estimate the probability of loan default and classify applicants into:

- 🟢 Low Risk
- 🔴 High Risk

A major focus of this project is Explainable AI. Instead of treating the ML model as a black box, SHAP is used to understand which features influence predictions.

The training dataset contains 32,581 records and includes demographic, employment, loan and credit-history features.

---

✨ Key Features

🤖 Machine Learning Prediction

- XGBoost classification model
- Predicts probability of loan default
- Converts probability into a risk classification
- Uses a saved classification threshold during inference

🔍 Explainable AI with SHAP

- SHAP TreeExplainer for the XGBoost model
- Global feature importance analysis
- Local prediction interpretation
- Helps understand how individual features influence model decisions

📊 Data Analysis

- Exploratory Data Analysis
- Missing-value analysis
- Numerical and categorical feature analysis
- Data preprocessing
- Model evaluation using classification metrics

⚙️ Production API

- FastAPI backend
- REST API prediction endpoint
- Pydantic data validation
- Serialized ML model using Joblib
- Real-time prediction response

☁️ Deployment

- Deployed application on Render
- Production-style API architecture
- Static frontend connected to FastAPI backend

---

🧠 Machine Learning Workflow

Raw Credit Dataset
        ↓
Data Cleaning & EDA
        ↓
Feature Preprocessing
        ↓
Train/Test Split
        ↓
Model Training
        ↓
XGBoost Classifier
        ↓
Model Evaluation
        ↓
Threshold Selection
        ↓
SHAP Explainability
        ↓
Model Serialization
        ↓
FastAPI REST API
        ↓
Cloud Deployment

---

📋 Input Features

The application accepts the following applicant and loan information:

Feature| Description
"person_age"| Applicant age
"person_income"| Applicant income
"person_home_ownership"| Home ownership status
"person_emp_length"| Employment length
"loan_intent"| Purpose of the loan
"loan_grade"| Loan grade
"loan_amnt"| Loan amount
"loan_int_rate"| Loan interest rate
"loan_percent_income"| Loan amount relative to income
"cb_person_default_on_file"| Previous default indicator
"cb_person_cred_hist_length"| Credit history length

The FastAPI application validates these fields using a Pydantic model before sending the data to the ML pipeline.

---

🔮 Prediction Output

The API returns:

{
  "default_probability": 0.XX,
  "default_prediction": 0,
  "threshold": 0.XX,
  "Result": "Low Risk"
}

Possible result:

Low Risk

or

High Risk

---

🔍 Explainable AI with SHAP

One of the main components of this project is SHAP-based model interpretation.

The project uses:

shap.TreeExplainer()

to calculate SHAP values for the trained XGBoost classifier.

This enables analysis at two levels:

Global Explainability

Identifies which features have the greatest overall influence on the model's predictions.

Local Explainability

Explains why the model produced a particular prediction for an individual applicant.

This makes the project more suitable for scenarios where understanding model decisions is important.

---

🛠️ Tech Stack

Programming

- Python

Data Science

- Pandas
- NumPy
- Matplotlib
- Seaborn

Machine Learning

- Scikit-learn
- XGBoost
- Joblib

Explainable AI

- SHAP

Backend

- FastAPI
- Pydantic

Deployment

- Render

---

📁 Project Structure

Credit-risk-using-SHAP/
│
├── static/
│   └── Frontend files
│
├── credit_risk.ipynb
├── credit_risk_dataset.csv
├── credit_risk_model.pkl
├── best_threshold.pkl
├── main.py
├── requirements.txt
├── render.yaml
├── runtime.txt
└── README.md

---

⚡ Running Locally

1. Clone the repository

git clone https://github.com/Gurvinder-singh28/Credit-risk-using-SHAP.git

2. Navigate to the project

cd Credit-risk-using-SHAP

3. Create a virtual environment

python -m venv venv

4. Activate the environment

Windows:

venv\Scripts\activate

Linux/macOS:

source venv/bin/activate

5. Install dependencies

pip install -r requirements.txt

6. Start the FastAPI application

uvicorn main:app --reload

The application will be available at:

http://127.0.0.1:8000

---

🔌 API Endpoint

Prediction

POST /predict

Example request:

{
  "person_age": 25,
  "person_income": 60000,
  "person_home_ownership": "RENT",
  "person_emp_length": 4,
  "loan_intent": "PERSONAL",
  "loan_grade": "B",
  "loan_amnt": 10000,
  "loan_int_rate": 12.5,
  "loan_percent_income": 0.17,
  "cb_person_default_on_file": "N",
  "cb_person_cred_hist_length": 5
}

---

💼 Why This Project is Resume-Worthy

This project demonstrates practical experience with:

- End-to-end Machine Learning development
- XGBoost classification
- Explainable AI and SHAP
- Model evaluation
- Probability-based prediction
- Classification threshold optimization
- Feature preprocessing
- REST API development
- Pydantic validation
- Model serialization
- Cloud deployment
- Production-oriented ML architecture

Rather than stopping at a Jupyter Notebook, the project converts the trained ML model into an accessible deployed application.

---

🎯 Future Improvements

Potential improvements include:

- Add interactive SHAP explanations directly to the web application
- Add probability visualizations
- Add model monitoring
- Add automated retraining pipeline
- Add Docker support
- Add CI/CD with GitHub Actions
- Add authentication and API security
- Add more advanced fairness and bias analysis

---

👨‍💻 Author

Gurvinder Singh

AI/ML Engineer | Generative AI | Agentic AI | Data Analytics

🔗 GitHub:
https://github.com/Gurvinder-singh28

---

⭐ If you find this project useful, consider giving the repository a star!
