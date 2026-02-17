# CUSTOMER SATISFACTION & LOYALTY ANALYSIS PROJECT

## PROJECT DESCRIPTION
   This Power BI project analyzes **customer satisfaction** and **loyalty** using survey feedback, demographic data, and behavioral metrics. The goal is to:
   - Identify regional strengths and pain points
   - Segment customers by loyalty (NPS categories) and demographics
   - Provide actionable insights to improve retention, experience, and long-term loyalty.
<img width="1366" height="768" alt="Screenshot (55)" src="https://github.com/user-attachments/assets/7a9128d4-d458-4383-8716-371e7ab04f17" />

## Technologies & Tools
- **Data Preparation & Cleaning**: Microsoft Excel + Power BI (Power Query)
- **Modeling & Calculations**: Power BI (DAX)
- **Visualization**: Power BI Desktop
- **Dataset Format**: Excel (.xlsx)

## Project Steps

### 1. Data Loading & Cleaning (Power Query)
       i. Load the Excel file into Power BI Desktop.
       ii. Open **Power Query Editor**.
       iii. Check for and handle:
           - Duplicates → Remove duplicates
           - Empty/missing values → Fill using average where appropriate (Fill Up/Down)
       iv. Close & Apply changes.

### 2. Calculated Columns (DAX)

       - **NPS Category** (Promoters, Passives, Detractors):

         ```dax
       NPS_CATEGORY = 
       SWITCH(
       TRUE(),
       'DataDNA Dataset Challenge - Cus'[Satisfaction_Score] >= 9, "PROMOTER",
       'DataDNA Dataset Challenge - Cus'[Satisfaction_Score] IN {7,8}, "PASSIVE",
       'DataDNA Dataset Challenge - Cus'[Satisfaction_Score] <= 6, "DETRACTOR",
       "INVALID"
     )

       Age Group (binned via Group By in Power Query):
       25–36
       37–48
       49–60


### 3. Key DAX Measures

       DAX
       Count of Customers = COUNT('DataDNA Dataset Challenge - Cus'[Customer_ID])

       Total Satisfaction Score = SUM('DataDNA Dataset Challenge - Cus'[Satisfaction_Score])

       Average Satisfaction Score = AVERAGE('DataDNA Dataset Challenge - Cus'[Satisfaction_Score])

       Satisfaction Rate % = 
       DIVIDE(AVERAGE('DataDNA Dataset Challenge - Cus'[Satisfaction_Score]), 7, 0) * 100
       

### VISUALIZATION
    * Step 1: Distribution by Age,Gender and Location <Clustered Bar Chart>
              Each bar shows the count of individuals in a specific age group split by gender and location.

 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/986064e1-bceb-4da1-83ab-4fc120b8a1f5" />         

    * Step 2: Percentage of Customers in each Loyalty Level<Donut Chart>
              Each Pie slice represents the percentage of customer in each loyalty level, with the largest slice indicating the most common tier.

 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/42e42869-cfea-4124-8a8f-1e6000d8577f" />

    * Step 3: Satisfaction rate in % <Gauge>
              The filled portion of the gauge represents the percentage of satisfied customers, with the arc pointing to the value.
              
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/26d55364-1dde-41fe-8f5c-eba42c08b58e" />

    * Step 4: Customer Distribution by Group and Location <Funnel>
              The funnel chart explains the percentage of customers in each group per location. This distribution helps us to understand where different
                types of customers are cocentrated and informs targeted strategies.

 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/a055e3e7-bc5f-41c3-8ea7-898547ce1b78" />

    * Step 5: Satisfaction Score by Age Group <Stacked Column Chart>
              Satisfaction Score measures how satisfied users are with a product or service. I segmented these scores by age group to identify trends and
              tailor improvements for different demographics.

 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/dfe0f4fd-9b07-42a0-9252-e789138e664c" />

    * Step 6: Correlation between NPS Category <Pie Chart>
              Net Promoter Score(NPS) measures customer loyalty based on their likehood to recommend a product or service, rated on a scale from 0(not likely)
              to 10(extremely likely). Responses are grouped into three categories:
              **Promoters**(9-10): Loyal customers who are highly likely to recommend a product.
              **Passives** (7-8): Satisfied but unenthusiastic customers who may not actively promote a product.
              **Detractors** (0-6): Unhappy customers who may spread negative feedback about a product.
              
              NPS is calculated as:
              NPS=% Promoters - % Detractors

 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/553bfc8b-3fc8-4adf-b731-d5e2c936a74f" />
 
### ADD INTERACTIVITY WITH SLICER
    Slicers added for interactivity:
    - Age Group
    - Gender
    - NPS Category
    These allow dynamic filtering across all visuals.


### KEY INSIGHTS & FINDINGS
    Austin, TX → Highest proportion of Promoters → Strong loyalty and satisfaction in this region.
    Phoenix, AZ → Highest share of Detractors → Indicates potential issues with product/service/experience; also has many Passives (balanced but not strongly loyal).
    Geographic variation is significant → Supports targeted regional strategies (e.g., retention campaigns in Phoenix, loyalty reinforcement in Austin).
    Age and gender segments reveal additional patterns for personalized improvements.

### How to Use / Explore This Project
    1. Clone or download the repository.
    2. Obtain the original Excel dataset (if you have access to the DataDNA challenge file or equivalent).
    3. Open CUSTOMER SATISFACTION & LOYALTY PROJECT.pbix in Power BI Desktop.
    4. If prompted, update the data source path to point to your local .xlsx file.
    5. Refresh the data and interact with slicers/visuals.

### CONCLUSION
    This interactive Power BI dashboard reveals clear geographic and demographic trends in customer satisfaction and loyalty. 
    It highlights Austin, TX as a loyalty stronghold and Phoenix, AZ as an area needing focused improvement efforts. 
    These insights can directly inform marketing, product, and customer support strategies to boost retention and overall experience. 
    
 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/ecfcf336-eb5e-45be-8444-8534b9b34768" />

