### **THE CHURN FACTOR: UNLOCKING CUSTOMER ROYALTY IN TELECOM**

#### BUSINESS UNDERSTANDING

Understanding telecom customer churn is crucial for businesses in the telecommunications industry, as it directly impacts revenue, customer retention, and overall profitability. Customer churn can be voluntary because of dissatisfaction in the services by the service provider and it can also be involuntary because of service disruption or payment issues. Understanding customer churn rates can have financial implications to the provider. Maintaining current customers is cheaper than that acquiring new ones. Analysing churn rates can give an advantage over competitors. This project aims to predict whether a customer will churn or not depending on the several factors on the datasets.

#### DATA UNDERSTANDING

This SyriaTel data is from https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset, a Telecommunication company. The dataset contains information about customer churn, which is a significant problem for telecom companies. The goal is to predict whether a customer will churn or not. The dataset contains the following columns:'state', 'account length', 'area code', 'phone number','international plan', 'voice mail plan', 'number vmail messages','total day minutes', 'total day calls', 'total day charge','total eve minutes', 'total eve calls', 'total eve charge','total night minutes', 'total night calls', 'total night charge','total intl minutes', 'total intl calls', 'total intl charge','customer service calls', 'churn'

**Data Visualization**
The dataset is visualized using the following plots:
1. Churn Distribution

![alt text](image.png)
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

**Data Preparation**
1. Data Cleaning where all missing values were handled and duplicates were dropped.
2. Data Transformation where all categorical variables were converted to numerical variables using one-hot encoding.
3. Feature Scaling where all numerical variables were scaled using StandardScaler from scikit-learn library.
4. Splitting the dataset into training and testing sets using train_test_split function from scikit-learn library.

**Modelling**
Three different models were used inorder to compare which one has the best accuracy scores and recall precision balance.
The models used were:
1. Logistic regression which was the baseline model: 
2. Decision tree
3. Random Forest Classifier.

**Model Evaluation**
The models were evaluated using the following metrics: accuracy, precision, recall, F1 score, and ROC-AUC score.
1. Logistic regression model: Accuracy: 0.859, Recall was 0.138 and the Precision was 0.666. There was no balance between recall and precision meaning that the model was struggling to detect positive cases correctly. Further tuning was done, using gridsearchCV and the results were as follows: Accuracy (0.864): This means that about 86.4% of the predictions made by the model are correct. However, accuracy alone can be misleading, especially if the classes are imbalanced.
Precision (0.639): The precision score indicates that when the model predicts the positive class, it is correct 63.9% of the time. This suggests that there are still some false positives in the model's predictions.
Recall (0.228): The recall score is quite low, at 22.8%. This implies that the model is not capturing a large portion of the actual positive cases, resulting in many false negatives.
F1-score (0.336): The F1-score, which balances precision and recall, is relatively low. This further indicates that the model is struggling to achieve a good balance between precision and recall.
2. Decision Tree: The evaluation metrics for the Decision Tree model indicate the following:
Accuracy (0.9805): The model correctly classified 98.05% of the samples in the test set. This indicates a high overall performance.
Precision (1.0000): The model achieved a perfect precision score, meaning all instances predicted as positive were indeed positive. There were no false positives.
Recall (0.8713): The recall score of 87.13% indicates that out of all actual positive cases, the model correctly identified 87.13%. There were some false negatives (13), meaning the model missed a few positive cases.
F1-score (0.9312): This score combines precision and recall into a single metric. A value of 0.9312 suggests a good balance between precision and recall.
3. Random Forest Classifier: The model performs well in predicting non-churning customers, with high precision, recall, and F1-score.
However, it struggles to identify churning customers, with a recall of only 0.50. This means that half of the actual churning customers are missed by the model.
To improve the model, techniques such as adjusting class weights, using a different threshold for classification, or employing resampling methods (e.g., SMOTE) could help address the imbalance and improve the recall for the "True" class.


#### NEXT STEPS:
1. Feature importance and Interpretation 
2. Model Deployment
3. Model Maintenance and Updates
4. Hyperparameter Tuning
5. Model Evaluation, Comparison, Model Selection and Ensemble Methods
6. Model Explainability and Transparency

