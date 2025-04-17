# 🛒 Building a Retail Data Pipeline (Walmart Sales Analysis)

Walmart is the largest retail store in the United States. Like many companies, it has been expanding its e-commerce operations. By the end of 2022, e-commerce accounted for $80 billion in sales—13% of Walmart’s total revenue. Public holidays such as the Super Bowl, Labor Day, Thanksgiving, and Christmas significantly affect these sales trends.

This project involves building a **data pipeline** to analyze the impact of public holidays on Walmart’s supply and demand, using two datasets: one from a `.csv` file and another from a `.parquet` file.

---

## 📁 Project Overview

The pipeline includes:

1. **Reading** sales data from a `.csv` file and complementary data from a `.parquet` file
2. **Merging** and cleaning the datasets
3. **Transforming** the data by extracting necessary features
4. **Aggregating** monthly sales data
5. **Saving** the cleaned and aggregated data to new `.csv` files

---

## 🗃️ Datasets

### 1. `grocery_sales.csv`
- `index`: Unique row identifier  
- `Store_ID`: Store number  
- `Date`: Week of sales  
- `Weekly_Sales`: Weekly sales amount  

### 2. `extra_data.parquet`
- `IsHoliday`: Whether the week contains a public holiday (1 = Yes, 0 = No)  
- `Temperature`: Temperature during the week  
- `Fuel_Price`: Regional fuel price  
- `CPI`: Consumer Price Index  
- `Unemployment`: Unemployment rate  
- `MarkDown1`, `MarkDown2`, `MarkDown3`, `MarkDown4`: Promotional markdowns  
- `Dept`: Department number  
- `Size`: Size of the store  
- `Type`: Type of store (based on size)  

---

## 🧼 Cleaned Data Columns (`clean_data.csv`)

After merging and cleaning, the resulting dataset contains:

- `Store_ID`  
- `Month`
- `Date`
- `Dept`  
- `IsHoliday`  
- `Weekly_Sales`  
- `CPI`  
- `Unemployment`  

---

## 📊 Aggregated Monthly Sales (`agg_data.csv`)

Sales are aggregated on a monthly level. Example output:

| Month | Weekly_Sales     |
|-------|------------------|
| 1.0   | 33,174.18        |
| 2.0   | 34,333.33        |
| ...   | ...              |

---

## 🧪 Technologies Used

- **Python**
- **Pandas**
- **NumPy**
- **Parquet**
- **Jupyter Notebook** 

---



