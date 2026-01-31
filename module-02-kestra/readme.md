# Repository for Zoomcamp Module 02 : Workflow Orchestration with Kestra

The homework question is based on this link : https://courses.datatalks.club/de-zoomcamp-2026/homework/hw2

The file in code directory is sourced from https://github.com/DataTalksClub/data-engineering-zoomcamp/tree/main/02-workflow-orchestration/flows
but with several modification <br>

The modifications are:
- at docker-compose.yaml, the port for Kestra is changed from localhost:8080 to localhost:8081, because  my local docker version claim port 8080 for backend proces so i can't use port 8080 for Kestra
- at 04_postgres_taxi.yaml, i add year "2021" as an input option
- at 05_postgres_taxi_scheduled.yaml. i modify the table name template and the cron schedule

   
