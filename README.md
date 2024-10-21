#### BUSINESS UNDERSTANDING

Understanding telecom customer churn is crucial for businesses in the telecommunications industry, as it directly impacts revenue, customer retention, and overall profitability. Customer churn can be voluntary because of dissatisfaction in the services by the service provider and it can also be involuntary because of service disruption or payment issues. Understanding customer churn rates can have financial implications to the provider. Maintaining current customers is cheaper than that acquiring new ones. Analysing churn rates can give an advantage over competitors. This project aims to predict whether a customer will churn or not depending on the several factors on the datasets.

#### DATA UNDERSTANDING

This SyriaTel data is from https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset, a Telecommunication company. The dataset contains information about customer churn, which is a significant problem for telecom companies. The goal is to predict whether a customer will churn or not. The dataset contains the following columns:'state', 'account length', 'area code', 'phone number','international plan', 'voice mail plan', 'number vmail messages','total day minutes', 'total day calls', 'total day charge','total eve minutes', 'total eve calls', 'total eve charge','total night minutes', 'total night calls', 'total night charge','total intl minutes', 'total intl calls', 'total intl charge','customer service calls', 'churn'

**Data Visualization**
The dataset is visualized using the following plots:
1. Churn Distribution

![alt text](image.png)

2. Count Plot

![alt text](image-1.png)
State: The plot shows that the number of churned customers is relatively consistent across different states, with a few states having slightly higher or lower churn rates.
Area Code: While the area code 415 has the highest number of customers, the churn rates across the three area codes (408, 415, and 510) are relatively similar.
International Plan: Customers with an international plan have a significantly higher churn rate compared to those without.
Voice Mail Plan: Customers with a voice mail plan have a slightly lower churn rate compared to those without.
International Plan: The international plan seems to be a strong predictor of churn. The company may want to investigate why customers with international plans are more likely to churn.
Voice Mail Plan: While the effect is less pronounced, having a voice mail plan appears to be slightly correlated with lower churn rates.
State and Area Code: While there are some variations in churn rates across states and area codes, these factors do not seem to be as significant as the international plan and voice mail plan.

3. International plan vs Churn
![alt text](<Visualizations/International Plan vs Churn.png>)
The plot suggests a strong association between having an international plan and customer churn. Customers who subscribed to the international plan are more likely to churn compared to those who did not. This could indicate potential issues or dissatisfaction with the international plan service, which might be worth investigating further.


