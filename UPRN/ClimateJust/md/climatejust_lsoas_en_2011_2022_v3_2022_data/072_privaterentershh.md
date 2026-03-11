### Private renters (% Households)

**Description:**
This field (identified internally as `PrivateRentersHH` in the spatial dataset) represents the percentage of households that rent their accommodation from a private landlord or letting agency within a given Lower Super Output Area (LSOA). It measures the local concentration of private renting to evaluate tenure-related vulnerabilities. 

**Vulnerability Rationale:**
This metric is a core indicator within the "Tenure" domain, which is utilized to evaluate a community's "(In)ability to Prepare" for extreme climate events, including both floods and heatwaves. 

Higher proportions of private renters indicate a higher level of social vulnerability. The rationale driving this includes:
*   **Inability to Modify Homes:** Private tenants generally have much less autonomy than homeowners and are often not permitted to make physical alterations to their properties. This makes it very difficult for them to independently install preventative measures, such as property-level flood defences or structural cooling adaptations for heatwaves. 
*   **Short Tenancies:** Private rentals often feature shorter lease terms and limited security of tenure. Because these residents move more frequently, they are likely to be less aware of the historical flood risks in their immediate neighbourhoods or local emergency procedures.
*   **Intersecting Disadvantage:** Evidence suggests that private renters are generally less well-off than homeowners, which means they may lack the financial capacity to afford meaningful physical risk-reducing measures or robust contents insurance. Furthermore, landlords in the private sector can be difficult to engage in residential flood protection planning.

**Interpretation:**
When used to calculate the final vulnerability indices, this raw percentage is standardized (e.g., as a Z-score, `Z_PrivateRenters_HH`) to allow for direct relative comparisons across different geographic areas:
*   **Higher percentages** denote a larger concentration of private renters, indicating a lower overall community ability to independently adapt properties and a higher level of social vulnerability.
*   **Lower percentages** signify fewer private renters, indicating relative higher rates of homeownership and lower relative vulnerability.

**Data Source:**
For the 2022 England LSOA dataset, no direct recent update was available, so the underlying data relies on the 2011 UK Census. Specifically, it utilizes Census table KS402 (the sum of '% households Private Rented; Private Landlord or Letting Agency' and '% households Private Rented; Other'). It carries a weight of 0.500 within the broader "Tenure" domain (sharing it equally with the social renters indicator), and the Tenure domain itself contributes a weight of 0.200 to the overall "(In)ability to Prepare" index for both heat and flood events.