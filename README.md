

# BlinkIt Dashboard

### Dashboard Link :https://drive.google.com/file/d/17vJKzv3bD352zqUKr2d-bQg_Aq9Bl4qA/view?usp=sharing


## Problem Statement

This dashboard helps the BlinkIt understand their customers better. It helps the BlinkIt to understand if their customers are satisfied with their services. Through different sales data, they get to know their improvement area, & thus they can improve their services by identifying these area. It also lets them know the average ratings per profuct,average sales and more, thus since by using this dashboard they have identified their improvment area, yearly sales data for different products. 






### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present except column named "Item Visibility". so i decided to replace all null values which was prenent into "Item Visibilty" column to "0".
- Step 5 : in the report view the theme of the dashboard was selected.
- Step 6 : insert a shape to establish background of the work "blinkIt" used "text box" option to write "BlinkIt" word and the other texts.
- Step 7 : use slicers to filter data according to "low-fat" and "regular" type.
- Step 8 : 4 card visuals are added to reflect summerise values of "Total sales", "Average sales", "Average ratings", "Total items".
          
           
           Although, by default, while calculating average, blank values are ignored.
- Step 9 :A stacked column chart is added to reflect "outlatetype by sales" data
- Step 10 : Aclustered bar chart is added to reflect "Item types by sales".
- Step 11 :A pie chart is added to reflect "Sales by outlate size".
- Step 12 : A matrix table is added reflect "overall overview".
- Step 13 :A donut chart and a area chart is added to reflect "Sales by Item fat content" and "sales by outlet establishment year" respectively and use funnel to reflect sales by outlet location type.
  


        

        
- Step 14 : New measure was created to find total Sales.

Following DAX expression was written for total Sales.
        
        Total Sales = 
             SUM('BlinkIT Grocery Data'[Sales]
               )
        


        
 - Step 15 : New measure was created to find  Total ratings,
 
 Following DAX expression was written to find Total ratings,
 
         Total Ratings = 
            SUM('BlinkIT Grocery Data'[Rating]
                )


 
 - Step 16 : New measure was created to find total product,
 
 Following DAX expression was written to find total product,
 
        Total Product = 
        COUNT('BlinkIT Grocery Data'[Sales]
                )
 
  - Step 17 : New measure was created to find total number of ratings,
 
 Following DAX expression was written to find total number of ratings,

       Total number of ratings = 
            COUNT('BlinkIT Grocery Data'[Rating]
                   )
 
 
 - Step 18 : New measure was created to find total product,
 
 Following DAX expression was written to find total product,


              Total Items = 
               DISTINCTCOUNT('BlinkIT Grocery Data'[Item Identifier]
                  )
Step 19 : New measure was created to find Average sales,
 
 Following DAX expression was written to find Average sales,

              Average Sales = 
                [Total Sales]/[Total Product]


Step 20 : New measure was created to find Average ratings,
 
 Following DAX expression was written to find Average ratings,

            Average Ratings = 
                [Total Ratings]/[Total number of ratings]

step 21 : Add a reset button with reset function to return back to its orginal value.
 

# Insights

A single page report was created on Power BI Desktop.

Following inferences can be drawn from the dashboard;

### [1] Total Sales = 1.20M $

   Average sale = 141 $

   In sales by outlet location type tier 3 is 0.5M $ which is more than tier 2 and tier 1.

   In sales by outlet type super market type 1 generate more sales than other supermerket types which is 0.79M $

   In sales by item type fruit and vegetables generate more sales than others which is 0.18M $

   sales by outlate establishment year sales for 2018 has incresed from the previous year 2017 which is 0.20M

   In sales by outlate size there are three types of outlate distribution High,which is $249k, medium which is $507.9k, small which is $444.8k

   sales by item fat containt includes regular type which is $425.4k and low fat which is $777.3k

   ### Below complete dashboard Image

![Dashboard Images](https://github.com/user-attachments/assets/60828805-57d9-40a2-b347-de22289fe557)


   

