### Median price paid for residential properties (£)

**Description:**
This field (identified internally as `HousingTrap` for the raw monetary value, and standardized as a Z-score under `ZHousingTrap` in the spatial dataset) represents the median price paid for residential properties within a given Lower Super Output Area (LSOA). It serves as an economic proxy to measure local neighbourhood wealth and property values.

**Vulnerability Rationale:**
This metric is the sole indicator within the "House Prices" domain, which is utilized to evaluate a community's "(In)ability to Prepare" and "(In)ability to Recover" from extreme climate events. 

The underlying assumption is that property values are indicative of broader community wealth and resources. Lower house prices generally point to areas with lower average wealth, meaning residents are less likely to have the financial capacity to invest in property-level adaptation measures (such as flood defences) prior to an event, and have fewer resources to draw upon to recover and repair damages following a disaster. 

**Interpretation:**
Because higher house prices denote a *greater* ability to recover and prepare, the raw data for this indicator is **reversed** when calculating the final vulnerability indices. This ensures it aligns with the standard dataset format where higher scores must equal higher vulnerability:
*   **Higher scores (or positive Z-scores):** Denote *lower* median house prices, indicating less community wealth, a reduced capacity to respond or rebuild, and a **higher** level of social vulnerability.
*   **Lower scores (or negative Z-scores):** Signify *higher* median house prices, indicating greater financial resources within the community and **lower** relative vulnerability.

**Data Source:**
For the 2022 England LSOA dataset, the underlying data for this indicator is derived from the HPSSA (House Price Statistics for Small Areas) Dataset 46, specifically the "Median price paid for residential properties by LSOA, England and Wales," utilizing data up to the year ending December 2020. As the only indicator in the "House Prices" domain, it carries a full weight of 1.000 within that category, and the domain itself contributes a weight of 0.143 to the broader "Inability to Prepare" and "Inability to Recover" indices.