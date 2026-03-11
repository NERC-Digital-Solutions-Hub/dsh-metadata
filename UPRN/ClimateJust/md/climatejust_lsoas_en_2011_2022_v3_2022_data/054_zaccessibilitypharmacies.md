### Mean distance to a pharmacy (Z-Score)

**Description:**
This field (identified as `ZAccessibilityPharmacies` in the spatial dataset) represents the standardized Z-score for the mean distance (in kilometres) to a pharmacy within a given Lower Super Output Area (LSOA). It measures how the local physical accessibility of pharmacies in a specific neighbourhood compares to the national average across England. 

**Vulnerability Rationale:**
This metric is the sole indicator within the "Pharmacy access" domain, which is utilized to evaluate a community's "(In)ability to Respond" and "(In)ability to Recover" from extreme climate events, such as floods and heatwaves. 

Higher distances to a pharmacy equate to higher social vulnerability. The rationale is that communities located further from pharmacies have poorer access to essential medical supplies and healthcare advice. During an extreme event (like a severe heatwave or flood), individuals may face significant practical or physical difficulties travelling long distances to replace lost or damaged medicines, or to seek treatment for emerging health impacts.

**Interpretation:**
Because this metric is standardized as a Z-score, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a greater mean distance to a pharmacy than the national average, indicating poorer access and a higher level of social vulnerability.
*   **Values around 0** indicate that the distance is approximately average for England.
*   **Negative values** signify shorter travel distances (better access) than the national average, indicating lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the updated 2022 England LSOA dataset, the underlying data for this indicator is derived from the Consumer Data Research Centre (CDRC) Data 2021. Specifically, it utilizes the `pharm_dist` (mean distance to a pharmacy) metric from the Access to Healthy Assets and Hazards (AHAH2) dataset. As the sole indicator for the Pharmacy Access domain, it carries a full weight of 1.000 within that domain.