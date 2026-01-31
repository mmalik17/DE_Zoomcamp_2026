# Question 5
How many rows are there for the Yellow Taxi data for the March 2021 CSV file? (1 point) <br>
a. 1,428,092 <br> 
b. 706,911 <br>
c. 1,925,152 <br>
d. 2,561,031 <br>

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

Then, we can execute by using this input: <br>
 <br>
<p align="center">
<img width="655" height="383" alt="image" src="https://github.com/user-attachments/assets/8b7a29fa-e9b8-41eb-a5e3-0117df30a849" /></p>
<br>

After execute, go to metrics tab, and you will see the number of rows <br>
 <br>
<p align="center">
<img width="659" height="287" alt="image" src="https://github.com/user-attachments/assets/6d2b2443-0e62-4a90-aa79-bcd99a8471a8" /></p>
<br>

From image above, we can conclude that the table has <b> 1,925,152 rows (c) </b>
