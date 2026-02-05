# LEFT JOIN(全教師)

```sql
SELECT teacher.name, dept.name 
FROM teacher LEFT JOIN dept ON (teacher.dept=dept.id)
```
