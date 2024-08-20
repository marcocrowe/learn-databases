
# Databases for Project - COMP06043 - Winter 2022 - Paper

**MODULE:**    COMP06056 - Databases for Project**

**PROGRAMME(S):**  

LC_KISYM_KMY  Bachelor of Science (Honours) Internet Systems Development
LC_KISYM_JMY  Bachelor of Science Internet Systems Development

**YEAR OF STUDY:**  2

**EXAMINER(S):**  

Carol Rainsford  (Internal) Dr. Stephen Sheridan  (External)

**TIME ALLOWED:**    2 HOURS

**INSTRUCTIONS:    Answer 4 questions. All questions carry equal marks.

**PLEASE DO NOT TURN OVER THIS PAGE UNTIL YOU ARE INSTRUCTED TO DO SO.** The use of programmable or text storing calculators is expressly forbidden.

Please note that where a candidate answers more than the required number of questions, the examiner will mark all questions attempted and then select the highest scoring ones.

***There are no additional requirements for this paper.***

## Question 1 - Database Definitions [Total Marks: 25]

### Question 1.A (16 Marks)

**Define** what is meant by the following and provide **examples** to illustrate your  definition:

1. Relation
2. Tuple
3. Degree
4. Cardinality

### Question 1.B (4 Marks)

Define  what  is  meant  by  the  Referential  Integrity  Rule  in  relation  to  relational databases.  

### Question 1.C (5 Marks)

An important concept in Normalisation is functional dependency. Define what is meant by functional dependency. Illustrate your answer with an example.

## Question 2 - Relational Keys [Total Marks: 25]

### Question 2.A (4 Marks)

Define **TWO** (2) properties of a Candidate Key.  

### Question 2.B (4 Marks)

When selecting a primary key, outline **four** (4) considerations you would consider when making your decision.  

### Question 2.C (17 Marks)

Given the **PatientAppointment** relation and business rules below outline the following relational keys for each of the tables. Should a key not exist write NONE. Number each of the relational keys.

1. Super-keys
2. Candidate Keys
3. Primary Keys
4. Alternate Keys

**Relation: PatientAppointment**  

| AppointmentNo | PatientID | DateOfApp  | TimeOfApp | Doctor        |
|---------------|-----------|------------|-----------|---------------|
| 1             | 3         | 01/12/2022 | 11:00     | Mark Twain    |
| 2             | 2         | 01/12/2022 | 11:00     | Harry O'Brien |
| 3             | 1         | 02/12/2022 | 09:00     | Harry O'Brien |
| 4             | 2         | 02/12/2022 | 09:30     | Harry O'Brien |
| 5             | 1         | 02/12/2022 | 16:00     | Harry O'Brien |

**Business Rules:**  

1. Each appointment is allocated a new appointment number (appointmentNo).
2. Many patients can make appointments for the same date and same time.
3. A patient can make many appointments for the same day at different times.

## Question 3 - Entity Relationship Modelling [Total Marks: 25]

**Read the following case study carefully.**  

Manufacturers have a name, which we may assume is unique, an address, and a phone number. Products have a model number and a type (e.g., television set). Each product is made by one manufacturer, and different manufacturers may have different products  with  the  same  model  number.  However,  you  may  assume  that  no manufacturer would have two products with the same model number. Customers are identified by their unique social security number. They have email addresses, and physical addresses. Several customers may live at the same (physical) address, but we assume that no two customers have the same email address. An order has a unique order number, and a date. An order is placed by one customer. A customers can place many orders.  For each order, there are one or more products ordered, each line is identified by an orderDetailNo. Many orders can have many products ordered on it. There is a quantity for each product on the order.

### Question 3(a)  [5 Marks]

Clearly identify the entities described in the above Case Study.

### Question 3(b)  [10 Marks]

Identify potential attributes and the primary key attribute(s) associated with each entity identified in (a) above.

### Question 3(c)  [10 Marks]

Draw a single Entity Relationship Diagram to represent the above case study. Remove many to many relationships.

## Question 4 - Normalisation [Total Marks: 25]

The table found in below contains information in unNormalised form.  It outlines the details of Employees, the department they work in and the job that they are working on.  

*UNF table*  

