# Employee Attrition and Turnover Dashboard
<img src="/image/HR Dashbord.JPG" alt="App interface" width="1000" height="600">

# Overview
This project was done using Power BI.
See below the business proposal and the necessary data preprocessing steps that were taken. Find a The PowerBI file and a PDF version of the dashboard in src folder.

# Executive Summary
In our ever-changing world, employees face various challenges, and all these attrition stand out the most as this is one of the significant observations in today's workforce. Despite the external changes to a company, attrition is a critical player in the internal environment of any company. Attrition is the percentage of employees that choose to leave per year compared to those who wish to stay. This is the gradual depletion of employee size over time. It is termed turnover when there is a gap in the hiring-to-resignation ratio. Employee attrition is the resignation, retirement or in any instance where there is a managerial decision not to rehire for a particular position. The greatest fear of any employer is to spend short amounts of resources on training an employee only for him/her to up and leave the following year without giving an equivalent of the worth spent on their training. This action creates a financial and technical vacuum in the company's workforce strength. Human resource personnel find this one of the most significant difficulties. Human resource managers are always at managers' disposal once they are highly skilled in identifying employee attrition, as this is one of their steps to reducing its percentage within their company. Employees leave for several reasons, most of which are generic across a sector, but most times, the key reasons are particular to the firm in question. Most of these reasons are undisclosed, ranging from a variety of reasons such as job security, financial satisfaction, growth on a career path, supervisory concerns, personal issues and sometimes the urge for more significant challenges. This project seeks to highlight the key reasons why employee attrition occurs, to begin with, and what areas Management can strengthen or explore to achieve a better retention rate. 
This report covered seven distinct areas in which attrition can arise. It highlights proper evaluations to determine the deductions from each of these sectors and how they affect employee attrition. In turn, the turnover rate was showcased from inception (Figure 4) and it clearly shows that the turnover rate spiralled out of control thirteen years ago and has never returned to the 20% mark ever since then. Hyacinth Parmarcitical stands at 32% turnover, beyond the  20% acceptance mark, clearly showing a strain on the workforce.

## Introduction
Employee attrition is essential in the 21st century as the global market is moving from the company mindset to focusing on the individual. This has caused a shift in power dynamics hence the need for companies to focus on their employees, as it is known that they are the most priced possession of the company. Because this day, individuals go out of their way to develop skill and discipline, foremost adding value to themselves before projecting this worth on the company in terms of amount and worth. This has made it inevitable to create a stable and developing workforce. This can be attributed to attrition as its rise over the years can be deduced directly or indirectly from these citations, making it inherently difficult for Human resource managers (HRM). However, attrition has some positives, as it makes room for constantly changing ideas.
Attrition is a percentage that can encompass some positives. A high attrition percentage mandates the company's Managerial team to invest in employees. The problem comes when this ratio exceeds a threshold where the outgoing is more than the incoming. On either side of the spectrum, time and money must be spent to keep or employ an individual who can never be transformed into dividends if the attrition percentage is high.
There has been a falling out between employers and employees over the years, and stories have been passed down by word of mouth and observation of previous members of the older workforce. Causing a negative space between the former and the latter, the breakdown that leads to employee loss is called attrition. Attrition cuts across all forms of industries and Job roles, as it is a naturally occurring effect. Apart from affecting goods and services, it also eats deeply into the company's reputation. Therefore, it is only sensible for management to approach attrition with a scientific mindset, dissect the various intricacies, and devise a feasible solution.
This project focuses on the health sector as the Dataset concerns a pharmaceutical company with several departments and various job roles. Attrition is on a high and is in constant increase in this sector. Therefore, some insight can be drawn with respect to attrition in the medical sector; in places like India, attrition is at 30 to 40 percent in the pharmaceutical industry [1]. Some other sectors to closely observe would be the Tech industries. 
## 1.1.	Data Set Source
The data set used for the comprehensive analysis of this project is from Kaggle: 
<a href = "https://www.kaggle.com/datasets/patelprashant/employee-attrition">Kaggle Link</a>
The development and citation of this Dataset acknowledges other sites: 
<a href= "https://www.ibm.com/communities/analytics/watson-analytics-blog/watson-analytics-use-case-for-hr-retaining-valuable-employees/"> Watson blog link</a>


