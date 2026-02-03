# Excel Salary Dashboard
![1_Salary_Dashboard_Final_Dashboard](https://github.com/user-attachments/assets/bebd72ef-3493-4dec-88b7-1e769f95d5ba)

## Introduction
This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated.

The data is from my Excel course, which provides a foundation in analyzing data using this powerful tool. The data contains detailed information on job titles, salaries, locations, and essential skills that are presented here.

### Dashboard File
My final dashboard is in [Salary_Dashboard.xlsx](Salary_Dashboard.xlsx)

### Excel Skills Used 
The following Excel skills were utilized for analysis:

- 📉 Charts
- 🧮 Formulas and Functions
- ❎ Data Validation
### Data Jobs Dataset 
The dataset used for this project contains real-world data science job information from 2023. The dataset is available via my Excel course, which provides a foundation for analyzing data using Excel. It includes detailed information on:

- 👨‍💼 Job titles
- 💰 Salaries
- 📍 Locations
- 🛠️ Skills
# Dashboard Build 
### 📉 Charts 
📊 Data Science Job Salaries - Bar Chart 
<img width="731" height="550" alt="Screenshot 2026-02-03 at 12 18 34 AM" src="https://github.com/user-attachments/assets/f5725899-5bb0-41d5-a2de-180ee9ebe543" />

- 🛠️ Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
- 🎨 Design Choice: Horizontal bar chart for visual comparison of median salaries.
- 📉 Data Organization: Sorted job titles by descending salary for improved readability.
- 💡 Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.
  
🗺️ Country Median Salaries - Map Chart
![1_Salary_Dashboard_Country_Map](https://github.com/user-attachments/assets/be33615a-6576-44ad-aa4c-07850f8e609c)


- 🛠️ Excel Features: Utilized Excel's map chart feature to plot median salaries globally.
- 🎨 Design Choice: Color-coded map to visually differentiate salary levels across regions.
- 📊 Data Representation: Plotted median salary for each country with available data.
- 👁️ Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.
- 💡 Insights Gained: Enables quick grasp of global salary disparities and highlights high/low salary regions.
## 🧮 Formulas and Functions 
💰 Median Salary by Job Titles 
``` =MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
``` 

- 🔍 Multi-Criteria Filtering: Checks job title, country, schedule type, and excludes blank salaries.
- 📊 Array Formula: Utilizes MEDIAN() function with nested IF() statement to analyze an array.
- 🎯 Tailored Insights: Provides specific salary information for job titles, regions, and schedule types.
- 🔢 Formula Purpose: This formula populates the table below, returning the median salary based on job title, country, and type specified. 


🍽️ Background Table 

<img width="300" height="220" alt="1_Salary_Dashboard_Screenshot1" src="https://github.com/user-attachments/assets/6558c143-eedb-4eb0-a05f-1b186096edb9" />.  




 📉 Dashboard Implementation  
 

<img width="400" height="2300" alt="1_Salary_Dashboard_Job_Title" src="https://github.com/user-attachments/assets/2cd54b9a-c343-4211-b9b3-c4eb3d3f90ba" />


#### ⏰ Count of Job Schedule Type
```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

- 🔍 Unique List Generation: This Excel formula below employs the FILTER() function to exclude entries containing "and" or commas, and omit zero values.
- 🔢 Formula Purpose: This formula populates the table below, which gives us a list of unique job schedule types.
  
🍽️ Background Table

<img width="195" height="119" alt="1_Salary_Dashboard_Screenshot2" src="https://github.com/user-attachments/assets/5a3184ae-e1c8-4936-b241-fe21c2ce15de" />. 



📉 Dashboard Implementation: 

<img width="421" height="519" alt="Screenshot 2026-02-03 at 12 46 07 AM" src="https://github.com/user-attachments/assets/ed8423b8-d7a3-43b5-b6e6-53b9d7e17254" />



## ❎ Data Validation
#### 🔍 Filtered List
- 🔒 Enhanced Data Validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the Data tab ensures:
  - 🎯 User input is restricted to predefined, validated schedule types
  - 🚫 Incorrect or inconsistent entries are prevented
  - 👥 Overall usability of the dashboard is enhanced 

![1_Salary_Dashboard_Data_Validation](https://github.com/user-attachments/assets/c2aa68c9-b448-4692-9a4d-e23f7b12e1ca)

## Conclusion
I created this dashboard to showcase insights into salary trends across various data-related job titles. This dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries.
