### 1.5℃ warmer world 

**Description:**
This field (identified internally as `TmaxP95Future15` for the raw temperature in Celsius, or `ZartMaxP95Future15` for the standardized "All-relative Z-Score" in the spatial dataset) represents the projected average daily-maximum temperature for the top 5% hottest days within a given Lower Super Output Area (LSOA). This projection specifically models a future scenario where global average surface temperatures are 1.5°C warmer than the pre-industrial period. 

**Hazard and Vulnerability Context:**
This metric serves as a key indicator of future extreme heat exposure. Within the dataset, this localized climate hazard data is combined equally with the Socio-Spatial Heat Vulnerability Index (SSHVI) to calculate the "Relative heat Disadvantage, 1.5°C warmer world" for each LSOA. This helps identify which neighbourhoods will face the most severe climate disadvantage if global temperatures reach the 1.5°C threshold.

**Interpretation:**
*   **Higher raw values (°C):** Denote geographical areas expected to experience more severe extreme high temperatures during their hottest days under a 1.5°C global warming scenario.
*   **Standardized values (All-relative Z-Score):** To facilitate direct comparisons, the data is also provided as an "All-relative Z-score". Unlike standard Z-scores that only compare areas within a single timeframe, this score is calculated using the mean and standard deviation across *all* of the dataset's temperature scenarios (recent past, 1.5°C, 2°C, and 3°C). This allows users to directly compare relative temperature extremes and disadvantage across both different geographic locations and different future warming scenarios.

**Data Source:**
For the updated 2022 England LSOA dataset, this climate data is derived from the analysis of Kennedy-Asser et al. (2022). Their research utilizes regional climate model simulations on a 12km grid over the UK from the Met Office Hadley Centre's UK Climate Projections 2018 (UKCP18).