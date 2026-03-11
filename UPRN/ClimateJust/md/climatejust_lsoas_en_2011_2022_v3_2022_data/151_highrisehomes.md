### High rise homes (% households with lowest floor 5th floor or above)

**Description:**
This field (identified internally as `HighRiseHomes` in the spatial dataset) represents the raw percentage of households whose lowest floor is situated on the 5th floor or higher within a given Lower Super Output Area (LSOA). 

**Vulnerability Context:**
This indicator is a key component of the **Housing characteristics** domain, which feeds into the **Enhanced Exposure** dimension of the socio-spatial heat vulnerability indices. 

The underlying assumption is that residential dwellings located in the upper levels of tower blocks or multi-storey flats are significantly more likely to overheat and be adversely affected by high temperatures during severe heatwaves compared to ground-level or alternative types of accommodation. Consequently, a high density of these housing types in a neighbourhood physically accentuates the severity of extreme heat exposure for its residents, increasing their overall vulnerability.

**Interpretation:**
Unlike its standardized Z-score counterpart, this field provides the absolute percentage rate for the neighbourhood:
*   **High values:** Denote an area with a high percentage of households living on the 5th floor or above. This points to a built environment that accentuates heat exposure, translating to **higher social vulnerability**.
*   **Low values:** Denote an area with a lower percentage of high-rise homes, indicating an environment less prone to this specific housing-related heat risk, thereby translating to **lower social vulnerability**.

**Data Source:**
For the 2022 England LSOA dataset update, the data used to calculate this indicator is derived from the Office for National Statistics (ONS) dataset: "Access to public green space in Great Britain". *(Note: In older versions of the ClimateJust dataset, this was derived directly from 2001 Census data, but it has been updated for the 2022 release).*