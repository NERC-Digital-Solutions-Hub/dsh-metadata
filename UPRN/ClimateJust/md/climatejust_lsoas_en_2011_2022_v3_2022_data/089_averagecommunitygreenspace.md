### Median combined size of parks and public gardens and playing fields within 1,000 m radius (m²)

**Description:**
This field (identified internally as `AverageCommunityGreenspace` for the raw measurement in square metres, and frequently standardized as a Z-score under `ZAverageCommunityGreenspace` in the spatial dataset) represents the median combined area of parks, public gardens, and playing fields accessible within a 1,000-metre radius of a given Lower Super Output Area (LSOA). It serves to measure the availability of local, public green infrastructure for a community.

**Vulnerability Rationale:**
This metric is a core indicator within the "Physical Environment" domain, which is utilized to evaluate a community's "Enhanced Exposure" to extreme climate events, such as floods and heatwaves. 

The physical characteristics of a neighbourhood can significantly accentuate or mitigate the severity of weather hazards. A higher availability of community greenspace provides a protective function, thereby reducing environmental vulnerability:
*   **Flooding:** Greenspace provides a vital natural drainage function. More greenspace results in higher water infiltration, which helps mitigate the severity of surface water flooding during periods of heavy rainfall.
*   **Heatwaves:** Parks and public gardens provide natural cooling functions that help counteract the urban heat island effect, lowering local temperatures and offering cooler refuge areas for residents during extreme heat.

**Interpretation:**
Because having access to more greenspace reduces vulnerability, the data for this indicator is **reversed** when calculating the final vulnerability indices so that it aligns with the standard dataset format where higher scores must equal higher vulnerability:
*   **Higher raw values (m²):** Denote larger areas of accessible public greenspace, indicating better natural cooling and drainage capacity, and therefore **lower** relative vulnerability.
*   **Higher standardized scores (Reversed Z-scores):** Denote a *lack* of accessible greenspace compared to the national average, indicating higher enhanced exposure and a **higher** level of overall social vulnerability.

**Data Source:**
For the 2022 England LSOA dataset, the underlying data for this indicator is derived from the Office for National Statistics (ONS) Greenspace dataset. It carries a weight of 0.330 within the broader "Physical Environment" domain, sharing this dimension equally with other environmental indicators, including the proportion of densely built-up areas and the lack of private domestic gardens.