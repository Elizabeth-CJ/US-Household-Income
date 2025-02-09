# 🏡 US Household Income Data Analysis  



## 📌 Project Overview  
This project analyzes US household income data using **MySQL** for data cleaning, transformation, and exploration. The goal is to identify patterns and insights in income distribution across different states and counties.  


## 📊 Data Sources  
- [US Household Income Dataset](#) (add dataset source)


## 🛠 Tools Used  
- **MySQL** – Data cleaning & analysis  


## 🔄 Data Cleaning & Preparation  
The following steps were taken to clean and prepare the data:  

1. **Data Loading & Inspection**  
   - Checked for duplicates  
   - Identified missing values  

2. **Handling Missing Values**  
   - Replaced empty values in 'Place' column  
   - Fixed state name inconsistencies (e.g., 'georia' → 'Georgia')  

3. **Data Formatting**  
   - Standardized state abbreviations  
   - Adjusted incorrect area values  

## 📈 Exploratory Data Analysis  
We explored key insights into **household income distribution** based on state and county.  

## 🏆 Data Analysis  
Some key queries used:  

```sql
-- Identifying duplicate entries

SELECT id, COUNT(id)
FROM us_household_project.ushouseholdincome
GROUP BY id
HAVING COUNT(id) > 1;

```

```
-- Fixing incorrect state names

UPDATE us_household_project.ushouseholdincome
SET State_name = 'Georgia'
WHERE State_name = 'georia';

```


## 🏆 Results & Findings
**Household income data is unevenly distributed across states**
 - Some states have significantly more entries than others.
 - This could be due to data availability or reporting inconsistencies.
 - Larger states like California, Texas, and New York have the most data entries, while smaller or rural states have fewer.


## ✅ Recommendations
**Perform deeper income analysis**
 - Further analysis on income inequality trends could be conducted.
 - Compare income levels across different regions and city types (urban vs. rural).


## 🚧 Limitations
1. **Data Imbalance Across States**
    - Some states have more data entries than others, making direct comparisons tricky.
    - Solution: Use proportional analysis instead of raw counts.

2. **Incomplete or Missing Data**
    - Some records lack place names, making it difficult to map income distribution.
    - Missing values in AWater (water area) could affect geographical insights.

