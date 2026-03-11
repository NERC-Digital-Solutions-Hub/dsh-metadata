### Homelessness indicator (Z-Score)

**Description:**
This field (referred to as `ZHomelessness` in the spatial dataset) represents the standardized Z-score for the rate of homelessness within a given Lower Super Output Area (LSOA). It measures how the local rate of homelessness (calculated per 1,000 households) in a specific neighbourhood compares to the national average across England.

**Vulnerability Rationale:**
This metric is a highly versatile indicator used to evaluate a community's vulnerability across two distinct dimensions of the socio-spatial climate vulnerability index:

1.  **Sensitivity (Health Domain):** Homelessness is strongly correlated with severe pre-existing physical and mental health issues. A high rate of homelessness indicates a population with higher underlying biophysical susceptibility to the negative health impacts of extreme weather events, such as floods and heatwaves. Within the Health domain, this indicator carries a weight of 0.143.
2.  **Enhanced Exposure (Housing Characteristics Domain):** Homelessness and insecure housing directly accentuate an individual's physical exposure to climate hazards. Individuals lacking permanent, secure shelter have little to no structural protection against extreme temperatures or floodwaters. Within the Housing Characteristics domain, this indicator carries a higher weight of 0.500.

**Interpretation:**
Standardizing this metric as a Z-score allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher rate of homelessness than the national average, indicating a higher level of social vulnerability.
*   **Values around 0** indicate that the homelessness rate is approximately average for England.
*   **Negative values** signify a lower rate of homelessness than the national average, indicating lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the updated 2022 England LSOA dataset, the underlying data for this indicator is derived from the 2019 English Indices of Deprivation (IMD). Specifically, it utilizes the homelessness rate (per 1000 households) indicator, which forms part of the wider IMD Barriers to Housing and Services Domain.