# 2741 - Student Grades

## [Description](https://judge.beecrowd.com/pt/problems/view/2741)

## Solution

Therefore, you should display the phrase 'Approved: ' along with the student's name and grade for students who have passed (grade ≥7).

Remember to order the list by highest score.

### PostgreSQL

```sql
SELECT CONCAT('Approved: ', s.name) AS name,
       s.grade
  FROM students s
 WHERE s.grade >= 7
 ORDER BY s.grade DESC;
 ```