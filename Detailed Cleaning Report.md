# Detailed Cleaning Report

## 1. CREATE TABLE
I began by creating a table in MySQL called 'credit_customers' in a database I already had. I created the table by taking the following actions
- In the 'Schemas' panel on the left hand side, right click 'Tables' and select 'Table Import Wizard'.
- I selected the csv file I had downloaded from Kaggle.
- Select 'create a new table'.
- Unselect the last 2 columns since we don't need them for the project.
- Finished.

## 2. NULL VALUES
```
SELECT *
FROM credit_customers AS cc
WHERE CLIENTNUM IS NULL
OR Attrition_Flag IS NULL
OR Customer_Age IS NULL
OR Gender IS NULL
OR Dependent_count IS NULL
OR Education_Level IS NULL
OR Marital_Status IS NULL
OR Income_Category IS NULL
OR Card_Category IS NULL
OR Months_on_book IS NULL
OR Total_Relationship_Count IS NULL
OR Months_Inactive_12_mon IS NULL
OR Contacts_Count_12_mon IS NULL
OR Credit_Limit IS NULL
OR Total_Revolving_Bal IS NULL
OR Avg_Open_To_Buy IS NULL
OR Total_Amt_Chng_Q4_Q1 IS NULL
OR Total_Trans_Amt IS NULL
OR Total_Trans_Ct IS NULL
OR Total_Ct_Chng_Q4_Q1 IS NULL
OR Avg_Utilization_Ratio IS NULL
```
No ```NULL``` values were found.

## DUPLICATES
```

```
