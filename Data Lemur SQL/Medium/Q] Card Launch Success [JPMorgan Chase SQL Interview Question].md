## Q] Card Launch Success [JPMorgan Chase SQL Interview Question]

![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/88f6b28e-9346-4a6b-bdb1-0fd6d659992a)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/f34fb6cf-acaf-47c9-a153-90a62ebfaa55)


**Answer:**
```sql

SELECT card_name,issued_amount FROM (
SELECT *,ROW_NUMBER() OVER(PARTITION BY card_name ORDER BY issue_year,issue_month) FROM monthly_cards_issued
) AS table_1
WHERE row_number=1
order by issued_amount DESC;


```
## Please click on the following link to try it out:
https://datalemur.com/questions/card-launch-success
