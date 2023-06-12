# EXP 07 - CREATE A PROGRAM IN AGGREGATE FUNCTION IN SQL

## AIM:

To create asql program in aggregate function in SUM(),COUNT(),AVG() OPERATIONS.

## ALGORITHM:

1) Initialize the accumulator variable(s) based on the type of aggregate functioN
2) Retrieve the data from the table or source based on the query's filtering conditions, if any.
3) Iterate over the retrieved data.
4) For each row:
      * Update the accumulator variable(s) based on the type of aggregate function
          * For SUM(): Add the value of the selected column to the sum variable.
          * For COUNT(): Increment the count variable by one.
          * For AVG(): Add the value of the selected column to the sum variable and increment the count variable by one.
5) After iterating over all the row
6) Display or use the result of the aggregate function as needed.

## PROGRAM:

```java

-- Create the table
CREATE TABLE Worker (
  WORKER_ID INT NOT NULL PRIMARY KEY,
  FIRST_NAME CHAR(25),
  LAST_NAME CHAR(25),
  SALARY INT(15),
  JOINING_DATE DATETIME,
  DEPARTMENT CHAR(25)
);

-- Insert values into the table
INSERT INTO Worker (WORKER_ID, FIRST_NAME, LAST_NAME, SALARY, JOINING_DATE, DEPARTMENT)
VALUES
  (1, 'Monika', 'Arora', 100000, '2020-02-14 09:00:00', 'HR'),
  (2, 'Niharika', 'Verma', 80000, '2021-06-11 09:00:00', 'Admin'),
  (3, 'Vishal', 'Singhal', 300000, '2020-02-14 09:00:00', 'HR'),
  (4, 'Amitabh', 'Singh', 500000, '2020-02-14 09:00:00', 'Admin'),
  (5, 'Vivek', 'Bhati', 500000, '2021-06-11 09:00:00', 'Admin'),
  (6, 'Vipul', 'Diwan', 200000, '2021-06-11 09:00:00', 'Account'),
  (7, 'Satish', 'Kumar', 75000, '2020-01-20 09:00:00', 'Account'),
  (8, 'Geetika', 'Chauhan', 90000, '2021-04-11 09:00:00', 'Admin');

-- Display the table
SELECT * FROM Worker;

-- Perform the SUM(), COUNT(), and AVG() operations
SELECT SUM(SALARY) AS sum_of_total_salary FROM Worker;
SELECT COUNT(*) AS count_of_total_workers FROM Worker;
SELECT AVG(SALARY) AS average_salary FROM Worker;
```
## OUTPUT:

### TABLE FOR WORKERS:

<img width="532" alt="dbms e7 1" src="https://github.com/divvisha/AGGREGATIVE-FUNCTION/assets/127508123/512ea0f7-f49c-4330-9230-0da3c7a5e3d8">

### SUM(),COUNT(),AVG():

![image](https://github.com/divvisha/AGGREGATIVE-FUNCTION/assets/127508123/26a79afe-2e12-42bb-9311-899523d94335)

## RESULT:

Thus we have successfully obtained the required result using the above-given code.
