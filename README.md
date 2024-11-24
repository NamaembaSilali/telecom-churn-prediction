### **THE CHURN FACTOR: UNLOCKING CUSTOMER ROYALTY IN TELECOM**

#### BUSINESS UNDERSTANDING

Understanding telecom customer churn is crucial for businesses in the telecommunications industry, as it directly impacts revenue, customer retention, and overall profitability. Customer churn can be voluntary because of dissatisfaction in the services by the service provider and it can also be involuntary because of service disruption or payment issues. Understanding customer churn rates can have financial implications to the provider. Maintaining current customers is cheaper than that acquiring new ones. Analysing churn rates can give an advantage over competitors. This project aims to predict whether a customer will churn or not depending on the several factors on the datasets.

#### DATA UNDERSTANDING

This SyriaTel data is from https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset, a Telecommunication company. The dataset contains information about customer churn, which is a significant problem for telecom companies. The goal is to predict whether a customer will churn or not. The dataset contains the following columns:'state', 'account length', 'area code', 'phone number','international plan', 'voice mail plan', 'number vmail messages','total day minutes', 'total day calls', 'total day charge','total eve minutes', 'total eve calls', 'total eve charge','total night minutes', 'total night calls', 'total night charge','total intl minutes', 'total intl calls', 'total intl charge','customer service calls', 'churn'

**Data Visualization**
The dataset is visualized using the following plots:
1. Churn Distribution

![alt text](<Visualizations/Churn Distribution.png>)

The plot indicates a churn rate of 14.49%. This means that approximately 14.49% of customers have left or are likely to leave the company.The majority of customers (represented by the blue bar) have not churned (False). The smaller pink bar represents the portion of customers who have churned (True).
Customer Retention: The company has a relatively high proportion of customers who have remained loyal.
Churn Prevention: Despite the majority of customers staying, the churn rate of 14.49% suggests that there is room for improvement in customer retention efforts.

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

4. Pairplot

![alt text](Visualizations/Pairplot.png)
*Distributions*

Features like 'customer service calls' and 'account length' show skewed distributions, suggesting they may have an impact on churn. The "customer service calls" feature appears to have distinct separations in churn behavior (many churned customers made a higher number of service calls).

*Relationships*

The scatter plots show the correlation between features and churn rates. For example, high total day minutes or total eve minutes don’t seem to correlate strongly with churn, given the scattered distribution.
customer service calls seems to show some level of separation between churn and non-churn classes, implying it might be a significant predictor.


#### Data Collection and Preprocessing:

The dataset includes various customer attributes such as demographics, usage patterns, account information, and service data.

* Data Cleaning: Missing values were handled, and outliers were addressed to ensure the dataset was ready for modeling.
* Feature Engineering: Categorical variables were encoded using techniques like One-Hot Encoding or Label Encoding. Numerical features were standardized or normalized where necessary.

#### MODELING

*Model Selection*

* Initial Model Exploration: Several classification models were considered, including Logistic Regression, Decision Trees, Random Forests, and Support Vector Machines (SVMs).
* Stacking Model Chosen: A Stacking Classifier was selected as the best model, combining multiple base models (e.g., Decision Trees, Logistic Regression, Random Forest) for better accuracy and robustness.

*Model Training and Evaluation:*

* Training: The stacking model was trained on the training dataset, with hyperparameters optimized for better performance.
* Metrics Evaluated: Accuracy, Precision, Recall, and F1-Score were used to evaluate the model’s performance. Recall was especially important due to the need to catch as many churned customers as possible.
* Cross-validation: K-fold cross-validation was used to validate the model's performance and ensure that it generalized well on unseen data.

*Model Performance:*

Final Metrics: The stacking model achieved a high accuracy of 0.97, with an F1-Score of 0.97 demonstrating a good balance between precision and recall. Recall was high, indicating the model effectively identified churned customers.

#### CONCLUSION

