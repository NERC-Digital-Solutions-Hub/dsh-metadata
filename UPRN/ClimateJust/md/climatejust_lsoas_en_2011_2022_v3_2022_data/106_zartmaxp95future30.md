### 3℃ warmer world (All-relative Z-Score)

**Description:**
This field (identified internally as `ZarTmaxP95Future30` in the spatial dataset) represents the standardized "All-relative Z-score" for the projected average daily-maximum temperature of the top 5% hottest days within a given Lower Super Output Area (LSOA). This specific projection models extreme heat exposure under a future scenario where global average surface temperatures are 3°C warmer than pre-industrial levels.

**Hazard Context and Standardization:**
Unlike standard Z-scores that evaluate an area only against others within the same timeframe, this "All-relative" score is calculated using the mean and standard deviation across *all four* of the dataset's temperature scenarios: the recent past (1990–2019), and the 1.5°C, 2°C, and 3°C warmer worlds. This specific method of standardization is designed to enable users to directly compare temperature extremes not only across different geographic neighbourhoods but also across the different future warming scenarios. 

**Interpretation:**
Because this field is presented as an all-relative Z-score, it evaluates how a specific neighbourhood's projected extreme heat under a 3°C warming scenario compares to the overall multi-scenario average for England:
*   **Positive values (High scores):** Denote that the projected extreme temperatures for the area are higher than the overall multi-scenario average. Scores ≥ 2.5 are classified as "Acute", 1.5 to 2.5 as "Extremely high", and 0.5 to 1.5 as "Relatively high".
*   **Values around 0 (-0.5 to 0.5):** Denote that the projected extreme temperatures are approximately equal to the overall average for England.
*   **Negative values (Low scores):** Denote that the projected extreme temperatures are lower than the overall average.

**Data Source:**
For the 2022 England LSOA dataset, the underlying climate hazard data is derived from the analysis of Kennedy-Asser et al. (2022), which utilizes regional climate model simulations on a 12km grid over the UK from the Met Office Hadley Centre's UK Climate Projections 2018 (UKCP18).