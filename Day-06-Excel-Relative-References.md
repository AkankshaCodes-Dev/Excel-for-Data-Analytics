
# Day 6 — Excel Relative References and Arithmetic

## 1. Learning Objectives

- Understand cell references in Excel.
- Learn how relative references work.
- Use addition, subtraction, multiplication, and division.
- Calculate sales using quantity and unit price.
- Build a sales summary using Excel formulas.

## 2. What Is a Cell Reference?

### Definition

A cell reference identifies a particular cell in an Excel worksheet using its column letter and row number.

Examples:

- A1 refers to column A, row 1.
- B2 refers to column B, row 2.
- C5 refers to column C, row 5.

Cell references allow formulas to use values stored in other cells.

## 3. Relative References

### Definition

A relative reference is a cell reference that automatically adjusts when a formula is copied or filled into another cell.

### Example Dataset

| Product | Quantity | Unit Price | Total Sales |
|---|---:|---:|---:|
| Laptop | 2 | 30000 | 60000 |
| Mouse | 5 | 500 | 2500 |
| Keyboard | 3 | 1000 | 3000 |
| Monitor | 2 | 8000 | 16000 |

### Formula in Cell D2

    =B2*C2

Explanation:
The formula multiplies the quantity in B2 by the unit price in C2.

Calculation:

2 × 30000 = 60000

### Copying the Formula

When the formula is copied down:

- D2: =B2*C2
- D3: =B3*C3
- D4: =B4*C4
- D5: =B5*C5

The cell references adjust automatically according to the new row.

### Why Relative References Are Useful

- Apply the same calculation to many rows.
- Avoid rewriting formulas manually.
- Reduce repetitive work.
- Make sales and financial calculations more efficient.

## 4. Basic Arithmetic Formulas

Excel formulas generally begin with an equals sign (=).

### Addition (+)

Definition: Adds two or more values.

Example:

    =B2+C2

If B2 is 10 and C2 is 5, the result is 15.

### Subtraction (-)

Definition: Subtracts one value from another.

Example:

    =B2-C2

If B2 is 10 and C2 is 5, the result is 5.

### Multiplication (*)

Definition: Multiplies two or more values.

Example:

    =B2*C2

If B2 is 4 and C2 is 200, the result is 800.

### Division (/)

Definition: Divides one value by another.

Example:

    =B2/C2

If B2 is 20 and C2 is 5, the result is 4.

Note: The divisor must not be zero.

## 5. Calculate Total Sales

Total sales for each product can be calculated using:

    =B2*C2

Assume:
- Column B contains Quantity.
- Column C contains Unit Price.
- Column D contains Total Sales.

Copy the formula down from D2 to D5 to calculate each product's sales.

### Expected Results

| Product | Quantity | Unit Price | Total Sales |
|---|---:|---:|---:|
| Laptop | 2 | 30000 | 60000 |
| Mouse | 5 | 500 | 2500 |
| Keyboard | 3 | 1000 | 3000 |
| Monitor | 2 | 8000 | 16000 |

## 6. Build a Sales Summary

Use the Total Sales values in D2:D5.

| Metric | Formula | Expected Result |
|---|---|---:|
| Total Sales | =SUM(D2:D5) | 81500 |
| Average Sale | =AVERAGE(D2:D5) | 20375 |
| Minimum Sale | =MIN(D2:D5) | 2500 |
| Maximum Sale | =MAX(D2:D5) | 60000 |
| Product Count | =COUNTA(A2:A5) | 4 |

### Explanation

- SUM calculates total sales.
- AVERAGE calculates the average sales value.
- MIN identifies the smallest sales value.
- MAX identifies the largest sales value.
- COUNTA counts the non-empty product names.

## 7. Calculate Profit

### Definition

Profit is the amount remaining after expenses are subtracted from sales, before any additional adjustments.

### Formula

    =D2-E2

Assume:
- D2 contains sales revenue.
- E2 contains expenses.

Example:
If sales are 10000 and expenses are 6500:

10000 - 6500 = 3500

The calculated profit is 3500.

## 8. Relative References in Practice

Suppose D2 contains:

    =B2*C2

When copied one row down, the formula becomes:

    =B3*C3

When copied another row down, it becomes:

    =B4*C4

This automatic adjustment is the key feature of relative references.

## 9. Practice Questions

Using the sample sales dataset:

1. Calculate the total sales for Laptop.
2. Calculate the total sales for Mouse.
3. Write a formula for Keyboard sales.
4. Write a formula for Monitor sales.
5. Calculate total sales for all four products.
6. Calculate average sales.
7. Find minimum and maximum sales.
8. Count the product names.
9. If sales are in D2 and expenses are in E2, calculate profit.
10. Explain what happens when =B2*C2 is copied from D2 to D3.

## 10. Practice Solutions

1. Laptop: =B2*C2 → 60000
2. Mouse: =B3*C3 → 2500
3. Keyboard: =B4*C4 → 3000
4. Monitor: =B5*C5 → 16000
5. Total sales: =SUM(D2:D5) → 81500
6. Average sales: =AVERAGE(D2:D5) → 20375
7. Minimum: =MIN(D2:D5) → 2500
8. Maximum: =MAX(D2:D5) → 60000
9. Product count: =COUNTA(A2:A5) → 4
10. Profit: =D2-E2
11. Copying =B2*C2 from D2 to D3 changes the formula to =B3*C3.

## 11. Key Takeaways

- A cell reference identifies a worksheet cell.
- Relative references adjust when formulas are copied.
- + performs addition.
- - performs subtraction.
- * performs multiplication.
- / performs division.
- Quantity multiplied by unit price gives total sales.
- Sales minus expenses gives profit before additional adjustments.
- Summary formulas help analyze business performance.

## 12. Data Analytics Applications

Excel formulas and relative references help Data Analysts calculate revenue, summarize sales, compare product performance, and prepare reports without repeating calculations manually.

## 13. Day 6 Completion

- [ ] Learned relative cell references.
- [ ] Practiced basic arithmetic formulas.
- [ ] Calculated sales for each product.
- [ ] Built a sales summary.
- [ ] Completed the practice questions.
