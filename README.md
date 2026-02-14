# Freelancer-Performance-Market-Analysis

Mini project analyzing global video game sales using Excel and Power BI

## Dataset Description
- **Source:** https://www.kaggle.com/datasets/urvishahir/global-freelancers-raw-dataset
- **Number of Sheets:** 1
- **Number of Rows:** 1001
- **Number of Columns:** 12

### Dataset Overview
This dataset contains 1000 fictional freelancer profiles from different countries.  
It includes inconsistencies, missing values, mixed formats, and variations in data entry.

### Fields Included
1. Freelancer ID  
2. Name  
3. Gender  
4. Age  
5. Country  
6. Language  
7. Primary Skill  
8. Years of Experience  
9. Hourly Rate (USD)  
10. Rating  
11. Is Active  
12. Client Satisfaction  

## Project Objectives
- Clean and prepare raw data for analysis
- Compare gender activity, hourly rate, rating, profile value score, and client satisfaction
- Categorize freelancers by age groups (18–29, 30–39, 40–49, 50+)
- Identify dominant age group
- Identify top freelance countries
- Compare low-income vs high-income countries
- Analyze language distribution and correlation with skills and hourly rate
- Identify most popular and highest-paying skills
- Compare skills by experience and hourly rate
- Analyze relationships:
  - Rating vs Experience
  - Hourly Rate vs Experience
  - Experience vs Client Satisfaction
- Identify countries/skills where hourly rate increases most with experience
- Display Top 10 freelancers by client satisfaction

##  Data Cleaning & Processing Steps (Excel)

1. Converted dataset into table format (No duplicates found)
2. Cleaned Name column using PROPER & TRIM functions
3. Standardized Gender values using IF function
4. Replaced 30 missing Age values with "Unknown"
5. Replaced 51 missing Experience values with "Unknown"
6. Cleaned Hourly Rate column:
   - Removed symbols ($, USD)
   - Used TRIM, CLEAN, SUBSTITUTE
   - Filled 91 blanks with median (50)
7. Filled 101 missing Ratings with median value
8. Standardized Is Active column:
   - Converted mixed values to TRUE/FALSE
   - Filled 89 blanks using mode (TRUE)
9. Standardized Client Satisfaction:
   - Converted % to decimal format
   - Filled 176 blanks with median (0.75)
10. Created final cleaned table using VLOOKUP
11. Applied proper formatting
12. Created PivotTables for summary analysis

## Power BI Data Modeling

### Calculated Columns

### 1. Age Category
- 50+ → Age > 50  
- 40–49 → Age > 40 and ≤ 49  
- 30–39 → Age > 30 and ≤ 39  
- 18–29 → Age ≤ 29  
- Unknown → Missing values  

### 2. Hourly Rate Category
- High → > 80 USD  
- Medium → 45–80 USD  
- Low → ≤ 45 USD  

### 3. Skill Category
- Development/Tech  
- Data & AI  
- Design  
- IT & Security  
- Others  

### 4. Experience Category
- Senior → > 10 years  
- Junior → 2–10 years  
- Fresher → ≤ 2 years  
- Unknown  

### 5. Rating Category
- High → > 4.5  
- Medium → 2.5–4.5  
- Low → ≤ 2.5  

## Profile Value Score Formula

Profile Value Score =
(Rating * 0.4) +
(Client Satisfaction * 0.3) +
(Experience * 0.2) +
(Is Active * 0.1)


##  Key Measures Created

- Count of Active Freelancers
- Average Profile Value Score by Gender
- Average Hourly Rate
- Gender Distribution
- Highest Paying Language
- Highest Paying Skill
- Total Freelancers
- Top Profile by Value Score

## Key Insights & Conclusions

1. Out of 1000 freelancers, 632 are active (Female: 317 | Male: 315)
2. Female freelancers have slightly higher average hourly rate (USD 53.22) compared to males (USD 52.08)
3. 50+ age group is dominant, indicating strong demand for experienced professionals
4. South Korea has the highest freelancer count
5. Low-income countries have more freelancers (46.3%), but high-income countries offer higher rates
6. English is most common language, Turkish has highest average hourly rate
7. Development/Technology is most popular skill category
8. Web Development is highest paying skill
9. Hourly rate increases significantly with experience
10. Experience impacts pricing more than rating
11. Client satisfaction is nearly equal across genders


##  Tools Used

- Microsoft Excel (Data Cleaning & PivotTables)
- Power BI (Data Modeling & Dashboard Visualization)


##  Project Files

- Raw Dataset
- Cleaned Dataset
- Excel File
- Power BI Dashboard (.pbix)



  
