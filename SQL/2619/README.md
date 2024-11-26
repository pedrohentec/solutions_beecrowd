# 2619 - Super Luxury

## [Description](https://judge.beecrowd.com/pt/problems/view/2619)

## Solution

Your job is display the name of products, name of providers and the price, for the products whose price be bigger 1000 and your categorie be 'Super Luxury'.

### PostgreSQL

```sql
SELECT pd.name AS product_name,
       pv.name AS provider_name,
       pd.price AS price
  FROM products pd
 INNER JOIN providers pv
    ON pd.id_providers = pv.id
 INNER JOIN categories c
    ON pd.id_categories = c.id
 WHERE pd.price > 1000 AND c.name = 'Super Luxury';
```