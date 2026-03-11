### Lack of private transport (Z-Score)

**Description:**
This field (identified as `ZLackPrivateTransport` in the spatial dataset) represents the standardized Z-score for the percentage of households that do not have access to a car or van within a given Lower Super Output Area (LSOA). It measures how the local concentration of households lacking private vehicles in a specific neighbourhood compares to the national average across England. 

**Vulnerability Rationale:**
This metric is a core indicator within the "Mobility" domain, which is utilized to evaluate a community's "(In)ability to Respond" and "(In)ability to Recover" from extreme climate events, such as floods and heatwaves. 

Higher proportions of households without private transport indicate a higher level of social vulnerability because a lack of mobility creates severe practical challenges during an emergency. Specifically, householders without private vehicles have a restricted capacity to relocate or evacuate safely, assist dependents, or quickly access essential services (like medical care). Furthermore, these populations are disproportionately affected when extreme weather causes disruptions to public transport networks.

**Interpretation:**
Because this metric is standardized as a Z-score, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher proportion of households without private transport than the national average, indicating a higher level of mobility-related social vulnerability.
*   **Values around 0** indicate that the proportion is approximately average for England.
*   **Negative values** signify better private transport access (a lower proportion of households without cars) than the national average, indicating lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the 2022 England LSOA dataset, no direct update was available for this specific metric, so the underlying data relies on the 2011 UK Census (table KS404 / KS404SC). It specifically calculates the number of households with "no cars or vans" divided by the total number of households. It carries a weight of 0.200 within the broader "Mobility" domain alongside other indicators like disability and care residency.