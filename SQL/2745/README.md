# 2745 - Rates

## [Description](https://judge.beecrowd.com/pt/problems/view/2745)

## Solution

Therefore, show the name of people and the value she must to pay to government with precision of two decimal places

### PostgreSQL

```sql
SELECT p.name,
       ROUND((p.salary * 0.1), 2) AS tax 
  FROM people p
 WHERE p.salary > 3000;
 ```