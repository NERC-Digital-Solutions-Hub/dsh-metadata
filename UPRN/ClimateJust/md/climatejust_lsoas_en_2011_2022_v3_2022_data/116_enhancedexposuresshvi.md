### Enhanced Exposure Index

**Description:**
This field (identified internally as `EnhancedExposureSSFVI` for flood and `EnhancedExposureSSHVI` for heat in the spatial dataset) represents the standardized score (Z-score) for the **Enhanced Exposure** dimension of socio-spatial vulnerability within a given Lower Super Output Area (LSOA). Enhanced exposure refers to aspects of the physical built environment that tend to accentuate or offset the severity of extreme weather events, such as heatwaves or floods. 

**Vulnerability Context and Composition:**
This index recognizes that hazard exposure is not entirely independent of socially related drivers and local neighborhood design. The index is calculated as an equally weighted combination of neighbourhood-level scores from two primary domains:
1.  **Physical Environment:** Indicators include the proportion of built-up areas (areas that are not greenspace), a lack of domestic gardens, and a lack of access to public parks and playing fields. Areas with less greenspace and blue space (water bodies) have poorer drainage during floods and lack the cooling functions necessary during heatwaves.
2.  **Housing Characteristics:** Indicators relate to the types of buildings people live in. For heat vulnerability, this includes the proportion of residents living in high-rise flats (5th floor or above), which get disproportionately hot. For flood vulnerability, this includes dwellings with basement or ground-floor living spaces that are more easily inundated.

**Interpretation:**
Because the index is presented as a standardized Z-score, it evaluates how a specific neighbourhood compares to the overall average across England:
*   **Positive values (High scores):** Denote an environment that *accentuates* the hazard (e.g., highly built-up areas with little greenspace) compared to the English average, indicating greater vulnerability. Scores ≥ 2.5 are classified as "Acute", scores between 1.5 and 2.5 are "Extremely high", and scores between 0.5 and 1.5 are "Relatively high".
*   **Values around 0 (-0.5 to 0.5):** Denote that the area's enhanced exposure is approximately equal to the national "Average".
*   **Negative values (Low scores):** Denote environments that tend to *offset* the hazard (e.g., areas with abundant greenspace and gardens) compared to the English average, scaling down through "Relatively low", "Extremely low", and "Slight" (≤ -2.5).