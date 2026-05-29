# <img width="35" height="35" alt="image" src="https://github.com/user-attachments/assets/80b27d26-e168-4a92-8fcd-f7f9f8097ead" /> Customer Behavior Analysis 

This project analyzes customer shopping behavior using transactional data from 3,900 purchases across various product categories. The goal is to uncover insights into spending patterns, customer segments, product preferences, and subscription behavior to guide strategic business decisions.

## 🎥 Demo

![Alt Text](https://github.com/Pradipjagi99/customer-behavior-trend-analysis-sql-python-powerbi/blob/main/Recording%202026-05-28%20201659%20(1).gif)

## ✨ Key Features

📌 **Data Visualization**: Interactive dashboards to provide clear insights into key metrics.

📌 **Trends Analysis**: Identifies performance trends over time.

📌 **Dynamic Reporting**: Easily filterable reports to focus on specific aspects of the dataset.

📌 **KPIs Monitoring**: Highlights the most critical performance indicators.

---

## 🛠️ Tools Used

**Python**: Exploratory Data Analysis using Python.

**SQL**: Data Analysis using SQL (Business Transactions).

**Power BI**: For data modeling, visualization, and dashboard creation.

---

## 🚀 Steps in Project

✔️ Requirement Gathering/Business Requirements
✔️ Exploratory Data Analysis
✔️ Data Import
✔️ Data Walkthrough  
✔️ Data Cleaning/Quality Check 
✔️ Data Connection
✔️ Data Analysis
✔️ Data Modeling  
✔️ Data Processing  
✔️ DAX Calculations  
✔️ Dashboard Lay outing  
✔️ Charts Development and Formatting  
✔️ Dashboard / Report Development  
✔️ Insights Generation

## 🧑‍💼 Business Requirement

A leading retail company wants to better understand its customers' shopping behavior in order
to improve sales, customer satisfaction, and long-term loyalty. The management team has
noticed changes in purchasing patterns across demographics, product categories, and sales
channels (online vs. offline). They are particularly interested in uncovering which factors, such
as discounts, reviews, seasons, or payment preferences, drive consumer decisions and repeat
purchases. 

"How can the company leverage consumer shopping data to identify trends, improve
customer engagement, and optimize marketing and product strategies?"

---

## <img width="28" height="28" alt="image" src="https://github.com/user-attachments/assets/69cdf0b2-f650-4bb9-92a0-dd00b75d0154" /> Exploratory Data Analysis

## <img width="28" height="28" alt="image" src="https://github.com/user-attachments/assets/f1c36522-dba4-470f-94da-b308a20aad60" /> Data Import

- Data Loading: Imported the dataset using pandas.

![Description of the screenshot](https://github.com/Pradipjagi99/customer-behavior-trend-analysis-sql-python-powerbi/blob/main/Images/Python/pyt1.jpg)

## <img width="28" height="28" alt="image" src="https://github.com/user-attachments/assets/9d0eeb64-72c3-4ba5-b79d-f37438f8fe5c" /> Data Walkthrough

- Rows: 3,900
- Columns: 18
- Customer demographics (Age, Gender, Location, Subscription Status)
- Purchase details (Item Purchased, Category, Purchase Amount, Season, Size, Color)
- Shopping behavior (Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type)
- Missing Data: 37 values in Review Rating column

## <img width="28" height="28" alt="image" src="https://github.com/user-attachments/assets/c37e7042-4b39-450e-87bc-52ae0adb7f05" /> Data Cleaning/Quality Check

- Initial Exploration: Used df.info() to check structure and .describe() for summary statistics.

![Description of the screenshot](https://github.com/Pradipjagi99/customer-behavior-trend-analysis-sql-python-powerbi/blob/main/Images/Python/pyt2.jpg)

![Description of the screenshot](https://github.com/Pradipjagi99/customer-behavior-trend-analysis-sql-python-powerbi/blob/main/Images/Python/pyt3.jpg)

- Missing Data Handling: Checked for null values and imputed missing values in the Review Rating column using the median rating of each product category.

![Description of the screenshot](https://github.com/Pradipjagi99/customer-behavior-trend-analysis-sql-python-powerbi/blob/main/Images/Python/pyt4.jpg)

- Column Standardization: Renamed columns to snake case for better readability and documentation.

![Description of the screenshot](https://github.com/Pradipjagi99/customer-behavior-trend-analysis-sql-python-powerbi/blob/main/Images/Python/pyt5.jpg)

- Created age_group column by binning customer ages.

![Description of the screenshot](https://github.com/Pradipjagi99/customer-behavior-trend-analysis-sql-python-powerbi/blob/main/Images/Python/pyt6.jpg)

- Created purchase_frequency_days column from purchase data.

![Description of the screenshot](https://github.com/Pradipjagi99/customer-behavior-trend-analysis-sql-python-powerbi/blob/main/Images/Python/pyt7.jpg)

- Data Consistency Check: Verified if discount_applied and promo_code_used were redundant; dropped promo_code_used.

![Description of the screenshot](https://github.com/Pradipjagi99/customer-behavior-trend-analysis-sql-python-powerbi/blob/main/Images/Python/pyt8.jpg)

## <img width="28" height="30" alt="image" src="https://github.com/user-attachments/assets/4fe9c387-dda0-421f-8264-9eb86f9f4cd1" /> ↔️ <img width="28" height="30" alt="image" src="https://github.com/user-attachments/assets/66fb9e4a-47f2-4e08-8ce2-29d37ae3d6a4" /> Data Connection

- Database Integration: Connected Python script to PostgreSQL and loaded the cleaned DataFrame into the database for SQL analysis.

![Description of the screenshot](https://github.com/Pradipjagi99/customer-behavior-trend-analysis-sql-python-powerbi/blob/main/Images/Python/pyt9.jpg)

---

> [!NOTE]
> Click the dropdown list below for more information on SQL or Power BI.

---

<details>
<summary>SQL <img width="28" height="28" alt="image" src="https://github.com/user-attachments/assets/ee2f380f-d0fc-4898-a809-6d7d7572d768" /> </summary>

## <img width="28" height="30" alt="image" src="https://github.com/user-attachments/assets/b6e94b3a-7abf-4b58-8056-ebc8a94beb70" /> Data Analysis

- performed structured analysis in PostgreSQL to answer key business questions: Revenue by Gender – Compared total revenue generated by male vs. female customers.

![Description of the screenshot](https://github.com/Pradipjagi99/customer-behavior-trend-analysis-sql-python-powerbi/blob/main/Images/SQL/Q1.jpg)

- High-Spending Discount Users – Identified customers who used discounts but still spent above the average purchase amount.

![Description of the screenshot](https://github.com/Pradipjagi99/customer-behavior-trend-analysis-sql-python-powerbi/blob/main/Images/SQL/Q2.jpg)

- Top 5 Products by Rating – Found products with the highest average review ratings.

![Description of the screenshot](https://github.com/Pradipjagi99/customer-behavior-trend-analysis-sql-python-powerbi/blob/main/Images/SQL/Q3.jpg)

- Shipping Type Comparison – Compared average purchase amounts between Standard and Express shipping.

![Description of the screenshot](https://github.com/Pradipjagi99/customer-behavior-trend-analysis-sql-python-powerbi/blob/main/Images/SQL/Q4.jpg)

- Subscribers vs. Non-Subscribers – Compared average spend and total revenue across subscription status.

![Description of the screenshot](https://github.com/Pradipjagi99/customer-behavior-trend-analysis-sql-python-powerbi/blob/main/Images/SQL/Q5.jpg)

- Discount-Dependent Products – Identified 5 products with the highest percentage of discounted purchases.

![Description of the screenshot](https://github.com/Pradipjagi99/customer-behavior-trend-analysis-sql-python-powerbi/blob/main/Images/SQL/Q6.jpg)

- Customer Segmentation – Classified customers into New, Returning, and Loyal segments based on purchase history.

![Description of the screenshot](https://github.com/Pradipjagi99/customer-behavior-trend-analysis-sql-python-powerbi/blob/main/Images/SQL/Q7.jpg)

- Top 3 Products per Category – Listed the most purchased products within each category.

![Description of the screenshot](https://github.com/Pradipjagi99/customer-behavior-trend-analysis-sql-python-powerbi/blob/main/Images/SQL/Q8.jpg)

- Repeat Buyers & Subscriptions – Checked whether customers with >5 purchases are more likely to subscribe.

![Description of the screenshot](https://github.com/Pradipjagi99/customer-behavior-trend-analysis-sql-python-powerbi/blob/main/Images/SQL/Q9.jpg)

- Revenue by Age Group – Calculated total revenue contribution of each age group.

![Description of the screenshot](https://github.com/Pradipjagi99/customer-behavior-trend-analysis-sql-python-powerbi/blob/main/Images/SQL/Q10.jpg)

</details>

---

<details>
    <summary>Power BI <img width="28" height="30" alt="image" src="https://github.com/user-attachments/assets/1500083e-bdef-447f-9461-587caf8c5990" /> </summary>

## <img width="28" height="30" alt="image" src="https://github.com/user-attachments/assets/9bdb0829-fe3d-451e-bca4-215ee422e53b" /> Customer Behavior Analysis Dashboard in Power BI

This Power BI Dashboard provides a comprehensive analysis of Customer Behavior and Subscription status, focusing on revenue by age group, average review rating. The analysis leverages dynamic dashboards, interactive charts, and key performance indicators (KPIs) to identify trends and insights.

## <img width="28" height="30" alt="image" src="https://github.com/user-attachments/assets/0d84fcf0-ed8b-4f45-8562-bfa71f9a93c5" /> KPI’s Requirements

**1. Number of Customer:** The total count of different customers.

**2. Average Purchase Amount:** The average of the purchase amount.

**3. Average Review Rating:** The average of the review rating.

---

![Description of the screenshot](https://github.com/Pradipjagi99/customer-behavior-trend-analysis-sql-python-powerbi/blob/main/Images/PowerBI/pbi1.jpg)

---

## <img width="28" height="30" alt="image" src="https://github.com/user-attachments/assets/cfa5bf02-459a-4151-9654-1752bdb43139" /> Chart’s Requirements






