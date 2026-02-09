# Question 4

How many records have a fare_amount of 0? (1 point) <br>
a. 128,210 <br>
b. 546,578 <br>
c. 20,188,016 <br>
d. 8,333 <br>

# Answer
Query to count the records with fare_amount of 0:
```sql
select count(1) from ny_taxi.external_yellow_tripdata_2024
where fare_amount = 0;
```

The above query yields the output of 8333, so the answer is (d)
