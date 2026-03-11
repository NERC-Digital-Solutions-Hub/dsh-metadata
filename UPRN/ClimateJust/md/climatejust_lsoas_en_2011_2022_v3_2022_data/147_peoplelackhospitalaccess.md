### People lacking easy hospital access (%)

**Description:**
This field (identified internally as `PeopleLackHospitalAccess` in the spatial dataset) represents the raw estimated percentage of the local population that lacks easy access to a hospital within a given Lower Super Output Area (LSOA). This typically captures the proportion of the "at-risk" population (such as those without access to a private car) who live more than 30 minutes away from the nearest hospital by walking or public transport.

**Vulnerability Context:**
This indicator is a component of the "Hospital Access" (or "Service access") domain, which feeds into the **(In)ability to Recover** dimension of the socio-spatial vulnerability indices. 

The core assumption behind this metric is that communities with higher proportions of people lacking easy access to a hospital are more socially vulnerable. During and after extreme weather events, such as heatwaves or floods, residents may suffer from severe health impacts and require emergency medical assistance. A lack of easy access to a hospital significantly limits a community's capacity to obtain this vital help and successfully recover.

**Interpretation:**
Because this field measures the absolute percentage of people experiencing a deficit in emergency service access, it is interpreted as follows:
*   **High values:** Denote a high percentage of the area's population lacking easy access to a hospital. This indicates poorer accessibility to emergency medical support, translating to **higher social vulnerability**.
*   **Low values:** Denote a low percentage of people lacking easy access. This indicates better, more reliable access to emergency medical care and, therefore, **lower social vulnerability**.

**Data Source:**
For the 2022 England LSOA dataset update, the data used for this indicator is derived from the Department for Transport's Journey Time Statistics 2017 (specifically, Table JTS0506: Travel time, destination and origin indicators for Hospitals by mode of travel, Lower Super Output Area, England).