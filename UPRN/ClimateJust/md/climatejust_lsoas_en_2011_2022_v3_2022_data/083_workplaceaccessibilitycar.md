### Workplace accessibility by car (travel time, destination and origin indicators)

**Description:**
This field (identified internally as `WorkplaceAccessibilityCar` in the spatial dataset) represents the average travel time to employment centres by car for residents within a given Lower Super Output Area (LSOA). It serves as a spatial proxy to measure how far and how long the local population typically commutes to work using private transport. 

**Vulnerability Rationale:**
This metric is an indicator within the "Mobility" domain, which is utilized to evaluate a community's "(In)ability to Prepare", "(In)ability to Respond", and "(In)ability to Recover" from extreme climate events, such as floods and heatwaves. 

The underlying rationale is that higher travel times to work equate to higher social vulnerability. Communities where a large proportion of the population works a long distance away from home are likely to exhibit a slower collective response to emergency warnings. Being a long distance from home restricts a person's ability to:
*   **Respond to Warnings:** Quickly return home during the day to deploy temporary property-level flood defences or secure belongings.
*   **Assist Others:** Rapidly travel back to their neighbourhood to assist vulnerable family members or dependents who may be struggling with sudden floodwaters or extreme heat. 

**Interpretation:**
When used to calculate vulnerability indices, this indicator assumes that longer commutes reduce adaptive capacity:
*   **Higher values (longer travel times)** denote a workforce that is generally further from home during the day, indicating slower community response capabilities and a **higher** level of relative social vulnerability.
*   **Lower values (shorter travel times)** signify that employment centres are highly accessible or closer to home, indicating quicker potential response times and **lower** relative vulnerability. 

**Data Source:**
For the updated 2022 England LSOA dataset, the underlying data for this indicator is derived from the Department for Transport's Journey Time Statistics 2017. Specifically, it utilizes table JTS0501 (Travel time, destination and origin indicators for Employment centres by mode of travel). It carries a weight of 0.200 within the broader "Mobility" domain, operating alongside other mobility indicators such as workplace accessibility by public transport, lack of private transport, and populations in medical/care establishments.