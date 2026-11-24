
# Superstore Sales and Profitability Analysis | Power BI

## 📌 Project Overview

This project focuses on analyzing the sales and profitability of a Superstore business using **Power BI**.

The objective is to understand business performance, identify sales trends, analyze product profitability, and generate meaningful insights that can help improve business decision-making.

An interactive two-page Power BI dashboard was developed to explore sales performance, customer segments, regional sales, product profitability, and loss-making products.

## 🎯 Project Objectives

- Analyze overall sales and profit performance.
- Identify sales trends over time.
- Compare sales across product categories and regions.
- Understand customer segment contributions.
- Identify profitable and loss-making sub-categories.
- Analyze the relationship between sales, profit, and discounts.
- Identify top-performing and bottom-performing products.
- Generate actionable business insights.

## 🛠️ Tools and Technologies

- **Power BI Desktop** – Dashboard development and data visualization
- **DAX** – Data analysis and calculated measures
- **Microsoft Excel / CSV** – Dataset preparation

## 📂 Dataset

The project uses the Sample Superstore dataset.

The dataset contains information about:

- Order Date
- Ship Date
- Product Name
- Category
- Sub-Category
- Sales
- Profit
- Quantity
- Discount
- Region
- Segment
- State

## 🧹 Data Preparation

The dataset was prepared before creating the dashboard.

The preparation process included:

- Inspecting the dataset
- Checking data types
- Identifying missing and null values
- Checking duplicate records
- Verifying numerical columns
- Ensuring date fields were correctly formatted
- Preparing the dataset for analysis

## 📊 DAX Measures

The following DAX measures were created to analyze business performance.

### Total Sales

```DAX
Total Sales = SUM(Superstore[Sales])
```

### Total Profit

```DAX
Total Profit = SUM(Superstore[Profit])
```

### Total Orders

```DAX
Total Orders = DISTINCTCOUNT(Superstore[Order ID])
```

### Total Quantity

```DAX
Total Quantity = SUM(Superstore[Quantity])
```

### Profit Margin

```DAX
Profit Margin =
DIVIDE([Total Profit], [Total Sales], 0)
```

### Average Order Value

```DAX
Average Order Value =
DIVIDE([Total Sales], [Total Orders], 0)
```

### Loss-Making Orders

```DAX
Loss-Making Orders =
CALCULATE(
    [Total Orders],
    FILTER(
        VALUES(Superstore[Order ID]),
        CALCULATE([Total Profit]) < 0
    )
)
```

### Average Discount

```DAX
Average Discount =
AVERAGE(Superstore[Discount])
```

## 📈 Dashboard Overview

The Power BI report contains two interactive dashboard pages.

### Page 1: Sales Performance
<img width="1920" height="1080" alt="Screenshot 2026-11-24 231256" src="https://github.com/user-attachments/assets/29a2b3ef-f5f8-42da-b955-bd34127bdd59" />


This page provides an overview of the business's sales performance.

#### KPI Cards

- Total Sales
- Total Profit
- Total Orders
- Profit Margin

#### Visualizations

- Sales Trend Over Time – Line Chart
- Sales by Region – Bar Chart
- Sales by Category – Bar Chart
- Sales by Customer Segment – Donut Chart

#### Interactive Slicers

- Year
- Region
- Category

These slicers allow users to explore sales performance across different years, regions, and product categories.

### Page 2: Profitability Analysis
<img width="1920" height="1080" alt="Screenshot 2026-11-24 231303" src="https://github.com/user-attachments/assets/691519dc-a76f-4ed1-bd9d-a23f8a9ad799" />

This page focuses on product profitability and identifying areas of business loss.

#### Visualizations

- Profit by Sub-Category – Bar Chart
- Sales vs Profit – Scatter Chart
- Discount vs Profit – Scatter Chart
- Profit by State – Bar Chart
- Top 10 Products by Profit – Bar Chart
- Bottom 10 Products by Profit – Bar Chart

## 🔍 Key Business Questions

The dashboard helps answer the following questions:

1. How much total sales and profit did the business generate?
2. How have sales changed over time?
3. Which product category generates the highest sales?
4. Which region contributes the most revenue?
5. Which customer segment contributes the most sales?
6. Which sub-categories generate the highest profit?
7. Which products are loss-making?
8. Are high-sales products also highly profitable?
9. Is there an association between discounts and profitability?
10. Which states contribute the most profit?

## 💡 Business Insights

The dashboard can be used to identify:

- Sales growth and declining sales periods
- High-performing product categories
- Regional sales and profitability differences
- Products with high sales but low profit
- Loss-making sub-categories
- Products contributing significantly to profit
- Potential relationships between discount levels and profitability

Business insights and recommendations should be based on the actual results observed in the dashboard.

## 💼 Business Recommendations

Based on the findings from the analysis, the business can:

- Focus on products with strong profitability.
- Review pricing and discount strategies for low-profit products.
- Investigate loss-making sub-categories.
- Compare regional performance to identify improvement opportunities.
- Monitor sales and profit trends regularly.
- Improve decision-making using interactive data visualization.

## 📌 Conclusion

This project demonstrates the use of Power BI to transform retail sales data into an interactive business intelligence dashboard.

By analyzing sales trends, regional performance, customer segments, and product profitability, the project provides a structured approach to understanding business performance and supporting data-driven decision-making.

---

