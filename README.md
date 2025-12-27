# 📊 Sales Analysis Dashboard – Amazon Products

## Overview
This Power BI project provides a comprehensive analysis of Amazon product sales using dynamic time intelligence measures. The dashboard visualizes key performance indicators (KPIs), sales trends, product category breakdowns, and customer engagement metrics to support data-driven decision-making.

## 📌 Key Measures Used

| Measure Name         | Description                                                                 | DAX Expression                                                                                          | Format       |
|----------------------|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|--------------|
| **Ytd Sales**         | Calculates total sales year-to-date based on product price.                | `TOTALYTD(SUM(Amazon_Data[Price(Dollar)]), 'Calender Table'[Date])`                                     | Currency     |
| **Qtd Sales**         | Calculates total sales quarter-to-date.                                    | `TOTALQTD(SUM(Amazon_Data[Price(Dollar)]), 'Calender Table'[Date])`                                     | Currency     |
| **Ytd Product Sold**  | Counts the number of products sold year-to-date.                           | `TOTALYTD(COUNT(Amazon_Data[Product Category]), 'Calender Table'[Date])`                                | Whole Number |
| **Ytd Reviews**       | Sums the number of customer reviews year-to-date.                          | `TOTALYTD(SUM(Amazon_Data[Number of reviews]), 'Calender Table'[Date])`                                 | Whole Number |
| **Measure**           | Placeholder measure (not currently defined).                               | *(Empty)*                                                                                                | *(N/A)*      |

## 📈 Visualizations Powered by These Measures

- **Top Metrics Cards**: Display YTD and QTD sales, product count, and review volume.
- **Sales by Month**: Line chart showing monthly sales trends.
- **Weekly Sales Summary**: Bar chart tracking weekly performance.
- **Category Breakdown**: Table showing sales by product category.
- **Top Products**: Bar charts for top products by sales and reviews.

## 🧠 Time Intelligence Logic

All time-based calculations leverage the `'Calender Table'[Date]` column to ensure accurate aggregation across YTD and QTD periods. This enables dynamic filtering and slicing by quarter and category.

## 🛠️ Technical Notes

- **Data Source**: `Amazon_Data` table
- **Calendar Table**: Required for time intelligence functions
- **Format Strings**: Currency measures use custom format strings for clarity
- **Last Modified**: Measures updated on 27 Dec 2025
