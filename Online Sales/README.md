# Online Sales Analysis

Online sales analysis aims to gain insight into sales performance and understand customer behavior. The K-Means clustering method aims to identify buying patterns and segment customers based on similar characteristics. In addition, RFM (Recency, Frequency, Monetary) analysis will be applied to categorize customers based on how recently they made a transaction, how often they shop, and the total value of their purchases. To support this analysis, data visualization is performed using Power BI.

## Dataset
### Orders.csv
This file contains 500 raws and 5 columns with the following variables:
- Order ID: Unique identification for each order (Primary Key).
- Order Date: The date when the order was placed.
- Customer Name: The name of the customer who placed the order.
- State: The province where the customer lives.
- City: The city where the customer lives.

### Details.csv
This file contains 1500 raws and 7 columns with the following variables:

- Order ID: A unique identification that links each order detail to the corresponding order in the Orders.csv file.
- Amount: The total monetary value of the order.
- Profit: The profit earned from the order after deducting costs.
- Quantity: The number of items purchased in the order.
- Category: The main category of the purchased products.
- Sub-Category: A more specific classification of the product within its category.
- Payment Mode: The payment method used by the customer.

## Data Preprocessing

Data preprocessing is a process of data preparation and cleaning that aims to ensure the data is in optimal condition so as to produce more accurate analysis. The data preprocessing process is as follows:
#### Checking missing value
![image](https://github.com/user-attachments/assets/9d632cab-71e7-4b37-b343-6b8ff2218ec7)
#### Checking duplicate
![image](https://github.com/user-attachments/assets/72dcdd4b-b7ab-4bd7-91bd-ccee39eb3c31)

#### Merged the Orders.csv (df_orders) and Details.csv (df_details) dataframes

The two dataframes are merged into one based on the Order ID column using the inner join method. The pandas function pd.merge() is used to merge two dataframes. Using inner join means that only the data that has a matching Order ID in both dataframes will be inserted into the result dataframe (df). Why use inner join? Inner join only joins data that has a match in both tables so the result is cleaner and focuses on information that has a direct relationship. It also helps avoid empty data from one of the tables.
![image](https://github.com/user-attachments/assets/323ad4b6-58d1-465e-8051-751b5e7ba149)

## 📊 Data Visualization

<p align="center">
  <img src="https://github.com/user-attachments/assets/78fb415c-4c2f-4fa4-b662-4c468b5347f8" alt="Total Sales by Category" width="45%">
  &nbsp;&nbsp;
  <img src="https://github.com/user-attachments/assets/daccef23-41d3-42fd-90e0-3a43cab9372b" alt="Total Profit by Sub-Category" width="45%">
</p>

Both graphs show that:
- High sales do not always result in high profits. For example, the electronics category has the highest sales, but some of its sub-categories have low profits or even losses.
- Focusing on high-profit sub-categories, such as printers and sarees, can help improve overall profitability.
- Pricing strategies and operational efficiency should be improved in loss-making sub-categories such as leggings, skirts, kurti, electronic games, and furnishings.

## K-Means Analysis

K-Means is used for customer segmentation based on purchasing behavior in order to:
- Identify high-value customers for retention and loyalty strategies
- Recognize customers with frequent and high-volume purchases
- Detect low-performing customer segments with potential for growth through targeted engagement

#### Metrics:
Amount: Total amount of money spent by the customer
Profit: Total profit of the customer
Order ID: The number of orders placed by the customer
Quantity: Number of product units purchased by the customer

#### Optimal Cluster Selection
<p align="center">
  <img src="https://github.com/user-attachments/assets/578cfe7c-d4d6-4680-bb55-5fefab171e9d" width="45%">
  &nbsp;&nbsp;
  <img src="https://github.com/user-attachments/assets/813930a4-5e2a-45db-888f-0f6ae4463625" width="45%">
</p>
Determining the optimal number of clusters is based on Silhouette scores and the Elbow method. The optimal number of clusters based on the Silhouette score is 2 because it has a score of more than 0.5 while based on the Elbow method is 4. In this analysis, 2 clusters were selected.

#### Result
<p align="center">
  <img src="https://github.com/user-attachments/assets/b1fbf087-16fe-43ba-afe3-0bb4d3d25868" width="45%">
  &nbsp;&nbsp;
  <img src="https://github.com/user-attachments/assets/90d06e0b-c85f-49a6-9b89-4fc3f0a34d96" width="45%">
</p>
- Cluster 0 (Blue):
 Represents customers with lower total spending (Amount), lower profit contributions, and fewer product units purchased.
These customers may be infrequent buyers or price-sensitive segments, and are potential targets for engagement strategies aimed at increasing order size and purchase frequency.

- Cluster 1 (Purple):
 Represents customers with higher total spending, greater profit contributions, and larger quantities purchased.
These are high-value customers who should be prioritized in retention and loyalty strategies.

## RFM (Recency, Frequency, Monetary) Analysis

RFM is an analytical method for customer segmentation based on three main metrics:
Recency (R): 
- Measures the time since the last transaction made by the customer. The more recent the transaction, the higher the value
- Frequency (F): Measures how often a customer makes a transaction within a certain period. The more often the transaction is made, the higher the value
- Monetary (M): Measures the total value of money spent by the customer. The larger the amount, the higher the value.

#### Result

<p align="center">
  <img src="https://github.com/user-attachments/assets/1c46f1b1-ae7c-4c06-81d9-50afec35a220" width="45%">
  &nbsp;&nbsp;
  <img src="https://github.com/user-attachments/assets/953f825c-58d4-49d4-891a-9ee7f71a8500" width="45%">
</p>

- Most customers are in the Lost segment indicating many customers are no longer actively transacting
- The Potential segment shows customers with the potential to become more active
- The At Risk segment shows 34 customers who are at risk of no longer transacting
- The Loyal segment of 3 customers shows very few customers who are truly loyal, customers who are frequent and make significant contributions

#### Correlation between RFM Metrics
![image](https://github.com/user-attachments/assets/2f06a960-5b9d-4432-8993-b3a7cdb2da83)

The correlation between R_Score and F_Score is 0.07, indicating that there is virtually no relationship between Recency and Frequency. In other words, how recently a customer made a purchase does not significantly relate to how often they buy.
The correlation between R_Score and M_Score is 0.10, suggesting that there is no meaningful relationship between the recency of purchase and the amount of money spent.
The correlation between F_Score and M_Score is 0.63, showing a moderately strong positive relationship. This means customers who purchase more frequently also tend to spend more money.

#### Recommendations based on RFM analysis

- The majority of customers belong to the Lost segment, indicating a need for reactivation strategies to revive their engagement and transactions.
- The main focus should be on Loyal customers, as they contribute the highest transaction frequency and monetary value. Retaining and rewarding them is crucial.
- Potential customers show promising recency and monetary value; therefore, engagement strategies should be implemented to encourage them to become loyal customers.
- At Risk customers require timely attention to prevent them from transitioning into the Lost segment.

## Conclusion

This analysis applied two segmentation methods — RFM and K-Means — on the same sales data to explore customer behavior from different angles.
- RFM Analysis: Segments customers by recency, frequency, and monetary value to understand engagement and lifecycle stages.
- K-Means Clustering: Groups customers by spending, profit, quantity, and order count to profile customer value and buying volume.

Both methods use different data but provide complementary insights:
- RFM shows engagement levels.
- K-Means highlights customer value.

These insights support targeted marketing strategies — from reactivating inactive customers to rewarding loyal, high-value buyers.

## Visualization Using Power BI
![image](https://github.com/user-attachments/assets/cae770d0-086b-4c31-a74b-89317d692f63)






