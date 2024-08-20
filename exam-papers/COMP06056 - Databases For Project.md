![](Aspose.Words.43f634ad-516e-4c63-af02-a6ed8de3283d.001.png)

**TECHNOLOGICAL UNIVERSITY OF THE SHANNON: MIDLANDS MIDWEST *![](Aspose.Words.43f634ad-516e-4c63-af02-a6ed8de3283d.002.png)*WINTER** **EXAMINATIONS** **2022**

**MODULE:**    COMP06056 - Databases for Project** 

**PROGRAMME(S):**  

LC\_KISYM\_KMY  Bachelor of Science (Honours) Internet Systems 

Development 

LC\_KISYM\_JMY  Bachelor of Science Internet Systems Development **YEAR OF STUDY:**  2 

**EXAMINER(S):**  

Carol Rainsford  (Internal) Dr. Stephen Sheridan  (External) 

**TIME ALLOWED:**    2 HOURS 

**INSTRUCTIONS:    Answer 4 questions. All questions carry equal marks. ![](Aspose.Words.43f634ad-516e-4c63-af02-a6ed8de3283d.003.png)**

**PLEASE DO NOT TURN OVER THIS PAGE UNTIL YOU ARE INSTRUCTED TO DO SO.** The use of programmable or text storing calculators is expressly forbidden.

Please note that where a candidate answers more than the required number of questions, the examiner will mark all questions attempted and then select the highest scoring ones.![](Aspose.Words.43f634ad-516e-4c63-af02-a6ed8de3283d.004.png)

***There are no additional requirements for this paper.***

***QUESTION 1 – Database Definitions  [TOTAL MARKS: 25]* Q 1(a)  [16 Marks]** 

**Define** what is meant by the following and provide **examples** to illustrate your  definition: 

1) Relation 
1) Tuple 
1) Degree 
1) Cardinality 

**Q 1(b)  [4 Marks]** 

Define  what  is  meant  by  the  Referential  Integrity  Rule  in  relation  to  relational databases.  

**Q 1(c)  [5 Marks]** 

An important concept in Normalisation is functional dependency. Define what is meant by functional dependency. Illustrate your answer with an example. 

***[End of Question 1]*** 

***QUESTION 2  –  RELATIONAL KEYS  [TOTAL MARKS: 25]* Q 2(a)  [4 Marks]** 

Define **TWO** (2) properties of a Candidate Key.  

**Q 2(b)  [4 Marks]** 

When selecting a primary key, outline **four** (4) considerations you would consider when making your decision.  

**Q 2(c)  [17 Marks]** 

Given the **PatientAppointment** relation and business rules below outline the following relational keys for each of the tables. Should a key not exist write NONE. Number each of the relational keys. 

1) Superkeys 
1) Candidate Keys 
1) Primary Keys 
1) Alternate Keys 

**Relation: PatientAppointment**  



|**AppointmentNo** |**PatientID** |**DateofApp** |**TimeofApp** |**Doctor** |
| - | - | - | - | - |
|1 |3 |01/12/2022 |11:00 |Mark Twain |
|2 |2 |01/12/2022 |11:00 |Harry O’ Brien |
|3 |1 |02/12/2022 |09:00 |Harry O’ Brien |
|4 |2 |02/12/2022 |09:30 |Harry O’ Brien |
|5 |1 |02/12/2022 |16:00 |Harry O’ Brien |

**Business Rules:** 

1) Each appointment is allocated a new appointment number (appointmentNo). 
1) Many patients can make appointments for the same date and same time. 
1) A patient can make many appointments for the same day at different times.  

***[End of Question 2]*** 

***QUESTION 3 – Entity Relationship Modelling  [TOTAL MARKS: 25]*** 

**Read the following case study carefully.** 

Manufacturers have a name, which we may assume is unique, an address, and a phone number. Products have a model number and a type (e.g., television set). Each product is made by one manufacturer, and different manufacturers may have different products  with  the  same  model  number.  However,  you  may  assume  that  no manufacturer would have two products with the same model number. Customers are identified by their unique social security number. They have email addresses, and physical addresses. Several customers may live at the same (physical) address, but we assume that no two customers have the same email address. An order has a unique order number, and a date. An order is placed by one customer. A customers can place many orders.  For each order, there are one or more products ordered, each line is identified by an orderDetailNo. Many orders can have many products ordered on it. There is a quantity for each product on the order. 

