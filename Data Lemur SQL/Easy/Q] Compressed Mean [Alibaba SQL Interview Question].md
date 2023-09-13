## Q] Compressed Mean [Alibaba SQL Interview Question]
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/4baf6c5c-3343-4506-9349-740a37fb0657)


**Answer:**
```sql

SELECT ROUND((SUM(mean_1)::decimal) /SUM(order_occurrences),1) as mean 
FROM
(SELECT order_occurrences ,(item_count*order_occurrences) as mean_1 
FROM items_per_order) 
as table_1;



```
## Please click on the following link to try it out:
https://datalemur.com/questions/alibaba-compressed-mean
