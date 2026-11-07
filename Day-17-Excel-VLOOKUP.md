# DAY 17 — Excel: VLOOKUP Basics

## Topics Covered
- Introduction to VLOOKUP
- VLOOKUP syntax
- Understanding VLOOKUP arguments
- Exact match using FALSE
- Column index numbers
- VLOOKUP vs XLOOKUP
- Handling lookup errors using IFERROR

---

## 1. What is VLOOKUP?

VLOOKUP stands for **Vertical Lookup**.

It is used to search for a value in the first column of a selected table and return related information from another column in the same table.

### Example: Employee Details

| Employee ID | Name | Department | Salary |
|---|---|---|---:|
| 101 | Akash | IT | 25000 |
| 102 | Priya | HR | 30000 |
| 103 | Rahul | Sales | 28000 |
| 104 | Sneha | IT | 35000 |
| 105 | Anjali | Finance | 32000 |

Suppose we want to find the salary of employee ID 103.

Instead of searching manually, we can use VLOOKUP.

## 2. VLOOKUP Syntax

```excel
=VLOOKUP(lookup_value, table_array, col_index_num, [range_lookup])
```

### Understanding the arguments

| Argument | Meaning |
|---|---|
| lookup_value | Value to search for |
| table_array | Selected table range |
| col_index_num | Column number containing the result |
| range_lookup | FALSE for exact match; TRUE for approximate match |

## 3. Practical Example: Find Employee Salary

Assume employee ID 103 is entered in cell F2.

```excel
=VLOOKUP(F2,A2:D6,4,FALSE)
```

**Expected Output: 28000**

### Explanation

- F2 → Employee ID to search.
- A2:D6 → Employee table range.
- 4 → Returns the value from the fourth column.
- FALSE → Finds an exact match.

## 4. Understanding Column Index Numbers

VLOOKUP counts columns starting from the first column of the selected table range.

| Column | Column Index |
|---|---:|
| Employee ID | 1 |
| Name | 2 |
| Department | 3 |
| Salary | 4 |

**Important:** The column index starts from the selected table range, not necessarily worksheet column A.

## 5. More VLOOKUP Examples

### Find Employee Name

```excel
=VLOOKUP(F2,A2:D6,2,FALSE)
```

**Expected Output:** Rahul

### Find Employee Department

```excel
=VLOOKUP(F2,A2:D6,3,FALSE)
```

**Expected Output:** Sales

### Find Employee Salary

```excel
=VLOOKUP(F2,A2:D6,4,FALSE)
```

**Expected Output:** 28000

## 6. VLOOKUP vs XLOOKUP

| VLOOKUP | XLOOKUP |
|---|---|
| Searches in the first column of the selected range | Can search in any column |
| Returns values to the right | Returns values to the left or right |
| Uses a column index number | Uses a return range |
| FALSE is used for exact matching | Exact match is the default |
| Older Excel function | Newer Excel function |

### VLOOKUP Example

```excel
=VLOOKUP(F2,A2:D6,4,FALSE)
```

### XLOOKUP Example

```excel
=XLOOKUP(F2,A2:A6,D2:D6,"Not Found")
```

Both formulas return 28000 when F2 contains 103.

## 7. Handling Errors Using IFERROR

When a lookup value does not exist, VLOOKUP with FALSE returns `#N/A`.

Example:

```excel
=VLOOKUP(F2,A2:D6,2,FALSE)
```

If employee ID 106 is not available, the result is `#N/A`.

We can handle this using IFERROR.

```excel
=IFERROR(VLOOKUP(F2,A2:D6,2,FALSE),"Not Found")
```

**Expected Output:** Not Found

---

# 8. Excel Practice Questions

Use the Employee Details table above.

Assume the employee ID to search is entered in cell F2.

### Q1.
Find the name of employee ID 103 using VLOOKUP.

### Q2.
Find the salary of employee ID 102.

### Q3.
Find the department of employee ID 105.

### Q4.
Find the salary of employee ID 104.

### Q5.
Search for employee ID 106 and display "Not Found" instead of an error.

---

# 9. Excel Practice Solutions

### Solution 1 — Find Employee Name

```excel
=VLOOKUP(F2,A2:D6,2,FALSE)
```

**Expected Output:** Rahul

### Solution 2 — Find Employee Salary

```excel
=VLOOKUP(F2,A2:D6,4,FALSE)
```

**Expected Output:** 30000

### Solution 3 — Find Employee Department

```excel
=VLOOKUP(F2,A2:D6,3,FALSE)
```

**Expected Output:** Finance

### Solution 4 — Find Employee Salary

```excel
=VLOOKUP(F2,A2:D6,4,FALSE)
```

**Expected Output:** 35000

### Solution 5 — Handle Missing Employee ID

```excel
=IFERROR(VLOOKUP(F2,A2:D6,2,FALSE),"Not Found")
```

**Expected Output:** Not Found

---

# 10. Key Takeaways

- VLOOKUP stands for Vertical Lookup.
- It searches for values in the first column of the selected range.
- It uses a column index number to return information.
- FALSE is used for an exact match.
- VLOOKUP cannot directly return values from columns to the left.
- XLOOKUP provides more flexibility than VLOOKUP.
- IFERROR helps display a meaningful message instead of an error.

## Day 17 Completion

- [x] Learned VLOOKUP basics
- [x] Understood VLOOKUP syntax and arguments
- [x] Practised exact matching
- [x] Compared VLOOKUP with XLOOKUP
- [x] Practised five Excel questions

**Day 17 — Excel Learning Completed!**
