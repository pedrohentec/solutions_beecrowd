# 2603 - Address of Customers

## [Description](https://judge.beecrowd.com/pt/problems/view/2603)

## Solution

Our work is to send address of customers lives on "Porto Alegre".

### PostgreSQL

```sql
SELECT c.name,
	   c.street
  FROM customers c
 WHERE c.city = 'Porto Alegre';
```