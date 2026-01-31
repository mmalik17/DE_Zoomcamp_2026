# Question 3 
How many rows are there for the Yellow Taxi data for all CSV files in the year 2020? (1 point) <br>
a. 13,537.299 <br>
b. 24,648,499 <br>
c. 18,324,219 <br>
d. 29,430,127 <br>

# ANSWER

1. Import the 05_postgres_taxi_scheduled.yaml to Kestra UI that run on localhost:8081
   (Notes: i change the port from 8080 to 8081 in my docker-compose.yaml, because my local docker version claim port 8080 for backend process)  
2. Go to Trigger Tab, and choose Execute Backfill button. <br> Use input below to execute the workflow
INPUT :
<img width="1243" height="594" alt="image" src="https://github.com/user-attachments/assets/e4023b56-3397-4e57-890e-ec0872b086df" />
Notes for choosing the time for backfill input: <br>
At workflow, i set the cron schedule to ............, so it will run every month at the first day on 02.00 a.m <br>
Because we need to run from Jan 2020 to Dec 2020, so... <br>
- the start time of backfill input should be set before 2020-01-01 02:00:00, so i set it on 2020-01-01 00:00:00 <br>
- the end time of backfill input should be set after 2020-12-01 02:00:00, so i set it on 2020-12-03 00:00:00 <br>
Then, click execute <br>
<br>
3. Login to PgAdmin that run on localhost:8085 <br>
<br>
4. Check whether the table contains data from january 2020 to december 2020 by using the query shown below: <br>
<img width="866" height="611" alt="image" src="https://github.com/user-attachments/assets/3ef7521d-5155-470b-b365-84b5bec5b901" />
<br>
5. If the output is like above, you can use query below to calculate the total rows inserted <br>
<img width="1114" height="498" alt="image" src="https://github.com/user-attachments/assets/68490d2b-a818-4286-a97d-8d007c45eb6f" />
<br>
from image above, we found out that the Yellow Taxi data on year 2020 contains <b> 24,648,499 rows (b) </b>

