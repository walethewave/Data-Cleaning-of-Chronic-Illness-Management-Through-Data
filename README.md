# Data-Cleaning-of-Chronic-Illness-Management-Through-Data

The data is too large , this is the link to the dataset
https://www.kaggle.com/datasets/flaredown/flaredown-autoimmune-symptom-tracker/data
# Data Cleaning Readme

## Overview

This document outlines the steps taken to clean and preprocess the dataset for analysis. The dataset used is a comprehensive log of user check-ins with various attributes such as age, sex, country, check-in date, and trackable items.

## Steps Taken

1. **Handling Mixed Data Types**: Upon initial import, columns such as 'trackable_value' raised a DtypeWarning due to mixed types. This was addressed by specifying dtype options or setting `low_memory=False` during import.

2. **Data Conversion and Formatting**:
   - **User ID Categorization**: Converted the 'user_id' column to categorical codes for efficient handling.
   - **Date Conversion**: Converted 'checkin_date' to datetime format to facilitate date-based analysis.
   - **Extracted Date Components**: Created new columns ('checkin_year', 'checkin_month', 'checkin_day') from 'checkin_date' to enable time-series analysis.

3. **Handling Missing Values**:
   - **Age, Sex, and Country**: Imputed missing values in 'age', 'sex', and 'country' columns using mean (for age) and mode (for sex and country).

4. **Additional Data Transformations**:
   - **Mapped Months**: Created a mapping of numeric months to month names for better readability ('checkin_month_name').

5. **Data Quality Checks**:
   - **Unique Values and Missing Data**: Checked unique values and missing data counts across columns ('trackable_value', 'trackable_name') to identify and handle inconsistencies.

6. **Descriptive Statistics**:
   - **Age Distribution**: Described the statistical distribution of 'age' to understand its range and central tendency.

7. **Visualization**:
   - **Trackable Type Distribution**: Visualized the distribution of 'trackable_type' using a bar chart to explore categorical data patterns.

8. **Final Dataset Information**:
   - **Dataset Size and Structure**: Confirmed the final dimensions of the dataset (7976223 rows, 13 columns) after cleaning and preprocessing.

## Conclusion

The data cleaning process involved handling mixed data types, converting formats, imputing missing values, and ensuring data integrity for further analysis. These steps were crucial to prepare the dataset for exploratory data analysis (EDA) and modeling.

