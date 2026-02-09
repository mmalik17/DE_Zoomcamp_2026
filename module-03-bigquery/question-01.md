# Question 1
What is count of records for the 2024 Yellow Taxi Data? (1 point) <br>
a. 65,623 <br>
b. 840,402 <br>
c. 20,332,093 <br>
d. 85,431,289 <br>

# Answer
STEP 1: Create external table that read data from Google Cloud Storage <br>
```sql
zoomcamp-2026-486804.ny_taxi.external_yellow_tripdata_2024
OPTIONS (
  format = 'PARQUET',
  uris = ['gs://nyc-tl-data-486804/ny_taxi_homework/yellow_tripdata_2024-*.parquet']
);
```

STEP 2: Read the external table to count the rows <br>
```sql
select count(1) from ny_taxi.external_yellow_tripdata_2024;
```

The result is 20,332,09, so the answer is (c)
