### Availability of superfast broadband (% Premises)

**Description:**
This field (identified internally as `LackSuperfastBroadband` in the spatial dataset) represents the percentage of premises within a given Lower Super Output Area (LSOA) that have access to superfast broadband (SFBB). It serves as a metric to evaluate local internet accessibility and the digital divide.

**Vulnerability Rationale:**
This metric is a core indicator within the "Internet" domain, which is utilized across multiple dimensions to evaluate a community's "(In)ability to Prepare", "(In)ability to Respond", and "(In)ability to Recover" from extreme climate events, such as floods and heatwaves. 

A lack of reliable internet access increases social vulnerability. During an extreme weather event, individuals without adequate internet access face significant disadvantages, including:
*   **Preparation and Response:** Difficulty accessing online flood alerts, heatwave health warnings, and local emergency guidance.
*   **Recovery:** Barriers to navigating online recovery services, applying for financial assistance, or submitting insurance claims in the aftermath of a disaster.

**Interpretation:**
The raw data represents the *availability* of superfast broadband. However, to properly calculate vulnerability (where higher values must equate to higher vulnerability), this indicator is frequently **reversed** (subtracted from 100) to represent a *lack* of availability.
*   **Higher raw percentages (Availability):** Denote better internet coverage, indicating greater capacity to access information and lower relative vulnerability.
*   **Higher reversed/standardized scores (Lack of Availability):** Often represented as a Z-score (`ZLackSuperfastBroadband`), this indicates poor internet infrastructure and a higher level of digital and social vulnerability.

**Data Source & Important Caveats:**
For the 2022 England LSOA dataset, the underlying data is derived from Ofcom (January 2018). It carries a weight of 0.500 within the broader "Internet" domain, sharing this dimension equally with an indicator for sub-standard broadband (premises falling below the Universal Service Obligation). 

**Note:** The dataset documentation explicitly advises caution when using this indicator, as it **does not take into account the availability of ultrafast broadband**. Users are recommended to refer to the latest data from Ofcom for the most current picture of local internet infrastructure.