| Employee Code | Last Name | Education Code | Education Description  | Year Earned | Department Code | Department Name | Job Class | Job  Title   | Birth Date | Hire Date  | Salary  |
|:--------------|:----------|:---------------|:-----------------------|:------------|:----------------|:----------------|:----------|--------------|------------|------------|---------|
| 1003          | Rainsford | SC             | Secondary School       | 1982        | MKTG            | Marketing       | 23        | Sales Agent  | 20/03/1970 | 14/09/2003 | 165,000 |
|               |           | BBA            | Bachelor of Business   | 1988        |                 |                 |           |              |            |            |         |
|               |           | MBA            | Masters Business       | 1993        |                 |                 |           |              |            |            |         |
|               |           |                |                        |             |                 |                 |           |              |            |            |         |
| 1006          | Smith     | SC             | Secondary School       | 1972        | MIS             | Info Systems    | 27        | Sys. Analyst | 13/12/1990 | 12/01/2002 | 95,000  |
|               |           | BSComp         | Bachelor of  Computing | 1976        |                 |                 |           |              |            |            |         |
|               |           | BEd            | Bachelor of  Education | 1997        |                 |                 |           |              |            |            |         |
|               |           |                |                        |             |                 |                 |           |              |            |            |         |
| 1010          | Thompson  | SC             | Secondary School       | 1982        | MKTG            | Marketing       | 23        | Sales Agent  | 19/06/2000 | 12/04/2005 | 76,000  |
|               |           | Bed            | Bachelor of  Education | 1988        |                 |                 |           |              |            |            |         |

**Examine** the table found in Appendix A and **perform** the following:  

1. Normalise the Relation found above using 1st, 2nd and 3rd normal form rules.  Clearly illustrate the Relations(s) and data in 1st, 2nd and 3rd normal form. **(17 Marks)**
2. Identify the primary key attribute(s) at each stage of normalization. **(5 Marks)**
3. Identify potential names for new tables. Names should reflect the content in each relation. **(3 Marks)**

## Answer 4

**First Normal Form (1NF)**  

To achieve 1NF, we ensure that each field contains only atomic (indivisible) values. In your UNF table, you have handled this correctly by listing each employee’s educational details in separate rows.

Here is the correct 1NF table (same as your UNF table):

An example of an un-atomic value would be if you had a single field for the employee’s full name, e.g. "John Doe". This would need to be split into two fields, one for the first name and one for the last name.

| Employee Code | Last Name | Education Code | Education Description  | Year Earned | Department Code | Department Name | Job Class | Job  Title   | Birth Date | Hire Date  |  Salary |
|:--------------|:----------|:---------------|:-----------------------|------------:|:----------------|:----------------|:----------|--------------|------------|------------|--------:|
| 1003          | Rainsford | SC             | Secondary School       |        1982 | MKTG            | Marketing       | 23        | Sales Agent  | 20/03/1970 | 14/09/2003 | 165,000 |
| 1003          | Rainsford | BBA            | Bachelor of Business   |        1988 | MKTG            | Marketing       | 23        | Sales Agent  | 20/03/1970 | 14/09/2003 | 165,000 |
| 1003          | Rainsford | MBA            | Masters Business       |        1993 | MKTG            | Marketing       | 23        | Sales Agent  | 20/03/1970 | 14/09/2003 | 165,000 |
| 1006          | Smith     | SC             | Secondary School       |        1972 | MIS             | Info Systems    | 27        | Sys. Analyst | 13/12/1990 | 12/01/2002 |  95,000 |
| 1006          | Smith     | BSComp         | Bachelor of  Computing |        1976 | MIS             | Info Systems    | 27        | Sys. Analyst | 13/12/1990 | 12/01/2002 |  95,000 |
| 1006          | Smith     | BEd            | Bachelor of  Education |        1997 | MIS             | Info Systems    | 27        | Sys. Analyst | 13/12/1990 | 12/01/2002 |  95,000 |
| 1010          | Thompson  | SC             | Secondary School       |        1982 | MKTG            | Marketing       | 23        | Sales Agent  | 19/06/2000 | 12/04/2005 |  76,000 |
| 1010          | Thompson  | Bed            | Bachelor of  Education |        1988 | MKTG            | Marketing       | 23        | Sales Agent  | 19/06/2000 | 12/04/2005 |  76,000 |

