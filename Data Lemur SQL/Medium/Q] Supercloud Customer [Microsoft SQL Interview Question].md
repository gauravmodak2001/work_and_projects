## Q] Supercloud Customer [Microsoft SQL Interview Question]

![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/3ec38ba2-4b5c-43fb-8ec4-e31da53d5c84)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/e69a9333-d6b0-4873-8ef6-06f7ef4a595b)


**Answer:**
```sql

SELECT customer_id FROM 
(SELECT DISTINCT con_fun , customer_id FROM 
(SELECT *,CONCAT(customer_id,product_category) AS con_fun FROM customer_contracts a
LEFT JOIN products b
ON a.product_id = b.product_id) AS table_1
)table_2
GROUP BY customer_id
HAVING count(customer_id)>=3;


```
## Please click on the following link to try it out:
[https://datalemur.com/questions/signup-confirmation-rate](https://datalemur.com/questions/supercloud-customer)https://datalemur.com/questions/supercloud-customer
