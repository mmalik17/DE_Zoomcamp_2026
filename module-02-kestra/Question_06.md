# Question 6
How would you configure the timezone to New York in a Schedule trigger? (1 point)
a. Add a timezone property set to EST in the Schedule trigger configuration
b. Add a timezone property set to America/New_York in the Schedule trigger configuration
c. Add a timezone property set to UTC-5 in the Schedule trigger configuration
d. Add a location property set to New_York in the Schedule trigger configuration

# Answer :
To answer this, i just look at the documentation link here: 
https://kestra.io/docs/workflow-components/triggers/schedule-trigger

The page give the example as below:

```yaml
triggers:
  - id: daily
    type: io.kestra.plugin.core.trigger.Schedule
    cron: "@daily"
    timezone: America/New_York
```
so, it is clear that <b> the answer is (b) Add a timezone property set to America/New_York in the Schedule trigger configuration </b>
