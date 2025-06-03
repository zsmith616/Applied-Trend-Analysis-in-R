# Applied Trend Analysis R Workshop
This repository contains materials for the Applied Trend Analysis in R workshop, covering the fundamentals of trend analysis, focusing on detecting and identifying for further investigation anomalies in public health surveillance data using the excessmort R package. The workshop was developed for the CSTE Annual Meeting on June 8, 2025. 

## What you'll learn
Participants will learn how to: 
1. Explain the utility of trend analysis to identify events of public health significance
2. Apply  regression modeling to detect and visualize anomalies in example datasets using the provided tools
3. Identify strengths and limitations and interpret public health implications of trend analysis results
4. Brainstorm additional public health applications for these tools in their communities

## Data Sources
We are using all-cause mortality data downloaded from CDC Wonder and adjusted for this training. **The data do not represent actual data from Michigan, but were transformed in a way to maintain the overall trends for training purposes. Please do not use the data for anything beyond learning purposes.**

The process of transforming the data included downloading county-level underlying cause of death data by county and month for Michigan from 2010 to 2020 from CDC Wonder. We also pulled count of death data grouped by month, race, county, and age group (18-64 and 65+). When death counts for a group were between 1 and 9, data were suppressed by CDC Wonder to protect privacy. We manipulated the aggregate data into line level data and assigned the suppressed data values between 1 and 9 based on the total sums for each grouping. 

Population estimates to calculate mortality rates were obtained using Census and American Community Surveys population estimates for Michigan between 2010 and 2020.

## Repository Contents
1. Slides from training explaining the background, data sources, analysis process and interpretation of results.

2. The following R scripts are included in the repository:
- 1_data_prep_walkthrough.R: Overview of how to prepare data for the analysis
- 2_trend_analysis_walkthrough.R: Overview of how to conduct the trend analysis
- 3_trend_analysis-guidedpractice.R: A script to test your understanding and application of data preparation and trend analysis. User must fill in the blanks and answer questions to get code to run.
- 3a_trend_analysis_gp_answerkey.R: Answer key for the first guided practice.
- 4_subgroup_analyses_walkthrough.R: Overview of how to conduct a subgroup analysis.
- 5_county_subanalysis_guided_practice.R: A script to test your understanding and application of conducting a subanalysis. User must fill in the blanks and answer questions to get code to run.
- 5a_county_subanalysis_answer_key.R: Answer key for the second guided practice.

3. The following data files are included in the repository:
- linelist_2010-2020_mi.csv: The line list mortality data from Michigan downloaded and adjusted from CDC Wonder. Use for training purposes only. 
- population_data.csv: Population data used in script 1 and 2.
- demo_by_year_2010-2020_MI.csv: Population data by year used in scripts 3 and 4.
- demo_by_year_by_age_2010-2020_MI.csv: Population data by age used in scripts 3 and 4.
- demo_by_year_by_county_2010-2020_MI.csv: Population data by county and year used in scripts 3 and 4.
- demo_by_year_by_race_2010-2020_MI.csv: Population data by race used in scripts 3 and 4.

## About the Training
This workshop was developed by members of the Johns Hopkins Bloomberg School of Public Health Surveillance & Outbreak Response Team. The excessmort R package, which is the focus on the training, was developed by Rafael Irizarry and Rolando Acosta and more information can be found at https://cran.r-project.org/web/packages/excessmort/vignettes/excessmort.html.

## License
All materials in this repository are shared under the Applied Trend Analysis in R © 2025 by BSPH Surveillance & Outbreak Response Team licensed under CC BY-NC 4.0. To view a copy of this license, visit https://creativecommons.org/licenses/by-nc/4.0/



