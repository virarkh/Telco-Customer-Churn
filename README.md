# Use Case Summary
## Objective Statement
- To get insight how many customers that churn and not churn.
- To get insight whether customers that churn and not churn based on gender, senior citizen, have partner and dependents.
- To get insight whether customers that churn and not churn based on how many customers use the services provided such as contract, phone service, multiple lines, internet service, online security, online backup, device protection, tech support, streaming tv, streaming movies, paperless billing and payment method.
- To get insight whether customers that churn and not churn based on how many spending their money every month and total spending.
- To get insight whether customers that churn and not churn based on how long their tenure.
- Create modeling using Machine Learning to predict customers churn.

## Challenges
- Large size of data, can not be maintained by excel spreadsheet.
- Dataset have missing values and incorrect data type.
- Don't understand the data stored in each column with the column name.

## Methodology / Analytic Technique
- Descriptive Analysis: to find out information on current conditions based on the data that has been collected.
- Graph Analysis: provide information from the graph.
- Modelling : Machine Learning Classification.

## Business Benefit
- Know how to treat customers based on their behavior.
- Help the business team provide products or services based on the behavior of each customer.

## Expected Outcome
- Know how many customers that churn and not churn.
- Know how many customers that churn and not churn based on gender, senior citizen, have partner and dependents.
- Know how many customers that churn and not churn based on contract, phone service, multiple lines, internet service, online security, online backup, device protection, tech support, streaming tv, streaming movies, paperless billing and payment method.
- Know how many customers that churn and not churn based on spending their money every month and total spending.
- Know how long customers that churn and not churn based on ong their tenure.
- Create modeling using Machine Learning to predict customers churn.
 
# Business Understanding
Telco Company is a company engaged in the information technology services, communications and telecommunications networks. Customer churn in telco company is one of the biggest problems in a company. Why? Because the cost of acquiring a new customer is way more expensive than retaining an existing one. Thus in this project has some business questions using the data telco :
- How many customers that churn and not churn ?
- How many customers that churn and not churn based on gender, senior citizen, have partner and dependents ?
- How many customers that churn and not churn based on contract, phone service, multiple lines, internet service, online security, online backup, device protection, tech support, streaming tv, streaming movies, paperless billing and payment method ?
- How many customers that churn and not churn based on spending their money every month and total spending ?
- How long customers that churn and not churn based on ong their tenure ?
- How produce modeling using Machine Learning to predict customers churn ?

# Data Understanding
## Source Data
Telco Customer Churn by International Business Machines Corporation (IBM) Sample Data Sets.
https://www.kaggle.com/datasets/blastchar/telco-customer-churn

## Data Dictionary
The dataset has 21 columns and 7043 rows.

**Demographic Information**
- CustomerID : Unique number for each customers.
- Gender : Whether the client is a female or a male (Female, Male).
- SeniorCitizen : Whether the client is a senior citizen or not (0, 1).
- Partner : Whether the client has a partner or not (Yes, No).
- Dependents : Whether the client has dependents or not (Yes, No).
- Churn : Whether the customer churned or not (Yes, No).

**Customer Account Information**
- Tenure : Number of months the customer has stayed with the company (Multiple different numeric values).
- Contract : Indicates the customers current contract type (Month-to-Month, One year, Two year).
- PaperlessBilling : Whether the client has paperless billing or not (Yes, No).
- PaymentMethod : The customers payment method (Electronic check, Mailed check, Bank transfer (automatic), Credit Card (automatic)).
- MonthlyCharges : The amount charged to the customer monthly (Multiple different numeric values).
- TotalCharges : The total amount charged to the customer (Multiple different numeric values).

**Services Information**
- PhoneService : Whether the client has a phone service or not (Yes, No).
- MultipleLines : Whether the client has multiple lines or not (No phone service, No, Yes).
- InternetService : Whether the client is subscribed to Internet service with the company (DSL, Fiber, optic, No).
- OnlineSecurity : Whether the client has online security or not (No internet service, No, Yes).
- OnlineBackup : Whether the client has online backup or not (No internet service, No, Yes).
- DeviceProtection : Whether the client has device protection or not (No internet service, No, Yes).
- TechSupport : Whether the client has tech support or not (No internet service, No, Yes).
- StreamingTV : Whether the client has streaming TV or not (No internet service, No, Yes).
- StreamingMovies : Whether the client has streaming movies or not (No internet service, No, Yes).

# Data Preparation
- Programming Language : Python Version 3.9.12. 
- Libraries : Pandas, Numpy, Matplotlib, Seaborn, Sklearn, Imblearn.

