### Relative heat Disadvantage, recent past 30 year mean 1990 - 2019

**Description:**
This field (identified internally as `ZarHeatDisadvantageRecentPast` in the spatial dataset) represents the final "all-relative" heat disadvantage score for a given Lower Super Output Area (LSOA) during the recent past baseline period (1990–2019). 

**Hazard and Vulnerability Context:**
"Heat Disadvantage" acts as a composite metric identifying where extreme heat hazard-exposure and socio-spatial vulnerability coincide. It is calculated as an equally weighted combination of two key factors for each LSOA:
1.  **Climate Hazard Data:** The average daily-maximum temperature for the top 5% hottest days in the recent past (1990–2019).
2.  **Social Vulnerability:** The local Socio-Spatial Heat Vulnerability Index (SSHVI) score.

**All-Relative Standardization:**
Crucially, the "Zar" prefix in the internal field name indicates that this is an **"All-relative Z-score"**. This score is standardized using the mean and standard deviation across *all four* of the dataset's temperature scenarios: the recent past baseline, plus the 1.5°C, 2°C, and 3°C warmer future worlds. This specific standardization method enables users to make direct comparisons of relative heat disadvantage not only across different geographic locations in England but also across different timeframes and future warming scenarios.

**Interpretation:**
Because this field is presented as an all-relative Z-score, it evaluates how a specific neighbourhood's historical heat disadvantage compares to the overall multi-scenario average. Based on the dataset's classification scheme:
*   **Positive values (High scores):** Denote higher heat disadvantage compared to the overall average. Scores ≥ 2.5 are classified as "Acute", scores between 1.5 and 2.5 are "Extremely high", and scores between 0.5 and 1.5 are "Relatively high".
*   **Values around 0 (-0.5 to 0.5):** Denote heat disadvantage that is around the overall average for England.
*   **Negative values (Low scores):** Denote lower heat disadvantage compared to the average, scaling down through "Relatively low" (-0.5 to -1.5), "Extremely low" (-1.5 to -2.5), and "Slight" (≤ -2.5).

**Data Source:**
For the updated 2022 England LSOA dataset, the underlying climate data is derived from the analysis of Kennedy-Asser et al. (2022), which utilizes regional climate model simulations from the Met Office's UK Climate Projections 2018 (UKCP18). This is then equally combined with the dataset's internal SSHVI calculations.