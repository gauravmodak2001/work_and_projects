## Q] Data Science Skills [LinkedIn SQL Interview Question]
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/30891426-6596-4656-ad97-a138e4cdc1e2)

**Answer:**
```sql
-- Approach 1
SELECT count(*) FILTER(WHERE candidate_id='Python' AND candidate_id='Tableau' AND candidate_id='PostgreSQL') FROM candidates
WHERE (SELECT candidate_id FROM candidates GROUP BY candidate_id) 
='Python'
AND 
(SELECT candidate_id FROM candidates GROUP BY candidate_id) 
='Tableau'
AND 
(SELECT candidate_id FROM candidates GROUP BY candidate_id) 
='PostgreSQL';

-- Approach 2
SELECT candidate_id FROM 
(SELECT candidate_id,count(candidate_id) AS count_1 FROM candidates
WHERE skill='Python' OR skill='Tableau' OR Skill='PostgreSQL'
GROUP BY candidate_id) AS table_1
WHERE table_1.count_1=3
ORDER BY candidate_id;


-- Approach 3
SELECT candidate_id
FROM candidates
WHERE skill IN ('Python', 'Tableau', 'PostgreSQL')
GROUP BY candidate_id
HAVING COUNT(skill) = 3
ORDER BY candidate_id;

```
## Please click on the following link to try it out:
https://datalemur.com/questions/matching-skills
