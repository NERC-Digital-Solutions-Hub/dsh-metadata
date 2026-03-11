### Median price paid for residential properties (Z-Score)

**Description:**
This field (identified as `ZHousingTrap` in the spatial dataset) represents the standardized Z-score for the median price paid for residential properties within a given Lower Super Output Area (LSOA). It measures how local house prices in a specific neighbourhood compare to the national average across England. 

**Vulnerability Rationale:**
This metric is the sole indicator within the "House prices" domain, which is utilized to evaluate a community's "(In)ability to Recover" from extreme climate events, such as floods and heatwaves. 

House prices act as a proxy for the general wealth and financial capacity of an area. Lower house prices generally indicate a lower ability to recover. Households in lower-value areas often have fewer financial resources or equity to draw upon to repair damages, replace lost goods, or relocate if their homes are severely impacted by extreme weather. Because higher house prices are associated with a *greater* ability to recover (and thus *lower* vulnerability), the original data for this indicator is **reversed** during index calculations.

**Interpretation:**
Because this metric is standardized as a Z-score and reversed to reflect vulnerability, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote *lower* median house prices than the national average, indicating less financial capacity and a higher level of social vulnerability.
*   **Values around 0** indicate that the median house prices are approximately average for England.
*   **Negative values** signify *higher* median house prices than the national average, indicating greater wealth and lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the 2022 England LSOA dataset, the underlying data for this indicator is derived from the HPSSA (House Price Statistics for Small Areas) Dataset 46, specifically utilizing the median price paid for residential properties by LSOA (year ending Dec 1995 to year ending Dec 2020). As the sole indicator for the House Prices domain, it carries a full weight of 1.000 within that domain, and the domain itself contributes a weight of 0.143 to the overall "(In)ability to Recover" index.