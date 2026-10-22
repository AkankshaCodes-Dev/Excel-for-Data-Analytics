# Day 9 — Excel: AND, OR, Nested IF

## 📌 Overview

On Day 9, I learned Excel logical functions: `AND()`, `OR()`, `IF()`, and nested `IF()`.

I practised checking multiple conditions, creating eligibility columns, assigning student statuses, and building simple decision-making formulas.

## 🎯 Learning Objectives

- Understand `AND()` and `OR()`.
- Use `IF()` to return different results.
- Combine `IF()` with `AND()` and `OR()`.
- Use nested `IF()` for multiple conditions.
- Create an eligibility/status column.
- Solve 10 Excel practice tasks using formulas.

---

## 1. What Is AND()?

The `AND()` function checks whether all specified conditions are true.

### Syntax

```excel
=AND(condition1, condition2)
```

### Example

```excel
=AND(B2>=18,C2>=60)
```

This returns `TRUE` only when:

- Age in `B2` is at least 18.
- Score in `C2` is at least 60.

| Age | Score | Result |
|---:|---:|---|
| 20 | 75 | TRUE |
| 17 | 75 | FALSE |
| 20 | 50 | FALSE |
| 17 | 50 | FALSE |

**Remember:** AND = All conditions must be true.

---

## 2. What Is OR()?

The `OR()` function checks whether at least one condition is true.

### Syntax

```excel
=OR(condition1, condition2)
```

### Example

```excel
=OR(B2>=18,C2>=60)
```

This returns `TRUE` if either the age is at least 18 or the score is at least 60.

| Age | Score | Result |
|---:|---:|---|
| 20 | 75 | TRUE |
| 17 | 75 | TRUE |
| 20 | 50 | TRUE |
| 17 | 50 | FALSE |

**Remember:** OR = At least one condition must be true.

---

## 3. AND vs OR

| AND | OR |
|---|---|
| All conditions must be true. | At least one condition must be true. |
| More restrictive. | More flexible. |
| Example: attendance and marks must meet requirements. | Example: marks or attendance can qualify someone. |

---

## 4. What Is IF()?

The `IF()` function returns one result when a condition is true and another when it is false.

### Syntax

```excel
=IF(condition, value_if_true, value_if_false)
```

### Example

```excel
=IF(B2>=40,"Pass","Fail")
```

If marks in `B2` are at least 40, Excel returns `Pass`. Otherwise, it returns `Fail`.

| Marks | Result |
|---:|---|
| 75 | Pass |
| 40 | Pass |
| 25 | Fail |

Text values such as `"Pass"` and `"Fail"` must be inside double quotation marks.

---

## 5. IF with AND()

### Example: Student Eligibility

A student is eligible only if attendance is at least 75% AND marks are at least 40.

Assume:

- `B2` = Attendance percentage
- `C2` = Marks

```excel
=IF(AND(B2>=75,C2>=40),"Eligible","Not Eligible")
```

| Attendance | Marks | Status |
|---:|---:|---|
| 85 | 70 | Eligible |
| 80 | 35 | Not Eligible |
| 65 | 80 | Not Eligible |
| 75 | 40 | Eligible |

Both conditions must be satisfied.

---

## 6. IF with OR()

### Example: Special Consideration

A student receives special consideration if attendance is at least 95% OR marks are at least 90.

Assume:

- `B2` = Attendance
- `C2` = Marks

```excel
=IF(OR(B2>=95,C2>=90),"Special Consideration","Normal")
```

| Attendance | Marks | Status |
|---:|---:|---|
| 96 | 60 | Special Consideration |
| 80 | 95 | Special Consideration |
| 85 | 75 | Normal |

Only one of the conditions needs to be true.

---

## 7. What Is Nested IF?

A nested IF is an `IF()` formula inside another `IF()` formula. It allows Excel to check multiple conditions in order.

### Example: Student Grade

- Marks of 75 or above → Excellent
- Marks of 60 or above → Good
- Marks of 40 or above → Pass
- Marks below 40 → Fail

```excel
=IF(B2>=75,"Excellent",
   IF(B2>=60,"Good",
      IF(B2>=40,"Pass","Fail")))
```

### Expected Results

| Marks | Status |
|---:|---|
| 90 | Excellent |
| 68 | Good |
| 45 | Pass |
| 30 | Fail |

### How It Works

1. Excel checks whether marks are at least 75.
2. If true, it returns `Excellent`.
3. If false, it checks whether marks are at least 60.
4. If false again, it checks whether marks are at least 40.
5. If all conditions fail, it returns `Fail`.

**Important:** Check the highest threshold first. Otherwise, higher marks may receive the wrong category.

---

## 8. Nested IF with AND()

### Example: Scholarship Eligibility

Rules:

- Marks at least 80 AND attendance at least 90% → Scholarship
- Otherwise, marks at least 60 → Consider
- Otherwise → Not Eligible

