# 2608 - Higher and Lower Price

## [Description](https://judge.beecrowd.com/pt/problems/view/2608)

## Solution

For this you must display only the highest and lowest price of the products table.

### PostgreSQL

```sql
SELECT MAX(price) AS maior,
    MIN(price) AS menor
FROM products p;
```