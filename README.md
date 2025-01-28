# Data Professionals Survey-Dashboard

### Dashboard Link : https://app.powerbi.com/groups/me/reports/384d017e-e935-44dc-9e7d-1626c1a36de1/ReportSection

## Introduction

- Project Name: Data Professional Survey
- Purpose: The purpose of this Power BI project is to analyze and visualize survey data to gain insight into the demographics, career satisfaction and preferences of respondent. The visualization focuses on:

      1. The distribution of survey participants by country & job role
      2. The relationship between average salary, job role & gender
      3. The average age of survey participants
      4. The most popular programming languages among the respondents
      5. Levels of satisfaction with salary and work-life balance 


## Data Overview

**Data sources:**

The survey data used in this project is publicly available and was created by Alex Freberg. The data is provided in Excel format and serves as the foundation for this analysis.

**Data Structure:**

Table: Data Professional Survey

This table contains survey responses from data professionals including demographics, career details, and satisfaction levels. Below is an overview of the columns:  
      
    (1) Unique ID

    (2) Email

    (3) Date Taken

    (4) Time Taken

    (5) Browser

    (6) OS

    (7) City

    (8) Country

    (9) Referrer

    (10) Time Spent

    (11) Q1 - Which Title Best Fits your Current Role?

    (12) Q2 - Did you switch careers into Data?

    (13) Q3 - Current yearly salary (in USD)

    (14) Q4 - What Industry do you work in?

    (15) Q5 - Favorite programming language

    (16) Q6.1 - How Happy are you in your Current Position with the following? (Salary)

    (17) Q6.2 - How Happy are you in your Current Position with the following? (Work/Life Balance)

    (18) Q6.3 - How Happy are you in your Current Position with the following? (Coworkers)

    (19) Q6.4 - How Happy are you in your Current Position with the following? (Management)

    (20) Q6.5 - How Happy are you in your Current Position with the following? (Upward Mobility)

    (21) Q6.6 -  How Happy are you in your Current Position with the following? (Upward Mobility)

    (22) Q7 - How difficult was it for you to break into Data?

    (23) Q8 - If you were to look for a new job today, what would be the most important thing to you?

    (24) Q9 - Male/Female)

    (25) Q10 - Current age

    (26) Q11 - Which Country do you live in?

    (27) Q12 - Highest Level of Education

    (28) Q13 - Ethnicity

**Data Preparation:**

This section explains how the raw data was processed and cleaned using Power Query to ensure accurate and meaningful insights.

    1. Removed Unnecessary Columns
        1.1 Deleted the following columns: Browser, OS, City, Country, and Referrer.

    2. Cleaned Data for Job Title, Country, and Industry of Employment columns
        2.1 Removed duplicate values under the 'Other' option to standardize and ensure consistency.

    3. Processed the Current Yearly Salary (in USD) Column
        3.1 Duplicated the column and split it into two new columns using the "By Digit to Non-Digit" split method to separate the salary range into:
            - A column for the lower salary value (Q3 - Current yearly salary (in USD) - Copy.1).
            - A column for the upper salary value (Q3 - Current yearly salary (in USD) - Copy.2).
            
![Image](https://github.com/user-attachments/assets/81dcd80e-bf98-43f6-adfb-d5c68649a6a2)

![Image](https://github.com/user-attachments/assets/2490c8a4-6bec-43e5-80e1-ab4ff5e9d781)

        3.2 Used the "Replace Values" function to remove any non-numeric characters(k and -).
![Image](https://github.com/user-attachments/assets/f040a4cd-7183-4e3e-afb0-1d8308811956)

        3.3 Changed the data type of both new columns to whole number.
        3.4 Added a new column called Average Salary, calculated using the formula:
            Q3 - Current yearly salary (in USD) - Copy.1 + Q3 - Current yearly salary (in USD) - Copy.2 / 2

![Image](https://github.com/user-attachments/assets/12cfa501-909a-422f-9ea6-370285925ecb)

        3.5 Removed the two intermediate columns after calculating the average salary:

            1. Q3 - Current yearly salary (in USD) - Copy.1
            2. Q3 - Current yearly salary (in USD) - Copy.2 

## Dashboard Design

**Key Metrics/visuals**

The dashboard is designed to present survey insight using a variety of visualization to highlight key data points. Here's an explanation of each component and its purpose:

- Cards for count of survey takers and average age of survey takers

        a. Purpose: Provides a quick overview of the total number of survey participants and their average age.
        b. Reasoning: These metrics serve as high-level KPIs to give context to the survey's scope and demographics.

- Clustered Bar Chart: Average Salary by Job Title

        a. Purpose: Displays the average yearly salary segmented by job title.
        b. Reasoning: Highlights salary trends across different roles, helping to identify which roles are more lucrative based on the survey results.

- Stacked Column Chart: Favorite Programming Language

        a. Purpose: Visualizes the distribution of respondents' preferred programming languages.
        b. Reasoning: Shows which programming languages are most popular among the survey takers, providing insights into skill preferences in the data professional field.

- Treemap: Country Where the Survey Takers Live

        a. Purpose: Maps the geographical distribution of the survey respondents.
        b. Reasoning: Offers a visual representation of the countries with the most survey participants, showcasing diversity and reach.

- Gauge: Happiness with Work-Life Balance

        a. Purpose: Measures and displays how satisfied respondents are with their work-life balance.
        b. Reasoning: Provides insight into how well survey takers perceive their work-life balance, which is an essential factor for job satisfaction.

- Gauge: Happiness with Salary

        a. Purpose: Reflects the level of satisfaction respondents have with their current salary.
        b. Reasoning: Offers a glimpse into whether compensation aligns with expectations, which can impact overall happiness at work.

- Donut Chart: Difficulty to break into data

        a. Purpose: Visualizes how respondents perceive the difficulty of entering the field, whether it's easy, moderate, or challenging. 
        b. Reasoning: Allow a quick view of how many found it difficult versus easy to break into the field.
    
**Filters and Interactions**

- Drill through to explore details at the project level

## Snapshot of Dashboard (Power BI Service)

## Findings and Takeaways

- Findings:

        1. Most survey respondents from the tech industry report a moderate level of satisfaction with their work-life balance, with 57.4% giving it an average rating.

        2. Survey results show that workers who are satisfied with their work-life balance tend to have lower salaries, with a happiness rating of 5.74 out of 10. In contrast, those with a lower work-life balance satisfaction score (4.27 out of 10) generally earn higher salaries, suggesting that achieving a higher salary may come at the cost of work-life balance.

        3. The data shows that Data Scientists earn the highest average salary. Since the average age of the survey respondents is around 30, it suggests that many people in this role are likely more experienced and hold senior positions.

        4. Python remains the most popular programming language among data professionals, with 60% of respondents choosing it as their primary tool.

        5. With 42.7% of survey respondents finding it neither easy nor challenging to break into the data field, it suggests that the data field is accessible and can be learned with consistent effort.

- Takeaways:

        1. The findings show that workers often have to choose between earning a higher salary or having a better work-life balance. This insight can help individuals decide what matters most to them and plan their career goals accordingly.

        2. For those interested in breaking into data and seeking high earnings, pursuing a role as a Data Scientist might be a strategic choice, given its reputation as the highest-paying job among survey respondents.

        3. With Python being the most widely used tool in the data field, learning this programming language is essential for anyone looking to build or switch careers in data.

        4. Breaking into data may seem daunting, but with nearly half of the survey respondents stating that it’s neither easy nor difficult, this field is accessible and achievable for those willing to put in consistent effort.



 
 
