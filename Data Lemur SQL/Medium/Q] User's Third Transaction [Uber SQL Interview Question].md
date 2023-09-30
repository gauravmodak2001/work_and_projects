## Q] App Click-through Rate (CTR) [Facebook SQL Interview Question]

![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/80e5fcf9-80a1-4673-ba5f-d0be3b2cefa9)

**Answer:**
```sql

SELECT app_id ,
    ROUND(
      100.00*
      count(*) FILTER(WHERE event_type='click')/
      count(*) FILTER(WHERE event_type='impression'),2) AS ctr_app
FROM (SELECT * FROM events
WHERE timestamp>'01/01/2022' AND timestamp<'12/31/2022') AS table_1
GROUP BY app_id;

```
## Please click on the following link to try it out:
https://datalemur.com/questions/click-through-rate
