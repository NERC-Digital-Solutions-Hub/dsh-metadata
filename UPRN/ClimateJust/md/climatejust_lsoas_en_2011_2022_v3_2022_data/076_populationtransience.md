### Population Transience (Residential Mobility Index)

**Description:**
This field (identified as `PopulationTransience` and standardized as a Z-score under `Z_PopulationTransience` in the spatial dataset) represents the level of population turnover within a given Lower Super Output Area (LSOA). It acts as a residential mobility index to measure the rate at which people move in and out of a local neighbourhood.

**Vulnerability Rationale:**
This metric is a core indicator within the "Local knowledge" domain, which is utilized to evaluate a community's "(In)ability to Prepare" and "(In)ability to Respond" to extreme climate events such as floods and heatwaves. 

Higher proportions of people moving into and out of an area indicate a higher level of social vulnerability. The primary rationale driving this includes:
*   **Lack of Awareness:** Communities where population turnover is high are generally less aware of the likelihood of being affected by extreme weather events, such as local flooding. 
*   **Loss of Community Clues:** People who have recently moved into an area often lack the vital awareness of local risks that is typically passed down and shared through established family and community networks.
*   **Response and Support:** Highly transient populations are less likely to know how to practically respond during an emergency or where to seek institutional and community support in the immediate aftermath.

**Interpretation:**
When used to calculate the final vulnerability indices, this raw index is standardized as a Z-score to allow for direct relative comparisons across different geographic areas:
*   **Positive values/Higher scores** denote a highly transient population with greater residential mobility than the average, indicating poorer local knowledge and a higher level of social vulnerability.
*   **Values around 0** indicate that the population turnover is approximately average.
*   **Negative values/Lower scores** signify a more stable, settled population, indicating better retention of local hazard knowledge and lower relative vulnerability.

**Data Source:**
For the 2022 England LSOA dataset, the underlying data for this indicator is derived from the Consumer Data Research Centre (CDRC) 2021, specifically utilizing the CDRC Residential Mobility Index (average 2012–2020). Its application and weighting vary depending on the specific hazard:
*   **Heat Indices:** For both the heat Inability to Prepare and Inability to Respond indices, it serves as the sole indicator within the "Local knowledge" domain, carrying a full weight of 1.000.
*   **Flood Indices:** For the flood Inability to Prepare and Inability to Respond indices, it carries a weight of 0.333 within the "Local knowledge" domain, sharing the dimension with indicators measuring a lack of flood alert/warning coverage and a lack of local past experience with historical flooding.