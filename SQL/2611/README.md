# 2611 - Movies of Action

## [Description](https://judge.beecrowd.com/pt/problems/view/2611)

## Solution

They need you select the code and the name of movies whose describe genre is "Action". 

### PostgreSQL

```sql
SELECT m.id,
	   m.name
  FROM movies m
 INNER JOIN genres g
 	ON m.id_genres = g.id
 WHERE g.description = 'Action';
```