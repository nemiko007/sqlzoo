# Alienのキャスト

```sql
SELECT name FROM movie, casting, actor 
WHERE title='Alien' 
  AND movieid=movie.id 
  AND actorid=actor.id
```
