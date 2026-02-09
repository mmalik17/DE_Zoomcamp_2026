# QUESTION 2
Write a query to count the distinct number of PULocationIDs for the entire dataset on both the tables.

What is the estimated amount of data that will be read when this query is executed on the External Table and the Table? (1 point) <br>
a. 18.82 MB for the External Table and 47.60 MB for the Materialized Table <br>
b. 0 MB for the External Table and 155.12 MB for the Materialized Table <br>
c. 2.14 GB for the External Table and 0MB for the Materialized Table <br>
d. 0 MB for the External Table and 0MB for the Materialized Table <br>

# ANSWER
In previous question, we have created The External Table, now we need to create the Table, using this query:
```sql
CREATE OR REPLACE TABLE `ny_taxi.yellow_tripdata_2024`
AS SELECT * FROM `ny_taxi.external_yellow_tripdata_2024`;
```
Notes: we create the table named "ny_taxi.yellow_tripdata_2024" that fetch the data from external table "ny_taxi.external_yellow_tripdata_2024" <br>

Now, we can compare using the identical query, but reading from different table.
```sql
SELECT COUNT(DISTINCT(PULocationID)) FROM zoomcamp-2026-486804.ny_taxi.external_yellow_tripdata_2024;
```
```sql
SELECT COUNT(DISTINCT(PULocationID)) FROM zoomcamp-2026-486804.ny_taxi.yellow_tripdata_2024;
```
