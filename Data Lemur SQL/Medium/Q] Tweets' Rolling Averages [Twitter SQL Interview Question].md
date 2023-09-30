## Q] Tweets' Rolling Averages [Twitter SQL Interview Question]

![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/b73d52d9-988c-4f0f-b743-fc94e8aae165)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/19f676c9-ab9e-4d18-a96b-cb78f291df53)


**Answer:**
```sql

SELECT user_id , tweet_date , 
   ROUND(AVG(tweet_count)
         OVER(PARTITION BY user_id ORDER BY tweet_date ROWS BETWEEN 2 PRECEDING AND CURRENT ROW 
         ),2)
         AS rolling_avg_3d
FROM tweets 

```
## Please click on the following link to try it out:
https://datalemur.com/questions/rolling-average-tweets
