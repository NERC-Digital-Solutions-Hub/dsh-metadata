### Older people (% people over 75 years)

**Description:**
This field (identified as `PeopleOver75` or `S_3` in the spatial dataset) represents the standardized Z-score for the percentage of the population aged over 75 years within a given Lower Super Output Area (LSOA),. It measures how the local concentration of older residents in a specific neighbourhood compares to the national average. This metric is a core indicator within the "Age" domain, utilized to evaluate a community's biophysical "Sensitivity" to extreme climate events such as floods and heatwaves,,.

**Vulnerability Rationale:**
Higher proportions of people over 75 in a neighbourhood indicate a higher level of social vulnerability,. The primary reasons driving this vulnerability include:
*   **Physical Susceptibility:** Older people are more physically susceptible to the direct health and welfare impacts of both high temperatures and flood events,,. Historical extreme weather events, such as the 1953 floods and the 2003 heatwaves, have demonstrated that excess deaths are highest among the elderly,,.
*   **Mobility Limitations:** Older individuals often have more limited physical mobility, which makes it difficult for them to implement property-level flood defence measures (such as putting up heavy flood gates),.
*   **Warning Response:** Evidence suggests that older people are less likely than other social groups to respond to emergency flood warnings and may be more reluctant to evacuate or leave their homes during a crisis,.

**Interpretation:**
Because this metric is standardized as a Z-score, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher proportion of older people than the national average, indicating a higher level of age-related sensitivity and relative vulnerability.
*   **Values around 0** indicate that the proportion is approximately average for England.
*   **Negative values** signify a lower proportion of older people than the national average, indicating lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the updated 2022 England LSOA dataset, the underlying data for this indicator is derived from the Office for National Statistics (ONS) Mid-2019 Population Estimates for Lower Layer Super Output Areas (Table SAPE22DT2),. It carries a weight of 0.500 within the broader "Age" domain, sharing this dimension equally with the indicator for young children (under 5 years),.