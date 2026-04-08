# CREDEBIT-INSURANCE-DASHBOARD

# Project Title

A brief description of what this project does and who it's for

# CREDEBIT INSURANCE DASHBOARD

### Dashboard Link : [https://app.powerbi.com/groups/1a12fa70-25fd-4bde-bc75-ca25d6312938/reports/e94f691b-209e-4ec2-a4c6-b43b75d5164a/4798cabb238abd001708?redirectedFromSignup=1&experience=power-bi](https://app.powerbi.com/reportEmbed?reportId=e94f691b-209e-4ec2-a4c6-b43b75d5164a&autoAuth=true&ctid=f63b639e-20d3-48e3-807e-b5db0f84ff9e)

## Problem Statement

Insurance organizations generate large volumes of data across multiple domains such as policies, claims, customers, and premiums. However, this data is often stored in disparate systems, making it difficult for business users to gain a unified and real-time view of performance.


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present except column named .
- Step 5 : Calculate coloumn like total premium amount , annual premium ammoun , paid premium amount , payble premium amount , maturity amount , ROI%
- Step 6 : In the report view, under the view tab, theme was selected.
- Step 7 : Since the data contains various ratings, thus in order to represent ratings, a new visual was added using the three ellipses in the visualizations pane in report view. 
- Step 8 : Visual filters (Slicers) were added for four fields named "Polcy type","Plocy name" , "Agent name".
- Step 9 : Added Filled Parameter for dynamic visual change.
           
           Although, by default, while calculating average, blank values are ignored.
- Step 10 : A bar chart was also added to the report design area representing stae wise sale , Treemap used for showing sale by agent. 
- 
  for creating new column  TOTAL ANNUAL PREMIUM following DAX expression was written;
       
       TOTAL ANNUAL PREMIUM = 
SWITCH(TRUE(),
'FCT Insurance_Policy_Table'[Payment Frequency] = "Annually" , 'FCT Insurance_Policy_Table'[Premium Amount]*1,
'FCT Insurance_Policy_Table'[Payment Frequency] = "Half Yearly",'FCT Insurance_Policy_Table'[Premium Amount]*6,
'FCT Insurance_Policy_Table'[Payment Frequency]="Quarterly",'FCT Insurance_Policy_Table'[Premium Amount]*4,
'FCT Insurance_Policy_Table'[Payment Frequency]="Monthly",'FCT Insurance_Policy_Table'[Premium Amount]*12,
BLANK())
        

snap of the coloumn 
https://github.com/user-attachments/assets/facf531e-19a2-4059-94dc-44fc9c6cbb81
        
- Step 15 : snap of reports 
https://github.com/user-attachments/assets/adee286a-0f62-451e-b2a7-67d116a9126d

- Step 15 : snap of KPI
(https://github.com/user-attachments/assets/37c92ba5-f778-44ae-81ce-d31c4b03046a)
