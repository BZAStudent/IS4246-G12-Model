# Loan Decision SHAP Report (Section 12)

```
======================================================================
BATCH LOAN DECISION EXPLANATIONS - FOR REPORT
======================================================================


######################################################################
CUSTOMER 1: CUST_001 - High-risk: Not graduate, self-employed, 4 dependents
######################################################################
======================================================================
🏦 LOAN APPLICATION DECISION
======================================================================
✅ APPROVED
📊 Approval Score: 47.5%
🎯 Minimum Required: 45.0%

🎉 Congratulations! Your loan application has been approved.

======================================================================
📋 APPLICATION SUMMARY
======================================================================
  • Annual Income: ₹500,000
  • Loan Amount: ₹1,500,000
  • Loan Term: 8 years
  • Credit Score: 650
  • Dependents: 4 people
  • Employment: Self-Employed
  • Education: Not Graduate
  • Existing Debt: Yes

======================================================================
NEXT CUSTOMER
======================================================================

######################################################################
CUSTOMER 2: CUST_002 - Low-risk: Graduate, salaried, strong finances
######################################################################
======================================================================
🏦 LOAN APPLICATION DECISION
======================================================================
✅ APPROVED
📊 Approval Score: 98.3%
🎯 Minimum Required: 45.0%

🎉 Congratulations! Your loan application has been approved.

======================================================================
📋 APPLICATION SUMMARY
======================================================================
  • Annual Income: ₹1,200,000
  • Loan Amount: ₹800,000
  • Loan Term: 4 years
  • Credit Score: 780
  • Dependents: 1 people
  • Employment: Salaried
  • Education: Graduate
  • Existing Debt: No

======================================================================
NEXT CUSTOMER
======================================================================

######################################################################
CUSTOMER 3: CUST_003 - Borderline: Graduate but high loan-to-income ratio
######################################################################
======================================================================
🏦 LOAN APPLICATION DECISION
======================================================================
✅ APPROVED
📊 Approval Score: 55.9%
🎯 Minimum Required: 45.0%

🎉 Congratulations! Your loan application has been approved.

======================================================================
📋 APPLICATION SUMMARY
======================================================================
  • Annual Income: ₹700,000
  • Loan Amount: ₹1,200,000
  • Loan Term: 6 years
  • Credit Score: 720
  • Dependents: 2 people
  • Employment: Salaried
  • Education: Graduate
  • Existing Debt: Yes

======================================================================
NEXT CUSTOMER
======================================================================

######################################################################
CUSTOMER 4: CUST_004 - Very high-risk: Multiple concerning factors
######################################################################
======================================================================
🏦 LOAN APPLICATION DECISION
======================================================================
❌ NOT APPROVED
📊 Your Score: 41.2%
🎯 Required Score: 45.0%
📉 Short by: 3.8% points

We appreciate your application, but based on our assessment, we are unable to approve it at this time.

======================================================================
📋 APPLICATION SUMMARY
======================================================================
  • Annual Income: ₹300,000
  • Loan Amount: ₹2,000,000
  • Loan Term: 10 years
  • Credit Score: 600
  • Dependents: 0 people
  • Employment: Self-Employed
  • Education: Not Graduate
  • Existing Debt: Yes

======================================================================
🔍 WHY WAS MY APPLICATION NOT APPROVED?
======================================================================

The application didn't meet our overall risk criteria.

The main factors affecting your application were:
--------------------------------------------------

1. Financial Dependents
   📊 Your situation: 0
   📉 Impact: Significant negative factor
   💡 Recommended: 0-2 dependents

2. Education Level
   📊 Your situation: Not Graduate
   📉 Impact: Significant negative factor
   💡 Recommended: Graduate

3. Employment Type
   📊 Your situation: Self-Employed
   📉 Impact: Significant negative factor
   💡 Recommended: Salaried employment

======================================================================
💡 HOW CAN I IMPROVE MY CHANCES?
======================================================================

Based on your application, we recommend:
  1. • Consider completing graduation to improve qualifications
  2. • Provide 2+ years of stable business income records
  3. • Maintain stable employment for 6+ months

💎 After making these improvements, your approval
   chances could increase from 41.2% to over 71.2%

================================================================================
SUMMARY TABLE - LOAN DECISION OVERVIEW
================================================================================

Customer ID  Description                                   Decision   Probability  Key Factors
----------------------------------------------------------------------------------------------------
CUST_001     High-risk: Not graduate, self-employed, 4 d... APPROVED   47.5%        Strong Profile
CUST_002     Low-risk: Graduate, salaried, strong financ... APPROVED   98.3%        Strong Profile
CUST_003     Borderline: Graduate but high loan-to-incom... APPROVED   55.9%        Strong Profile
CUST_004     Very high-risk: Multiple concerning factors   REJECTED   41.2%        no_of_dependents, education

================================================================================
DECISION STATISTICS:
Total Applications: 4
Approved: 3 (75.0%)
Rejected: 1 (25.0%)
================================================================================

```