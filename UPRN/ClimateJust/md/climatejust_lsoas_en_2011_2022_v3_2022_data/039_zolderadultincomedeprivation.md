### Income deprived older people in an area (Z-Score)

**Description:**
This field (identified as `ZOlderAdultIncomeDeprivation` in the spatial dataset) represents the standardized Z-score for the proportion of the older population (aged 60 or over) experiencing income deprivation within a given Lower Super Output Area (LSOA). It measures how the local level of income deprivation affecting older adults in a specific neighbourhood compares to the national average across England.

**Vulnerability Rationale:**
This metric is a core indicator within the "Income" domain, which is utilized to calculate a community's "(In)ability to Prepare," "(In)ability to Respond," and "(In)ability to Recover" from extreme climate events like floods and heatwaves. 

Older adults facing income deprivation represent a highly vulnerable group because they combine the biophysical sensitivities of older age with the reduced adaptive capacity of financial poverty. A lack of financial resources significantly restricts a person's ability to:
*   Afford preparatory measures, such as comprehensive home insurance or structural modifications to their homes (e.g., flood protections or cooling adaptations). 
*   Evacuate safely or use private transport during an emergency response.
*   Afford the repair or replacement of goods damaged by floodwaters or extreme weather in the recovery phase.

**Interpretation:**
Because this metric is standardized as a Z-score, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher rate of income-deprived older people than the national average, indicating a higher level of social vulnerability.
*   **Values around 0** indicate that the rate is approximately average for England.
*   **Negative values** signify a lower rate than the national average, indicating lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the 2022 England LSOA dataset, the underlying data for this indicator is derived from the 2019 English Indices of Deprivation (IMD), specifically utilizing the "Income Deprivation Affecting Older People" sub-domain. The data measures the number of income-deprived older people in an area, which is then converted into a percentage of the population aged 60 or over. The data originates from the Department for Work and Pensions and carries a weight of 0.333 within the broader "Income" domain.