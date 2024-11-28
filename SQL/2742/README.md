# 2742 - The Multiverse of Richard

## [Description](https://judge.beecrowd.com/pt/problems/view/2742)

## Solution

Your first task is to select all possible Richards from the C875 and C774 dimensions, along with their probability of existence (the N factor) with the precision of 3 decimal places.

Remember that (the N factor) is calculated by multiplying the omega value by 1.618. The data should be sorted by the smallest value in the omega field.

### PostgreSQL

```sql
SELECT lr.name,
       ROUND((lr.omega * 1.618), 3) AS "Fator N"
  FROM life_registry lr
 INNER JOIN dimensions d 
    ON lr.dimensions_id = d.id
 WHERE d.name IN ('C774', 'C875') 
   AND lr.name LIKE 'Richard%'
 ORDER BY lr.omega;
 ```