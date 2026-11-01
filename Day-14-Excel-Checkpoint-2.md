# Day 14 — Excel Checkpoint 2

## Overview

Today I completed my second Excel checkpoint as part of my Data Analytics learning journey.

The checkpoint focused on:
- Text cleaning
- TRIM and PROPER
- UPPER and LOWER
- SUM, AVERAGE, MAX and MIN
- COUNTA and COUNTIF
- YEAR, MONTH and DAY
- TEXT and date calculations
- SUMIF and IF
- Monthly sales summaries
- Business observations

---

## Sample Dataset

| Customer | City | Category | Amount | Order Date |
|---|---|---|---:|---|
| ` akanksha ` | raichur | electronics | 25000 | 10-01-2025 |
| `RAHUL` | BENGALURU | Clothing | 1500 | 15-01-2025 |
| ` priya` | hyderabad | ELECTRONICS | 18000 | 05-02-2025 |
| `SNEHA ` | RAICHUR | grocery | 800 | 20-02-2025 |
| `arjun` | bengaluru | CLOTHING | 3000 | 10-03-2025 |
| `KIRAN` | HYDERABAD | Grocery | 1200 | 15-03-2025 |

Assume the original columns are:

- A = Customer
- B = City
- C = Category
- D = Amount
- E = Order Date

Data starts in row 2 and ends in row 7.

---

## A. Text Cleaning

### 1. TRIM()

**Meaning:** Removes unnecessary spaces from text.

Syntax:

```excel
=TRIM(text)
```

Example:

```excel
=TRIM(A2)
```

### 2. PROPER()

**Meaning:** Converts the first letter of each word into uppercase.

Syntax:

```excel
=PROPER(text)
```

Example:

```excel
=PROPER(A2)
```

### 3. UPPER()

**Meaning:** Converts all text into uppercase.

Syntax:

```excel
=UPPER(text)
```

Example:

```excel
=UPPER(C2)
```

### 4. LOWER()

**Meaning:** Converts all text into lowercase.

Syntax:

```excel
=LOWER(text)
```

Example:

```excel
=LOWER(B2)
```

### Practice Tasks and Answers

**Task 1. Remove extra spaces from Customer.**

```excel
=TRIM(A2)
```

**Task 2. Convert Customer names into proper case.**

```excel
=PROPER(TRIM(A2))
```

**Task 3. Standardize City names using proper case.**

```excel
=PROPER(TRIM(B2))
```

**Task 4. Convert Category names into proper case.**

```excel
=PROPER(TRIM(C2))
```

Copy these formulas down for all six records.

Suggested cleaned columns:

| Column | Cleaned data |
|---|---|
| F | Clean Customer |
| G | Clean City |
| H | Clean Category |

---

## B. Formula Practice

### 5. SUM()

**Meaning:** Calculates the total of numbers.

Syntax:

```excel
=SUM(range)
```

Answer:

```excel
=SUM(D2:D7)
```

Expected result: ₹49,500

### 6. AVERAGE()

**Meaning:** Calculates the average of numbers.

Syntax:

```excel
=AVERAGE(range)
```

Answer:

```excel
=AVERAGE(D2:D7)
```

Expected result: ₹8,250

### 7. MAX()

**Meaning:** Finds the highest value.

Syntax:

```excel
=MAX(range)
```

Answer:

```excel
=MAX(D2:D7)
```

Expected result: ₹25,000

### 8. MIN()

**Meaning:** Finds the lowest value.

Syntax:

```excel
=MIN(range)
```

Answer:

```excel
=MIN(D2:D7)
```

Expected result: ₹800

### 9. COUNTA()

**Meaning:** Counts non-empty cells.

Syntax:

```excel
=COUNTA(range)
```

Answer:

```excel
=COUNTA(A2:A7)
```

Expected result: 6 customers.

### 10. COUNTIF()

**Meaning:** Counts cells that match a particular condition.

Syntax:

```excel
=COUNTIF(range, criteria)
```

Answer — Count Electronics orders:

```excel
=COUNTIF(H2:H7,"Electronics")
```

Expected result: 2 orders.

