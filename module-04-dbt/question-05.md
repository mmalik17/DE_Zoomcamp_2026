# Question 5

Using the fct_monthly_zone_revenue table, what is the total number of trips (total_monthly_trips) for Green taxis in October 2019?

a. 500,234
b. 350,891
c. 384,624
d. 421,509


# Answer 

Use this query to find out:
```sql
SELECT 
    revenue_month,
    SUM(total_monthly_trips) as total_trips_october_2019
FROM dbt_prod.fct_monthly_zone_revenue
WHERE service_type = 'Green'
  AND revenue_year = 2019
  AND revenue_month_num = 10
GROUP BY revenue_month;
```

The answer is (c)
