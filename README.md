# Credit Card Financial Dashboard

## Project Objective
To develop a comprehensive Credit Card Weekly Dashboard 
that provides real-time insights into key performance 
metrics and trends, enabling stakeholders to monitor 
and analyze credit card operations efficiently.

## Project Steps

### 1. Data Import
- Created MySQL database (ccdb)
- Created two tables: cc_detail (18 columns) 
  and cust_detail (15 columns)
- Imported 4 CSV files using LOAD DATA LOCAL INFILE
- Total rows imported: 10,293

### 2. Power BI Connection
- Connected Power BI to MySQL database
- Server: 127.0.0.1:3306
- Database: ccdb

### 3. DAX Queries Used
- AgeGroup: Grouped customers into age buckets 
  (20-30, 30-40, 40-50, 50-60, 60+)
- IncomeGroup: Grouped income into Low/Medium/High
- Revenue: Annual_Fees + Total_Trans_Amt + Interest_Earned
- WeekNum2: WEEKNUM function for correct week sorting
- CurrentWeekRevenue: CALCULATE + FILTER + MAX
- PreviousWeekRevenue: CALCULATE + FILTER + MAX-1
- WoW_Revenue: DIVIDE for week on week % change

### 4. Dashboards Created
Two dashboards created:
- Credit Card Transaction Report
- Credit Card Customer Report

### 5. Key Insights
- Total Revenue: 57 Million
- Total Interest: 8 Million
- Total Transaction Amount: 46 Million
- Male customers contribute more revenue than female
- Blue card generates highest revenue (93%)
- Top 3 states: Texas, New York, California
- Activation Rate: 57%
- Default Rate: 6.06%
- Self employed customers have highest default rate (1.66%)
- Week 53 revenue increased 28.8% week on week

## Files in Repository
- credit_card_report.pbix = Power BI dashboard file
- credit_card.csv = Main credit card transaction data
- customer.csv = Customer details data
- cc_add.csv = Week 53 additional credit card data
- cust_add.csv = Week 53 additional customer data
- credit_card_queries.sql = MySQL queries used

## Tools Used
- MySQL = Database creation and data import
- Power BI Desktop = Dashboard creation
- DAX = Data calculations and measures

