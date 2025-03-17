# SQL-Interview

Question: As per below table what will be year by year grouth in Percengeta?

![image](https://github.com/user-attachments/assets/5232184b-cade-44ad-8d6c-011ffb8185bd)

Answer: 
SELECT 
    Year,
    Amount,
    LAG(Amount) OVER (ORDER BY Year) AS Previous_Year_Amount,
    CASE 
        WHEN LAG(Amount) OVER (ORDER BY Year) IS NULL THEN NULL 
        ELSE (Amount - LAG(Amount) OVER (ORDER BY Year)) / LAG(Amount) OVER (ORDER BY Year) * 100 
    END AS Growth_Percentage
FROM 
    your_table_name
ORDER BY 
    Year;

## Yearly Growth Calculation in SQL

To calculate the year-by-year growth percentage, use the following SQL query:

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
    your_table_name
ORDER BY 
    Year;

