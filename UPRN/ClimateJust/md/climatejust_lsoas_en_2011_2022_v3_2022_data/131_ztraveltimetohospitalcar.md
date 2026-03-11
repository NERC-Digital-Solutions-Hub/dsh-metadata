### Travel time to nearest hospital by car (minutes) (Z-Score)

**Description:**
This field (identified internally as `ZTravelTimeToHospitalCar` in the spatial dataset) represents the standardized score (Z-score) of the estimated travel time (in minutes) required to reach the nearest hospital by private car within a given Lower Super Output Area (LSOA).

**Vulnerability Context:**
This indicator is a component of the "Hospital access" (or "Service access") domain, which feeds into the **(In)ability to Recover** dimension of the socio-spatial vulnerability indices, particularly with respect to heatwaves. 

The underlying assumption is that communities with higher travel times to the nearest hospital by car are more socially vulnerable. During extreme weather events, residents may suffer from severe health impacts (such as heat stress) and require rapid medical assistance. A relative lack of proximity to emergency medical help significantly hinders a community's capacity to access this vital assistance and recover successfully.

**Interpretation:**
Because this metric is presented as a standardized Z-score, it evaluates how a specific neighbourhood compares to the overall average across England:
*   **Positive values (High scores):** Denote areas with *longer* travel times to a hospital by car compared to the national average. This indicates poorer access to emergency medical support and translates to **higher social vulnerability**.
*   **Negative values (Low scores):** Denote areas with *shorter* travel times to a hospital by car compared to the average, indicating better, quicker access to emergency medical care and therefore **lower social vulnerability**.

**Data Source:**
For the 2022 England LSOA dataset, the underlying data used to calculate this standardized score is derived from the Department for Transport's Journey Time Statistics 2017 (specifically, Table JTS0506: Travel time, destination and origin indicators for Hospitals by mode of travel, Lower Super Output Area).