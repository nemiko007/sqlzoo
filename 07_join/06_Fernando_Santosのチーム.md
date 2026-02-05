# Fernando Santosのチーム

**テーブル構造:** 

```sql
SELECT mdate, teamname 
FROM game JOIN eteam ON (team1=eteam.id) 
WHERE coach='Fernando Santos'
```
