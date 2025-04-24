#  Advanced SQL Baseball Analysis
This project performs advanced SQL analysis on a baseball-related dataset using MySQL. The analysis is divided into four main sections: School Analysis, Salary Analysis, Player Career Analysis, and Player Comparison Analysis.

Database
Before running the queries, connect to the database:

sql
Copy
Edit

USE advanced_sql_baseball_analysis;

PART I: School Analysis
Explore the educational background of players and the influence of different schools over time.

Tasks:
View schools and school_details tables.

Count schools producing players by decade using numeric functions.

Identify the top 5 schools producing the most players (JOINs).

For each decade, list the top 3 schools by number of players using ROW_NUMBER() window function.

PART II: Salary Analysis
Evaluate team spending patterns and their financial strategies.

Tasks:
View the salaries table.

Identify the top 20% of teams by average annual spending (NTILE window function).

Show cumulative team spending over the years (Rolling SUM).

Find the first year each team's cumulative salary surpassed $1 billion.

PART III: Player Career Analysis
Delve into player careers — ages, team affiliations, and career spans.

Tasks:
View and count entries in the players table.

Calculate players’ starting age, ending age, and career length.

Determine starting and ending teams for each player using JOINs.

Identify players who played over 10 years and stayed on the same team.

PART IV: Player Comparison Analysis
Perform comparative analysis between players based on birthdays, batting stats, and physical attributes.

Tasks:
View the players table.

Find players sharing the same birthday using GROUP_CONCAT (string aggregation).

Show batting preferences (Right, Left, Both) per team — includes a more accurate approach using DISTINCT.

Analyze changes in average height and weight at debut over decades using LAG() window functions.

SQL Features Used
Window Functions: ROW_NUMBER, NTILE, LAG, SUM OVER

Joins: INNER JOIN, LEFT JOIN

Datetime Functions: TIMESTAMPDIFF, CAST, CONCAT

Aggregations: COUNT, AVG, SUM, GROUP BY

String Functions: GROUP_CONCAT, CONCAT

CTEs (Common Table Expressions): For step-wise query structuring

Compatibility Notes
This project is written for MySQL, but comments are included throughout with alternatives for:

PostgreSQL

SQL Server

Oracle

SQLite

Dataset Sources
This project assumes the presence of a database with the following key tables:

1. players

2. salaries

3. schools

4. school_details

These tables are commonly available in publicly shared baseball datasets like the Lahman Baseball Database.

How to Run
Connect to your MySQL database.

Run the queries in the order provided for each section.

Analyze results using your SQL client or export as needed.

License
This project is open-source and free to use under the MIT License.
