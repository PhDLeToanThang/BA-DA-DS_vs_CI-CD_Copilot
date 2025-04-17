# Student Performance Analysis with Power BI

## Overview

This Power BI project aims to analyze student performance data and derive insights to improve educational outcomes. The dataset includes information such as gender, race/ethnicity, parental level of education, lunch type, test preparation course completion, and scores in math, reading, and writing. This README provides an overview of key insights, DAX measures, and visualization suggestions derived from the analysis.

## Key Insights and DAX Measures

1. **Overall Performance:**
   - DAX Measure: `Overall Performance = AVERAGE('Case Study Table'[math_score] + 'Case Study Table'[reading_score] + 'Case Study Table'[writing_score])`
   - Description: Assess the overall academic performance of students across all subjects.

2. **Performance Gap:**
   - DAX Measure: `Performance Gap = ABS(AVERAGE('Case Study Table'[math_score]) - AVERAGE('Case Study Table'[reading_score]))`
   - Description: Identify the performance gap between different subjects.

3. **Test Preparation Impact:**
   - DAX Measure: `Test Preparation Impact = IF(ISBLANK(AVERAGE('Case Study Table'[test_preparation_course])), "No Course", "Course Completed")`
   - Description: Measure the impact of completing a test preparation course on overall performance.

4. **Gender Performance Disparity:**
   - DAX Measure: `Gender Performance Disparity = ABS(AVERAGE('Case Study Table'[math_score]) - AVERAGE('Case Study Table'[reading_score]))`
   - Description: Evaluate if there's a significant difference in performance between genders.

5. **Parental Education Influence:**
   - DAX Measure: `Parental Education Influence = IF(AVERAGE('Case Study Table'[parental_level_of_education]) = "Bachelor's Degree", "Bachelor's Degree", IF(AVERAGE('Case Study Table'[parental_level_of_education]) = "Master's Degree", "Master's Degree", "Other"))`
   - Description: Determine if parental level of education correlates with student performance.

## Visualization Suggestions

1. **Overall Performance:**
   - Visualization: Horizontal bar chart or bullet chart.

2. **Performance Gap:**
   - Visualization: Stacked bar chart or waterfall chart.

3. **Test Preparation Impact:**
   - Visualization: Pie chart or stacked column chart.

4. **Gender Performance Disparity:**
   - Visualization: Grouped bar chart or box plot.

5. **Parental Education Influence:**
   - Visualization: Clustered column chart or stacked bar chart.

These visualization suggestions aim to effectively communicate the insights derived from the DAX measures and facilitate data-driven decision-making in the educational context.

## Usage

1. Import the student performance dataset into Power BI.
2. Create DAX measures for each key insight using the provided expressions.
3. Utilize the DAX measures and visualization suggestions to analyze and visualize student performance data effectively.

