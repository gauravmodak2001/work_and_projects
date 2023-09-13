## Q] Histogram of Tweets [Twitter SQL Interview Question]

- ![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/d846c064-9ebd-403d-8871-56c3f52154fa)


**Answer:**
```sql
  SELECT  DISTINCT(tweet_bucket) , count(users_num)
  FROM (SELECT count(user_id) as tweet_bucket  , count(tweet_id) as users_num
  FROM tweets
  WHERE EXTRACT(YEAR FROM tweet_date)=2022
  GROUP BY user_id) AS tweet_1
  GROUP BY tweet_bucket;
```
## Please click on the following link to try it out:
https://datalemur.com/questions/sql-histogram-tweets