---

## C. Date Cleaning

### 11. YEAR()

**Meaning:** Extracts the year from a date.

Syntax:

```excel
=YEAR(date)
```

Answer:

```excel
=YEAR(E2)
```

Expected result: 2025

### 12. MONTH()

**Meaning:** Extracts the month number from a date.

Syntax:

```excel
=MONTH(date)
```

Answer:

```excel
=MONTH(E2)
```

Expected result: 1 for January.

### 13. DAY()

**Meaning:** Extracts the day from a date.

Syntax:

```excel
=DAY(date)
```

Answer:

```excel
=DAY(E2)
```

Expected result: 10

### 14. TEXT()

**Meaning:** Formats a value, such as a date, into text in a specified format.

Syntax:

```excel
=TEXT(value, format_text)
```

Answer — Display the full month name:

```excel
=TEXT(E2,"mmmm")
```

Expected result: January

Other examples:

```excel
=TEXT(E2,"mmm")
```

Output: Jan

```excel
=TEXT(E2,"yyyy")
```

Output: 2025

### 15. Date subtraction

**Meaning:** Subtracting an earlier date from a later date calculates the number of days between them.

Syntax:

```excel
=End_Date-Start_Date
```

Example:

If F2 contains 10-01-2025 and G2 contains 16-01-2025:

```excel
=G2-F2
```

Expected result: 6 days.

**Important:** The original dataset contains only Order Date, not a second date such as Delivery Date. Therefore, an actual delivery-time calculation requires another date column. Do not subtract the Amount column from the Order Date.

---

## D. Business Analysis

### 16. SUMIF() — Total sales for each city

**Meaning:** Adds values that meet a particular condition.

Syntax:

```excel
=SUMIF(criteria_range, criteria, sum_range)
```

Example — Total sales for Raichur:

```excel
=SUMIF(G2:G7,"Raichur",D2:D7)
```

Expected city summary:

| City | Total sales |
|---|---:|
| Raichur | ₹25,800 |
| Bengaluru | ₹4,500 |
| Hyderabad | ₹19,200 |

### 17. SUMIF() — Total sales for each category

Example — Electronics:

```excel
=SUMIF(H2:H7,"Electronics",D2:D7)
```

Expected category summary:

| Category | Total sales |
|---|---:|
| Electronics | ₹43,000 |
| Clothing | ₹4,500 |
| Grocery | ₹2,000 |

### 18. IF() — Identify orders above ₹5,000

**Meaning:** Checks a condition and returns one result if true and another if false.

Syntax:

```excel
=IF(condition, value_if_true, value_if_false)
```

Answer:

```excel
=IF(D2>5000,"High","Low")
```

Copy down for all orders.

### 19. Monthly Sales Summary

Create a Month column using:

```excel
=TEXT(E2,"mmmm")
```

Copy the formula down.

Then use SUMIF to calculate sales for each month.

Example:

```excel
=SUMIF(I2:I7,"January",D2:D7)
```

Expected monthly summary:

| Month | Total sales |
|---|---:|
| January | ₹26,500 |
| February | ₹18,800 |
| March | ₹4,200 |

---

## 20. Business Observations

Based on the dataset:

**Observation 1:** Electronics generated the highest revenue of ₹43,000 out of total sales of ₹49,500.

**Observation 2:** Raichur generated the highest city-wise sales of ₹25,800, followed by Hyderabad with ₹19,200.

These observations help identify the strongest product category and city in the sample dataset.

---

## Key Learnings

- Cleaned inconsistent text using TRIM and PROPER.
- Standardized names, cities and categories.
- Calculated sales totals and averages.
- Used COUNTIF and COUNTA.
- Extracted year, month and day from dates.
- Created monthly sales summaries.
- Used SUMIF and IF for business analysis.
- Identified useful insights from a dataset.

## Checkpoint Result

**Excel Checkpoint 2 completed.**

This exercise helped me practise data cleaning, formula usage, date handling and basic business analysis using Excel.

#Excel #MicrosoftExcel #DataAnalytics #DataCleaning #DataAnalyst #LearningJourney
