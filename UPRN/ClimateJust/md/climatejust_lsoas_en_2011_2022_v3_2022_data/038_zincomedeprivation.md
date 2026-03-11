### Income deprived people in an area (Z-Score)

**Description:**
This field (identified as `ZIncomeDeprivation` in the spatial dataset) represents the standardized Z-score for the proportion of the population experiencing income deprivation within a given Lower Super Output Area (LSOA). It measures how the local level of income deprivation in a specific neighbourhood compares to the national average across England.

**Vulnerability Rationale:**
This metric is a core indicator within the "Income" domain, which is utilized to calculate a community's "(In)ability to Prepare," "(In)ability to Respond," and "(In)ability to Recover" from extreme climate events like floods and heatwaves. 

Higher proportions of people on low incomes indicate a higher level of social vulnerability. Specifically, financial deprivation restricts a community's adaptive capacity in several ways:
*   Low-income households lack the financial capacity to effectively prepare for extreme events, such as purchasing comprehensive home insurance or installing property-level flood protection measures.
*   Low-income households are less likely to own their own homes. This lack of ownership, combined with limited funds, restricts their ability and autonomy to make physical modifications to their properties to prepare for hot weather or flooding.

**Interpretation:**
Because this metric is standardized as a Z-score, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher rate of income deprivation than the national average, indicating a higher level of social vulnerability.
*   **Values around 0** indicate that the income deprivation rate is approximately average for England.
*   **Negative values** signify a lower rate of income deprivation than the national average, indicating lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the 2022 England LSOA dataset, the underlying data for this indicator is derived from the 2019 English Indices of Deprivation (IMD), specifically utilizing the "Income Deprivation Domain". The data measures the number of income-deprived people in an area, which is then converted into a percentage of the total zone population. The data originates from the Department for Work and Pensions, Her Majesty's Revenue and Customs, and the Home Office. It carries a weight of 0.333 within the broader "Income" domain.