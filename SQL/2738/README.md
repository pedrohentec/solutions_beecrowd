# 2738 - Contest

## [Description](https://judge.beecrowd.com/pt/problems/view/2738)

## Solution

You must display the list of candidates, including the candidate's name and their final score (with two decimal places after the decimal point). Remember to display the list ordered by the candidate's score (highest score at the top of the list).

The candidate's score is the result of the weighted average described below:

      (math*2) + (specific*3) + (project_plan*5)
Avg = _____________________________________________
                            10


### PostgreSQL

```sql
SELECT c.name,
       (((s.math*2) + (s.specific*3) + (s.project_plan*5)) / 10)::NUMERIC(18,2) as avg
  FROM candidate c
 INNER JOIN score s
    ON s.candidate_id = c.id
 ORDER BY avg DESC;
 ```