# Introduction
### Problem Statement
This is a python exploratory data analysis and customer churn prediction project that I have completed as a part of my first semister Master's in Data Science.

The project explores the data of a fictional Tele communications company called Telco and its customers churn data that provided home phone and Internet service to 7,043 customers in California during the third quarter. It shows which customers have left, stayed or signed up for their services. Multiple important demographics are included for each customer, as well as a Satisfaction Score, Churn Score, and Customer Lifetime Value (CLTV) index.

For each of these data objects, there are 6 different files that I have uploaded to Google Drive to read data into the Google Cloud Colab Environment.

The project aims to use customer data like demographics, services opted by customers, and location of a customer to predict the possibility of churning out of a customer.

### Skills Used
In this exploratory data analysis and model prediction I'll be applying my knowledge and skills in:

* Python
  * Numpy
  * Pandas
  * Matplotlib
  * Seaborn
  * Scikit-Learn

# Data Sources

The Telco Chustomer churn data has 6 different files containing 7043 customers data of both running and churned out customers. The 6 different files and their data description is as follows:

## **Demographics**

1. **Customer ID:**
   - Unique identifier assigned to each customer.

2. **Count:**
   - Numeric count or frequency associated with each customer, possibly indicating the number of occurrences or transactions.

3. **Gender:**
   - Categorical variable indicating the gender of the customer (e.g., Male, Female).

4. **Age:**
   - Numeric variable representing the age of the customer.

5. **Under 30:**
   - Binary variable indicating whether the customer is under 30 years old (1 for Yes, 0 for No).

6. **Senior Citizen:**
   - Binary variable indicating whether the customer is a senior citizen (1 for Yes, 0 for No).

7. **Married:**
   - Binary variable indicating whether the customer is married (1 for Yes, 0 for No).

8. **Dependents:**
   - Binary variable indicating whether the customer has dependents (1 for Yes, 0 for No).

9. **Number of Dependents:**
   - Numeric variable representing the count of dependents associated with the customer.

This demographics data table appears to contain information about customers, including their unique identifier, gender, age, marital status, presence of dependents, and count-related variables. It's a mix of categorical and numerical features that could be used for analyzing customer demographics and behavior.

## **Location**

1. **Customer ID:**
   - Unique identifier assigned to each customer.

2. **Count:**
   - Numeric count or frequency associated with each customer, possibly indicating the number of occurrences or transactions.

3. **Country:**
   - Categorical variable indicating the country of residence for each customer.

4. **State:**
   - Categorical variable representing the state or region within the country where the customer resides.

5. **City:**
   - Categorical variable specifying the city of residence for each customer.

6. **Zip Code:**
   - Alphanumeric code representing the postal code or ZIP code associated with the customer's address.

7. **Lat Long (Latitude and Longitude):**
   - Geographic coordinates specifying the latitude and longitude of the customer's location.

8. **Latitude:**
   - Numeric variable indicating the latitude of the customer's location.

9. **Longitude:**
   - Numeric variable indicating the longitude of the customer's location.

This locations data table contains information about customers' geographical locations, including their country, state, city, ZIP code, and geographic coordinates (latitude and longitude). Additionally, it includes a unique identifier (Customer ID) and a count-related variable. This geographical information can be valuable for analyzing customer distribution, regional patterns, and location-based insights.

## **Population**

1. **ID:**
    Unique identifier assigned to each record in the population data table.

2. **Zip Code:**
    Alphanumeric code representing the postal code or ZIP code associated with a specific geographic area.

3. **Population:**
    Numeric variable indicating the population count associated with the corresponding ZIP code. This variable represents the number of residents or individuals in the specified geographic area.

This population data table appears to contain information about population counts in different ZIP codes or geographic areas. The combination of ID and Zip Code provides a unique identifier for each record, and the Population column holds the corresponding population count for each geographic area. This data can be valuable for demographic analysis, understanding population distribution, and related insights.

## **Services**

1. **Customer ID:** Unique identifier assigned to each customer.

2. **Count:** Numeric count or frequency associated with each customer, possibly indicating the number of occurrences or transactions.

3. **Quarter:** Categorical variable representing the quarter or time period during which the data was recorded.

4. **Referred a Friend:** Binary variable indicating whether the customer referred a friend (1 for Yes, 0 for No).

5. **Number of Referrals:** Numeric variable indicating the count of referrals made by the customer.

6. **Tenure in Months:** Numeric variable representing the duration of the customer's association with the service provider in months.

7. **Offer:** Categorical variable specifying the type of offer or plan subscribed to by the customer.

8. **Phone Service:** Binary variable indicating whether the customer has phone service (1 for Yes, 0 for No).

9. **Avg Monthly Long Distance Charges:** Numeric variable representing the average monthly long-distance charges incurred by the customer.

