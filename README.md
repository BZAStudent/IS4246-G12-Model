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

## Key Outputs

| Output | File | Description |
|:--------|:------|:-------------|
| Model Performance | model_metrics.json | Accuracy, AUC, F1 |
| Fairness Plots | bias_plots/*.png | Confusion, ROC, PR curves |
| Equalised Odds | equalised_odds_*.csv | Subgroup fairness tables |
| Explainability | customer_explanations.txt | SHAP explanations |
| Feature Importance | feature_importance.png | Most influential features |

---

## Requirements

The notebook runs directly in Google Colab, but you can also execute it locally:

pip install torch torchvision torchaudio
pip install scikit-learn shap seaborn matplotlib pandas

---

## How to Reproduce

### Option 1 — Run in Google Colab
Click the badge below to open and execute the notebook directly:
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/BZAStudent/IS4246-G12-Model/blob/main/IS4246_Model_pynb.ipynb)

1. Run Environment Setup, Imports & Reproducibility and Data Loading & Preprocessing.
2. Under section 2, a file-picker dialog will appear where you need to select the csv file to upload. Please upload the "loan_approval_dataset.csv". You can download the loan dataset from the github repo, under "data".
3. Run all cells sequentially.  
4. All generated outputs (metrics, bias plots, and SHAP explanations) will appear under sections 10 – 13.

---

## Acknowledgement

This notebook was developed as part of the IS4246 project on Responsible AI and Fairness Validation.  
It demonstrates practical governance tools aligned with MAS FEAT and AI Verify frameworks.
