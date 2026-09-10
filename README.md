# Café Sales Data Cleaning Using Power Query

## Overview

This project demonstrates the cleaning and preparation of a **café sales dataset using Power BI and Power Query**.

The raw dataset, `dirty_cafe_sales.csv`, contains **10,000 transaction records** with several data quality issues such as missing values, `ERROR` and `UNKNOWN` entries, incorrect data types, extra spaces, hidden characters, and invalid values.

The objective of this project is to transform the raw dataset into a **clean, consistent, and analysis-ready dataset**.

## Problem Statement

A retail company receives sales data containing incomplete and inconsistent records. Before the data can be used for business reporting, it must be cleaned and standardized.

Power Query was used to identify and resolve these data quality issues through a sequence of **22 transformation steps**.

## Dataset Information

**Dataset:** `dirty_cafe_sales.csv`

**Records:** 10,000

### Columns

* Transaction ID
* Item
* Quantity
* Price Per Unit
* Total Spent
* Payment Method
* Location
* Transaction Date

## Tools Used

| Tool        | Purpose                          |
| ----------- | -------------------------------- |
| Power BI    | Data analysis and reporting      |
| Power Query | Data cleaning and transformation |
| CSV         | Source data                      |

## Data Cleaning Process

The following major operations were performed in Power Query:

### Data Preparation

* Imported the CSV file into Power BI.
* Initially kept columns as Text.
* Promoted the first row as headers.
* Replaced `ERROR` and `UNKNOWN` values with blanks.

### Data Type Correction

Appropriate data types were assigned:

* Quantity → Number
* Price Per Unit → Decimal Number
* Total Spent → Decimal Number
* Transaction Date → Date
* Descriptive fields → Text

### Missing Value Handling

Missing values were handled using calculations wherever possible.

```text
Total Spent = Quantity × Price Per Unit
```

```text
Quantity = Total Spent ÷ Price Per Unit
```

```text
Price Per Unit = Total Spent ÷ Quantity
```

The cleaning process handled:

* 173 missing Total Spent values
* 138 missing Quantity values
* 179 missing Price Per Unit values
* 333 missing Item values
* 2,579 missing Payment Method values
* 3,265 missing Location values
* 159 records with missing Transaction Date

### Data Quality Improvements

Additional transformations included:

* Removing unnecessary columns
* Renaming columns
* Rechecking data types
* Replacing missing Item values
* Replacing missing Payment Method values
* Handling missing Location values
* Removing records with missing dates
* Checking duplicate records
* Trimming extra spaces
* Removing hidden/non-printable characters
* Removing invalid Quantity values
* Removing invalid Price values

## Transformation Workflow

```text
Raw Café Sales Data
        ↓
Import into Power BI
        ↓
Power Query Editor
        ↓
Handle ERROR / UNKNOWN values
        ↓
Correct Data Types
        ↓
Handle Missing Values
        ↓
Calculate Missing Sales Values
        ↓
Clean Text Data
        ↓
Remove Invalid Records
        ↓
Check Duplicates
        ↓
Final Clean Dataset
        ↓
Ready for Power BI Analysis

## Key Results

After the cleaning process:

* Data types were standardized.
* Incorrect placeholder values were handled.
* Missing values were calculated or replaced where appropriate.
* Invalid quantity and price records were removed.
* Text fields were standardized.
* Extra spaces and hidden characters were removed.
* Duplicate records were checked.
* The dataset became more consistent and reliable.

## Business Insights

The cleaned dataset can support future analysis of:

* Café sales performance
* Product/item performance
* Pricing
* Payment methods
* Location-based sales
* Transaction trends
* Inventory requirements
* Customer preferences

Clean and reliable data helps reduce reporting errors and supports better business decisions.



## Outcome

The project successfully transformed the raw café sales dataset into a **clean, organized, and analysis-ready dataset** using Power Query.

This experiment demonstrates how Power Query can be used to systematically identify and resolve common data quality problems before performing business analysis.
