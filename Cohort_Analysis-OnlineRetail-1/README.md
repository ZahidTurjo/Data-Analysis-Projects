# 🧮 Cohort Analysis on Online Retail Dataset

This project performs a **Cohort Analysis** using the famous **Online Retail Dataset** to understand **customer retention patterns** over time.

---

## 📘 Overview

Cohort analysis is a powerful analytical technique that helps businesses understand customer behavior by grouping them into cohorts (e.g., customers who made their first purchase in the same month).  
By tracking how many customers from each cohort remain active over time, we can measure **customer retention and loyalty**.

This project uses Python (Pandas, Matplotlib, and Seaborn) to:
- Identify customer purchase cohorts  
- Calculate retention rates month-over-month  
- Visualize retention using a heatmap  

---

## 📂 Dataset

The dataset used is the **Online Retail dataset**, which contains transactions from a UK-based online store between 2010 and 2011.

 **dataset link**-> https://archive.ics.uci.edu/dataset/352/online+retail

| Column Name | Description |
|--------------|-------------|
| `InvoiceNo` | Invoice number (unique per transaction) |
| `StockCode` | Product code |
| `Description` | Product name |
| `Quantity` | Number of items purchased |
| `InvoiceDate` | Date and time of invoice |
| `UnitPrice` | Price per item |
| `CustomerID` | Unique ID per customer |
| `Country` | Customer’s country |

---

###  Libraries
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```
## Retention Heatmap
<img width="1432" height="743" alt="image" src="https://github.com/user-attachments/assets/977a791f-290a-4737-b6ea-7098ad4449d2" />

## Result Interpretation

- Each row represents a cohort (customers who made their first purchase in the same month).

- Each column shows how many months have passed since their first purchase.

- Each cell shows the retention rate — what percentage of that cohort made a purchase again in that month.


## 🏁 Conclusion

Cohort analysis provides valuable insights into customer retention and behavior over time.
Using this approach, businesses can identify:

- Which customer segments are more loyal,

- When users are most likely to churn,

- How marketing strategies affect retention.



