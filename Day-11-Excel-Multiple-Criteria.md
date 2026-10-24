# Day 11 — Excel: Multiple Criteria Analysis

## 📌 Overview
On Day 11 of my Excel for Data Analytics learning journey, I learned how to use `COUNTIFS`, `SUMIFS`, and `AVERAGEIFS` to analyse data using multiple conditions.

I practised building region-wise and department-wise performance summaries using an employee salary dataset.

## 🎯 Learning Objectives
- Count records matching multiple conditions.
- Calculate totals using multiple criteria.
- Calculate averages for specific groups.
- Build a region performance summary.
- Apply Excel formulas to business-style questions.

## 🗂️ Practice Dataset: Employees

| EmployeeID | Name | Department | Region | Salary |
|---:|---|---|---|---:|
| 1 | Ravi | IT | South | 50000 |
| 2 | Priya | HR | North | 35000 |
| 3 | Amit | IT | South | 60000 |
| 4 | Sneha | Sales | North | 40000 |
| 5 | Kiran | Sales | South | 45000 |
| 6 | Neha | HR | South | 30000 |
| 7 | Arjun | IT | North | 55000 |
| 8 | Divya | Sales | North | 50000 |
| 9 | Rahul | HR | North | 40000 |
| 10 | Meena | IT | South | 45000 |

Assume the dataset is in cells `A1:E11`, with headers in row 1:
- Column C: Department
- Column D: Region
- Column E: Salary

## 📚 Concepts Learned

### 1. COUNTIFS — Count with Multiple Criteria

**Syntax**

```excel
=COUNTIFS(criteria_range1, criteria1, criteria_range2, criteria2)
```

Counts rows satisfying all specified criteria.

Example: Count IT employees in the South region.

```excel
=COUNTIFS(C2:C11,"IT",D2:D11,"South")
```

Expected result: **3**

Example: Count North-region employees earning at least ₹45,000.

```excel
=COUNTIFS(D2:D11,"North",E2:E11,">=45000")
```

Expected result: **2**

### 2. SUMIFS — Sum with Multiple Criteria

**Syntax**

```excel
=SUMIFS(sum_range, criteria_range1, criteria1, criteria_range2, criteria2)
```

Adds values that meet all specified criteria.

Example: Calculate the total salary of IT employees in the South region.

```excel
=SUMIFS(E2:E11,C2:C11,"IT",D2:D11,"South")
```

Expected result: **₹1,55,000**

Example: Calculate the total salary of North-region Sales employees.

```excel
=SUMIFS(E2:E11,C2:C11,"Sales",D2:D11,"North")
```

Expected result: **₹90,000**

### 3. AVERAGEIFS — Average with Multiple Criteria

**Syntax**

```excel
=AVERAGEIFS(average_range, criteria_range1, criteria1, criteria_range2, criteria2)
```

Calculates the average of values satisfying all specified criteria.

Example: Calculate the average salary of IT employees in the South region.

```excel
=AVERAGEIFS(E2:E11,C2:C11,"IT",D2:D11,"South")
```

Expected result: **₹51,666.67**

Example: Calculate the average salary of North-region HR employees.

```excel
=AVERAGEIFS(E2:E11,C2:C11,"HR",D2:D11,"North")
```

Expected result: **₹37,500**

## 💻 Practice: 10 Tasks with Solutions

### Task 1: Count IT employees in the South region.

```excel
=COUNTIFS(C2:C11,"IT",D2:D11,"South")
```

**Answer: 3 employees**

### Task 2: Calculate the total salary of North-region Sales employees.

```excel
=SUMIFS(E2:E11,C2:C11,"Sales",D2:D11,"North")
```

**Answer: ₹90,000**

### Task 3: Calculate the average salary of South-region HR employees.

```excel
=AVERAGEIFS(E2:E11,C2:C11,"HR",D2:D11,"South")
```

**Answer: ₹30,000**

### Task 4: Count North-region employees earning at least ₹45,000.

```excel
=COUNTIFS(D2:D11,"North",E2:E11,">=45000")
```

**Answer: 2 employees**

### Task 5: Calculate the total salary of IT employees earning at least ₹50,000.

```excel
=SUMIFS(E2:E11,C2:C11,"IT",E2:E11,">=50000")
```

**Answer: ₹1,65,000**

### Task 6: Calculate the average salary of South-region Sales employees.

```excel
=AVERAGEIFS(E2:E11,C2:C11,"Sales",D2:D11,"South")
```

**Answer: ₹45,000**

### Task 7: Build a region performance summary.

Create the following summary in cells G1:J3.

| Region | Employee Count | Total Salary | Average Salary |
|---|---:|---:|---:|
| North | 5 | 220000 | 44000 |
| South | 5 | 230000 | 46000 |

Assuming the region names are in `G2:G3`, enter the following formulas in row 2 and copy them down.

**Employee Count — H2**

```excel
=COUNTIFS($D$2:$D$11,G2)
```

**Total Salary — I2**

```excel
=SUMIFS($E$2:$E$11,$D$2:$D$11,G2)
```

**Average Salary — J2**

```excel
=AVERAGEIFS($E$2:$E$11,$D$2:$D$11,G2)
```

**Conclusion:** The South region has the higher average salary, at ₹46,000.

### Task 8: Build a department-and-region total salary summary.

Suppose column G contains Department and column H contains Region.

In cell I2, enter:

```excel
=SUMIFS($E$2:$E$11,$C$2:$C$11,G2,$D$2:$D$11,H2)
```

Copy the formula down for each department-region combination.

Expected results:

| Department | Region | Total Salary |
|---|---|---:|
| IT | North | 55000 |
| IT | South | 155000 |
| HR | North | 75000 |
| HR | South | 30000 |
| Sales | North | 90000 |
| Sales | South | 45000 |

### Task 9: Count South-region employees earning below ₹40,000.

```excel
=COUNTIFS(D2:D11,"South",E2:E11,"<40000")
```

**Answer: 1 employee**

### Task 10: Build a region performance summary and identify the higher average salary.

Use the three formulas from Task 7 to calculate employee count, total salary, and average salary for each region.

Expected results:

| Region | Employee Count | Total Salary | Average Salary |
|---|---:|---:|---:|
| North | 5 | 220000 | 44000 |
| South | 5 | 230000 | 46000 |

**Business conclusion:** The South region has a higher average salary by ₹2,000.

## 🔑 Key Takeaways
- `COUNTIFS` counts records matching multiple criteria.
- `SUMIFS` calculates totals using multiple criteria.
- `AVERAGEIFS` calculates averages using multiple criteria.
- Criteria can include text, numbers, and comparison operators.
- Absolute references such as `$E$2:$E$11` keep the source range fixed when copying formulas.

## 🚀 Progress
- [x] Excel concepts studied
- [x] Multiple-criteria formulas practised
- [x] Region and department summaries documented
- [x] Solutions and expected results included

**Day 11 completed — Excel for Data Analytics.**
