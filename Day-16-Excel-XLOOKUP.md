# Day 16 — Excel: XLOOKUP Basics

## Topics Learned
- Introduction to XLOOKUP
- XLOOKUP syntax and arguments
- Matching information between two tables
- Bringing customer details into an Orders table
- Handling missing values using Not Found

## 1. What is XLOOKUP?

XLOOKUP is an Excel function used to search for a value in one column and return its matching information from another column.

It helps combine information from different tables using a common value.

## 2. XLOOKUP Syntax

```excel
=XLOOKUP(lookup_value, lookup_array, return_array, [if_not_found])
```

### Understanding the Arguments

| Argument | Meaning |
|---|---|
| lookup_value | Value to search for |
| lookup_array | Column where Excel searches |
| return_array | Column from which the result is returned |
| if_not_found | Message displayed when no match exists |

## 3. Practice Dataset

### Table 1 — Orders

| OrderID | CustomerID | Quantity |
|---|---|---|
| 501 | 101 | 2 |
| 502 | 102 | 1 |
| 503 | 101 | 3 |
| 504 | 103 | 1 |
| 505 | 105 | 2 |

### Table 2 — Customers

| CustomerID | CustomerName | City |
|---|---|---|
| 101 | Akash | Hyderabad |
| 102 | Priya | Bangalore |
| 103 | Rahul | Chennai |
| 104 | Sneha | Mumbai |

## 4. Bring Customer Names into the Orders Table

Suppose:
- Orders table occupies columns A to C.
- Customer table occupies columns G to I.

In cell D1, enter:

CustomerName

In cell D2, enter:

```excel
=XLOOKUP(B2,$G$2:$G$5,$H$2:$H$5,"Not Found")
```

Drag the formula down to D6.

### Expected Output

| OrderID | CustomerID | Quantity | CustomerName |
|---|---|---|---|
| 501 | 101 | 2 | Akash |
| 502 | 102 | 1 | Priya |
| 503 | 101 | 3 | Akash |
| 504 | 103 | 1 | Rahul |
| 505 | 105 | 2 | Not Found |

## 5. Bring City Details into the Orders Table

In cell E1, enter:

City

In cell E2, enter:

```excel
=XLOOKUP(B2,$G$2:$G$5,$I$2:$I$5,"Not Found")
```

Drag the formula down to E6.

### Expected Output

| OrderID | CustomerID | Quantity | CustomerName | City |
|---|---|---|---|---|
| 501 | 101 | 2 | Akash | Hyderabad |
| 502 | 102 | 1 | Priya | Bangalore |
| 503 | 101 | 3 | Akash | Hyderabad |
| 504 | 103 | 1 | Rahul | Chennai |
| 505 | 105 | 2 | Not Found | Not Found |

## 6. Understanding the Dollar ($) Sign

In the formula:

```excel
=XLOOKUP(B2,$G$2:$G$5,$H$2:$H$5,"Not Found")
```

The dollar signs lock the lookup and return ranges.

This prevents the ranges from changing when the formula is dragged down.

## 7. Practice Questions with Solutions

**Q1. What is XLOOKUP used for?**

Answer: To search for a value and return its matching information from another column.

**Q2. Which column is common in both tables?**

Answer: CustomerID.

**Q3. What is the lookup key?**

Answer: CustomerID.

**Q4. Which product or customer matches CustomerID 101?**

Answer: Akash.

**Q5. What happens when CustomerID 105 is searched?**

Answer: Excel displays Not Found because CustomerID 105 is not present in the Customers table.

**Q6. Why do we use $ signs in the formula?**

Answer: To lock the lookup and return ranges when copying the formula down.

## 8. Key Takeaways

- XLOOKUP searches for matching values.
- lookup_value specifies what to search for.
- lookup_array specifies where to search.
- return_array specifies what information to return.
- if_not_found handles missing values.
- Dollar signs help lock cell ranges.

## What I Learned

Today, I learned how to use XLOOKUP to bring customer names and city details into an Orders table using CustomerID as the common lookup key.

**Day 16 — Excel Completed!**
