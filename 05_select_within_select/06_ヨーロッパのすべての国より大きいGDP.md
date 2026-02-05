# ヨーロッパのすべての国より大きいGDP

**テーブル構造:** `world(name, continent, area, population, gdp)`

```sql
SELECT name FROM world 
WHERE gdp > ALL (SELECT gdp FROM world 
                 WHERE continent = 'Europe' AND gdp IS NOT NULL)
```
