# CraiglochartとTollcrossを結ぶ路線

```sql
SELECT R1.company, R1.num 
FROM route R1, route R2, stops S1, stops S2 
WHERE R1.num=R2.num 
  AND R1.company=R2.company 
  AND R1.stop=S1.id 
  AND R2.stop=S2.id 
  AND S1.name='Craiglockhart' 
  AND S2.name='Tollcross'
```
