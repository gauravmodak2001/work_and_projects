## Q] Average Deal Size (Part 1) [Salesforce SQL Interview Question]
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/ea2a12c2-5711-4bbb-ae37-5f3264315d45)


**Answer:**
```sql
SELECT ROUND(AVG(num_seats * yearly_seat_cost),2) AS average_deal_size 
FROM contracts;
```
## Please click on the following link to try it out:
https://datalemur.com/questions/sql-average-deal-size
