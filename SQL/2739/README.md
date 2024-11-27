# 2739 - Payment Day

## [Description](https://judge.beecrowd.com/pt/problems/view/2739)

## Solution

The bank ask for your help for select the names and day of month that each customer must pay their share.

### PostgreSQL

```sql
SELECT l.name,
       CAST(EXTRACT(DAY FROM l.payday) AS INTEGER) as day
  FROM loan l;
 ```