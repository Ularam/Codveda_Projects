# Data Science Job Postings (Glassdoor) - Data Cleaning & Preprocessing Project



## 📌 Project Overview

This project demonstrates **end-to-end data cleaning and preprocessing** on a real-world, messy dataset of **Data Science job postings** scraped from Glassdoor (~672 rows).  

The raw data contains typical scraped-data issues: inconsistent salary formats, placeholders (`-1`), appended ratings in company names, missing values, outliers, and unstructured categorical variables.  

The goal was to transform this noisy dataset into a clean, analysis-ready format suitable for exploratory data analysis (EDA), visualization, or machine learning tasks (e.g., salary prediction).

## 📊 Dataset

- **Source**: [Data Science Job Posting on Glassdoor](https://www.kaggle.com/datasets/rashikrahmanpritom/data-science-job-posting-on-glassdoor) (Kaggle)
- **File**: `Data_jobs.csv`
- **Key Columns**: Job Title, Salary Estimate, Company Name, Location, Rating, Industry, Sector, Revenue, Size, etc.

## 🛠️ Key Preprocessing Steps

1. **Initial Cleaning**
   - Replaced placeholders (`-1`, `-1.0`, empty strings) with `NaN`
   - Cleaned company names (removed appended ratings like `\n3.8`)
   - Calculated company age from `Founded` year

2. **Feature Engineering: Salary Parsing**
   - Built a robust parser to extract:
     - `min_salary`
     - `max_salary`
     - `avg_salary` (in thousands, $K)
   - Handled multiple formats:
     - `$70K-$130K (Glassdoor est.)`
     - `Employer Provided Salary:$90K-$120K`
     - Rare hourly rates (converted to annual)

3. **Missing Data Handling**
   - Dropped columns with >50% missing values (e.g., Competitors)
   - Numerical features → imputed with **median**
   - Categorical features → imputed with **most frequent**

4. **Outlier Treatment**
   - Detected outliers in salary and rating columns using **IQR method**
   - Applied clipping (capping) to preserve data

5. **Categorical Encoding**
   - Applied **one-hot encoding** to nominal categories (Job Title, Location, Industry, Sector, Size, Revenue, etc.)

6. **Numerical Scaling**
   - Standardized numerical features (salaries, rating, company age) using **StandardScaler**

## 🐍 Tools & Libraries

- Python
- pandas
- NumPy
- scikit-learn (SimpleImputer, StandardScaler)


