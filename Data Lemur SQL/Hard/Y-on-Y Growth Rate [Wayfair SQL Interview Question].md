## Q] Y-on-Y Growth Rate [Wayfair SQL Interview Question]


![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/faa3c765-cded-45c8-8cbb-2eb9458c70e5)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/99262578-160c-487d-8edd-6c84d41ba826)


**Answer:**
```sql

WITH table_2 AS (SELECT year , product_id,spend ,
      spend as curr_year_spend,
      LAG(spend) OVER (
      PARTITION BY product_id 
      ORDER BY 
        product_id, 
      EXTRACT(YEAR FROM transaction_date)) AS prev_year_spend 
FROM
(SELECT CAST(EXTRACT(YEAR FROM transaction_date)as INT) as year , product_id, spend , transaction_date 
FROM user_transactions)as table_1)
  
SELECT year ,
      product_id,
      curr_year_spend,
      prev_year_spend, 
      ROUND(100 * 
        (curr_year_spend - prev_year_spend)
        / prev_year_spend
      , 2) AS yoy_rate 
FROM table_2;


```
## Please click on the following link to try it out:
https://datalemur.com/questions/yoy-growth-rate
