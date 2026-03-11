### Lack of school-related networks (% children not of primary school age)

**Description:**
This field (identified internally as `LackSchoolRelatedNetworks` or standardized as a Z-score under `ZLackSchoolRelatedNetworks` in the spatial dataset) represents the percentage of the population that is *not* of primary school age (4-11 years) within a given Lower Super Output Area (LSOA). It serves as a proxy metric for measuring the relative absence of local, school-based community ties within a neighbourhood.

**Vulnerability Rationale:**
This metric is a core indicator within the "Social networks" domain, which is utilized to evaluate a community's "(In)ability to Respond" and "(In)ability to Recover" from extreme climate events, such as floods and heatwaves, as well as its overall level of "Community Support". 

The primary assumption behind this indicator is that families with primary school-aged children tend to be better connected to local social networks through schools, other parents, and community activities. Conversely, a *lack* of these networks points to a higher level of social isolation in the area. Socially isolated populations are more vulnerable during extreme weather events because:
*   **Reduced Support:** They are less likely to ask for assistance during a crisis or benefit from collective community responses.
*   **Information Gaps:** They are less likely to benefit from the shared local knowledge and informal warning dissemination that spreads quickly through strong community networks.
*   **Slower Recovery:** Evidence shows that areas with weaker social networks struggle more with continuity of care (e.g., medical treatments) and experience a slower overall recovery following an emergency situation.

**Interpretation:**
Because having school-aged children provides a protective function (better social cohesion), the original census data is specifically **reversed** (calculated as 100% minus the percentage of children aged 4-11) so that the indicator measures the *lack* of these networks. This aligns it with the standard dataset format where higher values equal higher vulnerability:
*   **Higher percentages (or positive Z-scores):** Denote a greater *lack* of school-related networks (meaning fewer families with young children in the area), indicating greater potential social isolation and a **higher** level of social vulnerability.
*   **Lower percentages (or negative Z-scores):** Signify a higher proportion of school-aged children, indicating stronger community networks and **lower** relative vulnerability.

**Data Source:**
For the updated 2022 England LSOA dataset, no direct recent update was available, so the underlying data relies on the 2011 UK Census (specifically derived from Census table QS103: Number of people aged 4-11 years, divided by the total population, multiplied by 100, and then reversed). When calculating specific composite vulnerability indices, such as the "Inability to Respond" and "Inability to Recover" indices, it carries a weight of 0.500 within the broader "Social networks" domain, sharing this dimension equally with the indicator for single-pensioner households.