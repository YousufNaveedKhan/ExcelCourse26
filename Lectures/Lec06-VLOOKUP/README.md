# Lec06: VLOOKUP

**Workbook:** [Lec06-VLOOKUP.xlsx](./Lec06-VLOOKUP.xlsx)

In this lecture we make a **Summary** sheet: type a Roll No and Excel finds that student's name, marks and grade from the marksheet.

## VLOOKUP

```
=VLOOKUP(lookup_value, table_array, col_index_num, range_lookup)
```

| Part | Meaning | In the workbook |
|---|---|---|
| `lookup_value` | What to search for | `B1` (the Roll No typed) |
| `table_array` | Where to search | `Table1[#All]` (the marksheet) |
| `col_index_num` | Which column number to bring back | `2` for Name, `10` for Grade |
| `range_lookup` | `0` / `FALSE` = exact match | `0` |

```
=VLOOKUP(B1, Table1[#All], 2, 0)    Name
=VLOOKUP(B1, Table1[#All], 7, 0)    Obtained
=VLOOKUP(B1, Table1[#All], 10, 0)   Grade
```

Rules to remember:

* VLOOKUP searches only in the **first column** of the table. Here that is ROLL NO.
* Count columns from the table's first column: ROLL NO = 1, Name = 2, Section = 3…
* Always use `0` at the end for exact match, unless you really need an approximate match.

## Tables and Structured References

When data is a Table, formulas use names instead of cell addresses:

| Reference | Meaning |
|---|---|
| `Table1[#All]` | The whole table, including headings |
| `Table13[[#This Row],[JAN]:[MAR]]` | JAN to MAR in the same row |
| `Table13[[#This Row],[OBTAINED]]` | OBTAINED in the same row |

New rows added to the Table are included automatically.

## Errors

| Error | Usual reason |
|---|---|
| `#N/A` | The Roll No does not exist, or there is an extra space |
| `#REF!` | The column number is bigger than the table |

## Common Mistakes

* Using `1` or leaving out the last argument, which gives wrong answers on unsorted data.
* Counting the column number from column A of the sheet instead of the table's first column.

## Practice

Add a Data Validation dropdown (Lec05) to the Roll No cell so the user can pick a Roll No instead of typing it.
