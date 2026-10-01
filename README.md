# Retail-Sales-Performance-Analysis-Dashboard
An interactive retail sales analysis and dashboard exploring revenue, transactions, product performance, customer value, payment methods, and sales trends over time.

<img width="1269" height="675" alt="Retail Sales" src="https://github.com/user-attachments/assets/f4cd46ee-6402-4bb8-9136-835c9264df3b" />

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

## Tools & Technologies
- Power Query — Data cleaning and transformation
- Power BI — Data modelling, measure creation, analysis, and dashboard development
- DAX — Creation of analytical measures
- Analytics Engineering — Dataset source

## Data Cleaning & Transformation
The raw dataset required several cleaning and transformation steps before analysis.
The data preparation process was performed using Power Query.
1. **Item Column Transformation:** The original item field contained combined information such as; Item_10_PAT. The item column was split to separate the item identifier from the accompanying short name, producing fields such as: Item_10, PAT. A separate short-name field was subsequently created using a **conditional column** based on the product category. This provided a more consistent naming structure across the dataset. For example: Patisserie → Pat. This helped standardize the product naming used in the analysis.
2. **Row Filtering:** Irrelevant and unsuitable rows were filtered out to ensure that the dataset used for analysis contained valid records.
3. **Column Reordering:** Columns were reordered to improve the structure and readability of the transformed dataset and make the fields easier to work with during analysis.
4. **Data Type Transformation:** Column data types were reviewed and changed where necessary to ensure that fields such as dates, numerical values, quantities, and categorical fields were appropriately formatted for analysis.
5. **Text Transformation:** Text fields were trimmed to remove unnecessary leading or trailing spaces and improve consistency across categorical values.
6. **Removal of Unnecessary Columns:** Columns that were no longer required for the analysis were removed, including; original Price, Item, and other unnecessary fields after transformation. This reduced unnecessary data and kept the analytical dataset focused on the variables required for the dashboard.
7. **Price Calculation:** A **custom column** was created to derive price per unit using total spending and quantity:
Price per Unit = Total Spent ÷ Quantity. This provided a usable price measure for analyzing the relationship between quantity sold, selling price, and revenue.

## Data Analysis & Measures
After the data was cleaned and transformed, the dataset was loaded into Power BI for analysis and visualization. The following measures were created:
1. **Average Selling Price:** Measures the average price at which individual units were sold. This measure provides context when comparing products by revenue and quantity because revenue is influenced by both the number of units sold and the price per unit.
2. **Average Order Value (AOV):** Measures the average value generated per transaction. AOV provides a customer/order-level perspective that complements the overall revenue and transaction metrics.
3. **Revenue per Unit:** Measures the revenue generated per unit sold and provides additional context for evaluating product performance and differences between sales volume and revenue contribution.

## Dashboard Analysis
#### 1. Overall Sales Performance: 
The dashboard begins with six key performance indicators;
- Total Revenue: 1.55M
- Unique Customers: 25
- Average Selling Price: 23.42
- Total Transactions: 11.971K
- Quantity Sold: 66.28K
- Average Order Value: 129.66

Together, these metrics provide an overview of the scale and value of the retail activity represented in the dataset. Revenue and transaction volume show the overall scale of sales, while quantity sold provides a view of sales volume. Average selling price and average order value provide additional context for understanding how that sales volume translates into monetary value.
#### 2. Revenue and Transaction Activity Over Time: 
The dashboard uses both Revenue Trend Over Time and Monthly Transactions to examine sales performance across the period covered by the dataset. The transaction chart shows how the number of transactions changes from month to month, while the revenue trend shows how the monetary value generated changes over the same period.

Looking at both measures together allows changes in transaction activity to be considered alongside changes in revenue. Periods with similar transaction volumes can still produce different revenue levels because the value generated from each transaction can vary. This connects the time-based analysis back to Average Order Value, which helps explain the value of transactions beyond simply counting how many occurred.
The combined view therefore provides a more complete picture: Transaction Volume → Transaction Value → Revenue
#### 3. Location & Average Order Value:
The dashboard compares AOV between Online and In-store locations.
- Online: 130.42
- In-store: 128.87

Online transactions recorded a slightly higher average order value than in-store transactions. However, the difference between the two locations is relatively small, indicating that the overall AOV is not being driven by a large difference in average transaction value between the two locations. This comparison complements the overall 129.66 AOV KPI by showing how the overall figure is represented across the different purchasing locations.
The relationship can therefore be viewed as: Overall AOV → Location-level AOV → Comparison of transaction value
#### 4. Payment Method Analysis
The dashboard examines payment behaviour through two related visualizations:
- Percentage of Transactions by Payment Method
- Revenue by Location and Payment Method

