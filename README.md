# Use Case Summary
## Objective Statement
<li>To get insight how many customers that churn and not churn.</li>
<li>To get insight whether customers that churn and not churn based on gender, senior citizen, have partner and dependents.</li>
<li>To get insight whether customers that churn and not churn based on how many customers use the services provided such as contract, phone service, multiple lines, internet service, online security, online backup, device protection, tech support, streaming tv, streaming movies, paperless billing and payment method.</li>
<li>To get insight whether customers that churn and not churn based on how many spending their money every month and total spending.</li>
<li>To get insight whether customers that churn and not churn based on how long their tenure.</li>
<li>Create modeling using Machine Learning to predict customers churn.</li>

## Challenges
<li>Large size of data, can not be maintained by excel spreadsheet.</li>
<li>Dataset have missing values and incorrect data type.</li>
<li>Don't understand the data stored in each column with the column name.</li>

## Methodology / Analytic Technique
<li>Descriptive Analysis: to find out information on current conditions based on the data that has been collected.</li>
<li>Graph Analysis: provide information from the graph.</li>
<li>Modelling : Machine Learning Classification.</li>

## Business Benefit
<li>Know how to treat customers based on their behavior.</li>
<li>Help the business team provide products or services based on the behavior of each customer.</li>

## Expected Outcome
<li>Know how many customers that churn and not churn.</li>
<li>Know how many customers that churn and not churn based on gender, senior citizen, have partner and dependents.</li>
<li>Know how many customers that churn and not churn based on contract, phone service, multiple lines, internet service, online security, online backup, device protection, tech support, streaming tv, streaming movies, paperless billing and payment method.</li>
<li>Know how many customers that churn and not churn based on spending their money every month and total spending.</li>
<li>Know how long customers that churn and not churn based on ong their tenure.</li>
<li>Create modeling using Machine Learning to predict customers churn.</li>
 
# Business Understanding
Telco Company is a company engaged in the information technology services, communications and telecommunications networks. Customer churn in telco company is one of the biggest problems in a company. Why? Because the cost of acquiring a new customer is way more expensive than retaining an existing one. Thus in this project has some business questions using the data telco :
<li>How many customers that churn and not churn ?</li>
<li>How many customers that churn and not churn based on gender, senior citizen, have partner and dependents ?</li>
<li>How many customers that churn and not churn based on contract, phone service, multiple lines, internet service, online security, online backup, device protection, tech support, streaming tv, streaming movies, paperless billing and payment method ?</li>
<li>How many customers that churn and not churn based on spending their money every month and total spending ?</li>
<li>How long customers that churn and not churn based on ong their tenure ?</li>
<li>How produce modeling using Machine Learning to predict customers churn ?</li>

# Data Understanding
## Source Data
Telco Customer Churn by International Business Machines Corporation (IBM) Sample Data Sets.
https://www.kaggle.com/datasets/blastchar/telco-customer-churn

## Data Dictionary
The dataset has 21 columns and 7043 rows.
<br>
<b>Demographic Information</b>
<li> CustomerID : Unique number for each customers. </li>
<li> Gender : Whether the client is a female or a male (Female, Male). </li>
<li> SeniorCitizen : Whether the client is a senior citizen or not (0, 1). </li>
<li> Partner : Whether the client has a partner or not (Yes, No). </li>
<li> Dependents : Whether the client has dependents or not (Yes, No). </li>
<li> Churn : Whether the customer churned or not (Yes, No). </li>
<br>
<b>Customer Account Information</b>
<li> Tenure : Number of months the customer has stayed with the company (Multiple different numeric values). </li>
<li> Contract : Indicates the customers current contract type (Month-to-Month, One year, Two year). </li>
<li> PaperlessBilling : Whether the client has paperless billing or not (Yes, No). </li>
<li> PaymentMethod : The customers payment method (Electronic check, Mailed check, * Bank transfer (automatic), Credit Card (automatic)). </li>
<li> MonthlyCharges : The amount charged to the customer monthly (Multiple different numeric values). </li>
<li> TotalChargess : The total amount charged to the customer (Multiple different numeric values). </li>
<br>
<b>Services Information</b>
<li> PhoneService : Whether the client has a phone service or not (Yes, No).</li> 
<li> MultipleLines : Whether the client has multiple lines or not (No phone service, No, Yes).</li> 
<li> InternetService : Whether the client is subscribed to Internet service with the company (DSL, Fiber, optic, No).</li> 
<li> OnlineSecurity : Whether the client has online security or not (No internet service, No, Yes).</li> 
<li> OnlineBackup : Whether the client has online backup or not (No internet service, No, Yes).</li> 
<li> DeviceProtection : Whether the client has device protection or not (No internet service, No, Yes).</li> 
<li> TechSupport : Whether the client has tech support or not (No internet service, No, Yes).</li> 
<li> StreamingTV : Whether the client has streaming TV or not (No internet service, No, Yes).</li> 
<li> StreamingMovies : Whether the client has streaming movies or not (No internet service, No, Yes).

# Data Preparation
<li> Programming Language : Python Version 3.9.12. </li>
<li> Libraries : Pandas, Numpy, Matplotlib, Seaborn, Sklearn, Imblearn. </li>

# Data Cleaning
<li> There are 14% row data that are null. Where data is null in the Gender, SeniorCitizen, Partner, Dependents, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV and StreamingMovies columns. All of these columns store categorical data so to handle it by filling in the empty rows with unknown label.</li> 
<li> Changed the data type from object to float in the TotalCharges column. There are 11 empty rows after changing the data type. To handle it must fill in the null rows with the median from the Total Charges column.</li> 
<li> Delete the customer id column because it is an identifier.</li> 

# Exploratory Data Analysis 

# Feature Engineering 

# Preprocessing Model 

# Modeling

# Evaluation

# Result 

# Recommendations


