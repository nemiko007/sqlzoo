# 一人当たりGDP

**テーブル構造:** `world(name, continent, area, population, gdp)`

人口2億以上の国の名前と一人当たりGDP
```sql
SELECT name, gdp/population FROM world 
WHERE population > 200000000
```
