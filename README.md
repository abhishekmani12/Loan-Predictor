# Loan-Eligibilty-Predictor
The model predicts if a person is eligible for a loan and returns back a report of those who are eligible

EDA was done by
i)Univariate Analysis
ii)Bivariate Analysis
The 13 variables/Column names were divided into 3 types:
• Ordinal features: Variables in categorical features having some order involved (Dependents, Education, Property_Area)
• Numerical features: These features have numerical values (ApplicantIncome, Co-applicantIncome, LoanAmount, Loan_Amount_Term)
• Categorical features: These features have categories (Gender, Married, Self_Employed, Credit_History, Loan_Status)

Under Bivariate analysis, the relation between Categorical Independent Variable vs Target Variable was made and the inferences are as follows:
• The proportion of married applicants is higher for approved loans.
• Distribution of applicants with 1 or 3+ dependents is similar across both the categories of Loan_Status.
• People with a credit history as 1 are more likely to get their loans approved.
• Proportion of approved loans is higher for Low and Average Loan Amount as compared to that of High Loan Amount
• Chances of loan approval will be high when the loan amount is less.
In cleaning two methods were considered for filling the missing data:
• For numerical variables: imputation using median
• For categorical variables: imputation using mode
The outliers in the loan_amount data were right skewed and log transformation was used to remove the skewness.

Independent and dependent feature:
• 12 Independent Variables : Gender, Married, Self_Employed, Credit_History, Dependents, Education, Property_Area, ApplicantIncome, Co-applicantIncome, LoanAmount, Loan_Amount_Term
• 1 Target Variable: Loan_Status
3.selection/engineering/scaling:
Scaling modifies features to lie between a given minimum and maximum value, often between zero and one, or so that the maximum absolute value of each feature is scaled to unit size to improve the numerical stability of models.

Scaling was done using Normalizer

1.Normalizing was done on the numerical data in order to standardize the numerical data.
2.Normalizer on 'LoanAmount','CoapplicantIncome','ApplicantIncome', 'TotalIncome' .
 
4.Model, Accuracy and Output File:
Logistic Regression was used to predict the target variable: Loan_status
Accuracy: 0.7967479674796748
Prediction was done using a separate test data set and the result of it was imported to a submission file.
The submission file contains an addition column EMI through feature engineering
EMI was calculated through 2 existing columns: LoanAmount divided by Loan_Amount_Term
