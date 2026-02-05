# HaymarketとLeithを結ぶ路線

```sql
SELECT DISTINCT R1.company, R1.num 
FROM route R1, route R2 
WHERE R1.num=R2.num 
  AND R1.company=R2.company 
  AND R1.stop=115 
  AND R2.stop=137
```
