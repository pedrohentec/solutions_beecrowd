# 2621 - Quantities Between 10 and 20

## [Description](https://judge.beecrowd.com/pt/problems/view/2621)

## Solution

Display the name of products whose quantities are between 10 and 20 and whose supplier name begins with letter 'P'.

### PostgreSQL

```sql
SELECT pd.name
  FROM providers pv
 INNER JOIN products pd
    ON pd.id_providers = pv.id
 WHERE pd.amount BETWEEN 10 AND 20 
   AND pv.name LIKE 'P%';
 ```