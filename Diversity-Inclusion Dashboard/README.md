# Diversity & Inclusion | PWC Virtual Case Experience

![Cover](https://github.com/Baher1997/PWC_Power_bi_-Virtual_-Internship/blob/main/Diversity-Inclusion%20Dashboard/Home.png)


## Table of contents
- [Problem Statement]()
- [Data Sourcing]()
- [Data Preparation]()
- [Data Modeling]()
- [Data Visualization]()
- [Analysis and Insights]()
- [Shareable Link]()

# Problem Statement

- **Problem:** Understanding the diversity and inclusion landscape is critical for fostering an equitable workplace. This dashboard focuses on:
  
- **Objective**:
    - Analyzing promotions and turnover trends.
    - Evaluating diversity in new hires.
    - Identifying areas of improvement for retention and leadership opportunities.
 
  # Data Sourcing

The dataset used for this analysis was provided by [Pwc Switzerland](https://www.pwc.ch/en/careers-with-pwc/students/virtual-case-experience.html) and available here: [Diversity & Inclusion](https://github.com/Baher1997/PWC_Power_bi_-Virtual_-Internship/blob/main/Diversity-Inclusion%20Dashboard/03%20Diversity-Inclusion-Dataset.xlsx)

# Data Preparation

The dataset was loaded into Microsoft Power BI Desktop for modeling after transformation in Power Query.

### **Metadata**

The tabulation below shows the metadata of `Diversity & Inclusion` dataset:
| File name | 03 Diversity-Inclusion-Dataset |
| --- | --- |
| Format | .xlsx |
| Size | 176 KB |
| Fields | 32 |
| Entities | 500 |

The tabulation below shows the Diversity & Inclusion table with its field's names and their description:
| Column Name | Description |
| --- | --- |
| Employee ID | Represents the unique number of the employee in the dataset |
| Gender | Describes the gender of the employee |
| Job Level after FY20 promotions | Describes the job level of the employee after being promoted in FY20 |
| New hire FY20? | Describes if the employee is a new hire in FY20 |
| FY20 Performance Rating | Represents the performance rating of the employee in FY20 |
| Promotion in FY21? | Describes if the employee is being promoted in FY21 |
| In base group for Promotion FY21 | Describes if the employee is being selected for promotion in FY21 |
| Target hire balance | Describes the target hire balance of the employee |
| FY20 leaver? | Describes if the employee is a leaver in FY20 |
| In base group for turnover FY20 | Describes if the employee is in a group for turnover in FY20 |
| Department @01.07.2020 | Describes the department each employee belongs to as of January 7, 2020 |
| Leaver FY | Describes if the employee is a leaver in an FY |
| Job Level after FY21 promotions | Describes the job level of the employee after being promoted in FY21 |
| Last Department in FY20 | Describes the last department each employee belongs in FY20 |
| FTE group | Describes if the employee belongs to an FTE group |
| Time type | Describes the contract type employee |
| Department & JL group PRA status | Describes the department and JL group PRA status of the employee |
| Department & JL group for PRA | Describes the department and JL group PRA of the employee |
| Job Level group PRA status | Describes the job level group PRA status of the employee |
| Job Level group for PRA | Describes the job level group PRA of the employee |
| Time in Job Level @01.07.2020 | Describes the time in job level of the employee |
| Job Level before FY20 promotions | Describes the job level of the employee before being promoted in FY20 |
| Promotion in FY20? | Describes if the employee is being promoted in FY20 |
| FY19 Performance Rating | Describes the performance rating of the employee in FY19 |
| Age group | Describes the age group of the employee |
| Age @01.07.2020 | Represents the age of the employee as of January 07, 2020 |
| Nationality 1 | Describes the nationality of the employee at the state level |
| Region group: nationality 1 | Describes the nationality of the employee at the country level |
| Broad region group: nationality 1 | Describes the nationality of the employee at the regional level |
| Last hire date | Describes the last hire date of the employee |
| Years since the last hire | Represents the number of years since the last hire of the employee |
| Rand | generates a random number for each entry in the dataset |

### Data Cleaning

Data Cleaning for the dataset was done in Power Query as follows:

- Unnecessary columns were removed
- Unnecessary rows were filtered
- Each of the columns in the table was validated to have the correct data type

### Data Transformation

- For easy observing and analyzing, the extracted text had been applied for those columns: `Job Level after FY21 promotions`, `Job Level after FY20 promotions`
    - Extracted Text After Delimiter = `Table.TransformColumns(#"Extracted Text After Delimiter1", {{"Job Level before FY20 promotions", each Text.AfterDelimiter(_, "-"), type text}})`

# Data Modeling

After the dataset was cleaned and transformed, it was ready to be modeled. Because the dataset is just included one table, the Data Modeling is nothing much to modify
- `Measure` was created to store all DAX measures for ensuring the organization

![data modeling](https://github.com/Baher1997/PWC_Power_bi_-Virtual_-Internship/blob/main/Diversity-Inclusion%20Dashboard/Preformance%20Dashboard.png)


# Data Visualization

Data visualization for the dataset was done in Microsoft Power BI Desktop, the dashboard includes three main dashboards and three tooltip pages:

- Home (Insghits and Reccomendations)
- Performance Dashboard
- Diversity-Inclusion Analysis for new hires
- Analysis in promotion of employees

![detail](https://github.com/Baher1997/PWC_Power_bi_-Virtual_-Internship/blob/main/Diversity-Inclusion%20Dashboard/Diversity-Inclusion%20Analysis%20for%20new%20hires.png)
![detail](https://github.com/Baher1997/PWC_Power_bi_-Virtual_-Internship/blob/main/Diversity-Inclusion%20Dashboard/Analysis%20in%20promotion%20of%20employees.png)

### Dashboard Type

Dashboard by the level of detail: **Operational dashboard**

Dashboard by use-case: **Exploratory**

Target audience: **Human Resource Manager, Analyst**

### Key Performance Indicators and Metrics:

**Home Overview:**

![detail](https://github.com/Baher1997/PWC_Power_bi_-Virtual_-Internship/blob/main/Diversity-Inclusion%20Dashboard/Home.png)

- Overall Gender Distribution
- Turnover Rate
- Promotion Rate
- New Hire Diversity Metrics
- Employee Retention by Gender

**Diversity & Inclusion Analysis for New Hires:**

- Gender Distribution in New Hires
- Age Group Distribution
- Nationality Distribution
- Departmental Hiring Trends
- Regional Hiring Distribution
  
**Analysis in Promotion of Employees:**

- Promotion Rate by Gender
- Turnover Rate by Gender
- Department-Wise Promotion Rate
- Job Level Promotion Trends
- Performance Rating Changes

**Performance:**

- Average Performance of gender, leavers
- Performance Rate distribution
- Average Performance Rate by Positions, Age, Region
- Comparison performance between leaver and non-leaver by department
