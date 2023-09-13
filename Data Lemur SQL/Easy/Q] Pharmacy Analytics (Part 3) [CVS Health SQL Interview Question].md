## Q] Pharmacy Analytics (Part 3) [CVS Health SQL Interview Question]
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/a03c961e-ef4c-4f78-aa8b-d0cb135fcd9a)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/dc5014e6-cb55-4478-bbca-5fe48bcf71e6)


**Answer:**
```sql
SELECT manufacturer , CONCAT('$' , (ROUND(SUM(total_sales)/1000000)),' ','million') as sale FROM pharmacy_sales
GROUP BY manufacturer
ORDER BY SUM(total_sales) DESC ,manufacturer ASC ;
```
## Please click on the following link to try it out:
https://datalemur.com/questions/total-drugs-sales
