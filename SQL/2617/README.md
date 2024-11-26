# 2617 - Provider Ajax SA

## [Description](https://judge.beecrowd.com/pt/problems/view/2617)

## Solution

Your job is to show the name of products and the name of provider, for the products provided of provider 'Ajax SA'.

### PostgreSQL

```sql
SELECT pd.name AS product_name,
       pv.name AS provider_name
  FROM products pd
 INNER JOIN providers pv
    ON pd.id_providers = pv.id
 WHERE pv.name = 'Ajax SA';
```