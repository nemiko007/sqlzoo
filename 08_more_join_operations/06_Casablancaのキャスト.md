# Casablancaのキャスト

```sql
SELECT name FROM casting, actor 
WHERE movieid=(SELECT id FROM movie WHERE title='Casablanca' AND yr=1942) 
  AND actorid=actor.id
```
