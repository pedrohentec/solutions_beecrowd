# 2991 - Department Statistics

## [Description](https://judge.beecrowd.com/pt/problems/view/2991)

## Solution

For each department in the company, show its name, the number of employees, the average salary, the highest salary and the lowest salary. The result should be in descending order by average salary.

Tip: You can use the COALESCE(check_expression , 0) function to replace any null value with zero; you can also use the ROUND(value, 2) function to display the values ​​with 2 decimal places.

### PostgreSQL

```sql
SELECT dep.nome AS "Nome Departamento",
       COUNT(emp.matr) AS "Numero de Empregados",
       ROUND((AVG(tsalario.salario - tdesconto.descontos)), 2) AS "Media Salarial",
       ROUND((MAX(tsalario.salario - tdesconto.descontos)), 2) AS "Maior Salario",
       (CASE WHEN MIN(tsalario.salario - tdesconto.descontos) = 0 THEN '0'
             ELSE ROUND((MIN(tsalario.salario - tdesconto.descontos)), 2) END ) AS "Menor Salario"
  FROM departamento dep
 INNER JOIN empregado emp
    ON dep.cod_dep = emp.lotacao
 INNER JOIN(SELECT emp.matr,
                   COALESCE(SUM(v.valor), 0) AS salario
              FROM empregado emp
              LEFT JOIN emp_venc
                ON emp.matr = emp_venc.matr
              LEFT JOIN vencimento v
                ON emp_venc.cod_venc = v.cod_venc
             GROUP BY emp.matr
            ) AS tsalario ON emp.matr = tsalario.matr
 INNER JOIN(SELECT emp.matr,
                   COALESCE(SUM(desconto.valor), 0) AS descontos
              FROM empregado emp
              LEFT JOIN emp_desc
                ON emp.matr = emp_desc.matr
              LEFT JOIN desconto 
                ON emp_desc.cod_desc = desconto.cod_desc
             GROUP BY emp.matr
            ) AS tdesconto ON emp.matr = tdesconto.matr
 GROUP BY dep.cod_dep,
          dep.nome
 ORDER BY "Media Salarial" DESC;
 ```