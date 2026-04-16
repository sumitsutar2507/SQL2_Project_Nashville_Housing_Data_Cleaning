# 🏠 Nashville Housing Data Cleaning (SQL Project)

## 📌 Project Overview
This project focuses on cleaning and preparing raw housing data using SQL.  
The dataset was transformed into a structured and analysis-ready format by applying various data cleaning techniques.

---

## 🧩 Business Problem
Raw housing data often contains:
- Missing values  
- Inconsistent formats  
- Duplicate records  

This makes it difficult to perform accurate analysis and derive insights.

---

## 🎯 Goal
Clean and standardize housing data to make it suitable for data analysis and reporting.

---

## 📊 Dataset Description

The dataset contains housing-related information such as:

- UniqueID  
- ParcelID  
- PropertyAddress  
- SaleDate  
- SalePrice  
- LegalReference  
- OwnerName  
- OwnerAddress  
- Acreage  
- TaxDistrict  
- LandValue  
- BuildingValue  
- TotalValue  
- YearBuilt  
- Bedrooms  
- FullBath  
- HalfBath  
- SoldAsVacant  

---

## 🧹 Data Cleaning Steps

### 🔹 1. Standardizing Date Format
- Converted `SaleDate` to proper date format using `CONVERT()`  
- Removed unnecessary timestamp  

---

### 🔹 2. Handling Missing Property Address
- Filled NULL values using matching `ParcelID`  

---

### 🔹 3. Splitting Address Columns
- Extracted:
  - Property Address  
  - City  
  - State  

Using:
- `SUBSTRING()`  
- `CHARINDEX()`  
- `PARSENAME()`  

---

### 🔹 4. Cleaning 'SoldAsVacant' Field
- Converted:
  - `Y → Yes`  
  - `N → No`  
Using `CASE` statement  OR
We can use `REPLACE` statement

---

### 🔹 5. Removing Duplicates
- Used:
```sql
ROW_NUMBER() OVER (PARTITION BY ... ORDER BY ...)
```
---

### 🔹 6. Delete Unused Columns
- Used `DROP COLUMN` statement

---

## ✅ Final Step
The data has been successfully cleaned and transformed into an analysis-ready format, enabling accurate insights and data-driven decision-making.

---

## 🔍 Key Insights
- Raw housing data contained inconsistencies such as missing values, duplicate records and inconsistent formats  
- Standardizing date formats improved data consistency and usability  
- Splitting address fields into separate columns enhanced data clarity and usability  
- Cleaning categorical values (Yes/No) improved readability and analysis  
- Removing duplicates ensured data accuracy and reliability  

---

## 💼 Business Impact
- Provides a clean and reliable dataset for accurate analysis  
- Improves data quality for reporting and visualization  
- Reduces time required for downstream data processing  
- Enables better decision-making using structured data  

---

## 🛠 Tools Used
- SQL Server (SSMS)  
- SQL  

---

## 📂 Repository Structure
```
nashville-housing-data-cleaning-sql/
│
├── dataset/
│   └── nashville_housing_raw.xlsx
│
├── sql/
│   └── SQLQuery2=Data Cleaning on Nashville Housing Data.sql
│
├── docs/
│   └── data_catalog.md
│
├── README.md
└── .gitignore
```
---

## 🛡️ License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and share this project with proper attribution.

## 🌟 About Me

Hi there! I'm **Sumit Sutar**. An experienced Data Analyst who uncovers hidden trends, patterns and anomalies and leverages business intelligence to generate insights, improve operational efficiency and drive organizational growth.

Let's stay in touch! Feel free to connect with me on the following platforms:

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sumitsutar2507)
