# Question 1
Bruin Pipeline Structure. In a Bruin project, what are the required files/directories? (1 point) <br>
a. bruin.yml and assets/ <br>
b. .bruin.yml and pipeline.yml (assets can be anywhere) <br>
c. .bruin.yml and pipeline/ with pipeline.yml and assets/ <br>
d. pipeline.yml and assets/ only <br>

# Question 2 
Materialization Strategies. You're building a pipeline that processes NYC taxi data organized by month based on pickup_datetime. Which incremental strategy is best for processing a specific interval period by deleting and inserting data for that time period? (1 point) <br>
a. append - always add new rows <br>
b. replace - truncate and rebuild entirely <br>
c. time_interval - incremental based on a time column <br>
d. view - create a virtual table only <br>

# Question 3 
Pipeline Variables. You have a variable defined in pipeline.yml:variables: taxi_types: type: array items: type: string default: ["yellow", "green"]How do you override this when running the pipeline to only process yellow taxis? (1 point) <br>
a. bruin run --taxi-types yellow <br>
b. bruin run --var taxi_types=yellow <br>
c. bruin run --var 'taxi_types=["yellow"]' <br>
d. bruin run --set taxi_types=["yellow"] <br>

# Question 4 
Running with Dependencies. You've modified the ingestion/trips.py asset and want to run it plus all downstream assets. Which command should you use? (1 point) <br>
a. bruin run ingestion.trips --all <br>
b. bruin run ingestion/trips.py --downstream <br>
c. bruin run pipeline/trips.py --recursive <br>
d. bruin run --select ingestion.trips+ <br>

# Question 5
Quality Checks. You want to ensure the pickup_datetime column in your trips table never has NULL values. Which quality check should you add to your asset definition? (1 point) <br>
a. name: unique <br>
b. name: not_null <br>
c. name: positive <br>
d. name: accepted_values, value: [not_null] <br>

# Question 6 
Lineage and Dependencies.  After building your pipeline, you want to visualize the dependency graph between assets. Which Bruin command should you use? (1 point) <br>
a. bruin graph <br>
b. bruin dependencies <br>
c. bruin lineage <br>
d. bruin show <br>

# Question 7 
First-Time RunYou're running a Bruin pipeline for the first time on a new DuckDB database. What flag should you use to ensure tables are created from scratch? (1 point) <br>
a. --create <br>
b. --init <br>
c. --full-refresh <br>
d. --truncate <br>

## Answer
To create an entire new pipeline, the most appropriate answer is using <b> --full-refresh </b> command. --full-refresh will truncate and rebuild tables from scratch, so the answer is (c)
