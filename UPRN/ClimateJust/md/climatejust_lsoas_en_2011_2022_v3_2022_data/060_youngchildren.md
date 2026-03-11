### Young children (% people under 5 years)

**Description:**
This field (identified as `YoungChildren` in the spatial dataset) represents the standardized Z-score for the percentage of the population aged under 5 years within a given Lower Super Output Area (LSOA). It measures how the local concentration of young children in a specific neighbourhood compares to the national average across England. This metric is a core indicator within the "Age" domain, utilized to evaluate a community's biophysical "Sensitivity" to extreme climate events such as floods and heatwaves.

**Vulnerability Rationale:**
Higher proportions of young children in a neighbourhood indicate a higher level of social vulnerability. The primary reasons driving this vulnerability include:
*   **Physical Susceptibility:** Young children are physically more susceptible to the direct health impacts of high temperatures and floodwaters.
*   **Lack of Autonomy:** Children are dependent on parents and carers because they are generally unable to adapt their own behaviour and may not recognise the dangers associated with extreme weather events.
*   **Psychological and Social Impacts:** Evidence highlights a strong association between flooding and increased mental health and behavioural problems in children, driven by the trauma of the event and the subsequent disruption to their schooling and home-life.

**Interpretation:**
Because this metric is standardized as a Z-score, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher proportion of young children than the national average, indicating a higher level of age-related sensitivity and relative vulnerability.
*   **Values around 0** indicate that the proportion is approximately average for England.
*   **Negative values** signify a lower proportion of young children than the national average, indicating lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the updated 2022 England LSOA dataset, the underlying data for this indicator is derived from the Office for National Statistics (ONS) Mid-2019 Population Estimates for Lower Layer Super Output Areas (Table SAPE22DT2). It carries a weight of 0.500 within the broader "Age" domain, sharing this dimension equally with the indicator for older people (over 75 years).