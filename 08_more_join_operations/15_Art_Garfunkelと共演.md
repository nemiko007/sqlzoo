# Art Garfunkelと共演

```sql
SELECT DISTINCT d.name 
FROM actor d 
JOIN casting a ON (a.actorid=d.id) 
JOIN casting b ON (a.movieid=b.movieid) 
JOIN actor c ON (b.actorid=c.id AND c.name='Art Garfunkel') 
WHERE d.id != c.id
```
