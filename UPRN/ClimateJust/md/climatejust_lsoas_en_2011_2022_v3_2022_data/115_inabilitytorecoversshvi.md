### Inability to Recover Index

**Description:**
This field (identified internally as `InabilityToRecoverSSFVI` for flood and `InabilitytoRecoverSSHVI` for heat in the spatial dataset) represents the standardized score (Z-score) for the **(In)ability to Recover** dimension of socio-spatial vulnerability within a given Lower Super Output Area (LSOA). It measures the personal, environmental, and social factors that govern a community's capacity to bounce back and return to normal life after the occurrence of a climate or extreme weather event, such as a flood or heatwave.

**Vulnerability Context and Composition:**
A community's ability to recover from a hazard is primarily influenced by social factors and the availability of local services. The index is calculated as an equally weighted combination of neighbourhood-level scores from several key vulnerability domains:
*   **Income:** Areas with higher employment and income deprivation, which restricts the financial ability to replace lost goods or find temporary accommodation.
*   **Language:** Lower levels of proficiency in English, which can hinder the ability to understand what post-event help is available and how to navigate recovery services.
*   **Internet:** Sub-standard broadband or a lack of superfast connections, limiting access to online recovery resources.
*   **Social Networks:** High proportions of single-pensioner households or families lacking school-related networks, meaning isolated individuals are less likely to obtain community assistance.
*   **Mobility:** High rates of disability, medical and care residents, and a lack of private transport.
*   **Service Access:** Relative lack of access to medical help, measured by travel times to pharmacies, GPs, and hospitals.
*   **House Prices *(Flood only)*:** Evaluated using median house prices, which act as a proxy for housing mobility and the ability to move away from an affected area.

**Interpretation:**
Because the index is presented as a standardized Z-score, it evaluates how a specific neighbourhood compares to the overall average across England:
*   **Positive values (High scores):** Denote a *higher inability* to recover from events compared to the English average, indicating greater social vulnerability. Scores ≥ 2.5 are classified as "Acute", scores between 1.5 and 2.5 are "Extremely high", and scores between 0.5 and 1.5 are "Relatively high".
*   **Values around 0 (-0.5 to 0.5):** Denote that the area's ability to recover is approximately equal to the national "Average".
*   **Negative values (Low scores):** Denote a *lower inability* (i.e., a stronger capacity) to recover compared to the English average, scaling down through "Relatively low" (-0.5 to -1.5), "Extremely low" (-1.5 to -2.5), and "Slight" (≤ -2.5).