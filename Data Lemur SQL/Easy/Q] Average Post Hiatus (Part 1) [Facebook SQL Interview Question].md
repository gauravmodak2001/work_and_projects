
## Q] Average Post Hiatus (Part 1) [Facebook SQL Interview Question]
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/c89a655e-c8f4-40c0-b949-ba8d9f02d6fc)


**Answer:**
```sql
SELECT 
	user_id, 
    MAX(post_date::DATE) - MIN(post_date::DATE) AS days_between
FROM posts
WHERE DATE_PART('year', post_date::DATE) = 2021 
GROUP BY user_id
HAVING COUNT(post_id)>1;
```
## Please click on the following link to try it out:
https://datalemur.com/questions/sql-average-post-hiatus-1
