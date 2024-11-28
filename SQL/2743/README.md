# 2743 - Number of Characters

## [Description](https://judge.beecrowd.com/pt/problems/view/2743)

## Solution

You must show the number of characters for each name in descending order by the number of characters.

### PostgreSQL

```sql
SELECT p.name,
      CHAR_LENGTH(p.name) AS "Length"
  FROM people p
 ORDER BY "Length" desc;
 ```