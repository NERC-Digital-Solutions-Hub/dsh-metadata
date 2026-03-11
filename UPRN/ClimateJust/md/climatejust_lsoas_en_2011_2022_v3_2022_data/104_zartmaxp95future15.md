### 1.5℃ warmer world (All-relative Z-Score)

**Description:**
This field (identified internally as `ZarTmaxP95Future15` in the spatial dataset) represents the standardized "All-relative Z-score" for the projected average daily-maximum temperature of the top 5% hottest days within a given Lower Super Output Area (LSOA). This projection models extreme heat exposure under a scenario where global mean surface temperatures are 1.5°C warmer than pre-industrial conditions.

**Hazard Context and Standardization:**
Unlike standard Z-scores that only compare areas within a single timeframe, this "All-relative" score is calculated using the mean and standard deviation across *all* four of the dataset's temperature scenarios: the recent past (1990–2019), 1.5°C, 2°C, and 3°C warmer worlds. This specific standardization method is designed to enable users to directly compare relative temperature extremes not only across different geographic locations but also across the different future warming scenarios. 

**Interpretation:**
Based on the all-relative Z-score classification scheme:
*   **Positive values (High scores):** Denote that the projected extreme temperatures for the area under a 1.5°C warming scenario are higher than the overall multi-scenario average for England. Scores ≥ 2.5 are classified as "Acute", 1.5 to 2.5 as "Extremely high", and 0.5 to 1.5 as "Relatively high".
*   **Values around 0 (-0.5 to 0.5):** Denote that the projected extreme temperatures are approximately equal to the overall average for England.
*   **Negative values (Low scores):** Denote that the projected extreme temperatures are lower than the overall average.

**Data Source:**
For the updated 2022 England LSOA dataset, the underlying climate hazard data is derived from the analysis of Kennedy-Asser et al. (2022), which utilizes regional climate model simulations on a 12km grid over the UK from the Met Office Hadley Centre's UK Climate Projections 2018 (UKCP18).