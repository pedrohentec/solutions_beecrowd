# 2737 - Lawyers

## [Description](https://judge.beecrowd.com/pt/problems/view/2737)

## Solution

The director wants you to show him the name of the lawyer who has the most clients, the name of the lawyer who has the fewest clients, and the average number of clients among all lawyers.

NOTE: Before showing the average, show a field called Average in order to make the report more presentable. The average should be shown in integers.

### PostgreSQL

```sql
(
SELECT name, customers_number
FROM lawyers
ORDER BY customers_number DESC
LIMIT 1
)

UNION ALL

(
SELECT name, customers_number
FROM lawyers
ORDER BY customers_number ASC
LIMIT 1
)

UNION ALL

(
SELECT 'Average', round(AVG(customers_number), 0)
FROM lawyers
)
 ```