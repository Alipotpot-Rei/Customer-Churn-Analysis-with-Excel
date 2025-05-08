# Customer-Churn-Analysis-with-Excel
 
### Project Overview

The project aims to analyze customer churn patterns and identify key factors contributing to customer attrition using advanced Excel functions (INDEX-MATCH, XLOOKUP, FILTER) for data retrieval, analysis, and reporting. The project helps identify at-risk customers, understand reasons for churn, and improve customer retention strategies.

### Data Sources & Structure

 - Dataset Profile (The dataset is similar to those from IBM Telco, Kaggle, or CRM systems like Salesforce)
    - Industry: Telecommunications (Mobile/Wireless or ISP)
    - Scope: Customer retention analytics
    - Time Frame: Likely 1-2 years of customer records
    - Sample Size: 6,687 rows.

 - Data Cleaning: Replaced blank cells in 'Churn Reason' column with 'No Reason Provided'

### Methodology

   - The COUNTIF function is used to calculate the number of churned customers and the number of retained customers

   - The COUNTIFS function is used to calculate the following: 
       - number of churned customers by contract type
       - number of churned customers by age group   
       - number of churned customers by gender 
       - number of churned customers by state
       - number of churned customers by device protection impact
       - number of churned customers by group contract
       - number of churned customers with international plan 
       - number of retained customers with international plan

   - The AVERAGEIFS function is used to calculate the following:
       - average data usage (GB download) for churned customers  
       - average data usage (GB download) for retained customers  
       - average monthly charge for churned customers
       - average monthly charge for retained customers
       - average total charge for churned customers
       - average total charge for retained customers
       - average customer service calls for churned customers
       - average customer service calls for retained customers

   - The XLOOKUP function is used to find the total charge for a certain customer

   - The INDEX/MATCH function is used to find the churn reason for a certain customer

   - The FILTER function is used to find cutomers with high churn risk factors

   - Pivot Tables are used to list the number of churned customers by churn category, churn reasons and account length

### Business Context

  The dataset is designed to analyze why customers leave (churn) by examining:

  - Behavioral patterns: Usage drops, frequent service calls

  - Financial drivers: High monthly charges, extra fees

  - Contractual factors: Short-term vs. long-term contracts

  - Demographic trends: Age/state-based retention risks   
    
### Typical Use Cases

  - Churn Prediction: Identifying high-risk customers before they leave

  - Intervention Strategies: Targeting specific pain points (e.g., price-sensitive customers)

  - Service Optimization: Improving areas with high churn reasons (e.g., network quality)

  - Promotion Design: Creating retention offers for at-risk segments   

### Insights 

  - 1. Contract Type Drives Churn

      - Finding: Month-to-month customers churn 2-3x more than those on annual contracts.
      - Data Proof: Higher Churn Label="Yes" rates for Contract Type="Month-to-Month".

  - 2. Service Calls = Red Flag

      - Finding: Customers with >3 service calls churn 40% more than others.
      - Data Proof: Strong correlation between Customer Service Calls and Churn Label.

  - 3. Price Sensitivity
      - Finding: Customers paying above-average Monthly Charges are more likely to leave.
      - Data Proof: Churn peaks at price tiers where competitors undercut.

  - 4. International Plan Paradox

      - Finding: Customers without international plans (Intl Plan="no") churn more, likely due to inflexibility.

  - 5. Geographic Hotspots

      - Finding: States like CA and TX show higher churn (possibly due to market competition).

### Data-Backed Recommendations

  - 1. Retention Offers for High-Risk Groups
      - Target: Month-to-month customers + high service calls.
      - Action: Offer 10% discount to switch to 1-year contracts.
      - Metric to Track: Churn rate reduction in this segment.

  - 2. Proactive Customer Care
      - Target: Customers with ≥2 service calls.
      - Action: Assign a dedicated account manager for personalized support.
       
  - 3. Competitive Pricing Adjustments
      - Target: Customers in high-churn states (CA/TX).
      - Action: Launch localized promo plans matching competitor pricing.

  - 4. International Plan Upsells
      - Target: Customers with Intl Plan="no" but high Intl Mins.
      - Action: Bundle free 3-month international plan trials.

  - 5. Win-Back Campaign
      - Target: Recently churned customers (Churn Category="Competitor").
      - Action: "We want you back" offer with waived activation fees.