10. **Multiple Lines:** Binary variable indicating whether the customer has multiple phone lines (1 for Yes, 0 for No).

11. **Internet Service:** Binary variable indicating whether the customer has Internet Service (1 for Yes, 0 for No).

12. **Internet Type:** Categorical variable indicating the type of internet connection (e.g., DSL, Fiber).

13. **Avg Monthly GB Download:** Numeric variable representing the average monthly gigabytes of data downloaded by the customer.

14. **Online Security:** Binary variable indicating whether the customer has online security service (1 for True, 0 for False).

15. **Online Backup:** Binary variable indicating whether the customer has online backup service (1 for True, 0 for False).

16. **Device Protection Plan:** Binary variable indicating whether the customer has a device protection plan (1 for True, 0 for False).

17. **Premium Tech Support:** Binary variable indicating whether the customer has premium tech support service (1 for True, 0 for False).

18. **Streaming TV:** Binary variable indicating whether the customer has streaming TV service (1 for True, 0 for False).

19. **Streaming Movies:** Binary variable indicating whether the customer has streaming movies service (1 for True, 0 for False).

20. **Streaming Music:** Binary variable indicating whether the customer has streaming music service (1 for True, 0 for False).

21. **Unlimited Data:** Binary variable indicating whether the customer has unlimited data service (1 for True, 0 for False).

22. **Contract:** Categorical variable specifying the type of contract (e.g., month-to-month, one-year, two-year).

23. **Paperless Billing:** Binary variable indicating whether the customer has opted for paperless billing (1 for True, 0 for False).

24. **Payment Method:** Categorical variable specifying the customer's payment method.

25. **Monthly Charge:** Numeric variable representing the monthly charge incurred by the customer.

26. **Total Charges:** Numeric variable representing the total charges incurred by the customer.

27. **Total Refunds:** Numeric variable representing the total refund amount for the customer.

28. **Total Extra Data Charges:** Numeric variable representing the total extra data charges incurred by the customer.

29. **Total Long Distance Charges:** Numeric variable representing the total long-distance charges incurred by the customer.

30. **Total Revenue:** Numeric variable representing the total revenue generated from the customer, accounting for charges, refunds, and additional charges.

This service data table provides a comprehensive view of various aspects related to customer interactions, services subscribed, and financial transactions. The combination of categorical and numerical features allows for in-depth analysis of customer behavior and preferences.

## **Status**
1. **Customer ID:**
   - Unique identifier assigned to each customer.

2. **Count:**
   - Numeric count or frequency associated with each customer, possibly indicating the number of occurrences or transactions.

3. **Quarter:**
   - Categorical variable representing the quarter or time period during which the data was recorded.

4. **Satisfaction Score:**
   - Numeric variable representing the satisfaction score assigned to each customer.

5. **Customer Status:**
   - Categorical variable indicating the overall status of the customer (e.g., active, inactive).

6. **Churn Label:**
   - Categorical variable indicating whether the customer has churned (e.g., Yes, No).

7. **Churn Value:**
   - Binary variable indicating whether the customer has churned (1 for True, 0 for False).

8. **Churn Score:**
   - Numeric variable representing the churn score assigned to each customer.

9. **CLTV (Customer Lifetime Value):**
   - Numeric variable representing the predicted lifetime value of the customer.

10. **Churn Category:**
    - Categorical variable specifying the category of churn (e.g., voluntary, involuntary).

11. **Churn Reason:**
    - Categorical variable providing information about the reason for churn if applicable.

This status data table provides information about the status and churn-related metrics for each customer. It includes satisfaction scores, churn labels, churn scores, customer lifetime values, and reasons for churn. Analyzing this data can help in understanding customer satisfaction, predicting churn, and identifying factors contributing to customer attrition.

## Churn



1. **Customer ID:** Unique identifier assigned to each customer.

2. **Count:** Numeric count or frequency associated with each customer, possibly indicating the number of occurrences or transactions.

3. **Country:** Categorical variable indicating the country of residence for each customer.

4. **State:** Categorical variable representing the state or region within the country where the customer resides.

5. **City:** Categorical variable specifying the city of residence for each customer.

6. **Zip Code:** Alphanumeric code representing the postal code or ZIP code associated with the customer's address.

7. **Lat Long (Latitude and Longitude):** Geographic coordinates specifying the latitude and longitude of the customer's location.

8. **Latitude:** Numeric variable indicating the latitude of the customer's location.

9. **Longitude:** Numeric variable indicating the longitude of the customer's location.

10. **Gender:** Categorical variable indicating the gender of the customer (e.g., Male, Female).

11. **Senior Citizen:** Binary variable indicating whether the customer is a senior citizen (1 for Yes, 0 for No).

