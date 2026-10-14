# Lec03 Assignment: IF and Nested IF

**Given:** Wednesday, 14 October 2026
**Submission:** Next class, Friday, 16 October 2026

Make **one workbook** named `Lec03-Assignment-YourName.xlsx` with **four sheets**, one for each task below. Rename every sheet as shown in its heading.

### Quick reminder

* `IF` checks one condition and gives one of two answers:
  `=IF(condition, value_if_true, value_if_false)`
* **Nested `IF`** means putting another `IF` in the *false* part, so you can check more than two cases, one after another.
* `>` means "more than". `>=` means "equal to **or** more than". Read every condition carefully: they are not the same.

---

## Task 1: Electricity Bill (Sheet: `Bill`)

The electricity company charges a different **rate per unit** depending on how many units a customer used. Make a bill for each customer.

**Step 1: Enter this data**

| Customer | Previous Reading | Current Reading |
|---|---|---|
| Ali | 1200 | 1285 |
| Sara | 3400 | 3560 |
| Bilal | 560 | 830 |
| Hina | 2100 | 2200 |
| Usman | 4500 | 4920 |
| Ayesha | 900 | 1150 |

**Step 2: Add these columns and fill them with formulas**

1. **Units:** units used this month = Current Reading − Previous Reading
2. **Rate:** use a **nested `IF`** on Units:

   | Units used | Rate (Rs per unit) |
   |---|---|
   | 100 or less | 10 |
   | 101 to 200 | 15 |
   | 201 to 300 | 20 |
   | more than 300 | 25 |

3. **Bill** = Units × Rate
4. **Status:** use `IF`. Show "High Usage" if the Bill is **more than 10,000**, otherwise "Normal".

**Check your work:** Ali used 85 units, so his rate is 10, his bill is Rs 850 and his status is "Normal".

---

## Task 2: Salary Sheet (Sheet: `Salary`)

A company pays every employee a basic salary plus an allowance. It deducts tax from higher salaries and gives a bonus based on the employee's performance rating.

**Step 1: Enter this data**

| Employee | Basic Salary | Allowance | Rating |
|---|---|---|---|
| Kamran | 45000 | 5000 | B |
| Nida | 30000 | 4000 | A |
| Faisal | 60000 | 8000 | C |
| Asad | 25000 | 3000 | B |
| Sana | 70000 | 10000 | A |

**Step 2: Add these columns and fill them with formulas**

1. **Gross Salary** = Basic Salary + Allowance
2. **Tax:** use `IF`. If Gross Salary is **50,000 or more**, tax is **10% of Gross Salary**, otherwise tax is **0**.
3. **Bonus:** use a **nested `IF`** on Rating:

   | Rating | Bonus |
   |---|---|
   | A | 20% of Basic Salary |
   | B | 10% of Basic Salary |
   | C | 0 |

   Text in a condition goes inside double quotes, for example `D2="A"`.
4. **Net Salary** = Gross Salary + Bonus − Tax

**Check your work:** Nida's gross salary is Rs 34,000, so she pays no tax. Her rating is A, so her bonus is Rs 6,000 and her net salary is Rs 40,000.

Keep this sheet safe. We will use it again in later lectures.

---

## Task 3: Shop Billing System (Sheet: `Billing`)

A shop gives a bigger discount on bigger bills, and free delivery when the final bill is large enough.

**Step 1: Enter this data**

| Item | Qty | Price |
|---|---|---|
| Shoes | 2 | 3500 |
| Shirt | 3 | 800 |
| Watch | 1 | 12000 |
| Socks | 5 | 150 |
| Bag | 2 | 2500 |

**Step 2: Add these columns and fill them with formulas**

1. **Amount** = Qty × Price
2. **Discount %:** use a **nested `IF`** on Amount:

   | Amount | Discount |
   |---|---|
   | 10,000 or more | 15% |
   | 5,000 or more | 10% |
   | 2,000 or more | 5% |
   | less than 2,000 | 0% |

   Format this column as %.
3. **Discount** = Amount × Discount %
4. **Net Amount** = Amount − Discount
5. **Delivery:** use `IF`. Show "Free Delivery" if Net Amount is **3,000 or more**, otherwise "Delivery Charges".

**Check your work:** Shoes: amount Rs 7,000, discount 10% (Rs 700), net amount Rs 6,300, "Free Delivery".

---

## Task 4: Attendance (Sheet: `Attendance`) — Bonus Task

A student needs at least **75% attendance** to sit the exam.

**Step 1: Enter this data**

| Name | Total Classes | Attended |
|---|---|---|
| Hamza | 20 | 18 |
| Fatima | 20 | 13 |
| Zain | 20 | 15 |
| Maryam | 20 | 9 |

**Step 2: Add these columns and fill them with formulas**

1. **Attendance %** = Attended ÷ Total Classes. Format this column as %.
2. **Remarks:** use `IF`. Show "Allowed" if Attendance % is **75% or more**, otherwise "Short Attendance".

**Check your work:** Hamza attended 18 of 20 classes, so his attendance is 90% and he is "Allowed".

---

## Rules

* Every calculated cell must have a **formula**. Do not type answers by hand.
* Write each formula **once** in the first row, then copy it down the column.
* Format every sheet with a title row, bold headings, borders and proper column widths (what we did in Lec01).
* Format money columns as numbers and percentage columns as %.
* Before submitting, look out for rows that sit exactly on a limit (for example exactly 100 units or exactly 50,000 salary) and check they got the right answer.
