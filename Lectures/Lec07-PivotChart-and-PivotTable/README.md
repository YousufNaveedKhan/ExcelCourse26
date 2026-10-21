# Lec07: PivotTable and PivotChart

**Workbook:** [Lec07-PivotChart-and-PivotTable.xlsx](./Lec07-PivotChart-and-PivotTable.xlsx)

In this lecture we summarise 1,500 sales orders in seconds: salesperson-wise and product-wise sales, with charts.

## What Is a PivotTable?

A PivotTable groups and totals a large dataset **without writing formulas**. You drag fields and Excel does the calculation.

## Making a PivotTable

1. Click inside the data (in the workbook it is a Table on the `Raw_Data` sheet).
2. **Insert → PivotTable → New Worksheet → OK**.
3. Drag fields into the four areas:

| Area | What it does | Workbook example |
|---|---|---|
| **Rows** | One row for each item | Salesperson |
| **Columns** | One column for each item | (optional) Region |
| **Values** | The number to calculate | Sum of TotalPrice |
| **Filters** | A dropdown on top to filter the whole PivotTable | PaymentMethod |

The workbook has two PivotTables:

* `Salesman_perfomance`: Salesperson-wise sale, filtered by PaymentMethod
* `Productwise_sale`: Product-wise sale

## Value Field Settings

Click the field in **Values → Value Field Settings** to change **Sum** to **Count**, **Average**, **Max** or **Min**. Use **Number Format** there to add commas.

## PivotChart

Click inside the PivotTable, then **PivotTable Analyze → PivotChart** and choose a chart (the workbook uses a Column chart). The chart changes when you filter the PivotTable.

## Refresh

A PivotTable does **not** update by itself. After changing the raw data, right-click the PivotTable and choose **Refresh** (or **Data → Refresh All**).

Because the source is a Table, new rows added to it are included on refresh.

## Common Mistakes

* Blank headings or blank rows in the source data.
* Forgetting to Refresh after changing data.
* A number column showing **Count** instead of **Sum** because it has blank or text cells.

## Practice

Make a PivotTable showing Region-wise sale, with Product as a filter, and a PivotChart for it.
