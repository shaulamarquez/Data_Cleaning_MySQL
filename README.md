# Layoffs Data Cleaning with SQL
This project showcases a comprehensive SQL-based data cleaning process performed on a dataset containing global tech layoffs. The primary goal was to prepare the data for analysis by handling duplicates, nulls, inconsistencies, and formatting issues.

# Dataset
The original dataset includes details on:

* Company name

* Location and country

* Industry

* Total laid off employees

* Percentage laid off

* Date of layoffs

* Company stage

* Funds raised

# Tools Used
* SQL (MySQL syntax)

* SQL window functions (ROW_NUMBER)

* String and date functions (TRIM, STR_TO_DATE)

* CTEs (Common Table Expressions)

# Data Cleaning Steps
1. Create a Staging Table
Created a duplicate staging table (layoffs_staging) to preserve the original dataset and conduct cleaning safely.

2. Remove Duplicate Records
Used ROW_NUMBER() to identify duplicate rows based on key columns and removed them.

3. Standardize and Trim Text
* Removed trailing/leading spaces from text fields.

* Standardized entries

* Cleaned country names like "United States." to "United States".

4. Format and Convert Dates
Converted date strings to DATE type using STR_TO_DATE.


5. Handle Missing or Null Values
* Converted blank strings in industry to NULL.

* Used self-joins to fill in missing industry values from the same company.

* Deleted rows with both total_laid_off and percentage_laid_off missing.

6. Final Cleanup
Dropped helper column row_num used during the deduplication process.

# Final Output
The cleaned dataset (layoffs_staging2) is now ready for deeper analysis and insights on layoff trends across companies, industries, and countries.

# Next Steps
Potential next steps include:

* Creating visualizations on layoff trends.

* Performing time series analysis.

* Joining with external economic indicators for correlation insights.

Credits
Inspired by real-world tech layoffs datasets. Cleaning process inspired by best practices in data engineering.


