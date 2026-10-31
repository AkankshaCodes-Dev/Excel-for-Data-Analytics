# 📗 Day 13 — Excel Date Functions

## 🎯 Learning Objectives

In Day 13, I learned how to work with dates in Microsoft Excel using date functions and basic date calculations.

I practiced extracting years, months and days, calculating date differences, and creating separate date columns for data analysis.

Date functions are useful for analyzing sales trends, order history, delivery times and business performance.

## 1. What Are Dates in Excel?

Dates represent a particular day, month and year.

Examples:
- `10-01-2025`
- `15-02-2025`
- `31-12-2025`

Excel stores recognized dates internally as serial numbers, which allow calculations between dates.

**Example:**

| Date | Meaning |
|---|---|
| 10-01-2025 | 10 January 2025 |
| 15-02-2025 | 15 February 2025 |
| 31-12-2025 | 31 December 2025 |

**Use case:** Recording transaction dates, order dates and delivery dates.

## 2. YEAR() — Extract the Year

**Meaning:** YEAR() extracts the year from a date.

**Syntax:**
```excel
=YEAR(serial_number)
```

**Example:**

Suppose cell A2 contains `10-01-2025`.

```excel
=YEAR(A2)
```

**Output:** `2025`

**Use case:** Creating a separate year column for yearly analysis.

## 3. MONTH() — Extract the Month

**Meaning:** MONTH() extracts the month number from a date.

**Syntax:**
```excel
=MONTH(serial_number)
```

**Example:**

Suppose A3 contains `20-01-2025`.

```excel
=MONTH(A3)
```

**Output:** `1`

**Month number reference:**

| Month | Number |
|---|---:|
| January | 1 |
| February | 2 |
| March | 3 |
| April | 4 |
| May | 5 |
| June | 6 |
| July | 7 |
| August | 8 |
| September | 9 |
| October | 10 |
| November | 11 |
| December | 12 |

**Use case:** Creating monthly sales reports.

## 4. DAY() — Extract the Day

**Meaning:** DAY() extracts the day of the month from a date.

**Syntax:**
```excel
=DAY(serial_number)
```

**Example:**

Suppose A4 contains `05-02-2025`.

```excel
=DAY(A4)
```

**Output:** `5`

**Use case:** Analyzing transactions based on the day of the month.

## 5. Date Subtraction — Calculate Date Differences

**Meaning:** Subtracting one valid Excel date from another calculates the number of days between them.

**Syntax:**
```excel
=End_Date-Start_Date
```

**Example:**

| Cell | Date |
|---|---|
| A2 — Order Date | 01-01-2025 |
| B2 — Delivery Date | 06-01-2025 |

Formula:

```excel
=B2-A2
```

**Output:** `5`

**Explanation:**
- Order date = 1 January.
- Delivery date = 6 January.
- Difference = 5 days.

**Use case:** Calculating delivery time and order processing duration.

**Important:** The end date should normally be later than the start date. A negative result means the dates are reversed.

## 6. TODAY() — Get the Current Date

**Meaning:** TODAY() returns the current date based on your computer's date.

**Syntax:**
```excel
=TODAY()
```

**Example:**

If today's date is 31 October 2026:

**Output:** `31-10-2026`

**Use case:** Tracking how many days have passed since an order was placed.

**Example:**
```excel
=TODAY()-A2
```

If A2 contains `10-01-2025`, the output on 31 October 2026 is `659` days.

**Important:** TODAY() updates automatically when Excel recalculates.

## 7. Creating Separate Year, Month and Day Columns

Suppose we have an order dataset:

| Order ID | Order Date |
|---:|---|
| 101 | 10-01-2025 |
| 102 | 20-01-2025 |
| 103 | 05-02-2025 |
| 104 | 15-03-2025 |
| 105 | 25-03-2025 |

We want to create separate columns for year, month and day.

**Year formula:**
```excel
=YEAR(B2)
```

**Month formula:**
```excel
=MONTH(B2)
```

**Day formula:**
```excel
=DAY(B2)
```

