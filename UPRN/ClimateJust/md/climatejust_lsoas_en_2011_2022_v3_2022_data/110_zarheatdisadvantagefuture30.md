### Relative heat Disadvantage, 3℃ warmer world

**Description:**
This field (identified internally as `ZarHeatDisadvantageFuture30` in the spatial dataset) represents the final "all-relative" heat disadvantage score for a given Lower Super Output Area (LSOA) under a projected future scenario where global average surface temperatures are 3°C warmer than pre-industrial levels. 

**Hazard and Vulnerability Context:**
The concept of "Heat Disadvantage" acts as a composite metric identifying where extreme heat hazard-exposure and socio-spatial vulnerability coincide. It is calculated as an equally weighted combination of two key localized factors for each LSOA:
1.  **Climate Hazard Data:** The projected average daily-maximum temperature for the top 5% of hottest days in a 3°C warmer world.
2.  **Social Vulnerability:** The local Socio-Spatial Heat Vulnerability Index (SSHVI) score.

**Interpretation and Standardization:**
This metric is provided as an **All-relative Z-score**. Crucially, this means the score is calculated using the mean and standard deviation across *all four* of the dataset's temperature scenarios (the recent past baseline, plus the 1.5°C, 2°C, and 3°C warmer worlds). This specific method of standardization enables users to make direct comparisons of relative heat disadvantage not only across different geographic neighbourhoods, but also across the different future warming scenarios. 

Based on the dataset's classification scheme, the scores are interpreted as:
*   **Positive values (High scores):** Denote higher heat disadvantage compared to the overall average. Scores ≥ 2.5 are classified as "Acute", 1.5 to 2.5 as "Extremely high", and 0.5 to 1.5 as "Relatively high".
*   **Values around 0 (-0.5 to 0.5):** Denote heat disadvantage that is around the average for England.
*   **Negative values (Low scores):** Denote lower heat disadvantage compared to the average, scaling down through "Relatively low" (-0.5 to -1.5), "Extremely low" (-1.5 to -2.5), and "Slight" (≤ -2.5).

**Data Source:**
For the 2022 dataset update, the underlying climate hazard data is derived from the analysis of Kennedy-Asser et al. (2022), which utilizes regional climate model simulations from the UK Climate Projections 2018 (UKCP18). This is combined equally with the dataset's internal SSHVI mapping.