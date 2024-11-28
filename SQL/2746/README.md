# 2746 - Virus

## [Description](https://judge.beecrowd.com/pt/problems/view/2746)

## Solution

Therefore you must substitute all character 'H1' (Hemagglutinin) by 'X'(Xenomorphina).

### PostgreSQL

```sql
SELECT REPLACE(v.name, 'H1', 'X') AS name
  FROM virus v;
 ```