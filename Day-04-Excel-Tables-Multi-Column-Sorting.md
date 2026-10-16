
# Day 04 - Excel Tables and Multi-Column Sorting

## 1. Excel Tables

An Excel Table is a structured range of data that helps us organize, manage, filter, and sort information easily.

### How to Create an Excel Table
1. Select any cell inside your dataset.
2. Press Ctrl + T.
3. Check the "My table has headers" option.
4. Click OK.

### Example

Before converting the data into a table:

| Employee_Name | Department | Salary |
|---|---|---:|
| Kiran | Sales | 35000 |
| Anu | IT | 30000 |
| Ravi | Sales | 40000 |
| Priya | IT | 25000 |

After pressing Ctrl + T, Excel formats the selected data as a structured table with header filters.

### Advantages of Excel Tables
- Easy sorting and filtering.
- Consistent formatting.
- Automatic expansion when new rows are added.
- Better data organization.
- Easier use of structured references in formulas.

## 2. Excel Table Styles

Table Styles help improve the appearance and readability of a dataset.

### How to Apply a Table Style
1. Click any cell inside the table.
2. Open the Table Design tab.
3. Choose a style from the Table Styles gallery.

### Example

A table can use alternating row colours and a highlighted header to make employee names, departments, and salaries easier to read.

## 3. Multi-Column Sorting

Multi-column sorting means sorting data using two or more columns in a specified priority order.

### Example Dataset

| Employee_Name | Department | Salary |
|---|---|---:|
| Kiran | Sales | 35000 |
| Anu | IT | 30000 |
| Ravi | Sales | 40000 |
| Priya | IT | 25000 |
| Rahul | Sales | 45000 |

### Practical Example

Requirement:
- First, sort Department from A to Z.
- Then, sort Salary from Largest to Smallest within each department.

### Steps
1. Click inside the Excel Table.
2. Go to Data → Sort.
3. Select Department under Sort by.
4. Choose A to Z.
5. Click Add Level.
6. Select Salary under Then by.
7. Choose Largest to Smallest.
8. Click OK.

### Expected Result

| Employee_Name | Department | Salary |
|---|---|---:|
| Anu | IT | 30000 |
| Priya | IT | 25000 |
| Rahul | Sales | 45000 |
| Ravi | Sales | 40000 |
| Kiran | Sales | 35000 |

### Another Practice Example

Requirement:
- Sort Department from Z to A.
- Sort Salary from Smallest to Largest within each department.

Use Data → Sort → Add Level to apply both rules.

## 4. Key Learnings

- Excel Tables organize data into a structured format.
- Table Styles improve readability.
- Multi-column sorting applies rules in priority order.
- Sorting the entire table keeps each employee's details together.
- The second sorting level determines the order within groups that share the same first-level value.

## Practice Status

- Created an Excel Table.
- Applied a Table Style.
- Practised multi-column sorting.
