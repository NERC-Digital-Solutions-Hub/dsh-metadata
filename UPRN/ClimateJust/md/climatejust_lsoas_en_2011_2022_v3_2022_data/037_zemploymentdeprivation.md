### Employment deprived people in an area (Z-Score)

**Description:**
This field (identified as `ZEmploymentDeprivation` in the spatial dataset) represents the standardized Z-score for the proportion of the working-age population experiencing employment deprivation within a given Lower Super Output Area (LSOA). It measures how the local level of employment deprivation in a specific neighbourhood compares to the national average across England.

**Vulnerability Rationale:**
Unemployment and employment deprivation are strongly recognized proxy indicators of financial deprivation and are commonly used as measures of vulnerability. This metric is a core indicator within the "Income" domain, which is utilized across multiple dimensions of the socio-spatial climate vulnerability index, including a community's "(In)ability to Prepare," "(In)ability to Respond," and "(In)ability to Recover" from extreme climate events like floods and heatwaves. 

A lack of financial resources significantly restricts a community's capacity to adapt to extreme weather. People who are employment-deprived are generally less able to afford the necessary resources to effectively prepare for, safely respond to, and fully recover from environmental hazard events.

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
For the 2022 England LSOA dataset, the underlying data for this indicator is derived from the 2019 English Indices of Deprivation (IMD), specifically utilizing the "Employment Deprivation Domain". The data, originally sourced from the Department for Work and Pensions, measures the number of employment-deprived people in an area, which is then converted into a percentage of the working population. The indicator carries a weight of 0.333 within the broader "Income" domain.