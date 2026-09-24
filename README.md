# Student Performance Analysis

## Project Overview

This project performs **Student Performance Analysis** using a dataset containing 100 student records. The dataset includes information about students such as age, gender, course, semester, subject-wise marks, and attendance percentage.

The main objective of this project is to transform raw student data into meaningful information by following a complete **Data Analytics workflow**. The analysis focuses on data cleaning, feature creation, Key Performance Indicators (KPIs), exploratory data analysis, performance drivers, risk identification, and actionable recommendations.

The project demonstrates how data analytics can help educational institutions understand student performance, identify students who may require academic support, and make data-driven decisions.

---

## Project Objectives

The major objectives of this project are:

* Clean and prepare the raw student dataset.
* Identify and remove duplicate records.
* Check the dataset for missing values and data quality issues.
* Create useful derived features such as Total Marks and Average Marks.
* Calculate important student performance KPIs.
* Analyze student performance by course, semester, gender, and subject.
* Study the relationship between attendance and academic performance.
* Identify students who may be at academic risk.
* Categorize students into High, Medium, and Low risk groups.
* Identify performance trends, drivers, risks, and opportunities.
* Provide practical recommendations based on the analysis.
* Present the results using charts and data-driven insights.

---

## Dataset

The dataset contains **100 student records and 10 columns**. It also contains duplicate records that are identified and removed during the data-cleaning stage.

### Dataset Fields

| Field                | Description                                             |
| -------------------- | ------------------------------------------------------- |
| `Student_ID`         | Unique identifier assigned to each student              |
| `Name`               | Name of the student                                     |
| `Age`                | Age of the student                                      |
| `Gender`             | Gender of the student                                   |
| `Course`             | Student's course such as BCA, BSc IT, BSc CS, or BSc AI |
| `Semester`           | Current semester of the student                         |
| `Maths_Marks`        | Marks obtained in Mathematics out of 100                |
| `AI_Marks`           | Marks obtained in Artificial Intelligence out of 100    |
| `Python_Marks`       | Marks obtained in Python out of 100                     |
| `Attendance_Percent` | Student attendance percentage                           |

### Dataset Source

The raw dataset used for this project is:

`student_100_records_with_duplicates.xlsx`

The dataset contains **100 rows**, including **3 exact duplicate records**.

---

## Data Analytics Pipeline

The project follows the following analytics workflow:

```text
Raw Student Data
       ↓
Data Cleaning
       ↓
Duplicate Detection & Removal
       ↓
Missing Value Checking
       ↓
Feature Creation
       ↓
KPI Calculation
       ↓
Exploratory Data Analysis
       ↓
Driver Analysis
       ↓
Risk Analysis
       ↓
Insights
       ↓
Opportunities
       ↓
Recommended Actions
```

---

# 1. Data Cleaning

The first stage of the project is to inspect and clean the raw dataset.

The following activities are performed:

* Load the Excel dataset using Pandas.
* Inspect the number of rows and columns.
* Check column names and data types.
* Check for missing values.
* Identify exact duplicate rows.
* Identify duplicate `Student_ID` values.
* Remove exact duplicate records.
* Create a cleaned dataset for further analysis.

### Duplicate Handling

The original dataset contains:

```text
Original Records: 100
Duplicate Records: 3
Cleaned Records: 97
```

The duplicate rows are removed using Pandas so that the analysis is not affected by repeated records.

---

# 2. Feature Creation

After cleaning the dataset, additional features are created to make the analysis more meaningful.

### Total Marks

The `Total_Marks` feature is calculated using:

```text
Total_Marks = Maths_Marks + AI_Marks + Python_Marks
```

The maximum possible total is:

```text
300
```

### Average Marks

The `Average_Marks` feature is calculated using:

```text
Average_Marks = Total_Marks / 3
```

This gives the student's average score across the three subjects.

These derived features make it easier to compare overall student performance.

---

# 3. Key Performance Indicators (KPIs)

The project calculates important KPIs to provide an overall summary of student 
The major KPIs include:

Average Marks:
Shows the average academic performance of all cleaned student records.

Average Attendance:
Shows the average attendance percentage across students.

Pass Rate
Shows the percentage of students who satisfy the defined passing criteria.

Number of Students:
Shows the total number of unique student records after cleaning.

Risk Distribution:
Shows the number and percentage of students classified into:

* High Risk
* Medium Risk
* Low Risk

These KPIs provide a quick overview of the academic condition of the student population.

4. Exploratory Data Analysis
Exploratory Data Analysis (EDA) is performed to understand patterns and differences within the dataset.

The analysis covers:

Course-wise Analysis:
Student performance is compared across:

* BCA
* BSc IT
* BSc CS
* BSc AI
This helps identify differences in average marks and attendance between courses.

Semester-wise Analysis:
Performance is analyzed across semesters 1 to 4.
This helps identify whether average performance or attendance changes across different semesters.

Gender-wise Analysis:
The dataset is also analyzed by gender to understand the distribution and average performance of the available groups.

Subject-wise Analysis:
The three subjects are compared:

* Mathematics
* Artificial Intelligence
* Python

This helps identify which subject has relatively higher or lower average performance.

5. Driver Analysis:

Driver analysis is used to understand factors that may be associated with student performance.
One important factor examined in this project is:

