# bank-loan-analysis
## 🎯 Objective

The objective of this project is to analyze bank loan data using Tableau and provide meaningful insights through interactive dashboards. The analysis helps identify loan application trends, funded amounts, repayment behavior, and overall loan performance to support data-driven decision-making in the banking sector.
## Dataset Used
- <a href= "https://github.com/venu89-git/bank-loan-analysis/blob/main/bankloan.twb"
## 📊 Key Performance Indicators (KPIs)
-Loan Application and Funding
Total Loan Applications: 43,141

Good Loan Applications: 37,842

Bad Loan Applications: 5,333

Bad Loan %: 12.4%

Good Loan %: 87.6%

-Total Funded Amount: $539.81 million

Good Loan Funded Amount: $486.29 million

Bad Loan Funded Amount: $53.52 million

- Total Amount Received: $473.07 million

Good Loan Amount Received: $435.79 million

Bad Loan Amount Received: $37.28 million

- Month-over-Month (MOM) Analysis
MOM Loan Applications: -2.4%

MOM Total Funded Amount: -3.7%

MOM Total Amount Received: 15.8%

MOM Average Interest Rate: 2.6%

MOM Average DTI: 2.7%

- Other Key Metrics
Average Interest Rate: 12.0%

Average DTI (Debt-to-Income): 13.3%
## 📝 Step-by-Step Project Process (Updated)
This project is a Tableau workbook designed to analyze and visualize bank loan data. The analysis is presented through a series of dashboards and calculated metrics.

- 1. Data Source
Database: The project connects to a SQL Server database.


Server: LAPTOP-FKSBM4HK 


Database Name: Bank Loan DB 


Table: [dbo].[Bank_Loan_data] 

- 2. Key Calculated Fields and Metrics
The analysis is built on several calculated fields to create key performance indicators (KPIs) and other metrics:


Good vs. Bad Loans: A categorical bin is created from the [loan_status] field to classify loans as either "Good" (Current or Fully Paid) or "Bad" (Charged Off).






Total Loan Applications: A count of the [id] field.






Total Funded Amount: The sum of [loan_amount].






Total Amount Received: The sum of [total_payment].






Month-over-Month (MOM) Growth: Several calculations measure the percentage change from the previous month to the current month for various metrics, including loan applications , funded amounts , amount received , average interest rate , and average DTI (Debt-to-Income ratio).





- 3. Dashboards and Visualizations
The project is organized into three main dashboards.

Summary Dashboard: Provides a high-level overview.


KPI Cards: Displays key metrics like total loan applications, total funded amount, and total amount received.




MOM Growth: Shows month-over-month change for these KPIs.





"GOOD LOAN ISSUED" Chart: A pie chart created with two AVG(0) calculations on the rows shelf. It visualizes the proportion of "Good Loans" and "Bad Loans" based on 

Total Loan Applications.






Filters: Includes filters for Purpose, Grade, and Verification Status to enable interactive analysis.

Overview Dashboard: Presents detailed visualizations for the data.


Charts: Includes an area chart showing trends by month , a map of data by state , and bar charts breaking down data by employee length and loan purpose.






Parameter: A parameter named [Parameter 1] allows the user to dynamically switch the measure displayed in some charts between "Total Loan Application", "Total Funded Amount", and "Total Amount Recevied".





DETAILS Dashboard: A tabular view of the data.


Table: Displays detailed loan information in a table format.





Filters: Includes filters for Purpose, Grade, and Verification Status.

## Dashbord Summary  <a href="https://github.com/venu89-git/bank-loan-analysis/blob/main/Screenshot%202025-09-20%20233813.png"

## Dashbord overview <a href="https://github.com/venu89-git/bank-loan-analysis/blob/main/Screenshot%202025-09-20%20234145.png"

## Dashbord Details <a href="https://github.com/venu89-git/bank-loan-analysis/blob/main/Screenshot%202025-09-20%20234605.png"

# About the sql queries
## Summary KPIs
The summary section includes queries for key metrics like total applications, funded amounts, and received payments, with month-to-date (MTD) and previous month-to-date (PMTD) comparisons.


Total Loan Applications: There are a total of 38,576 loan applications. For the MTD (December), there were 

4,314 applications. For the PMTD (November), there were 



4,035 applications.


Total Funded Amount: The total amount funded is $435,757,075. The MTD funded amount is 

$53,981,425 , while the PMTD amount is 



$47,754,825.




Total Amount Received: The total amount received is $473,070,933. The MTD amount received is 

$58,074,380 , and the PMTD amount received is 



$50,132,030.




Average Interest Rate: The average interest rate is 12.05%. The MTD average interest rate is 

12.36% , and the PMTD average interest rate is 



11.94%.




Average DTI (Debt-to-Income): The average DTI is 13.33%. The MTD average DTI is 

13.67% , and the PMTD average DTI is 


13.30%.


## Good vs. Bad Loans
The queries also break down loans into "Good" and "Bad" categories, with "Good Loans" defined as "Fully Paid" or "Current," and "Bad Loans" defined as "Charged Off".





- Good Loans:


Percentage: 86.18% of all loans are considered "Good".




Applications: There are 33,243 Good Loan applications.




Funded Amount: The total funded amount for good loans is $370,224,850.




Amount Received: The total amount received for good loans is $435,786,170.


- Bad Loans:


Percentage: 13.82% of all loans are considered "Bad".



Applications: There are 5,333 Bad Loan applications.




Funded Amount: The total funded amount for bad loans is $65,532,225.




Amount Received: The total amount received for bad loans is $37,284,763.


## Loan Status and Overview Queries
Additional queries provide detailed breakdowns of loan data by status, month, state, term, employee length, purpose, and home ownership.






Loan Status: Loans are categorized as "Fully Paid," "Charged Off," or "Current". The data provides a count of loans, total amount received, total funded amount, average interest rate, and average DTI for each status. MTD data is also available for total amount received and total funded amount for each loan status.





Monthly Overview: Queries break down loan applications, funded amounts, and received amounts by month, showing data for each month from January to December.


Other Breakdowns: The document includes queries to view loan data by:


State: The total number of applications, funded amount, and received amount are provided for each state.



Term: Data is available for 36-month and 60-month loan terms.



Employee Length: Loan metrics are categorized by the applicant's employment length, such as "< 1 year," "1 year," "2 years," and "10+ years".



Purpose: Loan data is segmented by the purpose of the loan, such as "car," "credit card," "debt consolidation," and "home improvement".



Home Ownership: The data is also grouped by home ownership status, including "MORTGAGE," "NONE," "OTHER," "OWN," and "RENT".