**Q 3(a)  [5 Marks]** Clearly identify the entities described in the above Case Study. 

**Q 3(b)  [10 Marks]** 

Identify potential attributes and the primary key attribute(s) associated with each entity identified in (a) above. 

**Q 3(c)  [10 Marks]** 

Draw a single Entity Relationship Diagram to represent the above case study. Remove many to many relationships. 

**[End of Question 3]** 

***QUESTION 4 – Normalisation   [TOTAL MARKS: 25]*** 

The table found in Appendix A contains information in unNormalised form.  It outlines the details of Employees, the department they work in and the job that they are working on.  

**Examine** the table found in Appendix A and **perform** the following:  

**Q 4(a)  [17 Marks]** 

Normalise the Relation found above using 1st, 2nd and 3rd normal form rules**.**  Clearly illustrate the Relations(s) and data in 1st, 2nd and 3rd normal form.  

**Q 4(b)  [5 Marks]** Identify the primary key attribute(s) at each stage of normalization. 

**Q 4(c)  [3 Marks]** 

Identify potential names for new tables. Names should reflect the content in each relation. 

***[End of Question 4]*** 

***QUESTION 5 – Structured Query Language   [TOTAL MARKS: 25]*** 

The database relations found in Appendix B are for a simple garden kept by a small family. They plant their garden in the spring and pick their garden in summer. Details of each attribute and a description of each table can be found in Appendix B. Using the relations found in Appendix B perform the following: 

**Q 5(a)  [3 Marks]** 

Write an SQL command that would recreate the LOCATION table found in Appendix B. 

**Q 5(b)  [3 Marks]** 

Write a SQL statement to add an onion plant to the PLANT table. Values for the attributes are as follows: 

PlantID = 5 Name = Onion Sunlight 0.45 Water = 0.74 

**Q 5(c)  [3 Marks]** 

Write  a  valid  SQL  statement  that  calculates  the  total  weight  of  all  ears  of  corn (PlantID=2) that were picked from the garden: 

**Q 5(d)  [3 Marks]** 

Write a valid SQL statement that shows for each plant picked the Plant name and picked weight in pounds.  Using multiplicative conversion factor of 2.2 to convert kilograms to pounds  

**Q 5(e)  [4 Marks]** 

Write a valid SQL statement that would produce a list of vegetables picked by a particular gardener (gardenerID =2), the date picked, and amount picked. The result should output the following: 



|**GardenerName**  |**PlantName**   |**Date** |**Amount** |
| - | - | - | - |
|Tim |Radish      |2005-07-16 |23 |
|Tim |Carrot      |2005-08-18 |28 |
|Tim |Corn        |2005-08-28 |18 |

**Q 5 (f)  [4 Marks]** 

Write a valid SQL statement that would produce a result set which would include the plant name, location name, the amount of water the plant needs (needed), the water available in a location (available) and variance which is the difference between location water and plant water for the plant Carrot. The output should look like the following: 



|**PlantName**  |**LocationName**   |**Needed** |**Available** |**variance** |
| - | - | - | - | - |
|Carrot |East   |0\.82 |0\.8 |-0.02 |
|Carrot |West      |0\.82 |0\.48 |-0.34 |
|Carrot |North        |0\.82 |0\.84 |0\.02 |
|Carrot |South |0\.82 |0\.66 |-0.16 |

**Q 5 (g)  [5 Marks]** 

Write a valid SQL statement that calculates the average number of items produced per seed planted for each plant type: 

**(25 Marks Total)** 

**[End of Question 5] *[END OF EXAM]*** 

COMP06043 – Databases for Project 

Winter Examinations 2021/2022   Page 8 of 12 

**Appendix A** 

This UNF table refers to question 4 of your exam paper.  



