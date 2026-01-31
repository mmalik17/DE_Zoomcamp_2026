# Question 4
How many rows are there for the Green Taxi data for all CSV files in the year 2020? (1 point) <br>
a. 5,327,301 <br>
b. 936,199 <br>
c. 1,734,051 <br>
d. 1,342,034 <br>

# Answer :
1. Import the 05_postgres_taxi_scheduled.yaml to Kestra UI that run on localhost:8081  <br>
(Notes: i change the port from 8080 to 8081 in my docker-compose.yaml, because my local docker version claim port 8080 for backend process so i can't use localhost:8080 for Kestra UI) <br>
2. Go to Trigger Tab, and choose Execute Backfill button. <br>
Use input below to execute the workflow  :
<br>
     <img width="500" height="300" alt="image" src="https://github.com/user-attachments/assets/4fb8bb6d-43cd-46de-90cc-c953c0504401" /> <br>
Notes for choosing the time for backfill input: <br>
At workflow, i set the cron schedule "0 2 1 * *", so it will run every month at the first day on 02.00 a.m  <br>
Because we need to run from Jan 2020 to Dec 2020, so...  <br>
- the start time of backfill input should be set before 2020-01-01 02:00:00, so i set it on 2020-01-01 00:00:00
- the end time of backfill input should be set after 2020-12-01 02:00:00, so i set it on 2020-12-03 00:00:00
Then, click execute

3. Login to PgAdmin that run on localhost:8085 <br>

4. Check whether the table contains data from january 2020 to december 2020 by using the query shown below: <br>
<img width="769" height="663" alt="image" src="https://github.com/user-attachments/assets/5244b74a-5546-48bf-a237-ea591b57182b" />

5. If all the data has been inserted to postgresql table, you can use query below to calculate the total rows inserted <br>
<img width="1113" height="429" alt="image" src="https://github.com/user-attachments/assets/02372e7b-944f-4bbd-acd2-a3f65cc30cbb" />
