### Years of Potential Life Lost (Score)

**Description:**
This field (identified internally as `YearsOfPotentialLifeLost` in the spatial dataset) represents the standardized score for the rate of premature mortality within a given Lower Super Output Area (LSOA). It measures how the local rate of years of potential life lost in a specific neighbourhood compares to the national average.

**Vulnerability Rationale:**
This metric is a core indicator within the "Health" domain, which is utilized to evaluate a community's biophysical "Sensitivity" to extreme climate events, such as floods and heatwaves. 

Higher rates of potential life lost act as a proxy for poorer general health and higher health deprivation within a population. Higher proportions of people in poor health in an area indicate a higher level of social vulnerability. Individuals with underlying health issues are physically more susceptible to the direct impacts of extreme temperatures and flood events.

**Interpretation:**
Because this metric is standardized as a score, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher rate of years of potential life lost than the national average, indicating poorer health and higher relative vulnerability.
*   **Values around 0** indicate that the rate is approximately average for England.
*   **Negative values** signify a lower rate than the national average, indicating better overall health and lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the 2022 England LSOA dataset, the underlying data for this indicator is derived from the English Indices of Deprivation 2019 (IMD 2019). Specifically, it utilizes the "Years of Potential Life Lost" indicator from the IMD Health Deprivation and Disability Domain, which is sourced via the Office for National Statistics. It carries a weight of 0.143 within the broader "Health" domain for the Sensitivity index, sharing this dimension with other health indicators such as the comparative illness and disability ratio, emergency hospital admissions, and the mood and anxiety disorder indicator.