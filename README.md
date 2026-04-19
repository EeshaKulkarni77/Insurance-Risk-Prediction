# Insurance Risk Prediction and Policy Recommendation System

## Overview

This project is an end-to-end machine learning system designed to predict the likelihood of insurance claims and generate interpretable policy recommendations.

It combines:
- Machine learning for risk prediction  
- Explainable AI (XAI) for transparency  
- Large Language Models (LLMs) for natural language explanations  

The goal is to move beyond raw predictions and build a system that supports real-world decision-making.

---

## Problem Statement

Insurance companies rely on accurate risk assessment to determine policy pricing and coverage. Traditional approaches often fail to capture complex relationships in structured data.

This project addresses that by:
- Predicting claim probability using machine learning  
- Translating predictions into risk tiers  
- Mapping risk tiers to policy recommendations  
- Providing clear, human-readable explanations of decisions  

---

## System Architecture

The system follows a structured pipeline:

User Input
- Data Preprocessing
- ML Model (Risk Prediction)
- Risk Probability
- Risk Tier Assignment
- Policy Recommendation
- Explainability Layer
- LLM-Based Explanation


### Core Components

**1. Risk Prediction Engine**
- Models used: Logistic Regression, Random Forest, XGBoost, MLP  
- Output: Probability of insurance claim  

**2. Risk Tiering & Recommendation**
- Low Risk → Basic Plan  
- Medium Risk → Standard Plan  
- High Risk → Premium Plan  

**3. Explainability Layer**
- Feature importance (global)
- SHAP-based explanations (local)

**4. LLM-Based Assistant**
- Generates natural language explanations  
- Answers user questions about predictions and policies  
- Uses retrieval-augmented generation (RAG)  

---

## Dataset

- Source: Kaggle – Car Insurance Claim Prediction Dataset  
- Records: 58,592  
- Features: 43  
- Target: `is_claim` (0 = No Claim, 1 = Claim)

Includes:
- Policyholder demographics  
- Vehicle specifications  
- Safety and equipment features  

---

## Approach

### Data Processing
- One-hot encoding for categorical variables  
- Standardization for numerical features  
- Stratified train-test split  
- Class imbalance handled using class weights  

### Model Training
- Compared multiple model types  
- Used pipelines for consistent preprocessing  
- Evaluated using ROC-AUC, precision, recall, and F1-score  

---

## Results

- Random Forest selected as final model  
- Best balance between recall and precision  
- Moderate performance due to dataset limitations  

### Key Insight
> Model performance was constrained by feature representation rather than model complexity.

---

## Technologies Used

- Python  
- Pandas, NumPy  
- Scikit-learn  
- XGBoost  
- TensorFlow / Keras  
- SHAP  
- Jupyter Notebook  
- LLM API (for explanation layer)  

---

## Project Structure

├── notebooks/

├── data/

├── src/

├── README.md


---

## How to Run

1. Clone the repository: `git clone https://github.com/EeshaKulkarni77/Insurance-Risk-Prediction-System.git`

2. Open the notebook: `Insurance_Risk_Prediction_Code.ipynb`

3. Run all cells  

Note: The LLM component requires an API key and may incur usage limits.

---

## Key Takeaways

- Machine learning alone is not sufficient for real-world systems  
- Explainability is essential for trust and usability  
- LLMs improve accessibility of model outputs  
- Data quality impacts performance more than model complexity  

---

## Future Improvements

- Incorporate behavioral data (e.g., driving patterns)  
- Improve class imbalance handling  
- Add SHAP visualizations  
- Deploy as a web application  
- Expand LLM knowledge base  

---

## Disclaimer

This project is a prototype designed to demonstrate machine learning system design, explainability, and AI-assisted decision-making. It is not intended for real-world insurance deployment.
