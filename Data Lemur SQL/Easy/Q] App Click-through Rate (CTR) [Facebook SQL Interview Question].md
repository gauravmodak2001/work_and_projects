## Q] App Click-through Rate (CTR) [Facebook SQL Interview Question]

![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/c78fdea2-f6d5-4aa8-a391-582c7cdcd2e6)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/e5b5f7fd-4dae-452c-bd60-7ba67f3e69cf)


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
