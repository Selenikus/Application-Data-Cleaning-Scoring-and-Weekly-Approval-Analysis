# Application Data Cleaning, Scoring, and Weekly Approval Analysis
### Project Overview
This project focuses on cleaning, enriching, and analyzing application data using Pandas in Jupyter Notebook. 
The goal is to process application records, calculate scores based on predefined criteria, and visualize the weekly approval trends.

### Data Processing Steps

### 1. Load and Clean Data:
Remove duplicate values from the applicant_id column.
Fill missing values in the External Rating column with 0.
Fill missing values in the Education level column with "Ortaokul" (Middle School).

### 2. Merge Industry Data:
Join the applications.csv dataset with industries.csv to include industry ratings.

### 3. Calculate Application Score:
The score ranges from 0 to 100, based on the following conditions:
If Amount is missing or External Rating is 0, the score is set to 0.
Add 20 points if the applicant is aged between 35 and 55.
Add 20 points if the application was not submitted on a weekend.
Add 20 points if the applicant is married.
Add 10 points if the applicant is located in Kyiv or nearby.
Add the industry score (ranging from 0 to 20) from industries.csv.
Add 20 points if External Rating is 7 or higher.
Subtract 20 points if External Rating is 2 or lower.

#### 4.Filter Accepted Applications:
Keep only applications with a score greater than 0.

### 5. Weekly Analysis and Visualization:
Group accepted applications by week of submission.
Calculate the average score per week.
Visualize the trend using a graph.

### Results & Insights
The cleaned and enriched dataset provides insights into application approval trends.
The scoring system helps identify strong applications based on age, location, marital status, industry score, and external rating.
The final visualization shows the weekly average score of accepted applications, highlighting trends over time.
