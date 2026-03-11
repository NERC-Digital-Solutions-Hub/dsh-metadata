### Heat Disadvantage, 2℃ warmer world

**Description:**
This field (identified internally as `ZHeatDisadvantageFuture20` in the spatial dataset) represents the relative heat disadvantage for a given Lower Super Output Area (LSOA) under a future climate scenario where the global average surface temperature is 2°C warmer than the pre-industrial period. It serves to map how pre-existing heat-related social vulnerabilities combine with projected future geographic exposure to extreme high temperatures.

**Hazard and Vulnerability Context:**
The concept of "Heat Disadvantage" accounts for both the likelihood of a community coming into contact with extreme heat hazards and the severity of the negative impacts on health and well-being that could result from that contact. 

This composite metric is calculated as an equally weighted combination of two key factors:
1.  **Hazard Exposure:** Projected localized climate data representing the average daily-maximum temperature of the top 5% hottest days in a 2°C warmer world. 
2.  **Social Vulnerability:** The Socio-Spatial Heat Vulnerability Index (SSHVI) for the local area, which measures the community's overall sensitivity, enhanced exposure, and inability to prepare, respond, and recover from extreme heat events.

**Interpretation:**
The field is presented as a standardized Z-score to allow for relative comparison across different geographic areas. The scores are classified as follows:
*   **Positive values (High scores):** Denote areas with higher heat disadvantage than the English average. The severity is categorized by how high the score is: ≥ 2.5 is "Acute", 1.5 to 2.5 is "Extremely high", and 0.5 to 1.5 is "Relatively high".
*   **Values around 0 (-0.5 to 0.5):** Denote areas where the heat disadvantage is approximately equal to the average for England.
*   **Negative values (Low scores):** Denote areas with lower heat disadvantage than the average, scaling down through "Relatively low" (-0.5 to -1.5), "Extremely low" (-1.5 to -2.5), and "Slight" (≤ -2.5).

*Note on Standardization:* The dataset provides this standard Z-score as well as an "All-relative Z-score" (`ZarHeatDisadvantageFuture20`). While the standard score compares areas within this single 2°C scenario, the all-relative Z-score is calculated using the mean and standard deviation across *all* temperature scenarios (recent past, 1.5°C, 2°C, and 3°C) to enable direct comparisons of relative heat disadvantage between different warming futures.

**Data Source:**
For the 2022 dataset, the underlying future climate hazard data is derived from the analysis of Kennedy-Asser et al. (2022), which utilizes regional climate model simulations from the UK Climate Projections 2018 (UKCP18). This is combined with the local SSHVI, which is calculated from Census and other socio-economic data sources.