**Second Normal Form (2NF)**  

To find first normal form, we need to remove the repeating groups and create a separate table for the repeating groups.

Sorted the columns in the table to make it easier to identify the functional dependencies.

`UNF table`  

| Employee Code | Last Name | Department Code | Department Name | Job Class | Job Title    | Birth Date | Hire Date  |  Salary | Education Code | Education Description | Year Earned |
|---------------|-----------|-----------------|-----------------|-----------|--------------|------------|------------|--------:|----------------|-----------------------|------------:|
| 1003          | Rainsford | MKTG            | Marketing       | 23        | Sales Agent  | 20/03/1970 | 14/09/2003 | 165,000 | SC             | Secondary School      |        1982 |
| 1003          | Rainsford | MKTG            | Marketing       | 23        | Sales Agent  | 20/03/1970 | 14/09/2003 | 165,000 | BBA            | Bachelor of Business  |        1988 |
| 1003          | Rainsford | MKTG            | Marketing       | 23        | Sales Agent  | 20/03/1970 | 14/09/2003 | 165,000 | MBA            | Masters Business      |        1993 |
| 1006          | Smith     | MIS             | Info Systems    | 27        | Sys. Analyst | 13/12/1990 | 12/01/2002 |  95,000 | SC             | Secondary School      |        1972 |
| 1006          | Smith     | MIS             | Info Systems    | 27        | Sys. Analyst | 13/12/1990 | 12/01/2002 |  95,000 | BSComp         | Bachelor of Computing |        1976 |
| 1006          | Smith     | MIS             | Info Systems    | 27        | Sys. Analyst | 13/12/1990 | 12/01/2002 |  95,000 | BEd            | Bachelor of Education |        1997 |
| 1010          | Thompson  | MKTG            | Marketing       | 23        | Sales Agent  | 19/06/2000 | 12/04/2005 |  76,000 | SC             | Secondary School      |        1982 |
| 1010          | Thompson  | MKTG            | Marketing       | 23        | Sales Agent  | 19/06/2000 | 12/04/2005 |  76,000 | Bed            | Bachelor of Education |        1988 |

**Breaking the UNF table into sub tables**  

`Employee_v1` Table

| Employee Code | Last Name | Department Code | Department Name | Job Class | Job Title    | Birth Date | Hire Date  |  Salary |
|---------------|-----------|-----------------|-----------------|-----------|--------------|------------|------------|--------:|
| 1003          | Rainsford | MKTG            | Marketing       | 23        | Sales Agent  | 20/03/1970 | 14/09/2003 | 165,000 |
| 1006          | Smith     | MIS             | Info Systems    | 27        | Sys. Analyst | 13/12/1990 | 12/01/2002 |  95,000 |
| 1010          | Thompson  | MKTG            | Marketing       | 23        | Sales Agent  | 19/06/2000 | 12/04/2005 |  76,000 |

For the `Employee_v1` table:

- The candidate key is `Employee Code`.
- `Employee Code` -> `Last Name`, `Department Code`, `Department Name`, `Job Class`, `Job Title`, `Birth Date`, `Hire Date`, `Salary`
- The table is in 1NF, as all the columns contain atomic values.
- The table is not in 2NF, as there are partial dependencies on the candidate key.
  - `Employee Code` -> `Last Name`, `Birth Date`, `Hire Date`, `Salary`
  - `Department Code` -> `Department Name`
  - `Job Class` -> `Job Title` (Assuming based on Column names)

`Education_v1` Table

| Employee Code | Education Code | Education Description | Year Earned |
|---------------|----------------|-----------------------|------------:|
| 1003          | SC             | Secondary School      |        1982 |
| 1003          | BBA            | Bachelor of Business  |        1988 |
| 1003          | MBA            | Masters Business      |        1993 |
| 1006          | SC             | Secondary School      |        1972 |
| 1006          | BSComp         | Bachelor of Computing |        1976 |
| 1006          | BEd            | Bachelor of Education |        1997 |
| 1010          | SC             | Secondary School      |        1982 |
| 1010          | Bed            | Bachelor of Education |        1988 |

