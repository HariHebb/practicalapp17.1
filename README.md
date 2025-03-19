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
      1. Previous: Indicates the outcome of previous marketing campaigns.
      2. Emp.var.rate: Represents the employment variation rate.
      3. Euribor3m: Reflects the Euribor 3-month rate.
      4. Pdays: Denotes the number of days since the last contact.
      5. Nr.employed: Refers to the number of employees in the bank.
### Impact on Subscription Chances:
   #### Positive Factors:
      Duration & Previous: The more successful previous marketing outcomes, the higher the likelihood of subscribing to a term deposit. The higher the duration of interactions the higher the possibility of subscription

   #### Negative Factors:
      Emp.var.rate, Euribor3m, Pdays, and Nr.employed: Higher values in these categories decrease the chances of subscribing

# Model Performance without hyperparameter tuning
![image](https://github.com/user-attachments/assets/b876eff1-cf0d-4eda-9ddb-b53147d9ac9b)
Analysis Summary
1. SVM takes the longest time compared to the other 3 models
2. KNN took the shortest time to complete
3. Accuracies are fairly similar with Logistic Regression and SVM scoring marginally better on the test accuracy
4. All the models except decision tree performed better than the baseline model which had a accuracy of 89%

# Model Performance with hyperparameter tuning
![image](https://github.com/user-attachments/assets/46b1c03d-d8d0-4688-8de8-e082b5a2ade9)

## Time Taken:
    1. KNN: Fastest with 4.93 seconds.
    2. Decision Tree: Second fastest with 6.31 seconds.
    3. Logistic Regression: Takes 39.20 seconds.
    4. SVM: Slowest with 912.65 seconds.
## Train Accuracy:
   1. SVM: Highest with 0.9233.
   2. Decision Tree: Second highest with 0.9174.
   3. KNN: 0.9152.
   4. Logistic Regression: Lowest with 0.9117.
## Test Accuracy:
   1. SVM: Highest with 0.9120.
   2. Logistic Regression: 0.9123 (slightly higher than SVM).
   3. Decision Tree: 0.9162 (highest among all models).
   4. KNN: Lowest with 0.9052.
## Precision:
   1. SVM: Highest with 0.6772.
   2. Logistic Regression: 0.6747.
   3. Decision Tree: 0.6505.
   4. KNN: Lowest with 0.6480.
## Recall:
   1. Decision Tree: Highest with 0.5508.
   2. SVM: 0.4154.
   3. Logistic Regression: 0.4240.
   4. KNN: Lowest with 0.3419.
## F1 Score:
   1. Decision Tree: Highest with 0.5965.
   2. Logistic Regression: 0.5208.
   3. SVM: 0.5149.
   4. KNN: Lowest with 0.4477.
## Conclusion Best Model
   Based on multiple parameters, Decision Tree appears to be the best model overall: Test Accuracy: Highest among all models (0.9162). Recall: Highest among all models (0.5508). F1 Score: Highest among all models (0.5965). Time Taken: Reasonably fast with 6.31 seconds. However, if speed is a critical factor, KNN might be considered due to its fast training time, though it performs slightly inferior on other metrics. If you prioritize marginal accuracy and precision over speed, SVM could be an option, but its extremely long training time might be a significant drawback.









