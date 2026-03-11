### Private renters (Z-Score)

**Description:**
This field (identified as `ZPrivateRenting` in the spatial dataset) represents the standardized Z-score for the percentage of households that rent from a private landlord or letting agency within a given Lower Super Output Area (LSOA). It measures how the local concentration of private housing tenants in a specific neighbourhood compares to the national average across England. This metric is a key indicator within the "Tenure" domain, utilized to assess a community's "(In)ability to Prepare" for extreme climate events like floods and heatwaves.

**Vulnerability Rationale:**
Higher proportions of private renters in an area indicate a higher level of social vulnerability. Private renters are considered more vulnerable because they typically have a lower ability and less autonomy to modify or adapt their homes compared to owner-occupiers. The primary reasons driving this vulnerability include:
*   **Property restrictions:** Tenants are often not allowed to make physical alterations or structural adaptations to their properties (such as installing floodgates or heat-proofing).
*   **Lack of incentive:** Even if permitted, tenants have little incentive to invest in property-level physical risk-reducing measures because tenancies are often short and offer limited security of tenure, meaning they may also be less aware of local flood risks.
*   **Financial capacity:** Private tenants are generally less well-off than homeowners, restricting their ability to afford preventative modifications. 

**Interpretation:**
Because this metric is standardized as a Z-score, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher proportion of private renters than the national average, indicating a higher level of social vulnerability.
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
For the 2022 England LSOA dataset, no direct update was available for this specific metric, so the underlying data relies on the 2011 UK Census (table KS402: representing the sum of households renting from a private landlord or letting agency, plus other private renters). The indicator carries a weight of 0.500 within the broader "Tenure" domain.