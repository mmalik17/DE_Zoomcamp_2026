# Question 3 
How many rows are there for the Yellow Taxi data for all CSV files in the year 2020? (1 point) <br>
a. 13,537.299 <br>
b. 24,648,499 <br>
c. 18,324,219 <br>
d. 29,430,127 <br>

# ANSWER

1. Import the 05_postgres_taxi_scheduled.yaml to Kestra UI that run on localhost:8081
2. Go to Trigger Tab, and choose Execute Backfill button. Use input below to execute the workflow
INPUT :
<img width="1243" height="594" alt="image" src="https://github.com/user-attachments/assets/e4023b56-3397-4e57-890e-ec0872b086df" />
Notes for filling the backfill input:
At workflow, i set the cron schedule to ............, so it will run every month at the first day on 02.00 a.m
Because we need to run from Jan 2020 to Dec 2020, so...
- the start time of backfill input should be set before 2020-01-01 02:00:00, so i set it on 2020-01-01 00:00:00
- the end time of backfill input should be set after 2020-12-01 02:00:00, so i set it on 2020-12-03 00:00:00
Then, click execute

CHECK WHETHER THE TABLE IS FILLED OR NOT
<img width="866" height="611" alt="image" src="https://github.com/user-attachments/assets/3ef7521d-5155-470b-b365-84b5bec5b901" />

CHECK THE OUTPUT TABLE COUNT :
<img width="1114" height="498" alt="image" src="https://github.com/user-attachments/assets/68490d2b-a818-4286-a97d-8d007c45eb6f" />

