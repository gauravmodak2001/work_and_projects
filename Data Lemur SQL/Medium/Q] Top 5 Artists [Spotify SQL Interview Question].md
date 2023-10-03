## Q] Top 5 Artists [Spotify SQL Interview Question]

![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/1da56cf3-69b7-4a8f-b8a7-c495ba2d2d6b)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/7a0441a5-5190-40b1-91cc-780fc42a28f7)
![image](https://github.com/gauravmodak2001/work_and_projects/assets/83473763/30b910df-6dfe-4f95-bba4-bfad7ffb22a1)



**Answer:**
```sql


SELECT * FROM (
SELECT artist_name,
  DENSE_RANK() over (order by count(artist_name) DESC) AS artist_rank
FROM
(SELECT * FROM 
(SELECT * FROM global_song_rank gsr
JOIN songs s 
ON gsr.song_id = s.song_id) AS table_1
JOIN artists ar
ON table_1.artist_id=ar.artist_id) AS table_2
WHERE table_2.rank<=10
GROUP BY artist_name
ORDER BY count(artist_name) DESC) AS table_3
WHERE artist_rank<=5;



```
## Please click on the following link to try it out:
https://datalemur.com/questions/top-fans-rank
