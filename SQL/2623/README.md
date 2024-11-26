# 2623 - Categories with Multiple Products

## [Description](https://judge.beecrowd.com/pt/problems/view/2623)

## Solution

To help the sales department, display the product name and category name for products whose quantity is greater than 100 and the category code is 1,2,3,6 or 9. Show this information in ascending order by category code.

### PostgreSQL

```sql
SELECT pd.name AS product_name,
       c.name AS category_name
  FROM products pd
 INNER JOIN categories c
    ON pd.id_categories = c.id
 WHERE pd.amount > 100 
   AND c.id IN (1, 2, 3, 6, 9)
 ORDER BY c.id;
 ```