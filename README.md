# Lending club case study

## Problem statement
Lending club is a consumer finance company which specialises in lending various types of loans to urban customers. When the company receives a loan application, the company has to make a decision for loan approval based on the applicant’s profile. Two types of risks are associated with the bank’s decision.
1. If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company.
2. If the applicant is not likely to repay the loan, i.e. he/she is likely to default, then approving the loan may lead to a financial loss for the company

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

## General Information
###  Objective
The aim is to identify patterns which indicate if a person is likely to default, which may be used for taking actions such as denying the loan, reducing the amount of loan, lending (to risky applicants) at a higher interest rate, etc. Using exploratory data analysis (EDA) this objective needs to be achieved with the help of dataset which has information about past loan applicants.

The company wants to understand the driving factors (or driver variables) behind loan default, i.e. the variables which are strong indicators of default.  The company can utilise this knowledge for its portfolio and risk assessment. 

### Understanding the dataset
The Loan dataset contains information about past loan applicants and whether they defaulted or not. The aim is to identify patterns which indicate if a person is likely to default, which may be used for taking actions such as denying the loan, reducing the amount of loan, lending (to risky applicants) at a higher interest rate, etc.
The dataset does not contain the rejection criteria details.The loan process involves three steps.
1. Borrower requests a loan amount
2. The approver decides to approve the loan based on past history and verification (funded_amnt).
3. The investor determines the final loan amount to be offered (funded_amnt_inv).

### Data Analysis
1. Primary attributes identified
2. Key columns identified for analysis
3. Certain columns are excluded from the analysis as they do not provide insights into whether the loan can be approved or rejected, nor do they help in predicting potential defaults.
4. No header or footer rows in the dataset.
5. No column numbers, indicators, etc., found in the dataset.
6. No summary rows in the dataset.
7. Rows with a "loan_status" of "Current" will be dropped as they represent loans in progress.
8. Identified and removing columns having complete null values
9. Removed column that had single value 
10. Removed column having missing data more than 60%
11. Certian column formats converted
12. Standardised values
13. identify outliers and removed




## Conclusions
### Univariate analysis
#### Observations and Inferences from Ordered categorical Variables analysis
* Loans with a 36-month term are most likely to default. 3006 Loans under 36 months got defaulted. This indicates that individuals default on short-term loans.
* Grade B had the highest number of Charged off loan applicants, with a total of 1,352 applicants. The next is C with 1293 loan applicants. This indicates the lending club should pay attention for providing loan to B & C Grade applicants.
* Sub Grade-wise B3,B4 and B5 are the most defaulters under B. Also in C, we have majority of defaulters in C2 & C3. This means with Grade B & C, the lending club needs to focus on the above sub grades carefully before approving loans.
* Employees with 10+ years of experiences are the majority defaulters, this figure is 1474 loans, which means the employee experience will not guarantee full payment of loans.
* December is most of the month wherein maximum loans gets defaulted. Total of 640 loans got defaulted. This may be due to holiday season. Lending club should do proactive follow-ups during the previous month.
* Year 2011 reported 3152 loans got defaulted. This is more than 50% of 2010.The same trend is continued from 2007 to 2010. The trend shows there is likely to be more defaulters in upcoming years.
* Loans are getting defaulted in the last quarter (Q4). Reported that 1754 loans gets defaulted. This may have occured due to holiday season.
#### Observations and Inferences from Un-Ordered categorical Variables analysis
* Rented accommodation has the highest defaulters, which is 2715 loans. Lending club should take necessary caution on approving loans for those who are living in rented house as this can likely get defaulted.
* Comparatively majority of the loans are fully paid, which gives a positive indication about the process in place for lending club.
* 3331 Loans are defaulted which is also verified. This indicates lending club needs to revisit verification process and identify and fix gaps wherever required.
* Majority of loan got defaulted due to Debt consolidation. 2633 loans got defaulted. This indicates that when the loan is granted for this purpose the lending club has to ensure that the applicant has the capability to pay the loan as well.
* The state of CA contributes to the majority of defaulters. Lending club should be more cautious when we approve loan in this State.
#### Observations and Inferences from Quantitative analysis
* Majority of loan installment for defaulters lies between 160-400. This gives an indication for Lending company to monitor closely on these applicants with similar installments.
* Most defaulters are those with loan amount beween 5K to 10K . The lending company should evaluate applicants who apply for bigger amount. Should verify repayment capability as well.
* 1601 Loan applicants who received funds between 5K to 10K are most of the defaulters. The lending company should be cautious on providing large funds to applicants. Lending company should verify the repayment capebility before approval.
* 1716 Loan applicants with salary range from 0-40K are most of the defaulters. Lending company should check the repayment capability of employee who is in the lower salary band.
* 2546 Loan applicants having 10-15% interest rate contribute to the majority of charged off loans. A lower interest rate could possibly mitigate the risk of credit loss.
* 1235 Applicants have very high Debt-to-income ratio. The lending company should put strict debt to income ratio requirements in order to have sustainable levels for the debt against income.
### Bivariate analysis
* **Ordered categorical variable**
    * Loan applicants in Grades B, C, ano D account for the majority of ‘Charged Off’ loans. However, Grades A and B make up the largest portion of total loan applicants. This indicates that Grade A applicants positively impact the business, while caution is needed when approving loans for Grade B, C and D applicants.
    * Loan subgrade B3,B4,B5,C1,C2,C3 & D2 contribute to most of Charged off loans.
    * Most charged-off loans are short-term. However, when comparing the total loans for each term, the percentage of long-term loans being charged off is higher than that of short-term loans. In this case company should assess risk with long term loan and adjust term or the interest rate accordingly.
    * Employees having 10 or more years of experience are majority of loan applicants. They are also most likely to be defaulters. Experience should not be the only criteria for approving loans.
    * December month is the month with the maximum number of loan applicants. The company should adopt efficient way to meet customer needs with minimal risk on credit loss.   
    * From 2007 to 2011 there is a positive trend of loan applicants. This shows there is a positive trend of more applicants in upcoming years. The company should also note that with increasing trend of loan applicants, robust risk mitigation measures should be adopted.    
    