For the `Education_v1` table:

- The candidate key is the combination of `Employee Code` and `Education Code`.
- (`Employee Code`, `Education Code`) -> `Education Description`, `Year Earned`
- The table is in 1NF, as there are no repeating groups.
- The table is in 2NF, as there are no partial dependencies.
- The table is in 3NF, as there are no transitive dependencies.

Breaking the table `Employee_v1`

`Employee_v2` Table

| Employee Code | Last Name | Birth Date | Hire Date  |  Salary | Department Code | Job Class |
|---------------|-----------|------------|------------|--------:|-----------------|----------:|
| 1003          | Rainsford | 20/03/1970 | 14/09/2003 | 165,000 | MKTG            |        23 |
| 1006          | Smith     | 13/12/1990 | 12/01/2002 |  95,000 | MIS             |        27 |
| 1010          | Thompson  | 19/06/2000 | 12/04/2005 |  76,000 | MKTG            |        23 |

For the `Employee_v2` table:

- The candidate key is `Employee Code`.
- `Employee Code` -> `Last Name`, `Birth Date`, `Hire Date`, `Salary`, `Department Code`, `Job Class`
- `Department Code` and `Job Class` are foreign keys to the `Department_v1` and `Job_v1` tables, respectively.
- The table is in 1NF, as all the columns contain atomic values and there are no repeating groups.
- The table is in 2NF, as there are no partial dependencies on the candidate key.
- The table is in 3NF, as there are no transitive dependencies.

`Department_v1` Table

| Department Code | Department Name |
|-----------------|-----------------|
| MKTG            | Marketing       |
| MIS             | Info Systems    |

For the `Department_v1` table:

- The candidate key is `Department Code`.
- `Department Code` -> `Department Name`
- The table is in 1NF, as all the columns contain atomic values and there are no repeating groups.
- The table is in 2NF, as there are no partial dependencies on the candidate key.
- The table is in 3NF, as there are no transitive dependencies.

`Job_v1` Table

| Job Class | Job Title    |
|-----------|--------------|
| 23        | Sales Agent  |
| 27        | Sys. Analyst |

For the `Job_v1` table:

- The candidate key is `Job Class`.
- `Job Class` -> `Job Title`
- The table is in 1NF, as all the columns contain atomic values and there are no repeating groups.
- The table is in 2NF, as there are no partial dependencies on the candidate key.
- The table is in 3NF, as there are no transitive dependencies.

The Final Normalized Tables are:

- `Employee_v2` Table
- `Education_v1` Table
- `Department_v1` Table
- `Job_v1` Table

## Question 5 - Structured Query Language [Total Marks: 25]

The database relations found in Appendix B are for a simple garden kept by a small family. They plant their garden in the spring and pick their garden in summer. Details of each attribute and a description of each table can be found in Appendix B. Using the relations found in Appendix B perform the following:

### Question 5.A (3 Marks)

Write an SQL command that would recreate the LOCATION table found in Appendix B.

### Answer 5.A

```sql
CREATE TABLE `Location` (
  `LocationId` Int Not Null,
  `Name` VarChar(50) Not Null,
  `Sunlight` Decimal(3,2) Not Null,
  `Water` Decimal(3,2) Not Null,
  Primary Key (`LocationId`),
  Unique Key `Name` (`Name`)
);
```

### Question 5.B (3 Marks)

Write a SQL statement to add an onion plant to the PLANT table. Values for the attributes are as follows:

| Column     | Value |
|------------|-------|
| `PlantID`  | 5     |
| `Name`     | Onion |
| `Sunlight` | 0.45  |
| `Water`    | 0.74  |

### Answer 5.B

```sql
INSERT INTO `Plant` (`PlantId`, `Name`, `Sunlight`, `Water`) 
VALUES (5, 'Onion', 0.45, 0.74);
```

### Question 5.C (3 Marks)

Write a valid SQL  statement  that  calculates  the  total  weight  of  all  ears of  corn (PlantID=2) that were picked from the garden:

### Answer 5.C

```sql
SELECT 
    SUM(`Weight` * `Amount`) AS `Total Weight`
FROM 
    `Picked`
WHERE
    `PlantId` = 2;
```

