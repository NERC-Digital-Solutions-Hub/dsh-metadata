### Disadvantage (all potentially exposed, Z-Score)

**Description:**
This field represents the final Flood Disadvantage score for a given Lower Super Output Area (LSOA). It provides a relative measure of disadvantage by taking into account **all potentially exposed people**, irrespective of whether their area is protected by existing flood defences. A null value in this field indicates that there is no exposed population in that specific neighbourhood. 

**Methodology:**
Flood disadvantage is calculated as an equally weighted combination of two main factors:
1.  The degree of population-based exposure to flood risk within the LSOA.
2.  The Socio-Spatial Flood Vulnerability Index (SSFVI) for the LSOA as a whole.

**Interpretation:**
The metric is standardized as a Z-score to allow for direct relative comparison across neighbourhoods in England:
*   **Positive values** denote that the population is more potentially exposed and disadvantaged than the national average.
*   **Values around 0** indicate that the level of potential exposure and disadvantage is approximately average for England.
*   **Negative values** signify that fewer people are potentially exposed and disadvantaged compared to the national average.

To help map and categorize the relative severity of this disadvantage, the Z-scores are grouped into the standard dataset classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight