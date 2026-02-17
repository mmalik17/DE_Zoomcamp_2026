# Question 2

Q2: New value 6 appears in payment_type. What happens on dbt test? (1 point) <br>

a. dbt skips the test <br>
b. dbt fails the test with non-zero exit code <br>
c. dbt passes with warning <br>
d. dbt updates the configuration <br>

# Answer

The schema.yaml has configured like this

```yaml
columns:
  - name: payment_type
    data_tests:
      - accepted_values:
          arguments:
            values: [1, 2, 3, 4, 5]
            quote: false
```

There are no number 6 in value array, so it will fail. The answer is (b)