|**Employee Code** |**Last Name** |**Education Code** |**Education Description** |**Year Earned** |**Department Code** |**Department Name** |**Job Class** |**Job  Title** |**Birth Date** |**Hire Date** |**Salary** |
| :- | :- | :- | :- | :- | :- | :- | :- | - | - | - | - |
|1003 |Rainsford |SC |Secondary School |1982 |MKTG |Marketing |23 |Sales Agent |20/03/1970 |14/09/2003 |165,000 |
|||BBA |Bachelor of Business |1988 ||||||||
|||MBA |Masters Business |1993 ||||||||
|||||||||||||
|1006 |Smith |SC |Secondary School |1972 |MIS |Info Systems |27 |Sys. Analyst |13/12/1990 |12/01/2002 |95,000 |
|||BSComp |Bachelor of  Computing |1976 ||||||||
|||BEd |Bachelor of  Education |1997 ||||||||
|||||||||||||
|1010 |Thompson |SC |Secondary School |1982 |MKTG |Marketing |23 |Sales Agent |19/06/2000 |12/04/2005 |76,000 |
|||Bed |Bachelor of  Education |1988 ||||||||
COMP06043 – Databases for Project 

Winter Examinations 2021/2022   Page 9 of 11 


**Appendix B** 

These relations refer to question 5 of your exam paper.  

**Relation: GARDENER** 

The Gardener relation outlines the details of each gardener in the family.  



|**GardenerID** |**Name** |**Age** |
| - | - | - |
|0 |Mother |36 |
|1 |Father |38 |
|2 |Tim |15 |
|3 |Erin |12 |

**Relation: PLANT** 

The Plant relation outlines the details of each plant their sunlight, weight, and water requirements. The sunlight attribute refers to the optimal amount of sunshine required for a plant.** The water attribute refers to the optimal amount of water required for a plant.** 



|**PlantID** |**Name** |**Sunlight** |**Water** |**Weight** |
| - | - | - | - | - |
|0 |Carrot |0\.26 |0\.82 |0\.08 |
|1 |Beet |0\.44 |0\.80 |0\.04 |
|2 |Corn |0\.44 |0\.76 |0\.26 |
|3 |Tomato |0\.42 |0\.80 |0\.16 |
|4 |Radish |0\.28 |0\.84 |0\.02 |

**Relation: LOCATION** 

The Location relation outlines details of each location in the garden and the sunlight attribute refers to the percentage of a 24-hour day that the location gets sunlight. The water attribute refers to the percentage of average rainfall that makes it to the root level for a location 



|**LocationID** |**Name** |**Sunlight** |**Water** |
| - | - | - | - |
|0 |East |0\.28 |0\.80 |
|1 |North |0\.17 |0\.84 |
|2 |West |0\.38 |0\.48 |
|3 |South |0\.45 |0\.66 |

**Relation: PLANTED** 

The Planted relation outlines details of each plant, planted by a gardener in a specific location on a specific date and the number of seeds planted.  



|**PlantID** |**GardenerID** |**LocationID** |**Date** |**Seeds** |
| - | - | - | - | - |
|0 |0 |0 |04-18-2005 |28 |
|0 |1 |1 |04-14-2005 |14 |
|1 |0 |2 |04-18-2005 |36 |
|2 |1 |3 |04-14-2005 |20 |
|2 |2 |2 |04-19-2005 |12 |
|3 |3 |3 |04-25-2005 |38 |
|4 |2 |0 |04-30-2005 |30 |

- PlantID is a Foreign Key references the PlantID in the Plant Relation 
- GardenerID is a Foreign Key references the GardenerID in the Gardener Relation 
- LocationID is a Foreign Key references the LocationID in the Location Relation 

**Relation: PICKED** 

The Picked relation outlines details of each plant picked by a gardener in a specific location on a specific date. The picked amount is the number of items (one carrot, one beet, an ear of corn, one tomato, one radish) picked. The weight is the total weight of the picking. 



|**PlantID** |**GardenerID** |**LocationID** |**Date** |**Amount** |**Weight** |
| - | - | - | - | - | - |
|0 |2 |0 |08-18-2005 |28 |2\.32 |
|0 |3 |1 |08-16-2005 |12 |1\.02 |
|2 |1 |3 |08-22-2005 |52 |12\.96 |
|2 |2 |2 |08-28-2005 |18 |4\.58 |
|3 |3 |3 |08-22-2005 |15 |3\.84 |
|4 |2 |0 |07-16-2005 |23 |0\.52 |

- PlantID is a Foreign Key references the PlantID in the Plant Relation 
- GardenerID is a Foreign Key references the GardenerID in the Gardener Relation 
- LocationID is a Foreign Key references the LocationID in the Location Relation 
COMP06043 – Databases for Project 

Winter Examinations 2021/2022   Page 12 of 12 
