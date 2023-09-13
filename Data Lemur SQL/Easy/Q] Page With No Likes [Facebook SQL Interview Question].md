## Q] Page With No Likes [Facebook SQL Interview Question]
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/fae80042-3e3f-44bc-9f41-6d5934873e5e)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/cad42c8d-9566-4fb7-bc50-1d4d559af7ec)


**Answer:**
```sql
SELECT page_id FROM pages
WHERE page_id NOT IN (
(SELECT page_id FROM page_likes));
```
## Please click on the following link to try it out:
https://datalemur.com/questions/sql-page-with-no-likes