# Appendix: Business Intelligent Report

## 1. Data Pre-processing and Cleaning
The first step to preprocessing the Data is to import the HR Employee Attrition data; various methods exist. However, this data set was imported using the manual method. The "Get data" button was selected from the home tab, and the format of CSV was chosen, as this is the format of the data imported "WA_Fn-UseC_-HR-Employee-Attrition.csv". A dialogue pops up, requesting to load the data. The load is accepted, and data loading begins, see Figure 23. After successfully importing the Data, it shows no errors and is ready to be cleaned. "Transform data" is clicked on, and this displays the Data transformation terminal.

<img src="/image/23.JPG" alt="Data importation" width="1000" height="300">
Figure 23: Data importation

<img src="/image/24.JPG" alt="Data importation" width="1000" height="300">
Figure 24: Data successfully imported

Figure 24 shows the loaded Data in Power Bi as it is ready to be transformed. The quality of the Dataset is checked, and the Transformation terminal summarises the Dataset in the bottom left-hand corner of the window. None of the columns continued missing values or NAs see Figure 25. Figure 26 shows the reordering of the columns and the renaming of the WA_Fn-UseC_-HR-Employee-Attrition Dataset to Data. Figure 27 shows that columns were renamed for better understanding, as most column headers were not spelt with spaces. Columns were then deleted as they will not play any further part in the analysis of this report; "Business Travel", "Daily Rate", "Hourly Rate", "Over 18". See Figure 28.

<img src="/image/25.JPG" alt="Data importation" width="1000" height="300">
Figure 25:Dataset Quality checks

<img src="/image/26.JPG" alt="Data importation" width="1000" height="300">
Figure 26:Reordered Columns

<img src="/image/27.JPG" alt="Data importation" width="1000" height="300">
Figure 27:Renamed Columns

<img src="/image/28.JPG" alt="Data importation" width="1000" height="300">
Figure 28:Deleted Columns

## 2. Data Modeling
### 2.1. Calendar
Figure 29 represents the Model state after Data cleaning. Data normalisation and splitting of this fact table will occur from here out. First, we shall work on the Date table for the employees.

<img src="/image/29.JPG" alt="Data importation" width="1000" height="300">
Figure 29: Data model after cleaning

A new "Date Started Working" column was added using M langue. See the new Column in Figure 30. See the M language section for code subscripts. In order to create a column that is full Date, we will need to get the day and month. This was achieved by duplicating the current column "Date Started Working ??? Copy" and converting the duplicated Column to Date format by Changing its data type. A delimiter then splits this Column to bring out other new columns that would serve as the day, month and year.

<img src="/image/30.JPG" alt="Data importation" width="1000" height="300">
Figure 30:New Column added

The result can be seen in Figure 31. Columns with Copy 1 and 2 are reordered before the original "Date started working" Column. These three columns are then merged by "/". Their Data type is converted to Date type, and the Merged Column is renamed. See Figure 11. The "Date Started Working ??? Copy 3" column is deleted because we no longer use it. The exact process and steps were done to create the columns "Date in

current role", "Date joined the company"," Date of the last promo", and "Date started with manager" see Figure 32.
The Data table was then duplicated, and all the columns were deleted except the "Date joined company". See Figure 33. The "Date joined company" Column was then filtered to get the earliest Date on which the first Staff was employed. This was achieved using the "Date filter" tool and clicking on the "is earliest" option to prompt this filter. This value is converted to a whole number by changing the Data type to a Whole number type. Then this single value acquired is clicked on, and the "Drilled Down" is used to drop the value further to a single day see Figure 36.
This single-day value generates all the dates from that given Date until the Date. This is done by using an M langue function. See the M langue section for this script. Figure 37 shows the output after the function has been executed. The List of values is converted to a table by clicking on the "to table" convert at the top left-hand side of the window. The data type is then converted to its original setting, which is date format and the Column is renamed "Date". Then using the add column section of the data transformation toolbar, add new columns from the "Date" icon drop-down. Year, Month name, Quarter, Day name and Day of Week were added. See Figure 38.

<img src="/image/31.JPG" alt="Data importation" width="1000" height="300">
Figure 31:Delimiter slinging of Date started working-copy columns

