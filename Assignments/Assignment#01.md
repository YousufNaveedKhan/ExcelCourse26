# Lec03 Assignment: IF and Nested IF

**Given:** Wednesday, 14 October 2026
**Submission:** Next class, Friday, 16 October 2026

Make a new workbook named `Lec03-Assignment-YourName.xlsx` with two sheets.

## Task 1: Electricity Bill (Sheet name: `Bill`)

Enter this data:

| Customer | Previous Reading | Current Reading |
|---|---|---|
| Ali | 1200 | 1285 |
| Sara | 3400 | 3560 |
| Bilal | 560 | 830 |
| Hina | 2100 | 2195 |
| Usman | 4500 | 4870 |
| Ayesha | 900 | 1150 |

Add these columns and fill them with formulas:

1. **Units** = Current Reading − Previous Reading
2. **Rate** (use nested `IF`):

   | Units | Rate (Rs per unit) |
   |---|---|
   | up to 100 | 10 |
   | 101 to 200 | 15 |
   | 201 to 300 | 20 |
   | above 300 | 25 |

3. **Bill** = Units × Rate
4. **Status** (use `IF`): "High Usage" if Bill is more than 5,000, otherwise "Normal"

## Task 2: Attendance (Sheet name: `Attendance`)

| Name | Total Classes | Attended |
|---|---|---|
| Hamza | 20 | 18 |
| Fatima | 20 | 13 |
| Zain | 20 | 15 |
| Maryam | 20 | 9 |

Add:

1. **Attendance %** = Attended ÷ Total Classes (format as %)
2. **Remarks** (use `IF`): "Allowed" if 75% or more, otherwise "Short Attendance"

## Rules

* Every calculated cell must have a **formula**. No typing answers by hand.
* Format both sheets: a title row, borders, bold headings, proper column widths.
* Write each formula once, then copy it down the column.
