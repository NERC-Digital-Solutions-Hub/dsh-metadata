### Travel time to nearest hospital by walk/public transport (minutes) (Z-Score)

**Description:**
This field (identified internally as `ZTravelTimeToHospitalWalkPT` in the spatial dataset) represents the standardized score (Z-score) of the estimated travel time (in minutes) required to reach the nearest hospital by walking or using public transport within a given Lower Super Output Area (LSOA).

**Vulnerability Context:**
This indicator is a component of the "Hospital access" domain, which feeds into the **(In)ability to Recover** dimension of the Socio-Spatial Heat Vulnerability Index (SSHVI). 

The underlying assumption for this metric is that communities with higher travel times to the nearest hospital are more socially vulnerable. During and after extreme weather events, such as heatwaves, residents may suffer from severe health impacts (like heat stress) and require rapid medical assistance. A relative lack of mobility or physical isolation from emergency medical help significantly hinders a community's capacity to access this vital assistance and recover successfully.

**Interpretation:**
Because this metric is presented as a standardized Z-score, it evaluates how a specific neighbourhood compares to the overall average across England:
*   **Positive values (High scores):** Denote areas with *longer* travel times to a hospital by foot or public transport compared to the national average. This indicates poorer access to emergency medical support and translates to **higher social vulnerability**.
*   **Negative values (Low scores):** Denote areas with *shorter* travel times to a hospital compared to the average, indicating better, quicker access to medical care and therefore **lower social vulnerability**.

**Data Source:**
For the 2022 England LSOA dataset, the underlying data used to calculate this standardized score is derived from the Department for Transport's Journey Time Statistics 2017 (specifically, Table JTS0506: Travel time, destination and origin indicators for Hospitals by mode of travel).