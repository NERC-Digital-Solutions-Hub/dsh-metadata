### Disadvantage (all potentially undefended, Z-Score)

**Description:**
This field represents the final Flood Disadvantage score for a given Lower Super Output Area (LSOA), specifically taking into account **all potentially undefended people**. It accounts for published data on areas protected by river and coastal flood defences to isolate the populations lacking these mapped protections. A null value in this field indicates that either there is no exposed population in that specific neighbourhood, or all of the exposed population within the LSOA is considered defended. 

**Methodology:**
This specific flood disadvantage metric is calculated as an equally weighted combination of two main factors:
1.  The degree of *undefended* population-based exposure to flood risk within the LSOA.
2.  The Socio-Spatial Flood Vulnerability Index (SSFVI) for the LSOA as a whole.

**Interpretation:**
The metric is standardized as a Z-score to allow for direct relative comparisons across neighbourhoods in England:
*   **Positive values** denote that the population is more potentially exposed to undefended flood risks and is more disadvantaged than the national average.
*   **Values around 0** indicate that the level of potential undefended exposure and disadvantage is approximately average for England.
*   **Negative values** signify that fewer people are potentially exposed and disadvantaged compared to the national average.

To help categorize and map the relative severity of this disadvantage, the Z-scores are grouped into the dataset's standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight