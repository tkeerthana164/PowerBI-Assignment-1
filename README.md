# Power BI Assignment 1

## 📊 Overview

This project was completed as part of my Data Analytics learning journey using **Microsoft Power BI** and **Power Query**.

The assignment focused on preparing, transforming, cleaning, merging, analyzing, and modeling sales-related data to create a structured dataset ready for analysis.

---

## 🛠️ Tools Used

- Microsoft Power BI
- Power Query
- Power BI Data Modeling

---

## 🔄 1. Data Transformation

The following transformations were performed using Power Query:

- Restricted the **List of Orders** table to the first **500 rows**.
- Ensured the **Order Date** column was set to the **Date** data type.
- Changed the **Amount** and **Target** columns to **Fixed Decimal Number**.
- Formatted the **CustomerName** column using **Proper Case** for consistent capitalization.
- Created a new **Location** column in the format:
  
  `City, State`

- Created a custom **Profit Margin** column using:

  `Profit ÷ Amount`

- Formatted **Profit Margin** as a percentage.
- Created a conditional **Profit Status** column:
  - Profit < 0 → **Loss**
  - Profit = 0 → **Break-Even**
  - Profit > 0 → **Profit**

---

## 🔗 2. Merging Data (Joins)

The **List of Orders** and **Order Details** tables were merged using the common **Order ID** column.

A new table named:

`Orders Data`

was created from the merged data.

---

## 🧹 3. Handling Missing and Duplicate Data

### Missing Data

The data was checked using Power Query's **Column Quality** feature.

All columns contained **100% valid values** with no errors or empty values, so no missing-value treatment was required.

### Duplicate Data

Duplicate records were checked across all columns.

Repeated **Order IDs** were not considered duplicates because a single order can contain multiple order-detail records.

No completely identical rows were found, so no duplicate records were removed.

---

## 🔎 4. Sorting and Filtering Data

Sorting and filtering were performed on the **Orders Data** table.

### Sorting

The orders were sorted by **Order Date in descending order** to focus on recent orders and trends.

### Filtering

The data was filtered using the **State** column to focus specifically on:

`Tamil Nadu`

This was done for regional analysis.

---

## 📈 5. Grouping and Aggregating Data

### Order Details Analysis

A duplicate of the **Order Details** table was created for analysis.

The data was grouped by **Category** and the **Average Profit** was calculated.

The resulting categories were:

- Furniture
- Clothing
- Electronics

### Sales Target Analysis

A duplicate of the **Sales Target** table was created.

The data was grouped by **Month of Order Date**, and the **Total Target** amount was calculated using the Sum aggregation.

---

## 🧩 6. Data Modeling

Relationships were established between the required tables using Power BI's **Manage Relationships** feature.

### Relationship 1 — Order ID

**List of Orders** → **Order Details**

Relationship based on:

`Order ID`

Cardinality:

`One-to-Many (1:*)`

The relationship was kept **active**.

### Relationship 2 — Category

**Order Details** → **Sales Target**

Relationship based on:

`Category`

Cardinality:

`Many-to-Many (*:*)`

The relationship was kept **active**.

---

## 📁 Tables Created / Used

The project contains the following tables and analysis tables:

- **List of Orders**
- **Order Details**
- **Sales Target**
- **Orders Data**
- **Order Details Analysis**
- **Sales Target Analysis**

---

## 🎯 Key Skills Practiced

Through this assignment, I practiced:

- Data transformation using Power Query
- Data type management
- Proper case text transformation
- Custom columns
- Conditional columns
- Percentage calculations
- Merging tables using keys
- Missing-value validation
- Duplicate-data checking
- Sorting and filtering
- Grouping and aggregation
- Average and Sum calculations
- Creating relationships
- Understanding cardinality
- Power BI data modeling

---

## 📌 Project Status

**Assignment 1 — Completed ✅**

This project helped me gain practical experience in preparing and modeling data in Power BI before moving towards visualization and dashboard development.
