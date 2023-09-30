## Q] Signup Activation Rate [TikTok SQL Interview Question]


![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/6715fa25-0050-4300-8efa-389ba06c5197)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/c1c81599-e1e0-42b3-a600-a7e83f7fd411)


**Answer:**
```sql

SELECT CAST((CAST(COUNT(signup_action) FILTER(WHERE signup_action='Confirmed')AS DECIMAL(5,2)))/(CAST(COUNT(signup_action) AS DECIMAL(5,2))) AS DECIMAL(5,2))
AS confirm_rate
FROM emails e
JOIN texts t
ON e.email_id = t.email_id;

```
## Please click on the following link to try it out:
https://datalemur.com/questions/signup-confirmation-rate
