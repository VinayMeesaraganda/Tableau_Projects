# Loan Default Prediction
This Project is taken from the Zindi Loan Default Prediction 

![Loan Prediction](https://user-images.githubusercontent.com/91108341/230125546-d7160c6f-70d4-48db-b18b-a3b16443220e.png)

# Goal
To predict the chances of loan approval for the customers and if a loan was good or bad for the banks

# Dataset and Attributes

There are 3 different datasets for both train and test.

- Link : https://zindi.africa/competitions/data-science-nigeria-challenge-1-loan-default-prediction/data

# a) Demographic data (traindemographics.csv)

- customerid (Primary key used to merge to other data)
- birthdate (date of birth of the customer)
- bank_account_type (type of primary bank account)
- longitude_gps
- latitude_gps
- bank_name_clients (name of the bank)
- bank_branch_clients (location of the branch - not compulsory - so missing in a lot of the cases)
- employment_status_clients (type of employment that customer has)
- level_of_education_clients (highest level of education)

# b) Performance data (trainperf.csv) : 
This is the repeat loan that the customer has taken for which we need to predict the performance of. Basically, we need to predict whether this loan would default given all previous loans and demographics of a customer.

- customerid (Primary key used to merge to other data)
- systemloanid (The id associated with the particular loan. The same customerId can have multiple systemloanid’s for each loan he/she has taken out)
- loannumber (The number of the loan that you have to predict)
- approveddate (Date that loan was approved)
- creationdate (Date that loan application was created)
- loanamount (Loan value taken)
- totaldue (Total repayment required to settle the loan - this is the capital loan value disbursed +interest and fees)
- termdays (Term of loan)
- referredby (customerId of the customer that referred this person - is missing, then not referred)
- good_bad_flag (good = settled loan on time; bad = did not settled loan on time) - this is the target variable that we need to predict

# c) Previous loans data (trainprevloans.csv) : 
This dataset contains all previous loans that the customer had prior to the loan above that we want to predict the performance of. Each loan will have a different systemloanid, but the same customerid for each customer.

- customerid (Primary key used to merge to other data)
- systemloanid (The id associated with the particular loan. The same customerId can have multiple systemloanid’s for each loan he/she has taken out)
- loannumber (The number of the loan that you have to predict)
- approveddate (Date that loan was approved)
- creationdate (Date that loan application was created)
- loanamount (Date that loan application was created)
- totaldue (Total repayment required to settle the loan - this is the capital loan value disbursed +interest and fees) termdays (Term of loan)
- closeddate (Date that the loan was settled)
- referredby (customerId of the customer that referred this person - is missing, then not refrerred)
- firstduedate (Date of first payment due in cases where the term is longer than 30 days. So in the case where the term is 60+ days - then there are multiple monthly payments due - and this dates reflects the date of the first payment)
- firstrepaiddate (Actual date that he/she paid the first payment as defined above)

# Insights:
- Most clients apply for loan in the age gap of 34-38.
- GT Bank has the highest rate of loan Approvals
- Unity Bank has the lowest rate of approvals
- STERLING bank & SKYE Bank has highest rated Bad Flag Clients 
- Wema Bank & Standard Chartered bank has highest rated Good Flag Clients 
- All Contractors and Retired employment clients has high chances of loan Approvals
- Unemployed has the least chances of loan approval
- Clients with minimum Primary education has the highest chances 
- Clients with Permanent Jobs are more likely to apply loans and contractors are less likely to apply loans

# Interactive Dashboard
Link: https://public.tableau.com/app/profile/vinay3285/viz/Capstoneproject_16779629190470/LoanPrediction?publish=yes