```text
Attendance Percentage
        ↓
Average Marks


The correlation between attendance and average marks is calculated.

Correlation helps describe the strength and direction of the linear relationship between the two numerical variables.

A scatter plot is also used to visually examine the relationship between attendance and academic performance.

Important Note
Correlation indicates an association between variables. It does not by itself prove that attendance causes higher or lower marks.

6. Risk Analysis
A risk category is created to identify students who may require additional academic attention.
Students are classified using their academic performance and attendance.

The categories are:
High Risk:
Students showing relatively low academic performance and/or low attendance according to the defined project thresholds.

Medium Risk:
Students showing moderate academic or attendance concerns.

Low Risk:

Students meeting stronger academic and attendance conditions according to the defined thresholds.
The exact thresholds used in the analysis are documented in the project code.
The risk categorization is intended as an analytical indicator to support further review and not as a permanent judgment about any student.


7. Visualizations
The project uses Matplotlib to create visualizations that communicate important findings.
The main visualizations include:

Course Comparison:
Compares average student performance across different courses.

Semester Comparison
Compares average performance across semesters.

Attendance vs Average Marks:
A scatter plot showing the relationship between attendance percentage and average marks.

Risk Distribution:
Shows the distribution of students across High, Medium, and Low risk categories.
These visualizations help convert numerical analysis into an easier-to-understand format.

8. Business Intelligence Flow:
The project follows a simple Business Intelligence approach:

Data
 ↓
Cleaning
 ↓
Analysis
 ↓
Visualization
 ↓
Insights
 ↓
Decision Support
The purpose is not only to calculate statistics but also to convert the results into information that can support academic decision-making.

For example:

Low Attendance
       +
Low Average Marks
       ↓
Identify At-Risk Students
       ↓
Provide Academic Support
       ↓
Monitor Future Performance

9. Insights:
The analysis is used to identify important patterns such as:

* Overall student academic performance.
* Course-wise performance differences.
* Semester-wise performance patterns.
* Subject-wise performance differences.
* Attendance patterns.
* Relationship between attendance and average marks.
* Distribution of students across risk categories.
* Students requiring additional academic attention.

The final numerical findings and observations are documented in the project report.

10. Opportunities

The analysis can help identify opportunities for improving student outcomes.
Possible opportunities include:

* Providing additional support to students with low marks.
* Monitoring attendance regularly.
* Conducting additional practice sessions for weaker subjects.
* Providing subject-specific academic resources.
* Tracking performance across semesters.
* Identifying students who improve or decline over time.
* Using dashboards or automated reports for continuous monitoring.

These opportunities are based on the patterns identified from the dataset and should be evaluated with additional institutional information before implementation.

11. Recommended Actions
Based on the analytical findings, educational institutions can consider actions such as:

1. Monitor Attendance
   Regularly monitor students with low attendance percentages.

2. Academic Support
   Provide additional learning resources or mentoring to students showing lower academic performance.

3. Subject-Specific Support
   Identify subjects with lower average marks and organize additional practice or revision sessions.

4. Early Risk Identification
   Use academic and attendance indicators to identify students who may need early intervention.

5. Continuous Monitoring
   Compare student performance across semesters to identify changes over time.

6. Data-Driven Decision Making
   Use KPIs and visualizations to support academic planning rather than relying only on individual observations.


12. Project Outputs
The project produces the following outputs:

| File                                       | Purpose                                                    |
| ------------------------------------------ | ---------------------------------------------------------- |
| `student_100_records_with_duplicates.xlsx` | Raw input dataset                                          |
| `student_analysis.ipynb`                   | Complete Python analysis notebook                          |
| `requirements.txt`                         | Python libraries required to run the project               |
| `cleaned_student_data.csv`                 | Cleaned dataset with engineered features and risk category |
| `analysis_charts.png`                      | Generated data visualizations                              |
| `report.md`                                | Detailed project findings and recommendations              |

If the submission requires exactly four files, the final repository should contain only the files specified by the internship instructions.


13. Technologies Used

The project is implemented using Python and the following libraries:
  Python— Programming language used for data analysis.
  Pandas— Data loading, cleaning, transformation, and analysis.
  Matplotlib — Data visualization.
  OpenPyXL — Used by Pandas to read Excel files.


14. Requirements
The required Python libraries are:

pandas
matplotlib
openpyxl


15. How to Run the Project
Google Colab

1. Open Google Colab.
2. Upload `student_analysis.ipynb`.
3. Upload the Excel dataset:

student_100_records_with_duplicates.xlsx

4. Make sure the Excel file is available in the Colab runtime.
5. Run the notebook cells from top to bottom.
6. Review the cleaning results.
7. Review the calculated KPIs.
8. Review the EDA visualizations.
9. Review the driver and risk analysis.
10. Generate the final outputs.

Then open:
student_analysis.ipynb

Place the Excel dataset in the same working directory or update the file path in the notebook.
Run all cells sequentially.


16. Example Project Structure
Student-Performance-Analysis/
│
├── student_analysis.ipynb
├── requirements.txt
├── README.md
├── student_100_records_with_duplicates.xlsx
│
├── cleaned_student_data.csv
├── analysis_charts.png
└── report.md

17. Conclusion
This project demonstrates a complete student performance data analytics workflow, starting from raw Excel data and progressing through data cleaning, feature engineering, KPI calculation, exploratory analysis, driver analysis, risk identification, visualization, and recommendations.
The project shows how structured student data can be transformed into meaningful insights that can support academic monitoring and data-driven decision-making.
The analysis also demonstrates the importance of maintaining clean data, selecting relevant KPIs, using appropriate visualizations, and interpreting analytical results carefully.


Author:Dhanashree Rodi
BSc Artificial Intelligence Student

Project Type:
Data Analytics with AI — Student Performance Analysis

Skills Demonstrated:

* Data Cleaning
* Data Preprocessing
* Exploratory Data Analysis
* Feature Engineering
* KPI Analysis
* Statistical Analysis
* Correlation Analysis
* Data Visualization
* Risk Analysis
* Insight Generation
* Data-Driven Recommendations
* Python
* Pandas
* Matplotlib
* Excel Data Analysis
