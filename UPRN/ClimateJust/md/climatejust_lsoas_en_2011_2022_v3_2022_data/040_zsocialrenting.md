### Social renters (Z-Score)

**Description:**
This field (identified as `ZSocialRenting` in the spatial dataset) represents the standardized Z-score for the percentage of households that are social renters (renting from social or council landlords) within a given Lower Super Output Area (LSOA). It measures how the local concentration of social housing tenants in a specific neighbourhood compares to the national average across England.

**Vulnerability Rationale:**
This metric is a key indicator within the "Tenure" domain, which is utilized to assess a community's "(In)ability to Prepare" for extreme climate events, such as floods and heatwaves. 

Higher proportions of social renters in an area generally indicate a higher level of social vulnerability. Tenants are considered more vulnerable because they usually lack the autonomy, financial incentive, or capital to make physical modifications and structural adaptations to their homes (such as installing floodgates or heat-proofing) compared to owner-occupiers. 

*Caveat:* The methodology explicitly notes that while tenants are generally less prepared, social tenants may sometimes benefit from widespread adaptations and safety measures put in place by social landlords or local councils, which can offset some of this vulnerability.

**Interpretation:**
Because this metric is standardized as a Z-score, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher proportion of social renters than the national average, indicating a higher level of social vulnerability.
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
For the 2022 England LSOA dataset, no direct update was available for this specific metric, so the underlying data relies on the 2011 UK Census (households renting from the council or other social rented). The indicator carries a weight of 0.500 within the broader "Tenure" domain.