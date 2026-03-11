### Population Transience (Z-Score)

**Description:**
This field (identified as `ZPopulationTransience` in the spatial dataset) represents the standardized Z-score for the Residential Mobility Index within a given Lower Super Output Area (LSOA). It measures the level of population turnover or transience in a specific neighbourhood and compares it to the national average across England. 

**Vulnerability Rationale:**
This metric is the core indicator for the "Local Knowledge" domain, which is utilized to evaluate a community's "(In)ability to Prepare" and "(In)ability to Respond" to climate hazards like floods and heatwaves. 

Higher proportions of people who are new to an area (high population transience) indicate a higher level of social vulnerability. Communities with high population turnover generally have a lower adaptive capacity for several reasons:
*   **Lack of Risk Awareness:** New residents are less likely to be aware that their new community has historical flood or heat risk issues.
*   **Limited Informal Support:** People who have recently moved may lack local community networks and family ties that typically provide vital informal clues, hazard warnings, and emergency assistance. 
*   **Unfamiliarity with Services:** Transient populations often have less knowledge about how to properly respond to an event and where to seek local and national support services if they are affected.

**Interpretation:**
Because this metric is standardized as a Z-score, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher rate of population transience than the national average, indicating a higher level of social vulnerability.
*   **Values around 0** indicate that the population turnover rate is approximately average for England.
*   **Negative values** signify a lower rate of transience (a more established, stable population) than the national average, indicating lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the 2022 England LSOA dataset, the underlying data for this indicator is derived from the Consumer Data Research Centre (CDRC) 2021, specifically utilizing the CDRC Residential Mobility Index (representing the average from 2012–2020). Depending on the specific index being calculated (e.g., Heat vs. Flood, Prepare vs. Respond), it carries varying weights within the broader "Local Knowledge" domain alongside indicators like past flood experience.