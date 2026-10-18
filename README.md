# Power BI Assignment 1 – E-Commerce Sales Analysis

## 1. Data Transformation

### 1.1 Keep First 500 Rows
**Description:** Restricted the List of Orders table to the first 500 rows.

**Explanation:** Used Home → Keep Rows → Keep Top Rows and entered 500.

### 1.2 Change Order Date Data Type
**Description:** Changed Order Date to Date data type.

**Explanation:** Selected Order Date and used Transform → Data Type → Date.

### 1.3 Change Amount and Target Data Types
**Description:** Changed Amount and Target to Fixed Decimal Number.

**Explanation:** Selected each column and changed its data type to Fixed Decimal Number.

### 1.4 Format CustomerName
**Description:** Converted customer names into Proper Case.

**Explanation:** Used Transform → Format → Capitalize Each Word. For example, `rahul kumar` becomes `Rahul Kumar`.

### 1.5 Create Location Column
**Description:** Merged City and State into a new column named Location.

**Explanation:** Used Merge Columns with a comma and space separator to create the format `City, State`.

### 1.6 Create Profit Margin
**Description:** Created a custom column named Profit Margin.

**Explanation:** Used the formula `[Profit] / [Amount]` and changed the column data type to Percentage.

### 1.7 Create Profit Status
**Description:** Created a conditional column named Profit Status based on Profit values.

**Explanation:**
- Profit < 0 → Loss
- Profit = 0 → Break-Even
- Profit > 0 → Profit

## 2. Merging Data (Joins)

- Merged `List of Orders` and `Order Details` using `Order ID`.
- Used **Left Outer Join** in Power Query.
- Expanded the required columns and excluded the duplicate `Order ID` from the expanded columns.
- Renamed the new table to `Orders Data`.

## 3. Handling Missing Data & Duplicates

- Checked missing values using Column Quality.
- Found no missing values or errors in the merged columns.
- Checked for duplicate rows.
- Found no exact duplicate rows in the complete merged dataset.
- Kept repeated-looking records because they differed in other product details.

## 4. Sorting and Filtering Data

- Sorted `Orders Data` by `Order Date` in descending order to analyze recent orders.
- Filtered the `Location` column to `Chennai Tamil Nadu` for regional analysis.

## 5. Grouping and Aggregating Data

- Duplicated `Order Details` and calculated **Average Profit by Category** using Group By.
- Duplicated `Sales target` and calculated **Total Target by Month** using Sum.
- Created summary tables named `Order Details Summary` and `Sales Target Summary`.

## 6. Data Modeling

- Created an active **one-to-many (1:*)** relationship between `List of Orders[Order ID]` and `Order Details[Order ID]`.
- Created an active **many-to-many (*:*)** relationship between `Order Details[Category]` and `Sales target[Category]`.