# Data Cleaning
- There are 14% row data that are null. Where data is null in the Gender, SeniorCitizen, Partner, Dependents, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV and StreamingMovies columns. All of these columns store categorical data so to handle it by filling in the empty rows with unknown label.
- Changed the data type from object to float in the TotalCharges column. There are 11 empty rows after changing the data type. To handle it must fill in the null rows with the median from the Total Charges column.
- Delete the customer id column because it is an identifier. 

# Exploratory Data Analysis 
**Know how many customers that churn and not churn.**

![image](https://user-images.githubusercontent.com/50388300/200106517-bfdc71a3-187d-4b8e-9c8f-810c0181a7fc.png)

From the chart above, can be seen that most customers are non-churn. From 7043 customers, 73.4% are non-churn with 5174 customer and 26.6% are churn with 1869 customer.

**Know how many customers that churn and not churn based on gender, senior citizen, have partner and dependents.**

![image](https://user-images.githubusercontent.com/50388300/200106590-9951bd7b-b5d7-435d-9c0e-c1b088f73d31.png)

  * From the chart above, can be seen that most customers by gender are male.
  * From 7043 customers, 43.2% are male, 42.5% are female and 14.3% are customers who are not known male or female.
  * For customers who churn by gender for male 43.1%, female 42.9% and unknown gender the customer 14%.
  * Then for customers who not churn by gender, 43.3% are male, 42.3% female and the unknown gender the customers 14%.
  
![image](https://user-images.githubusercontent.com/50388300/200106614-088d4525-86b7-42d8-aef1-f3a2ae09b5dd.png)

  * From the chart above It can be seen that non-churn customers are dominated by non-senior citizens with 74.6% and 26.4% senior citizens.
  * From 7K customers, about 71.8% are not senior citizens, around 13.9% customers are senior citizens and 14.3% is not known whether they are senior citizens or not.
  * The total churn of not senior citizens is only around 1.1K or 16.9% of customers, but the total churn from senior citizens is almost half of the total senior citizens.
 
# Feature Engineering 
- Changes data categorical using hot end coding 
- Changes data ordinal using map for ordinal data
- Changes data numeric using min max scaler

# Preprocessing Model 
### Feature Selection
- We drop TotalCharges column because it contains multicolinear.
### Feature Important

![download](https://user-images.githubusercontent.com/113870155/200101977-7706d28a-66a4-4b2f-9c84-43d3c800b65a.png)

 - From the chart above we can see the top 10 feature that affect the model most. There are tenure, MonthlyCharges, Contract, PaymentMethod_Electronic check, OnlineSecurity_No, TechSupport_No, InternetService_Fiber optic, gender_Female, gender_Male, and OnlineBackup_No.
 
# Modeling Data : Logistic Regression
- Logistic Regression is a classification technique used in machine learning. It uses a logistic function to model the dependent variable. The dependent variable is dichotomous in nature, in this case is customer who churn or not. We are using deafult threshold in this model to classify the churn customer and not churn customer.
## Building a Model with Cross Validation
- Cross-Validation is a statistical method of evaluating and comparing learning algorithms by dividing data into two segments: one used to learn or train a model and the other used to validate the model.
## Hyperparameter Tuning in Logistic Regression
- Hyperparameter tuning consists of finding a set of optimal hyperparameter values for a learning algorithm while applying this optimized algorithm to any data set. That combination of hyperparameters maximizes the model's performance, minimizing a predefined loss function to produce better results with fewer errors.

## Oversampling with SMOTE
- SMOTE is an oversampling technique where the synthetic samples are generated for the minority class. It focuses on the feature space to generate new instances with the help of interpolation between the positive instances that like together.

# Evaluation
## Evaluation : Confusion Matrix
- A confusion matrix is a technique for summarizing the performance of a classification algorithm.
- Classification accuracy alone can be misleading if you have an unequal number of observations in each class or if you have more than two classes in your dataset.
- Calculating a confusion matrix can give you a better idea of what your classification model is getting right and what types of errors it is making.

![Capture](https://user-images.githubusercontent.com/113870155/200102051-1174a953-41ba-4110-8e02-4ccc17a69a3c.PNG)

### Classification Report
- From the table above we can see the precision for churn variable is 0.86 and not_churn variable is 0.69
- From the table above we can see the recall for churn variable is 0.91 and not_churn variable is 0.59
- From the table above we can  see the f1- score for churn variable is 0.88 and not_churn variable is 0.64
- From the table above we can see the accuracy for this model 0.82
### Confusion Matrix
There are 4 category in this matrix:
- True Positive, the number of true positive is 939
- True Negative, the number of true negative is 220
- False Negative, the number of false negative is 97
- False Positive, the number of false positive is 153
## AUC & RUC
- AUC - ROC curve is a performance measurement for the classification problems at various threshold settings. ROC is a probability curve and AUC represents the degree or measure of separability. It tells how much the model is capable of distinguishing between classes. Higher the AUC, the better the model is at predicting 0 classes as 0 and 1 classes as 1.

![download](https://user-images.githubusercontent.com/113870155/200102180-77dce475-cc55-4b41-8d37-b01625b3b145.png)

## Confusion Matrix with Hyperparameter Tuning Model

![Capture](https://user-images.githubusercontent.com/113870155/200102326-fdbf4d4e-3a46-4e52-bb98-abb7e0100ba5.PNG)

### Classification Report
- From the table above we can see the precision for churn variable is 0.86 and not_churn variable is 0.70
- From the table above we can see the recall for churn variable is 0.91 and not_churn variable is 0.59
- From the table above we can  see the f1- score for churn variable is 0.88 and not_churn variable is 0.64
- From the table above we can see the accuracy for this model 0.82
### Confusion Matrix
There are 4 category in this matrix:
- True Positive, the number of true positive is 940
- True Negative, the number of true negative is 220
- False Negative, the number of false negative is 96
- False Positive, the number of false positive is 153

## Confusion Matrix with SMOTE oversampling

![Capture](https://user-images.githubusercontent.com/113870155/200102445-43c93797-5f52-455e-a67e-8d85b49bdff2.PNG)

### Classification Report
- From the table above we can see the precision for churn variable is 0.89 and not_churn variable is 0.60
- From the table above we can see the recall for churn variable is 0.83 and not_churn variable is 0.71
- From the table above we can  see the f1- score for churn variable is 0.86 and not_churn variable is 0.65
- From the table above we can see the accuracy for this model 0.80
### Confusion Matrix
There are 4 category in this matrix:
- True Positive, the number of true positive is 863
- True Negative, the number of true negative is 263
- False Negative, the number of false negative is 173
- False Positive, the number of false positive is 110

# Results
- **How many customers that churn and not churn ?**
  * From 7043 customers, 73.46% are non-churn with 5174 customer and 26.6% are churn with 1869 customer.<br>
- **How many customers that churn and not churn based on gender, senior citizen, have partner and dependents ?**
  * Customers who churn by gender for male 43.1%, female 42.9% and unknown gender the customer 14%. Then for customers who not churn by gender, 43.3% are male, 42.3% female and the unknown gender the customers 14%.<br>
- **How many customers that churn and not churn based on contract, phone service, multiple lines, internet service, online security, online backup, device protection, tech support, streaming tv, streaming movies, paperless billing and payment method  ?**
  * Customers who churn by phone services, 90.9% using phone services and 9.1% not using phone services. Then customers who not churn by phone services, 90.1% using phone services and 9.9% not using phone services.<br>
- **How many customers that churn and not churn based on spending their money every month and total spending ?**
  * The churn customer highest density is above 0.0175 in the high range of monthly charges amount. The non-churn customer monthly charges density peak the highest at the lower amount and medium density at the mid to high amount. The churn customer monthly charges amount density peak at middle to high amount but low density at low amount.<br>
- **How long customers that churn and not churn based on ong their tenure ?**
  * Customers who churn from the long of tenure from 0 - 20 months with the highest density above 0.040.
  * Customers who not churn from the long of tenure from 60 - 80 months with the highest density above 0.015
- **How produce modeling using Machine Learning to predict customers churn ?**
  * To produce modeling using machine learning can use Logistic Regression. Logistic Regression is a classification technique used in machine learning. It uses a logistic function to model the dependent variable. The dependent variable is dichotomous in nature, in this case is customer who churn or not. We are using deafult threshold in this model to classify the churn customer and not churn customer.

# Recommendations
- For customer churn : maintain loyal customers by providing more economical prices and adjusting to the services they usually use.
- For customer by gender : Provide attractive services to customers who are differentiated by gender.
- For customers by senior citizens : The business team can increase the promotion by targeting young-adult citizens or non-senior citizens as their priority segment.
- For subscribers with streaming tv and streaming movies: offering bundling subscriptions for streaming tv and streaming movies at the same time with more economical price.
- For customer by internet service: improve internet service for fiber optic.
- For monthly charges : Therefore the team can make loyalty points for every purchase, so customer that purchase can change their points into some reward, so the customer who have points can change it into some rewards just like 1 month free or something else.
- For total charges : Therefore the team can make loyalty level based on total purchase, so customer who have reached some amount can go up to the next level with different benefit in each level.

