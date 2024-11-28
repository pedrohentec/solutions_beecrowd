# 2744 - Passwords

## [Description](https://judge.beecrowd.com/pt/problems/view/2744)

## Solution

Therefore you must select the **id**, the password current and the password transformed in MD5 of each user on table **account**.

### PostgreSQL

```sql
SELECT a.id,
       a.password,
       MD5(a.password) AS "MD5"
  FROM account a;
 ```