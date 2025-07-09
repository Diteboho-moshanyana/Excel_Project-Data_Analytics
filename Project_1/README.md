# Excel_Project-Data_Analytics

![1_Salary_Dashboard](https://github.com/user-attachments/assets/85ad14c7-3ad2-4fce-8c38-ad4267e9e845)

This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated. 
The data contains detailed information on job titles, salaries, locations, and essential skills that are presented here. 

##Dashboard File
[My final dashboard is in](Project_1)

### Excel Skills Used 

The following Excel skills were utilized for analysis: 

- 📉 Charts 
- 🧮 Formulas and Functions
- ❎ Data Validation

### Data Jobs Dataset 

The dataset used for this project contains real-world data science job information from 2023. It includes detailed information on: 

- 👨‍💼 Job titles
- 💰 Salaries
- 📍 Locations
- 🛠️ Skills

### Dashboard Build 
- 📉 Charts 
- 📊 Data Science Job Salaries - Bar Chart

![1_Salary_Dashboard_Chart1](https://github.com/user-attachments/assets/251a0128-0d1b-44a2-a849-03192283c461)

  
- 🛠️ Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
- 🎨 Design Choice: Horizontal bar chart for visual comparison of median salaries.
- 📉 Data Organization: Sorted job titles by descending salary for improved readability.
- 💡 Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.
  
🗺️ Country Median Salaries - Map Chart

![1_Salary_Dashboard_Chart2](https://github.com/user-attachments/assets/709f0e42-349c-47d4-bc83-180d383b3847)

  
- 🛠️ Excel Features: Utilized Excel's map chart feature to plot median salaries globally.
- 🎨 Design Choice: Color-coded map to visually differentiate salary levels across regions.
- 📊 Data Representation: Plotted median salary for each country with available data.
- 👁️ Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.
- 💡 Insights Gained: Enables quick grasp of global salary disparities and highlights high/low salary regions.
- 🧮 Formulas and Functions
  
💰 Median Salary by Job Titles
```
=MEDIAN( 
IF( 
    (jobs[job_title_short]=A2)* 
    (jobs[job_country]=country)* 
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))* 
    (jobs[salary_year_avg]<>0),     jobs[salary_year_avg] 
) 
) 
```
- 🔍 Multi-Criteria Filtering: Checks job title, country, schedule type, and excludes blank salaries.
- 📊 Array Formula: Utilizes MEDIAN() function with nested IF() statement to analyze an array.
- 🎯 Tailored Insights: Provides specific salary information for job titles, regions, and schedule types.
- 🔢 Formula Purpose: This formula populates the table below, returning the median salary based on job title, country, and type specified.
  
🍽️ Background Table

![1_Salary_Dashboard_Screenshot1](https://github.com/user-attachments/assets/cfceac9b-11ac-47bb-9a5b-7ddd82a22f31)
  
📉 Dashboard Implementation

![1_Salary_Dashboard_Job_Title](https://github.com/user-attachments/assets/fcb72cae-afdf-4ec3-a42a-dfb6322fe994)

  
⏰ Count of Job Schedule Type 
```  
  =FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<
>0))
```

- 🔍 Unique List Generation: This Excel formula below employs the FILTER() function to exclude entries containing "and" or commas, and omit zero values.
- 🔢 Formula Purpose: This formula populates the table below, which gives us a list of unique job schedule types.
  
🍽️ Background Table

![1_Salary_Dashboard_Screenshot2](https://github.com/user-attachments/assets/64db4f2e-6a45-45d6-b0d4-b3ea9f87b18f)


📉 Dashboard Implementation:

![1_Salary_Dashboard_Type](https://github.com/user-attachments/assets/323e0bfe-d007-47ee-8486-88653668c99c)
  
❎ Data Validation

🔍 Filtered List
- 🔒 Enhanced Data Validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type - option in the Data tab ensures:
- 🎯 User input is restricted to predefined, validated schedule types
- 🚫 Incorrect or inconsistent entries are prevented
- 👥 Overall usability of the dashboard is enhanced

![1_Salary_Dashboard_Data_Validation](https://github.com/user-attachments/assets/c67a603a-12aa-4ec5-ae66-26e8d3f79b12)

Conclusion 
I created this dashboard to showcase insights into salary trends across various datarelated job titles. Utilizing data from my Excel course, this dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries. 

