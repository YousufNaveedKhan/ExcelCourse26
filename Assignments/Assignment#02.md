# Assignment #02: Revision of Lec01 to Lec07

**Given:** Wednesday, 21 October 2026
**Submission:** Next class, Friday, 23 October 2026

This assignment uses everything we have done so far: formatting, formulas, `IF`, sorting and filtering, conditional formatting, `COUNTIF` / `SUMIF`, data validation, `VLOOKUP` and PivotTables.

Make **one workbook** named `Assignment02-YourName.xlsx`. You will make **four sheets**: `Sales`, `Summary`, `Search` and `Pivot`.

---

## Part 1: Sales Sheet (Lec01, Lec02, Lec03)

A small company sells four products through three salespersons. Rename `Sheet1` to `Sales` and enter this data:

| Order ID | Salesperson | Region | Product | Qty | Unit Price |
|---|---|---|---|---|---|
| ORD-01 | Ali | North | Laptop | 2 | 85000 |
| ORD-02 | Sara | South | Phone | 4 | 45000 |
| ORD-03 | Bilal | East | Monitor | 3 | 30000 |
| ORD-04 | Ali | South | Chair | 10 | 8000 |
| ORD-05 | Sara | North | Laptop | 3 | 85000 |
| ORD-06 | Bilal | South | Phone | 2 | 45000 |
| ORD-07 | Ali | East | Monitor | 4 | 30000 |
| ORD-08 | Sara | East | Chair | 25 | 8000 |
| ORD-09 | Bilal | North | Laptop | 1 | 85000 |
| ORD-10 | Ali | North | Phone | 5 | 45000 |
| ORD-11 | Sara | South | Monitor | 2 | 30000 |
| ORD-12 | Bilal | East | Chair | 12 | 8000 |

Add these columns and fill them with **formulas**:

1. **Total** = Qty × Unit Price
2. **Discount %:** use a **nested `IF`** on Total:
   * 200,000 or more → 10%
   * 100,000 or more → 5%
   * otherwise → 0%
3. **Net Amount** = Total − (Total × Discount %)

Then format the sheet: bold headings, borders, proper column widths, money columns as numbers with commas, and the Discount % column as %.

**Check your work:** ORD-01 has Total 170,000, Discount 5% and Net Amount 161,500. ORD-08 has Total exactly 200,000, so it must get 10%.

---

## Part 2: Table, Sort, Filter and Conditional Formatting (Lec04)

Still on the `Sales` sheet:

1. Click inside the data and convert it into a **Table** (`Ctrl + T`).
2. **Sort** the table by Net Amount, largest to smallest.
3. **Conditional formatting:**
   * Add **Data Bars** to the Net Amount column.
   * Highlight every **Qty less than 3** in light red.
4. **Filter** the Region column to show only **North**, take a screenshot, then clear the filter.

---

## Part 3: Summary Sheet (Lec05)

Make a new sheet named `Summary` with this layout:

| Product | No. of Orders | Total Net Amount |
|---|---|---|
| Laptop | | |
| Phone | | |
| Monitor | | |
| Chair | | |

1. **No. of Orders:** use `COUNTIF` on the Product column of the `Sales` sheet.
2. **Total Net Amount:** use `SUMIF` on the Product column, adding up the Net Amount column.
3. In a cell below the table, find the **total Net Amount of the North region** with `SUMIF`.

**Check your work:** Every product has 3 orders. Laptop's Total Net Amount is 476,000.

---

## Part 4: Search Sheet (Lec05, Lec06)

Make a new sheet named `Search` where you can pick any order and see its details:

| | |
|---|---|
| Order ID: | *(dropdown)* |
| Salesperson: | |
| Product: | |
| Qty: | |
| Net Amount: | |

1. In the cell next to **Order ID**, add a **Data Validation** dropdown (List) that shows all Order IDs from the `Sales` sheet.
2. Fill the other cells using **`VLOOKUP`** with exact match (`0` or `FALSE` as the last argument).
3. Change the Order ID from the dropdown and check that all the details change with it.

**Check your work:** Selecting ORD-10 should show Ali, Phone, 5 and 202,500.

---

## Part 5: PivotTable and PivotChart (Lec07)

Use the `Sales` table to make a **PivotTable** on a new sheet named `Pivot`:

1. **Rows:** Salesperson. **Values:** Sum of Net Amount.
2. Add **Region** as a **Filter** and try selecting different regions.
3. Insert a **PivotChart** (column chart) for this PivotTable.
4. Below it, make a second PivotTable showing **Product-wise** Sum of Net Amount.

**Check your work:** With all regions selected, Sara has the highest sale: 640,500.

---

## Rules

* Every calculated cell must have a **formula**. Do not type answers by hand.
* Write each formula once and copy it down the column.
* Name every sheet exactly as given above.
* Submit the `.xlsx` file and the filter screenshot from Part 2.
