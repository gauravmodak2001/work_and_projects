## Q] Teams Power Users [Microsoft SQL Interview Question]

![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/49c8f03d-7738-4473-a79c-e6612b3a5364)


**Answer:**
```sql
SELECT sender_id , count(*) AS message_count FROM 
(SELECT * FROM messages
WHERE EXTRACT(MONTH FROM sent_date) = 8
      AND 
      EXTRACT(YEAR FROM sent_date)= 2022) AS table_1
GROUP BY sender_id
ORDER BY message_count DESC
LIMIT 2 ;

```
## Please click on the following link to try it out:
https://datalemur.com/questions/teams-power-users
