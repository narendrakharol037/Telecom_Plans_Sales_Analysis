# Telecom Plans Sales Analysis


## Problem Statement

Create the comparison report based on the mock-up provided. Please note the mock-up is created by a business user who has a minimal idea about dashboarding. 
Hence you need to represent the insights in a much better wayThe target audience of this dashboard is top-level management - hence the dashboard should be self-explanatory and easy to understand.
Create relevant insights not provided in the metric list/mock-up dashboard to support the cause.

Mock up Dashboard

![t3](https://github.com/narendrakharol037/Telecom_Plans_Sales_Analysis/assets/121941969/b86c09fa-d328-4c3f-9aef-5ace1bbb4e2d)


### Tools Used

Database  -   Microsoft Excel
    
Visualization Tool  -  Power Bi Desktop

### Steps followed 

- Step 1 : Load data into Power BI Desktop from Microsoft Excel.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also we check duplicate values,null values and data types of all columns.
- Step 4 : In fact_gds_metrics table, I did extract Name of month from Date column after that I Named the column Month.
- Step 5 : After that i did close & Apply
- Step 6 : In the report view, under the view tab,5G theme was selected.
- Step 7 : I did create new table Key-Measures, In this Key-Measures i did create All Measures that is mentioned below.
    
   (A)  Average Revenue = AVERAGE(fact_gds_metrics[gds_revenue_crores])
    
   (B)  ARPU = AVERAGE(fact_gds_metrics[arpu])

   (C)  monthly active useres = [Total Active Users]/DISTINCTCOUNT(fact_gds_metrics[Month])

   (D)  Monthly Unsubscribed users = [Total Unsubscribe users]/DISTINCTCOUNT(fact_gds_metrics[Month])

   (E)  Active Useres After 5G = CALCULATE(SUM(fact_gds_metrics[active_users_lakhs]),FILTER(dim_date,dim_date[before/after_5g] = "after 5G"))

   (F)  Active Useres Before 5G = CALCULATE(sum(fact_gds_metrics[active_users_lakhs]),FILTER(dim_date,dim_date[before/after_5g] = "before 5G"))

   (G)  ARPU after 5G = CALCULATE(AVERAGE(fact_gds_metrics[arpu]),FILTER(dim_date,dim_date[before/after_5g] = "after 5G"))

   (H)  ARPU before 5G = CALCULATE(AVERAGE(fact_gds_metrics[arpu]),FILTER(dim_date,dim_date[before/after_5g] = "before 5G"))

   (I)  chg% active useres = ([Active Useres After 5G]-[Active Useres Before 5G])/[Active Useres Before 5G]

   (J)  Chg% Unsbscribed user = ([Unsubscribed useres after 5G]-[Unsubscribed useres before 5G])/[Unsubscribed useres before 5G]

   (K)  Chg% ARPU = ([ARPU after 5G] - [ARPU before 5G])/[ARPU before 5G]

   (L)  Chg% of Revenue = ([Revenue after 5G] - [Revenue before 5G])/[Revenue before 5G]

   (M)  Market share % = AVERAGE(fact_market_share[ms_pct])

   (N)  Revenue after 5G = CALCULATE(SUM(fact_gds_metrics[gds_revenue_crores]),FILTER(dim_date,dim_date[before/after_5g] = "after 5G"))

   (O)  Revenue before 5G = CALCULATE(SUM(fact_gds_metrics[gds_revenue_crores]),FILTER(dim_date,dim_date[before/after_5g] = "before 5G"))

   (P)  Total Active Users = sum(fact_gds_metrics[active_users_lakhs])

   (Q)  Total Revenue = sum(fact_gds_metrics[gds_revenue_crores])

   (R)  Total Unsubscribe users = sum(fact_gds_metrics[unsubscribed_users_lakhs])

   (S)  Unsubscribed useres after 5G = CALCULATE(sum(fact_gds_metrics[unsubscribed_users_lakhs]),FILTER(dim_date,dim_date[before/after_5g] = "after 5G"))

   (T)  Unsubscribed useres before 5G = CALCULATE(SUM(fact_gds_metrics[unsubscribed_users_lakhs]),FILTER(dim_date,dim_date[before/after_5g] = "before 5G"))

   
            
- Step 8 : After that I did take new-card visual from Visualization tab and then I did put four measures value in the card,like that Average Revenue,ARPU,Monthly Active Users and Monthly Unsubscribed Users.
- Step 9 :Then I did butified the cards and set the some Parameters of cards like that font,size of values.
- Step 10 :After I did created Some Line chart like that.

  (a) Monthly trend of Revenue Before 5G and After 5G

  (b) Monthly trend of ARPU Before 5G and After 5G
  
  (c) Monthly trend of active Useres Before 5G and After 5G
  
  (d) Monthly trend of Unsubscribed Useres Before 5G and After 5G
 

- Step 11 : After that I did take text box, In this box i did write Report title like that Comparison Report of Telecom Company before 5G and After 5G
- Step 12 : In the report view, I insert Three slicer from visualization tab, that is mentioned are below.

   (a)  By City Nmae

   (b)  By Before/After 5G

   (C)  By Month Name

   
### Snapshot of Dashboard (Power BI Desktop)

        PAGE 1
     
![t1](https://github.com/narendrakharol037/Telecom_Plans_Sales_Analysis/assets/121941969/895a627a-e622-4bfa-aa5a-b7d7ddd9aae2)   


- Step 13 : After that I did created Second Page of the Report and I set the 5G in background.
- Step 14 : In this Page I did also put all five Measures that is put in the above Home Page.
- Step 15 : After that I did created Some Visuals like that.

    (a)  Market Share % over Months for all Companies

    (b)  Top Plans By Revenue

    
 
- Step 16 : After that I did write Report title that is Telecom Company before 5G and After 5G.
- Step 17 : Then I did insert Three slicer from visualization tab that is like that Home Page.

### Report Snapshot (Power BI DESKTOP)

  PAGE 2
 
 ![t2](https://github.com/narendrakharol037/Telecom_Plans_Sales_Analysis/assets/121941969/ac1e1be5-9426-4b88-ad42-63f5836a5f67)
 
### Insights of PAGE 1

 (1) Change % of Revenue by City Increase to 1.82% in Lucknow and Decrease to -2.83% in Delhi.

 (2) Change % of ARPU by City Increase to 22% in Raipur and Ahmedabad, and Decrease to -13% in Pune.

 (3) Change % of active Useres Increase to 18.06% in Pune and Decrease to -18.93% in Ahmedabad.

 (4) Change % of Unsubscribed Useres Increase to 77.91% in Lucknow and Decrease to -12.63% in Mumbai.



### Insights of PAGE 2

 (1) Top Plans by Revenue is P1 and following that P2, P3, P4

 (2) For the Company PIO, Market Share % is maximum in month of Sep that is 12.96%.

 (3) For the Company Britel, Market Share % is maximum in month of Jun that is 13.09%.

 (4) For the Company GDS, Market Share % is maximum in month of March that is 13.40%.

 (5) For the Company Dadafone, Market Share % is maximum in month of Apr that is 12.86%.
 
 (6) For the Other Company,  Market Share % is maximum in month of Jun that is 12.64%.
 
 
