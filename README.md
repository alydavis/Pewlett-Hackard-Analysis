# Pewlett-Hackard-Analysis

## Overview
Using a fictional company's employee data, I helped the company determine the number of retiring employees, their titles, and employees would who would be eglibile to particpate in a mentorship program. There are an expected (X) number of employees eligible for retirement - a huge portion of the workforce. This analysis will help the company plan aheads for these changes and suggest possible solutions to minimize the business impact. 

## Results
ERD ![Image](Path) shows the relationships between the supplied employee data. My joining datasets based on the primary keys, I could build custom tables for the information needed.


Bulleted list with 4 major points from the two analysis deliverables
### The Number of Retiring Employees by Title
The first table needed holds the titles of employees who were born between Jan 1952-Dec 1955. As employees moved up through the ranks and recieved promotions throughout the years, the data needed to be cleaned for distinct titles to eliminate duplicate employee records. 

How many employees are expected to retire? - X -  link to file: retirement_titles.csv
 - due to promotions - some duplicates. using DISTINCT ON joins I was able to get the Unique titles - X - link to file: unique_titles.csv
Retiring titles X Retiring_titles.csv - what roles will the team need to focus on backfilling and which areas will feel the largest impact of the upcoming retirements.


### Employees Eligible for the Mentorship Program
Mentorship-eligibility - X of employees

how many employees are eligible?

## Summary 
The summary addresses the two questions:
How many roles will need to be filled as the "silver tsunami" begins to make an impact?
Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?
two additional quieries or tables that may provide more insight
-look into a month - by month view to see which seasons, business quarters, etc. may feel the most impact
