# RIGHT JOIN(全部署)

```sql
SELECT teacher.name, dept.name 
FROM teacher RIGHT JOIN dept ON (teacher.dept=dept.id)
```
