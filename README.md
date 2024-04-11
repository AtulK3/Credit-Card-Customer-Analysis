# Credit-Card-Customer-Analysis

**Credit Card Customer Churn Prediction**

_____________________________________________________________________________________________________________________________________________
In this repository, I do machine learning modeling that can later be used to predict customer churn on credit card services. Here I use the bankchurn.csv dataset obtained from Kaggle. The case in this dataset is a binary classification with an unbalanced proportion of target variables, namely 16.1% for the negative class and the rest for the positive class. In this dataset there are several features that are used as parameters to make predictions, including:
•	CLIENTNUM: customer account number.
•	Attrition_Flag: customer status (Existing and Attrited).
•	Customer_Age: age of the customer.
•	Gender: gender of customer (M for male and F for female).
•	Dependent_count: number of dependents of customers.
•	Education_Level: customer education level (Uneducated, High School, Graduate, College, Post-Graduate, Doctorate, and Unknown).
•	Marital_Status: customer's marital status (Single, Married, Divorced, and Unknown).
•	Income_Category: customer income interval category (Less than $40K, $40K-$60k, $60K-$80K, $80K-$120K, $120K +, and Unknown).
•	Card_Category: type of card used (Blue, Silver, Gold, and Platinum).
•	Months_on_Book: period of being a customer (in months).
•	Total_Relationship_Count: the number of products used by customers in the bank.
•	Months_Inactive_12_mon: period of inactivity for the last 12 months.
•	Contacts_Count_12_mon: the number of interactions between the bank and the customer in the last 12 months.
•	Credit_Limit: credit card transaction nominal limit in one period.
•	Total_Revolving_Bal: total funds used in one period.
•	Avg_Open_To_Buy: the difference between the credit limit set for the cardholder's account and the current balance.
•	Total_Amt_Chng_Q4_Q1: increase in customer transaction nominal between quarter 4 and quarter 1.
•	Total_Trans_Amt: total nominal transaction in the last 12 months.
•	Total_Trans_Ct: the number of transactions in the last 12 months.
•	Total_Ct_Chng_Q4_Q1: the number of customer transactions increased between quarter 4 and quarter 1.
•	Avg_Utilization_Ratio: percentage of credit card usage.
___________________________________________________________________________________________________________________________________________________________________________

**STEP-that I have performed here **

In the initial phase of the analysis, I conducted Exploratory Data Analysis (EDA) using various statistical methods and visualizations. This included checks for data validity, duplicates, and missing values, which revealed no significant issues. However, upon closer examination, disparities in data scale among features were observed, indicating variations in the range of values across different features.

Furthermore, the presence of outliers in certain features was identified through boxplot visualization, highlighting potential anomalies in the dataset. Additionally, abnormal data distributions were observed in some features, warranting further investigation.

Notably, a strong correlation was observed between certain features, particularly between "Credit_Limit" and "Average_Open_to_Buy," indicating a potential redundancy or dependency between these variables.

In these stage find out the descriptive statistics for the variable as well as used the chi-squared testfor finding the relationship between the categorical variables.

Also did the Vizualization of the data for continuous as well as for categorical features to find out the patterns in the data.

**STEP II**

The next step I took was Data Preprocessing with reference to the findings that I got in the Exploratory Data Analysis stage, the steps I took were as follows:

**Data Scaling:**

After examining the data, I found that some features have unusual distributions. To address this, I standardized normally distributed features like Customer_Age, Months_on_Book, Total_Trans_Ct, and Total_Ct_Chng_Q4_Q1. Additionally, I normalized features that weren't normally distributed. Scaling data also helps handle outliers in the features.

**Categorical Encoding:**

Next, I converted categorical features into numerical ones because machine learning models can't understand categorical data. I used two techniques: Label Encoding for features with an ordinal measurement scale and One Hot Encoding for features with a nominal measurement scale.

**Splitting Data into Training and Testing Sets:**

I split the dataset into training and testing sets, allocating 80% for training and 20% for testing. The training data is used to train the model, while the testing data is used to evaluate its performance.

**Dataset Balancing:**

In this dataset, there's an imbalance between the classes of the dependent variable (Existing Customers and Attributed Customers). This can affect the model's ability to predict customer status accurately. To address this, I balanced the classes using the SMOTE technique. Unlike other techniques, SMOTE adds data to the minority class based on the closest neighbors of the data points, resulting in a more varied dataset without reducing information.

**STEP- III**
In this analysis, I've utilized k-means clustering to segment the data based on its features.

Segmentation Model: I Used clustering techniques ( K-Means) to segment the customers based on their credit card usage and demographic data. Also using elbow method Determine the optimal number of clusters.

**STEP-IV**
In the final step, I used two different algorithms for modeling: Logistic Regression and Random Forest Classifier.

For the Logistic Regression model, it correctly predicted 244 cases of Existing Customers and 134 cases of Attributed Customers, but it also made 448 prediction errors. Overall, the model achieved an Accuracy score of 77%, a Precision score of 67%, and a Recall score of 76%.

On the other hand, the Random Forest Classifier model correctly predicted 272 cases of Existing Customers and 1,664 cases of Attributed Customers, with only 90 prediction errors. This model performed even better, achieving an Accuracy score of 95.51%, a Precision score of 92%, and a Recall score of 90%.

Considering the performance of both models, it's evident that the Random Forest model outperforms the Logistic Regression model for this dataset.



 

