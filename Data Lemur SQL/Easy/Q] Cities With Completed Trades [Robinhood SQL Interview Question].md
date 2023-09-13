## Q] Cities With Completed Trades [Robinhood SQL Interview Question]

![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/e52847c3-7b7f-40ed-8efb-edae56ec77e9)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/b7353a63-1087-4018-b467-0f7c92251224)


**Answer:**
```sql
SELECT city, count(*) AS total_orders FROM 
(SELECT * FROM trades x
JOIN users y
ON x.user_id = y.user_id) AS table_2
WHERE status='Completed'
GROUP BY city
ORDER BY total_orders DESC
LIMIT 3;

```
## Please click on the following link to try it out:
https://datalemur.com/questions/completed-trades
