# XOR - どちらか一方だけ大きい

**テーブル構造:** `world(name, continent, area, population, gdp)`

```sql
SELECT name, population, area FROM world 
WHERE (population > 250000000 OR area > 3000000) 
  AND NOT(population > 250000000 AND area > 3000000)
```
