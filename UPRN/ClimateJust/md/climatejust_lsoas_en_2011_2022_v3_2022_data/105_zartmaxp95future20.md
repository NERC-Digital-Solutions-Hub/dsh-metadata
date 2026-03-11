### 2℃ warmer world (All-relative Z-Score)

**Description:**
This field (identified internally as `ZarTmaxP95Future20` in the spatial dataset) represents the standardized "All-relative Z-score" of the projected average daily-maximum temperature for the top 5% hottest days within a given Lower Super Output Area (LSOA). This specific projection models extreme heat exposure under a scenario where global average surface temperatures are 2°C warmer than the pre-industrial period.

**Hazard and Vulnerability Context:**
Unlike a standard Z-score that only compares areas within a single timeframe, this "all-relative" metric is calculated using the mean and standard deviation across **all four** of the dataset's temperature scenarios (the recent past baseline, plus the 1.5°C, 2°C, and 3°C warmer future worlds). 

This specific method of standardization is highly useful because it enables users to make direct comparisons of extreme heat exposure not only across different geographic areas in England but also across the different future warming scenarios.

**Interpretation:**
Because this field is presented as an all-relative Z-score, it evaluates how a specific neighbourhood's projected extreme heat in a 2°C warmer world compares to the overall multi-scenario average across England:
*   **Positive values (High scores):** Denote geographical areas expected to experience relatively higher extreme temperatures compared to the overall average. Scores ≥ 2.5 are classified as "Acute", while scores between 1.5 and 2.5 are "Extremely high".
*   **Values around 0 (-0.5 to 0.5):** Denote projected temperatures that are approximately equal to the overall multi-scenario average for England.
*   **Negative values (Low scores):** Denote areas projected to experience relatively lower extreme temperatures. 

**Data Source:**
For the 2022 England LSOA dataset, the underlying climate data used to calculate this score is derived from the analysis of Kennedy-Asser et al. (2022). Their research utilizes regional climate model simulations on a 12km grid over the UK from the Met Office Hadley Centre's UK Climate Projections 2018 (UKCP18).