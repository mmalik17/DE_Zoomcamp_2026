# Question 3

After running your dbt project, query the fct_monthly_zone_revenue model. <br>

What is the count of records in the fct_monthly_zone_revenue model? <br>

a. 12,998 <br>
b. 14,120 <br>
c. 12,184 <br>
d. 15,421

# Answer 
Use this query to count the records

```sql
-- Count records
SELECT COUNT(*) as total_records
FROM dbt_prod.fct_monthly_zone_revenue;

```
the result is (c)
