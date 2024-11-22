# 2604 - Less than 10 or Greater than 100

## [Description](https://judge.beecrowd.com/pt/problems/view/2604)

## Solution

Show the code and the name of products where price are less than 10  or greater than 100.

### PostgreSQL

```sql
SELECT p.id,
	   p.name
  FROM products p
 WHERE p.price < 10 OR p.price > 100;
```