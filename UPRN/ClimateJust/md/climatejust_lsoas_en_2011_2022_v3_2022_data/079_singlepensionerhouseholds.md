### pensioner households (%)

**Description:**
This field (identified internally as `SinglePensionerHouseholds` and aliased as `pensioner households (%)` in the 2022 spatial dataset) represents the percentage of households consisting of a single person aged 65 and over within a given Lower Super Output Area (LSOA). It serves as a proxy metric to measure the local concentration of lone pensioners and evaluate vulnerabilities related to social isolation.

**Vulnerability Rationale:**
This metric is a core indicator within the "Social networks" domain, which is utilized to evaluate a community's "(In)ability to Respond" and "(In)ability to Recover" from extreme climate events, such as floods and heatwaves. 

Higher proportions of single-pensioner households indicate a higher level of social vulnerability. The primary rationale driving this vulnerability includes:
*   **Social Isolation:** Areas with high numbers of lone pensioners are more likely to contain socially isolated individuals. Socially isolated people are more vulnerable because they are less likely to ask for assistance and less likely to benefit from community knowledge and wider community responses.
*   **Lack of Informal Support:** Informal support networks are often absent during an extreme event. Adults who live alone may struggle to take physical action during a flood warning (such as moving heavy furniture) and may feel more uncertain and anxious without someone to confide in.
*   **Evacuation and Recovery:** Isolated individuals may face greater difficulties accessing short-term alternative accommodation with family or friends and are more likely to need public shelters if evacuated.

*Note: The broader Climate Just framework also sometimes assesses "All pensioner households" as a proxy for low income within the "Income" domain, as pensioner households generally have lower incomes than working households. However, this specific mapped field focuses on the isolation aspect of single-pensioner households.*

**Interpretation:**
When used to calculate the final vulnerability indices, this raw percentage allows for direct relative comparisons across different geographic areas:
*   **Higher percentages** denote a larger concentration of single-pensioner households, indicating weaker community social networks, a higher likelihood of social isolation, and a higher level of relative vulnerability.
*   **Lower percentages** signify fewer lone pensioners, indicating relatively stronger social networks and lower relative vulnerability.

**Data Source:**
For the 2022 England LSOA dataset, no direct recent update was available, so the underlying data relies on the 2011 UK Census. Specifically, it utilizes Census table QS113, calculated by taking the number of 'One-person household: Aged 65 and over' divided by the total number of households. It carries a weight of 0.500 within the broader "Social networks" domain, sharing this dimension with an indicator measuring a lack of school-related networks (children not of primary school age).