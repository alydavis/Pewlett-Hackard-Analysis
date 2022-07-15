# Pewlett-Hackard-Analysis

## Overview
Using a fictional company's employee data, this analysis helps the company understand the number of expected retiring employees and inform a plan for mentorship program solution. This analysis will help the company plan ahead for these changes and suggest possible solutions to minimize the business impact on employees transitioning out of the workforce.

## Results
The Entity Relationship Diagram helps visualize the relationship between the disparate data sources. ![ERD](ERD/EmployeeDB.png) 

### The Number of Retiring Employees by Title
The first query combined the titles of employees who were born between Jan 1952-Dec 1955, as they were nearing retirement age. The output file needed the employee's number, first and last name, title, and employment dates.
How many employees are expected to retire? The first query resulted in a list of 130k+ employees. [retirement_titles.csv](Data/retirement_titles.csv)

As employees moved up through the ranks and recieved promotions throughout the years, some employees had multiple titles and salaries. The data needed to be cleaned for distinct titles to eliminate duplicate employee records. 

Using the DISTINCT ON joins query I was able to get the [Unique_titles.csv](Data/unique_titles.csv). This will only return the latest title for each employee. 74,258 employees fit this criteria. This is a huge number of potentital employees to backfill.

The next query counts the number of roles by title, which could help HR and managers understand which roles will be most impacted by the retirees. [Retiring_titles.csv](Data/retiring_titles.csv). The company will want to prioritize Senior Enigneer and Senior Staff roles as these areas will feel the largest impact (70% of retiring employees):
 - 25,916	Senior Engineer
 - 24,926	Senior Staff
 - 9,285	Engineer
 - 7,636	Staff
 - 3,603	Technique Leader
 - 1,090	Assistant Engineer
 - 2	Manager

### Employees Eligible for the Mentorship Program
The Mentorship-eligibility query joined on the primary employee number key, combined first name, last name, birth date, and employement dates, and titles into a new table based on birth date criteria in 1965. Based on [the mentorship eligibility output](Data/mentorship_eligibility.csv), 1,549 employees are eligible for the mentorship program.

The full query [code is linked here for reference](Queries/Employee_Database_challenge.sql).

## Summary 
The company will need to fill 74,258 roles. While there are some qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees, it will not be enough.

The mentorship program as it is planned, is not enough to fill to the exodus of employees. The mentorship eligibility criteria could be expanded to be more inclusive. Other queries could help the HR and management teams recruiting talent from competitors with strong compensation opportunities. A deeper dive on compensation compared to industry averages could be useful. A query comparing mid level employees could also help inform promotions from within and set a plan for recruiting new entry-level talent.

