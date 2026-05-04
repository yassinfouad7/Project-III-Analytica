# Talabat Delivery Orders Analysis

A data analysis project focused on exploring Talabat food delivery orders to understand delivery performance, customer behavior, and the factors that may influence order outcomes.

This project applies exploratory data analysis, data visualization, and statistical hypothesis testing on a Talabat delivery dataset containing order, customer, restaurant, driver, payment, traffic, and delivery-related variables.

## Project Overview

Food delivery platforms depend heavily on speed, reliability, and customer satisfaction. This project investigates delivery order data to identify patterns in delivery duration, payment behavior, traffic conditions, customer demand, and order pricing.

The main research question is:

**What factors influence delivery performance and customer behavior in Talabat food delivery orders?**

The analysis is based on a dataset containing **100,000 total orders**, with **10,000 samples analyzed** and **23 variables** covering different parts of the delivery process, including order details, delivery time, distance, city, payment method, traffic level, and driver information. :contentReference[oaicite:0]{index=0}

## Dataset Description

The dataset includes the following main features:

- `Order_ID`: Unique identifier for each order
- `User_ID`: Unique identifier for each customer
- `Restaurant_ID`: Restaurant identifier
- `Driver_ID`: Driver identifier
- `Item_Name`: Ordered food item
- `Quantity`: Number of ordered items
- `Total_Price`: Total order cost
- `Order_Time`: Time when the order was placed
- `Delivery_Time`: Time when the order was delivered
- `Delivery_Duration_Minutes`: Delivery duration in minutes
- `City`: City where the order was placed
- `Payment_Method`: Cash, Wallet, or Credit Card
- `Order_Status`: Delivered, Cancelled, or In Transit
- `Driver_Vehicle`: Car, Motorbike, or Bicycle
- `Delivery_Distance_km`: Distance between restaurant and customer
- `Traffic_Level`: Low, Medium, or High traffic
- `Driver_Availability`: Driver online/offline status

## Tools and Libraries Used

The project was developed in Python using common data analysis libraries:

- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy

These libraries were used for data cleaning, exploration, visualization, and statistical testing.

## Analysis Performed

The notebook includes several stages of analysis:

### 1. Data Exploration

Initial exploration was performed to understand the dataset structure, column types, distributions, and overall quality. The dataset was found to be clean and balanced, with no major missing-value issues reported. :contentReference[oaicite:1]{index=1}

### 2. Visual Analysis

Several visualizations were created to better understand the data, including:

- Number of orders by city
- Payment method distribution
- Order status distribution
- Traffic level distribution
- Total price distribution
- Delivery duration distribution
- Total price by quantity
- Delivery duration by traffic level
- Delivery duration by vehicle type
- Orders by hour of day
- Orders by day of week
- Correlation heatmap

The visual analysis showed that orders were fairly evenly distributed across cities, payment methods were almost equally used, and most orders were successfully delivered. :contentReference[oaicite:2]{index=2}

### 3. Hypothesis Testing

Five hypothesis tests were conducted using a significance level of `α = 0.05`.

| Test | Method | Result |
|---|---|---|
| Delivery Duration vs 35 minutes | One-sample t-test | Reject H0 |
| Traffic Level vs Delivery Duration | One-way ANOVA | Fail to reject H0 |
| Payment Method vs Order Status | Chi-square test | Fail to reject H0 |
| Delivery Distance vs Delivery Duration | Pearson correlation | Fail to reject H0 |
| Quantity vs Total Price | Pearson correlation | Reject H0 |

The results showed that delivery duration is significantly greater than 35 minutes, and quantity has a significant effect on total price. However, traffic level, delivery distance, and payment method did not show statistically significant relationships with the tested outcomes. :contentReference[oaicite:3]{index=3}

## Key Findings

- Delivery durations are generally consistent but exceed the 35-minute benchmark.
- Quantity is strongly related to total order price.
- Traffic level does not significantly affect delivery duration in this dataset.
- Delivery distance does not show a significant correlation with delivery time.
- Payment method does not appear to influence order status.
- Orders are fairly balanced across cities and days of the week.
- Most orders are successfully delivered, indicating a high completion rate.

## Limitations

Although the dataset is useful for practicing data analysis techniques, some limitations should be considered:

- The dataset may be synthetic or simulated.
- Some relationships are weaker than expected in real-world delivery data.
- Distance and delivery duration would normally be expected to have a stronger relationship.
- The dataset is unusually clean, with no major missing data issues.
- Category distributions are very balanced, which may not fully reflect real customer behavior. :contentReference[oaicite:4]{index=4}

## Conclusion

This project shows how data analysis can be used to evaluate food delivery performance and customer behavior. The main insight is that delivery times consistently exceed the 35-minute benchmark, while common assumptions such as traffic level and delivery distance affecting delivery duration were not supported by the statistical tests in this dataset.

Overall, the analysis suggests that operational factors beyond traffic and distance, such as restaurant preparation time or driver dispatch efficiency, may have a stronger impact on delivery performance.
