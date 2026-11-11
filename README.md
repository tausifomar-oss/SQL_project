# Introduction
Dive into the data job market ! Focusing on data analyst roles , this project explores top paying jobs, in-demand skills , and where high demand meets high salary in data analytics.

SQL queries ? Check them out here : [project_sql folder](/project_sql/)

# Background
Driven by a quest to navigate the data analyst job market more effectively , this project was born from a desire to pin-point top-paid and in-demand skills, streamlining others work to find optimals jobs .

Data is from [ [SQL course](https://www.lukebarousse.com/sql) ] It's packed with insights on job titles , salaries , locations , and essential skills.

### The question I wanted to answer through my SQL queries were :

1. What are the top paying data analyst jobs?
2. What skills are required for these top paying jobs?

3. What skills are most in demand for data analysts ?

4. Which skills are associated with higher salaries ?
5. What are most optimal skills to learn ?


# Tools I used
For my deep dive into data analyst job market ,I harnessed the power of several key tools :

- **SQL**
- **PostgreSQL**
- **Visual Studio code**
- **Git & GitHuB**


#  The Analysis
Each query for this project aimed at investigating specific aspects of the data analyst job market . Here's how I approached each question :

### 1. Top paying data analyst jobs
To identify the highest paying roles, I filtered data analyst positions by average year salary and location , focusing on remote jobs . This query highlights the high paying opportunities in the field .

```sql
select 
skills,
count(skills_job_dim.job_id) AS demand_count
from job_postings_fact
    Inner join skills_job_dim on
    job_postings_fact.job_id=skills_job_dim.job_id
    inner join skills_dim on
    skills_job_dim.skill_id=skills_dim.skill_id
WHERE 
job_title_short='Data Analyst' AND job_work_from_home=TRUE
    group by 
    skills
    order by
    demand_count desc
    limit 5
```

Here's the breakdown of the top data analyst jobs in 2023 :

**Wide salary range**  Top 10 paying data analyst roles span from 184,000 USD to 650,000 USD indicating significant salary potential in the field .

**Diverse employers** Companies like SmartAsset , Meta and AT&T are among those offering high salaries , showing  a broad interest across different industries.

**Job title variety** 
There's a high diversity in job-titles , from Data Analyst to Director of Analytics, reflecting varied roles and specializations within data analytics.

# What I learned 
Throughout this course , I have learned use of SQL toolkit , merging tables , using functions like GROUPBY and COUNT 

# Conclusion
This project enhanced my SQL skills and provided valuable insights into the data analyst job market.