**Expected Output:**

| Order Date | Year | Month | Day |
|---|---:|---:|---:|
| 10-01-2025 | 2025 | 1 | 10 |
| 20-01-2025 | 2025 | 1 | 20 |
| 05-02-2025 | 2025 | 2 | 5 |
| 15-03-2025 | 2025 | 3 | 15 |
| 25-03-2025 | 2025 | 3 | 25 |

**Use case:** Preparing data for monthly and yearly analysis.

## 8. Sample Practice Dataset

Enter the following data into Excel.

### Order Dates

| Cell | Order Date |
|---|---|
| A2 | 10-01-2025 |
| A3 | 20-01-2025 |
| A4 | 05-02-2025 |
| A5 | 15-03-2025 |
| A6 | 25-03-2025 |

### Delivery Dates

| Cell | Delivery Date |
|---|---|
| B2 | 16-01-2025 |
| B3 | 25-01-2025 |
| B4 | 10-02-2025 |
| B5 | 20-03-2025 |
| B6 | 30-03-2025 |

Note: These dates are set so that every delivery date occurs after its corresponding order date.

## 9. Excel Practice Questions with Answers

### Q1. Extract the year from A2.

```excel
=YEAR(A2)
```

**Output:** `2025`

### Q2. Extract the month number from A3.

```excel
=MONTH(A3)
```

**Output:** `1`

### Q3. Extract the day from A4.

```excel
=DAY(A4)
```

**Output:** `5`

### Q4. Extract the year from A5.

```excel
=YEAR(A5)
```

**Output:** `2025`

### Q5. Extract the month from A6.

```excel
=MONTH(A6)
```

**Output:** `3`

### Q6. Calculate the number of days between A2 and B2.

```excel
=B2-A2
```

**Output:** `6`

Explanation: 16 January − 10 January = 6 days.

### Q7. Calculate the date difference between A3 and B3.

```excel
=B3-A3
```

**Output:** `5`

Explanation: 25 January − 20 January = 5 days.

### Q8. Calculate the date difference between A4 and B4.

```excel
=B4-A4
```

**Output:** `5`

Explanation: 10 February − 5 February = 5 days.

### Q9. Calculate the number of days between today's date and A2.

```excel
=TODAY()-A2
```

**Output as of 31 October 2026:** `659`

The result changes depending on the current date.

### Q10. Extract year, month and day from A2 into three separate columns.

**Year:**
```excel
=YEAR(A2)
```

**Month:**
```excel
=MONTH(A2)
```

**Day:**
```excel
=DAY(A2)
```

**Expected Output:**

| Year | Month | Day |
|---:|---:|---:|
| 2025 | 1 | 10 |

Enter these formulas in three separate cells, such as B2, C2 and D2.

## 10. Important Excel Date Concepts — Quick Revision

| Function / Concept | Purpose |
|---|---|
| YEAR() | Extracts year |
| MONTH() | Extracts month number |
| DAY() | Extracts day of month |
| TODAY() | Returns current date |
| Date subtraction | Calculates days between dates |
| ABS() | Returns absolute numeric difference |

## 11. Common Mistakes to Avoid

1. Enter dates in a format Excel recognizes as dates.
2. Check whether the date is stored as a real date rather than text.
3. Remember that MONTH() returns a number from 1 to 12.
4. Remember that DAY() returns the day of the month, not the weekday.
5. Use the later date minus the earlier date to calculate positive elapsed days.
6. TODAY() changes automatically as the current date changes.

## 12. Day 13 Key Takeaway

Excel date functions make it easier to organize, extract and analyze date-related information.

By using YEAR(), MONTH(), DAY(), TODAY() and date subtraction, I can create useful date columns and calculate time differences for business analysis.

## 📌 Skills Practiced

- Excel date handling
- Extracting year, month and day
- Date calculations
- Order and delivery analysis
- Creating separate date columns
- Preparing data for reporting

#Excel #DataAnalytics #ExcelLearning #30DaysOfLearning
