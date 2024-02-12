# Employee Attrition Analysis

### Dashboard Link : https://app.powerbi.com/groups/me/reports/346f26c7-bfa0-4211-a378-c872ac4ddc9c/ReportSectione5a92818b7e755760033?experience=power-bi

## Problem Statement

This dashboard helps the XYZ company which was established a few years back is facing around a 15% attrition rate for
a couple of years. And it's majorly affecting the company in many aspects. In order to
understand why employees are leaving the company and reduce the attrition rate XYZ
company has approached an HR analytics consultancy for analyzing the data they have. You
are playing the HR analyst role in this project and building a dashboard which can help the
organization in making data-driven decisions.


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present.
- Step 5 : there is number of ages of employee work in this compony that’s why I am created a age groups of their ages.
- Step 6 : In the report view, under the view tab, theme was selected.
- Step 7 : Since the data contains various employee in there different age group to live this company , thus in order to represent the attrition rate, a new visual was added using the card view in the visualizations pane in report view. 
- Step 8 : Visual filters (Slicers) were added for Two fields named “Departments”,”Total Attrition By Work Distance”
- Step 9 : Two card visuals were added to the canvas, "Total_Employee", "Total_Attrition", "Attrition Rate" & "Active employee",” Average Salary” and Average Years.
           Using visual level filter from the filters pane, basic filtering was used & null values were unselected for consideration into average calculation.
           
           Although, by default, while calculating average, blank values are ignored.
- Step 10 : A bar chart was also added to the report design area representing the Age Groups and sum of Attrition count. 
- Step 11 : Attrition rating image was used to represent the Attrion Rate of the company.
- Step 12 : In the report view, A 100% Stacked Bar chart was also added to the report design area representing the Attrition By Departments
- Step 13 : In the report view, under the insert tab, using shapes option from elements group a rectangle was inserted & similarly using image option company's logo was added to the report design area. 
- Step 14 : Calculated column was created in which,Employee were grouped into various age groups.

for creating new column following DAX expression was written;
       
        Age Group = 
        
        if(Attrition_Data[Age]<=25, "18-25 (25 included)",
        
        if(Attrition_Data [Age]<=35, "26-35 (35 included)",
        
        if(Attrition_Data [Age]<=45, "36-45 (45 included)",

        if(Attrition_Data [Age]<=55, "46-55 (55 included)",
        
        "55+ (100 included)")))
        
Snap of new calculated column ,

![image-1](https://github.com/prajukhobragade/PowerBi_Dashboard_Projects/assets/155815795/1e619619-2307-477c-9c42-ba72ddee7313).jpg)

        
- Step 15 : New measure was created to find total of Employee.

Following DAX expression was written for the same,
        
        Total_Employee = Count('Attrition data'[EmployeeID])
        
A card visual was used to represent Total Of Employee.

![Snap1](https://github.com/prajukhobragade/PowerBi_Dashboard_Projects/assets/155815795/3ba7cae2-9e82-4548-ad26-b9b145d33588)        
 - Step 16 : New measure was created to find  % of customers,
 
 Following DAX expression was written to find Total Attrition,
 
         Total_Attrition = SUM('Attrition data'[AttritionCount])
 
 A card visual was used to represent this Sum Of Employee Attrition .
 
 Snap of Total Employee attrition in this company.
 
 ![snap2](https://github.com/prajukhobragade/PowerBi_Dashboard_Projects/assets/155815795/7bd5ee6c-2102-42e5-b351-894793c9bb27)
 
 - Step 17 : New measure was created to calculate Attrition rate in this company.
 
 Following DAX expression was written to find total Attrition Rate,
 
         AttritionRate = SUM('Attrition data'[AttritionCount])/ SUM('Attrition data'[EmployeeCount])
    
 A card visual was used to represent this Attrition Rate.
 
 
![snap3](https://github.com/prajukhobragade/PowerBi_Dashboard_Projects/assets/155815795/89684269-ea2d-456a-b256-8e4673b574c8) 
 - Step 18 : The report was then published to Power BI Service.
 
 
![screenshot1](https://github.com/prajukhobragade/PowerBi_Dashboard_Projects/assets/155815795/a9e7fac4-f7bb-4e8c-8bba-680653348378)
# Snapshot of Dashboard (Power BI Service)

![snap19](https://github.com/prajukhobragade/PowerBi_Dashboard_Projects/assets/155815795/b12941ff-9ae1-4a4a-b3ae-ce879cac5606)
 
 # Report Snapshot (Power BI DESKTOP)

 
![snap20](https://github.com/prajukhobragade/PowerBi_Dashboard_Projects/assets/155815795/a22029d3-bd65-4dff-ae00-b2b7bfb18dc9)# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] Total Number of Employees = 4410

   Number of Total Employee (Male) = 2646 (60 %)

   Number of Total Employee (Female) = 1764 (40 %)

   Number of Total Attrition = 711 (16.01 %)

   Number of Total Attrition (Female) = 249 (37.97 %)
   
   Number of Total Attrition (Male) = 408 (62.03 %)

   Number of Job unsatisfied Employee  (Male) = 441 (10 %)

   Number of job unsatisfied Employees (Female) = 270 (6.12 %)


           thus, higher number of male Employee are leave this company and not satisfied with their job.
           
  
  
  
  

 ### [4] Some other insights
 
 ### Education
 
 1.1) 303 Employee leaving their jobs in Life science Field.
 
 1.2) 225 Employees leaving their jobs in Medical Science Field.
 
 1.3) 75  Employees leaving their jobs In Marketing Field.
 
         thus, maximum Employees Attrition In Life Science Education Field.
 
 ### Age Group
 
 2.1)  348 Employee Attrition belong to '26-35' age group.
 
 2.2)  132 Employee Attrition belong to '18-25' age group.
 
 2.3)  129 Employee Attrition belong to ‘36-45' age group.
 
 2.4)  78 Employee Attrition belong to ‘46-55' age group.
 
         thus, maximum Employee attrition belong to '26-35' age group.
