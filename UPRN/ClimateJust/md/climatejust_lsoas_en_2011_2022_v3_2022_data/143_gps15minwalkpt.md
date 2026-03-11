### Number of GPs within 15 minutes by walk/public transport

**Description:**
This field (identified internally as `GPs15minWalkPT` in the spatial dataset) represents the estimated absolute number of General Practitioner (GP) surgeries that can be reached within a 15-minute journey by walking or using public transport from a given Lower Super Output Area (LSOA).

**Vulnerability Context:**
This indicator is a component of the "GP Access" (or "Service access") domain, which feeds into the **(In)ability to Recover** dimension of the socio-spatial heat vulnerability index. 

The underlying assumption for this metric is that communities with lower numbers of GPs within a short 15-minute travel distance by foot or public transport are more socially vulnerable. During extreme weather events such as severe heatwaves, immediate access to primary medical care is critical for recovering from health impacts. Neighbourhoods with fewer proximate GPs have a lower capacity to quickly access this necessary medical help.

**Interpretation:**
Crucially, because this field measures the absolute *availability* of a positive resource (the actual number of GPs) rather than a deficit or negative condition, its interpretation is the **inverse** of most other vulnerability indicators in the dataset:
*   **High values:** Denote an area with a high number of accessible GPs. Because having more nearby GPs means better medical access, higher values for this specific indicator represent **lower social vulnerability**.
*   **Low values:** Denote an area with few or no accessible GPs within 15 minutes. This relative lack of proximate medical support indicates **higher social vulnerability**.

**Data Source:**
For the 2022 England LSOA dataset update, the data used for this indicator is derived from the Department for Transport's Journey Time Statistics 2017 (specifically, Table JTS0505: Travel time, destination and origin indicators for GPs by mode of travel, Lower Super Output Area, England).