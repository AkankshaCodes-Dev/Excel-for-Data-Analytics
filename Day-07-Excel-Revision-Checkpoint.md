# Excel Day 7 — Revision & Hands-on Practice Checkpoint

![Excel](https://img.shields.io/badge/Microsoft_Excel-Practice-green)
![Day](https://img.shields.io/badge/Day-07-purple)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 About This Day

Day 7 of my Data Analytics learning journey was dedicated to revising and practicing the Excel concepts I learned during Days 1–6.

I worked with an employee dataset containing 15 records and practiced formatting tables, sorting and filtering data, using basic formulas, understanding relative cell references, and creating department-wise summaries.

**Day 7 Goal:** Revise Excel fundamentals and apply formulas to analyze employee salary data.

## 🎯 Learning Objectives

- Organize employee data in an Excel table.
- Format headers, columns, and salary values.
- Sort data in ascending and descending order.
- Filter employees by department.
- Use `COUNTA()`, `COUNT()`, `SUM()`, `AVERAGE()`, `MIN()`, and `MAX()`.
- Understand relative cell references.
- Calculate salary plus bonus using formulas.
- Create department-wise summaries using `COUNTIF()`, `SUMIF()`, and `AVERAGEIF()`.

## 🗂️ Dataset: Employees

The `Employees` worksheet contains 15 employee records and five columns.

### Table Structure

| Column | Description |
|---|---|
| `employee_id` | Unique employee identification number |
| `employee_name` | Name of the employee |
| `department` | Department in which the employee works |
| `city` | Employee's city |
| `salary` | Employee's salary |

### Complete Employees Table

| employee_id | employee_name | department | city | salary |
|---:|---|---|---|---:|
| 101 | Anu | IT | Ballari | 30000 |
| 102 | Ravi | Sales | Bengaluru | 35000 |
| 103 | Priya | IT | Ballari | 40000 |
| 104 | Kiran | HR | Mysuru | 25000 |
| 105 | Meena | Sales | Bengaluru | 30000 |
| 106 | Arjun | IT | Mysuru | 45000 |
| 107 | Divya | HR | Ballari | 28000 |
| 108 | Suresh | Sales | Mysuru | 32000 |
| 109 | Neha | IT | Bengaluru | 38000 |
| 110 | Rahul | Finance | Ballari | 42000 |
| 111 | Sneha | Finance | Bengaluru | 40000 |
| 112 | Vikram | IT | Mysuru | 50000 |
| 113 | Pooja | Sales | Ballari | 27000 |
| 114 | Manish | HR | Bengaluru | 26000 |
| 115 | Kavya | Finance | Mysuru | 45000 |

## 📝 Day 7 — All Practice Tasks

### Part 1: Formatting, Sorting and Filtering

**Task 1. Format the employee table.**

- Make the header row bold.
- Adjust column widths to display all headings and names.
- Format the salary column with a thousands separator or currency format.
- Convert the dataset into an Excel table using `Ctrl + T`.
- Confirm that the table has headers.

**Concepts:** Cell formatting, column widths, Excel Tables.

**Task 2. Sort employee salaries.**

- Sort salary from smallest to largest.
- Sort salary from largest to smallest.
- Observe how the complete employee rows move together.
- Restore the original employee order after practicing.

**Concept:** Sort ascending and descending.

**Task 3. Filter employees by department.**

- Display only IT employees.
- Change the filter to display only Finance employees.
- Clear the filters to display all 15 employees again.

**Concepts:** Filter dropdowns, categorical filtering.

### Part 2: Basic Excel Formulas

**Task 4. Calculate employee statistics.**

Create a summary area in columns G and H of the `Employees` worksheet.

| Cell | Metric | Formula |
|---|---|---|
| G2/H2 | Employee count | `=COUNTA(B2:B16)` |
| G3/H3 | Total salary | `=SUM(E2:E16)` |
| G4/H4 | Average salary | `=AVERAGE(E2:E16)` |
| G5/H5 | Lowest salary | `=MIN(E2:E16)` |
| G6/H6 | Highest salary | `=MAX(E2:E16)` |
| G7/H7 | Count of salary values | `=COUNT(E2:E16)` |

Enter the metric names in column G and the formulas in their corresponding cells in column H.

**Concepts:** `COUNTA()`, `COUNT()`, `SUM()`, `AVERAGE()`, `MIN()`, `MAX()`.

### Part 3: Relative Cell References and Bonus Calculation

**Task 5. Calculate salary plus bonus.**

- Enter `Bonus` in G10.
- Enter `Salary + Bonus` in H10.
- Enter `5000` in G11.
- Enter `=E2+G11` in H11.
- Copy the formula down to the remaining employee rows.
- Observe how the cell references change as the formula is copied.

**Concept:** Relative cell references.

**Optional extension:** Explore an absolute reference using `$G$11` to keep the bonus cell fixed when copying the formula.

### Part 4: Department-Wise Summary

**Task 6. Create a Department Summary worksheet.**

Create a new worksheet named `Department Summary` with the following structure:

| Department | Employee Count | Total Salary | Average Salary |
|---|---:|---:|---:|
| Finance | | | |
| HR | | | |
| IT | | | |
| Sales | | | |

Use these formulas, assuming the department name is in cell A2 of the summary worksheet.

**Employee Count — B2**

```excel
=COUNTIF(Employees!C:C,A2)
```

**Total Salary — C2**

```excel
=SUMIF(Employees!C:C,A2,Employees!E:E)
```

**Average Salary — D2**

```excel
=AVERAGEIF(Employees!C:C,A2,Employees!E:E)
```

Copy the formulas down for all four departments.

**Concepts:** `COUNTIF()`, `SUMIF()`, `AVERAGEIF()`.

## 💻 Formula Practice and Expected Results

### 1. Count Employees

```excel
=COUNTA(B2:B16)
```

Expected result: **15**

### 2. Calculate Total Salary

```excel
=SUM(E2:E16)
```

Expected result: **₹5,33,000**

### 3. Calculate Average Salary

```excel
=AVERAGE(E2:E16)
```

Expected result: **₹35,533.33** approximately.

### 4. Find the Lowest Salary

```excel
=MIN(E2:E16)
```

Expected result: **₹25,000**

### 5. Find the Highest Salary

```excel
=MAX(E2:E16)
```

Expected result: **₹50,000**

### 6. Count Numeric Salary Values

```excel
=COUNT(E2:E16)
```

Expected result: **15**

### 7. Calculate Salary Plus Bonus

```excel
=E2+G11
```

If the employee salary is ₹30,000 and the bonus is ₹5,000, the result is **₹35,000**.

## 📊 Expected Department Summary

Use this table to verify your `Department Summary` worksheet after entering the formulas.

| Department | Employee Count | Total Salary | Average Salary |
|---|---:|---:|---:|
| Finance | 3 | ₹1,27,000 | ₹42,333.33 |
| HR | 3 | ₹79,000 | ₹26,333.33 |
| IT | 5 | ₹2,03,000 | ₹40,600 |
| Sales | 4 | ₹1,24,000 | ₹31,000 |
| **Total** | **15** | **₹5,33,000** | **₹35,533.33** |

## 📚 Excel Concepts Revised

| Function / Feature | Purpose |
|---|---|
| Format as Table | Organize data into a structured table |
| Sort | Arrange records in ascending or descending order |
| Filter | Display records matching selected conditions |
| `COUNTA()` | Count non-empty cells |
| `COUNT()` | Count cells containing numbers |
| `SUM()` | Calculate a total |
| `AVERAGE()` | Calculate an average |
| `MIN()` | Find the smallest value |
| `MAX()` | Find the largest value |
| Relative references | Automatically adjust cell references when formulas are copied |
| `COUNTIF()` | Count cells matching a condition |
| `SUMIF()` | Sum values matching a condition |
| `AVERAGEIF()` | Average values matching a condition |

## 🔍 Important Learning

### Difference Between COUNT and COUNTA

- `COUNT()` counts cells containing numeric values.
- `COUNTA()` counts non-empty cells, including cells containing text.

### Understanding Relative References

When `=E2+G11` is entered in H11 and copied down one row, it becomes `=E3+G12`.

Both row references change automatically because they are relative references.

### Connecting Excel with SQL

In SQL, `GROUP BY` helps calculate department-wise summaries. In Excel, `COUNTIF()`, `SUMIF()`, and `AVERAGEIF()` help perform similar category-wise calculations.

## 📈 Data Analytics Applications

These Excel skills help Data Analysts:

- Organize and format raw datasets.
- Sort and filter records for specific analysis.
- Calculate descriptive statistics.
- Compare salary information across departments.
- Create summary reports using formulas.
- Automate repetitive calculations with cell references.

## ✅ Day 7 Checkpoint Results

| Metric | Result |
|---|---|
| Dataset | 15 employee records |
| Worksheets | Employees and Department Summary |
| Formatting practice | Completed |
| Sorting practice | Completed |
| Filtering practice | Completed |
| Basic formula practice | Completed |
| Salary plus bonus | Practiced |
| Department summary | Completed |
| Main focus | Excel revision and hands-on analysis |

## 🚀 Key Takeaways

- Improved my understanding of Excel formatting, sorting, and filtering.
- Practiced formulas for counting and calculating salary statistics.
- Learned how relative cell references adjust when copied.
- Used conditional aggregation functions to summarize departments.
- Connected Excel summary functions with SQL grouping concepts.
- Practiced organizing data and presenting results in a structured format.

## 📅 Learning Journey

**Day 7 of my 30-day Data Analytics learning challenge — Excel Revision and Hands-on Practice.**

This checkpoint helped me strengthen my Excel fundamentals and understand how formulas can turn raw employee records into meaningful summaries.

I will continue practicing Excel and gradually progress toward data cleaning, lookup functions, PivotTables, charts, and practical data analysis projects.

---

**Skills:** Microsoft Excel | Data Formatting | Sorting | Filtering | Excel Formulas | Cell References | Conditional Aggregation | Data Analysis

**#Excel #DataAnalytics #ExcelPractice #LearningJourney #DataAnalyst**
