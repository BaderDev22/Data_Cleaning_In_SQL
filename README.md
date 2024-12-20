# SQL Project - Data Cleaning

## Project Overview
This project involves cleaning and preparing a dataset sourced from Kaggle on layoffs in 2022. The dataset, located [here](https://www.kaggle.com/datasets/swaptr/layoffs-2022), contains information about layoffs across various companies worldwide.

## Steps Undertaken
1. **Data Staging**
   - Created a staging table `layoffs_staging` to retain raw data.
   - Duplicated data into `layoffs_staging` for cleaning operations.

2. **Removing Duplicates**
   - Identified and removed duplicates based on specific columns (`company`, `location`, `industry`, etc.).

3. **Standardizing Data**
   - Handled inconsistencies in `industry` names (e.g., standardized variations of "Crypto" industry).
   - Corrected format discrepancies in `country` names (e.g., removed trailing periods).
   - Converted `date` column to proper date format using `STR_TO_DATE`.

4. **Handling Null Values**
   - Addressed null values in `industry` by updating where possible based on other records for the same `company`.
   - Retained nulls in numeric columns (`total_laid_off`, `percentage_laid_off`, `funds_raised_millions`) for ease during exploratory data analysis.

5. **Removing Unnecessary Data**
   - Deleted rows with missing critical information (`total_laid_off`, `percentage_laid_off`).
   - Cleaned up the staging table by removing auxiliary columns used during cleaning (`row_num`).

## Conclusion
The dataset (`layoffs_staging2`) is now prepared for further analysis and modeling tasks. It has been cleansed of duplicates, standardized for consistency, and prepared with minimal null values to facilitate robust analytical insights.

## Next Steps
- Proceed to exploratory data analysis (EDA) to uncover trends and insights.
- Prepare for modeling or reporting as per project requirements.

## Additional Notes
- Ensure data integrity throughout by documenting all steps and validating changes.
- Consider automating some cleaning steps for future data updates.

This README provides a comprehensive overview of the steps taken to clean and prepare the dataset. For further details, refer to the SQL scripts and queries used in the process.
