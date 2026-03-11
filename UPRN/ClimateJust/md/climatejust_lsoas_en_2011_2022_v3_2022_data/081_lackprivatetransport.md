### Lack of private transport (% households with no car or van)

**Description:**
This field (identified internally as `LackPrivateTransport` and often standardized as a Z-score under `ZLackPrivateTransport` in the spatial dataset) represents the percentage of households within a given Lower Super Output Area (LSOA) that do not own or have access to a car or van. It serves as a primary proxy metric to evaluate a local community's level of personal and household physical mobility.

**Vulnerability Rationale:**
This metric is a core indicator within the "Mobility" domain, utilized to evaluate a community's "(In)ability to Respond" and "(In)ability to Recover" from extreme climate events, such as floods and heatwaves. 

Higher proportions of households without private transport indicate a higher level of mobility-related social vulnerability. The primary rationale driving this vulnerability includes:
*   **Restricted Evacuation and Relocation:** Individuals without private vehicles have significantly less capacity to independently relocate or evacuate away from danger during a rapid-onset emergency. 
*   **Public Transport Reliance:** Those without cars are highly dependent on public transport services, which are frequently delayed, suspended, or entirely disrupted during severe floods and extreme heatwaves.
*   **Assisting Dependents and Accessing Services:** A lack of private transport restricts a householder's ability to quickly travel to assist vulnerable family members or dependents in other locations. It can also mean the difference between life and death if individuals need to rapidly access essential medical help or recovery services during a crisis.

**Interpretation:**
When used to calculate the final vulnerability indices, this raw percentage is frequently standardized as a Z-score to allow for direct relative comparisons across different geographic areas:
*   **Higher percentages (or positive Z-scores)** denote a higher concentration of households without cars, indicating lower community mobility, a slower overall response capacity, and a higher level of social vulnerability.
*   **Lower percentages (or negative Z-scores)** signify widespread access to private transport, indicating greater independent mobility and lower relative vulnerability.

**Data Source:**
For the 2022 England LSOA dataset, no direct recent update was available, so the underlying data relies on the 2011 UK Census. Specifically, it utilizes Census table KS404 (or KS404SC), calculated by taking the number of households with 'No cars or vans' divided by the total number of households. It carries a weight of 0.200 within the broader "Mobility" domain for both the "Inability to Respond" and "Inability to Recover" vulnerability indices.