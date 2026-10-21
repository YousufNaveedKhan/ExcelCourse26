# Lec04: Sorting, Filtering and Conditional Formatting

**Workbook:** [Lec04-Sorting-Filtering-and-Conditional-Formatting.xlsx](./Lec04-Sorting-Filtering-and-Conditional-Formatting.xlsx)

In this lecture we work with a product list: turn it into a Table, sort and filter it, and colour cells automatically.

## Excel Tables

Click anywhere inside your data and press **`Ctrl + T`** (or **Insert → Table**). Make sure **My table has headers** is ticked.

A Table gives you:

* Filter buttons on every heading.
* Banded (striped) rows.
* Formulas that copy down automatically when you add a new row.
* A **Total Row** (**Table Design → Total Row**) where you can pick Sum, Average, Count, Max and more for each column.

## Sorting

* **Quick sort:** click a cell in the column, then **Data → A→Z** or **Z→A**.
* **Multi-level sort:** **Data → Sort**, then **Add Level**. Example: sort by Status first, then by Qty largest to smallest.

Always sort the **whole table**, never one selected column alone, or the rows get mixed up.

## Filtering

1. Click the arrow on a heading.
2. Tick only the values you want to see, e.g. Status = Active.
3. Use **Number Filters** (Greater Than, Between…) or **Text Filters** (Contains, Begins With…) for more control.
4. **Data → Clear** removes all filters.

Filtering only **hides** rows. Nothing is deleted.

## Conditional Formatting

**Home → Conditional Formatting** changes a cell's look depending on its value.

| Rule used in the workbook | How |
|---|---|
| Status equal to "Inactive" → red | Highlight Cells Rules → Equal To |
| Qty less than 3 → highlighted | Highlight Cells Rules → Less Than |
| Data bars on Total Cost Price | Data Bars → pick a colour |

* **Manage Rules** shows, edits and deletes the rules on a sheet.
* **Clear Rules** removes them from the selected cells or the whole sheet.

## Selling Price with 10% Profit

```
=E2*0.1+E2      cost price + 10% of cost price
```

## Common Mistakes

* Applying conditional formatting to the heading row by selecting the whole column.
* Forgetting that a filter is on, then thinking data is missing. Look for the filter icon on the heading.

## Practice

Take a list of 10 products, make it a Table, sort it by price, filter only Active items and highlight low stock.
