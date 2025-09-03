# CUSTOMER SATISFACTION & LOYALTY ANALYSIS PROJECT

## PROJECT DESCRIPTION
   This project aims to evaluate customer satisfaction and loyalty to identify strenghths, areas for improvement and strategies to enhance customer retention.
   By analyzing customer feedback, behaviorial data and key performance metrics, the project will provide actionable insights to improve customer experience
   and drive long-term loyalty.

### SOFTWARE USED
    * Excel
    * Power Bi

### STEPS FOLLOWED:
    * Step 1: Load data into power bi desktop, dataset is an xlsx file.
    * Step 2: Open the power query editor to check for duplicates, empty cells and missing values.
    * Step 3: Remove duplicates, empty cells and fill up missing values using the fill up & down option (fill with averages).
    * Step 4: Click on the close & apply button on the menu bar to close the power query editor window and apply any pending changes.

### CREATE CALCULATED COLUMNS
    * Step 5: Categorize Satisfaction_Score into Net Promoter Score(Promoters, Passives and Detractors)
               NPS_CATEGORY = SWITCH(
               TRUE(),
               'DataDNA Dataset Challenge - Cus'[Satisfaction_Score]>=9,"PROMOTER",
               'DataDNA Dataset Challenge - Cus'[Satisfaction_Score]IN{7,8},"PASSIVE",
               'DataDNA Dataset Challenge - Cus'[Satisfaction_Score]<=6,"DETRACTOR",
               "INVALID"
             )


     * Step 6: Categorize Age into AGE GROUP (using the Group By option) into
                *25-36
                *37-48 and 
                *49-60 respectively.

### USE DAX(DATA ANALYSIS EXPRESSION) TO CREATE MEASURES FOR KEY METRICS, SUCH AS:
    * Step 7: COUNT OF CUSTOMERS = COUNT('DataDNA Dataset Challenge - Cus'[Customer_ID])

    * Step 8: TOTAL SATISFACTION SCORE = SUM('DataDNA Dataset Challenge - Cus'[Satisfaction_Score])

    * Step 9: AVERAGE SATISFACTION SCORE = AVERAGE('DataDNA Dataset Challenge - Cus'[Satisfaction_Score])

    * Step 10: SATISFACTION RATE % = DIVIDE(AVERAGE('DataDNA Dataset Challenge - Cus'[Satisfaction_Score]),7,0)*100

### VISUALIZATION
    * Step 11: Distribution by Age,Gender and Location <Clustered Bar Chart>
                Each bar shows the count of individuals in a specific age group split by gender and location.

     <!-- Uploading "Screenshot (49).png"... -->           

    * Step 12: Percentage of Customers in each Loyalty Level<Donut Chart>
                Each Pie slice represents the percentage of customer in each loyalty level, with the largest slice indicating the most common tier.

     <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/42e42869-cfea-4124-8a8f-1e6000d8577f" />

    * Step 13: Satisfaction rate in % <Gauge>
                The filled portion of the gauge represents the percentage of satisfied customers, with the arc pointing to the value.
     <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/26d55364-1dde-41fe-8f5c-eba42c08b58e" />

    * Step 14: Customer Distribution by Group and Location <Funnel>
                The funnel chart explains the percentage of customers in each group per location. This distribution helps us to understand where different
                types of customers are cocentrated and informs targeted strategies.

     <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/a055e3e7-bc5f-41c3-8ea7-898547ce1b78" />

    * Step 15: Satisfaction Score by Age Group <Stacked Column Chart>
                Satisfaction Score measures how satisfied users are with a product or service. I segmented these scores by age group to identify trends and
                tailor improvements for different demographics.

     <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/dfe0f4fd-9b07-42a0-9252-e789138e664c" />

    * Step 16: Correlation between NPS Category <Pie Chart>
                Net Promoter Score(NPS) measures customer loyalty based on their likehood to recommend a product or service, rated on a scale from 0(not likely)
                to 10(extremely likely). Responses are grouped into three categories:
                **Promoters**(9-10): Loyal customers who are highly likely to recommend a product.
                **Passives** (7-8): Satisfied but unenthusiastic customers who may not actively promote a product.
                **Detractors** (0-6): Unhappy customers who may spread negative feedback about a product.
                NPS is calculated as:
                NPS=% Promoters - % Detractors

 <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/553bfc8b-3fc8-4adf-b731-d5e2c936a74f" />
 
### ADD INTERACTIVITY WITH SLICER
    1. Select the slicer visual: In the visualizations pane (on the right), click the slicer icon. This adds a blank slicer to your report canvas.
    2. Add a field to the slicer: In the fields pane, locate the dataset and drag the field you want to filter(Age group, Gender and NPS_Category) into the 
       or values area of the slicer.
    3. Resize and format the slicers to control user interactions.

### KEY INSIGHTS
    - **Austin.TX** has the highest proportion of promoters, indicating strong customer loyalty in this region.
    - **Phoenix.AZ** has the highest share of detractors, suggesting potential issues with product or service satisfaction.
    - **Phoenix.AZ** shows a balanced distribution with passives being the largest group.

### CONCLUSION
    This dashboard delivers key insights into customer satisfaction and loyalty, highlighting trends like strong loyalty in Austin.TX and opportunities to improve
    satisfaction in Phoenix.AZ. These findings helps us tailor marketing and support to boost customer experience. The visualizations and underlying data are accessible
    via the <img width="1366" height="768" alt="Image" src="https://github.com/user-attachments/assets/ecfcf336-eb5e-45be-8444-8534b9b34768" />

