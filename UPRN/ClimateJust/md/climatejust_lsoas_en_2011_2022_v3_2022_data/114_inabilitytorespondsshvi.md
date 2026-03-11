### Inability to Respond Index

**Description:**
This field (identified internally as `InabilityToRespondSSFVI` for flood and `InabilityToRespondSSHVI` for heat in the spatial dataset) represents the standardized score (Z-score) for the **(In)ability to Respond** dimension of socio-spatial vulnerability within a given Lower Super Output Area (LSOA). It measures the personal, environmental, and social factors that govern a community's capacity to take immediate, effective action to avoid harm during an extreme weather event, such as a flood or a heatwave.

**Vulnerability Context and Composition:**
A community's ability to respond to a crisis is hindered by various social barriers. The index is calculated as an equally weighted combination of neighbourhood-level scores from several key vulnerability domains:
*   **Income:** Areas with higher employment and income deprivation.
*   **Language:** Communities with lower levels of proficiency in English, which can limit the ability to understand emergency warnings.
*   **Internet:** Lack of superfast broadband or sub-standard internet access, which can hinder access to real-time information.
*   **Local Knowledge:** High population transience or lack of coverage by flood warning systems.
*   **Social Networks:** High proportions of single-pensioner households or families lacking school-related networks, leading to potential isolation.
*   **Mobility:** High rates of disability, medical and care residents, and lack of private transport, which restrict physical movement during an evacuation.
*   **Crime:** High crime rates, which may make people reluctant to leave their homes or open windows during a heatwave.
*   **General Infrastructure *(Heat only)*:** Lower densities of retail units and a lack of local greenspace or domestic gardens, which limits access to informal refuges and cooling spaces.

**Interpretation:**
Because the index is presented as a standardized Z-score, it evaluates how a specific neighbourhood compares to the overall average across England:
*   **Positive values (High scores):** Denote a *higher inability* to respond to events compared to the English average, indicating greater social vulnerability. Scores ≥ 2.5 are classified as "Acute", scores between 1.5 and 2.5 are "Extremely high", and scores between 0.5 and 1.5 are "Relatively high".
*   **Values around 0 (-0.5 to 0.5):** Denote that the area's ability to respond is approximately equal to the national average.
*   **Negative values (Low scores):** Denote a *lower inability* (i.e., a better capacity) to respond compared to the English average, scaling down through "Relatively low" (-0.5 to -1.5), "Extremely low" (-1.5 to -2.5), and "Slight" (≤ -2.5).