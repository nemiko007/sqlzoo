# 首都が国名 + "City"

**テーブル構造:** `world(name, continent, area, population, gdp, capital)`

```sql
SELECT name FROM world WHERE capital = concat(name, ' City')
```
