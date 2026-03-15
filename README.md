# AdventureWorks Sales Analysis – Power BI Project

## Project Overview

This project analyzes sales performance for AdventureWorks using Microsoft Power BI.
The goal is to demonstrate core data analysis skills including data modeling, DAX calculations, and business insights through interactive reporting.

The report focuses on understanding yearly sales trends and cumulative sales growth to support better business decision-making.

---

## Business Scenario

AdventureWorks, a global bicycle manufacturer, wants to analyze its historical sales performance.

The company is interested in understanding:

* How sales have evolved year over year
* The cumulative growth of sales over time
* Revenue generated from product sales

By analyzing these metrics, business leaders can evaluate sales performance and identify long-term trends.

---

## Tools & Technologies

* Microsoft Power BI
* DAX (Data Analysis Expressions)
* Data Modeling
* Data Visualization

---

## Dataset

The project uses the AdventureWorks dataset which contains the following tables:

* Sales
* Products
* Date
* Region
* Salesperson

These tables allow analysis of sales across time, products, and geographic regions.

---

## Data Preparation & Validation

Before analysis, the dataset was reviewed to ensure accuracy and consistency.

Data validation steps included:

* Reviewing table relationships in the data model
* Confirming appropriate data types for columns
* Verifying sales values and calculated measures
* Ensuring correct date hierarchy for time-based analysis

---

## Key Measures Created

### Total Revenue

Calculates total revenue using quantity and cost for each transaction.

DAX formula:

```
Total Revenue =
SUMX(
    Sales,
    Sales[Quantity] * Sales[Cost]
)
```

---

### Running Total in Year

Calculates cumulative sales over time to track sales growth.

This measure was created using Power BI Quick Measures.

Example logic:

```
Running Total in Year =
CALCULATE(
    SUM(Sales[Total Sales]),
    FILTER(
        ALLSELECTED(Date[Year]),
        ISONORAFTER(Date[Year], MAX(Date[Year]), DESC)
    )
)
```

---

## Key Insights

The analysis highlights several trends:

* Sales show a consistent cumulative growth across years.
* Revenue generated from product sales significantly exceeds recorded sales values due to quantity-cost calculations.
* Running totals provide a clear view of long-term sales performance.

These insights help businesses understand overall revenue growth and evaluate yearly performance.

---


## Skills Demonstrated

This project demonstrates the following data analyst skills:

* Data modeling in Power BI
* Writing DAX measures
* Using iterator functions such as SUMX
* Creating running totals
* Data validation and reporting
* Business-oriented data storytelling

---

## Author

Vidya V.G.
Aspiring Data Analyst
