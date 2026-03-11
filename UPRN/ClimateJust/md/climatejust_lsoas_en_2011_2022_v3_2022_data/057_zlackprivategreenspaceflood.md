### Lack of domestic gardens (Z-Score)

**Description:**
This field (identified in the spatial dataset under aliases such as `ZLackPrivateGreenspaceFlood` or `ZLackPrivateGreenspaceHeat`) represents the standardized Z-score for the percentage of dwellings without private domestic gardens within a given Lower Super Output Area (LSOA). It measures how the local lack of private garden space in a specific neighbourhood compares to the national average across England.

**Vulnerability Rationale:**
This metric is a core indicator within the "Physical Environment" domain, which is primarily utilized to evaluate a community's "Enhanced Exposure" to extreme weather events like heatwaves and floods. 

The rationale for this indicator is that domestic gardens provide vital environmental functions that can offset the severity of extreme weather:
*   **Heatwaves:** Gardens provide a natural cooling function. Areas where housing has relatively small or no gardens are more likely to experience severe heatwave impacts due to higher temperatures.
*   **Flooding:** Gardens provide pervious surfaces that allow for better natural drainage, mitigating the impacts of surface water flooding. 

Therefore, a higher ratio of buildings to domestic gardens (a lack of gardens) indicates a higher level of environmental exposure and social vulnerability. 

**Interpretation:**
Because this metric is standardized as a Z-score, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher percentage of dwellings without gardens than the national average, indicating higher enhanced exposure and greater vulnerability.
*   **Values around 0** indicate that the proportion is approximately average for England.
*   **Negative values** signify a lower lack of gardens (i.e., more homes have access to private garden space) than the national average, indicating lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the 2022 England LSOA dataset, the underlying data is derived from the Office for National Statistics (ONS) Greenspace dataset, specifically utilizing the indicator that measures the percentage of dwellings without gardens. It carries a weight of 0.330 within the broader "Physical Environment" domain, sharing this dimension with indicators for built-up areas and the size of local public greenspaces.