# Churn Analysis and Prediction
## Project Overview
This project aims to uncover the key drivers of customer churn and to develop a predictive model that identifies customers at risk of churning in advance. By understanding the underlying factors, the company can implement targeted strategies to improve retention and reduce churn rates.

## Objectives
Uncover Key Churn Drivers: Identify the most influential factors that contribute to customer churn.
Predictive Modeling: Build and tune a machine learning model to forecast potential churners, enabling proactive retention efforts.

## Methodology
### 1. Data Collection and Initial Exploration
- Data Collection: The dataset, containing customer demographics, transaction details, and behavioral data, was collected from internal sources.
- Descriptive Analysis: A brief analysis was performed to understand the structure and distribution of the data.
### 2. Data Preprocessing
Missing Values Handling:
- Numerical Variables: Imputed missing values using the median.
- Categorical Variables: Imputed missing values using the mode.
- Data Imbalance:
  ![Customer_churn_percentage](https://github.com/user-attachments/assets/21907978-9121-44e5-86c8-ced2c359d862)

- Churn distribution: 16.8% churn vs. 83.2% non-churn.
The imbalance was deemed manageable without immediate need for re-sampling.
### 3. Exploratory Data Analysis (EDA)
Statistical Analysis:
- Conducted univariate, bivariate, and multivariate analyses to assess the relationships between features and churn.
- Performed ANOVA tests to determine statistically significant differences.
### Key Statistical Insights:
- Gender: The odds of churning are approximately 1.17 times higher for one gender compared to the other (Odds Ratio ≈ 1.1754), with males being more likely to churn.
  ![Customer_churn_distribution_by_gender](https://github.com/user-attachments/assets/503957ac-3036-4f60-9a67-45e199c28f05)


- Cashback: Non-churn customers have an average cashback of $180, suggesting that higher cashback rewards are linked to lower churn.
- Complaints: Customers who churned lodged significantly more complaints.
  ![Customer_comolaint_percentage_](https://github.com/user-attachments/assets/e90e1963-a8a5-4afe-84e7-c54969d7d3f8)

- Distance: Churned customers lived an average of 16.85 km from the warehouse versus 15.30 km for non-churners.
- City Tier: Customers in higher-tier cities are more likely to churn.
- Tenure: Churned customers had a much shorter average tenure (3.8 months) compared to non-churned customers (11.4 months).
- Preferred Payment Mode: Customers using COD show the highest churn, followed by those using E-wallets.
  ![Preferred_payment_mode](https://github.com/user-attachments/assets/7d3f053b-bbde-49e6-bd27-7b259f2ecd2d)
- Satisfaction score
- ![Satisfaction_score_distribution](https://github.com/user-attachments/assets/15c018ec-6354-439a-a8b4-e167521a5823)

- Order Category: Customers preferring Mobile/Mobile phone categories exhibit a churn rate of 27%.
- Marital Status: Single customers have the highest churn rate (26%).
### 4. Feature Engineering
- Engineered new features and transformed existing ones to better capture the nuances in customer behavior.
- Created variables such as order count, satisfaction score, days since the last order, and warehouse-to-home distance to enhance predictive power.
### 5. Model Building and Evaluation
- Model Development: Built a predictive model using machine learning algorithms.
- Hyper-Parameter Tuning: Optimized model parameters to achieve the best performance.
- Model Evaluation: Assessed the model using standard evaluation metrics (accuracy, precision, recall, AUC) to ensure robust performance in predicting churn.
  Evaluation for the Best Model:
### Precision: 0.9297
###  Recall: 0.8655
### F1-Score: 0.8964
###  Accuracy Score: 0.9674

![Evaluation Metrics](https://github.com/user-attachments/assets/b9ee516b-e752-4298-b329-affcb33441c4)

### Confusion Metrix
![Confusion Metric](https://github.com/user-attachments/assets/528fa62e-0f5b-425a-879d-ac5c54f1a0dc)



### 6. Feature Importance Analysis
The feature importance analysis confirmed the key drivers of churn, ranked as follows:


![Feature_importance](https://github.com/user-attachments/assets/ab380ed8-7f88-47a0-be8a-e292bfc3a459)


- Tenure
- Order Count
- Satisfaction Score
- Preferred Mode of Payment
- Warehouse-to-Home Distance
- Customer Complaints
- Day Since Last Order
- Cashback Amount
- Order Hike
- City Tier
These results underscore that customer tenure is the most significant predictor, with additional factors such as order frequency, satisfaction, and payment method also playing critical roles.

## Insights and Recommendations
### Key Insights
- Customer Tenure: Shorter tenure is strongly associated with higher churn, highlighting the need for improved onboarding and early customer engagement.
- Cashback Incentives: Customers receiving higher cashbacks are less likely to churn, suggesting that competitive rewards can foster loyalty.
- Customer Complaints: An elevated number of complaints is a clear indicator of churn risk.
- Geographical Factors: Greater distances from the warehouse and residence in higher-tier cities correlate with increased churn.
- Behavioral Drivers: Payment method and preferred order categories (notably Mobile/Mobile phone) are significant in understanding churn behavior.

## Recommendations
- Enhance Customer Support: Implement robust complaint resolution processes to address issues promptly.
- Competitive Cashback Programs: Maintain or enhance cashback incentives to retain customers.
- Improve Logistics: Optimize delivery processes to minimize the negative impact of distance.
- Targeted Marketing: Develop specific marketing strategies for customers in high-tier cities.
- Focus on Early Engagement: Strengthen the onboarding process to improve early customer satisfaction.
- Review Payment Methods: Encourage payment options that have lower churn rates (e.g., shift from COD to digital payments).
