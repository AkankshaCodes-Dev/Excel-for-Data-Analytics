# DAY 18 — Excel: INDEX + MATCH

## Topics Covered
- Introduction to INDEX
- Introduction to MATCH
- Understanding INDEX and MATCH syntax
- Combining INDEX and MATCH
- Practical lookup examples
- INDEX + MATCH vs VLOOKUP
- Handling missing values using IFERROR

---

## 1. What is INDEX?

INDEX is an Excel function that returns a value from a specified position in a selected range.

### Example: Employee Details

| Employee ID | Name | Department | Salary |
|---|---|---|---:|
| 101 | Akash | IT | 25000 |
| 102 | Priya | HR | 30000 |
| 103 | Rahul | Sales | 28000 |
| 104 | Sneha | IT | 35000 |
| 105 | Anjali | Finance | 32000 |

Suppose we want to retrieve the second name from the Name column.

```excel
=INDEX(B2:B6,2)
```

**Expected Output:** Priya

INDEX returns the value from the specified position.

## 2. What is MATCH?

MATCH searches for a particular value in a range and returns its relative position.

### Example

```excel
=MATCH(103,A2:A6,0)
```

**Expected Output:** 3

Employee ID 103 is in the third position of the selected range.

### MATCH Syntax

```excel
=MATCH(lookup_value, lookup_array, [match_type])
```

| Argument | Meaning |
|---|---|
| lookup_value | Value to search for |
| lookup_array | Range where Excel searches |
| match_type | 0 for exact match |

## 3. Combining INDEX and MATCH

INDEX and MATCH can work together to retrieve information based on a lookup value.

- MATCH finds the position of the required value.
- INDEX retrieves the corresponding value from another range.

### Practical Example — Find Employee Salary

Suppose employee ID 103 is entered in cell E2.

```excel
=INDEX(D2:D6,MATCH(E2,A2:A6,0))
```

**Expected Output:** 28000

### Understanding the Formula

**Step 1 — MATCH**

```excel
=MATCH(E2,A2:A6,0)
```

Finds employee ID 103 and returns position 3.

**Step 2 — INDEX**

```excel
=INDEX(D2:D6,3)
```

Returns the third value from the Salary range, which is 28000.

**Combined Formula**

```excel
=INDEX(D2:D6,MATCH(E2,A2:A6,0))
```

## 4. More INDEX + MATCH Examples

### Find Employee Name

```excel
=INDEX(B2:B6,MATCH(E2,A2:A6,0))
```

**Expected Output:** Rahul

### Find Employee Department

```excel
=INDEX(C2:C6,MATCH(E2,A2:A6,0))
```

**Expected Output:** Sales

### Find Employee Salary

```excel
=INDEX(D2:D6,MATCH(E2,A2:A6,0))
```

**Expected Output:** 28000

## 5. INDEX + MATCH vs VLOOKUP

| VLOOKUP | INDEX + MATCH |
|---|---|
| Searches in the first column of the selected range | MATCH can search in any selected range |
| Returns values to the right | Can return values to the left or right |
| Uses a column index number | Uses separate lookup and return ranges |
| Can be affected by inserting columns within its selected range | More flexible when columns are rearranged |

### VLOOKUP Example

```excel
=VLOOKUP(E2,A2:D6,4,FALSE)
```

### INDEX + MATCH Example

```excel
=INDEX(D2:D6,MATCH(E2,A2:A6,0))
```

Both formulas return 28000 when E2 contains 103.

## 6. Handling Missing Values Using IFERROR

If the employee ID does not exist, MATCH returns an #N/A error.

We can handle this using IFERROR.

```excel
=IFERROR(INDEX(B2:B6,MATCH(E2,A2:A6,0)),"Not Found")
```

If employee ID 106 is not available:

**Expected Output:** Not Found

---

# 7. Excel Practice Questions

Use the Employee Details dataset provided above.

Enter the employee ID you want to search in cell F2.

### Q1.
Find the employee name for ID 103 using INDEX + MATCH.

### Q2.
Find the salary for employee ID 102.

### Q3.
Find the department for employee ID 105.

### Q4.
Find the salary for employee ID 104.

### Q5.
Search for employee ID 106 and display "Not Found" if it does not exist.

---

# 8. Excel Practice Solutions

### Solution 1 — Find Employee Name

```excel
=INDEX(B2:B6,MATCH(F2,A2:A6,0))
```

**Expected Output:** Rahul

### Solution 2 — Find Employee Salary

```excel
=INDEX(D2:D6,MATCH(F2,A2:A6,0))
```

**Expected Output:** 30000

### Solution 3 — Find Employee Department

```excel
=INDEX(C2:C6,MATCH(F2,A2:A6,0))
```

**Expected Output:** Finance

### Solution 4 — Find Employee Salary

```excel
=INDEX(D2:D6,MATCH(F2,A2:A6,0))
```

**Expected Output:** 35000

### Solution 5 — Handle Missing Employee ID

```excel
=IFERROR(INDEX(B2:B6,MATCH(F2,A2:A6,0)),"Not Found")
```

**Expected Output:** Not Found

---

# 9. Key Takeaways

- INDEX retrieves a value from a specified position.
- MATCH finds the position of a lookup value.
- INDEX + MATCH combines both functions to retrieve information.
- MATCH uses 0 for exact matching.
- INDEX + MATCH can retrieve values from columns to the left or right.
- IFERROR helps handle missing lookup values.

## Day 18 Completion

- [x] Learned INDEX function.
- [x] Learned MATCH function.
- [x] Combined INDEX + MATCH.
- [x] Compared INDEX + MATCH with VLOOKUP.
- [x] Practised five Excel questions.

**Day 18 — Excel Learning Completed!**
