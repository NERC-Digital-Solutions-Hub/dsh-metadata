### Travel time to nearest GP by walk/public transport (minutes) (Z-Score)

**Description:**
This field (identified internally as `ZTravelTimeToGPWalkPT` in the spatial dataset) represents the standardized score (Z-score) of the estimated travel time (in minutes) required to reach the nearest General Practitioner (GP) surgery by walking or using public transport within a given Lower Super Output Area (LSOA).

**Vulnerability Context:**
This indicator is a component of the "GP access" domain, which feeds into the **(In)ability to Recover** dimension of the Socio-Spatial Heat Vulnerability Index (SSHVI). 

The underlying assumption for this metric is that communities with higher travel times to the nearest GP are more socially vulnerable. Physical isolation or a lack of mobility to reach medical help can be a critical factor during extreme weather events, such as heatwaves, as it hinders a community's capacity to access vital medical assistance to recover from severe health impacts like heat stress. 

**Interpretation:**
Because the metric is presented as a standardized Z-score, it evaluates how a specific neighbourhood compares to the overall average across England:
*   **Positive values (High scores):** Denote areas with *longer* travel times to a GP by foot or public transport compared to the national average. This indicates poorer access to medical support and translates to **higher social vulnerability**.
*   **Negative values (Low scores):** Denote areas with *shorter* travel times to a GP compared to the average, indicating better, quicker access to primary medical care and therefore **lower social vulnerability**.

**Data Source:**
For the 2022 England LSOA dataset, the underlying data used to calculate this standardized score is derived from the Department for Transport's Journey Time Statistics 2017 (specifically, Table JTS0505: Travel time, destination and origin indicators for GPs by mode of travel).