### Built up area (% not greenspace)

**Description:**
This field (identified internally as `UrbanCover` and frequently standardized as a Z-score under `ZUrbanCover` in the spatial dataset) represents the percentage of land within a given Lower Super Output Area (LSOA) that is classified as urban or built-up. It serves as a direct spatial measure to evaluate the local lack of natural green space within a neighbourhood.

**Vulnerability Rationale:**
This metric is a core indicator within the "Physical Environment" domain, which is utilized to evaluate a community's "Enhanced Exposure" to extreme climate events, particularly heatwaves and floods. 

The physical characteristics of a neighbourhood can significantly accentuate or mitigate the severity of weather events. Higher proportions of built-up areas indicate a higher level of environmental vulnerability. The rationale driving this includes:
*   **Heatwaves:** Built-up areas absorb and retain more heat, exacerbating local temperatures due to the urban heat island effect. Conversely, green spaces provide a vital natural cooling function for the surrounding neighbourhood. 
*   **Flooding:** Heavily built-up environments typically have a higher proportion of impermeable surfaces. This lack of pervious cover restricts natural water infiltration, leading to poorer drainage during heavy rainfall and enhancing the community's exposure to surface water flooding.

**Interpretation:**
When used to calculate the final vulnerability indices, the raw percentage is standardized (as a Z-score) to allow for direct relative comparisons across different geographic areas:
*   **Higher percentages (or positive Z-scores)** denote a more densely built-up area with less greenspace, indicating higher enhanced exposure and a **higher** level of overall vulnerability.
*   **Lower percentages (or negative Z-scores)** signify a higher proportion of natural green space, indicating better natural cooling and drainage capacity, and therefore **lower** relative vulnerability.

**Data Source:**
For the 2022 England LSOA dataset, the underlying data for this indicator is extracted from the UK Centre for Ecology & Hydrology (UKCEH) Land Cover Maps (2021) representing urban land cover. It is calculated by subtracting the area of greenspace from 100%. It carries a weight of 0.330 within the broader "Physical Environment" domain, sharing this dimension with other environmental indicators, such as the lack of domestic gardens and the median combined size of local parks and playing fields.