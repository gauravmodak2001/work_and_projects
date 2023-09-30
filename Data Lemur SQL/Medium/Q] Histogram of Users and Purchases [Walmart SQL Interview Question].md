## Q] Histogram of Users and Purchases [Walmart SQL Interview Question]


![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/1f35b576-a5a6-49af-8971-6bebc8938201)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/e0ffd7af-34c3-4e2d-b495-40d649a6ff85)



**Answer:**
```sql


SELECT transaction_date , user_id , purchase_count FROM (
SELECT transaction_date,user_id , count(user_id) AS purchase_count, 
      ROW_NUMBER() OVER(PARTITION BY user_id ORDER BY transaction_date DESC) AS rn
      FROM user_transactions
GROUP BY user_id,transaction_date) AS table_1
WHERE rn=1
ORDER BY transaction_date;


```
## Please click on the following link to try it out:
https://datalemur.com/questions/histogram-users-purchases
