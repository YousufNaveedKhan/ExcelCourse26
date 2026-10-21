# Lec03: IF and Nested IF

**Workbook:** [Lec03-IF-and-Nested-IF.xlsx](./Lec03-IF-and-Nested-IF.xlsx)

In this lecture Excel starts making **decisions**: PASS or FAIL, and the grade of each student.

## Comparison Operators

| Operator | Meaning |
|---|---|
| `=` | equal to |
| `<>` | not equal to |
| `>` | more than |
| `<` | less than |
| `>=` | equal to **or** more than |
| `<=` | equal to **or** less than |

## The IF Function

```
=IF(condition, value_if_true, value_if_false)
```

Example: the result is PASS if the percentage is 40% or more.

```
=IF(H2>=40%, "PASS", "FAIL")
```

* Text answers go inside **double quotes**: `"PASS"`.
* Numbers and formulas do not need quotes.

## Nested IF

When there are **more than two** possible answers, put another `IF` in the *false* part.

| Percentage | Grade |
|---|---|
| 80% or more | A+ |
| 70% or more | A |
| 60% or more | B |
| 50% or more | C |
| 40% or more | D |
| below 40% | F |

```
=IF(H2>=80%, "A+", IF(H2>=70%, "A", IF(H2>=60%, "B", IF(H2>=50%, "C", IF(H2>=40%, "D", "F")))))
```

Excel checks the conditions **from left to right** and stops at the first one that is true.

## Common Mistakes

* Checking the **smallest** value first (`H2>=40%` first). Then everyone above 40% gets "D". Always start from the highest.
* Forgetting to close all the brackets. Count them: 5 `IF`s need 5 `)` at the end.
* Using `>` where the rule says "or more" (`>=`).

## Think About It

Abdul Rehman got 0 in Sub 2 but his result is PASS because only the percentage is checked. Is that fair? We will fix this in a later lecture.

## Practice

See [Assignment #01](../../Assignments/Assignment%2301.md).
