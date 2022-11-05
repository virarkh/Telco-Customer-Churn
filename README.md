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
- TotalChargess : The total amount charged to the customer (Multiple different numeric values).

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

# Feature Engineering 

# Preprocessing Model 

# Modeling

# Evaluation

# Result 

# Recommendations


