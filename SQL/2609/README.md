# 2609 - Products by Categories

## [Description](https://judge.beecrowd.com/pt/problems/view/2609)

## Solution

Then your job will display the name and amount of products of each category.

### PostgreSQL

```sql
SELECT c.name,
	   SUM(p.amount) AS quantidade
  FROM products p
 INNER JOIN categories c
 	ON p.id_categories = c.id
 GROUP BY c.name
 ORDER BY quantidade;
```