### Question 5.D (3 Marks)

Write a valid SQL statement that shows for each plant picked the Plant name and picked weight in pounds. Using multiplicative conversion factor of 2.2 to convert kilograms to pounds

### Answer 5.D

```sql
SELECT 
    `Plant`.`Name` AS `Plant Name`,
    SUM(`Picked`.`Weight`) * 2.2 AS `Picked Weight (lbs)`
FROM
    `Plant`
INNER JOIN
    `Picked` ON `Plant`.`PlantId` = `Picked`.`PlantId`
GROUP BY
    `Plant`.`Name`;
```

### Question 5.E (4 Marks)

Write a valid SQL statement that would produce a list of vegetables picked by a particular gardener (gardenerID =2), the date picked, and amount picked. The result should output the following:

| GardenerName | PlantName | Date       | Amount |
|--------------|-----------|------------|--------|
| Tim          | Radish    | 2005-07-16 | 23     |
| Tim          | Carrot    | 2005-08-18 | 28     |
| Tim          | Corn      | 2005-08-28 | 18     |

```sql
SELECT 
    G.`Name` AS `GardenerName`,
    PL.`Name` AS `PlantName`,
    P.`Date` AS `Date`,
    P.`Amount` AS `Amount`
FROM
    `Gardener` G
INNER JOIN
    `Picked` P ON G.`GardenerId` = P.`GardenerId`
INNER JOIN
    `Plant` PL ON P.`PlantId` = PL.`PlantId`
WHERE
    G.`GardenerId` = 2;
```

### Question 5.F (4 Marks)

Write a valid SQL statement that would produce a result set which would include the plant name, location name, the amount of water the plant needs (needed), the water available in a location (available) and variance which is the difference between location water and plant water for the plant Carrot. The output should look like the following:

| **PlantName** | **LocationName** | **Needed** | **Available** | **variance** |
|---------------|------------------|------------|---------------|--------------|
| Carrot        | East             | 0\.82      | 0\.8          | -0.02        |
| Carrot        | West             | 0\.82      | 0\.48         | -0.34        |
| Carrot        | North            | 0\.82      | 0\.84         | 0\.02        |
| Carrot        | South            | 0\.82      | 0\.66         | -0.16        |

### Answer 5.F

```sql
SELECT 
    PL.`Name` AS `PlantName`,
    L.`Name` AS `LocationName`,
    PL.`Water` AS `Needed`,
    L.`Water` AS `Available`,
    PL.`Water` - L.`Water` AS `variance`
FROM
    `Plant` PL
INNER JOIN
    `Location` L ON PL.`LocationId` = L.`LocationId`
WHERE
    PL.`Name` = 'Carrot';
```

### Question 5.G (5 Marks)

Write a valid SQL statement that calculates the average number of items produced per seed planted for each plant type:

```sql
SELECT 
    PL.`Name` AS `PlantName`,
    SUM(`Amount`) / SUM(`Seeds`) AS `AvgItemsPerSeed`
FROM
    `Planted` P
INNER JOIN
    `Plant` PL ON P.`PlantId` = PL.`PlantId`
GROUP BY
    PL.`Name`;
```

## Appendix A

This UNF table refers to question 4 of your exam paper.  

| **Employee Code** | **Last Name** | **Education Code** | **Education Description** | **Year Earned** | **Department Code** | **Department Name** | **Job Class** | **Job  Title** | **Birth Date** | **Hire Date** | **Salary** |
|:------------------|:--------------|:-------------------|:--------------------------|:----------------|:--------------------|:--------------------|:--------------|----------------|----------------|---------------|------------|
| 1003              | Rainsford     | SC                 | Secondary School          | 1982            | MKTG                | Marketing           | 23            | Sales Agent    | 20/03/1970     | 14/09/2003    | 165,000    |
|                   |               | BBA                | Bachelor of Business      | 1988            |                     |                     |               |                |                |               |            |
|                   |               | MBA                | Masters Business          | 1993            |                     |                     |               |                |                |               |            |
|                   |               |                    |                           |                 |                     |                     |               |                |                |               |            |
| 1006              | Smith         | SC                 | Secondary School          | 1972            | MIS                 | Info Systems        | 27            | Sys. Analyst   | 13/12/1990     | 12/01/2002    | 95,000     |
|                   |               | BSComp             | Bachelor of  Computing    | 1976            |                     |                     |               |                |                |               |            |
|                   |               | BEd                | Bachelor of  Education    | 1997            |                     |                     |               |                |                |               |            |
|                   |               |                    |                           |                 |                     |                     |               |                |                |               |            |
| 1010              | Thompson      | SC                 | Secondary School          | 1982            | MKTG                | Marketing           | 23            | Sales Agent    | 19/06/2000     | 12/04/2005    | 76,000     |
|                   |               | Bed                | Bachelor of  Education    | 1988            |                     |                     |               |                |                |               |            |

