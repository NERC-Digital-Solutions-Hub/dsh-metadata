### Workplace accessibility by walking or public transport (Z-Score)

**Description:**
This field (identified as `ZWorkplaceAccessibilityWalkPT` in the spatial dataset) represents the standardized Z-score for the travel time to employment centres by walking or public transport within a given Lower Super Output Area (LSOA). It measures how local travel times to workplaces using public transit or walking in a specific neighbourhood compare to the national average across England.

**Vulnerability Rationale:**
This metric is a supporting indicator within the "Mobility" domain, which is utilized to evaluate a community's "(In)ability to Respond" and "(In)ability to Recover" from extreme climate events, such as floods and heatwaves. 

Higher travel times to employment centres equate to higher social vulnerability. The rationale for this is based on the challenges of working far from home or having long commutes:
*   **Delayed Response:** People facing long travel times on foot or via public transport are more likely to have a slower response to sudden extreme events (such as flash floods or unexpected heatwave warnings) because it takes them longer to get back to their local area. 
*   **Assisting Dependents:** Being further away or delayed restricts an individual's capacity to quickly return home to assist vulnerable dependents, such as children or elderly relatives, during an emergency. 
*   **Transport Disruptions:** Commuters who rely on public transport for long journeys are disproportionately affected when extreme weather causes severe disruptions or cancellations across the public transport network.

**Interpretation:**
Because this metric is standardized as a Z-score, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote higher travel times (poorer workplace accessibility) than the national average, indicating a higher level of mobility-related vulnerability.
*   **Values around 0** indicate that the travel time is approximately average for England.
*   **Negative values** signify shorter travel times (better workplace accessibility) than the national average, indicating lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the updated 2022 England LSOA dataset, the underlying data for this indicator is derived from the Department for Transport's Journey Time Statistics (2017). Specifically, it uses table JTS0501: "Travel time, destination and origin indicators for Employment centres by mode of travel, Lower Super Output Area (LSOA)". It carries a weight of 0.200 within the broader "Mobility" domain alongside other indicators like lack of private transport and comparative illness.