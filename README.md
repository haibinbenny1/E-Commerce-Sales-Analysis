# Power BI Assignment 1 – E-Commerce Sales Analysis

## Data Transformation

### 1. Keep First 500 Rows
**Description:** Restricted the List of Orders table to the first 500 rows.

**Explanation:** Used Home → Keep Rows → Keep Top Rows and entered 500.

### 2. Change Order Date Data Type
**Description:** Changed Order Date to Date data type.

**Explanation:** Selected Order Date and used Transform → Data Type → Date.

### 3. Change Amount and Target Data Types
**Description:** Changed Amount and Target to Fixed Decimal Number.

**Explanation:** Selected each column and changed its data type to Fixed Decimal Number.

### 4. Format CustomerName
**Description:** Converted customer names into Proper Case.

**Explanation:** Used Transform → Format → Capitalize Each Word. For example, `rahul kumar` becomes `Rahul Kumar`.

### 5. Create Location Column
**Description:** Merged City and State into a new column named Location.

**Explanation:** Used Merge Columns with a comma and space separator to create the format `City, State`.

### 6. Create Profit Margin
**Description:** Created a custom column named Profit Margin.

**Explanation:** Used the formula `[Profit] / [Amount]` and changed the column data type to Percentage.

### 7. Create Profit Status
**Description:** Created a conditional column named Profit Status based on Profit values.

**Explanation:**
- Profit < 0 → Loss
- Profit = 0 → Break-Even
- Profit > 0 → Profit
