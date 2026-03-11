### Rate of emergency admission to hospital (Z-Score)

**Description:**
This field (identified internally as `EmergencyHospitalAdmiss` in the spatial dataset) represents the standardized Z-score for the rate of emergency admissions to the hospital within a given Lower Super Output Area (LSOA). It measures how the local rate of acute morbidity and emergency healthcare reliance compares to the national average. This metric is a core indicator within the "Health" domain, which is utilized to evaluate a community's biophysical "Sensitivity" to extreme climate events such as floods and heatwaves.

**Vulnerability Rationale:**
Higher rates of emergency hospital admissions act as a proxy for poorer general health and high acute morbidity within a population. Higher proportions of people in poor health in an area indicate a higher level of social vulnerability. Individuals with underlying health conditions are physically more susceptible to the direct impacts of extreme temperatures and flood events. Experiencing an extreme weather event can make pre-existing medical conditions significantly worse, either acting as a sudden one-off "hit" to a person's system or by accelerating an adverse health trajectory. 

**Interpretation:**
Standardizing this metric as a Z-score allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher rate of emergency hospital admissions than the national average, indicating poorer health and higher relative vulnerability.
*   **Values around 0** indicate that the admission rate is approximately average for England.
*   **Negative values** signify a lower emergency admission rate than the national average, indicating better overall health and lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the 2022 England LSOA dataset, the underlying data for this indicator is derived from the English Indices of Deprivation 2019 (IMD 2019), specifically utilizing the "Acute Morbidity" indicator from the Health Deprivation and Disability Domain (sourced from the Health and Social Care Information Centre). It carries a weight of 0.143 within the broader "Health" domain, sharing this dimension with other health indicators such as comparative illness, mood and anxiety disorders, and years of potential life lost.