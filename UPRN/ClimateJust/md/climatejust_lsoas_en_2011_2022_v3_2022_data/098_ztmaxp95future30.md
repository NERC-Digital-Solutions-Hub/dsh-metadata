### Average temperature of top 5% hottest days, 3℃ warmer world (Score)

**Description:**
This field (identified internally as `ZTmaxP95Future30` in the spatial dataset) represents the standardized score (Z-score) of the projected average daily-maximum temperature during the top 5% hottest days for a given Lower Super Output Area (LSOA). This projection specifically models extreme heat exposure under a scenario where global average surface temperatures are 3°C warmer than the pre-industrial period. 

**Hazard and Vulnerability Context:**
This metric serves as a standardized indicator of projected future extreme heat exposure. Within the wider Climate Just framework, these measures of localized heat hazard exposure are combined equally with the Socio-Spatial Heat Vulnerability Index (SSHVI) to calculate the overall relative "Heat Disadvantage" for a neighbourhood. 

**Interpretation:**
Because this field is presented as a standard Z-score, it evaluates how a specific neighbourhood's projected extreme heat compares to the average across England specifically *within* this 3°C warming scenario:
*   **Positive values (High scores):** Denote that the projected temperatures for the hottest days in the area are higher than the English average, indicating greater exposure to extreme heat hazards. Scores ≥ 2.5 are classified as "Acute", while scores between 1.5 and 2.5 are "Extremely high".
*   **Values around 0:** Denote that the projected extreme temperatures are approximately equal to the average for England.
*   **Negative values (Low scores):** Denote that the projected extreme temperatures are lower than the English average.

*Note on Standardization:* The dataset provides this standard Z-score as well as an "All-relative Z-score" (`ZarTmaxP95Future30`). While this standard score compares areas within the single 3°C scenario, the all-relative Z-score is calculated using the mean and standard deviation across *all* temperature scenarios (recent past, 1.5°C, 2°C, and 3°C) to enable direct comparisons of temperature extremes between different future warming scenarios.

**Data Source:**
For the 2022 England LSOA dataset, the underlying climate data is derived from the analysis of Kennedy-Asser et al. (2022). Their research utilizes regional climate model simulations on a 12km grid over the UK from the Met Office Hadley Centre's UK Climate Projections 2018 (UKCP18).