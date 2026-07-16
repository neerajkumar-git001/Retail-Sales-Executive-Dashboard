# Previous Year Measures

This document contains DAX measures used to calculate previous year (PY) values for key business metrics using the `SAMEPERIODLASTYEAR()` function.

---

## 1. Sales PY

```DAX
Sales PY =
CALCULATE(
    [Total Sales],
    SAMEPERIODLASTYEAR('Calendar Table'[Date])
)
```

**Description:** Returns the total sales for the same period in the previous year, enabling year-over-year sales comparisons.

---

## 2. Profit PY

```DAX
Profit PY =
CALCULATE(
    [Total Profit],
    SAMEPERIODLASTYEAR('Calendar Table'[Date])
)
```

**Description:** Returns the total profit for the same period in the previous year for YoY profit analysis.

---

## 3. Profit Margin PY

```DAX
Profit Margin PY =
CALCULATE(
    [Profit Margin],
    SAMEPERIODLASTYEAR('Calendar Table'[Date])
)
```

**Description:** Returns the profit margin for the same period in the previous year to compare profitability trends.

---

## 4. Quantity PY

```DAX
Quantity PY =
CALCULATE(
    [Total Quantity],
    SAMEPERIODLASTYEAR('Calendar Table'[Date])
)
```

**Description:** Returns the total quantity sold during the same period in the previous year.

---

## 5. Orders PY

```DAX
Orders PY =
CALCULATE(
    [Total Orders],
    SAMEPERIODLASTYEAR('Calendar Table'[Date])
)
```

**Description:** Returns the total number of unique customer orders for the same period in the previous year.

---

## 6. AOV PY

```DAX
AOV PY =
CALCULATE(
    [Average Order Value],
    SAMEPERIODLASTYEAR('Calendar Table'[Date])
)
```

**Description:** Returns the Average Order Value (AOV) for the same period in the previous year to evaluate changes in customer spending patterns.





 percentage growth in Average Order Value (AOV).
