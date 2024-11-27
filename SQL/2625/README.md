# 2625 - CPF Mask

## [Description](https://judge.beecrowd.com/pt/problems/view/2625)

## Solution

Select all CPF of all customers, and apply a mask about return of data.

The CPF mask looks like: '000.000.000-00'.

### PostgreSQL

```sql
SELECT CONCAT(SUBSTRING(np.cpf,1,3),'.',
              SUBSTRING(np.cpf,4,3),'.',
              SUBSTRING(np.cpf,7,3),'-',
              SUBSTRING(np.cpf,10,2)) as CPF
  FROM customers c
 INNER JOIN natural_person np
    ON np.id_customers = c.id;
 ```