### Number of properties within historical flood boundary (Z-Score)

**Description:**
This field (identified as `ZDirectFloodExperience` in the spatial dataset) represents the standardized Z-score for the number of properties located within historical flood boundaries within a given Lower Super Output Area (LSOA). It measures the relative level of direct, past flood experience in a specific neighbourhood compared to the national average across England. 

**Vulnerability Rationale:**
This metric is a core indicator within the "Local Knowledge" domain, which is utilized to evaluate a community's "(In)ability to Prepare" and "(In)ability to Respond" to extreme climate events. 

Unlike most vulnerability indicators, a higher proportion of properties within a historical flood boundary actually indicates a **lower** level of social vulnerability. The rationale for this is often described as the "prisoner of experience" phenomenon:
*   **Awareness and Preparedness:** Communities with direct experience of past flooding have significantly more local knowledge about what to do, how to respond, and how to effectively take preventative action. 
*   **Warning Response:** Households that have previously flooded generally demonstrate a higher level of understanding of flood warning codes and take them more seriously.
*   **Community and Institutional Support:** Areas with a history of flooding are more likely to have established community support networks and a higher level of ongoing activity and support from government and non-government organizations.

**Interpretation:**
Because past experience *reduces* vulnerability, this indicator is **reversed** when calculating the final vulnerability indices. 
*   A neighbourhood with a high concentration of properties in historical flood boundaries will have greater local knowledge, effectively lowering its social vulnerability score.
*   Conversely, a neighbourhood with little to no historical flood experience lacks this localized knowledge and preparedness, which increases its relative vulnerability to unexpected flood events.

To map and categorize the relative severity of vulnerabilities, the dataset standardizes scores into classifications ranging from **Acute** (highest vulnerability/least experience) to **Slight** (lowest vulnerability/most experience).

**Data Source:**
For the 2022 England LSOA dataset, this indicator relies on estimates originally compiled by Sayers et al. (2017), which queried national residential property datasets against historical flood outlines limited to the past 50 years (sourced from the Environment Agency, Natural Resources Wales, SEPA, and NI Rivers Agency). It carries a weight of 0.333 within the broader "Local Knowledge" domain alongside indicators for population transience and flood warning coverage.