# Bits n Bobs-Sales-Analysis
This document details the data preparation and transformation process for the BitsAndBobs sales analysis project conducted on GitHub. This analysis aims to address the company's concerns about declining sales and provide valuable insights for future decision-making.

## Data Source:
AssignmentTwo2022Data.xls

## Software:
Power BI Desktop

## Process:
  ### 1. Connect to Data:
        Excel file containing sales data is loaded into Power BI Desktop.
  ### 2. Transform Data:
        Cleaning and manipulation of data to prepare it for analysis.
        Key steps include:
          Identifying and removing duplicate receipt IDs: Queries were used to detect and remove duplicate entries based on receipt IDs.
          Correcting inconsistencies in item quantities: Instances where multiple entries existed for the same item within a receipt (violating business rules) were addressed by summing quantities of such items into a single row.
          Adding columns:
            "New Reciept ID": A new unique identifier was created for each receipt to address duplicate issues.
            "Discount Status": Based on the number of items per receipt, a column was added to indicate eligibility for a 5% discount (receipts with 5 or more items).
          Checking data quality: Column Quality tool was used to identify and address null values and data validity issues.
  ### 3. Load - Datamart Creation:
          Create six reference tables (dimensions) from the staging table:
            dimDate
            dimCustomer
            dimStaff
            dimItem
            dimOffice
          Create the fact table (FactSale) by merging the dataset with dimension tables.
          Remove unnecessary columns to obtain the final output.

## Datamart Structure:
The following tables constitute the datamart:
  ### Dimension Tables:
        dimDate
        dimCustomer
        dimStaff
        dimItem
        dimOffice
  ### Fact Table:
        FactSale
  ### Foreign Keys in FactSale:
        Date_key
        Cust_key
        Staff_key
        Office_key
        Item_key

## Performance Evaluation:
  ### Branch Performance:
        Wagga Wagga consistently ranked highest in net revenue, total transactions, and year-end revenue for both 2021 and 2022.
        Wollongong consistently exhibited the lowest performance across these metrics.
  ### Item Performance:
        Mitre Saw was the most popular item across all branches.
        Top and least performing items were identified for each branch.
  ### Staff Performance:
        S186 consistently ranked among the top performers in both monthly earnings and transaction count.
        Low-performing staff members were identified through branch analysis.

### Dashboard
[Dashboard - BitsnBobsSales](https://app.powerbi.com/groups/me/dashboards/50e3223d-6beb-40bf-8a0c-59d24e72791b?experience=power-bi)

## Recommendations:
    Branch Consolidation:
        Instead of consolidating branches, focus on improving performance at Wollongong through targeted interventions.
        Potential strategies include staff training, performance incentives, and revised sales tactics.
    Sales Target Setting:
        Utilize average revenue per office as a benchmark for setting individual and team targets.
        For example, a yearly target of $1,500,000 for Melbourne with a 10-person sales team translates to individual quotas of $150,000.
        Align bonus and commission structures with quota achievement to motivate individual performance.
    Data-Driven Decision Making:
        Leverage the insights from this analysis to inform future marketing campaigns, inventory management, and pricing strategies.
        Continuously monitor and analyze sales data to adapt and optimize approach based on emerging trends and performance fluctuations.
## Additional Insights:    
    Income forecast for 2023 was estimated for each branch based on previous year's performance and percentage change.
    Specific staff members can be identified for targeted coaching and development initiatives based on their individual performance within their respective branches.
    By implementing these recommendations and continuously utilizing data-driven insights, BitsAndBobs can effectively overcome performance challenges, revitalize sales, and achieve long-term strategic goals.
