### Median combined size of parks and public gardens and playing fields within 1,000 m radius (Z-Score)

**Description:**
This field (identified internally as `ZAverageCommunityGreenspace` in the spatial dataset) represents the standardized Z-score for the median combined area (in square metres) of parks, public gardens, and playing fields within a 1,000-metre radius of a given Lower Super Output Area (LSOA). It measures how the local availability and size of public community greenspaces in a specific neighbourhood compare to the national average across England.

**Vulnerability Rationale:**
This metric is a core indicator within the "Physical Environment" domain, which is utilized to evaluate a community's "Enhanced Exposure" to both extreme heat and flooding events. 

The physical characteristics of a neighbourhood can significantly accentuate or offset the severity of an extreme weather event:
*   **Flooding:** Larger areas of greenspace provide pervious surfaces that result in higher natural water infiltration and better drainage, effectively offsetting exposure to surface water flooding.
*   **Heatwaves:** Greenspace provides vital natural cooling functions that help reduce the severity of high urban temperatures during heatwaves.

**Interpretation:**
Because having *more* greenspace provides a protective function (and thus *lower* vulnerability), the original data for this indicator is **reversed** when calculating the final vulnerability indices. Standardizing this metric as a Z-score allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a *smaller* median size of public greenspace than the national average, indicating less natural cooling and drainage capacity, which results in higher enhanced exposure and greater relative vulnerability.
*   **Values around 0** indicate that the median size of community greenspace is approximately average for England.
*   **Negative values** signify a *larger* median size of greenspace than the national average, indicating lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the 2022 England LSOA dataset, the underlying data for this indicator is derived from the Office for National Statistics (ONS) Greenspace dataset. It carries a weight of 0.330 within the broader "Physical Environment" domain, sharing this dimension with indicators for built-up urban land cover and a lack of private domestic gardens.