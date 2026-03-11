### Number of GPs within 15 minutes by car (Z-Score)

**Description:**
This field (identified internally as `ZGPs15minCar` in the spatial dataset) represents the standardized score (Z-score) of the estimated number of General Practitioner (GP) surgeries that can be reached within a 15-minute journey by car from a given Lower Super Output Area (LSOA).

**Vulnerability Context:**
This indicator is a component of the "GP Access" (or "Service access") domain, which feeds into the **(In)ability to Recover** dimension of the socio-spatial vulnerability indices. 

The underlying assumption is that communities with fewer GPs within a short driving distance are more socially vulnerable. During extreme weather events, such as severe heatwaves, timely access to primary medical care is critical for recovering from health impacts like heat stress. Neighbourhoods with fewer proximate GPs have a lower capacity to access this necessary medical help.

**Interpretation:**
Crucially, because this field measures the *abundance* of a resource (the number of GPs) rather than a deficit, its interpretation is the inverse of most other vulnerability indicators in the dataset:
*   **Positive values (High scores):** Denote an area with a *higher* number of accessible GPs by car compared to the national average. Because having more nearby GPs means better medical access, higher values for this specific indicator represent **lower social vulnerability**.
*   **Negative values (Low scores):** Denote an area with a *lower* number of accessible GPs compared to the average. This relative lack of proximate medical support indicates **higher social vulnerability**.

**Data Source:**
For the 2022 England LSOA dataset, the underlying data used to calculate this standardized score is derived from the Department for Transport's Journey Time Statistics 2017 (specifically, Table JTS0505: Travel time, destination and origin indicators for GPs by mode of travel, Lower Super Output Area).