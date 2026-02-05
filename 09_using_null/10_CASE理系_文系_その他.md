# CASE(理系/文系/その他)

```sql
SELECT name, 
       CASE WHEN dept IN (1,2) THEN 'Sci' 
            WHEN dept = 3 THEN 'Art' 
            ELSE 'None' END 
FROM teacher
```
