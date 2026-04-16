# 📊 Data Catalog – Nashville Housing Data Cleaning Project

## 📌 Overview
This document provides detailed information about the Nashville Housing dataset used in the data cleaning project. It includes column definitions, data types, and transformations applied to prepare the dataset for analysis.

---

## 🗂 Dataset: Nashville Housing Data

### 📊 Description
The dataset contains property sales data, including property details, owner information, and transaction values. It was cleaned and transformed using SQL to improve data quality and usability.

---

## 📑 Columns

| Column Name       | Data Type   | Description |
|------------------|------------|-------------|
| UniqueID         | Integer     | Unique identifier for each record |
| ParcelID         | Text        | Unique identifier for each property |
| PropertyAddress  | Text        | Address of the property |
| SaleDate         | Date        | Date when the property was sold |
| SalePrice        | Numeric     | Sale price of the property |
| LegalReference   | Text        | Legal reference for the transaction |
| OwnerName        | Text        | Name of the property owner |
| OwnerAddress     | Text        | Address of the owner |
| Acreage          | Numeric     | Size of the land |
| TaxDistrict      | Text        | Tax district of the property |
| LandValue        | Numeric     | Value of the land |
| BuildingValue    | Numeric     | Value of the building |
| TotalValue       | Numeric     | Total property value |
| YearBuilt        | Integer     | Year the property was built |
| Bedrooms         | Integer     | Number of bedrooms |
| FullBath         | Integer     | Number of full bathrooms |
| HalfBath         | Integer     | Number of half bathrooms |
| SoldAsVacant     | Categorical | Indicates if the property was vacant (Yes/No) |

---

## 🔄 Data Cleaning & Transformations

| Transformation Type       | Description |
|--------------------------|------------|
| Date Standardization     | Converted SaleDate to proper date format using `CONVERT()` |
| Missing Data Handling    | Filled NULL PropertyAddress using matching ParcelID |
| Address Splitting        | Split PropertyAddress into Address, City, and State |
| Owner Address Splitting  | Extracted Owner Address into Address, City, State |
| Data Standardization     | Converted 'Y' and 'N' in SoldAsVacant to 'Yes' and 'No' |
| Duplicate Removal        | Removed duplicate records using CTE and ROW_NUMBER() |
| Column Cleanup           | Dropped unnecessary or redundant columns |

---

## 📊 Derived Columns

| Column Name         | Description |
|--------------------|------------|
| PropertySplitAddress | Extracted street address |
| PropertySplitCity    | Extracted city |
| OwnerSplitAddress    | Owner street address |
| OwnerSplitCity       | Owner city |
| OwnerSplitState      | Owner state |

---

## 🔗 Data Relationships

| Key Column | Description |
|-----------|------------|
| ParcelID  | Used to identify duplicate and related property records |

---

## ⚠️ Data Notes

- Original dataset contained duplicate and missing records  
- Address fields were unstructured and required parsing  
- Some columns were removed after cleaning to reduce redundancy  

---

## 🎯 Purpose of Dataset

The cleaned dataset is used to:
- Perform accurate housing market analysis  
- Enable better reporting and visualization  
- Support data-driven decision-making in real estate  

---

## 💡 Tools Used

- SQL Server (SSMS)  
- SQL (Data Cleaning & Transformation)  
