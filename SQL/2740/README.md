# 2740 - League

## [Description](https://judge.beecrowd.com/pt/problems/view/2740)

## Solution

Select the top three teams from the list with the initial phrase Podium: and also, the last two teams that will be relegated to series B with the initial phrase Demoted:.

### PostgreSQL

```sql
(
SELECT CONCAT('Podium: ', l.team) as name
  FROM league l
 WHERE l.position IN (1,2,3)
)
UNION ALL 
(
 SELECT CONCAT('Demoted: ', l.team) as name
   FROM league l 
  WHERE l.position IN (14, 15)
)
 ```