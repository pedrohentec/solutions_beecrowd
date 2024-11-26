# 2620 - Orders in First Semester

## [Description](https://judge.beecrowd.com/pt/problems/view/2620)

## Solution

Then display the customer name and order number for customers who placed orders in the first half of 2016.

PS: The platform you are using may give an error regarding the date going out of range. To resolve this, modify the code offered between lines 33 and 38 to

 (1, TO_DATE('13/05/2016', 'DD/MM/YYYY'), 3),
 (2, TO_DATE('12/01/2016', 'DD/MM/YYYY'), 2),
 (3, TO_DATE('18/04/2016', 'DD/MM/YYYY'), 5),
 (4, TO_DATE('07/09/2016', 'DD/MM/YYYY'), 4),
 (5, TO_DATE('13/02/2016', 'DD/MM/YYYY'), 6),
 (6, TO_DATE('05/08/2016', 'DD/MM/YYYY'), 3);

### PostgreSQL

```sql
SELECT c.name,
       o.id
  FROM customers c
 INNER JOIN orders o 
    ON o.id_customers = c.id
 WHERE o.orders_date > '01/01/2016' AND o.orders_date < '06/30/2016';
 ```