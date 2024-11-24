# 2616 - No Rentals

## [Description](https://judge.beecrowd.com/pt/problems/view/2616)

## Solution

Your job is to give us the ID and name of the customers who did not make any rentals. Sort the output by ID.

### PostgreSQL

```sql
SELECT c.id AS id, 
       c.name AS name 
  FROM customers c 
  LEFT JOIN locations l 
  ON c.id = l.id_customers 
 WHERE l.id_customers IS NULL;
```