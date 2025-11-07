# Loan Decision SHAP Report (Batch)

```

================================================================================
SHAP-BASED LOAN DECISIONS ANALYSIS
================================================================================

CUSTOMER 1 PROFILE
--------------------------------------------------
DECISION SUMMARY:
   • Final Decision: APPROVED
   • Approval Probability: 98.2%
   • Actual Outcome: Approved

CUSTOMER BACKGROUND:
   • Education Level: Graduate
   • Employment Type: Self-Employed
   • Dependents: 2 people
   • Annual Income: $2,000,000
   • Debt Indicator: No

FINANCIAL PROFILE:
   • Loan Amount: $6,700,000
   • Loan Term: 14 years
   • Credit Score (CIBIL): 638
   • Total Assets: $12,300,000

SHAP-BASED DECISION DRIVERS:
KEY APPROVAL STRENGTHS:
   1. [CRITICAL] cibil_score
      Increased probability by 0.490
      Credit score of 638 indicates moderate credit risk
   2. [LOW] income_annum
      Increased probability by 0.028
      Income provides 0.3x coverage of loan amount
   3. [LOW] luxury_assets_value
      Increased probability by 0.008
      Luxury assets provide financial security

RECOMMENDATIONS:
   1. Continue maintaining good credit score
--------------------------------------------------

CUSTOMER 2 PROFILE
--------------------------------------------------
DECISION SUMMARY:
   • Final Decision: REJECTED
   • Approval Probability: 0.2%
   • Actual Outcome: Rejected

CUSTOMER BACKGROUND:
   • Education Level: Graduate
   • Employment Type: Salaried
   • Dependents: 2 people
   • Annual Income: $7,000,000
   • Debt Indicator: No

FINANCIAL PROFILE:
   • Loan Amount: $25,700,000
   • Loan Term: 18 years
   • Credit Score (CIBIL): 374
   • Total Assets: $36,500,000

SHAP-BASED DECISION DRIVERS:
KEY REJECTION FACTORS:
   1. [CRITICAL] cibil_score
      Reduced probability by 0.445
      Credit score of 374 is below minimum requirements (600+)
   2. [MEDIUM] loan_term
      Reduced probability by 0.069
      18-year term influences repayment schedule
   3. [LOW] income_annum
      Reduced probability by 0.015
      Income provides 0.3x coverage of loan amount

RECOMMENDATIONS:
   1. Improve credit score from 374 to 650+ by clearing outstanding debts
--------------------------------------------------

CUSTOMER 3 PROFILE
--------------------------------------------------
DECISION SUMMARY:
   • Final Decision: APPROVED
   • Approval Probability: 99.4%
   • Actual Outcome: Approved

CUSTOMER BACKGROUND:
   • Education Level: Not Graduate
   • Employment Type: Self-Employed
   • Dependents: 3 people
   • Annual Income: $7,700,000
   • Debt Indicator: No

FINANCIAL PROFILE:
   • Loan Amount: $18,100,000
   • Loan Term: 20 years
   • Credit Score (CIBIL): 736
   • Total Assets: $61,400,000

SHAP-BASED DECISION DRIVERS:
KEY APPROVAL STRENGTHS:
   1. [CRITICAL] cibil_score
      Increased probability by 0.527
      Excellent credit score of 736 demonstrates strong creditworthiness
   2. [LOW] loan_amount
      Increased probability by 0.004
      Loan amount represents 2.4x annual income
   3. [LOW] bank_asset_value
      Increased probability by 0.003
      Feature contributes to risk assessment

RECOMMENDATIONS:
   1. Continue maintaining good credit score
--------------------------------------------------

CUSTOMER 4 PROFILE
--------------------------------------------------
DECISION SUMMARY:
   • Final Decision: APPROVED
   • Approval Probability: 99.6%
   • Actual Outcome: Approved

CUSTOMER BACKGROUND:
   • Education Level: Not Graduate
   • Employment Type: Self-Employed
   • Dependents: 4 people
   • Annual Income: $4,100,000
   • Debt Indicator: No

FINANCIAL PROFILE:
   • Loan Amount: $10,400,000
   • Loan Term: 12 years
   • Credit Score (CIBIL): 727
   • Total Assets: $38,600,000

SHAP-BASED DECISION DRIVERS:
KEY APPROVAL STRENGTHS:
   1. [CRITICAL] cibil_score
      Increased probability by 0.508
      Excellent credit score of 727 demonstrates strong creditworthiness
   2. [LOW] income_annum
      Increased probability by 0.013
      Income provides 0.4x coverage of loan amount
   3. [LOW] residential_assets_value
      Increased probability by 0.006
      Residential assets provide financial security

RECOMMENDATIONS:
   1. Continue maintaining good credit score
--------------------------------------------------

CUSTOMER 5 PROFILE
--------------------------------------------------
DECISION SUMMARY:
   • Final Decision: APPROVED
   • Approval Probability: 99.2%
   • Actual Outcome: Approved

CUSTOMER BACKGROUND:
   • Education Level: Not Graduate
   • Employment Type: Salaried
   • Dependents: 1 people
   • Annual Income: $2,900,000
   • Debt Indicator: No

FINANCIAL PROFILE:
   • Loan Amount: $9,600,000
   • Loan Term: 4 years
   • Credit Score (CIBIL): 658
   • Total Assets: $22,200,000

SHAP-BASED DECISION DRIVERS:
KEY APPROVAL STRENGTHS:
   1. [CRITICAL] cibil_score
      Increased probability by 0.434
      Credit score of 658 indicates moderate credit risk
   2. [MEDIUM] loan_term
      Increased probability by 0.044
      4-year term influences repayment schedule
   3. [LOW] income_annum
      Increased probability by 0.024
      Income provides 0.3x coverage of loan amount

RECOMMENDATIONS:
   1. Continue maintaining good credit score
--------------------------------------------------

CUSTOMER 6 PROFILE
--------------------------------------------------
DECISION SUMMARY:
   • Final Decision: REJECTED
   • Approval Probability: 1.8%
   • Actual Outcome: Rejected

CUSTOMER BACKGROUND:
   • Education Level: Not Graduate
   • Employment Type: Salaried
   • Dependents: 2 people
   • Annual Income: $1,500,000
   • Debt Indicator: Yes

FINANCIAL PROFILE:
   • Loan Amount: $4,900,000
   • Loan Term: 16 years
   • Credit Score (CIBIL): 387
   • Total Assets: $7,300,000

SHAP-BASED DECISION DRIVERS:
KEY REJECTION FACTORS:
   1. [CRITICAL] cibil_score
      Reduced probability by 0.390
      Credit score of 387 is below minimum requirements (600+)
   2. [MEDIUM] has_debt
      Reduced probability by 0.076
      Customer has existing debt obligations, which increased risk assessment
   3. [MEDIUM] loan_term
      Reduced probability by 0.030
      16-year term influences repayment schedule

RECOMMENDATIONS:
   1. Improve credit score from 387 to 650+ by clearing outstanding debts
   2. Reduce outstanding debts before reapplying
--------------------------------------------------

CUSTOMER 7 PROFILE
--------------------------------------------------
DECISION SUMMARY:
   • Final Decision: APPROVED
   • Approval Probability: 98.7%
   • Actual Outcome: Approved

CUSTOMER BACKGROUND:
   • Education Level: Not Graduate
   • Employment Type: Salaried
   • Dependents: 1 people
   • Annual Income: $800,000
   • Debt Indicator: No

FINANCIAL PROFILE:
   • Loan Amount: $2,900,000
   • Loan Term: 8 years
   • Credit Score (CIBIL): 682
   • Total Assets: $6,900,000

SHAP-BASED DECISION DRIVERS:
KEY APPROVAL STRENGTHS:
   1. [CRITICAL] cibil_score
      Increased probability by 0.473
      Credit score of 682 indicates moderate credit risk
   2. [MEDIUM] income_annum
      Increased probability by 0.052
      Income provides 0.3x coverage of loan amount
   3. [LOW] loan_term
      Increased probability by 0.013
      8-year term influences repayment schedule

RECOMMENDATIONS:
   1. Continue maintaining good credit score
--------------------------------------------------

CUSTOMER 8 PROFILE
--------------------------------------------------
DECISION SUMMARY:
   • Final Decision: REJECTED
   • Approval Probability: 12.7%
   • Actual Outcome: Rejected

CUSTOMER BACKGROUND:
   • Education Level: Graduate
   • Employment Type: Self-Employed
   • Dependents: 3 people
   • Annual Income: $9,200,000
   • Debt Indicator: No

FINANCIAL PROFILE:
   • Loan Amount: $28,900,000
   • Loan Term: 8 years
   • Credit Score (CIBIL): 538
   • Total Assets: $59,500,000

SHAP-BASED DECISION DRIVERS:
KEY REJECTION FACTORS:
   1. [CRITICAL] cibil_score
      Reduced probability by 0.244
      Credit score of 538 is below minimum requirements (600+)
   2. [CRITICAL] income_annum
      Reduced probability by 0.172
      Income provides 0.3x coverage of loan amount
   3. [MEDIUM] luxury_assets_value
      Reduced probability by 0.046
      Luxury assets provide financial security

RECOMMENDATIONS:
   1. Improve credit score from 538 to 650+ by clearing outstanding debts
--------------------------------------------------

```