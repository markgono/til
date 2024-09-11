# Coalesce

The SQL coalesce operator can groom null values into a valid operand for a condition. 

Useful for where you want to include these rows in the output

```sql
SELECT name FROM Customer WHERE COALESCE(refferer,0) != 2
```