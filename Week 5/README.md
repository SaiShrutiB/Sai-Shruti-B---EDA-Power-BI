# Power BI Week 5 – Healthcare Data Cleaning and Data Modeling

##  Overview

This project focuses on cleaning and preparing a healthcare dataset using Power Query in Power BI. The cleaned data was then organized into dimension tables and a billing fact table to create a structured data model.

##  Objectives

- Clean and standardize the healthcare dataset
- Standardize categorical text fields
- Create age group categories
- Create Patient ID and Admission ID
- Create patient and admission dimension tables
- Create the Billing fact table
- Build relationships between the tables

##  Tools & Technologies

- Power BI Desktop
- Power Query
- Healthcare Dataset
- Data Modeling

##  Data Cleaning

The categorical columns were cleaned using **Trim** and **Clean** transformations to remove unnecessary spaces and unwanted characters.

The Name column was standardized using **Capitalize Each Word**.

The Date of Admission and Discharge Date columns were converted to the **Date** data type.

The provided dataset did not contain a Diagnostic Code column, so no transformation was applied to that field.

##  Age Group

A conditional column named **Age Group** was created using the following categories:

- 0-18
- 19-35
- 36-60
- 60+

This makes it easier to analyze patients based on different age ranges.

##  Data Model

The healthcare dataset was organized into the following tables:

### Dim_Patient

- Patient ID
- Name
- Age
- Gender
- Blood Type
- Age Group

### Dim_Admission

- Admission ID
- Admission Type
- Doctor
- Hospital
- Medical Condition
- Medication
- Room Number
- Test Results

### Billing

- Patient ID
- Admission ID
- Billing Amount
- Date of Admission
- Discharge Date
- Insurance Provider

##  Relationships

The dimension tables were connected to the Billing table using:

- `Dim_Patient[Patient ID]` → `Billing[Patient ID]`
- `Dim_Admission[Admission ID]` → `Billing[Admission ID]`

This creates a structured model where patient and admission details can be analyzed along with billing information.

##  Files

- `WEEK 5 - Sai Shruti B.pdf` – Week 5 report with screenshots
- `healthcare dataset.csv` – Healthcare dataset
- `week 5 - Sai Shruti B - powerbi eda.pdf` – Power BI project file

##  Outcome

The healthcare dataset was cleaned, standardized and transformed into a structured data model. The prepared model can be used for creating DAX measures and an interactive dashboard in the next stage.
