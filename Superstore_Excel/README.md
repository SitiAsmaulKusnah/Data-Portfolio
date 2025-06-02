# Superstore Data Analysis Using Excel

## Project Description

This project aims to analyze sales data from Superstore using Excel. The data analyzed includes sales transactions, product returns, and information related to regions and product categories. The analysis is intended to uncover patterns that can support more efficient business decision-making.

## Data Overview

The dataset consists of the following main sheets:

### 1. **Orders**
Berisi informasi transaksi penjualan:
- `Row ID` : Unique row identifier
- `Order ID`: Unique identifier for each transaction
- `Order Date`: Order placement date
- `Ship Date`: Shipping date
- `Ship Mode`: Shipping method
- `Customer ID`: Customer identifiers
- `Customer Name` : Customer's name
- `Segment`: Product segment
- `Country`: Customer's country
- `State`: Customer's state
- `Postal Code`: Postal code
- `Region`: Superstore's sales region
- `Produk ID`: Product identifier
- `Category`: Product category
- `Sub Category`: Product sub-category
- `Produk Name`: Product name
- `Sales`: Total sales per transaction
- `Quantity`: Number of units sold
- `Discount`: Discount applied to the product in the transaction
- `Profit`: Profit generated from the transaction

### 2. **Returns**
Contains product return information:
- `Order ID`: Returned order identifier
- `Returned`: Return status (Yes/No)
  
### 3. **People**
Contains regional and supervisor information:
- `Region`: Sales region
- `Person`: Regional supervisor name
  
## Data Merging
Data from the Orders, Returns, and People sheets were merged using the VLOOKUP function based on Order ID. This allowed for a more comprehensive analysis of transactions, returns, and sales regions.

## Data Cleaning
### Data cleaning steps included:
- Missing Value Identification: No missing values were found.
- Duplicate Check: Duplicate records were removed to ensure data accuracy.
- Date Format Normalization: Date formats were standardized for time-based analysis.

## Data Insights
Here are several key insights derived from the dataset:

### Q1: KWhen did the first and last transactions occur?
- First transaction: January 3, 2014
- Last transaction: December 30, 2017

### Q2: Are there any missing years in the dataset?
- No full years are missing. The dataset spans 2014 to 2017 completely.

### Q3: What are the total sales and profit during the period?
- Total Sales: $2,297,201
- Total Profit: $286,397

### Q4: What is the profit margin during the period?
- Profit Margin: 12.46%, indicating a moderately profitable business.

### Q5: Which segment contributed the most to profit in 2017?
- Consumer: $45.568,2391
- Corporate: $26.782,3633
- Home Office: $21.088,6672
- The Consumer segment had the highest profit contribution in 2017.

### Q6: Which product categories and sub-categories were most profitable in 2017?
- Technology contributed 54.24% of the total profit, with Copiers being the top sub-category at 26.79%. Machines, however, incurred a loss of -3.07%.
- Supplies followed with 42.53% contribution, led by Paper (12.89%), while Supplies sub-category showed a loss of -1.02%.
- Furniture contributed only 3.23%, with Chairs performing best (8.18%) and Tables having the largest sub-category loss at -8.71%.

### Q7: When did the highest sales spike occur?
- In 2016, sales increased by 29.47% compared to the previous year.

### Q8: Which category contributed most to the 2016 sales spike?
- Technology accounted for 39.06% of the 2016 sales increase.

### Q9: What was Technology’s sales contribution in 2016?
- Technology made up 37.16% of total sales in 2016.

### Q10: What is the quarterly sales distribution?
- Highest sales: Q4 (October–December)
- Lowest sales: Q1 (January–March)

### Q11: What can be predicted about future sales?
- Forecasting models suggest a continued increase in sales, although with low accuracy. For short-term forecasting, the Moving Average method is more appropriate.

### Q12: What is the distribution of Average Order Value (AOV)?
- Skewness: 7.01 (indicates a right-skewed distribution)
- Kurtosis: 78.5 (indicates a highly peaked distribution)
- This implies that 2017 sales data is not normally distributed.

### Q13: Who had the higher AOV in 2017, Chuck Magee or Kelly Williams?
- Chuck Magee (East) had the higher AOV at $231,3604.
- However, a two-sample t-test assuming unequal variances showed no statistically significant difference between the order sales of Chuck Magee and Kelly Williams.

## Conclusion
Based on the analysis:
- 2016 saw significant growth, mainly driven by the Technology category.
- Sales show a seasonal pattern, with Q4 being the strongest.
- Sub-categories like Tables and Supplies need attention due to consistent losses.
- More advanced forecasting models are needed for long-term sales predictions.

