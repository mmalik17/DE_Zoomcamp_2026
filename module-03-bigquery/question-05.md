# Question 5
What is the best strategy to make an optimized table in Big Query if your query will always filter based on tpep_dropoff_datetime and 
order the results by VendorID (Create a new table with this strategy) (1 point) <br>
a. Partition by tpep_dropoff_datetime and Cluster on VendorID <br>
b. Cluster on by tpep_dropoff_datetime and Cluster on VendorID <br>
c. Cluster on tpep_dropoff_datetime Partition by VendorID <br>
d. Partition by tpep_dropoff_datetime and Partition by VendorID <br>

# Answer
Partitioning is suitable to skip scanning the unfiltered data, while clustering is suitable for sorting the data. To optimize the table that often get filtered on column tpep_dropoff_datetime and get ordered on column VendorID, it would be the best to Create Partition by tpep_dropoff_datetime and Cluster on VendorID

The query:
```sql
CREATE OR REPLACE TABLE `ny_taxi.yellow_tripdata_2024_partitioned_clustered`
PARTITION BY DATE(tpep_dropoff_datetime)
CLUSTER BY VendorID 
AS SELECT * FROM `ny_taxi.yellow_tripdata_2024`;
```

The answer is (a)
