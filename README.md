# Bits and Bobs Sales Analysis

This repository documents the data preparation and transformation process for the BitsAndBobs sales analysis project conducted on GitHub. The analysis addresses the company's concerns about declining sales and provides valuable insights for future decision-making.

## Data Source
- **AssignmentTwo2022Data.xls**

## Software
- **Power BI Desktop**

## Process

1. **Connect to Data:**
   - Excel file containing sales data is loaded into Power BI Desktop.

2. **Transform Data:**
   - Cleaning and manipulation of data to prepare it for analysis.
   - Key steps include:
     - Identifying and removing duplicate receipt IDs.
     - Correcting inconsistencies in item quantities.
     - Adding columns: "New Reciept ID" and "Discount Status."
     - Checking data quality using the Column Quality tool.

3. **Load - Datamart Creation:**
   - Create six reference tables (dimensions) from the staging table.
   - Create the fact table (FactSale) by merging the dataset with dimension tables.
   - Remove unnecessary columns to obtain the final output.

## Datamart Structure

**Dimension Tables:**
- dimDate
- dimCustomer
- dimStaff
- dimItem
- dimOffice

**Fact Table:**
- FactSale

**Foreign Keys in FactSale:**
- Date_key
- Cust_key
- Staff_key
- Office_key
- Item_key

## Performance Evaluation

**Branch Performance:**
- Wagga Wagga consistently ranked highest in net revenue, total transactions, and year-end revenue.
- Wollongong consistently exhibited the lowest performance.

**Item Performance:**
- Mitre Saw was the most popular item across all branches.
- Top and least performing items were identified for each branch.

**Staff Performance:**
- S186 consistently ranked among the top performers in both monthly earnings and transaction count.
- Low-performing staff members were identified through branch analysis.

## Dashboard
[BitsnBobsSales Dashboard](https://app.powerbi.com/groups/me/dashboards/50e3223d-6beb-40bf-8a0c-59d24e72791b?experience=power-bi)

## Recommendations

**Branch Consolidation:**
- Focus on improving performance at Wollongong through targeted interventions.
- Potential strategies include staff training, performance incentives, and revised sales tactics.

**Sales Target Setting:**
- Utilize average revenue per office as a benchmark for setting individual and team targets.
- Align bonus and commission structures with quota achievement.

**Data-Driven Decision Making:**
- Leverage insights for future marketing campaigns, inventory management, and pricing strategies.
- Continuously monitor and analyze sales data for adaptive strategies.

## Additional Insights

- Income forecast for 2023 was estimated for each branch based on the previous year's performance and percentage change.
- Identify specific staff members for targeted coaching and development initiatives.
- Implement recommendations to overcome performance challenges and achieve long-term strategic goals.
