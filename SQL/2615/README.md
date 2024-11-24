# 2615 - Expanding the Business

## [Description](https://judge.beecrowd.com/pt/problems/view/2615)

## Solution

Select the name of all cities where rental company have customers. But please, dont repeat the name of city.

### PostgreSQL

```sql
SELECT DISTINCT(c.city)
  FROM customers c;
```