# 2613 - Movies on Sale

## [Description](https://judge.beecrowd.com/pt/problems/view/2613)

## Solution

Your job for us to help is select the ID and the name of movies whose price  is lower than 2.00

### PostgreSQL

```sql
SELECT m.id,
	   m.name
  FROM movies m
 INNER JOIN prices p
 	ON m.id_prices = p.id
 WHERE p.value < 2.00;
```