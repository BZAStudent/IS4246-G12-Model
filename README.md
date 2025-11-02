# Loan Approval Framework

This repository demonstrates a fairness validation framework for a loan approval AI prediction model.  
The project simulates a complete workflow from data preprocessing, model training, and bias evaluation to explainable AI reporting.  
It aims to ensure that machine learning–based credit approval systems are transparent, fair, and contestable — aligned with responsible AI governance principles.

---

## Overview

This notebook builds, trains, and validates a deep neural network loan approval classifier, then performs:
- Model Performance Evaluation – Accuracy, AUC, F1 tuning  
- Fairness Assessment – Equalised Odds across Education, Employment Type, and Number of Dependents  
- Explainability Analysis – SHAP-based customer-level rejection explanations  
- Reproducible Results – Key metrics, visualisations, and synthetic examples are automatically saved under `/results/`

---

## Validation

1. Technical Validation (Performance Evaluation)
    
    After preprocessing and training the neural network model, we validated its predictive performance using a hold-out test set that was never seen during training. The metrics computed were Accuracy, AUC (ROC) and F1 score. Furthermore, a classification table was generated using sk-learn. 

2. Equalised Odds

    To evaluate algorithmic fairness, we applied the Equalised Odds criterion, measures whether True Positive Rate (TPR) and False Positive Rate (FPR) are approximately equal across sensitive subgroups. We examined three key attributes that may cause unfair bias in loan approval, Education — Graduate vs Not Graduate, Employment Type — Self-Employed vs Salaried and Number of Dependents — 0–5 dependents.
    
    For each subgroup, we computed:
    
    TPR (True Positive Rate) — how often qualified applicants are correctly approved.
    
    FPR (False Positive Rate) — how often unqualified applicants are wrongly approved.
    
    Differences in these rates (ΔTPR and ΔFPR) were summarised in section 12. Smaller differences indicate more equitable treatment across groups. This step directly supports the Fairness and Accountability principles in AI governance.

3. Interpretability Validation (Explainability & Transparency)
    
    We then validated whether the model’s predictions can be explained to end-users in a clear and actionable manner. Using SHAP (SHapley Additive exPlanations), we generated Feature importance plots that illustrates which input variables most influence approval probability and Customer-specific explanations that summarised why an application was approved or rejected, and how to improve outcomes.



## Repository Structure

loan-fairness-validation/
│
├── fairness_validation.ipynb        ← Main notebook (Google Colab compatible)
│
├── data/
│   └── synthetic_loan_data.csv       ← Small sample dataset (non-confidential)
│
├── results/
│   ├── model_metrics.json            ← Accuracy, AUC, threshold, F1
│   ├── feature_importance.png        ← Permutation feature importance plot
│   ├── equalised_odds_education.csv  ← Fairness by education level
│   ├── equalised_odds_employment.csv ← Fairness by employment type
│   ├── equalised_odds_dependents.csv ← Fairness by dependents count
│   ├── equalised_odds_summary.json   ← Summary of TPR/FPR gaps
│   ├── bias_plots/
│   │   ├── confusion_matrix.png
│   │   ├── roc_curve.png
│   │   └── pr_curve.png
│   └── customer_explanations.txt     ← SHAP-based customer-level explanations
│
└── README.md

---

## Requirements

The notebook runs directly in Google Colab, but you can also execute it locally:

pip install torch torchvision torchaudio
pip install scikit-learn shap seaborn matplotlib pandas

---

## How to Reproduce

### Option 1 — Run in Google Colab
Click the badge below to open and execute the notebook directly:
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/<your-username>/loan-fairness-validation/blob/main/fairness_validation.ipynb)

1. Run all cells sequentially.  
2. All generated outputs (metrics, bias plots, SHAP explanations) will appear under `/results/`.

### Option 2 — Run Locally

git clone https://github.com/<your-username>/loan-fairness-validation.git
cd loan-fairness-validation
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
jupyter notebook fairness_validation.ipynb

---

## Validation Metrics

| Metric | Description |
|:--------|:-------------|
| Accuracy | Overall model correctness on test set |
| AUC (ROC) | Ability to distinguish approved vs rejected applicants |
| Equalised Odds | Fairness check across sensitive subgroups |
| Permutation Importance | Measures contribution of each feature |
| SHAP Explanations | Individual-level interpretability for loan decisions |

---

## Fairness Assessment

The notebook computes Equalised Odds per subgroup:
- Education: Graduate vs Not Graduate  
- Employment Type: Self-Employed vs Salaried  
- Number of Dependents: 0–4  

Each subgroup’s True Positive Rate (TPR) and False Positive Rate (FPR) differences are summarised in `/results/equalised_odds_summary.json`.

---

## Explainability & Transparency

Using SHAP, the framework generates natural-language explanations for approval or rejection decisions.  
Each customer report includes:
- Key factors influencing the outcome  
- Recommended improvement actions  
- Predicted approval probability  

Example excerpts are stored in `/results/customer_explanations.txt`.

---

## Key Outputs

| Output | File | Description |
|:--------|:------|:-------------|
| Model Performance | model_metrics.json | Accuracy, AUC, F1 |
| Fairness Plots | bias_plots/*.png | Confusion, ROC, PR curves |
| Equalised Odds | equalised_odds_*.csv | Subgroup fairness tables |
| Explainability | customer_explanations.txt | SHAP explanations |
| Feature Importance | feature_importance.png | Most influential features |

---

## Acknowledgement

This notebook was developed as part of the IS4246 project on Responsible AI and Fairness Validation.  
It demonstrates practical governance tools aligned with MAS FEAT and AI Verify frameworks.
