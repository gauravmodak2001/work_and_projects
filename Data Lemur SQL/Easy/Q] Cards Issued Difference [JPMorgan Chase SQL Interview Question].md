## Q] Cards Issued Difference [JPMorgan Chase SQL Interview Question]
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/fb4844c6-4801-41c1-8b10-bafa3f7a85f6)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/efc68537-a43e-4f28-8781-d4908afa014d)


**Answer:**
```sql
SELECT card_name, MAX(issued_amount)-MIN(issued_amount) as difference FROM monthly_cards_issued
GROUP BY card_name
ORDER BY difference DESC;

```
## Please click on the following link to try it out:
https://datalemur.com/questions/cards-issued-difference
