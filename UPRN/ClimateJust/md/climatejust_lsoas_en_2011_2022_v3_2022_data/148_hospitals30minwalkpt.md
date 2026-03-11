### Number of hospitals within 30 minutes by walk/public transport

**Description:**
This field (identified internally as `Hospitals30minWalkPT` in the spatial dataset) represents the estimated absolute number of hospitals that can be reached within a 30-minute journey by walking or using public transport from a given Lower Super Output Area (LSOA).

**Vulnerability Context:**
This indicator is a component of the "Service access" (or "Hospital access") domain, which feeds into the **(In)ability to Recover** dimension of the socio-spatial climate vulnerability indices, particularly with respect to extreme heat. 

The underlying assumption for this metric is that communities with lower numbers of hospitals within a 30-minute travel radius by foot or public transport are more socially vulnerable. During extreme weather events, timely access to emergency medical care is critical. Neighbourhoods with fewer proximate hospitals have a lower capacity to access this necessary medical help and recover from severe health impacts.

**Interpretation:**
Crucially, because this field measures the absolute *availability* of a positive resource (the actual number of accessible hospitals) rather than a deficit or negative condition, its interpretation is the **inverse** of most other vulnerability indicators in the dataset:
*   **High values:** Denote an area with a high number of accessible hospitals. Because having more nearby hospitals means better emergency medical access, higher values for this specific indicator represent **lower social vulnerability**.
*   **Low values:** Denote an area with few or no accessible hospitals within a 30-minute walk or public transport ride. This relative lack of proximate medical support indicates **higher social vulnerability**.

**Data Source:**
For the 2022 England LSOA dataset update, the data used for this indicator is derived from the Department for Transport's Journey Time Statistics 2017 (specifically, Table JTS0506: Travel time, destination and origin indicators for Hospitals by mode of travel, Lower Super Output Area, England).