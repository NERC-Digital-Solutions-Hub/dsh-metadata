### Mean distance to a pharmacy (km)

**Description:**
This field (identified internally as `AccessibilityPharmacies` or standardized as a Z-score under `ZAccessibilityPharmacies` in the spatial dataset) represents the average distance in kilometers that residents in a given Lower Super Output Area (LSOA) must travel to reach the nearest pharmacy. It serves as a primary metric to evaluate a local community's geographic access to essential health and medical supplies.

**Vulnerability Rationale:**
This metric is the sole indicator within the "Pharmacy Access" domain, which is utilized to evaluate a community's "(In)ability to Prepare", "(In)ability to Respond", and "(In)ability to Recover" from extreme climate events, including both floods and heatwaves. 

Greater distances to a pharmacy indicate a higher level of social vulnerability. The rationale driving this includes:
*   **Access to Medicine:** During extreme weather events like floods or heatwaves, individuals may urgently need to access prescriptions or medical advice. Communities located far from pharmacies face a significant disadvantage if travel is disrupted by floodwaters, severe heat, or suspended public transport services.
*   **Preparation and Recovery:** Being far from a pharmacy limits a household's ability to easily stock up on necessary supplies (like first aid or specific medications) before an event strikes, and slows down their recovery if they need medical support in the immediate aftermath.

**Interpretation:**
When used to calculate the final composite vulnerability indices, this raw distance is standardized (as a Z-score) to allow for direct relative comparisons across different geographic areas:
*   **Higher values (greater distances in km or positive Z-scores):** Denote poorer accessibility to pharmacies, indicating greater difficulty in accessing medical supplies and a **higher** level of social vulnerability.
*   **Lower values (shorter distances in km or negative Z-scores):** Signify that pharmacies are highly accessible, indicating better community service access and **lower** relative vulnerability.

**Data Source:**
For the 2022 England LSOA dataset, the underlying data for this indicator is derived from the Consumer Data Research Centre (CDRC) Data 2021, specifically utilizing the Access to Healthy Assets and Hazards (AHAH2) dataset (using the `pharm_dist` variable). As the sole indicator for the "Pharmacy Access" domain, it carries a full weight of 1.000 within that domain across the various preparation, response, and recovery indices.