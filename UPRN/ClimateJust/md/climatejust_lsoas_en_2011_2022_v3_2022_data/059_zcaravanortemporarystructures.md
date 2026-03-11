### Caravan or other mobile or temporary structures (Z-Score)

**Description:**
This field (identified as `ZCaravanOrTemporaryStructures` in the spatial dataset) represents the standardized Z-score for the percentage of households living in a caravan, or other mobile or temporary structures, within a given Lower Super Output Area (LSOA). It measures how the local concentration of such temporary housing in a specific neighbourhood compares to the national average across England. 

**Vulnerability Rationale:**
This metric is a core indicator within the "Housing Characteristics" domain, which is utilized to evaluate a community's "Enhanced Exposure" to flooding events. 

A higher proportion of households living in caravans or temporary structures indicates a higher level of social vulnerability. The primary reasons driving this vulnerability include:
*   **Physical Protection:** Poor quality or temporary housing provides significantly less structural protection against floodwaters than permanent, structurally competent buildings. In severe events, floodwaters can quickly devastate these homes and place lives at direct risk.
*   **Warning Response:** Residents in mobile or temporary structures often demonstrate a lower response rate to flood warnings because they are less likely to have a safe, elevated place to move their possessions. 
*   **Local Knowledge:** Evidence suggests that residents of caravan parks are more likely to be transient and consequently possess limited knowledge of the local area and its historical flood risks.
*   **Economic Appraisal:** In standard institutional project appraisals for flood defences, caravans are often considered "moveable," meaning their potential damages are rarely counted when justifying the cost of new flood defences.

**Interpretation:**
Because this metric is standardized as a Z-score, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher proportion of temporary/mobile structures than the national average, indicating higher enhanced exposure and greater relative vulnerability.
*   **Values around 0** indicate that the proportion is approximately average for England.
*   **Negative values** signify a lower proportion than the national average, indicating lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the 2022 England LSOA dataset, no direct update was available, so the underlying data relies on the 2011 UK Census (table KS401: 'All household spaces: Caravan or other mobile or temporary structure' divided by the total number of households). It carries a weight of 0.500 within the broader "Housing Characteristics" domain alongside the homelessness rate indicator for the calculation of the Socio-Spatial Flood Vulnerability Index.