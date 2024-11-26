# 2624 - Number of Cities per Customer

## [Description](https://judge.beecrowd.com/pt/problems/view/2624)

## Solution

Display the number of distinct cities in the customers table.

### PostgreSQL

```sql
SELECT COUNT(DISTINCT(customers.city)) AS amount
  FROM customers;
 ```