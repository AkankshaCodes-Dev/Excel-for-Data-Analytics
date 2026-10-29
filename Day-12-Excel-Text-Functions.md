# 📗 Day 12 — Excel Text Functions

## 🎯 Learning Objectives

In Day 12, I learned how to use Excel text functions to clean messy text, standardize names and categories, extract characters, and count text length.

These functions help prepare raw datasets for reporting, visualization, and data analysis.

## 1. TRIM() — Remove Extra Spaces

**Meaning:** Removes leading and trailing ordinary spaces and reduces repeated spaces between words to a single space.

**Syntax:**
```excel
=TRIM(text)
```

**Example:**

If A2 contains `  Akanksha   Sharma  `

```excel
=TRIM(A2)
```

**Output:** `Akanksha Sharma`

**Use case:** Cleaning customer names and product categories.

## 2. CLEAN() — Remove Nonprinting Characters

**Meaning:** Removes many nonprinting characters from text.

**Syntax:**
```excel
=CLEAN(text)
```

**Example:**
```excel
=CLEAN(A2)
```

This helps remove unwanted control characters from imported data.

**Important:** CLEAN does not remove every unusual character or all extra spaces. Combine it with TRIM when necessary.

```excel
=TRIM(CLEAN(A2))
```

## 3. UPPER() — Convert Text to Uppercase

**Meaning:** Converts text to uppercase.

**Syntax:**
```excel
=UPPER(text)
```

**Example:**
```excel
=UPPER("electronics")
```

**Output:** `ELECTRONICS`

**Use case:** Standardizing product categories and codes.

## 4. LOWER() — Convert Text to Lowercase

**Meaning:** Converts text to lowercase.

**Syntax:**
```excel
=LOWER(text)
```

**Example:**
```excel
=LOWER("BALLARI")
```

**Output:** `ballari`

**Use case:** Standardizing city names and text fields.

## 5. PROPER() — Capitalize Words

**Meaning:** Converts the first letter of each word to uppercase and other letters to lowercase.

**Syntax:**
```excel
=PROPER(text)
```

**Example:**
```excel
=PROPER("akanksha sharma")
```

**Output:** `Akanksha Sharma`

**Use case:** Formatting customer names and titles consistently.

Note: PROPER may not format every name correctly, especially names with special capitalization conventions.

## 6. LEFT() — Extract Characters from the Beginning

**Meaning:** Returns a specified number of characters from the left side of a text string.

**Syntax:**
```excel
=LEFT(text, [num_chars])
```

**Example:**
```excel
=LEFT("PRD105",3)
```

**Output:** `PRD`

**Use case:** Extracting product prefixes and category codes.

## 7. RIGHT() — Extract Characters from the End

**Meaning:** Returns a specified number of characters from the right side of a string.

**Syntax:**
```excel
=RIGHT(text, [num_chars])
```

**Example:**
```excel
=RIGHT("PRD105",3)
```

**Output:** `105`

**Use case:** Extracting the numeric portion of a product code.

## 8. MID() — Extract Characters from the Middle

**Meaning:** Returns a specified number of characters beginning at a chosen position.

**Syntax:**
```excel
=MID(text, start_num, num_chars)
```

**Example:**
```excel
=MID("PRD105",4,3)
```

**Output:** `105`

**Explanation:**
- Text: `PRD105`
- Starting position: `4`
- Number of characters: `3`

## 9. LEN() — Count Characters

**Meaning:** Counts the number of characters in a text string, including spaces.

**Syntax:**
```excel
=LEN(text)
```

**Example:**
```excel
=LEN("PRD105")
```

**Output:** `6`

Another example:

```excel
=LEN("A B")
```

Output: `3`, because the space also counts as a character.

**Use case:** Checking product code lengths and finding inconsistent identifiers.

## 10. Combining Text Functions

Suppose A2 contains a messy customer name.

```excel
=PROPER(TRIM(CLEAN(A2)))
```

**How it works:**
1. `CLEAN(A2)` removes many nonprinting characters.
2. `TRIM(...)` removes unnecessary ordinary spaces.
3. `PROPER(...)` standardizes capitalization.

Suppose A3 contains `  electronics  `.

```excel
=UPPER(TRIM(A3))
```

Output: `ELECTRONICS`

**Note:** Imported nonbreaking spaces may require an additional `SUBSTITUTE()` step. TRIM and CLEAN do not remove every possible kind of unwanted character.

## 11. Sample Practice Data

Enter these values into Excel:

| Cell | Value |
|---|---|
| A2 | `  akanksha sharma  ` |
| A3 | `RAHUL KUMAR` |
| A4 | `priya reddy` |
| A5 | `prd101` |
| A6 | `PRD205` |
| A7 | `  electronics  ` |
| A8 | `BALLARI` |
| A9 | `home decor` |
| A10 | `SKU98765` |
| A11 | `Data Analytics` |

## 12. Practice Questions with Answers

### Q1. Remove extra spaces from A2.

```excel
=TRIM(A2)
```

### Q2. Convert A3 to lowercase.

```excel
=LOWER(A3)
```

### Q3. Convert A4 to Proper Case.

```excel
=PROPER(A4)
```

### Q4. Convert A5 to uppercase.

```excel
=UPPER(A5)
```

### Q5. Extract the first three characters from A6.

```excel
=LEFT(A6,3)
```

Output: `PRD`

### Q6. Extract the last three characters from A10.

```excel
=RIGHT(A10,3)
```

Output: `765`

### Q7. Extract three characters starting at position 4 from A10.

```excel
=MID(A10,4,3)
```

Output: `987`

### Q8. Count the characters in A11.

```excel
=LEN(A11)
```

Output: `14`

The space between `Data` and `Analytics` counts as one character.

### Q9. Remove extra spaces from A7 and convert it to uppercase.

```excel
=UPPER(TRIM(A7))
```

Output: `ELECTRONICS`

### Q10. Clean A2 and standardize its capitalization.

```excel
=PROPER(TRIM(CLEAN(A2)))
```

Expected output: `Akanksha Sharma`

## 13. Day 12 Revision Table

| Function | Purpose |
|---|---|
| TRIM | Removes extra ordinary spaces |
| CLEAN | Removes many nonprinting characters |
| UPPER | Converts text to uppercase |
| LOWER | Converts text to lowercase |
| PROPER | Capitalizes the first letter of each word |
| LEFT | Extracts characters from the left |
| RIGHT | Extracts characters from the right |
| MID | Extracts characters from a specified position |
| LEN | Counts characters |

## 🚀 Day 12 Key Takeaway

Excel text functions make it easier to clean inconsistent text, standardize customer information, extract product identifiers, and prepare datasets for analysis.

## 📌 Skills Practiced

- Text cleaning
- Data standardization
- Character extraction
- Text length validation
- Combining functions

#Excel #DataAnalytics #ExcelFunctions #30DaysOfLearning
