# 年ごとの順位(PARTITION BY)

**テーブル構造:** `ge(id, lastName, firstName, constituency, party, votes, yr)`

'S14000021'選挙区における年ごとの各政党の順位を表示
```sql
SELECT yr, party, votes, RANK() OVER (PARTITION BY yr ORDER BY votes DESC) as posn FROM ge 
WHERE constituency = 'S14000021' 
ORDER BY party, yr
```
