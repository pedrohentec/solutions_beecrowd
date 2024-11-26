# 2618 - Products Imports

## [Description](https://judge.beecrowd.com/pt/problems/view/2618)

## Solution

Your task is display the name of products, the name of provider and the name of categorie, for the products providers by the provider 'Sansul SA' and whose name of categorie be 'Imported'.

### PostgreSQL

```sql
SELECT pd.name AS product_name,
       pv.name AS provider_name,
       c.name AS category_name
  FROM products pd
 INNER JOIN providers pv
    ON pd.id_providers = pv.id
 INNER JOIN categories c
    ON pd.id_categories = c.id
 WHERE pv.name = 'Sansul SA' AND c.name = 'Imported';
```