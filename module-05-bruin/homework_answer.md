# Question 1
Bruin Pipeline Structure In a Bruin project, what are the required files/directories? (1 point)
a. bruin.yml and assets/
b. .bruin.yml and pipeline.yml (assets can be anywhere)
c. .bruin.yml and pipeline/ with pipeline.yml and assets/
d. pipeline.yml and assets/ only

# Question 2 
Materialization Strategies You're building a pipeline that processes NYC taxi data organized by month based on pickup_datetime. Which incremental strategy is best for processing a specific interval period by deleting and inserting data for that time period? (1 point)
a. append - always add new rows
b. replace - truncate and rebuild entirely
c. time_interval - incremental based on a time column
d. view - create a virtual table only

# Question 3 
Pipeline VariablesYou have a variable defined in pipeline.yml:variables: taxi_types: type: array items: type: string default: ["yellow", "green"]How do you override this when running the pipeline to only process yellow taxis? (1 point)
a. bruin run --taxi-types yellow
b. bruin run --var taxi_types=yellow
c. bruin run --var 'taxi_types=["yellow"]'
d. bruin run --set taxi_types=["yellow"]

# Question 4 
Running with DependenciesYou've modified the ingestion/trips.py asset and want to run it plus all downstream assets. Which command should you use? (1 point)
a. bruin run ingestion.trips --all
b. bruin run ingestion/trips.py --downstream
c. bruin run pipeline/trips.py --recursive
d. bruin run --select ingestion.trips+

# Question 5
Quality Checks. You want to ensure the pickup_datetime column in your trips table never has NULL values. Which quality check should you add to your asset definition? (1 point)
a. name: unique
b. name: not_null
c. name: positive
d. name: accepted_values, value: [not_null]

# Question 6 
Lineage and DependenciesAfter building your pipeline, you want to visualize the dependency graph between assets. Which Bruin command should you use? (1 point)
a. bruin graph
b. bruin dependencies
c. bruin lineage
d. bruin show

# Question 7 
First-Time RunYou're running a Bruin pipeline for the first time on a new DuckDB database. What flag should you use to ensure tables are created from scratch? (1 point)
a. --create
b. --init
c. --full-refresh
d. --truncate

## Answer
To create an entire new pipeline, the most appropriate answer is using <b> --create </b> command, so the answer is (a)
