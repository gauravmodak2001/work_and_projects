## Q] Pharmacy Analytics (Part 2) [CVS Health SQL Interview Question]

![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/e7458dae-0789-4a61-aadf-47ef8eab88a1)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/cc8803c5-970f-43d4-bcea-ac5f0a55bf38)


**Answer:**
```sql

SELECT manufacturer , count(drug) as drug_count ,(sum(cogs)-sum(total_sales))  as total_loss  FROM pharmacy_sales
WHERE total_sales<cogs
GROUP BY manufacturer
ORDER BY total_loss DESC;

```
## Please click on the following link to try it out:
https://datalemur.com/questions/non-profitable-drugs