12. **Partner:** Binary variable indicating whether the customer is married (1 for Yes, 0 for No).

13. **Dependents:** Binary variable indicating whether the customer has dependents (1 for Yes, 0 for No).

14. **Tenure in Months:** Numeric variable representing the duration of the customer's association with the service provider in months.

15. **Phone Service:** Binary variable indicating whether the customer has phone service (1 for Yes, 0 for No).

16. **Multiple Lines:** Binary variable indicating whether the customer has multiple phone lines (1 for Yes, 0 for No).

17. **Online Security:** Binary variable indicating whether the customer has online security service (1 for True, 0 for False).

18. **Online Backup:** Binary variable indicating whether the customer has online backup service (1 for True, 0 for False).

19. **Device Protection Plan:** Binary variable indicating whether the customer has a device protection plan (1 for True, 0 for False).

20. Tech Support:** Binary variable indicating whether the customer has premium tech support service (1 for True, 0 for False).

21. **Streaming TV:** Binary variable indicating whether the customer has streaming TV service (1 for True, 0 for False).

22. **Streaming Movies:** Binary variable indicating whether the customer has streaming movies service (1 for True, 0 for False).

23. **Contract:** Categorical variable specifying the type of contract (e.g., month-to-month, one-year, two-year).

24. **Paperless Billing:** Binary variable indicating whether the customer has opted for paperless billing (1 for True, 0 for False).

25. **Payment Method:** Categorical variable specifying the customer's payment method.

26. **Monthly Charge:** Numeric variable representing the monthly charge incurred by the customer.

27. **Churn Label:** Categorical variable indicating whether the customer has churned (e.g., Yes, No).

28. **Churn Value:** Binary variable indicating whether the customer has churned (1 for True, 0 for False).

29. **Churn Score:** Numeric variable representing the churn score assigned to each customer.

30. **CLTV (Customer Lifetime Value):** Numeric variable representing the predicted lifetime value of the customer.

### Summary of EDA

After exploratory data analysis. lets look at some of the interesting findings.

1. Out of all the customers there are only 16.2% of the customers who are senior citizens.

2. The customers who are of age above 30 and have churned out are more than the customers who are of age below 30 and are still under subscription.

3. The customers who have churned out doesn't have more dependents as customers who are still under subscription.

4. Different locations have topped in both with customers who have churned and with customer who are still under subscriptions.

5. The customers who are still continuing the subscription have given more referals.

6. The customers who haven't churned whould obviously have more tenure in their subscription plan.

7. Offer B and Offer E are the offers that have been more opted by the Customers.

8. The customers who are using phone service have churned out more.

9. The customers who have opted for internet service are also churned out more.

10. Most of the customers who have churned out are using Banking withdrawl as their payment method.

11. Most of the customers who have churned out doesn't have any premium tech support for their subscription.

12. The churn score is more for the customer who have churned out.

# Feature Engineering

After the exploratory analysis, these are the columns/features from all the tables that need to be fit into a model for classifying whether the customer will churn out or not.

1. Under 30 - Binary Variable
2. Dependents - Binary Variable
3. Number of Dependents - Numerical Variable
4. City - Categorical Variable
5. Number of referrals - Numerical Variable
6. Tenure in months - Numerical Variable
7. Offer - Categorical Variable
8. Phone service - Binary Variable
9. Internet Service - Binary Variable
10. Premium Tech Support - Binary Variable
11. Payment Method - Categorical Variable
12. CLTV - Numerical Variable



After applying the logistic regression model for classifying the training the data below are models metrics....


1. Accuracy: 0.7928
The model correctly predicted the class of approximately 79.28% of instances in the dataset.

2. Precision: 0.6598
Out of the instances predicted as positive, around 65.98% were actually true positives. This metric emphasizes the accuracy of positive predictions.

3. Recall: 0.5575
The model captured approximately 55.75% of all actual positive instances. This metric emphasizes the ability of the model to find all positive instances.

4. F1 Score: 0.6043
The F1 score is approximately 60.43%, indicating a balanced performance between precision and recall. A higher F1 score is desirable, especially when precision and recall are equally important.

5. ROC AUC: 1.0000
An ROC AUC of 1.0000 indicates perfect discrimination between classes. The model has a flawless ability to separate positive and negative instances.

Confusion Matrix:
True Positives (TP): 223 instances were correctly predicted as positive.
True Negatives (TN): 894 instances were correctly predicted as negative.
False Positives (FP): 115 instances were incorrectly predicted as positive.
False Negatives (FN): 177 instances were incorrectly predicted as negative.

In summary, the model has a high overall accuracy, decent precision, recall, and F1 score. The perfect ROC AUC suggests excellent discrimination capability. The confusion matrix provides a detailed breakdown of correct and incorrect predictions, which can be useful for understanding the model's performance in different aspects.