* **Unordered categorical variable**
    * Loan applications received from those living in rented houoe and mortgage contribute to the majority and they are more likely to be defaulters. The lending company should take appropriate measures while lending loans to applicants with rented houses and mortgage.
    *  Verified loans are also getting defaulted. The Verification process need to be strengthened.
    * Majority loan has been approved on debt consolidation and this mostly contributes to charged off loans. To manage this situation, company should take appropriate measures to ensure loan repayment.
    * There are more loan applicants from States CA, FL & NY and they make to the majority of the defaulters list. Going forward there will be more defaulters from the above mentioned states.Company should take more stringent rules and efficient methodology while approving loans to applicants from these states.
    * High count of loans get charged off in cases where the Debt-to-income ratio is very high. Lending company should focus on granting loans for applicants with low DTI to reduce credit loss.
    * A significant count of loan defaulters received loans with interest rates falling within the range of 10% to 15%. Lending company should modify the interest rates such that the customer can repay and the risk on credit loss can be avoided.
     
* **Quantitative Variables**
  * Majority of loan amount applied is between 5K to 10K and the majority defaulters are in this category.This pattern could continue as trend. The lending company should be cautious when approving higher amount loans.
   * Majority of loan applicants are with salary less than 40000 and they contribute to most of the charged off loans. Less annual income leads to defaulting tendency. The company should implement a cap on loan amounts based on income levels to ensure affordability for the borrower.
   * Higher DTI and interest rate ranging from 10 to 15% are likely to contribute to loan default. Company should evaluvate on DTI and adjust interest rates accordingly so that customer can repay and the risk on credit loss can be avoided.
### Inference from Correlation Analysis
* **Strong correlation**
    * installment has strong correlation with loan_amnt, funded_amnt_inv and funded_amnt.
    * loan_amnt has strong correlation with funded_amnt and funded_amnt_inv.
* **Weak correlation**
    * dti has weak correlation with most of the columns.
    * emp_length has weak correlation with most of the columns.
* **Negative correlation**
    * pub_rec_bankruptcies has negative correlation with most of the fields
    * emp_length has negative correlation with int_rate.
    * annual_inc has negative correlation with dti.
### Multivariate analysis
* The tendency to default is higher for Grades B, C, and D. However, the charge-off percentages relative to the total number of loans are highest for Grades G and F, at 36.6% and 32.8%, respectively. Despite having fewer loans in Grades G and F, caution should be applied when approving loans on these grades too as the likelihood of default is higher in these grades as well.
* Borrowers in sub-grades B3, B4, B5, C1, C2, and D2 are likely to default. However, in terms of charge-off percentage relative to the total number of loans, F5 and G3 have the highest rates. The best performance in this category is seen in grades A1 to A5, with less than 10% of borrowers defaulting. Company should also provide special attention to subgrades F5 and G3 while approving loans.
* Employees with over 10 years of service had a charge-off rate of 16.5%.This clearly indicates that the length of service is not a reliable criterion for loan approval.
* Although the majority of loan defaulters are from CA, FL, and NY, there are 17 states with a charge-off rate more than 15%. The company should implement an efficient methodology to thoroughly evaluate loan applicants from these states before approving loans.
* Eventhough majority of defauters are in debt consolidation , considering Charge off percentage, small Business contribute the maximum which is 27.7%. Lending company should have proper measures in place for approving small business loans.
* The charge-off rate is highest for employees earning less than 40K, at 18.1%. Borrowers in lower income groups have the highest tendency to default on loans, and this tendency generally decreases as annual income increases.
* Rise in interest rate and increase in DTI will lead to higher default percentage. Before approving loans, the company should verify the open debts and assess the payment capability of loan applicants relative to their income.



## Technologies Used
- Python - 3.12.4
- NumPy version - 1.26.4
- pandas version - 2.2.2
- Matplotlib version - 3.8.4
- Seaborn version - 0.13.2

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
Give credit here.
- This project was inspired by...
- References if any...
- This project was based on [this tutorial](https://www.example.com).


## Contact
Created by [@githubusername] - feel free to contact me!

