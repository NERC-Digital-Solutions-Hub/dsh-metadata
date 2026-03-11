### Travel time to nearest GP by walk/public transport (minutes)

**Description:**
This field (identified internally in the spatial dataset under names such as `TravelTimeToGPWalkPT`) represents the estimated absolute travel time, in minutes, required to reach the nearest General Practitioner (GP) surgery by walking or using public transport from a given Lower Super Output Area (LSOA).

**Vulnerability Context:**
This indicator is a key component of the "GP Access" (or "Service access") domain, which feeds into the **(In)ability to Recover** dimension of the socio-spatial vulnerability indices, particularly concerning extreme heat. 

The core assumption behind this metric is that people living in areas with higher travel times to the nearest GP by foot or public transport are more socially vulnerable. Physical isolation or a lack of mobility to reach primary medical help quickly can be a critical factor during and after extreme weather events (such as severe heatwaves), as it significantly hinders a community's capacity to access the vital medical assistance needed to recover from health impacts.

**Interpretation:**
Unlike its standardized Z-score counterpart, this field provides the raw travel time in minutes. It is interpreted as follows:
*   **High values (Longer times):** Denote areas requiring *longer* journeys to reach a GP without a private car. This indicates poorer accessibility to medical support, translating to **higher social vulnerability**.
*   **Low values (Shorter times):** Denote areas with *shorter* travel times to a GP. This indicates quicker, more reliable access to primary medical care, translating to **lower social vulnerability**.

**Data Source:**
For the 2022 England LSOA dataset update, the data for this indicator is derived from the Department for Transport's Journey Time Statistics 2017 (specifically, Table JTS0505: Travel time, destination and origin indicators for GPs by mode of travel, Lower Super Output Area).