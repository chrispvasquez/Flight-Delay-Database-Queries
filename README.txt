Domain Application:

The application of our database system is as an analysis tool for airlines. Queries on the database allow an airline to examine 
flight patterns based on delays, perhaps allowing them to optimize troublesome routes or to investigate aircraft that may have frequent 
maintenance issues. By utilizing this database in such a way, airlines can save money spent for flight operations and can inform future 
business decisions to help avoid delays. This has the double-benefit of decreasing costs/increasing profits and becoming more reputable 
with the public for having more on-time flights versus competitors.



Database Design:

***airlines.txt***

| airline_id | airline_name |

> primary key is (airline_id)

***airports.txt***

| airport_iata | airport_name | city | state | country | lati | longi |

> primary key is (airport_iata)
- "iata" is a 3-letter unique identifier given to most airports (every airport in this list has one)

***flights.txt***

| year | month | day | week_day | airline_id | flight_num | tail_num | origin_iata | dest_iata | sched_dep_time | delay_dep | distance | sched_arr_time | delay_arr

> primary key is (year, month, day, tail_num, sched_dep_time)
- tail_num is the plane's "tail number" which is like its license plate, it is a unique identifier
- sched_dep_time is the scheduled departure time in 24-hr local time, with format: hhmm (0000 to 2359)



Database Creation:

The database was created with the data retrieved from the locations cited at the end of the report.
There are a total of ten queries that were created for the application that could assist an airline.
Note that all of the output samples contain the first five results, not the entire returned table.


Data Source: https://www.kaggle.com/usdot/flight-delays?select=airports.csv