# practicalapp17.1# Practical-App-3
# Link to the complete Python Notebook
   Dive into a comprehensive Python notebook [https://github.com/HariHebb/practicalapp17.1/blob/main/prompt_III.ipynb] showcasing exploratory data analysis and baseline model generation! Explore multiple classification models tested for accuracy, recall, precision, and F1 score, alongside a detailed comparison of their performance and training time.

# Objective
Leveraging a UCI dataset on Portuguese bank marketing campaigns [https://archive.ics.uci.edu/dataset/222/bank+marketing], we aim to predict term deposit subscriptions. This project explores Logistic Regression, KNN, Decision Trees, and SVM to determine the best model based on accuracy, recall, precision, F1 score, and training time, ultimately identifying top performer(s) and justifying our selection.

# EDA Summary
 ## Dataset Overview:
   Size: 41,118 rows and 21 columns.
   Data Quality: No NULL values, but "unknown" and "non-existent" values indicate missing data points.
   Pseudo-Null Values: Predominantly found in "poutcome" (previous campaign outcome) and "default" (credit default status) columns.

## Categorical Column Insights:
    ### Plots
   ![image](https://github.com/user-attachments/assets/88361d4f-2ff1-4bac-a9c9-29b558e7be83)
   ![image](https://github.com/user-attachments/assets/c9d921e4-0690-485c-bd14-38f734fa1084)
   ![image](https://github.com/user-attachments/assets/d1b56ace-37a4-47ec-bfa6-46998be2d14d)
   ![image](https://github.com/user-attachments/assets/e22b2cef-ed53-4995-a0cc-7c617f7e776a)
   ![image](https://github.com/user-attachments/assets/5d1a7914-fe96-4648-86b5-de4b68e9ddb9)
   ![image](https://github.com/user-attachments/assets/d57f14ca-43bb-4380-83d9-04ea37fd9022)
   #### Seasonal Bias: Data lacks January and February data; sparse in winter months of October, November and December.
   #### Education Dominance: College/University degrees are most common education pattern among the cohort.
   #### Target Imbalance: "No" dominates "Yes" in the target column.
   #### Loan Bias: The cohort contains a small percentage of folks with housing or personal loans.
   #### Contact Methods: Primarily cellular, first-time contacts.
   #### Previous Campaigns: Mostly non-subscribers.
   #### Job Bias: Admin jobs dominate the list
   #### Marital Status: A large percentage of cohort are married
   ### Inferences
      The data is overall imbalanced based on observations of various attributes as can be inferred from the above output
  

## Numerical Colum Insights
 No huge correlation between most features and the target variable 
 ![image](https://github.com/user-attachments/assets/95ac3934-b051-4c44-a056-95cb3fb1548a)
 ![image](https://github.com/user-attachments/assets/d1a62b10-2722-4559-830f-3b014a816c33)
 ![image](https://github.com/user-attachments/assets/50a0731d-1338-4d2b-a77a-29e6cac3ddcc)
 ### Inferences
   The following columns have a significant impact on whether a client subscribes to a term deposit, with an influence between 0.23 and 0.35 on the target column:
      #### Previous: Indicates the outcome of previous marketing campaigns.
      #### Emp.var.rate: Represents the employment variation rate.
      #### Euribor3m: Reflects the Euribor 3-month rate.
      #### Pdays: Denotes the number of days since the last contact.
      #### Nr.employed: Refers to the number of employees in the bank.
### Impact on Subscription Chances:
   #### Positive Factors:
      Duration & Previous: The more successful previous marketing outcomes, the higher the likelihood of subscribing to a term deposit. The higher the duration of interactions the higher the possibility of subscription

   #### Negative Factors:
      Emp.var.rate, Euribor3m, Pdays, and Nr.employed: Higher values in these categories decrease the chances of subscribing







