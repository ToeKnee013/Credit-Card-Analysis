# Data Cleaning

```
# Checking for Null Values
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

# Checking for Duplicates
SELECT CLIENTNUM,
       COUNT(CLIENTNUM),
       Attrition_Flag,
       COUNT(Attrition_Flag),
       Customer_Age,
       COUNT(Customer_Age),
       Gender,
       COUNT(Gender),
       Dependent_count,
       COUNT(Dependent_count),
       Education_Level,
       COUNT(Education_Level),
       Marital_Status,
       COUNT(Marital_Status),
       Income_Category,
       COUNT(Income_Category),
       Card_Category,
       COUNT(Card_Category),
       Months_on_book,
       COUNT(Months_on_book),
       Total_Relationship_Count,
       COUNT(Total_Relationship_Count),
       Months_Inactive_12_mon,
       COUNT(Months_Inactive_12_mon),
       Contacts_Count_12_mon,
       COUNT(Contacts_Count_12_mon),
       Credit_Limit,
       COUNT(Credit_Limit),
       Total_Revolving_Bal,
       COUNT(Total_Revolving_Bal),
       Avg_Open_To_Buy,
       COUNT(Avg_Open_To_Buy),
       Total_Amt_Chng_Q4_Q1,
       COUNT(Total_Amt_Chng_Q4_Q1),
       Total_Trans_Amt,
       COUNT(Total_Trans_Amt),
       Total_Trans_Ct,
       COUNT(Total_Trans_Ct),
       Total_Ct_Chng_Q4_Q1,
       COUNT(Total_Ct_Chng_Q4_Q1),
       Avg_Utilization_Ratio,
       COUNT(Avg_Utilization_Ratio)
FROM credit_customers AS cc
GROUP BY CLIENTNUM,
         Attrition_Flag,
         Customer_Age,
         Gender,
         Dependent_count,
         Education_Level,
         Marital_Status,
         Income_Category,
         Card_Category,
         Months_on_book,
         Total_Relationship_Count,
         Months_Inactive_12_mon,
         Contacts_Count_12_mon,
         Credit_Limit,
         Total_Revolving_Bal,
         Avg_Open_To_Buy,
         Total_Amt_Chng_Q4_Q1,
         Total_Trans_Amt,
         Total_Trans_Ct,
         Total_Ct_Chng_Q4_Q1,
         Avg_Utilization_Ratio
HAVING (COUNT(CLIENTNUM) > 1)
AND (COUNT(Attrition_Flag) > 1)
AND (COUNT(Customer_Age) > 1)
AND (COUNT(Gender) > 1)
AND (COUNT(Dependent_count) > 1)
AND (COUNT(Education_Level) > 1)
AND (COUNT(Marital_Status) > 1)
AND (COUNT(Income_Category) > 1)
AND (COUNT(Card_Category) > 1)
AND (COUNT(Months_on_book) > 1)
AND (COUNT(Total_Relationship_Count) > 1)
AND (COUNT(Months_Inactive_12_mon) > 1)
AND (COUNT(Contacts_Count_12_mon) > 1)
AND (COUNT(Credit_Limit) > 1)
AND (COUNT(Total_Revolving_Bal) > 1)
AND (COUNT(Avg_Open_To_Buy) > 1)
AND (COUNT(Total_Amt_Chng_Q4_Q1) > 1)
AND (COUNT(Total_Trans_Amt) > 1)
AND (COUNT(Total_Trans_Ct) > 1)
AND (COUNT(Total_Ct_Chng_Q4_Q1) > 1)
AND (COUNT(Avg_Utilization_Ratio) > 1)

```
