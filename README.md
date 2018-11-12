# python_project

November 12, 2018
Python coding test for perspective employer:

## Exercise 1:
Given an HTTP server access log with size greater than 100 GB, produce by-day rankings of:
- pages by unique hits
- pages by number of users
- users by unique page views

Assumptions: 
- HTTP Files are in ASC chronological order
- In a given HTTP access log, there are many more users than pages
- For this test, all log entries are considered reportabl (e.g., there is no regex screening for .json, .xml, .jpg files, etc)

Test file:
- Produced by random data generator to match example format (i.e., 'Path', 'User', 'Timestamp')
- 50 different page paths
- 1000 unique user IDs
- Date range for complete file is 1/1/2018 - 11/10/2018
- Complete test file is 800mb, 1,000,000 rows of data
- Sample file included contains 29,810 rows

Python code is in the included Jupyter Notebook.

The focus of the code was to parse a large (e.g., 100GB+) as efficiently as possible without having to load entire file into memory. I used the csv and pandas packages to add one line of the code into a pandas DataFrame, and then use pandas' groupby functionality to aggregate the findings.

## Exercise 2:
Included in this repository is the txt file with the SQL statements created to return the requested exercise questions, given the provided schema.
