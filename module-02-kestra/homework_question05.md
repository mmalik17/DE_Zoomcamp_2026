# Question 5
How many rows are there for the Yellow Taxi data for the March 2021 CSV file? (1 point)
a. 1,428,092
b. 706,911
c. 1,925,152
d. 2,561,031

# Answer
For fetching the data for year 2021, we need to modify a little bit of the 04_postgres_taxi.yaml file to add 2021 year input

Before:
```yaml
  - id: year
    type: SELECT
    displayName: Select year
    values: ["2019", "2020"]
    defaults: "2019"
```
After:
```yaml
  - id: year
    type: SELECT
    displayName: Select year
    values: ["2019", "2020","2021"]
    defaults: "2019"
```

Then, we can execute by using this input:
<img width="1555" height="883" alt="image" src="https://github.com/user-attachments/assets/8b7a29fa-e9b8-41eb-a5e3-0117df30a849" />

OUTPUT :
<img width="1502" height="648" alt="image" src="https://github.com/user-attachments/assets/76380f6a-76b3-449c-bca9-dde05a143782" />
