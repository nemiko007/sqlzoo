# Harrison Ford(脇役)

```sql
SELECT title FROM movie, casting, actor 
WHERE name='Harrison Ford' 
  AND movieid=movie.id 
  AND actorid=actor.id 
  AND ord <> 1
```
