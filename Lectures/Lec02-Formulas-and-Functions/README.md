# Lec02: Formulas and Functions

**Workbook:** [Lec02-Formulas-and-Functions.xlsx](./Lec02-Formulas-and-Functions.xlsx)

In this lecture the marksheet starts calculating by itself: obtained marks and percentage.

## Formulas

* Every formula starts with `=`.
* Use **cell addresses**, not the numbers themselves. Then if a mark changes, the answer updates automatically.

| Operator | Meaning | Example |
|---|---|---|
| `+` | Add | `=D2+E2` |
| `-` | Subtract | `=I2-D2` |
| `*` | Multiply | `=D2*2` |
| `/` | Divide | `=I2/500` |
| `^` | Power | `=D2^2` |

## The SUM Function

A **function** is a ready-made formula. `SUM` adds numbers.

```
=SUM(D2:H2)      adds every cell from D2 to H2 (a range)
=SUM(D2,E2,F2)   adds only the cells you list
```

## Calculating Percentage

```
Percentage = Obtained ÷ Total Marks
=I2/500
```

The answer looks like `0.76`. Select the column and click **Home → % (Percent Style)** to show it as `76%`.

## Copying a Formula Down

1. Write the formula once in the first row.
2. Select the cell and drag the small square at its bottom-right corner (**Fill Handle**) down, or double-click it.

Excel changes the row number for each row automatically (`D2` becomes `D3`, `D4`…). These are called **relative references**.

## Common Mistakes

* Forgetting the `=` at the start, so Excel shows the text instead of the answer.
* Typing the answer by hand instead of a formula.
* Multiplying the percentage by 100 **and** applying % format, which shows 7600%.

## Practice

Add Obtained and Percentage columns to your Lec01 marksheet using formulas only.
