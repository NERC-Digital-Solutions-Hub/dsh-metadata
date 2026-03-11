### Caravan or other mobile or temporary structures (% of all households)

**Description:**
This field (identified internally as `CaravanOrTemporaryStructures` and standardized as a Z-score under `ZCaravanOrTemporaryStructures` in the spatial dataset) represents the percentage of households residing in a caravan or another type of mobile or temporary structure within a given Lower Super Output Area (LSOA). It is used as a spatial metric to evaluate the quality and structural resilience of the local housing stock.

**Vulnerability Rationale:**
This metric is an indicator within the "Housing Characteristics" domain, utilized to evaluate a community's "Enhanced Exposure" and level of "Community Support" in the face of extreme climate events, particularly flooding. 

Higher proportions of people living in caravans or temporary structures indicate a significantly higher level of social and physical vulnerability. The rationale for this includes:
*   **Limited Physical Protection:** Temporary and mobile structures are generally of poorer quality and provide far more limited physical protection against floodwaters than structurally competent, permanent buildings, meaning sudden floods can devastate these homes and even place lives at risk.
*   **Restricted Emergency Response:** During a flood warning, residents in temporary structures are less likely to be able to move their possessions to a place of safety (such as an upper floor), leading to higher proportional losses.
*   **Institutional Disadvantage:** In official flood defence project appraisals, caravans are often classified as "moveable" during times of flood. Because of this, they rarely feature in standard assessments of damages, meaning these communities may not benefit from the funding and construction of broader flood defences.
*   **Lack of Local Knowledge:** Evidence suggests that residents of caravan parks and mobile homes are more likely to have a limited knowledge of the local area and its specific historical flood risks.

**Interpretation:**
When used to calculate the final composite vulnerability indices, this raw percentage is standardized (as a Z-score) to allow for direct relative comparisons across different geographic areas:
*   **Higher percentages (or positive Z-scores):** Denote a larger proportion of the population living in temporary structures, indicating lower structural resilience, higher enhanced exposure, and a **higher** level of overall social vulnerability.
*   **Lower percentages (or negative Z-scores):** Signify that a neighbourhood consists predominantly of permanent housing, indicating better physical protection and **lower** relative vulnerability.

**Data Source:**
For the updated 2022 England LSOA dataset, no direct recent update was available, so the underlying data relies on the 2011 UK Census, integrated via Sayers et al. (2017). Specifically, it utilizes Census table KS401 (calculated by taking the number of 'All household spaces: Caravan or other mobile or temporary structure' divided by the total number of households and multiplied by 100). Depending on the specific index being calculated, it carries a weight of either 0.500 or 1.000 within the broader "Housing Characteristics" domain.