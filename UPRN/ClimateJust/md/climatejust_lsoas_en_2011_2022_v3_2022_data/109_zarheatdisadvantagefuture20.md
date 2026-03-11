### Relative heat Disadvantage, 2℃ warmer world

**Description:**
This field (identified internally as `ZarHeatDisadvantageFuture20` in the spatial dataset) represents the **"all-relative" heat disadvantage score** for a given Lower Super Output Area (LSOA) under a projected future scenario where global average surface temperatures are **2°C warmer than pre-industrial levels**. 

**Hazard and Vulnerability Context:**
**"Heat Disadvantage"** acts as a composite metric identifying where extreme heat hazard-exposure and socio-spatial vulnerability coincide. It is calculated as an equally weighted combination of two key factors for each LSOA:
1.  **Climate Hazard Data:** The projected average daily-maximum temperature for the top 5% hottest days in a 2°C warmer world.
2.  **Social Vulnerability:** The local Socio-Spatial Heat Vulnerability Index (SSHVI) score.

**All-Relative Standardization:**
Crucially, the "Zar" prefix in the internal field name indicates that this is an **"All-relative Z-score"**. This score is standardized using the mean and standard deviation across **all four of the dataset's temperature scenarios**: the recent past baseline, plus the 1.5°C, 2°C, and 3°C warmer future worlds. This specific standardization method enables users to make **direct comparisons of relative heat disadvantage not only across different geographic locations in England but also across different future warming scenarios**.

**Interpretation:**
Because this field is presented as an all-relative Z-score, it evaluates how a specific neighbourhood's heat disadvantage in a 2°C warmer world compares to the overall multi-scenario average. Based on the dataset's classification scheme:
*   **Positive values (High scores):** Denote higher heat disadvantage compared to the overall average. Scores ≥ 2.5 are classified as "Acute", scores between 1.5 and 2.5 are "Extremely high", and scores between 0.5 and 1.5 are "Relatively high".
*   **Values around 0 (-0.5 to 0.5):** Denote heat disadvantage that is around the overall average for England.
*   **Negative values (Low scores):** Denote lower heat disadvantage compared to the average, scaling down through "Relatively low" (-0.5 to -1.5), "Extremely low" (-1.5 to -2.5), and "Slight" (≤ -2.5).

**Data Source:**
For the updated 2022 England LSOA dataset, the underlying climate hazard data is derived from the analysis of Kennedy-Asser et al. (2022), which utilizes regional climate model simulations from the UK Climate Projections 2018 (UKCP18). This hazard data is then equally combined with the dataset's internal SSHVI calculations.