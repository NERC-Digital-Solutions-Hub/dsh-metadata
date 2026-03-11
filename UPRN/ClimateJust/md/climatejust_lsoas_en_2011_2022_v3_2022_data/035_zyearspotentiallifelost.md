### Years of Potential Life Lost (Z-Score)

**Description:**
This field (referred to as `ZYearsPotentialLifeLost` in the spatial dataset) represents the standardized Z-score for the "Years of Potential Life Lost" indicator within a given Lower Super Output Area (LSOA). It measures the relative rate of premature death in a specific neighbourhood compared to the national average across England.

**Vulnerability Rationale:**
This metric is one of the supporting indicators used within the "Health" domain to calculate a community's overall biophysical "Sensitivity" to climate hazards, such as floods and heatwaves. A higher rate of years of potential life lost indicates a population with poorer underlying health. Individuals in poor health are inherently more physically susceptible to the negative health and welfare impacts of extreme weather.

**Interpretation:**
Because this metric is standardized as a Z-score, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher rate of years of potential life lost than the national average, indicating higher relative vulnerability.
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
For the updated 2022 England LSOA dataset, the underlying data for this indicator is derived from the 2019 English Indices of Deprivation (IMD). Specifically, it utilizes the "Years of Potential Life Lost" indicator from the Health Deprivation and Disability Domain, which is originally sourced from the Office for National Statistics. It carries an equal weighting of 0.143 within the broader Health domain alongside other health indicators.