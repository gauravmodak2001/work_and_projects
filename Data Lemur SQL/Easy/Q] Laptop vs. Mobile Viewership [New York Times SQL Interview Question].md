## Q] Laptop vs. Mobile Viewership [New York Times SQL Interview Question]
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/1f052510-9029-45b6-bcae-9025c7c67a69)



**Answer:**
```sql
-- Approach 1
SELECT count(*) FILTER(WHERE device_type='laptop') AS laptop_views,
      count(*) FILTER(WHERE NOT device_type='laptop') AS mobile_views FROM viewership;


-- Approach 2
SELECT count(*) FILTER(WHERE device_type='laptop') AS laptop_views,
      count(*) FILTER(WHERE device_type!='laptop') AS mobile_views FROM viewership;


-- Approach 3
SELECT count(*) FILTER(WHERE device_type='laptop') AS laptop_views,
      count(*) FILTER(WHERE device_type<>'laptop') AS mobile_views FROM viewership;


```
## Please click on the following link to try it out:
https://datalemur.com/questions/laptop-mobile-viewership
