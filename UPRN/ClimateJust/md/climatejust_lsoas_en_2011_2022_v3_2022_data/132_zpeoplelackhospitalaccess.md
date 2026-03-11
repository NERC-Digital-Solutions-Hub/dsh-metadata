### People lacking easy hospital access (%) (Z-Score)

**Description:**
This field (identified internally as `ZPeopleLackHospitalAccess` in the spatial dataset) represents the standardized score (Z-score) for the percentage of the local population that lacks easy access to a hospital within a given Lower Super Output Area (LSOA). This indicator typically captures the proportion of the at-risk population (such as those without access to a private car) who live more than 30 minutes away from the nearest hospital by walking or public transport.

**Vulnerability Context:**
This indicator is a key component of the "Hospital Access" (or "Service access") domain, which feeds into the **(In)ability to Recover** dimension of the socio-spatial vulnerability indices. 

The core assumption behind this metric is that communities with higher proportions of people lacking easy access to hospital care are more socially vulnerable. During and after extreme weather events, such as severe heatwaves, residents may suffer from serious health impacts (like heat stress) and require rapid medical assistance. A lack of easy access to a hospital significantly hinders a community's capacity to obtain this emergency help and successfully recover from the event.

**Interpretation:**
Because this field is presented as a standardized Z-score, it evaluates how a specific neighbourhood compares to the overall average across England:
*   **Positive values (High scores):** Denote areas with a *higher* percentage of people lacking easy hospital access compared to the national average. This indicates poorer access to emergency medical support and translates to **higher social vulnerability**.
*   **Negative values (Low scores):** Denote areas with a *lower* percentage of people lacking easy access compared to the average. This indicates better, more reliable access to hospital care and, therefore, **lower social vulnerability**.

**Data Source:**
For the 2022 England LSOA dataset, the underlying data used to calculate this standardized score is derived from the Department for Transport's Journey Time Statistics 2017 (specifically, Table JTS0506: Travel time, destination and origin indicators for Hospitals by mode of travel, Lower Super Output Area, England).