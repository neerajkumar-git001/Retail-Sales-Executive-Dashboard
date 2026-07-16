# Calendar Measures

This document contains the DAX calculated table and calculated columns used to create the Calendar table. The table serves as the primary date dimension for enabling time intelligence calculations, filtering, and trend analysis across the report.

---

## 1. Calendar Table

```DAX
Calender Table =
CALENDAR(
    DATE(2019, 1, 1),
    DATE(2024, 12, 31)
)
```

**Description:** Creates a continuous calendar table from **January 1, 2019** to **December 31, 2024**. This table acts as the date dimension for all time-based analysis.

---

## 2. Year

```DAX
Year =
YEAR('Calender Table'[Date].[Date])
```

**Description:** Extracts the year from each date for yearly analysis and filtering.

---

## 3. Year Month

```DAX
Year Month =
FORMAT('Calender Table'[Date], "MMM YYYY")
```

**Description:** Combines the month and year into a single field (e.g., **Jan 2024**) for chronological reporting.

---


## 4. Quarter

```DAX
Quarter =
"Q" & FORMAT('Calender Table'[Date], "Q")
```

**Description:** Returns the quarter of the year (Q1, Q2, Q3, or Q4) for quarterly analysis and reporting.

---

## 5. Month

```DAX
Month =
MONTH('Calender Table'[Date])
```

**Description:** Returns the numeric month (1–12) from each date.

---

## 6. Month Name

```DAX
Month Name =
FORMAT('Calender Table'[Date], "MMM")
```

**Description:** Returns the abbreviated month name (e.g., **Jan**, **Feb**, **Mar**) for report visuals.

---



## 7. Day Name

```DAX
Day Name =
FORMAT('Calender Table'[Date], "ddd")
```

**Description:** Returns the abbreviated day name (e.g., **Mon**, **Tue**, **Wed**) for weekday-based analysis and reporting.
