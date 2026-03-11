### Social renters (% Households renting from Social or Council landlords)

**Description:**
This field (identified internally as `SocialRentersHH` in the spatial dataset) represents the percentage of households that rent their accommodation from a social landlord, such as a local council or housing association, within a given Lower Super Output Area (LSOA). It measures the local concentration of social housing to evaluate tenure-related vulnerabilities. 

**Vulnerability Rationale:**
This metric is a core indicator within the "Tenure" domain, which is utilized to evaluate a community's "(In)ability to Prepare" for extreme climate events, including both floods and heatwaves,. 

Higher proportions of social renters indicate a higher level of social vulnerability. The rationale driving this includes:
*   **Inability to Modify Homes:** Tenants generally have much less autonomy than homeowners to adapt their living environments,. Social renters are often restricted from making physical alterations to their properties, making it difficult to install preventative measures like property-level flood defences or structural cooling adaptations for heatwaves,,. 
*   **Intersecting Deprivation:** Social housing tenants often face intersecting vulnerabilities, particularly because they are more likely to be on a low income, meaning they lack the financial resources to prepare for or respond to sudden extreme weather,. 
*   **Potential for Top-Down Adaptation:** A notable caveat to this vulnerability is that social tenants *may* benefit from large-scale adaptations if social landlords proactively put wider resilience measures in place across their housing stock.

**Interpretation:**
When used to calculate the final vulnerability indices, this raw percentage is often standardized (e.g., as a Z-score, `Z_SocialRenters_HH`) to allow for direct relative comparisons across different geographic areas:
*   **Higher percentages** denote a larger concentration of social renters, indicating a lower overall community ability to independently adapt properties and a higher level of social vulnerability,.
*   **Lower percentages** signify fewer social renters, indicating relative higher rates of homeownership or private renting.

**Data Source:**
For the 2022 England LSOA dataset, no direct recent update was available, so the underlying data relies on the 2011 UK Census. Specifically, it utilizes Census table KS402 (the sum of '% households social rented: council' and '% households social rented: other'),. It carries a weight of 0.500 within the broader "Tenure" domain (sharing it equally with the private renters indicator), and the Tenure domain itself contributes a weight of 0.200 to the overall "(In)ability to Prepare" index for both heat and flood events,.