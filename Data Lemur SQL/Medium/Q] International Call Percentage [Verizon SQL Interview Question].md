## Q] International Call Percentage [Verizon SQL Interview Question]


![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/b4ebb4e5-b974-43b5-8edf-a9a6e576eba8)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/d4ba2d1f-e814-4738-ba8b-ef9a91e4ec46)


**Answer:**
```sql

SELECT 
    CAST((100.0*(count(caller_country) FILTER(WHERE caller_country<>receiver_country)*1.0) /
    (count(caller_country)*1.0)) AS DECIMAL(5, 1)) AS international_calls_pct
    FROM 
(SELECT  
  caller.country_id AS caller_country,
  receiver.country_id AS receiver_country
FROM phone_calls AS calls
LEFT JOIN phone_info AS caller
  ON calls.caller_id = caller.caller_id
LEFT JOIN phone_info AS receiver
  ON calls.receiver_id = receiver.caller_id) AS table_1
;




```
## Please click on the following link to try it out:
https://datalemur.com/questions/international-call-percentage
