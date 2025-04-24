# HR Data Analysis in Excel and PowerBi

**Author:Nisha**

**Date: 07.02.2025**

# Introduction 

  HR Data Analysis involves collecting, processing, and interpreting workforce data to improve hiring, employee performance, retention, and overall business outcomes. It leverages analytics tools and techniques to drive strategic HR decisions.By using data-driven insights, HR professionals can enhance recruitment efficiency, reduce turnover, improve employee engagement, and ensure fair compensation. It helps organizations optimize workforce management and align HR strategies with business goals.
  
**Scope of the Document:**

This document explores key HR metrics, data sources, analytical techniques, and tools like Excel and  Power BI. It also covers real-world applications, challenges, and future trends in HR analytics.

## HR Data Sources

  Sourced From :<https://www.kaggle.com/datasets/rhuebner/human-resources-data-set> 
  
  Licence : This work is licensed under a Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License.
  
  Tools: Excel and PowerBi
  
  Details : extracting and cleaning are done in excel sheet and visualisation and report generation are performed in Powerbi
  

## HR Metrics and KPI

  - Demography (the whole statistical analysis of employees in the organisation)
  - Performance Analysis( YOY change in the performance score and engagement survey)
  - Recruitment Metrics( YOY Analysis of employee hiring ,attrition and best recruitment Sources )
  - Employee Personal Information ( Name,State, citizen, sex, etc)

