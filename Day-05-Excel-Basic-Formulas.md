
# Day 5 — Excel Basic Formulas

## 1. Learning Objectives

- Learn SUM, AVERAGE, MIN, MAX, COUNT, and COUNTA.
- Calculate summary statistics from a small dataset.
- Understand cell ranges and formula syntax.
- Apply basic Excel formulas to sales and marks data.

## 2. Sample Dataset

Enter the following data into Excel starting at cell A1.

| Product | Sales | Marks |
|---|---:|---:|
| Laptop | 5000 | 85 |
| Mouse | 1000 | 70 |
| Keyboard | 2000 | 90 |
| Monitor | 4000 | 75 |
| Headphones | 1500 | 80 |

The Sales values are in cells B2:B6, and the Marks values are in cells C2:C6.

## 3. SUM Function

### Definition

SUM adds numerical values in selected cells or ranges.

### Syntax

    =SUM(number1, [number2], ...)

### Example

    =SUM(B2:B6)

### Output

13500

Explanation: The total sales value is 13,500.

### Use in Data Analytics

SUM helps calculate total revenue, expenses, sales, and other numerical totals.

## 4. AVERAGE Function

### Definition

AVERAGE calculates the arithmetic mean of numerical values. Blank cells and text within a referenced range are ignored.

### Syntax

    =AVERAGE(number1, [number2], ...)

### Example

    =AVERAGE(C2:C6)

### Output

80

Explanation: The total marks are 400, divided by 5 observations, giving an average of 80.

### Use in Data Analytics

AVERAGE helps analyze average sales, marks, customer spending, and performance.

## 5. MIN Function

### Definition

MIN returns the smallest numerical value in a selected range.

### Syntax

    =MIN(number1, [number2], ...)

### Example

    =MIN(B2:B6)

### Output

1000

Explanation: The lowest sales value is 1,000.

### Use in Data Analytics

MIN helps identify the lowest sales, minimum expenses, or smallest observed value.

## 6. MAX Function

### Definition

MAX returns the largest numerical value in a selected range.

### Syntax

    =MAX(number1, [number2], ...)

### Example

    =MAX(B2:B6)

### Output

5000

Explanation: The highest sales value is 5,000.

### Use in Data Analytics

MAX helps identify peak sales, highest marks, or the maximum recorded value.

## 7. COUNT Function

### Definition

COUNT counts cells containing numbers in a selected range. It does not count text entries or blank cells.

### Syntax

    =COUNT(value1, [value2], ...)

### Example

    =COUNT(B2:B6)

### Output

5

Explanation: There are five numerical sales entries.

### Use in Data Analytics

COUNT helps determine the number of numerical observations in a dataset.

## 8. COUNTA Function

### Definition

COUNTA counts non-empty cells. It can count text, numbers, dates, and other non-empty values.

### Syntax

    =COUNTA(value1, [value2], ...)

### Example

    =COUNTA(A2:A6)

### Output

5

Explanation: Five product-name cells contain values.

### Use in Data Analytics

COUNTA helps count populated records, product names, employee names, and other non-empty entries.

## 9. COUNT vs COUNTA

| Feature | COUNT | COUNTA |
|---|---|---|
| Counts numbers | Yes | Yes |
| Counts text | No | Yes |
| Counts blank cells | No | No |
| Example | =COUNT(A1:A3) | =COUNTA(A1:A3) |

Suppose A1 contains Anu, A2 contains 500, and A3 contains Ravi.

- `=COUNT(A1:A3)` returns 1.
- `=COUNTA(A1:A3)` returns 3.

## 10. Summary Statistics Table

Use these formulas to create a summary of the sample dataset.

| Statistic | Excel Formula | Result |
|---|---|---:|
| Total Sales | =SUM(B2:B6) | 13500 |
| Average Marks | =AVERAGE(C2:C6) | 80 |
| Minimum Sales | =MIN(B2:B6) | 1000 |
| Maximum Sales | =MAX(B2:B6) | 5000 |
| Number of Sales Entries | =COUNT(B2:B6) | 5 |
| Number of Product Names | =COUNTA(A2:A6) | 5 |

## 11. Practice Questions

1. Calculate the total sales.
2. Calculate the average sales.
3. Find the lowest sales value.
4. Find the highest sales value.
5. Count the numerical entries in the Marks column.
6. Count the non-empty product names.
7. Calculate the average marks.
8. Create a summary table using all six functions.

## 12. Practice Solutions

1. Total sales: `=SUM(B2:B6)` → 13500
2. Average sales: `=AVERAGE(B2:B6)` → 2700
3. Lowest sales: `=MIN(B2:B6)` → 1000
4. Highest sales: `=MAX(B2:B6)` → 5000
5. Number of marks: `=COUNT(C2:C6)` → 5
6. Product names: `=COUNTA(A2:A6)` → 5
7. Average marks: `=AVERAGE(C2:C6)` → 80

## 13. Key Takeaways

- SUM calculates totals.
- AVERAGE calculates the arithmetic mean.
- MIN finds the smallest numerical value.
- MAX finds the largest numerical value.
- COUNT counts numerical entries.
- COUNTA counts non-empty cells.

## 14. Data Analytics Connection

These functions help Data Analysts summarize datasets before deeper analysis. For example, sales data can be summarized to identify total revenue, average sales, minimum sales, and peak sales.

## 15. Day 5 Completion

- [ ] Learned all six Excel functions.
- [ ] Entered the sample dataset.
- [ ] Calculated summary statistics.
- [ ] Completed practice questions.
