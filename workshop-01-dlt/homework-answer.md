# QUESTION 1
What is the start date and end date of the dataset? (1 point) <br>
a. 2009-01-01 to 2009-01-31 <br>
b. 2009-06-01 to 2009-07-01 <br>
c. 2024-01-01 to 2024-02-01 <br>
d. 2024-06-01 to 2024-07-01 <br>

### Answer :
To know the start and end date, i use this aggregation query
```sql
SELECT
    MIN(trip_pickup_date_time) as min_date,
    MAX(trip_pickup_date_time) as max_date
FROM nyc_taxi.trips
```
When executed, min_date has value of 2009-06-01, while the max_date has value of 2009-07-01,
so the date range is 2009-06-01 to 2009-07-01 (b)


# QUESTION 2
What proportion of trips are paid with credit card? (1 point) <br>
a. 16.66% <br>
b. 26.66% <br>
c. 36.66% <br>
d. 46.66% <br>

### Answer :

The proportion (percentage) of trips that are paid with credit card, can be calculated by using Count, Group By, and windows function sum(count(*)) over(). Here is the query:

```sql
SELECT
    payment_type,
    COUNT(*) as count,
    ROUND(COUNT(*) * 100.0 / SUM(COUNT(*)) OVER(), 2) as percentage
FROM nyc_taxi.trips
GROUP BY payment_type
ORDER BY count DESC
```
**SUM(COUNT(*)) OVER()** is a window function that calculates total trips across all payment types
The ROUND(... ,2) query is used to limit the decimal only have 2 number behind comma

From the query results, we noted that among 10,000 trips, 2,666 of them were paid with credit card, so the precentage of using credit card is 2,666 / 10,0000 = 26.66%.

# QUESTION 3
What is the total amount of money generated in tips? (1 point)
a. $4,063.41 <br>
b. $6,063.41 <br>
c. $8,063.41 <br>
d. $10,063.41 <br>

### Answer :

The sum of money generated in tips can be calculated with SUM() aggregation query
```sql
SELECT ROUND(SUM(tip_amt), 2) as total_tips
FROM nyc_taxi.trips
```
The ROUND(... ,2) query is used to limit the decimal only have 2 number behind comma.

from the query, we could infer that the number of money generated in tips are $6,063.41
