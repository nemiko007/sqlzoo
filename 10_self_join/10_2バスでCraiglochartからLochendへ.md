# 2バスでCraiglochartからLochendへ

```sql
SELECT bus1.num, bus1.company, name, bus2.num, bus2.company 
FROM (SELECT start1.num, start1.company, stop1.stop 
      FROM route AS start1 
      JOIN route AS stop1 ON start1.num = stop1.num 
                          AND start1.company = stop1.company 
                          AND start1.stop != stop1.stop 
      WHERE start1.stop = (SELECT id FROM stops WHERE name = 'Craiglockhart')) AS bus1 
JOIN (SELECT start2.num, start2.company, start2.stop 
      FROM route AS start2 
      JOIN route AS stop2 ON start2.num = stop2.num 
                          AND start2.company = stop2.company 
                          AND start2.stop != stop2.stop 
      WHERE stop2.stop = (SELECT id FROM stops WHERE name = 'Lochend')) AS bus2 
ON bus1.stop = bus2.stop 
JOIN stops ON bus1.stop = stops.id 
ORDER BY bus1.num, bus1.company, name, bus2.num, bus2.company
```

---

## まとめ

このドキュメントには、SQLZooの主要な10個のチュートリアルから合計**100問以上**の演習問題とその模範解答が含まれています。

各チュートリアルで学べる主なスキル:
- **SELECT basics**: 基本的なSELECT文とWHERE句
- **SELECT names**: LIKE演算子とパターンマッチング
- **SELECT from World**: 比較演算子、算術演算、文字列関数
- **SELECT from Nobel**: 複雑な条件、ORDER BY、CASE文
- **SELECT within SELECT**: サブクエリ、相関サブクエリ
- **SUM and COUNT**: 集約関数、GROUP BY、HAVING
- **JOIN**: 内部結合、複数テーブルの結合
- **More JOIN**: 複雑な結合、サブクエリとの組み合わせ
- **Using Null**: NULL処理、外部結合、COALESCE
- **Self join**: 自己結合、複雑なクエリ構築

これらの演習を通じて、SQLの基礎から応用まで体系的に学習できます。
