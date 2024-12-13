# Real-Estate-Business-Project-Power-BI-en:
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Business Case:
In this case study, I delved into a company with diversified ventures across various product ranges and a prominent presence in the real estate sector. The company’s global business head wants to use a dashboard that helps to track key metrics about their nine business unit managers (executives), products, Sales, Quantities sold, and gross margins (GM) from the year 2005-2014.

**Steps:**

#1 - **Extract, Load, Transform (ELT)**:
I began by downloading the dataset from the provided link **https://drive.google.com/drive/folders/1eplz7vmnNG67KECek0CUAyFaVxm4ngc2?usp=sharing**
and initiated the Extract-Load-Transform (ELT) process. Leveraging Power BI's capabilities, I extracted the data, loaded it into the Power BI environment, and transformed it. Using **Power Query Editor**, I cleaned unused or erroneous rows, rectified datatype discrepancies, and resolved any other data-related issues to ensure data accuracy and consistency.

#2 - **Data Modeling**:
Given the normalized database structure, with multiple tables representing distinct data points, I utilized Power BI's data modeling capabilities to establish coherent relationships among these tables. Leveraging Power BI's Relationship View, I defined and managed relationships, ensuring that the final schema reflected a cohesive structure facilitating seamless data interaction.

![Schema ](https://github.com/Arash-Kamboj/Real-Estate-Business-Project-Power-BI-/assets/156613048/fd873750-d33d-40ab-af6f-6aa9a7628ae7)


#3 - **Visual Level Filters with Slicer**:
After ensuring data quality and consistency, I utilized Power BI's visualization tools and implemented visual level filters using slicers. I configured slicers with multi-selection options and included a "Select All" option, enhancing user flexibility and analytical depth.

#4 - **Donut Chart for Gross Margin Contribution**:
After that, created a donut chart, visually representing the percentage contribution of Gross Margin to Total Gross Margin. Leveraging **Power BI's DAX** (Data Analysis Expressions) language, I computed Total Sales using the **Total Sales =  (Sum_Markdown_Sales_Dollars * Sum_Markdown_Sales_Units) + (Sum_Regular_Sales_Dollars * Sum_Regular_Sales_Units)** formula, incorporating both markdown and regular sales data.

#5 - **Revenue and Expense Analysis**:
Leveraging Power BI's analytical capabilities, I conducted a comprehensive analysis of revenue and expenses. Using DAX functions,  calculated Total Quantity (Units) by aggregating markdown and regular sales units. 
Management has an interest analysing newly launched 'Home category' for high margin transactions. So, focusing on the 'Home category' for high-margin transactions, I identified home sales with a gross margin exceeding 10% using Power BI's filtering and conditional formatting features.

#6 - **Table Chart for Gross Margin Scenarios**:
Developed a table chart, presenting the sum of Gross Margin for two distinct scenarios based on sales data. 
Scenario 1 occurs when due to lesser inventory, all the ordered goods were not delivered to the customer.
Scenario 2 occurs when all the ordered goods were delivered to the customer, thanks to optimized inventory levels maintained. 
Management wants to know that out of total gross margin availed, what percentage is due to the transactions that occurred due to Scenario 1. Thus Gross Percentage is obtained by dividing Gross Margin of Scenario 1 by Sum of Gross Margin Amount, subsequently multiplying with 100.

#7 - **Drill Down Capability for Rent Analysis**:
Utilizing Power BI's drill-down capabilities, I implemented a hierarchical structure ranging from Year to Quarter to Month levels for analyzing total rent obtained over time. I plotted charts with interactive drill-down functionality, enabling in-depth analysis and visualization.

The developed dashboard aims to offer actionable insights and facilitate informed decision-making for the company's leadership and stakeholders.

![Real State Busniess project ](https://github.com/Arash-Kamboj/Real-Estate-Business-Project-Power-BI-/assets/156613048/78460da7-917b-4e15-9e1a-ef7167aa85c4)
------------------------------------------
**Analysis and key finding of the project**

Some of the key findings from the Power BI dashboard for the Real Estate Business Project:

- The territory with the highest sales is PA.
- The total sales amount for the PA territory is 27.27 million,percentage contribution of PA territory sales to the total sales is 33.06%
- The strongest non-zero quarter for PA territory in 2014 is Quarter 2.
- The territory with the lowest sales is SC, with 988.93K total sales.
- Territory WV has the highest total sales of homes category with 8.93 Million of total homes sale and percentage contribution in this category of 33.29%
- The sales in Home category went through various fluctuations which could be influenced by various factors such as market conditions, economic changes, or property 
  management decisions.
- **Notable Home Sales trend-**
  **Increasing trend from 2006 to 2008.
  Sharp decrease in 2010.
  Rise again in 2012.
  Decline in 2014.**

- For the period years lower than 2010  during which stores have been opened, at which time (year, quarter, month) lowest rent was generated and how much?
(Note - Considering only the quarter and months which are in the year having the lowest rent and having atleast value greater than 0)
Answer -  
Year -  2007
Amount - 5,19,902
Quarter - 3
Amount - 1,33,521
Month - November 
Amount - 48,286

- The global business head is always on the lookout to expand the business to various new industries in existing regions where penetration is low.
For territories SC, NC, GA, OH and KY, what is the total number of units sold? 
Answer - 
Total Number of Units Sold: 169,010 units (169.01K)

---------------------------------------------------------------------------------------------------------------------------------------------------------------



------------------------------------------------------------------------------------------------------------------------------------------------------------------------




