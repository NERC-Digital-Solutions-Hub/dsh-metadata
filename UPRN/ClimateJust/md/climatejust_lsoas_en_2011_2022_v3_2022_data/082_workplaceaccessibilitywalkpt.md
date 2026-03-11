### Workplace accessibility by walking or public transport (travel time, destination and origin indicators)

**Description:**
This field (identified internally as `WorkplaceAccessibilityWalkPT` in the spatial dataset) represents the travel time required to reach employment centres by walking or using public transport within a given Lower Super Output Area (LSOA). It serves as a measure of local accessibility and the mobility constraints faced by residents who commute without private vehicles.

**Vulnerability Rationale:**
This metric is an indicator within the "Mobility" domain, which is utilized to evaluate a community's "(In)ability to Prepare", "(In)ability to Respond", and "(In)ability to Recover" from extreme climate events, such as floods and heatwaves. 

Higher travel times equate to lower general accessibility and indicate a higher level of social vulnerability. The rationale for this includes:
*   **Transport Disruptions:** During extreme weather events like floods or heatwaves, public transport services are frequently disrupted or delayed. People who already face long commutes via public transit or walking are disproportionately impacted by these disruptions.
*   **Slower Emergency Response:** When individuals are working far from home and rely on walking or public transit, it takes them significantly longer to return home to deploy property-level protections (like flood gates) or to assist vulnerable dependents during a rapidly developing crisis.
*   **Reduced Mobility:** Communities with poor public transit connections to major hubs (like employment centres) generally have fewer mobility options overall, restricting their ability to evacuate or move away from an affected area.

**Interpretation:**
When used to calculate the final vulnerability indices, the data allows for relative comparisons across different geographic areas:
*   **Higher values (longer travel times)** denote poorer accessibility to employment centres, indicating greater mobility constraints and a **higher** level of social vulnerability.
*   **Lower values (shorter travel times)** signify good public transport and walking access, indicating greater mobility and **lower** relative vulnerability.

**Data Source:**
For the 2022 England LSOA dataset, the underlying data for this indicator is derived from the Department for Transport's Journey Time Statistics, 2017. Specifically, it utilizes table JTS0501: "Travel time, destination and origin indicators for Employment centres by mode of travel" at the LSOA level. It carries a weight of 0.200 within the broader "Mobility" domain.