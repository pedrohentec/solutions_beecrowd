# 2622 - Legal Entities

## [Description](https://judge.beecrowd.com/pt/problems/view/2622)

## Solution

Display the name of customers are legal entities.

### PostgreSQL

```sql
SELECT c.name
  FROM customers c 
 INNER JOIN legal_person lp
    ON lp.id_customers = c.id;
 ```