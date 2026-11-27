# DAY 21 — EXCEL: LOOKUP & DATA CLEANING CHECKPOINT

## Topics Covered

- XLOOKUP revision
- VLOOKUP revision
- Matching two related datasets
- Identifying missing records
- Removing duplicate values
- Handling blank cells
- Correcting inconsistent data
- TRIM() function
- Practical dataset cleaning

---

## 1. Introduction

Excel is an important tool for Data Analysts.

Today, we revise lookup functions and data-cleaning techniques used to combine and prepare datasets for analysis.

These techniques help analysts:
- Match information between different datasets.
- Find missing records.
- Identify duplicate values.
- Correct inconsistent text.
- Prepare clean data for reporting.

## 2. Sample Datasets

### Dataset 1 — Employees

| Employee ID | Name |
|---|---|
| 101 | Akash |
| 102 | Ravi |
| 103 | Priya |

### Dataset 2 — Salaries

| Employee ID | Salary |
|---|---:|
| 101 | 20000 |
| 102 | 25000 |
| 104 | 30000 |

## 3. XLOOKUP

XLOOKUP searches for a value in one range and returns the corresponding value from another range.

### Syntax

```excel
=XLOOKUP(lookup_value, lookup_array, return_array, [if_not_found])
```

### Example

```excel
=XLOOKUP(A2,Sheet2!A:A,Sheet2!B:B,"Not Found")
```

**Explanation:**

- A2: Employee ID to search.
- Sheet2!A:A: Employee ID column.
- Sheet2!B:B: Salary column.
- Not Found: Message when no match exists.

### Expected Output

| Employee ID | Name | Salary |
|---|---|---:|
| 101 | Akash | 20000 |
| 102 | Ravi | 25000 |
| 103 | Priya | Not Found |

## 4. VLOOKUP

VLOOKUP searches for a value in the first column of a selected table range and returns a value from another column.

### Syntax

```excel
=VLOOKUP(lookup_value, table_array, col_index_num, [range_lookup])
```

### Example

```excel
=VLOOKUP(A2,Sheet2!A:B,2,FALSE)
```

**Explanation:**

- A2: Employee ID to search.
- Sheet2!A:B: Table containing employee IDs and salaries.
- 2: Returns the value from the second column.
- FALSE: Finds an exact match.

**Important:** VLOOKUP searches from left to right. XLOOKUP is more flexible because its lookup and return ranges can be in either order.

## 5. XLOOKUP vs VLOOKUP

| Feature | XLOOKUP | VLOOKUP |
|---|---|---|
| Search direction | Both directions | Left to right |
| Exact match | Default | Specify FALSE |
| Return column | Separate range | Column number |
| Not found message | Built-in argument | Usually IFERROR |
| Flexibility | More flexible | Less flexible |

## 6. Data Cleaning Techniques

Data cleaning means identifying and correcting errors or inconsistencies in a dataset.

### A. Remove Duplicates

Duplicates are repeated records in a dataset.

Steps:
1. Select the dataset.
2. Open the Data tab.
3. Select Remove Duplicates.
4. Choose the columns to check.
5. Click OK.

**Example:** If Employee ID 101 appears twice, check whether it is a genuine duplicate before removing it.

### B. Handle Blank Cells

Blank cells represent missing information.

Steps:
1. Select the dataset.
2. Open Filter.
3. Select the column filter.
4. Choose Blanks.
5. Inspect the missing values.

Do not automatically replace every blank with zero. Decide how to handle it based on the meaning of the data.

### C. Find and Replace

Find and Replace helps correct inconsistent spelling.

Example:

- Hydrabad → Hyderabad
- Banglore → Bangalore

Shortcut: Ctrl + H

### D. TRIM() Function

TRIM removes unnecessary spaces from text.

Syntax:

```excel
=TRIM(A2)
```

Example:

Original: `"  Akash  "`

Cleaned: `"Akash"`

### E. Identify Missing Records

When matching two datasets, some records may not have a corresponding match.

Example:

- Employee ID 103 has no salary record.
- Employee ID 104 has no matching employee record.

These records should be investigated.

## 7. Practical Exercise — Match Two Datasets

Use the Employees and Salaries datasets from Section 2.

### Tasks

1. Use XLOOKUP to bring salary into the Employees dataset.
2. Identify employees without matching salary records.
3. Identify salary records without matching employees.
4. Check for duplicate Employee IDs.
5. Identify blank cells.
6. Clean unnecessary spaces using TRIM().

### Expected Result

| Employee ID | Name | Salary |
|---|---|---:|
| 101 | Akash | 20000 |
| 102 | Ravi | 25000 |
| 103 | Priya | Not Found |

### Practice Questions

1. What is the purpose of XLOOKUP?
2. What does VLOOKUP search for?
3. Which function removes unnecessary spaces?
4. Which Excel feature removes duplicate records?
5. Which shortcut opens Find and Replace?
6. Why should missing values be checked before analysis?
7. What is the difference between XLOOKUP and VLOOKUP?

### Solutions

1. Searches for a value and returns a corresponding value.
2. Searches in the first column of a selected table range.
3. TRIM().
4. Remove Duplicates.
5. Ctrl + H.
6. Missing values can affect calculations and analysis.
7. XLOOKUP supports flexible lookup directions, while VLOOKUP searches from left to right.

## 8. Key Takeaways

- XLOOKUP and VLOOKUP help match related datasets.
- XLOOKUP offers more flexibility.
- Remove Duplicates helps identify repeated records.
- Find and Replace corrects inconsistent spelling.
- TRIM removes unnecessary spaces.
- Missing records should be investigated before analysis.
- Clean data produces more reliable results.

## Completion Checklist

- [ ] Revised XLOOKUP
- [ ] Revised VLOOKUP
- [ ] Compared both lookup functions
- [ ] Practised matching two datasets
- [ ] Checked duplicate records
- [ ] Identified blank cells
- [ ] Practised Find and Replace
- [ ] Used TRIM()
- [ ] Completed Excel practical exercise

**Day 21 Excel Checkpoint — Completed / In Progress**
