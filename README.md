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


**Questions**
1. How can we analyze historical claim data to detect patterns that indicate fraudulent claims?
   
 - The analysis reveals several effective approaches:
a- Financial Pattern Analysis
* Track claim amount distributions and flag outliers
* Monitor claim-to-deductible ratios
* Analyze patterns in capital gains/losses
* Review policy characteristics (deductibles, umbrella limits)
b- Demographic Profiling
* Analyze claim patterns across different relationship statuses
* Study educational background correlations
* Examine occupation-based patterns
* Track geographical distribution of claims
c- Incident Characteristic Analysis
* Evaluate damage severity patterns
* Analyze witness count distributions
* Study incident timing and location patterns
* Review vehicle-related factors

2. Which features are most predictive of fraudulent behavior?
   
- The analysis identified several high-impact predictors:
* Strong Predictors:
1. Claim Characteristics:
* Damage severity (strongest predictor)
* Total claim amount
* Claim-to-deductible ratio
2. Personal Factors:
* Relationship status (unmarried, not-in-family)
* Education level (particularly MD, JD degrees)
* Occupation (transport-moving sector)
3. Vehicle/Incident Details:
* Vehicle make (Audi shows higher risk)
* Vehicle age (older vehicles lower risk)
* Witness count (higher counts indicate potential fraud)

- Moderate Predictors:
* Geographic location
* Policy characteristics
* Capital flow patterns

3. Can we predict the likelihood of fraud for an incoming claim, based on past data?
- Yes, the analysis demonstrates effective prediction capability:
Model Performance:

1. Logistic Regression Model:
* 80.33% accuracy on validation data
* 70.27% sensitivity in fraud detection
* 83.63% specificity for legitimate claims
* Reliable for balanced prediction

2. Random Forest Model:
* 86.28% specificity on validation
* 56.76% sensitivity
* Better for conservative screening

3. Prediction Reliability:
* Models show strong capability in identifying legitimate claims
* Moderate to good performance in fraud detection
* Consistent performance across different validation sets

4. What insights can be drawn from the model that can help in improving the fraud detection process?
- Key insights for process improvement:

1. Risk Assessment Framework:
* Implement tiered risk scoring based on claim characteristics
* Focus on high-impact predictors like damage severity and claim ratios
* Consider demographic and geographic risk factors

2. Process Optimization:
* Use model predictions for initial screening
* Apply stricter verification for high-risk claims
* Streamline processing for low-risk claims

3. Strategic Recommendations:
* Develop specialized review processes for high-risk combinations
* Implement automated flagging systems based on key predictors
* Create region-specific risk assessment protocols

4. Continuous Improvement:
* Regular model retraining with new data
* Threshold adjustment based on business needs
* Feature engineering for better prediction
* Consider ensemble approaches combining multiple models

5. Business Implementation:
* Balance fraud detection with customer experience
* Develop risk-based verification procedures
* Create specialized handling for high-risk categories
* Implement automated screening systems
  
These insights provide a comprehensive framework for implementing and improving fraud detection processes, leveraging both statistical analysis and business context for optimal results.





