# 前週比(JOIN)

**テーブル構造:** `covid(name, whn, confirmed, deaths, recovered)`

イタリアの月曜日における前週比を表示
```sql
SELECT tw.name, DATE_FORMAT(tw.whn,'%Y-%m-%d'), tw.confirmed - lw.confirmed FROM covid tw 
LEFT JOIN covid lw ON DATE_ADD(lw.whn, INTERVAL 1 WEEK) = tw.whn AND tw.name=lw.name 
WHERE tw.name = 'Italy' AND WEEKDAY(tw.whn) = 0 
ORDER BY tw.whn
```
