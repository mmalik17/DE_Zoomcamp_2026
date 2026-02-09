# Question 3

Why are the estimated number of Bytes different? (1 point) <br>
a. BigQuery is a columnar database, and it only scans the specific columns requested in the query. Querying two columns (PULocationID, DOLocationID) 
requires reading more data than querying one column (PULocationID), leading to a higher estimated number of bytes processed. <br>
b. BigQuery duplicates data across multiple storage partitions, so selecting two columns instead of one requires scanning the table twice, 
doubling the estimated bytes processed. <br>
c. BigQuery automatically caches the first queried column, so adding a second column increases processing time but does not affect 
the estimated bytes scanned. <br>
d. When selecting multiple columns, BigQuery performs an implicit join operation between them, increasing the estimated bytes processed <br>

# Answer