# CLEANING DATA IN EXCEL

  The dataset was in CSV format and later changed them to Excel sheet for cleaning.
  
  ![Screenshot 2025-02-07 115102](https://github.com/user-attachments/assets/284e19e2-9cfd-413a-97bd-bfbb3e7c0b2a)

  **Total No of Rows 312 and Column 36.**
  
     
**Function and Techniques for Cleaning**

1. Handling Missing Values
2. Removing Duplicates
3. Correcting Inconsistent Format
4. Splitting & Merging Data
5. Standardizing Data Formats
6. Finding & Replacing Data

**1. Handling Missing Values**

The dataset is downloaded as CSV file format. First save the dataset into Excel workbook before editing.
We can use **Data TAB -> Filter** to identify the blank cells in each columns.

  
  <img width="917" alt="image" src="https://github.com/user-attachments/assets/893bb6ba-68ee-432d-ae63-7c85380a6914" />
  

Check each column by clicking on the column name tab down arrow button.There will be list of column data grouped together.scroll down to see the blank option.If no data with Blanks name then the column has free of blank space. If yes, then un select **"select all"** option from the list and select the **"(Blanks)"** option.

  
<img width="937" alt="image" src="https://github.com/user-attachments/assets/432807dd-11d7-4741-b5ab-0f17e2e7a7d6" />


There is one more empty column in the **AI Column**. select and delete the column it has no data init.


<img width="947" alt="image" src="https://github.com/user-attachments/assets/424585d0-80db-4b57-a8f2-fd5d00329557" />


Allign the data in the **Date of termination** column. Do this for all the column to look better.



<img width="930" alt="image" src="https://github.com/user-attachments/assets/46713775-7456-42cf-a6f6-fbd16bc03e45" />




<img width="928" alt="image" src="https://github.com/user-attachments/assets/4e71d84b-9afc-41da-b19d-5be9a2c4935b" />



Find and Replace the slach "/" with  "-"



<img width="937" alt="image" src="https://github.com/user-attachments/assets/60b5d406-87c3-4784-9407-d2b7914e1492" />



Replace all with Selecting **" - "** in the **Replace with** text box. and select **Replace all** to change the date format to look similar.



<img width="931" alt="image" src="https://github.com/user-attachments/assets/3a0bbbc6-078c-4549-8a49-229238eeeaf2" />



Now Delete or replace the blank space with N/A or Null based on the information the column contains. 
For deleting **filter -> un select "Select all"  -> Select (Blanks)** option and delete the rows with blank information.
For replacing the blanks use Go to option by selecting **"CTLR+G"** in keyboard option in excel and click **"Special"** button . 
In the Got to speacial dialog box select **"Blanks"** and click ok.



<img width="931" alt="image" src="https://github.com/user-attachments/assets/30651281-6b4f-48b4-a447-41ce411c972b" />



<img width="943" alt="image" src="https://github.com/user-attachments/assets/829ca46b-e1bb-42c4-bca3-cc8e34688d08" />


in the **Date of termination** column on the first cell type **=** and select the **"N/A- Still Employeed"** cell in **TermReason**. this will reference the cell 
as **"= Y2"** and then press **"CTLR+ENTER"**



<img width="946" alt="image" src="https://github.com/user-attachments/assets/627833b8-7cf3-4f41-96b1-5fe85f946725" />


Do the find and Replace for the column **LastPerformanceReview_Date**



<img width="902" alt="image" src="https://github.com/user-attachments/assets/cb3a5075-7503-4823-9c1a-63c8fa8279fb" />



Select **LastPerformanceReview_Date** column and select **"text to column"** option from Data tab click **"delimiter"** and click **Next** and again **Next** and select Date as **"DMY"**.

Since the column is mixed up of dmy and mdy we change the format as mdy.


<img width="869" alt="image" src="https://github.com/user-attachments/assets/bd59aeb5-908c-4ae4-b2a5-8faba0001bcc" />



Do the find and replace option for **DOB column**as the date formats are mixed up. Change the **"/"** to **"-"** and Replace all.



<img width="947" alt="image" src="https://github.com/user-attachments/assets/5bc3e245-bb78-43eb-b586-e17558fe3dd5" />



<img width="903" alt="image" src="https://github.com/user-attachments/assets/844bfe8d-94f8-41a9-a03b-b19b9c7c122e" />



Select DOB column and select **"text to column"** option from Data tab click **"delimiter"** and click **Next** and again **Next** and select Date as **"DMY"**.
Since the column is mixed up of dmy and mdy we change the format as mdy.


<img width="911" alt="image" src="https://github.com/user-attachments/assets/12b631f0-d3fb-437a-8b15-5e7f6b281df3" />



<img width="911" alt="image" src="https://github.com/user-attachments/assets/f97cd5c5-debe-431d-a72b-50440f5fe849" />



<img width="908" alt="image" src="https://github.com/user-attachments/assets/8e69aa1c-130d-490f-b784-a651cdd0e583" />



Next change the salary Column format into Currency "$" from Home and change general to Currency.



![Screenshot 2025-02-04 205404](https://github.com/user-attachments/assets/729ce3bf-4541-413f-a406-adb611c2ca37)



Select the **Employee_Name** and select **"text to column"** option from Data tab click **"delimiter"** and click **Next**. 
In the next dialog box select the **tab** and **comma**option and click **Next** and **Finish**.
The data will be separated into two column with first name and last name. fill the column name of second column as **Last Name**


![Screenshot 2025-02-04 132526](https://github.com/user-attachments/assets/6c0675c5-092f-4531-9a1a-9c7c296666f8)




![Screenshot 2025-02-04 132554](https://github.com/user-attachments/assets/ef177904-1e2a-4e2d-b21e-397414acf1e2)




![Screenshot 2025-02-04 205214](https://github.com/user-attachments/assets/6c9ed0ed-4ad3-48ff-8ecf-95214245cedb)



**Sorting and Filtring**

Use sorting and filtering to change the data by sorting and filter them by the order we prefer to view the data.



![Screenshot 2025-02-04 205214](https://github.com/user-attachments/assets/c9d2e772-6235-493b-927e-bcbdb3d1fa7b)




After cleaning the data using allignment, finding blank cells and replacing & deleting. we also changed the datatype of Date columns in the dataset.
no we group the data according to the analysis process.



**Performance Sheet**



<img width="930" alt="image" src="https://github.com/user-attachments/assets/9e414d7c-9e43-43b7-ba7b-0af8f6c3b8c4" />



**Personal Information**



<img width="937" alt="image" src="https://github.com/user-attachments/assets/190846bb-f0c5-4f5b-88b3-8f03835c6dc6" />



**Recruitment and Termination Sheet**



<img width="929" alt="image" src="https://github.com/user-attachments/assets/db6243dc-f4d2-4b11-849b-ab4ee9eec96b" />


**HRA Sheet**


<img width="936" alt="image" src="https://github.com/user-attachments/assets/624b463d-fc24-4c0d-803d-fba61f0cd037" />



**Salary**


<img width="467" alt="image" src="https://github.com/user-attachments/assets/9e7489a8-ab20-452a-a49b-cea9e5718848" />



# Visualizing The data in PowerBi


Select the Excel work book in the powerbi desktop by choosing Excel woorkbook option in the Home tab and select the File from the folders and after the choose the required sheets to load the data for the modeling and visualizing them.
Select the sheet from the left side as shown below. and click **Load.**



<img width="919" alt="image" src="https://github.com/user-attachments/assets/e626abf2-98a5-4875-873a-7f20d278b4a8" /> 



Select the right most icon **Model View**.

Manage the relationship of the data tables by selecting the **"Manage Relationship"** option from **Home** tab. 



<img width="944" alt="image" src="https://github.com/user-attachments/assets/771309d2-14a4-4675-9e1f-6e264d962c13" />




Write a Dax expression to create a new **Date Table** by selecting a **New Table** from **Home Tab**.


The date table can be viewed in the model view layout.

Connect the **Date table** with **recruitment and termination** table my selecting **manage relationship** in home tab.



<img width="953" alt="image" src="https://github.com/user-attachments/assets/1d95019c-2584-4485-8a0e-21edb959c491" />




Select **Table View** icon which display all the information of the table in row and column. 



select one column and check the data type , format and data category information.


We can change the data format by changing in the **column tools** tab.




<img width="925" alt="image" src="https://github.com/user-attachments/assets/11d657f4-7a83-452b-870e-43ca39cadfc7" />




Select the **Transform data** from **Home tab**.


click **Data source setting** for managing the data source before transforming the dataset. choose the correct source path and close.


Click the **Transform data** option to open the power query editor.



 <img width="821" alt="image" src="https://github.com/user-attachments/assets/158c8924-f5e7-47d6-b67d-c099be68d877" />


 

 <img width="929" alt="image" src="https://github.com/user-attachments/assets/06628050-0db5-4b78-9a3c-9876eb4f9943" />


 

 <img width="947" alt="image" src="https://github.com/user-attachments/assets/7431e70f-ff3e-4b1e-9fda-78bb4e1ce433" />


 

Using Reference Creates a new query that links to the original query without copying the data.

Any changes made in the original query are reflected in the referenced query.



Select the table **Performance**which need to be referenced and right click as shown below.

Click the **Reference** option this will create a new table as Creates a new table **Performance(2)**. 

Repeat this for all table by selcting reference option.




<img width="956" alt="image" src="https://github.com/user-attachments/assets/cb369f96-a2e2-4bd4-9cce-16163d844870" />



Now make the changes to the respective table and check the **Applied steps** displayed in the left to view the no of transformations done on each table this would help to replace or delete the applied steps. 

Correcting column name, data type, format and deleting the column and replacing the column are easier in power query editor.
The **View tab** has list of **Data Preview** options to view the column in descriptive and detail way.


Select **Column Quality Column Distribution Column Profile**option. 

Which provide Empty , error , valid data, column statistics and Value distribution as shown below.




<img width="934" alt="image" src="https://github.com/user-attachments/assets/c51a9887-e14e-4f58-a4b1-6473c1deb9cb" />



By checking the valid and empty data percentage and checking the summary of each column data it help us to understand the column in better format.



We can also de further transformation by selecting Transform tab in the top.



<img width="946" alt="image" src="https://github.com/user-attachments/assets/f874ba74-25ea-42ac-b1ca-2043c4dc1076" />



We can use **manage parameters** in the home tab to filter the dataset.


<img width="941" alt="image" src="https://github.com/user-attachments/assets/abca1aab-c35b-481a-a79f-c504f17efd75" />


much more data transformation like merge, group by and append , pivot table can be used in powerbi with power query editor.


after completing the transformation  click and close and apply option from the home tab.




<img width="875" alt="image" src="https://github.com/user-attachments/assets/b4c48ae9-7713-47fb-ac52-626a77c614f1" />




Creating Report in the Report View.

Using Visualisation tab the data can be charted and combined as a visual presentation for the stakeholders. 

the data from the data tab are draged into the visualisation tab field area to view the data in various form of charts and graphs. 

bar chart, line chart, pie chart , slicer , table , buttons and filters are used for viewing the data in visual form. which gives better understanding.



**Performance Report:**




<img width="931" alt="image" src="https://github.com/user-attachments/assets/491a1d71-9aad-4cf6-a26f-dda7cd533df7" />





**Employee Tracker:**



Using **Button** and **Bookmark** we can use different view of report in one page.



Click Recruitment Details Button.



<img width="956" alt="image" src="https://github.com/user-attachments/assets/946bc699-bda0-40c0-bffe-1c7a48c3c380" />




Click Personal Information Button.




<img width="954" alt="image" src="https://github.com/user-attachments/assets/b0bf2967-8c2b-4790-a015-6d8272dc1a6d" />




Click Performance Button.




<img width="952" alt="image" src="https://github.com/user-attachments/assets/2bedc44e-2281-4996-92d7-e9ebc31cd70d" />




Finally **Save** and  **Publish** the report in powerbi workspace.


Click **Publish** from **home tab**. The powerbi service app is connected with the desktop application So, before publishing connect the powerbi service with the desktop.




<img width="947" alt="image" src="https://github.com/user-attachments/assets/744677de-918e-49c0-a743-077deb8d1e75" />




<img width="938" alt="image" src="https://github.com/user-attachments/assets/3e6f77a8-d490-42ce-89f0-080059f3fab1" />




Open the my workspace option and select the Report.




<img width="925" alt="image" src="https://github.com/user-attachments/assets/3e62eadf-e68e-427e-af50-27add1a8a423" />




<img width="941" alt="image" src="https://github.com/user-attachments/assets/69575086-f4a6-4083-a37f-eef351708625" />




<img width="941" alt="image" src="https://github.com/user-attachments/assets/69a06c52-3600-416b-b545-a3d23fb682ef" />




Then Create a Dashboard in the powerbi service.



A dashboard in Power BI Service is a single-page, interactive visualization that provides a high-level view of your data, combining multiple reports and datasets. It is typically used to monitor key performance indicators (KPIs) and trends in real time.
