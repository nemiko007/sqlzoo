# National Stadium, Warsawのゴール

**テーブル構造:** 

```sql
SELECT player 
FROM goal JOIN game ON (id=matchid) 
WHERE stadium = 'National Stadium, Warsaw'
```
