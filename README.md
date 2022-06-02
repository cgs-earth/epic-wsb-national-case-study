# epic-wsb-national-case-study
This repository organizes the production of a national case study of Water Service Boundaries and their prospective impact on Justice40 metrics


## Research Question

What is the impact of adding a drinking water - based indicator to the Justice40 CEJST framework? On...

1. The number (and %) of tracts added
2. The population (and %) added
3. The characteristics of the population added (race/ethnicity, income, population density/ urban/ rural), and the differences in this population from the baseline overall and CEJST populations

## Data

1. The existing [CEJST tract layer](https://screeningtool.geoplatform.gov/en/downloads)
2. The SDWIS ["Serious Violator" List](https://echo.epa.gov/files/echodownloads/SDWA_latest_downloads.zip) Instead we need to do all health-based MCL violations
3. The SimpleLab WSB layer 

## Methods

1. Restrict SimpleLab layer to Tier 1 boundaries only. 
  * Further restrict away the "entire county" type boundaries

2. Restrict Census 2010-19 tract boundaries to boundaries that intersect the water service boundaries subsetted in step 1

3. Join by PWSID the SDWIS serious violator list. Construct PWSID-level variables = ```on serious violator list for at least one quarter in the last year/5 years/ 10 years```

4. Calculate the research metrics, using the tracts interseting the Tier 1 boundary subset as the baseline. As a secondary baseline, we can use another comparison with Utah's current estimated boundaries with Utah's DWR-provided boundaries. 

## Outputs

1. A layer file
2. An interactive web viewer
3. A report with tabular descriptive statistics and charts as appropriate
