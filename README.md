# springboard_datascience
Springboard Data Science Career Track Course - 201709
Chapter 5.2 Data Wrangling - Working with Data in Files 
Project: Work on JSON Based Data Exercises

Data: 
world_bank_projects.json

Objectives:
Using data in file 'data/world_bank_projects.json' and the techniques demonstrated above,
1.Find the 10 countries with most projects
2.Find the top 10 major project themes (using column 'mjtheme_namecode')
3.In 2. above you will notice that some entries have only the code and the name is missing. Create a dataframe with the missing names filled in.

Approach:
1. Find the 10 countries with most projects
We understand that each of data represents a project. To answer this question, the plan is to: 
  a.Extract all rows with column "countryname" which the country name is the easiest to understand.
  b.Count the number of rows for each of the country. Here we show two methods of counting by using Counter in Python Collections and directly using dataframe count and that sort the counts in descending order. Both approaches achieved the same result.
  c.List out the top 10 countries with the highest counts.

2. Find the top 10 major project themes (using column 'mjtheme_namecode')
The plan to answer this question:
  a. Understand the data structure of the column "mjtheme_namecode".
  b. Count the number of projects per project theme.

We observed that there was null string value in project names of the data file.  So comes qusetion 3.

3. In 2, above you will notice that some entries have only the code and the name is missing. Create a dataframe with the missing names filled in.
The plan to answer this question:
  a. Analyze the project type code and project type name relationship.
  b. Create a project theme dataframe.
  c. Loop over the project list dataframe. If the entry of project theme name is with null string value, assign appropriate project theme name according to the project theme dataframe.
