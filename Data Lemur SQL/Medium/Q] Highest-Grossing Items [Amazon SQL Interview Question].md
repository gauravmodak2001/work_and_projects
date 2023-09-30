## Q] Highest-Grossing Items [Amazon SQL Interview Question]

![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/a54086b6-4e82-48fc-8ae5-ce5c135aae42)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/a8946555-12ac-4356-a95b-c60f0ac2223a)


**Answer:**
```sql

SELECT category , product , tspend as total_spend FROM 
(SELECT category , product , tspend,
ROW_NUMBER() OVER(PARTITION BY category ORDER BY tspend DESC) as rn FROM 
(SELECT category ,product, SUM(spend) as tspend
FROM product_spend
where EXTRACT(YEAR FROM transaction_date)=2022
GROUP BY product,category) AS table_1
) AS table_2
WHERE rn<3;



```
## Please click on the following link to try it out:
https://datalemur.com/questions/sql-highest-grossing
