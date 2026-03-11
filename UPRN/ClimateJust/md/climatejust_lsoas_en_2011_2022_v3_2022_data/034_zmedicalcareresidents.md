### Employment deprived people in an area (Z-Score)

**Description:**
This field (referred to as `ZEmploymentDeprivation` in the spatial dataset) represents the standardized Z-score for the proportion of the working-age population that is employment deprived within a given Lower Super Output Area (LSOA). It measures how the local level of employment deprivation in a specific neighbourhood compares to the national average across England.

**Vulnerability Rationale:**
This metric is a core indicator within the "Income" domain, which is utilized across multiple dimensions of the socio-spatial climate vulnerability index, including a community's "(In)ability to Prepare," "(In)ability to Respond," and "(In)ability to Recover" from extreme climate events like floods and heatwaves. 

Unemployment and employment deprivation are strongly recognized indicators of financial deprivation and serve as a proxy for low incomes. Adaptation and resilience are heavily influenced by financial resources; people who are employment deprived are significantly more vulnerable because a lack of income restricts their ability to afford preventative measures (such as insurance or property-level protections), to evacuate or quickly replace lost goods during a crisis, and to effectively recover in the long term.

**Interpretation:**
Because this metric is standardized as a Z-score, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher rate of employment deprivation than the national average, indicating a higher level of social vulnerability.
*   **Values around 0** indicate that the employment deprivation rate is approximately average for England.
*   **Negative values** signify a lower rate of employment deprivation than the national average, indicating lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the updated 2022 England LSOA dataset, the underlying data for this indicator is derived from the 2019 English Indices of Deprivation (IMD), specifically utilizing the "Employment Deprivation Domain". The data measures the number of employment-deprived people in an area, which is then converted into a percentage of the working population. The indicator carries a weight of 0.333 within the broader "Income" domain.