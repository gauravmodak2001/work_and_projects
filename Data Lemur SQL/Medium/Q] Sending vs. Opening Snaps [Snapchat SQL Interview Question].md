## Q] Sending vs. Opening Snaps [Snapchat SQL Interview Question]

![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/0d999291-e64f-415e-a985-b114bc76badd)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/45625216-2ede-4478-8250-f86f42396bc1)


**Answer:**
```sql

SELECT age_bucket , ROUND((100.0 * (SUM(time_spent) FILTER(WHERE activity_type='send'))/((SUM(time_spent) FILTER(WHERE activity_type='send'))+(SUM(time_spent) FILTER(WHERE activity_type='open')))),2) AS send_per,
      ROUND((100.0*(SUM(time_spent) FILTER(WHERE activity_type='open'))/((SUM(time_spent) FILTER(WHERE activity_type='send'))+(SUM(time_spent) FILTER(WHERE activity_type='open')))),2) AS open_per FROM
(SELECT * FROM activities ac
LEFT JOIN age_breakdown ab
ON ac.user_id = ab.user_id
WHERE ac.activity_type <> 'chat') AS table_1
GROUP By age_bucket;

```
## Please click on the following link to try it out:
https://datalemur.com/questions/time-spent-snaps
