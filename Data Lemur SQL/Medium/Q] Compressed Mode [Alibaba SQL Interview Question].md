## Q] Compressed Mode [Alibaba SQL Interview Question]


![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/88f6b28e-9346-4a6b-bdb1-0fd6d659992a)


**Answer:**
```sql

SELECT item_count FROM items_per_order
WHERE order_occurrences = (SELECT MAX(order_occurrences) FROM items_per_order)
 


```
## Please click on the following link to try it out:
https://datalemur.com/questions/alibaba-compressed-mode
