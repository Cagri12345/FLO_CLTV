# Customer Lifetime Value (CLTV) Prediction with BG-NBD and Gamma-Gamma Models

## Project Overview
This project uses BG-NBD (Beta Geometric / Negative Binomial Distribution) and Gamma-Gamma models to predict the Customer Lifetime Value (CLTV) of a company's current customers. By analyzing customer purchasing behaviors, the goal is to predict their future potential value and help optimize marketing and customer retention strategies.

## Business Problem
FLO aims to optimize its sales and marketing strategies by analyzing the future potential value of its customers. To make medium- and long-term plans, the company needs to predict the future purchases and total value of its current customers.

## Dataset Description
The dataset consists of information derived from the purchasing behavior of customers who made purchases in both online and offline channels during 2020-2021. Key variables include:
- `master_id`: Unique customer ID
- `order_channel`: The platform used for shopping (e.g., Android, iOS, Desktop, Mobile, Offline)
- `first_order_date`: The date of the customer's first purchase
- `last_order_date`: The date of the customer's last purchase
- `order_num_total_ever_online`: Total number of purchases made by the customer online
- `order_num_total_ever_offline`: Total number of purchases made by the customer offline
- `customer_value_total_ever_online`: Total amount spent by the customer on online purchases
- `customer_value_total_ever_offline`: Total amount spent by the customer on offline purchases
- `interested_in_categories_12`: The list of categories the customer was interested in during the last 12 months

## Methods Used
This project utilizes the following techniques and models:
1. **BG-NBD Model (Beta Geometric / Negative Binomial Distribution)**: This model is used to predict how many times a customer will make a purchase in the future.
2. **Gamma-Gamma Model**: This model is used to predict how much a customer will spend on average per transaction.
3. **Customer Segmentation**: Customers are segmented into four groups (A, B, C, D) based on their CLTV scores, allowing for targeted marketing strategies.

## Steps
1. **Data Cleaning and Preprocessing**: Outliers were handled, and new features such as total purchase count and total spending were created.
2. **Feature Engineering**: Key metrics like `Recency`, `Frequency`, and `Monetary` were calculated for CLTV prediction.
3. **Modeling**:
   - The BG-NBD model was trained to predict future purchases.
   - The Gamma-Gamma model was used to predict the average spend per transaction.
4. **CLTV Calculation**: CLTV predictions for each customer were made for a 6-month period.
5. **Customer Segmentation**: Customers were grouped into four segments based on their CLTV scores.

## Results
This project provides CLTV predictions for each customer and segments them based on their potential value:

- **Segment A**: High-value customers (loyalty programs and personalized offers should be targeted)
- **Segment B & C**: Medium-value customers (discounts and incentive programs can help move them to higher segments)
- **Segment D**: Low-value customers (special campaigns should be run to prevent churn)

## Conclusion
By utilizing BG-NBD and Gamma-Gamma models, this project helps companies predict customer behaviors and optimize marketing strategies. The approach can be applied across various industries to improve customer retention and sales optimization.
