### Heat Disadvantage, 1.5℃ warmer world

**Description:**
This field (identified internally as `ZHeatDisadvantageFuture15` in the spatial dataset) represents the overall relative heat disadvantage for a given Lower Super Output Area (LSOA) under a projected future scenario where global average surface temperatures are 1.5°C warmer than pre-industrial levels. 

**Hazard and Vulnerability Context:**
The concept of "Heat Disadvantage" identifies where extreme heat hazard-exposure and socio-spatial vulnerability coincide. It accounts for both the likelihood of a community coming into contact with severe high temperatures and the severity of negative health and well-being impacts that could result from that contact. 

This metric is calculated as an equally weighted combination of two factors for each LSOA:
1.  **Climate Hazard Data:** The projected average daily-maximum temperature for the top 5% hottest days in a 1.5°C warmer world.
2.  **Socio-Spatial Heat Vulnerability Index (SSHVI):** The area's social vulnerability score, encompassing factors such as age, health, income, housing characteristics, and access to services.

**Interpretation:**
The raw disadvantage calculation is standardized as a Z-score to allow for relative comparisons across neighbourhoods. Based on the classification scheme:
*   **Positive values (High scores):** Denote higher heat disadvantage compared to the average. Scores ≥ 2.5 are classified as "Acute", scores between 1.5 and 2.5 are "Extremely high", and scores between 0.5 and 1.5 are "Relatively high".
*   **Values around 0 (-0.5 to 0.5):** Denote heat disadvantage that is around the average for England.
*   **Negative values (Low scores):** Denote lower heat disadvantage compared to the average.

**Data Source:**
For the 2022 England LSOA dataset, the climate hazard data is derived from the analysis of Kennedy-Asser et al. (2022), utilizing regional climate model simulations from the Met Office's UK Climate Projections 2018 (UKCP18). This is combined with the dataset's internal SSHVI calculations.