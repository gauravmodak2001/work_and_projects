## Q] Second Day Confirmation [TikTok SQL Interview Question]
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/33d90a41-7ba5-40c7-b15a-4394f5053592)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/5211f1c1-0612-4bd7-85f9-4b9cb6fa7d93)


**Answer:**
```sql
SELECT user_id FROM 
(SELECT * FROM emails e
JOIN texts t 
ON e.email_id=t.email_id
WHERE t.signup_action='Confirmed') AS table_1
WHERE DATE(table_1.signup_date) + 1 = table_1.action_date;

```
## Please click on the following link to try it out:
https://datalemur.com/questions/second-day-confirmation
