# Question 2 

What is the rendered value of the variable file when the inputs taxi is set to green, year is set to 2020, and month is set to 04 during execution? (1 point)
<br>
a. {{inputs.taxi}}_tripdata_{{inputs.year}}-{{inputs.month}}.csv <br>
b. green_tripdata_2020-04.csv <br>
c. green_tripdata_04_2020.csv <br>
d. green_tripdata_2020.csv <br>

# Answer

1. Run Kestra with Docker. Execute file docker-compose.yaml with command docker-compose up -d
2. Import file yaml 04_postgres_taxi.yaml to Kestra UI
3. Execute that file yaml with the input below
   <br>
   <img width="1603" height="765" alt="image" src="https://github.com/user-attachments/assets/cbee5c3b-655a-4453-b9cf-eda94135df15" />
5. After execute, go to Output tab > tasks: Extract > Outputs : outputFiles. Then, it will see image like below
   <br>
   <img width="905" height="444" alt="image" src="https://github.com/user-attachments/assets/79e9a541-5527-41bd-91d2-4d02dea54c6c" />
 6. So, the answer is <b> (b) green_tripdata_2020-04.csv </b>
