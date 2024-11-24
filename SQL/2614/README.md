# 2614 - September Rentals

## [Description](https://judge.beecrowd.com/pt/problems/view/2614)

## Solution

Select the name of the customers and the rental date, from rentals carried out in September 2016.

### PostgreSQL

```sql
SELECT c.name,
	   r.rentals_date
  FROM customers c 
 INNER JOIN rentals r 
    ON r.id_customers = c.id
 WHERE r.rentals_date BETWEEN '2016-09-01' AND '2016-09-30';
```