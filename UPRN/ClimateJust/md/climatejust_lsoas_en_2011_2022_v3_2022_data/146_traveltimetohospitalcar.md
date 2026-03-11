### Travel time to nearest hospital by car (minutes)

**Description:**
This field (identified internally as `TravelTimeToHospitalCar` in the spatial dataset) represents the absolute estimated travel time, in minutes, required to reach the nearest hospital by private car from a given Lower Super Output Area (LSOA).

**Vulnerability Context:**
This indicator is a component of the "Hospital Access" (or "Service access") domain, which feeds into the **(In)ability to Recover** dimension of the socio-spatial climate vulnerability indices. 

The core assumption behind this metric is that communities with higher travel times to the nearest hospital are more socially vulnerable. During extreme weather events such as severe heatwaves, residents may suffer from serious health impacts (like heat stress) and require rapid medical assistance. A relative lack of proximity to emergency medical help significantly hinders a community's capacity to access this vital assistance and successfully recover.

**Interpretation:**
Unlike its standardized Z-score counterpart, this field provides the raw travel time in minutes. It is interpreted as follows:
*   **High values (Longer times):** Denote areas requiring *longer* journeys to reach a hospital by car. This indicates poorer accessibility to emergency medical support, translating to **higher social vulnerability**.
*   **Low values (Shorter times):** Denote areas with *shorter* travel times to a hospital. This indicates quicker, more reliable access to emergency medical care, translating to **lower social vulnerability**.

**Data Source:**
For the 2022 England LSOA dataset update, the data for this indicator is derived from the Department for Transport's Journey Time Statistics 2017 (specifically, Table JTS0506: Travel time, destination and origin indicators for Hospitals by mode of travel, Lower Super Output Area, England).