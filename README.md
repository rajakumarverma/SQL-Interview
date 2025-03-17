# SQL-Interview

Question: As per below table what will be year by year grouth in Percengeta?

Data Set	
Yesr	Amount
2019	10000
2020	15000
2021	25000
2022	26000
2025	30000

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
