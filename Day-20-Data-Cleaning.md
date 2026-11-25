# DAY 20 — Excel: Data Cleaning

## Topics Covered

- Introduction to data cleaning
- Find & Replace
- Text to Columns
- Flash Fill
- Cleaning inconsistent names
- Correcting spelling mistakes
- Separating combined fields
- Preparing data for analysis

---

## 1. Introduction

Data cleaning is the process of identifying and correcting incorrect, inconsistent or improperly formatted data.

Raw datasets may contain:

- Spelling mistakes
- Inconsistent category names
- Combined information in one column
- Unorganized names
- Incorrect text formats

Excel provides several tools to clean and organize this information.

## 2. Find & Replace

Find & Replace is used to search for specific text and replace it with the correct value.

### Example

Consider the following category column:

| Original Category |
|---|
| Electonics |
| Fashion |
| Electonics |
| Furniture |
| Electonics |

Here, Electronics is misspelled as Electonics.

### Steps

1. Open the Excel worksheet.
2. Press Ctrl + H.
3. Enter `Electonics` in Find what.
4. Enter `Electronics` in Replace with.
5. Click Replace All.

### Expected Output

| Corrected Category |
|---|
| Electronics |
| Fashion |
| Electronics |
| Furniture |
| Electronics |

**Key Point:** Find & Replace helps correct repeated spelling mistakes quickly.

## 3. Text to Columns

Text to Columns is used to separate combined information into multiple columns.

### Example

Suppose a dataset contains full names in a single column.

| Full Name |
|---|
| Akanksha Sharma |
| Priya Reddy |
| Rahul Kumar |

We want to separate first names and last names.

### Steps

1. Select the Full Name column.
2. Open the Data tab.
3. Select Text to Columns.
4. Choose Delimited.
5. Click Next.
6. Select Space as the delimiter.
7. Click Finish.

### Expected Output

| First Name | Last Name |
|---|---|
| Akanksha | Sharma |
| Priya | Reddy |
| Rahul | Kumar |

**Key Point:** Text to Columns separates information using delimiters such as spaces, commas and tabs.

## 4. Flash Fill

Flash Fill automatically recognizes a pattern and fills the remaining cells.

It is useful for extracting or rearranging information.

### Example

Original dataset:

| Full Name | First Name |
|---|---|
| Akanksha Sharma | Akanksha |
| Priya Reddy | |
| Rahul Kumar | |

We want to extract first names.

### Steps

1. Enter Akanksha in the first First Name cell.
2. Move to the next empty cell in that column.
3. Press Ctrl + E.
4. Excel recognizes the pattern.
5. The remaining first names are automatically filled.

### Expected Output

| Full Name | First Name |
|---|---|
| Akanksha Sharma | Akanksha |
| Priya Reddy | Priya |
| Rahul Kumar | Rahul |

**Key Point:** Flash Fill recognizes patterns without requiring complicated formulas.

## 5. Difference Between Find & Replace, Text to Columns and Flash Fill

| Tool | Purpose |
|---|---|
| Find & Replace | Finds and corrects unwanted text |
| Text to Columns | Splits combined information |
| Flash Fill | Automatically fills data based on patterns |

## 6. Practical Data Cleaning Examples

### Example 1 — Correcting City Names

Original:

| City |
|---|
| Hydrabad |
| Bangalore |
| Hydrabad |
| Mumbai |

Correct Hydrabad to Hyderabad using Find & Replace.

### Example 2 — Separating City and State

Original:

| Location |
|---|
| Raichur, Karnataka |
| Hyderabad, Telangana |
| Mumbai, Maharashtra |

Use Text to Columns with a comma delimiter.

Expected:

| City | State |
|---|---|
| Raichur | Karnataka |
| Hyderabad | Telangana |
| Mumbai | Maharashtra |

### Example 3 — Extracting First Names

Use Flash Fill to extract first names from full names.

## 7. Excel Practice Questions

### Q1.
Correct the spelling Hydrabad to Hyderabad using Find & Replace.

### Q2.
Correct Electonics to Electronics.

### Q3.
Separate first names and last names using Text to Columns.

### Q4.
Separate city and state using a comma delimiter.

### Q5.
Extract first names using Flash Fill.

### Q6.
Extract last names using Flash Fill.

### Q7.
Identify inconsistent category names in a dataset.

### Q8.
Clean combined fields and organize the information into separate columns.

## 8. Key Takeaways

- Data cleaning improves data quality.
- Find & Replace corrects repeated text mistakes.
- Text to Columns separates combined information.
- Flash Fill recognizes patterns automatically.
- Clean data makes analysis easier and more reliable.
- Excel data cleaning is an important skill for Data Analysts.

## Day 20 Completion

- [x] Learned Find & Replace.
- [x] Learned Text to Columns.
- [x] Learned Flash Fill.
- [x] Understood practical data cleaning examples.
- [ ] Completed all practical exercises.

**Day 20 — Excel Learning Completed!**
