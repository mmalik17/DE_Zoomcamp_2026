# QUESTION 2
Given the docker-compose.yaml, what is the hostname and port that pgadmin should use to connect to the postgres database? (1 point)
<br>
a. postgres:5433 <br>
b. localhost:5432 <br>
c. db:5433 <br>
d. postgres:5432 <br>
e. db:5432 <br>

### Answer :
If the docker-compose.yaml looks like this :
````bash
...
image: postgres:18
    environment:
      POSTGRES_USER: "root"
      POSTGRES_PASSWORD: "root"
      POSTGRES_DB: "ny_taxi"
    volumes:
      - "ny_taxi_postgres_data:/var/lib/postgresql"
    ports:
      - "5432:5432"
...
````
<br>
then the host is localhost, and the port is 5432 so <b>the answer is localhost:5432 (b)</b>