After thoroughly evaluating various classification models for predicting customer churn in the telecom industry, the stacking model has emerged as the most effective model of choice for this task. The performance metrics indicate that the stacking model offers a comprehensive approach by combining the strengths of multiple models, which allows it to outperform individual models like Logistic Regression, Decision Trees, or Random Forests in certain areas.

*Key Findings:*

* The stacking model achieved an accuracy of 97.6%, indicating a high overall classification performance, with a precision of 97.6%, recall of 97.6%, and F1 score of 97.53%. These metrics demonstrate that the model not only correctly classifies a large proportion of churn and non-churn customers, but it also balances false positives and false negatives effectively.

* The stacking model is particularly beneficial in this context as it combines multiple base learners, such as Decision Trees, Logistic Regression, and Random Forests, thus leveraging their individual strengths to capture complex relationships in the data.

* The precision and recall scores indicate that the model is well-suited for identifying customers likely to churn (high recall) while maintaining a relatively low false positive rate (high precision). The F1 score further supports this, showing a strong balance between precision and recall, which is crucial for reducing both churn and retention costs for telecom companies.

#### RECOMMENDATIONS

* Given the stacking model's strong predictive capabilities, it is recommended that the telecom company adopt this model for customer churn prediction. By accurately identifying high-risk customers, the company can implement targeted retention strategies, such as personalized offers or customer engagement initiatives, to reduce churn and improve customer loyalty.

* Additionally, the high precision and recall values suggest that the model can be used effectively in real-time applications where timely intervention is necessary to retain customers, thus directly impacting the company’s bottom line.

* In conclusion, the stacking model stands out as the best-performing model for customer churn prediction in the telecom industry, offering a robust and reliable solution to help the company proactively manage churn and enhance customer retention strategies.

#### NEXT STEPS

1. Model Deployment:

* Integration with CRM Systems: Integrate the churn prediction model with the company's Customer Relationship Management (CRM) system to generate real-time churn predictions. This will enable the company to take proactive measures to retain high-risk customers.
* Automated Workflow: Create automated workflows for triggering alerts or action points based on churn predictions, such as offering retention campaigns, customer outreach, or personalized deals.

2. Monitor and Maintain the Model:

* Model Drift Monitoring: Set up a system to regularly monitor the model's performance over time and assess for model drift (changes in the data distribution). This can be done by retraining the model periodically using the most recent customer data.
* Performance Tracking: Implement a dashboard to track key performance metrics such as accuracy, recall, precision, and F1 score over time. This will allow you to track the effectiveness of churn retention efforts.

3. Exploring Advanced Models:

* Ensemble Methods: Explore advanced ensemble techniques, such as Boosting (e.g., XGBoost, LightGBM) or Bagging (e.g., Random Forest), to see if they can improve prediction accuracy or efficiency.
* Neural Networks: Consider experimenting with deep learning models (e.g., ANNs) for churn prediction if the dataset is large enough, as these models can capture highly non-linear relationships in the data.

4. Business Application and Strategy:

* Customer Retention Strategy: Work with the business team to define targeted customer retention strategies based on the model's predictions. This could involve personalized offers, loyalty programs, or proactive customer support interventions for high-risk customers.
* Cost-Benefit Analysis: Perform a cost-benefit analysis of churn reduction strategies (e.g., retention campaigns) based on the churn model’s predictions to determine the optimal investment in customer retention.

5. Customer Segmentation:

* Segment Analysis: Use the churn prediction model to create detailed customer segments based on churn likelihood, demographics, and behavior patterns. This will allow for more tailored retention efforts.
* Clustering: Explore clustering techniques (e.g., K-means, DBSCAN) to identify distinct groups of customers that behave similarly, helping to further refine retention strategies.

6. Data Expansion and Additional Features:

* More Data Sources: Explore incorporating additional data sources (e.g., customer feedback, usage patterns, social media sentiment) to enhance the model’s accuracy.
* Longitudinal Data: Incorporate longitudinal customer data to track behavior over time and better predict future churn behavior.

