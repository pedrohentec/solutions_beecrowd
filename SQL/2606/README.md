# 2606 - Categories

## [Description](https://judge.beecrowd.com/pt/problems/view/2606)

## Solution

Your chieff need than you to show the code and the name of products, where categories start with "super".

### PostgreSQL

```sql
SELECT p.id,
 	   p.name
  FROM products p
 INNER JOIN categories c
    ON c.name LIKE 'super%' 
   AND p.id_categories = c.id;
```