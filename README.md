# Sales-Analysis

1. Data Gathering / Requirement: 
Assemble a sales reports with different visuals to best show the Sales Insights. 

 

1. Sales (folder by year) 
2. Categories (Excel) 
3. Geography (Excel) 
4. Product (CSV / Database) 
5. SalesRep (Excel) 
6. SubCategories (Excel) 

 

Task 1.1: 
Created a mechanism to load all the files from the sales folder in a single Sales fact table. 
The mechanism needed to be resilient as: 
 -removing a file from the sales folder that does not create an error for missing files. 
 -adding a new yearly sales file will automatically be loaded in the fact query upon refresh. 

 

2. Data Modeling: 
Task 2.1:  
Did the respective transformations to the Sales fact table in order to split the Country from the 
City in the field “Location”. Made sure to set up the correct Data Type to allow Geo maps. 
Did the necessary updates in the Date field to make sure l can setup the Date format. 
Task 2.2:  
Created a unique key (GeoKey) in the Sales and Geography table 

 

Task 2.3: 
The Dimensional queries SalesRep and Sub Category needed additional treatment. Some ID 
columns have the following format:  

Created a small function that removed the “ID - ” part of these columns that l can invoke and 
reuse for these two queries to clean the IDs. 

Task 2.4:  
Created the Data Model connecting all tables and using the Calendar table already set up in the 
pbix. 


3. DAX calculations 
Task 3.1: 
Calculated Total Revenue in Sales table, using the Product’s Retail Price, and multiplying it by the 
Units. 
Task 3.2: 
 Calculated Total Cost in Sales table, using the Product’s Standard Cost, and multiplying it by the 
Units. 
Task 3.3: 
Calculated Gross Profit in Sales: Total Revenue – Total Cost 
Task 3.4: 
Calculated a Gross profit MoM growth Change% measure that could benefit us in decision making 
Task 3.5: 
Calculated a measure for AVG sales per day – this is the average sum of Total Revenue per day 
based on the Dates of actual Sales. 
Task 3.7:  
- Breakdown Analysis by Product (drop or increase) 
Calculated the following time measures: 
- This is QBR Report. So QoQ Growth is required 
