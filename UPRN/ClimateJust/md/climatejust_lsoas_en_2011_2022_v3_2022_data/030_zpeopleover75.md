### Older people (Z-Score)

**Description:**
This field represents the standardized Z-score for the proportion of the population aged 75 years and over within a given Lower Super Output Area (LSOA). It measures how the local concentration of older residents in a specific neighbourhood compares to the national average. 

**Vulnerability Rationale:**
This metric is a key indicator within the "Sensitivity" dimension of the socio-spatial climate vulnerability index. A higher proportion of older people (over 75) in an area indicates a higher level of underlying biophysical vulnerability. Older people are highly physically susceptible to the health and welfare impacts of extreme weather events, such as heat stress and flooding. Additionally, older people are generally less likely to respond to flood warnings, may be more reluctant to evacuate their homes, and often have more limited physical mobility, making it difficult to use property-level flood defence measures.

**Interpretation:**
Because this is a standardized Z-score, it allows for direct relative comparison across different neighbourhoods:
*   **Positive values** denote a higher proportion of older people than the national average, indicating higher vulnerability.
*   **Values around 0** indicate that the proportion of older people is approximately average for England.
*   **Negative values** signify a lower proportion of older people than the national average, indicating lower relative vulnerability.

To map and categorize the relative concentration of this sensitive demographic, the Z-scores are grouped into the dataset's standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the updated 2022 England LSOA dataset, the underlying population data used to calculate this score is derived from the Office for National Statistics (ONS) Mid-2019 Population Estimates for Lower Layer Super Output Areas by Single Year of Age and Sex (table SAPE22DT2).