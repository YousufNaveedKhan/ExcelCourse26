# Lec05: COUNTIF, SUMIF and Data Validation

**Workbook:** [Lec05-COUNTIF-SUMIF-and-DataValidation.xlsx](./Lec05-COUNTIF-SUMIF-and-DataValidation.xlsx)

In this lecture we answer questions about a large sales sheet (1,500 orders): how many laptop orders, how much laptop sale, and so on. We also make a dropdown list.

## COUNTIF: count with a condition

```
=COUNTIF(range, criteria)
```

```
=COUNTIF(C2:C1501, "Laptop")      how many orders are for Laptop
=COUNTIF(D2:D1501, ">10")         how many orders have Qty more than 10
=COUNTIF(C2:C1501, A20)           criteria taken from cell A20
```

## SUMIF: add with a condition

```
=SUMIF(range, criteria, sum_range)
```

* **range:** where Excel checks the condition
* **criteria:** what it looks for
* **sum_range:** what it adds up

```
=SUMIF(C2:C1501, "Laptop", J2:J1501)   total sale of Laptop
=SUMIF(C2:C1501, "Laptop", D2:D1501)   total quantity of Laptop
```

`range` and `sum_range` must be the **same size** (both rows 2 to 1501).

## Data Validation (Dropdown List)

Data Validation controls what can be typed in a cell.

1. Select the cell.
2. **Data → Data Validation**.
3. **Allow:** List.
4. **Source:** select the list, e.g. `$N$2:$N$1501` (all Order IDs), or type values separated by commas: `North,South,East,West`.
5. Click OK. The cell now shows a dropdown arrow.

The **Input Message** and **Error Alert** tabs let you show a hint and block wrong entries.

## Pictures in Cells

**Insert → Pictures → Place in Cell** puts a picture *inside* a cell, so it moves and sorts with the row. **Place over Cells** floats the picture on top of the sheet. Place in Cell needs Microsoft 365.

## Common Mistakes

* Forgetting the quotes around text or operators: `">10"`, not `>10`.
* `range` and `sum_range` of different sizes, which gives wrong totals.
* Spelling the criteria differently from the data ("Laptops" vs "Laptop").

## Practice

Find the number of orders and total sale for every product, and for every region.
