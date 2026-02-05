# 前日のデータ(LAG)

**テーブル構造:** `covid(name, whn, confirmed, deaths, recovered)`

イタリアの2020年3月の累積感染者数と前日の感染者数を表示
```sql
SELECT name, DAY(whn), confirmed, LAG(confirmed, 1) OVER (PARTITION BY name ORDER BY whn) AS dbf FROM covid 
WHERE name = 'Italy' AND MONTH(whn) = 3 AND YEAR(whn) = 2020 
ORDER BY whn
```
