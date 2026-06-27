# Automated Data Quality Validation Project

## Project Overview

This project demonstrates how to validate and clean a customer dataset before machine learning model training.

The project detects and fixes common data quality issues such as:

- Missing values
- Duplicate rows
- Outliers
- Invalid ranges
- Wrong data types

## Dataset Columns

- customer_id
- age
- income
- purchases

## Problems Detected

| Issue | Example |
|---|---|
| Missing values | Income values missing |
| Duplicate rows | Same customer records repeated |
| Outlier | Income nearly 1 billion |
| Invalid range | Age = -5 |
| Wrong data type | Purchases = "ABC" |

## Workflow

1. Create raw dataset
2. Generate quality report before cleaning
3. Detect missing values
4. Detect duplicate rows
5. Detect invalid age values
6. Detect wrong data types
7. Detect income outliers using IQR
8. Clean the dataset
9. Generate quality report after cleaning
10. Save the cleaned dataset

## Cleaning Strategy

| Problem | Solution |
|---|---|
| Duplicate rows | Drop duplicates |
| Invalid age | Remove negative age values |
| Wrong purchases type | Convert to numeric |
| Invalid purchases | Drop invalid rows |
| Income outlier | Clip using IQR |
| Missing income | Fill with median |

## Key Learning

Bad data can damage machine learning models. Data validation should happen before model training to avoid wrong predictions and pipeline failures.

## Tools Used

- Python
- Pandas
- NumPy

## Output Files

- raw_customer_data.csv
- clean_customer_data.csv
- quality_report_before.csv
- quality_report_after.csv
