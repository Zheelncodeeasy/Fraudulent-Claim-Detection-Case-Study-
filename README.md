# Fraudulent-Claim-Detection-Case-Study-

## Problem Statement
Global Insure, a leading insurance company, processes thousands of claims annually. However, a significant percentage of these claims turn out to be fraudulent, resulting in considerable financial losses. The company’s current process for identifying fraudulent claims involves manual inspections, which is time-consuming and inefficient. Fraudulent claims are often detected too late in the process, after the company has already paid out significant amounts. Global Insure wants to improve its fraud detection process using data-driven insights to classify claims as fraudulent or legitimate early in the approval process. This would minimise financial losses and optimise the overall claims handling process.

## Business Objective
Global Insure wants to build a model to classify insurance claims as either fraudulent or legitimate based on historical claim details and customer profiles. By using features like claim amounts, customer profiles and claim types, the company aims to predict which claims are likely to be fraudulent before they are approved.


Based on this assignment, you have to answer the following questions:<br>

● How can we analyse historical claim data to detect patterns that indicate fraudulent claims?<br>
● Which features are most predictive of fraudulent behaviour?<br>
● Can we predict the likelihood of fraud for an incoming claim, based on past data?<br>
● What insights can be drawn from the model that can help in improving the fraud detection process?<br>

## Key Insights from Feature Importances

- **Damage Severity**:  
  - `incident_severity_Minor Damage` is the top predictor, followed by `incident_severity_Total Loss` and `incident_severity_Trivial Damage`. Severity level is the strongest fraud signal.

- **Claim Size & Financial Ratios**:  
  - `total_claim_amount` and `claim_deduct_ratio` rank high, showing that larger claims and high claim-to-deductible ratios are strongly associated with fraud.

- **Behavioral Flags**:  
  - `insured_hobbies_chess` emerges as a notable non-financial indicator.

- **Customer & Incident Context**:  
  - `months_as_customer`, `net_capital`, and timing features (`incident_hour_of_the_day`, `incident_dayofweek`) provide additional signal.

- **Supporting Factors**:  
  - Vehicle age (`auto_year`), injury counts (`witnesses`, `bodily_injuries`), and policy attributes (`umbrella_limit`, `policy_deductable`) contribute modestly.

**Conclusion:**  
Severity and monetary structure drive most of the model’s predictive power, with select behavioral and temporal factors offering useful enhancements.  
