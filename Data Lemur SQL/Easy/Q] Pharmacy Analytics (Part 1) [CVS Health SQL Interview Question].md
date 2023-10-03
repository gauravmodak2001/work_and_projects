## Q] Pharmacy Analytics (Part 1) [CVS Health SQL Interview Question]
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/f4a901c0-8eac-4376-88ff-39a588fa0290)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/114f6fe2-e2af-46d1-9a2f-a99f5febc337)


**Answer:**
```sql
SELECT drug, (total_sales-cogs) as total_profit 
FROM pharmacy_sales
order by total_profit DESC
LIMIT 3;

```
## Please click on the following link to try it out:
https://datalemur.com/questions/top-profitable-drugs
