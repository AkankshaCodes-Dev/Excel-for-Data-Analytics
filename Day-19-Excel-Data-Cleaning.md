# DAY 19 — Excel: Data Cleaning

## Topics Covered
- Introduction to Data Cleaning
- Removing duplicate records
- Finding blank values
- Removing extra spaces
- Standardizing capitalization
- Correcting inconsistent spellings
- Using TRIM(), CLEAN() and PROPER()
- Find & Replace

---

## 1. What is Data Cleaning?

Data cleaning is the process of identifying and correcting errors, missing values, duplicates and inconsistencies in a dataset.

Real-world data is often messy and needs to be cleaned before analysis.

Common data problems include:
- Duplicate records
- Blank cells
- Extra spaces
- Inconsistent spelling
- Different capitalization
- Incorrect formats

## 2. Sample Messy Dataset

| CustomerID | Name | City |
|---|---|---|
| 101 | Akash | Hyderabad |
| 102 | PRIYA | bengaluru |
| 101 | Akash | Hyderabad |
| 103 | Rahul | Hydrabad |
| 104 | | Mumbai |
| 105 | Sneha | |
| 106 | ` Akanksha ` | ` HYDERABAD ` |

## 3. Removing Duplicate Records

Duplicate records are repeated rows containing the same information.

Customer 101 appears twice with identical details.

### Steps

1. Select the dataset.
2. Go to the Data tab.
3. Click Remove Duplicates.
4. Select the columns you want to check.
5. Click OK.

Excel removes duplicate records based on the selected columns.

**Important:** Keep a copy of the original data before removing duplicates.

## 4. Finding Blank Values

Blank values are missing information in cells.

In the sample dataset:
- Customer 104 has a missing name.
- Customer 105 has a missing city.

### Steps to find blanks

1. Select the required data range.
2. Press Ctrl + G.
3. Click Special.
4. Select Blanks.
5. Click OK.

Excel selects blank cells.

### Handling Missing Values

Missing values can be:
- Filled with the correct information if known.
- Replaced with "Unknown" when appropriate.
- Kept blank when the information is unavailable.
- Removed only when justified.

Never fill missing information randomly.

## 5. Removing Extra Spaces

Extra spaces can cause lookup mismatches and inconsistent data.

### Example

`"  Akanksha  "` → `"Akanksha"`

### TRIM() Function

```excel
=TRIM(A2)
```

TRIM removes unnecessary spaces from text.

## 6. Standardizing Capitalization

Names and cities may contain inconsistent capitalization.

### Examples

- HYDERABAD → Hyderabad
- hyderabad → Hyderabad
- PRIYA → Priya

### PROPER() Function

```excel
=PROPER(A2)
```

PROPER capitalizes the first letter of each word.

### UPPER() Function

```excel
=UPPER(A2)
```

Converts text to uppercase.

### LOWER() Function

```excel
=LOWER(A2)
```

Converts text to lowercase.

## 7. Correcting Inconsistent Spelling

Example:

- Hyderabad
- Hydrabad

These are spelling inconsistencies.

PROPER() cannot correct spelling mistakes.

### Find & Replace

1. Press Ctrl + H.
2. Enter the incorrect spelling in Find.
3. Enter the correct spelling in Replace.
4. Click Replace All.

Example:

Hydrabad → Hyderabad

## 8. CLEAN() Function

CLEAN removes many non-printable characters from text.

```excel
=CLEAN(A2)
```

It is useful when data contains unwanted characters from imported files.

## 9. Combining Cleaning Functions

```excel
=PROPER(TRIM(CLEAN(A2)))
```

This formula:
- CLEAN removes many non-printable characters.
- TRIM removes unnecessary spaces.
- PROPER standardizes capitalization.

## 10. Excel Data-Cleaning Tools

| Tool / Function | Purpose |
|---|---|
| Remove Duplicates | Removes repeated records |
| Go To Special → Blanks | Finds blank cells |
| TRIM() | Removes extra spaces |
| CLEAN() | Removes many non-printable characters |
| PROPER() | Standardizes capitalization |
| UPPER() | Converts text to uppercase |
| LOWER() | Converts text to lowercase |
| Find & Replace | Corrects inconsistent values |

---

# 11. Excel Practice

Use the messy dataset above.

### Q1.
Remove duplicate customer records.

### Q2.
Find all blank cells.

### Q3.
Remove extra spaces from customer names and cities.

### Q4.
Standardize capitalization.

### Q5.
Correct "Hydrabad" to "Hyderabad".

### Q6.
Replace missing names and cities with "Unknown" for this exercise.

---

# 12. Practice Solutions

### Solution 1 — Remove Duplicates

Use:

Data → Remove Duplicates

Customer 101 should appear only once.

### Solution 2 — Find Blanks

Use:

Ctrl + G → Special → Blanks → OK

Identify the missing name and city.

### Solution 3 — Remove Extra Spaces

```excel
=TRIM(B2)
```

For city:

```excel
=TRIM(C2)
```

### Solution 4 — Standardize Capitalization

For names:

```excel
=PROPER(TRIM(B2))
```

For cities:

```excel
=PROPER(TRIM(C2))
```

### Solution 5 — Correct Spelling

Use Ctrl + H.

Find:

```text
Hydrabad
```

Replace with:

```text
Hyderabad
```

Click Replace All.

### Solution 6 — Handle Missing Values

Replace missing names and cities with:

```text
Unknown
```

This is the chosen approach for this practice dataset.

---

# 13. Expected Cleaned Dataset

| CustomerID | Name | City |
|---|---|---|
| 101 | Akash | Hyderabad |
| 102 | Priya | Bengaluru |
| 103 | Rahul | Hyderabad |
| 104 | Unknown | Mumbai |
| 105 | Sneha | Unknown |
| 106 | Akanksha | Hyderabad |

## 14. Key Takeaways

- Data cleaning improves data quality.
- Duplicate records can affect calculations.
- Blank values should be handled carefully.
- TRIM() removes extra spaces.
- CLEAN() removes many non-printable characters.
- PROPER() standardizes capitalization.
- Find & Replace corrects inconsistent spellings.
- Clean data leads to more reliable analysis.

## Day 19 Completion

- [x] Learned data-cleaning basics.
- [x] Removed duplicates.
- [x] Identified blank values.
- [x] Removed extra spaces.
- [x] Standardized capitalization.
- [x] Corrected inconsistent spellings.
- [x] Practised Excel cleaning tools and formulas.

**Day 19 — Excel Learning Completed!**
