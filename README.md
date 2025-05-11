# SyriaTel-Customer-Churn-Classification-Project
![image](https://github.com/user-attachments/assets/5a9c6449-3dbb-463f-b9dd-adb1fc53269e)




## Predicting-Customer-Churn-at-SyriaTel-A-Strategic-Analysis-to-Improve-Retention
This project predicts customer churn at SyriaTel, a telecommunications company, using data science and machine learning. It analyzes historical data to identify churn patterns, helping SyriaTel improve retention, reduce revenue loss, and make informed decisions through a binary classification model.

## Business Understanding 
Churn, also known as customer attrition, refers to the percentage of customers who discontinue or stop using a company’s services during a given period. For telecommunications companies like SyriaTel, churn is a critical metric because it directly impacts revenue growth and profitability. When a customer leaves, the company not only loses the revenue from that customer but also incurs higher costs in trying to acquire new customers to replace them.

Acquiring new customers is significantly more expensive than retaining existing ones, [with estimates suggesting that it's up to 5 times more costly](https://www.surveysensum.com/customer-experience/saas-customer-retention#:~:text=The%20same%20study%20shows%20that,and%20addressing%20clients'%20evolving%20needs.). In a highly competitive global market, telecom companies face the constant challenge of retaining customers who have various options and can easily switch providers. High churn rates increase the costs of acquiring new customers and maintaining market share, affecting a company’s ability to grow and invest in new technologies or services.

Predicting and reducing churn is not only essential for sustaining SyriaTel’s market position but also for ensuring its capacity to grow, innovate, and provide competitive services in a rapidly evolving industry.

## Problem Statement
SyriaTel, a telecommunications company, is facing a high customer churn rate, negatively impacting its revenue growth and profitability. Customer acquisition is up to five times more expensive than retaining existing customers, making this a significant financial challenge. In an increasingly competitive market with numerous alternatives for customers, high churn rates make it difficult for SyriaTel to maintain its market share, reinvest in innovation, and achieve long-term growth.

## Objectives
1. To Identify Churn Rates by Region and which region is highly affected.
2. To examine the impact of Account Length on Churn. Which customers are highly prone to attrition.
3. To assess the influence of subscription plans (voicemail and international plans) on churn.
4. To evaluate the impact of customer service calls on churn and determine if there is a statistically significant relationship.
5. To predict churn by focusing on the most influential features that drive customer behavior and retention patterns.

## Success Metrics
The success metric for this project would be to achieve a recall rate of at least 70%, ensuring that the model identifies a significant percentage of customers at risk of churning. This will allow the business to proactively target retention efforts, minimizing customer loss while balancing the cost of engaging non-churners. With this, SyriaTel will take timely retention actions and allocate resources more effectively to prevent churn.

## Data Understanding and Preparation

This dataset was obtained from [kaggle](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset?resource=download) and contains customers' data from SyriaTel, a telecommunications company. It includes various features related to customer behavior, usage patterns, and service details, which are crucial for analyzing customer churn and understanding the factors that influence retention. The dataset entails 21 columns and 3333 rows. 

The cleaning of this dataset entailed dealing with outliers, dealing with duplicates, checking for missing values which the dataset didn't have, harmonizing the various data types and also operating both dummy encoding and label encoding in preparation of the data for modeling.

## Data Visualization and Analysis Objectives

1. To Identify Churn Rates by Region and which region is highly affected.
  
2. To examine the impact of Account Length on Churn. Which customers are highly prone to attrition.

3. To assess the influence of subscription plans (voicemail and international plans) on churn.

4. To evaluate the impact of customer service calls on churn and determine if there is a statistically significant relationship.

5. To predict churn by focusing on the most influential features that drive customer behavior and retention patterns.
   

Achieving these objectives involved training four distinct models: basic logistic regression and decision tree models, along with enhanced versions of both. The second models incorporated feature selection, addressed class imbalance using class weights, applied regularization (for logistic regression), and employed hyperparameter tuning (adjusting max depth, min samples, and entropy) for the decision tree models.

Logistic regression and decision tree models were chosen as they were well-suited for analyzing the categorical nature of the target variable (churn).

These models were analysed further using four different metrics entailing, cross validation score, confusion matrix, ROC Curve and classification Report. 

 ![image](https://github.com/user-attachments/assets/c92784b5-9f3f-4e71-8886-e1d7d47eba64)

 ![image](https://github.com/user-attachments/assets/06aff32d-b238-4dce-8b29-0ca9bba2b824)

 ![image](https://github.com/user-attachments/assets/601589a3-4f7f-46f9-9986-74ce781b489b)



- Based on validation score, the second logistic model presentred to have the highest score.
- Based on ROC-Curve, the Logistic Second Model,emerged as the best-performing model, achieving the highest TPR and lowest FPR, indicating effective optimization for churn prediction.
- Based on confusion matrix, the second logistic model recorded the highest number of true positives, outperforming others in correctly predicting churns. However, it also recorded more false positives, indicating a tendency to overpredict churn.
- Based on Classification report the emphasis was on recall, which tells how well is our model's ability in predicting churn. In this case as well, The second logistic model presented to have the highest recall compared to the rest.



## Conclusion
- The highly affected region for churn is 408, which has the leading churn rate

- The churn rate analysis based on account length shows that long-term customers (over 14 years) have the highest churn rate, followed by short-term customers (7 years or less) with the second-highest churn rate, while mid-term customers (7-14 years) exhibit the lowest churn rate.

- The findings reveal that customers with an International Plan but no Voicemail Plan have the highest churn rate, followed by those with both plans, while customers without either plan have the third-highest churn rate, and those with only a Voicemail Plan have the lowest churn rate.

- The analysis indicates that the average number of customer service calls is relatively high for both churners and non-churners, with no statistically significant relationship between customer service calls and churn rate.

- Based on the analysis, the second logistic regression model stands out as the most effective for predicting customer churn at SyriaTel.It meets the success criteria achieving a 77% recall. While it has a slightly higher False Positive rate, its superior recall score ensures it effectively identifies churners, a critical aspect for enhancing retention strategies. The model highlights key factors influencing churn, including call charges, account length, geographic region, subscription options, and the number of calls/minutes relative to charges.

## Recommendations
- SyriaTel should conduct further research to identify the factors driving the high churn rate in the 408 region, which differs from others, and develop targeted strategies for improving customer retention.

- SyriaTel should focus on retaining long-term customers by addressing potential dissatisfaction and innovating offerings, while improving short-term customer satisfaction through better onboarding and support. Mid-term customers should be engaged with loyalty programs to maintain their retention.

- SyriaTel should focus on retaining International Plan customers, especially those without a Voicemail Plan, by offering cost-effective strategies like enhancing plan benefits, bundling services, and improving customer support.

- Since customer service calls are not significantly related to churn rate, S SyriaTel should shift focus to improving other key aspects of the customer experience, such as product quality, pricing, and service offerings, to enhance customer retention and reduce churn.

- Based on the findings, SyriaTel should prioritize further tuning and optimization of the second logistic regression model, as its superior recall score makes it more effective at identifying churners, thereby enhancing customer retention strategies and reducing churn.


## Next Steps
- Deploy the logistic regression model into SyriaTel's customer retention system. Integrate the model's predictions into real-time operations, such as CRM systems, to trigger automated retention actions like personalized offers or loyalty programs for at-risk customers.The model should also be continuously updated with new customer data to maintain its predictive power and accuracy over time.

- There is a need for a deep dive into the 408 region to gather customer feedback or detailed insights into regional challenges. Further qualitative analysis may be needed to understand if factors like service quality, local competition, or pricing are impacting retention.

- Implement a feedback loop to gather insights from customers who churn and those who stay, continuously improving the customer experience and identifying pain points that were not previously addressed. Additionally, a structured process is needed for collecting and acting on customer feedback.
