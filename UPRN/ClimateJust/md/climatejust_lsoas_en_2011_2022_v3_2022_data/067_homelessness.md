### Homelessness rate (rate per 1000 households)

**Description:**
This field (identified internally as `Homelessness` in the spatial dataset) represents the rate of homelessness (per 1,000 households) within a given Lower Super Output Area (LSOA). It provides a measure of the local prevalence of homelessness and precarious housing situations in a specific neighbourhood.

**Vulnerability Rationale:**
This metric is a versatile indicator utilized across multiple vulnerability dimensions, specifically evaluating a community's biophysical "Sensitivity" (within the Health domain) and its "Enhanced Exposure" (within the Housing Characteristics domain) to extreme climate events such as floods and heatwaves. 

Higher rates of homelessness indicate a higher level of social vulnerability. The primary reasons driving this vulnerability include:
*   **Health and Sensitivity:** Homelessness is strongly associated with severe health inequalities, acute morbidity, and lower life expectancy. Individuals experiencing homelessness are physically far more susceptible to the direct adverse health impacts of extreme high temperatures and flooding.
*   **Enhanced Exposure (Housing):** Individuals experiencing homelessness, or those living in temporary and precarious accommodation, lack the structural protection of a secure home. This lack of adequate shelter significantly heightens their direct physical exposure to extreme heat and dangerous floodwaters, limiting their ability to shelter safely during a crisis.

**Interpretation:**
Unlike many other indicators in the dataset that are pre-standardized as Z-scores in their field names, this raw field is presented as a direct rate. When used to calculate the final vulnerability indices, it is standardized to allow for relative comparisons:
*   **Higher values/rates** denote a higher prevalence of homelessness, indicating a higher level of health and housing-related social vulnerability.
*   **Lower values/rates** signify a lower prevalence of homelessness, indicating lower relative vulnerability.

**Data Source:**
For the 2022 England LSOA dataset, the underlying data for this indicator is derived from the English Indices of Deprivation 2019 (IMD 2019), specifically utilizing the Homelessness indicator from the Wider Barriers sub-domain. It is applied with varying weights depending on the specific vulnerability index being calculated:
*   **Sensitivity Index:** It carries a weight of 0.143 within the broader "Health" domain alongside indicators like emergency hospital admissions and premature death.
*   **Flood Enhanced Exposure Index:** It carries a weight of 0.500 within the "Housing Characteristics" domain, sharing this dimension equally with the indicator for caravans and temporary structures.
*   **Heat Enhanced Exposure Index:** It carries a weight of 0.333 within the "Housing Characteristics" domain, sharing this dimension with household overcrowding and high-rise homes.