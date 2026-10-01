# Retail-Sales-Performance-Analysis-Dashboard
An interactive retail sales analysis and dashboard exploring revenue, transactions, product performance, customer value, payment methods, and sales trends over time.
## Project Overview
This project presents an analysis of retail sales data to evaluate revenue performance, product performance, sales volume, customer purchasing value, payment behaviour, location performance, and transaction trends over time.
The project involved cleaning and transforming the raw dataset using Power Query, creating analytical measures in Power BI, and developing an interactive dashboard to explore relationships between sales volume, pricing, revenue, transaction value, location, payment method, and time. Rather than looking at revenue as an isolated metric, the analysis examines the factors that contribute to revenue performance and how different sales metrics relate to one another.

## Project Objective
- Evaluating overall sales and revenue performance
- Identifying products with the highest revenue contribution
- Comparing product revenue performance with quantity sold
- Examining the relationship between selling price, quantity, and revenue
- Evaluating average transaction value across locations
- Understanding payment method usage and its contribution to revenue
- Examining transaction and revenue trends over time
- Identifying patterns that can provide a broader understanding of retail sales performance

## Dataset Source
The dataset used for this project was obtained from Analytics Engineering.
The original dataset contained retail transaction information relating to products, categories, locations, payment methods, quantities, prices, transaction dates, customers, and spending. The raw data was transformed and prepared before being used for analysis and dashboard development.

## Data Cleaning & Transformation
The raw dataset required several cleaning and transformation steps before analysis.
The data preparation process was performed using Power Query.
#### Item Column Transformation
The original item field contained combined information such as:
- Item_10_PAT: The item column was split to separate the item identifier from the accompanying short name, producing fields such as: Item_10, PAT.
A separate short-name field was subsequently created using a conditional column based on the product category. This provided a more consistent naming structure across the dataset.
For example: Patisserie → Pat
This helped standardize the product naming used in the analysis.
#### Row Filtering
Irrelevant and unsuitable rows were filtered out to ensure that the dataset used for analysis contained valid records.
#### Column Reordering
Columns were reordered to improve the structure and readability of the transformed dataset and make the fields easier to work with during analysis.
#### Data Type Transformation
Column data types were reviewed and changed where necessary to ensure that fields such as dates, numerical values, quantities, and categorical fields were appropriately formatted for analysis.
#### Text Transformation
Text fields were trimmed to remove unnecessary leading or trailing spaces and improve consistency across categorical values.
#### Removal of Unnecessary Columns
Columns that were no longer required for the analysis were removed, including:
- Previous Price
- Original Item column
- Other unnecessary fields after transformation
This reduced unnecessary data and kept the analytical dataset focused on the variables required for the dashboard.
#### Price Calculation
A custom column was created to derive price per unit using total spending and quantity:
Price per Unit = Total Spent ÷ Quantity
This provided a usable price measure for analysing the relationship between quantity sold, selling price, and revenue.

## Data Analysis & Measures

