# Task 6: Sales Trend Analysis Using Aggregations

##  Objective

Analyze monthly revenue and order volume from the `online_sales` dataset using SQL aggregation techniques. The analysis includes breaking down sales by month and year, calculating revenues, counting orders, and filtering based on time periods.

---

##  Tools Used

- **Database:** MySQL
- **Client:** MySQL Workbench
- **Output Format:** PDF (with SQL scripts and result tables as screenshots)

---

##  Analysis Breakdown

### A. Extract Month from `order_date`
Extracted the month number using:
```sql
EXTRACT(MONTH FROM order_date)
```

### B. Group By Year and Month
Grouped data using:
```sql
GROUP BY EXTRACT(YEAR FROM order_date), EXTRACT(MONTH FROM order_date)
```

### C. Calculate Total Revenue
Used `SUM(amount)` to find total revenue per month.

### D. Count Total Orders
Used `COUNT(DISTINCT order_id)` to calculate order volume.

### E. Sort Results
Sorted the data in chronological order using:
```sql
ORDER BY year ASC, month ASC
```

### F. Filter by Time Period
Restricted results to the year 2023 using:
```sql
WHERE order_date BETWEEN '2023-01-01' AND '2023-12-31'
```

##  Deliverables

- SQL scripts for each task (A–F)
- Result tables as screenshots in the PDF
