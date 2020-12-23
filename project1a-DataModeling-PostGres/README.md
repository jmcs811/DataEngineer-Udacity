**Introduction**
A startup called  **Sparkify**  want to analyze the data they have been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to.

The aim is to create a Postgres Database Schema and ETL pipeline to optimize queries for song play analysis.

**Project Description**
In this project, I have to model data with Postgres and build and ETL pipeline using Python. On the database side, I have to define fact and dimension tables for a Star Schema for a specific focus. On the other hand, ETL pipeline would transfer data from files located in two local directories into these tables in Postgres using Python and SQL

**Schema for Song Play Analysis**
| Fact Table | Dimension Tables  |
|--|--|
| song plays |Users
| |Songs
| | Artists
| | Time


**songplays**: records in log data associated with song plays
**users**: in the app
**songs**: in music database
**artists**: in music database
**time:**: timestamps of records in songplays broken down into specific units

**Project Design**
Database Design is very simple. With only a few tables we can get the information with a simple join.

ETL Design is also simplified. We only have to parse json files and then store into the correct table with the correct formatting. 

**Running the script**
First run the *create_tables.py* script. This will set up the tables needed for the ETL script. Then you can run *etl.py* script. This will parse the data and store the information into the relavent tabels. Finally, you can run *test.ipynb* to look at the data in the tables. 