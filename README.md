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
