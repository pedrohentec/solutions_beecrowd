# 2610 - Average Value of Products

## [Description](https://judge.beecrowd.com/pt/problems/view/2610)

## Solution

To help the industry that is doing this survey you should calculate and display the average value of the price of the products.

**OBS**: Show the value with two numbers after the period.

### PostgreSQL

```sql
SELECT AVG(p.price)::DECIMAL(18,2) AS media
  FROM products p;
```