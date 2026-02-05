# 順位の表示(RANK)

**テーブル構造:** `ge(id, lastName, firstName, constituency, party, votes, yr)`

2017年の'S14000024'選挙区における各政党の順位を表示
```sql
SELECT party, votes, RANK() OVER (ORDER BY votes DESC) as posn FROM ge 
WHERE constituency = 'S14000024' AND yr = 2017 
ORDER BY party
```
