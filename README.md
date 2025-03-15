# ElectricVehicles_Statistical_Analysis_Washingtonstate
## Project Overview

Electric vehicles have been revolutionising the world, and as part of sustainability, individuals are shifting towards EV adoption. On the other hand, technological advancements, such as self-driving capabilities, are further reshaping the EV landscape. With this, it becomes essential that we analyse the patterns and trends for future developments and adoption of EVs. This led to the beginning of the analysis, where I utilised an open-source dataset of registered EVs through the Washington State Department of Licensing. For the analysis purpose IBM SPSS application has been utilised to perform the statistical tests. 

The main objective of the analysis involves:
1. To examine the relationship between Electric Vehicle type, Battery Range, Clean Alternative Fuel Vehicle (CAFV) Eligibility, Make(Brand of the EV), Model
2. To understand the Market trend and identify any top brands
## Dataset Information
The dataset has been obtained from the official Washington State open data portal: https://data.wa.gov/Transportation/Electric-Vehicle-Population-Data/f6w7-q2d2/about_data.

The dataset consists of information on Battery Electric Vehicles(BEVs) and Plug-in Hybrid Electric Vehicles(PHEV) that are currently registered through the Washington State Department of Licensing(DOL). The dataset initially consisted of 232k observations with 17 columns; each row has information on the registered EV. 

Out of 17 variables, I have considered six key variables for my analysis. Below are the key variables that have been considered in the study.  

![image](https://github.com/user-attachments/assets/163b6ce6-9eba-4f09-a37d-868220737b55)
## Data Cleaning
1. Excluded the rows with missing County and City observations of 4 rows. 
2. Analysis intended on focusing on CAFVs that are eligible and which are not, so around 136k observations whose CAFV is "Eligibility unknown as battery range is not researched" has been removed
3. The column with Base MSRP has been ignored due to the many observations indicating zero as Base MSRP(Manufacturer Suggested Retail Price), which could skew the analysis.
4. After performing the above, 95k observations are left for analysis. 
## Research Questions analysed
1. Is there a significant difference in the electric range between Battery Electric Vehicles (BEVs) and Plug-in Hybrid Electric Vehicles (PHEVs)?
2. Is there a relationship between the model year and the electric range of electric vehicles?
3. Are Battery Electric Vehicles more likely to be CAFV eligible than Plug-in Hybrid Electric Vehicles?
4. Is there a significant relationship between the model year and electric range for Tesla electric vehicles registered in Washington State? 
## Statistical Analysis Performed
Descriptive Statistics such as pie charts and bar graphs have been utilised to understand the key trends and significant EV brands registered through Washington DOL.

An independent sample t-test was performed to compare the mean differences between the electric range and the electric vehicle type. 

Pearson correlation test has been utilised to understand the relationship between model year and electric range. This test has been mainly utilised as the variables involved are both continuous, and the Pearson correlation coefficient value can be utilised to analyse the relationship between 2 continuous variables. 

To find any significant relationship, a chi-square test was performed between two categorical variables, i.e., electric vehicle type and CAFV eligibility. 

Linear regression is being performed on the model year, and electric range of Tesla EVs registered in Washington State. A scatterplot is also plotted to understand Tesla's growth among customers. 
## Interpretations of Results
### Independent Sample T-Test in difference in Electric Range between BEV and PHEV
1. Independent Samples t-test (p < 0.001): Significant difference in electric range between BEVs (198.22 miles) and PHEVs (31.21 miles).
2. Levene's Test for Equality of Variances (p < 0.001): We use the "Equal variances not assumed” results as unequal variances observed.
3. t-value (489.552) and p-value (< 0.001): Strong evidence of a significant difference in electric range among EV types.
4. Effect Size (Cohen's d = 52.179): Extremely large effect size, indicating a very strong difference in electric range between the two vehicle types.
5. Confidence Interval: The range is between 166.34 and 167.68 miles, further confirming the large difference in the electric range.
6. BEVs have a significantly higher electric range than PHEVs, with a very strong effect size.
### Pearson Correlation on Model Year & Electric Range
1. Pearson Correlation (-0.185): Weak negative correlation between Model Year and Electric Range.
2. Statistical Significance (p-value < 0.001): The correlation is statistically significant at 0.01.
3. Confidence Interval (-0.191 to -0.179): A 95% confidence interval confirms the negative correlation and statistical significance.
4. Newer model years EVs tend to have slightly lower electric ranges with a weak relationship.
### Chi-Square test for CAFV Eligibility across EV types
1. Chi-Square Test (p < 0.001): Significant association between CAFV eligibility and electric vehicle type (BEV vs. PHEV).
2. Cramer's V (0.550): Strong association between the two variables.
3. Observed vs. Expected Counts: The observed count of BEVs and PHEVs eligible for CAFV differ broadly, suggesting that these variables are independent.
4. The electric vehicle type significantly affects eligibility for CAFV incentives
### Regression Test to determine Electric Range significance with Model years for Electric Vehicles
1. Pearson Correlation: A moderate positive relationship (0.651) between model year and electric range.
2. Significance: The relationship is statistically significant (p < 0.001), confirming it’s not by chance.
3. R-squared: 42.4% of the variance in the electric range can be explained by model year.
4. Unstandardised coefficient(b): Each additional model year increases the electric range by 13.95 miles.
5. Standardised coefficient(β): For each standard deviation increase in the model year, the electric range increases by 0.651 standard deviations.
6. The model year significantly predicts the electric range for Tesla vehicles in Washington State.
7. The electric vehicle type significantly affects eligibility for CAFV incentives
## Limitations
1. Base MSRP(lowest Manufacturer-suggested retail price) column has not been considered for analysis because the number of observations is 0.
2. Findings apply only to vehicles with known CAFV status and may not reflect the EV population.
3. The analysis doesn't represent all the regions restricted with EVs registered from Washington State DOL.
4. Other factors influencing EV adoption, such as charging infrastructure, price, etc., were absent in the dataset, limiting further analysis. 
## Key Findings/Observations
1. Tesla highlights its market leadership as the most registered EV brand in Washington state and has improved its electric range with new models over the years.
2. BEVs have a longer electric range and higher CAFV eligibility than PHEVs.
3. CAFV eligibility is strongly associated with Electric vehicle type (mostly BEVs) with sufficient Electric range.
4. Various manufacturers offer different BEV and PHEV options to meet consumer needs.
5. The different correlations between model year and electric range in the dataset and the Tesla-only condition are due to the varying mix of BEVs and PHEVs.














