# Day 10 — Excel COUNTIF, SUMIF, and AVERAGEIF

## 📌 Overview

On Day 10 of my Excel learning journey, I learned how to analyze data using conditional functions.

### 🎯 Topics Covered

- COUNTIF — Count cells that match a condition
- SUMIF — Add values that match a condition
- AVERAGEIF — Calculate the average of values that match a condition
- Analyze student marks by subject
- Analyze sales by product category

## 1. COUNTIF

`COUNTIF` counts the number of cells that satisfy a specified condition.

### Syntax

```excel
=COUNTIF(range, criteria)
```

- `range`: Cells to check.
- `criteria`: The condition to match.

### Example 1: Count Python students

```excel
=COUNTIF(B2:B7,"Python")
```

**Expected result:** 3

### Example 2: Count students scoring 75 or above

```excel
=COUNTIF(C2:C7,">=75")
```

**Expected result:** 3

Comparison criteria such as `">=75"` are written inside quotation marks.

## 2. SUMIF

`SUMIF` adds values that satisfy a specified condition.

### Syntax

```excel
=SUMIF(range, criteria, sum_range)
```

- `range`: Cells where Excel checks the condition.
- `criteria`: The condition to match.
- `sum_range`: Cells containing the numbers to add.

### Example 1: Total marks of Python students

```excel
=SUMIF(B2:B7,"Python",C2:C7)
```

**Expected result:** 235

### Example 2: Total marks of SQL students

```excel
=SUMIF(B2:B7,"SQL",C2:C7)
```

**Expected result:** 195

## 3. AVERAGEIF

`AVERAGEIF` calculates the average of values that satisfy a specified condition.

### Syntax

```excel
=AVERAGEIF(range, criteria, average_range)
```

- `range`: Cells where Excel checks the condition.
- `criteria`: The condition to match.
- `average_range`: Cells containing the values to average.

### Example 1: Average marks of Python students

```excel
=AVERAGEIF(B2:B7,"Python",C2:C7)
```

**Expected result:** 78.33 approximately

### Example 2: Average marks of SQL students

```excel
=AVERAGEIF(B2:B7,"SQL",C2:C7)
```

**Expected result:** 65

## 4. Practice Dataset — Student Marks

Enter the following data into Excel, starting from cell A1.

| Student | Subject | Marks |
|---|---|---:|
| Anu | Python | 85 |
| Ravi | SQL | 70 |
| Priya | Python | 90 |
| Kiran | SQL | 45 |
| Rahul | Python | 60 |
| Meena | SQL | 80 |

The data occupies cells A1:C7, including the headers.

## 5. Practice Dataset — Sales Analysis

| Product | Category | Sales |
|---|---|---:|
| Laptop | Electronics | 50000 |
| Mouse | Accessories | 1000 |
| Phone | Electronics | 20000 |
| Keyboard | Accessories | 2000 |
| Tablet | Electronics | 15000 |

The data occupies cells A1:C6, including the headers.

### Total Electronics sales

```excel
=SUMIF(B2:B6,"Electronics",C2:C6)
```

**Expected result:** 85000

### Average Electronics sales

```excel
=AVERAGEIF(B2:B6,"Electronics",C2:C6)
```

**Expected result:** 28333.33 approximately

### Average Accessories sales

```excel
=AVERAGEIF(B2:B6,"Accessories",C2:C6)
```

**Expected result:** 1500

## 📝 Practice Tasks and Solutions

### Task 1: Count Python students

```excel
=COUNTIF(B2:B7,"Python")
```

Answer: 3

### Task 2: Count SQL students

```excel
=COUNTIF(B2:B7,"SQL")
```

Answer: 3

### Task 3: Count students scoring 75 or above

```excel
=COUNTIF(C2:C7,">=75")
```

Answer: 3

### Task 4: Count students scoring below 60

```excel
=COUNTIF(C2:C7,"<60")
```

Answer: 1

### Task 5: Total marks of Python students

```excel
=SUMIF(B2:B7,"Python",C2:C7)
```

Answer: 235

### Task 6: Total marks of SQL students

```excel
=SUMIF(B2:B7,"SQL",C2:C7)
```

Answer: 195

### Task 7: Average marks of Python students

```excel
=AVERAGEIF(B2:B7,"Python",C2:C7)
```

Answer: 78.33 approximately

### Task 8: Average marks of SQL students

```excel
=AVERAGEIF(B2:B7,"SQL",C2:C7)
```

Answer: 65

### Task 9: Total Electronics sales

```excel
=SUMIF(B2:B6,"Electronics",C2:C6)
```

Answer: 85000

### Task 10: Average Accessories sales

```excel
=AVERAGEIF(B2:B6,"Accessories",C2:C6)
```

Answer: 1500

## 💡 Key Learnings

| Function | Purpose | Example |
|---|---|---|
| COUNTIF | Count matching cells | Count students studying Python |
| SUMIF | Add matching values | Calculate total Electronics sales |
| AVERAGEIF | Average matching values | Calculate average marks by subject |

These functions help analyze data efficiently without manually counting, adding, or averaging individual records.

## 📈 Day 10 Progress

- [x] Learned COUNTIF
- [x] Learned SUMIF
- [x] Learned AVERAGEIF
- [x] Practiced student marks analysis
- [x] Practiced sales analysis
- [x] Completed 10 practice tasks and checked solutions

**Next:** Continue learning Excel functions and apply them to practical data analysis tasks.
