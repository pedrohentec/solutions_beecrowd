# 2602 - Select Basic

## [Description](https://www.beecrowd.com.br/judge/pt/problems/view/2602)

## Solution

Show only customers name all where state is "RS"

### PostgreSQL

```sql
SELECT c.name
  FROM customers c
 WHERE c.state = 'RS';
```