# Adventure-Work-Sales-Analysis
You can view the dashboard here: https://public.tableau.com/app/profile/nguyen.linh8304/viz/AdventureWorkSalesAnalysis_17232791965170/Salespercustomer

**Project Overview**:  
This project focuses on the analysis of product category performance over time. It utilizes a sample dataset inspired by the "AdventureWorks sample databases" from Microsoft. The analysis provides stakeholders with insights into product and sales trends as well as employee performance.

- **Techniques**: Data filtering, exclusion, transformation, partitioning, merging, and data visualization.

**Technologies Used**:
- **SQL**: For data cleaning and preparation.
- **Tableau**: For data analysis and visualization.
- **QuickDBD**: For database schema visualization.

## Data Pre-processing:
- **Schema Design**: The data schema was initially designed using the QuickDBD tool.

![QuickDBD-Free Diagram (1)](https://github.com/user-attachments/assets/2ec78dd5-3859-45a9-884b-272a892a7966)

  
## Data Analysis Process
1. **Download CSV Dataset**: Obtain the dataset from GitHub.
2. **Design Data Schema**: Use QuickDBD tool to design the data schema.
3. **Import Schema**: Import the designed schema into a database structure.
4. **Pre-process Data**: Clean and prepare data using SQL.
5. **Connect to Tableau**: Link the database to Tableau for analysis.
6. **Perform Calculations and Create Visualizations**: Conduct data analysis and generate visualizations in Tableau.

## Data Processing Using SQL
- **Joined Tables**: Combined all relevant tables.
- **Null Value Calculation**: Calculated the percentage of null values in each column.
<img width="635" alt="Screen Shot 2024-08-13 at 14 34 50" src="https://github.com/user-attachments/assets/9d36dded-54b1-47e5-bcc7-5f198b912870">

- **Data Inspection**: Identified a problem where many product IDs in the vendor table did not match with those in the product table. So delete those columns.
- **Exclusion of Columns**: Excluded columns with more than 70% null values.
- **Exclusion of Rows**: Removed rows with remaining null values.

## Data Processing Using Tableau

### Margin Column Addition

In Tableau, a margin calculation was performed as follows:

- **Margin Calculation**: The margin was defined as the difference between `ListPrice` and `StandardCost`. This calculation was implemented directly within Tableau using a calculated field.

- **Margin Percentage**: To compute the margin percentage, the following formula was used:
  \[
  \text{Margin Percentage} = \frac{\text{ListPrice} - \text{StandardCost}}{\text{StandardCost}} \times 100
  \]
  This formula calculates the percentage of profit margin relative to the standard cost.

This approach allows for dynamic analysis and visualization of margins across different products or categories within Tableau.


## Data Analysis and Findings
- **Revenue by Subcategory**: Bikes, particularly Road and Mountain types, are significant revenue contributors. Accessories generate lower revenues, which may suggest reduced demand or lower pricing.
- **Monthly Trends**: Sales exhibit seasonal patterns, peaking during outdoor activity seasons and dipping in February. This trend could indicate customer behavior or potential inventory management issues.
- **Profit Margins**: Accessories, despite lower revenues, have higher profit margins, reflecting an effective high-margin pricing strategy. Balancing margin with volume is crucial for maximizing overall profit.
- **Customer Purchase Patterns**: Customers who place more frequent orders contribute to higher sales revenue. However, many customers make infrequent purchases.
- **Regional Revenue**: Southwest America leads in sales, followed by Central America. Australia represents the smallest market, which could impact marketing and growth strategies.
- **Employee Individual Performance**: The highest-performing employee was Linda Mitchell, while the lowest was Lynn Tsoflias.
![Dashboard 1 (1)](https://github.com/user-attachments/assets/4d56fe27-31b3-4f8d-a0a3-0f210680a2c1)


