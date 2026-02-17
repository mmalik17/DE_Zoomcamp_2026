# Question 6

Create a staging model for the For-Hire Vehicle (FHV) trip data for 2019.

Load the FHV trip data for 2019 into your data warehouse
Create a staging model stg_fhv_tripdata with these requirements:
Filter out records where dispatching_base_num IS NULL
Rename fields to match your project's naming conventions (e.g., PUlocationID → pickup_location_id)
What is the count of records in stg_fhv_tripdata? <br>

a. 42,084,899 <br>
b. 43,244,693 <br>
c. 22,998,722 <br>
d. 44,112,187

# Answer 

Use this query tp count the record after filtering

``` sql

select 
    count(*) as total_records,
    count(distinct dispatching_base_num) as unique_bases,
    min(pickup_datetime) as earliest_pickup,
    max(pickup_datetime) as latest_pickup,
    count(distinct pickup_datetime::date) as distinct_days
from dbt_prod.stg_fhv_tripdata;
```

from query above, The answer is 43,244,693
