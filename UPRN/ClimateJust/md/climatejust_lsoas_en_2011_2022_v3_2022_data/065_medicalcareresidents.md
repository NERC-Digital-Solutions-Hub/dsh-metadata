### Medical and Care Residents (Score)

**Description:**
This field (identified as `MedicalCareResidents` in the spatial dataset) represents the standardized score (Z-score) for the percentage of people living in medical and care establishments within a given Lower Super Output Area (LSOA). It measures how the local concentration of individuals residing in serviced care accommodation in a specific neighbourhood compares to the national average across England.

**Vulnerability Rationale:**
This metric is a versatile indicator used across multiple vulnerability dimensions, specifically within the "Sensitivity" (Health domain) and the "(In)ability to Respond" and "(In)ability to Recover" dimensions (Mobility domain) for both heat and flood events. 

Higher proportions of people living in medical and care establishments indicate a higher level of social vulnerability. The rationale for this includes:
*   **Physical Susceptibility:** Individuals in care environments typically have pre-existing health conditions and already require additional daily support, making them more physically sensitive to the direct impacts of extreme temperatures and flooding.
*   **Low Personal Mobility:** Residents in these establishments generally have limited personal, physical mobility, making them less capable of independently responding to a crisis or moving out of an affected area during an emergency.
*   **Reliance on Carers and Equipment:** People with reduced mobility are highly reliant on others to assist them during an evacuation. Disruptions caused by extreme weather (such as flooded roads or power outages) can prevent carers from reaching the facility and can leave essential assistance tools, such as electronic lifts, completely unusable.

**Interpretation:**
Because this metric is standardized as a Z-score, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher proportion of medical and care residents than the national average, indicating a higher level of mobility and health-related social vulnerability.
*   **Values around 0** indicate that the proportion is approximately average for England.
*   **Negative values** signify a lower proportion than the national average, indicating lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the updated 2022 England LSOA dataset, no direct recent update was available, so the underlying data relies on the 2011 UK Census (specifically table QS421SC: number of people in 'Medical and care establishments' divided by the total population) as compiled by Sayers et al. (2017). This indicator carries a weight of 0.143 within the "Health" domain (Sensitivity index) and a weight of 0.200 within the "Mobility" domain (Respond and Recover indices).