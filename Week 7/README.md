# Power BI Week 7 – Student Performance Data Preparation and Analysis

##  Overview

This project focuses on cleaning, transforming, and preparing a Student Performance dataset using Power BI. Power Query was used to clean the data, create calculated columns, and organize student information and subject-wise marks into separate tables. DAX measures were created to analyze academic performance.

##  Objectives

- Import and clean the Student Performance dataset.
- Create a unique Student ID.
- Calculate Total Marks and Average Marks.
- Categorize students based on their average marks.
- Create Pass/Fail results.
- Create separate StudentMarks and StudentDetails tables.
- Unpivot subject scores for subject-wise analysis.
- Create DAX measures for academic performance.
- Prepare the data model for the Week 8 dashboard.

##  Tools and Technologies

- Power BI Desktop
- Power Query Editor
- DAX (Data Analysis Expressions)
- Student Performance Dataset

##  Data Cleaning and Transformation

The dataset was imported into Power BI and opened in Power Query Editor.

The following transformations were performed:

- Cleaned text data.
- Added an Index Column and renamed it **Student ID**.
- Reordered columns for better organization.
- Created calculated columns for Total Marks, Average Marks, Grade, and Result.

##  Calculated Columns

### 1. Total Marks

Calculated by adding the Math, Reading, and Writing scores.

### 2. Average Marks

Calculated by dividing Total Marks by 3.

### 3. Grade

Created a conditional column to categorize students into the following grades based on their average marks:

- A
- B
- C
- F

### 4. Result

Created a Pass/Fail column based on the Average Marks.

##  StudentMarks Table

A separate `StudentMarks` table was created to organize subject-wise scores.

The Math, Reading, and Writing columns were unpivoted into the following structure:

- Student ID
- Subject
- Score

This structure supports comparisons between the three subjects.

##  StudentDetails Table

A separate `StudentDetails` table was created to store student background information.

The table contains:

- Student ID
- Gender
- Race/Ethnicity
- Parental Level of Education
- Lunch
- Test Preparation Course

##  DAX Measures

The following measures were created and stored in the Measures Student table.

### Average Math Score

```DAX
Average Math Score =
AVERAGE(StudentsPerformance[math score])
```

### Average Reading Score

```DAX
Average Reading Score =
AVERAGE(StudentsPerformance[reading score])
```

### Average Writing Score

```DAX
Average Writing Score =
AVERAGE(StudentsPerformance[writing score])
```

### Overall Average Score

```DAX
Overall Average Score =
DIVIDE(
    [Average Math Score] +
    [Average Reading Score] +
    [Average Writing Score],
    3
)
```

### Overall Pass %

```DAX
Overall Pass % =
DIVIDE(
    CALCULATE(
        COUNT(StudentsPerformance[Result]),
        StudentsPerformance[Result] = "Pass"
    ),
    DISTINCTCOUNT(StudentsPerformance[Student ID]),
    0
)
```

##  Data Model

The data model contains the following tables:

- `StudentsPerformance` – Main student performance dataset.
- `StudentMarks` – Subject-wise student scores.
- `StudentDetails` – Student demographic and background details.
- `Measures Student` – Stores DAX measures used for analysis.

##  Files

- `WEEK 7 - Sai Shruti B.pdf` – Week 7 assignment report with screenshots.

##  Outcome

The Student Performance dataset was cleaned and transformed using Power Query. Calculated columns, separate tables for subject marks and student details, and DAX measures were created. The prepared data model provides the foundation for building the interactive Student Performance Dashboard in Week 8.

