# COALESCE(部署名)

```sql
SELECT teacher.name, COALESCE(dept.name, 'None') 
FROM teacher LEFT JOIN dept ON teacher.dept=dept.id
```
