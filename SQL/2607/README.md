# 2607 - Cities in Alphabetical Order

## [Description](https://judge.beecrowd.com/pt/problems/view/2607)

## Solution

Return all the cities of providers, but in alphabetic order

### PostgreSQL

```sql
SELECT p.city
    FROM providers p
ORDER BY p.city;
```