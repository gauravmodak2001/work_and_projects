## Q] Odd and Even Measurements [Google SQL Interview Question]

=
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/e9ff9e52-3281-45bb-95e6-c114d21dd297)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/b44ba3ad-43eb-4584-bf2f-b01964103427)



**Answer:**
```sql

WITH table_1 AS (SELECT *,ROW_NUMBER() OVER(PARTITION BY EXTRACT(DAY FROM measurement_time) 
                  ORDER BY measurement_time) AS rn,
      CAST(measurement_time AS DATE) AS Date
FROM measurements)
,
table_2 AS (
SELECT date as measurement_day,SUM(measurement_value) AS odd_sum FROM table_1
WHERE (rn%2)!=0
GROUP BY date)
,
table_3 AS (
SELECT date as measurement_day,SUM(measurement_value) AS even_sum FROM table_1
WHERE (rn%2)=0
GROUP BY date)

SELECT t2.measurement_day , odd_sum , even_sum   FROM table_2 t2
JOIN table_3 t3
ON t2.measurement_day = t3.measurement_day
ORDER BY t2.measurement_day;



```
## Please click on the following link to try it out:
https://datalemur.com/questions/odd-even-measurements
