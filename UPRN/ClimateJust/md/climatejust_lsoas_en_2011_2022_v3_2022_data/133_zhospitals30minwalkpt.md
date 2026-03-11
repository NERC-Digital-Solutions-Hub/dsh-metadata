### Number of hospitals within 30 minutes by walk/public transport (Z-Score)

**Description:**
This field (identified internally as `ZHospitals30minWalkPT` in the spatial dataset) represents the standardized score (Z-score) of the estimated number of hospitals that can be reached within a 30-minute journey by walking or using public transport from a given Lower Super Output Area (LSOA). 

**Vulnerability Context:**
This indicator is a component of the "Hospital Access" (or "Service access") domain, which feeds into the **(In)ability to Recover** dimension of the socio-spatial vulnerability indices, particularly with respect to heatwaves. 

The underlying assumption is that communities with a lower number of hospitals within a 30-minute travel radius by foot or public transport are more socially vulnerable. During extreme weather events, timely access to emergency medical care is critical. Neighbourhoods with fewer proximate hospitals have a lower capacity to access this necessary medical help and recover from severe health impacts.

**Interpretation:**
Because this field measures the *availability* of a positive resource (the number of hospitals) rather than a deficit or negative condition, its interpretation is the **inverse** of most other vulnerability indicators in the dataset:
*   **Positive values (High scores):** Denote an area with a *higher* number of accessible hospitals within 30 minutes compared to the national average. Because having more nearby hospitals means better medical access, higher values for this specific indicator represent **lower social vulnerability**.
*   **Negative values (Low scores):** Denote an area with a *lower* number of accessible hospitals compared to the average. This relative lack of proximate medical support indicates **higher social vulnerability**.

**Data Source:**
For the 2022 England LSOA dataset update, the underlying data used to calculate this standardized score is derived from the Department for Transport's Journey Time Statistics 2017 (specifically, Table JTS0506: Travel time, destination and origin indicators for Hospitals by mode of travel, Lower Super Output Area, England).