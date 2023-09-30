## Q] Active User Retention [Facebook SQL Interview Question]


![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/6b8970a5-2c6a-4e53-b199-8c1f7ceef0a1)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/70af0b21-d723-4746-9d52-8f7b9077d0fe)


**Answer:**
```sql

SELECT 7 as month ,count(DISTINCT user_id) FROM user_actions
WHERE EXTRACT(MONTH FROM event_date) < 7
AND user_id IN(
SELECT DISTINCT user_id FROM user_actions
WHERE EXTRACT(MONTH FROM event_date)=7)




```
## Please click on the following link to try it out:
https://datalemur.com/questions/user-retention
