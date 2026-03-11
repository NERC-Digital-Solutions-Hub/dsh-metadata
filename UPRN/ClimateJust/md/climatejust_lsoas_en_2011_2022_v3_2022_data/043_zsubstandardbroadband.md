### Sub-standard Broadband (Z-Score)

**Description:**
This field (identified as `ZSubStandardBroadband` in the spatial dataset) represents the standardized Z-score for the percentage of premises that fall below the Universal Service Obligation (USO) for broadband access within a given Lower Super Output Area (LSOA). It measures how the local concentration of poor internet connectivity in a specific neighbourhood compares to the national average across England. 

**Vulnerability Rationale:**
This metric is a core indicator within the "Internet" domain, which is utilized to evaluate a community's "(In)ability to Prepare," "(In)ability to Respond," and "(In)ability to Recover" from extreme climate events, such as floods and heatwaves. 

Higher proportions of premises with sub-standard internet access indicate a higher level of social vulnerability. Poor digital connectivity can restrict a community's capacity to access vital online information, receive early flood or heatwave warnings, and navigate digital services required for recovery assistance.

**Interpretation:**
Because this metric is standardized as a Z-score, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher percentage of premises with sub-standard broadband than the national average, indicating a higher level of social vulnerability.
*   **Values around 0** indicate that the percentage is approximately average for England.
*   **Negative values** signify a lower percentage than the national average, indicating lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the 2022 England LSOA dataset, the underlying data for this indicator is derived from Ofcom (2018) data, which measures the percentage of premises below the Universal Service Obligation (USO). It carries a weight of 0.500 within the broader "Internet" domain, sharing this domain equally with the indicator for the lack of superfast broadband.