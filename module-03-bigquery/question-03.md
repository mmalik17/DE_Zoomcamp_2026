# Question 3
Write a query to retrieve the PULocationID from the table (not the external table) in BigQuery. Now write a query to retrieve the PULocationID and DOLocationID on the same table. <br>
Why are the estimated number of Bytes different? (1 point) <br>
<br>
a. BigQuery is a columnar database, and it only scans the specific columns requested in the query. Querying two columns (PULocationID, DOLocationID) 
requires reading more data than querying one column (PULocationID), leading to a higher estimated number of bytes processed. <br>
b. BigQuery duplicates data across multiple storage partitions, so selecting two columns instead of one requires scanning the table twice, 
doubling the estimated bytes processed. <br>
c. BigQuery automatically caches the first queried column, so adding a second column increases processing time but does not affect 
the estimated bytes scanned. <br>
d. When selecting multiple columns, BigQuery performs an implicit join operation between them, increasing the estimated bytes processed <br>

# Answer
Query to retrieve the PULocationID column: <br>
```sql
select PULocationID from zoomcamp-2026-486804.ny_taxi.yellow_tripdata_2024;
```
Query to retrieve the PULocationID and DOLocationID columns: <br>
```sql
select PULocationID, DOLocationID from zoomcamp-2026-486804.ny_taxi.yellow_tripdata_2024;
```
