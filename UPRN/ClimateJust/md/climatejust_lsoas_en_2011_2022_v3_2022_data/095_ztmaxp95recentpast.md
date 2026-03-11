### Average temperature of top 5% hottest days, recent past 30 year mean 1990 - 2019 (Score)

**Description:**
This field (identified internally as `ZTmaxP95RecentPast` in the spatial dataset) represents the standardized score for the average daily-maximum temperature of the top 5% hottest days during the recent past period (1990–2019) within a given Lower Super Output Area (LSOA). 

**Hazard and Vulnerability Context:**
Unlike the raw temperature measurement (in degrees Celsius), this metric is provided as an "All-relative Z-score". This means the score is calculated using the mean and standard deviation across *all* of the dataset's temperature scenarios, which includes the recent past baseline as well as future projections for 1.5°C, 2°C, and 3°C warmer worlds. This specific standardization method enables direct comparison of extreme heat exposure not only across different geographic areas but also across different timeframes and warming scenarios. 

**Interpretation:**
Based on the all-relative Z-score classification scheme:
*   **Positive/Higher scores:** Denote geographical areas that experienced relatively higher extreme temperatures during their hottest days between 1990 and 2019 compared to the overall multi-scenario average. 
*   **Values around 0:** Denote temperatures that are around the overall average for England.
*   **Negative/Lower scores:** Indicate areas that historically experienced relatively lower extreme temperatures.

**Data Source:**
For the 2022 England LSOA dataset, the underlying climate data used to calculate this score is derived from the analysis of Kennedy-Asser et al. (2022), which utilizes regional climate model simulations on a 12km grid over the UK from the Met Office Hadley Centre's UK Climate Projections 2018 (UKCP18).