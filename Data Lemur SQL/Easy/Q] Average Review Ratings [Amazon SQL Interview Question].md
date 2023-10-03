## Q] Average Review Ratings [Amazon SQL Interview Question]
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/10e6fd1b-39b2-45a5-8aec-3f460a129457)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/f4e451cc-e3c4-42b1-a3a4-30d7922d5927)



**Answer:**
```sql
SELECT  EXTRACT(MONTH FROM submit_date) as mth,product_id as product , 
        ROUND(AVG(stars),2) AS avg_stars FROM reviews
GROUP BY EXTRACT(MONTH FROM submit_date) , product_id
ORDER BY mth , product;

```
## Please click on the following link to try it out:
https://datalemur.com/questions/sql-avg-review-ratings
