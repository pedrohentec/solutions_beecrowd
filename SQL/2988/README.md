# 2988 - Championship Ceara native

## [Description](https://judge.beecrowd.com/pt/problems/view/2988)

## Solution

Show a table with following columns: the name of team, numbers matches, wins, defeats, tie and score. Knowing that score is calculated with every victory worth 3 points, tie worth 1 and defeat yields 0. At the final show your table with the score order from largest to smallest.

### PostgreSQL

```sql
SELECT REPLACE(v.name, 'H1', 'X') AS name
  FROM virus v;
 ```