## What was the problem? How to solve it?
[Homework link](https://github.com/DataTalksClub/data-engineering-zoomcamp/blob/main/cohorts/2023/week_1_docker_sql/homework.md)
Q3:
`select *
from green_tripdata201901
where lpep_dropoff_datetime BETWEEN '2019-01-15 00:00:00'::timestamp and '2019-01-16 00:00:00'::timestamp
AND lpep_pickup_datetime BETWEEN '2019-01-15 00:00:00'::timestamp and '2019-01-16 00:00:00'::timestamp;`


Q4:
`select *
from green_tripdata201901
where trip_distance =(select max(trip_distance) from green_tripdata201901);`

Q5:
`select count(*)
from green_tripdata201901
where passenger_count=2 and 
lpep_pickup_datetime >= '2019-01-01 00:00:00'::timestamp and lpep_pickup_datetime < '2019-01-02 00:00:00'::timestamp;`



`select count(*)
from green_tripdata201901
where passenger_count=3 
AND lpep_pickup_datetime BETWEEN '2019-01-01 00:00:00'::timestamp and '2019-01-02 00:00:00'::timestamp;`



