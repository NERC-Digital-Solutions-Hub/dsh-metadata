### Comparative illness and disability ratio (Z-Score)

**Description:**
This field (identified as `ZDisabilityIllHealth` in the spatial dataset) represents the standardized Z-score for the comparative illness and disability ratio within a given Lower Super Output Area (LSOA). It measures how the local concentration of people experiencing long-term illness or disability in a specific neighbourhood compares to the national average across England. 

**Vulnerability Rationale:**
This metric serves as a core indicator primarily within the "Health" domain, which is utilized to evaluate a community's biophysical "Sensitivity" to extreme climate events such as floods and heatwaves. 

Higher proportions of people with illness and disability in an area indicate a higher level of social vulnerability. The primary reasons driving this vulnerability include:
*   **Physical Susceptibility:** Individuals with pre-existing medical conditions are physically more susceptible to the direct impacts of extreme temperatures and flood events. The trauma and disruption of a flood or heatwave can make long-term illnesses significantly worse, either acting as a sudden one-off "hit" to a person's system or by accelerating an adverse health trajectory.
*   **Mobility Challenges:** High levels of disability and illness act as a proxy for limited personal physical mobility. Reduced mobility creates severe practical challenges when individuals need to deploy physical property-level protections (like flood gates) or evacuate safely during an emergency.
*   **Medical Dependency:** Extreme events frequently cause power outages and transport disruptions, which can cut off access to vital medications, prevent carers from reaching their patients, and disrupt the use of complex home-based healthcare systems (such as home dialysis).

**Interpretation:**
Because this metric is standardized as a Z-score, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher ratio of illness and disability than the national average, indicating poorer overall health, lower physical mobility, and a higher level of relative vulnerability.
*   **Values around 0** indicate that the illness and disability ratio is approximately average for England.
*   **Negative values** signify a lower ratio than the national average, indicating better overall health and lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the 2022 England LSOA dataset, the underlying data for this indicator is derived from the English Indices of Deprivation 2019 (IMD 2019). Specifically, it utilizes the "Comparative Illness and Disability Ratio" sub-indicator from the IMD Health Deprivation and Disability Domain, which is sourced via the Department for Work and Pensions. It carries a weight of 0.143 within the broader "Health" domain for the Sensitivity index, sharing this dimension with indicators like emergency hospital admissions and the mood and anxiety disorder indicator.