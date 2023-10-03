## Q] Duplicate Job Listings [Linkedin SQL Interview Question]
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/c47423d1-67cb-434c-992f-9d05bd49c1f7)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/5d3c20c5-9d54-4b43-bed3-9fcda94e78d1)


**Answer:**
```sql
-- Approach 1
SELECT count(*) FROM
(SELECT count(*) AS count_1 FROM
(SELECT *,concat(company_id,title) AS title_id FROM job_listings) AS table_1
GROUP BY title_id) AS table_2
WHERE count_1::INT >=2;


-- Approach 2
SELECT count(*) FROM (
SELECT count(*) FROM job_listings
GROUP BY title,company_id
HAVING count(1)>1
) a
GROUP BY count;


-- This approach will give you the dupliacte rows present in the table by doing group by on two columns.
WITH table_1 AS (
SELECT  company_id , title FROM job_listings
GROUP BY title,company_id
HAVING count(1)>1)

SELECT * FROM table_1 t1
INNER JOIN job_listings jl
ON t1.company_id=jl.company_id and t1.title = jl.title


```
## Please click on the following link to try it out:
https://datalemur.com/questions/duplicate-job-listings
