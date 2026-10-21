# Day 8 — Excel IF Function | Personal Data Analytics Practice

## 📌 Overview

On Day 8 of my personal Data Analytics learning journey, I learned how to use the Excel `IF` function to make logical decisions and categorize data based on conditions.

## 🎯 Learning Objectives

- Understand the Excel `IF` function.
- Apply logical tests using comparison operators.
- Classify student marks into Pass and Fail.
- Create High, Medium, and Low categories.
- Apply IF formulas to sales and eligibility data.
- Practice formulas using an Excel worksheet.

## 📚 Concepts Learned

| Concept | Purpose |
|---|---|
| `IF()` | Returns different results depending on a condition |
| Logical test | Checks whether a condition is TRUE or FALSE |
| `>=` | Greater than or equal to |
| `>` | Greater than |
| `<` | Less than |
| `<=` | Less than or equal to |
| `=` | Equal to |
| `<>` | Not equal to |
| Nested IF | Checks multiple conditions using multiple IF functions |
| `COUNTIF()` | Counts cells that meet a condition |

## 🧮 IF Function Syntax

```excel
=IF(logical_test, value_if_true, value_if_false)
```

**Example:**

```excel
=IF(B2>=35,"Pass","Fail")
```

This formula checks whether the value in cell B2 is at least 35. If the condition is TRUE, it returns `Pass`; otherwise, it returns `Fail`.

## 💻 Practical Examples

### 1. Pass or Fail

```excel
=IF(B2>=35,"Pass","Fail")
```

### 2. High, Medium, or Low

Rules:
- High: marks of at least 75
- Medium: marks of at least 40 but below 75
- Low: marks below 40

```excel
=IF(B2>=75,"High",IF(B2>=40,"Medium","Low"))
```

### 3. Eligibility Check

```excel
=IF(B2>=60,"Eligible","Not Eligible")
```

### 4. Excellent or Needs Improvement

```excel
=IF(B2>=90,"Excellent","Needs Improvement")
```

### 5. Bonus Eligibility

```excel
=IF(B2>=10000,"Bonus Eligible","Not Eligible")
```

### 6. Zero or Non-Zero

```excel
=IF(A2<>0,"Non-Zero","Zero")
```

## 🗃️ Practice Dataset — Student Marks

| Student | Marks |
|---|---:|
| Asha | 85 |
| Bharat | 29 |
| Charan | 35 |
| Divya | 64 |
| Esha | 48 |
| Farhan | 92 |
| Gita | 15 |
| Hari | 70 |

## 📝 Practice Questions — 10 Tasks

1. Use IF to classify each student as Pass or Fail, with 35 as the passing mark.
2. Count how many students passed and failed using `COUNTIF()`.
3. Create High, Medium, and Low categories based on the specified marks thresholds.
4. Display Eligible when marks are at least 60 and Not Eligible otherwise.
5. Display Excellent when marks are at least 90 and Needs Improvement otherwise.
6. Classify sales of ₹3,000, ₹6,000, ₹12,000, and ₹4,500 as High, Medium, or Low.
7. Display Bonus Eligible for sales of at least ₹10,000 and Not Eligible otherwise.
8. Use the not-equal operator to display Non-Zero or Zero.
9. Write an IF formula that returns Pass when marks are at least 35.
10. Apply the appropriate IF formulas to all rows, verify the results, and save the workbook.

## 💡 Key Takeaways

- The `IF` function helps automate decisions in spreadsheets.
- Logical tests compare values against specified conditions.
- Nested IF formulas can classify data into multiple categories.
- Correct comparison operators and formula references are important.
- `COUNTIF()` can count how many cells match a specified condition.

## 🚀 Learning Outcome

I practiced Excel logical formulas for student grading, eligibility checks, and sales classification. These skills are useful for data cleaning, reporting, and business analysis.

**Day 8 Status:** Excel learning and practice completed.

#Excel #DataAnalytics #ExcelPractice #LearningJourney
