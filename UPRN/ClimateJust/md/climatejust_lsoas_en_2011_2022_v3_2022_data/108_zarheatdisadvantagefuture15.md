### Relative heat Disadvantage, 1.5℃ warmer world

**Description:**
This field (identified internally as `ZarHeatDisadvantageFuture15` in the spatial dataset) represents the final "all-relative" heat disadvantage for a given Lower Super Output Area (LSOA) under a projected future scenario where global average surface temperatures are 1.5°C warmer than pre-industrial levels. 

**Hazard and Vulnerability Context:**
The concept of "Heat Disadvantage" identifies where extreme heat hazard-exposure and socio-spatial vulnerability coincide. This field is calculated as an equally weighted combination of two key localized factors for each LSOA:
1.  **Climate Hazard Data:** The projected average daily-maximum temperature for the top 5% hottest days in a 1.5°C warmer world.
2.  **Socio-Spatial Heat Vulnerability Index (SSHVI):** The area's overall social vulnerability score, encompassing sensitivity, enhanced exposure, and the inability to prepare, respond, and recover from heat events.

**Interpretation and Standardization:**
Unlike standard Z-scores that compare areas only within a single timeframe, this metric is provided as an **"All-relative Z-score"**. The score is calculated using the mean and standard deviation across *all* of the dataset's temperature scenarios (the recent past baseline, plus the 1.5°C, 2°C, and 3°C warmer worlds). This specific method of standardization allows users to directly compare relative heat disadvantage not only across different geographic neighbourhoods, but also across the different future warming scenarios. 

Based on the dataset's all-relative classification scheme, the scores are interpreted as:
*   **Positive values (High scores):** Denote higher heat disadvantage compared to the overall average. Scores ≥ 2.5 are classified as "Acute", 1.5 to 2.5 as "Extremely high", and 0.5 to 1.5 as "Relatively high".
*   **Values around 0 (0.5 to -0.5):** Denote heat disadvantage that is around the average for England.
*   **Negative values (Low scores):** Denote lower heat disadvantage compared to the average, scaling down through "Relatively low" (-0.5 to -1.5), "Extremely low" (-1.5 to -2.5), and "Slight" (≤ -2.5).

**Data Source:**
For the 2022 dataset update, the underlying climate hazard data is derived from the analysis of Kennedy-Asser et al. (2022), which utilizes regional climate model simulations from the Met Office's UK Climate Projections 2018 (UKCP18). This is combined equally with the dataset's internal SSHVI mapping.