## Appendix B

These relations refer to question 5 of your exam paper.

**Relation: GARDENER**  

The Gardener relation outlines the details of each gardener in the family.  

| **GardenerID** | **Name** | **Age** |
|----------------|----------|---------|
| 0              | Mother   | 36      |
| 1              | Father   | 38      |
| 2              | Tim      | 15      |
| 3              | Erin     | 12      |

**Relation: PLANT**  

The Plant relation outlines the details of each plant their sunlight, weight, and water requirements. The sunlight attribute refers to the optimal amount of sunshine required for a plant. **The water attribute refers to the optimal amount of water required for a plant.**

| **PlantID** | **Name** | **Sunlight** | **Water** | **Weight** |
|-------------|----------|--------------|-----------|------------|
| 0           | Carrot   | 0\.26        | 0\.82     | 0\.08      |
| 1           | Beet     | 0\.44        | 0\.80     | 0\.04      |
| 2           | Corn     | 0\.44        | 0\.76     | 0\.26      |
| 3           | Tomato   | 0\.42        | 0\.80     | 0\.16      |
| 4           | Radish   | 0\.28        | 0\.84     | 0\.02      |

**Relation: LOCATION**  

The Location relation outlines details of each location in the garden and the sunlight attribute refers to the percentage of a 24-hour day that the location gets sunlight. The water attribute refers to the percentage of average rainfall that makes it to the root level for a location

| **LocationID** | **Name** | **Sunlight** | **Water** |
|----------------|----------|--------------|-----------|
| 0              | East     | 0\.28        | 0\.80     |
| 1              | North    | 0\.17        | 0\.84     |
| 2              | West     | 0\.38        | 0\.48     |
| 3              | South    | 0\.45        | 0\.66     |

**Relation: PLANTED**  

The Planted relation outlines details of each plant, planted by a gardener in a specific location on a specific date and the number of seeds planted.  

| **PlantID** | **GardenerID** | **LocationID** | **Date**   | **Seeds** |
|-------------|----------------|----------------|------------|-----------|
| 0           | 0              | 0              | 04-18-2005 | 28        |
| 0           | 1              | 1              | 04-14-2005 | 14        |
| 1           | 0              | 2              | 04-18-2005 | 36        |
| 2           | 1              | 3              | 04-14-2005 | 20        |
| 2           | 2              | 2              | 04-19-2005 | 12        |
| 3           | 3              | 3              | 04-25-2005 | 38        |
| 4           | 2              | 0              | 04-30-2005 | 30        |

- PlantID is a Foreign Key references the PlantID in the Plant Relation
- GardenerID is a Foreign Key references the GardenerID in the Gardener Relation
- LocationID is a Foreign Key references the LocationID in the Location Relation

**Relation: PICKED**  

The Picked relation outlines details of each plant picked by a gardener in a specific location on a specific date. The picked amount is the number of items (one carrot, one beet, an ear of corn, one tomato, one radish) picked. The weight is the total weight of the picking.

| **PlantID** | **GardenerID** | **LocationID** | **Date**   | **Amount** | **Weight** |
|-------------|----------------|----------------|------------|------------|------------|
| 0           | 2              | 0              | 08-18-2005 | 28         | 2\.32      |
| 0           | 3              | 1              | 08-16-2005 | 12         | 1\.02      |
| 2           | 1              | 3              | 08-22-2005 | 52         | 12\.96     |
| 2           | 2              | 2              | 08-28-2005 | 18         | 4\.58      |
| 3           | 3              | 3              | 08-22-2005 | 15         | 3\.84      |
| 4           | 2              | 0              | 07-16-2005 | 23         | 0\.52      |

