### Heat Disadvantage, recent past 30 year mean 1990 - 2019

**Description:**
This field (identified internally as `ZHeatDisadvantageRecentPast` in the spatial dataset) represents the overall relative heat disadvantage for a given Lower Super Output Area (LSOA) during the recent past baseline period (1990–2019). It serves as a composite metric to map how heat-related social vulnerability combines with the actual geographic exposure to extreme high temperatures.

**Hazard and Vulnerability Context:**
The concept of "Heat Disadvantage" accounts for both the likelihood of a community coming into contact with extreme heat and the severity of the negative impacts on health and well-being that would result from that contact. 

This specific field is calculated as an equally weighted combination of two key components:
1.  **Hazard Exposure:** Localized climate data representing the average daily-maximum temperature of the top 5% hottest days in the 1990–2019 period. 
2.  **Social Vulnerability:** The Socio-Spatial Heat Vulnerability Index (SSHVI) for the LSOA as a whole, which measures the community's sensitivity, enhanced exposure, and inability to prepare, respond, and recover from heat events.

**Interpretation:**
The field is presented as a standardized Z-score to allow for relative comparison across different geographic areas. The scores are classified as follows:
*   **Positive values (High scores):** Denote areas with higher heat disadvantage than the English average. The severity is categorized by how high the score is: ≥ 2.5 is "Acute", 1.5 to 2.5 is "Extremely high", and 0.5 to 1.5 is "Relatively high".
*   **Values around 0 (-0.5 to 0.5):** Denote areas where the heat disadvantage is approximately equal to the average for England.
*   **Negative values (Low scores):** Denote areas with lower heat disadvantage than the English average, scaling down through "Relatively low", "Extremely low", and "Slight".

**Data Source:**
For the 2022 dataset, the underlying climate hazard data is derived from the analysis of Kennedy-Asser et al. (2022), utilizing regional climate model simulations from the UK Climate Projections 2018 (UKCP18). This is then combined with the SSHVI calculated from Census and other socio-economic data sources.