The transaction distribution shows the relative use of Cash, Digital Wallet, and Credit Card, while the revenue chart examines how revenue is distributed across these payment methods and locations. Looking at both charts together allows payment methods to be considered from two perspectives:
- How frequently is the payment method used? and
- How much revenue is associated with those transactions?

This distinction is important because transaction frequency and revenue contribution do not necessarily move in the same proportion. A payment method with a large share of transactions may not automatically account for a proportionally larger share of revenue if the average value of those transactions differs. The location breakdown adds another layer by showing how payment behavior and revenue interact across online and in-store transactions.
#### 5. Product, Price and Revenue Relationship
One of the key analytical relationships in the dashboard is the connection between:
- Quantity Sold → Price per Unit → Revenue
- Quantity sold represents sales volume, while price per unit determines how much revenue each unit contributes.

Consequently, evaluating products using quantity alone can provide an incomplete picture of their financial contribution. The comparison between product quantity and product revenue, supported by the Average Selling Price and Revenue per Unit measures, helps distinguish between products that perform strongly because of volume and products that generate substantial revenue because of their value per unit.

## Overall Analytical Relationship
The dashboard brings the different dimensions together to examine retail performance from multiple perspectives.

Products

→ What is being sold?

Quantity

→ How much is being sold?

Price

→ At what value is it being sold?

Revenue

→ What monetary contribution does the product generate?

Transactions & AOV

→ How much value is generated per transaction?

Location

→ Where are customers purchasing?

Payment Method

→ How are customers paying?

Time

→ How does sales activity and revenue change over time?

Together, these relationships allow the dashboard to move beyond simply reporting sales figures and instead examine the different factors that shape retail performance.

The interactive Power BI dashboard includes:

## Key Insights
1. Revenue performance is not determined by quantity alone. The product with the highest quantity sold is not the product with the highest revenue. This indicates that sales volume alone does not determine revenue contribution. The difference can be understood through the relationship between quantity sold and selling price. Products with higher selling prices can generate greater revenue even when their unit sales are lower.

2. Product performance differs depending on the metric used. A product can perform strongly in terms of sales volume without being the strongest contributor to revenue, and vice versa. This demonstrates why product performance should be evaluated using multiple measures rather than relying on quantity sold or revenue alone.

3. Transaction volume and revenue measure different aspects of performance. The dashboard's revenue and transaction trends demonstrate that the number of transactions does not, by itself, explain the full movement in revenue. The value generated per transaction also matters, which is why Average Order Value provides an important link between transaction volume and total revenue.

4. Online and in-store transaction values are relatively similar. Online AOV is 130.42, compared with 128.87 for in-store transactions. The relatively small difference indicates that the two locations have similar average transaction values within the dataset, rather than one location having a substantially higher average order value.

5. Payment behavior provides another perspective on revenue. The percentage of transactions by payment method shows how transaction activity is distributed across Cash, Digital Wallet, and Credit Card. Comparing this distribution with revenue by payment method provides a deeper view of whether transaction frequency corresponds proportionally with revenue contribution.

6. Revenue analysis requires both volume and value perspectives. The dashboard demonstrates the importance of analyzing retail performance through both volume-based measures such as quantity and transactions and value-based measures such as revenue, selling price, AOV, and revenue per unit. Using these measures together provides a more complete interpretation of sales performance.

## Dashboard Features
- Revenue performance KPIs
- Customer and transaction metrics
- Measures (Average selling price, Average order value, and Revenue per unit)
- Top products by revenue
- Product quantity comparison
- Revenue trends over time
- Monthly transaction trends
- Payment method analysis
- Revenue by location and payment method
- AOV by location
- Interactive filters for: Location, Payment Method, and Product Category

## Conclusion
This project demonstrates the process of transforming raw retail transaction data into an interactive analytical dashboard. Through Power Query, the raw data was cleaned, transformed, standardized, and prepared for analysis. Power BI was then used to create analytical measures and visualize relationships between sales volume, product pricing, revenue, transaction value, payment behaviour, location, and time.

The analysis highlights that retail performance cannot be understood through a single metric. Quantity sold explains volume, while price helps explain value; transactions measure activity, while AOV provides context for transaction value; and revenue brings these factors together into a monetary measure of performance.

The resulting dashboard provides an integrated view of retail sales performance and demonstrates the use of data cleaning, transformation, analytical measurement, and interactive visualization to derive insights from transactional data.
