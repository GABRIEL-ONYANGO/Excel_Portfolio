# Excel Data Cleaning Lab

A hands-on lab that teaches core data-cleaning techniques in Excel for the web, using a customer demographics and sales dataset.

## Objectives

- Deal with irrelevant or inaccurate data
- Remove empty rows and duplicated data
- Change text case and date formatting
- Trim whitespace from data
- Use Flash Fill and functions to clean data

## Prerequisites

- A Microsoft account with access to Excel for the web
- The dataset file: `Customer_demographics_and_sales_Lab5.xlsx`

## Getting Started

1. Download `Customer_demographics_and_sales_Lab5.xlsx`.
2. Upload it to OneDrive (or Microsoft 365) and open it in Excel for the web.
3. Work through the exercises below in order, since later tasks build on earlier ones.

## Lab Structure

### Exercise 1: Removing Duplicated, Irrelevant or Inaccurate Data

| Task | Description | Key Features |
|------|-------------|--------------|
| A | Check spelling in `CREDITCARD_TYPE` (column L). Leave `jcb` unchanged for Task D. | Review > Spelling |
| B | Remove empty rows by filtering `CUST_NAME` for blanks and deleting them. | Filter, Delete Rows |
| C | Highlight and remove duplicate rows using the unique `ORDER_ID` (column T). | Conditional Formatting, Remove Duplicates |
| D | Correct the `jcb` misspelling to `JCB`. | Find & Replace |

### Exercise 2: Dealing with Inconsistencies in Data

| Task | Description | Key Features |
|------|-------------|--------------|
| A | Convert header text from upper case to proper case. | `PROPER()` |
| B | Convert the `Generation` column (AG) to upper case. | `UPPER()`, Fill Handle |
| C | Convert the `T_Type` column (AC) to lower case. | `LOWER()`, Fill Handle |
| D | Format `Order_Ship_Date` (column Z) as a long date, e.g. *Wednesday, March 14, 2012*. | Number Format, Locale: English (US) |
| E | Replace double spaces with single spaces across the data. | Find & Replace |

### Exercise 3: More Excel Features for Cleaning Data

| Task | Description | Key Features |
|------|-------------|--------------|
| A | Split a name such as `Mr. Allen Perl` using pattern recognition, then undo. | Flash Fill |
| B | Split `Cust_Name` into first and last name columns. | `LEFT()`, `RIGHT()`, `LEN()`, `SEARCH()` |

## Common Technique: Convert Formulas to Values

Several tasks use the same helper-column pattern:

1. Insert a new column or row next to the data to clean.
2. Enter a formula (`PROPER`, `UPPER`, `LOWER`) and fill it down with the Fill Handle.
3. Copy the result and paste it over the original using **Paste Options > Values**.
4. Delete the helper column or row.

## Key Formulas

```excel
=PROPER(A1)                                  ' Capitalize each word
=UPPER(AH2)                                  ' Convert to UPPER CASE
=LOWER(AD2)                                  ' Convert to lower case
=LEFT(C2, SEARCH(" ",C2,1))                  ' Extract first name
=RIGHT(C2,LEN(C2)-SEARCH(" ",C2,1))          ' Extract last name
```

## Useful Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl+Home` | Jump to the first cell |
| `Ctrl+Shift+End` | Select to the last used cell |
| `Ctrl+C` | Copy |

## Tips

- Work on a copy of the original file so you can start over if needed.
- Complete Exercise 1 Task D before clearing conditional formatting rules.
- Do not fix `jcb` during the spell check; it is needed for the Find & Replace task.

## Learning Outcomes

After completing this lab you will be able to:

- Spot and fix spelling errors, blanks, and duplicates
- Standardize text case and date formats
- Remove stray whitespace
- Use Flash Fill and text functions to split and reshape data

## License

Add a license of your choice (e.g. MIT) before publishing.