- PlantID is a Foreign Key references the PlantID in the Plant Relation
- GardenerID is a Foreign Key references the GardenerID in the Gardener Relation
- LocationID is a Foreign Key references the LocationID in the Location Relation

### Appendix B SQL Code

```sql
-- Create the database
CREATE DATABASE GardenDB;
USE GardenDB;

-- Create the Gardener table
CREATE TABLE Gardener (
    GardenerID INT PRIMARY KEY,
    Name VarChar(50),
    Age INT
);

-- Insert data into the Gardener table
INSERT INTO Gardener (GardenerID, Name, Age) VALUES
(0, 'Mother', 36),
(1, 'Father', 38),
(2, 'Tim', 15),
(3, 'Erin', 12);

-- Create the Plant table
CREATE TABLE Plant (
    PlantID INT PRIMARY KEY,
    Name VarChar(50),
    Sunlight DECIMAL(4, 2),
    Water DECIMAL(4, 2),
    Weight DECIMAL(4, 2)
);

-- Insert data into the Plant table
INSERT INTO Plant (PlantID, Name, Sunlight, Water, Weight) VALUES
(0, 'Carrot', 0.26, 0.82, 0.08),
(1, 'Beet', 0.44, 0.80, 0.04),
(2, 'Corn', 0.44, 0.76, 0.26),
(3, 'Tomato', 0.42, 0.80, 0.16),
(4, 'Radish', 0.28, 0.84, 0.02);

-- Create the Location table
CREATE TABLE Location (
    LocationID INT PRIMARY KEY,
    Name VarChar(50),
    Sunlight DECIMAL(4, 2),
    Water DECIMAL(4, 2)
);

-- Insert data into the Location table
INSERT INTO Location (LocationID, Name, Sunlight, Water) VALUES
(0, 'East', 0.28, 0.80),
(1, 'North', 0.17, 0.84),
(2, 'West', 0.38, 0.48),
(3, 'South', 0.45, 0.66);

-- Create the Planted table
CREATE TABLE Planted (
    PlantID INT,
    GardenerID INT,
    LocationID INT,
    Date DATE,
    Seeds INT,
    PRIMARY KEY (PlantID, GardenerID, LocationID, Date),
    FOREIGN KEY (PlantID) REFERENCES Plant(PlantID),
    FOREIGN KEY (GardenerID) REFERENCES Gardener(GardenerID),
    FOREIGN KEY (LocationID) REFERENCES Location(LocationID)
);

-- Insert data into the Planted table
INSERT INTO Planted (PlantID, GardenerID, LocationID, Date, Seeds) VALUES
(0, 0, 0, '2005-04-18', 28),
(0, 1, 1, '2005-04-14', 14),
(1, 0, 2, '2005-04-18', 36),
(2, 1, 3, '2005-04-14', 20),
(2, 2, 2, '2005-04-19', 12),
(3, 3, 3, '2005-04-25', 38),
(4, 2, 0, '2005-04-30', 30);

-- Create the Picked table
CREATE TABLE Picked (
    PlantID INT,
    GardenerID INT,
    LocationID INT,
    Date DATE,
    Amount INT,
    Weight DECIMAL(4, 2),
    PRIMARY KEY (PlantID, GardenerID, LocationID, Date),
    FOREIGN KEY (PlantID) REFERENCES Plant(PlantID),
    FOREIGN KEY (GardenerID) REFERENCES Gardener(GardenerID),
    FOREIGN KEY (LocationID) REFERENCES Location(LocationID)
);

-- Insert data into the Picked table
INSERT INTO Picked (PlantID, GardenerID, LocationID, Date, Amount, Weight) VALUES
(0, 2, 0, '2005-08-18', 28, 2.32),
(0, 3, 1, '2005-08-16', 12, 1.02),
(2, 1, 3, '2005-08-22', 52, 12.96),
(2, 2, 2, '2005-08-28', 18, 4.58),
(3, 3, 3, '2005-08-22', 15, 3.84),
(4, 2, 0, '2005-07-16', 23, 0.52);
```

---
