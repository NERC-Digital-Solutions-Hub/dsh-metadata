### Sub-standard Broadband (% premises below the Universal Service Obligation)

**Description:**
This field (identified internally as `SubStandardBroadband` or standardized as a Z-score under `Z_SubStandardBroadband` in the spatial dataset) represents the percentage of premises within a given Lower Super Output Area (LSOA) that receive broadband internet speeds falling below the Universal Service Obligation (USO). It provides a measure of the local lack of basic digital connectivity and infrastructure.

**Vulnerability Rationale:**
This metric is a core indicator within the "Internet" domain, which is utilized to evaluate a community's "(In)ability to Prepare", "(In)ability to Respond", and "(In)ability to Recover" from extreme climate events such as floods and heatwaves. 

A lack of adequate internet access significantly increases a community's social vulnerability. During extreme weather events, digital connectivity is crucial for:
*   **Information Access:** The internet is a primary mechanism for accessing vital information about flood risks, heatwave guidance, and long-term preparation strategies. 
*   **Early Warnings:** Sub-standard broadband limits a household's ability to receive timely, digital emergency alerts or to monitor rapidly changing weather situations.
*   **Recovery Support:** Following an event, people without reliable internet access may face significant hurdles in registering insurance claims, accessing government assistance, or reaching out to wider social networks for help. 

**Interpretation:**
When used to calculate the final vulnerability indices, this raw percentage is standardized (as a Z-score) to allow for direct relative comparisons across different geographic areas:
*   **Higher percentages (or positive Z-scores)** denote a higher concentration of premises with sub-standard broadband, indicating poorer digital connectivity and a higher level of social vulnerability.
*   **Lower percentages (or negative Z-scores)** signify better basic internet provision, indicating a greater community capacity to access information and lower relative vulnerability.

**Data Source:**
For the 2022 England LSOA dataset, the underlying data for this indicator is derived from Ofcom (2018). It carries a weight of 0.500 within the broader "Internet" domain, sharing this dimension equally with the indicator for the availability (or lack) of superfast broadband. Depending on the specific index being calculated, the "Internet" domain contributes varying overall weights (e.g., 0.200 for the Inability to Prepare index, and 0.143 or 0.125 for the Respond and Recover indices).