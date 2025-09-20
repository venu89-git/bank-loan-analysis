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

