### Lack of domestic gardens (% dwellings without gardens)

**Description:**
This field (identified internally as `LackPrivateGreenspaceFlood` or `LackPrivateGreenspaceHeat`, and standardized as Z-scores under `ZLackPrivateGreenspaceFlood` and `ZLackPrivateGreenspaceHeat` in the spatial dataset) represents the percentage of residential dwellings within a given Lower Super Output Area (LSOA) that do not possess a private domestic garden. It serves as a measure of the local physical environment to assess the availability of private green infrastructure.

**Vulnerability Rationale:**
This metric is a core indicator within the "Physical Environment" domain, which is utilized to evaluate a community's "Enhanced Exposure" to extreme climate events, specifically floods and heatwaves.

A lack of private gardens in a neighbourhood accentuates the severity of climate impacts for two primary reasons:
*   **Heatwaves:** Domestic gardens provide an essential local cooling function that helps mitigate high temperatures during hot weather.
*   **Flooding:** Gardens offer pervious surfaces that provide better natural water drainage compared to concrete, asphalt, or heavily built-up environments.

Therefore, areas where a high proportion of housing lacks garden space are significantly more likely to experience severe impacts during extreme weather, as they lack these immediate natural drainage and cooling benefits.

**Interpretation:**
When used to calculate the final composite vulnerability indices, this raw percentage is standardized (as a Z-score) to allow for direct relative comparisons across different geographic areas:
*   **Higher percentages (or positive Z-scores)** denote a larger proportion of dwellings without gardens, indicating a higher level of enhanced exposure to climate hazards and **higher** overall social vulnerability.
*   **Lower percentages (or negative Z-scores)** signify that a larger proportion of homes have private gardens, indicating better local cooling and drainage capacity and **lower** relative vulnerability.

**Data Source:**
For the updated 2022 England LSOA dataset, the underlying data for this indicator is derived from the Office for National Statistics (ONS) Greenspace dataset (specifically, "Access to public green space in Great Britain"). It carries a weight of 0.330 within the broader "Physical Environment" domain, sharing this dimension with indicators measuring the proportion of built-up area (not greenspace) and the median size of nearby parks, public gardens, and playing fields.