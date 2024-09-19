# E-Commerce Customer Segmentation

## Project Overview
This project aims to analyze and segment e-commerce customers using transactional and demographic data. The main objective is to better understand customer behavior, including coupon usage, demographic insights, and geographical distribution. These insights will help businesses personalize marketing strategies and optimize coupon distribution.

## Dataset Description
The dataset is divided into six sheets, each containing information about various aspects of customer interaction within an e-commerce platform:

1. **Customers:**  
   Contains customer details such as customer ID, join date, city, and gender.
   
2. **Genders:**  
   Provides gender-related information with gender ID and name.
   
3. **Cities:**  
   Lists the city information with city ID and city name.
   
4. **Transactions:**  
   Contains transaction-related details, including transaction date, status (coupon burnt or not), and branch ID.
   
5. **Branches:**  
   Contains branch details such as branch ID and associated merchant.
   
6. **Merchants:**  
   Lists merchant information, including merchant ID and merchant name.

## Preprocessing Steps
The dataset underwent various cleaning and preprocessing stages to ensure analysis accuracy:

1. **Duplicate Removal:**  
   Duplicates were removed from all the sheets to prevent data redundancy.

2. **Missing Value Handling:**  
   - For numerical columns, missing values were filled using the column mean.
   - For categorical columns, missing values were filled with 'Unknown.'

3. **Date Formatting:**  
   Relevant date columns such as `join_date`, `transaction_date`, and `burn_date` were converted to datetime format.

4. **Merging Sheets:**  
   - Customers were merged with gender and city data to create a holistic demographic profile.
   - Transactions were merged with branch and city data to allow for geographical and branch-level analysis.

## Model Approach
### Exploratory Data Analysis (EDA)
- **Demographic Insights:**  
  Merged the customers with gender and city information to understand customer distribution across demographics.
  
- **Coupon Usage Over Time:**  
  The transactions data was grouped by transaction date (on a monthly basis) and transaction status to analyze coupon usage patterns over time.
  
- **City and Branch Analysis:**  
  A merged dataset between transactions, branches, and cities was created to analyze how coupon usage varies across different cities and branches.

### Segmentation and Visualization
Power BI or other visualization tools can be used for segmentation and deeper analysis, including:
- Customer segmentation based on geographical data.
- Time series analysis of coupon usage trends.
- Gender-based customer behavior analysis.

## Evaluation Metrics
The following key evaluation metrics are considered:
- **Coupon Burn Rate:**  
  The percentage of coupons that were successfully redeemed (burned).
  
- **Customer Retention:**  
  The number of repeat customers based on transaction data.

- **Geographical Distribution:**  
  Analyzing which cities and branches have the highest customer engagement and coupon redemption rates.

## Key Findings
- **Coupon Usage:**  
  Coupon usage trends reveal periods of high activity, likely coinciding with marketing campaigns or seasonal offers.
  
- **Geographical Insights:**  
  Some cities have a significantly higher rate of coupon redemption, which could be linked to local campaigns or customer behavior trends.

- **Branch Insights:**  
  Certain branches and merchants show higher customer engagement, providing an opportunity for targeted promotions.

## Customer Segmentation Findings:

- **Cluster 1:** Customers who frequently claim but rarely burn coupons. These customers may require more engaging offers to incentivize them to utilize their coupons.

- **Cluster 2:** Customers who burn most of the coupons they claim. They are highly engaged and should be rewarded with exclusive deals to increase their loyalty.

- **Cluster 3:** Newer customers who have not yet utilized many coupons. These customers could benefit from onboarding incentives to increase engagement.

- **Cluster 4:** Long-term customers with low engagement. Strategies such as personalized offers may help re-engage these customers.




## Conclusion
This project helps e-commerce platforms better understand their customer base by analyzing transactional, demographic, and geographical data. The insights derived can inform more effective marketing strategies, optimize coupon distribution, and personalize customer engagement.