<img src="/image/32.JPG" alt="Data importation" width="1000" height="300">
Figure 32:Date Started Working column is completed

<img src="/image/33.JPG" alt="Data importation" width="1000" height="300">
Figure 33:Date Columns

<img src="/image/34.JPG" alt="Data importation" width="1000" height="300">
Figure 34:Calendar Dataset

<img src="/image/35.JPG" alt="Data importation" width="1000" height="100">
Figure 35:Date Joined Column filtered for the earliest date

<img src="/image/36.JPG" alt="Data importation" width="1000" height="300">
Figure 36:Date drilldown

<img src="/image/37.JPG" alt="Data importation" width="1000" height="300">
Figure 37:Generated Values from the earliest date

<img src="/image/38.JPG" alt="Data importation" width="1000" height="300">
Figure 38:Calendar table

### 2.2. Dimension Table
The values of some columns needed to be encoded with new values to make their parameters understandable. The columns Education, Environmental Satisfaction, Job Involvement, Job satisfaction, Relationship satisfaction, and Work-life balance all needed some form of encoding. Each of these columns needs to be duplicated. Their data type was changed to a text format before they were encoded with the values stated in the Data source as the actual meaning of the numbered set. After, the columns with the numerical variables were renamed by adding "level" to the Column after their actual names. The copies encoded with the text values of the texts bearded the original names respectively. See Figure 39.
Duplicates of the Data table are made, and all other features are deleted except for employee Number and the previously encoded features, i.e., the Education, Environmental Satisfaction, Job Involvement, Job satisfaction, Relationship satisfaction, and Work-life balance columns. This table is renamed Employee Measure. See Figure 40. These measures are further broken down into six tables as these relationships lead to many connections with the fact table. See Figure 41.

<img src="/image/39.JPG" alt="Data importation" width="1000" height="300">
Figure 39:Dimension table features

Measures were also created for Department, Job role and Gender. See Figure 42 ??? 43. These measures were created by duplicating the original Data table, deleting all other columns in the individual table, naming them appropriately (Department, Designation and Gender) and then removing duplicates from their contents. This will drop the table values to district values.

<img src="/image/40.JPG" alt="Data importation" width="1000" height="300">
Figure 40: Employee measure table

<img src="/image/41.JPG" alt="Data importation" width="1000" height="300">
Figure 41:Department Dimension table

<img src="/image/42.JPG" alt="Data importation" width="1000" height="300">
Figure 42:Designation Dimension table

<img src="/image/43.JPG" alt="Data importation" width="1000" height="300">
Figure 43:Gender Dimension table

#### 2.2.1. Location dimension table
A new data set had to be imported to generate the location dimension table. This data set was loaded just like the primary data set sees Figure 44. The data set contains the individual location of groups of employees broken down based on their distance from work. The Dataset is then cleaned, missing columns are removed, and the table is renamed "Proximity to work". See Figures 45 and 46 for before and after data cleaning. See Figure 47 for a complete breakdown of the Dimension table.

<img src="/image/44.JPG" alt="Data importation" width="1000" height="300">
Figure 44:Area Dataset being loaded

<img src="/image/45.JPG" alt="Data importation" width="1000" height="300">
Figure 45:Area Dataset after loading

<img src="/image/46.JPG" alt="Data importation" width="1000" height="300">
Figure 46:Proximity to work Dimension table

<img src="/image/47.JPG" alt="Data importation" width="1000" height="300">
Figure 47: Dimension table obtained from measures

## 2.3. Fact table
Because of the duality of the Data set, we needed to split the fact table into two so that the necessary information could be easily gotten or decimated. The original Data table was duplicated in two pale, and the Attrition column was filtered to "Yes" and "No" for each duplicate. The data set that was filtered for "Yes" was renamed as the "Leavers" data set, while the set filtered for "No" is the current Staff data set. See Figure 48. The Original Data table was turned off because this table was for the various relationships where they were referenced. A final derivative of the Model can be seen in Figure 49.

<img src="/image/48.JPG" alt="Data importation" width="1000" height="300">
Figure 48: Fact tables

<img src="/image/49.JPG" alt="Data importation" width="1000" height="300">
Figure 49: Final Model


Author: <a href = "https://github.com/Gejix">Gerald Juwah</a>