Assume `B2` contains marks and `C2` contains attendance.

```excel
=IF(AND(B2>=80,C2>=90),"Scholarship",
   IF(B2>=60,"Consider","Not Eligible"))
```

### Expected Results

| Marks | Attendance | Status |
|---:|---:|---|
| 90 | 95 | Scholarship |
| 85 | 80 | Consider |
| 65 | 75 | Consider |
| 45 | 95 | Not Eligible |

The first condition checks both marks and attendance. If it fails, Excel checks the next condition.

---

## 9. Practical Exercise: Eligibility Status Column

Create the following table in Excel, starting from cell `A1`.

| Student | Attendance (%) | Marks | Status |
|---|---:|---:|---|
| Anu | 85 | 78 | |
| Ravi | 70 | 85 | |
| Priya | 95 | 90 | |
| Kiran | 80 | 35 | |
| Sneha | 75 | 60 | |
| Rahul | 60 | 30 | |

### Eligibility Rule

A student is eligible if:

- Attendance is at least 75%.
- Marks are at least 40.

Both conditions must be true.

### Formula for Cell D2

```excel
=IF(AND(B2>=75,C2>=40),"Eligible","Not Eligible")
```

Drag the formula from `D2` down to `D7`.

### Expected Output

| Student | Expected Status |
|---|---|
| Anu | Eligible |
| Ravi | Not Eligible |
| Priya | Eligible |
| Kiran | Not Eligible |
| Sneha | Eligible |
| Rahul | Not Eligible |

---

## 10. Excel Day 9 Practice Questions and Solutions

### Task 1: Check whether age in A2 is at least 18 AND marks in B2 are at least 40.

```excel
=AND(A2>=18,B2>=40)
```

### Task 2: Check whether marks in B2 are at least 90 OR attendance in C2 is at least 95%.

```excel
=OR(B2>=90,C2>=95)
```

### Task 3: Display Pass if marks in A2 are at least 40; otherwise, display Fail.

```excel
=IF(A2>=40,"Pass","Fail")
```

### Task 4: Attendance must be at least 75% AND marks must be at least 40.

Assume B2 is attendance and C2 is marks.

```excel
=IF(AND(B2>=75,C2>=40),"Eligible","Not Eligible")
```

### Task 5: Display Reward if marks are at least 90 OR attendance is at least 95%.

Assume B2 is marks and C2 is attendance.

```excel
=IF(OR(B2>=90,C2>=95),"Reward","No Reward")
```

### Task 6: Create four status categories using nested IF.

- At least 75 → Excellent
- At least 60 → Good
- At least 40 → Pass
- Otherwise → Fail

```excel
=IF(B2>=75,"Excellent",
   IF(B2>=60,"Good",
      IF(B2>=40,"Pass","Fail")))
```

### Task 7: A job applicant is eligible if age is at least 18 AND marks are at least 50.

Assume A2 is age and B2 is marks.

```excel
=IF(AND(A2>=18,B2>=50),"Eligible","Not Eligible")
```

### Task 8: Classify sales as High, Medium, or Low.

- At least ₹50,000 → High
- At least ₹25,000 → Medium
- Otherwise → Low

Assume sales are in `A2`.

```excel
=IF(A2>=50000,"High",
   IF(A2>=25000,"Medium","Low"))
```

### Task 9: Scholarship eligibility.

- Marks at least 80 AND attendance at least 90% → Scholarship
- Otherwise, marks at least 60 → Consider
- Otherwise → Not Eligible

Assume B2 is marks and C2 is attendance.

```excel
=IF(AND(B2>=80,C2>=90),"Scholarship",
   IF(B2>=60,"Consider","Not Eligible"))
```

### Task 10: Create a status formula.

- Marks at least 80 → Excellent
- Marks at least 40 but below 80 → Pass
- Marks below 40 → Fail

Assume marks are in `A2`.

```excel
=IF(A2>=80,"Excellent",
   IF(A2>=40,"Pass","Fail"))
```

---

## 11. Key Takeaways

- `AND()` checks whether all conditions are true.
- `OR()` checks whether at least one condition is true.
- `IF()` returns a result based on a condition.
- Nested `IF()` checks multiple conditions in sequence.
- Combine `IF()` with `AND()` to enforce multiple requirements.
- Combine `IF()` with `OR()` when one of several requirements is sufficient.
- Put text outputs inside double quotation marks.
- Check higher thresholds first when creating categories.

## ✅ Day 9 Status

- [x] Learned `AND()`.
- [x] Learned `OR()`.
- [x] Revised `IF()`.
- [x] Learned nested `IF()`.
- [x] Created an eligibility/status column.
- [x] Completed all 10 Excel practice tasks.

**Next Goal:** Continue practising Excel logical functions and apply them to real-world datasets for Data Analyst preparation.

#Excel #DataAnalytics #ExcelFormulas #Day9 #100DaysOfLearning
