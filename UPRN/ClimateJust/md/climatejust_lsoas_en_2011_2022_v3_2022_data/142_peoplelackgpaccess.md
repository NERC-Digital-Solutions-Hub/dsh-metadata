### People lacking easy GP access (%)

**Description:**
This field (identified internally as `PeopleLackGPAccess` in the spatial dataset) represents the raw percentage of the local population that lacks easy access to a General Practitioner (GP) within a given Lower Super Output Area (LSOA). This typically captures the proportion of the at-risk population (such as those without access to a private car) who live more than 15 minutes away from the nearest GP by walking or public transport.

**Vulnerability Context:**
This indicator is a component of the "GP Access" (or "Service access") domain, which feeds into the **(In)ability to Recover** dimension of the socio-spatial heat vulnerability index. 

The core assumption behind this metric is that communities with higher proportions of people lacking easy access to primary medical care are more socially vulnerable. During and after extreme weather events, such as heatwaves, residents may suffer from health impacts (like heat stress) and require rapid medical assistance. A lack of easy access to a GP significantly limits a community's capacity to obtain medical help and successfully recover.

**Interpretation:**
Because this field measures the absolute percentage of people experiencing a deficit in service access, it is interpreted as follows:
*   **High values:** Denote a high percentage of the area's population lacking easy access to a GP. This indicates poorer accessibility to medical support, translating to **higher social vulnerability**.
*   **Low values:** Denote a low percentage of people lacking easy access. This indicates better, more reliable access to primary medical care and, therefore, **lower social vulnerability**.

**Data Source:**
For the 2022 England LSOA dataset update, the data for this indicator is derived from the Department for Transport's Journey Time Statistics 2017 (specifically, Table JTS0505: Travel time, destination and origin indicators for GPs by mode of travel, Lower Super Output Area, England).