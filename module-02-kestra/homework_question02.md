# Question 2 

What is the rendered value of the variable file when the inputs taxi is set to green, year is set to 2020, and month is set to 04 during execution? (1 point)
<br>
a. {{inputs.taxi}}_tripdata_{{inputs.year}}-{{inputs.month}}.csv <br>
b. green_tripdata_2020-04.csv <br>
c. green_tripdata_04_2020.csv <br>
d. green_tripdata_2020.csv <br>

# Answer

1. Run Kestra di Docker dengan file docker-compose.yaml
2. Import file yaml 04_postgres_taxi.yaml ke Kestra
3. Execute file yaml tersebut dengan input sebagai berikut
   <img width="1603" height="765" alt="image" src="https://github.com/user-attachments/assets/cbee5c3b-655a-4453-b9cf-eda94135df15" />
4. Setelah selesai tereksekusi, pilih tab Output > tasks: Extract > Outputs : outputFiles
   maka, akan terlihat gambar berikut
   <img width="905" height="444" alt="image" src="https://github.com/user-attachments/assets/79e9a541-5527-41bd-91d2-4d02dea54c6c" />
 5. Maka, jawabannya adalah <b> (b) green_tripdata_2020-04.csv </b>
