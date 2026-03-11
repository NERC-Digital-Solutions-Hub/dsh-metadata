### Socio Spatial Heat Vulnerability Index

**Description:**
This field (identified internally as `SSHVI` in the spatial dataset) represents the overall mapped social vulnerability of a Lower Super Output Area (LSOA) with respect to extreme heat hazards. It illustrates how various personal, social, and environmental factors combine to explain why certain neighbourhoods are likely to experience disproportionately negative impacts from high temperatures.

**Composition and Dimensions:**
The index is calculated as an equally weighted combination of standardized neighbourhood-level scores (Z-scores) across five key dimensions of socio-spatial vulnerability:
1.  **Sensitivity:** Personal biophysical characteristics (such as age and pre-existing health conditions) that make individuals more physically susceptible to heat-related illness.
2.  **Enhanced Exposure:** Aspects of the local physical environment (such as a lack of green space or living in high-rise housing) that tend to accentuate the severity of heat events.
3.  **Inability to Prepare:** Social factors that limit a community's capacity to take precautions before an event, including income, housing tenure, language barriers, internet access, and a lack of local knowledge.
4.  **Inability to Respond:** Factors that hinder immediate action to avoid heat stress during a heatwave, such as a lack of social networks, limited mobility, fear of crime, and a lack of general community infrastructure.
5.  **Inability to Recover:** Factors affecting the ability to bounce back if heat stress occurs, heavily influenced by local service access (e.g., travel times to GPs, hospitals, and pharmacies).

**Interpretation:**
The final SSHVI is presented as a standardized Z-score to allow for direct relative comparison across England. Based on the dataset's classification scheme:
*   **Positive values (High scores):** Indicate higher social vulnerability than the English average. Scores ≥ 2.5 are classified as "Acute", scores between 1.5 and 2.5 are "Extremely high", and scores between 0.5 and 1.5 are "Relatively high".
*   **Values around 0 (0.5 to -0.5):** Denote that the neighbourhood's vulnerability is approximately "Average".
*   **Negative values (Low scores):** Indicate lower social vulnerability than the average, scaling down through "Relatively low", "Extremely low", and "Slight" (≤ -2.5).

**Hazard and Disadvantage Context:**
It is important to note that the SSHVI maps where severe *social impacts* are most likely, independent of the actual likelihood of a severe heatwave hitting that specific location. Within the wider dataset, this index is combined equally with localized climate projections (for the present day and 1.5°C, 2°C, and 3°C warmer worlds) to calculate the overall relative **Heat Disadvantage** for a neighbourhood.