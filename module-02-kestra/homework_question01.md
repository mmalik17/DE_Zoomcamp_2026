# Question 1 
Within the execution for Yellow Taxi data for the year 2020 and month 12: what is the uncompressed file size (i.e. the output file yellow_tripdata_2020-12.csv of the extract task)? (1 point) <br>

a. 128.3 MiB <br>
b. 134.5 MiB <br>
c. 364.7 MiB <br>
d. 692.6 MiB <br>

# Answer

1. Run Kestra with Docker. Execute file docker-compose.yaml with command : docker-compose up -d
2. Access Kestra UI on http://localhost:8081 <br> (Notes: i change the port from 8080 to 8081 in my docker-compose.yaml, because my local docker version claim port 8080 for backend process, so i can't use localhost:8080)
3. Import file yaml 04_postgres_taxi.yaml to Kestra UI <br>
4. Execute 04_postgres_taxi.yaml with this input: <br>
<br>
<p align="center">
<img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/6b8b2ef7-f26a-462d-9aba-93fae419b0ae" /> </p>

After Execute, look on Output Tab > Tasks: Extract > Outputs: Output Files, we will see the yellow_tripdata_2020-12.csv files with file size <br>
<br>
<p align="center">
<img width="755" height="397" alt="image" src="https://github.com/user-attachments/assets/0c09e342-1f2f-431b-a56d-ed4f12e6c657" />
</p>

From the image above, we concluded that the file size is <b> 128.3 MiB (a) </b>
