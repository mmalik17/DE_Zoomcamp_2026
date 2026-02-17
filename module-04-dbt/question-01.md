# Question 1

Q1: dbt run --select int_trips_unioned builds which models? (1 point) <br>

a. stg_green_tripdata, stg_yellow_tripdata, and int_trips_unioned <br>
b. Any model with upstream and downstream dependencies <br>
c. int_trips_unioned only <br>
d. int_trips_unioned, int_trips, and fct_trips <br>

# Answer:

If the parameter --select (or shorthand -s) is used after dbt run command and without any additional operators, DBT will exclusively run the specific model you have named.
The specific model is int_trips_unioned, so the answer is (c)
