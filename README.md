# Short Description
This study uses the case of Latinx panethnicity as an opportunity to better understand the political and cultural processes that underlie the adoption of ethnoracial labels. To date the research on the issue has largely focused on the state or on ethnic elites, and thus reveals how many of the identity labels we see today are a product of politically negotiated compromises between these two factions. Yet much less is known about label diffusion within target populations and how the politics of label construction might be reflected in adoption patterns among Latinxs. This research provides important theoretical insight by making explicit the role of generational politics in ethnoracial label adoption. While US racial history is saturated with examples of how politicized youth, especially the 60’s generation, pioneered and adopted unique identity labels that eventually became widely institutionalized, this fact has been underemphasized within sociological research on ethnoracial identity labels. This paper centralizes the issue and discusses how generational politics can be integrated into our understanding of label diffusion and panethnic adoption among Latinxs. 

To better understand adoption patterns among Latinxs, the author ran a binomial logistic regression in R predicting for panethnic adoption on a number of covariates, including all birth cohorts since the baby boomers. Before running the analysis, the author used RStudio to load, clean, and subset the 2020 IGS dataset, which asks respondents about their panethnic preferences. He then used ggplot to visualize panethnic adoption by several covariates. Finally, he ran a binomial logistic regression and created a regression table using stargazer. 

# Dependencies

R, version 1.2.5033

# Files
## Data

Latinx.csv: January 2020 Institute of Governmental Studies (IGS) dataset. Online analysis of dataset available here: https://dlab.berkeley.edu/data-resources/california-polls#IGSPOLL

Latinx_subset.csv: The final analysis dataset derived from the IGS dataset. This new dataset contains observations for the following variables:
  - Latinx_panethnic: Respondents use of Panethnic labels
  - Cohorts: Birth cohorts (boomers, gen x, millenials, and gen z) 
  - Ethnicity: Ethnic background (Mexican, Central American, South American, and Other)
  - Immigrant_Generation: Immigrant generation (First Generation, Second Generation, Third Generation & plus)
  - Political_Leanings: Political bent (liberal, moderate, conservative)
  - Gender: gender
  - HouseholdIncome: Income
  - Education: Highest degree acheived (HS, some college/Associates, Bachelors, Graduate)
## Code

01_Setup.Rmd: Loads Latinx raw dataset, creates variables for analysis, and creates final analysis dataset. 

02_Visualizations.Rmd: Conducts descriptive analysis of the data, producing bar graphs showing panethnic adoption by birth cohort, ethncity, and immigrant generation.

03_Regression Table.Rmd: Runs binomial logistic regression predicting for panethnic adoption and creates regression table using stargazer

## Results

Figure_01_Panethnic_by_Ethnicity.png: Graphs panethnic adoption by ethinicity.

Figure_02_Panethnic_by_Immigrant_Generation.png: Graphs panethnic adoption by Immigrant generation.

Figure_03_Panethnic_by_Cohort.png: Graphs panethnic adoption by birth cohort.

Regression Table.txt: Summarizes the results of binomial logistic regression, predicting panethnic adoption on a number of covariates.
