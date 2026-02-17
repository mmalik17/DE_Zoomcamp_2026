# Question 4

Using the fct_monthly_zone_revenue table, find the pickup zone with the highest total revenue (revenue_monthly_total_amount) for Green taxi trips in 2020. <br>

Which zone had the highest revenue? <br>

a. East Harlem North <br>
b. Morningside Heights <br>
c, East Harlem South <br>
d. Washington Heights South

# Answer 

Use this query to identify the result

```sql
-- Best performing zone for Green taxis in 2020

with green_2020_revenue as (
    select 
        zone,
        borough,
        sum(revenue_monthly_total_amount) as total_revenue,
        sum(total_monthly_trips) as total_trips,
        avg(revenue_monthly_total_amount) as avg_monthly_revenue
    from {{ ref('fct_monthly_zone_revenue') }}
    where service_type = 'Green'
      and revenue_year = 2020
    group by zone, borough
)

select 
    zone,
    borough,
    round(total_revenue::numeric, 2) as total_revenue,
    total_trips,
    round(avg_monthly_revenue::numeric, 2) as avg_monthly_revenue,
    rank() over (order by total_revenue desc) as revenue_rank
from green_2020_revenue
order by total_revenue desc
limit 5
```

from that query, it is concluded that the pickup zone with the highest total revenue is East Harlem  North, so the answer is (a)
