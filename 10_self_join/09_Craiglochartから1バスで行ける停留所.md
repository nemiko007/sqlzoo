# Craiglochartから1バスで行ける停留所

```sql
SELECT DISTINCT S2.name, R2.company, R2.num 
FROM stops S1, stops S2, route R1, route R2 
WHERE S1.name='Craiglockhart' 
  AND S1.id=R1.stop 
  AND R1.company=R2.company 
  AND R1.num=R2.num 
  AND R2.stop=S2.id
```
