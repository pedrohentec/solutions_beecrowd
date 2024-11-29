# 3483 - Second Biggest and Smallest

## [Description](https://judge.beecrowd.com/pt/problems/view/3483)

## Solution

Find the city with the second biggest population and then the second smallest population.
### PostgreSQL

```sql
WITH maior AS(
SELECT c.city_name,
      c.population
  FROM cities c 
ORDER BY c.population desc
LIMIT 2
), 

menor AS
(
SELECT c.city_name,
      c.population
  FROM cities c 
ORDER BY c.population
LIMIT 2
),

segundo_maior AS
(
SELECT *
  FROM maior m
 ORDER BY m.population
 LIMIT 1
),

segundo_menor AS
(
SELECT *
  FROM menor m
 ORDER BY m.population desc
 LIMIT 1
)

SELECT *
 FROM segundo_maior
 
UNION ALL

SELECT *
  FROM segundo_menor
 ```