# SQL-Interview

## Yearly Growth Calculation in SQL

![image](https://github.com/user-attachments/assets/5232184b-cade-44ad-8d6c-011ffb8185bd)

To calculate the year-by-year growth percentage:

```sql
SELECT 
    Year,
    Amount,
    LAG(Amount) OVER (ORDER BY Year) AS Previous_Year_Amount,
    CASE 
        WHEN LAG(Amount) OVER (ORDER BY Year) IS NULL THEN NULL 
        ELSE (Amount - LAG(Amount) OVER (ORDER BY Year)) / LAG(Amount) OVER (ORDER BY Year) * 100 
    END AS Growth_Percentage
FROM 
    dataset
ORDER BY 
    Year;
```

# Functions and Syntax for Looking Up Values Across Different Tables and Sheets

## 1. VLOOKUP Syntax:

```excel
=VLOOKUP(lookup_value, table_array, col_index_num, [range_lookup])
```
## 2. INDEX + MATCH Syntax:
```excel
=INDEX(return_range, MATCH(lookup_value, lookup_range, 0))
```
## 3. XLOOKUP Syntax (for newer Excel versions):
```excel
=XLOOKUP(lookup_value, lookup_array, return_array, [if_not_found], [match_mode], [search_mode])
```

## 4. IF Syntax:

```excel
=IF(logical_test, value_if_true, value_if_false)

```
## 5. IFS Syntax (for multiple conditions):
```excel
=IFS(condition1, value1, condition2, value2, ..., condition_n, value_n)
