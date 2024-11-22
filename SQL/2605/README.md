# 2605 - Executive Representants

## [Description](https://judge.beecrowd.com/pt/problems/view/2605)

## Solution

Your job is return the names of products and the suppliers where code of categories is 6.

### PostgreSQL

```sql
SELECT pd.name,
	   pv.name
  FROM products pd
 INNER JOIN providers pv
    ON pd.id_categories = 6 
   AND pd.id_providers = pv.id;
```